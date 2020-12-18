---
description: Retourne l’exception qui a entraîné l’exécution du contexte actuel dans l’état d’exception et réinitialise l’état d’exception pour le Runtime.
title: Fonction JsGetAndClearException | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetAndClearException
helpviewer_keywords:
- JsGetAndClearException function
ms.assetid: 6aec8a88-41ee-47f6-b5f4-32f3cae6bb7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb296ea351d0466a856d5ac020550ebacc254ac9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233100"
---
# JsGetAndClearException Function

Retourne l’exception qui a entraîné l’exécution du contexte actuel dans l’état d’exception et réinitialise l’état d’exception pour le Runtime.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetAndClearException(  
   _Out_ JsValueRef *exception  
);  
```  
  
#### Paramètres  
 `exception`  
 Exception pour le runtime du contexte actuel.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Si le runtime du contexte actuel ne se trouve pas dans un état d’exception, cette API renverra `JsErrorInvalidArgument` . Si le runtime est désactivé, il renverra une exception indiquant que le script a été arrêté, mais il n’effacera pas l’exception (l’exception sera effacée si le runtime est réactivé à l’aide de `JsEnableRuntimeExecution` ).  
  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
