---
description: Appelle une fonction en tant que constructeur.
title: Fonction JsConstructObject | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConstructObject
helpviewer_keywords:
- JsConstructObject function
ms.assetid: b07d2440-db55-4a6a-8376-56b40a8039a1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8dbb757456412e50efaf3a026d169e6b3612b6b1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232989"
---
# <span data-ttu-id="28442-103">JsConstructObject Function</span><span class="sxs-lookup"><span data-stu-id="28442-103">JsConstructObject Function</span></span>

<span data-ttu-id="28442-104">Appelle une fonction en tant que constructeur.</span><span class="sxs-lookup"><span data-stu-id="28442-104">Invokes a function as a constructor.</span></span>  
  
## <span data-ttu-id="28442-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28442-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConstructObject(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="28442-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28442-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="28442-107">Fonction pour appeler en tant que constructeur.</span><span class="sxs-lookup"><span data-stu-id="28442-107">The function to invoke as a constructor.</span></span>  
  
 `arguments`  
 <span data-ttu-id="28442-108">Les arguments de l’appel.</span><span class="sxs-lookup"><span data-stu-id="28442-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="28442-109">Nombre d’arguments passés à la fonction.</span><span class="sxs-lookup"><span data-stu-id="28442-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="28442-110">Valeur renvoyée à partir de l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="28442-110">The value returned from the function invocation.</span></span>  
  
## <span data-ttu-id="28442-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="28442-111">Return Value</span></span>  
 <span data-ttu-id="28442-112">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="28442-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="28442-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="28442-113">Remarks</span></span>  
 <span data-ttu-id="28442-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="28442-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="28442-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="28442-115">Requirements</span></span>  
 <span data-ttu-id="28442-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="28442-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="28442-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28442-117">See Also</span></span>  
 [<span data-ttu-id="28442-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="28442-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
