---
description: Rappel d’élément de tâche en arrière-plan.
title: JsBackgroundWorkItemCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d69306b334c2e0c9b27b96a5a417739ffdcd7dd7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233006"
---
# <span data-ttu-id="c9ffa-103">Typedef JsBackgroundWorkItemCallback</span><span class="sxs-lookup"><span data-stu-id="c9ffa-103">JsBackgroundWorkItemCallback Typedef</span></span>

<span data-ttu-id="c9ffa-104">Rappel d’élément de tâche en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="c9ffa-104">A background work item callback.</span></span>  
  
## <span data-ttu-id="c9ffa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9ffa-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBackgroundWorkItemCallback)(  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="c9ffa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9ffa-106">Parameters</span></span>  
 <span data-ttu-id="c9ffa-107">callbackData</span><span class="sxs-lookup"><span data-stu-id="c9ffa-107">callbackData</span></span>  
 <span data-ttu-id="c9ffa-108">L’argument Data est transmis au service de thread.</span><span class="sxs-lookup"><span data-stu-id="c9ffa-108">Data argument passed to the thread service.</span></span>  
  
## <span data-ttu-id="c9ffa-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="c9ffa-109">Remarks</span></span>  
 <span data-ttu-id="c9ffa-110">Ce dernier est transmis au service de thread de l’hôte (si fourni) pour permettre à l’hôte d’appeler le rappel d’élément de tâche sur le thread d’arrière-plan de son choix.</span><span class="sxs-lookup"><span data-stu-id="c9ffa-110">This is passed to the host's thread service (if provided) to allow the host to invoke the work item callback on the background thread of its choice.</span></span>  
  
## <span data-ttu-id="c9ffa-111">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="c9ffa-111">Requirements</span></span>  
 <span data-ttu-id="c9ffa-112">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c9ffa-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c9ffa-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9ffa-113">See Also</span></span>  
 [<span data-ttu-id="c9ffa-114">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c9ffa-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
