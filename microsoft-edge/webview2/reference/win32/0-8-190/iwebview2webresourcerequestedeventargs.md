---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: aa5206be13790fd7a783f2afb4471de90fc8f2ae
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885717"
---
# <span data-ttu-id="8d418-104">0.8.355-interface IWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d418-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="8d418-105">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="8d418-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="8d418-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="8d418-106">Summary</span></span>

 <span data-ttu-id="8d418-107">Ses</span><span class="sxs-lookup"><span data-stu-id="8d418-107">Members</span></span>                        | <span data-ttu-id="8d418-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="8d418-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8d418-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="8d418-109">get_Request</span></span>](#get_request) | <span data-ttu-id="8d418-110">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="8d418-110">The HTTP request.</span></span>
[<span data-ttu-id="8d418-111">get_Response</span><span class="sxs-lookup"><span data-stu-id="8d418-111">get_Response</span></span>](#get_response) | <span data-ttu-id="8d418-112">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="8d418-112">The HTTP response.</span></span>
[<span data-ttu-id="8d418-113">put_Response</span><span class="sxs-lookup"><span data-stu-id="8d418-113">put_Response</span></span>](#put_response) | <span data-ttu-id="8d418-114">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="8d418-114">Set the Response property.</span></span>
[<span data-ttu-id="8d418-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="8d418-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="8d418-116">Obtenez un objet [IWebView2Deferral](IWebView2Deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="8d418-116">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

## <span data-ttu-id="8d418-117">Ses</span><span class="sxs-lookup"><span data-stu-id="8d418-117">Members</span></span>

#### <span data-ttu-id="8d418-118">get_Request</span><span class="sxs-lookup"><span data-stu-id="8d418-118">get_Request</span></span> 

<span data-ttu-id="8d418-119">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="8d418-119">The HTTP request.</span></span>

> <span data-ttu-id="8d418-120">[get_Request](#get_request)par le biais[IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="8d418-120">public HRESULT [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="8d418-121">get_Response</span><span class="sxs-lookup"><span data-stu-id="8d418-121">get_Response</span></span> 

<span data-ttu-id="8d418-122">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="8d418-122">The HTTP response.</span></span>

> <span data-ttu-id="8d418-123">valeur publique HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="8d418-123">public HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="8d418-124">put_Response</span><span class="sxs-lookup"><span data-stu-id="8d418-124">put_Response</span></span> 

<span data-ttu-id="8d418-125">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="8d418-125">Set the Response property.</span></span>

> <span data-ttu-id="8d418-126">[put_Response](#put_response)par le biais du public[HRESULT (réponse](IWebView2WebResourceResponse.md) )</span><span class="sxs-lookup"><span data-stu-id="8d418-126">public HRESULT [put_Response](#put_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="8d418-127">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="8d418-127">GetDeferral</span></span> 

<span data-ttu-id="8d418-128">Obtenez un objet [IWebView2Deferral](IWebView2Deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="8d418-128">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="8d418-129">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="8d418-129">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="8d418-130">Vous pouvez utiliser l’objet [IWebView2Deferral](IWebView2Deferral.md) pour terminer la requête réseau ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="8d418-130">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the network request at a later time.</span></span>

