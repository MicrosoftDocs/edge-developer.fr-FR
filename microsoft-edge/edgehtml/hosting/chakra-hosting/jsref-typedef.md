---
description: Référence à un objet possédé par le récupérateur de mémoire Chakra.
title: JsRef typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 6aafc39f-6b9c-457f-8bf0-48831bffe9b8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 69d13472b15b5d448908b5dafb2e3d7dc0ace7e4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232800"
---
# Typedef JsRef

Référence à un objet possédé par le récupérateur de mémoire Chakra.  
  
## Syntaxe  
  
```cpp  
typedef void *JsRef;  
```  
  
## Remarques  
 Un Runtime Chakra effectue automatiquement le suivi des références JsRef tant que celles-ci sont stockées dans des variables locales ou dans des paramètres (c’est-à-dire sur la pile). Le stockage d’un JsRef dans un autre emplacement que sur la pile nécessite l’appel de JsAddRef et JsRelease pour gérer la durée de vie de l’objet, sinon le nettoyage de la mémoire peut libérer l’objet alors qu’il est toujours en cours d’utilisation.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
