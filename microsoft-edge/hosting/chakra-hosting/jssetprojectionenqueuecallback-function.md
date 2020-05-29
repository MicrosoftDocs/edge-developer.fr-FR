---
description: Définit le rappel à utiliser pour rappeler une fin de projection au thread des appelants requis.
title: Fonction JsSetProjectionEnqueueCallback | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: c751ccef-20d2-4d41-9568-1c54adf47cdf
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 02da0238360b0dc6fff9bb86c9f5ab04d1ba7112
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566235"
---
# Fonction JsSetProjectionEnqueueCallback
Définit le rappel à utiliser pour rappeler une fin de projection au thread des appelants requis.  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProjectionEnqueueCallback(  
   _In_ JsProjectionEnqueueCallback projectionEnqueueCallback,  
   _In_opt_ void *projectionEnqueueContext);  
  
```  
  
#### Paramètres  
 `projectionEnqueueContext`  
 Rappel qui sera appelé chaque fois qu’une achèvement de projection se produit sur un thread en arrière-plan.  
  
 `callbackState`  
 Contexte de l’application fourni à `projectionEnqueueContext` .  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
 L’appel doit être issu d’un autre thread COM ou d’un autre thread du même MTA.  
  
 Cette API est uniquement prise en charge en mode EdgeHTML.  
  
> [!CAUTION]
>  PInvoke n’est pas actuellement pris en charge pour cette API.  
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)