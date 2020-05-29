---
description: Renvoie une valeur qui indique si le tas du contexte actuel est énuméré.
title: Fonction JsIsEnumeratingHeap | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIsEnumeratingHeap
helpviewer_keywords:
- JsIsEnumeratingHeap function
ms.assetid: 5d14518e-3153-43f2-9a9c-068580cbd54f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 79f263547ef5812d905103d09ede7499d56c5dfb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565159"
---
# <span data-ttu-id="82fc8-103">Fonction JsIsEnumeratingHeap</span><span class="sxs-lookup"><span data-stu-id="82fc8-103">JsIsEnumeratingHeap Function</span></span>
<span data-ttu-id="82fc8-104">Renvoie une valeur qui indique si le tas du contexte actuel est énuméré.</span><span class="sxs-lookup"><span data-stu-id="82fc8-104">Returns a value that indicates whether the heap of the current context is being enumerated.</span></span>  
  
## <span data-ttu-id="82fc8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82fc8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsEnumeratingHeap(  
   _Out_ bool *isEnumeratingHeap  
);  
```  
  
#### <span data-ttu-id="82fc8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82fc8-106">Parameters</span></span>  
 `isEnumeratingHeap`  
 <span data-ttu-id="82fc8-107">La présence du tas dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="82fc8-107">Whether the heap is being enumerated.</span></span>  
  
## <span data-ttu-id="82fc8-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="82fc8-108">Return Value</span></span>  
 <span data-ttu-id="82fc8-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="82fc8-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="82fc8-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="82fc8-110">Remarks</span></span>  
 <span data-ttu-id="82fc8-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="82fc8-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="82fc8-112">Cette API est prise en charge dans les applications de bureau, mais n’est pas prise en charge dans les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="82fc8-112">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="82fc8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82fc8-113">Requirements</span></span>  
 <span data-ttu-id="82fc8-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="82fc8-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="82fc8-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82fc8-115">See Also</span></span>  
 [<span data-ttu-id="82fc8-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="82fc8-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)