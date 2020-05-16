---
title: Prise en charge du mode hors connexion et de la connectivité réseau dans les applications Web progressives
description: Découvrez comment utiliser les technologies de support pour créer des expériences résilientes qui répondent aux différentes conditions du réseau.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: applications Web progressives, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 58ffb8e9ae596dec4b99143a3061995a6598ce44
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659306"
---
# Prise en charge du mode hors connexion et de la connectivité réseau dans les applications Web progressives

Pour de nombreuses années, les organisations se sont importées énormément de logiciels sur le Web par le biais de logiciels natifs, car les applications Web sont basées sur des connexions réseau stables. Aujourd’hui, la plateforme Web propose désormais des options puissantes qui permettent aux utilisateurs de continuer à travailler, même si la connexion réseau devient instable ou qu’elle est complètement hors connexion.

## Utiliser la mise en cache pour améliorer les performances de PWAs

Avec l’introduction des [travailleurs de service][MDNServiceWorker], la plateforme Web a ajouté l' `Cache` API pour donner accès aux ressources mises en cache gérées. Cette API basée sur la promesse permet aux développeurs de stocker et de récupérer de nombreuses ressources Web (HTML, CSS, JavaScript, images, JSON, etc.). En règle générale, l’API de cache est utilisée dans le contexte d’un travailleur de service, mais elle est également disponible dans le thread principal de l' `window` objet.

Une utilisation courante de l' `Cache` API consiste à mettre en cache les ressources critiques lors de l’installation d’un employé de service, comme illustré dans l’extrait de code suivant.  

```javascript
self.addEventListener( "install", function( event ){
    event.waitUntil(
        caches.open( "static-cache" )
              .then(function( cache ){
            return cache.addAll([
                "/css/main.css",
                "/js/main.js",
                "/img/favicon.png",
                "/offline/"
            ]);
        })
    );
});
```  

Ce code, qui s’exécute pendant la durée de vie du travailleur du service `install` , ouvre un cache nommé `static-cache` et, lorsqu’il possède un pointeur vers le cache, lui ajoute quatre ressources à l’aide de la `addAll()` méthode.  Souvent, l’approche est associée à la récupération du cache lors d’un `fetch` événement   

```javascript
self.addEventListener( "fetch", event => {
    const request = event.request,
                    url = request.url;
    
    // If we are requesting an HTML page.
    if ( request.headers.get("Accept").includes("text/html") ) {
        event.respondWith(
            // Check the cache first to see if the asset exists, and if it does, return the cached asset.
            caches.match( request )
                  .then( cached_result => {
                if ( cached_result ) {
                    return cached_result;
                }
                // If the asset is not in the cache, fallback to a network request for the asset, and proceed to cache the result.
                return fetch( request )
                       .then( response => {
                    const copy = response.clone();
                    // Wait until the response we received is added to the cache.
                    event.waitUntil(
                        caches.open( "pages" )
                              .then( cache => {
                            return cache.put( request, response );
                        });
                    );
                    return response;
                })
                // If the network is unavailable to make a request, pull the offline page out of the cache.
                .catch(() => caches.match( "/offline/" ));
            })
        ); // end respondWith
    } // end if HTML
});
```  

L’extrait de code s’exécute au sein du travailleur de service chaque fois que le navigateur effectue une `fetch` demande pour ce site. Dans cet événement, il existe une instruction conditionnelle qui s’exécute si la requête concerne un fichier HTML. Le travailleur de service vérifie si le fichier existe déjà dans le cache \ (en utilisant la `match()` méthode \). Si la requête existe dans le cache, le résultat mis en cache est retourné. Si ce n’est pas le cas, une nouvelle `fetch` ressource est exécutée, une copie de la réponse est mise en cache pour le moment, et la réponse est renvoyée. En cas `fetch` d’échec du réseau, la page hors connexion est renvoyée à partir du cache.

Cette introduction simple montre comment utiliser la mise en cache dans votre application Web progressive (PWA). Chaque PWA est différent et peut utiliser différentes stratégies de mise en cache. Votre code risque de différer et vous pouvez utiliser différentes stratégies de mise en cache pour différents itinéraires au sein de la même application.

## Utiliser IndexedDB dans PWA pour stocker des données structurées

`IndexedDB` est une API pour le stockage des données structurées. Comme pour l' `Cache` API, il est également asynchrone, ce qui signifie que vous pouvez l’utiliser dans le thread principal ou avec des travailleurs Web tels que des travailleurs de service. Utilisez l' `IndexedDB` API pour stocker une quantité significative de données structurées sur le client ou des données binaires telles que des objets multimédias chiffrés. Pour plus d’informations, consultez la section [notions fondamentales sur MDN utilisation de IndexedDB][MDNIndexeddbApiUsing].

## Comprendre les options de stockage pour PWAs

Il peut arriver que vous deviez stocker de petites quantités de données afin de fournir une meilleure expérience hors connexion à vos utilisateurs. Si tel est le cas, il est possible que vous trouviez la simplicité du système de paire clé-valeur du stockage Web qui répond à vos besoins.  

