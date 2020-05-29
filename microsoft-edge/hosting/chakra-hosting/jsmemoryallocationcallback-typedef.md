---
description: Routine de rappel implémentée par l’utilisateur pour les événements d’allocation de mémoire.
title: JsMemoryAllocationCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b11b3d076c01dbfcae190fd665528323d6f8b987
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565155"
---
# <span data-ttu-id="faf07-103">JsMemoryAllocationCallback typedef</span><span class="sxs-lookup"><span data-stu-id="faf07-103">JsMemoryAllocationCallback Typedef</span></span>
<span data-ttu-id="faf07-104">Routine de rappel implémentée par l’utilisateur pour les événements d’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="faf07-104">User implemented callback routine for memory allocation events.</span></span>  
  
## <span data-ttu-id="faf07-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="faf07-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsMemoryAllocationCallback)(  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryEventType allocationEvent,  
   _In_ size_t allocationSize  
);  
```  
  
#### <span data-ttu-id="faf07-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="faf07-106">Parameters</span></span>  
 <span data-ttu-id="faf07-107">callbackState</span><span class="sxs-lookup"><span data-stu-id="faf07-107">callbackState</span></span>  
 <span data-ttu-id="faf07-108">État transmis à JsSetRuntimeMemoryAllocationCallback.</span><span class="sxs-lookup"><span data-stu-id="faf07-108">The state passed to JsSetRuntimeMemoryAllocationCallback.</span></span>  
  
 <span data-ttu-id="faf07-109">allocationEvent</span><span class="sxs-lookup"><span data-stu-id="faf07-109">allocationEvent</span></span>  
 <span data-ttu-id="faf07-110">Type d’événement d’allocation de type.</span><span class="sxs-lookup"><span data-stu-id="faf07-110">The type of type allocation event.</span></span>  
  
 <span data-ttu-id="faf07-111">allocations</span><span class="sxs-lookup"><span data-stu-id="faf07-111">allocationSize</span></span>  
 <span data-ttu-id="faf07-112">La taille de l’attribution.</span><span class="sxs-lookup"><span data-stu-id="faf07-112">The size of the allocation.</span></span>  
  
## <span data-ttu-id="faf07-113">Valeur de propriété/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="faf07-113">Property Value/Return Value</span></span>  
 <span data-ttu-id="faf07-114">Pour l’événement JsMemoryAllocate, la valeur true permet au runtime de continuer l’attribution.</span><span class="sxs-lookup"><span data-stu-id="faf07-114">For the JsMemoryAllocate event, returning true allows the runtime to continue with allocation.</span></span> <span data-ttu-id="faf07-115">Le retour de la valeur false indique que la demande d’allocation est refusée.</span><span class="sxs-lookup"><span data-stu-id="faf07-115">Returning false indicates the allocation request is rejected.</span></span> <span data-ttu-id="faf07-116">La valeur de retour est ignorée pour les autres événements d’allocation.</span><span class="sxs-lookup"><span data-stu-id="faf07-116">The return value is ignored for other allocation events.</span></span>  
  
## <span data-ttu-id="faf07-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="faf07-117">Remarks</span></span>  
 <span data-ttu-id="faf07-118">Utilisez JsSetRuntimeMemoryAllocationCallback pour inscrire ce rappel.</span><span class="sxs-lookup"><span data-stu-id="faf07-118">Use JsSetRuntimeMemoryAllocationCallback to register this callback.</span></span>  
  
## <span data-ttu-id="faf07-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="faf07-119">Requirements</span></span>  
 <span data-ttu-id="faf07-120">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="faf07-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="faf07-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="faf07-121">See Also</span></span>  
 [<span data-ttu-id="faf07-122">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="faf07-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)