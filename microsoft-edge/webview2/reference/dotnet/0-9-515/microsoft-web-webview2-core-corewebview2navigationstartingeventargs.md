---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: ea3936ac1267fa085f62db843f5cac3fad2635b5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879785"
---
# <span data-ttu-id="28dce-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="28dce-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="28dce-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="28dce-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="28dce-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="28dce-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="28dce-107">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="28dce-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="28dce-108">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="28dce-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="28dce-109">Arguments d’événement pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="28dce-109">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="28dce-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="28dce-110">Summary</span></span>

 <span data-ttu-id="28dce-111">Ses</span><span class="sxs-lookup"><span data-stu-id="28dce-111">Members</span></span>                        | <span data-ttu-id="28dce-112">Descriptions</span><span class="sxs-lookup"><span data-stu-id="28dce-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="28dce-113">Annuler</span><span class="sxs-lookup"><span data-stu-id="28dce-113">Cancel</span></span>](#cancel) | <span data-ttu-id="28dce-114">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="28dce-114">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="28dce-115">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="28dce-115">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="28dce-116">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="28dce-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="28dce-117">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="28dce-117">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="28dce-118">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="28dce-118">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="28dce-119">NavigationId</span><span class="sxs-lookup"><span data-stu-id="28dce-119">NavigationId</span></span>](#navigationid) | <span data-ttu-id="28dce-120">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="28dce-120">The ID of the navigation.</span></span>
[<span data-ttu-id="28dce-121">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="28dce-121">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="28dce-122">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="28dce-122">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="28dce-123">URI</span><span class="sxs-lookup"><span data-stu-id="28dce-123">Uri</span></span>](#uri) | <span data-ttu-id="28dce-124">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="28dce-124">The uri of the requested navigation.</span></span>

## <span data-ttu-id="28dce-125">Ses</span><span class="sxs-lookup"><span data-stu-id="28dce-125">Members</span></span>

#### <span data-ttu-id="28dce-126">Annuler</span><span class="sxs-lookup"><span data-stu-id="28dce-126">Cancel</span></span> 

<span data-ttu-id="28dce-127">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="28dce-127">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="28dce-128">public bool [Annuler](#cancel)</span><span class="sxs-lookup"><span data-stu-id="28dce-128">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="28dce-129">S’il est défini, il sera comme si la navigation ne s’est jamais produite et le contenu de la page active sera intact.</span><span class="sxs-lookup"><span data-stu-id="28dce-129">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="28dce-130">Pour des raisons de performances, les requêtes HTTP peuvent se produire alors que l’hôte répond.</span><span class="sxs-lookup"><span data-stu-id="28dce-130">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="28dce-131">Cela signifie que les cookies peuvent être définis et utilisés dans le cadre d’une demande de navigation.</span><span class="sxs-lookup"><span data-stu-id="28dce-131">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="28dce-132">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="28dce-132">IsRedirected</span></span> 

<span data-ttu-id="28dce-133">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="28dce-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="28dce-134">public bool [IsRedirected](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="28dce-134">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="28dce-135">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="28dce-135">IsUserInitiated</span></span> 

<span data-ttu-id="28dce-136">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="28dce-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="28dce-137">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="28dce-137">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="28dce-138">NavigationId</span><span class="sxs-lookup"><span data-stu-id="28dce-138">NavigationId</span></span> 

<span data-ttu-id="28dce-139">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="28dce-139">The ID of the navigation.</span></span>

> <span data-ttu-id="28dce-140">public ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="28dce-140">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="28dce-141">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="28dce-141">RequestHeaders</span></span> 

<span data-ttu-id="28dce-142">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="28dce-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="28dce-143">public HttpRequestHeaders [requestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="28dce-143">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="28dce-144">Remarque: vous ne pouvez pas modifier les en-têtes de requête HTTP dans un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="28dce-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="28dce-145">URI</span><span class="sxs-lookup"><span data-stu-id="28dce-145">Uri</span></span> 

<span data-ttu-id="28dce-146">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="28dce-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="28dce-147">[URI](#uri) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="28dce-147">public string [Uri](#uri)</span></span>

