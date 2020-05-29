---
description: Comparez deux valeurs JavaScript pour l’égalité stricte.
title: Fonction JsStrictEquals | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStrictEquals
helpviewer_keywords:
- JsStrictEquals function
ms.assetid: b35bc655-7ff8-496a-b678-8950bb976047
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b7f2b7a66c32428100f0c0d0f9db6150559ed7a2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566233"
---
# <span data-ttu-id="b5acd-103">Fonction JsStrictEquals</span><span class="sxs-lookup"><span data-stu-id="b5acd-103">JsStrictEquals Function</span></span>
<span data-ttu-id="b5acd-104">Comparez deux valeurs JavaScript pour l’égalité stricte.</span><span class="sxs-lookup"><span data-stu-id="b5acd-104">Compare two JavaScript values for strict equality.</span></span>  
  
## <span data-ttu-id="b5acd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5acd-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStrictEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="b5acd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5acd-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="b5acd-107">Premier objet à comparer.</span><span class="sxs-lookup"><span data-stu-id="b5acd-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="b5acd-108">Deuxième objet à comparer.</span><span class="sxs-lookup"><span data-stu-id="b5acd-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="b5acd-109">Si les valeurs sont strictement égales.</span><span class="sxs-lookup"><span data-stu-id="b5acd-109">Whether the values are strictly equal.</span></span>  
  
## <span data-ttu-id="b5acd-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b5acd-110">Return Value</span></span>  
 <span data-ttu-id="b5acd-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b5acd-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b5acd-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="b5acd-112">Remarks</span></span>  
 <span data-ttu-id="b5acd-113">Cette fonction équivaut à l' `===` opérateur dans JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b5acd-113">This function is equivalent to the `===` operator in Javascript.</span></span>  
  
 <span data-ttu-id="b5acd-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="b5acd-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b5acd-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5acd-115">Requirements</span></span>  
 <span data-ttu-id="b5acd-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b5acd-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b5acd-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5acd-117">See Also</span></span>  
 [<span data-ttu-id="b5acd-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b5acd-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)