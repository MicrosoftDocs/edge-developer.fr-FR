---
description: Obtient la valeur du `undefined` contexte de script actuel.
title: Fonction JsGetUndefinedValue | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetUndefinedValue
helpviewer_keywords:
- JsGetUndefinedValue function
ms.assetid: e118eaf6-452c-42f2-86b8-e63c7d987cba
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 34bfaec4548ee2b77d6d98749c3049bb8f679134
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232837"
---
# <span data-ttu-id="75df8-103">JsGetUndefinedValue Function</span><span class="sxs-lookup"><span data-stu-id="75df8-103">JsGetUndefinedValue Function</span></span>

<span data-ttu-id="75df8-104">Obtient la valeur du `undefined` contexte de script actuel.</span><span class="sxs-lookup"><span data-stu-id="75df8-104">Gets the value of `undefined` in the current script context.</span></span>  
  
## <span data-ttu-id="75df8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75df8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetUndefinedValue(  
   _Out_ JsValueRef *undefinedValue  
);  
```  
  
#### <span data-ttu-id="75df8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75df8-106">Parameters</span></span>  
 `undefinedValue`  
 <span data-ttu-id="75df8-107">`undefined`Valeur.</span><span class="sxs-lookup"><span data-stu-id="75df8-107">The `undefined` value.</span></span>  
  
## <span data-ttu-id="75df8-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="75df8-108">Return Value</span></span>  
 <span data-ttu-id="75df8-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="75df8-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="75df8-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="75df8-110">Remarks</span></span>  
 <span data-ttu-id="75df8-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="75df8-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="75df8-112">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="75df8-112">Requirements</span></span>  
 <span data-ttu-id="75df8-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="75df8-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="75df8-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75df8-114">See Also</span></span>  
 [<span data-ttu-id="75df8-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="75df8-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
