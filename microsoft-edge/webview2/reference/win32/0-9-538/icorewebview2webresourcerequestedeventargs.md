---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 3613ed9b2ef562e8760de1a88322ef028ddf4ca9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879218"
---
# <span data-ttu-id="9bd30-104">interface ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9bd30-104">interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="9bd30-105">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9bd30-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="9bd30-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="9bd30-106">Summary</span></span>

 <span data-ttu-id="9bd30-107">Ses</span><span class="sxs-lookup"><span data-stu-id="9bd30-107">Members</span></span>                        | <span data-ttu-id="9bd30-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="9bd30-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9bd30-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="9bd30-109">get_Request</span></span>](#get_request) | <span data-ttu-id="9bd30-110">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="9bd30-110">The HTTP request.</span></span>
[<span data-ttu-id="9bd30-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="9bd30-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="9bd30-112">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="9bd30-112">The web resource request contexts.</span></span>
[<span data-ttu-id="9bd30-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="9bd30-113">get_Response</span></span>](#get_response) | <span data-ttu-id="9bd30-114">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="9bd30-114">The HTTP response.</span></span>
[<span data-ttu-id="9bd30-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="9bd30-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="9bd30-116">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="9bd30-116">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="9bd30-117">put_Response</span><span class="sxs-lookup"><span data-stu-id="9bd30-117">put_Response</span></span>](#put_response) | <span data-ttu-id="9bd30-118">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="9bd30-118">Set the Response property.</span></span>

## <span data-ttu-id="9bd30-119">Ses</span><span class="sxs-lookup"><span data-stu-id="9bd30-119">Members</span></span>

#### <span data-ttu-id="9bd30-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="9bd30-120">get_Request</span></span> 

<span data-ttu-id="9bd30-121">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="9bd30-121">The HTTP request.</span></span>

> <span data-ttu-id="9bd30-122">[get_Request](#get_request)par le biais[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9bd30-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="9bd30-123">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="9bd30-123">get_ResourceContext</span></span> 

<span data-ttu-id="9bd30-124">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="9bd30-124">The web resource request contexts.</span></span>

> <span data-ttu-id="9bd30-125">[get_ResourceContext](#get_resourcecontext)par le biais du public HRESULT (COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* Context)</span><span class="sxs-lookup"><span data-stu-id="9bd30-125">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="9bd30-126">get_Response</span><span class="sxs-lookup"><span data-stu-id="9bd30-126">get_Response</span></span> 

<span data-ttu-id="9bd30-127">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="9bd30-127">The HTTP response.</span></span>

> <span data-ttu-id="9bd30-128">valeur publique HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="9bd30-128">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

#### <span data-ttu-id="9bd30-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="9bd30-129">GetDeferral</span></span> 

<span data-ttu-id="9bd30-130">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="9bd30-130">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="9bd30-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="9bd30-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="9bd30-132">Vous pouvez utiliser l’objet [ICoreWebView2Deferral](icorewebview2deferral.md) pour terminer la requête réseau ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="9bd30-132">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="9bd30-133">put_Response</span><span class="sxs-lookup"><span data-stu-id="9bd30-133">put_Response</span></span> 

<span data-ttu-id="9bd30-134">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="9bd30-134">Set the Response property.</span></span>

> <span data-ttu-id="9bd30-135">[put_Response](#put_response)par le biais du public[HRESULT (réponse](icorewebview2webresourceresponse.md) )</span><span class="sxs-lookup"><span data-stu-id="9bd30-135">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>

