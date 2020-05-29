---
description: Récupère la `int` valeur d’une valeur numérique.
title: Fonction JsNumberToInt | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: cf4c8cb42c737cfb9efee5422fe6bb3c1389cbfd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566289"
---
# Fonction JsNumberToInt
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
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)