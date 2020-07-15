---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: f59b5acac510b66eae0e1ada51e28b6dd9363ca8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877853"
---
# 0.9.430-interface ICoreWebView2NewBrowserVersionAvailableEventArgs 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement NewBrowserVersionAvailable.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_NewVersion](#get_newversion) | Les informations de la version du navigateur du [ICoreWebView2Environment](ICoreWebView2Environment.md)actuel.

## Ses

#### get_NewVersion 

Les informations de la version du navigateur du [ICoreWebView2Environment](ICoreWebView2Environment.md)actuel.

> valeur publique HRESULT [get_NewVersion](#get_newversion)(LPWSTR * NewVersion)

