---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 2282b36d3b7dfcca83f84ed50a976d4e6622ce07
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010123"
---
# <span data-ttu-id="9cb8a-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9cb8a-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="9cb8a-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="9cb8a-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="9cb8a-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="9cb8a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="9cb8a-107">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9cb8a-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="9cb8a-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="9cb8a-108">Summary</span></span>

 <span data-ttu-id="9cb8a-109">Ses</span><span class="sxs-lookup"><span data-stu-id="9cb8a-109">Members</span></span>                        | <span data-ttu-id="9cb8a-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="9cb8a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9cb8a-111">Requête</span><span class="sxs-lookup"><span data-stu-id="9cb8a-111">Request</span></span>](#request) | <span data-ttu-id="9cb8a-112">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="9cb8a-112">The HTTP request.</span></span>
[<span data-ttu-id="9cb8a-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="9cb8a-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="9cb8a-114">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="9cb8a-114">The web resource request contexts.</span></span>
[<span data-ttu-id="9cb8a-115">Réponse</span><span class="sxs-lookup"><span data-stu-id="9cb8a-115">Response</span></span>](#response) | <span data-ttu-id="9cb8a-116">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="9cb8a-116">The HTTP response.</span></span>
[<span data-ttu-id="9cb8a-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="9cb8a-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="9cb8a-118">Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="9cb8a-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="9cb8a-119">Ses</span><span class="sxs-lookup"><span data-stu-id="9cb8a-119">Members</span></span>

#### <span data-ttu-id="9cb8a-120">Requête</span><span class="sxs-lookup"><span data-stu-id="9cb8a-120">Request</span></span> 

<span data-ttu-id="9cb8a-121">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="9cb8a-121">The HTTP request.</span></span>

> <span data-ttu-id="9cb8a-122">[demande](#request) publique HttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="9cb8a-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="9cb8a-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="9cb8a-123">ResourceContext</span></span> 

<span data-ttu-id="9cb8a-124">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="9cb8a-124">The web resource request contexts.</span></span>

> <span data-ttu-id="9cb8a-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="9cb8a-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="9cb8a-126">Réponse</span><span class="sxs-lookup"><span data-stu-id="9cb8a-126">Response</span></span> 

<span data-ttu-id="9cb8a-127">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="9cb8a-127">The HTTP response.</span></span>

> <span data-ttu-id="9cb8a-128">[réponse](#response) HttpResponseMessage publique</span><span class="sxs-lookup"><span data-stu-id="9cb8a-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="9cb8a-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="9cb8a-129">GetDeferral</span></span> 

<span data-ttu-id="9cb8a-130">Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="9cb8a-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="9cb8a-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="9cb8a-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="9cb8a-132">Vous pouvez utiliser l’objet CoreWebView2Deferral pour terminer la requête réseau ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="9cb8a-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>

