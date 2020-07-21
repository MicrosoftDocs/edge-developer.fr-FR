---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: a9219266412c2872d9236ef93ce0e03e2dd5f7f2
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886396"
---
# <span data-ttu-id="7f3c2-104">0.9.515-interface ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="7f3c2-104">0.9.515 - interface ICoreWebView2NavigationStartingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="7f3c2-105">Arguments d’événement pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="7f3c2-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="7f3c2-106">Summary</span></span>

 <span data-ttu-id="7f3c2-107">Ses</span><span class="sxs-lookup"><span data-stu-id="7f3c2-107">Members</span></span>                        | <span data-ttu-id="7f3c2-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="7f3c2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7f3c2-109">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="7f3c2-109">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="7f3c2-110">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-110">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="7f3c2-111">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="7f3c2-111">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="7f3c2-112">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-112">True when the navigation is redirected.</span></span>
[<span data-ttu-id="7f3c2-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="7f3c2-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="7f3c2-114">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="7f3c2-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="7f3c2-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="7f3c2-116">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-116">The ID of the navigation.</span></span>
[<span data-ttu-id="7f3c2-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="7f3c2-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="7f3c2-118">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="7f3c2-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="7f3c2-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="7f3c2-120">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-120">The uri of the requested navigation.</span></span>
[<span data-ttu-id="7f3c2-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="7f3c2-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="7f3c2-122">Définissez la propriété Cancel.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-122">Set the Cancel property.</span></span>

## <span data-ttu-id="7f3c2-123">Ses</span><span class="sxs-lookup"><span data-stu-id="7f3c2-123">Members</span></span>

#### <span data-ttu-id="7f3c2-124">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="7f3c2-124">get_Cancel</span></span> 

<span data-ttu-id="7f3c2-125">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="7f3c2-126">valeur publique HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="7f3c2-126">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="7f3c2-127">S’il est défini, il sera comme si la navigation ne s’est jamais produite et le contenu de la page active sera intact.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="7f3c2-128">Pour des raisons de performances, les requêtes HTTP peuvent se produire alors que l’hôte répond.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="7f3c2-129">Cela signifie que les cookies peuvent être définis et utilisés dans le cadre d’une demande de navigation.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="7f3c2-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="7f3c2-130">get_IsRedirected</span></span> 

<span data-ttu-id="7f3c2-131">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="7f3c2-132">valeur publique HRESULT [get_IsRedirected](#get_isredirected)(bool \* IsRedirected)</span><span class="sxs-lookup"><span data-stu-id="7f3c2-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="7f3c2-133">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="7f3c2-133">get_IsUserInitiated</span></span> 

<span data-ttu-id="7f3c2-134">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="7f3c2-135">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="7f3c2-135">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="7f3c2-136">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="7f3c2-136">get_NavigationId</span></span> 

<span data-ttu-id="7f3c2-137">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-137">The ID of the navigation.</span></span>

> <span data-ttu-id="7f3c2-138">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="7f3c2-138">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="7f3c2-139">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="7f3c2-139">get_RequestHeaders</span></span> 

<span data-ttu-id="7f3c2-140">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="7f3c2-141">[get_RequestHeaders](#get_requestheaders)par le biais du public HRESULT ([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* requestHeaders)</span><span class="sxs-lookup"><span data-stu-id="7f3c2-141">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="7f3c2-142">Remarque: vous ne pouvez pas modifier les en-têtes de requête HTTP dans un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="7f3c2-143">get_Uri</span><span class="sxs-lookup"><span data-stu-id="7f3c2-143">get_Uri</span></span> 

<span data-ttu-id="7f3c2-144">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="7f3c2-145">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="7f3c2-145">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="7f3c2-146">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="7f3c2-146">put_Cancel</span></span> 

<span data-ttu-id="7f3c2-147">Définissez la propriété Cancel.</span><span class="sxs-lookup"><span data-stu-id="7f3c2-147">Set the Cancel property.</span></span>

> <span data-ttu-id="7f3c2-148">[put_Cancel](#put_cancel)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="7f3c2-148">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

