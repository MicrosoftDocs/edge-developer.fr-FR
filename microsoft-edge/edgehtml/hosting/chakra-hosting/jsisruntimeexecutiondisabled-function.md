---
description: Renvoie une valeur indiquant si l’exécution du script est désactivée dans le Runtime.
title: Fonction JsIsRuntimeExecutionDisabled | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0ce59c77525abdb2dd6cac71dde1378264395e79
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232798"
---
# JsIsRuntimeExecutionDisabled Function

Renvoie une valeur indiquant si l’exécution du script est désactivée dans le Runtime.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsIsRuntimeExecutionDisabled(    _In_ JsRuntimeHandle runtime,    _Out_ bool *isDisabled);  
```  
  
#### Paramètres  
 `runtime`  
 Spécifie le runtime pour vérifier si l’exécution est désactivée.  
  
 `isDisabled`  
 `true` dans le cas contraire, l’exécution est désactivée `false` .  
  
## Valeur renvoyée  
 `JsNoError` Si l’opération a réussi, le code d’erreur est contraire.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
