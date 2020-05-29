---
description: Rappel d’élément de tâche en arrière-plan.
title: JsBackgroundWorkItemCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9bc1e5687d92d7286e1e6d4387bd6b69d95ceb68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565269"
---
# <span data-ttu-id="db96a-103">JsBackgroundWorkItemCallback typedef</span><span class="sxs-lookup"><span data-stu-id="db96a-103">JsBackgroundWorkItemCallback Typedef</span></span>
<span data-ttu-id="db96a-104">Rappel d’élément de tâche en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="db96a-104">A background work item callback.</span></span>  
  
## <span data-ttu-id="db96a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db96a-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBackgroundWorkItemCallback)(  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="db96a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db96a-106">Parameters</span></span>  
 <span data-ttu-id="db96a-107">callbackData</span><span class="sxs-lookup"><span data-stu-id="db96a-107">callbackData</span></span>  
 <span data-ttu-id="db96a-108">L’argument Data est transmis au service de thread.</span><span class="sxs-lookup"><span data-stu-id="db96a-108">Data argument passed to the thread service.</span></span>  
  
## <span data-ttu-id="db96a-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="db96a-109">Remarks</span></span>  
 <span data-ttu-id="db96a-110">Ce dernier est transmis au service de thread de l’hôte (si fourni) pour permettre à l’hôte d’appeler le rappel d’élément de tâche sur le thread d’arrière-plan de son choix.</span><span class="sxs-lookup"><span data-stu-id="db96a-110">This is passed to the host's thread service (if provided) to allow the host to invoke the work item callback on the background thread of its choice.</span></span>  
  
## <span data-ttu-id="db96a-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db96a-111">Requirements</span></span>  
 <span data-ttu-id="db96a-112">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="db96a-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="db96a-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db96a-113">See Also</span></span>  
 [<span data-ttu-id="db96a-114">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="db96a-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)