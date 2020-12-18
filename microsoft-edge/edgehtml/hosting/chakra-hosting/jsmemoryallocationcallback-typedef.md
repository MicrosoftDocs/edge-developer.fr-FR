---
description: Routine de rappel implémentée par l’utilisateur pour les événements d’allocation de mémoire.
title: JsMemoryAllocationCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 22b5cc0fe5a2c8b49f71c91d28f95ba29af37849
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232974"
---
# <span data-ttu-id="65e00-103">Typedef JsMemoryAllocationCallback</span><span class="sxs-lookup"><span data-stu-id="65e00-103">JsMemoryAllocationCallback Typedef</span></span>

<span data-ttu-id="65e00-104">Routine de rappel implémentée par l’utilisateur pour les événements d’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="65e00-104">User implemented callback routine for memory allocation events.</span></span>  
  
## <span data-ttu-id="65e00-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65e00-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsMemoryAllocationCallback)(  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryEventType allocationEvent,  
   _In_ size_t allocationSize  
);  
```  
  
#### <span data-ttu-id="65e00-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65e00-106">Parameters</span></span>  
 <span data-ttu-id="65e00-107">callbackState</span><span class="sxs-lookup"><span data-stu-id="65e00-107">callbackState</span></span>  
 <span data-ttu-id="65e00-108">État transmis à JsSetRuntimeMemoryAllocationCallback.</span><span class="sxs-lookup"><span data-stu-id="65e00-108">The state passed to JsSetRuntimeMemoryAllocationCallback.</span></span>  
  
 <span data-ttu-id="65e00-109">allocationEvent</span><span class="sxs-lookup"><span data-stu-id="65e00-109">allocationEvent</span></span>  
 <span data-ttu-id="65e00-110">Type d’événement d’allocation de type.</span><span class="sxs-lookup"><span data-stu-id="65e00-110">The type of type allocation event.</span></span>  
  
 <span data-ttu-id="65e00-111">allocations</span><span class="sxs-lookup"><span data-stu-id="65e00-111">allocationSize</span></span>  
 <span data-ttu-id="65e00-112">La taille de l’attribution.</span><span class="sxs-lookup"><span data-stu-id="65e00-112">The size of the allocation.</span></span>  
  
## <span data-ttu-id="65e00-113">Valeur de propriété/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="65e00-113">Property Value/Return Value</span></span>  
 <span data-ttu-id="65e00-114">Pour l’événement JsMemoryAllocate, la valeur true permet au runtime de continuer l’attribution.</span><span class="sxs-lookup"><span data-stu-id="65e00-114">For the JsMemoryAllocate event, returning true allows the runtime to continue with allocation.</span></span> <span data-ttu-id="65e00-115">Le retour de la valeur false indique que la demande d’allocation est refusée.</span><span class="sxs-lookup"><span data-stu-id="65e00-115">Returning false indicates the allocation request is rejected.</span></span> <span data-ttu-id="65e00-116">La valeur de retour est ignorée pour les autres événements d’allocation.</span><span class="sxs-lookup"><span data-stu-id="65e00-116">The return value is ignored for other allocation events.</span></span>  
  
## <span data-ttu-id="65e00-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="65e00-117">Remarks</span></span>  
 <span data-ttu-id="65e00-118">Utilisez JsSetRuntimeMemoryAllocationCallback pour inscrire ce rappel.</span><span class="sxs-lookup"><span data-stu-id="65e00-118">Use JsSetRuntimeMemoryAllocationCallback to register this callback.</span></span>  
  
## <span data-ttu-id="65e00-119">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="65e00-119">Requirements</span></span>  
 <span data-ttu-id="65e00-120">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="65e00-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="65e00-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65e00-121">See Also</span></span>  
 [<span data-ttu-id="65e00-122">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="65e00-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
