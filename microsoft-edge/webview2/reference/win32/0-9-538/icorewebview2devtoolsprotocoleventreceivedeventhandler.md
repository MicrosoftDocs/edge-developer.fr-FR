---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2DevToolsProtocolEventReceivedEventHandler
ms.openlocfilehash: 2cb38d40e4e4a5e527cc8e8643b31ae7ceebecbe
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879596"
---
# interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

L’appelant implémente cette interface pour recevoir des événements DevToolsProtocolEventReceived du WebView.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.

## Ses

#### Invoke 

Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.

> [appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) * sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) * args)

