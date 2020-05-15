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
ms.openlocfilehash: ad3f4e5e95b0309628644f17e5d647ab6d4af658
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653312"
---
# <span data-ttu-id="11e57-104">interface IWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="11e57-104">interface IWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="11e57-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="11e57-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="11e57-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="11e57-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="11e57-107">Réponse HTTP utilisée avec l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="11e57-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="11e57-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="11e57-108">Summary</span></span>

 <span data-ttu-id="11e57-109">Ses</span><span class="sxs-lookup"><span data-stu-id="11e57-109">Members</span></span>                        | <span data-ttu-id="11e57-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="11e57-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="11e57-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="11e57-111">get_Content</span></span>](#get_content) | <span data-ttu-id="11e57-112">Contenu de réponse HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="11e57-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="11e57-113">put_Content</span><span class="sxs-lookup"><span data-stu-id="11e57-113">put_Content</span></span>](#put_content) | <span data-ttu-id="11e57-114">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="11e57-114">Set the Content property.</span></span>
[<span data-ttu-id="11e57-115">get_Headers</span><span class="sxs-lookup"><span data-stu-id="11e57-115">get_Headers</span></span>](#get_headers) | <span data-ttu-id="11e57-116">En-têtes de réponse HTTP ignorés.</span><span class="sxs-lookup"><span data-stu-id="11e57-116">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="11e57-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="11e57-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="11e57-118">Code d’état de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="11e57-118">The HTTP response status code.</span></span>
[<span data-ttu-id="11e57-119">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="11e57-119">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="11e57-120">Définissez la propriété StatusCode.</span><span class="sxs-lookup"><span data-stu-id="11e57-120">Set the StatusCode property.</span></span>
[<span data-ttu-id="11e57-121">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="11e57-121">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="11e57-122">Expression de raison de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="11e57-122">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="11e57-123">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="11e57-123">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="11e57-124">Définissez la propriété ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="11e57-124">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="11e57-125">Ses</span><span class="sxs-lookup"><span data-stu-id="11e57-125">Members</span></span>

#### <span data-ttu-id="11e57-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="11e57-126">get_Content</span></span> 

<span data-ttu-id="11e57-127">Contenu de réponse HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="11e57-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="11e57-128">accès public HRESULT [get_Content](#get_content)(IStream \* \* content)</span><span class="sxs-lookup"><span data-stu-id="11e57-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="11e57-129">Le flux doit avoir toutes les données de contenu disponibles lors du report de l’événement WebResourceRequested de la réponse.</span><span class="sxs-lookup"><span data-stu-id="11e57-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="11e57-130">Le flux doit être agile ou être créé à partir d’un thread d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="11e57-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="11e57-131">Null signifie qu’il n’y a pas de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="11e57-131">Null means no content data.</span></span> <span data-ttu-id="11e57-132">La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées)</span><span class="sxs-lookup"><span data-stu-id="11e57-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="11e57-133">put_Content</span><span class="sxs-lookup"><span data-stu-id="11e57-133">put_Content</span></span> 

<span data-ttu-id="11e57-134">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="11e57-134">Set the Content property.</span></span>

> <span data-ttu-id="11e57-135">[put_Content](#put_content)par le biais du contenu public HRESULT</span><span class="sxs-lookup"><span data-stu-id="11e57-135">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="11e57-136">get_Headers</span><span class="sxs-lookup"><span data-stu-id="11e57-136">get_Headers</span></span> 

<span data-ttu-id="11e57-137">En-têtes de réponse HTTP ignorés.</span><span class="sxs-lookup"><span data-stu-id="11e57-137">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="11e57-138">[get_Headersles](#get_headers)HRESULT publiques[(en](IWebView2HttpResponseHeaders.md) -têtes \* \*)</span><span class="sxs-lookup"><span data-stu-id="11e57-138">public HRESULT [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="11e57-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="11e57-139">get_StatusCode</span></span> 

<span data-ttu-id="11e57-140">Code d’état de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="11e57-140">The HTTP response status code.</span></span>

> <span data-ttu-id="11e57-141">valeur publique HRESULT [get_StatusCode](#get_statuscode)</span><span class="sxs-lookup"><span data-stu-id="11e57-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="11e57-142">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="11e57-142">put_StatusCode</span></span> 

<span data-ttu-id="11e57-143">Définissez la propriété StatusCode.</span><span class="sxs-lookup"><span data-stu-id="11e57-143">Set the StatusCode property.</span></span>

> <span data-ttu-id="11e57-144">[put_StatusCodes](#put_statuscode)par valeur HRESULT publiques (StatusCode de type ent)</span><span class="sxs-lookup"><span data-stu-id="11e57-144">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="11e57-145">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="11e57-145">get_ReasonPhrase</span></span> 

<span data-ttu-id="11e57-146">Expression de raison de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="11e57-146">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="11e57-147">valeur publique HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="11e57-147">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="11e57-148">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="11e57-148">put_ReasonPhrase</span></span> 

<span data-ttu-id="11e57-149">Définissez la propriété ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="11e57-149">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="11e57-150">[put_ReasonPhrase](#put_reasonphrase)par le biais du public HRESULT (LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="11e57-150">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

