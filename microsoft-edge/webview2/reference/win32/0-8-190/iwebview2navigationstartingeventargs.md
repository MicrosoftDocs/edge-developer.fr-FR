---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 5996f0eff4db17530750eb39c7693ea0f8496a4d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885897"
---
# <span data-ttu-id="8606b-104">0.8.355-interface IWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="8606b-104">0.8.355 - interface IWebView2NavigationStartingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="8606b-105">Arguments d’événement pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="8606b-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="8606b-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="8606b-106">Summary</span></span>

 <span data-ttu-id="8606b-107">Ses</span><span class="sxs-lookup"><span data-stu-id="8606b-107">Members</span></span>                        | <span data-ttu-id="8606b-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="8606b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8606b-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="8606b-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="8606b-110">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="8606b-110">The uri of the requested navigation.</span></span>
[<span data-ttu-id="8606b-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="8606b-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="8606b-112">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="8606b-112">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="8606b-113">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="8606b-113">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="8606b-114">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="8606b-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="8606b-115">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="8606b-115">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="8606b-116">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="8606b-116">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="8606b-117">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="8606b-117">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="8606b-118">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="8606b-118">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="8606b-119">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="8606b-119">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="8606b-120">Définissez la propriété Cancel.</span><span class="sxs-lookup"><span data-stu-id="8606b-120">Set the Cancel property.</span></span>

## <span data-ttu-id="8606b-121">Ses</span><span class="sxs-lookup"><span data-stu-id="8606b-121">Members</span></span>

#### <span data-ttu-id="8606b-122">get_Uri</span><span class="sxs-lookup"><span data-stu-id="8606b-122">get_Uri</span></span> 

<span data-ttu-id="8606b-123">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="8606b-123">The uri of the requested navigation.</span></span>

> <span data-ttu-id="8606b-124">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="8606b-124">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="8606b-125">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="8606b-125">get_IsUserInitiated</span></span> 

<span data-ttu-id="8606b-126">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="8606b-126">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="8606b-127">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="8606b-127">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="8606b-128">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="8606b-128">get_IsRedirected</span></span> 

<span data-ttu-id="8606b-129">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="8606b-129">True when the navigation is redirected.</span></span>

> <span data-ttu-id="8606b-130">valeur publique HRESULT [get_IsRedirected](#get_isredirected)(bool \* IsRedirected)</span><span class="sxs-lookup"><span data-stu-id="8606b-130">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="8606b-131">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="8606b-131">get_RequestHeaders</span></span> 

<span data-ttu-id="8606b-132">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="8606b-132">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="8606b-133">[get_RequestHeaders](#get_requestheaders)par le biais du public HRESULT ([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \* requestHeaders)</span><span class="sxs-lookup"><span data-stu-id="8606b-133">public HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="8606b-134">Remarque: vous ne pouvez pas modifier les en-têtes de requête HTTP dans un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="8606b-134">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="8606b-135">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="8606b-135">get_Cancel</span></span> 

<span data-ttu-id="8606b-136">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="8606b-136">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="8606b-137">valeur publique HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="8606b-137">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="8606b-138">S’il est défini, il sera comme si la navigation ne s’est jamais produite et le contenu de la page active sera intact.</span><span class="sxs-lookup"><span data-stu-id="8606b-138">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="8606b-139">Pour des raisons de performances, les requêtes HTTP peuvent se produire alors que l’hôte répond.</span><span class="sxs-lookup"><span data-stu-id="8606b-139">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="8606b-140">Cela signifie que les cookies peuvent être définis et utilisés dans le cadre d’une demande de navigation.</span><span class="sxs-lookup"><span data-stu-id="8606b-140">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="8606b-141">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="8606b-141">put_Cancel</span></span> 

<span data-ttu-id="8606b-142">Définissez la propriété Cancel.</span><span class="sxs-lookup"><span data-stu-id="8606b-142">Set the Cancel property.</span></span>

> <span data-ttu-id="8606b-143">[put_Cancel](#put_cancel)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="8606b-143">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

