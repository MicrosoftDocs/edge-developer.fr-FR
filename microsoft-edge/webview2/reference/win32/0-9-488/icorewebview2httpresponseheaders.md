---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 1daa6c3cdf03ce160968d43715f12ffa7eb41e84
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885582"
---
# <span data-ttu-id="7cbae-104">0.9.515-interface ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="7cbae-104">0.9.515 - interface ICoreWebView2HttpResponseHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="7cbae-105">En-têtes de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="7cbae-105">HTTP response headers.</span></span>

## <span data-ttu-id="7cbae-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="7cbae-106">Summary</span></span>

 <span data-ttu-id="7cbae-107">Ses</span><span class="sxs-lookup"><span data-stu-id="7cbae-107">Members</span></span>                        | <span data-ttu-id="7cbae-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="7cbae-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7cbae-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="7cbae-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="7cbae-110">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="7cbae-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="7cbae-111">Contains</span><span class="sxs-lookup"><span data-stu-id="7cbae-111">Contains</span></span>](#contains) | <span data-ttu-id="7cbae-112">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="7cbae-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="7cbae-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="7cbae-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="7cbae-114">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="7cbae-114">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="7cbae-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="7cbae-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="7cbae-116">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="7cbae-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="7cbae-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="7cbae-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="7cbae-118">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="7cbae-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="7cbae-119">Utilisé pour construire un WebResourceResponse pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="7cbae-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="7cbae-120">Ses</span><span class="sxs-lookup"><span data-stu-id="7cbae-120">Members</span></span>

#### <span data-ttu-id="7cbae-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="7cbae-121">AppendHeader</span></span> 

<span data-ttu-id="7cbae-122">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="7cbae-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="7cbae-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="7cbae-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name, LPCWSTR value)</span></span>

#### <span data-ttu-id="7cbae-124">Contains</span><span class="sxs-lookup"><span data-stu-id="7cbae-124">Contains</span></span> 

<span data-ttu-id="7cbae-125">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="7cbae-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="7cbae-126">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="7cbae-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="7cbae-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="7cbae-127">GetHeader</span></span> 

<span data-ttu-id="7cbae-128">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="7cbae-128">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="7cbae-129">public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="7cbae-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="7cbae-130">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="7cbae-130">GetHeaders</span></span> 

<span data-ttu-id="7cbae-131">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="7cbae-131">Gets the header values matching the name.</span></span>

> <span data-ttu-id="7cbae-132">public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="7cbae-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="7cbae-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="7cbae-133">GetIterator</span></span> 

<span data-ttu-id="7cbae-134">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="7cbae-134">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="7cbae-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="7cbae-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

