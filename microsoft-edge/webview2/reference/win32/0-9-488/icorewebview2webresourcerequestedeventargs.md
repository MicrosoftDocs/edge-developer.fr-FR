---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 85954a3f866ed9fd778af93fc27872af2d20eb2e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697944"
---
# <span data-ttu-id="afac9-104">interface ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="afac9-104">interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="afac9-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="afac9-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="afac9-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="afac9-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="afac9-107">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="afac9-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="afac9-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="afac9-108">Summary</span></span>

 <span data-ttu-id="afac9-109">Ses</span><span class="sxs-lookup"><span data-stu-id="afac9-109">Members</span></span>                        | <span data-ttu-id="afac9-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="afac9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="afac9-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="afac9-111">get_Request</span></span>](#get_request) | <span data-ttu-id="afac9-112">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="afac9-112">The HTTP request.</span></span>
[<span data-ttu-id="afac9-113">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="afac9-113">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="afac9-114">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="afac9-114">The web resource request contexts.</span></span>
[<span data-ttu-id="afac9-115">get_Response</span><span class="sxs-lookup"><span data-stu-id="afac9-115">get_Response</span></span>](#get_response) | <span data-ttu-id="afac9-116">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="afac9-116">The HTTP response.</span></span>
[<span data-ttu-id="afac9-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="afac9-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="afac9-118">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="afac9-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="afac9-119">put_Response</span><span class="sxs-lookup"><span data-stu-id="afac9-119">put_Response</span></span>](#put_response) | <span data-ttu-id="afac9-120">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="afac9-120">Set the Response property.</span></span>

## <span data-ttu-id="afac9-121">Ses</span><span class="sxs-lookup"><span data-stu-id="afac9-121">Members</span></span>

#### <span data-ttu-id="afac9-122">get_Request</span><span class="sxs-lookup"><span data-stu-id="afac9-122">get_Request</span></span> 

<span data-ttu-id="afac9-123">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="afac9-123">The HTTP request.</span></span>

> <span data-ttu-id="afac9-124">[get_Request](#get_request)par le biais[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="afac9-124">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="afac9-125">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="afac9-125">get_ResourceContext</span></span> 

<span data-ttu-id="afac9-126">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="afac9-126">The web resource request contexts.</span></span>

> <span data-ttu-id="afac9-127">[get_ResourceContext](#get_resourcecontext)par le biais du public HRESULT (COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* Context)</span><span class="sxs-lookup"><span data-stu-id="afac9-127">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="afac9-128">get_Response</span><span class="sxs-lookup"><span data-stu-id="afac9-128">get_Response</span></span> 

<span data-ttu-id="afac9-129">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="afac9-129">The HTTP response.</span></span>

> <span data-ttu-id="afac9-130">valeur publique HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="afac9-130">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

#### <span data-ttu-id="afac9-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="afac9-131">GetDeferral</span></span> 

<span data-ttu-id="afac9-132">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="afac9-132">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="afac9-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="afac9-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="afac9-134">Vous pouvez utiliser l’objet [ICoreWebView2Deferral](icorewebview2deferral.md) pour terminer la requête réseau ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="afac9-134">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="afac9-135">put_Response</span><span class="sxs-lookup"><span data-stu-id="afac9-135">put_Response</span></span> 

<span data-ttu-id="afac9-136">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="afac9-136">Set the Response property.</span></span>

> <span data-ttu-id="afac9-137">[put_Response](#put_response)par le biais du public[HRESULT (réponse](icorewebview2webresourceresponse.md) )</span><span class="sxs-lookup"><span data-stu-id="afac9-137">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>

