---
description: Appelle une fonction.
title: Fonction JsCallFunction | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCallFunction
helpviewer_keywords:
- JsCallFunction function
ms.assetid: 8a1dca72-d720-4a28-a86e-6809465006fe
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: dc26f66cb7deae0857ce34cbd4d83ee26046b3c8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232991"
---
# <span data-ttu-id="c6a28-103">JsCallFunction Function</span><span class="sxs-lookup"><span data-stu-id="c6a28-103">JsCallFunction Function</span></span>

<span data-ttu-id="c6a28-104">Appelle une fonction.</span><span class="sxs-lookup"><span data-stu-id="c6a28-104">Invokes a function.</span></span>  
  
## <span data-ttu-id="c6a28-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6a28-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCallFunction(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="c6a28-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6a28-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="c6a28-107">Fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="c6a28-107">The function to invoke.</span></span>  
  
 `arguments`  
 <span data-ttu-id="c6a28-108">Les arguments de l’appel.</span><span class="sxs-lookup"><span data-stu-id="c6a28-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="c6a28-109">Nombre d’arguments passés à la fonction.</span><span class="sxs-lookup"><span data-stu-id="c6a28-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="c6a28-110">Valeur renvoyée par l’appel de la fonction, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="c6a28-110">The value returned from the function invocation, if any.</span></span>  
  
## <span data-ttu-id="c6a28-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c6a28-111">Return Value</span></span>  
 <span data-ttu-id="c6a28-112">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c6a28-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c6a28-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="c6a28-113">Remarks</span></span>  
 <span data-ttu-id="c6a28-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="c6a28-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c6a28-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="c6a28-115">Requirements</span></span>  
 <span data-ttu-id="c6a28-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c6a28-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c6a28-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6a28-117">See Also</span></span>  
 [<span data-ttu-id="c6a28-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c6a28-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
