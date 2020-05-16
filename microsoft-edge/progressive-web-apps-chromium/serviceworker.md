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
# <span data-ttu-id="2f1af-104">Utiliser des travailleurs de services pour gérer les demandes réseau et les notifications de transmission</span><span class="sxs-lookup"><span data-stu-id="2f1af-104">Use Service Workers to manage network requests and push notifications</span></span>

<span data-ttu-id="2f1af-105">Les travailleurs de service constituent un type spécial de travailleur Web qui peut intercepter, modifier et répondre à toutes les requêtes réseau à l’aide de l' `Fetch` API.</span><span class="sxs-lookup"><span data-stu-id="2f1af-105">Service Workers are a special type of Web Worker with the ability to intercept, modify, and respond to all network requests using the `Fetch` API.</span></span>  <span data-ttu-id="2f1af-106">Les travailleurs de services peuvent accéder `Cache` à l’API et aux magasins de données côté client asynchrones, par exemple `IndexedDB` pour stocker des ressources.</span><span class="sxs-lookup"><span data-stu-id="2f1af-106">Service Workers can access the `Cache` API, and asynchronous client-side data stores, such as `IndexedDB`, to store resources.</span></span>  

## <span data-ttu-id="2f1af-107">Enregistrement d’un travailleur de service</span><span class="sxs-lookup"><span data-stu-id="2f1af-107">Registering a Service Worker</span></span>  

<span data-ttu-id="2f1af-108">À l’instar des autres travailleurs sur le Web, les travailleurs de services doivent exister dans un fichier distinct.</span><span class="sxs-lookup"><span data-stu-id="2f1af-108">Similar to other Web Workers, Service Workers must exist in a separate file.</span></span> <span data-ttu-id="2f1af-109">Vous référencez ce fichier lors de l’enregistrement du travailleur de service, comme le montre l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="2f1af-109">You reference this file when registering the Service Worker, as shown in the following code snippet.</span></span>  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

<span data-ttu-id="2f1af-110">Les navigateurs modernes fournissent différents niveaux de prise en charge pour les travailleurs de service.</span><span class="sxs-lookup"><span data-stu-id="2f1af-110">Modern browsers provide different levels of support for Service Workers.</span></span> <span data-ttu-id="2f1af-111">C’est pourquoi il est recommandé de tester l’existence de l' `serviceWorker` objet avant d’exécuter tout code lié au travailleur du service.</span><span class="sxs-lookup"><span data-stu-id="2f1af-111">As such, it is a good practice to test for the existence of the `serviceWorker` object before running any Service Worker-related code.</span></span> <span data-ttu-id="2f1af-112">Dans l’extrait de code ci-dessus, un ouvrier de service est enregistré à l’aide du `serviceworker.min.js` fichier situé à la racine du site.</span><span class="sxs-lookup"><span data-stu-id="2f1af-112">In the above code snippet, a Service Worker is registered using the `serviceworker.min.js` file located at the root of the site.</span></span> <span data-ttu-id="2f1af-113">Assurez-vous que le fichier JavaScript qui définit votre service d’assistance existe dans le répertoire de niveau supérieur que vous voulez qu’il gère \ (qui est appelé application du travailleur de service).</span><span class="sxs-lookup"><span data-stu-id="2f1af-113">Ensure that the JavaScript file that defines your Service Worker exists in the highest-level directory that you want it to manage \(which is referred to as the scope of the Service Worker\).</span></span>  <span data-ttu-id="2f1af-114">Dans l’extrait de code ci-dessus, le fichier est stocké à la racine et le travailleur de service gère toutes les pages du domaine.</span><span class="sxs-lookup"><span data-stu-id="2f1af-114">In the above code snippet, the file is stored in the root, and the Service Worker manages all pages in the domain.</span></span> <span data-ttu-id="2f1af-115">Si le fichier de travailleur de service était stocké dans un `js` répertoire, l’étendue du travailleur de service sera le `js` répertoire et tous ses sous-répertoires.</span><span class="sxs-lookup"><span data-stu-id="2f1af-115">If the Service Worker file was stored in a `js` directory, the scope of the Service Worker would be the `js` directory and any subdirectories.</span></span>  <span data-ttu-id="2f1af-116">Nous vous conseillons de placer le fichier du travailleur de service à la racine de votre site, sauf si vous avez besoin de réduire l’étendue de votre travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="2f1af-116">As a best practice, place the Service Worker file in the root of your site, unless you need to reduce the scope of your Service Worker.</span></span>  

