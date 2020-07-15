---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: a6c7acf933192bfe96ac863620d3348eeca41ec7
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880793"
---
# 0.9.515-interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs 

> [!NOTE]
> Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515. Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.

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

