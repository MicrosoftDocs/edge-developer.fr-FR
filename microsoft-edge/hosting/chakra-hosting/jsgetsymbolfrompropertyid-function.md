---
description: Obtient le symbole associé à l’ID de propriété.
title: Fonction JsGetSymbolFromPropertyId | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 0e822cb4-ba9e-44df-bf3a-fae97c354daa
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6902384772f29f80751660ce2d4a295d2ea620ab
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565171"
---
# <span data-ttu-id="4be4d-103">Fonction JsGetSymbolFromPropertyId</span><span class="sxs-lookup"><span data-stu-id="4be4d-103">JsGetSymbolFromPropertyId Function</span></span>
<span data-ttu-id="4be4d-104">Obtient le symbole associé à l’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="4be4d-104">Gets the symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="4be4d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4be4d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetSymbolFromPropertyId(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *symbol  
);  
```  
  
#### <span data-ttu-id="4be4d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4be4d-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="4be4d-107">ID de propriété pour obtenir le symbole.</span><span class="sxs-lookup"><span data-stu-id="4be4d-107">The property ID to get the symbol of.</span></span>  
  
 `symbol`  
 <span data-ttu-id="4be4d-108">Symbole associé à l’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="4be4d-108">The symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="4be4d-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4be4d-109">Return Value</span></span>  
 <span data-ttu-id="4be4d-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4be4d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4be4d-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="4be4d-111">Remarks</span></span>  
 <span data-ttu-id="4be4d-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="4be4d-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="4be4d-113">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4be4d-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="4be4d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4be4d-114">Requirements</span></span>  
 <span data-ttu-id="4be4d-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4be4d-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4be4d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4be4d-116">See Also</span></span>  
 [<span data-ttu-id="4be4d-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4be4d-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)