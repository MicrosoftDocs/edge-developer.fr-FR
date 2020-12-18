---
description: Convertit la valeur en objet à l’aide de la sémantique JavaScript standard.
title: Fonction JsConvertValueToObject | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToObject
helpviewer_keywords:
- JsConvertValueToObject function
ms.assetid: 6528b28a-1d2b-417f-bf78-bf05547c52e1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6f3676b512585b0750c994bcfcdf9d2e6e4e1cc3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232979"
---
# <span data-ttu-id="72d85-103">JsConvertValueToObject Function</span><span class="sxs-lookup"><span data-stu-id="72d85-103">JsConvertValueToObject Function</span></span>

<span data-ttu-id="72d85-104">Convertit la valeur en objet à l’aide de la sémantique JavaScript standard.</span><span class="sxs-lookup"><span data-stu-id="72d85-104">Converts the value to object using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="72d85-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72d85-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToObject(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="72d85-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72d85-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="72d85-107">Valeur à convertir.</span><span class="sxs-lookup"><span data-stu-id="72d85-107">The value to be converted.</span></span>  
  
 `object`  
 <span data-ttu-id="72d85-108">Valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="72d85-108">The converted value.</span></span>  
  
## <span data-ttu-id="72d85-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="72d85-109">Return Value</span></span>  
 <span data-ttu-id="72d85-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="72d85-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="72d85-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="72d85-111">Remarks</span></span>  
 <span data-ttu-id="72d85-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="72d85-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="72d85-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="72d85-113">Requirements</span></span>  
 <span data-ttu-id="72d85-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="72d85-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="72d85-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72d85-115">See Also</span></span>  
 [<span data-ttu-id="72d85-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="72d85-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
