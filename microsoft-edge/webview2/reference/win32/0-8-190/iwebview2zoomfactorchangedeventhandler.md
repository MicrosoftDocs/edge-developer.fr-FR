---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 237179df5ef704fb88516780696f3a9c10c9a198
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884665"
---
# 0.8.355-interface IWebView2ZoomFactorChangedEventHandler 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

L’appelant implémente cette interface pour recevoir des événements ZoomFactorChanged.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.

Utilisez la propriété IWebView2WebView. ZoomFactor pour obtenir le facteur de zoom modifié.

## Ses

#### Invoke 

Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.

> [appel](#invoke)vers un HRESULT public ([IWebView2WebView](IWebView2WebView.md) * WebView, IUnknown * args)

Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.

