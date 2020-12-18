---
description: Obtient le runtime auquel appartient le contexte.
title: Fonction JsGetRuntime | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntime
helpviewer_keywords:
- JsGetRuntime function
ms.assetid: 5b62e940-a885-405a-9fdd-0495fb391b95
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 49739f0cf3675a44b9fc328e3eaa7d49c6282e53
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233189"
---
# <span data-ttu-id="4881a-103">JsGetRuntime Function</span><span class="sxs-lookup"><span data-stu-id="4881a-103">JsGetRuntime Function</span></span>

<span data-ttu-id="4881a-104">Obtient le runtime auquel appartient le contexte.</span><span class="sxs-lookup"><span data-stu-id="4881a-104">Gets the runtime that the context belongs to.</span></span>  
  
## <span data-ttu-id="4881a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4881a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntime(  
   _In_ JsContextRef context,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### <span data-ttu-id="4881a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4881a-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="4881a-107">Contexte à partir duquel obtenir le Runtime.</span><span class="sxs-lookup"><span data-stu-id="4881a-107">The context to get the runtime from.</span></span>  
  
 `runtime`  
 <span data-ttu-id="4881a-108">Runtime auquel le contexte appartient.</span><span class="sxs-lookup"><span data-stu-id="4881a-108">The runtime the context belongs to.</span></span>  
  
## <span data-ttu-id="4881a-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4881a-109">Return Value</span></span>  
 <span data-ttu-id="4881a-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4881a-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4881a-111">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="4881a-111">Requirements</span></span>  
 <span data-ttu-id="4881a-112">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4881a-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4881a-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4881a-113">See Also</span></span>  
 [<span data-ttu-id="4881a-114">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4881a-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
