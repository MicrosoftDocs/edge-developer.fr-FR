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
ms.openlocfilehash: b0b868b99d3f77679b3684a20e7744d7a22fd715
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653446"
---
# <span data-ttu-id="6bba7-104">interface ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="6bba7-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="6bba7-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="6bba7-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="6bba7-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="6bba7-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="6bba7-107">Arguments d’événement pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="6bba7-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="6bba7-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="6bba7-108">Summary</span></span>

 <span data-ttu-id="6bba7-109">Ses</span><span class="sxs-lookup"><span data-stu-id="6bba7-109">Members</span></span>                        | <span data-ttu-id="6bba7-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6bba7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6bba7-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="6bba7-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="6bba7-112">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="6bba7-112">The uri of the requested navigation.</span></span>
[<span data-ttu-id="6bba7-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6bba7-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="6bba7-114">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="6bba7-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="6bba7-115">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="6bba7-115">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="6bba7-116">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="6bba7-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="6bba7-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="6bba7-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="6bba7-118">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="6bba7-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="6bba7-119">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="6bba7-119">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="6bba7-120">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="6bba7-120">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="6bba7-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="6bba7-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="6bba7-122">Définissez la propriété Cancel.</span><span class="sxs-lookup"><span data-stu-id="6bba7-122">Set the Cancel property.</span></span>
[<span data-ttu-id="6bba7-123">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="6bba7-123">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="6bba7-124">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="6bba7-124">The ID of the navigation.</span></span>

## <span data-ttu-id="6bba7-125">Ses</span><span class="sxs-lookup"><span data-stu-id="6bba7-125">Members</span></span>

#### <span data-ttu-id="6bba7-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="6bba7-126">get_Uri</span></span> 

<span data-ttu-id="6bba7-127">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="6bba7-127">The uri of the requested navigation.</span></span>

> <span data-ttu-id="6bba7-128">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="6bba7-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="6bba7-129">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6bba7-129">get_IsUserInitiated</span></span> 

<span data-ttu-id="6bba7-130">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="6bba7-130">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="6bba7-131">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="6bba7-131">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="6bba7-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="6bba7-132">get_IsRedirected</span></span> 

<span data-ttu-id="6bba7-133">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="6bba7-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="6bba7-134">valeur publique HRESULT [get_IsRedirected](#get_isredirected)(bool \* IsRedirected)</span><span class="sxs-lookup"><span data-stu-id="6bba7-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="6bba7-135">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="6bba7-135">get_RequestHeaders</span></span> 

<span data-ttu-id="6bba7-136">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="6bba7-136">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="6bba7-137">[get_RequestHeaders](#get_requestheaders)par le biais du public HRESULT ([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \* requestHeaders)</span><span class="sxs-lookup"><span data-stu-id="6bba7-137">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="6bba7-138">Remarque: vous ne pouvez pas modifier les en-têtes de requête HTTP dans un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="6bba7-138">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="6bba7-139">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="6bba7-139">get_Cancel</span></span> 

<span data-ttu-id="6bba7-140">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="6bba7-140">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="6bba7-141">valeur publique HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="6bba7-141">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="6bba7-142">S’il est défini, il sera comme si la navigation ne s’est jamais produite et le contenu de la page active sera intact.</span><span class="sxs-lookup"><span data-stu-id="6bba7-142">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="6bba7-143">Pour des raisons de performances, les requêtes HTTP peuvent se produire alors que l’hôte répond.</span><span class="sxs-lookup"><span data-stu-id="6bba7-143">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="6bba7-144">Cela signifie que les cookies peuvent être définis et utilisés dans le cadre d’une demande de navigation.</span><span class="sxs-lookup"><span data-stu-id="6bba7-144">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="6bba7-145">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="6bba7-145">put_Cancel</span></span> 

<span data-ttu-id="6bba7-146">Définissez la propriété Cancel.</span><span class="sxs-lookup"><span data-stu-id="6bba7-146">Set the Cancel property.</span></span>

> <span data-ttu-id="6bba7-147">[put_Cancel](#put_cancel)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="6bba7-147">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

#### <span data-ttu-id="6bba7-148">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="6bba7-148">get_NavigationId</span></span> 

<span data-ttu-id="6bba7-149">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="6bba7-149">The ID of the navigation.</span></span>

> <span data-ttu-id="6bba7-150">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="6bba7-150">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

