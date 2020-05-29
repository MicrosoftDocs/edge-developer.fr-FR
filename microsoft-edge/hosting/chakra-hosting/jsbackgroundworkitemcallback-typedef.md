---
description: Rappel d’élément de tâche en arrière-plan.
title: JsBackgroundWorkItemCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9bc1e5687d92d7286e1e6d4387bd6b69d95ceb68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565269"
---
# JsBackgroundWorkItemCallback typedef
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
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)