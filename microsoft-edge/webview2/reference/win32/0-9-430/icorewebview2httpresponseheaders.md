---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 321d18a726ac19db92018cb27d31867029991cf0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886219"
---
# <span data-ttu-id="073e7-104">0.9.430-interface ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="073e7-104">0.9.430 - interface ICoreWebView2HttpResponseHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="073e7-105">En-têtes de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="073e7-105">HTTP response headers.</span></span>

## <span data-ttu-id="073e7-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="073e7-106">Summary</span></span>

 <span data-ttu-id="073e7-107">Ses</span><span class="sxs-lookup"><span data-stu-id="073e7-107">Members</span></span>                        | <span data-ttu-id="073e7-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="073e7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="073e7-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="073e7-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="073e7-110">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="073e7-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="073e7-111">Contains</span><span class="sxs-lookup"><span data-stu-id="073e7-111">Contains</span></span>](#contains) | <span data-ttu-id="073e7-112">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="073e7-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="073e7-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="073e7-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="073e7-114">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="073e7-114">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="073e7-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="073e7-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="073e7-116">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="073e7-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="073e7-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="073e7-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="073e7-118">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="073e7-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="073e7-119">Utilisé pour construire un WebResourceResponse pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="073e7-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="073e7-120">Ses</span><span class="sxs-lookup"><span data-stu-id="073e7-120">Members</span></span>

#### <span data-ttu-id="073e7-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="073e7-121">AppendHeader</span></span> 

<span data-ttu-id="073e7-122">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="073e7-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="073e7-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="073e7-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="073e7-124">Contains</span><span class="sxs-lookup"><span data-stu-id="073e7-124">Contains</span></span> 

<span data-ttu-id="073e7-125">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="073e7-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="073e7-126">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="073e7-126">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="073e7-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="073e7-127">GetHeader</span></span> 

<span data-ttu-id="073e7-128">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="073e7-128">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="073e7-129">public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="073e7-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="073e7-130">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="073e7-130">GetHeaders</span></span> 

<span data-ttu-id="073e7-131">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="073e7-131">Gets the header values matching the name.</span></span>

> <span data-ttu-id="073e7-132">public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="073e7-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="073e7-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="073e7-133">GetIterator</span></span> 

<span data-ttu-id="073e7-134">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="073e7-134">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="073e7-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="073e7-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

