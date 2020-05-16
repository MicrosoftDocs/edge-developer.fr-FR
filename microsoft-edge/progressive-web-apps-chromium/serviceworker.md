---
title: Utiliser des travailleurs de services pour gérer les demandes réseau et les notifications de transmission
description: Les travailleurs de service sont des travailleurs Web qui vous permettent d’améliorer les performances, de répondre à des conditions réseau variables et de renforcer la connectivité avec votre application Web.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: applications Web progressives, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 9bf573b668ade351716b69965f653e05857c32ec
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659299"
---
# Utiliser des travailleurs de services pour gérer les demandes réseau et les notifications de transmission

Les travailleurs de service constituent un type spécial de travailleur Web qui peut intercepter, modifier et répondre à toutes les requêtes réseau à l’aide de l' `Fetch` API.  Les travailleurs de services peuvent accéder `Cache` à l’API et aux magasins de données côté client asynchrones, par exemple `IndexedDB` pour stocker des ressources.  

## Enregistrement d’un travailleur de service  

À l’instar des autres travailleurs sur le Web, les travailleurs de services doivent exister dans un fichier distinct. Vous référencez ce fichier lors de l’enregistrement du travailleur de service, comme le montre l’extrait de code suivant.  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

Les navigateurs modernes fournissent différents niveaux de prise en charge pour les travailleurs de service. C’est pourquoi il est recommandé de tester l’existence de l' `serviceWorker` objet avant d’exécuter tout code lié au travailleur du service. Dans l’extrait de code ci-dessus, un ouvrier de service est enregistré à l’aide du `serviceworker.min.js` fichier situé à la racine du site. Assurez-vous que le fichier JavaScript qui définit votre service d’assistance existe dans le répertoire de niveau supérieur que vous voulez qu’il gère \ (qui est appelé application du travailleur de service).  Dans l’extrait de code ci-dessus, le fichier est stocké à la racine et le travailleur de service gère toutes les pages du domaine. Si le fichier de travailleur de service était stocké dans un `js` répertoire, l’étendue du travailleur de service sera le `js` répertoire et tous ses sous-répertoires.  Nous vous conseillons de placer le fichier du travailleur de service à la racine de votre site, sauf si vous avez besoin de réduire l’étendue de votre travailleur de service.  

## Cycle de vie du travailleur de service  

Le cycle de vie d’un travailleur de service se compose de plusieurs étapes, chaque étape déclenchant un événement. Vous pouvez ajouter des écouteurs à ces événements pour exécuter du code afin d’effectuer une action. La liste suivante présente une vue d’ensemble du cycle de vie et des événements liés des travailleurs de service. 

1. Enregistrez le travailleur de service.  
1.  Le navigateur télécharge le fichier JavaScript, installe le travailleur du service et déclenche l' `install` événement. Vous pouvez utiliser l' `install` événement pour mettre en cache tout fichier important et à durée de vie longue (par exemple, fichiers CSS, fichiers JavaScript, images de logo, pages hors connexion, etc.) de votre site Web.  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  Le travailleur de service est activé, ce qui déclenche l' `activate` événement.  Utilisez cet événement pour nettoyer les caches obsolètes.  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  Le travailleur de service est prêt à s’exécuter lorsque la page est actualisée ou lorsque l’utilisateur navigue vers une nouvelle page sur le site. Si vous souhaitez exécuter le travailleur de service sans attendre, utilisez la `self.skipWaiting()` méthode pendant l' `install` événement.  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  Le travailleur du service s’exécute actuellement.     
    
## Utilisation de FETCH dans les travailleurs de service  

Il s’agit de l’événement principal que vous utilisez dans un travailleur de service `fetch` .  L' `fetch` événement s’exécute chaque fois que le navigateur tente d’accéder au contenu dans le cadre du travailleur de service. L’extrait de code suivant montre comment ajouter un écouteur à l’événement Fetch.  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

Dans le `fetch` Gestionnaire, vous pouvez contrôler si une requête accède au réseau, s’extrait du cache, etc.  L’approche que vous prenez peut varier en fonction du type de ressource demandé, de la fréquence de mise à jour et d’autres logiques métiers propres à votre application.  Voici quelques exemples de ce que vous pouvez faire:  

*   S’il est disponible, renvoyer une réponse à partir du cache, sinon le secours pour demander la ressource sur le réseau.  
*   Récupérer une ressource à partir du réseau, en mettre en cache une copie et retourner la réponse.
*   Permettre aux utilisateurs de spécifier une préférence pour enregistrer les données. 
*   Fournissez une image d’espace réservé pour certaines requêtes d’image.  
*   Générer une réponse directement dans le travailleur de service.  

## Notifications de transmission  

Les travailleurs de services peuvent transmettre les notifications aux utilisateurs. Les notifications de transmission sont utiles pour inviter les utilisateurs à se réengager avec votre application après un certain temps. Pour plus d’informations, reportez-vous à la rubrique [démonstration de notifications de transmission][AzurewebsitesWebpushdemo].  

## Voir également  

Pour en savoir plus sur les travailleurs de service, consultez la liste suivante de rubriques connexes.  

*   [Rendre PWAs travailler hors connexion avec des travailleurs de service][MDNPwasMakingOfflineServiceWorkers]  
*   [Comment faire pour rendre PWAs à nouveau à l’aide de notifications et de l’émission][MDNPwasMakeReengageablesingNotificationsPush]  

<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Notifications de transmission Web |  Démonstrations de Microsoft Edge"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Faire en sorte que PWAs travaille hors connexion avec des travailleurs de services-PWAs | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "Comment rendre PWAs réutilisable à l’aide de notifications et de PWAs | MDN"  
