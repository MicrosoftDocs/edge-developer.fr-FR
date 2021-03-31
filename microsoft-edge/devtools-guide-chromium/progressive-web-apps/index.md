---
description: Utilisez le panneau Application pour inspecter, modifier et déboguer les manifestes d’application web, les travailleurs de service et les caches de travail de service.
title: Débogage d’applications web progressives
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: aea01d25474a030e78ac0eaeaef3954ab7f4539f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398538"
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

# <a name="debug-progressive-web-apps"></a><span data-ttu-id="e2021-104">Débogage d’applications web progressives</span><span class="sxs-lookup"><span data-stu-id="e2021-104">Debug Progressive Web Apps</span></span>  

<span data-ttu-id="e2021-105">Utilisez le panneau **Application** pour inspecter, modifier et déboguer les manifestes d’application web, les travailleurs de service et les caches de travail de service.</span><span class="sxs-lookup"><span data-stu-id="e2021-105">Use the **Application** panel to inspect, modify, and debug web app manifests, service workers, and service worker caches.</span></span>  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

<span data-ttu-id="e2021-106">Ce guide traite uniquement des fonctionnalités Progressive Web App du panneau **Application.**</span><span class="sxs-lookup"><span data-stu-id="e2021-106">This guide only discusses the Progressive Web App features of the **Application** panel.</span></span>  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### <a name="summary"></a><span data-ttu-id="e2021-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="e2021-107">Summary</span></span>  

*   <span data-ttu-id="e2021-108">Utilisez le **volet Manifeste** pour inspecter le manifeste de votre application web et déclencher des événements Ajouter à l’écran d’accueil.</span><span class="sxs-lookup"><span data-stu-id="e2021-108">Use the **Manifest** pane to inspect your web app manifest and trigger Add to Homescreen events.</span></span>  
*   <span data-ttu-id="e2021-109">Utilisez  le volet Travailleurs du service pour toute une gamme de tâches liées au travail de service, telles que la désinssion ou la mise à jour d’un service, l’émulation d’événements Push, la mise hors connexion ou l’arrêt d’un service de travail.</span><span class="sxs-lookup"><span data-stu-id="e2021-109">Use the **Service Workers** pane for a whole range of service-worker-related tasks, like unregistering or updating a service, emulating push events, going offline, or stopping a service worker.</span></span>  
*   <span data-ttu-id="e2021-110">Affichez votre cache de travail de service à partir du **volet Stockage** du cache.</span><span class="sxs-lookup"><span data-stu-id="e2021-110">View your service worker cache from the **Cache Storage** pane.</span></span>  
*   <span data-ttu-id="e2021-111">Désinsistez un service de travail et désinsérez tout le stockage et les caches à l’aide d’un seul bouton dans le volet Effacer **le** stockage.</span><span class="sxs-lookup"><span data-stu-id="e2021-111">Unregister a service worker and clear all storage and caches with a single button choose from the **Clear storage** pane.</span></span>  
    
## <a name="web-app-manifest"></a><span data-ttu-id="e2021-112">Manifeste d’application web</span><span class="sxs-lookup"><span data-stu-id="e2021-112">Web app manifest</span></span>  

<span data-ttu-id="e2021-113">Si vous souhaitez que vos utilisateurs puissent ajouter votre application à leurs écrans d’accueil mobiles, vous avez besoin d’un manifeste d’application web.</span><span class="sxs-lookup"><span data-stu-id="e2021-113">If you want your users to be able to add your app to their mobile homescreens, you need a web app manifest.</span></span>  <span data-ttu-id="e2021-114">Le manifeste définit l’apparence de l’application sur l’écran d’accueil, l’endroit où diriger l’utilisateur lors du lancement à partir de l’écran d’accueil et l’apparence de l’application au lancement.</span><span class="sxs-lookup"><span data-stu-id="e2021-114">The manifest defines how the app appears on the homescreen, where to direct the user when launching from homescreen, and what the app looks like on launch.</span></span>  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

<span data-ttu-id="e2021-115">Une fois votre manifeste installé, vous  pouvez utiliser le volet Manifeste du panneau **Application** pour l’inspecter.</span><span class="sxs-lookup"><span data-stu-id="e2021-115">After you have your manifest set up, you may use the **Manifest** pane of the **Application** panel to inspect it.</span></span>  

