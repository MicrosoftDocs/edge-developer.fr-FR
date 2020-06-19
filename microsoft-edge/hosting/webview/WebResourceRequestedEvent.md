---
description: Événement déclenché lors de la tentative de requête HTTP.
title: Objet WebResourceRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 3d2bb54cc5d60aec5391f0e3fdd427c8ba8a3dab
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751981"
---
# Objet WebResourceRequestedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Événement déclenché lors de la tentative de requête HTTP.  

## Propriétés  

### args  

Informations sur la demande de ressource.  Il s’agit d’un [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).  

Cette propriété est en lecture seule.  

```javascript
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```  

#### Valeur de propriété  

Tapez: **tout**  
