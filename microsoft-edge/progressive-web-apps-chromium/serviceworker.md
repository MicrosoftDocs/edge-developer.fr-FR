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
# <a name="use-service-workers-to-manage-network-requests-and-push-notifications"></a><span data-ttu-id="af993-104">Utiliser les employés de service pour gérer les demandes réseau et les notifications Push</span><span class="sxs-lookup"><span data-stu-id="af993-104">Use Service Workers to manage network requests and push notifications</span></span>

<span data-ttu-id="af993-105">Les travailleurs de service sont un type spécial de travail web ayant la possibilité d’intercepter, de modifier et de répondre à toutes les demandes réseau à l’aide de `Fetch` l’API.</span><span class="sxs-lookup"><span data-stu-id="af993-105">Service Workers are a special type of Web Worker with the ability to intercept, modify, and respond to all network requests using the `Fetch` API.</span></span>  <span data-ttu-id="af993-106">Les employés de service peuvent accéder à l’API et aux magasins de données `Cache` côté client asynchrones, tels que, pour `IndexedDB` stocker des ressources.</span><span class="sxs-lookup"><span data-stu-id="af993-106">Service Workers can access the `Cache` API, and asynchronous client-side data stores, such as `IndexedDB`, to store resources.</span></span>  

## <a name="registering-a-service-worker"></a><span data-ttu-id="af993-107">Inscription d’un service de travail</span><span class="sxs-lookup"><span data-stu-id="af993-107">Registering a Service Worker</span></span>  

<span data-ttu-id="af993-108">Comme d’autres travailleurs web, les travailleurs du service doivent exister dans un fichier distinct.</span><span class="sxs-lookup"><span data-stu-id="af993-108">Similar to other Web Workers, Service Workers must exist in a separate file.</span></span> <span data-ttu-id="af993-109">Vous référencez ce fichier lors de l’inscription du service de travail, comme illustré dans l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="af993-109">You reference this file when registering the Service Worker, as shown in the following code snippet.</span></span>  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

<span data-ttu-id="af993-110">Les navigateurs modernes fournissent différents niveaux de prise en charge pour les travailleurs du service.</span><span class="sxs-lookup"><span data-stu-id="af993-110">Modern browsers provide different levels of support for Service Workers.</span></span> <span data-ttu-id="af993-111">En tant que tel, il est bon de tester l’existence de l’objet avant d’exécution d’un code lié au service `serviceWorker` de travail.</span><span class="sxs-lookup"><span data-stu-id="af993-111">As such, it is a good practice to test for the existence of the `serviceWorker` object before running any Service Worker-related code.</span></span> <span data-ttu-id="af993-112">Dans l’extrait de code ci-dessus, un service de travail est enregistré à l’aide du fichier situé à la `serviceworker.min.js` racine du site.</span><span class="sxs-lookup"><span data-stu-id="af993-112">In the above code snippet, a Service Worker is registered using the `serviceworker.min.js` file located at the root of the site.</span></span> <span data-ttu-id="af993-113">Assurez-vous que le fichier JavaScript qui définit votre service de travail existe dans le répertoire de niveau le plus élevé que vous souhaitez qu’il gère \(qui est appelé étendue du Service Worker\).</span><span class="sxs-lookup"><span data-stu-id="af993-113">Ensure that the JavaScript file that defines your Service Worker exists in the highest-level directory that you want it to manage \(which is referred to as the scope of the Service Worker\).</span></span>  <span data-ttu-id="af993-114">Dans l’extrait de code précédent, le fichier est stocké à la racine et le service de travail gère toutes les pages du domaine.</span><span class="sxs-lookup"><span data-stu-id="af993-114">In the previous code snippet, the file is stored in the root, and the Service Worker manages all pages in the domain.</span></span> <span data-ttu-id="af993-115">Si le fichier de travail de service était stocké dans un répertoire, l’étendue du service de travail serait le répertoire et tous les `js` `js` sous-répertoires.</span><span class="sxs-lookup"><span data-stu-id="af993-115">If the Service Worker file was stored in a `js` directory, the scope of the Service Worker would be the `js` directory and any subdirectories.</span></span>  <span data-ttu-id="af993-116">En tant que meilleure pratique, placez le fichier de travail de service à la racine de votre site, sauf si vous devez réduire l’étendue de votre service de travail.</span><span class="sxs-lookup"><span data-stu-id="af993-116">As a best practice, place the Service Worker file in the root of your site, unless you need to reduce the scope of your Service Worker.</span></span>  

