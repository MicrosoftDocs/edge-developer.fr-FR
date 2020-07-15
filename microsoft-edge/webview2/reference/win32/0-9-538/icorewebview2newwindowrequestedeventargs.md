---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2NewWindowRequestedEventArgs
ms.openlocfilehash: bb18b6662fd5921406e19b3c333c97f8a1cd0dbc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879435"
---
# <span data-ttu-id="aa0b0-104">interface ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="aa0b0-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="aa0b0-105">Arguments d’événement pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="aa0b0-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="aa0b0-106">Summary</span></span>

 <span data-ttu-id="aa0b0-107">Ses</span><span class="sxs-lookup"><span data-stu-id="aa0b0-107">Members</span></span>                        | <span data-ttu-id="aa0b0-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="aa0b0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aa0b0-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="aa0b0-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="aa0b0-110">Détermine si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="aa0b0-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="aa0b0-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="aa0b0-112">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="aa0b0-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="aa0b0-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="aa0b0-114">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-114">Gets the new window.</span></span>
[<span data-ttu-id="aa0b0-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="aa0b0-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="aa0b0-116">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="aa0b0-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="aa0b0-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="aa0b0-118">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="aa0b0-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="aa0b0-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="aa0b0-120">Détermine si le NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-120">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="aa0b0-121">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="aa0b0-121">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="aa0b0-122">Définit un WebView comme résultat du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-122">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="aa0b0-123">L’événement est déclenché lorsque le contenu de l’affichage WebView est demandé à une nouvelle fenêtre (via Window. Open () et ainsi de suite.)</span><span class="sxs-lookup"><span data-stu-id="aa0b0-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="aa0b0-124">Ses</span><span class="sxs-lookup"><span data-stu-id="aa0b0-124">Members</span></span>

#### <span data-ttu-id="aa0b0-125">get_Handled</span><span class="sxs-lookup"><span data-stu-id="aa0b0-125">get_Handled</span></span> 

<span data-ttu-id="aa0b0-126">Détermine si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-126">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="aa0b0-127">[get_Handled](#get_handled)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="aa0b0-127">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="aa0b0-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="aa0b0-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="aa0b0-129">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-129">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="aa0b0-130">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="aa0b0-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="aa0b0-131">Le bloqueur de fenêtres contextuelles Edge est désactivé pour WebView de sorte que l’application puisse utiliser cet indicateur pour bloquer les fenêtres contextuelles non-utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-131">The Edge popup blocker is disabled for WebView so the app can use this flag to block non-user initiated popups.</span></span>

#### <span data-ttu-id="aa0b0-132">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="aa0b0-132">get_NewWindow</span></span> 

<span data-ttu-id="aa0b0-133">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-133">Gets the new window.</span></span>

> <span data-ttu-id="aa0b0-134">[get_NewWindow](#get_newwindow)publique HRESULT ([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="aa0b0-134">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="aa0b0-135">get_Uri</span><span class="sxs-lookup"><span data-stu-id="aa0b0-135">get_Uri</span></span> 

<span data-ttu-id="aa0b0-136">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-136">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="aa0b0-137">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="aa0b0-137">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="aa0b0-138">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="aa0b0-138">GetDeferral</span></span> 

<span data-ttu-id="aa0b0-139">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-139">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="aa0b0-140">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="aa0b0-140">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="aa0b0-141">Vous pouvez utiliser l’objet [ICoreWebView2Deferral](icorewebview2deferral.md) pour terminer la requête d’ouverture de fenêtre ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-141">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="aa0b0-142">Même si cet événement est différé, la fenêtre d’ouverture sera renvoyée en tant que WindowProxy dans une fenêtre sans navigation, ce qui vous permettra de naviguer à l’issue du report.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-142">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="aa0b0-143">put_Handled</span><span class="sxs-lookup"><span data-stu-id="aa0b0-143">put_Handled</span></span> 

<span data-ttu-id="aa0b0-144">Détermine si le NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-144">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="aa0b0-145">[put_Handleds](#put_handled)HRESULT publiques (bool géré)</span><span class="sxs-lookup"><span data-stu-id="aa0b0-145">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="aa0b0-146">S’il s’agit d’une valeur false et qu’aucune NewWindow n’est définie, le WebView ouvrira une fenêtre contextuelle et sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-146">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="aa0b0-147">Si elle a la valeur true et qu’aucune propriété NewWindow n’est définie pour un appel Window. Open, le WindowProxy ouvert sera destiné à un objet Window factice et aucune fenêtre ne sera chargée.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-147">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="aa0b0-148">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-148">Default is false.</span></span>

#### <span data-ttu-id="aa0b0-149">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="aa0b0-149">put_NewWindow</span></span> 

<span data-ttu-id="aa0b0-150">Définit un WebView comme résultat du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-150">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="aa0b0-151">[put_NewWindow](#put_newwindow)par le biais du public HRESULT ([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="aa0b0-151">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="aa0b0-152">Le WebView cible ne doit pas être parcouru.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-152">The target webview should not be navigated.</span></span> <span data-ttu-id="aa0b0-153">Si l’NewWindow est définie, sa fenêtre de niveau supérieur sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-153">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

