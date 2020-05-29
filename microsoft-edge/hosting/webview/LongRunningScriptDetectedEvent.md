---
description: ''
title: Objet LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 6cf7af656531eea5046f7af44d4d43ff224d0f08
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565109"
---
# Objet LongRunningScriptDetectedEvent

Fournit des informations pour [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).

## Propriétés

### executionTime

Obtient le nombre de millisecondes pendant lesquelles l’élément [WebView](../webview.md) a exécuté un script de longue durée.

```js
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```

#### Valeur de propriété
Type: **long**

### stopPageScriptExecution
Arrête l’exécution d’un script longue dans l’élément [WebView](../webview.md) .

```js
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```

#### Valeur de propriété
Type: **booléen**