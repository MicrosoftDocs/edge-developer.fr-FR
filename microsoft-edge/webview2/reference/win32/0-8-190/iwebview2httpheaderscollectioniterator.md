---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 7abc6119d893cd1e9432d255969549f07d7e3a00
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878462"
---
# <span data-ttu-id="86fbf-104">0.8.355-interface IWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="86fbf-104">0.8.355 - interface IWebView2HttpHeadersCollectionIterator</span></span> 

> [!NOTE]
> <span data-ttu-id="86fbf-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="86fbf-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="86fbf-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="86fbf-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="86fbf-107">Itérateur pour une collection d’en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="86fbf-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="86fbf-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="86fbf-108">Summary</span></span>

 <span data-ttu-id="86fbf-109">Ses</span><span class="sxs-lookup"><span data-stu-id="86fbf-109">Members</span></span>                        | <span data-ttu-id="86fbf-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="86fbf-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="86fbf-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="86fbf-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="86fbf-112">Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.</span><span class="sxs-lookup"><span data-stu-id="86fbf-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="86fbf-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="86fbf-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="86fbf-114">Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.</span><span class="sxs-lookup"><span data-stu-id="86fbf-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="86fbf-115">Voir [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) et [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span><span class="sxs-lookup"><span data-stu-id="86fbf-115">See [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) and [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span></span>

## <span data-ttu-id="86fbf-116">Ses</span><span class="sxs-lookup"><span data-stu-id="86fbf-116">Members</span></span>

#### <span data-ttu-id="86fbf-117">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="86fbf-117">GetCurrentHeader</span></span> 

<span data-ttu-id="86fbf-118">Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.</span><span class="sxs-lookup"><span data-stu-id="86fbf-118">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="86fbf-119">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="86fbf-119">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name,LPWSTR \* value)</span></span>

<span data-ttu-id="86fbf-120">Cette méthode échoue si le dernier appel à MoveNext définit has_next sur FALSe.</span><span class="sxs-lookup"><span data-stu-id="86fbf-120">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="86fbf-121">MoveNext</span><span class="sxs-lookup"><span data-stu-id="86fbf-121">MoveNext</span></span> 

<span data-ttu-id="86fbf-122">Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.</span><span class="sxs-lookup"><span data-stu-id="86fbf-122">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="86fbf-123">public HRESULT [MoveNext](#movenext)(BOOL \* has_next)</span><span class="sxs-lookup"><span data-stu-id="86fbf-123">public HRESULT [MoveNext](#movenext)(BOOL \* has_next)</span></span>

<span data-ttu-id="86fbf-124">Le paramètre has_next est défini sur FALSe s’il n’y a plus d’en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="86fbf-124">The has_next parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="86fbf-125">Après cela, la méthode GetCurrentHeader échoue si elle est appelée.</span><span class="sxs-lookup"><span data-stu-id="86fbf-125">After this occurs the GetCurrentHeader method will fail if called.</span></span>

