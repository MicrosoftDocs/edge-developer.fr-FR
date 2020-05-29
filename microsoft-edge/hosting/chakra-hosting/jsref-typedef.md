---
description: Référence à un objet possédé par le récupérateur de mémoire Chakra.
title: JsRef typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 6aafc39f-6b9c-457f-8bf0-48831bffe9b8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f5ce1ada67a4530ba57345b90c0b7deba6954c7c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566273"
---
# JsRef typedef
Référence à un objet possédé par le récupérateur de mémoire Chakra.  
  
## Syntaxe  
  
```cpp  
typedef void *JsRef;  
```  
  
## Remarques  
 Un Runtime Chakra effectue automatiquement le suivi des références JsRef tant que celles-ci sont stockées dans des variables locales ou dans des paramètres (c’est-à-dire sur la pile). Le stockage d’un JsRef dans un autre emplacement que sur la pile nécessite l’appel de JsAddRef et JsRelease pour gérer la durée de vie de l’objet, sinon le nettoyage de la mémoire peut libérer l’objet alors qu’il est toujours en cours d’utilisation.  
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)