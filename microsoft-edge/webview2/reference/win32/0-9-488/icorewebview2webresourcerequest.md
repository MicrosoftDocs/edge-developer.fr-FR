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
ms.openlocfilehash: 4b76cf998f8e2fd8982f7e51f1d9167e3862ec02
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653309"
---
# <span data-ttu-id="62281-104">interface ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="62281-104">interface ICoreWebView2WebResourceRequest</span></span> 

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="62281-105">Une requête HTTP utilisée avec l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="62281-105">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="62281-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="62281-106">Summary</span></span>

 <span data-ttu-id="62281-107">Ses</span><span class="sxs-lookup"><span data-stu-id="62281-107">Members</span></span>                        | <span data-ttu-id="62281-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="62281-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="62281-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="62281-109">get_Content</span></span>](#get_content) | <span data-ttu-id="62281-110">Le corps du message de requête HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="62281-110">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="62281-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="62281-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="62281-112">En-têtes de requête HTTP mutables.</span><span class="sxs-lookup"><span data-stu-id="62281-112">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="62281-113">get_Method</span><span class="sxs-lookup"><span data-stu-id="62281-113">get_Method</span></span>](#get_method) | <span data-ttu-id="62281-114">Méthode de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="62281-114">The HTTP request method.</span></span>
[<span data-ttu-id="62281-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="62281-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="62281-116">URI de la requête.</span><span class="sxs-lookup"><span data-stu-id="62281-116">The request URI.</span></span>
[<span data-ttu-id="62281-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="62281-117">put_Content</span></span>](#put_content) | <span data-ttu-id="62281-118">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="62281-118">Set the Content property.</span></span>
[<span data-ttu-id="62281-119">put_Method</span><span class="sxs-lookup"><span data-stu-id="62281-119">put_Method</span></span>](#put_method) | <span data-ttu-id="62281-120">Définissez la propriété Method.</span><span class="sxs-lookup"><span data-stu-id="62281-120">Set the Method property.</span></span>
[<span data-ttu-id="62281-121">put_Uri</span><span class="sxs-lookup"><span data-stu-id="62281-121">put_Uri</span></span>](#put_uri) | <span data-ttu-id="62281-122">Définissez la propriété Uri.</span><span class="sxs-lookup"><span data-stu-id="62281-122">Set the Uri property.</span></span>

## <span data-ttu-id="62281-123">Ses</span><span class="sxs-lookup"><span data-stu-id="62281-123">Members</span></span>

#### <span data-ttu-id="62281-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="62281-124">get_Content</span></span> 

<span data-ttu-id="62281-125">Le corps du message de requête HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="62281-125">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="62281-126">accès public HRESULT [get_Content](#get_content)(IStream \* \* content)</span><span class="sxs-lookup"><span data-stu-id="62281-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="62281-127">Les données publiées seraient là.</span><span class="sxs-lookup"><span data-stu-id="62281-127">POST data would be here.</span></span> <span data-ttu-id="62281-128">Si un flux est défini, ce qui remplacera le corps du message, toutes les données de contenu doivent être disponibles lorsque le report de l’événement WebResourceRequested de la réponse est terminé.</span><span class="sxs-lookup"><span data-stu-id="62281-128">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="62281-129">Le flux doit être agile ou être créé à partir d’un STA d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="62281-129">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="62281-130">Null signifie qu’il n’y a pas de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="62281-130">Null means no content data.</span></span> <span data-ttu-id="62281-131">La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées)</span><span class="sxs-lookup"><span data-stu-id="62281-131">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="62281-132">get_Headers</span><span class="sxs-lookup"><span data-stu-id="62281-132">get_Headers</span></span> 

<span data-ttu-id="62281-133">En-têtes de requête HTTP mutables.</span><span class="sxs-lookup"><span data-stu-id="62281-133">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="62281-134">[get_Headersles](#get_headers)HRESULT publiques[(en](icorewebview2httprequestheaders.md) -têtes \* \*)</span><span class="sxs-lookup"><span data-stu-id="62281-134">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="62281-135">get_Method</span><span class="sxs-lookup"><span data-stu-id="62281-135">get_Method</span></span> 

<span data-ttu-id="62281-136">Méthode de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="62281-136">The HTTP request method.</span></span>

> <span data-ttu-id="62281-137">valeur publique HRESULT [get_Method](#get_method)(méthode LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="62281-137">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="62281-138">get_Uri</span><span class="sxs-lookup"><span data-stu-id="62281-138">get_Uri</span></span> 

<span data-ttu-id="62281-139">URI de la requête.</span><span class="sxs-lookup"><span data-stu-id="62281-139">The request URI.</span></span>

> <span data-ttu-id="62281-140">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="62281-140">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="62281-141">put_Content</span><span class="sxs-lookup"><span data-stu-id="62281-141">put_Content</span></span> 

<span data-ttu-id="62281-142">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="62281-142">Set the Content property.</span></span>

> <span data-ttu-id="62281-143">[put_Content](#put_content)par le biais du contenu public HRESULT</span><span class="sxs-lookup"><span data-stu-id="62281-143">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="62281-144">put_Method</span><span class="sxs-lookup"><span data-stu-id="62281-144">put_Method</span></span> 

<span data-ttu-id="62281-145">Définissez la propriété Method.</span><span class="sxs-lookup"><span data-stu-id="62281-145">Set the Method property.</span></span>

> <span data-ttu-id="62281-146">[put_Method](#put_method)par le biais du public HRESULT (méthode LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="62281-146">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="62281-147">put_Uri</span><span class="sxs-lookup"><span data-stu-id="62281-147">put_Uri</span></span> 

<span data-ttu-id="62281-148">Définissez la propriété Uri.</span><span class="sxs-lookup"><span data-stu-id="62281-148">Set the Uri property.</span></span>

> <span data-ttu-id="62281-149">[put_Uri](#put_uri)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="62281-149">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

