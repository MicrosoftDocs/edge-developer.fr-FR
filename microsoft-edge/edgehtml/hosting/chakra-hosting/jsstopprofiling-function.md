---
description: Arrête le profilage dans le contexte actuel.
title: Fonction JsStopProfiling | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStopProfiling
helpviewer_keywords:
- JsStopProfiling function
ms.assetid: 3639c04f-a0f9-418b-be39-92f64b4e7ef8
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 02c42afda7e61d71b90a9a1a71aa71cc53584ff8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233167"
---
# <span data-ttu-id="63856-103">JsStopProfiling Function</span><span class="sxs-lookup"><span data-stu-id="63856-103">JsStopProfiling Function</span></span>

<span data-ttu-id="63856-104">Arrête le profilage dans le contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="63856-104">Stops profiling in the current context.</span></span>  
  
## <span data-ttu-id="63856-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63856-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStopProfiling(  
   _In_ HRESULT reason  
);  
```  
  
#### <span data-ttu-id="63856-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63856-106">Parameters</span></span>  
 `reason`  
 <span data-ttu-id="63856-107">La raison pour laquelle vous arrêtez le profilage passe au rappel du profileur.</span><span class="sxs-lookup"><span data-stu-id="63856-107">The reason for stopping profiling to pass to the profiler callback.</span></span>  
  
## <span data-ttu-id="63856-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="63856-108">Return Value</span></span>  
 <span data-ttu-id="63856-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="63856-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="63856-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="63856-110">Remarks</span></span>  
 <span data-ttu-id="63856-111">Ne renvoie pas d’erreur si le profil n’a pas commencé.</span><span class="sxs-lookup"><span data-stu-id="63856-111">Will not return an error if profiling has not started.</span></span>  
  
 <span data-ttu-id="63856-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="63856-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="63856-113">Cette API est prise en charge dans les applications de bureau, mais n’est pas prise en charge dans les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="63856-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="63856-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="63856-114">Requirements</span></span>  
 <span data-ttu-id="63856-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="63856-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="63856-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63856-116">See Also</span></span>  
 [<span data-ttu-id="63856-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="63856-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
