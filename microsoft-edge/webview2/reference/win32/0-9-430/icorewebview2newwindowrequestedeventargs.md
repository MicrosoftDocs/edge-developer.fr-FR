---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 73f62e7130d50028b527353c6ba1a238f694dcda
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885680"
---
# <span data-ttu-id="77307-104">0.9.430-interface ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="77307-104">0.9.430 - interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="77307-105">Arguments d’événement pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="77307-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="77307-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="77307-106">Summary</span></span>

 <span data-ttu-id="77307-107">Ses</span><span class="sxs-lookup"><span data-stu-id="77307-107">Members</span></span>                        | <span data-ttu-id="77307-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="77307-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="77307-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="77307-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="77307-110">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="77307-110">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="77307-111">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="77307-111">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="77307-112">Définit un WebView comme résultat du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="77307-112">Sets a WebView as a result of the NewWindowRequest.</span></span>
[<span data-ttu-id="77307-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="77307-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="77307-114">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="77307-114">Gets the new window.</span></span>
[<span data-ttu-id="77307-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="77307-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="77307-116">Détermine si le NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="77307-116">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="77307-117">get_Handled</span><span class="sxs-lookup"><span data-stu-id="77307-117">get_Handled</span></span>](#get_handled) | <span data-ttu-id="77307-118">Détermine si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="77307-118">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="77307-119">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="77307-119">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="77307-120">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="77307-120">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="77307-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="77307-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="77307-122">Obtenez un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="77307-122">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

<span data-ttu-id="77307-123">L’événement est déclenché lorsque le contenu de l’affichage WebView est demandé à une nouvelle fenêtre (via Window. Open () etc.)</span><span class="sxs-lookup"><span data-stu-id="77307-123">The event is fired when content inside webview requested to a open a new window (through window.open() etc.)</span></span>

## <span data-ttu-id="77307-124">Ses</span><span class="sxs-lookup"><span data-stu-id="77307-124">Members</span></span>

#### <span data-ttu-id="77307-125">get_Uri</span><span class="sxs-lookup"><span data-stu-id="77307-125">get_Uri</span></span> 

<span data-ttu-id="77307-126">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="77307-126">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="77307-127">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="77307-127">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="77307-128">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="77307-128">put_NewWindow</span></span> 

<span data-ttu-id="77307-129">Définit un WebView comme résultat du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="77307-129">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="77307-130">[put_NewWindow](#put_newwindow)par le biais du public HRESULT ([ICoreWebView2](ICoreWebView2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="77307-130">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](ICoreWebView2.md) \* newWindow)</span></span>

<span data-ttu-id="77307-131">Le WebView cible ne doit pas être parcouru.</span><span class="sxs-lookup"><span data-stu-id="77307-131">The target webview should not be navigated.</span></span> <span data-ttu-id="77307-132">Si l’NewWindow est définie, sa fenêtre de niveau supérieur sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="77307-132">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="77307-133">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="77307-133">get_NewWindow</span></span> 

<span data-ttu-id="77307-134">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="77307-134">Gets the new window.</span></span>

> <span data-ttu-id="77307-135">[get_NewWindow](#get_newwindow)publique HRESULT ([ICoreWebView2](ICoreWebView2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="77307-135">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](ICoreWebView2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="77307-136">put_Handled</span><span class="sxs-lookup"><span data-stu-id="77307-136">put_Handled</span></span> 

<span data-ttu-id="77307-137">Détermine si le NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="77307-137">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="77307-138">[put_Handleds](#put_handled)HRESULT publiques (bool géré)</span><span class="sxs-lookup"><span data-stu-id="77307-138">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="77307-139">S’il s’agit d’une valeur false et qu’aucune NewWindow n’est définie, le WebView ouvrira une fenêtre contextuelle et sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="77307-139">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="77307-140">Si elle a la valeur true et qu’aucune propriété NewWindow n’est définie pour un appel Window. Open, le WindowProxy ouvert sera destiné à un objet Window factice et aucune fenêtre ne sera chargée.</span><span class="sxs-lookup"><span data-stu-id="77307-140">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="77307-141">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="77307-141">Default is false.</span></span>

#### <span data-ttu-id="77307-142">get_Handled</span><span class="sxs-lookup"><span data-stu-id="77307-142">get_Handled</span></span> 

<span data-ttu-id="77307-143">Détermine si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="77307-143">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="77307-144">[get_Handled](#get_handled)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="77307-144">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="77307-145">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="77307-145">get_IsUserInitiated</span></span> 

<span data-ttu-id="77307-146">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="77307-146">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="77307-147">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="77307-147">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="77307-148">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="77307-148">GetDeferral</span></span> 

<span data-ttu-id="77307-149">Obtenez un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="77307-149">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="77307-150">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="77307-150">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="77307-151">Vous pouvez utiliser l’objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) pour terminer la requête d’ouverture de fenêtre ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="77307-151">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="77307-152">Même si cet événement est différé, la fenêtre d’ouverture sera renvoyée en tant que WindowProxy dans une fenêtre sans navigation, ce qui vous permettra de naviguer à l’issue du report.</span><span class="sxs-lookup"><span data-stu-id="77307-152">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

