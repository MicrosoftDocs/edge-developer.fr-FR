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
# <a name="native-messaging-in-microsoft-edge"></a>Messagerie native dans Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <a name="native-messaging-architecture-overview"></a>Vue d’ensemble de l’architecture de messagerie native  

Avec Windows 10 Creators Update, les extensions Microsoft Edge peuvent utiliser la messagerie native pour communiquer avec une application complémentaire de plateforme Windows universelle \(UWP\).  À un niveau élevé, les extensions Microsoft Edge utilisent les mêmes API pour la messagerie native que les extensions Chrome et Firefox.  Toutefois, l’hôte de messagerie native doit être implémenté à l’aide de la plateforme Windows universelle.  

> [!NOTE]
> La méthode décrite ci-dessous \(connexion à une application UWP via AppService\) est le seul mécanisme pris en charge pour permettre la communication entre les extensions Microsoft Edge et les composants natifs.  Consultez la section [Ajout d’un](#adding-a-desktop-bridge-component) composant Pont du bureau de ce guide pour plus d’informations sur la façon d’activer la communication avec les composants Win32 hérités.  

L’architecture de messagerie native dans Microsoft Edge exploite l’API existante en tant qu’infrastructure de communication entre processus [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) sous-jacente \(IPC\).  Les applications UWP utilisent `AppService` l’API pour communiquer les unes avec les autres.  Pour cette raison, les extensions Microsoft Edge peuvent désormais communiquer avec les applications UWP.  

![architecture de messagerie native](../media/native-messaging-architecture.png)  

### <a name="when-and-when-not-to-use-native-messaging"></a>Quand et quand ne pas utiliser la messagerie native  

La messagerie native ajoute une nouvelle couche à votre extension.  En implémentant une application complémentaire UWP pour votre extension, les possibilités suivantes s’offrent à vous :  

*   Synchronisez les données \(par exemple les informations d’identification\) avec une application UWP complémentaire.  
*   Implémenter des algorithmes de chiffrement/déchiffrement plus puissants qui ne sont pas disponibles dans les API web.  
*   Accéder à des ressources qui ne sont pas accessibles via des API web, par exemple du matériel ou des périphériques USB  

Dans certains cas, la messagerie native ne doit pas être utilisée en raison de restrictions de sécurité ou de stratégie :  

*   Modification des paramètres utilisateur dans Microsoft Edge ou Windows, par exemple en modifiant le navigateur ou le moteur de recherche par défaut.  
*   Actions qui violent les stratégies du Microsoft Store pour les applications et les extensions.  
*   Transfert de données vers un point de terminaison distant via l’hôte de message natif.  
*   Autoriser d’autres applications à télécharger du contenu qui modifie le comportement de l’extension.  

## <a name="demos"></a>Démos  

Pour avoir une idée de ce à quoi ressemble une extension de messagerie native Microsoft Edge qui possède à la fois une application UWP et un pont du bureau, consultez les exemples [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) et [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) sur GitHub.  

### <a name="how-it-works"></a>Fonctionnement  

Le composant d’extension Microsoft Edge de l’exemple utilise son script de contenu pour détecter quand un utilisateur tape des informations qui doivent être chiffrées.  L’extension communique cela au composant Pont du bureau via la messagerie native.  Lorsque l’utilisateur est prêt à envoyer les données, l’extension retourne une valeur chiffrée au site web.  

> [!NOTE]
> Cet exemple fonctionne uniquement sur une page web qui utilise des événements personnalisés pour communiquer avec le script de contenu de l’extension.  L’exemple de dossier inclut [un fichier .html avec](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) qui tester l’extension.  

Dans cet exemple, l’application UWP est utilisée pour transmettre des réponses du Pont du bureau à Microsoft Edge, qui est ensuite envoyée à l’extension Microsoft Edge par rappel.  Bien que cet exemple exécute l’hôte de messagerie native dans l’application principale, il peut également s’exécuter en tant que tâche en arrière-plan.  Le basculement entre les deux nécessite la modification du script d’arrière-plan de l’extension, en modifiant la chaîne à `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` l’intérieur de `"NativeMessagingHostOutOfProcess"` .  

## <a name="chrome-vs-microsoft-edge-implementation"></a>Implémentation de Chrome et Microsoft Edge  

Bien que Chrome utilise les API de transmission de messages pour leurs extensions afin de communiquer avec les applications, Microsoft Edge utilise l’API qui permet désormais aux extensions Microsoft Edge et aux applications UWP de [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) communiquer.  

Cette section détaille les différences entre la façon dont Chrome et Microsoft Edge gèrent l’implémentation de la messagerie native.  

### <a name="registration-and-host-manifest"></a>Inscription et manifeste de l’hôte  

Pour que votre application soit reconnue par votre extension en tant qu’hôte de messagerie natif, elle doit être inscrite.  

Pour [l’inscription](https://developer.chrome.com/extensions/nativeMessaging) de l’hôte de messagerie native Chrome, votre application doit installer un fichier manifeste n’importe où dans le système de fichiers Windows qui définit la configuration de l’hôte de messagerie native.  

Le JSON suivant est un exemple de paramètres pour le fichier de configuration :  

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

Pour installer ce fichier, l’application doit :  

1.  Enregistrez le fichier manifeste à un emplacement prédéféré dans le Registre qui définit la configuration de l’hôte :  
    *   `HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
        or  
    *   `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
1.  Définissez la valeur par défaut de cette clé sur le chemin d’accès complet au fichier manifeste, par exemple `[HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"`  

Pour Microsoft Edge, pour inscrire un \(hôte de messagerie natif\), vous devez inclure l’application complémentaire UWP dans le même package que votre extension et spécifier [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) [l’extension AppService](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) dans le fichier de votre `Package.appxmanifest` projet.  Les `EntryPoint` `Name` attributs et les attributs peuvent être configurés par vous :  

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

Vous devez également définir les extensions autorisées à se connecter au service.  Étant donné que Microsoft Edge n’a pas de propriété de manifeste équivalente dans son AppxManifest, cela doit être déterminé et appliqué lors de l’exécution par `"allowed_origins"` votre application UWP.  Étant donné que Microsoft Edge établit la connexion pour le compte de l’extension, l’application recherche le nom de la famille de packages de l’appelant pour déterminer si le poste est connecté par Microsoft Edge pour contrôler ou authentifier l’appelant.  Par exemple   

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

### <a name="message-sending"></a>Envoi de messages  

Pour qu’une application et une extension communiquent entre elles, des messages doivent être envoyés vers et depuis eux.  

Les extensions Chrome lancent un message à l’aide de l’API pour remettre un message à l’hôte natif à l’aide d’un canal [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) non persistant.  

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```  

Le premier paramètre est le nom de l’hôte natif, que Chrome recherche dans le Registre pour le manifeste.  Le manifeste spécifie le .exe que Chrome lancera dans un bac à sable et le message est envoyé à l’aide de std i/o.  
Les extensions établissent également un canal persistant à l’aide de l’API, qui prend le nom de l’hôte `runtime.connectNative` natif comme seul paramètre.  

Microsoft Edge utilise la même construction que l’API de messagerie native dans Chrome pour permettre aux extensions Microsoft Edge de spécifier le service d’application auquel se connecter.  Le premier paramètre dans `runtime.sendNativeMessage` spécifie le nom du service d’application.  Dans la section [Inscription et manifeste de l’hôte,](#registration-and-host-manifest) il s’agit de `"com.microsoft.inventory"` .  La plateforme d’extension Microsoft Edge limite l’hôte de messagerie natif à être une application UWP empaqueté dans le même AppX que l’extension.  Cela permet d’atténuer les risques de sécurité associés aux attaques malveillantes qui tentent de connecter Microsoft Edge à un autre nom de famille de packages en falsifiant les entrées de manifeste.  

Cela signifie que Microsoft Edge utilisera le même nom de famille de package que l’extension, en plus du nom spécifié dans l’API, pour identifier de manière unique le fournisseur du `AppService` service d’application.  

> [!NOTE]
> Cela ne sera pas facilement converti par l’extension [Microsoft Edge Shared Computer Toolkit](./porting-chrome-extensions.md).  Toutes les extensions qui spécifient l’autorisation sont signalées comme nécessitant `"nativeMessaging"` une conversion manuelle pour ce composant.  

### <a name="communication-protocol"></a>Protocole de communication  

Le protocole de communication pour la messagerie native détermine la façon dont les messages sont mis en forme avant l’envoi.  

Chrome démarre chaque hôte de messagerie native dans un processus distinct et communique avec lui à l’aide de l’entrée standard et de la sortie standard.  Le même format est utilisé pour envoyer des messages dans les deux sens : chaque message est sérialisé à l’aide de JSON, codé en UTF-8 et est précédé de la longueur des messages 32 bits dans l’ordre d’byte natif.  

Pour Microsoft Edge, la tâche en arrière-plan/l’application principale qui implémente le service d’application sera démarrée par la plateforme.  Au démarrage, la `Run` méthode de la tâche en arrière-plan est invoquée :  

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

Lorsque votre extension envoie un message à votre application UWP, [`onRequestReceived`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) l’événement est levé.  Ce message au format JSON est ensuite stringified dans la première paire KeyValue d’un [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) objet.  :  

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```  

Lorsque votre application UWP renvoie une réponse à votre extension, une réponse est [`KeyValuePair`](/dotnet/api/system.collections.generic.keyvaluepair-2?view=netcore-3.1&preserve-view=true) ajoutée à `ValueSet` l’objet.  La propriété est ignorée par Microsoft Edge, mais elle contient `Key` `Value` une chaîne JSON valide.  

### <a name="callback"></a>Rappel  

Pour les rappels, Chrome utilise ce qui permet à une fonction de rappel de gérer toute réponse asynchrone lors de [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) l’envoi d’un message.  

Microsoft Edge utilise la méthode de l’objet pour que l’application renvoie [`SendResponseAsync`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) [`AppServiceRequest`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) un objet à [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) l’extension.  

### <a name="message-size-limit"></a>Limite de taille des messages  

Les messages envoyés entre une extension et une application ont des limites de taille de message différentes pour Chrome et Microsoft Edge.  

Chrome présente les limites de taille de message suivantes :  

*   Limite de message unique de l’hôte de messagerie native : 1 Mo  
*   Limite de message unique envoyée à l’hôte de messagerie native : 4 Go  

Pour Microsoft Edge, bien qu’il n’y ait aucune limite sur la taille des messages \(dépendant de la mémoire\), Microsoft Edge se protège contre les erreurs de comportement des applications natives en maintenant les limites de taille de `AppService` message suivantes :  

*   Limite de message unique entre l’application UWP et l’extension : 1 Mo  
*   Limite de message unique entre l’extension et l’application UWP : 100 Mo  

### <a name="native-messaging-connections"></a>Connexions de messagerie natives  

Il existe deux types de connexions pour la messagerie native ; persistantes et non persistantes.  
Une **connexion persistante** est une connexion qui est en cours d’exécution jusqu’à ce que le port soit détruit.  Une **connexion non persistante** est une connexion ouverte pour un message à la fois et qui se ferme après la remise.  

#### <a name="persistent"></a>Persistance  

Pour Chrome, une connexion permanente est réalisée en créant un port de messagerie à l’aide [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) de .  Une fois le port effectué, Chrome démarre un processus d’hôte de messagerie natif qui continue à s’exécute jusqu’au port qu’il a détruit.  

Pour Microsoft Edge, une fois qu’un port de messagerie est créé à l’aide de , Microsoft Edge démarre le port et le maintient en cours d’exécution jusqu’à ce que le `runtime.connectNative` [`AppServiceConnection`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) port soit détruit.  L’extrait de code suivant montre comment une connexion persistante est établie à partir d’une application UWP.  

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```  

#### <a name="non-persistent"></a>Non persistant  

Lorsqu’un message est envoyé à l’aide de Chrome, sans créer de port de messagerie, Chrome démarre un nouveau processus d’hôte de messagerie native [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) pour chaque message.  Le premier message généré par le processus hôte est géré comme une réponse à la demande d’origine, et tous les autres messages après celui-ci sont ignorés.  

Microsoft Edge arrête et met fin à la connexion une fois que chaque réponse à chaque message a été reçue.  L’extrait de code suivant montre une connexion non persistante établie avec qui sera ensuite terminée dans l’application UWP une fois qu’une demande a été reçue et stockée en tant `AppServiceConnection` que [`AppServiceResponse`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceResponse?view=winrt-19041&preserve-view=true) .  

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

### <a name="permission"></a>Autorisation  

Pour activer l’utilisation de la messagerie native avec votre extension, pour Chrome et Microsoft Edge, vous devez déclarer `"nativeMessaging"` l’autorisation dans votre `manifest.json` fichier.  

## <a name="app-services"></a>Services d’application  

Cette section détaille l’impact des services d’application sur les performances et la mémoire natives de la messagerie native de Microsoft Edge.  

### <a name="performance"></a>Niveau de performance  

Les services d’application sont « sponsorisés » par l’application au premier plan qui les appelle à des fins de messagerie native: Microsoft Edge.  Cela signifie que les services d’application peuvent s’exécuter tant que Microsoft Edge est en cours d’exécution.  

En ce qui concerne la latence, les services d’application utilisent des canaux nommés qui, après la connexion initiale, permettent à deux applications de communiquer directement.  Cette méthode de communication produit une faible latence.  Les appareils avec des processeurs lents rencontreront une certaine latence initiale après le démarrage du processus qui héberge le service d’application \(~80 ms pour démarrer la tâche en arrière-plan sur certains appareils\).  Après le démarrage, les performances sur les appareils de processeur lents doivent être bonnes.  

### <a name="memory"></a>Mémoire  

La mémoire allouée à un service d’application est sortie du quota alloué à Microsoft Edge.  Cela signifie que si Microsoft Edge démarre un trop grand nombre de services d’application, il est possible qu’ils n’ont plus de mémoire.  Les limites de mémoire habituelles des tâches en arrière-plan sont appliquées aux services d’application.  Par exemple, sur un appareil de 512 Mo, une tâche en arrière-plan du service d’application ne peut pas être supérieure à 16 Mo.  Ce nombre monte à mesure que les appareils sont mis à l’échelle.  

## <a name="creating-an-extension-with-native-messaging"></a>Création d’une extension avec la messagerie native  

Pour tester la messagerie native, votre extension a besoin d’un nom de famille de packages.  Microsoft Edge l’utilise pour déterminer l’identité d’hôte de message native, ce qui signifie que votre extension doit être empaqueté.  

Pour créer votre extension avec la messagerie native dans Visual Studio :  

1.  Créez un projet UWP dans Visual Studio.  
1.  [Ajouter `AppService` à votre application UWP.](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service)  
    *   Vous pouvez éventuellement [configurer pour `AppService` être hébergé](/windows/uwp/launch-resume/convert-app-service-in-process) dans l’application principale au lieu d’une tâche en arrière-plan à ce stade.  
1.  Créez et testez votre projet UWP.  
    *   Vous pouvez éventuellement ajouter un [composant Pont du bureau.](#adding-a-desktop-bridge-component)  
1.  Créez une extension Microsoft Edge qui utilise la messagerie native pour communiquer avec l’application complémentaire UWP.  Les fichiers d’extension peuvent être ajoutés dans un dossier nommé `Extension` dans le projet UWP.  Tous les fichiers sous ce dossier, y compris les sous-dossiers, doivent avoir leurs propriétés configurées de la sorte `Build Action=Content` et `Copy to Output Directory=Copy Always` .  `manifest.json`Assurez-vous qu’elle est également configurée avec ces propriétés.  
1.  Modifiez le `package.manifest.xml` fichier dans le projet pour inclure les métadonnées d’extension et convertissez-le en application sans en-tête en ajoutant `AppListEntry="none"` :  
    
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
    
1.  Utilisez le `AppService` nom configuré pour la UWP dans les API de messagerie native.  
1.  Créez [et déployez](#deploying) le projet UWP \(avec le composant Pont du bureau facultatif\).  
1.  [Mettre en package](#packaging) votre extension de messagerie native une fois qu’elle est prête pour la soumission au Store  
    
> [!NOTE]
> Référencez la section [Démonstrations](#demos) pour obtenir un exemple d’extension de messagerie native complète.  

## <a name="adding-a-desktop-bridge-component"></a>Ajout d’un composant Pont du bureau  

Si vous souhaitez ajouter un composant Pont du bureau à votre package, vous devez créer et générer votre projet Win32 dans Visual Studio.  Pour plus d’informations sur la conversion de votre application win32 en UWP, voir Portage d’applications vers [Windows 10 via Desktop Bridge.](/windows/uwp/porting/desktop-to-uwp-root)  Une fois Visual Studio, vous pouvez ajouter l’exécutable Win32 au package en suivant les étapes ci-après :  

1.  Ajoutez le projet Win32 à la même solution que le projet UWP.  
1.  Définissez le projet Win32 en tant que projet dépendant pour le projet UWP :  
    
    ![configuration des dépendances de projet](../media/project-dependencies.png)  
    
1.  Créez `Win32` un dossier dans le projet UWP.  Copiez les fichiers binaires nécessaires pour `Win32` le projet dans ce dossier.  Configurez les propriétés de tous les binaires de telle sorte que `Build Action=Content` et `Copy to Output Directory=Copy Always` .  
    
    ![dossier contenant des fichiers d’application win32 et UWP](../media/desktop-bridge.png)  
    
1.  Modifiez le fichier de projet UWP pour copier tous les fichiers binaires nécessaires pour le projet dans ce dossier à l’aide de la commande `Win32` d’événement PostBuild.  Cela garantit que les fichiers binaires mis à jour sont copiés dans le dossier à chaque reconstruction de la solution.  
    
    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```  
    
1.  Modifiez `package.manifest.xml` en ajoutant `<desktop:Extension>` l’élément à `<Extensions>` l’élément :  
    
    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```  
    
## <a name="deploying"></a>Déploiement  

Une fois que vous avez configuré votre projet UWP \(et éventuellement le projet Win32\) comme indiqué ci-dessus, vous êtes prêt à déployer la solution à l’aide de Visual Studio.  

![projet inprocess de build](../media/native-message-uwp-debug.png)  

Une fois la solution correctement déployée, vous devez voir votre extension dans Microsoft Edge.  

![extension s’affichant dans Microsoft Edge](../media/secureextension.png)  

## <a name="packaging"></a>Packages  

> [!NOTE]
> L’envoi d’une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte.  [Envoyez une demande](https://developer.microsoft.com/microsoft-edge/extensions/requests/) pour faire partie du Microsoft Store et être pris en compte pour les futures mises à jour.  

Vous pouvez générer un package du Windows Store pour la soumission au Centre de Visual Studio Windows :  

![Création d’un package store](../media/create-store-package.png)  

## <a name="debugging"></a>Débogage  

Les instructions de débogage varient en fonction du composant que vous souhaitez tester :  

### <a name="debugging-the-extension"></a>Débogage de l’extension  

Une fois la solution déployée, l’extension est installée dans Microsoft Edge.  Consultez le guide [de débogage](./debugging-extensions.md) pour plus d’informations sur le débogage d’une extension.  

### <a name="debugging-the-uwp-app"></a>Débogage de l’application UWP  

L’application UWP se lance lorsque l’extension tente de s’y connecter à l’aide des [API de messagerie native.](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative)  Vous ne devez déboguer l’application UWP qu’une fois le processus commencé.  Cela peut être configuré à l’aide de la page Propriété du projet :  

1.  Dans Visual Studio, pointez sur votre projet d’application UWP et ouvrez le menu contextuel \(clic droit\)  
1.  Sélectionner des **propriétés**  
1.  Vérifier **ne pas lancer, mais déboguer mon code au démarrage**  
    
    ![sélection de ne pas lancer la zone](../media/native-message-do-not-launch.png)  
    
Dans Visual Studio vous pouvez désormais définir des points d’arrêt dans le code où vous souhaitez déboguer, puis lancer le déboguer en appuyant sur F5.  Une fois que vous interagissez avec l’extension pour vous connecter à l’application UWP, Visual Studio s’attache automatiquement au processus.  

### <a name="debugging-the-desktop-bridge"></a>Débogage du Pont du bureau  

Même s’il [](/windows/msix/desktop/desktop-to-uwp-debug) existe différentes méthodes de débogage d’une application Pont du bureau \(application Win32 convertie\), la seule méthode applicable pour ce scénario est l’option PLMDebug.  Vous pouvez également ajouter du code de débogage à la fonction de démarrage pour effectuer une attente pendant une heure spécifique, ce qui vous permet d’attacher des Visual Studio au processus.  
