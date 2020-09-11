---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2HistoryChangedEventHandler
ms.openlocfilehash: 68cecdec63e64bde978156f17d6755a483abcc66
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011341"
---
# 0.9.579-interface ICoreWebView2HistoryChangedEventHandler 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

