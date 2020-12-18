---
description: Crée un nouvel objet d’erreur SyntaxError JavaScript.
title: Fonction JsCreateSyntaxError | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateSyntaxError
helpviewer_keywords:
- JsCreateSyntaxError function
ms.assetid: 839845fc-60c4-4ffc-bfcc-fd7a8f06126f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7d6534bfa2b59cb2f6ab68c231d7a97c84876d62
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233329"
---
# JsCreateSyntaxError Function

Crée un nouvel objet d’erreur SyntaxError JavaScript.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSyntaxError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### Paramètres  
 `message`  
 Message de l’objet d’erreur.  
  
 `error`  
 Nouvel objet d’erreur.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
