---
description: Récupère le pointeur de chaîne d’une valeur de chaîne.
title: Fonction JsStringToPointer | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStringToPointer
helpviewer_keywords:
- JsStringToPointer function
ms.assetid: c7aa7a09-489d-4435-8f8a-aeb62f8875ae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1f5997894c4ea479378a323b230492dde28ab177
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566137"
---
# Fonction JsStringToPointer
Récupère le pointeur de chaîne d’une valeur de chaîne.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsStringToPointer(  
   _In_ JsValueRef value,  
   _Outptr_result_buffer_(*stringLength) const wchar_t **stringValue,  
   _Out_ size_t *stringLength  
);  
```  
  
#### Paramètres  
 `value`  
 Valeur de chaîne à convertir en pointeur de chaîne.  
  
 `stringValue`  
 Pointeur de chaîne.  
  
 `stringLength`  
 Longueur de la chaîne.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Cette fonction récupère le pointeur de chaîne d’une valeur de chaîne. Il échouera avec `JsErrorInvalidArgument` si le type de la valeur n’est pas String. La durée de vie de la chaîne renvoyée est identique à la durée de vie de la valeur dont elle provient, mais le pointeur de chaîne n’est pas considéré comme une référence à la valeur (et donc elle ne sera pas récupérée par le biais du suivi).  
  
 Nécessite un contexte de script actif.  
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)