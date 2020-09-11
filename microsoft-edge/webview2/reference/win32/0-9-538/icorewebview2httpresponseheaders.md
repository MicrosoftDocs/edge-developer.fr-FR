---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2HttpResponseHeaders
ms.openlocfilehash: 6278f29f983503916e0015ab4bbac44f79ffe3d9
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011306"
---
# <span data-ttu-id="12d13-104">0.9.579-interface ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="12d13-104">0.9.579 - interface ICoreWebView2HttpResponseHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="12d13-105">En-têtes de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="12d13-105">HTTP response headers.</span></span>

## <span data-ttu-id="12d13-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="12d13-106">Summary</span></span>

 <span data-ttu-id="12d13-107">Ses</span><span class="sxs-lookup"><span data-stu-id="12d13-107">Members</span></span>                        | <span data-ttu-id="12d13-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="12d13-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="12d13-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="12d13-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="12d13-110">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="12d13-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="12d13-111">Contains</span><span class="sxs-lookup"><span data-stu-id="12d13-111">Contains</span></span>](#contains) | <span data-ttu-id="12d13-112">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="12d13-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="12d13-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="12d13-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="12d13-114">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="12d13-114">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="12d13-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="12d13-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="12d13-116">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="12d13-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="12d13-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="12d13-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="12d13-118">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="12d13-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="12d13-119">Utilisé pour construire un WebResourceResponse pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="12d13-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="12d13-120">Ses</span><span class="sxs-lookup"><span data-stu-id="12d13-120">Members</span></span>

#### <span data-ttu-id="12d13-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="12d13-121">AppendHeader</span></span> 

<span data-ttu-id="12d13-122">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="12d13-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="12d13-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="12d13-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name, LPCWSTR value)</span></span>

#### <span data-ttu-id="12d13-124">Contains</span><span class="sxs-lookup"><span data-stu-id="12d13-124">Contains</span></span> 

<span data-ttu-id="12d13-125">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="12d13-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="12d13-126">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="12d13-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="12d13-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="12d13-127">GetHeader</span></span> 

<span data-ttu-id="12d13-128">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="12d13-128">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="12d13-129">public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="12d13-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="12d13-130">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="12d13-130">GetHeaders</span></span> 

<span data-ttu-id="12d13-131">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="12d13-131">Gets the header values matching the name.</span></span>

> <span data-ttu-id="12d13-132">public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="12d13-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="12d13-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="12d13-133">GetIterator</span></span> 

<span data-ttu-id="12d13-134">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="12d13-134">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="12d13-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="12d13-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

