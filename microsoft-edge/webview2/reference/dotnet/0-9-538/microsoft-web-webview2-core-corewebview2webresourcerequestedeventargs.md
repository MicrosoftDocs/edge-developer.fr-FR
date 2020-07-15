---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 53cc31bc714417ab902fa8fdef9fd83f80871f10
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879666"
---
# <span data-ttu-id="99fd8-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="99fd8-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

<span data-ttu-id="99fd8-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="99fd8-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="99fd8-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="99fd8-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="99fd8-107">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="99fd8-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="99fd8-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="99fd8-108">Summary</span></span>

 <span data-ttu-id="99fd8-109">Ses</span><span class="sxs-lookup"><span data-stu-id="99fd8-109">Members</span></span>                        | <span data-ttu-id="99fd8-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="99fd8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="99fd8-111">Requête</span><span class="sxs-lookup"><span data-stu-id="99fd8-111">Request</span></span>](#request) | <span data-ttu-id="99fd8-112">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="99fd8-112">The HTTP request.</span></span>
[<span data-ttu-id="99fd8-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="99fd8-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="99fd8-114">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="99fd8-114">The web resource request contexts.</span></span>
[<span data-ttu-id="99fd8-115">Réponse</span><span class="sxs-lookup"><span data-stu-id="99fd8-115">Response</span></span>](#response) | <span data-ttu-id="99fd8-116">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="99fd8-116">The HTTP response.</span></span>
[<span data-ttu-id="99fd8-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="99fd8-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="99fd8-118">Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="99fd8-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="99fd8-119">Ses</span><span class="sxs-lookup"><span data-stu-id="99fd8-119">Members</span></span>

#### <span data-ttu-id="99fd8-120">Requête</span><span class="sxs-lookup"><span data-stu-id="99fd8-120">Request</span></span> 

<span data-ttu-id="99fd8-121">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="99fd8-121">The HTTP request.</span></span>

> <span data-ttu-id="99fd8-122">[demande](#request) publique HttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="99fd8-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="99fd8-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="99fd8-123">ResourceContext</span></span> 

<span data-ttu-id="99fd8-124">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="99fd8-124">The web resource request contexts.</span></span>

> <span data-ttu-id="99fd8-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="99fd8-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="99fd8-126">Réponse</span><span class="sxs-lookup"><span data-stu-id="99fd8-126">Response</span></span> 

<span data-ttu-id="99fd8-127">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="99fd8-127">The HTTP response.</span></span>

> <span data-ttu-id="99fd8-128">[réponse](#response) HttpResponseMessage publique</span><span class="sxs-lookup"><span data-stu-id="99fd8-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="99fd8-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="99fd8-129">GetDeferral</span></span> 

<span data-ttu-id="99fd8-130">Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="99fd8-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="99fd8-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="99fd8-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="99fd8-132">Vous pouvez utiliser l’objet CoreWebView2Deferral pour terminer la requête réseau ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="99fd8-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>

