---
description: Découvrez comment vous pouvez utiliser la messagerie native pour que votre extension communique avec une application UWP complémentaire.
title: Messagerie native | Extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, développement web, html, css, javascript, développeur, natif, messagerie, uwp
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9a306055b8f86b92aa5c3e7cd6de44f2386307d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399357"
---
# <a name="native-messaging-in-microsoft-edge"></a><span data-ttu-id="a5f97-104">Messagerie native dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a5f97-104">Native messaging in Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <a name="native-messaging-architecture-overview"></a><span data-ttu-id="a5f97-105">Vue d’ensemble de l’architecture de messagerie native</span><span class="sxs-lookup"><span data-stu-id="a5f97-105">Native messaging architecture overview</span></span>  

<span data-ttu-id="a5f97-106">Avec Windows 10 Creators Update, les extensions Microsoft Edge peuvent utiliser la messagerie native pour communiquer avec une application complémentaire de plateforme Windows universelle \(UWP\).</span><span class="sxs-lookup"><span data-stu-id="a5f97-106">With the Windows 10 Creators Update, Microsoft Edge extensions are able to use native messaging to communicate with a companion Universal Windows Platform \(UWP\) app.</span></span>  <span data-ttu-id="a5f97-107">À un niveau élevé, les extensions Microsoft Edge utilisent les mêmes API pour la messagerie native que les extensions Chrome et Firefox.</span><span class="sxs-lookup"><span data-stu-id="a5f97-107">At a high level, Microsoft Edge extensions use the same APIs for native messaging as Chrome and Firefox extensions.</span></span>  <span data-ttu-id="a5f97-108">Toutefois, l’hôte de messagerie native doit être implémenté à l’aide de la plateforme Windows universelle.</span><span class="sxs-lookup"><span data-stu-id="a5f97-108">However, the native messaging host will need to be implemented using the Universal Windows Platform.</span></span>  

