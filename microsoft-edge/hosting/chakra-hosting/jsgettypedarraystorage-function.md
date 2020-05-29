---
description: Obtient le stockage de mémoire sous-jacent utilisé par un tableau typé.
title: Fonction JsGetTypedArrayStorage | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 52e4ac5f-cc71-456d-95de-a48f7327503d
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f03414d64fa819ac464217c8362d02e866d45296
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566310"
---
# Fonction JsGetTypedArrayStorage
Obtient le stockage de mémoire sous-jacent utilisé par un tableau typé.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayStorage(  
   _In_ JsValueRef typedArray,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength,  
   _Out_opt_ JsTypedArrayType *arrayType,  
   _Out_opt_ int *elementSize  
);  
```  
  
#### Paramètres  
 `typedArray`  
 Instance de tableau typé.  
  
 `buffer`  
 Tampon du tableau. La durée de vie de la mémoire tampon renvoyée est identique à la durée de vie de la matrice. Le pointeur de tampon n’est pas considéré comme une référence au tableau à des fins de nettoyage de la mémoire.  
  
 `bufferLength`  
 Nombre d’octets de la mémoire tampon.  
  
 `arrayType`  
 Type du tableau.  
  
 `elementSize`  
 Taille d’un élément du tableau.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
 Cette API est uniquement prise en charge en mode Microsoft Edge.  
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)