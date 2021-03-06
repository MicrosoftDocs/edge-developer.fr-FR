---
description: Objet LongRunningScriptDetectedEvent
title: Objet LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: webview, applications Windows 10, uwp, edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5f5eb3230e46ee2cd7926b21f6526e512a7a0322
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397939"
---
# <a name="longrunningscriptdetectedevent-object"></a>Objet LongRunningScriptDetectedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Fournit des informations [pour MSWebViewLongRunningScriptDetected](../webview/index.md#mswebviewlongrunningscriptdetected).  

## <a name="properties"></a>Propriétés  

### <a name="executiontime"></a>executionTime  

Obtient le nombre de millisecondes pendant combien de millisecondes l’élément [webview](../webview/index.md) a exécuté un script de longue durée.  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### <a name="property-value"></a>Valeur de la propriété  

Type : **long**  

### <a name="stoppagescriptexecution"></a>stopPageScriptExecution  

Arrête l’exécution d’un script de longue durée dans [l’élément webview.](../webview/index.md)  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### <a name="property-value"></a>Valeur de la propriété  

Type : **Boolean**  
