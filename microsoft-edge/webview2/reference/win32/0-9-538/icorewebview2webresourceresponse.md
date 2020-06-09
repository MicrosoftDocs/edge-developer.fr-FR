---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 7072a25636efb638fcb42c593aa6cc77e990965a
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698677"
---
# <span data-ttu-id="0c736-104">interface ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="0c736-104">interface ICoreWebView2WebResourceResponse</span></span> 

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="0c736-105">Réponse HTTP utilisée avec l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="0c736-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="0c736-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="0c736-106">Summary</span></span>

 <span data-ttu-id="0c736-107">Ses</span><span class="sxs-lookup"><span data-stu-id="0c736-107">Members</span></span>                        | <span data-ttu-id="0c736-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0c736-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0c736-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="0c736-109">get_Content</span></span>](#get_content) | <span data-ttu-id="0c736-110">Contenu de réponse HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="0c736-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="0c736-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="0c736-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="0c736-112">En-têtes de réponse HTTP ignorés.</span><span class="sxs-lookup"><span data-stu-id="0c736-112">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="0c736-113">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="0c736-113">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="0c736-114">Expression de raison de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c736-114">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="0c736-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="0c736-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="0c736-116">Code d’état de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c736-116">The HTTP response status code.</span></span>
[<span data-ttu-id="0c736-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="0c736-117">put_Content</span></span>](#put_content) | <span data-ttu-id="0c736-118">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="0c736-118">Set the Content property.</span></span>
[<span data-ttu-id="0c736-119">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="0c736-119">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="0c736-120">Définissez la propriété ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="0c736-120">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="0c736-121">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="0c736-121">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="0c736-122">Définissez la propriété StatusCode.</span><span class="sxs-lookup"><span data-stu-id="0c736-122">Set the StatusCode property.</span></span>

## <span data-ttu-id="0c736-123">Ses</span><span class="sxs-lookup"><span data-stu-id="0c736-123">Members</span></span>

#### <span data-ttu-id="0c736-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="0c736-124">get_Content</span></span> 

<span data-ttu-id="0c736-125">Contenu de réponse HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="0c736-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="0c736-126">accès public HRESULT [get_Content](#get_content)(IStream \* \* content)</span><span class="sxs-lookup"><span data-stu-id="0c736-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="0c736-127">Le flux doit avoir toutes les données de contenu disponibles lors du report de l’événement WebResourceRequested de la réponse.</span><span class="sxs-lookup"><span data-stu-id="0c736-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="0c736-128">Le flux doit être agile ou être créé à partir d’un thread d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0c736-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="0c736-129">Null signifie qu’il n’y a pas de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="0c736-129">Null means no content data.</span></span> <span data-ttu-id="0c736-130">La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées)</span><span class="sxs-lookup"><span data-stu-id="0c736-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="0c736-131">get_Headers</span><span class="sxs-lookup"><span data-stu-id="0c736-131">get_Headers</span></span> 

<span data-ttu-id="0c736-132">En-têtes de réponse HTTP ignorés.</span><span class="sxs-lookup"><span data-stu-id="0c736-132">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="0c736-133">[get_Headersles](#get_headers)HRESULT publiques[(en](icorewebview2httpresponseheaders.md) -têtes \* \*)</span><span class="sxs-lookup"><span data-stu-id="0c736-133">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="0c736-134">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="0c736-134">get_ReasonPhrase</span></span> 

<span data-ttu-id="0c736-135">Expression de raison de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c736-135">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="0c736-136">valeur publique HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="0c736-136">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="0c736-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="0c736-137">get_StatusCode</span></span> 

<span data-ttu-id="0c736-138">Code d’état de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c736-138">The HTTP response status code.</span></span>

> <span data-ttu-id="0c736-139">valeur publique HRESULT [get_StatusCode](#get_statuscode)</span><span class="sxs-lookup"><span data-stu-id="0c736-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="0c736-140">put_Content</span><span class="sxs-lookup"><span data-stu-id="0c736-140">put_Content</span></span> 

<span data-ttu-id="0c736-141">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="0c736-141">Set the Content property.</span></span>

> <span data-ttu-id="0c736-142">[put_Content](#put_content)par le biais du contenu public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0c736-142">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="0c736-143">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="0c736-143">put_ReasonPhrase</span></span> 

<span data-ttu-id="0c736-144">Définissez la propriété ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="0c736-144">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="0c736-145">[put_ReasonPhrase](#put_reasonphrase)par le biais du public HRESULT (LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="0c736-145">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="0c736-146">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="0c736-146">put_StatusCode</span></span> 

<span data-ttu-id="0c736-147">Définissez la propriété StatusCode.</span><span class="sxs-lookup"><span data-stu-id="0c736-147">Set the StatusCode property.</span></span>

> <span data-ttu-id="0c736-148">[put_StatusCodes](#put_statuscode)par valeur HRESULT publiques (StatusCode de type ent)</span><span class="sxs-lookup"><span data-stu-id="0c736-148">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

