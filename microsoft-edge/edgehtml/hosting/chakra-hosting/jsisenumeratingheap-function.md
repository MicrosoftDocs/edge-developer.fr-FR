---
description: Renvoie une valeur qui indique si le tas du contexte actuel est énuméré.
title: Fonction JsIsEnumeratingHeap | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIsEnumeratingHeap
helpviewer_keywords:
- JsIsEnumeratingHeap function
ms.assetid: 5d14518e-3153-43f2-9a9c-068580cbd54f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5b66fc70ea79d78029f6bc0c900ade1aae38e604
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233349"
---
# <span data-ttu-id="84cc7-103">JsIsEnumeratingHeap Function</span><span class="sxs-lookup"><span data-stu-id="84cc7-103">JsIsEnumeratingHeap Function</span></span>

<span data-ttu-id="84cc7-104">Renvoie une valeur qui indique si le tas du contexte actuel est énuméré.</span><span class="sxs-lookup"><span data-stu-id="84cc7-104">Returns a value that indicates whether the heap of the current context is being enumerated.</span></span>  
  
## <span data-ttu-id="84cc7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84cc7-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsEnumeratingHeap(  
   _Out_ bool *isEnumeratingHeap  
);  
```  
  
#### <span data-ttu-id="84cc7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84cc7-106">Parameters</span></span>  
 `isEnumeratingHeap`  
 <span data-ttu-id="84cc7-107">La présence du tas dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="84cc7-107">Whether the heap is being enumerated.</span></span>  
  
## <span data-ttu-id="84cc7-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="84cc7-108">Return Value</span></span>  
 <span data-ttu-id="84cc7-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="84cc7-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="84cc7-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="84cc7-110">Remarks</span></span>  
 <span data-ttu-id="84cc7-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="84cc7-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="84cc7-112">Cette API est prise en charge dans les applications de bureau, mais n’est pas prise en charge dans les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="84cc7-112">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="84cc7-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="84cc7-113">Requirements</span></span>  
 <span data-ttu-id="84cc7-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="84cc7-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="84cc7-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84cc7-115">See Also</span></span>  
 [<span data-ttu-id="84cc7-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="84cc7-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