## <span data-ttu-id="2f1af-117">Cycle de vie du travailleur de service</span><span class="sxs-lookup"><span data-stu-id="2f1af-117">The Service Worker lifecycle</span></span>  

<span data-ttu-id="2f1af-118">Le cycle de vie d’un travailleur de service se compose de plusieurs étapes, chaque étape déclenchant un événement.</span><span class="sxs-lookup"><span data-stu-id="2f1af-118">The lifecycle of a Service Worker consists of multiple steps, with each step triggering an event.</span></span> <span data-ttu-id="2f1af-119">Vous pouvez ajouter des écouteurs à ces événements pour exécuter du code afin d’effectuer une action.</span><span class="sxs-lookup"><span data-stu-id="2f1af-119">You can add listeners to these events to run code to perform an action.</span></span> <span data-ttu-id="2f1af-120">La liste suivante présente une vue d’ensemble du cycle de vie et des événements liés des travailleurs de service.</span><span class="sxs-lookup"><span data-stu-id="2f1af-120">The following list presents a high-level view of the lifecycle and related events of service workers.</span></span> 

1. <span data-ttu-id="2f1af-121">Enregistrez le travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="2f1af-121">Register the Service Worker.</span></span>  
1.  <span data-ttu-id="2f1af-122">Le navigateur télécharge le fichier JavaScript, installe le travailleur du service et déclenche l' `install` événement.</span><span class="sxs-lookup"><span data-stu-id="2f1af-122">The browser downloads the JavaScript file, installs the Service Worker, and triggers the `install` event.</span></span> <span data-ttu-id="2f1af-123">Vous pouvez utiliser l' `install` événement pour mettre en cache tout fichier important et à durée de vie longue (par exemple, fichiers CSS, fichiers JavaScript, images de logo, pages hors connexion, etc.) de votre site Web.</span><span class="sxs-lookup"><span data-stu-id="2f1af-123">You can use the `install` event to pre-cache any important and long-lived files, such as CSS files, JavaScript files, logo images, offline pages, and so on from your website.</span></span>  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  <span data-ttu-id="2f1af-124">Le travailleur de service est activé, ce qui déclenche l' `activate` événement.</span><span class="sxs-lookup"><span data-stu-id="2f1af-124">The Service Worker is activated, which triggers the `activate` event.</span></span>  <span data-ttu-id="2f1af-125">Utilisez cet événement pour nettoyer les caches obsolètes.</span><span class="sxs-lookup"><span data-stu-id="2f1af-125">Use this event to clean up outdated caches.</span></span>  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  <span data-ttu-id="2f1af-126">Le travailleur de service est prêt à s’exécuter lorsque la page est actualisée ou lorsque l’utilisateur navigue vers une nouvelle page sur le site.</span><span class="sxs-lookup"><span data-stu-id="2f1af-126">The Service Worker is ready to run when the page is refreshed or when the user navigates to a new page on the site.</span></span> <span data-ttu-id="2f1af-127">Si vous souhaitez exécuter le travailleur de service sans attendre, utilisez la `self.skipWaiting()` méthode pendant l' `install` événement.</span><span class="sxs-lookup"><span data-stu-id="2f1af-127">If you want to run the Service Worker without waiting, use the `self.skipWaiting()` method during the `install` event.</span></span>  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  <span data-ttu-id="2f1af-128">Le travailleur du service s’exécute actuellement.</span><span class="sxs-lookup"><span data-stu-id="2f1af-128">The Service Worker is now running.</span></span>     
    
## <span data-ttu-id="2f1af-129">Utilisation de FETCH dans les travailleurs de service</span><span class="sxs-lookup"><span data-stu-id="2f1af-129">Using fetch in Service Workers</span></span>  

<span data-ttu-id="2f1af-130">Il s’agit de l’événement principal que vous utilisez dans un travailleur de service `fetch` .</span><span class="sxs-lookup"><span data-stu-id="2f1af-130">The main event that you use in a Service Worker is the `fetch` event.</span></span>  <span data-ttu-id="2f1af-131">L' `fetch` événement s’exécute chaque fois que le navigateur tente d’accéder au contenu dans le cadre du travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="2f1af-131">The `fetch` event runs every time the browser attempts to access content within the scope of the Service Worker.</span></span> <span data-ttu-id="2f1af-132">L’extrait de code suivant montre comment ajouter un écouteur à l’événement Fetch.</span><span class="sxs-lookup"><span data-stu-id="2f1af-132">The following code snippet shows how to add a listener to the fetch event.</span></span>  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

