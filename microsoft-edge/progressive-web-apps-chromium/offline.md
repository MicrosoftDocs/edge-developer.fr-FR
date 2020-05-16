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
# <span data-ttu-id="717c3-104">Prise en charge du mode hors connexion et de la connectivité réseau dans les applications Web progressives</span><span class="sxs-lookup"><span data-stu-id="717c3-104">Offline and network connectivity support in Progressive Web Apps</span></span>

<span data-ttu-id="717c3-105">Pour de nombreuses années, les organisations se sont importées énormément de logiciels sur le Web par le biais de logiciels natifs, car les applications Web sont basées sur des connexions réseau stables.</span><span class="sxs-lookup"><span data-stu-id="717c3-105">For many years organizations were reluctant to invest heavily in web-based software over native software because web applications depended on stable network connections.</span></span> <span data-ttu-id="717c3-106">Aujourd’hui, la plateforme Web propose désormais des options puissantes qui permettent aux utilisateurs de continuer à travailler, même si la connexion réseau devient instable ou qu’elle est complètement hors connexion.</span><span class="sxs-lookup"><span data-stu-id="717c3-106">Today, the web platform now offers robust options that enable users to continue working, even if the network connection becomes unstable or goes completely offline.</span></span>

## <span data-ttu-id="717c3-107">Utiliser la mise en cache pour améliorer les performances de PWAs</span><span class="sxs-lookup"><span data-stu-id="717c3-107">Use the caching to improve performance of PWAs</span></span>

<span data-ttu-id="717c3-108">Avec l’introduction des [travailleurs de service][MDNServiceWorker], la plateforme Web a ajouté l' `Cache` API pour donner accès aux ressources mises en cache gérées.</span><span class="sxs-lookup"><span data-stu-id="717c3-108">With the introduction of [Service Workers][MDNServiceWorker], the web platform added the `Cache` API to provide access to managed cached resources.</span></span> <span data-ttu-id="717c3-109">Cette API basée sur la promesse permet aux développeurs de stocker et de récupérer de nombreuses ressources Web (HTML, CSS, JavaScript, images, JSON, etc.).</span><span class="sxs-lookup"><span data-stu-id="717c3-109">This Promise-based API allows developers to store and retrieve many web resources—HTML, CSS, JavaScript, images, JSON, and so on.</span></span> <span data-ttu-id="717c3-110">En règle générale, l’API de cache est utilisée dans le contexte d’un travailleur de service, mais elle est également disponible dans le thread principal de l' `window` objet.</span><span class="sxs-lookup"><span data-stu-id="717c3-110">Usually, the Cache API is used within the context of a Service Worker, but it is also available in the main thread on the `window` object.</span></span>

<span data-ttu-id="717c3-111">Une utilisation courante de l' `Cache` API consiste à mettre en cache les ressources critiques lors de l’installation d’un employé de service, comme illustré dans l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="717c3-111">One common use for the `Cache` API is to pre-cache critical resources when a Service Worker is installed, as shown in the following code snippet.</span></span>  

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

<span data-ttu-id="717c3-112">Ce code, qui s’exécute pendant la durée de vie du travailleur du service `install` , ouvre un cache nommé `static-cache` et, lorsqu’il possède un pointeur vers le cache, lui ajoute quatre ressources à l’aide de la `addAll()` méthode.</span><span class="sxs-lookup"><span data-stu-id="717c3-112">This code, which runs during the Service Worker `install` life cycle event, opens a cache named `static-cache` and then, when it has a pointer to the cache, adds four resources to it using the `addAll()` method.</span></span>  <span data-ttu-id="717c3-113">Souvent, l’approche est associée à la récupération du cache lors d’un `fetch` événement</span><span class="sxs-lookup"><span data-stu-id="717c3-113">Often the approach is coupled with cache retrieval during a `fetch` event</span></span>   

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

