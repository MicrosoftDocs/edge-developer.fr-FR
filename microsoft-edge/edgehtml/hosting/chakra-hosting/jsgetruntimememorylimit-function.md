---
description: Obtient la limite de mémoire actuelle pour un Runtime.
title: Fonction JsGetRuntimeMemoryLimit | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryLimit
helpviewer_keywords:
- JsGetRuntimeMemoryLimit function
ms.assetid: ed81ca60-99fd-46b0-89ae-f6ac07926904
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ed04a0fb921d22eea17eaf86ef7a0152fbf2a1d0
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233486"
---
# <span data-ttu-id="69a86-103">JsGetRuntimeMemoryLimit Function</span><span class="sxs-lookup"><span data-stu-id="69a86-103">JsGetRuntimeMemoryLimit Function</span></span>

<span data-ttu-id="69a86-104">Obtient la limite de mémoire actuelle pour un Runtime.</span><span class="sxs-lookup"><span data-stu-id="69a86-104">Gets the current memory limit for a runtime.</span></span>  
  
## <span data-ttu-id="69a86-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69a86-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryLimit  
);  
```  
  
#### <span data-ttu-id="69a86-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69a86-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="69a86-107">Le runtime dont la limite de mémoire doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="69a86-107">The runtime whose memory limit is to be retrieved.</span></span>  
  
 `memoryLimit`  
 <span data-ttu-id="69a86-108">La limite de mémoire actuelle du runtime, en octets ou-1 si aucune limite n’est définie.</span><span class="sxs-lookup"><span data-stu-id="69a86-108">The runtime's current memory limit, in bytes, or -1 if no limit has been set.</span></span>  
  
## <span data-ttu-id="69a86-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="69a86-109">Return Value</span></span>  
 <span data-ttu-id="69a86-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="69a86-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="69a86-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="69a86-111">Remarks</span></span>  
 <span data-ttu-id="69a86-112">La limite de mémoire d’un Runtime peut être toujours Récupérée, même si le runtime est actif ou non sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="69a86-112">The memory limit of a runtime can be always be retrieved, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="69a86-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="69a86-113">Requirements</span></span>  
 <span data-ttu-id="69a86-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="69a86-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="69a86-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69a86-115">See Also</span></span>  
 [<span data-ttu-id="69a86-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="69a86-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
