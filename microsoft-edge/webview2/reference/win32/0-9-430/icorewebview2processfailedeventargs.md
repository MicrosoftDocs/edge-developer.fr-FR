---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: f4238f0d75f39727260296703e84740ca77b30d4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877736"
---
# 0.9.430-interface ICoreWebView2ProcessFailedEventArgs 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement ProcessFailed.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_ProcessFailedKind](#get_processfailedkind) | Type d’échec du processus qui s’est produit.

## Ses

#### get_ProcessFailedKind 

Type d’échec du processus qui s’est produit.

> [get_ProcessFailedKind](#get_processfailedkind)par le biais du public HRESULT (CORE_WEBVIEW2_PROCESS_FAILED_KIND * ProcessFailedKind)

