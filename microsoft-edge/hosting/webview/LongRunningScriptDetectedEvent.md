---
description: ''
title: Objet LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 5fe90495b83ab8f95ee594d3400c8c1a26f0547e
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752150"
---
# Objet LongRunningScriptDetectedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Fournit des informations pour [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).  

## Propriétés  

### executionTime  

Obtient le nombre de millisecondes pendant lesquelles l’élément [WebView](../webview.md) a exécuté un script de longue durée.  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### Valeur de propriété  

Type: **long**  

### stopPageScriptExecution  

Arrête l’exécution d’un script longue dans l’élément [WebView](../webview.md) .  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### Valeur de propriété  

Type: **booléen**  
