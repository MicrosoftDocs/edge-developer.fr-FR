---
description: Rappel de fonction.
title: JsNativeFunction typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 891fe55f776e8519a5d3c187104b2bc326336482
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232797"
---
# Typedef JsNativeFunction

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
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
