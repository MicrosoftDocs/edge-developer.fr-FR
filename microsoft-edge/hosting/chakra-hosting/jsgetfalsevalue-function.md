---
description: Obtient la valeur du `false` contexte de script actuel.
title: Fonction JsGetFalseValue | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetFalseValue
helpviewer_keywords:
- JsGetFalseValue function
ms.assetid: 621a584c-4ca8-4ba0-b19a-6cb50cf830b6
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 52e54ad7eb34877c3cb83b06f5aba70edf285bca
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565189"
---
# <span data-ttu-id="6a780-103">Fonction JsGetFalseValue</span><span class="sxs-lookup"><span data-stu-id="6a780-103">JsGetFalseValue Function</span></span>
<span data-ttu-id="6a780-104">Obtient la valeur du `false` contexte de script actuel.</span><span class="sxs-lookup"><span data-stu-id="6a780-104">Gets the value of `false` in the current script context.</span></span>  
  
## <span data-ttu-id="6a780-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a780-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetFalseValue(  
   _Out_ JsValueRef *falseValue  
);  
```  
  
#### <span data-ttu-id="6a780-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a780-106">Parameters</span></span>  
 `falseValue`  
 <span data-ttu-id="6a780-107">`false`Valeur.</span><span class="sxs-lookup"><span data-stu-id="6a780-107">The `false` value.</span></span>  
  
## <span data-ttu-id="6a780-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6a780-108">Return Value</span></span>  
 <span data-ttu-id="6a780-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6a780-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6a780-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="6a780-110">Remarks</span></span>  
 <span data-ttu-id="6a780-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="6a780-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="6a780-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a780-112">Requirements</span></span>  
 <span data-ttu-id="6a780-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6a780-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6a780-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a780-114">See Also</span></span>  
 [<span data-ttu-id="6a780-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6a780-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)