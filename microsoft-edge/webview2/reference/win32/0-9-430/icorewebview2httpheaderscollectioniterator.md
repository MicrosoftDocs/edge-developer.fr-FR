---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 29f4a09af459e80f8c299a66b24d061e79a96f92
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881024"
---
# <span data-ttu-id="c63d8-104">0.9.430-interface ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="c63d8-104">0.9.430 - interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

> [!NOTE]
> <span data-ttu-id="c63d8-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="c63d8-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="c63d8-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="c63d8-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="c63d8-107">Itérateur pour une collection d’en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="c63d8-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="c63d8-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="c63d8-108">Summary</span></span>

 <span data-ttu-id="c63d8-109">Ses</span><span class="sxs-lookup"><span data-stu-id="c63d8-109">Members</span></span>                        | <span data-ttu-id="c63d8-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c63d8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c63d8-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="c63d8-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="c63d8-112">Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.</span><span class="sxs-lookup"><span data-stu-id="c63d8-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="c63d8-113">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="c63d8-113">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="c63d8-114">True lorsque l’itérateur n’a plus d’en-têtes.</span><span class="sxs-lookup"><span data-stu-id="c63d8-114">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="c63d8-115">MoveNext</span><span class="sxs-lookup"><span data-stu-id="c63d8-115">MoveNext</span></span>](#movenext) | <span data-ttu-id="c63d8-116">Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.</span><span class="sxs-lookup"><span data-stu-id="c63d8-116">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="c63d8-117">Voir [ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) et [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md).</span><span class="sxs-lookup"><span data-stu-id="c63d8-117">See [ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) and [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md).</span></span> 

```cpp
std::wstring RequestHeadersToJsonString(ICoreWebView2HttpRequestHeaders* requestHeaders)
{
    wil::com_ptr<ICoreWebView2HttpHeadersCollectionIterator> iterator;
    CHECK_FAILURE(requestHeaders->GetIterator(&iterator));
    BOOL hasCurrent = FALSE;
    std::wstring result = L"[";

    while (SUCCEEDED(iterator->get_HasCurrentHeader(&hasCurrent)) && hasCurrent)
    {
        wil::unique_cotaskmem_string name;
        wil::unique_cotaskmem_string value;

        CHECK_FAILURE(iterator->GetCurrentHeader(&name, &value));
        result += L"{\"name\": " + EncodeQuote(name.get())
            + L", \"value\": " + EncodeQuote(value.get()) + L"}";

        BOOL hasNext = FALSE;
        CHECK_FAILURE(iterator->MoveNext(&hasNext));
        if (hasNext)
        {
            result += L", ";
        }
    }

    return result + L"]";
}
```

## <span data-ttu-id="c63d8-118">Ses</span><span class="sxs-lookup"><span data-stu-id="c63d8-118">Members</span></span>

#### <span data-ttu-id="c63d8-119">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="c63d8-119">GetCurrentHeader</span></span> 

<span data-ttu-id="c63d8-120">Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.</span><span class="sxs-lookup"><span data-stu-id="c63d8-120">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="c63d8-121">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="c63d8-121">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name,LPWSTR \* value)</span></span>

<span data-ttu-id="c63d8-122">Cette méthode échoue si le dernier appel à MoveNext définit has_next sur FALSe.</span><span class="sxs-lookup"><span data-stu-id="c63d8-122">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="c63d8-123">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="c63d8-123">get_HasCurrentHeader</span></span> 

<span data-ttu-id="c63d8-124">True lorsque l’itérateur n’a plus d’en-têtes.</span><span class="sxs-lookup"><span data-stu-id="c63d8-124">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="c63d8-125">valeur publique HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="c63d8-125">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="c63d8-126">Si la collection sur laquelle l’itérateur est une itération est vide ou si l’itérateur a dépassé la fin de la collection, il s’agit de la valeur false.</span><span class="sxs-lookup"><span data-stu-id="c63d8-126">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="c63d8-127">MoveNext</span><span class="sxs-lookup"><span data-stu-id="c63d8-127">MoveNext</span></span> 

<span data-ttu-id="c63d8-128">Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.</span><span class="sxs-lookup"><span data-stu-id="c63d8-128">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="c63d8-129">public HRESULT [MoveNext](#movenext)(bool \* hasNext)</span><span class="sxs-lookup"><span data-stu-id="c63d8-129">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="c63d8-130">Le paramètre hasNext est défini sur FALSe s’il n’y a plus d’en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="c63d8-130">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="c63d8-131">Après cela, la méthode GetCurrentHeader échoue si elle est appelée.</span><span class="sxs-lookup"><span data-stu-id="c63d8-131">After this occurs the GetCurrentHeader method will fail if called.</span></span>

