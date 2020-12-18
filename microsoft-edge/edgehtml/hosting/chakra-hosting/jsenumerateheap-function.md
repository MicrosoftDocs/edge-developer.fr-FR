---
description: Énumère le tas du contexte actuel.
title: Fonction JsEnumerateHeap | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEnumerateHeap
helpviewer_keywords:
- JsEnumerateHeap function
ms.assetid: 3e518e0b-b959-4686-899c-83e6b1946c9d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bb76b28f24b769f71827e59be691188e34e9e1a3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233323"
---
# JsEnumerateHeap Function

Énumère le tas du contexte actuel.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsEnumerateHeap(  
   _Out_ IActiveScriptProfilerHeapEnum **enumerator  
);  
```  
  
#### Paramètres  
 `enumerator`  
 Énumérateur du tas.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Pendant l’énumération du tas, le contexte actuel ne peut pas être supprimé, et tous les appels de modification de l’état du contexte échouent jusqu’à ce que l’énumérateur du tas soit officialisé.  
  
 Nécessite un contexte de script actif.  
  
 Cette API est prise en charge dans les applications de bureau, mais n’est pas prise en charge dans les applications du Windows Store.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
