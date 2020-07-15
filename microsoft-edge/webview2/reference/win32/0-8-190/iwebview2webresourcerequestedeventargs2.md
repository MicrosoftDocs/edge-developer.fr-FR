---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebResourceRequestedEventArgs2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 80ea596f28d1afeb451ce20d495961ca4eed507a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878112"
---
# 0.8.355-interface IWebView2WebResourceRequestedEventArgs2 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2WebResourceRequestedEventArgs2
  : public IWebView2WebResourceRequestedEventArgs
```

Arguments d’événement pour l’événement WebResourceRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_ResourceContext](#get_resourcecontext) | Les contextes de requête de ressource Web.

## Ses

#### get_ResourceContext 

Les contextes de requête de ressource Web.

> [get_ResourceContext](#get_resourcecontext)par le biais du public HRESULT (WEBVIEW2_WEB_RESOURCE_CONTEXT * Context)

