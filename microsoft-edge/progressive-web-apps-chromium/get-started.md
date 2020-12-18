---
description: Ce guide vous donne une vue d’ensemble des notions de base de Windows Store et des outils de création d’applications Web progressives (chrome) sur Windows.
title: Commencer à utiliser les applications Web progressives (chrome)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: applications Web progressives, PWA, Edge, Windows, PWABuilder, le manifeste Web, le travailleur de service, l’émission
ms.openlocfilehash: 7ad13f98f54c52891681d7591b21503c9d5825ff
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231222"
---
# Commencer à utiliser les applications Web progressives (chrome)  

Les applications Web progressives \ (PWAs) sont des applications Web qui sont [progressivement améliorées][WikiProgressiveEnhancement].  Les améliorations progressives incluent les fonctionnalités d’application, telles que l’installation, la prise en charge hors ligne et les notifications de transmission.  Vous pouvez également empaqueter vos magasins d’applications PWA.  Les magasins d’applications possibles incluent le Microsoft Store, Google Play, Mac App Store, etc.  Le Microsoft Store est le magasin d’applications commercial intégré à Windows 10.  

Le guide suivant vous donne une vue d’ensemble des concepts de base de la création de Project Web App et l’étend en tant que PWA.  Le projet finalisé fonctionne sur les navigateurs modernes.  

> [!TIP]
> Vous pouvez utiliser [PWABuilder][PwaBuilder] pour créer une nouvelle application Project Web App, améliorer votre version Web.  

## Prérequis  

*   Utilisez le [code Visual Studio][VisualstudioCodeMain] pour modifier votre code source PWA.  
*   Utilisez [Node.js][NodejsMain] comme serveur Web local.  
    
## Créer une application Web de base  

Pour créer une application Web vide, suivez les étapes décrites dans l’article [Générateur d’applications de nœud][ExpressjsApplicationGenerator]et nommez votre application `MySamplePwa` .  

Dans l’invite, exécutez les commandes suivantes.  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

Les commandes créent une application Web vide et installent des dépendances.  

Vous disposez maintenant d’une application Web simple et fonctionnelle.  Pour démarrer votre application Web, exécutez la commande suivante.  

```shell
npm start
```  

Rendez- `http://localhost:3000` vous sur pour afficher votre nouvelle application Web.  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Exécution de votre nouveau PWA sur localhost" lightbox="./media/vs-nodejs-express-index.png":::
   Exécution de votre nouveau PWA sur localhost
:::image-end:::

## Commencer à créer un PWA  

