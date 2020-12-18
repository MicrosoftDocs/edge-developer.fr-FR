---
description: Le rappel JsRT qui doit être appelé avec le contexte transmis au `JsProjectionEnqueueCallback` thread approprié.
title: JsProjectionCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 211325b536dc84340974b02973f1de9d5749a60a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233303"
---
# Typedef JsProjectionCallback

Le rappel JsRT qui doit être appelé avec le contexte transmis au `JsProjectionEnqueueCallback` thread approprié.  
  
## Syntaxe  
  
```cpp  
typedef void (CALLBACK *JsProjectionCallback)(  
  _In_ JsProjectionCallbackContext jsContext  
);  
```  
  
#### Paramètres  
 `jsContext`  
 Nécessite l’appel `JsSetProjectionEnqueueCallback` pour recevoir des rappels.  
  
## Remarques  
 Cette API est uniquement prise en charge en mode EdgeHTML.  
  
## Conditions requises  
 jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
