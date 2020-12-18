---
description: Un rappel du finaliseur.
title: JsFinalizeCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: aa7a0269-b9d4-4717-97ac-8da7eb6ced15
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 794edbb3a61c8c213c0908740ed0a867488a2c6d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233107"
---
# Typedef JsFinalizeCallback

Un rappel du finaliseur.  
  
## Syntaxe  
  
```cpp  
typedef void (CALLBACK *JsFinalizeCallback)(  
   _In_opt_ void *data  
);  
```  
  
#### Paramètres  
 data  
 Données externes transmises lors de la création de l’objet finalisé.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
