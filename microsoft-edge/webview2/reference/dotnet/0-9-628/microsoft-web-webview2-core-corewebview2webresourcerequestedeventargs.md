---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 501483894a2abca58c5a1856ab587b93be904c8b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011850"
---
# <span data-ttu-id="47a4e-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="47a4e-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

<span data-ttu-id="47a4e-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="47a4e-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="47a4e-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="47a4e-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="47a4e-107">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="47a4e-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="47a4e-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="47a4e-108">Summary</span></span>

 <span data-ttu-id="47a4e-109">Ses</span><span class="sxs-lookup"><span data-stu-id="47a4e-109">Members</span></span>                        | <span data-ttu-id="47a4e-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="47a4e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="47a4e-111">Requête</span><span class="sxs-lookup"><span data-stu-id="47a4e-111">Request</span></span>](#request) | <span data-ttu-id="47a4e-112">Demande de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="47a4e-112">The Web resource request.</span></span>
[<span data-ttu-id="47a4e-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="47a4e-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="47a4e-114">Contexte de demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="47a4e-114">The web resource request context.</span></span>
[<span data-ttu-id="47a4e-115">Réponse</span><span class="sxs-lookup"><span data-stu-id="47a4e-115">Response</span></span>](#response) | <span data-ttu-id="47a4e-116">Espace réservé à l’objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="47a4e-116">A placeholder for the web resource response object.</span></span>
[<span data-ttu-id="47a4e-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="47a4e-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="47a4e-118">Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="47a4e-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="47a4e-119">Ses</span><span class="sxs-lookup"><span data-stu-id="47a4e-119">Members</span></span>

#### <span data-ttu-id="47a4e-120">Requête</span><span class="sxs-lookup"><span data-stu-id="47a4e-120">Request</span></span> 

<span data-ttu-id="47a4e-121">Demande de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="47a4e-121">The Web resource request.</span></span>

> <span data-ttu-id="47a4e-122">[demande](#request) publique [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md)</span><span class="sxs-lookup"><span data-stu-id="47a4e-122">public [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md) [Request](#request)</span></span>

<span data-ttu-id="47a4e-123">Il est possible que l’objet de requête ne dispose pas de certains en-têtes ajoutés par la pile réseau plus tard.</span><span class="sxs-lookup"><span data-stu-id="47a4e-123">The request object may be missing some headers that are added by network stack later on.</span></span>

#### <span data-ttu-id="47a4e-124">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="47a4e-124">ResourceContext</span></span> 

<span data-ttu-id="47a4e-125">Contexte de demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="47a4e-125">The web resource request context.</span></span>

> <span data-ttu-id="47a4e-126">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="47a4e-126">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="47a4e-127">Réponse</span><span class="sxs-lookup"><span data-stu-id="47a4e-127">Response</span></span> 

<span data-ttu-id="47a4e-128">Espace réservé à l’objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="47a4e-128">A placeholder for the web resource response object.</span></span>

> <span data-ttu-id="47a4e-129">réponse [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [Response](#response) publique</span><span class="sxs-lookup"><span data-stu-id="47a4e-129">public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [Response](#response)</span></span>

<span data-ttu-id="47a4e-130">Si cet objet est défini, la demande de ressource Web sera exécutée avec cette réponse.</span><span class="sxs-lookup"><span data-stu-id="47a4e-130">If this object is set, the web resource request will be completed with this response.</span></span> <span data-ttu-id="47a4e-131">Un objet de réponse aux ressources Web vide peut être créé à l’aide de CreateWebResourceResponse, puis modifié pour créer la réponse.</span><span class="sxs-lookup"><span data-stu-id="47a4e-131">An empty Web resource response object can be created with CreateWebResourceResponse and then modified to construct the response.</span></span>

#### <span data-ttu-id="47a4e-132">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="47a4e-132">GetDeferral</span></span> 

<span data-ttu-id="47a4e-133">Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="47a4e-133">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="47a4e-134">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="47a4e-134">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="47a4e-135">Vous pouvez utiliser l’objet CoreWebView2Deferral pour exécuter la requête ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="47a4e-135">You can use the CoreWebView2Deferral object to complete the request at a later time.</span></span>