<span data-ttu-id="2f1af-133">Dans le `fetch` Gestionnaire, vous pouvez contrôler si une requête accède au réseau, s’extrait du cache, etc.</span><span class="sxs-lookup"><span data-stu-id="2f1af-133">Within the `fetch` handler, you may control whether a request goes to the network, pulls from the cache, and so on.</span></span>  <span data-ttu-id="2f1af-134">L’approche que vous prenez peut varier en fonction du type de ressource demandé, de la fréquence de mise à jour et d’autres logiques métiers propres à votre application.</span><span class="sxs-lookup"><span data-stu-id="2f1af-134">The approach you take likely varies based upon the type of resource being requested, how frequently it is updated, and other business logic unique to your application.</span></span>  <span data-ttu-id="2f1af-135">Voici quelques exemples de ce que vous pouvez faire:</span><span class="sxs-lookup"><span data-stu-id="2f1af-135">Here are a few examples of what you may do:</span></span>  

*   <span data-ttu-id="2f1af-136">S’il est disponible, renvoyer une réponse à partir du cache, sinon le secours pour demander la ressource sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="2f1af-136">If available, return a response from the cache, otherwise fallback to request the resource over the network.</span></span>  
*   <span data-ttu-id="2f1af-137">Récupérer une ressource à partir du réseau, en mettre en cache une copie et retourner la réponse.</span><span class="sxs-lookup"><span data-stu-id="2f1af-137">Fetch a resource from the network, cache a copy, and return the response.</span></span>
*   <span data-ttu-id="2f1af-138">Permettre aux utilisateurs de spécifier une préférence pour enregistrer les données.</span><span class="sxs-lookup"><span data-stu-id="2f1af-138">Allow user's to specify a preference to save data.</span></span> 
*   <span data-ttu-id="2f1af-139">Fournissez une image d’espace réservé pour certaines requêtes d’image.</span><span class="sxs-lookup"><span data-stu-id="2f1af-139">Supply a placeholder image for certain image requests.</span></span>  
*   <span data-ttu-id="2f1af-140">Générer une réponse directement dans le travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="2f1af-140">Generate a response directly in the Service Worker.</span></span>  

## <span data-ttu-id="2f1af-141">Notifications de transmission</span><span class="sxs-lookup"><span data-stu-id="2f1af-141">Push Notifications</span></span>  

<span data-ttu-id="2f1af-142">Les travailleurs de services peuvent transmettre les notifications aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2f1af-142">Service workers can push notifications to users.</span></span> <span data-ttu-id="2f1af-143">Les notifications de transmission sont utiles pour inviter les utilisateurs à se réengager avec votre application après un certain temps.</span><span class="sxs-lookup"><span data-stu-id="2f1af-143">Push Notifications are helpful to prompt users to re-engage with your application after some time has elapsed.</span></span> <span data-ttu-id="2f1af-144">Pour plus d’informations, reportez-vous à la rubrique [démonstration de notifications de transmission][AzurewebsitesWebpushdemo].</span><span class="sxs-lookup"><span data-stu-id="2f1af-144">For more information, see [Push Notifications walkthrough and demo][AzurewebsitesWebpushdemo].</span></span>  

## <span data-ttu-id="2f1af-145">Voir également</span><span class="sxs-lookup"><span data-stu-id="2f1af-145">See also</span></span>  

<span data-ttu-id="2f1af-146">Pour en savoir plus sur les travailleurs de service, consultez la liste suivante de rubriques connexes.</span><span class="sxs-lookup"><span data-stu-id="2f1af-146">To learn more about Service Workers, see the following list of related topics.</span></span>  

*   [<span data-ttu-id="2f1af-147">Rendre PWAs travailler hors connexion avec des travailleurs de service</span><span class="sxs-lookup"><span data-stu-id="2f1af-147">Making PWAs work offline with Service workers</span></span>][MDNPwasMakingOfflineServiceWorkers]  
*   [<span data-ttu-id="2f1af-148">Comment faire pour rendre PWAs à nouveau à l’aide de notifications et de l’émission</span><span class="sxs-lookup"><span data-stu-id="2f1af-148">How to make PWAs re-engageable using Notifications and Push</span></span>][MDNPwasMakeReengageablesingNotificationsPush]  

<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Notifications de transmission Web |  Démonstrations de Microsoft Edge"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Faire en sorte que PWAs travaille hors connexion avec des travailleurs de services-PWAs | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "Comment rendre PWAs réutilisable à l’aide de notifications et de PWAs | MDN"  
