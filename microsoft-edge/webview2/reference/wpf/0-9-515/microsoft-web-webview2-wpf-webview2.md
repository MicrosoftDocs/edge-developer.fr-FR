---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/13/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: f2c3bcb5334abc907a838971ebc1773b6485194f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653333"
---
# <span data-ttu-id="8014b-104">Classe Microsoft. Web. WebView2. WPF. WebView2</span><span class="sxs-lookup"><span data-stu-id="8014b-104">Microsoft.Web.WebView2.Wpf.WebView2 class</span></span> 

<span data-ttu-id="8014b-105">Espace de noms: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="8014b-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="8014b-106">Assembly: Microsoft. Web. WebView2. WPF. dll</span><span class="sxs-lookup"><span data-stu-id="8014b-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.WebView2
  : public HwndHost
```

<span data-ttu-id="8014b-107">Contrôle pour incorporer du contenu Web dans une application WPF.</span><span class="sxs-lookup"><span data-stu-id="8014b-107">A control to embed web content in a WPF application.</span></span>

## <span data-ttu-id="8014b-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="8014b-108">Summary</span></span>

 <span data-ttu-id="8014b-109">Ses</span><span class="sxs-lookup"><span data-stu-id="8014b-109">Members</span></span>                        | <span data-ttu-id="8014b-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="8014b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8014b-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="8014b-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="8014b-112">Wrapper de l’événement CoreWebView2. ContentLoading de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-112">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>
[<span data-ttu-id="8014b-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="8014b-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="8014b-114">Cet événement est déclenché lors de l’initialisation de l’CoreWebView2 du contrôle (quelle que soit l’origine du déclenchement de l’initialisation), mais avant qu’elle ne soit utilisée pour n’importe quelle opération.</span><span class="sxs-lookup"><span data-stu-id="8014b-114">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="8014b-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="8014b-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="8014b-116">Wrapper de l’événement CoreWebView2. NavigationCompleted de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-116">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>
[<span data-ttu-id="8014b-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="8014b-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="8014b-118">Wrapper de l’événement CoreWebView2. NavigationStarting de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-118">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>
[<span data-ttu-id="8014b-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="8014b-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="8014b-120">Wrapper entourant l’événement CoreWebView2. SourceChanged de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-120">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>
[<span data-ttu-id="8014b-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="8014b-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="8014b-122">Wrapper de l’événement CoreWebView2. WebMessageReceived de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-122">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>
[<span data-ttu-id="8014b-123">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="8014b-123">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="8014b-124">Renvoie vrai si le WebView peut accéder à une page précédente de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="8014b-124">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="8014b-125">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="8014b-125">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="8014b-126">Cette fonction renvoie la valeur vrai si le WebView peut accéder à une page suivante de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="8014b-126">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="8014b-127">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="8014b-127">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="8014b-128">Accédez à l’ensemble des fonctionnalités de l’API COM Core. CoreWebView2 sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="8014b-128">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>
[<span data-ttu-id="8014b-129">CreationProperties</span><span class="sxs-lookup"><span data-stu-id="8014b-129">CreationProperties</span></span>](#creationproperties) | <span data-ttu-id="8014b-130">Obtient ou définit un sac d’options qui sont utilisées lors de l’initialisation de la CoreWebView2 du contrôle.</span><span class="sxs-lookup"><span data-stu-id="8014b-130">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="8014b-131">Source</span><span class="sxs-lookup"><span data-stu-id="8014b-131">Source</span></span>](#source) | <span data-ttu-id="8014b-132">L’URI de niveau supérieur sur lequel est actuellement affiché le WebView (ou s’affichera une fois l’initialisation de son CoreWebView2 terminée).</span><span class="sxs-lookup"><span data-stu-id="8014b-132">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>
[<span data-ttu-id="8014b-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="8014b-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="8014b-134">Déclenchez explicitement l’initialisation de CoreWebView2 du contrôle.</span><span class="sxs-lookup"><span data-stu-id="8014b-134">Explicitly trigger initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="8014b-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="8014b-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="8014b-136">Exécute le code JavaScript du paramètre javaScript du document de niveau supérieur actuel affiché dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="8014b-136">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="8014b-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="8014b-137">GoBack</span></span>](#goback) | <span data-ttu-id="8014b-138">Permet d’accéder à la page précédente de l’historique de navigation via le WebView.</span><span class="sxs-lookup"><span data-stu-id="8014b-138">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="8014b-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="8014b-139">GoForward</span></span>](#goforward) | <span data-ttu-id="8014b-140">Navigue vers la page suivante de l’historique de navigation du WebView.</span><span class="sxs-lookup"><span data-stu-id="8014b-140">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="8014b-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="8014b-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="8014b-142">Lance une navigation vers htmlContent en tant que code HTML source d’un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="8014b-142">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="8014b-143">Recharger</span><span class="sxs-lookup"><span data-stu-id="8014b-143">Reload</span></span>](#reload) | <span data-ttu-id="8014b-144">Recharge la page active.</span><span class="sxs-lookup"><span data-stu-id="8014b-144">Reloads the current page.</span></span>
[<span data-ttu-id="8014b-145">Stop</span><span class="sxs-lookup"><span data-stu-id="8014b-145">Stop</span></span>](#stop) | <span data-ttu-id="8014b-146">Arrête toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="8014b-146">Stops all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="8014b-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="8014b-147">WebView2</span></span>](#webview2) | <span data-ttu-id="8014b-148">Crée une nouvelle instance d’un contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-148">Creates a new instance of a WebView2 control.</span></span>
[<span data-ttu-id="8014b-149">BuildWindowCore</span><span class="sxs-lookup"><span data-stu-id="8014b-149">BuildWindowCore</span></span>](#buildwindowcore) | <span data-ttu-id="8014b-150">Il est alors substitué de HwndHost et est appelé pour nous indiquer de créer notre HWND.</span><span class="sxs-lookup"><span data-stu-id="8014b-150">This is overridden from HwndHost and is called to instruct us to create our HWND.</span></span>
[<span data-ttu-id="8014b-151">DestroyWindowCore</span><span class="sxs-lookup"><span data-stu-id="8014b-151">DestroyWindowCore</span></span>](#destroywindowcore) | <span data-ttu-id="8014b-152">Il est alors substitué de HwndHost et est appelé pour nous demander de détruire le HWND.</span><span class="sxs-lookup"><span data-stu-id="8014b-152">This is overridden from HwndHost and is called to instruct us to destroy our HWND.</span></span>
[<span data-ttu-id="8014b-153">Suppression</span><span class="sxs-lookup"><span data-stu-id="8014b-153">Dispose</span></span>](#dispose) | <span data-ttu-id="8014b-154">C’est appelé par notre classe de base en fonction de l’implémentation type du modèle IDispose.</span><span class="sxs-lookup"><span data-stu-id="8014b-154">This is called by our base class according to the typical implementation of the IDispose pattern.</span></span>
[<span data-ttu-id="8014b-155">HasFocusWithinCore</span><span class="sxs-lookup"><span data-stu-id="8014b-155">HasFocusWithinCore</span></span>](#hasfocuswithincore) | <span data-ttu-id="8014b-156">Il est substitué de HwndHost et est appelé lorsque WPF a besoin de savoir si le focus se trouve dans notre contrôle/fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8014b-156">This is overridden from HwndHost and is called when WPF needs to know if the focus is in our control/window.</span></span>
[<span data-ttu-id="8014b-157">OnKeyDown</span><span class="sxs-lookup"><span data-stu-id="8014b-157">OnKeyDown</span></span>](#onkeydown) | <span data-ttu-id="8014b-158">Il est substitué de UIElement et appelé pour nous permettre de traiter les entrées de la pression de touche.</span><span class="sxs-lookup"><span data-stu-id="8014b-158">This is overridden from UIElement and called to allow us to handle key press input.</span></span>
[<span data-ttu-id="8014b-159">OnKeyUp</span><span class="sxs-lookup"><span data-stu-id="8014b-159">OnKeyUp</span></span>](#onkeyup) | <span data-ttu-id="8014b-160">Voir OnKeyDown.</span><span class="sxs-lookup"><span data-stu-id="8014b-160">See OnKeyDown.</span></span>
[<span data-ttu-id="8014b-161">OnPreviewKeyDown</span><span class="sxs-lookup"><span data-stu-id="8014b-161">OnPreviewKeyDown</span></span>](#onpreviewkeydown) | <span data-ttu-id="8014b-162">Il s’agit de la version d’évaluation («Preview») (c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="8014b-162">This is the "Preview" (i.e.</span></span>
[<span data-ttu-id="8014b-163">OnPreviewKeyUp</span><span class="sxs-lookup"><span data-stu-id="8014b-163">OnPreviewKeyUp</span></span>](#onpreviewkeyup) | <span data-ttu-id="8014b-164">Voir OnPreviewKeyDown.</span><span class="sxs-lookup"><span data-stu-id="8014b-164">See OnPreviewKeyDown.</span></span>
[<span data-ttu-id="8014b-165">OnWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="8014b-165">OnWindowPositionChanged</span></span>](#onwindowpositionchanged) | <span data-ttu-id="8014b-166">Il est substitué de HwndHost et appelé lorsque l’emplacement de votre contrôle a changé.</span><span class="sxs-lookup"><span data-stu-id="8014b-166">This is overridden from HwndHost and called when our control's location has changed.</span></span>
[<span data-ttu-id="8014b-167">TabIntoCore</span><span class="sxs-lookup"><span data-stu-id="8014b-167">TabIntoCore</span></span>](#tabintocore) | <span data-ttu-id="8014b-168">Il est alors substitué de HwndHost et est appelé pour nous informer que la touche de tabulation a entraîné le déplacement vers notre contrôle/fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8014b-168">This is overridden from HwndHost and is called to inform us that tabbing has caused the focus to move into our control/window.</span></span>

<span data-ttu-id="8014b-169">Ce contrôle est en réalité un wrapper qui entoure l’API COM WebView2, qui vous trouverez de la documentation pour cet emplacement: [https://aka.ms/webview2](https://aka.ms/webview2) vous pouvez accéder directement à l’interface ICoreWebView2 sous-jacente et à toutes ses fonctionnalités en accédant à la propriété CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-169">This control is effectively a wrapper around the WebView2 COM API, which you can find documentation for here: [https://aka.ms/webview2](https://aka.ms/webview2) You can directly access the underlying ICoreWebView2 interface and all of its functionality by accessing the CoreWebView2 property.</span></span> <span data-ttu-id="8014b-170">Certaines des fonctionnalités COM les plus courantes sont également accessibles directement via les méthodes d’encapsulation/propriétés/événements du contrôle.</span><span class="sxs-lookup"><span data-stu-id="8014b-170">Some of the most common COM functionality is also accessible directly through wrapper methods/properties/events on the control.</span></span>

<span data-ttu-id="8014b-171">Lors de la création, la propriété CoreWebView2 du contrôle est null.</span><span class="sxs-lookup"><span data-stu-id="8014b-171">Upon creation, the control's CoreWebView2 property will be null.</span></span> <span data-ttu-id="8014b-172">En effet, la création de CoreWebView2 est une opération onéreuse qui implique des opérations comme le lancement de processus de navigateur Edge.</span><span class="sxs-lookup"><span data-stu-id="8014b-172">This is because creating the CoreWebView2 is an expensive operation which involves things like launching Edge browser processes.</span></span> <span data-ttu-id="8014b-173">Il existe deux façons d’entraîner la création du CoreWebView2:1) appeler la méthode EnsureCoreWebView2Async.</span><span class="sxs-lookup"><span data-stu-id="8014b-173">There are two ways to cause the CoreWebView2 to be created: 1) Call the EnsureCoreWebView2Async method.</span></span> <span data-ttu-id="8014b-174">On parle d’initialisation explicite.</span><span class="sxs-lookup"><span data-stu-id="8014b-174">This is referred to as explicit initialization.</span></span> <span data-ttu-id="8014b-175">2) définissez la propriété source (qui peut être exécutée à partir du balisage, par exemple).</span><span class="sxs-lookup"><span data-stu-id="8014b-175">2) Set the Source property (which could be done from markup, for example).</span></span> <span data-ttu-id="8014b-176">On parle d’initialisation implicite.</span><span class="sxs-lookup"><span data-stu-id="8014b-176">This is referred to as implicit initialization.</span></span> <span data-ttu-id="8014b-177">L’une des deux options commencera l’initialisation en arrière-plan et renverra l’appelant sans attendre la fin de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="8014b-177">Either option will start initialization in the background and return back to the caller without waiting for it to finish.</span></span> <span data-ttu-id="8014b-178">Pour spécifier des options concernant le processus d’initialisation, transmettez votre propre CoreWebView2Environment à EnsureCoreWebView2Async ou définissez la propriété CreationProperties du contrôle avant l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="8014b-178">To specify options regarding the initialization process, either pass your own CoreWebView2Environment to EnsureCoreWebView2Async or set the control's CreationProperties property prior to initialization.</span></span>

<span data-ttu-id="8014b-179">Une fois l’initialisation terminée (quel que soit le mode de déclenchement), les éléments suivants se produisent, dans l’ordre suivant: 1) l’événement CoreWebView2Ready du contrôle est appelé.</span><span class="sxs-lookup"><span data-stu-id="8014b-179">When initialization has finished (regardless of how it was triggered) then the following things will occur, in this order: 1) The control's CoreWebView2Ready event will be invoked.</span></span> <span data-ttu-id="8014b-180">Si vous devez effectuer une opération de configuration ponctuelle sur le CoreWebView2 avant de l’utiliser, vous devez le faire dans un gestionnaire pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="8014b-180">If you need to perform one time setup operations on the CoreWebView2 prior to its use then you should do so in a handler for that event.</span></span> <span data-ttu-id="8014b-181">2) si un URI a été défini pour la propriété source, le contrôle commencera à y accéder en arrière-plan (c’est-à-dire, ces étapes continuent sans attendre la fin de la navigation).</span><span class="sxs-lookup"><span data-stu-id="8014b-181">2) If a Uri has been set to the Source property then the control will start navigating to it in the background (i.e. these steps will continue without waiting for the navigation to finish).</span></span> <span data-ttu-id="8014b-182">3) la tâche renvoyée par EnsureCoreWebView2Async sera terminée.</span><span class="sxs-lookup"><span data-stu-id="8014b-182">3) The Task returned from EnsureCoreWebView2Async will complete.</span></span>

<span data-ttu-id="8014b-183">Pour plus d’informations sur les méthodes/propriétés/événements impliqués dans le processus d’initialisation, voir sa documentation spécifique.</span><span class="sxs-lookup"><span data-stu-id="8014b-183">For more details about any of the methods/properties/events involved in the initialization process, see its specific documentation.</span></span>

<span data-ttu-id="8014b-184">Dans la mesure où le contrôle CoreWebView2 est un objet très haute densité (qui peut être responsable de plusieurs processus en cours d’exécution et de mégaoctets d’espace disque), le contrôle implémente IDisposable pour fournir un moyen explicite de le libérer.</span><span class="sxs-lookup"><span data-stu-id="8014b-184">Because the control's CoreWebView2 is a very heavyweight object (potentially responsible for multiple running processes and megabytes of disk space) the control implements IDisposable to provide an explicit means to free it.</span></span> <span data-ttu-id="8014b-185">L’appel de dispose va libérer le CoreWebView2 et ses ressources sous-jacentes (sauf s’ils sont également utilisés par d’autres WebViews) et réinitialiser CoreWebView2 sur null.</span><span class="sxs-lookup"><span data-stu-id="8014b-185">Calling Dispose will release the CoreWebView2 and its underlying resources (except any that are also being used by other WebViews), and reset CoreWebView2 to null.</span></span> <span data-ttu-id="8014b-186">Après avoir appelé la méthode CoreWebView2 ne peut pas être réinitialisée, et toute tentative d’utilisation de la fonctionnalité qui nécessite qu’elle lèvera une opération ObjectDisposedException.</span><span class="sxs-lookup"><span data-stu-id="8014b-186">After Dispose has been called the CoreWebView2 cannot be re-initialized, and any attempt to use functionality which requires it will throw an ObjectDisposedException.</span></span>

<span data-ttu-id="8014b-187">Notez que ce contrôle étend HwndHost afin d’incorporer des fenêtres qui résident en dehors de l’écosystème WPF.</span><span class="sxs-lookup"><span data-stu-id="8014b-187">Note that this control extends HwndHost in order to embed windows which live outside of the WPF ecosystem.</span></span> <span data-ttu-id="8014b-188">Cela a quelques implications sur le comportement de l’entrée et de la sortie du contrôle, ainsi que sur les fonctionnalités qu’il hérite de l’élément UIElement et de FrameworkElement.</span><span class="sxs-lookup"><span data-stu-id="8014b-188">This has some implications regarding the control's input and output behavior as well as the functionality it "inherits" from UIElement and FrameworkElement.</span></span> <span data-ttu-id="8014b-189">Pour plus d’informations, consultez la documentation sur l’interopérabilité HwndHost et WPF/Win32.</span><span class="sxs-lookup"><span data-stu-id="8014b-189">See the HwndHost and WPF/Win32 interop documentation for more info:</span></span>

* [https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost](https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost)

* [https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf](https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf)

## <span data-ttu-id="8014b-190">Ses</span><span class="sxs-lookup"><span data-stu-id="8014b-190">Members</span></span>

#### <span data-ttu-id="8014b-191">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="8014b-191">ContentLoading</span></span> 

<span data-ttu-id="8014b-192">Wrapper de l’événement CoreWebView2. ContentLoading de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-192">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>

> <span data-ttu-id="8014b-193">événement public EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="8014b-193">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="8014b-194">La seule différence entre cet événement et CoreWebView2. ContentLoading est le premier paramètre passé aux gestionnaires.</span><span class="sxs-lookup"><span data-stu-id="8014b-194">The only difference between this event and CoreWebView2.ContentLoading is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="8014b-195">Le gestionnaire de cet événement reçoit le contrôle WebView2, alors que les gestionnaires de CoreWebView2. ContentLoading recevront l’instance CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-195">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.ContentLoading will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="8014b-196">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="8014b-196">CoreWebView2Ready</span></span> 

<span data-ttu-id="8014b-197">Cet événement est déclenché lors de l’initialisation de l’CoreWebView2 du contrôle (quelle que soit l’origine du déclenchement de l’initialisation), mais avant qu’elle ne soit utilisée pour n’importe quelle opération.</span><span class="sxs-lookup"><span data-stu-id="8014b-197">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="8014b-198">événement public EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="8014b-198">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="8014b-199">Vous devez gérer cet événement si vous avez besoin d’effectuer des opérations d’installation ponctuelles sur le CoreWebView2 que vous voulez affecter à l’ensemble de ses utilisations (par exemple, ajout de gestionnaires d’événements, configuration des paramètres, installation de scripts de création de documents, ajout d’objets hôtes).</span><span class="sxs-lookup"><span data-stu-id="8014b-199">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span> <span data-ttu-id="8014b-200">Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-200">See the WebView2 class documentation for an initialization overview.</span></span>

<span data-ttu-id="8014b-201">Cet événement ne fournit aucun argument et l’expéditeur sera le contrôle WebView2, dont la propriété CoreWebView2 sera désormais valide (c’est-à-dire non null) pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="8014b-201">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="8014b-202">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="8014b-202">NavigationCompleted</span></span> 

<span data-ttu-id="8014b-203">Wrapper de l’événement CoreWebView2. NavigationCompleted de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-203">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>

> <span data-ttu-id="8014b-204">événement public EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="8014b-204">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="8014b-205">La seule différence entre cet événement et CoreWebView2. NavigationCompleted est le premier paramètre passé aux gestionnaires.</span><span class="sxs-lookup"><span data-stu-id="8014b-205">The only difference between this event and CoreWebView2.NavigationCompleted is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="8014b-206">Le gestionnaire de cet événement reçoit le contrôle WebView2, alors que les gestionnaires de CoreWebView2. NavigationCompleted recevront l’instance CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-206">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationCompleted will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="8014b-207">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="8014b-207">NavigationStarting</span></span> 

<span data-ttu-id="8014b-208">Wrapper de l’événement CoreWebView2. NavigationStarting de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-208">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>

> <span data-ttu-id="8014b-209">événement public EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="8014b-209">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="8014b-210">La seule différence entre cet événement et CoreWebView2. NavigationStarting est le premier paramètre passé aux gestionnaires.</span><span class="sxs-lookup"><span data-stu-id="8014b-210">The only difference between this event and CoreWebView2.NavigationStarting is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="8014b-211">Le gestionnaire de cet événement reçoit le contrôle WebView2, alors que les gestionnaires de CoreWebView2. NavigationStarting recevront l’instance CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-211">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationStarting will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="8014b-212">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="8014b-212">SourceChanged</span></span> 

<span data-ttu-id="8014b-213">Wrapper entourant l’événement CoreWebView2. SourceChanged de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-213">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>

> <span data-ttu-id="8014b-214">événement public EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="8014b-214">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="8014b-215">La seule différence entre cet événement et CoreWebView2. SourceChanged est le premier paramètre passé aux gestionnaires.</span><span class="sxs-lookup"><span data-stu-id="8014b-215">The only difference between this event and CoreWebView2.SourceChanged is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="8014b-216">Le gestionnaire de cet événement reçoit le contrôle WebView2, alors que les gestionnaires de CoreWebView2. SourceChanged reçoivent l’instance CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-216">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.SourceChanged will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="8014b-217">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="8014b-217">WebMessageReceived</span></span> 

<span data-ttu-id="8014b-218">Wrapper de l’événement CoreWebView2. WebMessageReceived de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-218">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>

> <span data-ttu-id="8014b-219">événement public EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="8014b-219">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="8014b-220">La seule différence entre cet événement et CoreWebView2. WebMessageReceived est le premier paramètre passé aux gestionnaires.</span><span class="sxs-lookup"><span data-stu-id="8014b-220">The only difference between this event and CoreWebView2.WebMessageReceived is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="8014b-221">Le gestionnaire de cet événement reçoit le contrôle WebView2, alors que les gestionnaires de CoreWebView2. WebMessageReceived recevront l’instance CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-221">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.WebMessageReceived will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="8014b-222">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="8014b-222">CanGoBack</span></span> 

<span data-ttu-id="8014b-223">Renvoie vrai si le WebView peut accéder à une page précédente de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="8014b-223">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="8014b-224">public bool [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="8014b-224">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="8014b-225">Wrapper dans la propriété CoreWebView2. CanGoBack de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-225">Wrapper around the CoreWebView2.CanGoBack property of CoreWebView2.</span></span> <span data-ttu-id="8014b-226">Si CoreWebView2 n’est pas initialisé, retourne false.</span><span class="sxs-lookup"><span data-stu-id="8014b-226">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="8014b-227">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="8014b-227">CanGoForward</span></span> 

<span data-ttu-id="8014b-228">Cette fonction renvoie la valeur vrai si le WebView peut accéder à une page suivante de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="8014b-228">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="8014b-229">public bool [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="8014b-229">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="8014b-230">Wrapper dans la propriété CoreWebView2. CanGoForward de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-230">Wrapper around the CoreWebView2.CanGoForward property of CoreWebView2.</span></span> <span data-ttu-id="8014b-231">Si CoreWebView2 n’est pas initialisé, retourne false.</span><span class="sxs-lookup"><span data-stu-id="8014b-231">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="8014b-232">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="8014b-232">CoreWebView2</span></span> 

<span data-ttu-id="8014b-233">Accédez à l’ensemble des fonctionnalités de l’API COM Core. CoreWebView2 sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="8014b-233">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>

> <span data-ttu-id="8014b-234">public CoreWebView2 [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="8014b-234">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="8014b-235">Retourne la valeur null jusqu’à la fin de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="8014b-235">Returns null until initialization has completed.</span></span> <span data-ttu-id="8014b-236">Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-236">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="8014b-237">Exceptions</span><span class="sxs-lookup"><span data-stu-id="8014b-237">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="8014b-238">Levée si le thread appelant n’est pas le thread qui a créé cet objet (généralement le thread d’interface utilisateur).</span><span class="sxs-lookup"><span data-stu-id="8014b-238">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="8014b-239">Pour plus d’informations, voir DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="8014b-239">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="8014b-240">Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="8014b-240">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8014b-241">CreationProperties</span><span class="sxs-lookup"><span data-stu-id="8014b-241">CreationProperties</span></span> 

<span data-ttu-id="8014b-242">Obtient ou définit un sac d’options qui sont utilisées lors de l’initialisation de la CoreWebView2 du contrôle.</span><span class="sxs-lookup"><span data-stu-id="8014b-242">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="8014b-243">public CoreWebView2CreationProperties [CreationProperties](#creationproperties)</span><span class="sxs-lookup"><span data-stu-id="8014b-243">public CoreWebView2CreationProperties [CreationProperties](#creationproperties)</span></span>

<span data-ttu-id="8014b-244">La définition de cette propriété ne fonctionnera pas une fois l’initialisation du CoreWebView2 du contrôle démarrée (l’ancienne valeur sera conservée).</span><span class="sxs-lookup"><span data-stu-id="8014b-244">Setting this property won't work after initialization of the control's CoreWebView2 has started (the old value will be retained).</span></span> <span data-ttu-id="8014b-245">Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-245">See the WebView2 class documentation for an initialization overview.</span></span>

#### <span data-ttu-id="8014b-246">Source</span><span class="sxs-lookup"><span data-stu-id="8014b-246">Source</span></span> 

<span data-ttu-id="8014b-247">L’URI de niveau supérieur sur lequel est actuellement affiché le WebView (ou s’affichera une fois l’initialisation de son CoreWebView2 terminée).</span><span class="sxs-lookup"><span data-stu-id="8014b-247">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>

> <span data-ttu-id="8014b-248">[source](#source) URI publique</span><span class="sxs-lookup"><span data-stu-id="8014b-248">public Uri [Source](#source)</span></span>

<span data-ttu-id="8014b-249">En règle générale, l’accès à cette propriété est équivalent à l’utilisation de la propriété CoreWebView2. source de CoreWebView2 et la définition de cette propriété revient à appeler la méthode CoreWebView2. Navigate sur CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-249">Generally speaking, getting this property is equivalent to getting the CoreWebView2.Source property of CoreWebView2 and setting this property is equivalent to calling the CoreWebView2.Navigate method on CoreWebView2.</span></span> <span data-ttu-id="8014b-250">L’accès à cette propriété avant l’initialisation de CoreWebView2 permet de récupérer le dernier URI qui a été défini.</span><span class="sxs-lookup"><span data-stu-id="8014b-250">Getting this property before the CoreWebView2 has been initialized will retrieve the last Uri which was set to it.</span></span> <span data-ttu-id="8014b-251">Le fait de définir cette propriété avant l’initialisation de CoreWebView2 entraînera le démarrage de l’initialisation en arrière-plan (si ce n’est pas déjà fait), après lequel WebView2 accède à l’URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="8014b-251">Setting this property before the CoreWebView2 has been initialized will cause initialization to start in the background (if not already in progress), after which the WebView2 will navigate to the specified Uri.</span></span> <span data-ttu-id="8014b-252">Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-252">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="8014b-253">Exceptions</span><span class="sxs-lookup"><span data-stu-id="8014b-253">Exceptions</span></span>
* `ObjectDisposedException` <span data-ttu-id="8014b-254">Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="8014b-254">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8014b-255">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="8014b-255">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="8014b-256">Déclenchez explicitement l’initialisation de CoreWebView2 du contrôle.</span><span class="sxs-lookup"><span data-stu-id="8014b-256">Explicitly trigger initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="8014b-257">[EnsureCoreWebView2Async](#ensurecorewebview2async)de tâches publiques (environnement CoreWebView2Environment)</span><span class="sxs-lookup"><span data-stu-id="8014b-257">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

<span data-ttu-id="8014b-258">Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-258">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="8014b-259">Parameters</span><span class="sxs-lookup"><span data-stu-id="8014b-259">Parameters</span></span>
* `environment` <span data-ttu-id="8014b-260">CoreWebView2Environment précréé qui doit être utilisé pour créer le CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-260">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="8014b-261">La création de votre propre environnement vous donne le contrôle de plusieurs options qui affectent la manière dont CoreWebView2 est initialisé.</span><span class="sxs-lookup"><span data-stu-id="8014b-261">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="8014b-262">Si vous passez un environnement à cette méthode, elle remplacera tout paramètre spécifié sur la propriété CreationProperties.</span><span class="sxs-lookup"><span data-stu-id="8014b-262">If you pass an environment to this method then it will override any settings specified on the CreationProperties property.</span></span> <span data-ttu-id="8014b-263">Si vous passez la valeur null (valeur par défaut) et qu’aucune valeur n’a été définie pour CreationProperties, un environnement par défaut sera créé et utilisé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="8014b-263">If you pass null (the default value) and no value has been set to CreationProperties then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="8014b-264">Renvoie</span><span class="sxs-lookup"><span data-stu-id="8014b-264">Returns</span></span>
<span data-ttu-id="8014b-265">Tâche qui représente le processus d’initialisation en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="8014b-265">A Task that represents the background initialization process.</span></span> <span data-ttu-id="8014b-266">Lorsque la tâche se termine, la propriété CoreWebView2 peut être utilisée (c’est-à-dire non null).</span><span class="sxs-lookup"><span data-stu-id="8014b-266">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="8014b-267">Notez que l’événement CoreWebView2Ready du contrôle est appelé avant la fin de la tâche.</span><span class="sxs-lookup"><span data-stu-id="8014b-267">Note that the control's CoreWebView2Ready event will be invoked before the task completes.</span></span> 

<span data-ttu-id="8014b-268">L’appel de cette méthode pour les autres temps n’aura aucun effet (l’environnement spécifié est ignoré) et renvoie la même tâche que le premier appel.</span><span class="sxs-lookup"><span data-stu-id="8014b-268">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="8014b-269">L’appel de cette méthode une fois l’initialisation déclenchée implicitement, la définition de la propriété source n’aura aucun effet (aucun environnement spécifié n’est ignoré) et renvoyez simplement une tâche représentant cette initialisation déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="8014b-269">Calling this method after initialization has been implicitly triggered by setting the Source property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> <span data-ttu-id="8014b-270">Notez que bien que cette méthode soit asynchrone et renvoie une tâche, celle-ci doit toujours être appelée sur le thread d’interface utilisateur, comme la plupart des fonctionnalités publiques de la plupart des contrôles d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8014b-270">Note that even though this method is asynchronous and returns a Task, it still must be called on the UI thread like most public functionality of most UI controls.</span></span> 

##### <span data-ttu-id="8014b-271">Exceptions</span><span class="sxs-lookup"><span data-stu-id="8014b-271">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="8014b-272">Levée si le thread appelant n’est pas le thread qui a créé cet objet (généralement le thread d’interface utilisateur).</span><span class="sxs-lookup"><span data-stu-id="8014b-272">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="8014b-273">Pour plus d’informations, voir DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="8014b-273">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="8014b-274">Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="8014b-274">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8014b-275">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="8014b-275">ExecuteScriptAsync</span></span> 

<span data-ttu-id="8014b-276">Exécute le code JavaScript du paramètre javaScript du document de niveau supérieur actuel affiché dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="8014b-276">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="8014b-277">Tâche asynchrone publique< chaîne > [ExecuteScriptAsync](#executescriptasync)(chaîne JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8014b-277">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string javaScript)</span></span>

<span data-ttu-id="8014b-278">Équivalent à l’appel de CoreWebView2. ExecuteScriptAsync sur CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="8014b-278">Equivalent to calling CoreWebView2.ExecuteScriptAsync on CoreWebView2</span></span>

##### <span data-ttu-id="8014b-279">Exceptions</span><span class="sxs-lookup"><span data-stu-id="8014b-279">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="8014b-280">Levée si CoreWebView2 n’a pas encore été initialisé.</span><span class="sxs-lookup"><span data-stu-id="8014b-280">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

* `InvalidOperationException` <span data-ttu-id="8014b-281">Levée si le thread appelant n’est pas le thread qui a créé cet objet (généralement le thread d’interface utilisateur).</span><span class="sxs-lookup"><span data-stu-id="8014b-281">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="8014b-282">Pour plus d’informations, voir DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="8014b-282">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="8014b-283">Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="8014b-283">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8014b-284">GoBack</span><span class="sxs-lookup"><span data-stu-id="8014b-284">GoBack</span></span> 

<span data-ttu-id="8014b-285">Permet d’accéder à la page précédente de l’historique de navigation via le WebView.</span><span class="sxs-lookup"><span data-stu-id="8014b-285">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="8014b-286">public void [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="8014b-286">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="8014b-287">L’équivalent de l’appel à CoreWebView2. GoBack sur CoreWebView2 si CoreWebView2 n’a pas encore été initialisé, ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="8014b-287">Equivalent to calling CoreWebView2.GoBack on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="8014b-288">Exceptions</span><span class="sxs-lookup"><span data-stu-id="8014b-288">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="8014b-289">Levée si le thread appelant n’est pas le thread qui a créé cet objet (généralement le thread d’interface utilisateur).</span><span class="sxs-lookup"><span data-stu-id="8014b-289">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="8014b-290">Pour plus d’informations, voir DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="8014b-290">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="8014b-291">Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="8014b-291">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8014b-292">GoForward</span><span class="sxs-lookup"><span data-stu-id="8014b-292">GoForward</span></span> 

<span data-ttu-id="8014b-293">Navigue vers la page suivante de l’historique de navigation du WebView.</span><span class="sxs-lookup"><span data-stu-id="8014b-293">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="8014b-294">public void [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="8014b-294">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="8014b-295">Équivalent à l’appel de la méthode CoreWebView2. GoForward sur CoreWebView2 si CoreWebView2 n’a pas été initialisée pour le moment.</span><span class="sxs-lookup"><span data-stu-id="8014b-295">Equivalent to calling CoreWebView2.GoForward on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="8014b-296">Exceptions</span><span class="sxs-lookup"><span data-stu-id="8014b-296">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="8014b-297">Levée si le thread appelant n’est pas le thread qui a créé cet objet (généralement le thread d’interface utilisateur).</span><span class="sxs-lookup"><span data-stu-id="8014b-297">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="8014b-298">Pour plus d’informations, voir DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="8014b-298">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="8014b-299">Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="8014b-299">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8014b-300">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="8014b-300">NavigateToString</span></span> 

<span data-ttu-id="8014b-301">Lance une navigation vers htmlContent en tant que code HTML source d’un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="8014b-301">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="8014b-302">public void [NavigateToString](#navigatetostring)(chaîne htmlContent)</span><span class="sxs-lookup"><span data-stu-id="8014b-302">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="8014b-303">Équivalent à l’appel de CoreWebView2. NavigateToString sur CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="8014b-303">Equivalent to calling CoreWebView2.NavigateToString on CoreWebView2</span></span>

##### <span data-ttu-id="8014b-304">Exceptions</span><span class="sxs-lookup"><span data-stu-id="8014b-304">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="8014b-305">Levée si CoreWebView2 n’a pas encore été initialisé.</span><span class="sxs-lookup"><span data-stu-id="8014b-305">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="8014b-306">" <exception cref="InvalidOperationException"> Levé si le thread d’appel n’est pas le thread qui a créé cet objet (habituellement le thread d’interface utilisateur).</span><span class="sxs-lookup"><span data-stu-id="8014b-306">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="8014b-307">Pour plus d’informations, voir DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="8014b-307">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8014b-308">Recharger</span><span class="sxs-lookup"><span data-stu-id="8014b-308">Reload</span></span> 

<span data-ttu-id="8014b-309">Recharge la page active.</span><span class="sxs-lookup"><span data-stu-id="8014b-309">Reloads the current page.</span></span>

> <span data-ttu-id="8014b-310">[rechargement](#reload)d’annulation publique ()</span><span class="sxs-lookup"><span data-stu-id="8014b-310">public void [Reload](#reload)()</span></span>

<span data-ttu-id="8014b-311">Équivalent à l’appel de CoreWebView2. Reload sur CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="8014b-311">Equivalent to calling CoreWebView2.Reload on CoreWebView2</span></span>

##### <span data-ttu-id="8014b-312">Exceptions</span><span class="sxs-lookup"><span data-stu-id="8014b-312">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="8014b-313">Levée si CoreWebView2 n’a pas encore été initialisé.</span><span class="sxs-lookup"><span data-stu-id="8014b-313">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="8014b-314">" <exception cref="InvalidOperationException"> Levé si le thread d’appel n’est pas le thread qui a créé cet objet (habituellement le thread d’interface utilisateur).</span><span class="sxs-lookup"><span data-stu-id="8014b-314">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="8014b-315">Pour plus d’informations, voir DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="8014b-315">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8014b-316">Stop</span><span class="sxs-lookup"><span data-stu-id="8014b-316">Stop</span></span> 

<span data-ttu-id="8014b-317">Arrête toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="8014b-317">Stops all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="8014b-318">public void [Stop](#stop)()</span><span class="sxs-lookup"><span data-stu-id="8014b-318">public void [Stop](#stop)()</span></span>

<span data-ttu-id="8014b-319">Équivalent à l’appel de CoreWebView2. Stop sur CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="8014b-319">Equivalent to calling CoreWebView2.Stop on CoreWebView2</span></span>

##### <span data-ttu-id="8014b-320">Exceptions</span><span class="sxs-lookup"><span data-stu-id="8014b-320">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="8014b-321">Levée si CoreWebView2 n’a pas encore été initialisé.</span><span class="sxs-lookup"><span data-stu-id="8014b-321">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="8014b-322">" <exception cref="InvalidOperationException"> Levé si le thread d’appel n’est pas le thread qui a créé cet objet (habituellement le thread d’interface utilisateur).</span><span class="sxs-lookup"><span data-stu-id="8014b-322">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="8014b-323">Pour plus d’informations, voir DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Levée si dispose est déjà appelé sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="8014b-323">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8014b-324">WebView2</span><span class="sxs-lookup"><span data-stu-id="8014b-324">WebView2</span></span> 

<span data-ttu-id="8014b-325">Crée une nouvelle instance d’un contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-325">Creates a new instance of a WebView2 control.</span></span>

> <span data-ttu-id="8014b-326">public [WebView2](#webview2)()</span><span class="sxs-lookup"><span data-stu-id="8014b-326">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="8014b-327">Notez que le CoreWebView2 du contrôle est null jusqu’à son initialisation.</span><span class="sxs-lookup"><span data-stu-id="8014b-327">Note that the control's CoreWebView2 will be null until initialized.</span></span> <span data-ttu-id="8014b-328">Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-328">See the WebView2 class documentation for an initialization overview.</span></span>

#### <span data-ttu-id="8014b-329">BuildWindowCore</span><span class="sxs-lookup"><span data-stu-id="8014b-329">BuildWindowCore</span></span> 

<span data-ttu-id="8014b-330">Il est alors substitué de HwndHost et est appelé pour nous indiquer de créer notre HWND.</span><span class="sxs-lookup"><span data-stu-id="8014b-330">This is overridden from HwndHost and is called to instruct us to create our HWND.</span></span>

> <span data-ttu-id="8014b-331">remplacement sécurisé de HandleRef [BuildWindowCore](#buildwindowcore)(HandleRef hwndParent)</span><span class="sxs-lookup"><span data-stu-id="8014b-331">protected override HandleRef [BuildWindowCore](#buildwindowcore)(HandleRef hwndParent)</span></span>

##### <span data-ttu-id="8014b-332">Parameters</span><span class="sxs-lookup"><span data-stu-id="8014b-332">Parameters</span></span>
* `hwndParent` <span data-ttu-id="8014b-333">HWND que nous devons utiliser en tant que parent de celle que nous créons.</span><span class="sxs-lookup"><span data-stu-id="8014b-333">The HWND that we should use as the parent of the one we create.</span></span>

##### <span data-ttu-id="8014b-334">Renvoie</span><span class="sxs-lookup"><span data-stu-id="8014b-334">Returns</span></span>
<span data-ttu-id="8014b-335">Le HWND que nous avons créé.</span><span class="sxs-lookup"><span data-stu-id="8014b-335">The HWND that we created.</span></span>

#### <span data-ttu-id="8014b-336">DestroyWindowCore</span><span class="sxs-lookup"><span data-stu-id="8014b-336">DestroyWindowCore</span></span> 

<span data-ttu-id="8014b-337">Il est alors substitué de HwndHost et est appelé pour nous demander de détruire le HWND.</span><span class="sxs-lookup"><span data-stu-id="8014b-337">This is overridden from HwndHost and is called to instruct us to destroy our HWND.</span></span>

> <span data-ttu-id="8014b-338">remplacement protégé void [DestroyWindowCore](#destroywindowcore)(HandleRef HWND)</span><span class="sxs-lookup"><span data-stu-id="8014b-338">protected override void [DestroyWindowCore](#destroywindowcore)(HandleRef hwnd)</span></span>

##### <span data-ttu-id="8014b-339">Parameters</span><span class="sxs-lookup"><span data-stu-id="8014b-339">Parameters</span></span>
* `hwnd` <span data-ttu-id="8014b-340">Notre HWND que nous devons détruire.</span><span class="sxs-lookup"><span data-stu-id="8014b-340">Our HWND that we need to destroy.</span></span>

#### <span data-ttu-id="8014b-341">Suppression</span><span class="sxs-lookup"><span data-stu-id="8014b-341">Dispose</span></span> 

<span data-ttu-id="8014b-342">C’est appelé par notre classe de base en fonction de l’implémentation type du modèle IDispose.</span><span class="sxs-lookup"><span data-stu-id="8014b-342">This is called by our base class according to the typical implementation of the IDispose pattern.</span></span>

> <span data-ttu-id="8014b-343">remplacement protégé void [dispose](#dispose)(bool disposer)</span><span class="sxs-lookup"><span data-stu-id="8014b-343">protected override void [Dispose](#dispose)(bool disposing)</span></span>

<span data-ttu-id="8014b-344">Nous nous mettons en œuvre en publiant toutes nos ressources COM sous-jacentes, dont notre CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-344">We implement it by releasing all of our underlying COM resources, including our CoreWebView2.</span></span>

##### <span data-ttu-id="8014b-345">Parameters</span><span class="sxs-lookup"><span data-stu-id="8014b-345">Parameters</span></span>
* `disposing` <span data-ttu-id="8014b-346">True si un appelant appelle explicitement dispose et false s’il est finalisé.</span><span class="sxs-lookup"><span data-stu-id="8014b-346">True if a caller is explicitly calling Dispose, false if we're being finalized.</span></span>

#### <span data-ttu-id="8014b-347">HasFocusWithinCore</span><span class="sxs-lookup"><span data-stu-id="8014b-347">HasFocusWithinCore</span></span> 

<span data-ttu-id="8014b-348">Il est substitué de HwndHost et est appelé lorsque WPF a besoin de savoir si le focus se trouve dans notre contrôle/fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8014b-348">This is overridden from HwndHost and is called when WPF needs to know if the focus is in our control/window.</span></span>

> <span data-ttu-id="8014b-349">remplacement protégé bool [HasFocusWithinCore](#hasfocuswithincore)()</span><span class="sxs-lookup"><span data-stu-id="8014b-349">protected override bool [HasFocusWithinCore](#hasfocuswithincore)()</span></span>

<span data-ttu-id="8014b-350">Dans la mesure où il s’agit de l’hébergement d’une fenêtre non-WPF, WPF ne peut pas le connaître en appelant cette fonction.</span><span class="sxs-lookup"><span data-stu-id="8014b-350">WPF can't know on its own since we're hosting a non-WPF window, so instead it asks us by calling this.</span></span> <span data-ttu-id="8014b-351">Pour répondre, nous effectuons simplement le suivi de l’État en fonction des événements CoreWebView2 qui sont déclenchés quand il gagne ou perd du focus.</span><span class="sxs-lookup"><span data-stu-id="8014b-351">To answer, we just track state based on CoreWebView2 events that fire when it gains or loses focus.</span></span>

##### <span data-ttu-id="8014b-352">Renvoie</span><span class="sxs-lookup"><span data-stu-id="8014b-352">Returns</span></span>
<span data-ttu-id="8014b-353">True si le focus se trouve dans notre contrôle/fenêtre, false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8014b-353">True if the focus is in our control/window, false if it isn't.</span></span>

#### <span data-ttu-id="8014b-354">OnKeyDown</span><span class="sxs-lookup"><span data-stu-id="8014b-354">OnKeyDown</span></span> 

<span data-ttu-id="8014b-355">Il est substitué de UIElement et appelé pour nous permettre de traiter les entrées de la pression de touche.</span><span class="sxs-lookup"><span data-stu-id="8014b-355">This is overridden from UIElement and called to allow us to handle key press input.</span></span>

> <span data-ttu-id="8014b-356">remplacement protégé void [OnKeyDown](#onkeydown)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="8014b-356">protected override void [OnKeyDown](#onkeydown)(KeyEventArgs e)</span></span>

<span data-ttu-id="8014b-357">WPF ne doit jamais réellement appeler cet élément en réponse à des événements de clavier, car nous hébergeons une fenêtre qui n’est pas WPF.</span><span class="sxs-lookup"><span data-stu-id="8014b-357">WPF should never actually call this in response to keyboard events because we're hosting a non-WPF window.</span></span> <span data-ttu-id="8014b-358">Lorsque notre fenêtre comporte des fenêtres de focalisation, celles-ci s’envoient directement au lieu de la fenêtre de niveau supérieur et du système d’entrée de WPF.</span><span class="sxs-lookup"><span data-stu-id="8014b-358">When our window has focus Windows will send the input directly to it rather than to WPF's top-level window and input system.</span></span> <span data-ttu-id="8014b-359">Cette substitution ne doit être appelée que lorsque nous transférons explicitement l’entrée de touche d’accès rapide du CoreWebView2 vers WPF (dans CoreWebView2Controller_AcceleratorKeyPressed).</span><span class="sxs-lookup"><span data-stu-id="8014b-359">This override should only be called when we're explicitly forwarding accelerator key input from the CoreWebView2 to WPF (in CoreWebView2Controller_AcceleratorKeyPressed).</span></span> <span data-ttu-id="8014b-360">Même alors, ce KeyDownEvent est déclenché, car notre implémentation de PreviewKeyDownEvent l’a explicitement déclenché, en correspondant au système habituel de WPF.</span><span class="sxs-lookup"><span data-stu-id="8014b-360">Even then, this KeyDownEvent is only triggered because our PreviewKeyDownEvent implementation explicitly triggers it, matching WPF's usual system.</span></span> <span data-ttu-id="8014b-361">Le processus est le suivant: CoreWebView2Controller_AcceleratorKeyPressed-> lever PreviewKeyDownEvent-> OnPreviewKeyDown-> lever KeyDownEvent-> OnKeyDown</span><span class="sxs-lookup"><span data-stu-id="8014b-361">So the process is: CoreWebView2Controller_AcceleratorKeyPressed -> raise PreviewKeyDownEvent -> OnPreviewKeyDown -> raise KeyDownEvent -> OnKeyDown</span></span>

#### <span data-ttu-id="8014b-362">OnKeyUp</span><span class="sxs-lookup"><span data-stu-id="8014b-362">OnKeyUp</span></span> 

<span data-ttu-id="8014b-363">Voir OnKeyDown.</span><span class="sxs-lookup"><span data-stu-id="8014b-363">See OnKeyDown.</span></span>

> <span data-ttu-id="8014b-364">l' [annulation de](#onkeyup)la substitution protégée</span><span class="sxs-lookup"><span data-stu-id="8014b-364">protected override void [OnKeyUp](#onkeyup)(KeyEventArgs e)</span></span>

#### <span data-ttu-id="8014b-365">OnPreviewKeyDown</span><span class="sxs-lookup"><span data-stu-id="8014b-365">OnPreviewKeyDown</span></span> 

<span data-ttu-id="8014b-366">Il s’agit de la version d’évaluation («Preview») (c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="8014b-366">This is the "Preview" (i.e.</span></span>

> <span data-ttu-id="8014b-367">remplacement protégé void [OnPreviewKeyDown](#onpreviewkeydown)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="8014b-367">protected override void [OnPreviewKeyDown](#onpreviewkeydown)(KeyEventArgs e)</span></span>

<span data-ttu-id="8014b-368">Tunneling) de OnKeyDown, ce qui fait qu’il se produit en premier.</span><span class="sxs-lookup"><span data-stu-id="8014b-368">tunneling) version of OnKeyDown, so it actually happens first.</span></span> <span data-ttu-id="8014b-369">Comme OnKeyDown, il n’est jamais possible d’appeler uniquement si nous transférons explicitement les touches d’appui du CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8014b-369">Like OnKeyDown, this will only ever be called if we're explicitly forwarding key presses from the CoreWebView2.</span></span> <span data-ttu-id="8014b-370">Pour imiter la gestion des entrées standard de WPF, lorsque nous avons reçu ce message, nous nous réactivons et nous déclenchons le KeyDownEvent de propagation standard.</span><span class="sxs-lookup"><span data-stu-id="8014b-370">In order to mimic WPF's standard input handling, when we receive this we turn around and fire off the standard bubbling KeyDownEvent.</span></span> <span data-ttu-id="8014b-371">Ainsi, les autres utilisateurs de l’arborescence WPF peuvent voir la même paire standard d’événements d’entrée que si le WPF lui-même aurait déclenché le déclenchement d’une pression sur la touche.</span><span class="sxs-lookup"><span data-stu-id="8014b-371">That way others in the WPF tree see the same standard pair of input events that WPF itself would have triggered if it were handling the key press.</span></span>

#### <span data-ttu-id="8014b-372">OnPreviewKeyUp</span><span class="sxs-lookup"><span data-stu-id="8014b-372">OnPreviewKeyUp</span></span> 

<span data-ttu-id="8014b-373">Voir OnPreviewKeyDown.</span><span class="sxs-lookup"><span data-stu-id="8014b-373">See OnPreviewKeyDown.</span></span>

> <span data-ttu-id="8014b-374">remplacement protégé void [OnPreviewKeyUp](#onpreviewkeyup)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="8014b-374">protected override void [OnPreviewKeyUp](#onpreviewkeyup)(KeyEventArgs e)</span></span>

#### <span data-ttu-id="8014b-375">OnWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="8014b-375">OnWindowPositionChanged</span></span> 

<span data-ttu-id="8014b-376">Il est substitué de HwndHost et appelé lorsque l’emplacement de votre contrôle a changé.</span><span class="sxs-lookup"><span data-stu-id="8014b-376">This is overridden from HwndHost and called when our control's location has changed.</span></span>

> <span data-ttu-id="8014b-377">remplacement protégé void [OnWindowPositionChanged](#onwindowpositionchanged)(Rect rcBoundingBox)</span><span class="sxs-lookup"><span data-stu-id="8014b-377">protected override void [OnWindowPositionChanged](#onwindowpositionchanged)(Rect rcBoundingBox)</span></span>

<span data-ttu-id="8014b-378">Le HwndHost prend en charge la mise à jour de HWND que nous avons créé.</span><span class="sxs-lookup"><span data-stu-id="8014b-378">The HwndHost takes care of updating the HWND we created.</span></span> <span data-ttu-id="8014b-379">Ce que nous devons faire est de déplacer notre CoreWebView2 pour correspondre au nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="8014b-379">What we need to do is move our CoreWebView2 to match the new location.</span></span>

#### <span data-ttu-id="8014b-380">TabIntoCore</span><span class="sxs-lookup"><span data-stu-id="8014b-380">TabIntoCore</span></span> 

<span data-ttu-id="8014b-381">Il est alors substitué de HwndHost et est appelé pour nous informer que la touche de tabulation a entraîné le déplacement vers notre contrôle/fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8014b-381">This is overridden from HwndHost and is called to inform us that tabbing has caused the focus to move into our control/window.</span></span>

> <span data-ttu-id="8014b-382">substitution protégée [TabIntoCore](#tabintocore)(demande TraversalRequest)</span><span class="sxs-lookup"><span data-stu-id="8014b-382">protected override bool [TabIntoCore](#tabintocore)(TraversalRequest request)</span></span>

<span data-ttu-id="8014b-383">Dans la mesure où WPF ne peut pas gérer le changement de focus sur un HWND non WPF, il est délégué ici.</span><span class="sxs-lookup"><span data-stu-id="8014b-383">Since WPF can't manage the transition of focus to a non-WPF HWND, it delegates the transition to us here.</span></span> <span data-ttu-id="8014b-384">C’est pourquoi notre travail consiste simplement à placer le focus sur notre HWND externe.</span><span class="sxs-lookup"><span data-stu-id="8014b-384">So our job is just to place the focus in our external HWND.</span></span>

##### <span data-ttu-id="8014b-385">Parameters</span><span class="sxs-lookup"><span data-stu-id="8014b-385">Parameters</span></span>
* `request` <span data-ttu-id="8014b-386">Informations sur le déplacement du focus.</span><span class="sxs-lookup"><span data-stu-id="8014b-386">Information about how the focus is moving.</span></span>

##### <span data-ttu-id="8014b-387">Renvoie</span><span class="sxs-lookup"><span data-stu-id="8014b-387">Returns</span></span>
<span data-ttu-id="8014b-388">True pour indiquer que nous avons géré la navigation ou false pour indiquer que ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="8014b-388">True to indicate that we handled the navigation, or false to indicate that we didn't.</span></span>

