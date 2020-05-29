---
description: Supprime un Runtime.
title: Fonction JsDisposeRuntime | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDisposeRuntime
helpviewer_keywords:
- JsDisposeRuntime function
ms.assetid: 0aefde3f-7250-48be-afc5-53ea85c12f30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 89166249616c265ce75ebc43a01c838d607bdd08
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566341"
---
# <span data-ttu-id="3b44e-103">Fonction JsDisposeRuntime</span><span class="sxs-lookup"><span data-stu-id="3b44e-103">JsDisposeRuntime Function</span></span>
<span data-ttu-id="3b44e-104">Supprime un Runtime.</span><span class="sxs-lookup"><span data-stu-id="3b44e-104">Disposes a runtime.</span></span>  
  
## <span data-ttu-id="3b44e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b44e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDisposeRuntime(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="3b44e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b44e-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="3b44e-107">Runtime à supprimer.</span><span class="sxs-lookup"><span data-stu-id="3b44e-107">The runtime to dispose.</span></span>  
  
## <span data-ttu-id="3b44e-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3b44e-108">Return Value</span></span>  
 <span data-ttu-id="3b44e-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3b44e-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3b44e-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="3b44e-110">Remarks</span></span>  
 <span data-ttu-id="3b44e-111">Une fois le runtime supprimé, toutes les ressources qu’il contient sont non valides et ne peuvent pas être utilisées.</span><span class="sxs-lookup"><span data-stu-id="3b44e-111">Once a runtime has been disposed, all resources owned by it are invalid and cannot be used.</span></span> <span data-ttu-id="3b44e-112">Si le runtime est actif (c’est-à-dire s’il a la valeur Current sur un thread particulier), il ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="3b44e-112">If the runtime is active (i.e. it is set to be current on a particular thread), it cannot be disposed.</span></span>  
  
## <span data-ttu-id="3b44e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b44e-113">Requirements</span></span>  
 <span data-ttu-id="3b44e-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3b44e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3b44e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b44e-115">See Also</span></span>  
 [<span data-ttu-id="3b44e-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3b44e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)