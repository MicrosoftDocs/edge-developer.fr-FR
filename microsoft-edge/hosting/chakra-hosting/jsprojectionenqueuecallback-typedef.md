---
description: Le rappel d’application qui est appelé par JsRT lorsqu’une API de projection est exécutée sur un thread différent de celui de l’original.
title: JsProjectionEnqueueCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 064a7d1077ae5222e44ab08ebe0592bb97b1f2af
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565143"
---
# <span data-ttu-id="a3fe0-103">JsProjectionEnqueueCallback typedef</span><span class="sxs-lookup"><span data-stu-id="a3fe0-103">JsProjectionEnqueueCallback Typedef</span></span>
<span data-ttu-id="a3fe0-104">Le rappel d’application qui est appelé par JsRT lorsqu’une API de projection est exécutée sur un thread différent de celui de l’original.</span><span class="sxs-lookup"><span data-stu-id="a3fe0-104">The application callback which is called by JsRT when a projection API is completed on a different thread than the original.</span></span>  
  
## <span data-ttu-id="a3fe0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3fe0-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionEnqueueCallback)(  
  _In_ JsProjectionCallback jsCallback,  
  _In_ JsProjectionCallbackContext jsContext,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="a3fe0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3fe0-106">Parameters</span></span>  
 `jsCallback`  
 <span data-ttu-id="a3fe0-107">Rappel à appeler sur le thread d’origine.</span><span class="sxs-lookup"><span data-stu-id="a3fe0-107">The callback to be invoked on the original thread.</span></span>  
  
 `jsContext`  
 <span data-ttu-id="a3fe0-108">Contexte de l’application.</span><span class="sxs-lookup"><span data-stu-id="a3fe0-108">The applications context.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="a3fe0-109">Contexte JsRT qui doit être transmis `jsCallback` .</span><span class="sxs-lookup"><span data-stu-id="a3fe0-109">The JsRT context that must be passed into `jsCallback`.</span></span>  
  
## <span data-ttu-id="a3fe0-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="a3fe0-110">Remarks</span></span>  
 <span data-ttu-id="a3fe0-111">Nécessite d’appeler JsSetProjectionEnqueueCallback pour recevoir des rappels.</span><span class="sxs-lookup"><span data-stu-id="a3fe0-111">Requires calling JsSetProjectionEnqueueCallback to receive callbacks.</span></span>  
  
 <span data-ttu-id="a3fe0-112">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="a3fe0-112">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="a3fe0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3fe0-113">Requirements</span></span>  
 <span data-ttu-id="a3fe0-114">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a3fe0-114">jsrt.h</span></span>  
  
## <span data-ttu-id="a3fe0-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3fe0-115">See Also</span></span>  
 [<span data-ttu-id="a3fe0-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a3fe0-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)