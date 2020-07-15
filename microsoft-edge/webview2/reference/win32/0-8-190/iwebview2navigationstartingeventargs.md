---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 8bc625d12cc3b3ebe06970fd282dd8f60bcabd22
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878399"
---
# <span data-ttu-id="e66f2-104">0.8.355-interface IWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="e66f2-104">0.8.355 - interface IWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="e66f2-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="e66f2-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="e66f2-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="e66f2-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="e66f2-107">Arguments d’événement pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="e66f2-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="e66f2-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="e66f2-108">Summary</span></span>

 <span data-ttu-id="e66f2-109">Ses</span><span class="sxs-lookup"><span data-stu-id="e66f2-109">Members</span></span>                        | <span data-ttu-id="e66f2-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e66f2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e66f2-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="e66f2-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="e66f2-112">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="e66f2-112">The uri of the requested navigation.</span></span>
[<span data-ttu-id="e66f2-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="e66f2-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="e66f2-114">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="e66f2-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="e66f2-115">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="e66f2-115">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="e66f2-116">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="e66f2-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="e66f2-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="e66f2-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="e66f2-118">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="e66f2-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="e66f2-119">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="e66f2-119">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="e66f2-120">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="e66f2-120">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="e66f2-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="e66f2-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="e66f2-122">Définissez la propriété Cancel.</span><span class="sxs-lookup"><span data-stu-id="e66f2-122">Set the Cancel property.</span></span>

## <span data-ttu-id="e66f2-123">Ses</span><span class="sxs-lookup"><span data-stu-id="e66f2-123">Members</span></span>

#### <span data-ttu-id="e66f2-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="e66f2-124">get_Uri</span></span> 

<span data-ttu-id="e66f2-125">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="e66f2-125">The uri of the requested navigation.</span></span>

> <span data-ttu-id="e66f2-126">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="e66f2-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="e66f2-127">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="e66f2-127">get_IsUserInitiated</span></span> 

<span data-ttu-id="e66f2-128">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="e66f2-128">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="e66f2-129">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="e66f2-129">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="e66f2-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="e66f2-130">get_IsRedirected</span></span> 

<span data-ttu-id="e66f2-131">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="e66f2-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="e66f2-132">valeur publique HRESULT [get_IsRedirected](#get_isredirected)(bool \* IsRedirected)</span><span class="sxs-lookup"><span data-stu-id="e66f2-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="e66f2-133">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="e66f2-133">get_RequestHeaders</span></span> 

<span data-ttu-id="e66f2-134">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="e66f2-134">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="e66f2-135">[get_RequestHeaders](#get_requestheaders)par le biais du public HRESULT ([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \* requestHeaders)</span><span class="sxs-lookup"><span data-stu-id="e66f2-135">public HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="e66f2-136">Remarque: vous ne pouvez pas modifier les en-têtes de requête HTTP dans un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="e66f2-136">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="e66f2-137">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="e66f2-137">get_Cancel</span></span> 

<span data-ttu-id="e66f2-138">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="e66f2-138">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="e66f2-139">valeur publique HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="e66f2-139">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="e66f2-140">S’il est défini, il sera comme si la navigation ne s’est jamais produite et le contenu de la page active sera intact.</span><span class="sxs-lookup"><span data-stu-id="e66f2-140">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="e66f2-141">Pour des raisons de performances, les requêtes HTTP peuvent se produire alors que l’hôte répond.</span><span class="sxs-lookup"><span data-stu-id="e66f2-141">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="e66f2-142">Cela signifie que les cookies peuvent être définis et utilisés dans le cadre d’une demande de navigation.</span><span class="sxs-lookup"><span data-stu-id="e66f2-142">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="e66f2-143">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="e66f2-143">put_Cancel</span></span> 

<span data-ttu-id="e66f2-144">Définissez la propriété Cancel.</span><span class="sxs-lookup"><span data-stu-id="e66f2-144">Set the Cancel property.</span></span>

> <span data-ttu-id="e66f2-145">[put_Cancel](#put_cancel)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e66f2-145">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

