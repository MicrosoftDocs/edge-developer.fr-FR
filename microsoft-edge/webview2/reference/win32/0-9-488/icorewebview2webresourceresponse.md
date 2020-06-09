---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 5b80691f0e42be4cdea7c99b165bfe9cebf632dd
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697930"
---
# <span data-ttu-id="cf76b-104">interface ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="cf76b-104">interface ICoreWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="cf76b-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="cf76b-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="cf76b-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="cf76b-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="cf76b-107">Réponse HTTP utilisée avec l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="cf76b-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="cf76b-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="cf76b-108">Summary</span></span>

 <span data-ttu-id="cf76b-109">Ses</span><span class="sxs-lookup"><span data-stu-id="cf76b-109">Members</span></span>                        | <span data-ttu-id="cf76b-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="cf76b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cf76b-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="cf76b-111">get_Content</span></span>](#get_content) | <span data-ttu-id="cf76b-112">Contenu de réponse HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="cf76b-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="cf76b-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="cf76b-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="cf76b-114">En-têtes de réponse HTTP ignorés.</span><span class="sxs-lookup"><span data-stu-id="cf76b-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="cf76b-115">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="cf76b-115">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="cf76b-116">Expression de raison de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="cf76b-116">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="cf76b-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="cf76b-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="cf76b-118">Code d’état de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="cf76b-118">The HTTP response status code.</span></span>
[<span data-ttu-id="cf76b-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="cf76b-119">put_Content</span></span>](#put_content) | <span data-ttu-id="cf76b-120">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="cf76b-120">Set the Content property.</span></span>
[<span data-ttu-id="cf76b-121">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="cf76b-121">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="cf76b-122">Définissez la propriété ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="cf76b-122">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="cf76b-123">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="cf76b-123">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="cf76b-124">Définissez la propriété StatusCode.</span><span class="sxs-lookup"><span data-stu-id="cf76b-124">Set the StatusCode property.</span></span>

## <span data-ttu-id="cf76b-125">Ses</span><span class="sxs-lookup"><span data-stu-id="cf76b-125">Members</span></span>

#### <span data-ttu-id="cf76b-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="cf76b-126">get_Content</span></span> 

<span data-ttu-id="cf76b-127">Contenu de réponse HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="cf76b-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="cf76b-128">accès public HRESULT [get_Content](#get_content)(IStream \* \* content)</span><span class="sxs-lookup"><span data-stu-id="cf76b-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="cf76b-129">Le flux doit avoir toutes les données de contenu disponibles lors du report de l’événement WebResourceRequested de la réponse.</span><span class="sxs-lookup"><span data-stu-id="cf76b-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="cf76b-130">Le flux doit être agile ou être créé à partir d’un thread d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf76b-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="cf76b-131">Null signifie qu’il n’y a pas de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="cf76b-131">Null means no content data.</span></span> <span data-ttu-id="cf76b-132">La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées)</span><span class="sxs-lookup"><span data-stu-id="cf76b-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="cf76b-133">get_Headers</span><span class="sxs-lookup"><span data-stu-id="cf76b-133">get_Headers</span></span> 

<span data-ttu-id="cf76b-134">En-têtes de réponse HTTP ignorés.</span><span class="sxs-lookup"><span data-stu-id="cf76b-134">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="cf76b-135">[get_Headersles](#get_headers)HRESULT publiques[(en](icorewebview2httpresponseheaders.md) -têtes \* \*)</span><span class="sxs-lookup"><span data-stu-id="cf76b-135">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="cf76b-136">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="cf76b-136">get_ReasonPhrase</span></span> 

<span data-ttu-id="cf76b-137">Expression de raison de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="cf76b-137">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="cf76b-138">valeur publique HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="cf76b-138">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="cf76b-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="cf76b-139">get_StatusCode</span></span> 

<span data-ttu-id="cf76b-140">Code d’état de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="cf76b-140">The HTTP response status code.</span></span>

> <span data-ttu-id="cf76b-141">valeur publique HRESULT [get_StatusCode](#get_statuscode)</span><span class="sxs-lookup"><span data-stu-id="cf76b-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="cf76b-142">put_Content</span><span class="sxs-lookup"><span data-stu-id="cf76b-142">put_Content</span></span> 

<span data-ttu-id="cf76b-143">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="cf76b-143">Set the Content property.</span></span>

> <span data-ttu-id="cf76b-144">[put_Content](#put_content)par le biais du contenu public HRESULT</span><span class="sxs-lookup"><span data-stu-id="cf76b-144">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="cf76b-145">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="cf76b-145">put_ReasonPhrase</span></span> 

<span data-ttu-id="cf76b-146">Définissez la propriété ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="cf76b-146">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="cf76b-147">[put_ReasonPhrase](#put_reasonphrase)par le biais du public HRESULT (LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="cf76b-147">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="cf76b-148">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="cf76b-148">put_StatusCode</span></span> 

<span data-ttu-id="cf76b-149">Définissez la propriété StatusCode.</span><span class="sxs-lookup"><span data-stu-id="cf76b-149">Set the StatusCode property.</span></span>

> <span data-ttu-id="cf76b-150">[put_StatusCodes](#put_statuscode)par valeur HRESULT publiques (StatusCode de type ent)</span><span class="sxs-lookup"><span data-stu-id="cf76b-150">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

