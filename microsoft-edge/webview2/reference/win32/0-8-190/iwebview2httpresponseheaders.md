---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 077c85b2458c2cf843c4d2f0548d17ec01ba4751
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885960"
---
# <span data-ttu-id="228bf-104">0.8.355-interface IWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="228bf-104">0.8.355 - interface IWebView2HttpResponseHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="228bf-105">En-têtes de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="228bf-105">HTTP response headers.</span></span>

## <span data-ttu-id="228bf-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="228bf-106">Summary</span></span>

 <span data-ttu-id="228bf-107">Ses</span><span class="sxs-lookup"><span data-stu-id="228bf-107">Members</span></span>                        | <span data-ttu-id="228bf-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="228bf-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="228bf-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="228bf-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="228bf-110">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="228bf-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="228bf-111">Contains</span><span class="sxs-lookup"><span data-stu-id="228bf-111">Contains</span></span>](#contains) | <span data-ttu-id="228bf-112">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="228bf-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="228bf-113">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="228bf-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="228bf-114">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="228bf-114">Gets the header values matching the name.</span></span>
[<span data-ttu-id="228bf-115">GetIterator</span><span class="sxs-lookup"><span data-stu-id="228bf-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="228bf-116">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="228bf-116">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="228bf-117">Utilisé pour construire un WebResourceResponse pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="228bf-117">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="228bf-118">Ses</span><span class="sxs-lookup"><span data-stu-id="228bf-118">Members</span></span>

#### <span data-ttu-id="228bf-119">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="228bf-119">AppendHeader</span></span> 

<span data-ttu-id="228bf-120">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="228bf-120">Appends header line with name and value.</span></span>

> <span data-ttu-id="228bf-121">public HRESULT [AppendHeader](#appendheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="228bf-121">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="228bf-122">Contains</span><span class="sxs-lookup"><span data-stu-id="228bf-122">Contains</span></span> 

<span data-ttu-id="228bf-123">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="228bf-123">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="228bf-124">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="228bf-124">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="228bf-125">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="228bf-125">GetHeaders</span></span> 

<span data-ttu-id="228bf-126">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="228bf-126">Gets the header values matching the name.</span></span>

> <span data-ttu-id="228bf-127">public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="228bf-127">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="228bf-128">GetIterator</span><span class="sxs-lookup"><span data-stu-id="228bf-128">GetIterator</span></span> 

<span data-ttu-id="228bf-129">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="228bf-129">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="228bf-130">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="228bf-130">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

