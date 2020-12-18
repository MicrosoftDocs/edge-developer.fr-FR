---
description: Le type JavaScript d’un JsValueRef.
title: Énumération JsValueType | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueType
helpviewer_keywords:
- JsValueType enumeration
ms.assetid: 6645e723-e554-41fc-b622-ab54ee044b3d
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 840afcde86d4df80490d463921a74c73e42ddfc2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233124"
---
# Énumération JsValueType

Le type JavaScript d’un JsValueRef.  
  
## Syntaxe  
  
```cpp  
enum JsValueType {  
    JsUndefined      = 0,  
    JsNull           = 1,  
    JsNumber         = 2,  
    JsString         = 3,  
    JsBoolean        = 4,  
    JsObject         = 5,  
    JsFunction       = 6,  
    JsError          = 7,  
    JsArray          = 8,  
    JsSymbol         = 9,  
    JsArrayBuffer    = 10,  
    JsTypedArray     = 11,  
    JsDataView       = 12,  
};  
```  
  
## Ses  
  
### Doubl  
  
|Nom|Description|  
|----------|-----------------|  
|`JsUndefined`|La valeur est la `undefined` valeur.|  
|`JsNull`|La valeur est la `null` valeur.|  
|`JsNumber`|La valeur est une valeur numérique JavaScript.|  
|`JsString`|La valeur est une valeur de chaîne JavaScript.|  
|`JsBoolean`|La valeur est une valeur booléenne JavaScript.|  
|`JsObject`|La valeur est une valeur d’objet JavaScript.|  
|`JsFunction`|La valeur est une valeur d’objet fonction JavaScript.|  
|`JsError`|La valeur est une valeur d’objet d’erreur JavaScript.|  
|`JsArray`|La valeur est une valeur d’objet de tableau JavaScript.|  
|`JsSymbol`|La valeur est une valeur de symbole JavaScript.<br /><br /> Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.|  
|`JsArrayBuffer`|La valeur est une `ArrayBuffer` valeur d’objet JavaScript.<br /><br /> Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.|  
|`JsTypedArray`|La valeur est une valeur d’objet de tableau typé JavaScript.<br /><br /> Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.|  
|`JsDataView`|La valeur est une `DataView` valeur d’objet JavaScript.<br /><br /> Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.|  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
