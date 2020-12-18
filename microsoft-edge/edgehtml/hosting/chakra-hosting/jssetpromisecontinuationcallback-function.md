---
description: Définit une fonction de rappel de continuation de promesse qui est appelée par le contexte quand une tâche doit être mise en file d’attente pour exécution future.
title: Fonction JsSetPromiseContinuationCallback | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 6ef0faf4-1500-4bd9-aeca-c208492af8ea
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da928431f05831c95d5bc116dbd129de9cb5f3b4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233212"
---
# <span data-ttu-id="1c062-103">JsSetPromiseContinuationCallback Function</span><span class="sxs-lookup"><span data-stu-id="1c062-103">JsSetPromiseContinuationCallback Function</span></span>

<span data-ttu-id="1c062-104">Définit une fonction de rappel de continuation de promesse qui est appelée par le contexte quand une tâche doit être mise en file d’attente pour exécution future.</span><span class="sxs-lookup"><span data-stu-id="1c062-104">Sets a promise continuation callback function that is called by the context when a task needs to be queued for future execution.</span></span>  
  
## <span data-ttu-id="1c062-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c062-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPromiseContinuationCallback(  
   _In_ JsPromiseContinuationCallback promiseContinuationCallback,  
   _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="1c062-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c062-106">Parameters</span></span>  
 `promiseContinuationCallback`  
 <span data-ttu-id="1c062-107">Fonction de rappel définie.</span><span class="sxs-lookup"><span data-stu-id="1c062-107">The callback function being set.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="1c062-108">État fourni par l’utilisateur qui sera transmis au rappel.</span><span class="sxs-lookup"><span data-stu-id="1c062-108">User provided state that will be passed back to the callback.</span></span>  
  
## <span data-ttu-id="1c062-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1c062-109">Return Value</span></span>  
 <span data-ttu-id="1c062-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1c062-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1c062-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="1c062-111">Remarks</span></span>  
 <span data-ttu-id="1c062-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="1c062-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="1c062-113">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="1c062-113">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="1c062-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="1c062-114">Requirements</span></span>  
 <span data-ttu-id="1c062-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1c062-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1c062-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c062-116">See Also</span></span>  
 [<span data-ttu-id="1c062-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1c062-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
