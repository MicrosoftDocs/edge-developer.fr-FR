---
description: Obtient la valeur du `null` contexte de script actuel.
title: Fonction JsGetNullValue | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetNullValue
helpviewer_keywords:
- JsGetNullValue function
ms.assetid: 132a1496-8dfe-4d3c-a8f8-389f5b0b50d2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 31e1ba19f9f27e75f0166238d98390e2c4a26c24
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232803"
---
# JsGetNullValue Function

Obtient la valeur du `null` contexte de script actuel.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetNullValue(  
   _Out_ JsValueRef *nullValue  
);  
```  
  
#### Paramètres  
 `nullValue`  
 `null`Valeur.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
