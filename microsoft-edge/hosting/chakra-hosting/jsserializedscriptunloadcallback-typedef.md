---
description: Appelé par le runtime lorsque toutes les ressources associées à l’exécution du script sont terminées. L’appelant doit libérer la source en cas de chargement, le code d’octet et le contexte pour le moment.
title: JsSerializedScriptUnloadCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c3da27af18ebc7a1913980a865d926bac6a29d11
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751939"
---
# Typedef JsSerializedScriptUnloadCallback
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