---
description: Utilisez le panneau application pour inspecter, modifier et déboguer des manifestes de l’application Web, des travailleurs de services et des mises en cache de service.
title: Déboguer des applications Web progressives
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 7eb71d0d57d8a9227a54b921f15dfe434ad6e65b
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993603"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# <span data-ttu-id="f45d3-104">Déboguer des applications Web progressives</span><span class="sxs-lookup"><span data-stu-id="f45d3-104">Debug Progressive Web Apps</span></span>   



<span data-ttu-id="f45d3-105">Utilisez le panneau **application** pour inspecter, modifier et déboguer des manifestes de l’application Web, des travailleurs de services et des mises en cache de service.</span><span class="sxs-lookup"><span data-stu-id="f45d3-105">Use the **Application** panel to inspect, modify, and debug web app manifests, service workers, and service worker caches.</span></span>  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

<span data-ttu-id="f45d3-106">Ce guide traite uniquement des fonctionnalités d’application Web progressive du panneau **application** .</span><span class="sxs-lookup"><span data-stu-id="f45d3-106">This guide only discusses the Progressive Web App features of the **Application** panel.</span></span>  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### <span data-ttu-id="f45d3-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="f45d3-107">Summary</span></span>  

*   <span data-ttu-id="f45d3-108">Utilisez le volet **manifeste** pour examiner le manifeste de votre application Web et déclencher l’ajout aux événements écran d’accueil.</span><span class="sxs-lookup"><span data-stu-id="f45d3-108">Use the **Manifest** pane to inspect your web app manifest and trigger Add to Homescreen events.</span></span>  
*   <span data-ttu-id="f45d3-109">Utilisez le volet **travailleurs de services** pour une gamme complète de tâches associées au service, telles que l’annulation de l’inscription ou la mise à jour d’un service, l’émulation des événements de transmission, la mise hors connexion ou l’arrêt d’un service.</span><span class="sxs-lookup"><span data-stu-id="f45d3-109">Use the **Service Workers** pane for a whole range of service-worker-related tasks, like unregistering or updating a service, emulating push events, going offline, or stopping a service worker.</span></span>  
*   <span data-ttu-id="f45d3-110">Affichez le cache de votre service d’assistance dans le volet **stockage du cache** .</span><span class="sxs-lookup"><span data-stu-id="f45d3-110">View your service worker cache from the **Cache Storage** pane.</span></span>  
*   <span data-ttu-id="f45d3-111">Annulez l’enregistrement d’un ouvrier de services et effacez l’intégralité du stockage et des caches à l’aide d’un seul bouton dans le volet de **stockage clair** .</span><span class="sxs-lookup"><span data-stu-id="f45d3-111">Unregister a service worker and clear all storage and caches with a single button click from the **Clear storage** pane.</span></span>  
    
## <span data-ttu-id="f45d3-112">Manifeste de l’application Web</span><span class="sxs-lookup"><span data-stu-id="f45d3-112">Web app manifest</span></span>   

<span data-ttu-id="f45d3-113">Si vous souhaitez que vos utilisateurs puissent ajouter votre application à leur mobile homescreens, vous avez besoin d’un manifeste d’application Web.</span><span class="sxs-lookup"><span data-stu-id="f45d3-113">If you want your users to be able to add your app to their mobile homescreens, you need a web app manifest.</span></span>  <span data-ttu-id="f45d3-114">Le manifeste définit la façon dont l’application s’affiche sur le écran d’accueil, où diriger l’utilisateur lors du lancement à partir de écran d’accueil, et l’apparence de l’application au moment du lancement.</span><span class="sxs-lookup"><span data-stu-id="f45d3-114">The manifest defines how the app appears on the homescreen, where to direct the user when launching from homescreen, and what the app looks like on launch.</span></span>  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

<span data-ttu-id="f45d3-115">Une fois votre manifeste configuré, vous pouvez utiliser le volet **manifeste** du panneau de l' **application** pour l’inspecter.</span><span class="sxs-lookup"><span data-stu-id="f45d3-115">After you have your manifest set up, you can use the **Manifest** pane of the **Application** panel to inspect it.</span></span>  

