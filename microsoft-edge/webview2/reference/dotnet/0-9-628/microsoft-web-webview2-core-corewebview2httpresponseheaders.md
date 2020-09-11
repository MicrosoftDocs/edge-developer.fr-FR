---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders
ms.openlocfilehash: 51218283460975421859c65da8a43553767ad216
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011894"
---
# <span data-ttu-id="102d3-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="102d3-104">Microsoft.Web.WebView2.Core.CoreWebView2HttpResponseHeaders class</span></span> 

<span data-ttu-id="102d3-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="102d3-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="102d3-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="102d3-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="102d3-107">En-têtes de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="102d3-107">HTTP response headers.</span></span>

## <span data-ttu-id="102d3-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="102d3-108">Summary</span></span>

 <span data-ttu-id="102d3-109">Ses</span><span class="sxs-lookup"><span data-stu-id="102d3-109">Members</span></span>                        | <span data-ttu-id="102d3-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="102d3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="102d3-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="102d3-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="102d3-112">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="102d3-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="102d3-113">Contains</span><span class="sxs-lookup"><span data-stu-id="102d3-113">Contains</span></span>](#contains) | <span data-ttu-id="102d3-114">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="102d3-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="102d3-115">GetHeader</span><span class="sxs-lookup"><span data-stu-id="102d3-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="102d3-116">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="102d3-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="102d3-117">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="102d3-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="102d3-118">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="102d3-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="102d3-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="102d3-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="102d3-120">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="102d3-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="102d3-121">Utilisé pour construire un WebResourceResponse pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="102d3-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="102d3-122">Ses</span><span class="sxs-lookup"><span data-stu-id="102d3-122">Members</span></span>

#### <span data-ttu-id="102d3-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="102d3-123">AppendHeader</span></span> 

<span data-ttu-id="102d3-124">Ajoute la ligne d’en-tête avec le nom et la valeur.</span><span class="sxs-lookup"><span data-stu-id="102d3-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="102d3-125">public void [AppendHeader](#appendheader)(nom de chaîne, valeur chaîne)</span><span class="sxs-lookup"><span data-stu-id="102d3-125">public void [AppendHeader](#appendheader)(string name, string value)</span></span>

#### <span data-ttu-id="102d3-126">Contains</span><span class="sxs-lookup"><span data-stu-id="102d3-126">Contains</span></span> 

<span data-ttu-id="102d3-127">Vérifie si les en-têtes contiennent des entrées correspondant au nom d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="102d3-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="102d3-128">public bool [Contains](#contains)(String name)</span><span class="sxs-lookup"><span data-stu-id="102d3-128">public bool [Contains](#contains)(string name)</span></span>

#### <span data-ttu-id="102d3-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="102d3-129">GetHeader</span></span> 

<span data-ttu-id="102d3-130">Obtient la première valeur d’en-tête dans la collection qui correspond au nom.</span><span class="sxs-lookup"><span data-stu-id="102d3-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="102d3-131">chaîne publique [GetHeader](#getheader)(nom de chaîne)</span><span class="sxs-lookup"><span data-stu-id="102d3-131">public string [GetHeader](#getheader)(string name)</span></span>

#### <span data-ttu-id="102d3-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="102d3-132">GetHeaders</span></span> 

<span data-ttu-id="102d3-133">Obtient les valeurs d’en-tête correspondant au nom.</span><span class="sxs-lookup"><span data-stu-id="102d3-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="102d3-134">public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(String name)</span><span class="sxs-lookup"><span data-stu-id="102d3-134">public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(string name)</span></span>

#### <span data-ttu-id="102d3-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="102d3-135">GetIterator</span></span> 

<span data-ttu-id="102d3-136">Obtient un itérateur sur la collection d’en-têtes de réponse entières.</span><span class="sxs-lookup"><span data-stu-id="102d3-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="102d3-137">public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()</span><span class="sxs-lookup"><span data-stu-id="102d3-137">public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()</span></span>

