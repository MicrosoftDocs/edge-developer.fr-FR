---
description: Effectue un `instanceof` test d’opérateur JavaScript.
title: Fonction JsInstanceOf | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 94399a62-b996-4fd2-82ce-1c26e7a4da08
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d8aec1d4512fe937d1fd48aa6f3e88294bf9850c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233356"
---
# JsInstanceOf Function

Effectue un `instanceof` test d’opérateur JavaScript.  
  
## Syntaxe  
  
```cpp  
JsInstanceOf(   
  _In_ JsValueRef object,  
  _In_ JsValueRef constructor,  
  _Out_ bool *result  
);  
  
```  
  
#### Paramètres  
 `object`  
 Objet à tester.  
  
 `constructor`  
 Fonction Constructor à tester.  
  
 `result`  
 La valeur de la propriété «Object instanceof Constructor».  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