:::image type="complex" source="./media/manifest-pane.msft.png" alt-text="Volet manifeste" lightbox="./media/manifest-pane.msft.png":::
   <span data-ttu-id="f45d3-117">Volet **manifeste**</span><span class="sxs-lookup"><span data-stu-id="f45d3-117">The **Manifest** Pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="f45d3-118">Pour examiner la source du manifeste, cliquez sur le lien ci-dessous intitulé du manifeste de l' **application** \ ( `https://airhorner.com/manifest.json` dans la figure ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="f45d3-118">To look at the manifest source, click the link below **App Manifest** label \(`https://airhorner.com/manifest.json` in the previous figure\).</span></span>  
<!-- *   Press the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   <span data-ttu-id="f45d3-119">Les sections **identité** et **Présentation** affichent simplement les champs de la source du manifeste dans un affichage plus convivial.</span><span class="sxs-lookup"><span data-stu-id="f45d3-119">The **Identity** and **Presentation** sections just display fields from the manifest source in a more user-friendly display.</span></span>  
*   <span data-ttu-id="f45d3-120">La section **icônes** affiche chaque icône que vous avez spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f45d3-120">The **Icons** section displays every icon that you've specified.</span></span>  
    
<!--### Simulate Add to Homescreen events   -->

<!--A web app can only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, this criteria can be inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You can test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Clicking on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="./media/io.msft.png" alt-text="Add to desktop shelf" lightbox="./media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature cannot yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you can successfully add your app to your desktop shelf, then it'll work for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you can connect a real mobile device to DevTools via **remote debugging**, and then click the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## <span data-ttu-id="f45d3-121">Travailleurs de service</span><span class="sxs-lookup"><span data-stu-id="f45d3-121">Service workers</span></span>   

<span data-ttu-id="f45d3-122">Les travailleurs de service constituent une technologie fondamentale dans la prochaine plateforme Web.</span><span class="sxs-lookup"><span data-stu-id="f45d3-122">Service workers are a fundamental technology in the future web platform.</span></span>  <span data-ttu-id="f45d3-123">Il s’agit de scripts que le navigateur exécute en arrière-plan, séparés d’une page Web.</span><span class="sxs-lookup"><span data-stu-id="f45d3-123">They are scripts that the browser runs in the background, separate from a web page.</span></span>  <span data-ttu-id="f45d3-124">Ces scripts vous permettent d’accéder aux fonctionnalités qui n’ont pas besoin d’une interaction utilisateur ou page Web, comme les notifications de transmission, la synchronisation en arrière-plan et les expériences hors connexion.</span><span class="sxs-lookup"><span data-stu-id="f45d3-124">These scripts enable you to access features that don't need a web page or user interaction, like push notifications, background sync, and offline experiences.</span></span>  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

<span data-ttu-id="f45d3-125">Le volet **travailleurs de services** dans le panneau d' **application** est l’endroit principal de devtools pour inspecter et déboguer des travailleurs de service.</span><span class="sxs-lookup"><span data-stu-id="f45d3-125">The **Service Workers** pane in the **Application** panel is the main place in DevTools to inspect and debug service workers.</span></span>  

:::image type="complex" source="./media/service-workers-pane.msft.png" alt-text="Volet travailleurs de service" lightbox="./media/service-workers-pane.msft.png":::
   <span data-ttu-id="f45d3-127">Volet **travailleurs de service**</span><span class="sxs-lookup"><span data-stu-id="f45d3-127">The **Service Workers** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="f45d3-128">Si un ouvrier de services est installé sur la page actuellement ouverte, il apparaît dans ce volet.</span><span class="sxs-lookup"><span data-stu-id="f45d3-128">If a service worker is installed to the currently open page, then you'll see it listed on this pane.</span></span>  <span data-ttu-id="f45d3-129">Par exemple, dans l’illustration précédente, il existe un travailleur de service dont l’étendue est `https://weather-pwa-sample.firebaseapp.com` .</span><span class="sxs-lookup"><span data-stu-id="f45d3-129">For example, in the previous figure, there is a service worker installed for the scope of `https://weather-pwa-sample.firebaseapp.com`.</span></span>  
