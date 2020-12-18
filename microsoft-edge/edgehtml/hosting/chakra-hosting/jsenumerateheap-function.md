---
description: Énumère le tas du contexte actuel.
title: Fonction JsEnumerateHeap | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEnumerateHeap
helpviewer_keywords:
- JsEnumerateHeap function
ms.assetid: 3e518e0b-b959-4686-899c-83e6b1946c9d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bb76b28f24b769f71827e59be691188e34e9e1a3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233323"
---
# <span data-ttu-id="d8a20-103">JsEnumerateHeap Function</span><span class="sxs-lookup"><span data-stu-id="d8a20-103">JsEnumerateHeap Function</span></span>

<span data-ttu-id="d8a20-104">Énumère le tas du contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="d8a20-104">Enumerates the heap of the current context.</span></span>  
  
## <span data-ttu-id="d8a20-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8a20-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnumerateHeap(  
   _Out_ IActiveScriptProfilerHeapEnum **enumerator  
);  
```  
  
#### <span data-ttu-id="d8a20-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8a20-106">Parameters</span></span>  
 `enumerator`  
 <span data-ttu-id="d8a20-107">Énumérateur du tas.</span><span class="sxs-lookup"><span data-stu-id="d8a20-107">The heap enumerator.</span></span>  
  
## <span data-ttu-id="d8a20-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d8a20-108">Return Value</span></span>  
 <span data-ttu-id="d8a20-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d8a20-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d8a20-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="d8a20-110">Remarks</span></span>  
 <span data-ttu-id="d8a20-111">Pendant l’énumération du tas, le contexte actuel ne peut pas être supprimé, et tous les appels de modification de l’état du contexte échouent jusqu’à ce que l’énumérateur du tas soit officialisé.</span><span class="sxs-lookup"><span data-stu-id="d8a20-111">While the heap is being enumerated, the current context cannot be removed, and all calls to modify the state of the context will fail until the heap enumerator is released.</span></span>  
  
 <span data-ttu-id="d8a20-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="d8a20-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="d8a20-113">Cette API est prise en charge dans les applications de bureau, mais n’est pas prise en charge dans les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="d8a20-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="d8a20-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="d8a20-114">Requirements</span></span>  
 <span data-ttu-id="d8a20-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d8a20-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d8a20-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8a20-116">See Also</span></span>  
 [<span data-ttu-id="d8a20-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d8a20-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
