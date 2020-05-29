---
description: Initialise la valeur transmise en `VARIANT` tant que projection d’une valeur JavaScript.
title: Fonction JsValueToVariant | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d8748fddcc149cf09fbd46ad3ad489cd66200b71
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565128"
---
# <span data-ttu-id="aec93-103">Fonction JsValueToVariant</span><span class="sxs-lookup"><span data-stu-id="aec93-103">JsValueToVariant Function</span></span>
<span data-ttu-id="aec93-104">Initialise la valeur transmise en `VARIANT` tant que projection d’une valeur JavaScript.</span><span class="sxs-lookup"><span data-stu-id="aec93-104">Initializes the passed in `VARIANT` as a projection of a JavaScript value.</span></span>  
  
## <span data-ttu-id="aec93-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aec93-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsValueToVariant(  
   _In_ JsValueRef object,  
   _Out_ VARIANT *variant  
);  
```  
  
#### <span data-ttu-id="aec93-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aec93-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="aec93-107">Valeur JavaScript à projeter en tant que `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="aec93-107">A JavaScript value to project as a `VARIANT`.</span></span>  
  
 `variant`  
 <span data-ttu-id="aec93-108">Pointeur vers un `VARIANT` struct qui sera initialisé comme une projection.</span><span class="sxs-lookup"><span data-stu-id="aec93-108">A pointer to a `VARIANT` struct that will be initialized as a projection.</span></span>  
  
## <span data-ttu-id="aec93-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="aec93-109">Return Value</span></span>  
  
## <span data-ttu-id="aec93-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="aec93-110">Remarks</span></span>  
 <span data-ttu-id="aec93-111">La projection `VARIANT` peut être utilisée par les clients com Automation pour appeler l’objet JavaScript projeté.</span><span class="sxs-lookup"><span data-stu-id="aec93-111">The projection `VARIANT` can be used by COM automation clients to call into the projected JavaScript object.</span></span>  
  
 <span data-ttu-id="aec93-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="aec93-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="aec93-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aec93-113">Requirements</span></span>  
 <span data-ttu-id="aec93-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="aec93-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="aec93-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aec93-115">See Also</span></span>  
 [<span data-ttu-id="aec93-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="aec93-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)