---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: e12809d1db7e8c7764ad75e9a10f44ac3f445fa4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653411"
---
# <span data-ttu-id="98ce5-104">interface ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="98ce5-104">interface ICoreWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="98ce5-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="98ce5-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="98ce5-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="98ce5-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="98ce5-107">En-têtes de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="98ce5-107">HTTP request headers.</span></span>

## <span data-ttu-id="98ce5-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="98ce5-108">Summary</span></span>

 <span data-ttu-id="98ce5-109">Ses</span><span class="sxs-lookup"><span data-stu-id="98ce5-109">Members</span></span>                        | <span data-ttu-id="98ce5-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="98ce5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="98ce5-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="98ce5-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="98ce5-112">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="98ce5-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="98ce5-113">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="98ce5-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="98ce5-114">Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.</span><span class="sxs-lookup"><span data-stu-id="98ce5-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="98ce5-115">Contains</span><span class="sxs-lookup"><span data-stu-id="98ce5-115">Contains</span></span>](#contains) | <span data-ttu-id="98ce5-116">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="98ce5-116">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="98ce5-117">SetHeader</span><span class="sxs-lookup"><span data-stu-id="98ce5-117">SetHeader</span></span>](#setheader) | <span data-ttu-id="98ce5-118">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="98ce5-118">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="98ce5-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="98ce5-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="98ce5-120">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="98ce5-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="98ce5-121">GetIterator</span><span class="sxs-lookup"><span data-stu-id="98ce5-121">GetIterator</span></span>](#getiterator) | <span data-ttu-id="98ce5-122">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="98ce5-122">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="98ce5-123">Utilisé pour inspecter la requête HTTP sur l’événement WebResourceRequested et l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="98ce5-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="98ce5-124">Remarque: vous pouvez modifier les en-têtes de requête HTTP à partir d’un événement WebResourceRequested, mais pas à partir d’un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="98ce5-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="98ce5-125">Ses</span><span class="sxs-lookup"><span data-stu-id="98ce5-125">Members</span></span>

#### <span data-ttu-id="98ce5-126">GetHeader</span><span class="sxs-lookup"><span data-stu-id="98ce5-126">GetHeader</span></span> 

<span data-ttu-id="98ce5-127">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="98ce5-127">Gets the header value matching the name.</span></span>

> <span data-ttu-id="98ce5-128">public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="98ce5-128">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="98ce5-129">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="98ce5-129">GetHeaders</span></span> 

<span data-ttu-id="98ce5-130">Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.</span><span class="sxs-lookup"><span data-stu-id="98ce5-130">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="98ce5-131">public HRESULT [GetHeaders](#getheaders)(nom LPCWSTR,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="98ce5-131">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="98ce5-132">Contains</span><span class="sxs-lookup"><span data-stu-id="98ce5-132">Contains</span></span> 

<span data-ttu-id="98ce5-133">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="98ce5-133">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="98ce5-134">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="98ce5-134">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="98ce5-135">SetHeader</span><span class="sxs-lookup"><span data-stu-id="98ce5-135">SetHeader</span></span> 

<span data-ttu-id="98ce5-136">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="98ce5-136">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="98ce5-137">public HRESULT [setHeader](#setheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="98ce5-137">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="98ce5-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="98ce5-138">RemoveHeader</span></span> 

<span data-ttu-id="98ce5-139">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="98ce5-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="98ce5-140">public HRESULT [RemoveHeader](#removeheader)(nom LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="98ce5-140">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="98ce5-141">GetIterator</span><span class="sxs-lookup"><span data-stu-id="98ce5-141">GetIterator</span></span> 

<span data-ttu-id="98ce5-142">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="98ce5-142">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="98ce5-143">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="98ce5-143">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

