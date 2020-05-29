---
description: Effectue un nettoyage de la mémoire complet.
title: Fonction JsCollectGarbage | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCollectGarbage
helpviewer_keywords:
- JsCollectGarbage function
ms.assetid: 995c79a5-6e18-45be-81ff-2a5d3348edb8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1702ad960a0a2f366e97b8a994abd0700cec50e7
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565259"
---
# <span data-ttu-id="2b09e-103">Fonction JsCollectGarbage</span><span class="sxs-lookup"><span data-stu-id="2b09e-103">JsCollectGarbage Function</span></span>
<span data-ttu-id="2b09e-104">Effectue un nettoyage de la mémoire complet.</span><span class="sxs-lookup"><span data-stu-id="2b09e-104">Performs a full garbage collection.</span></span>  
  
## <span data-ttu-id="2b09e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b09e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCollectGarbage(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="2b09e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b09e-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="2b09e-107">Runtime dans lequel le nettoyage de la mémoire sera effectué.</span><span class="sxs-lookup"><span data-stu-id="2b09e-107">The runtime in which the garbage collection will be performed.</span></span>  
  
## <span data-ttu-id="2b09e-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2b09e-108">Return Value</span></span>  
 <span data-ttu-id="2b09e-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2b09e-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2b09e-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b09e-110">Requirements</span></span>  
 <span data-ttu-id="2b09e-111">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2b09e-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2b09e-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b09e-112">See Also</span></span>  
 [<span data-ttu-id="2b09e-113">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2b09e-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)