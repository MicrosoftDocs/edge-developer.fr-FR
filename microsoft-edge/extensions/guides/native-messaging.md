---
description: Apprenez-en davantage sur la façon dont vous pouvez utiliser la messagerie native pour que votre extension puisse communiquer avec une application UWP.
title: Extensions-messagerie Native
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur, natif, messagerie, UWP
ms.openlocfilehash: 83f80e112180317c38763225c1cdd015da4238b0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565343"
---
# <span data-ttu-id="67198-104">Messagerie native dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="67198-104">Native messaging in Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <span data-ttu-id="67198-105">Présentation de l’architecture de messagerie Native</span><span class="sxs-lookup"><span data-stu-id="67198-105">Native messaging architecture overview</span></span>

<span data-ttu-id="67198-106">Avec Windows 10 Creators Update, les extensions Microsoft Edge peuvent utiliser la messagerie native pour communiquer avec une application de plateforme Windows universelle (UWP) complémentaire.</span><span class="sxs-lookup"><span data-stu-id="67198-106">With the Windows 10 Creators Update, Microsoft Edge extensions are able to use native messaging to communicate with a companion Universal Windows Platform (UWP) app.</span></span>  <span data-ttu-id="67198-107">À un niveau élevé, les extensions Microsoft Edge utilisent les mêmes API pour la messagerie Native que les extensions chrome et Firefox.</span><span class="sxs-lookup"><span data-stu-id="67198-107">At a high level, Microsoft Edge extensions use the same APIs for native messaging as Chrome and Firefox extensions.</span></span> <span data-ttu-id="67198-108">Toutefois, l’hôte de messagerie natif doit être implémenté à l’aide de la plateforme Windows universelle.</span><span class="sxs-lookup"><span data-stu-id="67198-108">However, the native messaging host will need to be implemented using the Universal Windows Platform.</span></span>

