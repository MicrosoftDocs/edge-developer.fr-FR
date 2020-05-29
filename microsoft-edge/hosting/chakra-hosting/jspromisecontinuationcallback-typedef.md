---
description: Rappel de continuation de promesse.
title: JsPromiseContinuationCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 023d88af5ff82056d8f57453e0a53b91b34565a6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565137"
---
# JsPromiseContinuationCallback typedef
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
  
## Configuration requise  
 jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)