---
description: Navigation
title: Navigation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/05/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: ac15b9f32a29c64bbdc2a7886fa654a2d71a5453
ms.sourcegitcommit: 4cea8cf99b5f12db9d2daba99bbf48f3ccc537fe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314796"
---
# <span data-ttu-id="44a5a-104">Événements de navigation</span><span class="sxs-lookup"><span data-stu-id="44a5a-104">Navigation events</span></span>  

<span data-ttu-id="44a5a-105">La séquence normale d’événements de navigation `NavigationStarting` est , , et puis `SourceChanged` `ContentLoading` `HistoryChanged` `NavigationCompleted` .</span><span class="sxs-lookup"><span data-stu-id="44a5a-105">The normal sequence of navigation events is `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span>  <span data-ttu-id="44a5a-106">Les événements suivants décrivent l’état de WebView2 pendant chaque navigation.</span><span class="sxs-lookup"><span data-stu-id="44a5a-106">The following events describe the state of WebView2 during each navigation.</span></span>  

| <span data-ttu-id="44a5a-107">Séquence</span><span class="sxs-lookup"><span data-stu-id="44a5a-107">Sequence</span></span> | <span data-ttu-id="44a5a-108">Nom de l’événement</span><span class="sxs-lookup"><span data-stu-id="44a5a-108">Event name</span></span> | <span data-ttu-id="44a5a-109">Détails</span><span class="sxs-lookup"><span data-stu-id="44a5a-109">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="44a5a-110">1</span><span class="sxs-lookup"><span data-stu-id="44a5a-110">1</span></span> | `NavigationStarting`  |  <span data-ttu-id="44a5a-111">WebView2 commence à naviguer et la navigation entraîne une demande réseau.</span><span class="sxs-lookup"><span data-stu-id="44a5a-111">WebView2 starts to navigate and the navigation results in a network request.</span></span>  <span data-ttu-id="44a5a-112">L’hôte est en mesure d’interdiquer la demande pendant l’événement.</span><span class="sxs-lookup"><span data-stu-id="44a5a-112">The host is able to disallow the request during the event.</span></span>  |  
| <span data-ttu-id="44a5a-113">2</span><span class="sxs-lookup"><span data-stu-id="44a5a-113">2</span></span> | `SourceChanged`  |  <span data-ttu-id="44a5a-114">La source de WebView2 se transforme en une nouvelle URL.</span><span class="sxs-lookup"><span data-stu-id="44a5a-114">The source of WebView2 changes to a new URL.</span></span>  <span data-ttu-id="44a5a-115">L’événement peut être le résultat d’une navigation qui ne provoque pas de demande réseau telle qu’une navigation par fragment.</span><span class="sxs-lookup"><span data-stu-id="44a5a-115">The event may result from a navigation that does not cause a network request such as a fragment navigation.</span></span>  |  
| <span data-ttu-id="44a5a-116">3</span><span class="sxs-lookup"><span data-stu-id="44a5a-116">3</span></span> | `HistoryChanged`  |  <span data-ttu-id="44a5a-117">Historique des mises à jour WebView2 suite à la navigation.</span><span class="sxs-lookup"><span data-stu-id="44a5a-117">The history of WebView2 updates as a result of the navigation.</span></span>  |  
| <span data-ttu-id="44a5a-118">4</span><span class="sxs-lookup"><span data-stu-id="44a5a-118">4</span></span> | `ContentLoading`  |  <span data-ttu-id="44a5a-119">WebView2 démarre le chargement du contenu pour la nouvelle page.</span><span class="sxs-lookup"><span data-stu-id="44a5a-119">WebView2 starts loading content for the new page.</span></span>  |  
| <span data-ttu-id="44a5a-120">5</span><span class="sxs-lookup"><span data-stu-id="44a5a-120">5</span></span> | `NavigationCompleted`  |  <span data-ttu-id="44a5a-121">WebView2 termine le chargement du contenu sur la nouvelle page.</span><span class="sxs-lookup"><span data-stu-id="44a5a-121">WebView2 completes loading content on the new page.</span></span>  |  

<span data-ttu-id="44a5a-122">Suivez `navigations` chaque nouveau document à l’aide de l’ID de navigation \( `NavigationId` \).</span><span class="sxs-lookup"><span data-stu-id="44a5a-122">Track `navigations` to each new document using the navigation ID \(`NavigationId`\).</span></span>  <span data-ttu-id="44a5a-123">Le `NavigationId` webview change chaque fois qu’une navigation vers un nouveau document réussit.</span><span class="sxs-lookup"><span data-stu-id="44a5a-123">The `NavigationId` of WebView changes every time there is a successful navigation to a new document.</span></span>

:::image type="complex" source="../media/navigation-graph.png" alt-text="Événements de navigation Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   <span data-ttu-id="44a5a-125">Événements de navigation Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="44a5a-125">The Microsoft Edge WebView2 Navigation Events</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="44a5a-126">La figure précédente représente les événements de navigation avec la même `NavigationId` propriété sur l’rg d’événement respectif.</span><span class="sxs-lookup"><span data-stu-id="44a5a-126">The previous figure represents navigation events with the same `NavigationId` property on the respective event arg.</span></span>  

 `Navigations` <span data-ttu-id="44a5a-127">les événements avec différentes instances `NavigationId` d’événement peuvent se chevaucher.</span><span class="sxs-lookup"><span data-stu-id="44a5a-127">events with different instances of `NavigationId` event may overlap.</span></span>  <span data-ttu-id="44a5a-128">Par exemple, lorsque vous démarrez une navigation, vous devez attendre l’événement `NavigationStarting` associé.</span><span class="sxs-lookup"><span data-stu-id="44a5a-128">For instance when you start a navigation, you have to wait for the related `NavigationStarting` event.</span></span>  <span data-ttu-id="44a5a-129">Si vous démarrez ensuite une autre navigation, vous devez voir l’événement pour la première navigation suivi de l’événement pour le second, suivi de l’événement pour la première navigation, puis de tous les autres événements de navigation appropriés pour la `NavigationStarting` `NavigationStarting` deuxième `NavigationCompleted` navigation.</span><span class="sxs-lookup"><span data-stu-id="44a5a-129">If you then start another navigation, you should see the `NavigationStarting` event for the first navigate followed by the `NavigationStarting` event for the second navigate, followed by the `NavigationCompleted` event for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span>  
 
 <span data-ttu-id="44a5a-130">Dans les cas d’erreur, il peut y avoir ou non un événement en fonction de la poursuite de la `ContentLoading` navigation vers une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="44a5a-130">In error cases there may or may not be a `ContentLoading` event depending on whether the navigation is continued to an error page.</span></span>  
 
 <span data-ttu-id="44a5a-131">Dans le cas d’une redirection HTTP, il existe plusieurs événements d’une ligne, où lesrgs d’événements suivants ont la propriété définie, mais les `NavigationStarting` `IsRedirect` `NavigationId` événements restent identiques.</span><span class="sxs-lookup"><span data-stu-id="44a5a-131">In the case of an HTTP redirect, there are multiple `NavigationStarting` events in a row, where subsequent event args have the `IsRedirect` property set, however the `NavigationId` remains the same.</span></span>  
 
 <span data-ttu-id="44a5a-132">Le même document, tel que la navigation vers un fragment, n’entraîne pas l’événement et `navigations` `NavigationStarting` n’incrémente pas le `NavigationId` .</span><span class="sxs-lookup"><span data-stu-id="44a5a-132">Same document `navigations`, such as navigating to a fragment, do not result in the `NavigationStarting` event and do not increment the `NavigationId`.</span></span>  

<span data-ttu-id="44a5a-133">Pour surveiller ou annuler à l’intérieur de sous-images du WebView, utilisez les événements qui agissent comme les événements équivalents `navigations` `FrameNavigationStarting` sans `FrameNavigationCompleted` trame.</span><span class="sxs-lookup"><span data-stu-id="44a5a-133">To monitor or cancel `navigations` inside subframes in the WebView, use the `FrameNavigationStarting` and the `FrameNavigationCompleted` events which act just like the equivalent non-frame counterpart events.</span></span>  

<!-- links -->  
