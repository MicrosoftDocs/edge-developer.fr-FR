---
description: Effectue un nettoyage de la mémoire complet.
title: Fonction JsCollectGarbage | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCollectGarbage
helpviewer_keywords:
- JsCollectGarbage function
ms.assetid: 995c79a5-6e18-45be-81ff-2a5d3348edb8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c551ddf119ec0aa349fcd756f6001d92dbbb0faa
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232992"
---
# <span data-ttu-id="313c3-103">JsCollectGarbage Function</span><span class="sxs-lookup"><span data-stu-id="313c3-103">JsCollectGarbage Function</span></span>

<span data-ttu-id="313c3-104">Effectue un nettoyage de la mémoire complet.</span><span class="sxs-lookup"><span data-stu-id="313c3-104">Performs a full garbage collection.</span></span>  
  
## <span data-ttu-id="313c3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="313c3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCollectGarbage(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="313c3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="313c3-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="313c3-107">Runtime dans lequel le nettoyage de la mémoire sera effectué.</span><span class="sxs-lookup"><span data-stu-id="313c3-107">The runtime in which the garbage collection will be performed.</span></span>  
  
## <span data-ttu-id="313c3-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="313c3-108">Return Value</span></span>  
 <span data-ttu-id="313c3-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="313c3-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="313c3-110">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="313c3-110">Requirements</span></span>  
 <span data-ttu-id="313c3-111">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="313c3-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="313c3-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="313c3-112">See Also</span></span>  
 [<span data-ttu-id="313c3-113">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="313c3-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
