---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: 5f63cd8a9dc16ee82d77fe4b5a0b705eb79e7c6f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010937"
---
# <span data-ttu-id="4c988-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="4c988-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="4c988-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="4c988-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="4c988-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="4c988-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="4c988-107">Arguments d’événement pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="4c988-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="4c988-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="4c988-108">Summary</span></span>

 <span data-ttu-id="4c988-109">Ses</span><span class="sxs-lookup"><span data-stu-id="4c988-109">Members</span></span>                        | <span data-ttu-id="4c988-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="4c988-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4c988-111">Annuler</span><span class="sxs-lookup"><span data-stu-id="4c988-111">Cancel</span></span>](#cancel) | <span data-ttu-id="4c988-112">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="4c988-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="4c988-113">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="4c988-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="4c988-114">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="4c988-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="4c988-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="4c988-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="4c988-116">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="4c988-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="4c988-117">NavigationId</span><span class="sxs-lookup"><span data-stu-id="4c988-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="4c988-118">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="4c988-118">The ID of the navigation.</span></span>
[<span data-ttu-id="4c988-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="4c988-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="4c988-120">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="4c988-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="4c988-121">URI</span><span class="sxs-lookup"><span data-stu-id="4c988-121">Uri</span></span>](#uri) | <span data-ttu-id="4c988-122">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="4c988-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="4c988-123">Ses</span><span class="sxs-lookup"><span data-stu-id="4c988-123">Members</span></span>

#### <span data-ttu-id="4c988-124">Annuler</span><span class="sxs-lookup"><span data-stu-id="4c988-124">Cancel</span></span> 

<span data-ttu-id="4c988-125">L’hôte est susceptible de définir cet indicateur pour annuler la navigation.</span><span class="sxs-lookup"><span data-stu-id="4c988-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="4c988-126">public bool [Annuler](#cancel)</span><span class="sxs-lookup"><span data-stu-id="4c988-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="4c988-127">S’il est défini, il sera comme si la navigation ne s’est jamais produite et le contenu de la page active sera intact.</span><span class="sxs-lookup"><span data-stu-id="4c988-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="4c988-128">Pour des raisons de performances, les requêtes HTTP peuvent se produire alors que l’hôte répond.</span><span class="sxs-lookup"><span data-stu-id="4c988-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="4c988-129">Cela signifie que les cookies peuvent être définis et utilisés dans le cadre d’une demande de navigation.</span><span class="sxs-lookup"><span data-stu-id="4c988-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="4c988-130">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="4c988-130">IsRedirected</span></span> 

<span data-ttu-id="4c988-131">True lors de la redirection de la navigation.</span><span class="sxs-lookup"><span data-stu-id="4c988-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="4c988-132">public bool [IsRedirected](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="4c988-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="4c988-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="4c988-133">IsUserInitiated</span></span> 

<span data-ttu-id="4c988-134">True lors du lancement de la navigation par le biais d’un mouvement utilisateur plutôt que de la navigation par programmation.</span><span class="sxs-lookup"><span data-stu-id="4c988-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="4c988-135">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="4c988-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="4c988-136">NavigationId</span><span class="sxs-lookup"><span data-stu-id="4c988-136">NavigationId</span></span> 

<span data-ttu-id="4c988-137">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="4c988-137">The ID of the navigation.</span></span>

> <span data-ttu-id="4c988-138">public ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="4c988-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="4c988-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="4c988-139">RequestHeaders</span></span> 

<span data-ttu-id="4c988-140">En-têtes de requête HTTP pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="4c988-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="4c988-141">public HttpRequestHeaders [requestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="4c988-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="4c988-142">Remarque: vous ne pouvez pas modifier les en-têtes de requête HTTP dans un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="4c988-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="4c988-143">URI</span><span class="sxs-lookup"><span data-stu-id="4c988-143">Uri</span></span> 

<span data-ttu-id="4c988-144">URI de la navigation demandée.</span><span class="sxs-lookup"><span data-stu-id="4c988-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="4c988-145">[URI](#uri) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="4c988-145">public string [Uri](#uri)</span></span>

