---
description: Rappel de fonction.
title: JsNativeFunction typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c0b73a11d3a0b2ed0867ef001f3c29c5643132a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565153"
---
# JsNativeFunction typedef
Rappel de fonction.  
  
## Syntaxe  
  
```cpp  
typedef _Ret_maybenull_ JsValueRef (CALLBACK * JsNativeFunction)(  
   _In_ JsValueRef callee,  
   _In_ bool isConstructCall,  
   _In_ JsValueRef *arguments,  
   _In_ unsigned short argumentCount  
);  
```  
  
#### Paramètres  
 l ʼ  
 `Function`Objet qui représente la fonction appelée.  
  
 isConstructCall  
 Indique s’il s’agit d’un appel régulier ou d’un nouvel appel.  
  
 arguments  
 Les arguments de l’appel.  
  
 argumentCount  
 Nombre d’arguments.  
  
## Valeur de propriété/valeur de retour  
 Le résultat de l’appel, le cas échéant.  
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)