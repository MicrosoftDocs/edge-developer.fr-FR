---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest
ms.openlocfilehash: 5c8d164b24995cc31070232dd9b1a2d88fc16cec
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011851"
---
# <span data-ttu-id="cdd74-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="cdd74-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequest class</span></span> 

<span data-ttu-id="cdd74-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="cdd74-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="cdd74-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="cdd74-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="cdd74-107">Une requête HTTP utilisée avec l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="cdd74-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="cdd74-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="cdd74-108">Summary</span></span>

 <span data-ttu-id="cdd74-109">Ses</span><span class="sxs-lookup"><span data-stu-id="cdd74-109">Members</span></span>                        | <span data-ttu-id="cdd74-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="cdd74-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cdd74-111">Contenu</span><span class="sxs-lookup"><span data-stu-id="cdd74-111">Content</span></span>](#content) | <span data-ttu-id="cdd74-112">Le corps du message de requête HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="cdd74-112">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="cdd74-113">En-têtes</span><span class="sxs-lookup"><span data-stu-id="cdd74-113">Headers</span></span>](#headers) | <span data-ttu-id="cdd74-114">En-têtes de requête HTTP mutables.</span><span class="sxs-lookup"><span data-stu-id="cdd74-114">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="cdd74-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="cdd74-115">Method</span></span>](#method) | <span data-ttu-id="cdd74-116">Méthode de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="cdd74-116">The HTTP request method.</span></span>
[<span data-ttu-id="cdd74-117">URI</span><span class="sxs-lookup"><span data-stu-id="cdd74-117">Uri</span></span>](#uri) | <span data-ttu-id="cdd74-118">URI de la requête.</span><span class="sxs-lookup"><span data-stu-id="cdd74-118">The request URI.</span></span>

## <span data-ttu-id="cdd74-119">Ses</span><span class="sxs-lookup"><span data-stu-id="cdd74-119">Members</span></span>

#### <span data-ttu-id="cdd74-120">Contenu</span><span class="sxs-lookup"><span data-stu-id="cdd74-120">Content</span></span> 

<span data-ttu-id="cdd74-121">Le corps du message de requête HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="cdd74-121">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="cdd74-122">[contenu](#content) de flux public</span><span class="sxs-lookup"><span data-stu-id="cdd74-122">public Stream [Content](#content)</span></span>

<span data-ttu-id="cdd74-123">Les données publiées seraient là.</span><span class="sxs-lookup"><span data-stu-id="cdd74-123">POST data would be here.</span></span> <span data-ttu-id="cdd74-124">Si un flux est défini, ce qui remplacera le corps du message, toutes les données de contenu doivent être disponibles lorsque le report de l’événement WebResourceRequested de la réponse est terminé.</span><span class="sxs-lookup"><span data-stu-id="cdd74-124">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="cdd74-125">Le flux doit être agile ou être créé à partir d’un STA d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cdd74-125">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="cdd74-126">Null signifie qu’il n’y a pas de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="cdd74-126">Null means no content data.</span></span> <span data-ttu-id="cdd74-127">La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées).</span><span class="sxs-lookup"><span data-stu-id="cdd74-127">IStream semantics apply (return S_OK to Read calls until all data is exhausted).</span></span>

#### <span data-ttu-id="cdd74-128">En-têtes</span><span class="sxs-lookup"><span data-stu-id="cdd74-128">Headers</span></span> 

<span data-ttu-id="cdd74-129">En-têtes de requête HTTP mutables.</span><span class="sxs-lookup"><span data-stu-id="cdd74-129">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="cdd74-130">[en-têtes](#headers) [CoreWebView2HttpRequestHeaders](microsoft-web-webview2-core-corewebview2httprequestheaders.md) publics</span><span class="sxs-lookup"><span data-stu-id="cdd74-130">public [CoreWebView2HttpRequestHeaders](microsoft-web-webview2-core-corewebview2httprequestheaders.md) [Headers](#headers)</span></span>

#### <span data-ttu-id="cdd74-131">Méthode</span><span class="sxs-lookup"><span data-stu-id="cdd74-131">Method</span></span> 

<span data-ttu-id="cdd74-132">Méthode de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="cdd74-132">The HTTP request method.</span></span>

> <span data-ttu-id="cdd74-133">[méthode](#method) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="cdd74-133">public string [Method](#method)</span></span>

#### <span data-ttu-id="cdd74-134">URI</span><span class="sxs-lookup"><span data-stu-id="cdd74-134">Uri</span></span> 

<span data-ttu-id="cdd74-135">URI de la requête.</span><span class="sxs-lookup"><span data-stu-id="cdd74-135">The request URI.</span></span>

> <span data-ttu-id="cdd74-136">[URI](#uri) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="cdd74-136">public string [Uri](#uri)</span></span>

