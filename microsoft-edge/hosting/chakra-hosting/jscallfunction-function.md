---
description: Appelle une fonction.
title: Fonction JsCallFunction | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCallFunction
helpviewer_keywords:
- JsCallFunction function
ms.assetid: 8a1dca72-d720-4a28-a86e-6809465006fe
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f242ccef71d8a2b361dbe2d1a299728f5551f5d3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565262"
---
# <span data-ttu-id="33edf-103">Fonction JsCallFunction</span><span class="sxs-lookup"><span data-stu-id="33edf-103">JsCallFunction Function</span></span>
<span data-ttu-id="33edf-104">Appelle une fonction.</span><span class="sxs-lookup"><span data-stu-id="33edf-104">Invokes a function.</span></span>  
  
## <span data-ttu-id="33edf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33edf-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCallFunction(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="33edf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33edf-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="33edf-107">Fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="33edf-107">The function to invoke.</span></span>  
  
 `arguments`  
 <span data-ttu-id="33edf-108">Les arguments de l’appel.</span><span class="sxs-lookup"><span data-stu-id="33edf-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="33edf-109">Nombre d’arguments passés à la fonction.</span><span class="sxs-lookup"><span data-stu-id="33edf-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="33edf-110">Valeur renvoyée par l’appel de la fonction, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="33edf-110">The value returned from the function invocation, if any.</span></span>  
  
## <span data-ttu-id="33edf-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="33edf-111">Return Value</span></span>  
 <span data-ttu-id="33edf-112">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="33edf-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="33edf-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="33edf-113">Remarks</span></span>  
 <span data-ttu-id="33edf-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="33edf-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="33edf-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33edf-115">Requirements</span></span>  
 <span data-ttu-id="33edf-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="33edf-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="33edf-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33edf-117">See Also</span></span>  
 [<span data-ttu-id="33edf-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="33edf-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)