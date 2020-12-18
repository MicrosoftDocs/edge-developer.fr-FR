---
description: Rappel appelé avant la collecte d’un objet.
title: JsObjectBeforeCollectCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: f21a064a-579f-44cb-9d21-76b62e8c18f5
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4c24385ec5e15919719ffb0ae71c8adf39c1724c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233313"
---
# Typedef JsObjectBeforeCollectCallback

Rappel appelé avant la collecte d’un objet.  
  
## Syntaxe  
  
```cpp  
typedef void (CALLBACK *JsObjectBeforeCollectCallback)(  
  _In_ JsRef ref,  
  _In_opt_ void *callbackState  
);  
```  
  
#### Paramètres  
 `ref`  
 Objet à collecter.  
  
 `callbackState`  
 État transmis `JsSetObjectBeforeCollectCallback` .  
  
## Remarques  
 Cette API est uniquement prise en charge en mode EdgeHTML.  
  
## Conditions requises  
 jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
