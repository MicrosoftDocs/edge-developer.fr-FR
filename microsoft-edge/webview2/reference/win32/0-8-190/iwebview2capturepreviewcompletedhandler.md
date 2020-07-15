---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 9e8b1cc973eefbd41c1fac0d7d9723ba35ec7302
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878679"
---
# 0.8.355-interface IWebView2CapturePreviewCompletedHandler 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

L’appelant implémente cette méthode pour recevoir le résultat de la méthode CapturePreview.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.

Le résultat est écrit dans le flux fourni lors de l’appel de méthode CapturePreview.

## Ses

#### Invoke 

Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.

> [appel](#invoke)HRESULT public (résultat HRESULT)

