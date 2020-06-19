---
description: Contient des informations de renvoi sur la navigation
title: Objet NavigationEventWithReferrer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 72c8a213f632e9e74145de9c34b949adf074cd22
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752125"
---
# Objet NavigationEventWithReferrer  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Objet qui représente un événement déclenché lorsque la navigation est lancée et que la navigation contient un referer.  

## Propriétés  

### Referer

URI (Uniform Resource Identifier) de la page du [WebView](../webview.md) demandant la navigation.  

Cette propriété est en lecture seule.  

#### Valeur de propriété  

Type: **DOMString**  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

### uri  

URI (Uniform Resource Identifier) de la destination de la navigation.  

Cette propriété est en lecture seule.  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### Valeur de propriété  

Type: **DOMString**  
