---
title: Prise en charge de la connectivité réseau et hors connexion dans les applications web progressives
description: Découvrez comment utiliser les technologies de prise en charge pour créer des expériences résilientes pour répondre à différentes conditions réseau.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: applications web progressives, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 6b6031aac10161c16195c83496f8d8b5b842628e
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398076"
---
# <a name="offline-and-network-connectivity-support-in-progressive-web-apps"></a>Prise en charge de la connectivité réseau et hors connexion dans les applications web progressives

Pendant de nombreuses années, les organisations ont dû investir massivement dans les logiciels web par rapport aux logiciels natifs, car les applications web dépendaient de connexions réseau stables. Aujourd’hui, la plateforme web offre désormais des options robustes qui permettent aux utilisateurs de continuer à travailler, même si la connexion réseau devient instable ou totalement déconnectée.

## <a name="use-the-caching-to-improve-performance-of-pwas"></a>Utiliser la mise en cache pour améliorer les performances des PPA

Avec l’introduction des travailleurs [de service,][MDNServiceWorker]la plateforme web a ajouté l’API pour fournir l’accès `Cache` aux ressources mises en cache gérées. Cette API basée sur la promesse permet aux développeurs de stocker et de récupérer de nombreuses ressources web (HTML, CSS, JavaScript, images, JSON, etc.). En règle générale, l’API de cache est utilisée dans le contexte d’un service de travail, mais elle est également disponible dans le thread principal sur `window` l’objet.

Une utilisation courante de l’API consiste à pré-mettre en cache les ressources critiques lorsqu’un service de travail est installé, comme illustré dans l’extrait de `Cache` code suivant.  

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

Ce code, qui s’exécute pendant l’événement de cycle de vie du service De travail, ouvre un cache nommé, puis, lorsqu’il a un pointeur vers le cache, y ajoute quatre ressources à l’aide de la `install` `static-cache` `addAll()` méthode.  Souvent, l’approche est associée à la récupération du cache au cours d’un `fetch` événement   

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

L’extrait de code s’exécute dans le service de travail chaque fois que le navigateur effectue `fetch` une demande pour ce site. Dans cet événement, il existe une instruction conditionnelle qui s’exécute si la demande est pour un fichier HTML. Le service de travail vérifie si le fichier existe déjà dans un cache \(à l’aide `match()` de la méthode\). Si la demande existe dans le cache, ce résultat mis en cache est renvoyé. Si ce n’est pas le cas, une nouvelle ressource est exécuté, une copie de la réponse est mise en cache pour plus tard et la `fetch` réponse est renvoyée. Si `fetch` l’échec est dû à l’indisponibilité du réseau, la page hors connexion est renvoyée à partir du cache.

Cette introduction simple montre comment utiliser la mise en cache dans votre application web progressive (PWA). Chaque PWA est différente et peut utiliser des stratégies de mise en cache différentes. Votre code peut avoir une apparence différente et vous pouvez utiliser différentes stratégies de mise en cache pour différents itinéraires au sein de la même application.

## <a name="use-indexeddb-in-your-pwa-to-store-structured-data"></a>Utiliser IndexedDB dans votre PWA pour stocker des données structurées

`IndexedDB` est une API de stockage des données structurées. Similaire à l’API, elle est également asynchrone, ce qui signifie que vous pouvez l’utiliser dans le thread principal ou avec des travailleurs web tels que les travailleurs `Cache` de service. Utilisez l’API pour stocker une quantité importante de données structurées sur le client, ou des données binaires, telles que des objets `IndexedDB` multimédias chiffrés. Pour plus d’informations, accédez à la base [de données de MDN sur l’utilisation d’IndexedDB.][MDNIndexeddbApiUsing]

## <a name="understand-storage-options-for-pwas"></a>Comprendre les options de stockage pour les P PWA

Parfois, vous devrez stocker de petites quantités de données afin de fournir une meilleure expérience hors connexion à vos utilisateurs. Si c’est le cas, vous trouverez peut-être que la simplicité du système de paire clé-valeur du stockage web répond à vos besoins.  

> [!IMPORTANT]
> La Stockage web est un processus synchrone et n’est pas disponible pour une utilisation dans les threads de travail tels que les travailleurs de service. Une utilisation importante peut créer des problèmes de performances pour votre application. 


