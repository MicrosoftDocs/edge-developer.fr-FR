---
description: Appelé par le runtime pour charger le code source du script sérialisé. L’appelant doit conserver le tampon de script valide jusqu’au `JsSerializedScriptUnloadCallback` .
title: JsSerializedScriptLoadSourceCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2bb30befc61003d20cdeaa293fd1fdfdc95b36f7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233535"
---
# Typedef JsSerializedScriptLoadSourceCallback

Appelé par le runtime pour charger le code source du script sérialisé. L’appelant doit conserver le tampon de script valide jusqu’au `JsSerializedScriptUnloadCallback` .  
  
## Syntaxe  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### Paramètres  
 `sourceContext`  
 Le contexte transmis à `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback` .  
  
 `scriptBuffer`  
 Le script renvoyé.  
  
## Remarques  
  
> [!WARNING]
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
