---
description: Crée une nouvelle fonction JavaScript avec Name.
title: Fonction JsCreateNamedFunction | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 72f40d06-ab82-4fed-a632-68af6b4126c2
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b54add359422a9312a0ded641051fd04585f3d7e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233114"
---
# JsCreateNamedFunction Function

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
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