*   <span data-ttu-id="f45d3-130">La case à cocher **mode hors connexion** place le devtools en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="f45d3-130">The **Offline** checkbox puts DevTools into offline mode.</span></span>  <span data-ttu-id="f45d3-131">Cela équivaut au mode hors connexion disponible sur le panneau **réseau** ou à l' `Go offline` option dans le [menu de commandes][DevtoolsCommandMenuIndex].</span><span class="sxs-lookup"><span data-stu-id="f45d3-131">This is equivalent to the offline mode available from the **Network** panel, or the `Go offline` option in the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
*   <span data-ttu-id="f45d3-132">La case à cocher **mettre à jour lors du rechargement** force le travailleur de service à procéder à la mise à jour à chaque chargement.</span><span class="sxs-lookup"><span data-stu-id="f45d3-132">The **Update on reload** checkbox forces the service worker to update on every page load.</span></span>  
*   <span data-ttu-id="f45d3-133">La case à cocher **contournement pour le réseau** ignore le travailleur du service et force le navigateur à accéder au réseau pour les ressources demandées.</span><span class="sxs-lookup"><span data-stu-id="f45d3-133">The **Bypass for network** checkbox bypasses the service worker and forces the browser to go to the network for requested resources.</span></span>  
*   <span data-ttu-id="f45d3-134">Le bouton **mettre à jour** effectue une mise à jour ponctuelle du travailleur de services spécifié.</span><span class="sxs-lookup"><span data-stu-id="f45d3-134">The **Update** button performs a one-time update of the specified service worker.</span></span>  
*   <span data-ttu-id="f45d3-135">Le bouton de **transmission** émule une notification de transmission sans une charge utile (également appelée « **Tickle**»).</span><span class="sxs-lookup"><span data-stu-id="f45d3-135">The **Push** button emulates a push notification without a payload \(also known as a **tickle**\).</span></span>  
*   <span data-ttu-id="f45d3-136">Le bouton **synchroniser** émule un événement de synchronisation en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f45d3-136">The **Sync** button emulates a background sync event.</span></span>  
*   <span data-ttu-id="f45d3-137">Le bouton **Annuler l’inscription** annule l’enregistrement du travailleur de service indiqué.</span><span class="sxs-lookup"><span data-stu-id="f45d3-137">The **Unregister** button unregisters the specified service worker.</span></span>  <span data-ttu-id="f45d3-138">Découvrez comment annuler l' [enregistrement d’un](#clear-storage) employé de service et effacer le stockage et les caches à l’aide d’un seul clic de bouton.</span><span class="sxs-lookup"><span data-stu-id="f45d3-138">Check out [Clear storage](#clear-storage) for a way to unregister a service worker and wipe storage and caches with a single button click.</span></span>  
*   <span data-ttu-id="f45d3-139">La ligne **source** vous indique lorsque le travailleur de service en cours d’exécution a été installé.</span><span class="sxs-lookup"><span data-stu-id="f45d3-139">The **Source** line tells you when the currently running service worker was installed.</span></span>  <span data-ttu-id="f45d3-140">Le lien est le nom du fichier source du travailleur du service.</span><span class="sxs-lookup"><span data-stu-id="f45d3-140">The link is the name of the service worker's source file.</span></span>  <span data-ttu-id="f45d3-141">Cliquer sur le lien vous envoie à la source du travailleur du service.</span><span class="sxs-lookup"><span data-stu-id="f45d3-141">Clicking on the link sends you to the service worker's source.</span></span>  
*   <span data-ttu-id="f45d3-142">La ligne de **statut** indique le statut du travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="f45d3-142">The **Status** line tells you the status of the service worker.</span></span>  <span data-ttu-id="f45d3-143">Le numéro d’identification en regard du voyant de statut vert ( `#36` dans la figure précédente \) est destiné au travailleur de service actuellement actif.</span><span class="sxs-lookup"><span data-stu-id="f45d3-143">The ID number next to the green status indicator \(`#36` in previous figure\) is for the currently active Service Worker.</span></span>  <span data-ttu-id="f45d3-144">En regard du statut, vous verrez un bouton **Démarrer** (si le travailleur a arrêté le service \) ou un bouton d' **arrêt** (si le travailleur du service exécute \).</span><span class="sxs-lookup"><span data-stu-id="f45d3-144">Next to the status you'll see a **start** button \(if the service worker is stopped\) or a **stop** button \(if the service worker is running\).</span></span>  <span data-ttu-id="f45d3-145">Les travailleurs de service sont conçus pour s’arrêter et démarrer par le navigateur à tout moment.</span><span class="sxs-lookup"><span data-stu-id="f45d3-145">Service workers are designed to be stopped and started by the browser at any time.</span></span>  <span data-ttu-id="f45d3-146">L’arrêt explicite de votre travailleur de service à l’aide du bouton **Stop** peut simuler.</span><span class="sxs-lookup"><span data-stu-id="f45d3-146">Explicitly stopping your service worker using the **stop** button can simulate that.</span></span>  <span data-ttu-id="f45d3-147">L’arrêt de votre travailleur est un excellent moyen de tester le comportement de votre code lors du redémarrage du travailleur du service.</span><span class="sxs-lookup"><span data-stu-id="f45d3-147">Stopping your service worker is a great way to test how your code behaves when the service worker starts back up again.</span></span>  <span data-ttu-id="f45d3-148">Il révèle fréquemment les bogues causés par des hypothèses incorrectes sur l’état global persistant.</span><span class="sxs-lookup"><span data-stu-id="f45d3-148">It frequently reveals bugs due to faulty assumptions about persistent global state.</span></span>  
*   <span data-ttu-id="f45d3-149">La ligne **clients** indique l’origine à laquelle le travailleur de service est limité.</span><span class="sxs-lookup"><span data-stu-id="f45d3-149">The **Clients** line tells you the origin that the service worker is scoped to.</span></span>  <span data-ttu-id="f45d3-150">Le bouton **focus** est principalement utile lorsque vous avez activé la case à cocher **Afficher tout** .</span><span class="sxs-lookup"><span data-stu-id="f45d3-150">The **focus** button is mostly useful when you've enabled the **show all** checkbox.</span></span>  <span data-ttu-id="f45d3-151">Lorsque cette case est cochée, tous les travailleurs de service inscrits apparaissent.</span><span class="sxs-lookup"><span data-stu-id="f45d3-151">When that checkbox is enabled, all registered service workers are listed.</span></span>  <span data-ttu-id="f45d3-152">Si vous cliquez sur le bouton **focus** en regard d’un ouvrier de services en cours d’exécution dans un autre onglet, Microsoft Edge est axé sur cet onglet.</span><span class="sxs-lookup"><span data-stu-id="f45d3-152">If you click on the **focus** button next to a service worker that is running in a different tab, Microsoft Edge focuses on that tab.</span></span>  
    
