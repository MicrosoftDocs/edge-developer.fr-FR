---
description: Initialise la valeur transmise en `VARIANT` tant que projection d’une valeur JavaScript.
title: Fonction JsValueToVariant | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f383f2d8bc3aab70b4a361b370698cd71cb714d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233126"
---
# JsValueToVariant Function

Initialise la valeur transmise en `VARIANT` tant que projection d’une valeur JavaScript.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsValueToVariant(  
   _In_ JsValueRef object,  
   _Out_ VARIANT *variant  
);  
```  
  
#### Paramètres  
 `object`  
 Valeur JavaScript à projeter en tant que `VARIANT` .  
  
 `variant`  
 Pointeur vers un `VARIANT` struct qui sera initialisé comme une projection.  
  
## Valeur renvoyée  
  
## Remarques  
 La projection `VARIANT` peut être utilisée par les clients com Automation pour appeler l’objet JavaScript projeté.  
  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
