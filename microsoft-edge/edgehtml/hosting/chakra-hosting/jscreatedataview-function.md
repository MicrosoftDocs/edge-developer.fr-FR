---
description: Crée un `DataView` objet JavaScript.
title: Fonction JsCreateDataView | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1d6d170d53f3bfaf885713b6f3abca0b066f8c1d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232972"
---
# JsCreateDataView Function

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
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
