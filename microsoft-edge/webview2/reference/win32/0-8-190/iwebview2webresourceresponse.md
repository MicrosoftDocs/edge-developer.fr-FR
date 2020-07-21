---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 82c94869a84165de4c3b8d09937d6ea5d1f79256
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885687"
---
# <span data-ttu-id="6ad3f-104">0.8.355-interface IWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="6ad3f-104">0.8.355 - interface IWebView2WebResourceResponse</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="6ad3f-105">Réponse HTTP utilisée avec l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="6ad3f-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="6ad3f-106">Summary</span></span>

 <span data-ttu-id="6ad3f-107">Ses</span><span class="sxs-lookup"><span data-stu-id="6ad3f-107">Members</span></span>                        | <span data-ttu-id="6ad3f-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6ad3f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6ad3f-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="6ad3f-109">get_Content</span></span>](#get_content) | <span data-ttu-id="6ad3f-110">Contenu de réponse HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="6ad3f-111">put_Content</span><span class="sxs-lookup"><span data-stu-id="6ad3f-111">put_Content</span></span>](#put_content) | <span data-ttu-id="6ad3f-112">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-112">Set the Content property.</span></span>
[<span data-ttu-id="6ad3f-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="6ad3f-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="6ad3f-114">En-têtes de réponse HTTP ignorés.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="6ad3f-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="6ad3f-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="6ad3f-116">Code d’état de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-116">The HTTP response status code.</span></span>
[<span data-ttu-id="6ad3f-117">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="6ad3f-117">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="6ad3f-118">Définissez la propriété StatusCode.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-118">Set the StatusCode property.</span></span>
[<span data-ttu-id="6ad3f-119">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="6ad3f-119">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="6ad3f-120">Expression de raison de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-120">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="6ad3f-121">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="6ad3f-121">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="6ad3f-122">Définissez la propriété ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-122">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="6ad3f-123">Ses</span><span class="sxs-lookup"><span data-stu-id="6ad3f-123">Members</span></span>

#### <span data-ttu-id="6ad3f-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="6ad3f-124">get_Content</span></span> 

<span data-ttu-id="6ad3f-125">Contenu de réponse HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="6ad3f-126">accès public HRESULT [get_Content](#get_content)(IStream \* \* content)</span><span class="sxs-lookup"><span data-stu-id="6ad3f-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="6ad3f-127">Le flux doit avoir toutes les données de contenu disponibles lors du report de l’événement WebResourceRequested de la réponse.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="6ad3f-128">Le flux doit être agile ou être créé à partir d’un thread d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="6ad3f-129">Null signifie qu’il n’y a pas de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-129">Null means no content data.</span></span> <span data-ttu-id="6ad3f-130">La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées)</span><span class="sxs-lookup"><span data-stu-id="6ad3f-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="6ad3f-131">put_Content</span><span class="sxs-lookup"><span data-stu-id="6ad3f-131">put_Content</span></span> 

<span data-ttu-id="6ad3f-132">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-132">Set the Content property.</span></span>

> <span data-ttu-id="6ad3f-133">[put_Content](#put_content)par le biais du contenu public HRESULT</span><span class="sxs-lookup"><span data-stu-id="6ad3f-133">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="6ad3f-134">get_Headers</span><span class="sxs-lookup"><span data-stu-id="6ad3f-134">get_Headers</span></span> 

<span data-ttu-id="6ad3f-135">En-têtes de réponse HTTP ignorés.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-135">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="6ad3f-136">[get_Headersles](#get_headers)HRESULT publiques[(en](IWebView2HttpResponseHeaders.md) -têtes \* \*)</span><span class="sxs-lookup"><span data-stu-id="6ad3f-136">public HRESULT [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="6ad3f-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="6ad3f-137">get_StatusCode</span></span> 

<span data-ttu-id="6ad3f-138">Code d’état de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-138">The HTTP response status code.</span></span>

> <span data-ttu-id="6ad3f-139">valeur publique HRESULT [get_StatusCode](#get_statuscode)</span><span class="sxs-lookup"><span data-stu-id="6ad3f-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="6ad3f-140">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="6ad3f-140">put_StatusCode</span></span> 

<span data-ttu-id="6ad3f-141">Définissez la propriété StatusCode.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-141">Set the StatusCode property.</span></span>

> <span data-ttu-id="6ad3f-142">[put_StatusCodes](#put_statuscode)par valeur HRESULT publiques (StatusCode de type ent)</span><span class="sxs-lookup"><span data-stu-id="6ad3f-142">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="6ad3f-143">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="6ad3f-143">get_ReasonPhrase</span></span> 

<span data-ttu-id="6ad3f-144">Expression de raison de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-144">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="6ad3f-145">valeur publique HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="6ad3f-145">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="6ad3f-146">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="6ad3f-146">put_ReasonPhrase</span></span> 

<span data-ttu-id="6ad3f-147">Définissez la propriété ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="6ad3f-147">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="6ad3f-148">[put_ReasonPhrase](#put_reasonphrase)par le biais du public HRESULT (LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="6ad3f-148">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

