---
description: Rappel appelé avant la collection.
title: JsBeforeCollectCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 58bece47-4e6d-49e7-a93d-b6a8f9928b41
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 17f279c2d2ffcc8d02819994dddebfc22baa4cab
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565266"
---
# <span data-ttu-id="1a714-103">JsBeforeCollectCallback typedef</span><span class="sxs-lookup"><span data-stu-id="1a714-103">JsBeforeCollectCallback Typedef</span></span>
<span data-ttu-id="1a714-104">Rappel appelé avant la collection.</span><span class="sxs-lookup"><span data-stu-id="1a714-104">A callback called before collection.</span></span>  
  
## <span data-ttu-id="1a714-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a714-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBeforeCollectCallback)(  
_In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="1a714-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a714-106">Parameters</span></span>  
 <span data-ttu-id="1a714-107">callbackState</span><span class="sxs-lookup"><span data-stu-id="1a714-107">callbackState</span></span>  
 <span data-ttu-id="1a714-108">État transmis à JsSetBeforeCollectCallback.</span><span class="sxs-lookup"><span data-stu-id="1a714-108">The state passed to JsSetBeforeCollectCallback.</span></span>  
  
## <span data-ttu-id="1a714-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a714-109">Remarks</span></span>  
 <span data-ttu-id="1a714-110">Utilisez JsSetBeforeCollectCallback pour inscrire ce rappel.</span><span class="sxs-lookup"><span data-stu-id="1a714-110">Use JsSetBeforeCollectCallback to register this callback.</span></span>  
  
## <span data-ttu-id="1a714-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a714-111">Requirements</span></span>  
 <span data-ttu-id="1a714-112">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1a714-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1a714-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a714-113">See Also</span></span>  
 [<span data-ttu-id="1a714-114">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1a714-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)