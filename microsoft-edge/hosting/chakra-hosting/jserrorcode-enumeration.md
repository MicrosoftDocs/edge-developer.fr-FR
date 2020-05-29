---
description: Code d’erreur retourné par une API d’hébergement Chakra.
title: Énumération JsErrorCode | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsErrorCode
helpviewer_keywords:
- JsErrorCode enumeration
ms.assetid: 4902f3f3-47a5-4e74-9c29-f96eeecbcda9
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e3d1a319872ac69b2acaf19997f3c38f9c04597b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566333"
---
# Énumération JsErrorCode
Code d’erreur retourné par une API d’hébergement Chakra.  
  
## Syntaxe  
  
```cpp  
enum JsErrorCode : unsigned int;  
```  
  
## Ses  
  
### Doubl  
  
|Nom|Description|  
|----------|-----------------|  
|`JsErrorAlreadyDebuggingContext`|Le contexte ne peut pas être placé dans un état de débogage, car il est déjà dans un état de débogage.|  
|`JsErrorAlreadyProfilingContext`|Le contexte ne peut pas démarrer le profilage, car il est déjà en cours de profilage.|  
|`JsErrorArgumentNotObject`|Une API d’hébergement qui fonctionne sur des valeurs d’objet a été appelée avec une valeur non Object.|  
|`JsErrorBadSerializedScript`|Un script sérialisé incorrect a été utilisé ou le script sérialisé a été sérialisé par une autre version du moteur Chakra.|  
|`JsErrorCannotDisableExecution`|Le runtime ne prend pas en charge l’interruption du script fiable.|  
|`JsErrorCannotSerializeDebugScript`|Les scripts ne peuvent pas être sérialisés dans les contextes de débogage.|  
|`JsErrorCategoryEngine`|Catégories d’erreurs liées à des erreurs se produisant dans le moteur lui-même.|  
|`JsErrorCategoryFatal`|Catégorie d’erreurs irrécupérable et signifiant échec du moteur.|  
|`JsErrorCategoryScript`|Catégories d’erreurs liées aux erreurs dans un script.|  
|`JsErrorCategoryUsage`|Catégories d’erreurs liées à l’utilisation incorrecte de l’API elle-même.|  
|`JsErrorFatal`|Une erreur irrécupérable s’est produite dans le moteur.|  
|`JsErrorHeapEnumInProgress`|Une énumération de tas est actuellement en cours dans le contexte de script.|  
|`JsErrorIdleNotEnabled`|Notification inactif fournie lorsque l’hôte n’a pas activé le traitement inactif.|  
|`JsErrorInDisabledState`|Le runtime est dans un état désactivé.|  
|`JsErrorInExceptionState`|Le moteur est dans un état d’exception et aucune API ne peut être appelée tant que l’exception n’est pas supprimée.|  
|`JsErrorInObjectBeforeCollectCallback`|L’opération n’est pas prise en charge dans un objet avant la collecte du rappel.<br /><br /> Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.|  
|`JsErrorInProfileCallback`|Un contexte de script se trouve au milieu d’un rappel de profil.|  
|`JsErrorInThreadServiceCallback`|Un rappel de service de thread est actuellement en cours.|  
|`JsErrorInvalidArgument`|Un argument d’une API d’hébergement n’est pas valide.|  
|`JsErrorNoCurrentContext`|L’API d’hébergement exige qu’un contexte soit à jour, mais qu’il n’y ait aucun contexte actuel.|  
|`JsErrorNotImplemented`|Une API d’hébergement n’est pas encore implémentée.|  
|`JsErrorNullArgument`|Un argument pour une API d’hébergement a la valeur null dans un contexte pour lequel la valeur NULL n’est pas autorisée.|  
|`JsErrorObjectNotInspectable`|L’objet ne peut pas être ajusté au `IInspectable` pointeur.<br /><br /> Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.|  
|`JsErrorOutOfMemory`|Mémoire insuffisante pour le moteur Chakra.|  
|`JsErrorPropertyNotSymbol`|Une API d’hébergement qui fonctionne sur les ID de propriété de symbole mais qui a été appelée avec un ID de propriété sans symbole. Le code d’erreur est retourné par `JsGetSymbolFromPropertyId` si la fonction est appelée avec un ID de propriété sans symbole.<br /><br /> Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.|  
|`JsErrorPropertyNotString`|API d’hébergement qui fonctionne sur les ID de propriété de chaîne, mais qui a été appelée avec un ID de propriété autre qu’une chaîne. Le code d’erreur est retourné par existing `JsGetPropertyNamefromId` si la fonction est appelée avec un ID de propriété autre qu’une chaîne.<br /><br /> Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.|  
|`JsErrorRuntimeInUse`|Un Runtime toujours en cours d’utilisation ne peut pas être supprimé.|  
|`JsErrorScriptCompile`|JavaScript n’a pas réussi à compiler.|  
|`JsErrorScriptEvalDisabled`|Un script a été arrêté car il a essayé d’utiliser `eval` ou `function` et eval a été désactivé.|  
|`JsErrorScriptException`|Une exception JavaScript s’est produite lors de l’exécution d’un script.|  
|`JsErrorScriptTerminated`|Un script a été arrêté en raison d’une demande de suspension d’un Runtime.|  
|`JsErrorWrongRuntime`|Une API d’hébergement a été appelée avec un objet créé sur un autre Runtime JavaScript.|  
|`JsErrorWrongThread`|Une API d’hébergement a été appelée sur le thread incorrect.|  
|`JsNoError`|Code d’erreur de réussite.|  
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)