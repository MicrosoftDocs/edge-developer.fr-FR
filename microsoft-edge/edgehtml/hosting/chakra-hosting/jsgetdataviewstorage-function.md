---
description: Obtient le stockage de mémoire sous-jacent utilisé par un DataView.
title: Fonction JsGetDataViewStorage | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 7c2180e0-51d5-4cc8-ad21-8bf29ff7c583
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55f357e4a94b1edbc417ebb14ab99db11083dff4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233222"
---
# JsGetDataViewStorage Function

Obtient le stockage de mémoire sous-jacent utilisé par a `DataView` .  
  
## Syntaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetDataViewStorage(  
   _In_ JsValueRef dataView,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### Paramètres  
 `dataView`  
 Instance DataView.  
  
 `buffer`  
 Tampon du DataView. La durée de vie de la mémoire tampon renvoyée est identique à celle du `DataView` . Le pointeur de tampon n’est pas compté en tant que référence à l' `DataView` objectif du nettoyage de la mémoire.  
  
 `bufferLength`  
 Nombre d’octets de la mémoire tampon.  
  
## Valeur renvoyée  
 Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.  
  
## Remarques  
 Nécessite un contexte de script actif.  
  
 Cette API est uniquement prise en charge en mode Microsoft Edge.  
  
## Conditions requises  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
