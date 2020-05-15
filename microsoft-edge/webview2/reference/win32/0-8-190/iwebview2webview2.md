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
ms.openlocfilehash: 62daeaab702b431f787bc800ab79664fc183c4ce
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653252"
---
# interface IWebView2WebView2 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2WebView2
  : public IUnknown
```

Fonctionnalités supplémentaires implémentées par l’objet WebView principal.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Stop](#stop) | Arrêtez toutes les navigations et les extractions de ressources en attente.

Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2WebView](IWebView2WebView.md). Pour plus d’informations, consultez l’interface [IWebView2WebView](IWebView2WebView.md) .

## Ses

#### Stop 

Arrêtez toutes les navigations et les extractions de ressources en attente.

> point d' [arrêt](#stop)public HRESULT ()