> [!NOTE]
> <span data-ttu-id="a5f97-109">La méthode décrite ci-dessous \(connexion à une application UWP via AppService\) est le seul mécanisme pris en charge pour permettre la communication entre les extensions Microsoft Edge et les composants natifs.</span><span class="sxs-lookup"><span data-stu-id="a5f97-109">The method outlined below \(connecting to a UWP app via AppService\) is the only supported mechanism for enabling communication between Microsoft Edge extensions and native components.</span></span>  <span data-ttu-id="a5f97-110">Consultez la section [Ajout d’un](#adding-a-desktop-bridge-component) composant Pont du bureau de ce guide pour plus d’informations sur la façon d’activer la communication avec les composants Win32 hérités.</span><span class="sxs-lookup"><span data-stu-id="a5f97-110">Please see the [Adding a Desktop Bridge component](#adding-a-desktop-bridge-component) section of this guide for more information on how to enable communication with legacy Win32 components.</span></span>  

<span data-ttu-id="a5f97-111">L’architecture de messagerie native dans Microsoft Edge exploite l’API existante en tant qu’infrastructure de communication entre processus [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) sous-jacente \(IPC\).</span><span class="sxs-lookup"><span data-stu-id="a5f97-111">The native messaging architecture in Microsoft Edge leverages the existing [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) API as the underlying inter-process communication \(IPC\) infrastructure.</span></span>  <span data-ttu-id="a5f97-112">Les applications UWP utilisent `AppService` l’API pour communiquer les unes avec les autres.</span><span class="sxs-lookup"><span data-stu-id="a5f97-112">UWP apps use the `AppService` API to communicate with one another.</span></span>  <span data-ttu-id="a5f97-113">Pour cette raison, les extensions Microsoft Edge peuvent désormais communiquer avec les applications UWP.</span><span class="sxs-lookup"><span data-stu-id="a5f97-113">Because of this, Microsoft Edge extensions are now able to communicate with UWP apps.</span></span>  

![architecture de messagerie native](../media/native-messaging-architecture.png)  

### <a name="when-and-when-not-to-use-native-messaging"></a><span data-ttu-id="a5f97-115">Quand et quand ne pas utiliser la messagerie native</span><span class="sxs-lookup"><span data-stu-id="a5f97-115">When and when not to use native messaging</span></span>  

<span data-ttu-id="a5f97-116">La messagerie native ajoute une nouvelle couche à votre extension.</span><span class="sxs-lookup"><span data-stu-id="a5f97-116">Native messaging adds a whole new layer to your extension.</span></span>  <span data-ttu-id="a5f97-117">En implémentant une application complémentaire UWP pour votre extension, les possibilités suivantes s’offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="a5f97-117">By implementing a UWP companion app for your extension, the following possibilities become available to you:</span></span>  

*   <span data-ttu-id="a5f97-118">Synchronisez les données \(par exemple les informations d’identification\) avec une application UWP complémentaire.</span><span class="sxs-lookup"><span data-stu-id="a5f97-118">Synchronize data \(for example credentials\) with a companion UWP app.</span></span>  
*   <span data-ttu-id="a5f97-119">Implémenter des algorithmes de chiffrement/déchiffrement plus puissants qui ne sont pas disponibles dans les API web.</span><span class="sxs-lookup"><span data-stu-id="a5f97-119">Implement stronger encryption/decryption algorithms not available in web APIs.</span></span>  
*   <span data-ttu-id="a5f97-120">Accéder à des ressources qui ne sont pas accessibles via des API web, par exemple du matériel ou des périphériques USB</span><span class="sxs-lookup"><span data-stu-id="a5f97-120">Access resources that are not accessible through web APIs, for example hardware or USB devices</span></span>  

<span data-ttu-id="a5f97-121">Dans certains cas, la messagerie native ne doit pas être utilisée en raison de restrictions de sécurité ou de stratégie :</span><span class="sxs-lookup"><span data-stu-id="a5f97-121">There are a few instances where native messaging should not be used due to security or policy restrictions:</span></span>  

*   <span data-ttu-id="a5f97-122">Modification des paramètres utilisateur dans Microsoft Edge ou Windows, par exemple en modifiant le navigateur ou le moteur de recherche par défaut.</span><span class="sxs-lookup"><span data-stu-id="a5f97-122">Modifying user settings in either Microsoft Edge or Windows, for example changing the default browser or search provider.</span></span>  
*   <span data-ttu-id="a5f97-123">Actions qui violent les stratégies du Microsoft Store pour les applications et les extensions.</span><span class="sxs-lookup"><span data-stu-id="a5f97-123">Actions that violate Microsoft Store policies for both apps and extensions.</span></span>  
*   <span data-ttu-id="a5f97-124">Transfert de données vers un point de terminaison distant via l’hôte de message natif.</span><span class="sxs-lookup"><span data-stu-id="a5f97-124">Transferring data to remote endpoint via native message host.</span></span>  
*   <span data-ttu-id="a5f97-125">Autoriser d’autres applications à télécharger du contenu qui modifie le comportement de l’extension.</span><span class="sxs-lookup"><span data-stu-id="a5f97-125">Allowing other apps to download content that changes extension behavior.</span></span>  

## <a name="demos"></a><span data-ttu-id="a5f97-126">Démos</span><span class="sxs-lookup"><span data-stu-id="a5f97-126">Demos</span></span>  

<span data-ttu-id="a5f97-127">Pour avoir une idée de ce à quoi ressemble une extension de messagerie native Microsoft Edge qui possède à la fois une application UWP et un pont du bureau, consultez les exemples [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) et [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="a5f97-127">To get a feel for what an Microsoft Edge native messaging extension that has both a companion UWP app and a Desktop Bridge looks like, check out the [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) and [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) examples on GitHub.</span></span>  

### <a name="how-it-works"></a><span data-ttu-id="a5f97-128">Fonctionnement</span><span class="sxs-lookup"><span data-stu-id="a5f97-128">How it works</span></span>  

<span data-ttu-id="a5f97-129">Le composant d’extension Microsoft Edge de l’exemple utilise son script de contenu pour détecter quand un utilisateur tape des informations qui doivent être chiffrées.</span><span class="sxs-lookup"><span data-stu-id="a5f97-129">The Microsoft Edge extension component of the sample uses its content script to detect when a user is typing in information that should be encrypted.</span></span>  <span data-ttu-id="a5f97-130">L’extension communique cela au composant Pont du bureau via la messagerie native.</span><span class="sxs-lookup"><span data-stu-id="a5f97-130">The extension communicates this to the Desktop Bridge component via native messaging.</span></span>  <span data-ttu-id="a5f97-131">Lorsque l’utilisateur est prêt à envoyer les données, l’extension retourne une valeur chiffrée au site web.</span><span class="sxs-lookup"><span data-stu-id="a5f97-131">When the user is ready to submit the data, the extension will return an encrypted value back to the website.</span></span>  

> [!NOTE]
> <span data-ttu-id="a5f97-132">Cet exemple fonctionne uniquement sur une page web qui utilise des événements personnalisés pour communiquer avec le script de contenu de l’extension.</span><span class="sxs-lookup"><span data-stu-id="a5f97-132">This sample will only work on a webpage that uses custom events to communicate with the content script of the extension.</span></span>  <span data-ttu-id="a5f97-133">L’exemple de dossier inclut [un fichier .html avec](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) qui tester l’extension.</span><span class="sxs-lookup"><span data-stu-id="a5f97-133">The sample folder includes a [.html file](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) to test the extension with.</span></span>  

<span data-ttu-id="a5f97-134">Dans cet exemple, l’application UWP est utilisée pour transmettre des réponses du Pont du bureau à Microsoft Edge, qui est ensuite envoyée à l’extension Microsoft Edge par rappel.</span><span class="sxs-lookup"><span data-stu-id="a5f97-134">In this example, the UWP app is used to pass responses from the Desktop Bridge to Microsoft Edge, which then gets sent to the Microsoft Edge extension via callback.</span></span>  <span data-ttu-id="a5f97-135">Bien que cet exemple exécute l’hôte de messagerie native dans l’application principale, il peut également s’exécuter en tant que tâche en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="a5f97-135">While this example has the native messaging host run in the main app, it is also able to run as a background task.</span></span>  <span data-ttu-id="a5f97-136">Le basculement entre les deux nécessite la modification du script d’arrière-plan de l’extension, en modifiant la chaîne à `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` l’intérieur de `"NativeMessagingHostOutOfProcess"` .</span><span class="sxs-lookup"><span data-stu-id="a5f97-136">Switching between the two requires editing the background script of the extension, changing the string within `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` to `"NativeMessagingHostOutOfProcess"`.</span></span>  

## <a name="chrome-vs-microsoft-edge-implementation"></a><span data-ttu-id="a5f97-137">Implémentation de Chrome et Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a5f97-137">Chrome vs Microsoft Edge implementation</span></span>  

<span data-ttu-id="a5f97-138">Bien que Chrome utilise les API de transmission de messages pour leurs extensions afin de communiquer avec les applications, Microsoft Edge utilise l’API qui permet désormais aux extensions Microsoft Edge et aux applications UWP de [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) communiquer.</span><span class="sxs-lookup"><span data-stu-id="a5f97-138">While Chrome goes the route of using message passing APIs for their extensions to communicate with apps, Microsoft Edge utilizes the [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) API which now enables Microsoft Edge extensions and UWP apps to communicate.</span></span>  

<span data-ttu-id="a5f97-139">Cette section détaille les différences entre la façon dont Chrome et Microsoft Edge gèrent l’implémentation de la messagerie native.</span><span class="sxs-lookup"><span data-stu-id="a5f97-139">This section details the differences between how Chrome and Microsoft Edge handle native messaging implementation.</span></span>  

### <a name="registration-and-host-manifest"></a><span data-ttu-id="a5f97-140">Inscription et manifeste de l’hôte</span><span class="sxs-lookup"><span data-stu-id="a5f97-140">Registration and host manifest</span></span>  

<span data-ttu-id="a5f97-141">Pour que votre application soit reconnue par votre extension en tant qu’hôte de messagerie natif, elle doit être inscrite.</span><span class="sxs-lookup"><span data-stu-id="a5f97-141">In order for your app to be recognized by your extension as a native messaging host, it will need to be registered.</span></span>  

<span data-ttu-id="a5f97-142">Pour [l’inscription](https://developer.chrome.com/extensions/nativeMessaging) de l’hôte de messagerie native Chrome, votre application doit installer un fichier manifeste n’importe où dans le système de fichiers Windows qui définit la configuration de l’hôte de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="a5f97-142">For [Chrome native messaging](https://developer.chrome.com/extensions/nativeMessaging) host registration, your app needs to install a manifest file anywhere in the Windows file system that defines the native messaging host configuration.</span></span>  

<span data-ttu-id="a5f97-143">Le JSON suivant est un exemple de paramètres pour le fichier de configuration :</span><span class="sxs-lookup"><span data-stu-id="a5f97-143">The following JSON is an example of settings for the config file:</span></span>  

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

<span data-ttu-id="a5f97-144">Pour installer ce fichier, l’application doit :</span><span class="sxs-lookup"><span data-stu-id="a5f97-144">To install this file, the app would need to:</span></span>  

1.  <span data-ttu-id="a5f97-145">Enregistrez le fichier manifeste à un emplacement prédéféré dans le Registre qui définit la configuration de l’hôte :</span><span class="sxs-lookup"><span data-stu-id="a5f97-145">Register the manifest file in a predefined location in the registry that defines the host configuration:</span></span>  
    *   `HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
        <span data-ttu-id="a5f97-146">or</span><span class="sxs-lookup"><span data-stu-id="a5f97-146">or</span></span>  
    *   `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
1.  <span data-ttu-id="a5f97-147">Définissez la valeur par défaut de cette clé sur le chemin d’accès complet au fichier manifeste, par exemple</span><span class="sxs-lookup"><span data-stu-id="a5f97-147">Set the default value of that key to the full path to the manifest file, for example</span></span> `[HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"`  

<span data-ttu-id="a5f97-148">Pour Microsoft Edge, pour inscrire un \(hôte de messagerie natif\), vous devez inclure l’application complémentaire UWP dans le même package que votre extension et spécifier [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) [l’extension AppService](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) dans le fichier de votre `Package.appxmanifest` projet.</span><span class="sxs-lookup"><span data-stu-id="a5f97-148">For Microsoft Edge, in order to register an [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) \(native messaging host\) you must include the UWP companion app in the same package as your extension and specify the [AppService extension](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) in the `Package.appxmanifest` file of your project.</span></span>  <span data-ttu-id="a5f97-149">Les `EntryPoint` `Name` attributs et les attributs peuvent être configurés par vous :</span><span class="sxs-lookup"><span data-stu-id="a5f97-149">The `EntryPoint` and `Name` attributes may be configured by you:</span></span>  

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

<span data-ttu-id="a5f97-150">Vous devez également définir les extensions autorisées à se connecter au service.</span><span class="sxs-lookup"><span data-stu-id="a5f97-150">You also need to set which extensions are allowed to connect to the service.</span></span>  <span data-ttu-id="a5f97-151">Étant donné que Microsoft Edge n’a pas de propriété de manifeste équivalente dans son AppxManifest, cela doit être déterminé et appliqué lors de l’exécution par `"allowed_origins"` votre application UWP.</span><span class="sxs-lookup"><span data-stu-id="a5f97-151">Because Microsoft Edge does not have an equivalent `"allowed_origins"` manifest property in its AppxManifest, this will need to be determined and enforced at runtime by your UWP app.</span></span>  <span data-ttu-id="a5f97-152">Étant donné que Microsoft Edge établit la connexion pour le compte de l’extension, l’application recherche le nom de la famille de packages de l’appelant pour déterminer si le poste est connecté par Microsoft Edge pour contrôler ou authentifier l’appelant.</span><span class="sxs-lookup"><span data-stu-id="a5f97-152">Since Microsoft Edge establishes the connection on behalf of the extension, the app looks up the Package Family Name of the caller to determine if extension is being connected by Microsoft Edge to control or authenticate the caller.</span></span>  <span data-ttu-id="a5f97-153">Par exemple</span><span class="sxs-lookup"><span data-stu-id="a5f97-153">For example</span></span>   

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

### <a name="message-sending"></a><span data-ttu-id="a5f97-154">Envoi de messages</span><span class="sxs-lookup"><span data-stu-id="a5f97-154">Message sending</span></span>  

<span data-ttu-id="a5f97-155">Pour qu’une application et une extension communiquent entre elles, des messages doivent être envoyés vers et depuis eux.</span><span class="sxs-lookup"><span data-stu-id="a5f97-155">For an app and an extension to communicate with one another, messages need to be sent to and from them.</span></span>  

<span data-ttu-id="a5f97-156">Les extensions Chrome lancent un message à l’aide de l’API pour remettre un message à l’hôte natif à l’aide d’un canal [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) non persistant.</span><span class="sxs-lookup"><span data-stu-id="a5f97-156">Chrome extensions initiate a message using the [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API to deliver a message to the native host using a non-persistent channel.</span></span>  

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```  

<span data-ttu-id="a5f97-157">Le premier paramètre est le nom de l’hôte natif, que Chrome recherche dans le Registre pour le manifeste.</span><span class="sxs-lookup"><span data-stu-id="a5f97-157">The first parameter is the name of the native host, which Chrome looks up in the registry for the manifest.</span></span>  <span data-ttu-id="a5f97-158">Le manifeste spécifie le .exe que Chrome lancera dans un bac à sable et le message est envoyé à l’aide de std i/o.</span><span class="sxs-lookup"><span data-stu-id="a5f97-158">The manifest specifies the .exe that Chrome will launch in a sandbox, and the message is sent using std i/o.</span></span>  
<span data-ttu-id="a5f97-159">Les extensions établissent également un canal persistant à l’aide de l’API, qui prend le nom de l’hôte `runtime.connectNative` natif comme seul paramètre.</span><span class="sxs-lookup"><span data-stu-id="a5f97-159">Extensions also establish a persistent channel using the `runtime.connectNative` API, which takes the name of the native host as the only parameter.</span></span>  

<span data-ttu-id="a5f97-160">Microsoft Edge utilise la même construction que l’API de messagerie native dans Chrome pour permettre aux extensions Microsoft Edge de spécifier le service d’application auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="a5f97-160">Microsoft Edge uses the same construct as the native messaging API in Chrome to allow Microsoft Edge extensions to specify which app service to connect to.</span></span>  <span data-ttu-id="a5f97-161">Le premier paramètre dans `runtime.sendNativeMessage` spécifie le nom du service d’application.</span><span class="sxs-lookup"><span data-stu-id="a5f97-161">The first parameter in `runtime.sendNativeMessage` specifies the app service name.</span></span>  <span data-ttu-id="a5f97-162">Dans la section [Inscription et manifeste de l’hôte,](#registration-and-host-manifest) il s’agit de `"com.microsoft.inventory"` .</span><span class="sxs-lookup"><span data-stu-id="a5f97-162">In the [Registration and host manifest](#registration-and-host-manifest) section, this is `"com.microsoft.inventory"`.</span></span>  <span data-ttu-id="a5f97-163">La plateforme d’extension Microsoft Edge limite l’hôte de messagerie natif à être une application UWP empaqueté dans le même AppX que l’extension.</span><span class="sxs-lookup"><span data-stu-id="a5f97-163">The Microsoft Edge extension platform restricts the native messaging host to being a UWP app that is packaged in the same AppX as the extension.</span></span>  <span data-ttu-id="a5f97-164">Cela permet d’atténuer les risques de sécurité associés aux attaques malveillantes qui tentent de connecter Microsoft Edge à un autre nom de famille de packages en falsifiant les entrées de manifeste.</span><span class="sxs-lookup"><span data-stu-id="a5f97-164">This mitigates any security risks associated with malicious attacks that try to connect Microsoft Edge with another Package Family Name by tampering with manifest entries.</span></span>  

<span data-ttu-id="a5f97-165">Cela signifie que Microsoft Edge utilisera le même nom de famille de package que l’extension, en plus du nom spécifié dans l’API, pour identifier de manière unique le fournisseur du `AppService` service d’application.</span><span class="sxs-lookup"><span data-stu-id="a5f97-165">This means that Microsoft Edge will use the same Package Family Name as the extension, in addition to the `AppService` name specified in the API, to uniquely identify the provider of the app service.</span></span>  

> [!NOTE]
> <span data-ttu-id="a5f97-166">Cela ne sera pas facilement converti par l’extension [Microsoft Edge Shared Computer Toolkit](./porting-chrome-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a5f97-166">This will not be easily converted by the [Microsoft Edge Extension Toolkit](./porting-chrome-extensions.md).</span></span>  <span data-ttu-id="a5f97-167">Toutes les extensions qui spécifient l’autorisation sont signalées comme nécessitant `"nativeMessaging"` une conversion manuelle pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="a5f97-167">Any extensions that specifies the `"nativeMessaging"` permission will be flagged as requiring manual conversion for this component.</span></span>  

### <a name="communication-protocol"></a><span data-ttu-id="a5f97-168">Protocole de communication</span><span class="sxs-lookup"><span data-stu-id="a5f97-168">Communication protocol</span></span>  

<span data-ttu-id="a5f97-169">Le protocole de communication pour la messagerie native détermine la façon dont les messages sont mis en forme avant l’envoi.</span><span class="sxs-lookup"><span data-stu-id="a5f97-169">Communication protocol for native messaging determines how messages are formatted before sending.</span></span>  

<span data-ttu-id="a5f97-170">Chrome démarre chaque hôte de messagerie native dans un processus distinct et communique avec lui à l’aide de l’entrée standard et de la sortie standard.</span><span class="sxs-lookup"><span data-stu-id="a5f97-170">Chrome starts each native messaging host in a separate process and communicates with it using standard input and standard output.</span></span>  <span data-ttu-id="a5f97-171">Le même format est utilisé pour envoyer des messages dans les deux sens : chaque message est sérialisé à l’aide de JSON, codé en UTF-8 et est précédé de la longueur des messages 32 bits dans l’ordre d’byte natif.</span><span class="sxs-lookup"><span data-stu-id="a5f97-171">The same format is used to send messages in both directions: each message is serialized using JSON, UTF-8 encoded and is preceded with 32-bit message length in native byte order.</span></span>  

<span data-ttu-id="a5f97-172">Pour Microsoft Edge, la tâche en arrière-plan/l’application principale qui implémente le service d’application sera démarrée par la plateforme.</span><span class="sxs-lookup"><span data-stu-id="a5f97-172">For Microsoft Edge, the background task/main app that implements the app service will be started by the platform.</span></span>  <span data-ttu-id="a5f97-173">Au démarrage, la `Run` méthode de la tâche en arrière-plan est invoquée :</span><span class="sxs-lookup"><span data-stu-id="a5f97-173">On startup, the `Run` method of the background task is invoked:</span></span>  

```csharp
public void Run(IBackgroundTaskInstance taskInstance)    
{
    this.backgroundTaskDeferral = taskInstance.GetDeferral();
    // Get a deferral so that the service is not stopped and ended.
    taskInstance.Canceled += OnTaskCanceled;
    // Associate a cancellation handler with the background task.
    // Retrieve the app service connection and set up a listener for incoming app service requests.
    var details = taskInstance.TriggerDetails as AppServiceTriggerDetails;
    appServiceconnection = details.AppServiceConnection;
    appServiceconnection.RequestReceived += OnRequestReceived;
}
```  

<span data-ttu-id="a5f97-174">Lorsque votre extension envoie un message à votre application UWP, [`onRequestReceived`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) l’événement est levé.</span><span class="sxs-lookup"><span data-stu-id="a5f97-174">When your extension sends a message to your UWP app, the [`onRequestReceived`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) event will be raised.</span></span>  <span data-ttu-id="a5f97-175">Ce message au format JSON est ensuite stringified dans la première paire KeyValue d’un [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) objet.</span><span class="sxs-lookup"><span data-stu-id="a5f97-175">This JSON formatted message will then be stringified into the first KeyValue pair of a [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) object.</span></span>  <span data-ttu-id="a5f97-176">:</span><span class="sxs-lookup"><span data-stu-id="a5f97-176">:</span></span>  

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```  

<span data-ttu-id="a5f97-177">Lorsque votre application UWP renvoie une réponse à votre extension, une réponse est [`KeyValuePair`](/dotnet/api/system.collections.generic.keyvaluepair-2?view=netcore-3.1&preserve-view=true) ajoutée à `ValueSet` l’objet.</span><span class="sxs-lookup"><span data-stu-id="a5f97-177">When your UWP app sends a response back to your extension, a [`KeyValuePair`](/dotnet/api/system.collections.generic.keyvaluepair-2?view=netcore-3.1&preserve-view=true) will be added to the `ValueSet` object.</span></span>  <span data-ttu-id="a5f97-178">La propriété est ignorée par Microsoft Edge, mais elle contient `Key` `Value` une chaîne JSON valide.</span><span class="sxs-lookup"><span data-stu-id="a5f97-178">The `Key` property will be ignored by Microsoft Edge, but the `Value` property will contain a valid JSON string.</span></span>  

### <a name="callback"></a><span data-ttu-id="a5f97-179">Rappel</span><span class="sxs-lookup"><span data-stu-id="a5f97-179">Callback</span></span>  

<span data-ttu-id="a5f97-180">Pour les rappels, Chrome utilise ce qui permet à une fonction de rappel de gérer toute réponse asynchrone lors de [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) l’envoi d’un message.</span><span class="sxs-lookup"><span data-stu-id="a5f97-180">For callbacks, Chrome uses [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) which allows a callback function to handle any asynchronous response from sending a message.</span></span>  

<span data-ttu-id="a5f97-181">Microsoft Edge utilise la méthode de l’objet pour que l’application renvoie [`SendResponseAsync`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) [`AppServiceRequest`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) un objet à [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) l’extension.</span><span class="sxs-lookup"><span data-stu-id="a5f97-181">Microsoft Edge uses the [`SendResponseAsync`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) method  of the [`AppServiceRequest`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) object to let the app send a [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) object back to the extension.</span></span>  

### <a name="message-size-limit"></a><span data-ttu-id="a5f97-182">Limite de taille des messages</span><span class="sxs-lookup"><span data-stu-id="a5f97-182">Message size limit</span></span>  

<span data-ttu-id="a5f97-183">Les messages envoyés entre une extension et une application ont des limites de taille de message différentes pour Chrome et Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a5f97-183">Messages that are sent back and forth between an extension and an app have different message size limitations in place for Chrome and Microsoft Edge.</span></span>  

<span data-ttu-id="a5f97-184">Chrome présente les limites de taille de message suivantes :</span><span class="sxs-lookup"><span data-stu-id="a5f97-184">Chrome has the following message size limitations:</span></span>  

*   <span data-ttu-id="a5f97-185">Limite de message unique de l’hôte de messagerie native : 1 Mo</span><span class="sxs-lookup"><span data-stu-id="a5f97-185">Single message limit from native messaging host:  1 MB</span></span>  
*   <span data-ttu-id="a5f97-186">Limite de message unique envoyée à l’hôte de messagerie native : 4 Go</span><span class="sxs-lookup"><span data-stu-id="a5f97-186">Single message limit sent to native messaging host:  4 GB</span></span>  

<span data-ttu-id="a5f97-187">Pour Microsoft Edge, bien qu’il n’y ait aucune limite sur la taille des messages \(dépendant de la mémoire\), Microsoft Edge se protège contre les erreurs de comportement des applications natives en maintenant les limites de taille de `AppService` message suivantes :</span><span class="sxs-lookup"><span data-stu-id="a5f97-187">For Microsoft Edge, while `AppService` has no limit on message size \(dependent on memory\), Microsoft Edge protects itself against misbehaving native apps by imposing the following message size limits:</span></span>  

*   <span data-ttu-id="a5f97-188">Limite de message unique entre l’application UWP et l’extension : 1 Mo</span><span class="sxs-lookup"><span data-stu-id="a5f97-188">Single message limit from UWP app to extension: 1 MB</span></span>  
*   <span data-ttu-id="a5f97-189">Limite de message unique entre l’extension et l’application UWP : 100 Mo</span><span class="sxs-lookup"><span data-stu-id="a5f97-189">Single message limit from extension to UWP app: 100 MB</span></span>  

### <a name="native-messaging-connections"></a><span data-ttu-id="a5f97-190">Connexions de messagerie natives</span><span class="sxs-lookup"><span data-stu-id="a5f97-190">Native messaging connections</span></span>  

<span data-ttu-id="a5f97-191">Il existe deux types de connexions pour la messagerie native ; persistantes et non persistantes.</span><span class="sxs-lookup"><span data-stu-id="a5f97-191">There are two types of connections for native messaging; persistent and non-persistent.</span></span>  
<span data-ttu-id="a5f97-192">Une **connexion persistante** est une connexion qui est en cours d’exécution jusqu’à ce que le port soit détruit.</span><span class="sxs-lookup"><span data-stu-id="a5f97-192">A **persistent** connection is a connection that is kept running until the port is destroyed.</span></span>  <span data-ttu-id="a5f97-193">Une **connexion non persistante** est une connexion ouverte pour un message à la fois et qui se ferme après la remise.</span><span class="sxs-lookup"><span data-stu-id="a5f97-193">A **non-persistent** connection is a connection that is opened for one message at a time and closes after delivery.</span></span>  

#### <a name="persistent"></a><span data-ttu-id="a5f97-194">Persistance</span><span class="sxs-lookup"><span data-stu-id="a5f97-194">Persistent</span></span>  

<span data-ttu-id="a5f97-195">Pour Chrome, une connexion permanente est réalisée en créant un port de messagerie à l’aide [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) de .</span><span class="sxs-lookup"><span data-stu-id="a5f97-195">For Chrome, a persistent connection is made by creating a messaging port using [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span>  <span data-ttu-id="a5f97-196">Une fois le port effectué, Chrome démarre un processus d’hôte de messagerie natif qui continue à s’exécute jusqu’au port qu’il a détruit.</span><span class="sxs-lookup"><span data-stu-id="a5f97-196">Once the port is made, Chrome starts a native messaging host process that keeps running until the port it destroyed.</span></span>  

<span data-ttu-id="a5f97-197">Pour Microsoft Edge, une fois qu’un port de messagerie est créé à l’aide de , Microsoft Edge démarre le port et le maintient en cours d’exécution jusqu’à ce que le `runtime.connectNative` [`AppServiceConnection`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) port soit détruit.</span><span class="sxs-lookup"><span data-stu-id="a5f97-197">For Microsoft Edge, once a messaging port is created using `runtime.connectNative`, Microsoft Edge starts the [`AppServiceConnection`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) and keeps it running until the port is destroyed.</span></span>  <span data-ttu-id="a5f97-198">L’extrait de code suivant montre comment une connexion persistante est établie à partir d’une application UWP.</span><span class="sxs-lookup"><span data-stu-id="a5f97-198">The following snippet shows how a persistent connection is established from within a UWP app.</span></span>  

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```  

#### <a name="non-persistent"></a><span data-ttu-id="a5f97-199">Non persistant</span><span class="sxs-lookup"><span data-stu-id="a5f97-199">Non-persistent</span></span>  

<span data-ttu-id="a5f97-200">Lorsqu’un message est envoyé à l’aide de Chrome, sans créer de port de messagerie, Chrome démarre un nouveau processus d’hôte de messagerie native [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) pour chaque message.</span><span class="sxs-lookup"><span data-stu-id="a5f97-200">When a message is sent using [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) in Chrome, without creating a messaging port, Chrome starts a new native messaging host process for each message.</span></span>  <span data-ttu-id="a5f97-201">Le premier message généré par le processus hôte est géré comme une réponse à la demande d’origine, et tous les autres messages après celui-ci sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="a5f97-201">The first message generated by the host process is handled as a response to the original request, and all other messages after it are ignored.</span></span>  

<span data-ttu-id="a5f97-202">Microsoft Edge arrête et met fin à la connexion une fois que chaque réponse à chaque message a été reçue.</span><span class="sxs-lookup"><span data-stu-id="a5f97-202">Microsoft Edge stops and ends the connection after every response to each message has been received.</span></span>  <span data-ttu-id="a5f97-203">L’extrait de code suivant montre une connexion non persistante établie avec qui sera ensuite terminée dans l’application UWP une fois qu’une demande a été reçue et stockée en tant `AppServiceConnection` que [`AppServiceResponse`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceResponse?view=winrt-19041&preserve-view=true) .</span><span class="sxs-lookup"><span data-stu-id="a5f97-203">The following snippet shows a non-persistent connection that is established with `AppServiceConnection` that will then be terminated within the UWP app after a request has been received and stored as an [`AppServiceResponse`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceResponse?view=winrt-19041&preserve-view=true).</span></span>  

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

### <a name="permission"></a><span data-ttu-id="a5f97-204">Autorisation</span><span class="sxs-lookup"><span data-stu-id="a5f97-204">Permission</span></span>  

<span data-ttu-id="a5f97-205">Pour activer l’utilisation de la messagerie native avec votre extension, pour Chrome et Microsoft Edge, vous devez déclarer `"nativeMessaging"` l’autorisation dans votre `manifest.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="a5f97-205">In order to enable native messaging use with your extension, for both Chrome and Microsoft Edge you must declare the `"nativeMessaging"` permission in you `manifest.json` file.</span></span>  

## <a name="app-services"></a><span data-ttu-id="a5f97-206">Services d’application</span><span class="sxs-lookup"><span data-stu-id="a5f97-206">App services</span></span>  

<span data-ttu-id="a5f97-207">Cette section détaille l’impact des services d’application sur les performances et la mémoire natives de la messagerie native de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a5f97-207">This section details the impact app services has on Microsoft Edge native messaging performance and memory.</span></span>  

### <a name="performance"></a><span data-ttu-id="a5f97-208">Niveau de performance</span><span class="sxs-lookup"><span data-stu-id="a5f97-208">Performance</span></span>  

<span data-ttu-id="a5f97-209">Les services d’application sont « sponsorisés » par l’application au premier plan qui les appelle à des fins de messagerie native: Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a5f97-209">App services are "sponsored" by the foreground app that calls them which for native messaging purposes is Microsoft Edge.</span></span>  <span data-ttu-id="a5f97-210">Cela signifie que les services d’application peuvent s’exécuter tant que Microsoft Edge est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a5f97-210">This means that app services can run as long as Microsoft Edge is running.</span></span>  

<span data-ttu-id="a5f97-211">En ce qui concerne la latence, les services d’application utilisent des canaux nommés qui, après la connexion initiale, permettent à deux applications de communiquer directement.</span><span class="sxs-lookup"><span data-stu-id="a5f97-211">In regards to latency, app services use named pipes that, after initial connection, allow two apps to directly communicate.</span></span>  <span data-ttu-id="a5f97-212">Cette méthode de communication produit une faible latence.</span><span class="sxs-lookup"><span data-stu-id="a5f97-212">This method of communication produces low latency.</span></span>  <span data-ttu-id="a5f97-213">Les appareils avec des processeurs lents rencontreront une certaine latence initiale après le démarrage du processus qui héberge le service d’application \(~80 ms pour démarrer la tâche en arrière-plan sur certains appareils\).</span><span class="sxs-lookup"><span data-stu-id="a5f97-213">Devices with slow CPUs will experience some initial latency after starting up the process that hosts the app service \(~80ms to startup the background task on some devices\).</span></span>  <span data-ttu-id="a5f97-214">Après le démarrage, les performances sur les appareils de processeur lents doivent être bonnes.</span><span class="sxs-lookup"><span data-stu-id="a5f97-214">After start-up, performance on slow CPU devices should be good.</span></span>  

### <a name="memory"></a><span data-ttu-id="a5f97-215">Mémoire</span><span class="sxs-lookup"><span data-stu-id="a5f97-215">Memory</span></span>  

<span data-ttu-id="a5f97-216">La mémoire allouée à un service d’application est sortie du quota alloué à Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a5f97-216">The memory allocated to an app service is taken out of the quota allocated to Microsoft Edge.</span></span>  <span data-ttu-id="a5f97-217">Cela signifie que si Microsoft Edge démarre un trop grand nombre de services d’application, il est possible qu’ils n’ont plus de mémoire.</span><span class="sxs-lookup"><span data-stu-id="a5f97-217">This means that if Microsoft Edge starts too many app services there is a possibility that they could run out of memory.</span></span>  <span data-ttu-id="a5f97-218">Les limites de mémoire habituelles des tâches en arrière-plan sont appliquées aux services d’application.</span><span class="sxs-lookup"><span data-stu-id="a5f97-218">The usual background task memory caps are enforced on app services.</span></span>  <span data-ttu-id="a5f97-219">Par exemple, sur un appareil de 512 Mo, une tâche en arrière-plan du service d’application ne peut pas être supérieure à 16 Mo.</span><span class="sxs-lookup"><span data-stu-id="a5f97-219">For instance, on a 512MB device an app service background task can be no larger than 16MB.</span></span>  <span data-ttu-id="a5f97-220">Ce nombre monte à mesure que les appareils sont mis à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="a5f97-220">This number goes up as the devices scale up.</span></span>  

## <a name="creating-an-extension-with-native-messaging"></a><span data-ttu-id="a5f97-221">Création d’une extension avec la messagerie native</span><span class="sxs-lookup"><span data-stu-id="a5f97-221">Creating an extension with native messaging</span></span>  

<span data-ttu-id="a5f97-222">Pour tester la messagerie native, votre extension a besoin d’un nom de famille de packages.</span><span class="sxs-lookup"><span data-stu-id="a5f97-222">In order to test native messaging, your extension needs a Package Family Name.</span></span>  <span data-ttu-id="a5f97-223">Microsoft Edge l’utilise pour déterminer l’identité d’hôte de message native, ce qui signifie que votre extension doit être empaqueté.</span><span class="sxs-lookup"><span data-stu-id="a5f97-223">Microsoft Edge uses this to determine the native message host identity, which means your extension should be packaged.</span></span>  

<span data-ttu-id="a5f97-224">Pour créer votre extension avec la messagerie native dans Visual Studio :</span><span class="sxs-lookup"><span data-stu-id="a5f97-224">To create your extension with native messaging in Visual Studio:</span></span>  

1.  <span data-ttu-id="a5f97-225">Créez un projet UWP dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a5f97-225">Create a UWP project in Visual Studio.</span></span>  
1.  <span data-ttu-id="a5f97-226">[Ajouter `AppService` à votre application UWP.](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service)</span><span class="sxs-lookup"><span data-stu-id="a5f97-226">[Add `AppService` to your UWP app](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span></span>  
    *   <span data-ttu-id="a5f97-227">Vous pouvez éventuellement [configurer pour `AppService` être hébergé](/windows/uwp/launch-resume/convert-app-service-in-process) dans l’application principale au lieu d’une tâche en arrière-plan à ce stade.</span><span class="sxs-lookup"><span data-stu-id="a5f97-227">You can optionally [configure `AppService` to be hosted in the main app](/windows/uwp/launch-resume/convert-app-service-in-process) instead of as a background task at this point.</span></span>  
1.  <span data-ttu-id="a5f97-228">Créez et testez votre projet UWP.</span><span class="sxs-lookup"><span data-stu-id="a5f97-228">Build and test your UWP project.</span></span>  
    *   <span data-ttu-id="a5f97-229">Vous pouvez éventuellement ajouter un [composant Pont du bureau.](#adding-a-desktop-bridge-component)</span><span class="sxs-lookup"><span data-stu-id="a5f97-229">You can optionally add a [Desktop Bridge component](#adding-a-desktop-bridge-component).</span></span>  
1.  <span data-ttu-id="a5f97-230">Créez une extension Microsoft Edge qui utilise la messagerie native pour communiquer avec l’application complémentaire UWP.</span><span class="sxs-lookup"><span data-stu-id="a5f97-230">Create a Microsoft Edge extension that uses native messaging to communicate with the UWP companion app.</span></span>  <span data-ttu-id="a5f97-231">Les fichiers d’extension peuvent être ajoutés dans un dossier nommé `Extension` dans le projet UWP.</span><span class="sxs-lookup"><span data-stu-id="a5f97-231">The extension files can be added into a folder named `Extension` in the UWP project.</span></span>  <span data-ttu-id="a5f97-232">Tous les fichiers sous ce dossier, y compris les sous-dossiers, doivent avoir leurs propriétés configurées de la sorte `Build Action=Content` et `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="a5f97-232">All of the files underneath this folder, including subfolders, need to have their properties configured such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span>  <span data-ttu-id="a5f97-233">`manifest.json`Assurez-vous qu’elle est également configurée avec ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a5f97-233">Make sure `manifest.json` is also configured with these properties.</span></span>  
1.  <span data-ttu-id="a5f97-234">Modifiez le `package.manifest.xml` fichier dans le projet pour inclure les métadonnées d’extension et convertissez-le en application sans en-tête en ajoutant `AppListEntry="none"` :</span><span class="sxs-lookup"><span data-stu-id="a5f97-234">Modify the `package.manifest.xml` file in the project to include extension metadata and convert it to a headless app by adding `AppListEntry="none"`:</span></span>  
    
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
    
1.  <span data-ttu-id="a5f97-235">Utilisez le `AppService` nom configuré pour la UWP dans les API de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="a5f97-235">Use the `AppService` name configured for the UWP in the native messaging APIs.</span></span>  
1.  <span data-ttu-id="a5f97-236">Créez [et déployez](#deploying) le projet UWP \(avec le composant Pont du bureau facultatif\).</span><span class="sxs-lookup"><span data-stu-id="a5f97-236">Build and [deploy](#deploying) the UWP project \(with the optional Desktop Bridge component\).</span></span>  
1.  <span data-ttu-id="a5f97-237">[Mettre en package](#packaging) votre extension de messagerie native une fois qu’elle est prête pour la soumission au Store</span><span class="sxs-lookup"><span data-stu-id="a5f97-237">[Package](#packaging) your native messaging extension once it is ready for Store submission</span></span>  
    
> [!NOTE]
> <span data-ttu-id="a5f97-238">Référencez la section [Démonstrations](#demos) pour obtenir un exemple d’extension de messagerie native complète.</span><span class="sxs-lookup"><span data-stu-id="a5f97-238">Reference the [Demos](#demos) section for an example of a complete native messaging extension.</span></span>  

## <a name="adding-a-desktop-bridge-component"></a><span data-ttu-id="a5f97-239">Ajout d’un composant Pont du bureau</span><span class="sxs-lookup"><span data-stu-id="a5f97-239">Adding a Desktop Bridge component</span></span>  

<span data-ttu-id="a5f97-240">Si vous souhaitez ajouter un composant Pont du bureau à votre package, vous devez créer et générer votre projet Win32 dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a5f97-240">If you want to add a Desktop Bridge component to your package, you must create and build your Win32 project in Visual Studio.</span></span>  <span data-ttu-id="a5f97-241">Pour plus d’informations sur la conversion de votre application win32 en UWP, voir Portage d’applications vers [Windows 10 via Desktop Bridge.](/windows/uwp/porting/desktop-to-uwp-root)</span><span class="sxs-lookup"><span data-stu-id="a5f97-241">For info on how to convert your win32 app to UWP, see [Porting apps to Windows 10 via Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root).</span></span>  <span data-ttu-id="a5f97-242">Une fois Visual Studio, vous pouvez ajouter l’exécutable Win32 au package en suivant les étapes ci-après :</span><span class="sxs-lookup"><span data-stu-id="a5f97-242">Once built in Visual Studio, you can add the Win32 executable to the package by doing the following steps:</span></span>  

1.  <span data-ttu-id="a5f97-243">Ajoutez le projet Win32 à la même solution que le projet UWP.</span><span class="sxs-lookup"><span data-stu-id="a5f97-243">Add the Win32 project to the same solution as the UWP project.</span></span>  
1.  <span data-ttu-id="a5f97-244">Définissez le projet Win32 en tant que projet dépendant pour le projet UWP :</span><span class="sxs-lookup"><span data-stu-id="a5f97-244">Set the Win32 project as a dependent project for the UWP project:</span></span>  
    
    ![configuration des dépendances de projet](../media/project-dependencies.png)  
    
1.  <span data-ttu-id="a5f97-246">Créez `Win32` un dossier dans le projet UWP.</span><span class="sxs-lookup"><span data-stu-id="a5f97-246">Create a `Win32` folder within the UWP project.</span></span>  <span data-ttu-id="a5f97-247">Copiez les fichiers binaires nécessaires pour `Win32` le projet dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="a5f97-247">Copy the necessary binaries for the `Win32` project to this folder.</span></span>  <span data-ttu-id="a5f97-248">Configurez les propriétés de tous les binaires de telle sorte que `Build Action=Content` et `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="a5f97-248">Configure the properties of all the binaries such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span>  
    
    ![dossier contenant des fichiers d’application win32 et UWP](../media/desktop-bridge.png)  
    
1.  <span data-ttu-id="a5f97-250">Modifiez le fichier de projet UWP pour copier tous les fichiers binaires nécessaires pour le projet dans ce dossier à l’aide de la commande `Win32` d’événement PostBuild.</span><span class="sxs-lookup"><span data-stu-id="a5f97-250">Modify the UWP project file to copy all the necessary binaries for the `Win32` project into this folder using PostBuild event command.</span></span>  <span data-ttu-id="a5f97-251">Cela garantit que les fichiers binaires mis à jour sont copiés dans le dossier à chaque reconstruction de la solution.</span><span class="sxs-lookup"><span data-stu-id="a5f97-251">This ensures that the updated binaries are being copied to the folder every time the solution is rebuilt.</span></span>  
    
    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```  
    
1.  <span data-ttu-id="a5f97-252">Modifiez `package.manifest.xml` en ajoutant `<desktop:Extension>` l’élément à `<Extensions>` l’élément :</span><span class="sxs-lookup"><span data-stu-id="a5f97-252">Modify `package.manifest.xml` by adding the `<desktop:Extension>` element to the `<Extensions>` element:</span></span>  
    
    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```  
    
## <a name="deploying"></a><span data-ttu-id="a5f97-253">Déploiement</span><span class="sxs-lookup"><span data-stu-id="a5f97-253">Deploying</span></span>  

<span data-ttu-id="a5f97-254">Une fois que vous avez configuré votre projet UWP \(et éventuellement le projet Win32\) comme indiqué ci-dessus, vous êtes prêt à déployer la solution à l’aide de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a5f97-254">Once you have configured your UWP project \(and optionally Win32 project\) as outlined above, you are ready to deploy the solution using Visual Studio.</span></span>  

![projet inprocess de build](../media/native-message-uwp-debug.png)  

<span data-ttu-id="a5f97-256">Une fois la solution correctement déployée, vous devez voir votre extension dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a5f97-256">Once the solution is correctly deployed, you should see your extension in Microsoft Edge.</span></span>  

![extension s’affichant dans Microsoft Edge](../media/secureextension.png)  

## <a name="packaging"></a><span data-ttu-id="a5f97-258">Packages</span><span class="sxs-lookup"><span data-stu-id="a5f97-258">Packaging</span></span>  

> [!NOTE]
> <span data-ttu-id="a5f97-259">L’envoi d’une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte.</span><span class="sxs-lookup"><span data-stu-id="a5f97-259">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="a5f97-260">[Envoyez une demande](https://developer.microsoft.com/microsoft-edge/extensions/requests/) pour faire partie du Microsoft Store et être pris en compte pour les futures mises à jour.</span><span class="sxs-lookup"><span data-stu-id="a5f97-260">[Send a request](https://developer.microsoft.com/microsoft-edge/extensions/requests/) to be a part of the Microsoft Store, and be considered for future updates.</span></span>  

<span data-ttu-id="a5f97-261">Vous pouvez générer un package du Windows Store pour la soumission au Centre de Visual Studio Windows :</span><span class="sxs-lookup"><span data-stu-id="a5f97-261">You may generate a Store package for submission to the Windows Dev Center using built-in Visual Studio functionality:</span></span>  

![Création d’un package store](../media/create-store-package.png)  

## <a name="debugging"></a><span data-ttu-id="a5f97-263">Débogage</span><span class="sxs-lookup"><span data-stu-id="a5f97-263">Debugging</span></span>  

<span data-ttu-id="a5f97-264">Les instructions de débogage varient en fonction du composant que vous souhaitez tester :</span><span class="sxs-lookup"><span data-stu-id="a5f97-264">The instructions for debugging vary depending on which component you want to test out:</span></span>  

### <a name="debugging-the-extension"></a><span data-ttu-id="a5f97-265">Débogage de l’extension</span><span class="sxs-lookup"><span data-stu-id="a5f97-265">Debugging the extension</span></span>  

<span data-ttu-id="a5f97-266">Une fois la solution déployée, l’extension est installée dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a5f97-266">Once the solution is deployed, the extension will be installed in Microsoft Edge.</span></span>  <span data-ttu-id="a5f97-267">Consultez le guide [de débogage](./debugging-extensions.md) pour plus d’informations sur le débogage d’une extension.</span><span class="sxs-lookup"><span data-stu-id="a5f97-267">Check out the [Debugging](./debugging-extensions.md) guide for info on how to debug an extension.</span></span>  

### <a name="debugging-the-uwp-app"></a><span data-ttu-id="a5f97-268">Débogage de l’application UWP</span><span class="sxs-lookup"><span data-stu-id="a5f97-268">Debugging the UWP app</span></span>  

<span data-ttu-id="a5f97-269">L’application UWP se lance lorsque l’extension tente de s’y connecter à l’aide des [API de messagerie native.](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative)</span><span class="sxs-lookup"><span data-stu-id="a5f97-269">The UWP app will launch when the extension tries to connect to it using [native messaging APIs](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span>  <span data-ttu-id="a5f97-270">Vous ne devez déboguer l’application UWP qu’une fois le processus commencé.</span><span class="sxs-lookup"><span data-stu-id="a5f97-270">You must debug the UWP app only once the process starts.</span></span>  <span data-ttu-id="a5f97-271">Cela peut être configuré à l’aide de la page Propriété du projet :</span><span class="sxs-lookup"><span data-stu-id="a5f97-271">This may be configured using the Property page of the project:</span></span>  

1.  <span data-ttu-id="a5f97-272">Dans Visual Studio, pointez sur votre projet d’application UWP et ouvrez le menu contextuel \(clic droit\)</span><span class="sxs-lookup"><span data-stu-id="a5f97-272">In Visual Studio, hover on your UWP app project and open the contextual menu \(right-click\)</span></span>  
1.  <span data-ttu-id="a5f97-273">Sélectionner des **propriétés**</span><span class="sxs-lookup"><span data-stu-id="a5f97-273">Select **Properties**</span></span>  
1.  <span data-ttu-id="a5f97-274">Vérifier **ne pas lancer, mais déboguer mon code au démarrage**</span><span class="sxs-lookup"><span data-stu-id="a5f97-274">Check **Do not launch, but debug my code when it starts**</span></span>  
    
    ![sélection de ne pas lancer la zone](../media/native-message-do-not-launch.png)  
    
<span data-ttu-id="a5f97-276">Dans Visual Studio vous pouvez désormais définir des points d’arrêt dans le code où vous souhaitez déboguer, puis lancer le déboguer en appuyant sur F5.</span><span class="sxs-lookup"><span data-stu-id="a5f97-276">In Visual Studio you can now set breakpoints in the code where you want to debug, then launch the debugger by pressing F5.</span></span>  <span data-ttu-id="a5f97-277">Une fois que vous interagissez avec l’extension pour vous connecter à l’application UWP, Visual Studio s’attache automatiquement au processus.</span><span class="sxs-lookup"><span data-stu-id="a5f97-277">Once you interact with the extension to connect to the UWP app, Visual Studio will automatically attach to the process.</span></span>  

### <a name="debugging-the-desktop-bridge"></a><span data-ttu-id="a5f97-278">Débogage du Pont du bureau</span><span class="sxs-lookup"><span data-stu-id="a5f97-278">Debugging the Desktop Bridge</span></span>  

<span data-ttu-id="a5f97-279">Même s’il [](/windows/msix/desktop/desktop-to-uwp-debug) existe différentes méthodes de débogage d’une application Pont du bureau \(application Win32 convertie\), la seule méthode applicable pour ce scénario est l’option PLMDebug.</span><span class="sxs-lookup"><span data-stu-id="a5f97-279">Even though there are various [methods for debugging a Desktop Bridge](/windows/msix/desktop/desktop-to-uwp-debug) \(converted Win32 app\), the only one applicable for this scenarios is the PLMDebug option.</span></span>  <span data-ttu-id="a5f97-280">Vous pouvez également ajouter du code de débogage à la fonction de démarrage pour effectuer une attente pendant une heure spécifique, ce qui vous permet d’attacher des Visual Studio au processus.</span><span class="sxs-lookup"><span data-stu-id="a5f97-280">You could also add debugging code to the startup function to perform a wait for a specific time, allowing you to attach Visual Studio to the process.</span></span>  
