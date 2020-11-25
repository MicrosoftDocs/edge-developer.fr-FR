---
description: En savoir plus sur les améliorations apportées aux travailleurs de services et leur utilisation.
title: Améliorations apportées aux travailleurs de services
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, travailleur de service, PWA
ms.openlocfilehash: 4e1b43235ccd7b108d2aadd1c803aa3276fa1265
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "11190029"
---
# <span data-ttu-id="e9fa6-104">Améliorations apportées aux travailleurs de services</span><span class="sxs-lookup"><span data-stu-id="e9fa6-104">Service Worker improvements</span></span>  

<span data-ttu-id="e9fa6-105">Cet article vous présente les améliorations apportées aux [travailleurs de services][MdnServiceWorkerApi] et aux requêtes réseau qui passent par eux.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-105">This article teaches you about improvements to [service workers][MdnServiceWorkerApi] and the network requests that pass through each one.</span></span>  <span data-ttu-id="e9fa6-106">Les **améliorations apportées aux travailleurs de services** se trouvent dans les outils **réseau**, **application**et **sources** .</span><span class="sxs-lookup"><span data-stu-id="e9fa6-106">The **service worker improvements** are in the **Network**, **Application**, and **Sources** tools.</span></span>  <span data-ttu-id="e9fa6-107">Les améliorations incluent les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-107">The improvements include the following tasks.</span></span>  

*   <span data-ttu-id="e9fa6-108">Déboguer selon les chronologies des travailleurs de service.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-108">Debug based on Service Worker timelines.</span></span>  
    *   <span data-ttu-id="e9fa6-109">Le début d’une demande et la durée de l’amorce.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-109">The start of a request and duration of the bootstrap.</span></span>  
    *   <span data-ttu-id="e9fa6-110">Mise à jour vers l’enregistrement du travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-110">Update to Service worker registration.</span></span>  
    *   <span data-ttu-id="e9fa6-111">Exécution d’une requête à l’aide du gestionnaire d' [événements FETCH][MdnFetchEvent] .</span><span class="sxs-lookup"><span data-stu-id="e9fa6-111">The runtime of a request using the [fetch event][MdnFetchEvent] handler.</span></span>  
    *   <span data-ttu-id="e9fa6-112">Exécution de tous les événements de récupération pour le chargement d’un client.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-112">The runtime of all fetch events for loading a client.</span></span>  
