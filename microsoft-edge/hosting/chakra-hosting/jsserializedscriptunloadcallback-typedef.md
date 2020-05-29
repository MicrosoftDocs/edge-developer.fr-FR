---
description: Appelé par le runtime lorsque toutes les ressources associées à l’exécution du script sont terminées. L’appelant doit libérer la source en cas de chargement, le code d’octet et le contexte pour le moment.
title: JsSerializedScriptUnloadCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9555b3fd8c14c9629d17c13592e3c78a78be150e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566254"
---
# JsSerializedScriptUnloadCallback typedef
Appelé par le runtime lorsque toutes les ressources associées à l’exécution du script sont terminées. L’appelant doit libérer la source en cas de chargement, le code d’octet et le contexte pour le moment.  
  
## Syntaxe  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### Paramètres  
 `sourceContext`  
 Le contexte transmis à `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback` .  
  
## Remarques  
  
> [!WARNING]
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)