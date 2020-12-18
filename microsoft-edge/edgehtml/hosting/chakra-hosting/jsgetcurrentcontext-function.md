---
description: Obtient le contexte de script actuel sur le thread.
title: Fonction JsGetCurrentContext | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetCurrentContext
helpviewer_keywords:
- JsGetCurrentContext function
ms.assetid: dd5fe0fa-d1e5-4af6-809e-e655a27519b5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a43b9a6d4413ef1dc1b66321d6078aef84a0645f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233226"
---
# JsGetCurrentContext Function

Obtient le contexte de script actuel sur le thread.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetCurrentContext(  
   _Out_ JsContextRef *currentContext  
);  
```  
  
#### Paramètres  
 `currentContext`  
 Contexte de script actuel sur le thread, null s’il n’y a aucun contexte de script actuel.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
