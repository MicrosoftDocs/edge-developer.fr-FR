---
description: Obtient l’ID de propriété associé au symbole.
title: Fonction JsGetPropertyIdFromSymbol | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 190fe4b9-352e-4b10-9d0e-6c6bbd6363e8
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 0d11dbaf25b85e2bcd85a0cf2bac1b499fd4fa3e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566313"
---
# <span data-ttu-id="28725-103">Fonction JsGetPropertyIdFromSymbol</span><span class="sxs-lookup"><span data-stu-id="28725-103">JsGetPropertyIdFromSymbol Function</span></span>
<span data-ttu-id="28725-104">Obtient l’ID de propriété associé au symbole.</span><span class="sxs-lookup"><span data-stu-id="28725-104">Gets the property ID associated with the symbol.</span></span>  
  
## <span data-ttu-id="28725-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28725-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromSymbol(  
   _In_ JsValueRef symbol,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="28725-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28725-106">Parameters</span></span>  
 `symbol`  
 <span data-ttu-id="28725-107">Le symbole dont l’ID de propriété est récupéré.</span><span class="sxs-lookup"><span data-stu-id="28725-107">The symbol whose property ID is being retrieved.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="28725-108">ID de propriété pour le symbole donné.</span><span class="sxs-lookup"><span data-stu-id="28725-108">The property ID for the given symbol.</span></span>  
  
## <span data-ttu-id="28725-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="28725-109">Return Value</span></span>  
 <span data-ttu-id="28725-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="28725-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="28725-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="28725-111">Remarks</span></span>  
 <span data-ttu-id="28725-112">Les ID de propriété sont spécifiques à un contexte et ne peuvent pas être utilisés dans les contextes.</span><span class="sxs-lookup"><span data-stu-id="28725-112">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="28725-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="28725-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="28725-114">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="28725-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="28725-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28725-115">Requirements</span></span>  
 <span data-ttu-id="28725-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="28725-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="28725-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28725-117">See Also</span></span>  
 [<span data-ttu-id="28725-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="28725-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)