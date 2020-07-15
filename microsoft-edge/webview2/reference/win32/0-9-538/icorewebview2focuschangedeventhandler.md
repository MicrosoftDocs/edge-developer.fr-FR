---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2FocusChangedEventHandler
ms.openlocfilehash: fc952437a9d5ffa7bb709bb6fb322438851babcd
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879897"
---
# interface ICoreWebView2FocusChangedEventHandler 

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

L’appelant implémente cette méthode pour recevoir les événements GotFocus et LostFocus.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.

Il n’existe aucun argument d’événement pour cet événement.

## Ses

#### Invoke 

Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.

> [appel](#invoke)de HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) * sender, IUnknown * args)

Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.

