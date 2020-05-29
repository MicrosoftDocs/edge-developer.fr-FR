---
description: Événement déclenché lors de la tentative de requête HTTP.
title: Objet WebResourceRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 79cff0d8fd68e3b5747008f343b5b46fb8093013
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564622"
---
# Objet WebResourceRequestedEvent

Événement déclenché lors de la tentative de requête HTTP.

## Propriétés

### args

Informations sur la demande de ressource. Il s’agit d’un [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).

Cette propriété est en lecture seule.

```js
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```

#### Valeur de propriété
Tapez: **tout**

