---
description: Définit un rappel d’allocation de mémoire pour le runtime spécifié.
title: Fonction JsSetRuntimeMemoryAllocationCallback | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryAllocationCallback
helpviewer_keywords:
- JsSetRuntimeMemoryAllocationCallback function
ms.assetid: 6aa7d58d-6456-4df1-815f-1ba36fb4ae14
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ee2abf36e14c26ac58b90d48a6115fd6502307c9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233132"
---
# <span data-ttu-id="1c35e-103">JsSetRuntimeMemoryAllocationCallback Function</span><span class="sxs-lookup"><span data-stu-id="1c35e-103">JsSetRuntimeMemoryAllocationCallback Function</span></span>

<span data-ttu-id="1c35e-104">Définit un rappel d’allocation de mémoire pour le runtime spécifié.</span><span class="sxs-lookup"><span data-stu-id="1c35e-104">Sets a memory allocation callback for specified runtime.</span></span>  
  
## <span data-ttu-id="1c35e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c35e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryAllocationCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryAllocationCallback allocationCallback  
);  
```  
  
#### <span data-ttu-id="1c35e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c35e-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="1c35e-107">Le runtime pour lequel inscrire le rappel d’allocation.</span><span class="sxs-lookup"><span data-stu-id="1c35e-107">The runtime for which to register the allocation callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="1c35e-108">État fourni par l’utilisateur qui sera transmis au rappel.</span><span class="sxs-lookup"><span data-stu-id="1c35e-108">User provided state that will be passed back to the callback.</span></span>  
  
 `allocationCallback`  
 <span data-ttu-id="1c35e-109">Rappel d’allocation de mémoire à appeler pour les événements d’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="1c35e-109">Memory allocation callback to be called for memory allocation events.</span></span>  
  
## <span data-ttu-id="1c35e-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1c35e-110">Return Value</span></span>  
 <span data-ttu-id="1c35e-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1c35e-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1c35e-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="1c35e-112">Remarks</span></span>  
 <span data-ttu-id="1c35e-113">En inscrivant un rappel d’allocation de mémoire, le runtime peut rappeler l’hôte à chaque fois qu’il acquiert une mémoire ou libère de la mémoire, le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1c35e-113">Registering a memory allocation callback will cause the runtime to call back to the host whenever it acquires memory from, or releases memory to, the OS.</span></span> <span data-ttu-id="1c35e-114">La routine de rappel est appelée avant que le gestionnaire de mémoire Runtime alloue un bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="1c35e-114">The callback routine is called before the runtime memory manager allocates a block of memory.</span></span> <span data-ttu-id="1c35e-115">L’attribution sera refusée si le rappel retourne false.</span><span class="sxs-lookup"><span data-stu-id="1c35e-115">The allocation will be rejected if the callback returns false.</span></span> <span data-ttu-id="1c35e-116">Le gestionnaire de mémoire Runtime appelle également la routine de rappel après la libération d’un bloc de mémoire, ainsi que les échecs de répartition.</span><span class="sxs-lookup"><span data-stu-id="1c35e-116">The runtime memory manager will also invoke the callback routine after freeing a block of memory, as well as after allocation failures.</span></span>  
  
 <span data-ttu-id="1c35e-117">Le rappel est appelé sur le thread d’exécution du runtime actuel, donc l’exécution est bloquée jusqu’à ce que le rappel se termine.</span><span class="sxs-lookup"><span data-stu-id="1c35e-117">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="1c35e-118">La valeur de retour du rappel n’est pas stockée; les attributions précédemment rejetées n’empêchent pas le runtime d’appeler de nouveau le rappel plus tard pour les nouvelles allocations de mémoire.</span><span class="sxs-lookup"><span data-stu-id="1c35e-118">The return value of the callback is not stored; previously rejected allocations will not prevent the runtime from invoking the callback again later for new memory allocations.</span></span>  
  
## <span data-ttu-id="1c35e-119">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="1c35e-119">Requirements</span></span>  
 <span data-ttu-id="1c35e-120">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1c35e-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1c35e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c35e-121">See Also</span></span>  
 [<span data-ttu-id="1c35e-122">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1c35e-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
