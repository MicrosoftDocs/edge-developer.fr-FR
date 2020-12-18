---
description: Obtient les propriétés fréquemment utilisées d’un tableau typé.
title: Fonction JsGetTypedArrayInfo | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fdc9a05a2aebdabfd0c8e95c848d3bd5f97e580a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233341"
---
# JsGetTypedArrayInfo Function

Obtient les propriétés fréquemment utilisées d’un tableau typé.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayInfo(  
  _In_ JsValueRef typedArray,  
  _Out_opt_ JsTypedArrayType *arrayType,  
  _Out_opt_ JsValueRef *arrayBuffer,  
  _Out_opt_ unsigned int *byteOffset,  
  _Out_opt_ unsigned int *byteLength  
);  
  
```  
  
#### Paramètres  
 `typedArray`  
 Instance de tableau typé.  
  
 `arrayType`  
 Type du tableau.  
  
 `arrayBuffer`  
 `ArrayBuffer`Magasin du tableau.  
  
 `byteOffset`  
 Décalage en octets du début de arrayBuffer référencé par le tableau.  
  
 `byteLength`  
 Nombre d’octets dans le tableau.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
