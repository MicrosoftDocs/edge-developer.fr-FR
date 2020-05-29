---
description: Définit les propriétés indexées d’un objet sur des données externes. Les données externes seront utilisées comme magasin back pour les propriétés indexées de l’objet et consultées comme un tableau typé.
title: Fonction JsSetIndexedPropertiesToExternalData | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: cee2d86d-ed42-4acb-86ef-95a67e63d0d6
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c1aed6e194b1dc1c35f403626a7b6c02a7752ffb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566242"
---
# Fonction JsSetIndexedPropertiesToExternalData
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
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)