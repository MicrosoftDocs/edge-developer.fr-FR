---
description: Navigation
title: Navigation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 0df8e12acb11824006515ac711250d776d276e36
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895554"
---
# <span data-ttu-id="b8c9d-104">Événements de navigation</span><span class="sxs-lookup"><span data-stu-id="b8c9d-104">Navigation events</span></span>  

<span data-ttu-id="b8c9d-105">L’ordre normal des événements de navigation est,,,, puis `NavigationStarting` `SourceChanged` `ContentLoading` `HistoryChanged` `NavigationCompleted` .</span><span class="sxs-lookup"><span data-stu-id="b8c9d-105">The normal sequence of navigation events is `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span>  <span data-ttu-id="b8c9d-106">Les événements suivants décrivent l’état de WebView2 pendant chaque navigation.</span><span class="sxs-lookup"><span data-stu-id="b8c9d-106">The following events describe the state of WebView2 during each navigation.</span></span>  

| <span data-ttu-id="b8c9d-107">Souche</span><span class="sxs-lookup"><span data-stu-id="b8c9d-107">Sequence</span></span> | <span data-ttu-id="b8c9d-108">Nom de l’événement</span><span class="sxs-lookup"><span data-stu-id="b8c9d-108">Event name</span></span> | <span data-ttu-id="b8c9d-109">Détails</span><span class="sxs-lookup"><span data-stu-id="b8c9d-109">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="b8c9d-110">1</span><span class="sxs-lookup"><span data-stu-id="b8c9d-110">1</span></span> | `NavigationStarting`  |  <span data-ttu-id="b8c9d-111">WebView2 commence à naviguer et aux résultats de navigation dans une requête réseau.</span><span class="sxs-lookup"><span data-stu-id="b8c9d-111">WebView2 starts to navigate and the navigation results in a network request.</span></span>  <span data-ttu-id="b8c9d-112">L’hôte est en mesure d’interdire la requête pendant l’événement.</span><span class="sxs-lookup"><span data-stu-id="b8c9d-112">The host is able to disallow the request during the event.</span></span>  |  
| <span data-ttu-id="b8c9d-113">deuxième</span><span class="sxs-lookup"><span data-stu-id="b8c9d-113">2</span></span> | `SourceChanged`  |  <span data-ttu-id="b8c9d-114">La source de WebView2 passe à une nouvelle URL.</span><span class="sxs-lookup"><span data-stu-id="b8c9d-114">The source of WebView2 changes to a new URL.</span></span>  <span data-ttu-id="b8c9d-115">L’événement peut résulter d’une navigation qui n’entraîne pas de requête réseau telle qu’une navigation de type fragment.</span><span class="sxs-lookup"><span data-stu-id="b8c9d-115">The event may result from a navigation that does not cause a network request such as a fragment navigation.</span></span>  |  
| <span data-ttu-id="b8c9d-116">3D</span><span class="sxs-lookup"><span data-stu-id="b8c9d-116">3</span></span> | `HistoryChanged`  |  <span data-ttu-id="b8c9d-117">L’historique des mises à jour de WebView2 est le résultat de la navigation.</span><span class="sxs-lookup"><span data-stu-id="b8c9d-117">The history of WebView2 updates as a result of the navigation.</span></span>  |  
| <span data-ttu-id="b8c9d-118">n°4</span><span class="sxs-lookup"><span data-stu-id="b8c9d-118">4</span></span> | `ContentLoading`  |  <span data-ttu-id="b8c9d-119">WebView démarre le chargement du contenu de la nouvelle page.</span><span class="sxs-lookup"><span data-stu-id="b8c9d-119">WebView starts loading content for the new page.</span></span>  |  
| <span data-ttu-id="b8c9d-120">n°5</span><span class="sxs-lookup"><span data-stu-id="b8c9d-120">5</span></span> | `NavigationCompleted`  |  <span data-ttu-id="b8c9d-121">WebView2 termine le chargement du contenu de la nouvelle page.</span><span class="sxs-lookup"><span data-stu-id="b8c9d-121">WebView2 completes loading content on the new page.</span></span>  |  

<span data-ttu-id="b8c9d-122">Effectuer un suivi `navigations` vers chaque nouveau document à l’aide de l’ID de navigation \ ( `NavigationId` \).</span><span class="sxs-lookup"><span data-stu-id="b8c9d-122">Track `navigations` to each new document using the navigation ID \(`NavigationId`\).</span></span>  <span data-ttu-id="b8c9d-123">Le `NavigationId` mode d’affichage du WebView change chaque fois qu’une navigation est réussie vers un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="b8c9d-123">The `NavigationId` of WebView changes every time there is a successful navigation to a new document.</span></span>

:::image type="complex" source="../media/navigation-graph.png" alt-text="Événements de navigation Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   <span data-ttu-id="b8c9d-125">Événements de navigation Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="b8c9d-125">The Microsoft Edge WebView2 Navigation Events</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="b8c9d-126">La figure précédente représente les événements de navigation ayant la même `NavigationId` propriété sur l’élément Arg correspondant.</span><span class="sxs-lookup"><span data-stu-id="b8c9d-126">The previous figure represents navigation events with the same `NavigationId` property on the respective event arg.</span></span>  

 `Navigations` <span data-ttu-id="b8c9d-127">les événements présentant différentes instances d' `NavigationId` événement risquent de se chevaucher.</span><span class="sxs-lookup"><span data-stu-id="b8c9d-127">events with different instances of `NavigationId` event may overlap.</span></span>  <span data-ttu-id="b8c9d-128">Par exemple, lorsque vous démarrez une navigation, vous devez attendre l’événement associé `NavigationStarting` .</span><span class="sxs-lookup"><span data-stu-id="b8c9d-128">For instance when you start a navigation, you have to wait for the related `NavigationStarting` event.</span></span>  <span data-ttu-id="b8c9d-129">Si vous démarrez une autre navigation, vous devriez voir l' `NavigationStarting` événement pour la première navigation suivie de l' `NavigationStarting` événement pour la deuxième navigation, suivi de l' `NavigationCompleted` événement pour la première navigation, puis de tout le reste des événements de navigation appropriés pour la deuxième navigation.</span><span class="sxs-lookup"><span data-stu-id="b8c9d-129">If you then start another navigation, you should see the `NavigationStarting` event for the first navigate followed by the `NavigationStarting` event for the second navigate, followed by the `NavigationCompleted` event for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span>  
 
 <span data-ttu-id="b8c9d-130">Dans les cas d’erreur, il est possible qu’il n’y ait ou non un `ContentLoading` événement selon que la navigation se poursuit sur une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b8c9d-130">In error cases there may or may not be a `ContentLoading` event depending on whether the navigation is continued to an error page.</span></span>  
 
 <span data-ttu-id="b8c9d-131">Dans le cas d’une redirection HTTP, il existe plusieurs `NavigationStarting` événements dans une ligne, où les arguments d’événement suivants sont définis par la `IsRedirect` propriété, même si la propriété `NavigationId` reste la même.</span><span class="sxs-lookup"><span data-stu-id="b8c9d-131">In the case of an HTTP redirect, there are multiple `NavigationStarting` events in a row, where subsequent event args have the `IsRedirect` property set, however the `NavigationId` remains the same.</span></span>  
 
 <span data-ttu-id="b8c9d-132">Même document `navigations` , par exemple, la navigation jusqu’à un fragment, ne génèrent pas d' `NavigationStarting` événement et n’incrémentent pas le `NavigationId` .</span><span class="sxs-lookup"><span data-stu-id="b8c9d-132">Same document `navigations`, such as navigating to a fragment, do not result in the `NavigationStarting` event and do not increment the `NavigationId`.</span></span>  

<span data-ttu-id="b8c9d-133">Pour surveiller ou annuler l' `navigations` intérieur de sous-trames dans le WebView, utilisez les `FrameNavigationStarting` événements et, `FrameNavigationCompleted` qui agissent de la même façon que les événements équivalents non liés aux images.</span><span class="sxs-lookup"><span data-stu-id="b8c9d-133">To monitor or cancel `navigations` inside subframes in the WebView, use the `FrameNavigationStarting` and the `FrameNavigationCompleted` events which act just like the equivalent non-frame counterpart events.</span></span>  

<!-- links -->  
