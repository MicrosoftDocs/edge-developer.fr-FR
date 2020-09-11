---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2HttpHeadersCollectionIterator
ms.openlocfilehash: 8044b629c5b182d98e4731409301f615a6fba18e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011963"
---
# interface ICoreWebView2HttpHeadersCollectionIterator 

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

Itérateur pour une collection d’en-têtes HTTP.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_HasCurrentHeader](#get_hascurrentheader) | True lorsque l’itérateur n’a plus d’en-têtes.
[GetCurrentHeader](#getcurrentheader) | Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.
[MoveNext](#movenext) | Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.

Voir [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) et [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).

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

## Ses

#### get_HasCurrentHeader 

True lorsque l’itérateur n’a plus d’en-têtes.

> valeur publique HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(bool * hasCurrent)

Si la collection sur laquelle l’itérateur est une itération est vide ou si l’itérateur a dépassé la fin de la collection, il s’agit de la valeur false.

#### GetCurrentHeader 

Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.

> public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR * Name, LPWStr * value)

Cette méthode échoue si le dernier appel à MoveNext définit hasNext sur FALSe.

#### MoveNext 

Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.

> public HRESULT [MoveNext](#movenext)(bool * hasNext)

Le paramètre hasNext est défini sur FALSe s’il n’y a plus d’en-têtes HTTP. Après cela, la méthode GetCurrentHeader échoue si elle est appelée.

