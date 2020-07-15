---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: cdea3b4d4643e6f14e546eb9edd27bf1534beadd
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877349"
---
# <span data-ttu-id="b930d-104">0.9.515-interface ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="b930d-104">0.9.515 - interface ICoreWebView2WebResourceRequest</span></span> 

> [!NOTE]
> <span data-ttu-id="b930d-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="b930d-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="b930d-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="b930d-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="b930d-107">Une requête HTTP utilisée avec l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="b930d-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="b930d-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="b930d-108">Summary</span></span>

 <span data-ttu-id="b930d-109">Ses</span><span class="sxs-lookup"><span data-stu-id="b930d-109">Members</span></span>                        | <span data-ttu-id="b930d-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b930d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b930d-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="b930d-111">get_Content</span></span>](#get_content) | <span data-ttu-id="b930d-112">Le corps du message de requête HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="b930d-112">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="b930d-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="b930d-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="b930d-114">En-têtes de requête HTTP mutables.</span><span class="sxs-lookup"><span data-stu-id="b930d-114">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="b930d-115">get_Method</span><span class="sxs-lookup"><span data-stu-id="b930d-115">get_Method</span></span>](#get_method) | <span data-ttu-id="b930d-116">Méthode de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="b930d-116">The HTTP request method.</span></span>
[<span data-ttu-id="b930d-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b930d-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="b930d-118">URI de la requête.</span><span class="sxs-lookup"><span data-stu-id="b930d-118">The request URI.</span></span>
[<span data-ttu-id="b930d-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="b930d-119">put_Content</span></span>](#put_content) | <span data-ttu-id="b930d-120">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="b930d-120">Set the Content property.</span></span>
[<span data-ttu-id="b930d-121">put_Method</span><span class="sxs-lookup"><span data-stu-id="b930d-121">put_Method</span></span>](#put_method) | <span data-ttu-id="b930d-122">Définissez la propriété Method.</span><span class="sxs-lookup"><span data-stu-id="b930d-122">Set the Method property.</span></span>
[<span data-ttu-id="b930d-123">put_Uri</span><span class="sxs-lookup"><span data-stu-id="b930d-123">put_Uri</span></span>](#put_uri) | <span data-ttu-id="b930d-124">Définissez la propriété Uri.</span><span class="sxs-lookup"><span data-stu-id="b930d-124">Set the Uri property.</span></span>

## <span data-ttu-id="b930d-125">Ses</span><span class="sxs-lookup"><span data-stu-id="b930d-125">Members</span></span>

#### <span data-ttu-id="b930d-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="b930d-126">get_Content</span></span> 

<span data-ttu-id="b930d-127">Le corps du message de requête HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="b930d-127">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="b930d-128">accès public HRESULT [get_Content](#get_content)(IStream \* \* content)</span><span class="sxs-lookup"><span data-stu-id="b930d-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="b930d-129">Les données publiées seraient là.</span><span class="sxs-lookup"><span data-stu-id="b930d-129">POST data would be here.</span></span> <span data-ttu-id="b930d-130">Si un flux est défini, ce qui remplacera le corps du message, toutes les données de contenu doivent être disponibles lorsque le report de l’événement WebResourceRequested de la réponse est terminé.</span><span class="sxs-lookup"><span data-stu-id="b930d-130">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="b930d-131">Le flux doit être agile ou être créé à partir d’un STA d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b930d-131">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="b930d-132">Null signifie qu’il n’y a pas de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="b930d-132">Null means no content data.</span></span> <span data-ttu-id="b930d-133">La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées)</span><span class="sxs-lookup"><span data-stu-id="b930d-133">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="b930d-134">get_Headers</span><span class="sxs-lookup"><span data-stu-id="b930d-134">get_Headers</span></span> 

<span data-ttu-id="b930d-135">En-têtes de requête HTTP mutables.</span><span class="sxs-lookup"><span data-stu-id="b930d-135">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="b930d-136">[get_Headersles](#get_headers)HRESULT publiques[(en](icorewebview2httprequestheaders.md) -têtes \* \*)</span><span class="sxs-lookup"><span data-stu-id="b930d-136">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="b930d-137">get_Method</span><span class="sxs-lookup"><span data-stu-id="b930d-137">get_Method</span></span> 

<span data-ttu-id="b930d-138">Méthode de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="b930d-138">The HTTP request method.</span></span>

> <span data-ttu-id="b930d-139">valeur publique HRESULT [get_Method](#get_method)(méthode LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="b930d-139">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="b930d-140">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b930d-140">get_Uri</span></span> 

<span data-ttu-id="b930d-141">URI de la requête.</span><span class="sxs-lookup"><span data-stu-id="b930d-141">The request URI.</span></span>

> <span data-ttu-id="b930d-142">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="b930d-142">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="b930d-143">put_Content</span><span class="sxs-lookup"><span data-stu-id="b930d-143">put_Content</span></span> 

<span data-ttu-id="b930d-144">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="b930d-144">Set the Content property.</span></span>

> <span data-ttu-id="b930d-145">[put_Content](#put_content)par le biais du contenu public HRESULT</span><span class="sxs-lookup"><span data-stu-id="b930d-145">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="b930d-146">put_Method</span><span class="sxs-lookup"><span data-stu-id="b930d-146">put_Method</span></span> 

<span data-ttu-id="b930d-147">Définissez la propriété Method.</span><span class="sxs-lookup"><span data-stu-id="b930d-147">Set the Method property.</span></span>

> <span data-ttu-id="b930d-148">[put_Method](#put_method)par le biais du public HRESULT (méthode LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="b930d-148">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="b930d-149">put_Uri</span><span class="sxs-lookup"><span data-stu-id="b930d-149">put_Uri</span></span> 

<span data-ttu-id="b930d-150">Définissez la propriété Uri.</span><span class="sxs-lookup"><span data-stu-id="b930d-150">Set the Uri property.</span></span>

> <span data-ttu-id="b930d-151">[put_Uri](#put_uri)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="b930d-151">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

