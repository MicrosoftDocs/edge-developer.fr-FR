---
description: Convertit la valeur en valeur booléenne à l’aide d’une sémantique JavaScript standard.
title: Fonction JsConvertValueToBoolean | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToBoolean
helpviewer_keywords:
- JsConvertValueToBoolean function
ms.assetid: 7298ec72-a388-4334-b81b-1691ab4cecf0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d2e109690fc8a7a98a1ecb84d6f5abf6a646162b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232993"
---
# <span data-ttu-id="17e78-103">JsConvertValueToBoolean Function</span><span class="sxs-lookup"><span data-stu-id="17e78-103">JsConvertValueToBoolean Function</span></span>

<span data-ttu-id="17e78-104">Convertit la valeur en valeur booléenne à l’aide d’une sémantique JavaScript standard.</span><span class="sxs-lookup"><span data-stu-id="17e78-104">Converts the value to Boolean using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="17e78-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17e78-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToBoolean(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="17e78-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17e78-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="17e78-107">Valeur à convertir.</span><span class="sxs-lookup"><span data-stu-id="17e78-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="17e78-108">Valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="17e78-108">The converted value.</span></span>  
  
## <span data-ttu-id="17e78-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="17e78-109">Return Value</span></span>  
 <span data-ttu-id="17e78-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="17e78-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="17e78-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="17e78-111">Remarks</span></span>  
 <span data-ttu-id="17e78-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="17e78-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="17e78-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="17e78-113">Requirements</span></span>  
 <span data-ttu-id="17e78-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="17e78-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="17e78-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17e78-115">See Also</span></span>  
 [<span data-ttu-id="17e78-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="17e78-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
