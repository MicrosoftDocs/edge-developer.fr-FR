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
# <a name="offline-and-network-connectivity-support-in-progressive-web-apps"></a><span data-ttu-id="00452-104">Prise en charge de la connectivité réseau et hors connexion dans les applications web progressives</span><span class="sxs-lookup"><span data-stu-id="00452-104">Offline and network connectivity support in Progressive Web Apps</span></span>

<span data-ttu-id="00452-105">Pendant de nombreuses années, les organisations ont dû investir massivement dans les logiciels web par rapport aux logiciels natifs, car les applications web dépendaient de connexions réseau stables.</span><span class="sxs-lookup"><span data-stu-id="00452-105">For many years organizations were reluctant to invest heavily in web-based software over native software because web applications depended on stable network connections.</span></span> <span data-ttu-id="00452-106">Aujourd’hui, la plateforme web offre désormais des options robustes qui permettent aux utilisateurs de continuer à travailler, même si la connexion réseau devient instable ou totalement déconnectée.</span><span class="sxs-lookup"><span data-stu-id="00452-106">Today, the web platform now offers robust options that enable users to continue working, even if the network connection becomes unstable or goes completely offline.</span></span>

## <a name="use-the-caching-to-improve-performance-of-pwas"></a><span data-ttu-id="00452-107">Utiliser la mise en cache pour améliorer les performances des PPA</span><span class="sxs-lookup"><span data-stu-id="00452-107">Use the caching to improve performance of PWAs</span></span>

<span data-ttu-id="00452-108">Avec l’introduction des travailleurs [de service,][MDNServiceWorker]la plateforme web a ajouté l’API pour fournir l’accès `Cache` aux ressources mises en cache gérées.</span><span class="sxs-lookup"><span data-stu-id="00452-108">With the introduction of [Service Workers][MDNServiceWorker], the web platform added the `Cache` API to provide access to managed cached resources.</span></span> <span data-ttu-id="00452-109">Cette API basée sur la promesse permet aux développeurs de stocker et de récupérer de nombreuses ressources web (HTML, CSS, JavaScript, images, JSON, etc.).</span><span class="sxs-lookup"><span data-stu-id="00452-109">This Promise-based API allows developers to store and retrieve many web resources—HTML, CSS, JavaScript, images, JSON, and so on.</span></span> <span data-ttu-id="00452-110">En règle générale, l’API de cache est utilisée dans le contexte d’un service de travail, mais elle est également disponible dans le thread principal sur `window` l’objet.</span><span class="sxs-lookup"><span data-stu-id="00452-110">Usually, the Cache API is used within the context of a Service Worker, but it is also available in the main thread on the `window` object.</span></span>

<span data-ttu-id="00452-111">Une utilisation courante de l’API consiste à pré-mettre en cache les ressources critiques lorsqu’un service de travail est installé, comme illustré dans l’extrait de `Cache` code suivant.</span><span class="sxs-lookup"><span data-stu-id="00452-111">One common use for the `Cache` API is to pre-cache critical resources when a Service Worker is installed, as shown in the following code snippet.</span></span>  

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

<span data-ttu-id="00452-112">Ce code, qui s’exécute pendant l’événement de cycle de vie du service De travail, ouvre un cache nommé, puis, lorsqu’il a un pointeur vers le cache, y ajoute quatre ressources à l’aide de la `install` `static-cache` `addAll()` méthode.</span><span class="sxs-lookup"><span data-stu-id="00452-112">This code, which runs during the Service Worker `install` life cycle event, opens a cache named `static-cache` and then, when it has a pointer to the cache, adds four resources to it using the `addAll()` method.</span></span>  <span data-ttu-id="00452-113">Souvent, l’approche est associée à la récupération du cache au cours d’un `fetch` événement</span><span class="sxs-lookup"><span data-stu-id="00452-113">Often the approach is coupled with cache retrieval during a `fetch` event</span></span>   

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

