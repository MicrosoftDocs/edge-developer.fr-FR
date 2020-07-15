---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: a2ac747a9981b3d44e8dbddd390bbb9b72690105
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880135"
---
# <span data-ttu-id="46d75-104">0.9.430-interface ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="46d75-104">0.9.430 - interface ICoreWebView2WebResourceRequest</span></span> 

> [!NOTE]
> <span data-ttu-id="46d75-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="46d75-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="46d75-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="46d75-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="46d75-107">Une requête HTTP utilisée avec l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="46d75-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="46d75-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="46d75-108">Summary</span></span>

 <span data-ttu-id="46d75-109">Ses</span><span class="sxs-lookup"><span data-stu-id="46d75-109">Members</span></span>                        | <span data-ttu-id="46d75-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="46d75-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="46d75-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="46d75-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="46d75-112">URI de la requête.</span><span class="sxs-lookup"><span data-stu-id="46d75-112">The request URI.</span></span>
[<span data-ttu-id="46d75-113">put_Uri</span><span class="sxs-lookup"><span data-stu-id="46d75-113">put_Uri</span></span>](#put_uri) | <span data-ttu-id="46d75-114">Définissez la propriété Uri.</span><span class="sxs-lookup"><span data-stu-id="46d75-114">Set the Uri property.</span></span>
[<span data-ttu-id="46d75-115">get_Method</span><span class="sxs-lookup"><span data-stu-id="46d75-115">get_Method</span></span>](#get_method) | <span data-ttu-id="46d75-116">Méthode de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="46d75-116">The HTTP request method.</span></span>
[<span data-ttu-id="46d75-117">put_Method</span><span class="sxs-lookup"><span data-stu-id="46d75-117">put_Method</span></span>](#put_method) | <span data-ttu-id="46d75-118">Définissez la propriété Method.</span><span class="sxs-lookup"><span data-stu-id="46d75-118">Set the Method property.</span></span>
[<span data-ttu-id="46d75-119">get_Content</span><span class="sxs-lookup"><span data-stu-id="46d75-119">get_Content</span></span>](#get_content) | <span data-ttu-id="46d75-120">Le corps du message de requête HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="46d75-120">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="46d75-121">put_Content</span><span class="sxs-lookup"><span data-stu-id="46d75-121">put_Content</span></span>](#put_content) | <span data-ttu-id="46d75-122">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="46d75-122">Set the Content property.</span></span>
[<span data-ttu-id="46d75-123">get_Headers</span><span class="sxs-lookup"><span data-stu-id="46d75-123">get_Headers</span></span>](#get_headers) | <span data-ttu-id="46d75-124">En-têtes de requête HTTP mutables.</span><span class="sxs-lookup"><span data-stu-id="46d75-124">The mutable HTTP request headers.</span></span>

## <span data-ttu-id="46d75-125">Ses</span><span class="sxs-lookup"><span data-stu-id="46d75-125">Members</span></span>

#### <span data-ttu-id="46d75-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="46d75-126">get_Uri</span></span> 

<span data-ttu-id="46d75-127">URI de la requête.</span><span class="sxs-lookup"><span data-stu-id="46d75-127">The request URI.</span></span>

> <span data-ttu-id="46d75-128">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="46d75-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="46d75-129">put_Uri</span><span class="sxs-lookup"><span data-stu-id="46d75-129">put_Uri</span></span> 

<span data-ttu-id="46d75-130">Définissez la propriété Uri.</span><span class="sxs-lookup"><span data-stu-id="46d75-130">Set the Uri property.</span></span>

> <span data-ttu-id="46d75-131">[put_Uri](#put_uri)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="46d75-131">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

#### <span data-ttu-id="46d75-132">get_Method</span><span class="sxs-lookup"><span data-stu-id="46d75-132">get_Method</span></span> 

<span data-ttu-id="46d75-133">Méthode de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="46d75-133">The HTTP request method.</span></span>

> <span data-ttu-id="46d75-134">valeur publique HRESULT [get_Method](#get_method)(méthode LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="46d75-134">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="46d75-135">put_Method</span><span class="sxs-lookup"><span data-stu-id="46d75-135">put_Method</span></span> 

<span data-ttu-id="46d75-136">Définissez la propriété Method.</span><span class="sxs-lookup"><span data-stu-id="46d75-136">Set the Method property.</span></span>

> <span data-ttu-id="46d75-137">[put_Method](#put_method)par le biais du public HRESULT (méthode LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="46d75-137">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="46d75-138">get_Content</span><span class="sxs-lookup"><span data-stu-id="46d75-138">get_Content</span></span> 

<span data-ttu-id="46d75-139">Le corps du message de requête HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="46d75-139">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="46d75-140">accès public HRESULT [get_Content](#get_content)(IStream \* \* content)</span><span class="sxs-lookup"><span data-stu-id="46d75-140">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="46d75-141">Les données publiées seraient là.</span><span class="sxs-lookup"><span data-stu-id="46d75-141">POST data would be here.</span></span> <span data-ttu-id="46d75-142">Si un flux est défini, ce qui remplacera le corps du message, toutes les données de contenu doivent être disponibles lorsque le report de l’événement WebResourceRequested de la réponse est terminé.</span><span class="sxs-lookup"><span data-stu-id="46d75-142">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="46d75-143">Le flux doit être agile ou être créé à partir d’un STA d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="46d75-143">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="46d75-144">Null signifie qu’il n’y a pas de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="46d75-144">Null means no content data.</span></span> <span data-ttu-id="46d75-145">La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées)</span><span class="sxs-lookup"><span data-stu-id="46d75-145">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="46d75-146">put_Content</span><span class="sxs-lookup"><span data-stu-id="46d75-146">put_Content</span></span> 

<span data-ttu-id="46d75-147">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="46d75-147">Set the Content property.</span></span>

> <span data-ttu-id="46d75-148">[put_Content](#put_content)par le biais du contenu public HRESULT</span><span class="sxs-lookup"><span data-stu-id="46d75-148">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="46d75-149">get_Headers</span><span class="sxs-lookup"><span data-stu-id="46d75-149">get_Headers</span></span> 

<span data-ttu-id="46d75-150">En-têtes de requête HTTP mutables.</span><span class="sxs-lookup"><span data-stu-id="46d75-150">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="46d75-151">[get_Headersles](#get_headers)HRESULT publiques[(en](ICoreWebView2HttpRequestHeaders.md) -têtes \* \*)</span><span class="sxs-lookup"><span data-stu-id="46d75-151">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* headers)</span></span>

