---
description: Démarre le profilage dans le contexte actuel.
title: Fonction JsStartProfiling | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStartProfiling
helpviewer_keywords:
- JsStartProfiling function
ms.assetid: 638da395-42dd-4fc5-b581-819e647e887d
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 332ff04a987e6e7ae5030983af96dd48249e58e2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233166"
---
# <span data-ttu-id="13355-103">JsStartProfiling Function</span><span class="sxs-lookup"><span data-stu-id="13355-103">JsStartProfiling Function</span></span>

<span data-ttu-id="13355-104">Démarre le profilage dans le contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="13355-104">Starts profiling in the current context.</span></span>  
  
## <span data-ttu-id="13355-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13355-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStartProfiling(  
   _In_ IActiveScriptProfilerCallback *callback,  
   _In_ PROFILER_EVENT_MASK eventMask,  
   _In_ unsigned long context  
);  
```  
  
#### <span data-ttu-id="13355-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13355-106">Parameters</span></span>  
 `callback`  
 <span data-ttu-id="13355-107">Rappel de profil à utiliser.</span><span class="sxs-lookup"><span data-stu-id="13355-107">The profiling callback to use.</span></span>  
  
 `eventMask`  
 <span data-ttu-id="13355-108">Événements de profilage avec lesquels effectuer un rappel.</span><span class="sxs-lookup"><span data-stu-id="13355-108">The profiling events to callback with.</span></span>  
  
 `context`  
 <span data-ttu-id="13355-109">Contexte à transmettre au rappel de profilage.</span><span class="sxs-lookup"><span data-stu-id="13355-109">A context to pass to the profiling callback.</span></span>  
  
## <span data-ttu-id="13355-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="13355-110">Return Value</span></span>  
 <span data-ttu-id="13355-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="13355-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="13355-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="13355-112">Remarks</span></span>  
 <span data-ttu-id="13355-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="13355-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="13355-114">Cette API est prise en charge dans les applications de bureau, mais n’est pas prise en charge dans les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="13355-114">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="13355-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="13355-115">Requirements</span></span>  
 <span data-ttu-id="13355-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="13355-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="13355-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13355-117">See Also</span></span>  
 [<span data-ttu-id="13355-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="13355-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
