---
description: Type d’événement de rappel d’attribution.
title: Énumération JsMemoryEventType | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsMemoryEventType
helpviewer_keywords:
- JsMemoryEventType enumeration
ms.assetid: b4b176b6-b536-472e-8999-95b681a1df55
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e9833777ed8fe5a19fd2a1487715296279f7351
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565152"
---
# Énumération JsMemoryEventType
Type d’événement de rappel d’attribution.  
  
## Syntaxe  
  
```cpp  
enum JsMemoryEventType;  
```  
  
## Ses  
  
### Doubl  
  
|Nom|Description|  
|----------|-----------------|  
|`JsMemoryAllocate`|Indique une demande d’allocation de mémoire.|  
|`JsMemoryFailure`|Indique un événement d’allocation ayant échoué.|  
|`JsMemoryFree`|Indique un événement de libère de la mémoire.|  
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)