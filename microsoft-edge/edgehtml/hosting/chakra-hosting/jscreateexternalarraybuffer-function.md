---
description: Crée un `ArrayBuffer` objet JavaScript pour accéder à la mémoire externe.
title: Fonction JsCreateExternalArrayBuffer | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 78c0d3c8b298876358f247c86a488b6f10e52c6d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233365"
---
# JsCreateExternalArrayBuffer Function

Crée un `ArrayBuffer` objet JavaScript pour accéder à la mémoire externe.
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalArrayBuffer(  
  _Pre_maybenull_ _Pre_writable_byte_size_(byteLength) void *data,  
  _In_ unsigned int byteLength,  
  _In_opt_ JsFinalizeCallback finalizeCallback,  
  _In_opt_ void *callbackState,  
  _Out_ JsValueRef *result  
);  
  
```  
  
#### Paramètres  
 `data`  
 Pointeur vers la mémoire externe.  
  
 `byteLength`  
 Nombre d’octets de la mémoire externe.  
  
 `finalizeCallback`  
 Rappel lors de la finalisation de l’objet. Est susceptible d’être null.  
  
 `callbackState`  
 État fourni par l’utilisateur qui sera renvoyé à finalizeCallback.  
  
 `result`  
 Nouvel `ArrayBuffer` objet.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
