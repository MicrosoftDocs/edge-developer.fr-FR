---
description: Comparez deux valeurs JavaScript pour l’égalité stricte.
title: Fonction JsStrictEquals | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStrictEquals
helpviewer_keywords:
- JsStrictEquals function
ms.assetid: b35bc655-7ff8-496a-b678-8950bb976047
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 98af1629129986cc21cafe5660d3155e031919dc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233133"
---
# <span data-ttu-id="aecc8-103">JsStrictEquals Function</span><span class="sxs-lookup"><span data-stu-id="aecc8-103">JsStrictEquals Function</span></span>

<span data-ttu-id="aecc8-104">Comparez deux valeurs JavaScript pour l’égalité stricte.</span><span class="sxs-lookup"><span data-stu-id="aecc8-104">Compare two JavaScript values for strict equality.</span></span>  
  
## <span data-ttu-id="aecc8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aecc8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStrictEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="aecc8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aecc8-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="aecc8-107">Premier objet à comparer.</span><span class="sxs-lookup"><span data-stu-id="aecc8-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="aecc8-108">Deuxième objet à comparer.</span><span class="sxs-lookup"><span data-stu-id="aecc8-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="aecc8-109">Si les valeurs sont strictement égales.</span><span class="sxs-lookup"><span data-stu-id="aecc8-109">Whether the values are strictly equal.</span></span>  
  
## <span data-ttu-id="aecc8-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="aecc8-110">Return Value</span></span>  
 <span data-ttu-id="aecc8-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="aecc8-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="aecc8-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="aecc8-112">Remarks</span></span>  
 <span data-ttu-id="aecc8-113">Cette fonction équivaut à l' `===` opérateur dans JavaScript.</span><span class="sxs-lookup"><span data-stu-id="aecc8-113">This function is equivalent to the `===` operator in Javascript.</span></span>  
  
 <span data-ttu-id="aecc8-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="aecc8-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="aecc8-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="aecc8-115">Requirements</span></span>  
 <span data-ttu-id="aecc8-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="aecc8-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="aecc8-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aecc8-117">See Also</span></span>  
 [<span data-ttu-id="aecc8-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="aecc8-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
