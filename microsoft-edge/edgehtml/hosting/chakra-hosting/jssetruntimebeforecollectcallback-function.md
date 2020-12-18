---
description: 'Définit une fonction de rappel appelée par le runtime avant le nettoyage de la mémoire. '
title: Fonction JsSetRuntimeBeforeCollectCallback | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeBeforeCollectCallback
helpviewer_keywords:
- JsSetRuntimeBeforeCollectCallback function
ms.assetid: 7b2fb911-6007-4ed9-a307-66cefe590ea4
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 94ad29fcfb778fc630d70664f917c6b5c2637dde
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232962"
---
# JsSetRuntimeBeforeCollectCallback Function

Définit une fonction de rappel appelée par le runtime avant le nettoyage de la mémoire.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeBeforeCollectCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsBeforeCollectCallback beforeCollectCallback  
);  
```  
  
#### Paramètres  
 `runtime`  
 Le runtime pour lequel inscrire le rappel d’allocation.  
  
 `callbackState`  
 État fourni par l’utilisateur qui sera transmis au rappel.  
  
 `beforeCollectCallback`  
 Fonction de rappel définie.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Le rappel est appelé sur le thread d’exécution du runtime actuel, donc l’exécution est bloquée jusqu’à ce que le rappel se termine.  
  
 Le rappel peut être utilisé par des hôtes pour préparer le nettoyage de la mémoire. Par exemple, en libérant les références inutiles sur les objets Chakra.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
