---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2DevToolsProtocolEventReceivedEventArgs
ms.openlocfilehash: de10adbfe7e74a1679aa8b77cb96775561d87a17
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880128"
---
# interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement DevToolsProtocolEventReceived.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_ParameterObjectAsJson](#get_parameterobjectasjson) | Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.

## Ses

#### get_ParameterObjectAsJson 

Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.

> valeur publique HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR * ParameterObjectAsJson)

