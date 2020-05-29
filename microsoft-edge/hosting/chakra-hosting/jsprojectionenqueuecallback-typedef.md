---
description: Le rappel d’application qui est appelé par JsRT lorsqu’une API de projection est exécutée sur un thread différent de celui de l’original.
title: JsProjectionEnqueueCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 064a7d1077ae5222e44ab08ebe0592bb97b1f2af
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565143"
---
# JsProjectionEnqueueCallback typedef
Le rappel d’application qui est appelé par JsRT lorsqu’une API de projection est exécutée sur un thread différent de celui de l’original.  
  
## Syntaxe  
  
```cpp  
typedef void (CALLBACK *JsProjectionEnqueueCallback)(  
  _In_ JsProjectionCallback jsCallback,  
  _In_ JsProjectionCallbackContext jsContext,  
  _In_opt_ void *callbackState  
);  
```  
  
#### Paramètres  
 `jsCallback`  
 Rappel à appeler sur le thread d’origine.  
  
 `jsContext`  
 Contexte de l’application.  
  
 `callbackState`  
 Contexte JsRT qui doit être transmis `jsCallback` .  
  
## Remarques  
 Nécessite d’appeler JsSetProjectionEnqueueCallback pour recevoir des rappels.  
  
 Cette API est uniquement prise en charge en mode EdgeHTML.  
  
## Configuration requise  
 jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)