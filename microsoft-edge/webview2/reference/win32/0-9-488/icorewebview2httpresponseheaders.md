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
ms.openlocfilehash: fe03c3ab6d951ecd54bd76cd7abc89de637496ea
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653482"
---
# <span data-ttu-id="88387-104">interface ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="88387-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="88387-105">En-têtes de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="88387-105">HTTP response headers.</span></span>

## <span data-ttu-id="88387-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="88387-106">Summary</span></span>

 <span data-ttu-id="88387-107">Ses</span><span class="sxs-lookup"><span data-stu-id="88387-107">Members</span></span>                        | <span data-ttu-id="88387-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="88387-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="88387-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="88387-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="88387-110">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="88387-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="88387-111">Contains</span><span class="sxs-lookup"><span data-stu-id="88387-111">Contains</span></span>](#contains) | <span data-ttu-id="88387-112">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="88387-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="88387-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="88387-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="88387-114">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="88387-114">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="88387-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="88387-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="88387-116">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="88387-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="88387-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="88387-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="88387-118">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="88387-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="88387-119">Utilisé pour construire un WebResourceResponse pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="88387-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="88387-120">Ses</span><span class="sxs-lookup"><span data-stu-id="88387-120">Members</span></span>

#### <span data-ttu-id="88387-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="88387-121">AppendHeader</span></span> 

<span data-ttu-id="88387-122">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="88387-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="88387-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="88387-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name, LPCWSTR value)</span></span>

#### <span data-ttu-id="88387-124">Contains</span><span class="sxs-lookup"><span data-stu-id="88387-124">Contains</span></span> 

<span data-ttu-id="88387-125">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="88387-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="88387-126">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="88387-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="88387-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="88387-127">GetHeader</span></span> 

<span data-ttu-id="88387-128">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="88387-128">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="88387-129">public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="88387-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="88387-130">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="88387-130">GetHeaders</span></span> 

<span data-ttu-id="88387-131">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="88387-131">Gets the header values matching the name.</span></span>

> <span data-ttu-id="88387-132">public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="88387-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="88387-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="88387-133">GetIterator</span></span> 

<span data-ttu-id="88387-134">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="88387-134">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="88387-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="88387-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

