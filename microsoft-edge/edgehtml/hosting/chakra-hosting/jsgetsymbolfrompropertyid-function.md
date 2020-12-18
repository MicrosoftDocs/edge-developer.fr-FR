---
description: Obtient le symbole associé à l’ID de propriété.
title: Fonction JsGetSymbolFromPropertyId | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0e822cb4-ba9e-44df-bf3a-fae97c354daa
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 472253aea228ca0374c42d99710a7a7ab528184c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233543"
---
# <span data-ttu-id="03fea-103">JsGetSymbolFromPropertyId Function</span><span class="sxs-lookup"><span data-stu-id="03fea-103">JsGetSymbolFromPropertyId Function</span></span>

<span data-ttu-id="03fea-104">Obtient le symbole associé à l’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="03fea-104">Gets the symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="03fea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03fea-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetSymbolFromPropertyId(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *symbol  
);  
```  
  
#### <span data-ttu-id="03fea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03fea-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="03fea-107">ID de propriété pour obtenir le symbole.</span><span class="sxs-lookup"><span data-stu-id="03fea-107">The property ID to get the symbol of.</span></span>  
  
 `symbol`  
 <span data-ttu-id="03fea-108">Symbole associé à l’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="03fea-108">The symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="03fea-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="03fea-109">Return Value</span></span>  
 <span data-ttu-id="03fea-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="03fea-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="03fea-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="03fea-111">Remarks</span></span>  
 <span data-ttu-id="03fea-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="03fea-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="03fea-113">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="03fea-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="03fea-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="03fea-114">Requirements</span></span>  
 <span data-ttu-id="03fea-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="03fea-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="03fea-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03fea-116">See Also</span></span>  
 [<span data-ttu-id="03fea-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="03fea-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
