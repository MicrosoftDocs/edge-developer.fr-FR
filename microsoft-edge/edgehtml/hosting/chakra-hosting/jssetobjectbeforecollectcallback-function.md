---
description: Définit une fonction de rappel qui est appelée par le runtime avant le nettoyage de la mémoire d’un objet.
title: Fonction JsSetObjectBeforeCollectCallback | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: ea2cbd94-d8b0-4fa9-a4a1-c75a4e338eaf
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4689184dccaf6bc9f98eeacda5f5a4b91a927d40
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232961"
---
# JsSetObjectBeforeCollectCallback Function

Définit une fonction de rappel qui est appelée par le runtime avant le nettoyage de la mémoire d’un objet.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetObjectBeforeCollectCallback(  
   _In_ JsRef ref,  
   _In_opt_ void *callbackState,  
   _In_ JsObjectBeforeCollectCallback objectBeforeCollectCallback  
);  
```  
  
#### Paramètres  
 `ref`  
 Objet pour lequel inscrire le rappel.  
  
 `callbackState`  
 État fourni par l’utilisateur qui sera renvoyé au rappel.  
  
 `objectBeforeCollectCallback`  
 Fonction de rappel définie. Utilisez la valeur null pour effacer le rappel enregistré précédemment.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Le rappel est appelé sur le thread d’exécution du runtime actuel, donc l’exécution est bloquée jusqu’à ce que le rappel se termine.  
  
 Cette API est uniquement prise en charge en mode EdgeHTML.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