Il existe 2 types de Stockage Web : `localStorage` et `sessionStorage` . Chacun d’eux est conservé en tant que magasin de données distinct isolé du domaine qui l’a créé. `sessionStorage` persiste uniquement pendant la durée de la session de navigation (par exemple, lorsque le navigateur est ouvert, ce qui inclut l’actualisation et les restaurations). `localStorage` persiste jusqu’à ce que les données soient supprimées par le code, l’utilisateur ou le navigateur (par exemple, en cas de stockage limité). L’extrait de code suivant montre comment utiliser , ce qui `localStorage` est similaire à la façon dont il est `sessionStorage` utilisé.

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

Cet extrait de code extrait les métadonnées sur la page actuelle et les stocke dans un objet JavaScript. Ensuite, il stocke cette valeur en tant que JSON à l’aide de la méthode et affecte une clé `localStorage` `setItem()` égale à `window.location` l’URL actuelle. Vous pouvez récupérer les informations à partir `localStorage` de l’utilisation de `getItem()` la méthode. 

L’extrait de code suivant montre comment utiliser la mise en cache pour énumérer les pages mises en cache et extraire des métadonnées pour effectuer une tâche, telle que la création d’une liste de `localstorage` liens.

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

La `insertOfflineLink()` méthode transmet l’URL de la demande à la `localStorage.getItem()` méthode pour récupérer les métadonnées stockées. Les données récupérées sont vérifiées pour voir si elles existent et, si c’est le cas, une action peut être prise sur les données, telle que la création et l’insertion du marques de vérification pour les afficher.

## <a name="test-for-network-connections-in-your-pwa"></a>Tester les connexions réseau dans votre PWA

Outre le stockage des informations pour une utilisation hors connexion, il est utile de savoir quand une connexion réseau est disponible pour synchroniser les données ou informer les utilisateurs que l’état du réseau a changé. Utilisez les options suivantes pour tester la connectivité réseau.

### <a name="navigatoronline"></a>navigator.onLine  

La propriété est un booléen qui vous permet de connaître `navigator.onLine` l’état actuel du réseau. Si la valeur est `true` , l’utilisateur est en ligne, sinon l’utilisateur est hors connexion.

### <a name="online-and-offline-events"></a>Événements en ligne et hors connexion  

Il est utile de savoir si le réseau est disponible, mais vous pouvez prendre des mesures lorsque votre connectivité réseau change. Dans ce cas, vous pouvez écouter et prendre des mesures en réponse à des événements réseau. Les événements sont disponibles sur les éléments , et comme affiché dans l’extrait de `window` `document` code `document.body` suivant.

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## <a name="see-also"></a>Articles associés  

Pour en savoir plus sur la gestion des scénarios hors connexion, accédez aux pages suivantes.  

*   [Cache][MDNCache]  
*   [IndexedDB][MDNIndexeddbApi]  
*   [Service Worker][MDNServiceWorker]  
*   [Web Stockage][MDNWebStorageApi]  
*   [navigator.onLine][MDNNavigatoronline]  
*   [Événements en ligne et hors connexion][MDNNavigatoronlineOfflineEvents]  
*   [Demande avec intention : stratégies de mise en cache à l’âge des PPA][AlistapartRequestIntentCachingStrategiesAgePwas]
    
<!-- links -->  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNIndexeddbApi]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "IndexedDB API | MDN"  
[MDNIndexeddbApiUsing]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Utilisation d’IndexDb - Api IndexDB | MDN"  
[MDNServiceWorker]: https://developer.mozilla.org/docs/Web/API/ServiceWorker "ServiceWorker | MDN"  
[MDNWebStorageApi]: https://developer.mozilla.org/docs/Web/API/Web_Storage_API "Web Stockage API | MDN"  
[MDNNavigatoronline]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine "NavigateurOnLine | MDN"  
[MDNNavigatoronlineOfflineEvents]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine/Online_and_offline_events "Événements en ligne et hors connexion - NavigateurOnLine | MDN"  

[AbookapartGoingOffline]: https://abookapart.com/products/going-offline "Mise en mode hors connexion par LasSyrxy| A Book Apart"  

[AlistapartRequestIntentCachingStrategiesAgePwas]: https://alistapart.com/article/request-with-intent-caching-strategies-in-the-age-of-pwas "Demande avec intention : stratégies de mise en cache à l’âge des PPA par| Liste à part"  
