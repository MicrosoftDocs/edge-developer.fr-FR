---
description: Définit les propriétés indexées d’un objet sur des données externes. Les données externes seront utilisées comme magasin back pour les propriétés indexées de l’objet et consultées comme un tableau typé.
title: Fonction JsSetIndexedPropertiesToExternalData | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: cee2d86d-ed42-4acb-86ef-95a67e63d0d6
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fa0eba3659c20066913cd42a0a18dd5ffe5f857f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232960"
---
# JsSetIndexedPropertiesToExternalData Function

Définit les propriétés indexées d’un objet sur des données externes. Les données externes seront utilisées comme magasin back pour les propriétés indexées de l’objet et consultées comme un tableau typé.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedPropertiesToExternalData(  
   _In_ JsValueRef object,  
   _In_ void* data,  
   _In_ JsTypedArrayType arrayType,  
   _In_ unsigned int elementLength  
);  
```  
  
#### Paramètres  
 `object`  
 Objet sur lequel travailler.  
  
 `data`  
 Données externes à utiliser en tant que magasin back pour les propriétés indexées de l’objet.  
  
 `arrayType`  
 Le type d’élément de tableau dans les données externes.  
  
 `elementLength`  
 Nombre d’éléments de tableau de données externes.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
 Cette API est uniquement prise en charge en mode EdgeHTML.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
