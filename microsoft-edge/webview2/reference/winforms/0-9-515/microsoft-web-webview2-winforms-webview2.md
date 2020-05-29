---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/27/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 532c898845125564ad5af6460dc8d1ff6464abfb
ms.sourcegitcommit: 83efa259be89cc773a82751242495a0a919d54cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2020
ms.locfileid: "10687803"
---
# <span data-ttu-id="7bcf4-104">Classe Microsoft. Web. WebView2. WinForms. WebView2</span><span class="sxs-lookup"><span data-stu-id="7bcf4-104">Microsoft.Web.WebView2.WinForms.WebView2 class</span></span> 

<span data-ttu-id="7bcf4-105">Espace de noms: Microsoft. Web. WebView2. WinForms </span><span class="sxs-lookup"><span data-stu-id="7bcf4-105">Namespace: Microsoft.Web.WebView2.WinForms</span></span>\
<span data-ttu-id="7bcf4-106">Assembly: Microsoft. Web. WebView2. WinForms. dll</span><span class="sxs-lookup"><span data-stu-id="7bcf4-106">Assembly: Microsoft.Web.WebView2.WinForms.dll</span></span>

```
class Microsoft.Web.WebView2.WinForms.WebView2
  : public Control
```

<span data-ttu-id="7bcf4-107">Ctrl pour incorporer WebView2 dans WinForms.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-107">Control to embed WebView2 in WinForms.</span></span>

## <span data-ttu-id="7bcf4-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="7bcf4-108">Summary</span></span>

 <span data-ttu-id="7bcf4-109">Ses</span><span class="sxs-lookup"><span data-stu-id="7bcf4-109">Members</span></span>                        | <span data-ttu-id="7bcf4-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="7bcf4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7bcf4-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="7bcf4-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="7bcf4-112">ContentLoading est distribué après le début d’une navigation sur un nouvel URI et le contenu de cet URI commence à être restitué.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-112">ContentLoading dispatches after a navigation begins to a new URI and the content of that URI begins to render.</span></span>
