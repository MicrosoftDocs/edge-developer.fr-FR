---
description: Un rappel de service de thread.
title: JsThreadServiceCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5f1fe416e158e9524bdd1caab847977a5dd21b8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233128"
---
# Typedef JsThreadServiceCallback

Un rappel de service de thread.  
  
## Syntaxe  
  
```cpp  
typedef bool (CALLBACK *JsThreadServiceCallback)(  
   _In_ JsBackgroundWorkItemCallback callback,  
   _In_opt_ void *callbackData  
);  
```  
  
#### Paramètres  
 rappeler  
 Rappel pour l’élément de tâche en arrière-plan.  
  
 callbackData  
 L’argument Data à transmettre au rappel.  
  
## Remarques  
 L’hôte peut spécifier un service de thread en arrière-plan lors de l’appel de JsCreateRuntime. Si ce paramètre est spécifié, les éléments de tâche en arrière-plan sont transmis à l’hôte à l’aide de ce rappel. L’hôte doit commencer immédiatement exécuter l’élément de tâche en arrière-plan et retourner true ou false, et le runtime doit gérer l’élément de bureau en thread.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
