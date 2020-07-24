---
description: Ce guide vous donne une vue d’ensemble des notions de base et des outils de Project Web App pour créer des applications Web progressives sur Windows.
title: Commencer à utiliser les applications Web progressives (chrome)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: applications Web progressives, PWA, Edge, Windows, PWABuilder, le manifeste Web, le travailleur de service, l’émission
ms.openlocfilehash: a9a0cad2d771e52b783053e36f0f23dec5d8e70c
ms.sourcegitcommit: 515522959f517e194f93a27f5d360690600edd9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894709"
---
# Commencer à utiliser les applications Web progressives (chrome)  

Les applications Web progressives (PWAs) sont des applications Web qui sont [progressivement améliorées][WikiProgressiveEnhancement] avec des fonctionnalités de type application, telles que l’installation, la prise en charge hors ligne et les notifications de transmission.  Vous pouvez également empaqueter votre PWA pour les magasins d’applications, y compris le Microsoft Store ainsi que Google Play, Mac App Store et bien plus encore.  Le Microsoft Store est le magasin d’applications commercial intégré à Windows 10.  

Le guide suivant vous donne une vue d’ensemble des concepts de base de la création de Project Web App et l’étend en tant que PWA.  Le projet finalisé fonctionne sur les navigateurs modernes.  

> [!TIP]
> Vous pouvez utiliser [PWABuilder][PwaBuilder] pour créer une nouvelle application Project Web App, améliorer votre version Web.  

## Conditions préalables  

*   Utilisez le [code vs][VisualstudioCodeMain] pour modifier votre code source PWA.  
*   Utilisez [Node.js][NodejsMain] comme serveur Web local.  

## Configurer une application Web de base  

Pour créer une application Web vide, suivez les étapes décrites dans l’article [Générateur d’applications de nœud][ExpressjsApplicationGenerator]et nommez votre application `MySamplePwa` .  

Dans l’invite, exécutez les commandes suivantes.  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

Les commandes créent une application Web vide et installent des dépendances.  

Vous disposez maintenant d’une application Web simple et fonctionnelle.  Pour commencer, exécutez la commande suivante.  

```shell
npm start
```  

Rendez- `http://localhost:3000` vous sur pour afficher votre nouvelle application Web.  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Exécution de votre nouveau PWA sur localhost":::
   Exécution de votre nouveau PWA sur localhost
:::image-end:::

## Commencer à créer un PWA  

