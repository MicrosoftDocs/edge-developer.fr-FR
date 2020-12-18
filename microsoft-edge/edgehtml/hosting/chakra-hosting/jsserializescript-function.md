---
description: Sérialise un script analysé dans une mémoire tampon qu’il est possible de réutiliser.
title: Fonction JsSerializeScript | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSerializeScript
helpviewer_keywords:
- JsSerializeScript function
ms.assetid: ca42c194-e1c1-407d-b542-b9d494e3ac4e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 236cf40c91256e999d5390acd395b1e97fe538ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233484"
---
# JsSerializeScript Function

Sérialise un script analysé dans une mémoire tampon qu’il est possible de réutiliser.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSerializeScript(  
   _In_z_ const wchar_t *script,  
   _Out_writes_to_opt_(*bufferSize,  
   *bufferSize) BYTE *buffer,  
   _Inout_ unsigned long *bufferSize  
);  
```  
  
#### Paramètres  
 `script`  
 Script à sérialiser.  
  
 `buffer`  
 Mémoire tampon dans laquelle placer le script sérialisé. Peut être null.  
  
 `bufferSize`  
 À l’entrée, la taille de la mémoire tampon, en octets; en sortie, la taille de la mémoire tampon, en octets, doit contenir le script sérialisé.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 `JsSerializeScript` analyse un script, puis stocke le formulaire analysé du script dans un format indépendant du Runtime. Le script sérialisé peut ensuite être désérialisé dans n’importe quel Runtime sans nécessiter de nouvelle analyse du script.  
  
 Nécessite un contexte de script actif.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
