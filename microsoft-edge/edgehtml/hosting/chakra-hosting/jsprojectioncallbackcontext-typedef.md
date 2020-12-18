---
description: Le contexte transmis au rappel d’application, JsProjectionEnqueueCallback, de JsRT, puis de nouveau transmis à JsRT dans le rappel fourni, `JsProjectionCallback` par l’application sur le thread approprié.
title: JsProjectionCallbackContext typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7742b0186a49e99f2738b81357b9e55cfe00042b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233299"
---
# Typedef JsProjectionCallbackContext

Le contexte transmis au rappel d’application, JsProjectionEnqueueCallback, de JsRT, puis de nouveau transmis à JsRT dans le rappel fourni, `JsProjectionCallback` par l’application sur le thread approprié.  
  
## Syntaxe  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## Remarques  
 Nécessite l’appel `JsSetProjectionEnqueueCallback` pour recevoir des rappels.  
  
 Cette API est uniquement prise en charge en mode EdgeHTML.  
  
## Conditions requises  
 jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
