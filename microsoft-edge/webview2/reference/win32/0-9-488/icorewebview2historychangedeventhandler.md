---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 5c4807a6f1772354f4448b25d49ea7ea86278f57
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880604"
---
# 0.9.515-interface ICoreWebView2HistoryChangedEventHandler 

> [!NOTE]
> Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515. Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.

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

> [appel](#invoke)vers un HRESULT public ([ICoreWebView2](icorewebview2.md) * WebView, IUnknown * args)

