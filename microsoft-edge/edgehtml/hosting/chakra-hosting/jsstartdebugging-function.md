---
description: Démarre le débogage dans le contexte actuel.
title: Fonction JsStartDebugging | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStartDebugging
helpviewer_keywords:
- JsStartDebugging function
ms.assetid: c48ba02d-6d47-466f-a970-02f087d525f3
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9685779911db8e3045986682b66d13e38c70fe8d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233469"
---
# JsStartDebugging Function

Démarre le débogage dans le contexte actuel.  
  
## Syntaxe  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsStartDebugging();  
  
// Legacy mode signature  
STDAPI_(JsErrorCode)  JsStartDebugging(  
   _In_ IDebugApplication *debugApplication  
);  
```  
  
#### Paramètres  
 `debugApplication`  
 Application de débogage à utiliser pour le débogage.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 L’hôte doit s’assurer qu’il `CoInitializeEx` est appelé `COINIT_MULTITHREADED` ou `COINIT_APARTMENTTHREADED` au moins une fois avant d’utiliser cette API.  
  
 Le `debugApplication` paramètre n’est pas pris en charge en mode Microsoft Edge. Pour plus d’informations sur l’utilisation de cette API dans le mode Microsoft Edge, consultez [ciblage des moteurs Microsoft Edge et hérités](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
