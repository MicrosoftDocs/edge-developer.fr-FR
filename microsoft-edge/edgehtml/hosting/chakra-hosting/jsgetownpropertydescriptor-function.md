---
description: Obtient un descripteur de propriété pour la propriété propre d’un objet.
title: Fonction JsGetOwnPropertyDescriptor | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyDescriptor
helpviewer_keywords:
- JsGetOwnPropertyDescriptor function
ms.assetid: 44c417ce-ab63-44eb-a0ab-19838e3ab34f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 05c7a58fa12d7ca8013c512f40031963ebc8ac18
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233171"
---
# JsGetOwnPropertyDescriptor Function

Obtient un descripteur de propriété pour la propriété propre d’un objet.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyDescriptor(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *propertyDescriptor  
);  
```  
  
#### Paramètres  
 `object`  
 Objet qui comporte la propriété.  
  
 `propertyId`  
 ID de la propriété.  
  
 `propertyDescriptor`  
 Le descripteur de propriété.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
