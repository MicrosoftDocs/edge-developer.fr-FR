---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 640926481e99c6571c0cbf9c345efa56d97e3f66
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885596"
---
# <span data-ttu-id="10a58-104">0.9.430-interface ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="10a58-104">0.9.430 - interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="10a58-105">Itérateur pour une collection d’en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="10a58-105">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="10a58-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="10a58-106">Summary</span></span>

 <span data-ttu-id="10a58-107">Ses</span><span class="sxs-lookup"><span data-stu-id="10a58-107">Members</span></span>                        | <span data-ttu-id="10a58-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="10a58-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="10a58-109">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="10a58-109">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="10a58-110">Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.</span><span class="sxs-lookup"><span data-stu-id="10a58-110">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="10a58-111">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="10a58-111">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="10a58-112">True lorsque l’itérateur n’a plus d’en-têtes.</span><span class="sxs-lookup"><span data-stu-id="10a58-112">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="10a58-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="10a58-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="10a58-114">Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.</span><span class="sxs-lookup"><span data-stu-id="10a58-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="10a58-115">Voir [ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) et [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md).</span><span class="sxs-lookup"><span data-stu-id="10a58-115">See [ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) and [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md).</span></span> 

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

## <span data-ttu-id="10a58-116">Ses</span><span class="sxs-lookup"><span data-stu-id="10a58-116">Members</span></span>

#### <span data-ttu-id="10a58-117">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="10a58-117">GetCurrentHeader</span></span> 

<span data-ttu-id="10a58-118">Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.</span><span class="sxs-lookup"><span data-stu-id="10a58-118">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="10a58-119">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="10a58-119">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name,LPWSTR \* value)</span></span>

<span data-ttu-id="10a58-120">Cette méthode échoue si le dernier appel à MoveNext définit has_next sur FALSe.</span><span class="sxs-lookup"><span data-stu-id="10a58-120">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="10a58-121">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="10a58-121">get_HasCurrentHeader</span></span> 

<span data-ttu-id="10a58-122">True lorsque l’itérateur n’a plus d’en-têtes.</span><span class="sxs-lookup"><span data-stu-id="10a58-122">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="10a58-123">valeur publique HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="10a58-123">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="10a58-124">Si la collection sur laquelle l’itérateur est une itération est vide ou si l’itérateur a dépassé la fin de la collection, il s’agit de la valeur false.</span><span class="sxs-lookup"><span data-stu-id="10a58-124">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="10a58-125">MoveNext</span><span class="sxs-lookup"><span data-stu-id="10a58-125">MoveNext</span></span> 

<span data-ttu-id="10a58-126">Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.</span><span class="sxs-lookup"><span data-stu-id="10a58-126">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="10a58-127">public HRESULT [MoveNext](#movenext)(bool \* hasNext)</span><span class="sxs-lookup"><span data-stu-id="10a58-127">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="10a58-128">Le paramètre hasNext est défini sur FALSe s’il n’y a plus d’en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="10a58-128">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="10a58-129">Après cela, la méthode GetCurrentHeader échoue si elle est appelée.</span><span class="sxs-lookup"><span data-stu-id="10a58-129">After this occurs the GetCurrentHeader method will fail if called.</span></span>

