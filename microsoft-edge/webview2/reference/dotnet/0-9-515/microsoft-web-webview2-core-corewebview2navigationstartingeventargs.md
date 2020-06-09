---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 98e242ace5eb0ae5958ddb1eb6cd380d194294be
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697629"
---
# <span data-ttu-id="c3497-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="c3497-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="c3497-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="c3497-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="c3497-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="c3497-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="c3497-107">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="c3497-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="c3497-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="c3497-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="c3497-109">Arguments d’événement pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="c3497-109">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="c3497-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="c3497-110">Summary</span></span>

 <span data-ttu-id="c3497-111">Ses</span><span class="sxs-lookup"><span data-stu-id="c3497-111">Members</span></span>                        | <span data-ttu-id="c3497-112">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c3497-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c3497-113">Annuler</span><span class="sxs-lookup"><span data-stu-id="c3497-113">Cancel</span></span>](#cancel) | <span data-ttu-id="c3497-114">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="c3497-114">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="c3497-115">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="c3497-115">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="c3497-116">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="c3497-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="c3497-117">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c3497-117">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="c3497-118">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="c3497-118">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="c3497-119">NavigationId</span><span class="sxs-lookup"><span data-stu-id="c3497-119">NavigationId</span></span>](#navigationid) | <span data-ttu-id="c3497-120">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="c3497-120">The ID of the navigation.</span></span>
[<span data-ttu-id="c3497-121">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="c3497-121">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="c3497-122">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="c3497-122">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="c3497-123">URI</span><span class="sxs-lookup"><span data-stu-id="c3497-123">Uri</span></span>](#uri) | <span data-ttu-id="c3497-124">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="c3497-124">The uri of the requested navigation.</span></span>

## <span data-ttu-id="c3497-125">Ses</span><span class="sxs-lookup"><span data-stu-id="c3497-125">Members</span></span>

#### <span data-ttu-id="c3497-126">Annuler</span><span class="sxs-lookup"><span data-stu-id="c3497-126">Cancel</span></span> 

<span data-ttu-id="c3497-127">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="c3497-127">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="c3497-128">public bool [Annuler](#cancel)</span><span class="sxs-lookup"><span data-stu-id="c3497-128">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="c3497-129">S’il est défini, il sera comme si la navigation ne s’est jamais produite et le contenu de la page active sera intact.</span><span class="sxs-lookup"><span data-stu-id="c3497-129">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="c3497-130">Pour des raisons de performances, les requêtes HTTP peuvent se produire alors que l’hôte répond.</span><span class="sxs-lookup"><span data-stu-id="c3497-130">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="c3497-131">Cela signifie que les cookies peuvent être définis et utilisés dans le cadre d’une demande de navigation.</span><span class="sxs-lookup"><span data-stu-id="c3497-131">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="c3497-132">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="c3497-132">IsRedirected</span></span> 

<span data-ttu-id="c3497-133">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="c3497-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="c3497-134">public bool [IsRedirected](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="c3497-134">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="c3497-135">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c3497-135">IsUserInitiated</span></span> 

<span data-ttu-id="c3497-136">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="c3497-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="c3497-137">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="c3497-137">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="c3497-138">NavigationId</span><span class="sxs-lookup"><span data-stu-id="c3497-138">NavigationId</span></span> 

<span data-ttu-id="c3497-139">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="c3497-139">The ID of the navigation.</span></span>

> <span data-ttu-id="c3497-140">public ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="c3497-140">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="c3497-141">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="c3497-141">RequestHeaders</span></span> 

<span data-ttu-id="c3497-142">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="c3497-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="c3497-143">public HttpRequestHeaders [requestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="c3497-143">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="c3497-144">Remarque: vous ne pouvez pas modifier les en-têtes de requête HTTP dans un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="c3497-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="c3497-145">URI</span><span class="sxs-lookup"><span data-stu-id="c3497-145">Uri</span></span> 

<span data-ttu-id="c3497-146">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="c3497-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="c3497-147">[URI](#uri) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="c3497-147">public string [Uri](#uri)</span></span>

