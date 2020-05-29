---
description: Détermine si le runtime du contexte actuel est dans un état d’exception.
title: Fonction JsHasException | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasException
helpviewer_keywords:
- JsHasException function
ms.assetid: ac7da3ce-c746-4154-bbb8-bcb0859a8d5b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 25ddb8f9cc407dd414a6cd2210c315eb4dd7b141
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566297"
---
# <span data-ttu-id="51d10-103">Fonction JsHasException</span><span class="sxs-lookup"><span data-stu-id="51d10-103">JsHasException Function</span></span>
<span data-ttu-id="51d10-104">Détermine si le runtime du contexte actuel est dans un état d’exception.</span><span class="sxs-lookup"><span data-stu-id="51d10-104">Determines whether the runtime of the current context is in an exception state.</span></span>  
  
## <span data-ttu-id="51d10-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51d10-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasException(  
   _Out_ bool *hasException  
);  
```  
  
#### <span data-ttu-id="51d10-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51d10-106">Parameters</span></span>  
 `hasException`  
 <span data-ttu-id="51d10-107">Si le runtime du contexte actuel est dans l’état de l’exception.</span><span class="sxs-lookup"><span data-stu-id="51d10-107">Whether the runtime of the current context is in the exception state.</span></span>  
  
## <span data-ttu-id="51d10-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="51d10-108">Return Value</span></span>  
 <span data-ttu-id="51d10-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="51d10-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="51d10-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="51d10-110">Remarks</span></span>  
 <span data-ttu-id="51d10-111">Si un appel dans le runtime génère une exception (soit suite à l’exécution d’un script, soit en raison d’un échec de conversion, par exemple), le runtime est placé dans un «état d’exception».</span><span class="sxs-lookup"><span data-stu-id="51d10-111">If a call into the runtime results in an exception (either as the result of running a script or due to something like a conversion failure), the runtime is placed into an "exception state."</span></span> <span data-ttu-id="51d10-112">Tous les appels dans n’importe quel contexte créé par le runtime (à l’exception des API d’exception) échoueront `JsErrorInExceptionState` tant que l’exception n’aura pas été effacée.</span><span class="sxs-lookup"><span data-stu-id="51d10-112">All calls into any context created by the runtime (except for the exception APIs) will fail with `JsErrorInExceptionState` until the exception is cleared.</span></span>  
  
 <span data-ttu-id="51d10-113">Si le runtime du contexte actuel est dans l’état de l’exception lorsqu’un rappel est retourné dans le moteur, le moteur lèvera automatiquement l’exception.</span><span class="sxs-lookup"><span data-stu-id="51d10-113">If the runtime of the current context is in the exception state when a callback returns into the engine, the engine will automatically rethrow the exception.</span></span>  
  
 <span data-ttu-id="51d10-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="51d10-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="51d10-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51d10-115">Requirements</span></span>  
 <span data-ttu-id="51d10-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="51d10-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="51d10-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51d10-117">See Also</span></span>  
 [<span data-ttu-id="51d10-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="51d10-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)