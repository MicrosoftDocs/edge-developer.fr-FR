---
description: Obtient la valeur du `true` contexte de script actuel.
title: Fonction JsGetTrueValue | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetTrueValue
helpviewer_keywords:
- JsGetTrueValue function
ms.assetid: c2a56d48-344b-492b-90b8-f570710f8310
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 58798e1e8aab57d626be0c8c878f9be39d0af942
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233539"
---
# <span data-ttu-id="673ec-103">JsGetTrueValue Function</span><span class="sxs-lookup"><span data-stu-id="673ec-103">JsGetTrueValue Function</span></span>

<span data-ttu-id="673ec-104">Obtient la valeur du `true` contexte de script actuel.</span><span class="sxs-lookup"><span data-stu-id="673ec-104">Gets the value of `true` in the current script context.</span></span>  
  
## <span data-ttu-id="673ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="673ec-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTrueValue(  
   _Out_ JsValueRef *trueValue  
);  
```  
  
#### <span data-ttu-id="673ec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="673ec-106">Parameters</span></span>  
 `trueValue`  
 <span data-ttu-id="673ec-107">`true`Valeur.</span><span class="sxs-lookup"><span data-stu-id="673ec-107">The `true` value.</span></span>  
  
## <span data-ttu-id="673ec-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="673ec-108">Return Value</span></span>  
 <span data-ttu-id="673ec-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="673ec-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="673ec-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="673ec-110">Remarks</span></span>  
 <span data-ttu-id="673ec-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="673ec-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="673ec-112">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="673ec-112">Requirements</span></span>  
 <span data-ttu-id="673ec-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="673ec-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="673ec-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="673ec-114">See Also</span></span>  
 [<span data-ttu-id="673ec-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="673ec-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
