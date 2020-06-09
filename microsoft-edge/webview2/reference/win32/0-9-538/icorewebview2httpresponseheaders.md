---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 508ecacc867330c73132ae7e446b7483ea002f83
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698719"
---
# <span data-ttu-id="eb1d6-104">interface ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="eb1d6-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="eb1d6-105">En-têtes de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="eb1d6-105">HTTP response headers.</span></span>

## <span data-ttu-id="eb1d6-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="eb1d6-106">Summary</span></span>

 <span data-ttu-id="eb1d6-107">Ses</span><span class="sxs-lookup"><span data-stu-id="eb1d6-107">Members</span></span>                        | <span data-ttu-id="eb1d6-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="eb1d6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eb1d6-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="eb1d6-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="eb1d6-110">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="eb1d6-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="eb1d6-111">Contains</span><span class="sxs-lookup"><span data-stu-id="eb1d6-111">Contains</span></span>](#contains) | <span data-ttu-id="eb1d6-112">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="eb1d6-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="eb1d6-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="eb1d6-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="eb1d6-114">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="eb1d6-114">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="eb1d6-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="eb1d6-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="eb1d6-116">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="eb1d6-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="eb1d6-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="eb1d6-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="eb1d6-118">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="eb1d6-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="eb1d6-119">Utilisé pour construire un WebResourceResponse pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="eb1d6-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="eb1d6-120">Ses</span><span class="sxs-lookup"><span data-stu-id="eb1d6-120">Members</span></span>

#### <span data-ttu-id="eb1d6-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="eb1d6-121">AppendHeader</span></span> 

<span data-ttu-id="eb1d6-122">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="eb1d6-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="eb1d6-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="eb1d6-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name, LPCWSTR value)</span></span>

#### <span data-ttu-id="eb1d6-124">Contains</span><span class="sxs-lookup"><span data-stu-id="eb1d6-124">Contains</span></span> 

<span data-ttu-id="eb1d6-125">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="eb1d6-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="eb1d6-126">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="eb1d6-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="eb1d6-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="eb1d6-127">GetHeader</span></span> 

<span data-ttu-id="eb1d6-128">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="eb1d6-128">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="eb1d6-129">public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="eb1d6-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="eb1d6-130">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="eb1d6-130">GetHeaders</span></span> 

<span data-ttu-id="eb1d6-131">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="eb1d6-131">Gets the header values matching the name.</span></span>

> <span data-ttu-id="eb1d6-132">public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="eb1d6-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="eb1d6-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="eb1d6-133">GetIterator</span></span> 

<span data-ttu-id="eb1d6-134">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="eb1d6-134">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="eb1d6-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="eb1d6-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

