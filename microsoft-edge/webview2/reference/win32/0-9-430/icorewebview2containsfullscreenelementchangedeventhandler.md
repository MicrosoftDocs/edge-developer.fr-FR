---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 497a6b19800b6bb69712b57a4e4484d3f73662c5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881164"
---
# 0.9.430-interface ICoreWebView2ContainsFullScreenElementChangedEventHandler 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

L’appelant implémente cette méthode pour recevoir les événements ContainsFullScreenElementChanged.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.

Il n’existe aucun argument d’événement pour cet événement.

## Ses

#### Invoke 

Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.

> [appel](#invoke)de HRESULT public ([ICoreWebView2](ICoreWebView2.md) * sender, IUnknown * args)

Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.

