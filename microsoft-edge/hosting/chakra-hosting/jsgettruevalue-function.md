---
description: Obtient la valeur du `true` contexte de script actuel.
title: Fonction JsGetTrueValue | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetTrueValue
helpviewer_keywords:
- JsGetTrueValue function
ms.assetid: c2a56d48-344b-492b-90b8-f570710f8310
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 620ed775947db9d7156d61df1cfdf974a46baec2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565169"
---
# <span data-ttu-id="14dcb-103">Fonction JsGetTrueValue</span><span class="sxs-lookup"><span data-stu-id="14dcb-103">JsGetTrueValue Function</span></span>
<span data-ttu-id="14dcb-104">Obtient la valeur du `true` contexte de script actuel.</span><span class="sxs-lookup"><span data-stu-id="14dcb-104">Gets the value of `true` in the current script context.</span></span>  
  
## <span data-ttu-id="14dcb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14dcb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTrueValue(  
   _Out_ JsValueRef *trueValue  
);  
```  
  
#### <span data-ttu-id="14dcb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14dcb-106">Parameters</span></span>  
 `trueValue`  
 <span data-ttu-id="14dcb-107">`true`Valeur.</span><span class="sxs-lookup"><span data-stu-id="14dcb-107">The `true` value.</span></span>  
  
## <span data-ttu-id="14dcb-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="14dcb-108">Return Value</span></span>  
 <span data-ttu-id="14dcb-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="14dcb-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="14dcb-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="14dcb-110">Remarks</span></span>  
 <span data-ttu-id="14dcb-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="14dcb-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="14dcb-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14dcb-112">Requirements</span></span>  
 <span data-ttu-id="14dcb-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="14dcb-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="14dcb-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14dcb-114">See Also</span></span>  
 [<span data-ttu-id="14dcb-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="14dcb-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)