> [!NOTE]
> <span data-ttu-id="67198-109">La méthode décrite ci-dessous (la connexion à une application UWP via AppService) est le seul mécanisme pris en charge pour l’activation de la communication entre les extensions Microsoft Edge et les composants natifs.</span><span class="sxs-lookup"><span data-stu-id="67198-109">The method outlined below (connecting to a UWP app via AppService) is the only supported mechanism for enabling communication between Microsoft Edge extensions and native components.</span></span> <span data-ttu-id="67198-110">Pour plus d’informations sur l’activation de la communication avec les anciens composants Win32, voir la section [Ajout d’un composant Desktop Bridge](#adding-a-desktop-bridge-component) de ce guide.</span><span class="sxs-lookup"><span data-stu-id="67198-110">Please see the [Adding a Desktop Bridge component](#adding-a-desktop-bridge-component) section of this guide for more information on how to enable communication with legacy Win32 components.</span></span> 

 <span data-ttu-id="67198-111">L’architecture de messagerie native de Microsoft Edge tire parti de l' [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API existante en tant qu’infrastructure de communication entre processus (IPC) sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="67198-111">Microsoft Edge's native messaging architecture leverages the existing [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API as the underlying inter-process communication (IPC) infrastructure.</span></span> <span data-ttu-id="67198-112">Les applications UWP utilisent l' `AppService` API pour communiquer entre elles.</span><span class="sxs-lookup"><span data-stu-id="67198-112">UWP apps use the `AppService` API to communicate with one another.</span></span> <span data-ttu-id="67198-113">Pour cette raison, les extensions Microsoft Edge peuvent désormais communiquer avec des applications UWP.</span><span class="sxs-lookup"><span data-stu-id="67198-113">Because of this, Microsoft Edge extensions can now communicate with UWP apps.</span></span>

![architecture de messagerie Native](./../media/native-messaging-architecture.png)


### <span data-ttu-id="67198-115">Quand et quand ne pas utiliser la messagerie Native</span><span class="sxs-lookup"><span data-stu-id="67198-115">When and when not to use native messaging</span></span>

<span data-ttu-id="67198-116">La messagerie Native ajoute un nouveau calque à votre extension.</span><span class="sxs-lookup"><span data-stu-id="67198-116">Native messaging adds a whole new layer to your extension.</span></span> <span data-ttu-id="67198-117">En implémentant une application complémentaire UWP pour votre extension, les possibilités suivantes sont disponibles:</span><span class="sxs-lookup"><span data-stu-id="67198-117">By implementing a UWP companion app for your extension, the following possibilities become available to you:</span></span>

* <span data-ttu-id="67198-118">Synchroniser des données (par exemple, des informations d’identification) avec une application UWP complémentaire.</span><span class="sxs-lookup"><span data-stu-id="67198-118">Synchronize data (e.g. credentials) with a companion UWP app.</span></span>
* <span data-ttu-id="67198-119">Les algorithmes de déchiffrement/déchiffrement renforcés ne sont pas disponibles dans les API Web.</span><span class="sxs-lookup"><span data-stu-id="67198-119">Implement stronger encryption/decryption algorithms not available in web APIs.</span></span>
* <span data-ttu-id="67198-120">Accès aux ressources qui ne sont pas accessibles par le biais d’API Web (par exemple, matériel ou périphériques USB);</span><span class="sxs-lookup"><span data-stu-id="67198-120">Access resources that are not accessible through web APIs, e.g. hardware or USB devices</span></span>

<span data-ttu-id="67198-121">Dans certains cas, la messagerie Native ne peut pas être utilisée en raison de restrictions de sécurité ou de stratégie:</span><span class="sxs-lookup"><span data-stu-id="67198-121">There are a few instances where native messaging can't be used due to security or policy restrictions:</span></span>

* <span data-ttu-id="67198-122">Modification des paramètres de l’utilisateur dans Microsoft Edge ou Windows, par exemple, la modification du navigateur par défaut ou du fournisseur de recherche;</span><span class="sxs-lookup"><span data-stu-id="67198-122">Modifying user settings in either Microsoft Edge or Windows, e.g. changing the default browser or search provider.</span></span>
* <span data-ttu-id="67198-123">Actions qui enfreignent les stratégies du Windows Store pour les applications et les extensions.</span><span class="sxs-lookup"><span data-stu-id="67198-123">Actions that violate Microsoft Store policies for both apps and extensions.</span></span>
* <span data-ttu-id="67198-124">Transfert de données vers un point de terminaison distant via un hôte de message natif.</span><span class="sxs-lookup"><span data-stu-id="67198-124">Transferring data to remote endpoint via native message host.</span></span>
* <span data-ttu-id="67198-125">Autorisation d’autres applications de télécharger le contenu qui modifie le comportement de l’extension.</span><span class="sxs-lookup"><span data-stu-id="67198-125">Allowing other apps to download content that changes extension behavior.</span></span>

## <span data-ttu-id="67198-126">Démos</span><span class="sxs-lookup"><span data-stu-id="67198-126">Demos</span></span>

<span data-ttu-id="67198-127">Pour avoir un aperçu de ce qu’est une extension de messagerie Native Microsoft Edge qui comporte à la fois une application UWP complémentaire et une application de bureau, consultez les exemples [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) et [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="67198-127">To get a feel for what an Microsoft Edge native messaging extension that has both a companion UWP app and a Desktop Bridge looks like, check out the [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) and [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) examples on GitHub.</span></span>

### <span data-ttu-id="67198-128">Fonctionnement</span><span class="sxs-lookup"><span data-stu-id="67198-128">How it works</span></span>

<span data-ttu-id="67198-129">Le composant d’extension Microsoft Edge de l’exemple utilise son script de contenu pour détecter lorsqu’un utilisateur tape des informations qui doivent être chiffrées.</span><span class="sxs-lookup"><span data-stu-id="67198-129">The Microsoft Edge extension component of the sample uses its content script to detect when a user is typing in information that should be encrypted.</span></span> <span data-ttu-id="67198-130">L’extension communique cela au composant Desktop Bridge par le biais de la messagerie native.</span><span class="sxs-lookup"><span data-stu-id="67198-130">The extension communicates this to the Desktop Bridge component via native messaging.</span></span> <span data-ttu-id="67198-131">Lorsque l’utilisateur est prêt à envoyer les données, l’extension renverra une valeur chiffrée au site Web.</span><span class="sxs-lookup"><span data-stu-id="67198-131">When the user is ready to submit the data, the extension will return an encrypted value back to the website.</span></span>

> [!NOTE]
> <span data-ttu-id="67198-132">Cet exemple ne fonctionne que sur une page Web qui utilise des événements personnalisés pour communiquer avec le script de contenu de l’extension.</span><span class="sxs-lookup"><span data-stu-id="67198-132">This sample will only work on a webpage that uses custom events to communicate with the extension's content script.</span></span> <span data-ttu-id="67198-133">L’exemple de dossier inclut un [fichier. html](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) pour tester l’extension.</span><span class="sxs-lookup"><span data-stu-id="67198-133">The sample folder includes a [.html file](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) to test the extension with.</span></span>

<span data-ttu-id="67198-134">Dans cet exemple, l’application UWP est utilisée pour passer les réponses de Desktop Bridge à Microsoft Edge, qui est ensuite envoyée à l’extension Microsoft Edge via le rappel.</span><span class="sxs-lookup"><span data-stu-id="67198-134">In this example, the UWP app is used to pass responses from the Desktop Bridge to Microsoft Edge, which then gets sent to the Microsoft Edge extension via callback.</span></span> <span data-ttu-id="67198-135">Dans cet exemple, l’hôte de messagerie natif s’exécute dans l’application principale, il peut également être exécuté en tant que tâche en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="67198-135">While this example has the native messaging host run in the main app, it's also able to run as a background task.</span></span> <span data-ttu-id="67198-136">Le passage de l’un à l’autre nécessite la modification du script en arrière-plan de l’extension, en modifiant la chaîne à l’intérieur `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` de `"NativeMessagingHostOutOfProcess"` .</span><span class="sxs-lookup"><span data-stu-id="67198-136">Switching between the two requires editing the extension's background script, changing the string within `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` to `"NativeMessagingHostOutOfProcess"`.</span></span>

## <span data-ttu-id="67198-137">Implémentation de chrome et de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="67198-137">Chrome vs Microsoft Edge implementation</span></span>

<span data-ttu-id="67198-138">Lorsque chrome passe l’itinéraire d’utilisation des API de passage de messages pour leurs extensions de communication avec les applications, Microsoft Edge utilise l' [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API qui permet à l’application Microsoft Edge extensions et aux applications UWP de communiquer.</span><span class="sxs-lookup"><span data-stu-id="67198-138">While Chrome goes the route of using message passing APIs for their extensions to communicate with apps, Microsoft Edge utilizes the [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API which now enables Microsoft Edge extensions and UWP apps to communicate.</span></span>

<span data-ttu-id="67198-139">Cette section décrit en détail les différences qui existent entre le mode chrome et Microsoft Edge et la mise en œuvre de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="67198-139">This section details the differences between how Chrome and Microsoft Edge handle native messaging implementation.</span></span>

### <span data-ttu-id="67198-140">Inscription et manifeste d’hébergement</span><span class="sxs-lookup"><span data-stu-id="67198-140">Registration and host manifest</span></span>
<span data-ttu-id="67198-141">Pour que votre application soit reconnue par votre extension en tant qu’hôte de messagerie natif, vous devez être inscrite.</span><span class="sxs-lookup"><span data-stu-id="67198-141">In order for your app to be recognized by your extension as a native messaging host, it will need to be registered.</span></span>


<span data-ttu-id="67198-142">Pour l’inscription de l’hôte de [messagerie natif de chrome](https://developer.chrome.com/extensions/nativeMessaging) , votre application doit installer un fichier manifeste en tout lieu dans le système de fichiers Windows qui définit la configuration hôte de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="67198-142">For [Chrome native messaging](https://developer.chrome.com/extensions/nativeMessaging) host registration, your app needs to install a manifest file anywhere in the Windows file system that defines the native messaging host configuration.</span></span>

<span data-ttu-id="67198-143">Le code JSON suivant est un exemple de la façon dont le fichier de configuration peut être configuré:</span><span class="sxs-lookup"><span data-stu-id="67198-143">The following JSON is an example of how the config file can be set up:</span></span>

```json
{
   "name": "com.my_company.my_application",
   "description": "My Application",
   "path": "C:\\ProgramFiles\\MyApplication\\chrome_native_messaging_host.exe",
   "type": "stdio",
   "allowed_origins": [
      "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
    ]
}
```

<span data-ttu-id="67198-144">Pour installer ce fichier, l’application doit effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="67198-144">To install this file, the app would need to:</span></span>

1. <span data-ttu-id="67198-145">Enregistrez le fichier manifeste dans un emplacement prédéfini du Registre qui définit la configuration d’hôte:</span><span class="sxs-lookup"><span data-stu-id="67198-145">Register the manifest file in a predefined location in the registry that defines the host configuration:</span></span>
   - `HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`

     <span data-ttu-id="67198-146">ou</span><span class="sxs-lookup"><span data-stu-id="67198-146">or</span></span>
   - `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`

2. <span data-ttu-id="67198-147">Définissez la valeur par défaut de cette clé sur le chemin d’accès complet au fichier manifeste (par exemple,</span><span class="sxs-lookup"><span data-stu-id="67198-147">Set the default value of that key to the full path to the manifest file, e.g.</span></span>  `[HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"`




<span data-ttu-id="67198-148">Pour Microsoft Edge, afin d’inscrire un [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) (hôte de messagerie natif), vous devez inclure l’application compagnon UWP dans le même package que votre extension et spécifier l' [extension AppService](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) dans le fichier de votre projet `Package.appxmanifest` .</span><span class="sxs-lookup"><span data-stu-id="67198-148">For Microsoft Edge, in order to register an [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx)(native messaging host) you'll need to include the UWP companion app in the same package as your extension and specify the [AppService extension](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) in your project's `Package.appxmanifest` file.</span></span> <span data-ttu-id="67198-149">Les `EntryPoint` `Name` attributs et peuvent être configurés comme suit:</span><span class="sxs-lookup"><span data-stu-id="67198-149">The `EntryPoint` and `Name` attributes can be configured by you:</span></span>

```xml
...
<Applications>    
    <Application Id="App"         
        <Extensions>        
            <uap:Extension Category="windows.appService" EntryPoint="MyAppService.Inventory">          
            <uap:AppService Name="com.microsoft.inventory"/>        
            </uap:Extension>      
        </Extensions>      
        ...    
    </Application>
</Applications>
```


<span data-ttu-id="67198-150">Vous devez également définir quelles extensions sont autorisées à se connecter au service.</span><span class="sxs-lookup"><span data-stu-id="67198-150">You'll also need to set which extension(s) are allowed to connect to the service.</span></span> <span data-ttu-id="67198-151">Dans la mesure où Microsoft Edge ne possède pas `"allowed_origins"` de propriété de manifeste équivalente dans son AppxManifest, il doit être déterminé et appliqué lors de l’exécution par votre application UWP.</span><span class="sxs-lookup"><span data-stu-id="67198-151">Because Microsoft Edge doesn't have an equivalent `"allowed_origins"` manifest property in its AppxManifest, this will need to be determined and enforced at runtime by your UWP app.</span></span> <span data-ttu-id="67198-152">Dans la mesure où Microsoft Edge établit la connexion de la part de l’extension, l’application peut chercher le nom de la famille de packages de l’appelant afin de déterminer s’il est connecté par Microsoft Edge pour contrôler ou authentifier l’appelant.</span><span class="sxs-lookup"><span data-stu-id="67198-152">Since Microsoft Edge will be establishing the connection on behalf of the extension, the app can look up the caller's Package Family Name to determine if they're being connected by Microsoft Edge to control or authenticate the caller.</span></span> <span data-ttu-id="67198-153">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="67198-153">E.g.</span></span> 

```csharp
protected async override void
OnBackgroundActivated(BackgroundActivatedEventArgs args)
{
    IBackgroundTaskInstance taskInstance = args.TaskInstance;
    if (taskInstance.TriggerDetails is AppServiceTriggerDetails)
    {
        AppServiceTriggerDetails appService = taskInstance.TriggerDetails as AppServiceTriggerDetails;
        if (appService.CallerPackageFamilyName == EdgePFN)
        {
            // Establish the connection
        }
        else
        {
            // Reject the connection
        }
    }
}
```



### <span data-ttu-id="67198-154">Envoi de messages</span><span class="sxs-lookup"><span data-stu-id="67198-154">Message sending</span></span>

<span data-ttu-id="67198-155">Pour qu’une application et une extension puissent communiquer entre elles, les messages doivent être envoyés vers et à partir de celles-ci.</span><span class="sxs-lookup"><span data-stu-id="67198-155">For an app and an extension to communicate with one another, messages need to be sent to and from them.</span></span>

<span data-ttu-id="67198-156">Les extensions chrome déclenchent un message à l’aide de l' [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API pour envoyer un message à l’hôte natif à l’aide d’un canal non persistant.</span><span class="sxs-lookup"><span data-stu-id="67198-156">Chrome extensions initiate a message using the [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API to deliver a message to the native host using a non-persistent channel.</span></span> 

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```

<span data-ttu-id="67198-157">Le premier paramètre est le nom de l’hôte natif, lequel recherche chrome dans le registre pour le manifeste.</span><span class="sxs-lookup"><span data-stu-id="67198-157">The first parameter is the name of the native host, which Chrome looks up in the registry for the manifest.</span></span> <span data-ttu-id="67198-158">Le manifeste spécifie le fichier. exe dans lequel le chrome sera lancé dans un bac à sable (sandbox), et le message est envoyé à l’aide du standard d’e/s.</span><span class="sxs-lookup"><span data-stu-id="67198-158">The manifest specifies the .exe that Chrome will launch in a sandbox, and the message is sent using std i/o.</span></span> <span data-ttu-id="67198-159">Les extensions peuvent également établir un canal permanent à l’aide de l' `runtime.connectNative` API, qui prend le nom de l’hôte natif en tant que paramètre unique.</span><span class="sxs-lookup"><span data-stu-id="67198-159">Extensions can also establish a persistent channel using the `runtime.connectNative` API, which takes the name of the native host as the only parameter.</span></span> 

<span data-ttu-id="67198-160">Microsoft Edge utilise la même construction que l’API de messagerie native de chrome pour autoriser les extensions Microsoft Edge à spécifier le service d’application auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="67198-160">Microsoft Edge uses the same construct as Chrome's native messaging API to allow Microsoft Edge extensions to specify which app service to connect to.</span></span> <span data-ttu-id="67198-161">Le premier paramètre de `runtime.sendNativeMessage` spécifie le nom du service d’application.</span><span class="sxs-lookup"><span data-stu-id="67198-161">The first parameter in `runtime.sendNativeMessage` specifies the app service name.</span></span> <span data-ttu-id="67198-162">Dans la section [inscription et manifeste](#registration-and-host-manifest) de l’hôte, il s’agit de `"com.microsoft.inventory"` .</span><span class="sxs-lookup"><span data-stu-id="67198-162">In the [Registration and host manifest](#registration-and-host-manifest) section, this is `"com.microsoft.inventory"`.</span></span> <span data-ttu-id="67198-163">La plateforme d’extension Microsoft Edge limite l’hôte de messagerie natif à être une application UWP empaquetée dans le même AppX que l’extension.</span><span class="sxs-lookup"><span data-stu-id="67198-163">The Microsoft Edge extension platform restricts the native messaging host to being a UWP app that is packaged in the same AppX as the extension.</span></span> <span data-ttu-id="67198-164">Cela permet de réduire les risques liés à la sécurité liés aux attaques malveillantes qui essaient de connecter Microsoft Edge avec un autre nom de la famille de packages en falsifiant des entrées de manifeste.</span><span class="sxs-lookup"><span data-stu-id="67198-164">This mitigates any security risks associated with malicious attacks that try to connect Microsoft Edge with another Package Family Name by tampering with manifest entries.</span></span> 

<span data-ttu-id="67198-165">Cela signifie que Microsoft Edge utilisera le même nom de famille de packages que l’extension, en plus du `AppService` nom spécifié dans l’API, pour identifier de manière unique le fournisseur de service d’application.</span><span class="sxs-lookup"><span data-stu-id="67198-165">This means that Microsoft Edge will use the same Package Family Name as the extension, in addition to the `AppService` name specified in the API, to uniquely identify the provider of the app service.</span></span>  

> [!NOTE]
> <span data-ttu-id="67198-166">Le [Kit de connaissances Microsoft Edge extension](./porting-chrome-extensions.md)ne sera pas facilement converti.</span><span class="sxs-lookup"><span data-stu-id="67198-166">This will not be easily converted by the [Microsoft Edge Extension Toolkit](./porting-chrome-extensions.md).</span></span> <span data-ttu-id="67198-167">Toute extension spécifiant l' `"nativeMessaging"` autorisation sera signalée comme nécessitant une conversion manuelle pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="67198-167">Any extensions that specifies the `"nativeMessaging"` permission will be flagged as requiring manual conversion for this component.</span></span>





### <span data-ttu-id="67198-168">Protocole de communication</span><span class="sxs-lookup"><span data-stu-id="67198-168">Communication protocol</span></span>

<span data-ttu-id="67198-169">Le protocole de communication pour la messagerie Native détermine le mode de mise en forme des messages avant leur envoi.</span><span class="sxs-lookup"><span data-stu-id="67198-169">Communication protocol for native messaging determines how messages are formatted before sending.</span></span>

<span data-ttu-id="67198-170">Chrome démarre chaque hôte de messagerie natif dans un processus distinct et communique avec ce dernier à l’aide d’une entrée standard et d’une sortie standard.</span><span class="sxs-lookup"><span data-stu-id="67198-170">Chrome starts each native messaging host in a separate process and communicates with it using standard input and standard output.</span></span> <span data-ttu-id="67198-171">Le même format est utilisé pour envoyer des messages dans les deux sens: chaque message est sérialisé en utilisant JSON, UTF-8 encodé et est précédé d’une longueur de message de 32 bits dans l’ordre d’octets natif.</span><span class="sxs-lookup"><span data-stu-id="67198-171">The same format is used to send messages in both directions: each message is serialized using JSON, UTF-8 encoded and is preceded with 32-bit message length in native byte order.</span></span>


<span data-ttu-id="67198-172">Pour Microsoft Edge, la tâche en arrière-plan/l’application principale qui implémente le service d’application est démarrée par la plateforme.</span><span class="sxs-lookup"><span data-stu-id="67198-172">For Microsoft Edge, the background task/main app that implements the app service will be started by the platform.</span></span> <span data-ttu-id="67198-173">Au démarrage, la méthode de la tâche en arrière-plan est `Run` appelée:</span><span class="sxs-lookup"><span data-stu-id="67198-173">On startup, the background task's `Run` method will be invoked:</span></span>  

```csharp
public void Run(IBackgroundTaskInstance taskInstance)    
{
    this.backgroundTaskDeferral = taskInstance.GetDeferral();
    // Get a deferral so that the service isn't terminated.
    taskInstance.Canceled += OnTaskCanceled;
    // Associate a cancellation handler with the background task.
    // Retrieve the app service connection and set up a listener for incoming app service requests.
    var details = taskInstance.TriggerDetails as AppServiceTriggerDetails;
    appServiceconnection = details.AppServiceConnection;
    appServiceconnection.RequestReceived += OnRequestReceived;
}
```

<span data-ttu-id="67198-174">Lorsque votre extension envoie un message à votre application UWP, l' [`onRequestReceived`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection.requestreceived) événement est déclenché.</span><span class="sxs-lookup"><span data-stu-id="67198-174">When your extension sends a message to your UWP app, the [`onRequestReceived`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection.requestreceived) event will be raised.</span></span> <span data-ttu-id="67198-175">Ce message au format JSON sera alors stringified dans le premier couple KeyValue d’un [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) objet.</span><span class="sxs-lookup"><span data-stu-id="67198-175">This JSON formatted message will then be stringified into the first KeyValue pair of a [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) object.</span></span> <span data-ttu-id="67198-176">:</span><span class="sxs-lookup"><span data-stu-id="67198-176">:</span></span>

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```

<span data-ttu-id="67198-177">Lorsque votre application UWP envoie de nouveau une réponse à votre extension, une [`KeyValuePair`](https://msdn.microsoft.com/library/windows/apps/5tbh8a42) est ajoutée à l' `ValueSet` objet.</span><span class="sxs-lookup"><span data-stu-id="67198-177">When your UWP app sends a response back to your extension, a [`KeyValuePair`](https://msdn.microsoft.com/library/windows/apps/5tbh8a42) will be added to the `ValueSet` object.</span></span> <span data-ttu-id="67198-178">La `Key` propriété est ignorée par Microsoft Edge, mais la `Value` propriété contient une chaîne JSON valide.</span><span class="sxs-lookup"><span data-stu-id="67198-178">The `Key` property will be ignored by Microsoft Edge, but the `Value` property will contain a valid JSON string.</span></span>

### <span data-ttu-id="67198-179">Rappeler</span><span class="sxs-lookup"><span data-stu-id="67198-179">Callback</span></span>

<span data-ttu-id="67198-180">Pour les rappels, chrome utilise [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) ce qui permet à une fonction de rappel de gérer toute réponse asynchrone lors de l’envoi d’un message.</span><span class="sxs-lookup"><span data-stu-id="67198-180">For callbacks, Chrome uses [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) which allows a callback function to handle any asynchronous response from sending a message.</span></span>

<span data-ttu-id="67198-181">Microsoft Edge utilise la [`AppServiceRequest`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest) méthode de l’objet [`SendResponseAsync`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest.sendresponseasync) pour permettre à l’application de renvoyer un [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) objet à l’extension.</span><span class="sxs-lookup"><span data-stu-id="67198-181">Microsoft Edge uses the [`AppServiceRequest`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest) object's [`SendResponseAsync`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest.sendresponseasync) method to let the app send a [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) object back to the extension.</span></span>


### <span data-ttu-id="67198-182">Taille limite du message</span><span class="sxs-lookup"><span data-stu-id="67198-182">Message size limit</span></span>
<span data-ttu-id="67198-183">Les messages échangés entre une extension et une application présentent des limitations de taille de messages différentes pour chrome et Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="67198-183">Messages that are sent back and forth between an extension and an app have different message size limitations in place for Chrome and Microsoft Edge.</span></span>

<span data-ttu-id="67198-184">Chrome a les limites de taille de message suivantes:</span><span class="sxs-lookup"><span data-stu-id="67198-184">Chrome has the following message size limitations:</span></span>
- <span data-ttu-id="67198-185">Limite de messages unique de l’hôte de messagerie natif: 1 Mo</span><span class="sxs-lookup"><span data-stu-id="67198-185">Single message limit from native messaging host: 1 MB</span></span>
- <span data-ttu-id="67198-186">Limite de messages unique envoyée à l’hôte de messagerie natif: 4 Go</span><span class="sxs-lookup"><span data-stu-id="67198-186">Single message limit sent to native messaging host: 4 GB</span></span>

<span data-ttu-id="67198-187">Pour Microsoft Edge, sans `AppService` limite de taille de message (en fonction de la quantité de mémoire), Microsoft Edge se protège lui-même contre les applications natives inefficaces en imposant les limites de taille de message suivantes:</span><span class="sxs-lookup"><span data-stu-id="67198-187">For Microsoft Edge, while `AppService` has no limit on message size (dependent on memory), Microsoft Edge protects itself against misbehaving native apps by imposing the following message size limits:</span></span>
- <span data-ttu-id="67198-188">Limite de messages unique de l’application UWP à l’extension: 1 Mo</span><span class="sxs-lookup"><span data-stu-id="67198-188">Single message limit from UWP app to extension: 1 MB</span></span>
- <span data-ttu-id="67198-189">Limite de messages unique de l’extension à l’application UWP: 100 Mo</span><span class="sxs-lookup"><span data-stu-id="67198-189">Single message limit from extension to UWP app: 100 MB</span></span>



### <span data-ttu-id="67198-190">Connexions de messagerie Native</span><span class="sxs-lookup"><span data-stu-id="67198-190">Native messaging connections</span></span>

<span data-ttu-id="67198-191">Il existe deux types de connexions pour la messagerie Native; persistant et non persistant.</span><span class="sxs-lookup"><span data-stu-id="67198-191">There are two types of connections for native messaging; persistent and non-persistent.</span></span>
<span data-ttu-id="67198-192">Une connexion **permanente** est une connexion qui s’exécute jusqu’à ce que le port soit détruit.</span><span class="sxs-lookup"><span data-stu-id="67198-192">A **persistent** connection is a connection that is kept running until the port is destroyed.</span></span> <span data-ttu-id="67198-193">Une connexion **non permanente** est une connexion ouverte pour un message à la fois et qui se ferme après la remise.</span><span class="sxs-lookup"><span data-stu-id="67198-193">A **non-persistent** connection is a connection that is opened for one message at a time and closes after delivery.</span></span>

#### <span data-ttu-id="67198-194">Persistance</span><span class="sxs-lookup"><span data-stu-id="67198-194">Persistent</span></span>

<span data-ttu-id="67198-195">Pour Chrome, une connexion permanente est effectuée en créant un port de messagerie à l’aide de [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) .</span><span class="sxs-lookup"><span data-stu-id="67198-195">For Chrome, a persistent connection is made by creating a messaging port using [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span> <span data-ttu-id="67198-196">Une fois le port créé, chrome démarre un processus hôte de messagerie natif qui continue de s’exécuter jusqu’à ce qu’il soit détruit.</span><span class="sxs-lookup"><span data-stu-id="67198-196">Once the port is made, Chrome starts a native messaging host process that keeps running until the port it destroyed.</span></span>

<span data-ttu-id="67198-197">Dans le cadre de l’utilisation de Microsoft Edge, une fois que vous avez créé un port de messagerie à l’aide de `runtime.connectNative` , Microsoft Edge démarre [`AppServiceConnection`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection) et continue de s’exécuter jusqu’à ce que le port soit détruit.</span><span class="sxs-lookup"><span data-stu-id="67198-197">For Microsoft Edge, once a messaging port is created using `runtime.connectNative`, Microsoft Edge starts the [`AppServiceConnection`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection) and keeps it running until the port is destroyed.</span></span> <span data-ttu-id="67198-198">L’extrait de code suivant montre comment une connexion permanente est établie à partir d’une application UWP.</span><span class="sxs-lookup"><span data-stu-id="67198-198">The following snippet shows how a persistent connection is established from within a UWP app.</span></span> 

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```

#### <span data-ttu-id="67198-199">Non permanent</span><span class="sxs-lookup"><span data-stu-id="67198-199">Non-persistent</span></span>

<span data-ttu-id="67198-200">Lors de l’envoi d’un message à l’aide [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) de chrome, sans création de port de messagerie, chrome démarre un nouveau processus hôte de messagerie natif pour chaque message.</span><span class="sxs-lookup"><span data-stu-id="67198-200">When a message is sent using [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) in Chrome, without creating a messaging port, Chrome starts a new native messaging host process for each message.</span></span> <span data-ttu-id="67198-201">Le premier message généré par le processus hôte est géré en tant que réponse à la requête d’origine, et tous les autres messages qu’elle contient sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="67198-201">The first message generated by the host process is handled as a response to the original request, and all other messages after it are ignored.</span></span>

<span data-ttu-id="67198-202">Microsoft Edge va mettre fin à la connexion après la réception de chaque message.</span><span class="sxs-lookup"><span data-stu-id="67198-202">Microsoft Edge will terminate the connection after every messages' response has been received.</span></span> <span data-ttu-id="67198-203">L’extrait de code suivant montre une connexion non permanente qui est établie avec celle-ci, `AppServiceConnection` puis arrêtée au sein de l’application UWP après réception d’une demande et stockage en tant que [`AppServiceResponse`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceresponse) .</span><span class="sxs-lookup"><span data-stu-id="67198-203">The following snippet shows a non-persistent connection that is established with `AppServiceConnection` that will then be terminated within the UWP app after a request has been received and stored as an [`AppServiceResponse`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceresponse).</span></span>

```csharp
using (var connection = new AppServiceConnection())
{    
    //Set up a new app service connection
    connection.AppServiceName = "com.microsoft.randomnumbergenerator";
    connection.PackageFamilyName = "Microsoft.SDKSamples.AppServicesProvider.CS_8wekyb3d8bbwe";
    AppServiceConnectionStatus status = await connection.OpenAsync();
    AppServiceResponse response = await connection.SendMessageAsync(inputs);
}
```

### <span data-ttu-id="67198-204">Autorisation</span><span class="sxs-lookup"><span data-stu-id="67198-204">Permission</span></span>

<span data-ttu-id="67198-205">Afin d’autoriser l’utilisation de la messagerie native avec votre extension, pour chrome et Microsoft Edge, vous devez déclarer l' `"nativeMessaging"` autorisation dans votre `manifest.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="67198-205">In order to enable native messaging use with your extension, for both Chrome and Microsoft Edge you'll need to declare the `"nativeMessaging"` permission in you `manifest.json` file.</span></span>


## <span data-ttu-id="67198-206">Services d’application</span><span class="sxs-lookup"><span data-stu-id="67198-206">App services</span></span>
<span data-ttu-id="67198-207">Cette section détaille les services d’application d’impact sur les performances et la mémoire de messagerie native de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="67198-207">This section details the impact app services has on Microsoft Edge native messaging performance and memory.</span></span>

### <span data-ttu-id="67198-208">Analyse des performances</span><span class="sxs-lookup"><span data-stu-id="67198-208">Performance</span></span>

<span data-ttu-id="67198-209">Les services d’application sont «parrainés» par l’application au premier plan qui les appelle qui, pour des raisons de messagerie native, est Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="67198-209">App services are "sponsored" by the foreground app that calls them which for native messaging purposes is Microsoft Edge.</span></span> <span data-ttu-id="67198-210">Cela signifie que les services d’application peuvent s’exécuter tant que Microsoft Edge est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="67198-210">This means that app services can run as long as Microsoft Edge is running.</span></span>

<span data-ttu-id="67198-211">En ce qui concerne la latence, les services d’application utilisent des canaux nommés qui, après la connexion initiale, autorisent deux applications à communiquer directement.</span><span class="sxs-lookup"><span data-stu-id="67198-211">In regards to latency, app services use named pipes that, after initial connection, allow two apps to directly communicate.</span></span> <span data-ttu-id="67198-212">Cette méthode de communication produit une latence faible.</span><span class="sxs-lookup"><span data-stu-id="67198-212">This method of communication produces low latency.</span></span> <span data-ttu-id="67198-213">Les appareils équipés de processeurs lents connaissent une latence initiale après le démarrage du processus qui héberge le service d’application (~ 80ms de démarrage de la tâche en arrière-plan sur certains appareils).</span><span class="sxs-lookup"><span data-stu-id="67198-213">Devices with slow CPUs will experience some initial latency after starting up the process that hosts the app service (~80ms to startup the background task on some devices).</span></span> <span data-ttu-id="67198-214">Après le démarrage, les performances sur les périphériques de processeur lente doivent être efficaces.</span><span class="sxs-lookup"><span data-stu-id="67198-214">After start-up, performance on slow CPU devices should be good.</span></span> 


### <span data-ttu-id="67198-215">Mémoire</span><span class="sxs-lookup"><span data-stu-id="67198-215">Memory</span></span>
<span data-ttu-id="67198-216">La mémoire allouée à un service d’application est extraite du quota attribué à Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="67198-216">The memory allocated to an app service is taken out of the quota allocated to Microsoft Edge.</span></span> <span data-ttu-id="67198-217">Cela signifie que si Microsoft Edge démarre trop de services d’application, il est possible qu’il n’y ait plus de mémoire.</span><span class="sxs-lookup"><span data-stu-id="67198-217">This means that if Microsoft Edge starts too many app services there is a possibility that they could run out of memory.</span></span> <span data-ttu-id="67198-218">Les limites de mémoire de tâches en arrière-plan usuelles sont appliquées aux services d’application.</span><span class="sxs-lookup"><span data-stu-id="67198-218">The usual background task memory caps are enforced on app services.</span></span> <span data-ttu-id="67198-219">Par exemple, sur un appareil de 512 Mo, une tâche en arrière-plan de service d’application ne peut pas être supérieure à 16 Mo.</span><span class="sxs-lookup"><span data-stu-id="67198-219">For instance, on a 512MB device an app service background task can be no larger than 16MB.</span></span> <span data-ttu-id="67198-220">Ce numéro augmente à mesure que les appareils évoluent.</span><span class="sxs-lookup"><span data-stu-id="67198-220">This number goes up as the devices scale up.</span></span>


## <span data-ttu-id="67198-221">Création d’une extension avec la messagerie Native</span><span class="sxs-lookup"><span data-stu-id="67198-221">Creating an extension with native messaging</span></span>

<span data-ttu-id="67198-222">Pour tester la messagerie native, votre extension doit avoir le nom de la famille de packages.</span><span class="sxs-lookup"><span data-stu-id="67198-222">In order to test native messaging, your extension needs a Package Family Name.</span></span> <span data-ttu-id="67198-223">Microsoft Edge utilise cette méthode pour déterminer l’identité de l’hôte de messages natif, ce qui signifie que votre extension doit être empaquetée.</span><span class="sxs-lookup"><span data-stu-id="67198-223">Microsoft Edge uses this to determine the native message host identity, which means your extension should be packaged.</span></span> 


<span data-ttu-id="67198-224">Pour créer votre extension avec la messagerie native dans Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="67198-224">To create your extension with native messaging in Visual Studio:</span></span>

1. <span data-ttu-id="67198-225">Créer un projet UWP dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="67198-225">Create a UWP project in Visual Studio.</span></span>
2. <span data-ttu-id="67198-226">[Ajoutez `AppService` à votre application UWP](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span><span class="sxs-lookup"><span data-stu-id="67198-226">[Add `AppService` to your UWP app](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span></span>
   - <span data-ttu-id="67198-227">Vous pouvez éventuellement [configurer `AppService` l’hébergement sur l’application principale](https://msdn.microsoft.com/windows/uwp/launch-resume/convert-app-service-in-process) plutôt que sur une tâche en arrière-plan à ce stade.</span><span class="sxs-lookup"><span data-stu-id="67198-227">You can optionally [configure `AppService` to be hosted in the main app](https://msdn.microsoft.com/windows/uwp/launch-resume/convert-app-service-in-process) instead of as a background task at this point.</span></span>
3. <span data-ttu-id="67198-228">Générez et testez votre projet UWP.</span><span class="sxs-lookup"><span data-stu-id="67198-228">Build and test your UWP project.</span></span>
   - <span data-ttu-id="67198-229">Vous pouvez éventuellement ajouter un [composant Desktop Bridge](#adding-a-desktop-bridge-component).</span><span class="sxs-lookup"><span data-stu-id="67198-229">You can optionally add a [Desktop Bridge component](#adding-a-desktop-bridge-component).</span></span>
4. <span data-ttu-id="67198-230">Créez une extension Microsoft Edge qui utilise la messagerie native pour communiquer avec l’application complémentaire UWP.</span><span class="sxs-lookup"><span data-stu-id="67198-230">Create a Microsoft Edge extension that uses native messaging to communicate with the UWP companion app.</span></span> <span data-ttu-id="67198-231">Les fichiers d’extension peuvent être ajoutés dans un dossier nommé `Extension` dans le projet UWP.</span><span class="sxs-lookup"><span data-stu-id="67198-231">The extension files can be added into a folder named `Extension` in the UWP project.</span></span> <span data-ttu-id="67198-232">Tous les fichiers sous ce dossier, y compris les sous-dossiers, doivent avoir leurs propriétés configurées de manière à ce que `Build Action=Content` et `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="67198-232">All of the files underneath this folder, including subfolders, need to have their properties configured such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span> <span data-ttu-id="67198-233">Vérifiez qu' `manifest.json` elle est également configurée avec ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="67198-233">Make sure `manifest.json` is also configured with these properties.</span></span>
5. <span data-ttu-id="67198-234">Modifiez le `package.manifest.xml` fichier dans le projet de façon à inclure les métadonnées d’extension et à le convertir en application headless en ajoutant `AppListEntry="none"` :</span><span class="sxs-lookup"><span data-stu-id="67198-234">Modify the `package.manifest.xml` file in the project to include extension metadata and convert it to a headless app by adding `AppListEntry="none"`:</span></span>

    ```xml
    <Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10" 
    xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities" 
    xmlns:mp="http://schemas.microsoft.com/appx/2014/phone/manifest" 
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10" 
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap uap3 mp rescap build" 
    xmlns:build="http://schemas.microsoft.com/developer/appx/2015/build">

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.15063.0" MaxVersionTested="10.0.15063.0" />
    </Dependencies>

       <Application Id="App" Executable="$targetnametoken$.exe" EntryPoint="NativeMessagingHostInProcess.App">
          <uap:VisualElements AppListEntry="none"
            DisplayName="SecureInput"
            Square150x150Logo="Assets\Square150x150Logo.png"
            Square44x44Logo="Assets\Square44x44Logo.png"
            Description="NativeMessagingHostInProcess"
            BackgroundColor="transparent">
          </uap:VisualElements>
          <Extensions>
            <uap3:Extension Category="windows.appExtension">
                <uap3:AppExtension
                    Name="com.microsoft.edge.extension"
                    Id="EdgeExtension"
                    PublicFolder="Extension"
                    DisplayName="ms-resource:DisplayName">
                </uap3:AppExtension>
            </uap3:Extension>
          </Extensions>
    </Application>
    ```

6. <span data-ttu-id="67198-235">Utilisez le `AppService` nom configuré pour UWP dans les API de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="67198-235">Use the `AppService` name configured for the UWP in the native messaging APIs.</span></span>
7. <span data-ttu-id="67198-236">Générez et [déployez](#deploying) le projet UWP (avec le composant Desktop Bridge facultatif).</span><span class="sxs-lookup"><span data-stu-id="67198-236">Build and [deploy](#deploying) the UWP project (with the optional Desktop Bridge component).</span></span>
8. <span data-ttu-id="67198-237">[Empaqueter](#packaging) votre extension de messagerie Native une fois qu’elle est prête pour la soumission au Windows Store</span><span class="sxs-lookup"><span data-stu-id="67198-237">[Package](#packaging) your native messaging extension once it's ready for Store submission</span></span>

> [!NOTE]
> <span data-ttu-id="67198-238">Référencez la section [démonstrations](#demos) pour obtenir un exemple d’extension de messagerie native complète.</span><span class="sxs-lookup"><span data-stu-id="67198-238">Reference the [Demos](#demos) section for an example of a complete native messaging extension.</span></span>


## <span data-ttu-id="67198-239">Ajout d’un composant Desktop Bridge</span><span class="sxs-lookup"><span data-stu-id="67198-239">Adding a Desktop Bridge component</span></span> 
<span data-ttu-id="67198-240">Si vous souhaitez ajouter un composant Desktop Bridge à votre package, vous devez créer et générer votre projet Win32 dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="67198-240">If you want to add a Desktop Bridge component to your package, you'll need to create and build your Win32 project in Visual Studio.</span></span> <span data-ttu-id="67198-241">Pour plus d’informations sur la conversion de votre application Win32 vers UWP, voir [Portage d’applications vers Windows 10 via Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root).</span><span class="sxs-lookup"><span data-stu-id="67198-241">For info on how to convert your win32 app to UWP, see [Porting apps to Windows 10 via Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root).</span></span> <span data-ttu-id="67198-242">Une fois créé dans Visual Studio, vous pouvez ajouter le code exécutable Win32 au package en procédant comme suit:</span><span class="sxs-lookup"><span data-stu-id="67198-242">Once built in Visual Studio, you can add the Win32 executable to the package by doing the following steps:</span></span>

1. <span data-ttu-id="67198-243">Ajoutez le projet Win32 dans la même solution que le projet UWP.</span><span class="sxs-lookup"><span data-stu-id="67198-243">Add the Win32 project to the same solution as the UWP project.</span></span> 

2. <span data-ttu-id="67198-244">Définissez le projet Win32 en tant que projet dépendant pour le projet UWP:</span><span class="sxs-lookup"><span data-stu-id="67198-244">Set the Win32 project as a dependent project for the UWP project:</span></span>

    ![configuration de dépendances de projet](./../media/project-dependencies.PNG)

3. <span data-ttu-id="67198-246">Créer un `Win32` dossier au sein du projet UWP.</span><span class="sxs-lookup"><span data-stu-id="67198-246">Create a `Win32` folder within the UWP project.</span></span> <span data-ttu-id="67198-247">Copiez les fichiers binaires nécessaires pour le `Win32` projet dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="67198-247">Copy the necessary binaries for the `Win32` project to this folder.</span></span> <span data-ttu-id="67198-248">Configurez les propriétés de tous les fichiers binaires, tels que `Build Action=Content` et `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="67198-248">Configure the properties of all the binaries such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span>

    ![dossier contenant les fichiers d’application Win32 et UWP](./../media/desktop-bridge.png)

4. <span data-ttu-id="67198-250">Modifiez le fichier de projet UWP pour copier tous les fichiers binaires nécessaires pour le `Win32` projet dans ce dossier à l’aide de la commande d’événement PostBuild.</span><span class="sxs-lookup"><span data-stu-id="67198-250">Modify the UWP project file to copy all the necessary binaries for the `Win32` project into this folder using PostBuild event command.</span></span> <span data-ttu-id="67198-251">Cela permet de s’assurer que les fichiers binaires mis à jour sont copiés dans le dossier chaque fois que la solution est reconstruite.</span><span class="sxs-lookup"><span data-stu-id="67198-251">This ensures that the updated binaries are being copied to the folder every time the solution is rebuilt.</span></span>

    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```


5. <span data-ttu-id="67198-252">Modifiez `package.manifest.xml` en ajoutant l' `<desktop:Extension>` élément à l' `<Extensions>` élément:</span><span class="sxs-lookup"><span data-stu-id="67198-252">Modify `package.manifest.xml` by adding the `<desktop:Extension>` element to the `<Extensions>` element:</span></span>

    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```

## <span data-ttu-id="67198-253">Déploiement</span><span class="sxs-lookup"><span data-stu-id="67198-253">Deploying</span></span>
<span data-ttu-id="67198-254">Une fois que vous avez configuré votre projet UWP (et éventuellement le projet Win32) comme décrit ci-dessus, vous êtes prêt à déployer la solution à l’aide de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="67198-254">Once you have configured your UWP project (and optionally Win32 project) as outlined above, you are ready to deploy the solution using Visual Studio.</span></span>

![créer un projet d’inprocessus](../media/native-message-uwp-debug.PNG)

<span data-ttu-id="67198-256">Lorsque la solution est déployée correctement, vous devriez voir votre extension dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="67198-256">Once the solution is correctly deployed, you should see your extension in Microsoft Edge.</span></span>

![extension affichée dans Microsoft Edge](../media/secureextension.png)

## <span data-ttu-id="67198-258">Intégration</span><span class="sxs-lookup"><span data-stu-id="67198-258">Packaging</span></span>

> [!NOTE]
> <span data-ttu-id="67198-259">Le fait de soumettre une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte.</span><span class="sxs-lookup"><span data-stu-id="67198-259">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="67198-260">Contactez [-nous](https://aka.ms/extension-request) pour obtenir vos demandes en tant que partie du Microsoft Store et nous vous enverrons une prochaine mise à jour.</span><span class="sxs-lookup"><span data-stu-id="67198-260">[Reach out to us](https://aka.ms/extension-request) with your requests to be a part of the Microsoft Store, and we'll consider you for a future update.</span></span>


<span data-ttu-id="67198-261">Vous pouvez générer un package de magasin pour la soumission au centre de développement Windows à l’aide de la fonctionnalité intégrée de Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="67198-261">You can generate a Store package for submission to the Windows Dev Center using built-in Visual Studio functionality:</span></span>


![Création d’un package du Windows Store](../media/create-store-package.PNG)

## <span data-ttu-id="67198-263">Débogage</span><span class="sxs-lookup"><span data-stu-id="67198-263">Debugging</span></span>
<span data-ttu-id="67198-264">Les instructions relatives au débogage varient selon le composant que vous voulez tester:</span><span class="sxs-lookup"><span data-stu-id="67198-264">The instructions for debugging vary depending on which component you want to test out:</span></span>

### <span data-ttu-id="67198-265">Débogage de l’extension</span><span class="sxs-lookup"><span data-stu-id="67198-265">Debugging the extension</span></span>
<span data-ttu-id="67198-266">Une fois la solution déployée, l’extension sera installée dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="67198-266">Once the solution is deployed, the extension will be installed in Microsoft Edge.</span></span> <span data-ttu-id="67198-267">Pour plus d’informations sur le débogage d’une extension, voir le Guide de [débogage](./debugging-extensions.md) .</span><span class="sxs-lookup"><span data-stu-id="67198-267">Check out the [Debugging](./debugging-extensions.md) guide for info on how to debug an extension.</span></span>


### <span data-ttu-id="67198-268">Débogage de l’application UWP</span><span class="sxs-lookup"><span data-stu-id="67198-268">Debugging the UWP app</span></span>
<span data-ttu-id="67198-269">L’application UWP démarre lorsque l’extension tente de s’y connecter à l’aide des [API de messagerie Native](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span><span class="sxs-lookup"><span data-stu-id="67198-269">The UWP app will launch when the extension tries to connect to it using [native messaging APIs](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span> <span data-ttu-id="67198-270">Vous devez déboguer l’application UWP uniquement une fois le processus démarré.</span><span class="sxs-lookup"><span data-stu-id="67198-270">You'll need to debug the UWP app only once the process starts.</span></span> <span data-ttu-id="67198-271">Ce problème peut être configuré via la page de propriétés du projet:</span><span class="sxs-lookup"><span data-stu-id="67198-271">This can be configured via the project's Property page:</span></span>

1.  <span data-ttu-id="67198-272">Dans Visual Studio, cliquez avec le bouton droit sur votre projet d’application UWP.</span><span class="sxs-lookup"><span data-stu-id="67198-272">In Visual Studio, right click your UWP app project</span></span>
2.  <span data-ttu-id="67198-273">Sélectionner les propriétés</span><span class="sxs-lookup"><span data-stu-id="67198-273">Select Properties</span></span>
3.  <span data-ttu-id="67198-274">Cochez la case ne pas lancer, mais déboguer mon code au démarrage.</span><span class="sxs-lookup"><span data-stu-id="67198-274">Check "Do not launch, but debug my code when it starts"</span></span>

    ![sélection de la zone ne pas lancer](../media/native-message-do-not-launch.png)

<span data-ttu-id="67198-276">Dans Visual Studio, vous pouvez maintenant définir des points d’arrêt dans le code pour lequel vous voulez déboguer, puis lancer le débogueur en appuyant sur F5.</span><span class="sxs-lookup"><span data-stu-id="67198-276">In Visual Studio you can now set breakpoints in the code where you want to debug, then launch the debugger by pressing F5.</span></span> <span data-ttu-id="67198-277">Lorsque vous interagissez avec l’extension pour vous connecter à l’application UWP, Visual Studio s’attache automatiquement au processus.</span><span class="sxs-lookup"><span data-stu-id="67198-277">Once you interact with the extension to connect to the UWP app, Visual Studio will automatically attach to the process.</span></span>


### <span data-ttu-id="67198-278">Débogage de Desktop Bridge</span><span class="sxs-lookup"><span data-stu-id="67198-278">Debugging the Desktop Bridge</span></span>
<span data-ttu-id="67198-279">Même s’il existe différentes [méthodes pour le débogage de Desktop Bridge](https://msdn.microsoft.com/windows/uwp/porting/desktop-to-uwp-debug) (application Win32 convertie), la seule application applicable pour ce scénario est l’option PLMDebug.</span><span class="sxs-lookup"><span data-stu-id="67198-279">Even though there are various [methods for debugging a Desktop Bridge](https://msdn.microsoft.com/windows/uwp/porting/desktop-to-uwp-debug) (converted Win32 app), the only one applicable for this scenarios is the PLMDebug option.</span></span> <span data-ttu-id="67198-280">Vous pouvez également ajouter du code de débogage à la fonction de démarrage pour exécuter une attente pour une heure spécifique, ce qui vous permet d’attacher Visual Studio au processus.</span><span class="sxs-lookup"><span data-stu-id="67198-280">You could also add debugging code to the startup function to perform a wait for a specific time, allowing you to attach Visual Studio to the process.</span></span>
