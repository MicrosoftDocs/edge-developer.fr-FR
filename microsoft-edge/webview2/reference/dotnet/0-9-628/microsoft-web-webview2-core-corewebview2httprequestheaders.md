---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
ms.openlocfilehash: 1441d5a45caf4e8f561de2487438b66e067760f6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011830"
---
# <span data-ttu-id="8bc1a-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="8bc1a-104">Microsoft.Web.WebView2.Core.CoreWebView2HttpRequestHeaders class</span></span> 

<span data-ttu-id="8bc1a-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="8bc1a-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="8bc1a-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="8bc1a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="8bc1a-107">En-têtes de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="8bc1a-107">HTTP request headers.</span></span>

## <span data-ttu-id="8bc1a-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="8bc1a-108">Summary</span></span>

 <span data-ttu-id="8bc1a-109">Ses</span><span class="sxs-lookup"><span data-stu-id="8bc1a-109">Members</span></span>                        | <span data-ttu-id="8bc1a-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="8bc1a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8bc1a-111">Contains</span><span class="sxs-lookup"><span data-stu-id="8bc1a-111">Contains</span></span>](#contains) | <span data-ttu-id="8bc1a-112">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="8bc1a-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="8bc1a-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="8bc1a-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="8bc1a-114">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="8bc1a-114">Gets the header value matching the name.</span></span>
[<span data-ttu-id="8bc1a-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="8bc1a-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="8bc1a-116">Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.</span><span class="sxs-lookup"><span data-stu-id="8bc1a-116">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="8bc1a-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="8bc1a-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="8bc1a-118">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="8bc1a-118">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="8bc1a-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="8bc1a-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="8bc1a-120">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="8bc1a-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="8bc1a-121">SetHeader</span><span class="sxs-lookup"><span data-stu-id="8bc1a-121">SetHeader</span></span>](#setheader) | <span data-ttu-id="8bc1a-122">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="8bc1a-122">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="8bc1a-123">Utilisé pour inspecter la requête HTTP sur l’événement WebResourceRequested et l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="8bc1a-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="8bc1a-124">Remarque: vous pouvez modifier les en-têtes de requête HTTP à partir d’un événement WebResourceRequested, mais pas à partir d’un événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="8bc1a-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="8bc1a-125">Ses</span><span class="sxs-lookup"><span data-stu-id="8bc1a-125">Members</span></span>

#### <span data-ttu-id="8bc1a-126">Contains</span><span class="sxs-lookup"><span data-stu-id="8bc1a-126">Contains</span></span> 

<span data-ttu-id="8bc1a-127">Vérifie si les en-têtes contiennent une entrée qui correspond au nom de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="8bc1a-127">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="8bc1a-128">public bool [Contains](#contains)(String name)</span><span class="sxs-lookup"><span data-stu-id="8bc1a-128">public bool [Contains](#contains)(string name)</span></span>

#### <span data-ttu-id="8bc1a-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="8bc1a-129">GetHeader</span></span> 

<span data-ttu-id="8bc1a-130">Obtient la valeur d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="8bc1a-130">Gets the header value matching the name.</span></span>

> <span data-ttu-id="8bc1a-131">chaîne publique [GetHeader](#getheader)(nom de chaîne)</span><span class="sxs-lookup"><span data-stu-id="8bc1a-131">public string [GetHeader](#getheader)(string name)</span></span>

#### <span data-ttu-id="8bc1a-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="8bc1a-132">GetHeaders</span></span> 

<span data-ttu-id="8bc1a-133">Obtient la valeur d’en-tête correspondant au nom par le biais d’un itérateur.</span><span class="sxs-lookup"><span data-stu-id="8bc1a-133">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="8bc1a-134">public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(String name)</span><span class="sxs-lookup"><span data-stu-id="8bc1a-134">public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(string name)</span></span>

#### <span data-ttu-id="8bc1a-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="8bc1a-135">GetIterator</span></span> 

<span data-ttu-id="8bc1a-136">Obtient un itérateur sur la collection d’en-têtes de requête.</span><span class="sxs-lookup"><span data-stu-id="8bc1a-136">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="8bc1a-137">public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()</span><span class="sxs-lookup"><span data-stu-id="8bc1a-137">public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()</span></span>

#### <span data-ttu-id="8bc1a-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="8bc1a-138">RemoveHeader</span></span> 

<span data-ttu-id="8bc1a-139">Supprime l’en-tête qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="8bc1a-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="8bc1a-140">public void [RemoveHeader](#removeheader)(String name)</span><span class="sxs-lookup"><span data-stu-id="8bc1a-140">public void [RemoveHeader](#removeheader)(string name)</span></span>

#### <span data-ttu-id="8bc1a-141">SetHeader</span><span class="sxs-lookup"><span data-stu-id="8bc1a-141">SetHeader</span></span> 

<span data-ttu-id="8bc1a-142">Permet d’ajouter ou de mettre à jour l’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="8bc1a-142">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="8bc1a-143">public void [setHeader](#setheader)(nom de chaîne, valeur chaîne)</span><span class="sxs-lookup"><span data-stu-id="8bc1a-143">public void [SetHeader](#setheader)(string name, string value)</span></span>

