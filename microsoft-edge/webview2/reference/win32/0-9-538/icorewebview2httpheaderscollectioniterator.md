---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2HttpHeadersCollectionIterator
ms.openlocfilehash: 56eacc7b06a3de5b29d316df032448b076b33e8f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879036"
---
# <span data-ttu-id="8376f-104">interface ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="8376f-104">interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="8376f-105">Itérateur pour une collection d’en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="8376f-105">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="8376f-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="8376f-106">Summary</span></span>

 <span data-ttu-id="8376f-107">Ses</span><span class="sxs-lookup"><span data-stu-id="8376f-107">Members</span></span>                        | <span data-ttu-id="8376f-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="8376f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8376f-109">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="8376f-109">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="8376f-110">True lorsque l’itérateur n’a plus d’en-têtes.</span><span class="sxs-lookup"><span data-stu-id="8376f-110">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="8376f-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="8376f-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="8376f-112">Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.</span><span class="sxs-lookup"><span data-stu-id="8376f-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="8376f-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="8376f-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="8376f-114">Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.</span><span class="sxs-lookup"><span data-stu-id="8376f-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="8376f-115">Voir [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) et [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span><span class="sxs-lookup"><span data-stu-id="8376f-115">See [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) and [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span></span> 
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

## <span data-ttu-id="8376f-116">Ses</span><span class="sxs-lookup"><span data-stu-id="8376f-116">Members</span></span>

#### <span data-ttu-id="8376f-117">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="8376f-117">get_HasCurrentHeader</span></span> 

<span data-ttu-id="8376f-118">True lorsque l’itérateur n’a plus d’en-têtes.</span><span class="sxs-lookup"><span data-stu-id="8376f-118">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="8376f-119">valeur publique HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="8376f-119">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="8376f-120">Si la collection sur laquelle l’itérateur est une itération est vide ou si l’itérateur a dépassé la fin de la collection, il s’agit de la valeur false.</span><span class="sxs-lookup"><span data-stu-id="8376f-120">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="8376f-121">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="8376f-121">GetCurrentHeader</span></span> 

<span data-ttu-id="8376f-122">Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.</span><span class="sxs-lookup"><span data-stu-id="8376f-122">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="8376f-123">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="8376f-123">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name, LPWSTR \* value)</span></span>

<span data-ttu-id="8376f-124">Cette méthode échoue si le dernier appel à MoveNext définit has_next sur FALSe.</span><span class="sxs-lookup"><span data-stu-id="8376f-124">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="8376f-125">MoveNext</span><span class="sxs-lookup"><span data-stu-id="8376f-125">MoveNext</span></span> 

<span data-ttu-id="8376f-126">Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.</span><span class="sxs-lookup"><span data-stu-id="8376f-126">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="8376f-127">public HRESULT [MoveNext](#movenext)(bool \* hasNext)</span><span class="sxs-lookup"><span data-stu-id="8376f-127">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="8376f-128">Le paramètre hasNext est défini sur FALSe s’il n’y a plus d’en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="8376f-128">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="8376f-129">Après cela, la méthode GetCurrentHeader échoue si elle est appelée.</span><span class="sxs-lookup"><span data-stu-id="8376f-129">After this occurs the GetCurrentHeader method will fail if called.</span></span>