<span data-ttu-id="f45d3-153">Si le travailleur du service génère des erreurs, une nouvelle étiquette appelée **Erreurs** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f45d3-153">If the service worker causes any errors, a new label called **Errors** shows up.</span></span>  

<!--  
:::image type="complex" source="./media/sw-error.msft.png" alt-text="Service worker with errors" lightbox="./media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## <span data-ttu-id="f45d3-154">Caches du travailleur de service</span><span class="sxs-lookup"><span data-stu-id="f45d3-154">Service worker caches</span></span> 

<span data-ttu-id="f45d3-155">Le volet **stockage du cache** fournit une liste en lecture seule de ressources qui ont été mises en cache à l’aide de l' [API de cache][MDNWebCacheAPI]\ (Service Worker \).</span><span class="sxs-lookup"><span data-stu-id="f45d3-155">The **Cache Storage** pane provides a read-only list of resources that have been cached using the \(service worker\) [Cache API][MDNWebCacheAPI].</span></span>  

:::image type="complex" source="./media/cache-pane-cache-storage-resources.msft.png" alt-text="Volet stockage du cache" lightbox="./media/cache-pane-cache-storage-resources.msft.png":::
   <span data-ttu-id="f45d3-157">Volet **stockage du cache**</span><span class="sxs-lookup"><span data-stu-id="f45d3-157">The **Cache Storage** Pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="f45d3-158">La première fois que vous ouvrez un cache et y ajoutez une ressource, il est possible que DevTools ne détecte pas la modification.</span><span class="sxs-lookup"><span data-stu-id="f45d3-158">The first time you open a cache and add a resource to it, DevTools might not detect the change.</span></span>  <span data-ttu-id="f45d3-159">Rechargez la page et vous devriez voir le cache.</span><span class="sxs-lookup"><span data-stu-id="f45d3-159">Reload the page and you should see the cache.</span></span>  

<span data-ttu-id="f45d3-160">Si vous avez deux mises en cache ouvertes, celles-ci s’affichent sous la liste déroulante **stockage du cache** .</span><span class="sxs-lookup"><span data-stu-id="f45d3-160">If you have two or more caches open, you'll see them listed below the **Cache Storage** dropdown.</span></span>  

:::image type="complex" source="./media/cache-pane-cache-storage.msft.png" alt-text="Liste déroulante stockage du cache" lightbox="./media/cache-pane-cache-storage.msft.png":::
   <span data-ttu-id="f45d3-162">Liste déroulante **stockage du cache**</span><span class="sxs-lookup"><span data-stu-id="f45d3-162">The **Cache Storage** dropdown</span></span>  
:::image-end:::  

