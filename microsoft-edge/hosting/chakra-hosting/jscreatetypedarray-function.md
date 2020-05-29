---
description: Crée un objet de tableau typé JavaScript.
title: Fonction JsCreateTypedArray | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 937a2a91-6f5f-4aaa-a018-d3089702bf36
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 57c5d15d76bf8b3ff29d10f7500fe41b3e959f68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565214"
---
# Fonction JsCreateTypedArray
Crée un objet de tableau typé JavaScript.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypedArray(  
   _In_ JsTypedArrayType arrayType,  
   _In_ JsValueRef baseArray,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int elementLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Paramètres  
 `arrayType`  
 Type du tableau à créer.  
  
 `baseArray`  
 Tableau de base du nouveau tableau. Utilisez ce `JS_INVALID_REFERENCE` numéro si aucune matrice de base n’est utilisée.  
  
 `byteOffset`  
 Décalage en octets du début de `baseArray` () du `ArrayBuffer` tableau tapé pour le résultat à référencer. Applicable uniquement lorsqu' `baseArray` il s’agit d’un `ArrayBuffer` objet. Doit être zéro dans le cas présent.  
  
 `elementLength`  
 Nombre d’éléments de la matrice. Applicable uniquement lors de la création d’un tableau typé sans `baseArray` ( `baseArray` is `JS_INVALID_REFERENCE` ) ou lorsqu' `baseArray` il s’agit d’un `ArrayBuffer` objet. Doit être zéro dans le cas présent.  
  
 `result`  
 Nouvel objet de tableau typé.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Il `baseArray` peut s’agir d’un, d’un `ArrayBuffer` autre tableau typé ou d’un code JavaScript `Array` . Le tableau typé retourné utilise le `baseArray` cas échéant `ArrayBuffer` , ou crée et utilise une copie du tableau source sous-jacent.  
  
 Nécessite un contexte de script actif.  
  
 Cette API est uniquement prise en charge en mode Microsoft Edge.  
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)