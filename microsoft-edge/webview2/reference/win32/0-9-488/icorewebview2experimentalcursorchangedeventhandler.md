---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 6fbcc82409791bc3d2da3bb2f7985732cb344a97
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880625"
---
# 0.9.515-interface ICoreWebView2ExperimentalCursorChangedEventHandler 

> [!NOTE]
> Cette API expérimentale qui est fournie avec notre version bêta du SDK version 0.9.488.

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

L’appelant implémente cette interface pour recevoir des événements CursorChanged.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.

Utilisez la propriété Cursor pour obtenir le nouveau curseur.

## Ses

#### Invoke 

Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.

> [appel](#invoke)de HRESULT public ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) * sender, IUnknown * args)

Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.

