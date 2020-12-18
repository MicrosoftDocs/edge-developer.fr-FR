---
description: Référence à un contexte de script.
title: JsContextRef typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c8a8fcbd67afb150d682cfc19321f0f13acfe3a6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232995"
---
# Typedef JsContextRef

Référence à un contexte de script.  
  
## Syntaxe  
  
```cpp  
typedef JsRef JsContextRef;  
```  
  
## Remarques  
 Chaque contexte de script contient son propre objet global, distinct de l’objet global dans d’autres contextes de script.  
  
 De nombreuses API d’hébergement Chakra requièrent un contexte de script «actif», qui peut être défini à l’aide de `JsSetCurrentContext` . Les API d’hébergement chakra qui nécessitent la définition d’un contexte actuel seront signalées explicitement dans leurs documents.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
