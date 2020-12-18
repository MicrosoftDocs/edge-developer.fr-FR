---
description: Convertit la valeur en nombre à l’aide de la sémantique JavaScript standard.
title: Fonction JsConvertValueToNumber | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToNumber
helpviewer_keywords:
- JsConvertValueToNumber function
ms.assetid: c47b8653-0591-4863-b8b5-33187b315816
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8d00950ef3835c6d75f8f55ffe5002b32c6ee160
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232996"
---
# <span data-ttu-id="c5d6d-103">JsConvertValueToNumber Function</span><span class="sxs-lookup"><span data-stu-id="c5d6d-103">JsConvertValueToNumber Function</span></span>

<span data-ttu-id="c5d6d-104">Convertit la valeur en nombre à l’aide de la sémantique JavaScript standard.</span><span class="sxs-lookup"><span data-stu-id="c5d6d-104">Converts the value to number using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="c5d6d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5d6d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToNumber(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *numberValue  
);  
```  
  
#### <span data-ttu-id="c5d6d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5d6d-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="c5d6d-107">Valeur à convertir.</span><span class="sxs-lookup"><span data-stu-id="c5d6d-107">The value to be converted.</span></span>  
  
 `numberValue`  
 <span data-ttu-id="c5d6d-108">Valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="c5d6d-108">The converted value.</span></span>  
  
## <span data-ttu-id="c5d6d-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c5d6d-109">Return Value</span></span>  
 <span data-ttu-id="c5d6d-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c5d6d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c5d6d-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5d6d-111">Remarks</span></span>  
 <span data-ttu-id="c5d6d-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="c5d6d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c5d6d-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="c5d6d-113">Requirements</span></span>  
 <span data-ttu-id="c5d6d-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c5d6d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c5d6d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5d6d-115">See Also</span></span>  
 [<span data-ttu-id="c5d6d-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c5d6d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
