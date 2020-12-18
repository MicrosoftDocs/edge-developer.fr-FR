---
description: Interrompt l’exécution du script et arrête tout script en cours d’exécution dans le Runtime.
title: Fonction JsDisableRuntimeExecution | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisableRuntimeExecution
helpviewer_keywords:
- JsDisableRuntimeExecution function
ms.assetid: 4bd4670a-a9da-4f8c-b3fd-1fd366d915c3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6a08e6a7f89c724f8cf1a73afd97d2cb23c0334e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233177"
---
# JsDisableRuntimeExecution Function

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
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
