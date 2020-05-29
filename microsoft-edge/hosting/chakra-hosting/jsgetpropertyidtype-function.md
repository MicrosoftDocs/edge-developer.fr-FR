---
description: Obtient le type de propriété.
title: Fonction JsGetPropertyIdType | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2b6e85ad-c630-4a07-a759-3b344d06faaa
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a43cfc2efd69cc14813ad88850afbf602d477d71
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566311"
---
# <span data-ttu-id="0598e-103">Fonction JsGetPropertyIdType</span><span class="sxs-lookup"><span data-stu-id="0598e-103">JsGetPropertyIdType Function</span></span>
<span data-ttu-id="0598e-104">Obtient le type de propriété.</span><span class="sxs-lookup"><span data-stu-id="0598e-104">Gets the type of property.</span></span>  
  
## <span data-ttu-id="0598e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0598e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdType(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsPropertyIdType* propertyIdType  
);  
```  
  
#### <span data-ttu-id="0598e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0598e-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="0598e-107">ID de propriété pour obtenir le type de.</span><span class="sxs-lookup"><span data-stu-id="0598e-107">The property ID to get the type of.</span></span>  
  
 `propertyIdType`  
 <span data-ttu-id="0598e-108">`JsPropertyIdType`ID de propriété donné.</span><span class="sxs-lookup"><span data-stu-id="0598e-108">The `JsPropertyIdType` of the given property ID.</span></span>  
  
## <span data-ttu-id="0598e-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0598e-109">Return Value</span></span>  
 <span data-ttu-id="0598e-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0598e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0598e-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="0598e-111">Remarks</span></span>  
 <span data-ttu-id="0598e-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="0598e-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="0598e-113">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0598e-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="0598e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0598e-114">Requirements</span></span>  
 <span data-ttu-id="0598e-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0598e-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0598e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0598e-116">See Also</span></span>  
 [<span data-ttu-id="0598e-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0598e-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)