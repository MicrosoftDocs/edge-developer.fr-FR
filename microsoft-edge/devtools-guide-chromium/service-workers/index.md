---
description: Tout sur les améliorations apportées aux services de travail et sur l’utilisation de chacune d’elles.
title: Améliorations apportées aux services de travail
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools, service worker, PWA
ms.openlocfilehash: c00b7c7fd18d4bb3d413369ec1464c0cb0255311
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597142"
---
# <a name="service-worker-improvements"></a><span data-ttu-id="08acd-104">Améliorations apportées aux services de travail</span><span class="sxs-lookup"><span data-stu-id="08acd-104">Service Worker improvements</span></span>  

<span data-ttu-id="08acd-105">Cet article vous explique les améliorations apportées aux outils de développement pour travailler avec les travailleurs du [service][MdnServiceWorkerApi] et les demandes réseau qui passent par chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="08acd-105">This article teaches you about improvements to developer tools for working with [service workers][MdnServiceWorkerApi] and the network requests that pass through each one.</span></span>  <span data-ttu-id="08acd-106">Les améliorations **apportées aux services de travail se** font dans les outils **Réseau,** **Application**et **Sources.**</span><span class="sxs-lookup"><span data-stu-id="08acd-106">The **service worker improvements** are in the **Network**, **Application**, and **Sources** tools.</span></span>  <span data-ttu-id="08acd-107">Les améliorations simplifient les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="08acd-107">The improvements simplify the following tasks.</span></span>  

*   <span data-ttu-id="08acd-108">Déboguer en fonction des chronologies du service de travail.</span><span class="sxs-lookup"><span data-stu-id="08acd-108">Debug based on Service Worker timelines.</span></span>  
    *   <span data-ttu-id="08acd-109">Le début d’une demande et la durée du démarrage.</span><span class="sxs-lookup"><span data-stu-id="08acd-109">The start of a request and duration of the bootstrap.</span></span>  
    *   <span data-ttu-id="08acd-110">Mise à jour de l’inscription du service de travail.</span><span class="sxs-lookup"><span data-stu-id="08acd-110">Update to Service worker registration.</span></span>  
    *   <span data-ttu-id="08acd-111">Runtime d’une demande à l’aide du [handler d’événements fetch.][MdnFetchEvent]</span><span class="sxs-lookup"><span data-stu-id="08acd-111">The runtime of a request using the [fetch event][MdnFetchEvent] handler.</span></span>  
    *   <span data-ttu-id="08acd-112">Runtime de tous les événements de récupération pour le chargement d’un client.</span><span class="sxs-lookup"><span data-stu-id="08acd-112">The runtime of all fetch events for loading a client.</span></span>  