À présent que vous disposez d’une application Web simple, étendez-la en tant que PWA en ajoutant les trois conditions requises pour PWAs<!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]-->: [Https](#step-1---use-https), manifeste d’une [application Web](#step-2---create-a-web-app-manifest)et [travailleur de service](#step-3---add-a-service-worker).  

### Étape 1: utiliser HTTPs  

Les principales parties de la plateforme PWA, telles que les [travailleurs de service][MDNServiceWorkerApi], nécessitent l’utilisation de HTTPS.  Lorsque vous avez atteint la mise en service de Project Web App, vous devez la publier sur une URL HTTPs.  

Pour le débogage, Microsoft Edge permet également `http://localhost` d’utiliser les API PWA.  

[Publiez votre application Web en tant que site en ligne][VisualStudioNodejsTutorialPublishAzureAppService], mais assurez-vous que votre serveur est configuré pour HTTPS.  Par exemple, vous pouvez créer un [compte gratuit Azure][AzureCreateFreeAccount].  Hébergez votre site sur le [service Microsoft Azure App][AzureWebApps] et il est desservi par défaut par le biais de HTTPS.  

Le guide suivant, `http://localhost` qui vous permet de créer votre PWA.  

### Étape 2: créer un manifeste de l’application Web  

Le [manifeste d’une application Web][MDNWebAppManifest] est un fichier JSON contenant les métadonnées relatives à votre application, telles que le nom, la description, les icônes, etc.  

Pour ajouter un manifeste d’application à l’application Web:  

1.  Dans le code Visual Studio, choisissez **fichier**  >  **ouvrir le dossier** , puis sélectionnez le `MySamplePwa` répertoire que vous avez créé précédemment.  
1.  Sélectionnez `Ctrl` + `N` pour créer un fichier, puis collez l’extrait de code suivant.  
    
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
1.  Dans le code Visual Studio, ouvrez `/public/index.html` et ajoutez l’extrait de code suivant à l’intérieur de la `<head>` balise.  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### Étape 3: ajouter un travailleur de service  

Les travailleurs de service sont la technologie clé de PWAs, qui permet de prendre en charge les scénarios tels que la prise en charge hors connexion, la mise en cache avancée et l’exécution des tâches en arrière-plan précédemment limitées  

Les travailleurs de service sont des tâches en arrière-plan qui interceptent les requêtes réseau de votre application Web.  Les travailleurs de service essaient d’exécuter des tâches, même si votre ordinateur n’est pas en cours d’exécution.  Les tâches incluent les actions suivantes.  

*   Service des ressources demandées à partir d’un cache  
*   Envoyer des notifications de transmission  
*   Exécution des tâches de récupération en arrière-plan  
*   Icônes de badge  
*   et bien plus encore  
    
Les travailleurs de service sont définis dans un fichier spécial JavaScript.  Pour plus d’informations, accédez à [utiliser les travailleurs de service][MDNUsingServiceWorkers] et les API du travailleur du [service][MDNServiceWorkerApi].  

Pour créer un Worker Worker dans votre projet, utilisez la recette du travailleur du service de première connexion de service de **mise en cache** du [Générateur PWA][PwaBuilderServiceWorker].  

1.  Accédez à [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], sélectionnez le travailleur **du service de premier réseau de mise en cache** , puis cliquez sur le bouton **Télécharger** .  Le fichier téléchargé contient les fichiers suivants:
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  Copiez les fichiers téléchargés dans le `public` dossier de votre projet d’application Web.  
1.  Dans le code Visual Studio, ouvrez `/public/index.html` et ajoutez l’extrait de code suivant à l’intérieur de la `<head>` balise.  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
Pour l’instant, votre application Web utilise un service d’assistance qui utilise la stratégie d’abord de cache.  Le nouveau travailleur de service extrait les ressources du cache en premier, et à partir du réseau uniquement selon les besoins.  Les ressources mises en cache incluent des images, JavaScript, CSS et HTML.

Procédez comme suit pour vérifier que votre travailleur de service s’exécute.  

1.  Accédez à votre application Web à l’aide de `http://localhost:3000` .  Si votre application Web n’est pas disponible, exécutez la commande suivante.   
    
    ```shell
    npm start
    ```
    
1.  Dans Microsoft Edge, sélectionnez `F12` pour ouvrir Microsoft Edge devtools.  Sélectionnez **application**, puis **travailleurs de service** pour afficher les travailleurs de service.  Si le travailleur de service n’est pas affiché, actualisez la page.  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Vue d’ensemble des travailleurs de service Microsoft Edge DevTools" lightbox="./media/devtools-sw-overview.png":::
       Vue d’ensemble des travailleurs de service Microsoft Edge DevTools
    :::image-end:::
    
1.  Affichez le cache du travailleur de service en développant **stockage du cache** et sélectionnez **pwabuilder-cache**.  Toutes les ressources mises en cache par le travailleur de service doivent être affichées.  Les ressources mises en cache par le travailleur de service incluent l’icône d’application, le manifeste de l’application, les fichiers CSS et JavaScript.  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Cache du travailleur de service dans Microsoft Edge DevTools" lightbox="./media/devtools-cache.png":::
       Cache du travailleur de service dans Microsoft Edge DevTools (F12)
    :::image-end:::
    
1.  Essayez votre application PWA en tant qu’application en mode hors connexion.  Dans Microsoft Edge DevTools \ ( `F12` \), cliquez sur **réseau** , puis **** définissez l’état de **connexion sur hors connexion**.  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Définir l’application en mode hors connexion dans Microsoft Edge DevTools" lightbox="./media/devtools-offline.png":::
       Définir l’application en mode hors connexion dans Microsoft Edge DevTools
    :::image-end:::
    
1.  Actualisez votre application pour qu’elle affiche le mécanisme hors connexion pour le service des ressources de votre application à partir du cache.  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="PWA exécuté hors connexion" lightbox="./media/vs-nodejs-express-index.png":::
       PWA exécuté hors connexion
    :::image-end:::
    
## Ajouter des notifications de transmission à votre PWA  

Vous pouvez créer des PWAs qui prennent en charge les notifications de transmission en effectuant les tâches suivantes.  

1.  S’abonner à un service de messagerie à l’aide de l' [API de transmission][MDNPushApi]  
1.  Afficher un message Toast lors de la réception d’un message du service à l’aide de l' [API notifications][MDNNotificationsApi]  
    
Comme pour les travailleurs de service, les API de notifications de transmission d’API sont des API basées sur des normes.  Comme les API de notifications de transmission fonctionnent entre les navigateurs, votre code doit fonctionner partout où PWAs est pris en charge.  Pour plus d’informations sur la distribution de messages de type pousser vers différents navigateurs sur votre serveur, accédez à la section [Web-Poussée][NPMWebPush].  

Les étapes ci-dessous ont été adaptées à partir du livre de recettes de travail complet du [travailleur de service][ServiceWorkerCookbookPushRichDemo] fourni par Mozilla, qui comporte un certain nombre d’autres recettes utiles pour les employés sur le Web et les services.  

### Étape 1: générer les clés de VAPID  

Les notifications de transmission requièrent VAPID \ (application d’identification du serveur d’application) pour envoyer des messages envoyés au client de Project Web App.  Plusieurs générateurs de clés VAPID sont disponibles en ligne (par exemple, [vapidkeys.com][VapidkeysMain]\).  Après la génération, vous devez obtenir un objet JSON contenant une clé publique et privée.  Enregistrez les clés pour les étapes ultérieures dans le didacticiel suivant.  Pour plus d’informations sur VAPID et webpoussée, accédez à [Envoyer des notifications webtransmission identifiées par VAPID à l’aide du service Mozilla de Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush].  

### Étape 2: s’abonner aux notifications de transmission  

Les travailleurs de service gèrent les événements d’émission et les interactions de notification Toast dans votre PWA.  Pour abonner PWA aux notifications de transmission du serveur, assurez-vous que les conditions suivantes sont remplies.  

*   Votre PWA est installé, actif et enregistré  
*   Votre code de réalisation de la tâche d’abonnement se trouve sur le thread d’interface utilisateur principal de PWA  
*   Vous avez une connectivité réseau  
    
Avant la création d’un nouvel abonnement envoyé, Microsoft Edge vérifie que l’utilisateur lui a accordé l’autorisation PWA de recevoir des notifications.  Si ce n’est pas le cas, l’utilisateur est invité par le navigateur à entrer une autorisation.  Si l’autorisation est refusée, la demande de `registration.pushManager.subscribe` lever a `DOMException` qui doit être gérée.  Pour plus d’informations sur la gestion des autorisations, accédez à [notifications de transmission dans Microsoft Edge][WindowsBlogsWebNotificationsEdge].  

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

Pour plus d’informations, accédez à [PushManager][MDNPushManager] et [Web-Poussée][NPMWebPushUsage].  

### Étape 3: écouter les notifications de transmission  

Après avoir créé un abonnement dans votre PWA, ajoutez des gestionnaires au travailleur de service pour répondre aux événements de transmission.  Un événement de type pousser est envoyé à partir du serveur pour afficher les notifications Toast.  Notifications Toast affichent des données pour un message reçu.  Pour effectuer les tâches suivantes, vous devez ajouter un gestionnaire de clic.  

*   Ignorer la notification Toast  
*   Ouvrir, mettre au point ou ouvrir et sélectionner des fenêtres ouvertes  
*   Ouvrir et focaliser une nouvelle fenêtre pour afficher une page client de Project Web App  
    
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
    
    // This attempts to display the current notification if it is already open and then focuses on it.
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

Pour tester les notifications de transmission pour votre PWA, procédez comme suit.  

1.  Accédez à votre PWA à l’adresse `http://localhost:3000` .  Lorsque le travailleur de votre service active et tente d’abonner votre PWA aux notifications de transmission, Microsoft Edge vous invite à autoriser votre PWA à afficher les notifications.  Sélectionnez **autoriser**.  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Boîte de dialogue autorisation permettant d’activer les notifications" lightbox="./media/notification-permission.png":::
       Boîte de dialogue autorisation permettant d’activer les notifications
    :::image-end:::
    
1.  Simuler une notification de transmission côté serveur.  Avec votre PWA ouvert `http://localhost:3000` dans votre navigateur, sélectionnez `F12` pour ouvrir le devtools.  Sélectionnez ****  >  **Worker Worker Worker Worker**  >  **** pour envoyer une notification d’émission de test à votre application Project Web App.  
    
    :::row:::
       :::column span="":::
          Une notification de transmission doit s’afficher à proximité de la barre des tâches.  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Pousser une notification de DevTools" lightbox="./media/devtools-push.png":::
             Pousser une notification de DevTools  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Si vous ne sélectionnez pas \ (ou activer) une notification Toast, le système la ferme automatiquement après quelques secondes et la met en file d’attente dans votre centre de maintenance Windows.  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Notifications dans le centre de notifications Windows" lightbox="./media/windows-action-center.png":::
             Notifications dans le centre de notifications Windows :::image-end:::
       :::column-end:::
    :::row-end:::  
    
## Étapes suivantes  

Les étapes suivantes incluent des tâches supplémentaires pour vous aider à comprendre la création de PWAss réalistes.  

*   Gérer et stocker des abonnements envoyés  
*   [Chiffrer][NPMWebPushEncrypt] les données de charge utile  
*   Conception réactive  
*   Liaison Poussée  
*   [Tests entre navigateurs][BrowserStackTestEdgeBrowser]  
*   Mettre en œuvre des pratiques de validation et de test telles que [webhint][Webhint]  
    
## Voir également  

*   [Applications Web progressives sur MDN Web docs][MDNProgressiveWebApps]  
*   [Applications Web progressives sur le Web. dev][WebDevProgressiveWebApps]  
*   [Lecteurs de News malveillants: applications Web progressives][HackerNewsProgressiveWebApps] -compare les différents types d’infrastructure et de performance permettant d’implémenter un exemple de version de Project  
*   [PWAs de combustion de mythe][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Plan progressif de votre application Web progressive][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Billets hors ligne avec des applications Web progressives][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [PWA Q&A][AaronGustafsonNotebookPwaQa]  
*   [Paris sur le Web][JoretegBlogBettingWeb]  
*   [Attribution d’un nom aux applications Web progressives][Fberriman20170626NamingProgressiveWebApps]  
*   [Conception et création d’une application Web progressive sans infrastructure (partie 1)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [Conception et création d’une application Web progressive sans infrastructure (partie 2)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [Conception et création d’une application Web progressive sans infrastructure (partie 3)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Déploiement d’une application Node.js sur Azure avec du code Visual Studio | Documents Microsoft"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Créer un compte gratuit Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Applications Web | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Notifications Web dans Microsoft Edge | Blogs Windows"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Code Visual Studio"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Tests gratuits du navigateur Microsoft Edge sur Windows 10 | BrowserStack"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Plan progressif de votre application Web progressive"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "PWAs: la nouvelle version de Microsoft Edge"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Générateur d’application rapide | Explorer" 

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Attribution d’un nom aux applications Web progressives"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Lecteurs de nouvelles pirates en application Web progressive"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Paris sur le Web"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API notifications | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Applications Web progressives (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API de type pousser | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API du travailleur de service | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Utiliser des travailleurs de service | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifeste de l’application Web | MDN"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Billets hors ligne avec des applications Web progressives"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Envoyer des notifications webtransmission identifiées par VAPID via le service pousser de Mozilla Services Mozilla"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "Web-Poussée | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, Payload, contentEncoding)-Web-Poussée | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Utilisation-Web-Poussée | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Applications Web progressives"  

[PwaBuilder]: https://www.pwabuilder.com "Générateur PWA"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Travailleur de service | Générateur PWA"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Démonstration complète | Livre de ServiceWorker"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Conception et création d’une application Web progressive sans infrastructure (partie 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Conception et création d’une application Web progressive sans infrastructure (partie 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Conception et création d’une application Web progressive sans infrastructure (partie 3)"  

[VapidkeysMain]: https://vapidkeys.com "Générateur de clés sécurisées VAPID | VapidKeys" 

[Webhint]: https://webhint.io "webhint"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Applications Web progressives | Web. dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Amélioration progressive | Wikipédia"  
