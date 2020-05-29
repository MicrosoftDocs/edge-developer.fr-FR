---
description: Crée un `ArrayBuffer` objet JavaScript pour accéder à la mémoire externe.
title: Fonction JsCreateExternalArrayBuffer | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 376eedda18393436d9dce340753586bf32599b21
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565233"
---
# Fonction JsCreateExternalArrayBuffer
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
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)