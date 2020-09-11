---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator
ms.openlocfilehash: e7aad408372acbbd19ecab9d04312f21e2396e88
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011897"
---
# <span data-ttu-id="031c6-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="031c6-104">Microsoft.Web.WebView2.Core.CoreWebView2HttpHeadersCollectionIterator class</span></span> 

<span data-ttu-id="031c6-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="031c6-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="031c6-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="031c6-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="031c6-107">Itérateur pour une collection d’en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="031c6-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="031c6-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="031c6-108">Summary</span></span>

 <span data-ttu-id="031c6-109">Ses</span><span class="sxs-lookup"><span data-stu-id="031c6-109">Members</span></span>                        | <span data-ttu-id="031c6-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="031c6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="031c6-111">HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="031c6-111">HasCurrentHeader</span></span>](#hascurrentheader) | <span data-ttu-id="031c6-112">True lorsque l’itérateur n’a plus d’en-têtes.</span><span class="sxs-lookup"><span data-stu-id="031c6-112">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="031c6-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="031c6-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="031c6-114">Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.</span><span class="sxs-lookup"><span data-stu-id="031c6-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="031c6-115">Voir CoreWebView2HttpRequestHeaders et CoreWebView2HttpResponseHeaders.</span><span class="sxs-lookup"><span data-stu-id="031c6-115">See CoreWebView2HttpRequestHeaders and CoreWebView2HttpResponseHeaders.</span></span>

## <span data-ttu-id="031c6-116">Ses</span><span class="sxs-lookup"><span data-stu-id="031c6-116">Members</span></span>

#### <span data-ttu-id="031c6-117">HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="031c6-117">HasCurrentHeader</span></span> 

<span data-ttu-id="031c6-118">True lorsque l’itérateur n’a plus d’en-têtes.</span><span class="sxs-lookup"><span data-stu-id="031c6-118">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="031c6-119">public bool [HasCurrentHeader](#hascurrentheader)</span><span class="sxs-lookup"><span data-stu-id="031c6-119">public bool [HasCurrentHeader](#hascurrentheader)</span></span>

<span data-ttu-id="031c6-120">Si la collection sur laquelle l’itérateur est une itération est vide ou si l’itérateur a dépassé la fin de la collection, il s’agit de la valeur false.</span><span class="sxs-lookup"><span data-stu-id="031c6-120">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="031c6-121">MoveNext</span><span class="sxs-lookup"><span data-stu-id="031c6-121">MoveNext</span></span> 

<span data-ttu-id="031c6-122">Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.</span><span class="sxs-lookup"><span data-stu-id="031c6-122">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="031c6-123">public bool [MoveNext](#movenext)()</span><span class="sxs-lookup"><span data-stu-id="031c6-123">public bool [MoveNext](#movenext)()</span></span>

<span data-ttu-id="031c6-124">Le paramètre hasNext est défini sur FALSe s’il n’y a plus d’en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="031c6-124">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="031c6-125">Après cela, la méthode GetCurrentHeader échoue si elle est appelée.</span><span class="sxs-lookup"><span data-stu-id="031c6-125">After this occurs the GetCurrentHeader method will fail if called.</span></span>

