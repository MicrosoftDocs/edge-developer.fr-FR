---
description: Définit le contexte de script actuel sur le thread.
title: Fonction JsSetCurrentContext | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetCurrentContext
helpviewer_keywords:
- JsSetCurrentContext function
ms.assetid: 603cc94c-6585-411b-89f9-c6f144e2aa30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 60ec1760c582f1f6771a5af64f59c4a77b1a43f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233134"
---
# JsSetCurrentContext Function

Définit le contexte de script actuel sur le thread.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetCurrentContext(  
   _In_ JsContextRef context  
);  
```  
  
#### Paramètres  
 `context`  
 Contexte de script pour rendre active.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  

## Exemple

```cpp
JsRuntimeHandle runtime;
JsContextRef context;

// Create a runtime.
JsCreateRuntime(JsRuntimeAttributeNone, nullptr, &runtime);

// Create an execution context.
JsCreateContext(runtime, &context);

// Now set the current execution context.
JsSetCurrentContext(context);
```

## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
