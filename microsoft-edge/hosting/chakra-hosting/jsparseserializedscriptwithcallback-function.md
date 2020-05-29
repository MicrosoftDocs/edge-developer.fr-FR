---
description: Analyse un script sérialisé et retourne une fonction qui représente le script. Offre la possibilité de charger les sources de scripts uniquement si vous en avez besoin.
title: Fonction JsParseSerializedScriptWithCallback | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 0a93ecfb-4b82-4a85-b24c-6816db2332ea
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ad6d635722f0b3fea8b19f8d16679b402d1fd56e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566280"
---
# Fonction JsParseSerializedScriptWithCallback
Analyse un script sérialisé et retourne une fonction qui représente le script. Offre la possibilité de charger les sources de scripts uniquement si vous en avez besoin.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_ JsValueRef * result  
);  
  
```  
  
#### Paramètres  
 `scriptLoadCallback`  
 Rappel appelé lorsque le code source du script doit être chargé.  
  
 `scriptUnloadCallback`  
 Rappel appelé lorsque le script sérialisé et le code source ne sont plus nécessaires.  
  
 `buffer`  
 Script sérialisé.  
  
 `sourceContext`  
 Un cookie identifiant le script qui peut être utilisé par les contextes de script déboguables.     Ce contexte est transmis à scriptLoadCallback et scriptUnloadCallback.  
  
 `sourceUrl`  
 Emplacement à partir duquel provient le script.  
  
 `result`  
 Fonction qui représente le code de script.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
  
> [!NOTE]
>  Cette API n’est pas encore disponible pour les applications du Windows Store.  
  
 Nécessite un contexte de script actif.  
  
 Le runtime sera maintenu sur la mémoire tampon jusqu’à ce que toutes les instances de toutes les fonctions créées à partir de la mémoire tampon soient récupérées par le garbage collector.  Il appelle alors scriptUnloadCallback pour indiquer à l’appelant qu’il est en sécurité.  
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)