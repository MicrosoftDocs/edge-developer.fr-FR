---
description: Obtient le jeu de données interne sur JsrtContext.
title: Fonction JsGetContextData | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: f5d7e446-267a-4a80-a427-6e1b95a3391b
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8f5f70a9c36fea355792050c1a2a810bca2d07b3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233099"
---
# JsGetContextData Function

Obtient le jeu de données interne sur JsrtContext.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextData(  
  _In_ JsContextRef context,  
  _Out_ void **data  
);  
```  
  
#### Paramètres  
 `context`  
 Contexte à partir duquel obtenir les données.  
  
 `data`  
 Pointeur vers les données où les données seront renvoyées.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
