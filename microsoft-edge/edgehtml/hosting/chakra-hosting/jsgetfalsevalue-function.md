---
description: Obtient la valeur du `false` contexte de script actuel.
title: Fonction JsGetFalseValue | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetFalseValue
helpviewer_keywords:
- JsGetFalseValue function
ms.assetid: 621a584c-4ca8-4ba0-b19a-6cb50cf830b6
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c87ad969fc7547f4d650148005327fb93dce805d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233219"
---
# <span data-ttu-id="55aac-103">JsGetFalseValue Function</span><span class="sxs-lookup"><span data-stu-id="55aac-103">JsGetFalseValue Function</span></span>

<span data-ttu-id="55aac-104">Obtient la valeur du `false` contexte de script actuel.</span><span class="sxs-lookup"><span data-stu-id="55aac-104">Gets the value of `false` in the current script context.</span></span>  
  
## <span data-ttu-id="55aac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55aac-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetFalseValue(  
   _Out_ JsValueRef *falseValue  
);  
```  
  
#### <span data-ttu-id="55aac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55aac-106">Parameters</span></span>  
 `falseValue`  
 <span data-ttu-id="55aac-107">`false`Valeur.</span><span class="sxs-lookup"><span data-stu-id="55aac-107">The `false` value.</span></span>  
  
## <span data-ttu-id="55aac-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="55aac-108">Return Value</span></span>  
 <span data-ttu-id="55aac-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="55aac-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="55aac-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="55aac-110">Remarks</span></span>  
 <span data-ttu-id="55aac-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="55aac-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="55aac-112">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="55aac-112">Requirements</span></span>  
 <span data-ttu-id="55aac-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="55aac-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="55aac-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55aac-114">See Also</span></span>  
 [<span data-ttu-id="55aac-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="55aac-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
