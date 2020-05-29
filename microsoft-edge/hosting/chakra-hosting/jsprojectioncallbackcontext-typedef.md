---
description: Le contexte transmis au rappel d’application, JsProjectionEnqueueCallback, de JsRT, puis de nouveau transmis à JsRT dans le rappel fourni, `JsProjectionCallback` par l’application sur le thread approprié.
title: JsProjectionCallbackContext typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 58d4c74da13ae0dd269f3c101bbf3d2b95e77732
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565145"
---
# JsProjectionCallbackContext typedef
Le contexte transmis au rappel d’application, JsProjectionEnqueueCallback, de JsRT, puis de nouveau transmis à JsRT dans le rappel fourni, `JsProjectionCallback` par l’application sur le thread approprié.  
  
## Syntaxe  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## Remarques  
 Nécessite l’appel `JsSetProjectionEnqueueCallback` pour recevoir des rappels.  
  
 Cette API est uniquement prise en charge en mode EdgeHTML.  
  
## Configuration requise  
 jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)