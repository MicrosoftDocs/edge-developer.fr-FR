---
description: Rappel appelé avant la collecte d’un objet.
title: JsObjectBeforeCollectCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: f21a064a-579f-44cb-9d21-76b62e8c18f5
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4c24385ec5e15919719ffb0ae71c8adf39c1724c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233313"
---
# <span data-ttu-id="a9450-103">Typedef JsObjectBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="a9450-103">JsObjectBeforeCollectCallback Typedef</span></span>

<span data-ttu-id="a9450-104">Rappel appelé avant la collecte d’un objet.</span><span class="sxs-lookup"><span data-stu-id="a9450-104">A callback called before collecting an object.</span></span>  
  
## <span data-ttu-id="a9450-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9450-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsObjectBeforeCollectCallback)(  
  _In_ JsRef ref,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="a9450-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9450-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="a9450-107">Objet à collecter.</span><span class="sxs-lookup"><span data-stu-id="a9450-107">The object to be collected.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="a9450-108">État transmis `JsSetObjectBeforeCollectCallback` .</span><span class="sxs-lookup"><span data-stu-id="a9450-108">The state passed to `JsSetObjectBeforeCollectCallback`.</span></span>  
  
## <span data-ttu-id="a9450-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="a9450-109">Remarks</span></span>  
 <span data-ttu-id="a9450-110">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="a9450-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="a9450-111">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="a9450-111">Requirements</span></span>  
 <span data-ttu-id="a9450-112">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a9450-112">jsrt.h</span></span>  
  
## <span data-ttu-id="a9450-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9450-113">See Also</span></span>  
 [<span data-ttu-id="a9450-114">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a9450-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
