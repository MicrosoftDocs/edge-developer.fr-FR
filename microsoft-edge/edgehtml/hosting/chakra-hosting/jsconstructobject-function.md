---
description: Appelle une fonction en tant que constructeur.
title: Fonction JsConstructObject | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConstructObject
helpviewer_keywords:
- JsConstructObject function
ms.assetid: b07d2440-db55-4a6a-8376-56b40a8039a1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8dbb757456412e50efaf3a026d169e6b3612b6b1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232989"
---
# JsConstructObject Function

Appelle une fonction en tant que constructeur.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsConstructObject(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### Paramètres  
 `function`  
 Fonction pour appeler en tant que constructeur.  
  
 `arguments`  
 Les arguments de l’appel.  
  
 `argumentCount`  
 Nombre d’arguments passés à la fonction.  
  
 `result`  
 Valeur renvoyée à partir de l’appel de fonction.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
