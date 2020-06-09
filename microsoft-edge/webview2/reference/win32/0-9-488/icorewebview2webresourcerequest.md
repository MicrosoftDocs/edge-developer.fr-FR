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
ms.openlocfilehash: d91b7aeeebc8fd82587ac6c01fddd14e693c2559
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697062"
---
# <span data-ttu-id="eb460-104">interface ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="eb460-104">interface ICoreWebView2WebResourceRequest</span></span> 

> [!NOTE]
> <span data-ttu-id="eb460-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="eb460-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="eb460-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="eb460-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="eb460-107">Une requête HTTP utilisée avec l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="eb460-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="eb460-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="eb460-108">Summary</span></span>

 <span data-ttu-id="eb460-109">Ses</span><span class="sxs-lookup"><span data-stu-id="eb460-109">Members</span></span>                        | <span data-ttu-id="eb460-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="eb460-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eb460-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="eb460-111">get_Content</span></span>](#get_content) | <span data-ttu-id="eb460-112">Le corps du message de requête HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="eb460-112">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="eb460-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="eb460-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="eb460-114">En-têtes de requête HTTP mutables.</span><span class="sxs-lookup"><span data-stu-id="eb460-114">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="eb460-115">get_Method</span><span class="sxs-lookup"><span data-stu-id="eb460-115">get_Method</span></span>](#get_method) | <span data-ttu-id="eb460-116">Méthode de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="eb460-116">The HTTP request method.</span></span>
[<span data-ttu-id="eb460-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="eb460-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="eb460-118">URI de la requête.</span><span class="sxs-lookup"><span data-stu-id="eb460-118">The request URI.</span></span>
[<span data-ttu-id="eb460-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="eb460-119">put_Content</span></span>](#put_content) | <span data-ttu-id="eb460-120">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="eb460-120">Set the Content property.</span></span>
[<span data-ttu-id="eb460-121">put_Method</span><span class="sxs-lookup"><span data-stu-id="eb460-121">put_Method</span></span>](#put_method) | <span data-ttu-id="eb460-122">Définissez la propriété Method.</span><span class="sxs-lookup"><span data-stu-id="eb460-122">Set the Method property.</span></span>
[<span data-ttu-id="eb460-123">put_Uri</span><span class="sxs-lookup"><span data-stu-id="eb460-123">put_Uri</span></span>](#put_uri) | <span data-ttu-id="eb460-124">Définissez la propriété Uri.</span><span class="sxs-lookup"><span data-stu-id="eb460-124">Set the Uri property.</span></span>

## <span data-ttu-id="eb460-125">Ses</span><span class="sxs-lookup"><span data-stu-id="eb460-125">Members</span></span>

#### <span data-ttu-id="eb460-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="eb460-126">get_Content</span></span> 

<span data-ttu-id="eb460-127">Le corps du message de requête HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="eb460-127">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="eb460-128">accès public HRESULT [get_Content](#get_content)(IStream \* \* content)</span><span class="sxs-lookup"><span data-stu-id="eb460-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="eb460-129">Les données publiées seraient là.</span><span class="sxs-lookup"><span data-stu-id="eb460-129">POST data would be here.</span></span> <span data-ttu-id="eb460-130">Si un flux est défini, ce qui remplacera le corps du message, toutes les données de contenu doivent être disponibles lorsque le report de l’événement WebResourceRequested de la réponse est terminé.</span><span class="sxs-lookup"><span data-stu-id="eb460-130">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="eb460-131">Le flux doit être agile ou être créé à partir d’un STA d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eb460-131">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="eb460-132">Null signifie qu’il n’y a pas de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="eb460-132">Null means no content data.</span></span> <span data-ttu-id="eb460-133">La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées)</span><span class="sxs-lookup"><span data-stu-id="eb460-133">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="eb460-134">get_Headers</span><span class="sxs-lookup"><span data-stu-id="eb460-134">get_Headers</span></span> 

<span data-ttu-id="eb460-135">En-têtes de requête HTTP mutables.</span><span class="sxs-lookup"><span data-stu-id="eb460-135">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="eb460-136">[get_Headersles](#get_headers)HRESULT publiques[(en](icorewebview2httprequestheaders.md) -têtes \* \*)</span><span class="sxs-lookup"><span data-stu-id="eb460-136">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="eb460-137">get_Method</span><span class="sxs-lookup"><span data-stu-id="eb460-137">get_Method</span></span> 

<span data-ttu-id="eb460-138">Méthode de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="eb460-138">The HTTP request method.</span></span>

> <span data-ttu-id="eb460-139">valeur publique HRESULT [get_Method](#get_method)(méthode LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="eb460-139">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="eb460-140">get_Uri</span><span class="sxs-lookup"><span data-stu-id="eb460-140">get_Uri</span></span> 

<span data-ttu-id="eb460-141">URI de la requête.</span><span class="sxs-lookup"><span data-stu-id="eb460-141">The request URI.</span></span>

> <span data-ttu-id="eb460-142">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="eb460-142">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="eb460-143">put_Content</span><span class="sxs-lookup"><span data-stu-id="eb460-143">put_Content</span></span> 

<span data-ttu-id="eb460-144">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="eb460-144">Set the Content property.</span></span>

> <span data-ttu-id="eb460-145">[put_Content](#put_content)par le biais du contenu public HRESULT</span><span class="sxs-lookup"><span data-stu-id="eb460-145">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="eb460-146">put_Method</span><span class="sxs-lookup"><span data-stu-id="eb460-146">put_Method</span></span> 

<span data-ttu-id="eb460-147">Définissez la propriété Method.</span><span class="sxs-lookup"><span data-stu-id="eb460-147">Set the Method property.</span></span>

> <span data-ttu-id="eb460-148">[put_Method](#put_method)par le biais du public HRESULT (méthode LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="eb460-148">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="eb460-149">put_Uri</span><span class="sxs-lookup"><span data-stu-id="eb460-149">put_Uri</span></span> 

<span data-ttu-id="eb460-150">Définissez la propriété Uri.</span><span class="sxs-lookup"><span data-stu-id="eb460-150">Set the Uri property.</span></span>

> <span data-ttu-id="eb460-151">[put_Uri](#put_uri)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="eb460-151">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

