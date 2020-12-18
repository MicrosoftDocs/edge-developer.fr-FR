---
description: Le rappel JsRT qui doit être appelé avec le contexte transmis au `JsProjectionEnqueueCallback` thread approprié.
title: JsProjectionCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 211325b536dc84340974b02973f1de9d5749a60a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233303"
---
# <span data-ttu-id="95b9e-103">Typedef JsProjectionCallback</span><span class="sxs-lookup"><span data-stu-id="95b9e-103">JsProjectionCallback Typedef</span></span>

<span data-ttu-id="95b9e-104">Le rappel JsRT qui doit être appelé avec le contexte transmis au `JsProjectionEnqueueCallback` thread approprié.</span><span class="sxs-lookup"><span data-stu-id="95b9e-104">The JsRT callback which should be called with the context passed to `JsProjectionEnqueueCallback` on the correct thread.</span></span>  
  
## <span data-ttu-id="95b9e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95b9e-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionCallback)(  
  _In_ JsProjectionCallbackContext jsContext  
);  
```  
  
#### <span data-ttu-id="95b9e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95b9e-106">Parameters</span></span>  
 `jsContext`  
 <span data-ttu-id="95b9e-107">Nécessite l’appel `JsSetProjectionEnqueueCallback` pour recevoir des rappels.</span><span class="sxs-lookup"><span data-stu-id="95b9e-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
## <span data-ttu-id="95b9e-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="95b9e-108">Remarks</span></span>  
 <span data-ttu-id="95b9e-109">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="95b9e-109">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="95b9e-110">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="95b9e-110">Requirements</span></span>  
 <span data-ttu-id="95b9e-111">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="95b9e-111">jsrt.h</span></span>  
  
## <span data-ttu-id="95b9e-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95b9e-112">See Also</span></span>  
 [<span data-ttu-id="95b9e-113">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="95b9e-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
