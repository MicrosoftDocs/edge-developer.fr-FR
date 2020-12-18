---
description: Obtient la valeur du `null` contexte de script actuel.
title: Fonction JsGetNullValue | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetNullValue
helpviewer_keywords:
- JsGetNullValue function
ms.assetid: 132a1496-8dfe-4d3c-a8f8-389f5b0b50d2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 31e1ba19f9f27e75f0166238d98390e2c4a26c24
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232803"
---
# <span data-ttu-id="a3115-103">JsGetNullValue Function</span><span class="sxs-lookup"><span data-stu-id="a3115-103">JsGetNullValue Function</span></span>

<span data-ttu-id="a3115-104">Obtient la valeur du `null` contexte de script actuel.</span><span class="sxs-lookup"><span data-stu-id="a3115-104">Gets the value of `null` in the current script context.</span></span>  
  
## <span data-ttu-id="a3115-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3115-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetNullValue(  
   _Out_ JsValueRef *nullValue  
);  
```  
  
#### <span data-ttu-id="a3115-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3115-106">Parameters</span></span>  
 `nullValue`  
 <span data-ttu-id="a3115-107">`null`Valeur.</span><span class="sxs-lookup"><span data-stu-id="a3115-107">The `null` value.</span></span>  
  
## <span data-ttu-id="a3115-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a3115-108">Return Value</span></span>  
 <span data-ttu-id="a3115-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a3115-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a3115-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="a3115-110">Remarks</span></span>  
 <span data-ttu-id="a3115-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="a3115-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a3115-112">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="a3115-112">Requirements</span></span>  
 <span data-ttu-id="a3115-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a3115-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a3115-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3115-114">See Also</span></span>  
 [<span data-ttu-id="a3115-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a3115-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
