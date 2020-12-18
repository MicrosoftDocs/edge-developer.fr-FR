---
description: Obtient l’utilisation de la mémoire actuelle pour un Runtime.
title: Fonction JsGetRuntimeMemoryUsage | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryUsage
helpviewer_keywords:
- JsGetRuntimeMemoryUsage function
ms.assetid: b9bd4146-bfbc-4cb1-a0e9-a0ded7fb09bd
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a9c8d59e8cf73ad178f539f2f9f0ed191ceb47fd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233547"
---
# <span data-ttu-id="dc171-103">JsGetRuntimeMemoryUsage Function</span><span class="sxs-lookup"><span data-stu-id="dc171-103">JsGetRuntimeMemoryUsage Function</span></span>

<span data-ttu-id="dc171-104">Obtient l’utilisation de la mémoire actuelle pour un Runtime.</span><span class="sxs-lookup"><span data-stu-id="dc171-104">Gets the current memory usage for a runtime.</span></span>  
  
## <span data-ttu-id="dc171-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc171-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryUsage(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryUsage  
);  
```  
  
#### <span data-ttu-id="dc171-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc171-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="dc171-107">Le runtime dont l’utilisation de la mémoire doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="dc171-107">The runtime whose memory usage is to be retrieved.</span></span>  
  
 `memoryUsage`  
 <span data-ttu-id="dc171-108">L’utilisation de la mémoire actuelle du runtime, en octets.</span><span class="sxs-lookup"><span data-stu-id="dc171-108">The runtime's current memory usage, in bytes.</span></span>  
  
## <span data-ttu-id="dc171-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dc171-109">Return Value</span></span>  
 <span data-ttu-id="dc171-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="dc171-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dc171-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="dc171-111">Remarks</span></span>  
 <span data-ttu-id="dc171-112">L’utilisation de la mémoire peut être toujours Récupérée, même si le runtime est actif ou non sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="dc171-112">Memory usage can be always be retrieved, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="dc171-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="dc171-113">Requirements</span></span>  
 <span data-ttu-id="dc171-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dc171-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dc171-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc171-115">See Also</span></span>  
 [<span data-ttu-id="dc171-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="dc171-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
