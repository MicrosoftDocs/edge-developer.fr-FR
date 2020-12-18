---
description: Handle vers un Runtime Chakra.
title: JsRuntimeHandle typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ab08243505b9699fe07ca2e80f7294adf9eb78ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232959"
---
# Typedef JsRuntimeHandle

Handle vers un Runtime Chakra.  
  
## Syntaxe  
  
```cpp  
typedef void *JsRuntimeHandle;  
```  
  
## Remarques  
 Chaque Runtime Chakra possède son propre moteur d’exécution indépendant, son compilateur JIT et son segment de mémoire récupéré. Ainsi, chaque Runtime est complètement isolé des autres runtimes.  
  
 Les Runtime peuvent être utilisés sur n’importe quel thread, mais un seul thread peut appeler à tout moment dans le Runtime.  
  
> [!WARNING]
>  Contrairement à d’autres références d’objet dans l’API d’hébergement chakra, il n’y a pas de nettoyage de la mémoire car il contient le tas récupéré par le garbage collector. Un Runtime restera disponible tant que JsDisposeRuntime n’est pas appelé.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
