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
ms.openlocfilehash: 8b7ac3ab27cf5a2d9e80a77eabc488599820a02f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653684"
---
# <span data-ttu-id="56dad-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="56dad-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

<span data-ttu-id="56dad-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="56dad-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="56dad-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="56dad-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="56dad-107">Arguments d’événement pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="56dad-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="56dad-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="56dad-108">Summary</span></span>

 <span data-ttu-id="56dad-109">Ses</span><span class="sxs-lookup"><span data-stu-id="56dad-109">Members</span></span>                        | <span data-ttu-id="56dad-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="56dad-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="56dad-111">Annuler</span><span class="sxs-lookup"><span data-stu-id="56dad-111">Cancel</span></span>](#cancel) | <span data-ttu-id="56dad-112">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="56dad-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="56dad-113">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="56dad-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="56dad-114">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="56dad-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="56dad-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="56dad-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="56dad-116">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="56dad-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="56dad-117">NavigationId</span><span class="sxs-lookup"><span data-stu-id="56dad-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="56dad-118">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="56dad-118">The ID of the navigation.</span></span>
[<span data-ttu-id="56dad-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="56dad-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="56dad-120">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="56dad-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="56dad-121">URI</span><span class="sxs-lookup"><span data-stu-id="56dad-121">Uri</span></span>](#uri) | <span data-ttu-id="56dad-122">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="56dad-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="56dad-123">Ses</span><span class="sxs-lookup"><span data-stu-id="56dad-123">Members</span></span>

#### <span data-ttu-id="56dad-124">Annuler</span><span class="sxs-lookup"><span data-stu-id="56dad-124">Cancel</span></span> 

<span data-ttu-id="56dad-125">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="56dad-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="56dad-126">public bool [Annuler](#cancel)</span><span class="sxs-lookup"><span data-stu-id="56dad-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="56dad-127">S’il est défini, il sera comme si la navigation ne s’est jamais produite et le contenu de la page active sera intact.</span><span class="sxs-lookup"><span data-stu-id="56dad-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="56dad-128">Pour des raisons de performances, les requêtes HTTP peuvent se produire alors que l’hôte répond.</span><span class="sxs-lookup"><span data-stu-id="56dad-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="56dad-129">Cela signifie que les cookies peuvent être définis et utilisés dans le cadre d’une demande de navigation.</span><span class="sxs-lookup"><span data-stu-id="56dad-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="56dad-130">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="56dad-130">IsRedirected</span></span> 

<span data-ttu-id="56dad-131">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="56dad-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="56dad-132">public bool [IsRedirected](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="56dad-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="56dad-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="56dad-133">IsUserInitiated</span></span> 

<span data-ttu-id="56dad-134">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="56dad-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="56dad-135">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="56dad-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="56dad-136">NavigationId</span><span class="sxs-lookup"><span data-stu-id="56dad-136">NavigationId</span></span> 

<span data-ttu-id="56dad-137">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="56dad-137">The ID of the navigation.</span></span>

> <span data-ttu-id="56dad-138">public ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="56dad-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="56dad-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="56dad-139">RequestHeaders</span></span> 

<span data-ttu-id="56dad-140">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="56dad-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="56dad-141">public HttpRequestHeaders [requestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="56dad-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="56dad-142">Remarque: vous ne pouvez pas modifier les en-têtes de requête HTTP dans un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="56dad-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="56dad-143">URI</span><span class="sxs-lookup"><span data-stu-id="56dad-143">Uri</span></span> 

<span data-ttu-id="56dad-144">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="56dad-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="56dad-145">[URI](#uri) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="56dad-145">public string [Uri](#uri)</span></span>

