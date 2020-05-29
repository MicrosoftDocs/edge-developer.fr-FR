---
description: Type d’événement de rappel d’attribution.
title: Énumération JsMemoryEventType | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsMemoryEventType
helpviewer_keywords:
- JsMemoryEventType enumeration
ms.assetid: b4b176b6-b536-472e-8999-95b681a1df55
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e9833777ed8fe5a19fd2a1487715296279f7351
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565152"
---
# <span data-ttu-id="66794-103">Énumération JsMemoryEventType</span><span class="sxs-lookup"><span data-stu-id="66794-103">JsMemoryEventType Enumeration</span></span>
<span data-ttu-id="66794-104">Type d’événement de rappel d’attribution.</span><span class="sxs-lookup"><span data-stu-id="66794-104">Allocation callback event type.</span></span>  
  
## <span data-ttu-id="66794-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66794-105">Syntax</span></span>  
  
```cpp  
enum JsMemoryEventType;  
```  
  
## <span data-ttu-id="66794-106">Ses</span><span class="sxs-lookup"><span data-stu-id="66794-106">Members</span></span>  
  
### <span data-ttu-id="66794-107">Doubl</span><span class="sxs-lookup"><span data-stu-id="66794-107">Values</span></span>  
  
|<span data-ttu-id="66794-108">Nom</span><span class="sxs-lookup"><span data-stu-id="66794-108">Name</span></span>|<span data-ttu-id="66794-109">Description</span><span class="sxs-lookup"><span data-stu-id="66794-109">Description</span></span>|  
|----------|-----------------|  
|`JsMemoryAllocate`|<span data-ttu-id="66794-110">Indique une demande d’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="66794-110">Indicates a request for memory allocation.</span></span>|  
|`JsMemoryFailure`|<span data-ttu-id="66794-111">Indique un événement d’allocation ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="66794-111">Indicates a failed allocation event.</span></span>|  
|`JsMemoryFree`|<span data-ttu-id="66794-112">Indique un événement de libère de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="66794-112">Indicates a memory freeing event.</span></span>|  
  
## <span data-ttu-id="66794-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66794-113">Requirements</span></span>  
 <span data-ttu-id="66794-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="66794-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="66794-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66794-115">See Also</span></span>  
 [<span data-ttu-id="66794-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="66794-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)