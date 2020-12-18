---
description: Rappel d’élément de tâche en arrière-plan.
title: JsBackgroundWorkItemCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d69306b334c2e0c9b27b96a5a417739ffdcd7dd7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233006"
---
# Typedef JsBackgroundWorkItemCallback

Rappel d’élément de tâche en arrière-plan.  
  
## Syntaxe  
  
```cpp  
typedef void (CALLBACK *JsBackgroundWorkItemCallback)(  
   _In_opt_ void *callbackData  
);  
```  
  
#### Paramètres  
 callbackData  
 L’argument Data est transmis au service de thread.  
  
## Remarques  
 Ce dernier est transmis au service de thread de l’hôte (si fourni) pour permettre à l’hôte d’appeler le rappel d’élément de tâche sur le thread d’arrière-plan de son choix.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