> [!IMPORTANT]
> Le stockage Web est un processus synchrone qui ne peut pas être utilisé dans les threads de travail, tels que les travailleurs de service. Une utilisation intense risque de générer des problèmes de performances pour votre application. 


Il existe 2 types de stockage Web: `localStorage` et `sessionStorage` . Chacun d’eux est géré en tant que magasin de données distinct isolé du domaine qui l’a créé. `sessionStorage` persiste uniquement pendant la durée de la session de navigation (par exemple, lorsque le navigateur est ouvert, y compris l’actualisation et la restauration). `localStorage` persiste tant que les données n’ont pas été supprimées par le code, par l’utilisateur ou par le navigateur (par exemple, quand un stockage limité est disponible). L’extrait de code suivant montre comment utiliser `localStorage` , qui est similaire à celui `sessionStorage` utilisé.

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

Cet extrait de code extrait les métadonnées relatives à la page active et les stocke dans un objet JavaScript. Il stocke ensuite cette valeur comme JSON lors de `localStorage` l’utilisation de la `setItem()` méthode et attribue une clé égale à l' `window.location` URL actuelle. Vous pouvez récupérer les informations relatives `localStorage` à l’utilisation de la `getItem()` méthode. 

L’extrait de code suivant montre comment utiliser la mise en cache `localstorage` pour énumérer les pages mises en cache et extraire les métadonnées pour effectuer une tâche, par exemple créer une liste de liens.

```javascript
caches.open( "pages" )
      .then( cache => {
    cache.keys()
         .then( keys => {
        if ( keys.length )
        {
            keys.forEach( insertOfflineLink );
        }
    })
});

function insertOfflineLink( request ) {
    var data = JSON.parse( localStorage.getItem( request.url ) );
    // If data exists and this page is not an offline page, assuming that offline pages have the word offline in the URL.
    if ( data && request.url.indexOf('offline') < 0  )
    {
        // Build a link and insert it into the page.
    }
}
```  

La `insertOfflineLink()` méthode transmet l’URL de la requête dans la `localStorage.getItem()` méthode pour récupérer des métadonnées stockées. Les données récupérées sont examinées pour voir s’il existe, et si tel est le cas, une action peut être effectuée sur les données, comme le bâtiment et l’insertion du balisage pour l’afficher.

## Test de connexions réseau dans votre PWA

Outre le stockage des informations pour une utilisation en mode hors connexion, il est utile de savoir à quel moment une connexion réseau est disponible pour synchroniser les données ou informer les utilisateurs que le statut du réseau a changé. Utilisez les options suivantes pour tester la connectivité réseau.

### Navigator. onLine  

La `navigator.onLine` propriété est une valeur booléenne qui vous permet de connaître l’état actuel du réseau. Si la valeur est `true` , l’utilisateur est en ligne, sinon l’utilisateur est hors connexion.

### Événements en ligne et hors connexion  

Le fait de savoir si le réseau est disponible est utile, mais il se peut que vous souhaitiez agir en cas de modification de votre connectivité réseau. Dans cette situation, il est possible que vous souhaitiez écouter et entreprendre une action en réponse à des événements réseau. Les événements sont disponibles sur les `window` `document` éléments, et `document.body` comme illustré dans l’extrait de code suivant.

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## Voir également  

Pour en savoir plus sur la gestion des scénarios hors connexion, voir les pages suivantes.  

*   [Cache][MDNCache]  
*   [IndexedDB][MDNIndexeddbApi]  
*   [Travailleur de service][MDNServiceWorker]  
*   [Stockage Web][MDNWebStorageApi]  
*   [Navigator. onLine][MDNNavigatoronline]  
*   [Événements en ligne et hors connexion][MDNNavigatoronlineOfflineEvents]  
*   [Demander avec des conseils: stratégies de mise en cache de l’âge de PWAs][AlistapartRequestIntentCachingStrategiesAgePwas]

<!-- links -->  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNIndexeddbApi]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API IndexedDB | MDN"  
[MDNIndexeddbApiUsing]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Utilisation de l’API IndexDb-IndexDB | MDN"  
[MDNServiceWorker]: https://developer.mozilla.org/docs/Web/API/ServiceWorker "ServiceWorker | MDN"  
[MDNWebStorageApi]: https://developer.mozilla.org/docs/Web/API/Web_Storage_API "API de stockage Web | MDN"  
[MDNNavigatoronline]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine "NavigatorOnLine | MDN"  
[MDNNavigatoronlineOfflineEvents]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine/Online_and_offline_events "Événements en ligne et hors connexion-NavigatorOnLine | MDN"  

[AbookapartGoingOffline]: https://abookapart.com/products/going-offline "Passer hors ligne par Jeremy Keith | Un livre éloigné"  

[AlistapartRequestIntentCachingStrategiesAgePwas]: https://alistapart.com/article/request-with-intent-caching-strategies-in-the-age-of-pwas "Demandez-vous d’utiliser des stratégies de mise en cache de l’âge de PWAs par Aaron Gustafson | Une liste séparée"  