## <a name="the-service-worker-lifecycle"></a><span data-ttu-id="af993-117">Cycle de vie des travailleurs du service</span><span class="sxs-lookup"><span data-stu-id="af993-117">The Service Worker lifecycle</span></span>  

<span data-ttu-id="af993-118">Le cycle de vie d’un service de travail se compose de plusieurs étapes, chaque étape déclenchant un événement.</span><span class="sxs-lookup"><span data-stu-id="af993-118">The lifecycle of a Service Worker consists of multiple steps, with each step triggering an event.</span></span> <span data-ttu-id="af993-119">Vous pouvez ajouter des écouteurs à ces événements pour exécuter du code pour effectuer une action.</span><span class="sxs-lookup"><span data-stu-id="af993-119">You can add listeners to these events to run code to perform an action.</span></span> <span data-ttu-id="af993-120">La liste suivante présente une vue d’un haut niveau du cycle de vie et des événements connexes des travailleurs du service.</span><span class="sxs-lookup"><span data-stu-id="af993-120">The following list presents a high-level view of the lifecycle and related events of service workers.</span></span> 

1.  <span data-ttu-id="af993-121">Inscrivez le service de travail.</span><span class="sxs-lookup"><span data-stu-id="af993-121">Register the Service Worker.</span></span>  
1.  <span data-ttu-id="af993-122">Le navigateur télécharge le fichier JavaScript, installe le service de travail et déclenche `install` l’événement.</span><span class="sxs-lookup"><span data-stu-id="af993-122">The browser downloads the JavaScript file, installs the Service Worker, and triggers the `install` event.</span></span> <span data-ttu-id="af993-123">Vous pouvez utiliser l’événement pour pré-mettre en cache tous les fichiers importants et à durée de vie longue, tels que les fichiers CSS, les fichiers JavaScript, les images de logo, les pages hors connexion, etc. à partir de votre `install` site web.</span><span class="sxs-lookup"><span data-stu-id="af993-123">You can use the `install` event to pre-cache any important and long-lived files, such as CSS files, JavaScript files, logo images, offline pages, and so on from your website.</span></span>  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  <span data-ttu-id="af993-124">Le service de travail est activé, ce qui déclenche `activate` l’événement.</span><span class="sxs-lookup"><span data-stu-id="af993-124">The Service Worker is activated, which triggers the `activate` event.</span></span>  <span data-ttu-id="af993-125">Utilisez cet événement pour nettoyer les caches obsolètes.</span><span class="sxs-lookup"><span data-stu-id="af993-125">Use this event to clean up outdated caches.</span></span>  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  <span data-ttu-id="af993-126">Le service de travail est prêt à s’exécuter lorsque la page est actualisée ou lorsque l’utilisateur navigue vers une nouvelle page sur le site.</span><span class="sxs-lookup"><span data-stu-id="af993-126">The Service Worker is ready to run when the page is refreshed or when the user navigates to a new page on the site.</span></span> <span data-ttu-id="af993-127">Si vous souhaitez exécuter le service de travail sans attendre, utilisez `self.skipWaiting()` la méthode pendant `install` l’événement.</span><span class="sxs-lookup"><span data-stu-id="af993-127">If you want to run the Service Worker without waiting, use the `self.skipWaiting()` method during the `install` event.</span></span>  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  <span data-ttu-id="af993-128">Le service de travail est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="af993-128">The Service Worker is now running.</span></span>     
    
## <a name="using-fetch-in-service-workers"></a><span data-ttu-id="af993-129">Utilisation de la récupération dans les travailleurs du service</span><span class="sxs-lookup"><span data-stu-id="af993-129">Using fetch in Service Workers</span></span>  

<span data-ttu-id="af993-130">L’événement principal que vous utilisez dans un service de travail est `fetch` l’événement.</span><span class="sxs-lookup"><span data-stu-id="af993-130">The main event that you use in a Service Worker is the `fetch` event.</span></span>  <span data-ttu-id="af993-131">L’événement s’exécute chaque fois que le navigateur tente d’accéder au contenu `fetch` dans l’étendue du service de travail.</span><span class="sxs-lookup"><span data-stu-id="af993-131">The `fetch` event runs every time the browser attempts to access content within the scope of the Service Worker.</span></span> <span data-ttu-id="af993-132">L’extrait de code suivant montre comment ajouter un listener à l’événement fetch.</span><span class="sxs-lookup"><span data-stu-id="af993-132">The following code snippet shows how to add a listener to the fetch event.</span></span>  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

