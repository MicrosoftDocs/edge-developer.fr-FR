---
description: Crée une valeur numérique à partir d’une valeur double.
title: Fonction JsDoubleToNumber | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDoubleToNumber
helpviewer_keywords:
- JsDoubleToNumber function
ms.assetid: 43eb2ee1-2789-4302-954e-c4087e1ee786
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d3385633f41c2e20c43ca865eaeec763b6ff7f43
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233176"
---
# JsDoubleToNumber Function

Crée une valeur numérique à partir d’une `double` valeur.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsDoubleToNumber(  
   _In_ double doubleValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### Paramètres  
 `doubleValue`  
 La `double` valeur à convertir en nombre.  
  
 `value`  
 Nouvelle valeur du numéro.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