[<span data-ttu-id="7bcf4-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="7bcf4-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="7bcf4-114">Cet événement est déclenché lors de l’initialisation de l' [CoreWebView2](#corewebview2) du contrôle (quelle que soit l’origine du déclenchement de l’initialisation), mais avant qu’elle ne soit utilisée pour n’importe quelle opération.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-114">This event is triggered when the control's [CoreWebView2](#corewebview2) has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="7bcf4-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="7bcf4-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="7bcf4-116">NavigationCompleted Dispatches après qu’une navigation du document de niveau supérieur effectue un rendu correct ou non.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-116">NavigationCompleted dispatches after a navigate of the top level document completes rendering either successfully or not.</span></span>
[<span data-ttu-id="7bcf4-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="7bcf4-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="7bcf4-118">NavigationStarting dispatchs avant le début de la navigation dans le document de niveau supérieur de la WebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-118">NavigationStarting dispatches before a new navigate starts for the top level document of the WebView2.</span></span>
[<span data-ttu-id="7bcf4-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="7bcf4-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="7bcf4-120">SourceChanged dispatchs après modification de la propriété source.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-120">SourceChanged dispatches after the Source property changes.</span></span>
[<span data-ttu-id="7bcf4-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="7bcf4-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="7bcf4-122">WebMessageReceived de distribution de contenu Web permet d’envoyer un message à l’hôte de l’application par le biais de `chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="7bcf4-122">WebMessageReceived dispatches after web content sends a message to the app host via `chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="7bcf4-123">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="7bcf4-123">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="7bcf4-124">CoreWebView2 sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-124">The underlying CoreWebView2.</span></span>
[<span data-ttu-id="7bcf4-125">Source</span><span class="sxs-lookup"><span data-stu-id="7bcf4-125">Source</span></span>](#source) | <span data-ttu-id="7bcf4-126">La propriété source est l’URI du document de niveau supérieur du WebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-126">The Source property is the URI of the top level document of the WebView2.</span></span>
[<span data-ttu-id="7bcf4-127">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="7bcf4-127">ZoomFactor</span></span>](#zoomfactor) | <span data-ttu-id="7bcf4-128">Facteur de zoom pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-128">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="7bcf4-129">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="7bcf4-129">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="7bcf4-130">Retourne true si WebView peut accéder à une page précédente de l’historique de navigation via la méthode GoBack.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-130">Returns true if the webview can navigate to a previous page in the navigation history via the GoBack method.</span></span>
[<span data-ttu-id="7bcf4-131">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="7bcf4-131">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="7bcf4-132">Retourne true si WebView peut accéder à une page suivante de l’historique de navigation via la méthode GoForward.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-132">Returns true if the webview can navigate to a next page in the navigation history via the GoForward method.</span></span>
[<span data-ttu-id="7bcf4-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="7bcf4-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="7bcf4-134">Déclenchez explicitement l’initialisation de [CoreWebView2](#corewebview2)du contrôle.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-134">Explicitly trigger initialization of the control's [CoreWebView2](#corewebview2).</span></span>
[<span data-ttu-id="7bcf4-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="7bcf4-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="7bcf4-136">Exécute le script fourni dans le document de niveau supérieur du WebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-136">Executes the provided script in the top level document of the WebView2.</span></span>
[<span data-ttu-id="7bcf4-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="7bcf4-137">GoBack</span></span>](#goback) | <span data-ttu-id="7bcf4-138">Revenir à la page précédente de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-138">Navigate to the previous page in navigation history.</span></span>
[<span data-ttu-id="7bcf4-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="7bcf4-139">GoForward</span></span>](#goforward) | <span data-ttu-id="7bcf4-140">Accédez à la page suivante de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-140">Navigate to the next page in navigation history.</span></span>
[<span data-ttu-id="7bcf4-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="7bcf4-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="7bcf4-142">Affichez le code HTML fourni en tant que document de niveau supérieur du WebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-142">Render the provided HTML as the top level document of the WebView2.</span></span>
[<span data-ttu-id="7bcf4-143">Recharger</span><span class="sxs-lookup"><span data-stu-id="7bcf4-143">Reload</span></span>](#reload) | <span data-ttu-id="7bcf4-144">Rechargez le document de niveau supérieur du WebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-144">Reload the top level document of the WebView2.</span></span>
[<span data-ttu-id="7bcf4-145">Stop</span><span class="sxs-lookup"><span data-stu-id="7bcf4-145">Stop</span></span>](#stop) | <span data-ttu-id="7bcf4-146">Arrêtez la navigation en cours dans le WebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-146">Stop any in progress navigation in the WebView2.</span></span>
[<span data-ttu-id="7bcf4-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="7bcf4-147">WebView2</span></span>](#webview2) | <span data-ttu-id="7bcf4-148">Créer un contrôle WinForms WebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-148">Create a new WebView2 WinForms control.</span></span>

## <span data-ttu-id="7bcf4-149">Ses</span><span class="sxs-lookup"><span data-stu-id="7bcf4-149">Members</span></span>

#### <span data-ttu-id="7bcf4-150">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="7bcf4-150">ContentLoading</span></span> 

<span data-ttu-id="7bcf4-151">ContentLoading est distribué après le début d’une navigation sur un nouvel URI et le contenu de cet URI commence à être restitué.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-151">ContentLoading dispatches after a navigation begins to a new URI and the content of that URI begins to render.</span></span>

> <span data-ttu-id="7bcf4-152">événement public EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="7bcf4-152">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="7bcf4-153">Cela équivaut à l’événement ContentLoading sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-153">This is equivalent to the ContentLoading event on the CoreWebView2.</span></span> <span data-ttu-id="7bcf4-154">Pour plus d’informations, consultez la documentation CoreWebView2. ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-154">See CoreWebView2.ContentLoading documentation for more information.</span></span>

#### <span data-ttu-id="7bcf4-155">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="7bcf4-155">CoreWebView2Ready</span></span> 

<span data-ttu-id="7bcf4-156">Cet événement est déclenché lors de l’initialisation de l' [CoreWebView2](#corewebview2) du contrôle (quelle que soit l’origine du déclenchement de l’initialisation), mais avant qu’elle ne soit utilisée pour n’importe quelle opération.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-156">This event is triggered when the control's [CoreWebView2](#corewebview2) has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="7bcf4-157">événement public EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="7bcf4-157">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="7bcf4-158">Vous devez gérer cet événement si vous avez besoin d’effectuer des opérations d’installation ponctuelles sur le CoreWebView2 que vous voulez affecter à l’ensemble de ses utilisations (par exemple, ajout de gestionnaires d’événements, configuration des paramètres, installation de scripts de création de documents, ajout d’objets hôtes).</span><span class="sxs-lookup"><span data-stu-id="7bcf4-158">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span>

<span data-ttu-id="7bcf4-159">Cet événement ne fournit aucun argument et l’expéditeur sera le contrôle WebView2, dont la propriété CoreWebView2 sera désormais valide (c’est-à-dire non null) pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-159">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="7bcf4-160">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="7bcf4-160">NavigationCompleted</span></span> 

<span data-ttu-id="7bcf4-161">NavigationCompleted Dispatches après qu’une navigation du document de niveau supérieur effectue un rendu correct ou non.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-161">NavigationCompleted dispatches after a navigate of the top level document completes rendering either successfully or not.</span></span>

> <span data-ttu-id="7bcf4-162">événement public EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="7bcf4-162">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="7bcf4-163">Cela équivaut à l’événement NavigationCompleted sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-163">This is equivalent to the NavigationCompleted event on the CoreWebView2.</span></span> <span data-ttu-id="7bcf4-164">Pour plus d’informations, consultez la documentation CoreWebView2. NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-164">See CoreWebView2.NavigationCompleted documentation for more information.</span></span>

#### <span data-ttu-id="7bcf4-165">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="7bcf4-165">NavigationStarting</span></span> 

<span data-ttu-id="7bcf4-166">NavigationStarting dispatchs avant le début de la navigation dans le document de niveau supérieur de la WebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-166">NavigationStarting dispatches before a new navigate starts for the top level document of the WebView2.</span></span>

> <span data-ttu-id="7bcf4-167">événement public EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="7bcf4-167">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="7bcf4-168">Cela équivaut à l’événement NavigationStarting sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-168">This is equivalent to the NavigationStarting event on the CoreWebView2.</span></span> <span data-ttu-id="7bcf4-169">Pour plus d’informations, consultez la documentation CoreWebView2. NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-169">See CoreWebView2.NavigationStarting documentation for more information.</span></span>

#### <span data-ttu-id="7bcf4-170">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="7bcf4-170">SourceChanged</span></span> 

<span data-ttu-id="7bcf4-171">SourceChanged dispatchs après modification de la propriété source.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-171">SourceChanged dispatches after the Source property changes.</span></span>

> <span data-ttu-id="7bcf4-172">événement public EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="7bcf4-172">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="7bcf4-173">Cela se produit au cours d’une navigation ou, dans le cas contraire, le script de la page modifie l’URI du document.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-173">This may happen during a navigation or if otherwise the script in the page changes the URI of the document.</span></span> <span data-ttu-id="7bcf4-174">Cela équivaut à l’événement SourceChanged sur le CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-174">This is equivalent to the SourceChanged event on the CoreWebView2.</span></span> <span data-ttu-id="7bcf4-175">Pour plus d’informations, voir la documentation relative à CoreWebView2. SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-175">See CoreWebView2.SourceChanged documentation for more information.</span></span>

#### <span data-ttu-id="7bcf4-176">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="7bcf4-176">WebMessageReceived</span></span> 

<span data-ttu-id="7bcf4-177">WebMessageReceived de distribution de contenu Web permet d’envoyer un message à l’hôte de l’application par le biais de `chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="7bcf4-177">WebMessageReceived dispatches after web content sends a message to the app host via `chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="7bcf4-178">événement public EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="7bcf4-178">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="7bcf4-179">Cela équivaut à l’événement WebMessageReceived sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-179">This is equivalent to the WebMessageReceived event on the CoreWebView2.</span></span> <span data-ttu-id="7bcf4-180">Pour plus d’informations, consultez la documentation CoreWebView2. WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-180">See CoreWebView2.WebMessageReceived documentation for more information.</span></span>

#### <span data-ttu-id="7bcf4-181">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="7bcf4-181">CoreWebView2</span></span> 

<span data-ttu-id="7bcf4-182">CoreWebView2 sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-182">The underlying CoreWebView2.</span></span>

> <span data-ttu-id="7bcf4-183">public CoreWebView2 [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="7bcf4-183">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="7bcf4-184">Utilisez cette propriété pour effectuer davantage d’opérations sur le contenu WebView2 que ce qui est exposé sur le WebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-184">Use this property to perform more operations on the WebView2 content than is exposed on the WebView2.</span></span> <span data-ttu-id="7bcf4-185">Cette valeur est null jusqu’à ce qu’elle soit initialisée.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-185">This value is null until it is initialized.</span></span> <span data-ttu-id="7bcf4-186">Vous pouvez forcer l’initialisation du CoreWebView2 sous-jacent via la méthode InitializeAsync.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-186">You can force the underlying CoreWebView2 to initialize via the InitializeAsync method.</span></span>

#### <span data-ttu-id="7bcf4-187">Source</span><span class="sxs-lookup"><span data-stu-id="7bcf4-187">Source</span></span> 

<span data-ttu-id="7bcf4-188">La propriété source est l’URI du document de niveau supérieur du WebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-188">The Source property is the URI of the top level document of the WebView2.</span></span>

> <span data-ttu-id="7bcf4-189">[source](#source) URI publique</span><span class="sxs-lookup"><span data-stu-id="7bcf4-189">public Uri [Source](#source)</span></span>

<span data-ttu-id="7bcf4-190">Le fait de définir la source est l’équivalent d’appeler CoreWebView2. Navigate.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-190">Setting the Source is equivalent to calling CoreWebView2.Navigate.</span></span> <span data-ttu-id="7bcf4-191">Si l’CoreWebView2 sous-jacent n’est pas encore initialisé, il s’agit de la propriété «about: Blank».</span><span class="sxs-lookup"><span data-stu-id="7bcf4-191">If the underlying CoreWebView2 is not yet initialized, this property is "about:blank".</span></span> <span data-ttu-id="7bcf4-192">Si la propriété est définie sur un URI non absolu ou null, la propriété reste inchangée.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-192">If the property is set to a non-absolute URI or null, the property remains unchanged.</span></span> <span data-ttu-id="7bcf4-193">Pour plus d’informations, voir CoreWebView2. Navigate.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-193">See CoreWebView2.Navigate documentation for more information.</span></span>

#### <span data-ttu-id="7bcf4-194">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="7bcf4-194">ZoomFactor</span></span> 

<span data-ttu-id="7bcf4-195">Facteur de zoom pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-195">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="7bcf4-196">double [ZoomFactor](#zoomfactor) public</span><span class="sxs-lookup"><span data-stu-id="7bcf4-196">public double [ZoomFactor](#zoomfactor)</span></span>

#### <span data-ttu-id="7bcf4-197">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="7bcf4-197">CanGoBack</span></span> 

<span data-ttu-id="7bcf4-198">Retourne true si WebView peut accéder à une page précédente de l’historique de navigation via la méthode GoBack.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-198">Returns true if the webview can navigate to a previous page in the navigation history via the GoBack method.</span></span>

> <span data-ttu-id="7bcf4-199">public bool [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="7bcf4-199">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="7bcf4-200">Cela équivaut à la propriété CanGoBack sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-200">This is equivalent to the CanGoBack property on the CoreWebView2.</span></span> <span data-ttu-id="7bcf4-201">Si l’CoreWebView2 sous-jacent n’est pas encore initialisé, cette propriété a la valeur false.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-201">If the underlying CoreWebView2 is not yet initialized, this property is false.</span></span> <span data-ttu-id="7bcf4-202">Pour plus d’informations, consultez la documentation CoreWebView2. CanGoBack.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-202">See CoreWebView2.CanGoBack documentation for more information.</span></span>

#### <span data-ttu-id="7bcf4-203">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="7bcf4-203">CanGoForward</span></span> 

<span data-ttu-id="7bcf4-204">Retourne true si WebView peut accéder à une page suivante de l’historique de navigation via la méthode GoForward.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-204">Returns true if the webview can navigate to a next page in the navigation history via the GoForward method.</span></span>

> <span data-ttu-id="7bcf4-205">public bool [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="7bcf4-205">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="7bcf4-206">Cela équivaut à la propriété CanGoForward sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-206">This is equivalent to the CanGoForward property on the CoreWebView2.</span></span> <span data-ttu-id="7bcf4-207">Si l’CoreWebView2 sous-jacent n’est pas encore initialisé, cette propriété a la valeur false.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-207">If the underlying CoreWebView2 is not yet initialized, this property is false.</span></span> <span data-ttu-id="7bcf4-208">Pour plus d’informations, consultez la documentation CoreWebView2. CanGoForward.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-208">See CoreWebView2.CanGoForward documentation for more information.</span></span>

#### <span data-ttu-id="7bcf4-209">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="7bcf4-209">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="7bcf4-210">Déclenchez explicitement l’initialisation de [CoreWebView2](#corewebview2)du contrôle.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-210">Explicitly trigger initialization of the control's [CoreWebView2](#corewebview2).</span></span>

> <span data-ttu-id="7bcf4-211">[EnsureCoreWebView2Async](#ensurecorewebview2async)de tâches publiques (environnement CoreWebView2Environment)</span><span class="sxs-lookup"><span data-stu-id="7bcf4-211">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

##### <span data-ttu-id="7bcf4-212">Parameters</span><span class="sxs-lookup"><span data-stu-id="7bcf4-212">Parameters</span></span>
* `environment` <span data-ttu-id="7bcf4-213">CoreWebView2Environment précréé qui doit être utilisé pour créer le CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-213">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="7bcf4-214">La création de votre propre environnement vous donne le contrôle de plusieurs options qui affectent la manière dont CoreWebView2 est initialisé.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-214">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="7bcf4-215">Si vous passez la valeur null (valeur par défaut), un environnement par défaut sera créé et utilisé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-215">If you pass null (the default value) then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="7bcf4-216">Renvoie</span><span class="sxs-lookup"><span data-stu-id="7bcf4-216">Returns</span></span>
<span data-ttu-id="7bcf4-217">Tâche qui représente le processus d’initialisation en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-217">A Task that represents the background initialization process.</span></span> <span data-ttu-id="7bcf4-218">Lorsque la tâche se termine, la propriété CoreWebView2 peut être utilisée (c’est-à-dire non null).</span><span class="sxs-lookup"><span data-stu-id="7bcf4-218">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="7bcf4-219">Notez que l’événement [CoreWebView2Ready](#corewebview2ready) du contrôle est appelé avant la fin de la tâche.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-219">Note that the control's [CoreWebView2Ready](#corewebview2ready) event will be invoked before the task completes.</span></span> 

<span data-ttu-id="7bcf4-220">L’appel de cette méthode pour les autres temps n’aura aucun effet (l’environnement spécifié est ignoré) et renvoie la même tâche que le premier appel.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-220">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="7bcf4-221">L’appel de cette méthode une fois l’initialisation déclenchée implicitement, la définition de la propriété [source](#source) n’aura aucun effet (aucun environnement spécifié n’est ignoré) et renvoyez simplement une tâche représentant cette initialisation déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-221">Calling this method after initialization has been implicitly triggered by setting the [Source](#source) property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> 

##### <span data-ttu-id="7bcf4-222">Exceptions</span><span class="sxs-lookup"><span data-stu-id="7bcf4-222">Exceptions</span></span>
* `System.InvalidOperationException` <span data-ttu-id="7bcf4-223">Levée en cas d’appel à partir d’un thread sans interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-223">Thrown when invoked from non-UI thread.</span></span>

#### <span data-ttu-id="7bcf4-224">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="7bcf4-224">ExecuteScriptAsync</span></span> 

<span data-ttu-id="7bcf4-225">Exécute le script fourni dans le document de niveau supérieur du WebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-225">Executes the provided script in the top level document of the WebView2.</span></span>

> <span data-ttu-id="7bcf4-226">Tâche asynchrone publique< chaîne > [ExecuteScriptAsync](#executescriptasync)(script de chaîne)</span><span class="sxs-lookup"><span data-stu-id="7bcf4-226">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string script)</span></span>

<span data-ttu-id="7bcf4-227">Cela équivaut à la méthode ExecuteScriptAsync sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-227">This is equivalent to the ExecuteScriptAsync method on the CoreWebView2.</span></span> <span data-ttu-id="7bcf4-228">Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode lève une exception InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-228">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="7bcf4-229">Pour plus d’informations, consultez la documentation CoreWebView2. ExecuteScriptAsync.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-229">See CoreWebView2.ExecuteScriptAsync documentation for more information.</span></span>

#### <span data-ttu-id="7bcf4-230">GoBack</span><span class="sxs-lookup"><span data-stu-id="7bcf4-230">GoBack</span></span> 

<span data-ttu-id="7bcf4-231">Revenir à la page précédente de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-231">Navigate to the previous page in navigation history.</span></span>

> <span data-ttu-id="7bcf4-232">public void [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="7bcf4-232">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="7bcf4-233">Cela équivaut à la méthode GoBack sur le CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-233">This is equivalent to the GoBack method on the CoreWebView2.</span></span> <span data-ttu-id="7bcf4-234">Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-234">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="7bcf4-235">Pour plus d’informations, voir la documentation CoreWebView2. GoBack.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-235">See CoreWebView2.GoBack documentation for more information.</span></span>

#### <span data-ttu-id="7bcf4-236">GoForward</span><span class="sxs-lookup"><span data-stu-id="7bcf4-236">GoForward</span></span> 

<span data-ttu-id="7bcf4-237">Accédez à la page suivante de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-237">Navigate to the next page in navigation history.</span></span>

> <span data-ttu-id="7bcf4-238">public void [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="7bcf4-238">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="7bcf4-239">Cela équivaut à la méthode GoForward sur le CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-239">This is equivalent to the GoForward method on the CoreWebView2.</span></span> <span data-ttu-id="7bcf4-240">Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-240">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="7bcf4-241">Pour plus d’informations, voir la documentation CoreWebView2. GoForward.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-241">See CoreWebView2.GoForward documentation for more information.</span></span>

#### <span data-ttu-id="7bcf4-242">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="7bcf4-242">NavigateToString</span></span> 

<span data-ttu-id="7bcf4-243">Affichez le code HTML fourni en tant que document de niveau supérieur du WebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-243">Render the provided HTML as the top level document of the WebView2.</span></span>

> <span data-ttu-id="7bcf4-244">public void [NavigateToString](#navigatetostring)(chaîne htmlContent)</span><span class="sxs-lookup"><span data-stu-id="7bcf4-244">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="7bcf4-245">Cela équivaut à la méthode NavigateToString sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-245">This is equivalent to the NavigateToString method on the CoreWebView2.</span></span> <span data-ttu-id="7bcf4-246">Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode lève une exception InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-246">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="7bcf4-247">Pour plus d’informations, consultez la documentation CoreWebView2. NavigateToString.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-247">See CoreWebView2.NavigateToString documentation for more information.</span></span>

#### <span data-ttu-id="7bcf4-248">Recharger</span><span class="sxs-lookup"><span data-stu-id="7bcf4-248">Reload</span></span> 

<span data-ttu-id="7bcf4-249">Rechargez le document de niveau supérieur du WebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-249">Reload the top level document of the WebView2.</span></span>

> <span data-ttu-id="7bcf4-250">[rechargement](#reload)d’annulation publique ()</span><span class="sxs-lookup"><span data-stu-id="7bcf4-250">public void [Reload](#reload)()</span></span>

<span data-ttu-id="7bcf4-251">Cela équivaut à la méthode reload sur le CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-251">This is equivalent to the Reload method on the CoreWebView2.</span></span> <span data-ttu-id="7bcf4-252">Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode lève une exception InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-252">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="7bcf4-253">Pour plus d’informations, voir CoreWebView2. Reload documentation.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-253">See CoreWebView2.Reload documentation for more information.</span></span>

#### <span data-ttu-id="7bcf4-254">Stop</span><span class="sxs-lookup"><span data-stu-id="7bcf4-254">Stop</span></span> 

<span data-ttu-id="7bcf4-255">Arrêtez la navigation en cours dans le WebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-255">Stop any in progress navigation in the WebView2.</span></span>

> <span data-ttu-id="7bcf4-256">public void [Stop](#stop)()</span><span class="sxs-lookup"><span data-stu-id="7bcf4-256">public void [Stop](#stop)()</span></span>

<span data-ttu-id="7bcf4-257">Cela équivaut à la méthode Stop sur le CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-257">This is equivalent to the Stop method on the CoreWebView2.</span></span> <span data-ttu-id="7bcf4-258">Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-258">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="7bcf4-259">Pour plus d’informations, voir la documentation CoreWebView2. Stop.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-259">See CoreWebView2.Stop documentation for more information.</span></span>

#### <span data-ttu-id="7bcf4-260">WebView2</span><span class="sxs-lookup"><span data-stu-id="7bcf4-260">WebView2</span></span> 

<span data-ttu-id="7bcf4-261">Créer un contrôle WinForms WebView2.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-261">Create a new WebView2 WinForms control.</span></span>

> <span data-ttu-id="7bcf4-262">public [WebView2](#webview2)()</span><span class="sxs-lookup"><span data-stu-id="7bcf4-262">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="7bcf4-263">Après construction, la propriété CoreWebView2 a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-263">After construction the CoreWebView2 property is null.</span></span> <span data-ttu-id="7bcf4-264">Appelez [EnsureCoreWebView2Async](#ensurecorewebview2async) pour initialiser la CoreWebView2 sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-264">Call [EnsureCoreWebView2Async](#ensurecorewebview2async) to initialize the underlying CoreWebView2.</span></span>

