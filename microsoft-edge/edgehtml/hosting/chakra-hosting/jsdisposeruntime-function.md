---
description: Supprime un Runtime.
title: Fonction JsDisposeRuntime | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisposeRuntime
helpviewer_keywords:
- JsDisposeRuntime function
ms.assetid: 0aefde3f-7250-48be-afc5-53ea85c12f30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8cff4578415cdf1aaa01b7203ce734cef9115301
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233178"
---
# JsDisposeRuntime Function

Supprime un Runtime.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsDisposeRuntime(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### Paramètres  
 `runtime`  
 Runtime à supprimer.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Une fois le runtime supprimé, toutes les ressources qu’il contient sont non valides et ne peuvent pas être utilisées. Si le runtime est actif (c’est-à-dire s’il a la valeur Current sur un thread particulier), il ne peut pas être supprimé.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
