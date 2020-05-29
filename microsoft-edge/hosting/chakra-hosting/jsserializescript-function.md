---
description: Sérialise un script analysé dans une mémoire tampon qu’il est possible de réutiliser.
title: Fonction JsSerializeScript | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSerializeScript
helpviewer_keywords:
- JsSerializeScript function
ms.assetid: ca42c194-e1c1-407d-b542-b9d494e3ac4e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1b45067fddb7ea4dff02e527e460db1270011c61
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566252"
---
# Fonction JsSerializeScript
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
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)