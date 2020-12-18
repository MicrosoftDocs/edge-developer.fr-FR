---
description: Définit l’exécution du contexte actuel sur un état d’exception.
title: Fonction JsSetException | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2c2e3840d2a831db23a525c5d8854b9b2fcfb8c9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233173"
---
# <span data-ttu-id="c459a-103">JsSetException Function</span><span class="sxs-lookup"><span data-stu-id="c459a-103">JsSetException Function</span></span>

<span data-ttu-id="c459a-104">Définit l’exécution du contexte actuel sur un état d’exception.</span><span class="sxs-lookup"><span data-stu-id="c459a-104">Sets the runtime of the current context to an exception state.</span></span>  
  
## <span data-ttu-id="c459a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c459a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetException(  
   _In_ JsValueRef exception  
);  
```  
  
#### <span data-ttu-id="c459a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c459a-106">Parameters</span></span>  
 `exception`  
 <span data-ttu-id="c459a-107">Exception JavaScript à définir pour le runtime du contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="c459a-107">The JavaScript exception to set for the runtime of the current context.</span></span>  
  
## <span data-ttu-id="c459a-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c459a-108">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="c459a-109">Si le moteur a été défini comme état d’exception, il est contraire d’un code d’échec.</span><span class="sxs-lookup"><span data-stu-id="c459a-109">if the engine was set into an exception state, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c459a-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="c459a-110">Remarks</span></span>  
 <span data-ttu-id="c459a-111">Si le runtime du contexte actuel est déjà dans un état d’exception, cette API retourne `JsErrorInExceptionState` .</span><span class="sxs-lookup"><span data-stu-id="c459a-111">If the runtime of the current context is already in an exception state, this API will return `JsErrorInExceptionState`.</span></span>  
  
 <span data-ttu-id="c459a-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="c459a-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c459a-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="c459a-113">Requirements</span></span>  
 <span data-ttu-id="c459a-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c459a-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c459a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c459a-115">See Also</span></span>  
 [<span data-ttu-id="c459a-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c459a-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
