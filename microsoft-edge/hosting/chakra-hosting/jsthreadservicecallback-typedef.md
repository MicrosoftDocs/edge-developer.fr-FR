---
description: Un rappel de service de thread.
title: JsThreadServiceCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5eb9f2986c79db024f01f4d22050f79c9689400c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565135"
---
# JsThreadServiceCallback typedef
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
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)