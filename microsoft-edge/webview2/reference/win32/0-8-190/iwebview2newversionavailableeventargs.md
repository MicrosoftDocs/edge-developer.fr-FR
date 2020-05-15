---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 0314c796865d3d745b831d050498f59868e38e8f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653594"
---
# interface IWebView2NewVersionAvailableEventArgs 

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

