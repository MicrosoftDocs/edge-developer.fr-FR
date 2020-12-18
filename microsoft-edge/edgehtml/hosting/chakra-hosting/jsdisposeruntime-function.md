---
description: Supprime un Runtime.
title: Fonction JsDisposeRuntime | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisposeRuntime
helpviewer_keywords:
- JsDisposeRuntime function
ms.assetid: 0aefde3f-7250-48be-afc5-53ea85c12f30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8cff4578415cdf1aaa01b7203ce734cef9115301
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233178"
---
# <span data-ttu-id="f11d0-103">JsDisposeRuntime Function</span><span class="sxs-lookup"><span data-stu-id="f11d0-103">JsDisposeRuntime Function</span></span>

<span data-ttu-id="f11d0-104">Supprime un Runtime.</span><span class="sxs-lookup"><span data-stu-id="f11d0-104">Disposes a runtime.</span></span>  
  
## <span data-ttu-id="f11d0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f11d0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDisposeRuntime(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="f11d0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f11d0-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="f11d0-107">Runtime à supprimer.</span><span class="sxs-lookup"><span data-stu-id="f11d0-107">The runtime to dispose.</span></span>  
  
## <span data-ttu-id="f11d0-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f11d0-108">Return Value</span></span>  
 <span data-ttu-id="f11d0-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f11d0-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f11d0-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="f11d0-110">Remarks</span></span>  
 <span data-ttu-id="f11d0-111">Une fois le runtime supprimé, toutes les ressources qu’il contient sont non valides et ne peuvent pas être utilisées.</span><span class="sxs-lookup"><span data-stu-id="f11d0-111">Once a runtime has been disposed, all resources owned by it are invalid and cannot be used.</span></span> <span data-ttu-id="f11d0-112">Si le runtime est actif (c’est-à-dire s’il a la valeur Current sur un thread particulier), il ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="f11d0-112">If the runtime is active (i.e. it is set to be current on a particular thread), it cannot be disposed.</span></span>  
  
## <span data-ttu-id="f11d0-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="f11d0-113">Requirements</span></span>  
 <span data-ttu-id="f11d0-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f11d0-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f11d0-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f11d0-115">See Also</span></span>  
 [<span data-ttu-id="f11d0-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f11d0-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
