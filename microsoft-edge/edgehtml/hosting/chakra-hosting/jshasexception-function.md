---
description: Détermine si le runtime du contexte actuel est dans un état d’exception.
title: Fonction JsHasException | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasException
helpviewer_keywords:
- JsHasException function
ms.assetid: ac7da3ce-c746-4154-bbb8-bcb0859a8d5b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4f4abbd6c69a6b2b6414dae2f1de3a2acf21cc32
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232841"
---
# JsHasException Function

Détermine si le runtime du contexte actuel est dans un état d’exception.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsHasException(  
   _Out_ bool *hasException  
);  
```  
  
#### Paramètres  
 `hasException`  
 Si le runtime du contexte actuel est dans l’état de l’exception.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Si un appel dans le runtime génère une exception (soit suite à l’exécution d’un script, soit en raison d’un échec de conversion, par exemple), le runtime est placé dans un «état d’exception». Tous les appels dans n’importe quel contexte créé par le runtime (à l’exception des API d’exception) échoueront `JsErrorInExceptionState` tant que l’exception n’aura pas été effacée.  
  
 Si le runtime du contexte actuel est dans l’état de l’exception lorsqu’un rappel est retourné dans le moteur, le moteur lèvera automatiquement l’exception.  
  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
