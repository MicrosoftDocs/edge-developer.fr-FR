---
description: Obtient la valeur du `null` contexte de script actuel.
title: Fonction JsGetNullValue | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetNullValue
helpviewer_keywords:
- JsGetNullValue function
ms.assetid: 132a1496-8dfe-4d3c-a8f8-389f5b0b50d2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 84164aa9ce5d522b0933d928d85b26c652be066f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566322"
---
# <span data-ttu-id="015a9-103">Fonction JsGetNullValue</span><span class="sxs-lookup"><span data-stu-id="015a9-103">JsGetNullValue Function</span></span>
<span data-ttu-id="015a9-104">Obtient la valeur du `null` contexte de script actuel.</span><span class="sxs-lookup"><span data-stu-id="015a9-104">Gets the value of `null` in the current script context.</span></span>  
  
## <span data-ttu-id="015a9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="015a9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetNullValue(  
   _Out_ JsValueRef *nullValue  
);  
```  
  
#### <span data-ttu-id="015a9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="015a9-106">Parameters</span></span>  
 `nullValue`  
 <span data-ttu-id="015a9-107">`null`Valeur.</span><span class="sxs-lookup"><span data-stu-id="015a9-107">The `null` value.</span></span>  
  
## <span data-ttu-id="015a9-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="015a9-108">Return Value</span></span>  
 <span data-ttu-id="015a9-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="015a9-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="015a9-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="015a9-110">Remarks</span></span>  
 <span data-ttu-id="015a9-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="015a9-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="015a9-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="015a9-112">Requirements</span></span>  
 <span data-ttu-id="015a9-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="015a9-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="015a9-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="015a9-114">See Also</span></span>  
 [<span data-ttu-id="015a9-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="015a9-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)