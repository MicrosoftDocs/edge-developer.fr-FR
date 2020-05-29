---
description: Handle vers un Runtime Chakra.
title: JsRuntimeHandle typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4ccdcf39ec6062db47e1b9de249d75c8804de405
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566256"
---
# JsRuntimeHandle typedef
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
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)