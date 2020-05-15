---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 0f3564fa96bc1c13527cbf3b26ce92114d44eae4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653460"
---
# <span data-ttu-id="61e61-104">interface IWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="61e61-104">interface IWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="61e61-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="61e61-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="61e61-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="61e61-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="61e61-107">En-têtes de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="61e61-107">HTTP response headers.</span></span>

## <span data-ttu-id="61e61-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="61e61-108">Summary</span></span>

 <span data-ttu-id="61e61-109">Ses</span><span class="sxs-lookup"><span data-stu-id="61e61-109">Members</span></span>                        | <span data-ttu-id="61e61-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="61e61-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="61e61-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="61e61-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="61e61-112">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="61e61-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="61e61-113">Contains</span><span class="sxs-lookup"><span data-stu-id="61e61-113">Contains</span></span>](#contains) | <span data-ttu-id="61e61-114">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="61e61-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="61e61-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="61e61-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="61e61-116">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="61e61-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="61e61-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="61e61-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="61e61-118">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="61e61-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="61e61-119">Utilisé pour construire un WebResourceResponse pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="61e61-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="61e61-120">Ses</span><span class="sxs-lookup"><span data-stu-id="61e61-120">Members</span></span>

#### <span data-ttu-id="61e61-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="61e61-121">AppendHeader</span></span> 

<span data-ttu-id="61e61-122">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="61e61-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="61e61-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="61e61-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="61e61-124">Contains</span><span class="sxs-lookup"><span data-stu-id="61e61-124">Contains</span></span> 

<span data-ttu-id="61e61-125">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="61e61-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="61e61-126">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="61e61-126">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="61e61-127">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="61e61-127">GetHeaders</span></span> 

<span data-ttu-id="61e61-128">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="61e61-128">Gets the header values matching the name.</span></span>

> <span data-ttu-id="61e61-129">public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="61e61-129">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="61e61-130">GetIterator</span><span class="sxs-lookup"><span data-stu-id="61e61-130">GetIterator</span></span> 

<span data-ttu-id="61e61-131">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="61e61-131">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="61e61-132">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="61e61-132">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