<span data-ttu-id="af993-133">Au sein du handler, vous pouvez contrôler si une demande est traitée sur le réseau, s’il est tiré du `fetch` cache, etc.</span><span class="sxs-lookup"><span data-stu-id="af993-133">Within the `fetch` handler, you may control whether a request goes to the network, pulls from the cache, and so on.</span></span>  <span data-ttu-id="af993-134">L’approche que vous prenez varie probablement en fonction du type de ressource demandée, de la fréquence de sa mise à jour et d’une autre logique métier propre à votre application.</span><span class="sxs-lookup"><span data-stu-id="af993-134">The approach you take likely varies based upon the type of resource being requested, how frequently it is updated, and other business logic unique to your application.</span></span>  <span data-ttu-id="af993-135">Voici quelques exemples de ce que vous pouvez faire :</span><span class="sxs-lookup"><span data-stu-id="af993-135">Here are a few examples of what you may do:</span></span>  

*   <span data-ttu-id="af993-136">Si disponible, renvoyer une réponse à partir du cache, sinon de secours pour demander la ressource sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="af993-136">If available, return a response from the cache, otherwise fallback to request the resource over the network.</span></span>  
*   <span data-ttu-id="af993-137">Récupérer une ressource à partir du réseau, mettre en cache une copie et renvoyer la réponse.</span><span class="sxs-lookup"><span data-stu-id="af993-137">Fetch a resource from the network, cache a copy, and return the response.</span></span>
*   <span data-ttu-id="af993-138">Autoriser les utilisateurs à spécifier une préférence pour enregistrer des données.</span><span class="sxs-lookup"><span data-stu-id="af993-138">Allow user's to specify a preference to save data.</span></span> 
*   <span data-ttu-id="af993-139">Fournir une image d’espace réservé pour certaines demandes d’image.</span><span class="sxs-lookup"><span data-stu-id="af993-139">Supply a placeholder image for certain image requests.</span></span>  
*   <span data-ttu-id="af993-140">Générer une réponse directement dans le service de travail.</span><span class="sxs-lookup"><span data-stu-id="af993-140">Generate a response directly in the Service Worker.</span></span>  
    
## <a name="push-notifications"></a><span data-ttu-id="af993-141">Push Notifications</span><span class="sxs-lookup"><span data-stu-id="af993-141">Push Notifications</span></span>  

<span data-ttu-id="af993-142">Les employés de service peuvent envoyer des notifications aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="af993-142">Service workers can push notifications to users.</span></span> <span data-ttu-id="af993-143">Les notifications Push sont utiles pour inciter les utilisateurs à interagir à l’aide de votre application après un certain temps.</span><span class="sxs-lookup"><span data-stu-id="af993-143">Push Notifications are helpful to prompt users to re-engage with your application after some time has elapsed.</span></span> <span data-ttu-id="af993-144">Pour plus d’informations, accédez à la démonstration et à la démonstration des [notifications Push.][AzurewebsitesWebpushdemo]</span><span class="sxs-lookup"><span data-stu-id="af993-144">For more information, navigate to [Push Notifications walkthrough and demo][AzurewebsitesWebpushdemo].</span></span>  

## <a name="see-also"></a><span data-ttu-id="af993-145">Voir également</span><span class="sxs-lookup"><span data-stu-id="af993-145">See also</span></span>  

<span data-ttu-id="af993-146">Pour en savoir plus sur les travailleurs de service, accédez à la liste suivante des rubriques connexes.</span><span class="sxs-lookup"><span data-stu-id="af993-146">To learn more about Service Workers, navigate to the following list of related topics.</span></span>  

*   [<span data-ttu-id="af993-147">Mise en mode hors connexion des P PWA avec les travailleurs du service</span><span class="sxs-lookup"><span data-stu-id="af993-147">Making PWAs work offline with Service workers</span></span>][MDNPwasMakingOfflineServiceWorkers]  
*   [<span data-ttu-id="af993-148">Comment rendre les P.A.S. ré-engageables à l’aide de Notifications et Push</span><span class="sxs-lookup"><span data-stu-id="af993-148">How to make PWAs re-engageable using Notifications and Push</span></span>][MDNPwasMakeReengageablesingNotificationsPush]  
    
<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Web Push Notifications |  Démonstrations de Microsoft Edge"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Mise en mode hors connexion des P PWAs avec les travailleurs du service : les P PWAs | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "Comment rendre les PAS ré-engageables à l’aide de Notifications et Push - P PWAs | MDN"  
