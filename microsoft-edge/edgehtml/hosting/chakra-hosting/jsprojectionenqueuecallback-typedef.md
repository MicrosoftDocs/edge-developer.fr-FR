---
description: Le rappel d’application qui est appelé par JsRT lorsqu’une API de projection est exécutée sur un thread différent de celui de l’original.
title: JsProjectionEnqueueCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 47527d5e32076e40a82ab5452c2e0f624e8a2818
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233538"
---
# <span data-ttu-id="0d09d-103">Typedef JsProjectionEnqueueCallback</span><span class="sxs-lookup"><span data-stu-id="0d09d-103">JsProjectionEnqueueCallback Typedef</span></span>

<span data-ttu-id="0d09d-104">Le rappel d’application qui est appelé par JsRT lorsqu’une API de projection est exécutée sur un thread différent de celui de l’original.</span><span class="sxs-lookup"><span data-stu-id="0d09d-104">The application callback which is called by JsRT when a projection API is completed on a different thread than the original.</span></span>  
  
## <span data-ttu-id="0d09d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d09d-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionEnqueueCallback)(  
  _In_ JsProjectionCallback jsCallback,  
  _In_ JsProjectionCallbackContext jsContext,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="0d09d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d09d-106">Parameters</span></span>  
 `jsCallback`  
 <span data-ttu-id="0d09d-107">Rappel à appeler sur le thread d’origine.</span><span class="sxs-lookup"><span data-stu-id="0d09d-107">The callback to be invoked on the original thread.</span></span>  
  
 `jsContext`  
 <span data-ttu-id="0d09d-108">Contexte de l’application.</span><span class="sxs-lookup"><span data-stu-id="0d09d-108">The applications context.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="0d09d-109">Contexte JsRT qui doit être transmis `jsCallback` .</span><span class="sxs-lookup"><span data-stu-id="0d09d-109">The JsRT context that must be passed into `jsCallback`.</span></span>  
  
## <span data-ttu-id="0d09d-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="0d09d-110">Remarks</span></span>  
 <span data-ttu-id="0d09d-111">Nécessite d’appeler JsSetProjectionEnqueueCallback pour recevoir des rappels.</span><span class="sxs-lookup"><span data-stu-id="0d09d-111">Requires calling JsSetProjectionEnqueueCallback to receive callbacks.</span></span>  
  
 <span data-ttu-id="0d09d-112">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="0d09d-112">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="0d09d-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="0d09d-113">Requirements</span></span>  
 <span data-ttu-id="0d09d-114">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0d09d-114">jsrt.h</span></span>  
  
## <span data-ttu-id="0d09d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d09d-115">See Also</span></span>  
 [<span data-ttu-id="0d09d-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0d09d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
