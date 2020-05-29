---
description: Supprimez la valeur à l’index spécifié d’un objet.
title: Fonction JsDeleteIndexedProperty | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteIndexedProperty
helpviewer_keywords:
- JsDeleteIndexedProperty function
ms.assetid: cc876839-2ecd-41a8-82d0-c19b3de944e3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6148a9c59105749a78ece73578d4b840501c6ecc
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565206"
---
# <span data-ttu-id="77057-103">Fonction JsDeleteIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="77057-103">JsDeleteIndexedProperty Function</span></span>
<span data-ttu-id="77057-104">Supprimez la valeur à l’index spécifié d’un objet.</span><span class="sxs-lookup"><span data-stu-id="77057-104">Delete the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="77057-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77057-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index  
);  
```  
  
#### <span data-ttu-id="77057-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77057-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="77057-107">Objet sur lequel travailler.</span><span class="sxs-lookup"><span data-stu-id="77057-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="77057-108">Index à supprimer.</span><span class="sxs-lookup"><span data-stu-id="77057-108">The index to delete.</span></span>  
  
## <span data-ttu-id="77057-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="77057-109">Return Value</span></span>  
 <span data-ttu-id="77057-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="77057-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="77057-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="77057-111">Remarks</span></span>  
 <span data-ttu-id="77057-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="77057-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="77057-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77057-113">Requirements</span></span>  
 <span data-ttu-id="77057-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="77057-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="77057-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77057-115">See Also</span></span>  
 [<span data-ttu-id="77057-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="77057-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)