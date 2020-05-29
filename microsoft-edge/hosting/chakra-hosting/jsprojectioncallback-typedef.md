---
description: Le rappel JsRT qui doit être appelé avec le contexte transmis au `JsProjectionEnqueueCallback` thread approprié.
title: JsProjectionCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b30f9a7dc4671896eeacecbf58ef88f0383e9e7e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565144"
---
# JsProjectionCallback typedef
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
  
## Configuration requise  
 jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)