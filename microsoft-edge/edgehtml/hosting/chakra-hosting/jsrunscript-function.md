---
description: Exécute un script.
title: Fonction JsRunScript | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRunScript
helpviewer_keywords:
- JsRunScript function
ms.assetid: 8d6b8c9a-af3a-4e21-a330-5a6b535423a3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d61771991e1d22a9d71a928d785390b814a992a8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233472"
---
# JsRunScript Function

Exécute un script.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsRunScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Paramètres  
 `script`  
 Script à exécuter.  
  
 `sourceContext`  
 Un cookie identifiant le script qui peut être utilisé par les contextes de script déboguables.  
  
 `sourceUrl`  
 Emplacement à partir duquel provient le script.  
  
 `result`  
 Le résultat du script, le cas échéant. Ce paramètre peut être null.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
