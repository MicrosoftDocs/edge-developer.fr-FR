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
ms.openlocfilehash: aea00f37f28034e1b7a33d4fd11c5ed78f779d00
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653546"
---
# <span data-ttu-id="3b410-104">interface IWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="3b410-104">interface IWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="3b410-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="3b410-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="3b410-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="3b410-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="3b410-107">En-têtes de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="3b410-107">HTTP request headers.</span></span>

## <span data-ttu-id="3b410-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="3b410-108">Summary</span></span>

 <span data-ttu-id="3b410-109">Ses</span><span class="sxs-lookup"><span data-stu-id="3b410-109">Members</span></span>                        | <span data-ttu-id="3b410-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3b410-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3b410-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="3b410-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="3b410-112">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="3b410-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="3b410-113">Contains</span><span class="sxs-lookup"><span data-stu-id="3b410-113">Contains</span></span>](#contains) | <span data-ttu-id="3b410-114">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="3b410-114">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="3b410-115">SetHeader</span><span class="sxs-lookup"><span data-stu-id="3b410-115">SetHeader</span></span>](#setheader) | <span data-ttu-id="3b410-116">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="3b410-116">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="3b410-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="3b410-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="3b410-118">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="3b410-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="3b410-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="3b410-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="3b410-120">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="3b410-120">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="3b410-121">Utilisé pour inspecter la requête HTTP sur l’événement WebResourceRequested et l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="3b410-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="3b410-122">Remarque: vous pouvez modifier les en-têtes de requête HTTP à partir d’un événement WebResourceRequested, mais pas à partir d’un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="3b410-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="3b410-123">Ses</span><span class="sxs-lookup"><span data-stu-id="3b410-123">Members</span></span>

#### <span data-ttu-id="3b410-124">GetHeader</span><span class="sxs-lookup"><span data-stu-id="3b410-124">GetHeader</span></span> 

<span data-ttu-id="3b410-125">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="3b410-125">Gets the header value matching the name.</span></span>

> <span data-ttu-id="3b410-126">public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="3b410-126">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="3b410-127">Contains</span><span class="sxs-lookup"><span data-stu-id="3b410-127">Contains</span></span> 

<span data-ttu-id="3b410-128">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="3b410-128">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="3b410-129">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="3b410-129">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="3b410-130">SetHeader</span><span class="sxs-lookup"><span data-stu-id="3b410-130">SetHeader</span></span> 

<span data-ttu-id="3b410-131">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="3b410-131">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="3b410-132">public HRESULT [setHeader](#setheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="3b410-132">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="3b410-133">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="3b410-133">RemoveHeader</span></span> 

<span data-ttu-id="3b410-134">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="3b410-134">Removes header that matches the name.</span></span>

> <span data-ttu-id="3b410-135">public HRESULT [RemoveHeader](#removeheader)(nom LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="3b410-135">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="3b410-136">GetIterator</span><span class="sxs-lookup"><span data-stu-id="3b410-136">GetIterator</span></span> 

<span data-ttu-id="3b410-137">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="3b410-137">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="3b410-138">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="3b410-138">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

