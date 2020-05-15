---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: ee6886e32b32f4da4bbdc04fe6e866210a76488b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653696"
---
# <span data-ttu-id="9e1b8-104">interface IWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="9e1b8-104">interface IWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="9e1b8-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="9e1b8-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="9e1b8-107">Arguments d’événement pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="9e1b8-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="9e1b8-108">Summary</span></span>

 <span data-ttu-id="9e1b8-109">Ses</span><span class="sxs-lookup"><span data-stu-id="9e1b8-109">Members</span></span>                        | <span data-ttu-id="9e1b8-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="9e1b8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9e1b8-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="9e1b8-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="9e1b8-112">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-112">The uri of the requested navigation.</span></span>
[<span data-ttu-id="9e1b8-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="9e1b8-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="9e1b8-114">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="9e1b8-115">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="9e1b8-115">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="9e1b8-116">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="9e1b8-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="9e1b8-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="9e1b8-118">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="9e1b8-119">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="9e1b8-119">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="9e1b8-120">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-120">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="9e1b8-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="9e1b8-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="9e1b8-122">Définissez la propriété Cancel.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-122">Set the Cancel property.</span></span>

## <span data-ttu-id="9e1b8-123">Ses</span><span class="sxs-lookup"><span data-stu-id="9e1b8-123">Members</span></span>

#### <span data-ttu-id="9e1b8-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="9e1b8-124">get_Uri</span></span> 

<span data-ttu-id="9e1b8-125">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-125">The uri of the requested navigation.</span></span>

> <span data-ttu-id="9e1b8-126">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="9e1b8-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="9e1b8-127">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="9e1b8-127">get_IsUserInitiated</span></span> 

<span data-ttu-id="9e1b8-128">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-128">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="9e1b8-129">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="9e1b8-129">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="9e1b8-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="9e1b8-130">get_IsRedirected</span></span> 

<span data-ttu-id="9e1b8-131">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="9e1b8-132">valeur publique HRESULT [get_IsRedirected](#get_isredirected)(bool \* IsRedirected)</span><span class="sxs-lookup"><span data-stu-id="9e1b8-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="9e1b8-133">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="9e1b8-133">get_RequestHeaders</span></span> 

<span data-ttu-id="9e1b8-134">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-134">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="9e1b8-135">[get_RequestHeaders](#get_requestheaders)par le biais du public HRESULT ([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \* requestHeaders)</span><span class="sxs-lookup"><span data-stu-id="9e1b8-135">public HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="9e1b8-136">Remarque: vous ne pouvez pas modifier les en-têtes de requête HTTP dans un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-136">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="9e1b8-137">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="9e1b8-137">get_Cancel</span></span> 

<span data-ttu-id="9e1b8-138">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-138">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="9e1b8-139">valeur publique HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="9e1b8-139">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="9e1b8-140">S’il est défini, il sera comme si la navigation ne s’est jamais produite et le contenu de la page active sera intact.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-140">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="9e1b8-141">Pour des raisons de performances, les requêtes HTTP peuvent se produire alors que l’hôte répond.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-141">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="9e1b8-142">Cela signifie que les cookies peuvent être définis et utilisés dans le cadre d’une demande de navigation.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-142">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="9e1b8-143">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="9e1b8-143">put_Cancel</span></span> 

<span data-ttu-id="9e1b8-144">Définissez la propriété Cancel.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-144">Set the Cancel property.</span></span>

> <span data-ttu-id="9e1b8-145">[put_Cancel](#put_cancel)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9e1b8-145">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

