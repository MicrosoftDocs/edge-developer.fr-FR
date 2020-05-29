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
ms.openlocfilehash: a0030e1a2a77d65963bd8333f2071485ab2fe308
ms.sourcegitcommit: 83efa259be89cc773a82751242495a0a919d54cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2020
ms.locfileid: "10687796"
---
# <span data-ttu-id="30903-104">Classe Microsoft. Web. WebView2. WPF. WebView2</span><span class="sxs-lookup"><span data-stu-id="30903-104">Microsoft.Web.WebView2.Wpf.WebView2 class</span></span> 

<span data-ttu-id="30903-105">Espace de noms: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="30903-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="30903-106">Assembly: Microsoft. Web. WebView2. WPF. dll</span><span class="sxs-lookup"><span data-stu-id="30903-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.WebView2
  : public HwndHost
```

<span data-ttu-id="30903-107">Contrôle pour incorporer du contenu Web dans une application WPF.</span><span class="sxs-lookup"><span data-stu-id="30903-107">A control to embed web content in a WPF application.</span></span>

## <span data-ttu-id="30903-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="30903-108">Summary</span></span>

 <span data-ttu-id="30903-109">Ses</span><span class="sxs-lookup"><span data-stu-id="30903-109">Members</span></span>                        | <span data-ttu-id="30903-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="30903-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="30903-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="30903-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="30903-112">Wrapper de l’événement CoreWebView2. ContentLoading de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-112">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>
[<span data-ttu-id="30903-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="30903-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="30903-114">Cet événement est déclenché lors de l’initialisation de l’CoreWebView2 du contrôle (quelle que soit l’origine du déclenchement de l’initialisation), mais avant qu’elle ne soit utilisée pour n’importe quelle opération.</span><span class="sxs-lookup"><span data-stu-id="30903-114">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="30903-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="30903-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="30903-116">Wrapper de l’événement CoreWebView2. NavigationCompleted de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-116">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>
[<span data-ttu-id="30903-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="30903-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="30903-118">Wrapper de l’événement CoreWebView2. NavigationStarting de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-118">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>
[<span data-ttu-id="30903-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="30903-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="30903-120">Wrapper entourant l’événement CoreWebView2. SourceChanged de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-120">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>
[<span data-ttu-id="30903-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="30903-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="30903-122">Wrapper de l’événement CoreWebView2. WebMessageReceived de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-122">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>
[<span data-ttu-id="30903-123">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="30903-123">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="30903-124">Renvoie vrai si le WebView peut accéder à une page précédente de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="30903-124">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="30903-125">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="30903-125">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="30903-126">Cette fonction renvoie la valeur vrai si le WebView peut accéder à une page suivante de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="30903-126">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="30903-127">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="30903-127">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="30903-128">Accédez à l’ensemble des fonctionnalités de l’API COM Core. CoreWebView2 sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="30903-128">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>
[<span data-ttu-id="30903-129">CreationProperties</span><span class="sxs-lookup"><span data-stu-id="30903-129">CreationProperties</span></span>](#creationproperties) | <span data-ttu-id="30903-130">Obtient ou définit un sac d’options qui sont utilisées lors de l’initialisation de la CoreWebView2 du contrôle.</span><span class="sxs-lookup"><span data-stu-id="30903-130">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="30903-131">Source</span><span class="sxs-lookup"><span data-stu-id="30903-131">Source</span></span>](#source) | <span data-ttu-id="30903-132">L’URI de niveau supérieur sur lequel est actuellement affiché le WebView (ou s’affichera une fois l’initialisation de son CoreWebView2 terminée).</span><span class="sxs-lookup"><span data-stu-id="30903-132">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>
[<span data-ttu-id="30903-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="30903-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="30903-134">Déclenchez explicitement l’initialisation de CoreWebView2 du contrôle.</span><span class="sxs-lookup"><span data-stu-id="30903-134">Explicitly trigger initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="30903-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="30903-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="30903-136">Exécute le code JavaScript du paramètre javaScript du document de niveau supérieur actuel affiché dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="30903-136">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="30903-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="30903-137">GoBack</span></span>](#goback) | <span data-ttu-id="30903-138">Permet d’accéder à la page précédente de l’historique de navigation via le WebView.</span><span class="sxs-lookup"><span data-stu-id="30903-138">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="30903-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="30903-139">GoForward</span></span>](#goforward) | <span data-ttu-id="30903-140">Navigue vers la page suivante de l’historique de navigation du WebView.</span><span class="sxs-lookup"><span data-stu-id="30903-140">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="30903-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="30903-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="30903-142">Lance une navigation vers htmlContent en tant que code HTML source d’un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="30903-142">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="30903-143">Recharger</span><span class="sxs-lookup"><span data-stu-id="30903-143">Reload</span></span>](#reload) | <span data-ttu-id="30903-144">Recharge la page active.</span><span class="sxs-lookup"><span data-stu-id="30903-144">Reloads the current page.</span></span>
[<span data-ttu-id="30903-145">Stop</span><span class="sxs-lookup"><span data-stu-id="30903-145">Stop</span></span>](#stop) | <span data-ttu-id="30903-146">Arrête toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="30903-146">Stops all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="30903-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="30903-147">WebView2</span></span>](#webview2) | <span data-ttu-id="30903-148">Crée une nouvelle instance d’un contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-148">Creates a new instance of a WebView2 control.</span></span>

<span data-ttu-id="30903-149">Ce contrôle est en réalité un wrapper qui entoure l’API COM WebView2, qui vous trouverez de la documentation pour cet emplacement: [https://aka.ms/webview2](https://aka.ms/webview2) vous pouvez accéder directement à l’interface ICoreWebView2 sous-jacente et à toutes ses fonctionnalités en accédant à la propriété CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-149">This control is effectively a wrapper around the WebView2 COM API, which you can find documentation for here: [https://aka.ms/webview2](https://aka.ms/webview2) You can directly access the underlying ICoreWebView2 interface and all of its functionality by accessing the CoreWebView2 property.</span></span> <span data-ttu-id="30903-150">Certaines des fonctionnalités COM les plus courantes sont également accessibles directement via les méthodes d’encapsulation/propriétés/événements du contrôle.</span><span class="sxs-lookup"><span data-stu-id="30903-150">Some of the most common COM functionality is also accessible directly through wrapper methods/properties/events on the control.</span></span>

<span data-ttu-id="30903-151">Lors de la création, la propriété CoreWebView2 du contrôle est null.</span><span class="sxs-lookup"><span data-stu-id="30903-151">Upon creation, the control's CoreWebView2 property will be null.</span></span> <span data-ttu-id="30903-152">En effet, la création de CoreWebView2 est une opération onéreuse qui implique des opérations comme le lancement de processus de navigateur Edge.</span><span class="sxs-lookup"><span data-stu-id="30903-152">This is because creating the CoreWebView2 is an expensive operation which involves things like launching Edge browser processes.</span></span> <span data-ttu-id="30903-153">Il existe deux façons d’entraîner la création du CoreWebView2:1) appeler la méthode EnsureCoreWebView2Async.</span><span class="sxs-lookup"><span data-stu-id="30903-153">There are two ways to cause the CoreWebView2 to be created: 1) Call the EnsureCoreWebView2Async method.</span></span> <span data-ttu-id="30903-154">On parle d’initialisation explicite.</span><span class="sxs-lookup"><span data-stu-id="30903-154">This is referred to as explicit initialization.</span></span> <span data-ttu-id="30903-155">2) définissez la propriété source (qui peut être exécutée à partir du balisage, par exemple).</span><span class="sxs-lookup"><span data-stu-id="30903-155">2) Set the Source property (which could be done from markup, for example).</span></span> <span data-ttu-id="30903-156">On parle d’initialisation implicite.</span><span class="sxs-lookup"><span data-stu-id="30903-156">This is referred to as implicit initialization.</span></span> <span data-ttu-id="30903-157">L’une des deux options commencera l’initialisation en arrière-plan et renverra l’appelant sans attendre la fin de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="30903-157">Either option will start initialization in the background and return back to the caller without waiting for it to finish.</span></span> <span data-ttu-id="30903-158">Pour spécifier des options concernant le processus d’initialisation, transmettez votre propre CoreWebView2Environment à EnsureCoreWebView2Async ou définissez la propriété CreationProperties du contrôle avant l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="30903-158">To specify options regarding the initialization process, either pass your own CoreWebView2Environment to EnsureCoreWebView2Async or set the control's CreationProperties property prior to initialization.</span></span>

<span data-ttu-id="30903-159">Une fois l’initialisation terminée (quel que soit le mode de déclenchement), les éléments suivants se produisent, dans l’ordre suivant: 1) l’événement CoreWebView2Ready du contrôle est appelé.</span><span class="sxs-lookup"><span data-stu-id="30903-159">When initialization has finished (regardless of how it was triggered) then the following things will occur, in this order: 1) The control's CoreWebView2Ready event will be invoked.</span></span> <span data-ttu-id="30903-160">Si vous devez effectuer une opération de configuration ponctuelle sur le CoreWebView2 avant de l’utiliser, vous devez le faire dans un gestionnaire pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="30903-160">If you need to perform one time setup operations on the CoreWebView2 prior to its use then you should do so in a handler for that event.</span></span> <span data-ttu-id="30903-161">2) si un URI a été défini pour la propriété source, le contrôle commencera à y accéder en arrière-plan (c’est-à-dire, ces étapes continuent sans attendre la fin de la navigation).</span><span class="sxs-lookup"><span data-stu-id="30903-161">2) If a Uri has been set to the Source property then the control will start navigating to it in the background (i.e. these steps will continue without waiting for the navigation to finish).</span></span> <span data-ttu-id="30903-162">3) la tâche renvoyée par EnsureCoreWebView2Async sera terminée.</span><span class="sxs-lookup"><span data-stu-id="30903-162">3) The Task returned from EnsureCoreWebView2Async will complete.</span></span>

<span data-ttu-id="30903-163">Pour plus d’informations sur les méthodes/propriétés/événements impliqués dans le processus d’initialisation, voir sa documentation spécifique.</span><span class="sxs-lookup"><span data-stu-id="30903-163">For more details about any of the methods/properties/events involved in the initialization process, see its specific documentation.</span></span>

<span data-ttu-id="30903-164">Dans la mesure où le contrôle CoreWebView2 est un objet très haute densité (qui peut être responsable de plusieurs processus en cours d’exécution et de mégaoctets d’espace disque), le contrôle implémente IDisposable pour fournir un moyen explicite de le libérer.</span><span class="sxs-lookup"><span data-stu-id="30903-164">Because the control's CoreWebView2 is a very heavyweight object (potentially responsible for multiple running processes and megabytes of disk space) the control implements IDisposable to provide an explicit means to free it.</span></span> <span data-ttu-id="30903-165">L’appel de dispose va libérer le CoreWebView2 et ses ressources sous-jacentes (sauf s’ils sont également utilisés par d’autres WebViews) et réinitialiser CoreWebView2 sur null.</span><span class="sxs-lookup"><span data-stu-id="30903-165">Calling Dispose will release the CoreWebView2 and its underlying resources (except any that are also being used by other WebViews), and reset CoreWebView2 to null.</span></span> <span data-ttu-id="30903-166">Après avoir appelé la méthode CoreWebView2 ne peut pas être réinitialisée, et toute tentative d’utilisation de la fonctionnalité qui nécessite qu’elle lèvera une opération ObjectDisposedException.</span><span class="sxs-lookup"><span data-stu-id="30903-166">After Dispose has been called the CoreWebView2 cannot be re-initialized, and any attempt to use functionality which requires it will throw an ObjectDisposedException.</span></span>

<span data-ttu-id="30903-167">Notez que ce contrôle étend HwndHost afin d’incorporer des fenêtres qui résident en dehors de l’écosystème WPF.</span><span class="sxs-lookup"><span data-stu-id="30903-167">Note that this control extends HwndHost in order to embed windows which live outside of the WPF ecosystem.</span></span> <span data-ttu-id="30903-168">Cela a quelques implications sur le comportement de l’entrée et de la sortie du contrôle, ainsi que sur les fonctionnalités qu’il hérite de l’élément UIElement et de FrameworkElement.</span><span class="sxs-lookup"><span data-stu-id="30903-168">This has some implications regarding the control's input and output behavior as well as the functionality it "inherits" from UIElement and FrameworkElement.</span></span> <span data-ttu-id="30903-169">Pour plus d’informations, consultez la documentation sur l’interopérabilité HwndHost et WPF/Win32.</span><span class="sxs-lookup"><span data-stu-id="30903-169">See the HwndHost and WPF/Win32 interop documentation for more info:</span></span>

* [https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost](https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost)

* [https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf](https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf)

## <span data-ttu-id="30903-170">Ses</span><span class="sxs-lookup"><span data-stu-id="30903-170">Members</span></span>

#### <span data-ttu-id="30903-171">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="30903-171">ContentLoading</span></span> 

<span data-ttu-id="30903-172">Wrapper de l’événement CoreWebView2. ContentLoading de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-172">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>

> <span data-ttu-id="30903-173">événement public EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="30903-173">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="30903-174">La seule différence entre cet événement et CoreWebView2. ContentLoading est le premier paramètre passé aux gestionnaires.</span><span class="sxs-lookup"><span data-stu-id="30903-174">The only difference between this event and CoreWebView2.ContentLoading is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="30903-175">Le gestionnaire de cet événement reçoit le contrôle WebView2, alors que les gestionnaires de CoreWebView2. ContentLoading recevront l’instance CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-175">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.ContentLoading will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="30903-176">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="30903-176">CoreWebView2Ready</span></span> 

<span data-ttu-id="30903-177">Cet événement est déclenché lors de l’initialisation de l’CoreWebView2 du contrôle (quelle que soit l’origine du déclenchement de l’initialisation), mais avant qu’elle ne soit utilisée pour n’importe quelle opération.</span><span class="sxs-lookup"><span data-stu-id="30903-177">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="30903-178">événement public EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="30903-178">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="30903-179">Vous devez gérer cet événement si vous avez besoin d’effectuer des opérations d’installation ponctuelles sur le CoreWebView2 que vous voulez affecter à l’ensemble de ses utilisations (par exemple, ajout de gestionnaires d’événements, configuration des paramètres, installation de scripts de création de documents, ajout d’objets hôtes).</span><span class="sxs-lookup"><span data-stu-id="30903-179">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span> <span data-ttu-id="30903-180">Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-180">See the WebView2 class documentation for an initialization overview.</span></span>

<span data-ttu-id="30903-181">Cet événement ne fournit aucun argument et l’expéditeur sera le contrôle WebView2, dont la propriété CoreWebView2 sera désormais valide (c’est-à-dire non null) pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="30903-181">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="30903-182">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="30903-182">NavigationCompleted</span></span> 

<span data-ttu-id="30903-183">Wrapper de l’événement CoreWebView2. NavigationCompleted de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-183">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>

> <span data-ttu-id="30903-184">événement public EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="30903-184">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="30903-185">La seule différence entre cet événement et CoreWebView2. NavigationCompleted est le premier paramètre passé aux gestionnaires.</span><span class="sxs-lookup"><span data-stu-id="30903-185">The only difference between this event and CoreWebView2.NavigationCompleted is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="30903-186">Le gestionnaire de cet événement reçoit le contrôle WebView2, alors que les gestionnaires de CoreWebView2. NavigationCompleted recevront l’instance CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-186">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationCompleted will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="30903-187">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="30903-187">NavigationStarting</span></span> 

<span data-ttu-id="30903-188">Wrapper de l’événement CoreWebView2. NavigationStarting de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-188">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>

> <span data-ttu-id="30903-189">événement public EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="30903-189">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="30903-190">La seule différence entre cet événement et CoreWebView2. NavigationStarting est le premier paramètre passé aux gestionnaires.</span><span class="sxs-lookup"><span data-stu-id="30903-190">The only difference between this event and CoreWebView2.NavigationStarting is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="30903-191">Le gestionnaire de cet événement reçoit le contrôle WebView2, alors que les gestionnaires de CoreWebView2. NavigationStarting recevront l’instance CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-191">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationStarting will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="30903-192">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="30903-192">SourceChanged</span></span> 

<span data-ttu-id="30903-193">Wrapper entourant l’événement CoreWebView2. SourceChanged de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-193">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>

> <span data-ttu-id="30903-194">événement public EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="30903-194">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="30903-195">La seule différence entre cet événement et CoreWebView2. SourceChanged est le premier paramètre passé aux gestionnaires.</span><span class="sxs-lookup"><span data-stu-id="30903-195">The only difference between this event and CoreWebView2.SourceChanged is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="30903-196">Le gestionnaire de cet événement reçoit le contrôle WebView2, alors que les gestionnaires de CoreWebView2. SourceChanged reçoivent l’instance CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-196">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.SourceChanged will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="30903-197">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="30903-197">WebMessageReceived</span></span> 

<span data-ttu-id="30903-198">Wrapper de l’événement CoreWebView2. WebMessageReceived de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-198">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>

> <span data-ttu-id="30903-199">événement public EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="30903-199">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="30903-200">La seule différence entre cet événement et CoreWebView2. WebMessageReceived est le premier paramètre passé aux gestionnaires.</span><span class="sxs-lookup"><span data-stu-id="30903-200">The only difference between this event and CoreWebView2.WebMessageReceived is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="30903-201">Le gestionnaire de cet événement reçoit le contrôle WebView2, alors que les gestionnaires de CoreWebView2. WebMessageReceived recevront l’instance CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-201">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.WebMessageReceived will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="30903-202">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="30903-202">CanGoBack</span></span> 

<span data-ttu-id="30903-203">Renvoie vrai si le WebView peut accéder à une page précédente de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="30903-203">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="30903-204">public bool [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="30903-204">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="30903-205">Wrapper dans la propriété CoreWebView2. CanGoBack de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-205">Wrapper around the CoreWebView2.CanGoBack property of CoreWebView2.</span></span> <span data-ttu-id="30903-206">Si CoreWebView2 n’est pas initialisé, retourne false.</span><span class="sxs-lookup"><span data-stu-id="30903-206">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="30903-207">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="30903-207">CanGoForward</span></span> 

<span data-ttu-id="30903-208">Cette fonction renvoie la valeur vrai si le WebView peut accéder à une page suivante de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="30903-208">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="30903-209">public bool [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="30903-209">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="30903-210">Wrapper dans la propriété CoreWebView2. CanGoForward de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-210">Wrapper around the CoreWebView2.CanGoForward property of CoreWebView2.</span></span> <span data-ttu-id="30903-211">Si CoreWebView2 n’est pas initialisé, retourne false.</span><span class="sxs-lookup"><span data-stu-id="30903-211">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="30903-212">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="30903-212">CoreWebView2</span></span> 

<span data-ttu-id="30903-213">Accédez à l’ensemble des fonctionnalités de l’API COM Core. CoreWebView2 sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="30903-213">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>

> <span data-ttu-id="30903-214">public CoreWebView2 [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="30903-214">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="30903-215">Retourne la valeur null jusqu’à la fin de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="30903-215">Returns null until initialization has completed.</span></span> <span data-ttu-id="30903-216">Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-216">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="30903-217">Exceptions</span><span class="sxs-lookup"><span data-stu-id="30903-217">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="30903-218">Levée si le thread appelant n’est pas le thread qui a créé cet objet (généralement le thread d’interface utilisateur).</span><span class="sxs-lookup"><span data-stu-id="30903-218">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="30903-219">Pour plus d’informations, voir DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="30903-219">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="30903-220">Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="30903-220">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="30903-221">CreationProperties</span><span class="sxs-lookup"><span data-stu-id="30903-221">CreationProperties</span></span> 

<span data-ttu-id="30903-222">Obtient ou définit un sac d’options qui sont utilisées lors de l’initialisation de la CoreWebView2 du contrôle.</span><span class="sxs-lookup"><span data-stu-id="30903-222">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="30903-223">public CoreWebView2CreationProperties [CreationProperties](#creationproperties)</span><span class="sxs-lookup"><span data-stu-id="30903-223">public CoreWebView2CreationProperties [CreationProperties](#creationproperties)</span></span>

<span data-ttu-id="30903-224">La définition de cette propriété ne fonctionnera pas une fois l’initialisation du CoreWebView2 du contrôle démarrée (l’ancienne valeur sera conservée).</span><span class="sxs-lookup"><span data-stu-id="30903-224">Setting this property won't work after initialization of the control's CoreWebView2 has started (the old value will be retained).</span></span> <span data-ttu-id="30903-225">Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-225">See the WebView2 class documentation for an initialization overview.</span></span>

#### <span data-ttu-id="30903-226">Source</span><span class="sxs-lookup"><span data-stu-id="30903-226">Source</span></span> 

<span data-ttu-id="30903-227">L’URI de niveau supérieur sur lequel est actuellement affiché le WebView (ou s’affichera une fois l’initialisation de son CoreWebView2 terminée).</span><span class="sxs-lookup"><span data-stu-id="30903-227">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>

> <span data-ttu-id="30903-228">[source](#source) URI publique</span><span class="sxs-lookup"><span data-stu-id="30903-228">public Uri [Source](#source)</span></span>

<span data-ttu-id="30903-229">En règle générale, l’accès à cette propriété est équivalent à l’utilisation de la propriété CoreWebView2. source de CoreWebView2 et la définition de cette propriété revient à appeler la méthode CoreWebView2. Navigate sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-229">Generally speaking, getting this property is equivalent to getting the CoreWebView2.Source property of CoreWebView2 and setting this property is equivalent to calling the CoreWebView2.Navigate method on CoreWebView2.</span></span> <span data-ttu-id="30903-230">L’accès à cette propriété avant l’initialisation de CoreWebView2 permet de récupérer le dernier URI qui a été défini.</span><span class="sxs-lookup"><span data-stu-id="30903-230">Getting this property before the CoreWebView2 has been initialized will retrieve the last Uri which was set to it.</span></span> <span data-ttu-id="30903-231">Le fait de définir cette propriété avant l’initialisation de CoreWebView2 entraînera le démarrage de l’initialisation en arrière-plan (si ce n’est pas déjà fait), après lequel WebView2 accède à l’URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="30903-231">Setting this property before the CoreWebView2 has been initialized will cause initialization to start in the background (if not already in progress), after which the WebView2 will navigate to the specified Uri.</span></span> <span data-ttu-id="30903-232">Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-232">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="30903-233">Exceptions</span><span class="sxs-lookup"><span data-stu-id="30903-233">Exceptions</span></span>
* `ObjectDisposedException` <span data-ttu-id="30903-234">Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="30903-234">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="30903-235">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="30903-235">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="30903-236">Déclenchez explicitement l’initialisation de CoreWebView2 du contrôle.</span><span class="sxs-lookup"><span data-stu-id="30903-236">Explicitly trigger initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="30903-237">[EnsureCoreWebView2Async](#ensurecorewebview2async)de tâches publiques (environnement CoreWebView2Environment)</span><span class="sxs-lookup"><span data-stu-id="30903-237">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

<span data-ttu-id="30903-238">Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-238">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="30903-239">Parameters</span><span class="sxs-lookup"><span data-stu-id="30903-239">Parameters</span></span>
* `environment` <span data-ttu-id="30903-240">CoreWebView2Environment précréé qui doit être utilisé pour créer le CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-240">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="30903-241">La création de votre propre environnement vous donne le contrôle de plusieurs options qui affectent la manière dont CoreWebView2 est initialisé.</span><span class="sxs-lookup"><span data-stu-id="30903-241">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="30903-242">Si vous passez un environnement à cette méthode, elle remplacera tout paramètre spécifié sur la propriété CreationProperties.</span><span class="sxs-lookup"><span data-stu-id="30903-242">If you pass an environment to this method then it will override any settings specified on the CreationProperties property.</span></span> <span data-ttu-id="30903-243">Si vous passez la valeur null (valeur par défaut) et qu’aucune valeur n’a été définie pour CreationProperties, un environnement par défaut sera créé et utilisé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="30903-243">If you pass null (the default value) and no value has been set to CreationProperties then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="30903-244">Renvoie</span><span class="sxs-lookup"><span data-stu-id="30903-244">Returns</span></span>
<span data-ttu-id="30903-245">Tâche qui représente le processus d’initialisation en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="30903-245">A Task that represents the background initialization process.</span></span> <span data-ttu-id="30903-246">Lorsque la tâche se termine, la propriété CoreWebView2 peut être utilisée (c’est-à-dire non null).</span><span class="sxs-lookup"><span data-stu-id="30903-246">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="30903-247">Notez que l’événement CoreWebView2Ready du contrôle est appelé avant la fin de la tâche.</span><span class="sxs-lookup"><span data-stu-id="30903-247">Note that the control's CoreWebView2Ready event will be invoked before the task completes.</span></span> 

<span data-ttu-id="30903-248">L’appel de cette méthode pour les autres temps n’aura aucun effet (l’environnement spécifié est ignoré) et renvoie la même tâche que le premier appel.</span><span class="sxs-lookup"><span data-stu-id="30903-248">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="30903-249">L’appel de cette méthode une fois l’initialisation déclenchée implicitement, la définition de la propriété source n’aura aucun effet (aucun environnement spécifié n’est ignoré) et renvoyez simplement une tâche représentant cette initialisation déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="30903-249">Calling this method after initialization has been implicitly triggered by setting the Source property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> <span data-ttu-id="30903-250">Notez que bien que cette méthode soit asynchrone et renvoie une tâche, celle-ci doit toujours être appelée sur le thread d’interface utilisateur, comme la plupart des fonctionnalités publiques de la plupart des contrôles d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="30903-250">Note that even though this method is asynchronous and returns a Task, it still must be called on the UI thread like most public functionality of most UI controls.</span></span> 

##### <span data-ttu-id="30903-251">Exceptions</span><span class="sxs-lookup"><span data-stu-id="30903-251">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="30903-252">Levée si le thread appelant n’est pas le thread qui a créé cet objet (généralement le thread d’interface utilisateur).</span><span class="sxs-lookup"><span data-stu-id="30903-252">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="30903-253">Pour plus d’informations, voir DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="30903-253">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="30903-254">Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="30903-254">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="30903-255">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="30903-255">ExecuteScriptAsync</span></span> 

<span data-ttu-id="30903-256">Exécute le code JavaScript du paramètre javaScript du document de niveau supérieur actuel affiché dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="30903-256">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="30903-257">Tâche asynchrone publique< chaîne > [ExecuteScriptAsync](#executescriptasync)(chaîne JavaScript)</span><span class="sxs-lookup"><span data-stu-id="30903-257">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string javaScript)</span></span>

<span data-ttu-id="30903-258">Équivalent à l’appel de CoreWebView2. ExecuteScriptAsync sur CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="30903-258">Equivalent to calling CoreWebView2.ExecuteScriptAsync on CoreWebView2</span></span>

##### <span data-ttu-id="30903-259">Exceptions</span><span class="sxs-lookup"><span data-stu-id="30903-259">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="30903-260">Levée si CoreWebView2 n’a pas encore été initialisé.</span><span class="sxs-lookup"><span data-stu-id="30903-260">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

* `InvalidOperationException` <span data-ttu-id="30903-261">Levée si le thread appelant n’est pas le thread qui a créé cet objet (généralement le thread d’interface utilisateur).</span><span class="sxs-lookup"><span data-stu-id="30903-261">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="30903-262">Pour plus d’informations, voir DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="30903-262">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="30903-263">Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="30903-263">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="30903-264">GoBack</span><span class="sxs-lookup"><span data-stu-id="30903-264">GoBack</span></span> 

<span data-ttu-id="30903-265">Permet d’accéder à la page précédente de l’historique de navigation via le WebView.</span><span class="sxs-lookup"><span data-stu-id="30903-265">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="30903-266">public void [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="30903-266">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="30903-267">L’équivalent de l’appel à CoreWebView2. GoBack sur CoreWebView2 si CoreWebView2 n’a pas encore été initialisé, ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="30903-267">Equivalent to calling CoreWebView2.GoBack on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="30903-268">Exceptions</span><span class="sxs-lookup"><span data-stu-id="30903-268">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="30903-269">Levée si le thread appelant n’est pas le thread qui a créé cet objet (généralement le thread d’interface utilisateur).</span><span class="sxs-lookup"><span data-stu-id="30903-269">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="30903-270">Pour plus d’informations, voir DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="30903-270">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="30903-271">Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="30903-271">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="30903-272">GoForward</span><span class="sxs-lookup"><span data-stu-id="30903-272">GoForward</span></span> 

<span data-ttu-id="30903-273">Navigue vers la page suivante de l’historique de navigation du WebView.</span><span class="sxs-lookup"><span data-stu-id="30903-273">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="30903-274">public void [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="30903-274">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="30903-275">Équivalent à l’appel de la méthode CoreWebView2. GoForward sur CoreWebView2 si CoreWebView2 n’a pas été initialisée pour le moment.</span><span class="sxs-lookup"><span data-stu-id="30903-275">Equivalent to calling CoreWebView2.GoForward on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="30903-276">Exceptions</span><span class="sxs-lookup"><span data-stu-id="30903-276">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="30903-277">Levée si le thread appelant n’est pas le thread qui a créé cet objet (généralement le thread d’interface utilisateur).</span><span class="sxs-lookup"><span data-stu-id="30903-277">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="30903-278">Pour plus d’informations, voir DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="30903-278">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="30903-279">Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="30903-279">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="30903-280">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="30903-280">NavigateToString</span></span> 

<span data-ttu-id="30903-281">Lance une navigation vers htmlContent en tant que code HTML source d’un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="30903-281">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="30903-282">public void [NavigateToString](#navigatetostring)(chaîne htmlContent)</span><span class="sxs-lookup"><span data-stu-id="30903-282">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="30903-283">Équivalent à l’appel de CoreWebView2. NavigateToString sur CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="30903-283">Equivalent to calling CoreWebView2.NavigateToString on CoreWebView2</span></span>

##### <span data-ttu-id="30903-284">Exceptions</span><span class="sxs-lookup"><span data-stu-id="30903-284">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="30903-285">Levée si CoreWebView2 n’a pas encore été initialisé.</span><span class="sxs-lookup"><span data-stu-id="30903-285">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="30903-286">" <exception cref="InvalidOperationException"> Levé si le thread d’appel n’est pas le thread qui a créé cet objet (habituellement le thread d’interface utilisateur).</span><span class="sxs-lookup"><span data-stu-id="30903-286">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="30903-287">Pour plus d’informations, voir DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="30903-287">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="30903-288">Recharger</span><span class="sxs-lookup"><span data-stu-id="30903-288">Reload</span></span> 

<span data-ttu-id="30903-289">Recharge la page active.</span><span class="sxs-lookup"><span data-stu-id="30903-289">Reloads the current page.</span></span>

> <span data-ttu-id="30903-290">[rechargement](#reload)d’annulation publique ()</span><span class="sxs-lookup"><span data-stu-id="30903-290">public void [Reload](#reload)()</span></span>

<span data-ttu-id="30903-291">Équivalent à l’appel de CoreWebView2. Reload sur CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="30903-291">Equivalent to calling CoreWebView2.Reload on CoreWebView2</span></span>

##### <span data-ttu-id="30903-292">Exceptions</span><span class="sxs-lookup"><span data-stu-id="30903-292">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="30903-293">Levée si CoreWebView2 n’a pas encore été initialisé.</span><span class="sxs-lookup"><span data-stu-id="30903-293">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="30903-294">" <exception cref="InvalidOperationException"> Levé si le thread d’appel n’est pas le thread qui a créé cet objet (habituellement le thread d’interface utilisateur).</span><span class="sxs-lookup"><span data-stu-id="30903-294">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="30903-295">Pour plus d’informations, voir DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="30903-295">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="30903-296">Stop</span><span class="sxs-lookup"><span data-stu-id="30903-296">Stop</span></span> 

<span data-ttu-id="30903-297">Arrête toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="30903-297">Stops all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="30903-298">public void [Stop](#stop)()</span><span class="sxs-lookup"><span data-stu-id="30903-298">public void [Stop](#stop)()</span></span>

<span data-ttu-id="30903-299">Équivalent à l’appel de CoreWebView2. Stop sur CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="30903-299">Equivalent to calling CoreWebView2.Stop on CoreWebView2</span></span>

##### <span data-ttu-id="30903-300">Exceptions</span><span class="sxs-lookup"><span data-stu-id="30903-300">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="30903-301">Levée si CoreWebView2 n’a pas encore été initialisé.</span><span class="sxs-lookup"><span data-stu-id="30903-301">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="30903-302">" <exception cref="InvalidOperationException"> Levé si le thread d’appel n’est pas le thread qui a créé cet objet (habituellement le thread d’interface utilisateur).</span><span class="sxs-lookup"><span data-stu-id="30903-302">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="30903-303">Pour plus d’informations, voir DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="30903-303">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="30903-304">WebView2</span><span class="sxs-lookup"><span data-stu-id="30903-304">WebView2</span></span> 

<span data-ttu-id="30903-305">Crée une nouvelle instance d’un contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-305">Creates a new instance of a WebView2 control.</span></span>

> <span data-ttu-id="30903-306">public [WebView2](#webview2)()</span><span class="sxs-lookup"><span data-stu-id="30903-306">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="30903-307">Notez que le CoreWebView2 du contrôle est null jusqu’à son initialisation.</span><span class="sxs-lookup"><span data-stu-id="30903-307">Note that the control's CoreWebView2 will be null until initialized.</span></span> <span data-ttu-id="30903-308">Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.</span><span class="sxs-lookup"><span data-stu-id="30903-308">See the WebView2 class documentation for an initialization overview.</span></span>

