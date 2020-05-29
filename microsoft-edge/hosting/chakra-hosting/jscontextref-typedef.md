---
description: Référence à un contexte de script.
title: JsContextRef typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 80e4b5034079f4f0d26da070bd209aa41bf3475f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565256"
---
# JsContextRef typedef
Référence à un contexte de script.  
  
## Syntaxe  
  
```cpp  
typedef JsRef JsContextRef;  
```  
  
## Remarques  
 Chaque contexte de script contient son propre objet global, distinct de l’objet global dans d’autres contextes de script.  
  
 De nombreuses API d’hébergement Chakra requièrent un contexte de script «actif», qui peut être défini à l’aide de `JsSetCurrentContext` . Les API d’hébergement chakra qui nécessitent la définition d’un contexte actuel seront signalées explicitement dans leurs documents.  
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)