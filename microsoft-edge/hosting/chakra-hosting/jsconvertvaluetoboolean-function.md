---
description: Convertit la valeur en valeur booléenne à l’aide d’une sémantique JavaScript standard.
title: Fonction JsConvertValueToBoolean | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToBoolean
helpviewer_keywords:
- JsConvertValueToBoolean function
ms.assetid: 7298ec72-a388-4334-b81b-1691ab4cecf0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 861871a030d5a47621ccaf40b6cd332f42a06583
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565252"
---
# <span data-ttu-id="acb87-103">Fonction JsConvertValueToBoolean</span><span class="sxs-lookup"><span data-stu-id="acb87-103">JsConvertValueToBoolean Function</span></span>
<span data-ttu-id="acb87-104">Convertit la valeur en valeur booléenne à l’aide d’une sémantique JavaScript standard.</span><span class="sxs-lookup"><span data-stu-id="acb87-104">Converts the value to Boolean using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="acb87-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="acb87-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToBoolean(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="acb87-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acb87-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="acb87-107">Valeur à convertir.</span><span class="sxs-lookup"><span data-stu-id="acb87-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="acb87-108">Valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="acb87-108">The converted value.</span></span>  
  
## <span data-ttu-id="acb87-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="acb87-109">Return Value</span></span>  
 <span data-ttu-id="acb87-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="acb87-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="acb87-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="acb87-111">Remarks</span></span>  
 <span data-ttu-id="acb87-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="acb87-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="acb87-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acb87-113">Requirements</span></span>  
 <span data-ttu-id="acb87-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="acb87-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="acb87-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acb87-115">See Also</span></span>  
 [<span data-ttu-id="acb87-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="acb87-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)