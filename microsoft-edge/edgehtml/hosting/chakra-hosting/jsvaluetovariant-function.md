---
description: Initialise la valeur transmise en `VARIANT` tant que projection d’une valeur JavaScript.
title: Fonction JsValueToVariant | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f383f2d8bc3aab70b4a361b370698cd71cb714d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233126"
---
# <span data-ttu-id="eb12e-103">JsValueToVariant Function</span><span class="sxs-lookup"><span data-stu-id="eb12e-103">JsValueToVariant Function</span></span>

<span data-ttu-id="eb12e-104">Initialise la valeur transmise en `VARIANT` tant que projection d’une valeur JavaScript.</span><span class="sxs-lookup"><span data-stu-id="eb12e-104">Initializes the passed in `VARIANT` as a projection of a JavaScript value.</span></span>  
  
## <span data-ttu-id="eb12e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb12e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsValueToVariant(  
   _In_ JsValueRef object,  
   _Out_ VARIANT *variant  
);  
```  
  
#### <span data-ttu-id="eb12e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb12e-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="eb12e-107">Valeur JavaScript à projeter en tant que `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="eb12e-107">A JavaScript value to project as a `VARIANT`.</span></span>  
  
 `variant`  
 <span data-ttu-id="eb12e-108">Pointeur vers un `VARIANT` struct qui sera initialisé comme une projection.</span><span class="sxs-lookup"><span data-stu-id="eb12e-108">A pointer to a `VARIANT` struct that will be initialized as a projection.</span></span>  
  
## <span data-ttu-id="eb12e-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eb12e-109">Return Value</span></span>  
  
## <span data-ttu-id="eb12e-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="eb12e-110">Remarks</span></span>  
 <span data-ttu-id="eb12e-111">La projection `VARIANT` peut être utilisée par les clients com Automation pour appeler l’objet JavaScript projeté.</span><span class="sxs-lookup"><span data-stu-id="eb12e-111">The projection `VARIANT` can be used by COM automation clients to call into the projected JavaScript object.</span></span>  
  
 <span data-ttu-id="eb12e-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="eb12e-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="eb12e-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="eb12e-113">Requirements</span></span>  
 <span data-ttu-id="eb12e-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="eb12e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="eb12e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb12e-115">See Also</span></span>  
 [<span data-ttu-id="eb12e-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="eb12e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
