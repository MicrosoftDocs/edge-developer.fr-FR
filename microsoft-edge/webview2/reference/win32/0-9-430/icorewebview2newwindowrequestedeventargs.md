---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 2ea3500c5e230b543f75241c47c58163276942da
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653493"
---
# <span data-ttu-id="d235a-104">interface ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d235a-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="d235a-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="d235a-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="d235a-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="d235a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="d235a-107">Arguments d’événement pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="d235a-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="d235a-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="d235a-108">Summary</span></span>

 <span data-ttu-id="d235a-109">Ses</span><span class="sxs-lookup"><span data-stu-id="d235a-109">Members</span></span>                        | <span data-ttu-id="d235a-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d235a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d235a-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="d235a-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="d235a-112">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="d235a-112">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="d235a-113">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="d235a-113">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="d235a-114">Définit un WebView comme résultat du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="d235a-114">Sets a WebView as a result of the NewWindowRequest.</span></span>
[<span data-ttu-id="d235a-115">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="d235a-115">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="d235a-116">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d235a-116">Gets the new window.</span></span>
[<span data-ttu-id="d235a-117">put_Handled</span><span class="sxs-lookup"><span data-stu-id="d235a-117">put_Handled</span></span>](#put_handled) | <span data-ttu-id="d235a-118">Détermine si le NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="d235a-118">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="d235a-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="d235a-119">get_Handled</span></span>](#get_handled) | <span data-ttu-id="d235a-120">Détermine si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="d235a-120">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="d235a-121">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="d235a-121">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="d235a-122">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="d235a-122">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="d235a-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d235a-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="d235a-124">Obtenez un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="d235a-124">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

<span data-ttu-id="d235a-125">L’événement est déclenché lorsque le contenu de l’affichage WebView est demandé à une nouvelle fenêtre (via Window. Open () etc.)</span><span class="sxs-lookup"><span data-stu-id="d235a-125">The event is fired when content inside webview requested to a open a new window (through window.open() etc.)</span></span>

## <span data-ttu-id="d235a-126">Ses</span><span class="sxs-lookup"><span data-stu-id="d235a-126">Members</span></span>

#### <span data-ttu-id="d235a-127">get_Uri</span><span class="sxs-lookup"><span data-stu-id="d235a-127">get_Uri</span></span> 

<span data-ttu-id="d235a-128">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="d235a-128">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="d235a-129">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="d235a-129">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="d235a-130">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="d235a-130">put_NewWindow</span></span> 

<span data-ttu-id="d235a-131">Définit un WebView comme résultat du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="d235a-131">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="d235a-132">[put_NewWindow](#put_newwindow)par le biais du public HRESULT ([ICoreWebView2](ICoreWebView2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="d235a-132">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](ICoreWebView2.md) \* newWindow)</span></span>

<span data-ttu-id="d235a-133">Le WebView cible ne doit pas être parcouru.</span><span class="sxs-lookup"><span data-stu-id="d235a-133">The target webview should not be navigated.</span></span> <span data-ttu-id="d235a-134">Si l’NewWindow est définie, sa fenêtre de niveau supérieur sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="d235a-134">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="d235a-135">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="d235a-135">get_NewWindow</span></span> 

<span data-ttu-id="d235a-136">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d235a-136">Gets the new window.</span></span>

> <span data-ttu-id="d235a-137">[get_NewWindow](#get_newwindow)publique HRESULT ([ICoreWebView2](ICoreWebView2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="d235a-137">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](ICoreWebView2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="d235a-138">put_Handled</span><span class="sxs-lookup"><span data-stu-id="d235a-138">put_Handled</span></span> 

<span data-ttu-id="d235a-139">Détermine si le NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="d235a-139">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="d235a-140">[put_Handleds](#put_handled)HRESULT publiques (bool géré)</span><span class="sxs-lookup"><span data-stu-id="d235a-140">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="d235a-141">S’il s’agit d’une valeur false et qu’aucune NewWindow n’est définie, le WebView ouvrira une fenêtre contextuelle et sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="d235a-141">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="d235a-142">Si elle a la valeur true et qu’aucune propriété NewWindow n’est définie pour un appel Window. Open, le WindowProxy ouvert sera destiné à un objet Window factice et aucune fenêtre ne sera chargée.</span><span class="sxs-lookup"><span data-stu-id="d235a-142">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="d235a-143">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="d235a-143">Default is false.</span></span>

#### <span data-ttu-id="d235a-144">get_Handled</span><span class="sxs-lookup"><span data-stu-id="d235a-144">get_Handled</span></span> 

<span data-ttu-id="d235a-145">Détermine si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="d235a-145">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="d235a-146">[get_Handled](#get_handled)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="d235a-146">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="d235a-147">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="d235a-147">get_IsUserInitiated</span></span> 

<span data-ttu-id="d235a-148">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="d235a-148">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="d235a-149">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="d235a-149">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="d235a-150">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d235a-150">GetDeferral</span></span> 

<span data-ttu-id="d235a-151">Obtenez un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="d235a-151">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="d235a-152">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="d235a-152">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="d235a-153">Vous pouvez utiliser l’objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) pour terminer la requête d’ouverture de fenêtre ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d235a-153">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="d235a-154">Même si cet événement est différé, la fenêtre d’ouverture sera renvoyée en tant que WindowProxy dans une fenêtre sans navigation, ce qui vous permettra de naviguer à l’issue du report.</span><span class="sxs-lookup"><span data-stu-id="d235a-154">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

