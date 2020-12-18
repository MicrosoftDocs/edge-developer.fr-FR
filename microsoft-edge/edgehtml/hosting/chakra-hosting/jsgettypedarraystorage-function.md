---
description: Obtient le stockage de mémoire sous-jacent utilisé par un tableau typé.
title: Fonction JsGetTypedArrayStorage | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 52e4ac5f-cc71-456d-95de-a48f7327503d
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 442727228433368de14bac528ea416fcc2a95fa8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232838"
---
# JsGetTypedArrayStorage Function

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
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
