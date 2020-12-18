---
description: Obtient l’ID de propriété associé au symbole.
title: Fonction JsGetPropertyIdFromSymbol | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 190fe4b9-352e-4b10-9d0e-6c6bbd6363e8
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d97f1fb517164d692cdd010f899dc40d2e3596ed
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233360"
---
# <span data-ttu-id="20be3-103">JsGetPropertyIdFromSymbol Function</span><span class="sxs-lookup"><span data-stu-id="20be3-103">JsGetPropertyIdFromSymbol Function</span></span>

<span data-ttu-id="20be3-104">Obtient l’ID de propriété associé au symbole.</span><span class="sxs-lookup"><span data-stu-id="20be3-104">Gets the property ID associated with the symbol.</span></span>  
  
## <span data-ttu-id="20be3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20be3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromSymbol(  
   _In_ JsValueRef symbol,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="20be3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20be3-106">Parameters</span></span>  
 `symbol`  
 <span data-ttu-id="20be3-107">Le symbole dont l’ID de propriété est récupéré.</span><span class="sxs-lookup"><span data-stu-id="20be3-107">The symbol whose property ID is being retrieved.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="20be3-108">ID de propriété pour le symbole donné.</span><span class="sxs-lookup"><span data-stu-id="20be3-108">The property ID for the given symbol.</span></span>  
  
## <span data-ttu-id="20be3-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="20be3-109">Return Value</span></span>  
 <span data-ttu-id="20be3-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="20be3-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="20be3-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="20be3-111">Remarks</span></span>  
 <span data-ttu-id="20be3-112">Les ID de propriété sont spécifiques à un contexte et ne peuvent pas être utilisés dans les contextes.</span><span class="sxs-lookup"><span data-stu-id="20be3-112">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="20be3-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="20be3-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="20be3-114">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="20be3-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="20be3-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="20be3-115">Requirements</span></span>  
 <span data-ttu-id="20be3-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="20be3-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="20be3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20be3-117">See Also</span></span>  
 [<span data-ttu-id="20be3-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="20be3-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
