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
ms.openlocfilehash: 072ce10e7ac1f34238278366c3e8799a3268cb0b
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697531"
---
# <span data-ttu-id="2cfda-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2cfda-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="2cfda-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="2cfda-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="2cfda-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="2cfda-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="2cfda-107">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="2cfda-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="2cfda-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="2cfda-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="2cfda-109">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2cfda-109">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="2cfda-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="2cfda-110">Summary</span></span>

 <span data-ttu-id="2cfda-111">Ses</span><span class="sxs-lookup"><span data-stu-id="2cfda-111">Members</span></span>                        | <span data-ttu-id="2cfda-112">Descriptions</span><span class="sxs-lookup"><span data-stu-id="2cfda-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2cfda-113">Requête</span><span class="sxs-lookup"><span data-stu-id="2cfda-113">Request</span></span>](#request) | <span data-ttu-id="2cfda-114">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="2cfda-114">The HTTP request.</span></span>
[<span data-ttu-id="2cfda-115">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="2cfda-115">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="2cfda-116">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="2cfda-116">The web resource request contexts.</span></span>
[<span data-ttu-id="2cfda-117">Réponse</span><span class="sxs-lookup"><span data-stu-id="2cfda-117">Response</span></span>](#response) | <span data-ttu-id="2cfda-118">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="2cfda-118">The HTTP response.</span></span>
[<span data-ttu-id="2cfda-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2cfda-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="2cfda-120">Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="2cfda-120">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="2cfda-121">Ses</span><span class="sxs-lookup"><span data-stu-id="2cfda-121">Members</span></span>

#### <span data-ttu-id="2cfda-122">Requête</span><span class="sxs-lookup"><span data-stu-id="2cfda-122">Request</span></span> 

<span data-ttu-id="2cfda-123">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="2cfda-123">The HTTP request.</span></span>

> <span data-ttu-id="2cfda-124">[demande](#request) publique HttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="2cfda-124">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="2cfda-125">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="2cfda-125">ResourceContext</span></span> 

<span data-ttu-id="2cfda-126">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="2cfda-126">The web resource request contexts.</span></span>

> <span data-ttu-id="2cfda-127">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="2cfda-127">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="2cfda-128">Réponse</span><span class="sxs-lookup"><span data-stu-id="2cfda-128">Response</span></span> 

<span data-ttu-id="2cfda-129">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="2cfda-129">The HTTP response.</span></span>

> <span data-ttu-id="2cfda-130">[réponse](#response) HttpResponseMessage publique</span><span class="sxs-lookup"><span data-stu-id="2cfda-130">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="2cfda-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2cfda-131">GetDeferral</span></span> 

<span data-ttu-id="2cfda-132">Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="2cfda-132">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="2cfda-133">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="2cfda-133">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="2cfda-134">Vous pouvez utiliser l’objet CoreWebView2Deferral pour terminer la requête réseau ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="2cfda-134">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>

