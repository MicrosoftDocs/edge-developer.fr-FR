---
description: Énumère le tas du contexte actuel.
title: Fonction JsEnumerateHeap | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsEnumerateHeap
helpviewer_keywords:
- JsEnumerateHeap function
ms.assetid: 3e518e0b-b959-4686-899c-83e6b1946c9d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f1c2590388fcc09b641e3908d45eef7271bcb1ad
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566339"
---
# <span data-ttu-id="29b18-103">Fonction JsEnumerateHeap</span><span class="sxs-lookup"><span data-stu-id="29b18-103">JsEnumerateHeap Function</span></span>
<span data-ttu-id="29b18-104">Énumère le tas du contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="29b18-104">Enumerates the heap of the current context.</span></span>  
  
## <span data-ttu-id="29b18-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29b18-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnumerateHeap(  
   _Out_ IActiveScriptProfilerHeapEnum **enumerator  
);  
```  
  
#### <span data-ttu-id="29b18-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29b18-106">Parameters</span></span>  
 `enumerator`  
 <span data-ttu-id="29b18-107">Énumérateur du tas.</span><span class="sxs-lookup"><span data-stu-id="29b18-107">The heap enumerator.</span></span>  
  
## <span data-ttu-id="29b18-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="29b18-108">Return Value</span></span>  
 <span data-ttu-id="29b18-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="29b18-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="29b18-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="29b18-110">Remarks</span></span>  
 <span data-ttu-id="29b18-111">Pendant l’énumération du tas, le contexte actuel ne peut pas être supprimé, et tous les appels de modification de l’état du contexte échouent jusqu’à ce que l’énumérateur du tas soit officialisé.</span><span class="sxs-lookup"><span data-stu-id="29b18-111">While the heap is being enumerated, the current context cannot be removed, and all calls to modify the state of the context will fail until the heap enumerator is released.</span></span>  
  
 <span data-ttu-id="29b18-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="29b18-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="29b18-113">Cette API est prise en charge dans les applications de bureau, mais n’est pas prise en charge dans les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="29b18-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="29b18-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29b18-114">Requirements</span></span>  
 <span data-ttu-id="29b18-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="29b18-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="29b18-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29b18-116">See Also</span></span>  
 [<span data-ttu-id="29b18-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="29b18-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)