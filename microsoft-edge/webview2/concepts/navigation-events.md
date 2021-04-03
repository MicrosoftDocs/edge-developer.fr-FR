---
description: Navigation
title: Navigation | WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: e87994d6205f81e01385a131e17091d0c8b001d5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11470843"
---
# <a name="navigation-events"></a><span data-ttu-id="491c9-104">Événements de navigation</span><span class="sxs-lookup"><span data-stu-id="491c9-104">Navigation events</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="491c9-105">Plateformes pris en charge :</span><span class="sxs-lookup"><span data-stu-id="491c9-105">Supported platforms:</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="491c9-106">Win32, Windows Forms, WinUi, WPF</span><span class="sxs-lookup"><span data-stu-id="491c9-106">Win32, Windows Forms, WinUi, WPF</span></span>
   :::column-end:::
:::row-end:::  

<span data-ttu-id="491c9-107">Les événements de navigation s’exécutent lorsque des actions asynchrones spécifiques se produisent sur le contenu affiché dans une instance WebView2.</span><span class="sxs-lookup"><span data-stu-id="491c9-107">Navigation events run when specific asynchronous actions occur to the content displayed in a WebView2 instance.</span></span>  <span data-ttu-id="491c9-108">Par exemple, lorsqu’un utilisateur WebView2 navigue vers un nouveau site web, le contenu natif écoute la modification à l’aide de `NavigationStarting` l’événement.</span><span class="sxs-lookup"><span data-stu-id="491c9-108">For example, when a WebView2 user navigates to a new website, the native content listens for the change using `NavigationStarting` event.</span></span>  <span data-ttu-id="491c9-109">Une fois l’action de navigation terminée, `NavigationCompleted` s’exécute.</span><span class="sxs-lookup"><span data-stu-id="491c9-109">When the navigation action completes, `NavigationCompleted` runs.</span></span>  <span data-ttu-id="491c9-110">Pour obtenir un bon exemple d’événements de navigation, accédez au guide de [mise en place de WebView2.][Webview2IndexGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="491c9-110">For a good example of navigation events, navigate to [WebView2 getting started guide][Webview2IndexGettingStarted].</span></span>  

<!--todo:  Move the relevant information out of the getting started guide to better focus the content and leave the most concise elements in the getting started guide.  -->   

<span data-ttu-id="491c9-111">La séquence normale d’événements de navigation `NavigationStarting` est , , et puis `SourceChanged` `ContentLoading` `HistoryChanged` `NavigationCompleted` .</span><span class="sxs-lookup"><span data-stu-id="491c9-111">The normal sequence of navigation events is `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span>  <span data-ttu-id="491c9-112">Les événements suivants décrivent l’état de WebView2 pendant chaque navigation.</span><span class="sxs-lookup"><span data-stu-id="491c9-112">The following events describe the state of WebView2 during each navigation.</span></span>  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/navigation-graph.png" alt-text="Événements de navigation Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
         <span data-ttu-id="491c9-114">Événements de navigation Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="491c9-114">The Microsoft Edge WebView2 Navigation Events</span></span>  
      :::image-end:::  
      
      > [!NOTE]
      > <span data-ttu-id="491c9-115">La figure représente les événements de navigation avec la même `NavigationId` propriété sur l’argument d’événement respectif.</span><span class="sxs-lookup"><span data-stu-id="491c9-115">The figure represents navigation events with the same `NavigationId` property on the respective event argument.</span></span>  
   :::column-end:::
   :::column span="2":::
      | <span data-ttu-id="491c9-116">Séquence</span><span class="sxs-lookup"><span data-stu-id="491c9-116">Sequence</span></span> | <span data-ttu-id="491c9-117">Nom de l’événement</span><span class="sxs-lookup"><span data-stu-id="491c9-117">Event name</span></span> | <span data-ttu-id="491c9-118">Détails</span><span class="sxs-lookup"><span data-stu-id="491c9-118">Details</span></span> |  
      |:--- |:--- |:--- |  
      | <span data-ttu-id="491c9-119">1</span><span class="sxs-lookup"><span data-stu-id="491c9-119">1</span></span> | `NavigationStarting`  |  <span data-ttu-id="491c9-120">WebView2 commence à naviguer et la navigation entraîne une demande réseau.</span><span class="sxs-lookup"><span data-stu-id="491c9-120">WebView2 starts to navigate and the navigation results in a network request.</span></span>  <span data-ttu-id="491c9-121">L’hôte peut désapprouver la demande pendant l’événement.</span><span class="sxs-lookup"><span data-stu-id="491c9-121">The host may disallow the request during the event.</span></span>  |  
      | <span data-ttu-id="491c9-122">2</span><span class="sxs-lookup"><span data-stu-id="491c9-122">2</span></span> | `SourceChanged`  |  <span data-ttu-id="491c9-123">La source de WebView2 se transforme en une nouvelle URL.</span><span class="sxs-lookup"><span data-stu-id="491c9-123">The source of WebView2 changes to a new URL.</span></span>  <span data-ttu-id="491c9-124">L’événement peut être le résultat d’une action de navigation qui ne provoque pas de demande réseau telle qu’une navigation par fragment.</span><span class="sxs-lookup"><span data-stu-id="491c9-124">The event may result from a navigation action that does not cause a network request such as a fragment navigation.</span></span>  |  
      | <span data-ttu-id="491c9-125">3</span><span class="sxs-lookup"><span data-stu-id="491c9-125">3</span></span> | `ContentLoading`  |  <span data-ttu-id="491c9-126">WebView commence à charger le contenu de la nouvelle page.</span><span class="sxs-lookup"><span data-stu-id="491c9-126">WebView starts loading content for the new page.</span></span>  |  
      | <span data-ttu-id="491c9-127">4</span><span class="sxs-lookup"><span data-stu-id="491c9-127">4</span></span> | `HistoryChanged`  |  <span data-ttu-id="491c9-128">La navigation entraîne la mise à jour de l’historique de WebView2.</span><span class="sxs-lookup"><span data-stu-id="491c9-128">The navigation causes the history of WebView2 to update.</span></span>  |  
      | <span data-ttu-id="491c9-129">5</span><span class="sxs-lookup"><span data-stu-id="491c9-129">5</span></span> | `NavigationCompleted`  |  <span data-ttu-id="491c9-130">WebView2 termine le chargement du contenu sur la nouvelle page.</span><span class="sxs-lookup"><span data-stu-id="491c9-130">WebView2 completes loading content on the new page.</span></span>  |  
   :::column-end:::
:::row-end:::

<span data-ttu-id="491c9-131">Suivre les événements de navigation vers chaque nouveau document à l’aide de l’ID de navigation \( `NavigationId` événement\).</span><span class="sxs-lookup"><span data-stu-id="491c9-131">Track navigation events to each new document using the navigation ID \(`NavigationId` event\).</span></span>  <span data-ttu-id="491c9-132">`NavigationId`L’événement WebView change chaque fois qu’une navigation réussie vers un nouveau document se termine.</span><span class="sxs-lookup"><span data-stu-id="491c9-132">The `NavigationId` event of WebView changes every time a successful navigation to a new document completes.</span></span>  

 <span data-ttu-id="491c9-133">Les événements de navigation avec différentes instances `NavigationId` d’événement peuvent se chevaucher.</span><span class="sxs-lookup"><span data-stu-id="491c9-133">Navigation events with different instances of `NavigationId` event may overlap.</span></span>  <span data-ttu-id="491c9-134">Par exemple, lorsque vous démarrez un événement de navigation, vous devez attendre l’événement `NavigationStarting` associé.</span><span class="sxs-lookup"><span data-stu-id="491c9-134">For instance, when you start a navigation event, you must wait for the related `NavigationStarting` event.</span></span>  <span data-ttu-id="491c9-135">Si vous démarrez ensuite une autre navigation, vous devez voir l’événement pour la première navigation suivi de l’événement pour le second, suivi de l’événement pour la première navigation, puis de tous les autres événements de navigation appropriés pour la `NavigationStarting` `NavigationStarting` deuxième `NavigationCompleted` navigation.</span><span class="sxs-lookup"><span data-stu-id="491c9-135">If you then start another navigation, you should see the `NavigationStarting` event for the first navigate followed by the `NavigationStarting` event for the second navigate, followed by the `NavigationCompleted` event for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span>  
 
 <span data-ttu-id="491c9-136">Dans les cas d’erreur, il peut y avoir ou non un événement selon que la navigation est continue `ContentLoading` à une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="491c9-136">In error cases, there may or may not be a `ContentLoading` event depending on whether the navigation is continued to an error page.</span></span>  
 
 <span data-ttu-id="491c9-137">Si une redirection HTTP se produit, il existe plusieurs événements dans une ligne, où les arguments d’événement ultérieurs ont la propriété définie, mais l’événement `NavigationStarting` `IsRedirect` reste le `NavigationId` même.</span><span class="sxs-lookup"><span data-stu-id="491c9-137">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row, where later event arguments have the `IsRedirect` property set, however the `NavigationId` event remains the same.</span></span>  
 
 <span data-ttu-id="491c9-138">Les mêmes événements de navigation de document, tels que la navigation vers un fragment, n’entraînent pas l’événement et `NavigationStarting` n’incrémentent `NavigationId` pas l’événement.</span><span class="sxs-lookup"><span data-stu-id="491c9-138">Same document navigation events, such as navigating to a fragment, do not result in the `NavigationStarting` event and do not increment the `NavigationId` event.</span></span>  

<span data-ttu-id="491c9-139">Pour surveiller ou annuler des événements de navigation à l’intérieur de sous-images dans une instance WebView2, utilisez les événements qui agissent comme les événements équivalents `FrameNavigationStarting` `FrameNavigationCompleted` sans trame.</span><span class="sxs-lookup"><span data-stu-id="491c9-139">To monitor or cancel navigation events inside subframes in a WebView2 instance, use the `FrameNavigationStarting` and `FrameNavigationCompleted` events that act just like the equivalent non-frame counterpart events.</span></span>  

## <a name="see-also"></a><span data-ttu-id="491c9-140">Voir également</span><span class="sxs-lookup"><span data-stu-id="491c9-140">See also</span></span>  

*   <span data-ttu-id="491c9-141">Pour commencer à utiliser WebView2, accédez aux guides de mise en page [WebView2.][Webview2IndexGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="491c9-141">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2IndexGettingStarted] guides.</span></span>  
*   <span data-ttu-id="491c9-142">Pour obtenir un exemple complet des fonctionnalités WebView2, accédez au référentiel [WebView2Samples][GithubMicrosoftedgeWebview2samples] sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="491c9-142">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>  
*   <span data-ttu-id="491c9-143">Pour plus d’informations sur les API WebView2, accédez à la [référence d’API.][DotnetApiMicrosoftWebWebview2WpfWebview2]</span><span class="sxs-lookup"><span data-stu-id="491c9-143">For more detailed information about WebView2 APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2WpfWebview2].</span></span>  
*   <span data-ttu-id="491c9-144">Pour plus d’informations sur WebView2, accédez à [Ressources WebView2.][Webview2IndexNextSteps]</span><span class="sxs-lookup"><span data-stu-id="491c9-144">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="491c9-145">Entrer en contact avec l’équipe Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="491c9-145">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGettingStarted]: ../index.md#getting-started "Getting started - Introduction to Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Étapes suivantes : présentation de Microsoft Edge WebView2 | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Classe WebView2 | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
