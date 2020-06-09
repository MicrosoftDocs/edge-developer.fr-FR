---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: e83078b6ac45fbc0b479c5d6b0fde3263a8f34fd
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698679"
---
# <span data-ttu-id="40155-104">interface ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="40155-104">interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="40155-105">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="40155-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="40155-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="40155-106">Summary</span></span>

 <span data-ttu-id="40155-107">Ses</span><span class="sxs-lookup"><span data-stu-id="40155-107">Members</span></span>                        | <span data-ttu-id="40155-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="40155-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="40155-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="40155-109">get_Request</span></span>](#get_request) | <span data-ttu-id="40155-110">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="40155-110">The HTTP request.</span></span>
[<span data-ttu-id="40155-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="40155-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="40155-112">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="40155-112">The web resource request contexts.</span></span>
[<span data-ttu-id="40155-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="40155-113">get_Response</span></span>](#get_response) | <span data-ttu-id="40155-114">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="40155-114">The HTTP response.</span></span>
[<span data-ttu-id="40155-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="40155-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="40155-116">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="40155-116">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="40155-117">put_Response</span><span class="sxs-lookup"><span data-stu-id="40155-117">put_Response</span></span>](#put_response) | <span data-ttu-id="40155-118">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="40155-118">Set the Response property.</span></span>

## <span data-ttu-id="40155-119">Ses</span><span class="sxs-lookup"><span data-stu-id="40155-119">Members</span></span>

#### <span data-ttu-id="40155-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="40155-120">get_Request</span></span> 

<span data-ttu-id="40155-121">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="40155-121">The HTTP request.</span></span>

> <span data-ttu-id="40155-122">[get_Request](#get_request)par le biais[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="40155-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="40155-123">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="40155-123">get_ResourceContext</span></span> 

<span data-ttu-id="40155-124">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="40155-124">The web resource request contexts.</span></span>

> <span data-ttu-id="40155-125">[get_ResourceContext](#get_resourcecontext)par le biais du public HRESULT (COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* Context)</span><span class="sxs-lookup"><span data-stu-id="40155-125">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="40155-126">get_Response</span><span class="sxs-lookup"><span data-stu-id="40155-126">get_Response</span></span> 

<span data-ttu-id="40155-127">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="40155-127">The HTTP response.</span></span>

> <span data-ttu-id="40155-128">valeur publique HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="40155-128">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

#### <span data-ttu-id="40155-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="40155-129">GetDeferral</span></span> 

<span data-ttu-id="40155-130">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="40155-130">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="40155-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="40155-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="40155-132">Vous pouvez utiliser l’objet [ICoreWebView2Deferral](icorewebview2deferral.md) pour terminer la requête réseau ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="40155-132">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="40155-133">put_Response</span><span class="sxs-lookup"><span data-stu-id="40155-133">put_Response</span></span> 

<span data-ttu-id="40155-134">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="40155-134">Set the Response property.</span></span>

> <span data-ttu-id="40155-135">[put_Response](#put_response)par le biais du public[HRESULT (réponse](icorewebview2webresourceresponse.md) )</span><span class="sxs-lookup"><span data-stu-id="40155-135">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>

