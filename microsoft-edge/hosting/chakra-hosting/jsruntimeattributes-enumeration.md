---
description: 'Attributs d’un Runtime. '
title: Énumération JsRuntimeAttributes | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRuntimeAttributes
helpviewer_keywords:
- JsRuntimeAttributes enumeration
ms.assetid: f76d82e9-a695-4d6a-96c1-b3a4d27fed68
caps.latest.revision: 14
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9b8f6788f1de4988e3936701cfc742a564c92cfd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566258"
---
# Énumération JsRuntimeAttributes
Attributs d’un Runtime.  
  
## Syntaxe  
  
```cpp  
enum JsRuntimeAttributes;  
```  
  
## Ses  
  
### Doubl  
  
|Nom|Description|  
|----------|-----------------|  
|`JsRuntimeAttributeAllowScriptInterrupt`|Le Runtime doit prendre en charge l’interruption du script fiable. Cela augmente le nombre d’emplacements dans lesquels le runtime recherche une requête d’interruption de script au coût d’une petite quantité de performances d’exécution.|  
|`JsRuntimeAttributeDisableBackgroundWork`|Le runtime ne fonctionnera pas (par exemple, le nettoyage de la mémoire) sur les threads d’arrière-plan.|  
|`JsRuntimeAttributeDisableEval`|L’utilisation `eval` de ou du `function` constructeur lèvera une exception.|  
|`JsRuntimeAttributeDisableNativeCodeGeneration`|Runtime ne génère pas de code natif.|  
|`JsRuntimeAttributeEnableExperimentalFeatures`|Runtime active toutes les fonctionnalités expérimentales.|  
|`JsRuntimeAttributeEnableIdleProcessing`|L’hôte appelle alors le `JsIdle` traitement inactif. Dans le cas contraire, le runtime va gérer la mémoire de manière légèrement plus agressive.|  
|`JsRuntimeAttributeDispatchSetExceptionsToDebugger`|Les appels `JsSetException` sont également distribués à l’exception sur le débogueur de script (le cas échéant), ce qui donne au débogueur la possibilité de s’arrêter sur l’exception.|  
|`JsRuntimeAttributeNone`|Aucun attribut spécial.|  
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)