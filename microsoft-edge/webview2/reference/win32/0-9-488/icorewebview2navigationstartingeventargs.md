---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 9aa44483fc824f8a26af6293f031c58d681de624
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880471"
---
# <span data-ttu-id="ae55c-104">0.9.515-interface ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="ae55c-104">0.9.515 - interface ICoreWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="ae55c-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="ae55c-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="ae55c-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="ae55c-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="ae55c-107">Arguments d’événement pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="ae55c-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="ae55c-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="ae55c-108">Summary</span></span>

 <span data-ttu-id="ae55c-109">Ses</span><span class="sxs-lookup"><span data-stu-id="ae55c-109">Members</span></span>                        | <span data-ttu-id="ae55c-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="ae55c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ae55c-111">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="ae55c-111">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="ae55c-112">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="ae55c-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="ae55c-113">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="ae55c-113">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="ae55c-114">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="ae55c-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="ae55c-115">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ae55c-115">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="ae55c-116">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="ae55c-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="ae55c-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="ae55c-117">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="ae55c-118">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="ae55c-118">The ID of the navigation.</span></span>
[<span data-ttu-id="ae55c-119">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="ae55c-119">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="ae55c-120">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="ae55c-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="ae55c-121">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ae55c-121">get_Uri</span></span>](#get_uri) | <span data-ttu-id="ae55c-122">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="ae55c-122">The uri of the requested navigation.</span></span>
[<span data-ttu-id="ae55c-123">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="ae55c-123">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="ae55c-124">Définissez la propriété Cancel.</span><span class="sxs-lookup"><span data-stu-id="ae55c-124">Set the Cancel property.</span></span>

## <span data-ttu-id="ae55c-125">Ses</span><span class="sxs-lookup"><span data-stu-id="ae55c-125">Members</span></span>

#### <span data-ttu-id="ae55c-126">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="ae55c-126">get_Cancel</span></span> 

<span data-ttu-id="ae55c-127">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="ae55c-127">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="ae55c-128">valeur publique HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="ae55c-128">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="ae55c-129">S’il est défini, il sera comme si la navigation ne s’est jamais produite et le contenu de la page active sera intact.</span><span class="sxs-lookup"><span data-stu-id="ae55c-129">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="ae55c-130">Pour des raisons de performances, les requêtes HTTP peuvent se produire alors que l’hôte répond.</span><span class="sxs-lookup"><span data-stu-id="ae55c-130">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="ae55c-131">Cela signifie que les cookies peuvent être définis et utilisés dans le cadre d’une demande de navigation.</span><span class="sxs-lookup"><span data-stu-id="ae55c-131">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="ae55c-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="ae55c-132">get_IsRedirected</span></span> 

<span data-ttu-id="ae55c-133">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="ae55c-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="ae55c-134">valeur publique HRESULT [get_IsRedirected](#get_isredirected)(bool \* IsRedirected)</span><span class="sxs-lookup"><span data-stu-id="ae55c-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="ae55c-135">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ae55c-135">get_IsUserInitiated</span></span> 

<span data-ttu-id="ae55c-136">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="ae55c-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="ae55c-137">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="ae55c-137">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="ae55c-138">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="ae55c-138">get_NavigationId</span></span> 

<span data-ttu-id="ae55c-139">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="ae55c-139">The ID of the navigation.</span></span>

> <span data-ttu-id="ae55c-140">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="ae55c-140">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="ae55c-141">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="ae55c-141">get_RequestHeaders</span></span> 

<span data-ttu-id="ae55c-142">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="ae55c-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="ae55c-143">[get_RequestHeaders](#get_requestheaders)par le biais du public HRESULT ([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* requestHeaders)</span><span class="sxs-lookup"><span data-stu-id="ae55c-143">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="ae55c-144">Remarque: vous ne pouvez pas modifier les en-têtes de requête HTTP dans un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="ae55c-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="ae55c-145">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ae55c-145">get_Uri</span></span> 

<span data-ttu-id="ae55c-146">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="ae55c-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="ae55c-147">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="ae55c-147">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="ae55c-148">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="ae55c-148">put_Cancel</span></span> 

<span data-ttu-id="ae55c-149">Définissez la propriété Cancel.</span><span class="sxs-lookup"><span data-stu-id="ae55c-149">Set the Cancel property.</span></span>

> <span data-ttu-id="ae55c-150">[put_Cancel](#put_cancel)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="ae55c-150">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

