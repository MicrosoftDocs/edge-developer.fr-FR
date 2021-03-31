---
description: Ce guide vous donne une vue d’ensemble des notions de base et des outils de Project Web App pour créer des applications Web progressives sur Windows.
title: Découvrir les applications Web progressives
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: applications Web progressives, PWA, Edge, Windows, PWABuilder, le manifeste Web, le travailleur de service, l’émission
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9a76399616ab7645b82242b94dd4757b73b37f60
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232796"
---
# Découvrir les applications Web progressives  

Les applications Web progressives \(PWAs \) sont simplement des applications Web qui ont été [améliorées][WikiProgressiveEnhancement] avec les fonctionnalités de type application native sur la prise en charge des plateformes et des moteurs de navigateur, tels que les installations de lancement à partir de écran d’accueil, la prise en charge hors ligne et les notifications de transmission.  Sur Windows 10 avec le moteur Microsoft Edge \(EdgeHTML \), PWAs Profitez de l’avantage supplémentaire de s’exécuter indépendamment de la fenêtre du navigateur en tant qu’applications pour la [plateforme Windows universelle][WindowsUwpGetStartedWhat] .  

Ce guide vous donne une vue d’ensemble des concepts de base de la création d’une `localhost` application Web à l’aide de Microsoft Visual Studio et de certains utilitaires de création de Project Web App.  Le produit fini fonctionne de la même manière dans tous les navigateurs qui prennent en charge PWAs.  

> [!TIP]
> Pour obtenir une méthode rapide de conversion d’un site existant dans un fichier PWA et de package pour Windows 10 et d’autres plateformes d’application, consultez le [Générateur PWA][PwaBuilder].  

## Prérequis  

Vous pouvez générer PWAs avec n’importe quel éditeur de développement Web.  Vous trouverez ci-après les conditions préalables pour ce guide, qui vous guident dans la prise en charge des outils de Project Web App.  

*   Téléchargez la [communauté 2017 Visual Studio Community][VisualStudioDownloads].  Vous pouvez également utiliser les éditions professionnel, entreprise ou [preview][VisualStudioPreview] .  Dans le programme d’installation de Visual Studio, choisissez les charges de travail suivantes.  
    
    *   **Développement de plateforme Windows universelle**  
    *   **Développement Node.js**  

## Configurer une application Web de base  

Par souci de simplicité, utilisez Visual StudioNode.js et le modèle d' [ application Express][VisualStudioNodeJsTutorial] pour créer `localhost` une application Web qui dessert une `index.html` page.  Imaginez qu’il s’agit d’un espace réservé pour l’application Web complète attrayante que vous développez en tant que PWA.  

1.  Lancez Visual Studio et démarrez un nouveau projet.  
    *   **Fichier**  >  **Nouvelle**  >  **Projet...**  
    *   `Ctrl`+`Shift`+`N`  
1.  Sous **JavaScript**, sélectionnez l' **application Basic Node.js Express 4**.  Définissez le nom et l’emplacement, puis sélectionnez **OK**.  
    
    ![Sélection du modèle de projet Node.js Express 4 dans Visual Studio][ImageVsNodejsExpressTemplate]  
    
1.  Après le chargement de votre nouveau projet, sélectionnez **Build** \( `Ctrl` + `Shift` + `B` \) et **Démarrer le débogage** \( `F5` \).  Vérifiez que le `index.html` fichier est chargé lorsque vous naviguez vers `http://localhost:1337` .  
    
    ![Exécution de votre nouveau site sur localhost][ImageVsNodejsExpressIndex]  

## Transformer votre application en PWA  

Maintenant, il est temps de vous connecter à la [Configuration minimale requise][PwaEdgehtmlIndexRequirements] de base pour votre application Web: manifeste de l' *application Web*, *https* et *travailleurs de service*.  

### Manifeste de l’application Web  

Le [manifeste d’une application Web][MDNWebAppManifest] est un fichier de MÉTADONNÉEs JSON décrivant votre application, y compris le nom, l’auteur, l’URL de la page d’entrée et une ou plusieurs icônes.  Dans la mesure où il suit un [schéma normalisé][W3cWebAppManifest], vous devez uniquement fournir un manifeste de l’application Web unique pour le PWA que vous installez sur n’importe quelle plateforme, système d’exploitation et combinaison de périphériques prenant en charge PWAS.  Dans l’écosystème Windows, le manifeste de votre application Web signale à l’indexeur Web de Bing qu’il est candidat pour une inclusion automatique dans le [Microsoft Store][PwaEdgehtmlMicrosoftStore], où il peut arriver qu’il atteigne près de 700 millions utilisateurs d’un mois actif dans le cadre d’une application Windows 10.  

