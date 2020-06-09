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
ms.openlocfilehash: 63044cae80aebfb1e759070ec797673b0c9378d2
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697251"
---
# <span data-ttu-id="3fe7a-104">interface ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="3fe7a-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="3fe7a-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="3fe7a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="3fe7a-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="3fe7a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="3fe7a-107">En-têtes de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="3fe7a-107">HTTP response headers.</span></span>

## <span data-ttu-id="3fe7a-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="3fe7a-108">Summary</span></span>

 <span data-ttu-id="3fe7a-109">Ses</span><span class="sxs-lookup"><span data-stu-id="3fe7a-109">Members</span></span>                        | <span data-ttu-id="3fe7a-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3fe7a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3fe7a-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="3fe7a-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="3fe7a-112">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="3fe7a-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="3fe7a-113">Contains</span><span class="sxs-lookup"><span data-stu-id="3fe7a-113">Contains</span></span>](#contains) | <span data-ttu-id="3fe7a-114">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="3fe7a-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="3fe7a-115">GetHeader</span><span class="sxs-lookup"><span data-stu-id="3fe7a-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="3fe7a-116">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="3fe7a-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="3fe7a-117">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="3fe7a-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="3fe7a-118">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="3fe7a-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="3fe7a-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="3fe7a-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="3fe7a-120">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="3fe7a-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="3fe7a-121">Utilisé pour construire un WebResourceResponse pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="3fe7a-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="3fe7a-122">Ses</span><span class="sxs-lookup"><span data-stu-id="3fe7a-122">Members</span></span>

#### <span data-ttu-id="3fe7a-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="3fe7a-123">AppendHeader</span></span> 

<span data-ttu-id="3fe7a-124">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="3fe7a-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="3fe7a-125">public HRESULT [AppendHeader](#appendheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="3fe7a-125">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name, LPCWSTR value)</span></span>

#### <span data-ttu-id="3fe7a-126">Contains</span><span class="sxs-lookup"><span data-stu-id="3fe7a-126">Contains</span></span> 

<span data-ttu-id="3fe7a-127">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="3fe7a-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="3fe7a-128">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="3fe7a-128">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="3fe7a-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="3fe7a-129">GetHeader</span></span> 

<span data-ttu-id="3fe7a-130">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="3fe7a-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="3fe7a-131">public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="3fe7a-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="3fe7a-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="3fe7a-132">GetHeaders</span></span> 

<span data-ttu-id="3fe7a-133">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="3fe7a-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="3fe7a-134">public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="3fe7a-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="3fe7a-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="3fe7a-135">GetIterator</span></span> 

<span data-ttu-id="3fe7a-136">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="3fe7a-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="3fe7a-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="3fe7a-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

