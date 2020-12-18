---
description: Le rappel d’application qui est appelé par JsRT lorsqu’une API de projection est exécutée sur un thread différent de celui de l’original.
title: JsProjectionEnqueueCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 47527d5e32076e40a82ab5452c2e0f624e8a2818
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233538"
---
# Typedef JsProjectionEnqueueCallback

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
  
## Conditions requises  
 jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
