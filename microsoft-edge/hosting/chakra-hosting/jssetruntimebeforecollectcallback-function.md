---
description: 'Définit une fonction de rappel appelée par le runtime avant le nettoyage de la mémoire. '
title: Fonction JsSetRuntimeBeforeCollectCallback | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeBeforeCollectCallback
helpviewer_keywords:
- JsSetRuntimeBeforeCollectCallback function
ms.assetid: 7b2fb911-6007-4ed9-a307-66cefe590ea4
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 31aefd28698c14a6fe17421a990a7c8b120876bf
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566142"
---
# Fonction JsSetRuntimeBeforeCollectCallback
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
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)