*   <span data-ttu-id="e9fa6-113">Explorez les détails d’exécution des gestionnaires d’événements de récupération, d’installation de gestionnaires d’événements et de gestionnaires d’événements d’activation.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-113">Explore the runtime details of fetch event handlers, install event handlers, and activate event handlers.</span></span>  
*   <span data-ttu-id="e9fa6-114">Pas à pas dans le gestionnaire d’événements Fetch et déconnectez-vous avec les [informations de script de page](#sources).</span><span class="sxs-lookup"><span data-stu-id="e9fa6-114">Step into and out of fetch event handler with [page script information](#sources).</span></span>  

<span data-ttu-id="e9fa6-115">Ces expériences s’étendent à trois outils de développement différents.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-115">The experiences span three different developer tools.</span></span>  

1.  <span data-ttu-id="e9fa6-116">Outil [réseau](#network) .</span><span class="sxs-lookup"><span data-stu-id="e9fa6-116">The [Network](#network) tool.</span></span>  <span data-ttu-id="e9fa6-117">Choisissez une requête réseau qui s’exécute par le biais d’un travailleur de service et accédez à la chronologie correspondante du travailleur de service dans l’outil **minutage** .</span><span class="sxs-lookup"><span data-stu-id="e9fa6-117">Choose a network request that runs through a service worker and access the corresponding timeline of the service worker in the **Timing** tool.</span></span>  
1.  <span data-ttu-id="e9fa6-118">Outil de l' [application](#application) .</span><span class="sxs-lookup"><span data-stu-id="e9fa6-118">The [Application](#application) tool.</span></span>  <span data-ttu-id="e9fa6-119">Pour déboguer les travailleurs de service, accédez à l’outil **travailleurs de service** .</span><span class="sxs-lookup"><span data-stu-id="e9fa6-119">To debug the service workers, navigate to the **Service Workers** tool.</span></span>  
1.  <span data-ttu-id="e9fa6-120">Outil [sources](#sources) .</span><span class="sxs-lookup"><span data-stu-id="e9fa6-120">The [Sources](#sources) tool.</span></span>  <span data-ttu-id="e9fa6-121">Accédez à des informations de script de page lorsque vous accédez à des gestionnaires d’événements Fetch.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-121">Access page script information when stepping into fetch event handlers.</span></span>  

## <span data-ttu-id="e9fa6-122">Network</span><span class="sxs-lookup"><span data-stu-id="e9fa6-122">Network</span></span>  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Chronologie du travailleur de service dans l’outil réseau" lightbox="../media/sw-network-timeline.msft.png":::
   <span data-ttu-id="e9fa6-124">Vue réseau</span><span class="sxs-lookup"><span data-stu-id="e9fa6-124">Network view</span></span>  
:::image-end:::  

<span data-ttu-id="e9fa6-125">Pour accéder aux fonctionnalités de débogage du travailleur de service dans l’outil **réseau** , effectuez l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-125">To access the service worker debugging features in the **Network** tool, complete one of the following actions.</span></span>  

*   <span data-ttu-id="e9fa6-126">Accédez directement à l’outil **réseau** .</span><span class="sxs-lookup"><span data-stu-id="e9fa6-126">Access directly in the **Network** tool.</span></span>  
*   <span data-ttu-id="e9fa6-127">Démarré dans l’outil de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="e9fa6-127">Started in the **Application** tool.</span></span>  
    
### <span data-ttu-id="e9fa6-128">Demander le routage</span><span class="sxs-lookup"><span data-stu-id="e9fa6-128">Request routing</span></span>  

<span data-ttu-id="e9fa6-129">Pour faciliter l’affichage du routage de requête, les chronologies affichent désormais le démarrage du travailleur de service et les `respondWith` événements de récupération.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-129">To make request routing easier to visualize, timelines now display the service worker start-up and the `respondWith` fetch events.</span></span>  <span data-ttu-id="e9fa6-130">Pour déboguer et visualiser une requête réseau transmise par le biais d’un travailleur de service, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-130">To debug and visualize a network request that passed through a service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="e9fa6-131">Cliquez sur la demande de réseau qui a été passée par un travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-131">Choose the network request that went through a service worker.</span></span>  
1.  <span data-ttu-id="e9fa6-132">Ouvrez l’outil **minutage** .</span><span class="sxs-lookup"><span data-stu-id="e9fa6-132">Open the **Timing** tool.</span></span>  
    
### <span data-ttu-id="e9fa6-133">Extraire des événements</span><span class="sxs-lookup"><span data-stu-id="e9fa6-133">Fetch events</span></span>  

<span data-ttu-id="e9fa6-134">Pour en savoir plus sur les `respondWith` événements FETCH, cliquez sur la flèche déroulante située à gauche de la zone `respondWith` .</span><span class="sxs-lookup"><span data-stu-id="e9fa6-134">To learn more about the `respondWith` fetch events, choose the dropdown arrow to the left of the `respondWith`.</span></span>  <span data-ttu-id="e9fa6-135">Pour en savoir plus sur la demande et la **réponse** **d’origine** reçues, utilisez les flèches déroulantes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-135">To find more details about the **Original Request** and **Response Received**, use the corresponding dropdown arrows.</span></span>  

## <span data-ttu-id="e9fa6-136">Application</span><span class="sxs-lookup"><span data-stu-id="e9fa6-136">Application</span></span>  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Affichage des applications" lightbox="../media/sw-application-timeline.msft.png":::
   <span data-ttu-id="e9fa6-138">Affichage des applications</span><span class="sxs-lookup"><span data-stu-id="e9fa6-138">Application view</span></span>  
:::image-end:::  

### <span data-ttu-id="e9fa6-139">Chronologie des mises à jour de service Worker</span><span class="sxs-lookup"><span data-stu-id="e9fa6-139">Service worker update timeline</span></span>  

<span data-ttu-id="e9fa6-140">L’équipe Microsoft Edge DevTools a ajouté une chronologie dans l’outil de l' **application** pour refléter le cycle de vie des mises à jour du travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-140">The Microsoft Edge DevTools team added a timeline in the **Application** tool to reflect the update lifecycle of the service worker.</span></span>  <span data-ttu-id="e9fa6-141">Il affiche les événements d’installation et d’activation.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-141">It displays the installation and activation events.</span></span>  <span data-ttu-id="e9fa6-142">Chacun des événements dispose d’une flèche déroulante correspondante pour vous fournir des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-142">Each of the events has a corresponding dropdown arrow to give you more details.</span></span>  

### <span data-ttu-id="e9fa6-143">Demander le routage et récupérer des événements</span><span class="sxs-lookup"><span data-stu-id="e9fa6-143">Request routing and fetch events</span></span>  

<span data-ttu-id="e9fa6-144">Vous pouvez maintenant accéder aux chronologies du travailleur de service via l’outil **réseau** du tiroir de la console.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-144">You may now access the service worker timelines through the **Network** tool in the console drawer.</span></span>  <span data-ttu-id="e9fa6-145">La fonctionnalité présente les performances, réduit la réplication de l’interface utilisateur et crée une connaissance plus complète en matière de débogage.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-145">The feature benefits performance, minimizes UI duplication, and creates a more comprehensive debugging experience.</span></span>  

1.  <span data-ttu-id="e9fa6-146">Ouvrez le travailleur de service en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-146">Open the service worker you are debugging.</span></span>  
1.  <span data-ttu-id="e9fa6-147">Cliquez sur le bouton **réseau** pour ouvrir l' [interface de demande de routage](#network).</span><span class="sxs-lookup"><span data-stu-id="e9fa6-147">Choose the **Network** button to open up the [request routing experience](#network).</span></span>  
1.  <span data-ttu-id="e9fa6-148">Utilisez les listes déroulantes **respondWith** pour récupérer des informations de demande et de réponse à l’événement.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-148">Use the **respondWith** dropdowns for fetch event request and response information.</span></span>  

<span data-ttu-id="e9fa6-149">L’outil **réseau** affiche les requêtes réseau ayant suivi le travailleur de service en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-149">The **Network** tool displays the network requests that went through the service worker you are debugging.</span></span>  <span data-ttu-id="e9fa6-150">Le filtre automatique permet de limiter votre exploration.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-150">The automatic filter is a way to narrow down your exploration.</span></span>

## <span data-ttu-id="e9fa6-151">Sources</span><span class="sxs-lookup"><span data-stu-id="e9fa6-151">Sources</span></span>  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="Affichage DOM" lightbox="../media/sw-sources.msft.png":::
   <span data-ttu-id="e9fa6-153">Affichage DOM</span><span class="sxs-lookup"><span data-stu-id="e9fa6-153">DOM view</span></span>  
:::image-end:::  

<span data-ttu-id="e9fa6-154">Pour trouver d’autres informations sur la pile, définissez un point d’arrêt dans le gestionnaire de récupération.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-154">To find more stack information, set a break point in the fetch handler.</span></span>  <span data-ttu-id="e9fa6-155">Les détails conduisent à l’endroit où la ressource est demandée dans le script de la page.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-155">The details lead to where the resource is requested in the page script.</span></span>  <span data-ttu-id="e9fa6-156">Lorsque le débogueur s’arrête dans un gestionnaire de récupération, des informations sur la pile combinée apparaissent dans le panneau de droite.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-156">When the debugger pauses inside a fetch handler, a combined stack information is displayed in the panel to the right.</span></span>  <span data-ttu-id="e9fa6-157">Après cela, vous pouvez vous déplacer dans les frames de pile.</span><span class="sxs-lookup"><span data-stu-id="e9fa6-157">After that, you may move around in the stack frames.</span></span>  

### <span data-ttu-id="e9fa6-158">Future Work</span><span class="sxs-lookup"><span data-stu-id="e9fa6-158">Future work</span></span>  

<span data-ttu-id="e9fa6-159">L’équipe Microsoft Edge DevTools envisage d’améliorer davantage les détails de la mise en cache et étudie d’autres façons d’améliorer l’interface de débogage du travailleur de services pour les développeurs d' [applications Web progressives][MdnProgressiveWebApps] .</span><span class="sxs-lookup"><span data-stu-id="e9fa6-159">The Microsoft Edge DevTools team plans to further develop the cache detail and are investigating more ways to improve the service worker debugging experience for [Progressive Web Application][MdnProgressiveWebApps] developers.</span></span>  

## <span data-ttu-id="e9fa6-160">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="e9fa6-160">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Applications Web progressives (PWAs) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API du travailleur de service | MDN"  
