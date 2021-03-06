---
title: Utiliser les employés de service pour gérer les demandes réseau et les notifications Push
description: Les travailleurs de service sont des travailleurs web qui permettent d’améliorer les performances, de répondre à différentes conditions réseau et d’améliorer la connectivité avec votre application web.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: applications web progressives, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 314acbbd5a2f423c274f92e815b2be4329ace9b8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399133"
---
# <a name="use-service-workers-to-manage-network-requests-and-push-notifications"></a>Utiliser les employés de service pour gérer les demandes réseau et les notifications Push

Les travailleurs de service sont un type spécial de travail web ayant la possibilité d’intercepter, de modifier et de répondre à toutes les demandes réseau à l’aide de `Fetch` l’API.  Les employés de service peuvent accéder à l’API et aux magasins de données `Cache` côté client asynchrones, tels que, pour `IndexedDB` stocker des ressources.  

## <a name="registering-a-service-worker"></a>Inscription d’un service de travail  

Comme d’autres travailleurs web, les travailleurs du service doivent exister dans un fichier distinct. Vous référencez ce fichier lors de l’inscription du service de travail, comme illustré dans l’extrait de code suivant.  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

Les navigateurs modernes fournissent différents niveaux de prise en charge pour les travailleurs du service. En tant que tel, il est bon de tester l’existence de l’objet avant d’exécution d’un code lié au service `serviceWorker` de travail. Dans l’extrait de code ci-dessus, un service de travail est enregistré à l’aide du fichier situé à la `serviceworker.min.js` racine du site. Assurez-vous que le fichier JavaScript qui définit votre service de travail existe dans le répertoire de niveau le plus élevé que vous souhaitez qu’il gère \(qui est appelé étendue du Service Worker\).  Dans l’extrait de code précédent, le fichier est stocké à la racine et le service de travail gère toutes les pages du domaine. Si le fichier de travail de service était stocké dans un répertoire, l’étendue du service de travail serait le répertoire et tous les `js` `js` sous-répertoires.  En tant que meilleure pratique, placez le fichier de travail de service à la racine de votre site, sauf si vous devez réduire l’étendue de votre service de travail.  

## <a name="the-service-worker-lifecycle"></a>Cycle de vie des travailleurs du service  

Le cycle de vie d’un service de travail se compose de plusieurs étapes, chaque étape déclenchant un événement. Vous pouvez ajouter des écouteurs à ces événements pour exécuter du code pour effectuer une action. La liste suivante présente une vue d’un haut niveau du cycle de vie et des événements connexes des travailleurs du service. 

1.  Inscrivez le service de travail.  
1.  Le navigateur télécharge le fichier JavaScript, installe le service de travail et déclenche `install` l’événement. Vous pouvez utiliser l’événement pour pré-mettre en cache tous les fichiers importants et à durée de vie longue, tels que les fichiers CSS, les fichiers JavaScript, les images de logo, les pages hors connexion, etc. à partir de votre `install` site web.  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  Le service de travail est activé, ce qui déclenche `activate` l’événement.  Utilisez cet événement pour nettoyer les caches obsolètes.  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  Le service de travail est prêt à s’exécuter lorsque la page est actualisée ou lorsque l’utilisateur navigue vers une nouvelle page sur le site. Si vous souhaitez exécuter le service de travail sans attendre, utilisez `self.skipWaiting()` la méthode pendant `install` l’événement.  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  Le service de travail est en cours d’exécution.     
    
## <a name="using-fetch-in-service-workers"></a>Utilisation de la récupération dans les travailleurs du service  

L’événement principal que vous utilisez dans un service de travail est `fetch` l’événement.  L’événement s’exécute chaque fois que le navigateur tente d’accéder au contenu `fetch` dans l’étendue du service de travail. L’extrait de code suivant montre comment ajouter un listener à l’événement fetch.  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

Au sein du handler, vous pouvez contrôler si une demande est traitée sur le réseau, s’il est tiré du `fetch` cache, etc.  L’approche que vous prenez varie probablement en fonction du type de ressource demandée, de la fréquence de sa mise à jour et d’une autre logique métier propre à votre application.  Voici quelques exemples de ce que vous pouvez faire :  

*   Si disponible, renvoyer une réponse à partir du cache, sinon de secours pour demander la ressource sur le réseau.  
*   Récupérer une ressource à partir du réseau, mettre en cache une copie et renvoyer la réponse.
*   Autoriser les utilisateurs à spécifier une préférence pour enregistrer des données. 
*   Fournir une image d’espace réservé pour certaines demandes d’image.  
*   Générer une réponse directement dans le service de travail.  
    
## <a name="push-notifications"></a>Push Notifications  

Les employés de service peuvent envoyer des notifications aux utilisateurs. Les notifications Push sont utiles pour inciter les utilisateurs à interagir à l’aide de votre application après un certain temps. Pour plus d’informations, accédez à la démonstration et à la démonstration des [notifications Push.][AzurewebsitesWebpushdemo]  

## <a name="see-also"></a>Voir également  

Pour en savoir plus sur les travailleurs de service, accédez à la liste suivante des rubriques connexes.  

*   [Mise en mode hors connexion des P PWA avec les travailleurs du service][MDNPwasMakingOfflineServiceWorkers]  
*   [Comment rendre les P.A.S. ré-engageables à l’aide de Notifications et Push][MDNPwasMakeReengageablesingNotificationsPush]  
    
<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Web Push Notifications |  Démonstrations de Microsoft Edge"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Mise en mode hors connexion des P PWAs avec les travailleurs du service : les P PWAs | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "Comment rendre les PAS ré-engageables à l’aide de Notifications et Push - P PWAs | MDN"  
