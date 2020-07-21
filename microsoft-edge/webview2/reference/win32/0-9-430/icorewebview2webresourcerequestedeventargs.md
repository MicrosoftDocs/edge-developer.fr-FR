---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 00aaddcc732076e4f7aa808b04132641fe7fe969
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886443"
---
# <span data-ttu-id="f1d9c-104">0.9.430-interface ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f1d9c-104">0.9.430 - interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="f1d9c-105">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="f1d9c-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="f1d9c-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="f1d9c-106">Summary</span></span>

 <span data-ttu-id="f1d9c-107">Ses</span><span class="sxs-lookup"><span data-stu-id="f1d9c-107">Members</span></span>                        | <span data-ttu-id="f1d9c-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f1d9c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f1d9c-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="f1d9c-109">get_Request</span></span>](#get_request) | <span data-ttu-id="f1d9c-110">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="f1d9c-110">The HTTP request.</span></span>
[<span data-ttu-id="f1d9c-111">get_Response</span><span class="sxs-lookup"><span data-stu-id="f1d9c-111">get_Response</span></span>](#get_response) | <span data-ttu-id="f1d9c-112">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="f1d9c-112">The HTTP response.</span></span>
[<span data-ttu-id="f1d9c-113">put_Response</span><span class="sxs-lookup"><span data-stu-id="f1d9c-113">put_Response</span></span>](#put_response) | <span data-ttu-id="f1d9c-114">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="f1d9c-114">Set the Response property.</span></span>
[<span data-ttu-id="f1d9c-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f1d9c-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="f1d9c-116">Obtenez un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="f1d9c-116">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="f1d9c-117">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="f1d9c-117">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="f1d9c-118">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="f1d9c-118">The web resource request contexts.</span></span>

## <span data-ttu-id="f1d9c-119">Ses</span><span class="sxs-lookup"><span data-stu-id="f1d9c-119">Members</span></span>

#### <span data-ttu-id="f1d9c-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="f1d9c-120">get_Request</span></span> 

<span data-ttu-id="f1d9c-121">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="f1d9c-121">The HTTP request.</span></span>

> <span data-ttu-id="f1d9c-122">[get_Request](#get_request)par le biais[ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="f1d9c-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="f1d9c-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="f1d9c-123">get_Response</span></span> 

<span data-ttu-id="f1d9c-124">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="f1d9c-124">The HTTP response.</span></span>

> <span data-ttu-id="f1d9c-125">valeur publique HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="f1d9c-125">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="f1d9c-126">put_Response</span><span class="sxs-lookup"><span data-stu-id="f1d9c-126">put_Response</span></span> 

<span data-ttu-id="f1d9c-127">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="f1d9c-127">Set the Response property.</span></span>

> <span data-ttu-id="f1d9c-128">[put_Response](#put_response)par le biais du public[HRESULT (réponse](ICoreWebView2WebResourceResponse.md) )</span><span class="sxs-lookup"><span data-stu-id="f1d9c-128">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="f1d9c-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f1d9c-129">GetDeferral</span></span> 

<span data-ttu-id="f1d9c-130">Obtenez un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="f1d9c-130">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="f1d9c-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="f1d9c-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="f1d9c-132">Vous pouvez utiliser l’objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) pour terminer la requête réseau ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="f1d9c-132">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="f1d9c-133">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="f1d9c-133">get_ResourceContext</span></span> 

<span data-ttu-id="f1d9c-134">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="f1d9c-134">The web resource request contexts.</span></span>

> <span data-ttu-id="f1d9c-135">[get_ResourceContext](#get_resourcecontext)par le biais du public HRESULT (CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* Context)</span><span class="sxs-lookup"><span data-stu-id="f1d9c-135">public HRESULT [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

