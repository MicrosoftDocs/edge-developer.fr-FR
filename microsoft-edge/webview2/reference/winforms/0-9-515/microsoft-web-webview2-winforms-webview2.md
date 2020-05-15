---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 25ea8367aa9d64d0a1066cf8c1564f4d9c9f05ed
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653260"
---
# <span data-ttu-id="9cea3-104">Classe Microsoft. Web. WebView2. WinForms. WebView2</span><span class="sxs-lookup"><span data-stu-id="9cea3-104">Microsoft.Web.WebView2.WinForms.WebView2 class</span></span> 

<span data-ttu-id="9cea3-105">Espace de noms: Microsoft. Web. WebView2. WinForms </span><span class="sxs-lookup"><span data-stu-id="9cea3-105">Namespace: Microsoft.Web.WebView2.WinForms</span></span>\
<span data-ttu-id="9cea3-106">Assembly: Microsoft. Web. WebView2. WinForms. dll</span><span class="sxs-lookup"><span data-stu-id="9cea3-106">Assembly: Microsoft.Web.WebView2.WinForms.dll</span></span>

```
class Microsoft.Web.WebView2.WinForms.WebView2
  : public Control
```

<span data-ttu-id="9cea3-107">Ctrl pour incorporer WebView2 dans WinForms.</span><span class="sxs-lookup"><span data-stu-id="9cea3-107">Control to embed WebView2 in WinForms.</span></span>

## <span data-ttu-id="9cea3-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="9cea3-108">Summary</span></span>

 <span data-ttu-id="9cea3-109">Ses</span><span class="sxs-lookup"><span data-stu-id="9cea3-109">Members</span></span>                        | <span data-ttu-id="9cea3-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="9cea3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9cea3-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="9cea3-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="9cea3-112">ContentLoading est distribué après le début d’une navigation sur un nouvel URI et le contenu de cet URI commence à être restitué.</span><span class="sxs-lookup"><span data-stu-id="9cea3-112">ContentLoading dispatches after a navigation begins to a new URI and the content of that URI begins to render.</span></span>
