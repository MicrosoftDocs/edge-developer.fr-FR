---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 2f129f36502ccc404da74904c73c4bdab1d9f472
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886373"
---
# <span data-ttu-id="02790-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="02790-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="02790-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="02790-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="02790-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="02790-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="02790-107">Arguments d’événement pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="02790-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="02790-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="02790-108">Summary</span></span>

 <span data-ttu-id="02790-109">Ses</span><span class="sxs-lookup"><span data-stu-id="02790-109">Members</span></span>                        | <span data-ttu-id="02790-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="02790-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="02790-111">Annuler</span><span class="sxs-lookup"><span data-stu-id="02790-111">Cancel</span></span>](#cancel) | <span data-ttu-id="02790-112">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="02790-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="02790-113">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="02790-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="02790-114">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="02790-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="02790-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="02790-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="02790-116">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="02790-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="02790-117">NavigationId</span><span class="sxs-lookup"><span data-stu-id="02790-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="02790-118">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="02790-118">The ID of the navigation.</span></span>
[<span data-ttu-id="02790-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="02790-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="02790-120">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="02790-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="02790-121">URI</span><span class="sxs-lookup"><span data-stu-id="02790-121">Uri</span></span>](#uri) | <span data-ttu-id="02790-122">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="02790-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="02790-123">Ses</span><span class="sxs-lookup"><span data-stu-id="02790-123">Members</span></span>

#### <span data-ttu-id="02790-124">Annuler</span><span class="sxs-lookup"><span data-stu-id="02790-124">Cancel</span></span> 

<span data-ttu-id="02790-125">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="02790-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="02790-126">public bool [Annuler](#cancel)</span><span class="sxs-lookup"><span data-stu-id="02790-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="02790-127">S’il est défini, il sera comme si la navigation ne s’est jamais produite et le contenu de la page active sera intact.</span><span class="sxs-lookup"><span data-stu-id="02790-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="02790-128">Pour des raisons de performances, les requêtes HTTP peuvent se produire alors que l’hôte répond.</span><span class="sxs-lookup"><span data-stu-id="02790-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="02790-129">Cela signifie que les cookies peuvent être définis et utilisés dans le cadre d’une demande de navigation.</span><span class="sxs-lookup"><span data-stu-id="02790-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="02790-130">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="02790-130">IsRedirected</span></span> 

<span data-ttu-id="02790-131">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="02790-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="02790-132">public bool [IsRedirected](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="02790-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="02790-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="02790-133">IsUserInitiated</span></span> 

<span data-ttu-id="02790-134">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="02790-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="02790-135">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="02790-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="02790-136">NavigationId</span><span class="sxs-lookup"><span data-stu-id="02790-136">NavigationId</span></span> 

<span data-ttu-id="02790-137">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="02790-137">The ID of the navigation.</span></span>

> <span data-ttu-id="02790-138">public ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="02790-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="02790-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="02790-139">RequestHeaders</span></span> 

<span data-ttu-id="02790-140">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="02790-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="02790-141">public HttpRequestHeaders [requestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="02790-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="02790-142">Remarque: vous ne pouvez pas modifier les en-têtes de requête HTTP dans un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="02790-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="02790-143">URI</span><span class="sxs-lookup"><span data-stu-id="02790-143">Uri</span></span> 

<span data-ttu-id="02790-144">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="02790-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="02790-145">[URI](#uri) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="02790-145">public string [Uri](#uri)</span></span>

