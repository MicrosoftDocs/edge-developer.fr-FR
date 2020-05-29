---
description: Obtient la valeur du `undefined` contexte de script actuel.
title: Fonction JsGetUndefinedValue | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetUndefinedValue
helpviewer_keywords:
- JsGetUndefinedValue function
ms.assetid: e118eaf6-452c-42f2-86b8-e63c7d987cba
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5edd536a29f5003591de476cb5d21ddb64f48c0b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566303"
---
# <span data-ttu-id="25186-103">Fonction JsGetUndefinedValue</span><span class="sxs-lookup"><span data-stu-id="25186-103">JsGetUndefinedValue Function</span></span>
<span data-ttu-id="25186-104">Obtient la valeur du `undefined` contexte de script actuel.</span><span class="sxs-lookup"><span data-stu-id="25186-104">Gets the value of `undefined` in the current script context.</span></span>  
  
## <span data-ttu-id="25186-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25186-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetUndefinedValue(  
   _Out_ JsValueRef *undefinedValue  
);  
```  
  
#### <span data-ttu-id="25186-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25186-106">Parameters</span></span>  
 `undefinedValue`  
 <span data-ttu-id="25186-107">`undefined`Valeur.</span><span class="sxs-lookup"><span data-stu-id="25186-107">The `undefined` value.</span></span>  
  
## <span data-ttu-id="25186-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="25186-108">Return Value</span></span>  
 <span data-ttu-id="25186-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="25186-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="25186-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="25186-110">Remarks</span></span>  
 <span data-ttu-id="25186-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="25186-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="25186-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25186-112">Requirements</span></span>  
 <span data-ttu-id="25186-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="25186-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="25186-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25186-114">See Also</span></span>  
 [<span data-ttu-id="25186-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="25186-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)