## <span data-ttu-id="f45d3-163">Utilisation du quota</span><span class="sxs-lookup"><span data-stu-id="f45d3-163">Quota usage</span></span> 

<span data-ttu-id="f45d3-164">Certaines réponses dans le volet **stockage du cache** sont signalées comme «opaques».</span><span class="sxs-lookup"><span data-stu-id="f45d3-164">Some responses within the **Cache Storage** pane may be flagged as being "opaque".</span></span>  <span data-ttu-id="f45d3-165">Fait référence à une réponse Récupérée à partir d’une autre origine, par exemple à partir d’une API de **réseau de distribution de contenu ou d'** une API distante, lorsque [cors][FetchHttpCorsProtocol] n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="f45d3-165">This refers to a response retrieved from a different origin, like from a **CDN** or remote API, when [CORS][FetchHttpCorsProtocol] is not enabled.</span></span>  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

<span data-ttu-id="f45d3-166">Afin d’éviter toute fuite d’information entre domaines, un remplissage important est ajouté à la taille d’une réponse opaque utilisée pour calculer les limites de quota de stockage (par exemple, si une `QuotaExceeded` exception est levée \) et signalée par l' `navigator.storage` API.</span><span class="sxs-lookup"><span data-stu-id="f45d3-166">In order to avoid leakage of cross-domain information, there's significant padding added to the size of an opaque response used for calculating storage quota limits \(for example whether a `QuotaExceeded` exception is thrown\) and reported by the `navigator.storage` API.</span></span>  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

<span data-ttu-id="f45d3-167">Les détails de ces remplissages varient d’un navigateur à l’autre, mais pour Microsoft Edge, cela signifie que la **taille minimale** d’une seule réponse opaque mise en cache est d' [environ 7 Mo][ChromiumIssues796060#c17].</span><span class="sxs-lookup"><span data-stu-id="f45d3-167">The details of this padding vary from browser to browser, but for Microsoft Edge, this means that the **minimum size** that any single cached opaque response contributes to the overall storage usage is [approximately 7 megabytes][ChromiumIssues796060#c17].</span></span>  <span data-ttu-id="f45d3-168">N’oubliez pas de savoir ce que vous devez faire lorsque vous déterminez le nombre de réponses opaques que vous souhaitez mettre en cache, dans la mesure où vous risquez de dépasser facilement les limitations de quota de stockage de manière plus rapide que si vous vous attendiez en fonction de la taille réelle des ressources opaques.</span><span class="sxs-lookup"><span data-stu-id="f45d3-168">You should keep this in mind when determining how many opaque responses you want to cache, since you could easily exceeded storage quota limitations much sooner than you'd otherwise expect based on the actual size of the opaque resources.</span></span>  

<span data-ttu-id="f45d3-169">Guides connexes:</span><span class="sxs-lookup"><span data-stu-id="f45d3-169">Related Guides:</span></span>  

*   [<span data-ttu-id="f45d3-170">Débordement de pile: quelles limitations s’appliquent aux réponses opaques?</span><span class="sxs-lookup"><span data-stu-id="f45d3-170">Stack Overflow: What limitations apply to opaque responses?</span></span>][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## <span data-ttu-id="f45d3-171">Effacement du stockage</span><span class="sxs-lookup"><span data-stu-id="f45d3-171">Clear storage</span></span> 

<span data-ttu-id="f45d3-172">Le volet **Vider le stockage** est une fonctionnalité très utile lorsque vous développez des applications Web progressives.</span><span class="sxs-lookup"><span data-stu-id="f45d3-172">The **Clear Storage** pane is a very useful feature when developing progressive web apps.</span></span>  <span data-ttu-id="f45d3-173">Ce volet vous permet d’annuler l’enregistrement des travailleurs de services et d’effacer tous les caches et stockage avec un seul clic de bouton.</span><span class="sxs-lookup"><span data-stu-id="f45d3-173">This pane lets you unregister service workers and clear all caches and storage with a single button click.</span></span>  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides 

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
<!--TODO  -->

<!--  
 


-->  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ./command-menu/index.md "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Problème de chrome 796060: une valeur de stockage de cache augmente chaque actualisation lorsque le code d’analyse est dans le code html"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Cache-API Web | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Débordement de pile: quelles limitations s’appliquent aux réponses opaques?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> <span data-ttu-id="f45d3-178">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f45d3-178">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f45d3-179">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="f45d3-179">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="f45d3-181">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f45d3-181">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
