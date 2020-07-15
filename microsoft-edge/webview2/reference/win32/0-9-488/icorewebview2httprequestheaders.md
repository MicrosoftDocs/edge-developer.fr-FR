---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 2587a3e07869076be659e29d484a647b74c2bd7f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880548"
---
# <span data-ttu-id="3265b-104">0.9.515-interface ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="3265b-104">0.9.515 - interface ICoreWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="3265b-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="3265b-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="3265b-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="3265b-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="3265b-107">En-têtes de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="3265b-107">HTTP request headers.</span></span>

## <span data-ttu-id="3265b-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="3265b-108">Summary</span></span>

 <span data-ttu-id="3265b-109">Ses</span><span class="sxs-lookup"><span data-stu-id="3265b-109">Members</span></span>                        | <span data-ttu-id="3265b-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3265b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3265b-111">Contains</span><span class="sxs-lookup"><span data-stu-id="3265b-111">Contains</span></span>](#contains) | <span data-ttu-id="3265b-112">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="3265b-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="3265b-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="3265b-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="3265b-114">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="3265b-114">Gets the header value matching the name.</span></span>
[<span data-ttu-id="3265b-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="3265b-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="3265b-116">Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.</span><span class="sxs-lookup"><span data-stu-id="3265b-116">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="3265b-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="3265b-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="3265b-118">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="3265b-118">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="3265b-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="3265b-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="3265b-120">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="3265b-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="3265b-121">SetHeader</span><span class="sxs-lookup"><span data-stu-id="3265b-121">SetHeader</span></span>](#setheader) | <span data-ttu-id="3265b-122">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="3265b-122">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="3265b-123">Utilisé pour inspecter la requête HTTP sur l’événement WebResourceRequested et l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="3265b-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="3265b-124">Remarque: vous pouvez modifier les en-têtes de requête HTTP à partir d’un événement WebResourceRequested, mais pas à partir d’un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="3265b-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="3265b-125">Ses</span><span class="sxs-lookup"><span data-stu-id="3265b-125">Members</span></span>

#### <span data-ttu-id="3265b-126">Contains</span><span class="sxs-lookup"><span data-stu-id="3265b-126">Contains</span></span> 

<span data-ttu-id="3265b-127">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="3265b-127">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="3265b-128">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="3265b-128">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="3265b-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="3265b-129">GetHeader</span></span> 

<span data-ttu-id="3265b-130">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="3265b-130">Gets the header value matching the name.</span></span>

> <span data-ttu-id="3265b-131">public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="3265b-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="3265b-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="3265b-132">GetHeaders</span></span> 

<span data-ttu-id="3265b-133">Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.</span><span class="sxs-lookup"><span data-stu-id="3265b-133">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="3265b-134">public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="3265b-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="3265b-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="3265b-135">GetIterator</span></span> 

<span data-ttu-id="3265b-136">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="3265b-136">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="3265b-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="3265b-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="3265b-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="3265b-138">RemoveHeader</span></span> 

<span data-ttu-id="3265b-139">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="3265b-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="3265b-140">public HRESULT [RemoveHeader](#removeheader)(nom LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="3265b-140">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="3265b-141">SetHeader</span><span class="sxs-lookup"><span data-stu-id="3265b-141">SetHeader</span></span> 

<span data-ttu-id="3265b-142">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="3265b-142">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="3265b-143">public HRESULT [setHeader](#setheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="3265b-143">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>

