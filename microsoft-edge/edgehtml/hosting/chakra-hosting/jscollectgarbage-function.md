---
description: Effectue un nettoyage de la mémoire complet.
title: Fonction JsCollectGarbage | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCollectGarbage
helpviewer_keywords:
- JsCollectGarbage function
ms.assetid: 995c79a5-6e18-45be-81ff-2a5d3348edb8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c551ddf119ec0aa349fcd756f6001d92dbbb0faa
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232992"
---
# JsCollectGarbage Function

Effectue un nettoyage de la mémoire complet.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsCollectGarbage(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### Paramètres  
 `runtime`  
 Runtime dans lequel le nettoyage de la mémoire sera effectué.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