<span data-ttu-id="717c3-114">L’extrait de code s’exécute au sein du travailleur de service chaque fois que le navigateur effectue une `fetch` demande pour ce site.</span><span class="sxs-lookup"><span data-stu-id="717c3-114">The code snippet runs within the Service Worker whenever the browser makes a `fetch` request for this site.</span></span> <span data-ttu-id="717c3-115">Dans cet événement, il existe une instruction conditionnelle qui s’exécute si la requête concerne un fichier HTML.</span><span class="sxs-lookup"><span data-stu-id="717c3-115">Within that event, there is a conditional statement that runs if the request is for an HTML file.</span></span> <span data-ttu-id="717c3-116">Le travailleur de service vérifie si le fichier existe déjà dans le cache \ (en utilisant la `match()` méthode \).</span><span class="sxs-lookup"><span data-stu-id="717c3-116">The Service Worker checks to see if the file already exists in any cache \(using the `match()` method\).</span></span> <span data-ttu-id="717c3-117">Si la requête existe dans le cache, le résultat mis en cache est retourné.</span><span class="sxs-lookup"><span data-stu-id="717c3-117">If the request exists in the cache, that cached result is returned.</span></span> <span data-ttu-id="717c3-118">Si ce n’est pas le cas, une nouvelle `fetch` ressource est exécutée, une copie de la réponse est mise en cache pour le moment, et la réponse est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="717c3-118">If not, a new `fetch` for that resource is run, a copy of the response is cached for later, and the response is returned.</span></span> <span data-ttu-id="717c3-119">En cas `fetch` d’échec du réseau, la page hors connexion est renvoyée à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="717c3-119">If the `fetch` fails because the network is unavailable, the offline page is returned from the cache.</span></span>

<span data-ttu-id="717c3-120">Cette introduction simple montre comment utiliser la mise en cache dans votre application Web progressive (PWA).</span><span class="sxs-lookup"><span data-stu-id="717c3-120">This simple introduction shows how to use caching in your progressive web app (PWA).</span></span> <span data-ttu-id="717c3-121">Chaque PWA est différent et peut utiliser différentes stratégies de mise en cache.</span><span class="sxs-lookup"><span data-stu-id="717c3-121">Each PWA is different and may use different caching strategies.</span></span> <span data-ttu-id="717c3-122">Votre code risque de différer et vous pouvez utiliser différentes stratégies de mise en cache pour différents itinéraires au sein de la même application.</span><span class="sxs-lookup"><span data-stu-id="717c3-122">Your code may look different, and you may use different caching strategies for different routes within the same application.</span></span>

## <span data-ttu-id="717c3-123">Utiliser IndexedDB dans PWA pour stocker des données structurées</span><span class="sxs-lookup"><span data-stu-id="717c3-123">Use IndexedDB in your PWA to store structured data</span></span>

`IndexedDB` <span data-ttu-id="717c3-124">est une API pour le stockage des données structurées.</span><span class="sxs-lookup"><span data-stu-id="717c3-124">is an API for storing structured data.</span></span> <span data-ttu-id="717c3-125">Comme pour l' `Cache` API, il est également asynchrone, ce qui signifie que vous pouvez l’utiliser dans le thread principal ou avec des travailleurs Web tels que des travailleurs de service.</span><span class="sxs-lookup"><span data-stu-id="717c3-125">Similar to the `Cache` API, it is also asynchronous, which means you may use it in the main thread or with Web Workers such as Service Workers.</span></span> <span data-ttu-id="717c3-126">Utilisez l' `IndexedDB` API pour stocker une quantité significative de données structurées sur le client ou des données binaires telles que des objets multimédias chiffrés.</span><span class="sxs-lookup"><span data-stu-id="717c3-126">Use the `IndexedDB` API for storing a significant amount of structured data on the client, or binary data, such as encrypted media objects.</span></span> <span data-ttu-id="717c3-127">Pour plus d’informations, consultez la section [notions fondamentales sur MDN utilisation de IndexedDB][MDNIndexeddbApiUsing].</span><span class="sxs-lookup"><span data-stu-id="717c3-127">For more information, see [MDN primer on using IndexedDB][MDNIndexeddbApiUsing].</span></span>

## <span data-ttu-id="717c3-128">Comprendre les options de stockage pour PWAs</span><span class="sxs-lookup"><span data-stu-id="717c3-128">Understand storage options for PWAs</span></span>

<span data-ttu-id="717c3-129">Il peut arriver que vous deviez stocker de petites quantités de données afin de fournir une meilleure expérience hors connexion à vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="717c3-129">Sometimes you may need to store small amounts of data in order to provide a better offline experience for your users.</span></span> <span data-ttu-id="717c3-130">Si tel est le cas, il est possible que vous trouviez la simplicité du système de paire clé-valeur du stockage Web qui répond à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="717c3-130">If that is the case, you may find the simplicity of the key-value pair system of web storage meets your needs.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="717c3-131">Le stockage Web est un processus synchrone qui ne peut pas être utilisé dans les threads de travail, tels que les travailleurs de service.</span><span class="sxs-lookup"><span data-stu-id="717c3-131">Web Storage is a synchronous process and is not available for use within worker threads such as Service Workers.</span></span> <span data-ttu-id="717c3-132">Une utilisation intense risque de générer des problèmes de performances pour votre application.</span><span class="sxs-lookup"><span data-stu-id="717c3-132">Heavy usage may create performance issues for your application.</span></span> 


