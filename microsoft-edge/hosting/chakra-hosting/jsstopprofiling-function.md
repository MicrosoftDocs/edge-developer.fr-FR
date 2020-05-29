---
description: Arrête le profilage dans le contexte actuel.
title: Fonction JsStopProfiling | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStopProfiling
helpviewer_keywords:
- JsStopProfiling function
ms.assetid: 3639c04f-a0f9-418b-be39-92f64b4e7ef8
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9d021c7c9849d20283a39d6ecffc89c5b2ea0db0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566135"
---
# <span data-ttu-id="fc3c0-103">Fonction JsStopProfiling</span><span class="sxs-lookup"><span data-stu-id="fc3c0-103">JsStopProfiling Function</span></span>
<span data-ttu-id="fc3c0-104">Arrête le profilage dans le contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="fc3c0-104">Stops profiling in the current context.</span></span>  
  
## <span data-ttu-id="fc3c0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc3c0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStopProfiling(  
   _In_ HRESULT reason  
);  
```  
  
#### <span data-ttu-id="fc3c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc3c0-106">Parameters</span></span>  
 `reason`  
 <span data-ttu-id="fc3c0-107">La raison pour laquelle vous arrêtez le profilage passe au rappel du profileur.</span><span class="sxs-lookup"><span data-stu-id="fc3c0-107">The reason for stopping profiling to pass to the profiler callback.</span></span>  
  
## <span data-ttu-id="fc3c0-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fc3c0-108">Return Value</span></span>  
 <span data-ttu-id="fc3c0-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="fc3c0-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fc3c0-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="fc3c0-110">Remarks</span></span>  
 <span data-ttu-id="fc3c0-111">Ne renvoie pas d’erreur si le profil n’a pas commencé.</span><span class="sxs-lookup"><span data-stu-id="fc3c0-111">Will not return an error if profiling has not started.</span></span>  
  
 <span data-ttu-id="fc3c0-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="fc3c0-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="fc3c0-113">Cette API est prise en charge dans les applications de bureau, mais n’est pas prise en charge dans les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="fc3c0-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="fc3c0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc3c0-114">Requirements</span></span>  
 <span data-ttu-id="fc3c0-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fc3c0-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fc3c0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc3c0-116">See Also</span></span>  
 [<span data-ttu-id="fc3c0-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fc3c0-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)