À présent que vous disposez d’une application Web simple, étendez-la en tant que PWA en ajoutant les 3 conditions requises pour PWAs<!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]-->: [Https](#step-1---use-https), manifeste d’une [application Web](#step-2---create-a-web-app-manifest)et [travailleur de service](#step-3---add-a-service-worker).  

### Étape 1: utiliser HTTPs  

Les principales parties de la plateforme PWA, telles que les [travailleurs de service][MDNServiceWorkerApi], nécessitent l’utilisation de HTTPS.  Lorsque vous avez atteint la mise en service de Project Web App, vous devez la publier sur une URL HTTPs.  

Pour le débogage, Microsoft Edge permet également `http://localhost` d’utiliser les API PWA.  

Si vous [publiez votre application Web en tant que site actif][VisualStudioNodejsTutorialPublishAzureAppService] (par exemple, en installant un [compte gratuit Azure][AzureCreateFreeAccount]), vous devez vous assurer que votre serveur est configuré pour HTTPS.  Si vous utilisez le [service Microsoft Azure App][AzureWebApps] pour héberger votre site, il est desservi par défaut par défaut.  

Le guide suivant, `http://localhost` qui vous permet de créer votre PWA.  

### Étape 2: créer un manifeste de l’application Web  

Le [manifeste d’une application Web][MDNWebAppManifest] est un fichier JSON contenant les métadonnées relatives à votre application, telles que le nom, la description, les icônes, etc.  

Pour ajouter un manifeste d’application à l’application Web:  

1.  Dans le code vs, **File**accédez  >  au**dossier ouverture** du fichier et sélectionnez le `MySamplePwa` répertoire que vous avez créé précédemment.  
1.  Appuyez sur `Ctrl` + `N` pour créer un fichier, puis collez-le dans l’extrait de code suivant.  
    
    ```json
    {
        "lang": "en-us",
        "name": "My Sample PWA",
        "short_name": "SamplePWA",
        "description": "A sample PWA for testing purposes",
        "start_url": "/",
        "background_color": "#2f3d58",
        "theme_color": "#2f3d58",        
        "orientation": "any",
        "display": "standalone",
        "icons": [
            {
                "src": "/icon512.png",
                "sizes": "512x512"
            }
        ]
    }
    ```  
    
1.  Enregistrez le fichier sous `/MySamplePwa/public/manifest.json` .  
1.  Ajoutez une image d’icône d’application 512x512 nommée `icon512.png` à `/MySamplePwa/public/images` .  Vous pouvez utiliser l' [exemple d’image][ImagePwa] à des fins de test.  
1.  Dans le code VS, ouvrez `/public/index.html` et ajoutez l’extrait de code suivant à l’intérieur de la `<head>` balise.  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### Étape 3: ajouter un travailleur de service  

Les travailleurs de service sont la technologie clé de PWAs, qui permet de prendre en charge les scénarios tels que la prise en charge hors connexion, la mise en cache avancée et l’exécution des tâches en arrière-plan précédemment limitées  

Les travailleurs de service sont des tâches en arrière-plan qui interceptent les requêtes réseau de votre application Web.  Ces derniers effectuent des tâches, même lorsque votre PWA n’est pas en cours d’exécution, comme le service des ressources demandées à partir d’un cache, l’envoi de notifications de transmission, l’exécution de tâches de récupération en arrière-plan, d’icônes badge, etc.  Les travailleurs de service sont définis dans un fichier spécial JavaScript.  Pour plus d’informations, voir [utilisation des travailleurs de service][MDNUsingServiceWorkers] et des API du travailleur du [service][MDNServiceWorkerApi].  

Pour créer un Worker Worker dans votre projet, utilisez la recette du travailleur du service de première connexion de service de **mise en cache** du [Générateur PWA][PwaBuilderServiceWorker].  

1.  Accédez à [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], sélectionnez le travailleur **du service de premier réseau de mise en cache** , puis cliquez sur le bouton **Télécharger** .  Le fichier téléchargé contient les fichiers suivants:
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
    
1.  Copiez les fichiers téléchargés dans le `public` dossier de votre projet d’application Web.  
    
1.  Dans le code VS, ouvrez `/public/index.html` et ajoutez l’extrait de code suivant à l’intérieur de la `<head>` balise.  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
Votre application Web possède désormais un service Worker qui fait appel à la stratégie de mise en cache prioritaire, qui extrait d’abord les ressources telles que les images, JS, CSS et HTML du cache, et repasse au réseau selon les besoins.  

Procédez comme suit pour vérifier que votre travailleur de service s’exécute.  

1.  Accédez à votre application Web à l’aide de `http://localhost:3000` .  Si votre application Web n’est pas disponible, exécutez la commande suivante.   
    
    ```shell
    npm start
    ```
    
1.  Dans Microsoft Edge, sélectionnez `F12` pour ouvrir Microsoft Edge devtools.  Sélectionnez **application**, puis **travailleurs de service** pour afficher les travailleurs de service.  Si vous ne voyez pas le travailleur de service, il est possible que vous deviez actualiser la page.  
     
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Vue d’ensemble des travailleurs de service Microsoft Edge DevTools":::
       Vue d’ensemble des travailleurs de service Microsoft Edge DevTools
    :::image-end:::
    
1.  Affichez le cache du travailleur de service en développant **stockage du cache** et sélectionnez **pwabuilder-cache**.  Vous devez voir toutes les ressources mises en cache par le travailleur du service, telles que l’icône de l’application, le manifeste de l’application, les fichiers CSS et JavaScript.  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Cache du travailleur de service dans Microsoft Edge DevTools":::
       Cache du travailleur de service dans Microsoft Edge DevTools (F12)
    :::image-end:::
    
1.  Essayez votre application PWA en tant qu’application en mode hors connexion.  Dans Microsoft Edge DevTools \ ( `F12` \), cliquez sur **réseau** , puis **Online** définissez l’état de **connexion sur hors connexion**.  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Définir l’application en mode hors connexion dans Microsoft Edge DevTools":::
       Définir l’application en mode hors connexion dans Microsoft Edge DevTools
    :::image-end:::
    
1.  Actualisez votre application pour pouvoir la voir travailler hors connexion en utilisant les ressources de votre application à partir du cache.  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="PWA exécuté hors connexion":::
       PWA exécuté hors connexion
    :::image-end:::
    
## Ajouter des notifications de transmission à votre PWA  

Vous pouvez créer des PWAs qui prennent en charge les notifications de transmission en effectuant les tâches suivantes.  

1.  S’abonner à un service de messagerie à l’aide de l' [API de transmission][MDNPushApi]  
1.  Afficher des messages toast lors de la réception d’un message du service à l’aide de l' [API notifications][MDNNotificationsApi]  

Comme pour les travailleurs de service, il s’agit d’API normalisées qui fonctionnent avec tous les navigateurs, de sorte que vous n’avez à écrire le code qu’une seule fois pour fonctionner partout où PWAs est pris en charge.  Pour plus d’informations sur la distribution de messages de type pousser vers différents navigateurs sur votre serveur, utilisez la bibliothèque open-source sur le [Web][NPMWebPush] .  

Les étapes ci-dessous ont été adaptées à partir du livre de recettes de travail complet du [travailleur de service][ServiceWorkerCookbookPushRichDemo] fourni par Mozilla, qui comporte un certain nombre d’autres recettes utiles pour les employés sur le Web et les services.  

### Étape 1: générer les clés de VAPID  

Les notifications de transmission requièrent VAPID \ (application d’identification du serveur d’application) pour envoyer des messages envoyés au client de Project Web App.  Plusieurs générateurs de clés VAPID sont disponibles en ligne (par exemple, [vapidkeys.com][VapidkeysMain]\).  Après la génération, vous devez obtenir un objet JSON contenant une clé publique et privée.  Enregistrez les clés pour les étapes suivantes dans le didacticiel suivant.  Pour plus d’informations sur le fonctionnement de VAPID et de webpousser, voir [envoi de notifications webtravers de Mozilla par le biais du service pousser de Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush].  

### Étape 2: s’abonner aux notifications de transmission  

Les travailleurs de service gèrent les événements d’émission et les interactions de notification Toast dans votre PWA.  Pour abonner PWA aux notifications de transmission du serveur, assurez-vous que les conditions suivantes sont remplies.  

*   Votre PWA est installé, actif et inscrit  
*   Votre code qui exécute la tâche d’abonnement se trouve sur le thread d’interface utilisateur principal de PWA.  
*   Vous avez une connectivité réseau  

Avant de créer un nouvel abonnement envoyé, Microsoft Edge vérifie que l’utilisateur lui a accordé l’autorisation PWA pour recevoir des notifications.  Si ce n’est pas le cas, l’utilisateur est invité par le navigateur à entrer une autorisation.  Si l’autorisation est refusée, la demande de `registration.pushManager.subscribe` lever a `DOMException` qui doit être gérée.  Pour plus d’informations sur la gestion des autorisations, voir [notifications de transmission dans Microsoft Edge][WindowsBlogsWebNotificationsEdge].  

Dans votre `pwabuilder-sw-register.js` fichier, ajoutez l’extrait de code suivant.  

```javascript
// Ask the user for permission to send push notifications.
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                const vapidPublicKey = "PASTE YOUR PUBLIC VAPID KEY HERE";             
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: urlBase64ToUint8Array(vapidPublicKey)
                });
            });
    });

// Utility function for browser interoperability
function urlBase64ToUint8Array(base64String) {
    var padding = '='.repeat((4 - base64String.length % 4) % 4);
    var base64 = (base64String + padding)
        .replace(/\-/g, '+')
        .replace(/_/g, '/');
        
    var rawData = window.atob(base64);
    var outputArray = new Uint8Array(rawData.length);
    
    for (var i = 0; i < rawData.length; ++i) {
        outputArray[i] = rawData.charCodeAt(i);
    }
    return outputArray;
}
```  

Pour plus d’informations, voir [PushManager][MDNPushManager] et [Web-Poussée][NPMWebPushUsage].  

### Étape 3: écouter les notifications de transmission  

À présent qu’un abonnement est configuré dans votre PWA, ajoutez des gestionnaires au travailleur de service pour répondre aux événements de transmission \ (envoyés à partir du serveur \) pour afficher les notifications toast avec les données d’un message reçu.  Vous devez ajouter un gestionnaire de Click pour effectuer l’une des tâches suivantes.  
*   ignorer la notification Toast  
*   ouvrir, mettre au point ou ouvrir et sélectionner des fenêtres ouvertes  
*   ouvrir et focaliser une nouvelle fenêtre pour afficher une page client de Project Web App  

Dans votre `pwabuilder-sw.js` fichier, ajoutez les gestionnaires suivants.  

```javascript
// Respond to a server push with a user notification.
self.addEventListener('push', function (event) {
    if (Notification.permission === "granted") {
        const notificationText = event.data.text();
        const showNotification = self.registration.showNotification('Sample PWA', {
            body: notificationText,
            icon: 'images/icon512.png'
        });
        // Ensure the toast notification is displayed before exiting the function.
        event.waitUntil(showNotification);
    }
});

// Respond to the user selecting the toast notification.
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This looks to see if the current notification is already open and focuses it.
    event.waitUntil(clients.matchAll({
        type: 'window'
    }).then(function (clientList) {
        for (var i = 0; i < clientList.length; i++) {
            var client = clientList[i];
            if (client.url == 'http://localhost:1337/' && 'focus' in client)
                return client.focus();
        }
        if (clients.openWindow)
            return clients.openWindow('/');
    }));
});
```  

### Étape 4: testez-le  

Suivez les étapes ci-dessous pour tester les notifications de transmission dans votre PWA.  

1.  Accédez à votre PWA à l’adresse `http://localhost:3000` .  Lorsque le travailleur de votre service active et tente d’abonner votre PWA aux notifications de transmission, Microsoft Edge vous invite à autoriser votre PWA à afficher les notifications.  Sélectionnez **autoriser**.  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Boîte de dialogue autorisation permettant d’activer les notifications":::
       Boîte de dialogue autorisation permettant d’activer les notifications
    :::image-end:::
    
    
1.  Simuler une notification de transmission côté serveur.  Avec votre PWA ouvert `http://localhost:3000` dans votre navigateur, sélectionnez `F12` pour ouvrir le devtools.  Sélectionnez **Application**  >  **Worker Worker Worker Worker**  >  **Push** pour envoyer une notification d’émission de test à votre application Project Web App.  Une notification de transmission doit s’afficher à proximité de la barre des tâches.  
    
    :::image type="complex" source="./media/devtools-push.png" alt-text="Pousser une notification de DevTools":::
       Pousser une notification de DevTools
    :::image-end:::
     
    Si vous ne sélectionnez pas \ (ou activer) une notification Toast, elle est ignorée après quelques secondes et est mise en file d’attente dans le centre de notifications Windows.  
    
    :::image type="complex" source="./media/windows-action-center.png" alt-text="Notifications dans le centre de notifications Windows":::
       Notifications dans le centre de notifications Windows
    :::image-end:::
    
    
## Étapes suivantes  

Vous trouverez ci-dessous une liste de tâches supplémentaires à découvrir lors de la création de PWAss réalistes:  

*  Gérer et stocker des abonnements envoyés  
*  [Chiffrer][NPMWebPushEncrypt] les données de charge utile  
*  Conception réactive  
*  Liaison Poussée  
*  [Tests entre navigateurs][BrowserStackTestEdgeBrowser]  
*  Mettre en œuvre des pratiques recommandées telles que [webhint][Webhint]  

## Voir également  

*   [Applications Web progressives sur MDN Web docs][MDNProgressiveWebApps].  
*   [Applications Web progressives sur le Web. dev][WebDevProgressiveWebApps].  
*   [Lecteurs de News malveillants: applications Web progressives][HackerNewsProgressiveWebApps] -compare les différents types d’infrastructure et de performance permettant d’implémenter un exemple de version de Project  

<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps-edgehtml/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Déploiement d’une application Node.js sur Azure avec code VS | Documents Microsoft"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Créer un compte gratuit Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Applications Web | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Notifications Web dans Microsoft Edge | Blogs Windows"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Code Visual Studio"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Tests gratuits du navigateur Microsoft Edge sur Windows 10 | BrowserStack"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Générateur d’application rapide | Explorer" 

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Lecteurs de nouvelles pirates en application Web progressive"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API notifications | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Applications Web progressives (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API de type pousser | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API du travailleur de service | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Utiliser des travailleurs de service | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifeste de l’application Web | MDN"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Envoyer des notifications webtransmission identifiées par VAPID via le service pousser de Mozilla Services Mozilla"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "Web-Poussée | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, Payload, contentEncoding)-Web-Poussée | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Utilisation-Web-Poussée | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Applications Web progressives"  

[PwaBuilder]: https://www.pwabuilder.com "Générateur PWA"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Travailleur de service | Générateur PWA"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Démonstration complète | Livre de ServiceWorker"  

[VapidkeysMain]: https://vapidkeys.com "Générateur de clés sécurisées VAPID | VapidKeys" 

[Webhint]: https://sonarwhal.com "webhint, le moteur d’indicateurs pour les meilleures pratiques sur le Web"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Applications Web progressives | Web. dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Amélioration progressive | Wikipédia"  
