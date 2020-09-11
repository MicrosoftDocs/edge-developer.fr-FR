---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator
ms.openlocfilehash: e7aad408372acbbd19ecab9d04312f21e2396e88
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011897"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator 

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Itérateur pour une collection d’en-têtes HTTP.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[HasCurrentHeader](#hascurrentheader) | True lorsque l’itérateur n’a plus d’en-têtes.
[MoveNext](#movenext) | Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.

Voir CoreWebView2HttpRequestHeaders et CoreWebView2HttpResponseHeaders.

## Ses

#### HasCurrentHeader 

True lorsque l’itérateur n’a plus d’en-têtes.

> public bool [HasCurrentHeader](#hascurrentheader)

Si la collection sur laquelle l’itérateur est une itération est vide ou si l’itérateur a dépassé la fin de la collection, il s’agit de la valeur false.

#### MoveNext 

Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.

> public bool [MoveNext](#movenext)()

Le paramètre hasNext est défini sur FALSe s’il n’y a plus d’en-têtes HTTP. Après cela, la méthode GetCurrentHeader échoue si elle est appelée.

