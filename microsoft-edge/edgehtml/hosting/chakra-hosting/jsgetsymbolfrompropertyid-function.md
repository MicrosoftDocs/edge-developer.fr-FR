---
description: Obtient le symbole associé à l’ID de propriété.
title: Fonction JsGetSymbolFromPropertyId | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0e822cb4-ba9e-44df-bf3a-fae97c354daa
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 472253aea228ca0374c42d99710a7a7ab528184c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233543"
---
# JsGetSymbolFromPropertyId Function

Obtient le symbole associé à l’ID de propriété.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetSymbolFromPropertyId(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *symbol  
);  
```  
  
#### Paramètres  
 `propertyId`  
 ID de propriété pour obtenir le symbole.  
  
 `symbol`  
 Symbole associé à l’ID de propriété.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
 Cette API est uniquement prise en charge en mode Microsoft Edge.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
