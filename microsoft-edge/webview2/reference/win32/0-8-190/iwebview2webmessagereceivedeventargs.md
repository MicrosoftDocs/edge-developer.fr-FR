---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 4dfe2296312ac3ff3e9c67667c660aafcea38211
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885757"
---
# 0.8.355-interface IWebView2WebMessageReceivedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement WebMessageReceived.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Source](#get_source) | URI du document qui a envoyé ce message Web.
[get_WebMessageAsJson](#get_webmessageasjson) | Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.
[get_WebMessageAsString](#get_webmessageasstring) | Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.

## Ses

#### get_Source 

URI du document qui a envoyé ce message Web.

> valeur publique HRESULT [get_Source](#get_source)(LPWSTR * source)

#### get_WebMessageAsJson 

Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.

> valeur publique HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR * WebMessageAsJson)

Utilisez cette fonction pour communiquer par le biais d’objets JavaScript.

Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsJson suivantes:

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### get_WebMessageAsString 

Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.

> valeur publique HRESULT [get_WebMessageAsString](#get_webmessageasstring)(LPWSTR * WebMessageAsString)

Si le message publié est un autre type de type JavaScript, cette méthode échoue avec E_INVALIDARG. Utilisez cette fonction pour communiquer via des chaînes simples.

Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsString suivantes:

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

