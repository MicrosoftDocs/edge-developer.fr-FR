---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2NewWindowRequestedEventArgs
ms.openlocfilehash: d1cf39fe71c4b00f10a14da8a65428eb24daa71f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011934"
---
# <span data-ttu-id="df554-104">interface ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="df554-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="df554-105">Arguments d’événement pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="df554-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="df554-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="df554-106">Summary</span></span>

 <span data-ttu-id="df554-107">Ses</span><span class="sxs-lookup"><span data-stu-id="df554-107">Members</span></span>                        | <span data-ttu-id="df554-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="df554-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="df554-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="df554-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="df554-110">Détermine si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="df554-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="df554-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="df554-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="df554-112">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="df554-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="df554-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="df554-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="df554-114">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="df554-114">Gets the new window.</span></span>
[<span data-ttu-id="df554-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="df554-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="df554-116">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="df554-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="df554-117">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="df554-117">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="df554-118">Fonctionnalités de fenêtre spécifiées par l’appel Window. Open.</span><span class="sxs-lookup"><span data-stu-id="df554-118">Window features specified by the window.open call.</span></span>
[<span data-ttu-id="df554-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="df554-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="df554-120">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="df554-120">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="df554-121">put_Handled</span><span class="sxs-lookup"><span data-stu-id="df554-121">put_Handled</span></span>](#put_handled) | <span data-ttu-id="df554-122">Détermine si le NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="df554-122">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="df554-123">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="df554-123">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="df554-124">Définit un WebView comme résultat du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="df554-124">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="df554-125">L’événement est déclenché lorsque le contenu de l’affichage WebView est demandé à une nouvelle fenêtre (via Window. Open () et ainsi de suite.)</span><span class="sxs-lookup"><span data-stu-id="df554-125">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="df554-126">Ses</span><span class="sxs-lookup"><span data-stu-id="df554-126">Members</span></span>

#### <span data-ttu-id="df554-127">get_Handled</span><span class="sxs-lookup"><span data-stu-id="df554-127">get_Handled</span></span> 

<span data-ttu-id="df554-128">Détermine si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="df554-128">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="df554-129">[get_Handled](#get_handled)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="df554-129">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="df554-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="df554-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="df554-131">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="df554-131">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="df554-132">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="df554-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="df554-133">Le bloqueur de fenêtres contextuelles Edge est désactivé pour WebView de sorte que l’application puisse utiliser cet indicateur pour bloquer les fenêtres contextuelles non-utilisateur.</span><span class="sxs-lookup"><span data-stu-id="df554-133">The Edge popup blocker is disabled for WebView so the app can use this flag to block non-user initiated popups.</span></span>

#### <span data-ttu-id="df554-134">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="df554-134">get_NewWindow</span></span> 

<span data-ttu-id="df554-135">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="df554-135">Gets the new window.</span></span>

> <span data-ttu-id="df554-136">[get_NewWindow](#get_newwindow)publique HRESULT ([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="df554-136">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="df554-137">get_Uri</span><span class="sxs-lookup"><span data-stu-id="df554-137">get_Uri</span></span> 

<span data-ttu-id="df554-138">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="df554-138">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="df554-139">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="df554-139">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="df554-140">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="df554-140">get_WindowFeatures</span></span> 

<span data-ttu-id="df554-141">Fonctionnalités de fenêtre spécifiées par l’appel Window. Open.</span><span class="sxs-lookup"><span data-stu-id="df554-141">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="df554-142">[get_WindowFeatures](#get_windowfeatures)par le biais du public HRESULT ([ICoreWebView2WindowFeatures](icorewebview2windowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="df554-142">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2WindowFeatures](icorewebview2windowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="df554-143">Ces fonctionnalités peuvent être envisagées pour le positionnement et le dimensionnement des nouvelles fenêtres WebView.</span><span class="sxs-lookup"><span data-stu-id="df554-143">These features can be considered for positioning and sizing of new webview windows.</span></span>

#### <span data-ttu-id="df554-144">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="df554-144">GetDeferral</span></span> 

<span data-ttu-id="df554-145">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="df554-145">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="df554-146">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="df554-146">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="df554-147">Vous pouvez utiliser l’objet [ICoreWebView2Deferral](icorewebview2deferral.md) pour terminer la requête d’ouverture de fenêtre ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="df554-147">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="df554-148">Même si cet événement est différé, la fenêtre d’ouverture sera renvoyée en tant que WindowProxy dans une fenêtre sans navigation, ce qui vous permettra de naviguer à l’issue du report.</span><span class="sxs-lookup"><span data-stu-id="df554-148">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="df554-149">put_Handled</span><span class="sxs-lookup"><span data-stu-id="df554-149">put_Handled</span></span> 

<span data-ttu-id="df554-150">Détermine si le NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="df554-150">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="df554-151">[put_Handleds](#put_handled)HRESULT publiques (bool géré)</span><span class="sxs-lookup"><span data-stu-id="df554-151">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="df554-152">S’il s’agit d’une valeur false et qu’aucune NewWindow n’est définie, le WebView ouvrira une fenêtre contextuelle et sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="df554-152">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="df554-153">Si elle a la valeur true et qu’aucune propriété NewWindow n’est définie pour un appel Window. Open, le WindowProxy ouvert sera destiné à un objet Window factice et aucune fenêtre ne sera chargée.</span><span class="sxs-lookup"><span data-stu-id="df554-153">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="df554-154">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="df554-154">Default is false.</span></span>

#### <span data-ttu-id="df554-155">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="df554-155">put_NewWindow</span></span> 

<span data-ttu-id="df554-156">Définit un WebView comme résultat du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="df554-156">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="df554-157">[put_NewWindow](#put_newwindow)par le biais du public HRESULT ([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="df554-157">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="df554-158">Le WebView cible ne doit pas être parcouru.</span><span class="sxs-lookup"><span data-stu-id="df554-158">The target WebView should not be navigated.</span></span> <span data-ttu-id="df554-159">Si l’NewWindow est définie, sa fenêtre de niveau supérieur sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="df554-159">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

