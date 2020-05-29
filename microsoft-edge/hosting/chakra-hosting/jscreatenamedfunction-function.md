---
description: Crée une nouvelle fonction JavaScript avec Name.
title: Fonction JsCreateNamedFunction | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 72f40d06-ab82-4fed-a632-68af6b4126c2
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d963fe196b8e56394e22501ed3898a0d887a3d3b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565229"
---
# Fonction JsCreateNamedFunction
Crée une nouvelle fonction JavaScript avec Name.
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateNamedFunction(  
   _In_ JsValueRef name,  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### Paramètres  
 `name`  
 Nom de cette fonction qui sera utilisé à des fins de diagnostic et de stringification.  
  
 `nativeFunction`  
 Méthode à appeler lors de l’appel de la fonction.  
  
 `callbackState`  
 État fourni par l’utilisateur qui sera transmis au rappel.  
  
 `function`  
 Nouvel objet fonction.  
  
## Valeur renvoyée  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
 Cette API est uniquement prise en charge en mode Microsoft Edge.  
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)