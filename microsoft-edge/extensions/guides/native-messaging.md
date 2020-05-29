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
# Messagerie native dans Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## Présentation de l’architecture de messagerie Native

Avec Windows 10 Creators Update, les extensions Microsoft Edge peuvent utiliser la messagerie native pour communiquer avec une application de plateforme Windows universelle (UWP) complémentaire.  À un niveau élevé, les extensions Microsoft Edge utilisent les mêmes API pour la messagerie Native que les extensions chrome et Firefox. Toutefois, l’hôte de messagerie natif doit être implémenté à l’aide de la plateforme Windows universelle.

> [!NOTE]
> La méthode décrite ci-dessous (la connexion à une application UWP via AppService) est le seul mécanisme pris en charge pour l’activation de la communication entre les extensions Microsoft Edge et les composants natifs. Pour plus d’informations sur l’activation de la communication avec les anciens composants Win32, voir la section [Ajout d’un composant Desktop Bridge](#adding-a-desktop-bridge-component) de ce guide. 

 L’architecture de messagerie native de Microsoft Edge tire parti de l' [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API existante en tant qu’infrastructure de communication entre processus (IPC) sous-jacente. Les applications UWP utilisent l' `AppService` API pour communiquer entre elles. Pour cette raison, les extensions Microsoft Edge peuvent désormais communiquer avec des applications UWP.

![architecture de messagerie Native](./../media/native-messaging-architecture.png)


### Quand et quand ne pas utiliser la messagerie Native

La messagerie Native ajoute un nouveau calque à votre extension. En implémentant une application complémentaire UWP pour votre extension, les possibilités suivantes sont disponibles:

* Synchroniser des données (par exemple, des informations d’identification) avec une application UWP complémentaire.
* Les algorithmes de déchiffrement/déchiffrement renforcés ne sont pas disponibles dans les API Web.
* Accès aux ressources qui ne sont pas accessibles par le biais d’API Web (par exemple, matériel ou périphériques USB);

Dans certains cas, la messagerie Native ne peut pas être utilisée en raison de restrictions de sécurité ou de stratégie:

* Modification des paramètres de l’utilisateur dans Microsoft Edge ou Windows, par exemple, la modification du navigateur par défaut ou du fournisseur de recherche;
* Actions qui enfreignent les stratégies du Windows Store pour les applications et les extensions.
* Transfert de données vers un point de terminaison distant via un hôte de message natif.
* Autorisation d’autres applications de télécharger le contenu qui modifie le comportement de l’extension.

## Démos

Pour avoir un aperçu de ce qu’est une extension de messagerie Native Microsoft Edge qui comporte à la fois une application UWP complémentaire et une application de bureau, consultez les exemples [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) et [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) sur GitHub.

### Fonctionnement

Le composant d’extension Microsoft Edge de l’exemple utilise son script de contenu pour détecter lorsqu’un utilisateur tape des informations qui doivent être chiffrées. L’extension communique cela au composant Desktop Bridge par le biais de la messagerie native. Lorsque l’utilisateur est prêt à envoyer les données, l’extension renverra une valeur chiffrée au site Web.

> [!NOTE]
> Cet exemple ne fonctionne que sur une page Web qui utilise des événements personnalisés pour communiquer avec le script de contenu de l’extension. L’exemple de dossier inclut un [fichier. html](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) pour tester l’extension.

Dans cet exemple, l’application UWP est utilisée pour passer les réponses de Desktop Bridge à Microsoft Edge, qui est ensuite envoyée à l’extension Microsoft Edge via le rappel. Dans cet exemple, l’hôte de messagerie natif s’exécute dans l’application principale, il peut également être exécuté en tant que tâche en arrière-plan. Le passage de l’un à l’autre nécessite la modification du script en arrière-plan de l’extension, en modifiant la chaîne à l’intérieur `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` de `"NativeMessagingHostOutOfProcess"` .

## Implémentation de chrome et de Microsoft Edge

Lorsque chrome passe l’itinéraire d’utilisation des API de passage de messages pour leurs extensions de communication avec les applications, Microsoft Edge utilise l' [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API qui permet à l’application Microsoft Edge extensions et aux applications UWP de communiquer.

Cette section décrit en détail les différences qui existent entre le mode chrome et Microsoft Edge et la mise en œuvre de messagerie native.

### Inscription et manifeste d’hébergement
Pour que votre application soit reconnue par votre extension en tant qu’hôte de messagerie natif, vous devez être inscrite.


Pour l’inscription de l’hôte de [messagerie natif de chrome](https://developer.chrome.com/extensions/nativeMessaging) , votre application doit installer un fichier manifeste en tout lieu dans le système de fichiers Windows qui définit la configuration hôte de messagerie native.

Le code JSON suivant est un exemple de la façon dont le fichier de configuration peut être configuré:

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

Pour installer ce fichier, l’application doit effectuer les opérations suivantes:

1. Enregistrez le fichier manifeste dans un emplacement prédéfini du Registre qui définit la configuration d’hôte:
   - `HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`

     ou
   - `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`

2. Définissez la valeur par défaut de cette clé sur le chemin d’accès complet au fichier manifeste (par exemple,  `[HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"`




Pour Microsoft Edge, afin d’inscrire un [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) (hôte de messagerie natif), vous devez inclure l’application compagnon UWP dans le même package que votre extension et spécifier l' [extension AppService](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) dans le fichier de votre projet `Package.appxmanifest` . Les `EntryPoint` `Name` attributs et peuvent être configurés comme suit:

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


Vous devez également définir quelles extensions sont autorisées à se connecter au service. Dans la mesure où Microsoft Edge ne possède pas `"allowed_origins"` de propriété de manifeste équivalente dans son AppxManifest, il doit être déterminé et appliqué lors de l’exécution par votre application UWP. Dans la mesure où Microsoft Edge établit la connexion de la part de l’extension, l’application peut chercher le nom de la famille de packages de l’appelant afin de déterminer s’il est connecté par Microsoft Edge pour contrôler ou authentifier l’appelant. Par exemple, 

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



### Envoi de messages

Pour qu’une application et une extension puissent communiquer entre elles, les messages doivent être envoyés vers et à partir de celles-ci.

Les extensions chrome déclenchent un message à l’aide de l' [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API pour envoyer un message à l’hôte natif à l’aide d’un canal non persistant. 

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```

Le premier paramètre est le nom de l’hôte natif, lequel recherche chrome dans le registre pour le manifeste. Le manifeste spécifie le fichier. exe dans lequel le chrome sera lancé dans un bac à sable (sandbox), et le message est envoyé à l’aide du standard d’e/s. Les extensions peuvent également établir un canal permanent à l’aide de l' `runtime.connectNative` API, qui prend le nom de l’hôte natif en tant que paramètre unique. 

Microsoft Edge utilise la même construction que l’API de messagerie native de chrome pour autoriser les extensions Microsoft Edge à spécifier le service d’application auquel se connecter. Le premier paramètre de `runtime.sendNativeMessage` spécifie le nom du service d’application. Dans la section [inscription et manifeste](#registration-and-host-manifest) de l’hôte, il s’agit de `"com.microsoft.inventory"` . La plateforme d’extension Microsoft Edge limite l’hôte de messagerie natif à être une application UWP empaquetée dans le même AppX que l’extension. Cela permet de réduire les risques liés à la sécurité liés aux attaques malveillantes qui essaient de connecter Microsoft Edge avec un autre nom de la famille de packages en falsifiant des entrées de manifeste. 

Cela signifie que Microsoft Edge utilisera le même nom de famille de packages que l’extension, en plus du `AppService` nom spécifié dans l’API, pour identifier de manière unique le fournisseur de service d’application.  

> [!NOTE]
> Le [Kit de connaissances Microsoft Edge extension](./porting-chrome-extensions.md)ne sera pas facilement converti. Toute extension spécifiant l' `"nativeMessaging"` autorisation sera signalée comme nécessitant une conversion manuelle pour ce composant.





### Protocole de communication

Le protocole de communication pour la messagerie Native détermine le mode de mise en forme des messages avant leur envoi.

Chrome démarre chaque hôte de messagerie natif dans un processus distinct et communique avec ce dernier à l’aide d’une entrée standard et d’une sortie standard. Le même format est utilisé pour envoyer des messages dans les deux sens: chaque message est sérialisé en utilisant JSON, UTF-8 encodé et est précédé d’une longueur de message de 32 bits dans l’ordre d’octets natif.


Pour Microsoft Edge, la tâche en arrière-plan/l’application principale qui implémente le service d’application est démarrée par la plateforme. Au démarrage, la méthode de la tâche en arrière-plan est `Run` appelée:  

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

Lorsque votre extension envoie un message à votre application UWP, l' [`onRequestReceived`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection.requestreceived) événement est déclenché. Ce message au format JSON sera alors stringified dans le premier couple KeyValue d’un [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) objet. :

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```

Lorsque votre application UWP envoie de nouveau une réponse à votre extension, une [`KeyValuePair`](https://msdn.microsoft.com/library/windows/apps/5tbh8a42) est ajoutée à l' `ValueSet` objet. La `Key` propriété est ignorée par Microsoft Edge, mais la `Value` propriété contient une chaîne JSON valide.

### Rappeler

Pour les rappels, chrome utilise [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) ce qui permet à une fonction de rappel de gérer toute réponse asynchrone lors de l’envoi d’un message.

Microsoft Edge utilise la [`AppServiceRequest`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest) méthode de l’objet [`SendResponseAsync`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest.sendresponseasync) pour permettre à l’application de renvoyer un [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) objet à l’extension.


### Taille limite du message
Les messages échangés entre une extension et une application présentent des limitations de taille de messages différentes pour chrome et Microsoft Edge.

Chrome a les limites de taille de message suivantes:
- Limite de messages unique de l’hôte de messagerie natif: 1 Mo
- Limite de messages unique envoyée à l’hôte de messagerie natif: 4 Go

Pour Microsoft Edge, sans `AppService` limite de taille de message (en fonction de la quantité de mémoire), Microsoft Edge se protège lui-même contre les applications natives inefficaces en imposant les limites de taille de message suivantes:
- Limite de messages unique de l’application UWP à l’extension: 1 Mo
- Limite de messages unique de l’extension à l’application UWP: 100 Mo



### Connexions de messagerie Native

Il existe deux types de connexions pour la messagerie Native; persistant et non persistant.
Une connexion **permanente** est une connexion qui s’exécute jusqu’à ce que le port soit détruit. Une connexion **non permanente** est une connexion ouverte pour un message à la fois et qui se ferme après la remise.

#### Persistance

Pour Chrome, une connexion permanente est effectuée en créant un port de messagerie à l’aide de [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) . Une fois le port créé, chrome démarre un processus hôte de messagerie natif qui continue de s’exécuter jusqu’à ce qu’il soit détruit.

Dans le cadre de l’utilisation de Microsoft Edge, une fois que vous avez créé un port de messagerie à l’aide de `runtime.connectNative` , Microsoft Edge démarre [`AppServiceConnection`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection) et continue de s’exécuter jusqu’à ce que le port soit détruit. L’extrait de code suivant montre comment une connexion permanente est établie à partir d’une application UWP. 

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```

#### Non permanent

Lors de l’envoi d’un message à l’aide [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) de chrome, sans création de port de messagerie, chrome démarre un nouveau processus hôte de messagerie natif pour chaque message. Le premier message généré par le processus hôte est géré en tant que réponse à la requête d’origine, et tous les autres messages qu’elle contient sont ignorés.

Microsoft Edge va mettre fin à la connexion après la réception de chaque message. L’extrait de code suivant montre une connexion non permanente qui est établie avec celle-ci, `AppServiceConnection` puis arrêtée au sein de l’application UWP après réception d’une demande et stockage en tant que [`AppServiceResponse`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceresponse) .

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

### Autorisation

Afin d’autoriser l’utilisation de la messagerie native avec votre extension, pour chrome et Microsoft Edge, vous devez déclarer l' `"nativeMessaging"` autorisation dans votre `manifest.json` fichier.


## Services d’application
Cette section détaille les services d’application d’impact sur les performances et la mémoire de messagerie native de Microsoft Edge.

### Analyse des performances

Les services d’application sont «parrainés» par l’application au premier plan qui les appelle qui, pour des raisons de messagerie native, est Microsoft Edge. Cela signifie que les services d’application peuvent s’exécuter tant que Microsoft Edge est en cours d’exécution.

En ce qui concerne la latence, les services d’application utilisent des canaux nommés qui, après la connexion initiale, autorisent deux applications à communiquer directement. Cette méthode de communication produit une latence faible. Les appareils équipés de processeurs lents connaissent une latence initiale après le démarrage du processus qui héberge le service d’application (~ 80ms de démarrage de la tâche en arrière-plan sur certains appareils). Après le démarrage, les performances sur les périphériques de processeur lente doivent être efficaces. 


### Mémoire
La mémoire allouée à un service d’application est extraite du quota attribué à Microsoft Edge. Cela signifie que si Microsoft Edge démarre trop de services d’application, il est possible qu’il n’y ait plus de mémoire. Les limites de mémoire de tâches en arrière-plan usuelles sont appliquées aux services d’application. Par exemple, sur un appareil de 512 Mo, une tâche en arrière-plan de service d’application ne peut pas être supérieure à 16 Mo. Ce numéro augmente à mesure que les appareils évoluent.


## Création d’une extension avec la messagerie Native

Pour tester la messagerie native, votre extension doit avoir le nom de la famille de packages. Microsoft Edge utilise cette méthode pour déterminer l’identité de l’hôte de messages natif, ce qui signifie que votre extension doit être empaquetée. 


Pour créer votre extension avec la messagerie native dans Visual Studio:

1. Créer un projet UWP dans Visual Studio.
2. [Ajoutez `AppService` à votre application UWP](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).
   - Vous pouvez éventuellement [configurer `AppService` l’hébergement sur l’application principale](https://msdn.microsoft.com/windows/uwp/launch-resume/convert-app-service-in-process) plutôt que sur une tâche en arrière-plan à ce stade.
3. Générez et testez votre projet UWP.
   - Vous pouvez éventuellement ajouter un [composant Desktop Bridge](#adding-a-desktop-bridge-component).
4. Créez une extension Microsoft Edge qui utilise la messagerie native pour communiquer avec l’application complémentaire UWP. Les fichiers d’extension peuvent être ajoutés dans un dossier nommé `Extension` dans le projet UWP. Tous les fichiers sous ce dossier, y compris les sous-dossiers, doivent avoir leurs propriétés configurées de manière à ce que `Build Action=Content` et `Copy to Output Directory=Copy Always` . Vérifiez qu' `manifest.json` elle est également configurée avec ces propriétés.
5. Modifiez le `package.manifest.xml` fichier dans le projet de façon à inclure les métadonnées d’extension et à le convertir en application headless en ajoutant `AppListEntry="none"` :

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

6. Utilisez le `AppService` nom configuré pour UWP dans les API de messagerie native.
7. Générez et [déployez](#deploying) le projet UWP (avec le composant Desktop Bridge facultatif).
8. [Empaqueter](#packaging) votre extension de messagerie Native une fois qu’elle est prête pour la soumission au Windows Store

> [!NOTE]
> Référencez la section [démonstrations](#demos) pour obtenir un exemple d’extension de messagerie native complète.


## Ajout d’un composant Desktop Bridge 
Si vous souhaitez ajouter un composant Desktop Bridge à votre package, vous devez créer et générer votre projet Win32 dans Visual Studio. Pour plus d’informations sur la conversion de votre application Win32 vers UWP, voir [Portage d’applications vers Windows 10 via Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root). Une fois créé dans Visual Studio, vous pouvez ajouter le code exécutable Win32 au package en procédant comme suit:

1. Ajoutez le projet Win32 dans la même solution que le projet UWP. 

2. Définissez le projet Win32 en tant que projet dépendant pour le projet UWP:

    ![configuration de dépendances de projet](./../media/project-dependencies.PNG)

3. Créer un `Win32` dossier au sein du projet UWP. Copiez les fichiers binaires nécessaires pour le `Win32` projet dans ce dossier. Configurez les propriétés de tous les fichiers binaires, tels que `Build Action=Content` et `Copy to Output Directory=Copy Always` .

    ![dossier contenant les fichiers d’application Win32 et UWP](./../media/desktop-bridge.png)

4. Modifiez le fichier de projet UWP pour copier tous les fichiers binaires nécessaires pour le `Win32` projet dans ce dossier à l’aide de la commande d’événement PostBuild. Cela permet de s’assurer que les fichiers binaires mis à jour sont copiés dans le dossier chaque fois que la solution est reconstruite.

    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```


5. Modifiez `package.manifest.xml` en ajoutant l' `<desktop:Extension>` élément à l' `<Extensions>` élément:

    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```

## Déploiement
Une fois que vous avez configuré votre projet UWP (et éventuellement le projet Win32) comme décrit ci-dessus, vous êtes prêt à déployer la solution à l’aide de Visual Studio.

![créer un projet d’inprocessus](../media/native-message-uwp-debug.PNG)

Lorsque la solution est déployée correctement, vous devriez voir votre extension dans Microsoft Edge.

![extension affichée dans Microsoft Edge](../media/secureextension.png)

## Intégration

> [!NOTE]
> Le fait de soumettre une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte. Contactez [-nous](https://aka.ms/extension-request) pour obtenir vos demandes en tant que partie du Microsoft Store et nous vous enverrons une prochaine mise à jour.


Vous pouvez générer un package de magasin pour la soumission au centre de développement Windows à l’aide de la fonctionnalité intégrée de Visual Studio:


![Création d’un package du Windows Store](../media/create-store-package.PNG)

## Débogage
Les instructions relatives au débogage varient selon le composant que vous voulez tester:

### Débogage de l’extension
Une fois la solution déployée, l’extension sera installée dans Microsoft Edge. Pour plus d’informations sur le débogage d’une extension, voir le Guide de [débogage](./debugging-extensions.md) .


### Débogage de l’application UWP
L’application UWP démarre lorsque l’extension tente de s’y connecter à l’aide des [API de messagerie Native](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative). Vous devez déboguer l’application UWP uniquement une fois le processus démarré. Ce problème peut être configuré via la page de propriétés du projet:

1.  Dans Visual Studio, cliquez avec le bouton droit sur votre projet d’application UWP.
2.  Sélectionner les propriétés
3.  Cochez la case ne pas lancer, mais déboguer mon code au démarrage.

    ![sélection de la zone ne pas lancer](../media/native-message-do-not-launch.png)

Dans Visual Studio, vous pouvez maintenant définir des points d’arrêt dans le code pour lequel vous voulez déboguer, puis lancer le débogueur en appuyant sur F5. Lorsque vous interagissez avec l’extension pour vous connecter à l’application UWP, Visual Studio s’attache automatiquement au processus.


### Débogage de Desktop Bridge
Même s’il existe différentes [méthodes pour le débogage de Desktop Bridge](https://msdn.microsoft.com/windows/uwp/porting/desktop-to-uwp-debug) (application Win32 convertie), la seule application applicable pour ce scénario est l’option PLMDebug. Vous pouvez également ajouter du code de débogage à la fonction de démarrage pour exécuter une attente pour une heure spécifique, ce qui vous permet d’attacher Visual Studio au processus.
