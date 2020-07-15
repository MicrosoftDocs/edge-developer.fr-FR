---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 372bd0f6faa3b5ed50c539a2e10809bfe9b95209
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878231"
---
# 0.8.355-interface IWebView2ProcessFailedEventHandler 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2ProcessFailedEventHandler
  : public IUnknown
```

L’appelant implémente cette interface pour recevoir des événements ProcessFailed.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.

## Ses

#### Invoke 

Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.

> [appel](#invoke)HRESULT public ([IWebView2WebView](IWebView2WebView.md) * WebView,[IWebView2ProcessFailedEventArgs](IWebView2ProcessFailedEventArgs.md) * args)