*   <span data-ttu-id="08acd-113">Explorez les détails d’utilisation des handlers d’événements d’extraction, installez les handlers d’événements et activez les handlers d’événements.</span><span class="sxs-lookup"><span data-stu-id="08acd-113">Explore the runtime details of fetch event handlers, install event handlers, and activate event handlers.</span></span>  
*   <span data-ttu-id="08acd-114">Entrez et sortz du handler d’événements de récupération avec les [informations de script de page.](#sources)</span><span class="sxs-lookup"><span data-stu-id="08acd-114">Step into and out of fetch event handler with [page script information](#sources).</span></span>  
    
<span data-ttu-id="08acd-115">Les expériences s’étendent sur trois outils de développement différents.</span><span class="sxs-lookup"><span data-stu-id="08acd-115">The experiences span three different developer tools.</span></span>  

1.  <span data-ttu-id="08acd-116">Outil [Réseau.](#network)</span><span class="sxs-lookup"><span data-stu-id="08acd-116">The [Network](#network) tool.</span></span>  <span data-ttu-id="08acd-117">Choisissez une demande réseau qui s’exécute par le biais d’un service de travail et accédez à la chronologie correspondante du travail de service dans **l’outil de minutage.**</span><span class="sxs-lookup"><span data-stu-id="08acd-117">Choose a network request that runs through a service worker and access the corresponding timeline of the service worker in the **Timing** tool.</span></span>  
1.  <span data-ttu-id="08acd-118">Outil [Application.](#application)</span><span class="sxs-lookup"><span data-stu-id="08acd-118">The [Application](#application) tool.</span></span>  <span data-ttu-id="08acd-119">Pour déboguer les travailleurs du service, accédez à l’outil **Travailleurs de** service.</span><span class="sxs-lookup"><span data-stu-id="08acd-119">To debug the service workers, navigate to the **Service Workers** tool.</span></span>  
1.  <span data-ttu-id="08acd-120">Outil [Sources.](#sources)</span><span class="sxs-lookup"><span data-stu-id="08acd-120">The [Sources](#sources) tool.</span></span>  <span data-ttu-id="08acd-121">Accéder aux informations de script de page lors de l’accès aux handlers d’événements de récupération.</span><span class="sxs-lookup"><span data-stu-id="08acd-121">Access page script information when stepping into fetch event handlers.</span></span>  
    
## <a name="network"></a><span data-ttu-id="08acd-122">Network</span><span class="sxs-lookup"><span data-stu-id="08acd-122">Network</span></span>  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Chronologie du travail de service dans l’outil Réseau" lightbox="../media/sw-network-timeline.msft.png":::
   <span data-ttu-id="08acd-124">Affichage réseau</span><span class="sxs-lookup"><span data-stu-id="08acd-124">Network view</span></span>  
:::image-end:::  

<span data-ttu-id="08acd-125">Pour accéder aux fonctionnalités de débogage du service de travail dans l’outil **Réseau,** effectuer l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="08acd-125">To access the service worker debugging features in the **Network** tool, complete one of the following actions.</span></span>  

*   <span data-ttu-id="08acd-126">Accédez directement à **l’outil** Réseau.</span><span class="sxs-lookup"><span data-stu-id="08acd-126">Access directly in the **Network** tool.</span></span>  
*   <span data-ttu-id="08acd-127">Démarré dans **l’outil Application.**</span><span class="sxs-lookup"><span data-stu-id="08acd-127">Started in the **Application** tool.</span></span>  
    
### <a name="request-routing"></a><span data-ttu-id="08acd-128">Routage des demandes</span><span class="sxs-lookup"><span data-stu-id="08acd-128">Request routing</span></span>  

<span data-ttu-id="08acd-129">Pour faciliter la visualisation du routage des demandes, les chronologies affichent désormais la start-up du service de travail et les événements `respondWith` de récupération.</span><span class="sxs-lookup"><span data-stu-id="08acd-129">To make request routing easier to visualize, timelines now display the service worker start-up and the `respondWith` fetch events.</span></span>  <span data-ttu-id="08acd-130">Pour déboguer et visualiser une demande réseau qui passe par un service de travail, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="08acd-130">To debug and visualize a network request that passed through a service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="08acd-131">Choisissez la demande réseau qui a été passée par un service de travail.</span><span class="sxs-lookup"><span data-stu-id="08acd-131">Choose the network request that went through a service worker.</span></span>  
1.  <span data-ttu-id="08acd-132">Ouvrez **l’outil** De minutage.</span><span class="sxs-lookup"><span data-stu-id="08acd-132">Open the **Timing** tool.</span></span>  
    
### <a name="fetch-events"></a><span data-ttu-id="08acd-133">Récupérer des événements</span><span class="sxs-lookup"><span data-stu-id="08acd-133">Fetch events</span></span>  

<span data-ttu-id="08acd-134">Pour en savoir plus sur les `respondWith` événements de récupération, sélectionnez la flèche de la flèche vers la gauche du `respondWith` .</span><span class="sxs-lookup"><span data-stu-id="08acd-134">To learn more about the `respondWith` fetch events, choose the dropdown arrow to the left of the `respondWith`.</span></span>  <span data-ttu-id="08acd-135">Pour plus d’informations \*\*\*\* sur la demande d’origine et la réponse **reçue,** utilisez les flèches de liste rouge correspondantes.</span><span class="sxs-lookup"><span data-stu-id="08acd-135">To find more details about the **Original Request** and **Response Received**, use the corresponding dropdown arrows.</span></span>  

## <a name="application"></a><span data-ttu-id="08acd-136">Application</span><span class="sxs-lookup"><span data-stu-id="08acd-136">Application</span></span>  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Affichage de l’application" lightbox="../media/sw-application-timeline.msft.png":::
   <span data-ttu-id="08acd-138">Affichage de l’application</span><span class="sxs-lookup"><span data-stu-id="08acd-138">Application view</span></span>  
:::image-end:::  

### <a name="service-worker-update-timeline"></a><span data-ttu-id="08acd-139">Chronologie de mise à jour du service de travail</span><span class="sxs-lookup"><span data-stu-id="08acd-139">Service worker update timeline</span></span>  

<span data-ttu-id="08acd-140">L Microsoft Edge’équipe DevTools a ajouté une chronologie dans l’outil **Application** pour refléter le cycle de vie de mise à jour du service de travail.</span><span class="sxs-lookup"><span data-stu-id="08acd-140">The Microsoft Edge DevTools team added a timeline in the **Application** tool to reflect the update lifecycle of the service worker.</span></span>  <span data-ttu-id="08acd-141">Il affiche les événements d’installation et d’activation.</span><span class="sxs-lookup"><span data-stu-id="08acd-141">It displays the installation and activation events.</span></span>  <span data-ttu-id="08acd-142">Chacun des événements possède une flèche de liste verte correspondante pour vous donner plus de détails.</span><span class="sxs-lookup"><span data-stu-id="08acd-142">Each of the events has a corresponding dropdown arrow to give you more details.</span></span>  

### <a name="request-routing-and-fetch-events"></a><span data-ttu-id="08acd-143">Demander des événements de routage et de récupération</span><span class="sxs-lookup"><span data-stu-id="08acd-143">Request routing and fetch events</span></span>  

<span data-ttu-id="08acd-144">Vous pouvez maintenant accéder aux chronologies de travail de service via **l’outil Réseau** dans le caisse de la console.</span><span class="sxs-lookup"><span data-stu-id="08acd-144">You may now access the service worker timelines through the **Network** tool in the console drawer.</span></span>  <span data-ttu-id="08acd-145">La fonctionnalité bénéficie de performances, réduit la duplication de l’interface utilisateur et crée une expérience de débogage plus complète.</span><span class="sxs-lookup"><span data-stu-id="08acd-145">The feature benefits performance, minimizes UI duplication, and creates a more comprehensive debugging experience.</span></span>  

1.  <span data-ttu-id="08acd-146">Ouvrez le service de travail que vous déboguer.</span><span class="sxs-lookup"><span data-stu-id="08acd-146">Open the service worker you are debugging.</span></span>  
1.  <span data-ttu-id="08acd-147">Choisissez le **bouton Réseau** pour ouvrir l’expérience [de routage des demandes.](#network)</span><span class="sxs-lookup"><span data-stu-id="08acd-147">Choose the **Network** button to open up the [request routing experience](#network).</span></span>  
1.  <span data-ttu-id="08acd-148">Utilisez les dropdowns **respondWith** pour récupérer les informations de demande d’événement et de réponse.</span><span class="sxs-lookup"><span data-stu-id="08acd-148">Use the **respondWith** dropdowns for fetch event request and response information.</span></span>  

<span data-ttu-id="08acd-149">**L’outil** Réseau affiche les demandes réseau qui ont été passées par le service de travail que vous déboguer.</span><span class="sxs-lookup"><span data-stu-id="08acd-149">The **Network** tool displays the network requests that went through the service worker you are debugging.</span></span>  <span data-ttu-id="08acd-150">Le filtre automatique est un moyen de restreindre votre exploration.</span><span class="sxs-lookup"><span data-stu-id="08acd-150">The automatic filter is a way to narrow down your exploration.</span></span>

## <a name="sources"></a><span data-ttu-id="08acd-151">Sources</span><span class="sxs-lookup"><span data-stu-id="08acd-151">Sources</span></span>  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="Arborescence DOM" lightbox="../media/sw-sources.msft.png":::
   <span data-ttu-id="08acd-153">Arborescence DOM</span><span class="sxs-lookup"><span data-stu-id="08acd-153">DOM tree</span></span>  
:::image-end:::  

<span data-ttu-id="08acd-154">Pour trouver plus d’informations sur la pile, définissez un point d’coupure dans le handler d’extraction.</span><span class="sxs-lookup"><span data-stu-id="08acd-154">To find more stack information, set a break point in the fetch handler.</span></span>  <span data-ttu-id="08acd-155">Les détails mènent à l’endroit où la ressource est demandée dans le script de page.</span><span class="sxs-lookup"><span data-stu-id="08acd-155">The details lead to where the resource is requested in the page script.</span></span>  <span data-ttu-id="08acd-156">Lorsque le débogger s’interrompt à l’intérieur d’un handler d’extraction, une pile combinée d’informations s’affiche dans le panneau à droite.</span><span class="sxs-lookup"><span data-stu-id="08acd-156">When the debugger pauses inside a fetch handler, a combined stack information is displayed in the panel to the right.</span></span>  <span data-ttu-id="08acd-157">Après cela, vous pouvez vous déplacer dans les cadres de pile.</span><span class="sxs-lookup"><span data-stu-id="08acd-157">After that, you may move around in the stack frames.</span></span>  

### <a name="future-work"></a><span data-ttu-id="08acd-158">Travail à venir</span><span class="sxs-lookup"><span data-stu-id="08acd-158">Future work</span></span>  

<span data-ttu-id="08acd-159">L Microsoft Edge’équipe DevTools prévoit de développer davantage les détails du cache et étudie d’autres façons d’améliorer l’expérience de débogage des travailleurs du service pour les développeurs [d’applications web][MdnProgressiveWebApps] progressives.</span><span class="sxs-lookup"><span data-stu-id="08acd-159">The Microsoft Edge DevTools team plans to further develop the cache detail and are investigating more ways to improve the service worker debugging experience for [Progressive Web Application][MdnProgressiveWebApps] developers.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="08acd-160">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="08acd-160">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Applications web progressives (P PWA) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Service Worker API | MDN"  