<span data-ttu-id="00452-114">L’extrait de code s’exécute dans le service de travail chaque fois que le navigateur effectue `fetch` une demande pour ce site.</span><span class="sxs-lookup"><span data-stu-id="00452-114">The code snippet runs within the Service Worker whenever the browser makes a `fetch` request for this site.</span></span> <span data-ttu-id="00452-115">Dans cet événement, il existe une instruction conditionnelle qui s’exécute si la demande est pour un fichier HTML.</span><span class="sxs-lookup"><span data-stu-id="00452-115">Within that event, there is a conditional statement that runs if the request is for an HTML file.</span></span> <span data-ttu-id="00452-116">Le service de travail vérifie si le fichier existe déjà dans un cache \(à l’aide `match()` de la méthode\).</span><span class="sxs-lookup"><span data-stu-id="00452-116">The Service Worker checks to see if the file already exists in any cache \(using the `match()` method\).</span></span> <span data-ttu-id="00452-117">Si la demande existe dans le cache, ce résultat mis en cache est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="00452-117">If the request exists in the cache, that cached result is returned.</span></span> <span data-ttu-id="00452-118">Si ce n’est pas le cas, une nouvelle ressource est exécuté, une copie de la réponse est mise en cache pour plus tard et la `fetch` réponse est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="00452-118">If not, a new `fetch` for that resource is run, a copy of the response is cached for later, and the response is returned.</span></span> <span data-ttu-id="00452-119">Si `fetch` l’échec est dû à l’indisponibilité du réseau, la page hors connexion est renvoyée à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="00452-119">If the `fetch` fails because the network is unavailable, the offline page is returned from the cache.</span></span>

<span data-ttu-id="00452-120">Cette introduction simple montre comment utiliser la mise en cache dans votre application web progressive (PWA).</span><span class="sxs-lookup"><span data-stu-id="00452-120">This simple introduction shows how to use caching in your progressive web app (PWA).</span></span> <span data-ttu-id="00452-121">Chaque PWA est différente et peut utiliser des stratégies de mise en cache différentes.</span><span class="sxs-lookup"><span data-stu-id="00452-121">Each PWA is different and may use different caching strategies.</span></span> <span data-ttu-id="00452-122">Votre code peut avoir une apparence différente et vous pouvez utiliser différentes stratégies de mise en cache pour différents itinéraires au sein de la même application.</span><span class="sxs-lookup"><span data-stu-id="00452-122">Your code may look different, and you may use different caching strategies for different routes within the same application.</span></span>

## <a name="use-indexeddb-in-your-pwa-to-store-structured-data"></a><span data-ttu-id="00452-123">Utiliser IndexedDB dans votre PWA pour stocker des données structurées</span><span class="sxs-lookup"><span data-stu-id="00452-123">Use IndexedDB in your PWA to store structured data</span></span>

`IndexedDB` <span data-ttu-id="00452-124">est une API de stockage des données structurées.</span><span class="sxs-lookup"><span data-stu-id="00452-124">is an API for storing structured data.</span></span> <span data-ttu-id="00452-125">Similaire à l’API, elle est également asynchrone, ce qui signifie que vous pouvez l’utiliser dans le thread principal ou avec des travailleurs web tels que les travailleurs `Cache` de service.</span><span class="sxs-lookup"><span data-stu-id="00452-125">Similar to the `Cache` API, it is also asynchronous, which means you may use it in the main thread or with Web Workers such as Service Workers.</span></span> <span data-ttu-id="00452-126">Utilisez l’API pour stocker une quantité importante de données structurées sur le client, ou des données binaires, telles que des objets `IndexedDB` multimédias chiffrés.</span><span class="sxs-lookup"><span data-stu-id="00452-126">Use the `IndexedDB` API for storing a significant amount of structured data on the client, or binary data, such as encrypted media objects.</span></span> <span data-ttu-id="00452-127">Pour plus d’informations, accédez à la base [de données de MDN sur l’utilisation d’IndexedDB.][MDNIndexeddbApiUsing]</span><span class="sxs-lookup"><span data-stu-id="00452-127">For more information, navigate to [MDN primer on using IndexedDB][MDNIndexeddbApiUsing].</span></span>

## <a name="understand-storage-options-for-pwas"></a><span data-ttu-id="00452-128">Comprendre les options de stockage pour les P PWA</span><span class="sxs-lookup"><span data-stu-id="00452-128">Understand storage options for PWAs</span></span>

<span data-ttu-id="00452-129">Parfois, vous devrez stocker de petites quantités de données afin de fournir une meilleure expérience hors connexion à vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="00452-129">Sometimes you may need to store small amounts of data in order to provide a better offline experience for your users.</span></span> <span data-ttu-id="00452-130">Si c’est le cas, vous trouverez peut-être que la simplicité du système de paire clé-valeur du stockage web répond à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="00452-130">If that is the case, you may find the simplicity of the key-value pair system of web storage meets your needs.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="00452-131">La Stockage web est un processus synchrone et n’est pas disponible pour une utilisation dans les threads de travail tels que les travailleurs de service.</span><span class="sxs-lookup"><span data-stu-id="00452-131">Web Storage is a synchronous process and is not available for use within worker threads such as Service Workers.</span></span> <span data-ttu-id="00452-132">Une utilisation importante peut créer des problèmes de performances pour votre application.</span><span class="sxs-lookup"><span data-stu-id="00452-132">Heavy usage may create performance issues for your application.</span></span> 