<span data-ttu-id="717c3-133">Il existe 2 types de stockage Web: `localStorage` et `sessionStorage` .</span><span class="sxs-lookup"><span data-stu-id="717c3-133">There are 2 types of Web Storage: `localStorage` and `sessionStorage`.</span></span> <span data-ttu-id="717c3-134">Chacun d’eux est géré en tant que magasin de données distinct isolé du domaine qui l’a créé.</span><span class="sxs-lookup"><span data-stu-id="717c3-134">Each is maintained as a separate data store isolated to the domain that created it.</span></span> `sessionStorage` <span data-ttu-id="717c3-135">persiste uniquement pendant la durée de la session de navigation (par exemple, lorsque le navigateur est ouvert, y compris l’actualisation et la restauration).</span><span class="sxs-lookup"><span data-stu-id="717c3-135">persists only for the duration of the browsing session (for example, while the browser is open, which includes refresh and restores).</span></span> `localStorage` <span data-ttu-id="717c3-136">persiste tant que les données n’ont pas été supprimées par le code, par l’utilisateur ou par le navigateur (par exemple, quand un stockage limité est disponible).</span><span class="sxs-lookup"><span data-stu-id="717c3-136">persists until the data is removed by the code, the user, or the browser (for example, when there is limited storage available).</span></span> <span data-ttu-id="717c3-137">L’extrait de code suivant montre comment utiliser `localStorage` , qui est similaire à celui `sessionStorage` utilisé.</span><span class="sxs-lookup"><span data-stu-id="717c3-137">The following code snippet shows how to use `localStorage`, which is similar to how `sessionStorage` is used.</span></span>

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

<span data-ttu-id="717c3-138">Cet extrait de code extrait les métadonnées relatives à la page active et les stocke dans un objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="717c3-138">This code snippet grabs metadata about the current page and stores it in a JavaScript object.</span></span> <span data-ttu-id="717c3-139">Il stocke ensuite cette valeur comme JSON lors de `localStorage` l’utilisation de la `setItem()` méthode et attribue une clé égale à l' `window.location` URL actuelle.</span><span class="sxs-lookup"><span data-stu-id="717c3-139">Then it stores that value as JSON in `localStorage` using the `setItem()` method, and assigns a key equal to the current `window.location` URL.</span></span> <span data-ttu-id="717c3-140">Vous pouvez récupérer les informations relatives `localStorage` à l’utilisation de la `getItem()` méthode.</span><span class="sxs-lookup"><span data-stu-id="717c3-140">You may retrieve the information from `localStorage` using the `getItem()` method.</span></span> 

<span data-ttu-id="717c3-141">L’extrait de code suivant montre comment utiliser la mise en cache `localstorage` pour énumérer les pages mises en cache et extraire les métadonnées pour effectuer une tâche, par exemple créer une liste de liens.</span><span class="sxs-lookup"><span data-stu-id="717c3-141">The following code snippet shows how to use caching with `localstorage` to enumerate cached pages and extract metadata to perform a task, such as building a list of links.</span></span>

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

<span data-ttu-id="717c3-142">La `insertOfflineLink()` méthode transmet l’URL de la requête dans la `localStorage.getItem()` méthode pour récupérer des métadonnées stockées.</span><span class="sxs-lookup"><span data-stu-id="717c3-142">The `insertOfflineLink()` method passes the URL of the request into the `localStorage.getItem()` method to retrieve any stored metadata.</span></span> <span data-ttu-id="717c3-143">Les données récupérées sont examinées pour voir s’il existe, et si tel est le cas, une action peut être effectuée sur les données, comme le bâtiment et l’insertion du balisage pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="717c3-143">The retrieved data is checked to see if it exists, and if it does, an action can be taken on the data, such as building and inserting the markup to display it.</span></span>