S’il s’agissait d’un site actif existant, vous pouvez générer un manifeste de l’application Web à l’aide du [Générateur PWA][PwaBuilder].  Dans la mesure où il s’agit toujours d’un projet non publié, copiez un exemple de manifeste.  

1.  Dans l’Explorateur de *solutions*de Visual Studio, cliquez avec le bouton droit sur le dossier *public* , puis sélectionnez **Ajouter**  >  **un nouveau fichier...**, en spécifiant `manifest.json` le nom de l’élément.  
1.  Dans le `manifest.json` fichier, copiez le code suivant.  

    ```json
    {
        "dir": "ltr",
        "lang": "en-us",
        "name": "My Sample PWA",
        "scope": "/",
        "display": "browser",
        "start_url": "https://PLACEHOLDER-FOR-PWA-URL",
        "short_name": "SamplePWA",
        "theme_color": "transparent",
        "description": "A sample PWA for testing purposes",
        "orientation": "any",
        "background_color": "transparent",
        "related_applications": [],
        "prefer_related_applications": false,
        "icons": []
    }
    ```  
    
    Dans un espace de noms réel, l’étape suivante consiste à personnaliser le *nom*, le *start_url*, les *SHORT_NAME*, la *Description*et les *icônes* \(les icônes sont décrites dans l’étape suivante.).  
    
    Pour en savoir plus sur les différentes valeurs des membres et leurs objectifs associés, voir référence du manifeste de l' [application Web][MDNWebAppManifest] .  
    
1.  Ensuite, remplissez le tableau vide `icons` avec des trajectoires d’image réelles à l’aide du générateur d’image de l’application Project Builder.  
    
    1.  À l’aide d’un navigateur Web, téléchargez cet [exemple d’image 512X512 PWA][ImagePwa].  
    1.  Accédez au [Générateur d’image][PwaBuilderAppImageGenerator]de l’application concepteur PWA, puis sélectionnez l' `pwa.png` image que vous venez d’enregistrer en tant qu' **image d’entrée** , puis cliquez sur le bouton **Télécharger** .  
    1.  **Ouvrez** et **extrayez** le fichier zip.  
    1.  Dans l’Explorateur de solutions de Visual Studio, cliquez avec le bouton droit sur le `public` dossier et **Ouvrez le dossier dans l’Explorateur de fichiers**.  Créer un **dossier** nommé `images` .  
    1.  Copiez tous les dossiers de la plateforme \( `android` , `chrome` , `windows10` et ainsi de suite) à partir de votre code postal extrait dans le `images` dossier, puis fermez la fenêtre de l’Explorateur de fichiers.  Ajoutez les dossiers à votre projet Visual Studio, dans l’Explorateur de solutions, cliquez avec le bouton droit sur le `images` dossier, puis sélectionnez **Ajouter**un  >  **dossier existant...** pour chacun des dossiers \).  
    1.  Ouvrez \(avec Visual Studio ou n’importe quel éditeur) le `icons.json` fichier à partir du code postal extrait et copiez le `"icons": [...]` tableau dans le `manifest.json` fichier de votre projet.  

1.  Vous devez maintenant associer le manifeste de votre application Web à votre application.  Ouvrez le `layout.pug` fichier \(dans le `views` dossier \) pour le modifier, puis ajoutez cette ligne juste après le lien de la feuille de style.  \(Il s’agit simplement du nœud [Pug][PugAttributes] de gabarit pour `<link rel='manifest' href='/manifest.json'>` \).  
    
    ```html
    link(rel='manifest', href='/manifest.json')
    ```  
    
Lorsque vous avez terminé, votre application Web utilise désormais une icône de manifeste et d’application écran d’accueil.  Essayez d’exécuter votre application \( `F5` \) et de charger le manifeste.  

![Chargement du manifeste de l’application Web à partir de localhost][ImageVsNodejsExpressManifest]  

Et l’une de vos icônes.  

![Chargement du logo de l’application Square71x71Logo à partir de localhost][ImageVsNodejsExpressIcon]  

