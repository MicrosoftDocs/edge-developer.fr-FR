---
description: Rappel de continuation de promesse.
title: JsPromiseContinuationCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da121d186cd9d0ab1a9770be08c9a92b52cf3366
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233536"
---
# Typedef JsPromiseContinuationCallback

Rappel de continuation de promesse.  
  
## Syntaxe  
  
```cpp  
typedef void (CALLBACK *JsPromiseContinuationCallback)(  
  _In_ JsValueRef task,  
  _In_opt_ void *callbackState  
);  
```  
  
#### Paramètres  
 `task`  
  `callbackState`  
  
## Remarques  
 L’hôte peut spécifier un rappel de continuation de promesse en `JsSetPromiseContinuationCallback` . Si un script crée une tâche à exécuter par la suite, le rappel de continuation à la suite sera appelé par la tâche et la tâche doit être placée dans une file d’attente FIFO pour être exécutée à la fin de l’exécution du script actuel.  
  
 Cette API est uniquement prise en charge en mode EdgeHTML.  
  
## Conditions requises  
 jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
