---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: aeefa0257a273f0eecd99d3f666adc03be709d9a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880492"
---
# <span data-ttu-id="a42d7-104">0.9.515-interface ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a42d7-104">0.9.515 - interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="a42d7-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="a42d7-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="a42d7-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="a42d7-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="a42d7-107">Arguments d’événement pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="a42d7-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="a42d7-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="a42d7-108">Summary</span></span>

 <span data-ttu-id="a42d7-109">Ses</span><span class="sxs-lookup"><span data-stu-id="a42d7-109">Members</span></span>                        | <span data-ttu-id="a42d7-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="a42d7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a42d7-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="a42d7-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="a42d7-112">Détermine si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="a42d7-112">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="a42d7-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a42d7-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="a42d7-114">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="a42d7-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="a42d7-115">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="a42d7-115">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="a42d7-116">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a42d7-116">Gets the new window.</span></span>
[<span data-ttu-id="a42d7-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="a42d7-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="a42d7-118">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="a42d7-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="a42d7-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="a42d7-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="a42d7-120">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="a42d7-120">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="a42d7-121">put_Handled</span><span class="sxs-lookup"><span data-stu-id="a42d7-121">put_Handled</span></span>](#put_handled) | <span data-ttu-id="a42d7-122">Détermine si le NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="a42d7-122">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="a42d7-123">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="a42d7-123">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="a42d7-124">Définit un WebView comme résultat du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="a42d7-124">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="a42d7-125">L’événement est déclenché lorsque le contenu de l’affichage WebView est demandé à une nouvelle fenêtre (via Window. Open () et ainsi de suite.)</span><span class="sxs-lookup"><span data-stu-id="a42d7-125">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="a42d7-126">Ses</span><span class="sxs-lookup"><span data-stu-id="a42d7-126">Members</span></span>

#### <span data-ttu-id="a42d7-127">get_Handled</span><span class="sxs-lookup"><span data-stu-id="a42d7-127">get_Handled</span></span> 

<span data-ttu-id="a42d7-128">Détermine si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="a42d7-128">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="a42d7-129">[get_Handled](#get_handled)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="a42d7-129">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="a42d7-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a42d7-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="a42d7-131">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="a42d7-131">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="a42d7-132">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="a42d7-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="a42d7-133">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="a42d7-133">get_NewWindow</span></span> 

<span data-ttu-id="a42d7-134">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a42d7-134">Gets the new window.</span></span>

> <span data-ttu-id="a42d7-135">[get_NewWindow](#get_newwindow)publique HRESULT ([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="a42d7-135">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="a42d7-136">get_Uri</span><span class="sxs-lookup"><span data-stu-id="a42d7-136">get_Uri</span></span> 

<span data-ttu-id="a42d7-137">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="a42d7-137">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="a42d7-138">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="a42d7-138">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="a42d7-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="a42d7-139">GetDeferral</span></span> 

<span data-ttu-id="a42d7-140">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="a42d7-140">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="a42d7-141">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="a42d7-141">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="a42d7-142">Vous pouvez utiliser l’objet [ICoreWebView2Deferral](icorewebview2deferral.md) pour terminer la requête d’ouverture de fenêtre ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="a42d7-142">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="a42d7-143">Même si cet événement est différé, la fenêtre d’ouverture sera renvoyée en tant que WindowProxy dans une fenêtre sans navigation, ce qui vous permettra de naviguer à l’issue du report.</span><span class="sxs-lookup"><span data-stu-id="a42d7-143">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="a42d7-144">put_Handled</span><span class="sxs-lookup"><span data-stu-id="a42d7-144">put_Handled</span></span> 

<span data-ttu-id="a42d7-145">Détermine si le NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="a42d7-145">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="a42d7-146">[put_Handleds](#put_handled)HRESULT publiques (bool géré)</span><span class="sxs-lookup"><span data-stu-id="a42d7-146">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="a42d7-147">S’il s’agit d’une valeur false et qu’aucune NewWindow n’est définie, le WebView ouvrira une fenêtre contextuelle et sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="a42d7-147">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="a42d7-148">Si elle a la valeur true et qu’aucune propriété NewWindow n’est définie pour un appel Window. Open, le WindowProxy ouvert sera destiné à un objet Window factice et aucune fenêtre ne sera chargée.</span><span class="sxs-lookup"><span data-stu-id="a42d7-148">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="a42d7-149">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="a42d7-149">Default is false.</span></span>

#### <span data-ttu-id="a42d7-150">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="a42d7-150">put_NewWindow</span></span> 

<span data-ttu-id="a42d7-151">Définit un WebView comme résultat du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="a42d7-151">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="a42d7-152">[put_NewWindow](#put_newwindow)par le biais du public HRESULT ([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="a42d7-152">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="a42d7-153">Le WebView cible ne doit pas être parcouru.</span><span class="sxs-lookup"><span data-stu-id="a42d7-153">The target webview should not be navigated.</span></span> <span data-ttu-id="a42d7-154">Si l’NewWindow est définie, sa fenêtre de niveau supérieur sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="a42d7-154">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

