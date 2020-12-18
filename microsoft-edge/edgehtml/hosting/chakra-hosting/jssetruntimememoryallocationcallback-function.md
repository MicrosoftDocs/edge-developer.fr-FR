---
description: Définit un rappel d’allocation de mémoire pour le runtime spécifié.
title: Fonction JsSetRuntimeMemoryAllocationCallback | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryAllocationCallback
helpviewer_keywords:
- JsSetRuntimeMemoryAllocationCallback function
ms.assetid: 6aa7d58d-6456-4df1-815f-1ba36fb4ae14
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ee2abf36e14c26ac58b90d48a6115fd6502307c9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233132"
---
# JsSetRuntimeMemoryAllocationCallback Function

Définit un rappel d’allocation de mémoire pour le runtime spécifié.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryAllocationCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryAllocationCallback allocationCallback  
);  
```  
  
#### Paramètres  
 `runtime`  
 Le runtime pour lequel inscrire le rappel d’allocation.  
  
 `callbackState`  
 État fourni par l’utilisateur qui sera transmis au rappel.  
  
 `allocationCallback`  
 Rappel d’allocation de mémoire à appeler pour les événements d’allocation de mémoire.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 En inscrivant un rappel d’allocation de mémoire, le runtime peut rappeler l’hôte à chaque fois qu’il acquiert une mémoire ou libère de la mémoire, le système d’exploitation. La routine de rappel est appelée avant que le gestionnaire de mémoire Runtime alloue un bloc de mémoire. L’attribution sera refusée si le rappel retourne false. Le gestionnaire de mémoire Runtime appelle également la routine de rappel après la libération d’un bloc de mémoire, ainsi que les échecs de répartition.  
  
 Le rappel est appelé sur le thread d’exécution du runtime actuel, donc l’exécution est bloquée jusqu’à ce que le rappel se termine.  
  
 La valeur de retour du rappel n’est pas stockée; les attributions précédemment rejetées n’empêchent pas le runtime d’appeler de nouveau le rappel plus tard pour les nouvelles allocations de mémoire.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
