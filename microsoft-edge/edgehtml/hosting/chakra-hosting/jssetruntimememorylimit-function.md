---
description: Définit la limite de mémoire actuelle pour un Runtime.
title: Fonction JsSetRuntimeMemoryLimit | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryLimit
helpviewer_keywords:
- JsSetRuntimeMemoryLimit function
ms.assetid: 74feb31f-19f6-43e3-b117-0694c59ac593
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1c31d8bbbec4be22fc1af09e546ad4c95f8ec2bd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232784"
---
# JsSetRuntimeMemoryLimit Function

Définit la limite de mémoire actuelle pour un Runtime.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _In_ size_t memoryLimit  
);  
```  
  
#### Paramètres  
 `runtime`  
 Le runtime dont la limite de mémoire doit être définie.  
  
 `memoryLimit`  
 La nouvelle limite de mémoire d’exécution, en octets ou-1 pour aucune limite de mémoire.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Une limite de mémoire entraîne une opération qui dépasse la limite pour l’échec de l’exécution d’une erreur «mémoire insuffisante». La définition de la limite de mémoire d’un Runtime sur-1 signifie que le runtime n’a pas de limite de mémoire. Par défaut, les nouveaux Runtime ne possèdent aucune limite de mémoire. Si la nouvelle limite de mémoire est supérieure à l’utilisation actuelle, l’appel aboutit et toutes les attributions ultérieures dans ce Runtime échouent jusqu’à ce que l’utilisation de la mémoire du runtime reste en dessous de la limite.  
  
 Il est toujours possible de définir la limite de mémoire d’un Runtime, que le runtime soit actif ou non sur un autre thread.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
