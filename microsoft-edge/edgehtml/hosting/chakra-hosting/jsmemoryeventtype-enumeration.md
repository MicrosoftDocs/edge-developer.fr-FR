---
description: Type d’événement de rappel d’attribution.
title: Énumération JsMemoryEventType | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsMemoryEventType
helpviewer_keywords:
- JsMemoryEventType enumeration
ms.assetid: b4b176b6-b536-472e-8999-95b681a1df55
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a28010f908285098cf652b497b6d6c272bc763fc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232783"
---
# <span data-ttu-id="71a48-103">Énumération JsMemoryEventType</span><span class="sxs-lookup"><span data-stu-id="71a48-103">JsMemoryEventType Enumeration</span></span>

<span data-ttu-id="71a48-104">Type d’événement de rappel d’attribution.</span><span class="sxs-lookup"><span data-stu-id="71a48-104">Allocation callback event type.</span></span>  
  
## <span data-ttu-id="71a48-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71a48-105">Syntax</span></span>  
  
```cpp  
enum JsMemoryEventType;  
```  
  
## <span data-ttu-id="71a48-106">Ses</span><span class="sxs-lookup"><span data-stu-id="71a48-106">Members</span></span>  
  
### <span data-ttu-id="71a48-107">Doubl</span><span class="sxs-lookup"><span data-stu-id="71a48-107">Values</span></span>  
  
|<span data-ttu-id="71a48-108">Nom</span><span class="sxs-lookup"><span data-stu-id="71a48-108">Name</span></span>|<span data-ttu-id="71a48-109">Description</span><span class="sxs-lookup"><span data-stu-id="71a48-109">Description</span></span>|  
|----------|-----------------|  
|`JsMemoryAllocate`|<span data-ttu-id="71a48-110">Indique une demande d’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="71a48-110">Indicates a request for memory allocation.</span></span>|  
|`JsMemoryFailure`|<span data-ttu-id="71a48-111">Indique un événement d’allocation ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="71a48-111">Indicates a failed allocation event.</span></span>|  
|`JsMemoryFree`|<span data-ttu-id="71a48-112">Indique un événement de libère de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="71a48-112">Indicates a memory freeing event.</span></span>|  
  
## <span data-ttu-id="71a48-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="71a48-113">Requirements</span></span>  
 <span data-ttu-id="71a48-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="71a48-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="71a48-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71a48-115">See Also</span></span>  
 [<span data-ttu-id="71a48-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="71a48-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
