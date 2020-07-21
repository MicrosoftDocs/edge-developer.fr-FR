---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 3197368c7ce202fae3223d517d060a23a6b21ef8
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885493"
---
# <span data-ttu-id="186dc-104">0.9.515-interface ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="186dc-104">0.9.515 - interface ICoreWebView2HttpRequestHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="186dc-105">En-têtes de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="186dc-105">HTTP request headers.</span></span>

## <span data-ttu-id="186dc-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="186dc-106">Summary</span></span>

 <span data-ttu-id="186dc-107">Ses</span><span class="sxs-lookup"><span data-stu-id="186dc-107">Members</span></span>                        | <span data-ttu-id="186dc-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="186dc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="186dc-109">Contains</span><span class="sxs-lookup"><span data-stu-id="186dc-109">Contains</span></span>](#contains) | <span data-ttu-id="186dc-110">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="186dc-110">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="186dc-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="186dc-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="186dc-112">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="186dc-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="186dc-113">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="186dc-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="186dc-114">Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.</span><span class="sxs-lookup"><span data-stu-id="186dc-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="186dc-115">GetIterator</span><span class="sxs-lookup"><span data-stu-id="186dc-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="186dc-116">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="186dc-116">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="186dc-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="186dc-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="186dc-118">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="186dc-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="186dc-119">SetHeader</span><span class="sxs-lookup"><span data-stu-id="186dc-119">SetHeader</span></span>](#setheader) | <span data-ttu-id="186dc-120">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="186dc-120">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="186dc-121">Utilisé pour inspecter la requête HTTP sur l’événement WebResourceRequested et l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="186dc-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="186dc-122">Remarque: vous pouvez modifier les en-têtes de requête HTTP à partir d’un événement WebResourceRequested, mais pas à partir d’un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="186dc-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="186dc-123">Ses</span><span class="sxs-lookup"><span data-stu-id="186dc-123">Members</span></span>

#### <span data-ttu-id="186dc-124">Contains</span><span class="sxs-lookup"><span data-stu-id="186dc-124">Contains</span></span> 

<span data-ttu-id="186dc-125">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="186dc-125">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="186dc-126">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="186dc-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="186dc-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="186dc-127">GetHeader</span></span> 

<span data-ttu-id="186dc-128">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="186dc-128">Gets the header value matching the name.</span></span>

> <span data-ttu-id="186dc-129">public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="186dc-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="186dc-130">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="186dc-130">GetHeaders</span></span> 

<span data-ttu-id="186dc-131">Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.</span><span class="sxs-lookup"><span data-stu-id="186dc-131">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="186dc-132">public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="186dc-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="186dc-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="186dc-133">GetIterator</span></span> 

<span data-ttu-id="186dc-134">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="186dc-134">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="186dc-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="186dc-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="186dc-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="186dc-136">RemoveHeader</span></span> 

<span data-ttu-id="186dc-137">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="186dc-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="186dc-138">public HRESULT [RemoveHeader](#removeheader)(nom LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="186dc-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="186dc-139">SetHeader</span><span class="sxs-lookup"><span data-stu-id="186dc-139">SetHeader</span></span> 

<span data-ttu-id="186dc-140">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="186dc-140">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="186dc-141">public HRESULT [setHeader](#setheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="186dc-141">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>

