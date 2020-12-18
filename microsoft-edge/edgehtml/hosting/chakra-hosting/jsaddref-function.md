---
description: Ajoute une référence à un objet nettoyé.
title: Fonction JsAddRef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsAddRef
helpviewer_keywords:
- JsAddRef function
ms.assetid: a7f3ed49-6a86-489a-abdf-c99428e79cae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fd397dbfeacafdf12728ef0ca2a98d97405f6592
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233008"
---
# JsAddRef Function

Ajoute une référence à un objet nettoyé.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsAddRef(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### Paramètres  
 `ref`  
 Objet auquel ajouter une référence.  
  
 `count`  
 Le nouveau nombre de références (peut être transmis à null).  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Pour cela, il suffit d’appeler sur des `JsRef` Handles qui n’ont pas pu être stockés quelque part dans la pile. L’appel `JsAddRef` vérifie que l’objet auquel le `JsRef` fait référence ne sera pas libéré tant qu' `JsRelease` il n’est pas appelé.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
