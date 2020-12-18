---
description: Définit une fonction de rappel de continuation de promesse qui est appelée par le contexte quand une tâche doit être mise en file d’attente pour exécution future.
title: Fonction JsSetPromiseContinuationCallback | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 6ef0faf4-1500-4bd9-aeca-c208492af8ea
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da928431f05831c95d5bc116dbd129de9cb5f3b4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233212"
---
# JsSetPromiseContinuationCallback Function

Définit une fonction de rappel de continuation de promesse qui est appelée par le contexte quand une tâche doit être mise en file d’attente pour exécution future.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPromiseContinuationCallback(  
   _In_ JsPromiseContinuationCallback promiseContinuationCallback,  
   _In_opt_ void *callbackState  
);  
```  
  
#### Paramètres  
 `promiseContinuationCallback`  
 Fonction de rappel définie.  
  
 `callbackState`  
 État fourni par l’utilisateur qui sera transmis au rappel.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
 Cette API est uniquement prise en charge en mode EdgeHTML.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
