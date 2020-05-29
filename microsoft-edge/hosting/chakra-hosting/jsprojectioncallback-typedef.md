---
description: Le rappel JsRT qui doit être appelé avec le contexte transmis au `JsProjectionEnqueueCallback` thread approprié.
title: JsProjectionCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b30f9a7dc4671896eeacecbf58ef88f0383e9e7e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565144"
---
# <span data-ttu-id="8e92d-103">JsProjectionCallback typedef</span><span class="sxs-lookup"><span data-stu-id="8e92d-103">JsProjectionCallback Typedef</span></span>
<span data-ttu-id="8e92d-104">Le rappel JsRT qui doit être appelé avec le contexte transmis au `JsProjectionEnqueueCallback` thread approprié.</span><span class="sxs-lookup"><span data-stu-id="8e92d-104">The JsRT callback which should be called with the context passed to `JsProjectionEnqueueCallback` on the correct thread.</span></span>  
  
## <span data-ttu-id="8e92d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e92d-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionCallback)(  
  _In_ JsProjectionCallbackContext jsContext  
);  
```  
  
#### <span data-ttu-id="8e92d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e92d-106">Parameters</span></span>  
 `jsContext`  
 <span data-ttu-id="8e92d-107">Nécessite l’appel `JsSetProjectionEnqueueCallback` pour recevoir des rappels.</span><span class="sxs-lookup"><span data-stu-id="8e92d-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
## <span data-ttu-id="8e92d-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="8e92d-108">Remarks</span></span>  
 <span data-ttu-id="8e92d-109">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="8e92d-109">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="8e92d-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e92d-110">Requirements</span></span>  
 <span data-ttu-id="8e92d-111">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8e92d-111">jsrt.h</span></span>  
  
## <span data-ttu-id="8e92d-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e92d-112">See Also</span></span>  
 [<span data-ttu-id="8e92d-113">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8e92d-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)