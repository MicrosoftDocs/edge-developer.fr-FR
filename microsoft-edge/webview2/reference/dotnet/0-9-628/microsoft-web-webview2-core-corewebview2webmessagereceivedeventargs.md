---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
ms.openlocfilehash: ab273337307eeef6e8842d337296756877939aff
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011852"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs 

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

