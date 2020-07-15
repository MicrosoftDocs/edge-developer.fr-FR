---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2NewVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: e8965ebe2e0434d83b4d6e8eabe74466adb7cec6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878343"
---
# 0.8.355-interface IWebView2NewVersionAvailableEventArgs 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement NewVersionAvailable.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_NewVersion](#get_newversion) | Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel.

## Ses

#### get_NewVersion 

Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel.

> valeur publique HRESULT [get_NewVersion](#get_newversion)(LPWSTR * NewVersion)

