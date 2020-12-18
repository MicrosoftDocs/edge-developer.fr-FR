---
description: Arrête le profilage dans le contexte actuel.
title: Fonction JsStopProfiling | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStopProfiling
helpviewer_keywords:
- JsStopProfiling function
ms.assetid: 3639c04f-a0f9-418b-be39-92f64b4e7ef8
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 02c42afda7e61d71b90a9a1a71aa71cc53584ff8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233167"
---
# JsStopProfiling Function

Arrête le profilage dans le contexte actuel.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsStopProfiling(  
   _In_ HRESULT reason  
);  
```  
  
#### Paramètres  
 `reason`  
 La raison pour laquelle vous arrêtez le profilage passe au rappel du profileur.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Ne renvoie pas d’erreur si le profil n’a pas commencé.  
  
 Nécessite un contexte de script actif.  
  
 Cette API est prise en charge dans les applications de bureau, mais n’est pas prise en charge dans les applications du Windows Store.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
