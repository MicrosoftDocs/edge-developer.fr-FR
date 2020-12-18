---
description: Exécute un script sérialisé.
title: Fonction JsRunSerializedScript | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRunSerializedScript
helpviewer_keywords:
- JsRunSerializedScript function
ms.assetid: 3fd3f6f1-eb3e-4751-92a5-c93b1035f3b2
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 46f293d76bf0944c1cdedae917735c505798f4ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233471"
---
# JsRunSerializedScript Function

Exécute un script sérialisé.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Paramètres  
 `script`  
 Code source du script sérialisé.  
  
 `buffer`  
 Script sérialisé.  
  
 `sourceContext`  
 Un cookie identifiant le script qui peut être utilisé par les contextes de script déboguables.  
  
 `sourceUrl`  
 Emplacement à partir duquel provient le script.  
  
 `result`  
 Résultat de l’exécution du script, le cas échéant. Ce paramètre peut être null.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
 La mémoire tampon n’est pas conservée en mémoire par le moteur de script, de sorte que votre code doit rester actif tant qu’il peut être utilisé pour exécuter des scripts.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
