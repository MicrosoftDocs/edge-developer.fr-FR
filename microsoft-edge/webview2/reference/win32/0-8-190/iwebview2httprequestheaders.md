---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 1e0148c0d1e27cb4f1c52fb6ad55cc2e7613a94b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885967"
---
# <span data-ttu-id="9d508-104">0.8.355-interface IWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="9d508-104">0.8.355 - interface IWebView2HttpRequestHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="9d508-105">En-têtes de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="9d508-105">HTTP request headers.</span></span>

## <span data-ttu-id="9d508-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="9d508-106">Summary</span></span>

 <span data-ttu-id="9d508-107">Ses</span><span class="sxs-lookup"><span data-stu-id="9d508-107">Members</span></span>                        | <span data-ttu-id="9d508-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="9d508-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9d508-109">GetHeader</span><span class="sxs-lookup"><span data-stu-id="9d508-109">GetHeader</span></span>](#getheader) | <span data-ttu-id="9d508-110">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="9d508-110">Gets the header value matching the name.</span></span>
[<span data-ttu-id="9d508-111">Contains</span><span class="sxs-lookup"><span data-stu-id="9d508-111">Contains</span></span>](#contains) | <span data-ttu-id="9d508-112">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="9d508-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="9d508-113">SetHeader</span><span class="sxs-lookup"><span data-stu-id="9d508-113">SetHeader</span></span>](#setheader) | <span data-ttu-id="9d508-114">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="9d508-114">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="9d508-115">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="9d508-115">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="9d508-116">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="9d508-116">Removes header that matches the name.</span></span>
[<span data-ttu-id="9d508-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="9d508-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="9d508-118">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="9d508-118">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="9d508-119">Utilisé pour inspecter la requête HTTP sur l’événement WebResourceRequested et l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9d508-119">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="9d508-120">Remarque: vous pouvez modifier les en-têtes de requête HTTP à partir d’un événement WebResourceRequested, mais pas à partir d’un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9d508-120">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="9d508-121">Ses</span><span class="sxs-lookup"><span data-stu-id="9d508-121">Members</span></span>

#### <span data-ttu-id="9d508-122">GetHeader</span><span class="sxs-lookup"><span data-stu-id="9d508-122">GetHeader</span></span> 

<span data-ttu-id="9d508-123">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="9d508-123">Gets the header value matching the name.</span></span>

> <span data-ttu-id="9d508-124">public HRESULT [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="9d508-124">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="9d508-125">Contains</span><span class="sxs-lookup"><span data-stu-id="9d508-125">Contains</span></span> 

<span data-ttu-id="9d508-126">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="9d508-126">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="9d508-127">le HRESULT public [contient](#contains)(nom LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="9d508-127">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="9d508-128">SetHeader</span><span class="sxs-lookup"><span data-stu-id="9d508-128">SetHeader</span></span> 

<span data-ttu-id="9d508-129">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="9d508-129">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="9d508-130">public HRESULT [setHeader](#setheader)(LPCWSTR Name, LPCWSTR value)</span><span class="sxs-lookup"><span data-stu-id="9d508-130">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="9d508-131">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="9d508-131">RemoveHeader</span></span> 

<span data-ttu-id="9d508-132">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="9d508-132">Removes header that matches the name.</span></span>

> <span data-ttu-id="9d508-133">public HRESULT [RemoveHeader](#removeheader)(nom LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="9d508-133">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="9d508-134">GetIterator</span><span class="sxs-lookup"><span data-stu-id="9d508-134">GetIterator</span></span> 

<span data-ttu-id="9d508-135">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="9d508-135">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="9d508-136">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* itérateur)</span><span class="sxs-lookup"><span data-stu-id="9d508-136">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

