---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 3885556af38e2cef83e4147319f83f567c0cebd4
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884070"
---
# <span data-ttu-id="61d51-104">0.9.515-interface ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="61d51-104">0.9.515 - interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="61d51-105">Arguments d’événement pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="61d51-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="61d51-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="61d51-106">Summary</span></span>

 <span data-ttu-id="61d51-107">Ses</span><span class="sxs-lookup"><span data-stu-id="61d51-107">Members</span></span>                        | <span data-ttu-id="61d51-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="61d51-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="61d51-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="61d51-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="61d51-110">Détermine si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="61d51-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="61d51-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="61d51-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="61d51-112">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="61d51-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="61d51-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="61d51-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="61d51-114">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="61d51-114">Gets the new window.</span></span>
[<span data-ttu-id="61d51-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="61d51-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="61d51-116">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="61d51-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="61d51-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="61d51-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="61d51-118">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="61d51-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="61d51-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="61d51-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="61d51-120">Détermine si le NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="61d51-120">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="61d51-121">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="61d51-121">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="61d51-122">Définit un WebView comme résultat du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="61d51-122">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="61d51-123">L’événement est déclenché lorsque le contenu de l’affichage WebView est demandé à une nouvelle fenêtre (via Window. Open () et ainsi de suite.)</span><span class="sxs-lookup"><span data-stu-id="61d51-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="61d51-124">Ses</span><span class="sxs-lookup"><span data-stu-id="61d51-124">Members</span></span>

#### <span data-ttu-id="61d51-125">get_Handled</span><span class="sxs-lookup"><span data-stu-id="61d51-125">get_Handled</span></span> 

<span data-ttu-id="61d51-126">Détermine si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="61d51-126">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="61d51-127">[get_Handled](#get_handled)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="61d51-127">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="61d51-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="61d51-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="61d51-129">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="61d51-129">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="61d51-130">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="61d51-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="61d51-131">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="61d51-131">get_NewWindow</span></span> 

<span data-ttu-id="61d51-132">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="61d51-132">Gets the new window.</span></span>

> <span data-ttu-id="61d51-133">[get_NewWindow](#get_newwindow)publique HRESULT ([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="61d51-133">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="61d51-134">get_Uri</span><span class="sxs-lookup"><span data-stu-id="61d51-134">get_Uri</span></span> 

<span data-ttu-id="61d51-135">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="61d51-135">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="61d51-136">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="61d51-136">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="61d51-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="61d51-137">GetDeferral</span></span> 

<span data-ttu-id="61d51-138">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="61d51-138">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="61d51-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="61d51-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="61d51-140">Vous pouvez utiliser l’objet [ICoreWebView2Deferral](icorewebview2deferral.md) pour terminer la requête d’ouverture de fenêtre ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="61d51-140">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="61d51-141">Même si cet événement est différé, la fenêtre d’ouverture sera renvoyée en tant que WindowProxy dans une fenêtre sans navigation, ce qui vous permettra de naviguer à l’issue du report.</span><span class="sxs-lookup"><span data-stu-id="61d51-141">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="61d51-142">put_Handled</span><span class="sxs-lookup"><span data-stu-id="61d51-142">put_Handled</span></span> 

<span data-ttu-id="61d51-143">Détermine si le NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="61d51-143">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="61d51-144">[put_Handleds](#put_handled)HRESULT publiques (bool géré)</span><span class="sxs-lookup"><span data-stu-id="61d51-144">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="61d51-145">S’il s’agit d’une valeur false et qu’aucune NewWindow n’est définie, le WebView ouvrira une fenêtre contextuelle et sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="61d51-145">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="61d51-146">Si elle a la valeur true et qu’aucune propriété NewWindow n’est définie pour un appel Window. Open, le WindowProxy ouvert sera destiné à un objet Window factice et aucune fenêtre ne sera chargée.</span><span class="sxs-lookup"><span data-stu-id="61d51-146">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="61d51-147">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="61d51-147">Default is false.</span></span>

#### <span data-ttu-id="61d51-148">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="61d51-148">put_NewWindow</span></span> 

<span data-ttu-id="61d51-149">Définit un WebView comme résultat du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="61d51-149">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="61d51-150">[put_NewWindow](#put_newwindow)par le biais du public HRESULT ([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="61d51-150">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="61d51-151">Le WebView cible ne doit pas être parcouru.</span><span class="sxs-lookup"><span data-stu-id="61d51-151">The target webview should not be navigated.</span></span> <span data-ttu-id="61d51-152">Si l’NewWindow est définie, sa fenêtre de niveau supérieur sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="61d51-152">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

