---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 70a7d997dfd89b6d9bb8eb8af9a87ff0a130b69f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880303"
---
# <span data-ttu-id="d213f-104">0.9.515-interface ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d213f-104">0.9.515 - interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="d213f-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="d213f-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="d213f-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="d213f-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="d213f-107">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d213f-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="d213f-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="d213f-108">Summary</span></span>

 <span data-ttu-id="d213f-109">Ses</span><span class="sxs-lookup"><span data-stu-id="d213f-109">Members</span></span>                        | <span data-ttu-id="d213f-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d213f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d213f-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="d213f-111">get_Request</span></span>](#get_request) | <span data-ttu-id="d213f-112">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="d213f-112">The HTTP request.</span></span>
[<span data-ttu-id="d213f-113">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="d213f-113">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="d213f-114">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="d213f-114">The web resource request contexts.</span></span>
[<span data-ttu-id="d213f-115">get_Response</span><span class="sxs-lookup"><span data-stu-id="d213f-115">get_Response</span></span>](#get_response) | <span data-ttu-id="d213f-116">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="d213f-116">The HTTP response.</span></span>
[<span data-ttu-id="d213f-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d213f-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="d213f-118">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="d213f-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="d213f-119">put_Response</span><span class="sxs-lookup"><span data-stu-id="d213f-119">put_Response</span></span>](#put_response) | <span data-ttu-id="d213f-120">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="d213f-120">Set the Response property.</span></span>

## <span data-ttu-id="d213f-121">Ses</span><span class="sxs-lookup"><span data-stu-id="d213f-121">Members</span></span>

#### <span data-ttu-id="d213f-122">get_Request</span><span class="sxs-lookup"><span data-stu-id="d213f-122">get_Request</span></span> 

<span data-ttu-id="d213f-123">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="d213f-123">The HTTP request.</span></span>

> <span data-ttu-id="d213f-124">[get_Request](#get_request)par le biais[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="d213f-124">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="d213f-125">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="d213f-125">get_ResourceContext</span></span> 

<span data-ttu-id="d213f-126">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="d213f-126">The web resource request contexts.</span></span>

> <span data-ttu-id="d213f-127">[get_ResourceContext](#get_resourcecontext)par le biais du public HRESULT (COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* Context)</span><span class="sxs-lookup"><span data-stu-id="d213f-127">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="d213f-128">get_Response</span><span class="sxs-lookup"><span data-stu-id="d213f-128">get_Response</span></span> 

<span data-ttu-id="d213f-129">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="d213f-129">The HTTP response.</span></span>

> <span data-ttu-id="d213f-130">valeur publique HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="d213f-130">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

#### <span data-ttu-id="d213f-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d213f-131">GetDeferral</span></span> 

<span data-ttu-id="d213f-132">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="d213f-132">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="d213f-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="d213f-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="d213f-134">Vous pouvez utiliser l’objet [ICoreWebView2Deferral](icorewebview2deferral.md) pour terminer la requête réseau ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d213f-134">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="d213f-135">put_Response</span><span class="sxs-lookup"><span data-stu-id="d213f-135">put_Response</span></span> 

<span data-ttu-id="d213f-136">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="d213f-136">Set the Response property.</span></span>

> <span data-ttu-id="d213f-137">[put_Response](#put_response)par le biais du public[HRESULT (réponse](icorewebview2webresourceresponse.md) )</span><span class="sxs-lookup"><span data-stu-id="d213f-137">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>

