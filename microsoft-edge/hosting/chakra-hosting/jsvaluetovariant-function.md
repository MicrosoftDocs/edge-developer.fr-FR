---
description: Initialise la valeur transmise en `VARIANT` tant que projection d’une valeur JavaScript.
title: Fonction JsValueToVariant | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d8748fddcc149cf09fbd46ad3ad489cd66200b71
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565128"
---
# Fonction JsValueToVariant
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
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)