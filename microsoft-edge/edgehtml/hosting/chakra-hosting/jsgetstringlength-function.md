---
description: Obtient la longueur d’une valeur de chaîne.
title: Fonction JsGetStringLength | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetStringLength
helpviewer_keywords:
- JsGetStringLength function
ms.assetid: e9f9f28c-e644-439c-aee5-7ce362f71347
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 10fd6be4bb839ccb9eb64c99931cdb474e3aa7a2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233544"
---
# JsGetStringLength Function

Obtient la longueur d’une valeur de chaîne.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetStringLength(  
   _In_ JsValueRef stringValue,  
   _Out_ int *length  
);  
```  
  
#### Paramètres  
 `stringValue`  
 Valeur de chaîne dont la longueur est égale à.  
  
 `length`  
 Longueur de la chaîne.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
