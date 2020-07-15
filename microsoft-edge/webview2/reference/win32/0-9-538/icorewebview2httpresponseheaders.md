---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2HttpResponseHeaders
ms.openlocfilehash: 359e79b2ecfd92ee0b7dc608a5ae5748ff6f20ce
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878742"
---
# <span data-ttu-id="f9505-104">interface ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="f9505-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="f9505-105">En-têtes de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="f9505-105">HTTP response headers.</span></span>

## <span data-ttu-id="f9505-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="f9505-106">Summary</span></span>

 <span data-ttu-id="f9505-107">Ses</span><span class="sxs-lookup"><span data-stu-id="f9505-107">Members</span></span>                        | <span data-ttu-id="f9505-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f9505-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f9505-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="f9505-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="f9505-110">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="f9505-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="f9505-111">Contains</span><span class="sxs-lookup"><span data-stu-id="f9505-111">Contains</span></span>](#contains) | <span data-ttu-id="f9505-112">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="f9505-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="f9505-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="f9505-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="f9505-114">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="f9505-114">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="f9505-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="f9505-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="f9505-116">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="f9505-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="f9505-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="f9505-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="f9505-118">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="f9505-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="f9505-119">Utilisé pour construire un WebResourceResponse pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="f9505-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="f9505-120">Ses</span><span class="sxs-lookup"><span data-stu-id="f9505-120">Members</span></span>

#### <span data-ttu-id="f9505-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="f9505-121">AppendHeader</span></span> 

<span data-ttu-id="f9505-122">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="f9505-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="f9505-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="f9505-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name, LPCWSTR value)</span></span>

#### <span data-ttu-id="f9505-124">Contains</span><span class="sxs-lookup"><span data-stu-id="f9505-124">Contains</span></span> 

<span data-ttu-id="f9505-125">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="f9505-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="f9505-126">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="f9505-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="f9505-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="f9505-127">GetHeader</span></span> 

<span data-ttu-id="f9505-128">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="f9505-128">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="f9505-129">public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="f9505-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="f9505-130">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="f9505-130">GetHeaders</span></span> 

<span data-ttu-id="f9505-131">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="f9505-131">Gets the header values matching the name.</span></span>

> <span data-ttu-id="f9505-132">public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="f9505-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="f9505-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="f9505-133">GetIterator</span></span> 

<span data-ttu-id="f9505-134">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="f9505-134">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="f9505-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="f9505-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

