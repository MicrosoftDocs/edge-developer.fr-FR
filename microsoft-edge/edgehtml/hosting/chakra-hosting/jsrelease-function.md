---
description: Libère une référence à un objet nettoyé.
title: Fonction JsRelease | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRelease
helpviewer_keywords:
- JsRelease function
ms.assetid: 8714fd0b-5b66-48e0-927e-7b93af6cde7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 46552a03dc56a10b1d258d8c33da1c533f38464a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232956"
---
# JsRelease Function

Libère une référence à un objet nettoyé.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsRelease(  
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
 Supprime une référence à une `JsRef` poignée créée par `JsAddRef` .  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
