---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 899a6f50db1d77f3f24524c5ccec139dcbdbcaf9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653323"
---
# <span data-ttu-id="b891a-104">interface IWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b891a-104">interface IWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="b891a-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="b891a-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="b891a-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="b891a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="b891a-107">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="b891a-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="b891a-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="b891a-108">Summary</span></span>

 <span data-ttu-id="b891a-109">Ses</span><span class="sxs-lookup"><span data-stu-id="b891a-109">Members</span></span>                        | <span data-ttu-id="b891a-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b891a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b891a-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="b891a-111">get_Request</span></span>](#get_request) | <span data-ttu-id="b891a-112">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="b891a-112">The HTTP request.</span></span>
[<span data-ttu-id="b891a-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="b891a-113">get_Response</span></span>](#get_response) | <span data-ttu-id="b891a-114">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="b891a-114">The HTTP response.</span></span>
[<span data-ttu-id="b891a-115">put_Response</span><span class="sxs-lookup"><span data-stu-id="b891a-115">put_Response</span></span>](#put_response) | <span data-ttu-id="b891a-116">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="b891a-116">Set the Response property.</span></span>
[<span data-ttu-id="b891a-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b891a-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="b891a-118">Obtenez un objet [IWebView2Deferral](IWebView2Deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="b891a-118">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

## <span data-ttu-id="b891a-119">Ses</span><span class="sxs-lookup"><span data-stu-id="b891a-119">Members</span></span>

#### <span data-ttu-id="b891a-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="b891a-120">get_Request</span></span> 

<span data-ttu-id="b891a-121">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="b891a-121">The HTTP request.</span></span>

> <span data-ttu-id="b891a-122">[get_Request](#get_request)par le biais[IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="b891a-122">public HRESULT [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="b891a-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="b891a-123">get_Response</span></span> 

<span data-ttu-id="b891a-124">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="b891a-124">The HTTP response.</span></span>

> <span data-ttu-id="b891a-125">valeur publique HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="b891a-125">public HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="b891a-126">put_Response</span><span class="sxs-lookup"><span data-stu-id="b891a-126">put_Response</span></span> 

<span data-ttu-id="b891a-127">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="b891a-127">Set the Response property.</span></span>

> <span data-ttu-id="b891a-128">[put_Response](#put_response)par le biais du public[HRESULT (réponse](IWebView2WebResourceResponse.md) )</span><span class="sxs-lookup"><span data-stu-id="b891a-128">public HRESULT [put_Response](#put_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="b891a-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b891a-129">GetDeferral</span></span> 

<span data-ttu-id="b891a-130">Obtenez un objet [IWebView2Deferral](IWebView2Deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="b891a-130">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="b891a-131">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="b891a-131">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="b891a-132">Vous pouvez utiliser l’objet [IWebView2Deferral](IWebView2Deferral.md) pour terminer la requête réseau ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="b891a-132">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the network request at a later time.</span></span>

