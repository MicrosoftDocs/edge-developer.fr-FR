---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: b3d3e6bc3efae663d78fab2f6b74dc43a88120b7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884511"
---
# <span data-ttu-id="0acfa-104">interface ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="0acfa-104">interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="0acfa-105">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="0acfa-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="0acfa-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="0acfa-106">Summary</span></span>

 <span data-ttu-id="0acfa-107">Ses</span><span class="sxs-lookup"><span data-stu-id="0acfa-107">Members</span></span>                        | <span data-ttu-id="0acfa-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0acfa-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0acfa-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="0acfa-109">get_Request</span></span>](#get_request) | <span data-ttu-id="0acfa-110">Demande de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="0acfa-110">The Web resource request.</span></span>
[<span data-ttu-id="0acfa-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="0acfa-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="0acfa-112">Contexte de demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="0acfa-112">The web resource request context.</span></span>
[<span data-ttu-id="0acfa-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="0acfa-113">get_Response</span></span>](#get_response) | <span data-ttu-id="0acfa-114">Espace réservé à l’objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="0acfa-114">A placeholder for the web resource response object.</span></span>
[<span data-ttu-id="0acfa-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="0acfa-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="0acfa-116">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="0acfa-116">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="0acfa-117">put_Response</span><span class="sxs-lookup"><span data-stu-id="0acfa-117">put_Response</span></span>](#put_response) | <span data-ttu-id="0acfa-118">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="0acfa-118">Set the Response property.</span></span>

## <span data-ttu-id="0acfa-119">Ses</span><span class="sxs-lookup"><span data-stu-id="0acfa-119">Members</span></span>

#### <span data-ttu-id="0acfa-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="0acfa-120">get_Request</span></span> 

<span data-ttu-id="0acfa-121">Demande de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="0acfa-121">The Web resource request.</span></span>

> <span data-ttu-id="0acfa-122">[get_Request](#get_request)par le biais[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0acfa-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

<span data-ttu-id="0acfa-123">Il est possible que l’objet de requête ne dispose pas de certains en-têtes ajoutés par la pile réseau plus tard.</span><span class="sxs-lookup"><span data-stu-id="0acfa-123">The request object may be missing some headers that are added by network stack later on.</span></span>

#### <span data-ttu-id="0acfa-124">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="0acfa-124">get_ResourceContext</span></span> 

<span data-ttu-id="0acfa-125">Contexte de demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="0acfa-125">The web resource request context.</span></span>

> <span data-ttu-id="0acfa-126">[get_ResourceContext](#get_resourcecontext)par le biais du public HRESULT (COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* Context)</span><span class="sxs-lookup"><span data-stu-id="0acfa-126">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="0acfa-127">get_Response</span><span class="sxs-lookup"><span data-stu-id="0acfa-127">get_Response</span></span> 

<span data-ttu-id="0acfa-128">Espace réservé à l’objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="0acfa-128">A placeholder for the web resource response object.</span></span>

> <span data-ttu-id="0acfa-129">valeur publique HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="0acfa-129">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

<span data-ttu-id="0acfa-130">Si cet objet est défini, la demande de ressource Web sera exécutée avec cette réponse.</span><span class="sxs-lookup"><span data-stu-id="0acfa-130">If this object is set, the web resource request will be completed with this response.</span></span>

#### <span data-ttu-id="0acfa-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="0acfa-131">GetDeferral</span></span> 

<span data-ttu-id="0acfa-132">Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="0acfa-132">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="0acfa-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="0acfa-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="0acfa-134">Vous pouvez utiliser l’objet [ICoreWebView2Deferral](icorewebview2deferral.md) pour exécuter la requête ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="0acfa-134">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the request at a later time.</span></span>

#### <span data-ttu-id="0acfa-135">put_Response</span><span class="sxs-lookup"><span data-stu-id="0acfa-135">put_Response</span></span> 

<span data-ttu-id="0acfa-136">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="0acfa-136">Set the Response property.</span></span>

> <span data-ttu-id="0acfa-137">[put_Response](#put_response)par le biais du public[HRESULT (réponse](icorewebview2webresourceresponse.md) )</span><span class="sxs-lookup"><span data-stu-id="0acfa-137">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>

<span data-ttu-id="0acfa-138">Un objet de réponse aux ressources Web vide peut être créé à l’aide de CreateWebResourceResponse, puis modifié pour créer la réponse.</span><span class="sxs-lookup"><span data-stu-id="0acfa-138">An empty Web resource response object can be created with CreateWebResourceResponse and then modified to construct the response.</span></span>

