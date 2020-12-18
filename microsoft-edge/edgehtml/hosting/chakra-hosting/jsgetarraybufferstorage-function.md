---
description: Obtient le stockage de mémoire sous-jacent utilisé par un ArrayBuffer.
title: Fonction JsGetArrayBufferStorage | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 712ae298-36a9-47ef-b089-e51835c056bc
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 64b031a81506e68322759eff49da7467cac6f219
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233101"
---
# JsGetArrayBufferStorage Function

Obtient le stockage de mémoire sous-jacent utilisé par un `ArrayBuffer` .  
  
## Syntaxe  
  
```cpp  
JsErrorCode STDAPI_ JsGetArrayBufferStorage(  
   _In_ JsValueRef arrayBuffer,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### Paramètres  
 `arrayBuffer`  
 L’instance ArrayBuffer.  
  
 `buffer`  
 Le tampon de l’ArrayBuffer. La durée de vie de la mémoire tampon renvoyée est identique à celle du `ArrayBuffer` . Le pointeur de tampon n’est pas compté en tant que référence à l' `ArrayBuffer` objectif du nettoyage de la mémoire.  
  
 `bufferLength`  
 Nombre d’octets de la mémoire tampon.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
 Cette API est uniquement prise en charge en mode Microsoft Edge.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