## <span data-ttu-id="717c3-144">Test de connexions réseau dans votre PWA</span><span class="sxs-lookup"><span data-stu-id="717c3-144">Test for network connections in your PWA</span></span>

<span data-ttu-id="717c3-145">Outre le stockage des informations pour une utilisation en mode hors connexion, il est utile de savoir à quel moment une connexion réseau est disponible pour synchroniser les données ou informer les utilisateurs que le statut du réseau a changé.</span><span class="sxs-lookup"><span data-stu-id="717c3-145">In addition to storing information for offline use, it is helpful to know when a network connection is available in order to synchronize data or inform users that the network status has changed.</span></span> <span data-ttu-id="717c3-146">Utilisez les options suivantes pour tester la connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="717c3-146">Use the following options to test for network connectivity.</span></span>

### <span data-ttu-id="717c3-147">Navigator. onLine</span><span class="sxs-lookup"><span data-stu-id="717c3-147">navigator.onLine</span></span>  

<span data-ttu-id="717c3-148">La `navigator.onLine` propriété est une valeur booléenne qui vous permet de connaître l’état actuel du réseau.</span><span class="sxs-lookup"><span data-stu-id="717c3-148">The `navigator.onLine` property is a boolean that lets you know the current status of the network.</span></span> <span data-ttu-id="717c3-149">Si la valeur est `true` , l’utilisateur est en ligne, sinon l’utilisateur est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="717c3-149">If the value is `true`, the user is online, otherwise the user is offline.</span></span>

### <span data-ttu-id="717c3-150">Événements en ligne et hors connexion</span><span class="sxs-lookup"><span data-stu-id="717c3-150">Online and Offline Events</span></span>  

<span data-ttu-id="717c3-151">Le fait de savoir si le réseau est disponible est utile, mais il se peut que vous souhaitiez agir en cas de modification de votre connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="717c3-151">Knowing whether the network is available is helpful, but you may want to take action  when your network connectivity changes.</span></span> <span data-ttu-id="717c3-152">Dans cette situation, il est possible que vous souhaitiez écouter et entreprendre une action en réponse à des événements réseau.</span><span class="sxs-lookup"><span data-stu-id="717c3-152">In this situation, you may want to listen and take action in response to network events.</span></span> <span data-ttu-id="717c3-153">Les événements sont disponibles sur les `window` `document` éléments, et `document.body` comme illustré dans l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="717c3-153">The events are available on the `window`, `document`, and `document.body` elements as displayed in the following code snippet.</span></span>

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## <span data-ttu-id="717c3-154">Voir également</span><span class="sxs-lookup"><span data-stu-id="717c3-154">See also</span></span>  

<span data-ttu-id="717c3-155">Pour en savoir plus sur la gestion des scénarios hors connexion, voir les pages suivantes.</span><span class="sxs-lookup"><span data-stu-id="717c3-155">To learn more about managing offline scenarios, see the following pages.</span></span>  

*   [<span data-ttu-id="717c3-156">Cache</span><span class="sxs-lookup"><span data-stu-id="717c3-156">Cache</span></span>][MDNCache]  
*   [<span data-ttu-id="717c3-157">IndexedDB</span><span class="sxs-lookup"><span data-stu-id="717c3-157">IndexedDB</span></span>][MDNIndexeddbApi]  
*   [<span data-ttu-id="717c3-158">Travailleur de service</span><span class="sxs-lookup"><span data-stu-id="717c3-158">Service Worker</span></span>][MDNServiceWorker]  
*   [<span data-ttu-id="717c3-159">Stockage Web</span><span class="sxs-lookup"><span data-stu-id="717c3-159">Web Storage</span></span>][MDNWebStorageApi]  
*   [<span data-ttu-id="717c3-160">Navigator. onLine</span><span class="sxs-lookup"><span data-stu-id="717c3-160">navigator.onLine</span></span>][MDNNavigatoronline]  
*   [<span data-ttu-id="717c3-161">Événements en ligne et hors connexion</span><span class="sxs-lookup"><span data-stu-id="717c3-161">Online and Offline Events</span></span>][MDNNavigatoronlineOfflineEvents]  
*   [<span data-ttu-id="717c3-162">Demander avec des conseils: stratégies de mise en cache de l’âge de PWAs</span><span class="sxs-lookup"><span data-stu-id="717c3-162">Request with Intent: Caching Strategies in the Age of PWAs</span></span>][AlistapartRequestIntentCachingStrategiesAgePwas]

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
