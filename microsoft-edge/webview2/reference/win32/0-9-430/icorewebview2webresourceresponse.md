---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 61f731a948dee970731ba3dbe83426cbb40eb831
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884000"
---
# <span data-ttu-id="357f9-104">0.9.430-interface ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="357f9-104">0.9.430 - interface ICoreWebView2WebResourceResponse</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="357f9-105">Réponse HTTP utilisée avec l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="357f9-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="357f9-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="357f9-106">Summary</span></span>

 <span data-ttu-id="357f9-107">Ses</span><span class="sxs-lookup"><span data-stu-id="357f9-107">Members</span></span>                        | <span data-ttu-id="357f9-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="357f9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="357f9-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="357f9-109">get_Content</span></span>](#get_content) | <span data-ttu-id="357f9-110">Contenu de réponse HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="357f9-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="357f9-111">put_Content</span><span class="sxs-lookup"><span data-stu-id="357f9-111">put_Content</span></span>](#put_content) | <span data-ttu-id="357f9-112">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="357f9-112">Set the Content property.</span></span>
[<span data-ttu-id="357f9-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="357f9-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="357f9-114">En-têtes de réponse HTTP ignorés.</span><span class="sxs-lookup"><span data-stu-id="357f9-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="357f9-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="357f9-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="357f9-116">Code d’état de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="357f9-116">The HTTP response status code.</span></span>
[<span data-ttu-id="357f9-117">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="357f9-117">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="357f9-118">Définissez la propriété StatusCode.</span><span class="sxs-lookup"><span data-stu-id="357f9-118">Set the StatusCode property.</span></span>
[<span data-ttu-id="357f9-119">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="357f9-119">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="357f9-120">Expression de raison de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="357f9-120">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="357f9-121">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="357f9-121">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="357f9-122">Définissez la propriété ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="357f9-122">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="357f9-123">Ses</span><span class="sxs-lookup"><span data-stu-id="357f9-123">Members</span></span>

#### <span data-ttu-id="357f9-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="357f9-124">get_Content</span></span> 

<span data-ttu-id="357f9-125">Contenu de réponse HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="357f9-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="357f9-126">accès public HRESULT [get_Content](#get_content)(IStream \* \* content)</span><span class="sxs-lookup"><span data-stu-id="357f9-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="357f9-127">Le flux doit avoir toutes les données de contenu disponibles lors du report de l’événement WebResourceRequested de la réponse.</span><span class="sxs-lookup"><span data-stu-id="357f9-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="357f9-128">Le flux doit être agile ou être créé à partir d’un thread d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="357f9-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="357f9-129">Null signifie qu’il n’y a pas de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="357f9-129">Null means no content data.</span></span> <span data-ttu-id="357f9-130">La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées)</span><span class="sxs-lookup"><span data-stu-id="357f9-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="357f9-131">put_Content</span><span class="sxs-lookup"><span data-stu-id="357f9-131">put_Content</span></span> 

<span data-ttu-id="357f9-132">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="357f9-132">Set the Content property.</span></span>

> <span data-ttu-id="357f9-133">[put_Content](#put_content)par le biais du contenu public HRESULT</span><span class="sxs-lookup"><span data-stu-id="357f9-133">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="357f9-134">get_Headers</span><span class="sxs-lookup"><span data-stu-id="357f9-134">get_Headers</span></span> 

<span data-ttu-id="357f9-135">En-têtes de réponse HTTP ignorés.</span><span class="sxs-lookup"><span data-stu-id="357f9-135">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="357f9-136">[get_Headersles](#get_headers)HRESULT publiques[(en](ICoreWebView2HttpResponseHeaders.md) -têtes \* \*)</span><span class="sxs-lookup"><span data-stu-id="357f9-136">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="357f9-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="357f9-137">get_StatusCode</span></span> 

<span data-ttu-id="357f9-138">Code d’état de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="357f9-138">The HTTP response status code.</span></span>

> <span data-ttu-id="357f9-139">valeur publique HRESULT [get_StatusCode](#get_statuscode)</span><span class="sxs-lookup"><span data-stu-id="357f9-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="357f9-140">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="357f9-140">put_StatusCode</span></span> 

<span data-ttu-id="357f9-141">Définissez la propriété StatusCode.</span><span class="sxs-lookup"><span data-stu-id="357f9-141">Set the StatusCode property.</span></span>

> <span data-ttu-id="357f9-142">[put_StatusCodes](#put_statuscode)par valeur HRESULT publiques (StatusCode de type ent)</span><span class="sxs-lookup"><span data-stu-id="357f9-142">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="357f9-143">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="357f9-143">get_ReasonPhrase</span></span> 

<span data-ttu-id="357f9-144">Expression de raison de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="357f9-144">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="357f9-145">valeur publique HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="357f9-145">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="357f9-146">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="357f9-146">put_ReasonPhrase</span></span> 

<span data-ttu-id="357f9-147">Définissez la propriété ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="357f9-147">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="357f9-148">[put_ReasonPhrase](#put_reasonphrase)par le biais du public HRESULT (LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="357f9-148">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

