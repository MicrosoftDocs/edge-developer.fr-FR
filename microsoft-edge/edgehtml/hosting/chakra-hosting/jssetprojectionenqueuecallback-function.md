---
description: Définit le rappel à utiliser pour rappeler une fin de projection au thread des appelants requis.
title: Fonction JsSetProjectionEnqueueCallback | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c751ccef-20d2-4d41-9568-1c54adf47cdf
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7dfedfeb1df5a97159a211795a2dd072d239bb35
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232957"
---
# JsSetProjectionEnqueueCallback Function

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
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
