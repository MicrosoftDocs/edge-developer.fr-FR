---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: dbcc5b10ce1973df61554f3f27174f600fb25280
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885980"
---
# <span data-ttu-id="ca37d-104">0.8.355-interface IWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="ca37d-104">0.8.355 - interface IWebView2HttpHeadersCollectionIterator</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="ca37d-105">Itérateur pour une collection d’en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="ca37d-105">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="ca37d-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="ca37d-106">Summary</span></span>

 <span data-ttu-id="ca37d-107">Ses</span><span class="sxs-lookup"><span data-stu-id="ca37d-107">Members</span></span>                        | <span data-ttu-id="ca37d-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="ca37d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ca37d-109">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="ca37d-109">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="ca37d-110">Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.</span><span class="sxs-lookup"><span data-stu-id="ca37d-110">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="ca37d-111">MoveNext</span><span class="sxs-lookup"><span data-stu-id="ca37d-111">MoveNext</span></span>](#movenext) | <span data-ttu-id="ca37d-112">Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.</span><span class="sxs-lookup"><span data-stu-id="ca37d-112">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="ca37d-113">Voir [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) et [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span><span class="sxs-lookup"><span data-stu-id="ca37d-113">See [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) and [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span></span>

## <span data-ttu-id="ca37d-114">Ses</span><span class="sxs-lookup"><span data-stu-id="ca37d-114">Members</span></span>

#### <span data-ttu-id="ca37d-115">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="ca37d-115">GetCurrentHeader</span></span> 

<span data-ttu-id="ca37d-116">Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.</span><span class="sxs-lookup"><span data-stu-id="ca37d-116">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="ca37d-117">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="ca37d-117">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name,LPWSTR \* value)</span></span>

<span data-ttu-id="ca37d-118">Cette méthode échoue si le dernier appel à MoveNext définit has_next sur FALSe.</span><span class="sxs-lookup"><span data-stu-id="ca37d-118">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="ca37d-119">MoveNext</span><span class="sxs-lookup"><span data-stu-id="ca37d-119">MoveNext</span></span> 

<span data-ttu-id="ca37d-120">Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.</span><span class="sxs-lookup"><span data-stu-id="ca37d-120">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="ca37d-121">public HRESULT [MoveNext](#movenext)(BOOL \* has_next)</span><span class="sxs-lookup"><span data-stu-id="ca37d-121">public HRESULT [MoveNext](#movenext)(BOOL \* has_next)</span></span>

<span data-ttu-id="ca37d-122">Le paramètre has_next est défini sur FALSe s’il n’y a plus d’en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="ca37d-122">The has_next parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="ca37d-123">Après cela, la méthode GetCurrentHeader échoue si elle est appelée.</span><span class="sxs-lookup"><span data-stu-id="ca37d-123">After this occurs the GetCurrentHeader method will fail if called.</span></span>

