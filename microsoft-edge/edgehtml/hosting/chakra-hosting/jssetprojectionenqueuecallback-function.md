---
description: Définit le rappel à utiliser pour rappeler une fin de projection au thread des appelants requis.
title: Fonction JsSetProjectionEnqueueCallback | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c751ccef-20d2-4d41-9568-1c54adf47cdf
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7dfedfeb1df5a97159a211795a2dd072d239bb35
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232957"
---
# <span data-ttu-id="e84d9-103">JsSetProjectionEnqueueCallback Function</span><span class="sxs-lookup"><span data-stu-id="e84d9-103">JsSetProjectionEnqueueCallback Function</span></span>

<span data-ttu-id="e84d9-104">Définit le rappel à utiliser pour rappeler une fin de projection au thread des appelants requis.</span><span class="sxs-lookup"><span data-stu-id="e84d9-104">Sets the callback to be used in order to invoke a projection completion back to the callers required thread.</span></span>  
  
## <span data-ttu-id="e84d9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e84d9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProjectionEnqueueCallback(  
   _In_ JsProjectionEnqueueCallback projectionEnqueueCallback,  
   _In_opt_ void *projectionEnqueueContext);  
  
```  
  
#### <span data-ttu-id="e84d9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e84d9-106">Parameters</span></span>  
 `projectionEnqueueContext`  
 <span data-ttu-id="e84d9-107">Rappel qui sera appelé chaque fois qu’une achèvement de projection se produit sur un thread en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="e84d9-107">The callback that will be invoked any time a projection completion occurs on a background thread.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="e84d9-108">Contexte de l’application fourni à `projectionEnqueueContext` .</span><span class="sxs-lookup"><span data-stu-id="e84d9-108">The application context provided to `projectionEnqueueContext`.</span></span>  
  
## <span data-ttu-id="e84d9-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e84d9-109">Return Value</span></span>  
 <span data-ttu-id="e84d9-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e84d9-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e84d9-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="e84d9-111">Remarks</span></span>  
 <span data-ttu-id="e84d9-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="e84d9-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="e84d9-113">L’appel doit être issu d’un autre thread COM ou d’un autre thread du même MTA.</span><span class="sxs-lookup"><span data-stu-id="e84d9-113">The call should be coming from a different COM apartment or from a different thread in the same MTA.</span></span>  
  
 <span data-ttu-id="e84d9-114">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="e84d9-114">This API is supported only in EdgeHTML mode.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="e84d9-115">PInvoke n’est pas actuellement pris en charge pour cette API.</span><span class="sxs-lookup"><span data-stu-id="e84d9-115">PInvoke is not currently supported for this API.</span></span>  
  
## <span data-ttu-id="e84d9-116">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="e84d9-116">Requirements</span></span>  
 <span data-ttu-id="e84d9-117">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e84d9-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e84d9-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e84d9-118">See Also</span></span>  
 [<span data-ttu-id="e84d9-119">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e84d9-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
