---
description: Renvoie une valeur indiquant si l’exécution du script est désactivée dans le Runtime.
title: Fonction JsIsRuntimeExecutionDisabled | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6968a31c9acab70589fe58c86cc566e631778c3c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565156"
---
# Fonction JsIsRuntimeExecutionDisabled
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
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)