Si vous publiez l’application Live \(avec un `start_url` \), le moteur de recherche Bing le considère désormais comme un candidat pour [le Packaging automatique et la soumission à la boutique Microsoft][PwaEdgehtmlMicrosoftStore] en tant qu’application Windows 10 installable.  Assurez-vous que votre manifest.jsdans le fichier inclut les [signaux de qualité pour les applications Web progressives][WindowsBlogsPwaEdge] pour lesquelles Bing analyse Bing, y compris les éléments suivants.   

*   `name`  
*   `description`  
*   Au moins une icône 512px carré ou supérieur \(pour garantir la résolution de l’écran de démarrage de votre application dans le Windows Store, la description de votre application dans le Windows Store, l’image de la vignette, etc.).  

Par ailleurs [, utilisez les](#https) [prestataires de services](#service-workers)et les politiques du Windows [Store][LegalWindowsAgrementsMicrosoftStorePolicies].  

### HTTPS  

[Les travailleurs de services][MDNServiceWorkerApi] et autres technologies PWA clés qui fonctionnent avec des travailleurs de service (par exemple, les API de synchronisation [en cache][MDNCache], de [transmission][MDNPushApi]et en [arrière-plan][MDNSyncManager] ) ne fonctionnent que sur des connexions sécurisées, ce qui signifie [https][WikiHttps] pour les sites dynamiques ou `localhost` à des fins de débogage.  

Si vous [publiez cette application Web en tant que site actif][VisualStudioNodejsTutorialPublishAzureAppService] , vous devez vous assurer que votre [][AzureCreateFreeAccount]serveur est configuré pour la configuration de votre serveur pour http  Si vous utilisez le [service Microsoft Azure App][AzureWebApps] pour héberger votre site, il est desservi par défaut par défaut.  

Pour ce guide, continuez à utiliser `http://localhost` en tant qu’espace réservé pour un site actif `https://` .  

### Worker du service  

Les travailleurs de service constituent la technologie clé en coulisse de PWAs. Les travailleurs de service agissent en tant que proxy entre votre PWA et votre réseau pour permettre à votre site Web de fonctionner en tant qu’application native installée qui gère les scénarios hors connexion, répond aux notifications de transmission de serveur et exécute des tâches en arrière-plan.  Les travailleurs de service ouvrent également de nouvelles stratégies de performance.  Vous n’êtes pas tenu de mettre en œuvre une application Web complète pour utiliser le cache du travailleur du service pour améliorer les performances de chargement de page de votre site Web.  

Les travailleurs de service sont des threads d’arrière-plan pilotés par des événements qui s’exécutent à partir de fichiers JavaScript servis avec les scripts standard de votre application Web.  Étant donné que les travailleurs de service ne s’exécutent pas sur le thread d’interface utilisateur principal, les travailleurs de service n’ont pas accès au DOM, même si le [thread d’interface utilisateur][MDNWorkerPrototypePostMessage] et un [thread de travail][MDNDedicatedWorkerGlobalScopePostMessage] sont en mesure de communiquer au moyen de `postMessage()` gestionnaires d’événements et de communication `onmessage` .  

Pour associer un ouvrier de service à votre application, vous devez l’inscrire à l’adresse d’URL de votre site \(ou un chemin d’accès spécifié dans le fichier \).  Une fois inscrit, le fichier de travailleur de service est alors téléchargé, installé et activé sur l’ordinateur de l’utilisateur.  Pour en savoir plus, MDN Web documentation dispose d’un guide complet sur [l’utilisation des travailleurs de services][MDNUsingServiceWorkers] et une référence d' [API de service][MDNServiceWorkerApi] détaillée.  

Pour ce didacticiel, utilisez le script de travail de service de page en mode hors connexion dans le [Générateur PWA][PwaBuilderServiceWorker].  Commencez par personnaliser le script en fonction de vos besoins en matière de performances, de la bande passante réseau, etc.  Consultez le livre de [recettes du travailleur][ServiceWorkerCookbook]  fourni par Mozilla pour un certain nombre d’idées mises en cache par des travailleurs de services utiles.  

1.  Ouvrez [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] et sélectionnez le travailleur de service de **page hors connexion** \(par défaut), puis cliquez sur le bouton **Télécharger le service ouvrier** .  
1.  Ouvrez le dossier de téléchargement et copiez les deux fichiers suivants.  

    *   ServiceWorker1\pwabuilder-sw-register.js  
    *   ServiceWorker1\pwabuilder-sw.js  
    
    Enregistrez les fichiers dans le `public` dossier de votre projet Visual Studio Web App.  \(Dans Visual Studio, utilisez `Ctrl` + `O` l’Explorateur de fichiers pour ouvrir l’Explorateur de fichiers et accédez au `public` dossier \).  
    
    Dans l’Explorateur de solutions, ouvrez le `public/pwabuilder-sw.js` fichier, puis changez la valeur de `offlineFallbackPage` to `offline.html` .  
    
    ```javascript
    const offlineFallbackPage = "offline.html";
    ```
    
    Il est important de revoir le code de ces deux fichiers afin d’obtenir le message d’enregistrement d’un ouvrier de service qui met en cache une page désignée \( `offline.html` \) et le remplit lorsqu’une extraction réseau échoue.  Ensuite, créez une `offline.html` page simple en tant qu’espace réservé pour la fonctionnalité de votre application en mode hors connexion.  
    
1.  Dans l’Explorateur de solutions, ouvrez le `views/layout.pug` fichier, puis ajoutez la ligne suivante sous vos balises de lien.  
    
    ```html
    script(src='/pwabuilder-sw-register.js' type='module')
    ```  
    
    Votre site charge et exécute le script d’inscription de votre travailleur de service.  
    
1.  Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le `public` dossier, puis sélectionnez **Ajouter**  >  **un nouveau fichier...**.  Nommez-le `offline.html` , puis ajoutez un `<title>` et du contenu du corps, par exemple le code suivant.  
    
    ```html
    <!DOCTYPE html>
    
    <html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <meta charset="utf-8" />
        <title>Offline mode</title>
    </head>
    <body>
        You are now offline.
    </body>
    </html>
    ```  
    
    À ce stade, votre `public` dossier doit contenir trois nouveaux fichiers.  
    
    ![Fichiers ajoutés dans le dossier public de la solution][ImageVsNodejsExpressPublic]  
    
1.  Dans l’Explorateur de solutions, ouvrez le `routes\index.js` fichier et ajoutez le code suivant juste avant la commande finale \( `module.exports = router;` \).  
    
    ```javascript
    router.get('/offline.html', function (req, res) {
        res.sendFile('public/offline.html');
    });
    ```  
    
    Cela indique à votre application d’avoir le `offline.html` fichier \(lorsque le travailleur du service le récupère pour le cache hors connexion \).  
    
1.  Testez votre PWA.  Créez \( `Ctrl` + `Shift` + `B` \) et exécutez \( `F5` \) votre application Web pour lancer Microsoft Edge et ouvrir votre `localhost` page.  Procédez comme suit.  
    
    1.  Ouvrez la **console** de devtools Edge \( `Ctrl` + `Shift` + `J` \) et vérifiez que le travailleur du service a été enregistré.  
    1.  Dans le volet **débogueur** , développez le contrôle **travailleurs de service** , puis cliquez sur votre origine.  Dans la **vue d’ensemble du travailleur de services**, vérifiez que votre travailleur de service est activé et en cours d’exécution.  
        
        ![Présentation du service d’DevTools Edge][ImageDevtoolsSwOverview]  
        
    1.  Développez le contrôle de **cache** et vérifiez que la `offline.html` page est mise en cache.  
        
        ![Cache du travailleur du service Edge DevTools][ImageDevtoolsSwCache]  
        
1.  Temps d’essayer votre application PWA en tant qu’application en mode hors connexion.  Dans Visual Studio, **Arrêtez de déboguer** \( `Shift` + `F5` \) votre application Web, puis ouvrez Microsoft Edge \(ou actualisez) sur l’adresse localhost de votre site Web.  Le chargement de la `offline.html` page \(par le biais de votre ouvrier de services et du cache hors connexion \) devrait désormais être chargé.  
    
    ![offline.html du http://localhost:1337 chargé dans Microsoft Edge][ImageOfflineHtml]  

## Ajouter des notifications de transmission  

Rendez votre application Project de plus en plus proche en ajoutant une prise en charge côté client des notifications de transmission à l’aide de l' [API de transmission][MDNPushApi] pour vous abonner à un service de messagerie et l' [API notifications][MDNNotificationsApi] pour afficher un message Toast lors de la réception d’un message.  Comme pour les travailleurs de service, il s’agit d’API normalisées qui fonctionnent par le biais du navigateur, de sorte que vous n’avez à écrire le code qu’une seule fois pour le travail partout où PWAs est pris en charge.  Sur le côté serveur, [Utilisez la bibliothèque open-source][NPMWebPush] pour gérer les différences inhérentes à la fourniture de messages de type pousser dans différents navigateurs.  

Les solutions suivantes sont adaptées à partir du livre de [recettes de travail][ServiceWorkerCookbookPushRichDemo] complet fourni par Mozilla, qui est un bon d’examen pour un certain nombre d’autres recettes utiles sur les services Web et les employés.  

### Étape 1: installation de la bibliothèque Web NPM  

Dans l’Explorateur de solutions de Visual Studio, cliquez avec le bouton droit sur votre projet et **ouvrez Node.js fenêtre interactive...**.  Entrez le code suivant.  

```javascript
.npm install web-push
```  

Cette opération installe la bibliothèque [de transmission Web][NPMWebPush] .  Ensuite, ouvrez votre `index.js` fichier et ajoutez la ligne suivante en haut de votre fichier après les autres instructions.  

```javascript
var webpush = require('web-push');
```  

### Étape 2: générer les clés VAPID pour votre serveur  

Ensuite, vous devez générer des clés VAPID \(d’identification involontaires du serveur d’application) pour que votre serveur envoie des messages de type pousser au client Project Web App.  Pour cela, il vous suffit de le faire une fois \(autrement dit, votre serveur nécessite uniquement une seule paire de clés VAPID \).  Dans la fenêtre interactif du Node.js, tapez le code suivant.  

```javascript
var webpush = require('web-push');
webpush.generateVAPIDKeys();
```  

La sortie doit produire un objet JSON contenant une clé publique et privée, que vous copiez dans la logique de votre serveur.  

Dans votre `index.js` fichier, juste avant la fin de la `module.exports = router` ligne \(\), ajoutez le code suivant.  

```javascript
const vapidKeys = {
    publicKey: '',
    privateKey: ''
};

webpush.setVapidDetails(
    'mailto:pwa@example.com',
    vapidKeys.publicKey,
    vapidKeys.privateKey
);
```  

Copiez `publicKey` les `privateKey` valeurs et les valeurs que vous venez de générer.  N’hésitez pas à personnaliser l' `mailto` adresse également \(bien qu’il ne soit pas nécessaire pour exécuter cet exemple).  

Le [blog ingénierie des services Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush] est doté d’un VAPID et de webpousser si vous êtes intéressé par le fonctionnement des coulisses.  

### Étape 3: gérer les demandes de serveur liées à l’émission  

Configurez désormais des itinéraires pour gérer les demandes en relation poussée à partir du client de Project Web App, y compris la gestion de la clé publique VAPID et l’inscription du client pour recevoir des émission de type pousser.  

Dans un scénario réel, une notification de transmission peut provenir d’un événement dans votre logique serveur.  Pour simplifier les choses à ce stade, vous devez ajouter un bouton de **notification de transmission** à la page d’accueil de Project Web App pour générer des poussées à partir de notre serveur et un `/sendNotification` point de terminaison (itinéraire serveur \) pour la gestion de ces requêtes.  

Dans votre `index.js` fichier, ajoutez les itinéraires suivants juste après le code d’initialisation VAPID que vous avez ajouté dans [étape 2] [#step-2---Generate-VAPID-Keys-for-your-Server].  

```javascript
router.get('/vapidPublicKey', function (req, res) {
    res.send(vapidKeys.publicKey);
});

router.post('/register', function (req, res) {
    // A real world application stores the subscription info.
    res.sendStatus(201);
});

router.post('/sendNotification', function (req, res) {
    const subscription = req.body.subscription;
    const payload = 'payload';
    const options = null;
    
    webpush.sendNotification(subscription, payload, options)
        .then(function () {
            res.sendStatus(201);
        })
        .catch(function (error) {
            res.sendStatus(500);
            console.log(error);
        });
});
```  

Lorsque le code côté serveur est sur place, montez les notifications de transmission sur le client PWA.  

### Étape 4: s’abonner aux notifications de transmission  

Dans le cadre de leur rôle de proxy réseau sur Project Web App, les travailleurs de services gèrent les événements d’émission et les interactions de notification Toast.  Toutefois, comme il s’agit de la première configuration de \(ou de l’enregistrement \) d’un travailleur de service, il est possible d’abonner les notifications de type «PWA» aux notifications de transmission du serveur sur le thread d’interface utilisateur principal de PWA et nécessite une connectivité réseau.  S’abonner à des notifications d’émission nécessite l’inscription d’un employé de service actif, vous devez donc vérifier que votre travailleur de service est installé et actif avant d’essayer de s’abonner aux notifications de transmission.  

Avant la création d’un nouvel abonnement envoyé, Microsoft Edge vérifie que l’utilisateur a accordé l’autorisation PWA de recevoir des notifications.  Si ce n’est pas le cas, l’utilisateur est invité par le navigateur à entrer une autorisation.  Si l’autorisation est refusée, la demande de `registration.pushManager.subscribe` lever a `DOMException` et doit donc être gérée.  Pour plus d’informations sur la gestion des autorisations, voir [notifications de transmission dans Microsoft Edge][WindowsBlogsWebNotificationsEdge].  

Dans votre `pwabuilder-sw-register.js` fichier, ajoutez le code suivant.  

```javascript
// Subscribe this PWA to push notifications from the server
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(async function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                // Otherwise subscribe with the server public key
                const response = await fetch('./vapidPublicKey');
                const vapidPublicKey = await response.text();
                const convertedVapidKey = urlBase64ToUint8Array(vapidPublicKey);
                
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: convertedVapidKey
                });
            });
    }).then(function (subscription) {
        // Send the subscription details to the server
        fetch('./register', {
            method: 'post',
            headers: {
                'Content-type': 'application/json'
            },
            body: JSON.stringify({
                subscription: subscription
            }),
        });
        
        // Create a button to mimic server pushes for testing purposes
        var button = document.createElement('input');
        button.type = 'button';
        button.id = 'notify';
        button.value = 'Send Notification';
        document.body.appendChild(button);
        document.getElementById('notify').addEventListener('click', function () {
            fetch('./sendNotification', {
                method: 'post',
                headers: {
                    'Content-type': 'application/json'
                },
                body: JSON.stringify({
                    subscription: subscription
                }),
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

Reportez-vous à la documentation MDN sur l’interface [PushManager][MDNPushManager] et NPM documents sur la bibliothèque de documents [Web][NPMWebPushUsage] pour plus d’informations sur le fonctionnement des API et sur diverses options associées.  

### Étape 5: configurer les gestionnaires d’événements de type pousser et notificationclick  

Avec notre abonnement envoyé, le reste du travail intervient dans le travailleur de service.  Tout d’abord, vous devez configurer un gestionnaire pour les événements de transmission envoyés par le serveur et répondre avec une notification Toast \(si une autorisation a été accordée \) indiquant la charge utile des données de type pousser.  Ensuite, ajoutez un gestionnaire de Click pour le Toast afin d’ignorer la notification et de trier dans la liste des fenêtres actuellement ouvertes pour ouvrir, mettre au point, ou ouvrir et mettre le focus sur la page du client Project Web App prévue.  

Dans votre `pwabuilder-sw.js` fichier, ajoutez les gestionnaires suivants.  

```javascript
//Respond to a server push with a user notification
self.addEventListener('push', function (event) {
    if ("granted" === Notification.permission) {
        var payload = event.data ? event.data.text() : 'no payload';
        const promiseChain = self.registration.showNotification('Sample PWA', {
            body: payload,
            icon: 'images/windows10/Square44x44Logo.scale-100.png'
        });
        //Ensure the toast notification is displayed before exiting this function
        event.waitUntil(promiseChain);
    }
});
    
//Respond to the user clicking the toast notification
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This looks to see if the current is already open and focuses it
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

### Étape 6: essayez-le  

Temps de test des notifications de transmission dans votre PWA  

1.  Exécutez \( `F5` \) votre PWA dans le navigateur.  Étant donné que vous avez modifié le code de travailleur du service \( `pwabuilder-sw.js` \), vous devez ouvrir le débogueur de devtools \( `F12` \) dans le panneau de **vue d’ensemble des travailleurs de services** et **Annuler l’enregistrement** du travailleur de service, puis recharger \( `F5` \) la page pour le réenregistrer \(ou cliquer sur **mettre à jour**\).  Dans un scénario de production, le navigateur vérifie régulièrement les mises à jour des travailleurs de services et installe les mises à jour en arrière-plan.  Nous vous conseillons de le faire pour les résultats immédiats.  
    
    Lorsque le travailleur de votre service est actif et tente de s’abonner à votre PWA pour les notifications de transmission, une boîte de dialogue d’autorisation apparaît en bas de la page.  
    
    ![Boîte de dialogue autorisation permettant d’activer les notifications][ImageNotificationPermission]  
    
    Cliquez sur **Oui** pour activer les notifications toast pour votre PWA.  
    
1.  Dans le volet vue d’ensemble des travailleurs de services, essayez de choisir le bouton  **transmission** .  Une notification toast avec le message électronique de test «test de test» de DevTools "\) doit apparaître.  
    
    ![Pousser une notification de DevTools][ImageDevtoolsPush]  
    
1.  Essayez ensuite de cliquer sur le bouton **Envoyer une notification** sur la page d’accueil de votre PWA.  Cette fois, un toast avec la charge utile de votre serveur s’affiche.  
    
    ![Pousser une notification à partir du serveur PWA][ImagePwaPush]  
    
    Si vous ne cliquez pas sur \(ou activer) une notification Toast, elle est ignorée après quelques secondes, puis mise en file d’attente dans le centre de notifications Windows.  
    
    ![Notifications dans le centre de notifications Windows][ImageWindowsActionCenter]  
    
    Vous avez les bases des notifications de transmission de Project Web App.  Dans une application réelle, les étapes suivantes sont implémentées de manière à gérer et stocker les abonnements envoyés et à [chiffrer][NPMWebPushEncrypt] correctement les données de charge utile envoyées sur le réseau.  
    
## Aller plus loin  

Ce guide a démontré l’anatomie de base d’une application Web progressive et des outils de développement de Microsoft Project Web App, dont Visual Studio, le concepteur PWA et DevTools Edge.  

Bien entendu, il y a beaucoup plus de choses à [faire][PwaEdgehtmlIndexRequirements] au-delà de ce que vous lisez ici, y compris la conception réactive, les liens hypertexte, les [Tests multinavigateurs][BrowserStackTestEdgeBrowser] et d’autres [pratiques recommandées][Webhint] (sans mentionner la fonctionnalité de votre application! \), mais j’espère que ce guide vous a donné une présentation solide des notions de base sur Project Web App  Si vous avez d’autres questions sur le développement de Project Web App avec Windows ou Visual Studio, n’hésitez pas à nous laisser un commentaire!  

Passez en revue les autres guides de Project Web App pour découvrir comment augmenter l’implication des clients et offrir une interface plus transparente et intégrée au système d’exploitation.  

*   [Personnalisation de Windows][PwaEdgehtmlWindowsFeatures]. À l’aide d’une détection de fonctionnalités simple, vous pouvez améliorer progressivement vos clients Windows 10 par le biais des API Windows Runtime \(WinRT \) natives, telles que celles permettant de personnaliser les notifications par vignette du menu **Démarrer** de Windows et la barre des tâches JumpLists et \  
*   [PWAS dans le Microsoft Store][PwaEdgehtmlMicrosoftStore].  En savoir plus sur les avantages de la distribution de l’App Store et sur la soumission de votre PWA.  

## Voir également  

*   Des [applications Web progressives sur MDN Web docs][MDNProgressiveWebApps] -excellent guide sur les applications Web progressives.  
*   [Applications Web progressivement sur le Web. dev][WebDevProgressiveWebApps] -excellent guide sur les applications Web progressives.  
*   [Applications Web progressives-présentation Rocks][ProgressiveWebApps] : exemples concrets de PWAS.  
*   [Lecteurs de News malveillants: applications Web progressives][HackerNewsProgressiveWebApps] -compare les différents types d’infrastructure et de performance permettant d’implémenter un exemple de version de Project  

<!-- image links -->  

[ImageDevtoolsPush]: ./media/devtools-push.png  
[ImageDevtoolsSwCache]: ./media/devtools-cache.png  
[ImageDevtoolsSwOverview]: ./media/devtools-sw-overview.png  
[ImageNotificationPermission]: ./media/notification-permission.png  
[ImageOfflineHtml]: ./media/offline-html.png  
[ImagePwa]: ./media/pwa.png  
[ImagePwaPush]: ./media/pwa-push.png  
[ImageVsNodejsExpressIcon]: ./media/vs-nodejs-express-icon.png  
[ImageVsNodejsExpressIndex]: ./media/vs-nodejs-express-index.png  
[ImageVsNodejsExpressManifest]: ./media/vs-nodejs-express-manifest.png  
[ImageVsNodejsExpressPublic]: ./media/vs-nodejs-express-public.png  
[ImageVsNodejsExpressTemplate]: ./media/vs-nodejs-express-template.png  
[ImageWindowsActionCenter]: ./media/windows-action-center.png  

<!-- links -->  

[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Configuration requise-applications Web progressives \(EdgeHTML \) sur Windows | Documents Microsoft"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps/microsoft-store.md "Applications Web progressives \(EdgeHTML \) sur le Microsoft Store | Documents Microsoft"  
[PwaEdgehtmlWindowsFeatures]: ../progressive-web-apps/windows-features.md "Personnaliser votre PWA \(EdgeHTML \) pour Windows | Documents Microsoft"  

[LegalWindowsAgrementsMicrosoftStorePolicies]: /legal/windows/agreements/store-policies "Politiques du Microsoft Store | Documents Microsoft"  

[VisualStudioNodeJsTutorial]: /visualstudio/nodejs/tutorial-nodejs "Didacticiel: créer un Node.js et une application rapide dans Visual Studio | Documents Microsoft"  
[VisualStudioNodejsTutorialPublishAzureAppService]: /visualstudio/nodejs/tutorial-nodejs#optional-publish-to-azure-app-service "Publier dans Azure App service-créer une Node.js et une application rapide dans Visual Studio | Documents Microsoft"  

[WindowsUwpGetStartedWhat]: /windows/uwp/get-started/whats-a-uwp "Qu’est-ce qu’une application de plateforme Windows universelle (UWP)?  | Documents Microsoft"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Créer un compte gratuit Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Applications Web | Microsoft Azure"  

<!--[DeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote/ "page not found"  -->  

[WindowsBlogsPwaEdge]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#4UOdrDJj3124VIkc.97 "Accueillir des applications Web progressives sur Microsoft Edge et Windows 10 | Blogs Windows"  
[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Notifications Web dans Microsoft Edge | Blogs Windows"  

[VisualStudioDownloads]: https://www.visualstudio.com/downloads "Téléchargements | Visual Studio"  
[VisualStudioFree]: https://visualstudio.microsoft.com/free-developer-offers "Services de & de logiciels de développeur gratuits | Visual Studio"  
[VisualStudioPreview]: https://www.visualstudio.com/vs/preview "Visual Studio preview"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Tests gratuits du navigateur Microsoft Edge sur Windows 10 | BrowserStack"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Lecteurs de nouvelles pirates en application Web progressive"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/DedicatedWorkerGlobalScope/postMessage "DedicatedWorkerGlobalScope. postMessage \(\) | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API notifications | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Applications Web progressives (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API de type pousser | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API du travailleur de service | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Utiliser des travailleurs de service | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifeste de l’application Web | MDN"  
[MDNWorkerPrototypePostMessage]: https://developer.mozilla.org/docs/Web/API/Worker/postMessage "Worker. prototype. postMessage \(\) | MDN"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Envoyer des notifications webtransmission identifiées par VAPID via le service pousser de Mozilla Services Mozilla"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "Web-Poussée | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, Payload, contentEncoding)-Web-Poussée | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Utilisation-Web-Poussée | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Applications Web progressives"  

[PugAttributes]: https://pugjs.org/language/attributes.html "Attributs | Pug"  

[PwaBuilder]: https://www.pwabuilder.com "Générateur PWA"  
[PwaBuilderAppImageGenerator]: https://www.pwabuilder.com/imageGenerator "Générateur d’image d’application"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Travailleur de service | Générateur PWA"  

[ServiceWorkerCookbook]: https://serviceworke.rs "Livre de ServiceWorker"  
[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Démonstration complète | Livre de ServiceWorker"  

[W3cWebAppManifest]: https://www.w3.org/TR/appmanifest "Manifeste de l’application Web | W3C"  

[Webhint]: https://sonarwhal.com "webhint, le moteur d’indicateurs pour les meilleures pratiques sur le Web" 
 
[MDNWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Utilisation des travailleurs Web" 

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Applications Web progressives | Web. dev"  

[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS | Wikipédia"  
[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Amélioration progressive | Wikipédia"  
