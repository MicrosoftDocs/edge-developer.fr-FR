---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: b23b724977b9d164c48dc99d0da2e64d61539549
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653613"
---
# <span data-ttu-id="6c608-104">interface ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="6c608-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="6c608-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="6c608-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="6c608-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="6c608-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="6c608-107">En-têtes de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="6c608-107">HTTP response headers.</span></span>

## <span data-ttu-id="6c608-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="6c608-108">Summary</span></span>

 <span data-ttu-id="6c608-109">Ses</span><span class="sxs-lookup"><span data-stu-id="6c608-109">Members</span></span>                        | <span data-ttu-id="6c608-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6c608-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6c608-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="6c608-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="6c608-112">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="6c608-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="6c608-113">Contains</span><span class="sxs-lookup"><span data-stu-id="6c608-113">Contains</span></span>](#contains) | <span data-ttu-id="6c608-114">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="6c608-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="6c608-115">GetHeader</span><span class="sxs-lookup"><span data-stu-id="6c608-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="6c608-116">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="6c608-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="6c608-117">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="6c608-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="6c608-118">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="6c608-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="6c608-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="6c608-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="6c608-120">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="6c608-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="6c608-121">Utilisé pour construire un WebResourceResponse pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="6c608-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="6c608-122">Ses</span><span class="sxs-lookup"><span data-stu-id="6c608-122">Members</span></span>

#### <span data-ttu-id="6c608-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="6c608-123">AppendHeader</span></span> 

<span data-ttu-id="6c608-124">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="6c608-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="6c608-125">public HRESULT [AppendHeader](#appendheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="6c608-125">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="6c608-126">Contains</span><span class="sxs-lookup"><span data-stu-id="6c608-126">Contains</span></span> 

<span data-ttu-id="6c608-127">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="6c608-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="6c608-128">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="6c608-128">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="6c608-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="6c608-129">GetHeader</span></span> 

<span data-ttu-id="6c608-130">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="6c608-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="6c608-131">public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="6c608-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="6c608-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="6c608-132">GetHeaders</span></span> 

<span data-ttu-id="6c608-133">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="6c608-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="6c608-134">public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="6c608-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="6c608-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="6c608-135">GetIterator</span></span> 

<span data-ttu-id="6c608-136">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="6c608-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="6c608-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="6c608-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

