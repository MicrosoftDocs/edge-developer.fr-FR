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
ms.openlocfilehash: 9210a4b70d0e2edf30cbaad906f57b360688dfe8
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653341"
---
# <span data-ttu-id="2d5d7-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2d5d7-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

<span data-ttu-id="2d5d7-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="2d5d7-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="2d5d7-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="2d5d7-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="2d5d7-107">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2d5d7-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="2d5d7-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="2d5d7-108">Summary</span></span>

 <span data-ttu-id="2d5d7-109">Ses</span><span class="sxs-lookup"><span data-stu-id="2d5d7-109">Members</span></span>                        | <span data-ttu-id="2d5d7-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="2d5d7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2d5d7-111">Requête</span><span class="sxs-lookup"><span data-stu-id="2d5d7-111">Request</span></span>](#request) | <span data-ttu-id="2d5d7-112">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="2d5d7-112">The HTTP request.</span></span>
[<span data-ttu-id="2d5d7-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="2d5d7-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="2d5d7-114">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="2d5d7-114">The web resource request contexts.</span></span>
[<span data-ttu-id="2d5d7-115">Réponse</span><span class="sxs-lookup"><span data-stu-id="2d5d7-115">Response</span></span>](#response) | <span data-ttu-id="2d5d7-116">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="2d5d7-116">The HTTP response.</span></span>
[<span data-ttu-id="2d5d7-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2d5d7-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="2d5d7-118">Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="2d5d7-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="2d5d7-119">Ses</span><span class="sxs-lookup"><span data-stu-id="2d5d7-119">Members</span></span>

#### <span data-ttu-id="2d5d7-120">Requête</span><span class="sxs-lookup"><span data-stu-id="2d5d7-120">Request</span></span> 

<span data-ttu-id="2d5d7-121">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="2d5d7-121">The HTTP request.</span></span>

> <span data-ttu-id="2d5d7-122">[demande](#request) publique HttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="2d5d7-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="2d5d7-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="2d5d7-123">ResourceContext</span></span> 

<span data-ttu-id="2d5d7-124">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="2d5d7-124">The web resource request contexts.</span></span>

> <span data-ttu-id="2d5d7-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="2d5d7-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="2d5d7-126">Réponse</span><span class="sxs-lookup"><span data-stu-id="2d5d7-126">Response</span></span> 

<span data-ttu-id="2d5d7-127">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="2d5d7-127">The HTTP response.</span></span>

> <span data-ttu-id="2d5d7-128">[réponse](#response) HttpResponseMessage publique</span><span class="sxs-lookup"><span data-stu-id="2d5d7-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="2d5d7-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2d5d7-129">GetDeferral</span></span> 

<span data-ttu-id="2d5d7-130">Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="2d5d7-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="2d5d7-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="2d5d7-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="2d5d7-132">Vous pouvez utiliser l’objet CoreWebView2Deferral pour terminer la requête réseau ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="2d5d7-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>

