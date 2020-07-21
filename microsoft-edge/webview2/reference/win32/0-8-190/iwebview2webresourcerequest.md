---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: e9d84fbd459d56b82ab4b7d253526e517960c1db
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885722"
---
# <span data-ttu-id="e8755-104">0.8.355-interface IWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="e8755-104">0.8.355 - interface IWebView2WebResourceRequest</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="e8755-105">Une requête HTTP utilisée avec l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="e8755-105">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="e8755-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="e8755-106">Summary</span></span>

 <span data-ttu-id="e8755-107">Ses</span><span class="sxs-lookup"><span data-stu-id="e8755-107">Members</span></span>                        | <span data-ttu-id="e8755-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e8755-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e8755-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="e8755-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="e8755-110">URI de la requête.</span><span class="sxs-lookup"><span data-stu-id="e8755-110">The request URI.</span></span>
[<span data-ttu-id="e8755-111">put_Uri</span><span class="sxs-lookup"><span data-stu-id="e8755-111">put_Uri</span></span>](#put_uri) | <span data-ttu-id="e8755-112">Définissez la propriété Uri.</span><span class="sxs-lookup"><span data-stu-id="e8755-112">Set the Uri property.</span></span>
[<span data-ttu-id="e8755-113">get_Method</span><span class="sxs-lookup"><span data-stu-id="e8755-113">get_Method</span></span>](#get_method) | <span data-ttu-id="e8755-114">Méthode de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="e8755-114">The HTTP request method.</span></span>
[<span data-ttu-id="e8755-115">put_Method</span><span class="sxs-lookup"><span data-stu-id="e8755-115">put_Method</span></span>](#put_method) | <span data-ttu-id="e8755-116">Définissez la propriété Method.</span><span class="sxs-lookup"><span data-stu-id="e8755-116">Set the Method property.</span></span>
[<span data-ttu-id="e8755-117">get_Content</span><span class="sxs-lookup"><span data-stu-id="e8755-117">get_Content</span></span>](#get_content) | <span data-ttu-id="e8755-118">Le corps du message de requête HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="e8755-118">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="e8755-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="e8755-119">put_Content</span></span>](#put_content) | <span data-ttu-id="e8755-120">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="e8755-120">Set the Content property.</span></span>
[<span data-ttu-id="e8755-121">get_Headers</span><span class="sxs-lookup"><span data-stu-id="e8755-121">get_Headers</span></span>](#get_headers) | <span data-ttu-id="e8755-122">En-têtes de requête HTTP mutables.</span><span class="sxs-lookup"><span data-stu-id="e8755-122">The mutable HTTP request headers.</span></span>

## <span data-ttu-id="e8755-123">Ses</span><span class="sxs-lookup"><span data-stu-id="e8755-123">Members</span></span>

#### <span data-ttu-id="e8755-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="e8755-124">get_Uri</span></span> 

<span data-ttu-id="e8755-125">URI de la requête.</span><span class="sxs-lookup"><span data-stu-id="e8755-125">The request URI.</span></span>

> <span data-ttu-id="e8755-126">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="e8755-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="e8755-127">put_Uri</span><span class="sxs-lookup"><span data-stu-id="e8755-127">put_Uri</span></span> 

<span data-ttu-id="e8755-128">Définissez la propriété Uri.</span><span class="sxs-lookup"><span data-stu-id="e8755-128">Set the Uri property.</span></span>

> <span data-ttu-id="e8755-129">[put_Uri](#put_uri)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e8755-129">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

#### <span data-ttu-id="e8755-130">get_Method</span><span class="sxs-lookup"><span data-stu-id="e8755-130">get_Method</span></span> 

<span data-ttu-id="e8755-131">Méthode de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="e8755-131">The HTTP request method.</span></span>

> <span data-ttu-id="e8755-132">valeur publique HRESULT [get_Method](#get_method)(méthode LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="e8755-132">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="e8755-133">put_Method</span><span class="sxs-lookup"><span data-stu-id="e8755-133">put_Method</span></span> 

<span data-ttu-id="e8755-134">Définissez la propriété Method.</span><span class="sxs-lookup"><span data-stu-id="e8755-134">Set the Method property.</span></span>

> <span data-ttu-id="e8755-135">[put_Method](#put_method)par le biais du public HRESULT (méthode LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="e8755-135">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="e8755-136">get_Content</span><span class="sxs-lookup"><span data-stu-id="e8755-136">get_Content</span></span> 

<span data-ttu-id="e8755-137">Le corps du message de requête HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="e8755-137">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="e8755-138">accès public HRESULT [get_Content](#get_content)(IStream \* \* content)</span><span class="sxs-lookup"><span data-stu-id="e8755-138">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="e8755-139">Les données publiées seraient là.</span><span class="sxs-lookup"><span data-stu-id="e8755-139">POST data would be here.</span></span> <span data-ttu-id="e8755-140">Si un flux est défini, ce qui remplacera le corps du message, toutes les données de contenu doivent être disponibles lorsque le report de l’événement WebResourceRequested de la réponse est terminé.</span><span class="sxs-lookup"><span data-stu-id="e8755-140">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="e8755-141">Le flux doit être agile ou être créé à partir d’un STA d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e8755-141">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="e8755-142">Null signifie qu’il n’y a pas de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="e8755-142">Null means no content data.</span></span> <span data-ttu-id="e8755-143">La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées)</span><span class="sxs-lookup"><span data-stu-id="e8755-143">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="e8755-144">put_Content</span><span class="sxs-lookup"><span data-stu-id="e8755-144">put_Content</span></span> 

<span data-ttu-id="e8755-145">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="e8755-145">Set the Content property.</span></span>

> <span data-ttu-id="e8755-146">[put_Content](#put_content)par le biais du contenu public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e8755-146">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="e8755-147">get_Headers</span><span class="sxs-lookup"><span data-stu-id="e8755-147">get_Headers</span></span> 

<span data-ttu-id="e8755-148">En-têtes de requête HTTP mutables.</span><span class="sxs-lookup"><span data-stu-id="e8755-148">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="e8755-149">[get_Headersles](#get_headers)HRESULT publiques[(en](IWebView2HttpRequestHeaders.md) -têtes \* \*)</span><span class="sxs-lookup"><span data-stu-id="e8755-149">public HRESULT [get_Headers](#get_headers)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* headers)</span></span>

