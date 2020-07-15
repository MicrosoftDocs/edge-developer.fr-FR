---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: a67c5c267178ea873cd12d8a22dea7409b260d52
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880996"
---
# <span data-ttu-id="29102-104">0.9.430-interface ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="29102-104">0.9.430 - interface ICoreWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="29102-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="29102-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="29102-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="29102-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="29102-107">En-têtes de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="29102-107">HTTP request headers.</span></span>

## <span data-ttu-id="29102-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="29102-108">Summary</span></span>

 <span data-ttu-id="29102-109">Ses</span><span class="sxs-lookup"><span data-stu-id="29102-109">Members</span></span>                        | <span data-ttu-id="29102-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="29102-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="29102-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="29102-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="29102-112">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="29102-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="29102-113">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="29102-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="29102-114">Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.</span><span class="sxs-lookup"><span data-stu-id="29102-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="29102-115">Contains</span><span class="sxs-lookup"><span data-stu-id="29102-115">Contains</span></span>](#contains) | <span data-ttu-id="29102-116">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="29102-116">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="29102-117">SetHeader</span><span class="sxs-lookup"><span data-stu-id="29102-117">SetHeader</span></span>](#setheader) | <span data-ttu-id="29102-118">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="29102-118">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="29102-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="29102-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="29102-120">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="29102-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="29102-121">GetIterator</span><span class="sxs-lookup"><span data-stu-id="29102-121">GetIterator</span></span>](#getiterator) | <span data-ttu-id="29102-122">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="29102-122">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="29102-123">Utilisé pour inspecter la requête HTTP sur l’événement WebResourceRequested et l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="29102-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="29102-124">Remarque: vous pouvez modifier les en-têtes de requête HTTP à partir d’un événement WebResourceRequested, mais pas à partir d’un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="29102-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="29102-125">Ses</span><span class="sxs-lookup"><span data-stu-id="29102-125">Members</span></span>

#### <span data-ttu-id="29102-126">GetHeader</span><span class="sxs-lookup"><span data-stu-id="29102-126">GetHeader</span></span> 

<span data-ttu-id="29102-127">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="29102-127">Gets the header value matching the name.</span></span>

> <span data-ttu-id="29102-128">public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="29102-128">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="29102-129">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="29102-129">GetHeaders</span></span> 

<span data-ttu-id="29102-130">Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.</span><span class="sxs-lookup"><span data-stu-id="29102-130">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="29102-131">public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="29102-131">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="29102-132">Contains</span><span class="sxs-lookup"><span data-stu-id="29102-132">Contains</span></span> 

<span data-ttu-id="29102-133">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="29102-133">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="29102-134">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="29102-134">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="29102-135">SetHeader</span><span class="sxs-lookup"><span data-stu-id="29102-135">SetHeader</span></span> 

<span data-ttu-id="29102-136">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="29102-136">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="29102-137">public HRESULT [setHeader](#setheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="29102-137">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="29102-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="29102-138">RemoveHeader</span></span> 

<span data-ttu-id="29102-139">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="29102-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="29102-140">public HRESULT [RemoveHeader](#removeheader)(nom LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="29102-140">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="29102-141">GetIterator</span><span class="sxs-lookup"><span data-stu-id="29102-141">GetIterator</span></span> 

<span data-ttu-id="29102-142">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="29102-142">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="29102-143">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="29102-143">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

