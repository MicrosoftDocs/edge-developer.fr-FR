---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 053e186aec3871b47e2eb5c6684bc00c934c3a77
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653377"
---
# interface IWebView2WebMessageReceivedEventArgs 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

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

