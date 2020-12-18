---
description: Indique au runtime d’effectuer tout traitement inactif qu’il doit effectuer.
title: Fonction JsIdle | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIdle
helpviewer_keywords:
- JsIdle function
ms.assetid: 372d1c62-8e19-4886-aa33-364cabc09bba
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ecba0aafb6b4dcccb4485c2956cae5ce4045355f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233487"
---
# JsIdle Function

Indique au runtime d’effectuer tout traitement inactif qu’il doit effectuer.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsIdle(  
   _Out_opt_ unsigned int *nextIdleTick  
);  
```  
  
#### Paramètres  
 `nextIdleTick`  
 La prochaine coche système lorsque le fonctionnement est plus inactif. Peut être null. Renvoie le nombre maximal de graduations s’il n’y a pas de tâches à venir.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Si le traitement inactif a été activé pour le runtime actuel, l’appel `JsIdle` informera le runtime actuel qu’il est inactif et que le runtime peut effectuer des tâches de nettoyage de la mémoire.  
  
 `JsIdle` peut également renvoyer le nombre de battements système jusqu’à ce que le runtime puisse y exécuter plus de tâches. Les appels `JsIdle` antérieurs à ce nombre de coches ne fonctionneront pas.  
  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
