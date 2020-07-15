---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 6afd1983b90b4412fd3011dc35f192809a9583b7
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881017"
---
# 0.9.430-interface ICoreWebView2HistoryChangedEventHandler 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

L’appelant implémente cette interface pour recevoir l’événement HistoryChanged.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.

## Ses

#### Invoke 

Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.

> [appel](#invoke)vers un HRESULT public ([ICoreWebView2](ICoreWebView2.md) * WebView, IUnknown * args)

