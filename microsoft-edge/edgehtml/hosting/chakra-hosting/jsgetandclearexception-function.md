---
description: Retourne l’exception qui a entraîné l’exécution du contexte actuel dans l’état d’exception et réinitialise l’état d’exception pour le Runtime.
title: Fonction JsGetAndClearException | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetAndClearException
helpviewer_keywords:
- JsGetAndClearException function
ms.assetid: 6aec8a88-41ee-47f6-b5f4-32f3cae6bb7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb296ea351d0466a856d5ac020550ebacc254ac9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233100"
---
# <span data-ttu-id="9d822-103">JsGetAndClearException Function</span><span class="sxs-lookup"><span data-stu-id="9d822-103">JsGetAndClearException Function</span></span>

<span data-ttu-id="9d822-104">Retourne l’exception qui a entraîné l’exécution du contexte actuel dans l’état d’exception et réinitialise l’état d’exception pour le Runtime.</span><span class="sxs-lookup"><span data-stu-id="9d822-104">Returns the exception that caused the runtime of the current context to be in the exception state and resets the exception state for that runtime.</span></span>  
  
## <span data-ttu-id="9d822-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d822-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetAndClearException(  
   _Out_ JsValueRef *exception  
);  
```  
  
#### <span data-ttu-id="9d822-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d822-106">Parameters</span></span>  
 `exception`  
 <span data-ttu-id="9d822-107">Exception pour le runtime du contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="9d822-107">The exception for the runtime of the current context.</span></span>  
  
## <span data-ttu-id="9d822-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9d822-108">Return Value</span></span>  
 <span data-ttu-id="9d822-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9d822-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9d822-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="9d822-110">Remarks</span></span>  
 <span data-ttu-id="9d822-111">Si le runtime du contexte actuel ne se trouve pas dans un état d’exception, cette API renverra `JsErrorInvalidArgument` .</span><span class="sxs-lookup"><span data-stu-id="9d822-111">If the runtime of the current context is not in an exception state, this API will return `JsErrorInvalidArgument`.</span></span> <span data-ttu-id="9d822-112">Si le runtime est désactivé, il renverra une exception indiquant que le script a été arrêté, mais il n’effacera pas l’exception (l’exception sera effacée si le runtime est réactivé à l’aide de `JsEnableRuntimeExecution` ).</span><span class="sxs-lookup"><span data-stu-id="9d822-112">If the runtime is disabled, this will return an exception indicating that the script was terminated, but it will not clear the exception (the exception will be cleared if the runtime is re-enabled using `JsEnableRuntimeExecution`).</span></span>  
  
 <span data-ttu-id="9d822-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="9d822-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9d822-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="9d822-114">Requirements</span></span>  
 <span data-ttu-id="9d822-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9d822-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9d822-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d822-116">See Also</span></span>  
 [<span data-ttu-id="9d822-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9d822-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
