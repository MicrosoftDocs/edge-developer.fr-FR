---
description: Définit une fonction de rappel de continuation de promesse qui est appelée par le contexte quand une tâche doit être mise en file d’attente pour exécution future.
title: Fonction JsSetPromiseContinuationCallback | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 6ef0faf4-1500-4bd9-aeca-c208492af8ea
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9438bf05d879b0c2014c0a4d49d374d26eff3fb4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566236"
---
# <span data-ttu-id="d0350-103">Fonction JsSetPromiseContinuationCallback</span><span class="sxs-lookup"><span data-stu-id="d0350-103">JsSetPromiseContinuationCallback Function</span></span>
<span data-ttu-id="d0350-104">Définit une fonction de rappel de continuation de promesse qui est appelée par le contexte quand une tâche doit être mise en file d’attente pour exécution future.</span><span class="sxs-lookup"><span data-stu-id="d0350-104">Sets a promise continuation callback function that is called by the context when a task needs to be queued for future execution.</span></span>  
  
## <span data-ttu-id="d0350-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0350-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPromiseContinuationCallback(  
   _In_ JsPromiseContinuationCallback promiseContinuationCallback,  
   _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="d0350-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0350-106">Parameters</span></span>  
 `promiseContinuationCallback`  
 <span data-ttu-id="d0350-107">Fonction de rappel définie.</span><span class="sxs-lookup"><span data-stu-id="d0350-107">The callback function being set.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="d0350-108">État fourni par l’utilisateur qui sera transmis au rappel.</span><span class="sxs-lookup"><span data-stu-id="d0350-108">User provided state that will be passed back to the callback.</span></span>  
  
## <span data-ttu-id="d0350-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d0350-109">Return Value</span></span>  
 <span data-ttu-id="d0350-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d0350-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d0350-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="d0350-111">Remarks</span></span>  
 <span data-ttu-id="d0350-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="d0350-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="d0350-113">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="d0350-113">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="d0350-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0350-114">Requirements</span></span>  
 <span data-ttu-id="d0350-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d0350-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d0350-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0350-116">See Also</span></span>  
 [<span data-ttu-id="d0350-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d0350-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)