<span data-ttu-id="00452-133">Il existe 2 types de Stockage Web : `localStorage` et `sessionStorage` .</span><span class="sxs-lookup"><span data-stu-id="00452-133">There are 2 types of Web Storage: `localStorage` and `sessionStorage`.</span></span> <span data-ttu-id="00452-134">Chacun d’eux est conservé en tant que magasin de données distinct isolé du domaine qui l’a créé.</span><span class="sxs-lookup"><span data-stu-id="00452-134">Each is maintained as a separate data store isolated to the domain that created it.</span></span> `sessionStorage` <span data-ttu-id="00452-135">persiste uniquement pendant la durée de la session de navigation (par exemple, lorsque le navigateur est ouvert, ce qui inclut l’actualisation et les restaurations).</span><span class="sxs-lookup"><span data-stu-id="00452-135">persists only for the duration of the browsing session (for example, while the browser is open, which includes refresh and restores).</span></span> `localStorage` <span data-ttu-id="00452-136">persiste jusqu’à ce que les données soient supprimées par le code, l’utilisateur ou le navigateur (par exemple, en cas de stockage limité).</span><span class="sxs-lookup"><span data-stu-id="00452-136">persists until the data is removed by the code, the user, or the browser (for example, when there is limited storage available).</span></span> <span data-ttu-id="00452-137">L’extrait de code suivant montre comment utiliser , ce qui `localStorage` est similaire à la façon dont il est `sessionStorage` utilisé.</span><span class="sxs-lookup"><span data-stu-id="00452-137">The following code snippet shows how to use `localStorage`, which is similar to how `sessionStorage` is used.</span></span>

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

<span data-ttu-id="00452-138">Cet extrait de code extrait les métadonnées sur la page actuelle et les stocke dans un objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="00452-138">This code snippet grabs metadata about the current page and stores it in a JavaScript object.</span></span> <span data-ttu-id="00452-139">Ensuite, il stocke cette valeur en tant que JSON à l’aide de la méthode et affecte une clé `localStorage` `setItem()` égale à `window.location` l’URL actuelle.</span><span class="sxs-lookup"><span data-stu-id="00452-139">Then it stores that value as JSON in `localStorage` using the `setItem()` method, and assigns a key equal to the current `window.location` URL.</span></span> <span data-ttu-id="00452-140">Vous pouvez récupérer les informations à partir `localStorage` de l’utilisation de `getItem()` la méthode.</span><span class="sxs-lookup"><span data-stu-id="00452-140">You may retrieve the information from `localStorage` using the `getItem()` method.</span></span> 

<span data-ttu-id="00452-141">L’extrait de code suivant montre comment utiliser la mise en cache pour énumérer les pages mises en cache et extraire des métadonnées pour effectuer une tâche, telle que la création d’une liste de `localstorage` liens.</span><span class="sxs-lookup"><span data-stu-id="00452-141">The following code snippet shows how to use caching with `localstorage` to enumerate cached pages and extract metadata to perform a task, such as building a list of links.</span></span>

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

<span data-ttu-id="00452-142">La `insertOfflineLink()` méthode transmet l’URL de la demande à la `localStorage.getItem()` méthode pour récupérer les métadonnées stockées.</span><span class="sxs-lookup"><span data-stu-id="00452-142">The `insertOfflineLink()` method passes the URL of the request into the `localStorage.getItem()` method to retrieve any stored metadata.</span></span> <span data-ttu-id="00452-143">Les données récupérées sont vérifiées pour voir si elles existent et, si c’est le cas, une action peut être prise sur les données, telle que la création et l’insertion du marques de vérification pour les afficher.</span><span class="sxs-lookup"><span data-stu-id="00452-143">The retrieved data is checked to see if it exists, and if it does, an action can be taken on the data, such as building and inserting the markup to display it.</span></span>

## <a name="test-for-network-connections-in-your-pwa"></a><span data-ttu-id="00452-144">Tester les connexions réseau dans votre PWA</span><span class="sxs-lookup"><span data-stu-id="00452-144">Test for network connections in your PWA</span></span>

