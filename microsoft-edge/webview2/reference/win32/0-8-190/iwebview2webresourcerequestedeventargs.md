---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 40474d6b1169467022e5bb47e82eba3883edc2aa
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878098"
---
# <span data-ttu-id="d13b4-104">0.8.355-interface IWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d13b4-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="d13b4-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="d13b4-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="d13b4-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="d13b4-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="d13b4-107">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d13b4-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="d13b4-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="d13b4-108">Summary</span></span>

 <span data-ttu-id="d13b4-109">Ses</span><span class="sxs-lookup"><span data-stu-id="d13b4-109">Members</span></span>                        | <span data-ttu-id="d13b4-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d13b4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d13b4-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="d13b4-111">get_Request</span></span>](#get_request) | <span data-ttu-id="d13b4-112">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="d13b4-112">The HTTP request.</span></span>
[<span data-ttu-id="d13b4-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="d13b4-113">get_Response</span></span>](#get_response) | <span data-ttu-id="d13b4-114">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="d13b4-114">The HTTP response.</span></span>
[<span data-ttu-id="d13b4-115">put_Response</span><span class="sxs-lookup"><span data-stu-id="d13b4-115">put_Response</span></span>](#put_response) | <span data-ttu-id="d13b4-116">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="d13b4-116">Set the Response property.</span></span>
[<span data-ttu-id="d13b4-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d13b4-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="d13b4-118">Obtenez un objet [IWebView2Deferral](IWebView2Deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="d13b4-118">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

## <span data-ttu-id="d13b4-119">Ses</span><span class="sxs-lookup"><span data-stu-id="d13b4-119">Members</span></span>

#### <span data-ttu-id="d13b4-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="d13b4-120">get_Request</span></span> 

<span data-ttu-id="d13b4-121">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="d13b4-121">The HTTP request.</span></span>

> <span data-ttu-id="d13b4-122">[get_Request](#get_request)par le biais[IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="d13b4-122">public HRESULT [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="d13b4-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="d13b4-123">get_Response</span></span> 

<span data-ttu-id="d13b4-124">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="d13b4-124">The HTTP response.</span></span>

> <span data-ttu-id="d13b4-125">valeur publique HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="d13b4-125">public HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="d13b4-126">put_Response</span><span class="sxs-lookup"><span data-stu-id="d13b4-126">put_Response</span></span> 

<span data-ttu-id="d13b4-127">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="d13b4-127">Set the Response property.</span></span>

> <span data-ttu-id="d13b4-128">[put_Response](#put_response)par le biais du public[HRESULT (réponse](IWebView2WebResourceResponse.md) )</span><span class="sxs-lookup"><span data-stu-id="d13b4-128">public HRESULT [put_Response](#put_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="d13b4-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d13b4-129">GetDeferral</span></span> 

<span data-ttu-id="d13b4-130">Obtenez un objet [IWebView2Deferral](IWebView2Deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="d13b4-130">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="d13b4-131">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="d13b4-131">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="d13b4-132">Vous pouvez utiliser l’objet [IWebView2Deferral](IWebView2Deferral.md) pour terminer la requête réseau ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d13b4-132">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the network request at a later time.</span></span>

