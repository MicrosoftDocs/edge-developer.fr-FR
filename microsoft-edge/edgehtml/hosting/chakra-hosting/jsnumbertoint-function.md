---
description: Récupère la `int` valeur d’une valeur numérique.
title: Fonction JsNumberToInt | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 928be9a7cc5cd3e26e8b8df99af1e08a6c50209c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233315"
---
# JsNumberToInt Function

Récupère la `int` valeur d’une valeur numérique.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToInt(  
      _In_ JsValueRef value,  
      _Out_ int *intValue  
);  
```  
  
#### Paramètres  
 `value`  
 Valeur numérique à convertir en `int` valeur.  
  
 `intValue`  
 `int`Valeur.  
  
## Valeur renvoyée  
  
## Remarques  
 Cette fonction récupère la valeur d’une valeur numérique et la convertit en une `int` valeur. Il échouera avec `JsErrorInvalidArgument` si le type de la valeur n’est pas numérique.  
  
 Nécessite un contexte de script actif.  
  
 Cette API est uniquement prise en charge en mode EdgeHTML.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
