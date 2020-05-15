---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: cc64e805b0d929d71340d5a012e7848860c35f5c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653511"
---
# <span data-ttu-id="c9ad8-104">interface ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c9ad8-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="c9ad8-105">Arguments d’événement pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="c9ad8-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="c9ad8-106">Summary</span></span>

 <span data-ttu-id="c9ad8-107">Ses</span><span class="sxs-lookup"><span data-stu-id="c9ad8-107">Members</span></span>                        | <span data-ttu-id="c9ad8-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c9ad8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c9ad8-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="c9ad8-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="c9ad8-110">Détermine si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="c9ad8-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c9ad8-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="c9ad8-112">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="c9ad8-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="c9ad8-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="c9ad8-114">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-114">Gets the new window.</span></span>
[<span data-ttu-id="c9ad8-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="c9ad8-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="c9ad8-116">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="c9ad8-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c9ad8-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="c9ad8-118">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="c9ad8-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="c9ad8-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="c9ad8-120">Détermine si le NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-120">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="c9ad8-121">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="c9ad8-121">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="c9ad8-122">Définit un WebView comme résultat du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-122">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="c9ad8-123">L’événement est déclenché lorsque le contenu de l’affichage WebView est demandé à une nouvelle fenêtre (via Window. Open () et ainsi de suite.)</span><span class="sxs-lookup"><span data-stu-id="c9ad8-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="c9ad8-124">Ses</span><span class="sxs-lookup"><span data-stu-id="c9ad8-124">Members</span></span>

#### <span data-ttu-id="c9ad8-125">get_Handled</span><span class="sxs-lookup"><span data-stu-id="c9ad8-125">get_Handled</span></span> 

<span data-ttu-id="c9ad8-126">Détermine si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-126">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="c9ad8-127">[get_Handled](#get_handled)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="c9ad8-127">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="c9ad8-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c9ad8-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="c9ad8-129">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-129">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="c9ad8-130">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="c9ad8-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="c9ad8-131">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="c9ad8-131">get_NewWindow</span></span> 

<span data-ttu-id="c9ad8-132">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-132">Gets the new window.</span></span>

> <span data-ttu-id="c9ad8-133">[get_NewWindow](#get_newwindow)publique HRESULT ([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="c9ad8-133">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="c9ad8-134">get_Uri</span><span class="sxs-lookup"><span data-stu-id="c9ad8-134">get_Uri</span></span> 

<span data-ttu-id="c9ad8-135">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-135">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="c9ad8-136">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="c9ad8-136">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="c9ad8-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c9ad8-137">GetDeferral</span></span> 

<span data-ttu-id="c9ad8-138">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-138">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="c9ad8-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="c9ad8-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="c9ad8-140">Vous pouvez utiliser l’objet [ICoreWebView2Deferral](icorewebview2deferral.md) pour terminer la requête d’ouverture de fenêtre ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-140">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="c9ad8-141">Même si cet événement est différé, la fenêtre d’ouverture sera renvoyée en tant que WindowProxy dans une fenêtre sans navigation, ce qui vous permettra de naviguer à l’issue du report.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-141">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="c9ad8-142">put_Handled</span><span class="sxs-lookup"><span data-stu-id="c9ad8-142">put_Handled</span></span> 

<span data-ttu-id="c9ad8-143">Détermine si le NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-143">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="c9ad8-144">[put_Handleds](#put_handled)HRESULT publiques (bool géré)</span><span class="sxs-lookup"><span data-stu-id="c9ad8-144">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="c9ad8-145">S’il s’agit d’une valeur false et qu’aucune NewWindow n’est définie, le WebView ouvrira une fenêtre contextuelle et sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-145">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="c9ad8-146">Si elle a la valeur true et qu’aucune propriété NewWindow n’est définie pour un appel Window. Open, le WindowProxy ouvert sera destiné à un objet Window factice et aucune fenêtre ne sera chargée.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-146">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="c9ad8-147">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-147">Default is false.</span></span>

#### <span data-ttu-id="c9ad8-148">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="c9ad8-148">put_NewWindow</span></span> 

<span data-ttu-id="c9ad8-149">Définit un WebView comme résultat du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-149">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="c9ad8-150">[put_NewWindow](#put_newwindow)par le biais du public HRESULT ([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="c9ad8-150">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="c9ad8-151">Le WebView cible ne doit pas être parcouru.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-151">The target webview should not be navigated.</span></span> <span data-ttu-id="c9ad8-152">Si l’NewWindow est définie, sa fenêtre de niveau supérieur sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="c9ad8-152">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

