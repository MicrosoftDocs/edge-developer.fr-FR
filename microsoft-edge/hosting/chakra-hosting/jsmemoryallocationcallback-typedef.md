---
description: Routine de rappel implémentée par l’utilisateur pour les événements d’allocation de mémoire.
title: JsMemoryAllocationCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b11b3d076c01dbfcae190fd665528323d6f8b987
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565155"
---
# JsMemoryAllocationCallback typedef
Routine de rappel implémentée par l’utilisateur pour les événements d’allocation de mémoire.  
  
## Syntaxe  
  
```cpp  
typedef bool (CALLBACK * JsMemoryAllocationCallback)(  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryEventType allocationEvent,  
   _In_ size_t allocationSize  
);  
```  
  
#### Paramètres  
 callbackState  
 État transmis à JsSetRuntimeMemoryAllocationCallback.  
  
 allocationEvent  
 Type d’événement d’allocation de type.  
  
 allocations  
 La taille de l’attribution.  
  
## Valeur de propriété/valeur de retour  
 Pour l’événement JsMemoryAllocate, la valeur true permet au runtime de continuer l’attribution. Le retour de la valeur false indique que la demande d’allocation est refusée. La valeur de retour est ignorée pour les autres événements d’allocation.  
  
## Remarques  
 Utilisez JsSetRuntimeMemoryAllocationCallback pour inscrire ce rappel.  
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)