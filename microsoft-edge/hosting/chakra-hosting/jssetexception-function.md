---
description: Définit l’exécution du contexte actuel sur un état d’exception.
title: Fonction JsSetException | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 75d2895a725c622a0b46887d10154c3a0c56c7e9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566248"
---
# Fonction JsSetException
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
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)