---
description: Obtient le stockage de mémoire sous-jacent utilisé par un DataView.
title: Fonction JsGetDataViewStorage | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 7c2180e0-51d5-4cc8-ad21-8bf29ff7c583
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 54f8a91b6dea1e0997ad31d6585ea741fde8ba99
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565194"
---
# Fonction JsGetDataViewStorage
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
  
## Configuration requise  
 **En-tête:** jsrt. h  
  
## Voir aussi  
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)