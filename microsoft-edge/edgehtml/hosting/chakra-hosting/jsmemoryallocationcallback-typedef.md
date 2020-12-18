---
description: Routine de rappel implémentée par l’utilisateur pour les événements d’allocation de mémoire.
title: JsMemoryAllocationCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 22b5cc0fe5a2c8b49f71c91d28f95ba29af37849
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232974"
---
# Typedef JsMemoryAllocationCallback

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
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
