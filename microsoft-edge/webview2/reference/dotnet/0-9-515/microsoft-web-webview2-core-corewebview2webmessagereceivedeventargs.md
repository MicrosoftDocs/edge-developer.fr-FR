---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: a3d1f899cb270f9a44d92d647ab2f5a4d5c3b02a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886366"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Arguments d’événement pour l’événement WebMessageReceived.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Source](#source) | URI du document qui a envoyé ce message Web.
[WebMessageAsJson](#webmessageasjson) | Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.
[TryGetWebMessageAsString](#trygetwebmessageasstring) | Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.

## Ses

#### Source 

URI du document qui a envoyé ce message Web.

> [source](#source) de chaîne publique

#### WebMessageAsJson 

Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.

> [WebMessageAsJson](#webmessageasjson) de chaîne publique

Utilisez cette fonction pour communiquer par le biais d’objets JavaScript.

Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsJson suivantes:

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### TryGetWebMessageAsString 

Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.

> chaîne publique [TryGetWebMessageAsString](#trygetwebmessageasstring)()

Si le message publié est un autre type de type JavaScript, cette méthode échoue avec E_INVALIDARG. Utilisez cette fonction pour communiquer via des chaînes simples.

Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsString suivantes:

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

