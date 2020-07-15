---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 356f8bfc235e522ef5e976baf61f8c9017766a3d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880534"
---
# <span data-ttu-id="6c541-104">0.9.515-interface ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="6c541-104">0.9.515 - interface ICoreWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="6c541-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="6c541-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="6c541-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="6c541-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="6c541-107">En-têtes de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="6c541-107">HTTP response headers.</span></span>

## <span data-ttu-id="6c541-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="6c541-108">Summary</span></span>

 <span data-ttu-id="6c541-109">Ses</span><span class="sxs-lookup"><span data-stu-id="6c541-109">Members</span></span>                        | <span data-ttu-id="6c541-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6c541-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6c541-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="6c541-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="6c541-112">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="6c541-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="6c541-113">Contains</span><span class="sxs-lookup"><span data-stu-id="6c541-113">Contains</span></span>](#contains) | <span data-ttu-id="6c541-114">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="6c541-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="6c541-115">GetHeader</span><span class="sxs-lookup"><span data-stu-id="6c541-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="6c541-116">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="6c541-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="6c541-117">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="6c541-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="6c541-118">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="6c541-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="6c541-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="6c541-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="6c541-120">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="6c541-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="6c541-121">Utilisé pour construire un WebResourceResponse pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="6c541-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="6c541-122">Ses</span><span class="sxs-lookup"><span data-stu-id="6c541-122">Members</span></span>

#### <span data-ttu-id="6c541-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="6c541-123">AppendHeader</span></span> 

<span data-ttu-id="6c541-124">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="6c541-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="6c541-125">public HRESULT [AppendHeader](#appendheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="6c541-125">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name, LPCWSTR value)</span></span>

#### <span data-ttu-id="6c541-126">Contains</span><span class="sxs-lookup"><span data-stu-id="6c541-126">Contains</span></span> 

<span data-ttu-id="6c541-127">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="6c541-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="6c541-128">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="6c541-128">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="6c541-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="6c541-129">GetHeader</span></span> 

<span data-ttu-id="6c541-130">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="6c541-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="6c541-131">public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="6c541-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="6c541-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="6c541-132">GetHeaders</span></span> 

<span data-ttu-id="6c541-133">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="6c541-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="6c541-134">public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="6c541-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="6c541-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="6c541-135">GetIterator</span></span> 

<span data-ttu-id="6c541-136">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="6c541-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="6c541-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="6c541-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

