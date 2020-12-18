---
description: Crée un `ArrayBuffer` objet JavaScript.
title: Fonction JsCreateArrayBuffer | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c9e74184-7dd9-41a7-a1fe-9575e1701392
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3bee44d77f78bd35705211c598db78ab09000c71
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232973"
---
# JsCreateArrayBuffer Function

Crée un `ArrayBuffer` objet JavaScript.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArrayBuffer(  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Paramètres  
 `byteLength`  
 Nombre d’octets dans le ArrayBuffer.  
  
 `result`  
 Nouvel objet ArrayBuffer.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
 Cette API est uniquement prise en charge en mode Microsoft Edge.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
