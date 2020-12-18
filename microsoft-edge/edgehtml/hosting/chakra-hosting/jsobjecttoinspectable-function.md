---
description: Détourne un objet JavaScript en `IInspectable` pointeur.
title: Fonction JsObjectToInspectable | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 1d15b0b8-516f-4fc6-95aa-2ddd65f8ab75
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0d818f798805e2afad4dc87b308258464d31bf92
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233305"
---
# JsObjectToInspectable Function

Détourne un objet JavaScript en `IInspectable` pointeur.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsObjectToInspectable(  
   _In_ JsValueRef value,  
   _Out_ IInspectable  **inspectable  
);  
```  
  
#### Paramètres  
 `value`  
 Valeur JavaScript devant être projetée `IInspectable` .  
  
 `inspectable`  
 `IInspectable`Valeur de l’objet.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Les hôtes sont chargés d’appliquer les règles de thread COM.  
  
 Nécessite un contexte de script actif.  
  
 Cette API est uniquement prise en charge en mode EdgeHTML.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
