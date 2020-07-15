---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2HttpRequestHeaders
ms.openlocfilehash: 903355ff04463ad86f1e25771f5f321f7d0df479
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879162"
---
# <span data-ttu-id="cfbeb-104">interface ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="cfbeb-104">interface ICoreWebView2HttpRequestHeaders</span></span> 

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="cfbeb-105">En-têtes de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="cfbeb-105">HTTP request headers.</span></span>

## <span data-ttu-id="cfbeb-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="cfbeb-106">Summary</span></span>

 <span data-ttu-id="cfbeb-107">Ses</span><span class="sxs-lookup"><span data-stu-id="cfbeb-107">Members</span></span>                        | <span data-ttu-id="cfbeb-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="cfbeb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cfbeb-109">Contains</span><span class="sxs-lookup"><span data-stu-id="cfbeb-109">Contains</span></span>](#contains) | <span data-ttu-id="cfbeb-110">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="cfbeb-110">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="cfbeb-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="cfbeb-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="cfbeb-112">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="cfbeb-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="cfbeb-113">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="cfbeb-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="cfbeb-114">Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.</span><span class="sxs-lookup"><span data-stu-id="cfbeb-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="cfbeb-115">GetIterator</span><span class="sxs-lookup"><span data-stu-id="cfbeb-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="cfbeb-116">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="cfbeb-116">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="cfbeb-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="cfbeb-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="cfbeb-118">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="cfbeb-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="cfbeb-119">SetHeader</span><span class="sxs-lookup"><span data-stu-id="cfbeb-119">SetHeader</span></span>](#setheader) | <span data-ttu-id="cfbeb-120">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="cfbeb-120">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="cfbeb-121">Utilisé pour inspecter la requête HTTP sur l’événement WebResourceRequested et l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="cfbeb-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="cfbeb-122">Remarque: vous pouvez modifier les en-têtes de requête HTTP à partir d’un événement WebResourceRequested, mais pas à partir d’un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="cfbeb-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="cfbeb-123">Ses</span><span class="sxs-lookup"><span data-stu-id="cfbeb-123">Members</span></span>

#### <span data-ttu-id="cfbeb-124">Contains</span><span class="sxs-lookup"><span data-stu-id="cfbeb-124">Contains</span></span> 

<span data-ttu-id="cfbeb-125">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="cfbeb-125">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="cfbeb-126">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="cfbeb-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="cfbeb-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="cfbeb-127">GetHeader</span></span> 

<span data-ttu-id="cfbeb-128">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="cfbeb-128">Gets the header value matching the name.</span></span>

> <span data-ttu-id="cfbeb-129">public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="cfbeb-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="cfbeb-130">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="cfbeb-130">GetHeaders</span></span> 

<span data-ttu-id="cfbeb-131">Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.</span><span class="sxs-lookup"><span data-stu-id="cfbeb-131">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="cfbeb-132">public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="cfbeb-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="cfbeb-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="cfbeb-133">GetIterator</span></span> 

<span data-ttu-id="cfbeb-134">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="cfbeb-134">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="cfbeb-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="cfbeb-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="cfbeb-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="cfbeb-136">RemoveHeader</span></span> 

<span data-ttu-id="cfbeb-137">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="cfbeb-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="cfbeb-138">public HRESULT [RemoveHeader](#removeheader)(nom LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="cfbeb-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="cfbeb-139">SetHeader</span><span class="sxs-lookup"><span data-stu-id="cfbeb-139">SetHeader</span></span> 

<span data-ttu-id="cfbeb-140">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="cfbeb-140">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="cfbeb-141">public HRESULT [setHeader](#setheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="cfbeb-141">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>

