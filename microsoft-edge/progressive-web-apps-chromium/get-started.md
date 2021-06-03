---
description: Ce guide vous donne une vue d’ensemble des PWA de base et des outils de création d’applications web progressives (Chromium) sur Windows.
title: Mise en place des applications web progressives (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/16/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: applications web progressives, PWA, Edge, Windows, PWABuilder, manifeste web, service de travail, push
ms.openlocfilehash: 3023c38790185ca6989f4a487928abc79b1d5a2c
ms.sourcegitcommit: 146072bf606b84e5145a48333abf9c6b892a12d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/07/2021
ms.locfileid: "11480194"
---
# <a name="get-started-with-progressive-web-apps-chromium"></a>Mise en place des applications web progressives (Chromium)  

Les applications web progressives \(PWAs\) sont des applications web qui sont [progressivement améliorées.][WikiProgressiveEnhancement]  Les améliorations progressives incluent des fonctionnalités de type application, telles que l’installation, la prise en charge hors connexion et les notifications Push.  Vous pouvez également packager votre PWA pour les magasins d’applications.  Les magasins d’applications possibles incluent Microsoft Store, Google Play, Mac App Store, etc.  Le Microsoft Store est le magasin d’applications commerciales intégré à Windows 10.  

Le guide suivant vous donne une vue d’PWA de base en créant une application web simple et en l’étendant en tant que PWA.  Le projet terminé fonctionne dans les navigateurs modernes.  

> [!TIP]
> Vous pouvez utiliser [PWABuilder][PwaBuilder] pour créer une PWA, améliorer vos PWA existants ou créer un package de vos PWA pour les magasins d’applications.  

## <a name="prerequisites"></a>Conditions préalables  

*   Utilisez [Visual Studio Code][VisualstudioCodeMain] pour modifier votre code PWA source.  
*   Utilisez [Node.js][NodejsMain] comme serveur web local.  
    
## <a name="create-a-basic-web-app"></a>Créer une application web de base  

Pour créer une application web vide, suivez les étapes du Générateur d’applications [Node Express][ExpressjsApplicationGenerator]et nommez votre `MySamplePwa` application.  

Dans l’invite, exécutez les commandes suivantes.  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

Les commandes créent une application web vide et installent les dépendances.  

Vous avez maintenant une application web simple et fonctionnelle.  Pour démarrer votre application web, exécutez la commande suivante.  

```shell
npm start
```  

À présent, `http://localhost:3000` recherchez l’affichage de votre nouvelle application web.  

:::image type="complex" source="./media/visual-studio-nodejs-express-index.png" alt-text="Exécution de votre nouvelle PWA sur localhost" lightbox="./media/visual-studio-nodejs-express-index.png":::
   Exécution de votre nouvelle PWA sur localhost  
:::image-end:::  

## <a name="get-started-building-a-pwa"></a>Commencer à créer une PWA  

Maintenant que vous avez une application web simple, étendez-la en tant que PWA en ajoutant les trois conditions requises pour les applications de bureau d’entreprise<!--[3 requirements for PWAs][ArchiveMicrosoftEdgeLegacyDeveloperPWAsIndexRequirements]-->: [HTTPS](#step-1---use-https), un [manifeste d’application web](#step-2---create-a-web-app-manifest)et un service de [travail](#step-3---add-a-service-worker).  

### <a name="step-1---use-https"></a>Étape 1 : utiliser HTTPS  

Les principales parties de la plateforme PWA, telles que les travailleurs de [service,][MDNServiceWorkerApi]nécessitent l’utilisation du protocole HTTPS.  Lorsque votre PWA est en ligne, vous devez la publier sur une URL HTTPS.  

À des fins de débogage, Microsoft Edge permet également d’utiliser PWA `http://localhost` API.  

[Publiez votre application web en tant que site en direct,][VisualStudioNodejsTutorialPublishAzureAppService]mais assurez-vous que votre serveur est configuré pour HTTPS.  Par exemple, vous pouvez créer un [compte gratuit Azure.][AzureCreateFreeAccount]  Hébergez votre site sur [Microsoft Azure App Service][AzureWebApps] et il est servi sur HTTPS par défaut.  

Le guide suivant, à `http://localhost` utiliser pour créer votre PWA.  

### <a name="step-2---create-a-web-app-manifest"></a>Étape 2 : créer un manifeste d’application web  

Un [manifeste d’application web][MDNWebAppManifest] est un fichier JSON contenant des métadonnées sur votre application, telles que le nom, la description, les icônes, etc.  

Pour ajouter un manifeste d’application à l’application web :  

1.  In Visual Studio Code, choose **File**  >  **Open Folder** and choose the `MySamplePwa` directory you created earlier.  
1.  Sélectionnez `Ctrl` + `N` pour créer un fichier et collez-le dans l’extrait de code suivant.  
    
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
1.  Ajoutez une image d’icône d’application 512 x 512 nommée `icon512.png` à `/MySamplePwa/public/images` .  Vous pouvez utiliser [l’exemple d’image à](./media/progressive-web-app.png) des fins de test.  
1.  Dans Visual Studio Code, ouvrez et ajoutez l’extrait de code suivant `/public/index.html` à l’intérieur de la `<head>` balise.  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <a name="step-3---add-a-service-worker"></a>Étape 3 : ajouter un service de travail  

Les travailleurs de service sont la technologie clé derrière les PPA, permettant des scénarios tels que la prise en charge hors connexion, la mise en cache avancée et l’exécution de tâches en arrière-plan précédemment limitées aux applications natives.  

Les employés de service sont des tâches en arrière-plan qui interceptent les demandes réseau de votre application web.  Les employés de service tentent d’effectuer des tâches, même lorsque votre PWA n’est pas en cours d’exécution.  Les tâches incluent les actions suivantes.  

*   Service des ressources demandées à partir d’un cache  
*   Envoi de notifications Push  
*   Exécution de tâches de récupération en arrière-plan  
*   Icônes de badging  
*   et plus  
    
Les employés de service sont définis dans un fichier JavaScript spécial.  Pour plus d’informations, accédez à [Utilisation des travailleurs de service][MDNUsingServiceWorkers] et de [l’API de travail de service.][MDNServiceWorkerApi]  

Pour créer un service de travail dans votre projet, utilisez la recette de travail de travail de service réseau mise en **cache** à partir PWA [Générateur][PwaBuilderServiceWorker].  

1.  Accédez [à pwabuilder.com/serviceworker,][PwaBuilderServiceWorker]sélectionnez le travail de service réseau mis **en cache** en premier, puis sélectionnez le bouton Télécharger. ****  Le fichier téléchargé contient les fichiers suivants :
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  Copiez les fichiers téléchargés dans le `public` dossier de votre projet d’application web.  
1.  Dans Visual Studio Code, ouvrez et ajoutez l’extrait de code suivant `/public/index.html` à l’intérieur de la `<head>` balise.  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
Votre application web dispose désormais d’un service de travail qui utilise la stratégie de mise en cache en premier.  Le nouveau service de travail récupère d’abord les ressources du cache et du réseau uniquement si nécessaire.  Les ressources mises en cache incluent les images, JavaScript, CSS et HTML.

Utilisez les étapes suivantes pour confirmer que votre service de travail s’exécute.  

1.  Accédez à votre application web à l’aide `http://localhost:3000` de .  Si votre application web n’est pas disponible, exécutez la commande suivante.   
    
    ```shell
    npm start
    ```
    
1.  In Microsoft Edge, select `F12` to open the Microsoft Edge DevTools.  Sélectionnez **Application,** puis **Service Workers** pour afficher les travailleurs du service.  Si le service de travail n’est pas affiché, actualisez la page.  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Microsoft Edge Vue d’ensemble du travail de service DevTools" lightbox="./media/devtools-sw-overview.png":::
       Microsoft Edge Vue d’ensemble du travail de service DevTools  
    :::image-end:::  
    
1.  Affichez le cache de travail de service en Stockage **cache** et sélectionnez **pwabuilder-precache**.  Toutes les ressources mises en cache par le service de travail doivent être affichées.  Les ressources mises en cache par le service comprennent l’icône de l’application, le manifeste de l’application, les fichiers CSS et JavaScript.  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Cache de travail de service dans Microsoft Edge DevTools" lightbox="./media/devtools-cache.png":::
       Cache de travail de service Microsoft Edge DevTools \(F12\)  
    :::image-end:::  
    
1.  Essayez votre PWA en tant qu’application hors connexion.  In Microsoft Edge DevTools \( `F12` \), choose **Network** then change the **Online** status to **Offline**.  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Définition de l’application en mode hors connexion Microsoft Edge DevTools" lightbox="./media/devtools-offline.png":::
       Définition de l’application en mode hors connexion Microsoft Edge DevTools  
    :::image-end:::  
    
1.  Actualisez votre application et affichez le mécanisme hors connexion pour servir les ressources de votre application à partir du cache.  
    
    :::image type="complex" source="./media/visual-studio-nodejs-express-index.png" alt-text="PWA hors connexion" lightbox="./media/visual-studio-nodejs-express-index.png":::
       PWA hors connexion  
    :::image-end:::  
    
## <a name="add-push-notifications-to-your-pwa"></a>Ajouter des notifications Push à votre PWA  

Vous pouvez créer des P.A.P. qui prendre en charge les notifications Push en effectuant les tâches suivantes.  

1.  S’abonner à un service de messagerie à l’aide de [l’API Push][MDNPushApi]  
1.  Afficher un message toast lorsqu’un message est reçu du service à l’aide de [l’API Notifications][MDNNotificationsApi]  
    
Comme pour les travailleurs de service, les API de notification Push sont des API basées sur des normes.  Les API de notification Push fonctionnent dans tous les navigateurs. Votre code doit donc fonctionner partout où les PPA sont pris en charge.  Pour plus d’informations sur la livraison de messages Push à différents navigateurs sur votre serveur, accédez [à Web-Push][NPMWebPush].  

Les étapes suivantes ont été adaptées à partir du manuel de travail de démonstration enrichie Push in [Service][ServiceWorkerCookbookPushRichDemo] fourni par Mozilla, qui offre un certain nombre d’autres recettes utiles de travail de service et Web Push.  

### <a name="step-1---generate-vapid-keys"></a>Étape 1 : générer des clés VAPID  

Les notifications Push nécessitent des clés VAPID \(Identification du serveur d’applications volontaires\) pour envoyer des messages push au client PWA client.  Plusieurs générateurs de clés VAPID sont disponibles en ligne [\(par][VapidkeysMain]exemple, vapidkeys.com \).  Après la génération, vous devez obtenir un objet JSON contenant une clé publique et privée.  Enregistrez les clés pour les étapes ultérieures dans le didacticiel suivant.  Pour plus d’informations sur VAPID et WebPush, accédez à Envoyer des [notifications WebPush identifiées par VAPID][MozillaServicesSendingVapidWebPushNotificationsPush]à l’aide du service Push Mozilla.  

### <a name="step-2---subscribe-to-push-notifications"></a>Étape 2 : s’abonner aux notifications Push  

Les employés de service gèrent les événements Push et les interactions de notification toast dans PWA.  Pour abonner les PWA aux notifications Push du serveur, assurez-vous que les conditions suivantes sont remplies.  

*   Votre PWA est installé, actif et inscrit  
*   Votre code pour effectuer la tâche d’abonnement se trouve sur le thread d’interface utilisateur principal du PWA  
*   Vous avez une connectivité réseau  
    
Avant la création d’un abonnement Push, Microsoft Edge si l’utilisateur a accordé l’autorisation PWA recevoir des notifications.  Si ce n’est pas le cas, le navigateur demande l’autorisation à l’utilisateur.  Si l’autorisation est refusée, la demande de `registration.pushManager.subscribe` throws a `DOMException` , qui doit être gérée.  Pour plus d’informations sur la gestion des [autorisations,][WindowsBlogsWebNotificationsEdge]accédez à Notifications Push dans Microsoft Edge .  

Dans votre `pwabuilder-sw-register.js` fichier,endez l’extrait de code suivant.  

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

Pour plus d’informations, accédez [à PushManager][MDNPushManager] et [Web-Push.][NPMWebPushUsage]  

### <a name="step-3---listen-for-push-notifications"></a>Étape 3 : écouter les notifications Push  

Une fois qu’un abonnement est créé dans votre PWA, ajoutez des handlers au service de travail pour répondre aux événements Push.  Les événements Push sont envoyés à partir du serveur pour afficher des notifications toast.  Les notifications toast affichent les données d’un message reçu.  Pour effectuer les tâches suivantes, vous devez ajouter `click` un handler.  

*   Ignorer la notification toast  
*   Ouvrir, mettre au point ou ouvrir et mettre au point toutes les fenêtres ouvertes  
*   Ouvrir et mettre au point une nouvelle fenêtre pour afficher une page PWA client  
    
Dans votre `pwabuilder-sw.js` fichier, ajoutez les handlers suivants.  

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

### <a name="step-4---try-it-out"></a>Étape 4 : essayez  

Pour tester les notifications Push pour votre PWA, complétez les étapes suivantes.  

1.  Accédez à votre PWA `http://localhost:3000` sur .  Lorsque votre service de travail s’active et tente d’abonner votre PWA aux notifications Push, Microsoft Edge vous invite à autoriser votre PWA à afficher les notifications.  Sélectionnez **Autoriser**.  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Boîte de dialogue d’autorisation pour l’activation des notifications" lightbox="./media/notification-permission.png":::
       Boîte de dialogue d’autorisation pour l’activation des notifications  
    :::image-end:::  
    
1.  Simulez une notification Push côté serveur.  Une fois votre PWA ouvert dans votre navigateur, sélectionnez `http://localhost:3000` `F12` l’ouverture de DevTools.  Choose **Application**  >  **Service Worker**  >  **Push** to send a test push notification to your PWA.  
    
    :::row:::
       :::column span="":::
          Une notification Push doit s’afficher près de la barre des tâches.  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Envoyer une notification à partir de DevTools" lightbox="./media/devtools-push.png":::
             Envoyer une notification à partir de DevTools  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Si vous ne sélectionnez pas \(ou n’activez pas\) une notification toast, le système la masque automatiquement après plusieurs secondes et la met en file d’attente dans Windows centre de notifications.  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Notifications dans le centre Windows actions" lightbox="./media/windows-action-center.png":::
             Notifications dans le centre Windows actions  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="next-steps"></a>Étapes suivantes  

Les étapes suivantes incluent des tâches supplémentaires pour vous aider à comprendre la création de P PWAs réels.  

*   Gérer et stocker les abonnements Push  
*   [Chiffrer les][NPMWebPushEncrypt] données de charge utile  
*   Conception réactive  
*   Liaisons profondes  
*   [Test entre navigateurs][BrowserStackTestEdgeBrowser]  
*   Implémenter des pratiques de validation et de test telles [que Webhint][Webhint]  
    
## <a name="see-also"></a>Articles associés  

*   [Applications web progressives sur des documents web MDN][MDNProgressiveWebApps]  
*   [Applications web progressives sur web.dev][WebDevProgressiveWebApps]  
*   [Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.  
*   [#A0][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Une feuille de route progressive pour votre application web progressive][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Posts hors connexion avec applications web progressives][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [PWA Q&A][AaronGustafsonNotebookPwaQa]  
*   [Se menter sur le Web][JoretegBlogBettingWeb]  
*   [Attribution de noms aux applications web progressives][Fberriman20170626NamingProgressiveWebApps]  
*   [Conception et création d’une application Web progressive sans infrastructure (partie 1)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [Conception et création d’une application Web progressive sans infrastructure (partie 2)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [Conception et création d’une application Web progressive sans infrastructure (partie 3)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  

<!-- links -->  

<!--[ArchiveMicrosoftEdgeLegacyDeveloperPWAsIndexRequirements]: /archive/microsoft-edge/legacy/developer/progressive-web-apps/index#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Déployer une application Node.js azure avec Visual Studio Code | Documents Microsoft"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Créer des comptes azure gratuits | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Web Apps | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Notifications web dans Microsoft Edge | Windows Blogs"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Code Visual Studio"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Test Microsoft Edge navigateur gratuit sur Windows 10 | BrowserStack"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Une feuille de route progressive pour votre application web progressive"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "#A0 – Nouvelle édition Edge"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Express application Generator | Express" 

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Attribution de noms aux applications web progressives"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Lecteurs d’actualités sur les pirates en tant qu’applications web progressives"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Se menter sur le Web"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Notifications API | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Applications web progressives \(PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Api Push | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "| PushManager MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Service Worker API | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Utilisation du service | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Contenu du manifeste d’application | MDN"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Posts hors connexion avec applications web progressives"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Envoi de notifications WebPush identifiées par VAPID via le service Push de Mozilla | Mozilla Services"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "web-push | npm"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "encrypt(userPublicKey, userAuth, payload, contentEncoding) - web-push | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Utilisation - web-push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Applications web progressives"  

[PwaBuilder]: https://www.pwabuilder.com "PWA Générateur"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Service Worker | PWA Générateur"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich Demo | ServiceWorker Cookbook"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Conception et création d’une application Web progressive sans infrastructure (partie 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Conception et création d’une application Web progressive sans infrastructure (partie 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Conception et création d’une application Web progressive sans infrastructure (partie 3)"  

[VapidkeysMain]: https://vapidkeys.com "Sécuriser le générateur de clés VAPID | VapidKeys" 

[Webhint]: https://webhint.io "webhint"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Applications web progressives | web.dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Améliorations progressives | Wikipedia"  