:::image type="complex" source="../media/manifest-pane.msft.png" alt-text="Volet manifeste" lightbox="../media/manifest-pane.msft.png":::
   <span data-ttu-id="e2021-117">Volet  manifeste</span><span class="sxs-lookup"><span data-stu-id="e2021-117">The **Manifest** Pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="e2021-118">Pour examiner la source du manifeste, choisissez le lien sous l’étiquette **de manifeste** d’application \( `https://airhorner.com/manifest.json` dans la figure précédente\).</span><span class="sxs-lookup"><span data-stu-id="e2021-118">To look at the manifest source, choose the link below **App Manifest** label \(`https://airhorner.com/manifest.json` in the previous figure\).</span></span>  
<!-- *   Choose the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   <span data-ttu-id="e2021-119">Les **sections** **Identité** et Présentation affichent simplement les champs de la source de manifeste dans un affichage plus convivial.</span><span class="sxs-lookup"><span data-stu-id="e2021-119">The **Identity** and **Presentation** sections just display fields from the manifest source in a more user-friendly display.</span></span>  
*   <span data-ttu-id="e2021-120">La section **Icônes** affiche chaque icône que vous avez spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e2021-120">The **Icons** section displays every icon that you've specified.</span></span>  
    
<!--### Simulate Add to Homescreen events  -->

<!--A web app may only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, the criteria is potentially inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You may test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Choosing on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="../media/io.msft.png" alt-text="Add to desktop shelf" lightbox="../media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature may not yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you may successfully add your app to your desktop shelf, then it works for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you may connect a real mobile device to DevTools via **remote debugging**, and then choose the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## <a name="service-workers"></a><span data-ttu-id="e2021-121">Travailleurs du service</span><span class="sxs-lookup"><span data-stu-id="e2021-121">Service workers</span></span>  

<span data-ttu-id="e2021-122">Les travailleurs de service sont une technologie fondamentale dans la future plateforme web.</span><span class="sxs-lookup"><span data-stu-id="e2021-122">Service workers are a fundamental technology in the future web platform.</span></span>  <span data-ttu-id="e2021-123">Il s’agit de scripts que le navigateur exécute en arrière-plan, séparés d’une page web.</span><span class="sxs-lookup"><span data-stu-id="e2021-123">They are scripts that the browser runs in the background, separate from a web page.</span></span>  <span data-ttu-id="e2021-124">Les scripts vous permettent d’accéder à des fonctionnalités qui n’ont pas besoin d’une page web ou d’une interaction utilisateur, telles que les notifications Push, la synchronisation en arrière-plan et les expériences hors connexion.</span><span class="sxs-lookup"><span data-stu-id="e2021-124">The scripts allow you to access features that without the need of a web page or user interaction, like push notifications, background sync, and offline experiences.</span></span>  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

<span data-ttu-id="e2021-125">Le **volet Travailleurs** du service dans le panneau **Application** est l’endroit principal dans DevTools pour inspecter et déboguer les travailleurs du service.</span><span class="sxs-lookup"><span data-stu-id="e2021-125">The **Service Workers** pane in the **Application** panel is the main place in DevTools to inspect and debug service workers.</span></span>  

:::image type="complex" source="../media/service-workers-pane.msft.png" alt-text="Volet Travailleurs du service" lightbox="../media/service-workers-pane.msft.png":::
   <span data-ttu-id="e2021-127">Volet **Travailleurs** du service</span><span class="sxs-lookup"><span data-stu-id="e2021-127">The **Service Workers** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="e2021-128">Si un service de travail est installé sur la page actuellement ouverte, il est répertorié dans ce volet.</span><span class="sxs-lookup"><span data-stu-id="e2021-128">If a service worker is installed to the currently open page, then it is listed on this pane.</span></span>  <span data-ttu-id="e2021-129">Par exemple, dans la figure précédente, un service de travail est installé pour l’étendue de `https://weather-pwa-sample.firebaseapp.com` .</span><span class="sxs-lookup"><span data-stu-id="e2021-129">For example, in the previous figure, there is a service worker installed for the scope of `https://weather-pwa-sample.firebaseapp.com`.</span></span>  
