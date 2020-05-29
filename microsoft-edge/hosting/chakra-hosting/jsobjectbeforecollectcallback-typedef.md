---
description: Rappel appelé avant la collecte d’un objet.
title: JsObjectBeforeCollectCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: f21a064a-579f-44cb-9d21-76b62e8c18f5
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 27bbd1aed72cc751397ac4e6734f107612653b66
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565147"
---
# JsObjectBeforeCollectCallback typedef
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
  
## Configuration requise  
 jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)