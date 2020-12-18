---
description: Place la propriété d’un objet.
title: Fonction JsSetProperty | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetProperty
helpviewer_keywords:
- JsSetProperty function
ms.assetid: 2c36bebf-ec86-425c-8131-2dd75fd30f40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 29c3e04fc240bd63fc755c6727752d053b94484d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233186"
---
# JsSetProperty Function

Place la propriété d’un objet.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef value,  
   _In_ bool useStrictRules  
);  
```  
  
#### Paramètres  
 `object`  
 Objet qui contient la propriété.  
  
 `propertyId`  
 ID de la propriété.  
  
 `value`  
 Nouvelle valeur de la propriété.  
  
 `useStrictRules`  
 Le jeu de propriétés doit suivre des règles en mode strict.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
