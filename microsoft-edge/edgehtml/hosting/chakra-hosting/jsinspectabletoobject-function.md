---
description: Crée une valeur JavaScript qui est une projection du `IInspectable` pointeur transmis.
title: Fonction JsInspectableToObject | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dd0ad567-2ba8-4a63-bee4-2c6ff5ce9fa9
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5d3d91b38c9db5de2eb8fb02526f6072f0f5147
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233358"
---
# JsInspectableToObject Function

Crée une valeur JavaScript qui est une projection du `IInspectable` pointeur transmis.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsInspectableToObject(  
        _In_ IInspectable  *inspectable,  
        _Out_ JsValueRef *value  
);  
```  
  
#### Paramètres  
 `inspectable`  
 A `IInspectable` à projeter.  
  
 `value`  
 Valeur JavaScript qui est une projection de la `IInspectable` .  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 La valeur projetée peut être utilisée par le script pour appeler un objet WinRT. Les hôtes sont chargés d’appliquer les règles de thread COM.  
  
 Nécessite un contexte de script actif.  
  
 Cette API est uniquement prise en charge en mode EdgeHTML.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
