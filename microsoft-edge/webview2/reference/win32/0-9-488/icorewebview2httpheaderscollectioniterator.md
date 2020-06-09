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
ms.openlocfilehash: 2f0a41c72c6ac6f7bcfbf7a5cbd5eef61ffa3a68
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697265"
---
# <span data-ttu-id="0064a-104">interface ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="0064a-104">interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

> [!NOTE]
> <span data-ttu-id="0064a-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="0064a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="0064a-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="0064a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="0064a-107">Itérateur pour une collection d’en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="0064a-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="0064a-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="0064a-108">Summary</span></span>

 <span data-ttu-id="0064a-109">Ses</span><span class="sxs-lookup"><span data-stu-id="0064a-109">Members</span></span>                        | <span data-ttu-id="0064a-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0064a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0064a-111">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="0064a-111">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="0064a-112">True lorsque l’itérateur n’a plus d’en-têtes.</span><span class="sxs-lookup"><span data-stu-id="0064a-112">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="0064a-113">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="0064a-113">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="0064a-114">Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.</span><span class="sxs-lookup"><span data-stu-id="0064a-114">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="0064a-115">MoveNext</span><span class="sxs-lookup"><span data-stu-id="0064a-115">MoveNext</span></span>](#movenext) | <span data-ttu-id="0064a-116">Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.</span><span class="sxs-lookup"><span data-stu-id="0064a-116">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="0064a-117">Voir [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) et [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span><span class="sxs-lookup"><span data-stu-id="0064a-117">See [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) and [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span></span> 
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

## <span data-ttu-id="0064a-118">Ses</span><span class="sxs-lookup"><span data-stu-id="0064a-118">Members</span></span>

#### <span data-ttu-id="0064a-119">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="0064a-119">get_HasCurrentHeader</span></span> 

<span data-ttu-id="0064a-120">True lorsque l’itérateur n’a plus d’en-têtes.</span><span class="sxs-lookup"><span data-stu-id="0064a-120">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="0064a-121">valeur publique HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="0064a-121">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="0064a-122">Si la collection sur laquelle l’itérateur est une itération est vide ou si l’itérateur a dépassé la fin de la collection, il s’agit de la valeur false.</span><span class="sxs-lookup"><span data-stu-id="0064a-122">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="0064a-123">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="0064a-123">GetCurrentHeader</span></span> 

<span data-ttu-id="0064a-124">Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.</span><span class="sxs-lookup"><span data-stu-id="0064a-124">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="0064a-125">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* Name, LPWStr \* value)</span><span class="sxs-lookup"><span data-stu-id="0064a-125">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name, LPWSTR \* value)</span></span>

<span data-ttu-id="0064a-126">Cette méthode échoue si le dernier appel à MoveNext définit has_next sur FALSe.</span><span class="sxs-lookup"><span data-stu-id="0064a-126">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="0064a-127">MoveNext</span><span class="sxs-lookup"><span data-stu-id="0064a-127">MoveNext</span></span> 

<span data-ttu-id="0064a-128">Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.</span><span class="sxs-lookup"><span data-stu-id="0064a-128">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="0064a-129">public HRESULT [MoveNext](#movenext)(bool \* hasNext)</span><span class="sxs-lookup"><span data-stu-id="0064a-129">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="0064a-130">Le paramètre hasNext est défini sur FALSe s’il n’y a plus d’en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="0064a-130">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="0064a-131">Après cela, la méthode GetCurrentHeader échoue si elle est appelée.</span><span class="sxs-lookup"><span data-stu-id="0064a-131">After this occurs the GetCurrentHeader method will fail if called.</span></span>

