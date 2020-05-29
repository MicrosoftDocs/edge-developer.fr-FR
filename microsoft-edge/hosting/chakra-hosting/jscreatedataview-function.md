---
description: Crée un `DataView` objet JavaScript.
title: Fonction JsCreateDataView | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1bf237458e8561b7070e4f3f0d4a14050f028375
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565239"
---
# Fonction JsCreateDataView
Crée un `DataView` objet JavaScript.  
  
## Syntaxe  
  
```cpp  
JsErrorCode  JsCreateDataView(  
   _In_ JsValueRef arrayBuffer,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Paramètres  
 `arrayBuffer`  
 Objet existant `ArrayBuffer` à utiliser comme espace de stockage de l’objet de résultat `DataView` .  
  
 `byteOffset`  
 Le décalage en octets entre le début du `arrayBuffer` résultat `DataView` et la référence.  
  
 `byteLength`  
 Nombre d’octets dans ArrayBuffer pour le DataView de résultats à référencer.  
  
 `result`  
 Nouvel objet DataView.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
 Cette API est uniquement prise en charge en mode Microsoft Edge.  
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)