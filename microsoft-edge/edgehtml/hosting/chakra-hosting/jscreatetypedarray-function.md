---
description: Crée un objet de tableau typé JavaScript.
title: Fonction JsCreateTypedArray | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 937a2a91-6f5f-4aaa-a018-d3089702bf36
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 62f62296d81dafe6515f69a990e33ff5c00730e1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233328"
---
# JsCreateTypedArray Function

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
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
