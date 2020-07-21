---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 04a8bf376ad7649021c4ab1555c3090cce5b52fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885610"
---
# <span data-ttu-id="885af-104">0.9.430-interface ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="885af-104">0.9.430 - interface ICoreWebView2HttpRequestHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="885af-105">En-têtes de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="885af-105">HTTP request headers.</span></span>

## <span data-ttu-id="885af-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="885af-106">Summary</span></span>

 <span data-ttu-id="885af-107">Ses</span><span class="sxs-lookup"><span data-stu-id="885af-107">Members</span></span>                        | <span data-ttu-id="885af-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="885af-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="885af-109">GetHeader</span><span class="sxs-lookup"><span data-stu-id="885af-109">GetHeader</span></span>](#getheader) | <span data-ttu-id="885af-110">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="885af-110">Gets the header value matching the name.</span></span>
[<span data-ttu-id="885af-111">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="885af-111">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="885af-112">Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.</span><span class="sxs-lookup"><span data-stu-id="885af-112">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="885af-113">Contains</span><span class="sxs-lookup"><span data-stu-id="885af-113">Contains</span></span>](#contains) | <span data-ttu-id="885af-114">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="885af-114">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="885af-115">SetHeader</span><span class="sxs-lookup"><span data-stu-id="885af-115">SetHeader</span></span>](#setheader) | <span data-ttu-id="885af-116">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="885af-116">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="885af-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="885af-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="885af-118">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="885af-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="885af-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="885af-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="885af-120">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="885af-120">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="885af-121">Utilisé pour inspecter la requête HTTP sur l’événement WebResourceRequested et l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="885af-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="885af-122">Remarque: vous pouvez modifier les en-têtes de requête HTTP à partir d’un événement WebResourceRequested, mais pas à partir d’un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="885af-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="885af-123">Ses</span><span class="sxs-lookup"><span data-stu-id="885af-123">Members</span></span>

#### <span data-ttu-id="885af-124">GetHeader</span><span class="sxs-lookup"><span data-stu-id="885af-124">GetHeader</span></span> 

<span data-ttu-id="885af-125">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="885af-125">Gets the header value matching the name.</span></span>

> <span data-ttu-id="885af-126">public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="885af-126">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="885af-127">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="885af-127">GetHeaders</span></span> 

<span data-ttu-id="885af-128">Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.</span><span class="sxs-lookup"><span data-stu-id="885af-128">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="885af-129">public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="885af-129">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="885af-130">Contains</span><span class="sxs-lookup"><span data-stu-id="885af-130">Contains</span></span> 

<span data-ttu-id="885af-131">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="885af-131">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="885af-132">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="885af-132">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="885af-133">SetHeader</span><span class="sxs-lookup"><span data-stu-id="885af-133">SetHeader</span></span> 

<span data-ttu-id="885af-134">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="885af-134">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="885af-135">public HRESULT [setHeader](#setheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="885af-135">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="885af-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="885af-136">RemoveHeader</span></span> 

<span data-ttu-id="885af-137">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="885af-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="885af-138">public HRESULT [RemoveHeader](#removeheader)(nom LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="885af-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="885af-139">GetIterator</span><span class="sxs-lookup"><span data-stu-id="885af-139">GetIterator</span></span> 

<span data-ttu-id="885af-140">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="885af-140">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="885af-141">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="885af-141">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

