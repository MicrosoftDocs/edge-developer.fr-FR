---
description: Interrompt l’exécution du script et arrête tout script en cours d’exécution dans le Runtime.
title: Fonction JsDisableRuntimeExecution | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDisableRuntimeExecution
helpviewer_keywords:
- JsDisableRuntimeExecution function
ms.assetid: 4bd4670a-a9da-4f8c-b3fd-1fd366d915c3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 575947d3038eaa136e9d6ae62507501bc768eabe
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565205"
---
# Fonction JsDisableRuntimeExecution
Interrompt l’exécution du script et arrête tout script en cours d’exécution dans le Runtime.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsDisableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### Paramètres  
 `runtime`  
 Exécution du Runtime.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Les appels vers un Runtime suspendu échouent jusqu’à ce qu' `JsEnableRuntimeExecution` il soit appelé.  
  
 Il n’est pas nécessaire d’appeler cette API sur le thread sur lequel le runtime est actif. Même si le runtime est défini comme étant suspendu, un script d’exécution ne peut pas être suspendu immédiatement. le script actif sera arrêté en utilisant une exception dès que possible.  
  
 Le fait de suspendre l’exécution dans un Runtime qui est déjà suspendu est un absence d’opération.  
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)