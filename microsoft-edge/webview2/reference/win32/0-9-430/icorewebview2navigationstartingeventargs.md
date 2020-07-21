---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: bd9d10d5f281b2e8f0a5d0687235560c44edc170
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886436"
---
# <span data-ttu-id="8f2be-104">0.9.430-interface ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="8f2be-104">0.9.430 - interface ICoreWebView2NavigationStartingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="8f2be-105">Arguments d’événement pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="8f2be-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="8f2be-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="8f2be-106">Summary</span></span>

 <span data-ttu-id="8f2be-107">Ses</span><span class="sxs-lookup"><span data-stu-id="8f2be-107">Members</span></span>                        | <span data-ttu-id="8f2be-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="8f2be-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8f2be-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="8f2be-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="8f2be-110">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="8f2be-110">The uri of the requested navigation.</span></span>
[<span data-ttu-id="8f2be-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="8f2be-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="8f2be-112">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="8f2be-112">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="8f2be-113">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="8f2be-113">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="8f2be-114">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="8f2be-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="8f2be-115">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="8f2be-115">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="8f2be-116">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="8f2be-116">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="8f2be-117">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="8f2be-117">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="8f2be-118">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="8f2be-118">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="8f2be-119">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="8f2be-119">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="8f2be-120">Définissez la propriété Cancel.</span><span class="sxs-lookup"><span data-stu-id="8f2be-120">Set the Cancel property.</span></span>
[<span data-ttu-id="8f2be-121">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="8f2be-121">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="8f2be-122">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="8f2be-122">The ID of the navigation.</span></span>

## <span data-ttu-id="8f2be-123">Ses</span><span class="sxs-lookup"><span data-stu-id="8f2be-123">Members</span></span>

#### <span data-ttu-id="8f2be-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="8f2be-124">get_Uri</span></span> 

<span data-ttu-id="8f2be-125">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="8f2be-125">The uri of the requested navigation.</span></span>

> <span data-ttu-id="8f2be-126">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="8f2be-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="8f2be-127">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="8f2be-127">get_IsUserInitiated</span></span> 

<span data-ttu-id="8f2be-128">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="8f2be-128">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="8f2be-129">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="8f2be-129">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="8f2be-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="8f2be-130">get_IsRedirected</span></span> 

<span data-ttu-id="8f2be-131">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="8f2be-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="8f2be-132">valeur publique HRESULT [get_IsRedirected](#get_isredirected)(bool \* IsRedirected)</span><span class="sxs-lookup"><span data-stu-id="8f2be-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="8f2be-133">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="8f2be-133">get_RequestHeaders</span></span> 

<span data-ttu-id="8f2be-134">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="8f2be-134">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="8f2be-135">[get_RequestHeaders](#get_requestheaders)par le biais du public HRESULT ([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \* requestHeaders)</span><span class="sxs-lookup"><span data-stu-id="8f2be-135">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="8f2be-136">Remarque: vous ne pouvez pas modifier les en-têtes de requête HTTP dans un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="8f2be-136">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="8f2be-137">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="8f2be-137">get_Cancel</span></span> 

<span data-ttu-id="8f2be-138">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="8f2be-138">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="8f2be-139">valeur publique HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="8f2be-139">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="8f2be-140">S’il est défini, il sera comme si la navigation ne s’est jamais produite et le contenu de la page active sera intact.</span><span class="sxs-lookup"><span data-stu-id="8f2be-140">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="8f2be-141">Pour des raisons de performances, les requêtes HTTP peuvent se produire alors que l’hôte répond.</span><span class="sxs-lookup"><span data-stu-id="8f2be-141">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="8f2be-142">Cela signifie que les cookies peuvent être définis et utilisés dans le cadre d’une demande de navigation.</span><span class="sxs-lookup"><span data-stu-id="8f2be-142">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="8f2be-143">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="8f2be-143">put_Cancel</span></span> 

<span data-ttu-id="8f2be-144">Définissez la propriété Cancel.</span><span class="sxs-lookup"><span data-stu-id="8f2be-144">Set the Cancel property.</span></span>

> <span data-ttu-id="8f2be-145">[put_Cancel](#put_cancel)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="8f2be-145">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

#### <span data-ttu-id="8f2be-146">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="8f2be-146">get_NavigationId</span></span> 

<span data-ttu-id="8f2be-147">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="8f2be-147">The ID of the navigation.</span></span>

> <span data-ttu-id="8f2be-148">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="8f2be-148">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

