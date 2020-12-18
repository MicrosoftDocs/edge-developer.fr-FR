---
description: Définit l’exécution du contexte actuel sur un état d’exception.
title: Fonction JsSetException | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2c2e3840d2a831db23a525c5d8854b9b2fcfb8c9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233173"
---
# JsSetException Function

Définit l’exécution du contexte actuel sur un état d’exception.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetException(  
   _In_ JsValueRef exception  
);  
```  
  
#### Paramètres  
 `exception`  
 Exception JavaScript à définir pour le runtime du contexte actuel.  
  
## Valeur renvoyée  
 `JsNoError` Si le moteur a été défini comme état d’exception, il est contraire d’un code d’échec.  
  
## Remarques  
 Si le runtime du contexte actuel est déjà dans un état d’exception, cette API retourne `JsErrorInExceptionState` .  
  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
