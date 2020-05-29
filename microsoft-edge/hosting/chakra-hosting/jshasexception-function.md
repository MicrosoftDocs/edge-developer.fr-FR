---
description: Détermine si le runtime du contexte actuel est dans un état d’exception.
title: Fonction JsHasException | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasException
helpviewer_keywords:
- JsHasException function
ms.assetid: ac7da3ce-c746-4154-bbb8-bcb0859a8d5b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 25ddb8f9cc407dd414a6cd2210c315eb4dd7b141
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566297"
---
# Fonction JsHasException
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
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)