*   <span data-ttu-id="e2021-130">La **case à** cocher Hors connexion place DevTools en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="e2021-130">The **Offline** checkbox puts DevTools into offline mode.</span></span>  <span data-ttu-id="e2021-131">Cela équivaut au mode hors connexion disponible à partir de l’outil **Réseau** ou à l’option `Go offline` du menu [Commande.][DevtoolsCommandMenuIndex]</span><span class="sxs-lookup"><span data-stu-id="e2021-131">This is equivalent to the offline mode available from the **Network** tool, or the `Go offline` option in the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
*   <span data-ttu-id="e2021-132">La case à cocher Mise à **jour lors du rechargement** force le service de travail à mettre à jour chaque chargement de page.</span><span class="sxs-lookup"><span data-stu-id="e2021-132">The **Update on reload** checkbox forces the service worker to update on every page load.</span></span>  
*   <span data-ttu-id="e2021-133">La **case à cocher** Contournement du réseau contourne le service de travail et force le navigateur à se rendre sur le réseau pour les ressources demandées.</span><span class="sxs-lookup"><span data-stu-id="e2021-133">The **Bypass for network** checkbox bypasses the service worker and forces the browser to go to the network for requested resources.</span></span>  
*   <span data-ttu-id="e2021-134">Le **bouton** Mettre à jour effectue une mise à jour à une seule fois du service de travail spécifié.</span><span class="sxs-lookup"><span data-stu-id="e2021-134">The **Update** button performs a one-time update of the specified service worker.</span></span>  
*   <span data-ttu-id="e2021-135">Le **bouton Push** émule une notification Push sans charge utile \(également appelée une coche \). </span><span class="sxs-lookup"><span data-stu-id="e2021-135">The **Push** button emulates a push notification without a payload \(also known as a **tickle**\).</span></span>  
*   <span data-ttu-id="e2021-136">Le **bouton Synchroniser** émule un événement de synchronisation en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="e2021-136">The **Sync** button emulates a background sync event.</span></span>  
*   <span data-ttu-id="e2021-137">Le **bouton Désinsserrement** désinsère le service de travail spécifié.</span><span class="sxs-lookup"><span data-stu-id="e2021-137">The **Unregister** button unregisters the specified service worker.</span></span>  <span data-ttu-id="e2021-138">Consultez [Effacer le stockage](#clear-storage) pour supprimer l’enregistrement d’un service de travail et effacer le stockage et les caches avec un seul bouton.</span><span class="sxs-lookup"><span data-stu-id="e2021-138">Check out [Clear storage](#clear-storage) for a way to unregister a service worker and wipe storage and caches with a single button choose.</span></span>  
*   <span data-ttu-id="e2021-139">La **ligne Source** vous indique quand le service de travail en cours d’exécution a été installé.</span><span class="sxs-lookup"><span data-stu-id="e2021-139">The **Source** line tells you when the currently running service worker was installed.</span></span>  <span data-ttu-id="e2021-140">Le lien est le nom du fichier source du service de travail.</span><span class="sxs-lookup"><span data-stu-id="e2021-140">The link is the name of the source file of the service worker.</span></span>  <span data-ttu-id="e2021-141">Le choix du lien vous envoie à la source du service de travail.</span><span class="sxs-lookup"><span data-stu-id="e2021-141">Choosing on the link sends you to the source of the service worker.</span></span>  
*   <span data-ttu-id="e2021-142">La **ligne État** vous indique l’état du service de travail.</span><span class="sxs-lookup"><span data-stu-id="e2021-142">The **Status** line tells you the status of the service worker.</span></span>  <span data-ttu-id="e2021-143">Le numéro d’ID à côté de l’indicateur d’état vert \( dans la figure précédente\) est pour le service de travail `#36` actif.</span><span class="sxs-lookup"><span data-stu-id="e2021-143">The ID number next to the green status indicator \(`#36` in previous figure\) is for the currently active Service Worker.</span></span>  <span data-ttu-id="e2021-144">En plus de  l’état, un bouton de démarrage \(si le service de travail est arrêté\) ou un bouton d’arrêt \(si le service de travail est en cours d’exécution\) s’affiche. </span><span class="sxs-lookup"><span data-stu-id="e2021-144">Next to the status, a **start** button \(if the service worker is stopped\) or a **stop** button \(if the service worker is running\) is displayed.</span></span>  <span data-ttu-id="e2021-145">Les employés de service sont conçus pour être arrêtés et démarrés par le navigateur à tout moment.</span><span class="sxs-lookup"><span data-stu-id="e2021-145">Service workers are designed to be stopped and started by the browser at any time.</span></span>  <span data-ttu-id="e2021-146">L’arrêt explicite de votre service à l’aide du **bouton** d’arrêt peut simuler cela.</span><span class="sxs-lookup"><span data-stu-id="e2021-146">Explicitly stopping your service worker using the **stop** button may simulate that.</span></span>  <span data-ttu-id="e2021-147">L’arrêt de votre service de travail est un excellent moyen de tester le comportement de votre code lorsque le service de travail recommence à le faire.</span><span class="sxs-lookup"><span data-stu-id="e2021-147">Stopping your service worker is a great way to test how your code behaves when the service worker starts back up again.</span></span>  <span data-ttu-id="e2021-148">Il révèle fréquemment des bogues en raison d’hypothèses erronées sur l’état global persistant.</span><span class="sxs-lookup"><span data-stu-id="e2021-148">It frequently reveals bugs due to faulty assumptions about persistent global state.</span></span>  
*   <span data-ttu-id="e2021-149">La **ligne Clients** vous indique l’origine de l’étendue du service de travail.</span><span class="sxs-lookup"><span data-stu-id="e2021-149">The **Clients** line tells you the origin that the service worker is scoped to.</span></span>  <span data-ttu-id="e2021-150">Le **bouton Focus** est principalement utile lorsque vous avez activé la case à cocher Afficher **tout.**</span><span class="sxs-lookup"><span data-stu-id="e2021-150">The **focus** button is mostly useful when you've enabled the **show all** checkbox.</span></span>  <span data-ttu-id="e2021-151">Lorsque cette case à cocher est activée, tous les employés de service inscrits sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="e2021-151">When that checkbox is enabled, all registered service workers are listed.</span></span>  <span data-ttu-id="e2021-152">Si vous choisissez sur le **bouton focus** en face d’un service de travail qui s’exécute sous un autre onglet, Microsoft Edge se concentre sur cet onglet.</span><span class="sxs-lookup"><span data-stu-id="e2021-152">If you choose on the **focus** button next to a service worker that is running in a different tab, Microsoft Edge focuses on that tab.</span></span>  
    
<span data-ttu-id="e2021-153">Si le service de travail provoque des erreurs, une nouvelle étiquette appelée **Erreurs** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e2021-153">If the service worker causes any errors, a new label called **Errors** shows up.</span></span>  

<!--  
:::image type="complex" source="../media/sw-error.msft.png" alt-text="Service worker with errors" lightbox="../media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## <a name="service-worker-caches"></a><span data-ttu-id="e2021-154">Caches de travail de service</span><span class="sxs-lookup"><span data-stu-id="e2021-154">Service worker caches</span></span>  

<span data-ttu-id="e2021-155">Le **volet Stockage** du cache fournit une liste en lecture seule des ressources qui ont été mises en cache à l’aide de l’API de [cache][MDNWebCacheAPI]\(service worker\).</span><span class="sxs-lookup"><span data-stu-id="e2021-155">The **Cache Storage** pane provides a read-only list of resources that have been cached using the \(service worker\) [Cache API][MDNWebCacheAPI].</span></span>  

:::image type="complex" source="../media/cache-pane-cache-storage-resources.msft.png" alt-text="Volet de stockage du cache" lightbox="../media/cache-pane-cache-storage-resources.msft.png":::
   <span data-ttu-id="e2021-157">Volet **de stockage du** cache</span><span class="sxs-lookup"><span data-stu-id="e2021-157">The **Cache Storage** Pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="e2021-158">La première fois que vous ouvrez un cache et y ajoutez une ressource, DevTools risque de ne pas détecter la modification.</span><span class="sxs-lookup"><span data-stu-id="e2021-158">The first time you open a cache and add a resource to it, DevTools may not detect the change.</span></span>  <span data-ttu-id="e2021-159">Actualisez la page et affichez le cache.</span><span class="sxs-lookup"><span data-stu-id="e2021-159">Refresh the page and to display the cache.</span></span>  

<span data-ttu-id="e2021-160">Si vous avez au moins deux caches ouverts, les caches s’affichent sous la **liste** de stockage de cache suivante.</span><span class="sxs-lookup"><span data-stu-id="e2021-160">If you have two or more caches open, the caches display under the following **Cache Storage** dropdown.</span></span>  

:::image type="complex" source="../media/cache-pane-cache-storage.msft.png" alt-text="La zone de dépôt Stockage du cache" lightbox="../media/cache-pane-cache-storage.msft.png":::
   <span data-ttu-id="e2021-162">La zone **de dépôt Stockage** du cache</span><span class="sxs-lookup"><span data-stu-id="e2021-162">The **Cache Storage** dropdown</span></span>  
:::image-end:::  

## <a name="quota-usage"></a><span data-ttu-id="e2021-163">Utilisation des quotas</span><span class="sxs-lookup"><span data-stu-id="e2021-163">Quota usage</span></span>  

<span data-ttu-id="e2021-164">Certaines réponses dans le **volet Stockage** du cache peuvent être marquées comme étant « opaques ».</span><span class="sxs-lookup"><span data-stu-id="e2021-164">Some responses within the **Cache Storage** pane may be flagged as being "opaque".</span></span>  <span data-ttu-id="e2021-165">Cela fait référence à une réponse extraite d’une origine différente, comme à partir d’un **CDN** ou d’une API distante, lorsque [CORS][FetchHttpCorsProtocol] n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="e2021-165">This refers to a response retrieved from a different origin, like from a **CDN** or remote API, when [CORS][FetchHttpCorsProtocol] is not enabled.</span></span>  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

<span data-ttu-id="e2021-166">Afin d’éviter les fuites d’informations entre domaines, un remplissage important est ajouté à la taille d’une réponse opaque utilisée pour calculer les limites de quota de stockage \(par exemple, si une exception est déclarée\) et signalée par `QuotaExceeded` `navigator.storage` l’API.</span><span class="sxs-lookup"><span data-stu-id="e2021-166">In order to avoid leakage of cross-domain information, significant padding is added to the size of an opaque response used for calculating storage quota limits \(for example whether a `QuotaExceeded` exception is thrown\) and reported by the `navigator.storage` API.</span></span>  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

<span data-ttu-id="e2021-167">Les détails de ce remplissage varient d’un navigateur à l’autre, mais pour Microsoft Edge, cela signifie que la taille **minimale** de toute réponse opaque mise en cache contribue à l’utilisation globale du stockage est d’environ [7 mégaoctets][ChromiumIssues796060#c17].</span><span class="sxs-lookup"><span data-stu-id="e2021-167">The details of this padding vary from browser to browser, but for Microsoft Edge, this means that the **minimum size** that any single cached opaque response contributes to the overall storage usage is [approximately 7 megabytes][ChromiumIssues796060#c17].</span></span>  <span data-ttu-id="e2021-168">N’oubliez pas le remplissage lors de la détermination du nombre de réponses opaques que vous souhaitez mettre en cache, car vous pouvez facilement dépasser les limites de quota de stockage beaucoup plus tôt que prévu en fonction de la taille réelle des ressources opaques.</span><span class="sxs-lookup"><span data-stu-id="e2021-168">Remember the padding when determining how many opaque responses you want to cache, since you may easily exceed storage quota limitations much sooner than you otherwise expect based on the actual size of the opaque resources.</span></span>  

<span data-ttu-id="e2021-169">Guides connexes :</span><span class="sxs-lookup"><span data-stu-id="e2021-169">Related Guides:</span></span>  

*   [<span data-ttu-id="e2021-170">Stack Overflow : quelles limitations s’appliquent aux réponses opaques ?</span><span class="sxs-lookup"><span data-stu-id="e2021-170">Stack Overflow: What limitations apply to opaque responses?</span></span>][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## <a name="clear-storage"></a><span data-ttu-id="e2021-171">Effacer le stockage</span><span class="sxs-lookup"><span data-stu-id="e2021-171">Clear storage</span></span>  

<span data-ttu-id="e2021-172">Le **volet Effacer le** stockage est une fonctionnalité très utile lors du développement d’applications web progressives.</span><span class="sxs-lookup"><span data-stu-id="e2021-172">The **Clear Storage** pane is a very useful feature when developing progressive web apps.</span></span>  <span data-ttu-id="e2021-173">Ce volet vous permet de désinsser les travailleurs du service et d’effacer tous les caches et tous les espaces de stockage en un seul bouton.</span><span class="sxs-lookup"><span data-stu-id="e2021-173">This pane lets you unregister service workers and clear all caches and storage with a single button choose.</span></span>  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides   

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="e2021-174">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="e2021-174">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Exécuter des commandes avec le menu de commandes Microsoft Edge DevTools | Documents Microsoft"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Chromium Issue 796060: Cache Storage value rises on each refresh when Analytics code is in the html"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Cache : api web | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Stack Overflow : quelles limitations s’appliquent aux réponses opaques ?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> <span data-ttu-id="e2021-179">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e2021-179">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e2021-180">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="e2021-180">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="e2021-182">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e2021-182">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
