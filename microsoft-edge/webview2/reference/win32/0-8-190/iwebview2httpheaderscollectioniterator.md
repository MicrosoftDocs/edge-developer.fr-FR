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
# 0.8.355-interface IWebView2HttpHeadersCollectionIterator 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

Itérateur pour une collection d’en-têtes HTTP.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[GetCurrentHeader](#getcurrentheader) | Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.
[MoveNext](#movenext) | Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.

Voir [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) et [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).

## Ses

#### GetCurrentHeader 

Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.

> public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR * Name, LPWStr * value)

Cette méthode échoue si le dernier appel à MoveNext définit has_next sur FALSe.

#### MoveNext 

Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.

> public HRESULT [MoveNext](#movenext)(BOOL * has_next)

Le paramètre has_next est défini sur FALSe s’il n’y a plus d’en-têtes HTTP. Après cela, la méthode GetCurrentHeader échoue si elle est appelée.