[<span data-ttu-id="9cea3-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="9cea3-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="9cea3-114">Cet événement est déclenché lors de l’initialisation de l' [CoreWebView2](#corewebview2) du contrôle (quelle que soit l’origine du déclenchement de l’initialisation), mais avant qu’elle ne soit utilisée pour n’importe quelle opération.</span><span class="sxs-lookup"><span data-stu-id="9cea3-114">This event is triggered when the control's [CoreWebView2](#corewebview2) has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="9cea3-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="9cea3-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="9cea3-116">NavigationCompleted Dispatches après qu’une navigation du document de niveau supérieur effectue un rendu correct ou non.</span><span class="sxs-lookup"><span data-stu-id="9cea3-116">NavigationCompleted dispatches after a navigate of the top level document completes rendering either successfully or not.</span></span>
[<span data-ttu-id="9cea3-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9cea3-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="9cea3-118">NavigationStarting dispatchs avant le début de la navigation dans le document de niveau supérieur de la WebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-118">NavigationStarting dispatches before a new navigate starts for the top level document of the WebView2.</span></span>
[<span data-ttu-id="9cea3-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="9cea3-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="9cea3-120">SourceChanged dispatchs après modification de la propriété source.</span><span class="sxs-lookup"><span data-stu-id="9cea3-120">SourceChanged dispatches after the Source property changes.</span></span>
[<span data-ttu-id="9cea3-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="9cea3-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="9cea3-122">WebMessageReceived de distribution de contenu Web permet d’envoyer un message à l’hôte de l’application par le biais de `chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="9cea3-122">WebMessageReceived dispatches after web content sends a message to the app host via `chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="9cea3-123">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="9cea3-123">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="9cea3-124">CoreWebView2 sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="9cea3-124">The underlying CoreWebView2.</span></span>
[<span data-ttu-id="9cea3-125">Source</span><span class="sxs-lookup"><span data-stu-id="9cea3-125">Source</span></span>](#source) | <span data-ttu-id="9cea3-126">La propriété source est l’URI du document de niveau supérieur du WebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-126">The Source property is the URI of the top level document of the WebView2.</span></span>
[<span data-ttu-id="9cea3-127">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="9cea3-127">ZoomFactor</span></span>](#zoomfactor) | <span data-ttu-id="9cea3-128">Facteur de zoom pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="9cea3-128">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="9cea3-129">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="9cea3-129">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="9cea3-130">Retourne true si WebView peut accéder à une page précédente de l’historique de navigation via la méthode GoBack.</span><span class="sxs-lookup"><span data-stu-id="9cea3-130">Returns true if the webview can navigate to a previous page in the navigation history via the GoBack method.</span></span>
[<span data-ttu-id="9cea3-131">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="9cea3-131">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="9cea3-132">Retourne true si WebView peut accéder à une page suivante de l’historique de navigation via la méthode GoForward.</span><span class="sxs-lookup"><span data-stu-id="9cea3-132">Returns true if the webview can navigate to a next page in the navigation history via the GoForward method.</span></span>
[<span data-ttu-id="9cea3-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="9cea3-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="9cea3-134">Déclenchez explicitement l’initialisation de [CoreWebView2](#corewebview2)du contrôle.</span><span class="sxs-lookup"><span data-stu-id="9cea3-134">Explicitly trigger initialization of the control's [CoreWebView2](#corewebview2).</span></span>
[<span data-ttu-id="9cea3-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="9cea3-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="9cea3-136">Exécute le script fourni dans le document de niveau supérieur du WebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-136">Executes the provided script in the top level document of the WebView2.</span></span>
[<span data-ttu-id="9cea3-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="9cea3-137">GoBack</span></span>](#goback) | <span data-ttu-id="9cea3-138">Revenir à la page précédente de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="9cea3-138">Navigate to the previous page in navigation history.</span></span>
[<span data-ttu-id="9cea3-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="9cea3-139">GoForward</span></span>](#goforward) | <span data-ttu-id="9cea3-140">Accédez à la page suivante de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="9cea3-140">Navigate to the next page in navigation history.</span></span>
[<span data-ttu-id="9cea3-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="9cea3-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="9cea3-142">Affichez le code HTML fourni en tant que document de niveau supérieur du WebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-142">Render the provided HTML as the top level document of the WebView2.</span></span>
[<span data-ttu-id="9cea3-143">Recharger</span><span class="sxs-lookup"><span data-stu-id="9cea3-143">Reload</span></span>](#reload) | <span data-ttu-id="9cea3-144">Rechargez le document de niveau supérieur du WebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-144">Reload the top level document of the WebView2.</span></span>
[<span data-ttu-id="9cea3-145">Stop</span><span class="sxs-lookup"><span data-stu-id="9cea3-145">Stop</span></span>](#stop) | <span data-ttu-id="9cea3-146">Arrêtez la navigation en cours dans le WebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-146">Stop any in progress navigation in the WebView2.</span></span>
[<span data-ttu-id="9cea3-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="9cea3-147">WebView2</span></span>](#webview2) | <span data-ttu-id="9cea3-148">Créer un contrôle WinForms WebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-148">Create a new WebView2 WinForms control.</span></span>
[<span data-ttu-id="9cea3-149">OnEnter</span><span class="sxs-lookup"><span data-stu-id="9cea3-149">OnEnter</span></span>](#onenter) | <span data-ttu-id="9cea3-150">Gestionnaire de focus protégé.</span><span class="sxs-lookup"><span data-stu-id="9cea3-150">Protected focus handler.</span></span>
[<span data-ttu-id="9cea3-151">OnSizeChanged</span><span class="sxs-lookup"><span data-stu-id="9cea3-151">OnSizeChanged</span></span>](#onsizechanged) | <span data-ttu-id="9cea3-152">Gestionnaire de SizeChanged protégé.</span><span class="sxs-lookup"><span data-stu-id="9cea3-152">Protected SizeChanged handler.</span></span>
[<span data-ttu-id="9cea3-153">OnVisibleChanged</span><span class="sxs-lookup"><span data-stu-id="9cea3-153">OnVisibleChanged</span></span>](#onvisiblechanged) | <span data-ttu-id="9cea3-154">Gestionnaire de VisibilityChanged protégé.</span><span class="sxs-lookup"><span data-stu-id="9cea3-154">Protected VisibilityChanged handler.</span></span>

## <span data-ttu-id="9cea3-155">Ses</span><span class="sxs-lookup"><span data-stu-id="9cea3-155">Members</span></span>

#### <span data-ttu-id="9cea3-156">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="9cea3-156">ContentLoading</span></span> 

<span data-ttu-id="9cea3-157">ContentLoading est distribué après le début d’une navigation sur un nouvel URI et le contenu de cet URI commence à être restitué.</span><span class="sxs-lookup"><span data-stu-id="9cea3-157">ContentLoading dispatches after a navigation begins to a new URI and the content of that URI begins to render.</span></span>

> <span data-ttu-id="9cea3-158">événement public EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="9cea3-158">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="9cea3-159">Cela équivaut à l’événement ContentLoading sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-159">This is equivalent to the ContentLoading event on the CoreWebView2.</span></span> <span data-ttu-id="9cea3-160">Pour plus d’informations, consultez la documentation CoreWebView2. ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="9cea3-160">See CoreWebView2.ContentLoading documentation for more information.</span></span>

#### <span data-ttu-id="9cea3-161">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="9cea3-161">CoreWebView2Ready</span></span> 

<span data-ttu-id="9cea3-162">Cet événement est déclenché lors de l’initialisation de l' [CoreWebView2](#corewebview2) du contrôle (quelle que soit l’origine du déclenchement de l’initialisation), mais avant qu’elle ne soit utilisée pour n’importe quelle opération.</span><span class="sxs-lookup"><span data-stu-id="9cea3-162">This event is triggered when the control's [CoreWebView2](#corewebview2) has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="9cea3-163">événement public EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="9cea3-163">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="9cea3-164">Vous devez gérer cet événement si vous avez besoin d’effectuer des opérations d’installation ponctuelles sur le CoreWebView2 que vous voulez affecter à l’ensemble de ses utilisations (par exemple, ajout de gestionnaires d’événements, configuration des paramètres, installation de scripts de création de documents, ajout d’objets hôtes).</span><span class="sxs-lookup"><span data-stu-id="9cea3-164">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span>

<span data-ttu-id="9cea3-165">Cet événement ne fournit aucun argument et l’expéditeur sera le contrôle WebView2, dont la propriété CoreWebView2 sera désormais valide (c’est-à-dire non null) pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="9cea3-165">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="9cea3-166">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="9cea3-166">NavigationCompleted</span></span> 

<span data-ttu-id="9cea3-167">NavigationCompleted Dispatches après qu’une navigation du document de niveau supérieur effectue un rendu correct ou non.</span><span class="sxs-lookup"><span data-stu-id="9cea3-167">NavigationCompleted dispatches after a navigate of the top level document completes rendering either successfully or not.</span></span>

> <span data-ttu-id="9cea3-168">événement public EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="9cea3-168">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="9cea3-169">Cela équivaut à l’événement NavigationCompleted sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-169">This is equivalent to the NavigationCompleted event on the CoreWebView2.</span></span> <span data-ttu-id="9cea3-170">Pour plus d’informations, consultez la documentation CoreWebView2. NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9cea3-170">See CoreWebView2.NavigationCompleted documentation for more information.</span></span>

#### <span data-ttu-id="9cea3-171">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9cea3-171">NavigationStarting</span></span> 

<span data-ttu-id="9cea3-172">NavigationStarting dispatchs avant le début de la navigation dans le document de niveau supérieur de la WebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-172">NavigationStarting dispatches before a new navigate starts for the top level document of the WebView2.</span></span>

> <span data-ttu-id="9cea3-173">événement public EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="9cea3-173">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="9cea3-174">Cela équivaut à l’événement NavigationStarting sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-174">This is equivalent to the NavigationStarting event on the CoreWebView2.</span></span> <span data-ttu-id="9cea3-175">Pour plus d’informations, consultez la documentation CoreWebView2. NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9cea3-175">See CoreWebView2.NavigationStarting documentation for more information.</span></span>

#### <span data-ttu-id="9cea3-176">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="9cea3-176">SourceChanged</span></span> 

<span data-ttu-id="9cea3-177">SourceChanged dispatchs après modification de la propriété source.</span><span class="sxs-lookup"><span data-stu-id="9cea3-177">SourceChanged dispatches after the Source property changes.</span></span>

> <span data-ttu-id="9cea3-178">événement public EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="9cea3-178">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="9cea3-179">Cela se produit au cours d’une navigation ou, dans le cas contraire, le script de la page modifie l’URI du document.</span><span class="sxs-lookup"><span data-stu-id="9cea3-179">This may happen during a navigation or if otherwise the script in the page changes the URI of the document.</span></span> <span data-ttu-id="9cea3-180">Cela équivaut à l’événement SourceChanged sur le CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-180">This is equivalent to the SourceChanged event on the CoreWebView2.</span></span> <span data-ttu-id="9cea3-181">Pour plus d’informations, voir la documentation relative à CoreWebView2. SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="9cea3-181">See CoreWebView2.SourceChanged documentation for more information.</span></span>

#### <span data-ttu-id="9cea3-182">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="9cea3-182">WebMessageReceived</span></span> 

<span data-ttu-id="9cea3-183">WebMessageReceived de distribution de contenu Web permet d’envoyer un message à l’hôte de l’application par le biais de `chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="9cea3-183">WebMessageReceived dispatches after web content sends a message to the app host via `chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="9cea3-184">événement public EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="9cea3-184">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="9cea3-185">Cela équivaut à l’événement WebMessageReceived sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-185">This is equivalent to the WebMessageReceived event on the CoreWebView2.</span></span> <span data-ttu-id="9cea3-186">Pour plus d’informations, consultez la documentation CoreWebView2. WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="9cea3-186">See CoreWebView2.WebMessageReceived documentation for more information.</span></span>

#### <span data-ttu-id="9cea3-187">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="9cea3-187">CoreWebView2</span></span> 

<span data-ttu-id="9cea3-188">CoreWebView2 sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="9cea3-188">The underlying CoreWebView2.</span></span>

> <span data-ttu-id="9cea3-189">public CoreWebView2 [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="9cea3-189">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="9cea3-190">Utilisez cette propriété pour effectuer davantage d’opérations sur le contenu WebView2 que ce qui est exposé sur le WebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-190">Use this property to perform more operations on the WebView2 content than is exposed on the WebView2.</span></span> <span data-ttu-id="9cea3-191">Cette valeur est null jusqu’à ce qu’elle soit initialisée.</span><span class="sxs-lookup"><span data-stu-id="9cea3-191">This value is null until it is initialized.</span></span> <span data-ttu-id="9cea3-192">Vous pouvez forcer l’initialisation du CoreWebView2 sous-jacent via la méthode InitializeAsync.</span><span class="sxs-lookup"><span data-stu-id="9cea3-192">You can force the underlying CoreWebView2 to initialize via the InitializeAsync method.</span></span>

#### <span data-ttu-id="9cea3-193">Source</span><span class="sxs-lookup"><span data-stu-id="9cea3-193">Source</span></span> 

<span data-ttu-id="9cea3-194">La propriété source est l’URI du document de niveau supérieur du WebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-194">The Source property is the URI of the top level document of the WebView2.</span></span>

> <span data-ttu-id="9cea3-195">[source](#source) URI publique</span><span class="sxs-lookup"><span data-stu-id="9cea3-195">public Uri [Source](#source)</span></span>

<span data-ttu-id="9cea3-196">Le fait de définir la source est l’équivalent d’appeler CoreWebView2. Navigate.</span><span class="sxs-lookup"><span data-stu-id="9cea3-196">Setting the Source is equivalent to calling CoreWebView2.Navigate.</span></span> <span data-ttu-id="9cea3-197">Si l’CoreWebView2 sous-jacent n’est pas encore initialisé, il s’agit de la propriété «about: Blank».</span><span class="sxs-lookup"><span data-stu-id="9cea3-197">If the underlying CoreWebView2 is not yet initialized, this property is "about:blank".</span></span> <span data-ttu-id="9cea3-198">Si la propriété est définie sur un URI non absolu ou null, la propriété reste inchangée.</span><span class="sxs-lookup"><span data-stu-id="9cea3-198">If the property is set to a non-absolute URI or null, the property remains unchanged.</span></span> <span data-ttu-id="9cea3-199">Pour plus d’informations, voir CoreWebView2. Navigate.</span><span class="sxs-lookup"><span data-stu-id="9cea3-199">See CoreWebView2.Navigate documentation for more information.</span></span>

#### <span data-ttu-id="9cea3-200">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="9cea3-200">ZoomFactor</span></span> 

<span data-ttu-id="9cea3-201">Facteur de zoom pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="9cea3-201">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="9cea3-202">double [ZoomFactor](#zoomfactor) public</span><span class="sxs-lookup"><span data-stu-id="9cea3-202">public double [ZoomFactor](#zoomfactor)</span></span>

#### <span data-ttu-id="9cea3-203">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="9cea3-203">CanGoBack</span></span> 

<span data-ttu-id="9cea3-204">Retourne true si WebView peut accéder à une page précédente de l’historique de navigation via la méthode GoBack.</span><span class="sxs-lookup"><span data-stu-id="9cea3-204">Returns true if the webview can navigate to a previous page in the navigation history via the GoBack method.</span></span>

> <span data-ttu-id="9cea3-205">public bool [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="9cea3-205">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="9cea3-206">Cela équivaut à la propriété CanGoBack sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-206">This is equivalent to the CanGoBack property on the CoreWebView2.</span></span> <span data-ttu-id="9cea3-207">Si l’CoreWebView2 sous-jacent n’est pas encore initialisé, cette propriété a la valeur false.</span><span class="sxs-lookup"><span data-stu-id="9cea3-207">If the underlying CoreWebView2 is not yet initialized, this property is false.</span></span> <span data-ttu-id="9cea3-208">Pour plus d’informations, consultez la documentation CoreWebView2. CanGoBack.</span><span class="sxs-lookup"><span data-stu-id="9cea3-208">See CoreWebView2.CanGoBack documentation for more information.</span></span>

#### <span data-ttu-id="9cea3-209">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="9cea3-209">CanGoForward</span></span> 

<span data-ttu-id="9cea3-210">Retourne true si WebView peut accéder à une page suivante de l’historique de navigation via la méthode GoForward.</span><span class="sxs-lookup"><span data-stu-id="9cea3-210">Returns true if the webview can navigate to a next page in the navigation history via the GoForward method.</span></span>

> <span data-ttu-id="9cea3-211">public bool [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="9cea3-211">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="9cea3-212">Cela équivaut à la propriété CanGoForward sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-212">This is equivalent to the CanGoForward property on the CoreWebView2.</span></span> <span data-ttu-id="9cea3-213">Si l’CoreWebView2 sous-jacent n’est pas encore initialisé, cette propriété a la valeur false.</span><span class="sxs-lookup"><span data-stu-id="9cea3-213">If the underlying CoreWebView2 is not yet initialized, this property is false.</span></span> <span data-ttu-id="9cea3-214">Pour plus d’informations, consultez la documentation CoreWebView2. CanGoForward.</span><span class="sxs-lookup"><span data-stu-id="9cea3-214">See CoreWebView2.CanGoForward documentation for more information.</span></span>

#### <span data-ttu-id="9cea3-215">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="9cea3-215">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="9cea3-216">Déclenchez explicitement l’initialisation de [CoreWebView2](#corewebview2)du contrôle.</span><span class="sxs-lookup"><span data-stu-id="9cea3-216">Explicitly trigger initialization of the control's [CoreWebView2](#corewebview2).</span></span>

> <span data-ttu-id="9cea3-217">[EnsureCoreWebView2Async](#ensurecorewebview2async)de tâches publiques (environnement CoreWebView2Environment)</span><span class="sxs-lookup"><span data-stu-id="9cea3-217">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

##### <span data-ttu-id="9cea3-218">Parameters</span><span class="sxs-lookup"><span data-stu-id="9cea3-218">Parameters</span></span>
* `environment` <span data-ttu-id="9cea3-219">CoreWebView2Environment précréé qui doit être utilisé pour créer le CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-219">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="9cea3-220">La création de votre propre environnement vous donne le contrôle de plusieurs options qui affectent la manière dont CoreWebView2 est initialisé.</span><span class="sxs-lookup"><span data-stu-id="9cea3-220">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="9cea3-221">Si vous passez la valeur null (valeur par défaut), un environnement par défaut sera créé et utilisé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="9cea3-221">If you pass null (the default value) then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="9cea3-222">Renvoie</span><span class="sxs-lookup"><span data-stu-id="9cea3-222">Returns</span></span>
<span data-ttu-id="9cea3-223">Tâche qui représente le processus d’initialisation en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="9cea3-223">A Task that represents the background initialization process.</span></span> <span data-ttu-id="9cea3-224">Lorsque la tâche se termine, la propriété CoreWebView2 peut être utilisée (c’est-à-dire non null).</span><span class="sxs-lookup"><span data-stu-id="9cea3-224">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="9cea3-225">Notez que l’événement [CoreWebView2Ready](#corewebview2ready) du contrôle est appelé avant la fin de la tâche.</span><span class="sxs-lookup"><span data-stu-id="9cea3-225">Note that the control's [CoreWebView2Ready](#corewebview2ready) event will be invoked before the task completes.</span></span> 

<span data-ttu-id="9cea3-226">L’appel de cette méthode pour les autres temps n’aura aucun effet (l’environnement spécifié est ignoré) et renvoie la même tâche que le premier appel.</span><span class="sxs-lookup"><span data-stu-id="9cea3-226">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="9cea3-227">L’appel de cette méthode une fois l’initialisation déclenchée implicitement, la définition de la propriété [source](#source) n’aura aucun effet (aucun environnement spécifié n’est ignoré) et renvoyez simplement une tâche représentant cette initialisation déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="9cea3-227">Calling this method after initialization has been implicitly triggered by setting the [Source](#source) property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> 

##### <span data-ttu-id="9cea3-228">Exceptions</span><span class="sxs-lookup"><span data-stu-id="9cea3-228">Exceptions</span></span>
* `System.InvalidOperationException` <span data-ttu-id="9cea3-229">Levée en cas d’appel à partir d’un thread sans interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9cea3-229">Thrown when invoked from non-UI thread.</span></span>

#### <span data-ttu-id="9cea3-230">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="9cea3-230">ExecuteScriptAsync</span></span> 

<span data-ttu-id="9cea3-231">Exécute le script fourni dans le document de niveau supérieur du WebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-231">Executes the provided script in the top level document of the WebView2.</span></span>

> <span data-ttu-id="9cea3-232">Tâche asynchrone publique< chaîne > [ExecuteScriptAsync](#executescriptasync)(script de chaîne)</span><span class="sxs-lookup"><span data-stu-id="9cea3-232">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string script)</span></span>

<span data-ttu-id="9cea3-233">Cela équivaut à la méthode ExecuteScriptAsync sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-233">This is equivalent to the ExecuteScriptAsync method on the CoreWebView2.</span></span> <span data-ttu-id="9cea3-234">Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode lève une exception InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="9cea3-234">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="9cea3-235">Pour plus d’informations, consultez la documentation CoreWebView2. ExecuteScriptAsync.</span><span class="sxs-lookup"><span data-stu-id="9cea3-235">See CoreWebView2.ExecuteScriptAsync documentation for more information.</span></span>

#### <span data-ttu-id="9cea3-236">GoBack</span><span class="sxs-lookup"><span data-stu-id="9cea3-236">GoBack</span></span> 

<span data-ttu-id="9cea3-237">Revenir à la page précédente de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="9cea3-237">Navigate to the previous page in navigation history.</span></span>

> <span data-ttu-id="9cea3-238">public void [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="9cea3-238">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="9cea3-239">Cela équivaut à la méthode GoBack sur le CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-239">This is equivalent to the GoBack method on the CoreWebView2.</span></span> <span data-ttu-id="9cea3-240">Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="9cea3-240">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="9cea3-241">Pour plus d’informations, voir la documentation CoreWebView2. GoBack.</span><span class="sxs-lookup"><span data-stu-id="9cea3-241">See CoreWebView2.GoBack documentation for more information.</span></span>

#### <span data-ttu-id="9cea3-242">GoForward</span><span class="sxs-lookup"><span data-stu-id="9cea3-242">GoForward</span></span> 

<span data-ttu-id="9cea3-243">Accédez à la page suivante de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="9cea3-243">Navigate to the next page in navigation history.</span></span>

> <span data-ttu-id="9cea3-244">public void [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="9cea3-244">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="9cea3-245">Cela équivaut à la méthode GoForward sur le CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-245">This is equivalent to the GoForward method on the CoreWebView2.</span></span> <span data-ttu-id="9cea3-246">Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="9cea3-246">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="9cea3-247">Pour plus d’informations, voir la documentation CoreWebView2. GoForward.</span><span class="sxs-lookup"><span data-stu-id="9cea3-247">See CoreWebView2.GoForward documentation for more information.</span></span>

#### <span data-ttu-id="9cea3-248">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="9cea3-248">NavigateToString</span></span> 

<span data-ttu-id="9cea3-249">Affichez le code HTML fourni en tant que document de niveau supérieur du WebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-249">Render the provided HTML as the top level document of the WebView2.</span></span>

> <span data-ttu-id="9cea3-250">public void [NavigateToString](#navigatetostring)(chaîne htmlContent)</span><span class="sxs-lookup"><span data-stu-id="9cea3-250">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="9cea3-251">Cela équivaut à la méthode NavigateToString sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-251">This is equivalent to the NavigateToString method on the CoreWebView2.</span></span> <span data-ttu-id="9cea3-252">Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode lève une exception InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="9cea3-252">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="9cea3-253">Pour plus d’informations, consultez la documentation CoreWebView2. NavigateToString.</span><span class="sxs-lookup"><span data-stu-id="9cea3-253">See CoreWebView2.NavigateToString documentation for more information.</span></span>

#### <span data-ttu-id="9cea3-254">Recharger</span><span class="sxs-lookup"><span data-stu-id="9cea3-254">Reload</span></span> 

<span data-ttu-id="9cea3-255">Rechargez le document de niveau supérieur du WebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-255">Reload the top level document of the WebView2.</span></span>

> <span data-ttu-id="9cea3-256">[rechargement](#reload)d’annulation publique ()</span><span class="sxs-lookup"><span data-stu-id="9cea3-256">public void [Reload](#reload)()</span></span>

<span data-ttu-id="9cea3-257">Cela équivaut à la méthode reload sur le CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-257">This is equivalent to the Reload method on the CoreWebView2.</span></span> <span data-ttu-id="9cea3-258">Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode lève une exception InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="9cea3-258">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="9cea3-259">Pour plus d’informations, voir CoreWebView2. Reload documentation.</span><span class="sxs-lookup"><span data-stu-id="9cea3-259">See CoreWebView2.Reload documentation for more information.</span></span>

#### <span data-ttu-id="9cea3-260">Stop</span><span class="sxs-lookup"><span data-stu-id="9cea3-260">Stop</span></span> 

<span data-ttu-id="9cea3-261">Arrêtez la navigation en cours dans le WebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-261">Stop any in progress navigation in the WebView2.</span></span>

> <span data-ttu-id="9cea3-262">public void [Stop](#stop)()</span><span class="sxs-lookup"><span data-stu-id="9cea3-262">public void [Stop](#stop)()</span></span>

<span data-ttu-id="9cea3-263">Cela équivaut à la méthode Stop sur le CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-263">This is equivalent to the Stop method on the CoreWebView2.</span></span> <span data-ttu-id="9cea3-264">Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="9cea3-264">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="9cea3-265">Pour plus d’informations, voir la documentation CoreWebView2. Stop.</span><span class="sxs-lookup"><span data-stu-id="9cea3-265">See CoreWebView2.Stop documentation for more information.</span></span>

#### <span data-ttu-id="9cea3-266">WebView2</span><span class="sxs-lookup"><span data-stu-id="9cea3-266">WebView2</span></span> 

<span data-ttu-id="9cea3-267">Créer un contrôle WinForms WebView2.</span><span class="sxs-lookup"><span data-stu-id="9cea3-267">Create a new WebView2 WinForms control.</span></span>

> <span data-ttu-id="9cea3-268">public [WebView2](#webview2)()</span><span class="sxs-lookup"><span data-stu-id="9cea3-268">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="9cea3-269">Après construction, la propriété CoreWebView2 a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="9cea3-269">After construction the CoreWebView2 property is null.</span></span> <span data-ttu-id="9cea3-270">Appelez [EnsureCoreWebView2Async](#ensurecorewebview2async) pour initialiser la CoreWebView2 sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="9cea3-270">Call [EnsureCoreWebView2Async](#ensurecorewebview2async) to initialize the underlying CoreWebView2.</span></span>

#### <span data-ttu-id="9cea3-271">OnEnter</span><span class="sxs-lookup"><span data-stu-id="9cea3-271">OnEnter</span></span> 

<span data-ttu-id="9cea3-272">Gestionnaire de focus protégé.</span><span class="sxs-lookup"><span data-stu-id="9cea3-272">Protected focus handler.</span></span>

> <span data-ttu-id="9cea3-273">remplacement [protégé annulé entrée](#onenter)(EventArgs e)</span><span class="sxs-lookup"><span data-stu-id="9cea3-273">protected override void [OnEnter](#onenter)(EventArgs e)</span></span>

#### <span data-ttu-id="9cea3-274">OnSizeChanged</span><span class="sxs-lookup"><span data-stu-id="9cea3-274">OnSizeChanged</span></span> 

<span data-ttu-id="9cea3-275">Gestionnaire de SizeChanged protégé.</span><span class="sxs-lookup"><span data-stu-id="9cea3-275">Protected SizeChanged handler.</span></span>

> <span data-ttu-id="9cea3-276">[OnSizeChanged](#onsizechanged)de remplacement protégé void</span><span class="sxs-lookup"><span data-stu-id="9cea3-276">protected override void [OnSizeChanged](#onsizechanged)(EventArgs e)</span></span>

#### <span data-ttu-id="9cea3-277">OnVisibleChanged</span><span class="sxs-lookup"><span data-stu-id="9cea3-277">OnVisibleChanged</span></span> 

<span data-ttu-id="9cea3-278">Gestionnaire de VisibilityChanged protégé.</span><span class="sxs-lookup"><span data-stu-id="9cea3-278">Protected VisibilityChanged handler.</span></span>

> <span data-ttu-id="9cea3-279">[OnVisibleChanged](#onvisiblechanged)de remplacement protégé void</span><span class="sxs-lookup"><span data-stu-id="9cea3-279">protected override void [OnVisibleChanged](#onvisiblechanged)(EventArgs e)</span></span>

