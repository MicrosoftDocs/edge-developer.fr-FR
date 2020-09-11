---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
ms.openlocfilehash: 5359634d83717ce844d2c1604a2645ceffc477cc
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011847"
---
# <span data-ttu-id="fe7d2-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="fe7d2-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponse class</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="fe7d2-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="fe7d2-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="fe7d2-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="fe7d2-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="fe7d2-107">Réponse HTTP utilisée avec l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="fe7d2-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="fe7d2-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="fe7d2-108">Summary</span></span>

 <span data-ttu-id="fe7d2-109">Ses</span><span class="sxs-lookup"><span data-stu-id="fe7d2-109">Members</span></span>                        | <span data-ttu-id="fe7d2-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="fe7d2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fe7d2-111">Contenu</span><span class="sxs-lookup"><span data-stu-id="fe7d2-111">Content</span></span>](#content) | <span data-ttu-id="fe7d2-112">Contenu de réponse HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="fe7d2-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="fe7d2-113">En-têtes</span><span class="sxs-lookup"><span data-stu-id="fe7d2-113">Headers</span></span>](#headers) | <span data-ttu-id="fe7d2-114">En-têtes de réponse HTTP ignorés.</span><span class="sxs-lookup"><span data-stu-id="fe7d2-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="fe7d2-115">ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="fe7d2-115">ReasonPhrase</span></span>](#reasonphrase) | <span data-ttu-id="fe7d2-116">Expression de raison de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="fe7d2-116">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="fe7d2-117">StatusCode</span><span class="sxs-lookup"><span data-stu-id="fe7d2-117">StatusCode</span></span>](#statuscode) | <span data-ttu-id="fe7d2-118">Code d’état de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="fe7d2-118">The HTTP response status code.</span></span>

## <span data-ttu-id="fe7d2-119">Ses</span><span class="sxs-lookup"><span data-stu-id="fe7d2-119">Members</span></span>

#### <span data-ttu-id="fe7d2-120">Contenu</span><span class="sxs-lookup"><span data-stu-id="fe7d2-120">Content</span></span> 

<span data-ttu-id="fe7d2-121">Contenu de réponse HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="fe7d2-121">HTTP response content as stream.</span></span>

> <span data-ttu-id="fe7d2-122">[contenu](#content) de flux public</span><span class="sxs-lookup"><span data-stu-id="fe7d2-122">public Stream [Content](#content)</span></span>

<span data-ttu-id="fe7d2-123">Le flux doit avoir toutes les données de contenu disponibles lors du report de l’événement WebResourceRequested de la réponse.</span><span class="sxs-lookup"><span data-stu-id="fe7d2-123">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="fe7d2-124">Le flux doit être agile ou être créé à partir d’un thread d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fe7d2-124">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="fe7d2-125">Null signifie qu’il n’y a pas de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="fe7d2-125">Null means no content data.</span></span> <span data-ttu-id="fe7d2-126">La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées).</span><span class="sxs-lookup"><span data-stu-id="fe7d2-126">IStream semantics apply (return S_OK to Read calls until all data is exhausted).</span></span>

#### <span data-ttu-id="fe7d2-127">En-têtes</span><span class="sxs-lookup"><span data-stu-id="fe7d2-127">Headers</span></span> 

<span data-ttu-id="fe7d2-128">En-têtes de réponse HTTP ignorés.</span><span class="sxs-lookup"><span data-stu-id="fe7d2-128">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="fe7d2-129">[en-têtes](#headers) [CoreWebView2HttpResponseHeaders](microsoft-web-webview2-core-corewebview2httpresponseheaders.md) publics</span><span class="sxs-lookup"><span data-stu-id="fe7d2-129">public [CoreWebView2HttpResponseHeaders](microsoft-web-webview2-core-corewebview2httpresponseheaders.md) [Headers](#headers)</span></span>

#### <span data-ttu-id="fe7d2-130">ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="fe7d2-130">ReasonPhrase</span></span> 

<span data-ttu-id="fe7d2-131">Expression de raison de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="fe7d2-131">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="fe7d2-132">[ReasonPhrase](#reasonphrase) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="fe7d2-132">public string [ReasonPhrase](#reasonphrase)</span></span>

#### <span data-ttu-id="fe7d2-133">StatusCode</span><span class="sxs-lookup"><span data-stu-id="fe7d2-133">StatusCode</span></span> 

<span data-ttu-id="fe7d2-134">Code d’état de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="fe7d2-134">The HTTP response status code.</span></span>

> <span data-ttu-id="fe7d2-135">[statusCode](#statuscode) ent public</span><span class="sxs-lookup"><span data-stu-id="fe7d2-135">public int [StatusCode](#statuscode)</span></span>