<span data-ttu-id="00452-145">Outre le stockage des informations pour une utilisation hors connexion, il est utile de savoir quand une connexion réseau est disponible pour synchroniser les données ou informer les utilisateurs que l’état du réseau a changé.</span><span class="sxs-lookup"><span data-stu-id="00452-145">In addition to storing information for offline use, it is helpful to know when a network connection is available in order to synchronize data or inform users that the network status has changed.</span></span> <span data-ttu-id="00452-146">Utilisez les options suivantes pour tester la connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="00452-146">Use the following options to test for network connectivity.</span></span>

### <a name="navigatoronline"></a><span data-ttu-id="00452-147">navigator.onLine</span><span class="sxs-lookup"><span data-stu-id="00452-147">navigator.onLine</span></span>  

<span data-ttu-id="00452-148">La propriété est un booléen qui vous permet de connaître `navigator.onLine` l’état actuel du réseau.</span><span class="sxs-lookup"><span data-stu-id="00452-148">The `navigator.onLine` property is a boolean that lets you know the current status of the network.</span></span> <span data-ttu-id="00452-149">Si la valeur est `true` , l’utilisateur est en ligne, sinon l’utilisateur est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="00452-149">If the value is `true`, the user is online, otherwise the user is offline.</span></span>

### <a name="online-and-offline-events"></a><span data-ttu-id="00452-150">Événements en ligne et hors connexion</span><span class="sxs-lookup"><span data-stu-id="00452-150">Online and Offline Events</span></span>  

<span data-ttu-id="00452-151">Il est utile de savoir si le réseau est disponible, mais vous pouvez prendre des mesures lorsque votre connectivité réseau change.</span><span class="sxs-lookup"><span data-stu-id="00452-151">Knowing whether the network is available is helpful, but you may want to take action  when your network connectivity changes.</span></span> <span data-ttu-id="00452-152">Dans ce cas, vous pouvez écouter et prendre des mesures en réponse à des événements réseau.</span><span class="sxs-lookup"><span data-stu-id="00452-152">In this situation, you may want to listen and take action in response to network events.</span></span> <span data-ttu-id="00452-153">Les événements sont disponibles sur les éléments , et comme affiché dans l’extrait de `window` `document` code `document.body` suivant.</span><span class="sxs-lookup"><span data-stu-id="00452-153">The events are available on the `window`, `document`, and `document.body` elements as displayed in the following code snippet.</span></span>

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## <a name="see-also"></a><span data-ttu-id="00452-154">Articles associés</span><span class="sxs-lookup"><span data-stu-id="00452-154">See also</span></span>  

<span data-ttu-id="00452-155">Pour en savoir plus sur la gestion des scénarios hors connexion, accédez aux pages suivantes.</span><span class="sxs-lookup"><span data-stu-id="00452-155">To learn more about managing offline scenarios, navigate to the following pages.</span></span>  

*   [<span data-ttu-id="00452-156">Cache</span><span class="sxs-lookup"><span data-stu-id="00452-156">Cache</span></span>][MDNCache]  
*   [<span data-ttu-id="00452-157">IndexedDB</span><span class="sxs-lookup"><span data-stu-id="00452-157">IndexedDB</span></span>][MDNIndexeddbApi]  
*   [<span data-ttu-id="00452-158">Service Worker</span><span class="sxs-lookup"><span data-stu-id="00452-158">Service Worker</span></span>][MDNServiceWorker]  
*   [<span data-ttu-id="00452-159">Web Stockage</span><span class="sxs-lookup"><span data-stu-id="00452-159">Web Storage</span></span>][MDNWebStorageApi]  
*   [<span data-ttu-id="00452-160">navigator.onLine</span><span class="sxs-lookup"><span data-stu-id="00452-160">navigator.onLine</span></span>][MDNNavigatoronline]  
*   [<span data-ttu-id="00452-161">Événements en ligne et hors connexion</span><span class="sxs-lookup"><span data-stu-id="00452-161">Online and Offline Events</span></span>][MDNNavigatoronlineOfflineEvents]  
*   [<span data-ttu-id="00452-162">Demande avec intention : stratégies de mise en cache à l’âge des PPA</span><span class="sxs-lookup"><span data-stu-id="00452-162">Request with Intent: Caching Strategies in the Age of PWAs</span></span>][AlistapartRequestIntentCachingStrategiesAgePwas]
    
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
