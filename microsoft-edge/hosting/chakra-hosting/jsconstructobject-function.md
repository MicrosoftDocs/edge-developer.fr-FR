---
description: Appelle une fonction en tant que constructeur.
title: Fonction JsConstructObject | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConstructObject
helpviewer_keywords:
- JsConstructObject function
ms.assetid: b07d2440-db55-4a6a-8376-56b40a8039a1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6fb9654b5c7321d6c6b0b255ec897fb30a114041
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565257"
---
# <span data-ttu-id="c2cc3-103">Fonction JsConstructObject</span><span class="sxs-lookup"><span data-stu-id="c2cc3-103">JsConstructObject Function</span></span>
<span data-ttu-id="c2cc3-104">Appelle une fonction en tant que constructeur.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-104">Invokes a function as a constructor.</span></span>  
  
## <span data-ttu-id="c2cc3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2cc3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConstructObject(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="c2cc3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2cc3-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="c2cc3-107">Fonction pour appeler en tant que constructeur.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-107">The function to invoke as a constructor.</span></span>  
  
 `arguments`  
 <span data-ttu-id="c2cc3-108">Les arguments de l’appel.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="c2cc3-109">Nombre d’arguments passés à la fonction.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="c2cc3-110">Valeur renvoyée à partir de l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-110">The value returned from the function invocation.</span></span>  
  
## <span data-ttu-id="c2cc3-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c2cc3-111">Return Value</span></span>  
 <span data-ttu-id="c2cc3-112">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c2cc3-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="c2cc3-113">Remarks</span></span>  
 <span data-ttu-id="c2cc3-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c2cc3-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2cc3-115">Requirements</span></span>  
 <span data-ttu-id="c2cc3-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c2cc3-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c2cc3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2cc3-117">See Also</span></span>  
 [<span data-ttu-id="c2cc3-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c2cc3-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)