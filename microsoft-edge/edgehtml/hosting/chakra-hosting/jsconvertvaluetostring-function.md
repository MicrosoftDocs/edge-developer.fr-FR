---
description: Convertit la valeur en chaîne à l’aide d’une sémantique JavaScript standard.
title: Fonction JsConvertValueToString | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToString
helpviewer_keywords:
- JsConvertValueToString function
ms.assetid: a97aca04-b2ce-446a-acf4-49cd6777a85c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 499f9555f6385b8458524fb4e14b92339c0aa478
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232978"
---
# <span data-ttu-id="4d4c2-103">JsConvertValueToString Function</span><span class="sxs-lookup"><span data-stu-id="4d4c2-103">JsConvertValueToString Function</span></span>

<span data-ttu-id="4d4c2-104">Convertit la valeur en chaîne à l’aide d’une sémantique JavaScript standard.</span><span class="sxs-lookup"><span data-stu-id="4d4c2-104">Converts the value to string using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="4d4c2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d4c2-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToString(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *stringValue  
);  
```  
  
#### <span data-ttu-id="4d4c2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d4c2-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="4d4c2-107">Valeur à convertir.</span><span class="sxs-lookup"><span data-stu-id="4d4c2-107">The value to be converted.</span></span>  
  
 `stringValue`  
 <span data-ttu-id="4d4c2-108">Valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="4d4c2-108">The converted value.</span></span>  
  
## <span data-ttu-id="4d4c2-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4d4c2-109">Return Value</span></span>  
 <span data-ttu-id="4d4c2-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4d4c2-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4d4c2-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="4d4c2-111">Remarks</span></span>  
 <span data-ttu-id="4d4c2-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="4d4c2-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4d4c2-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="4d4c2-113">Requirements</span></span>  
 <span data-ttu-id="4d4c2-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4d4c2-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4d4c2-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d4c2-115">See Also</span></span>  
 [<span data-ttu-id="4d4c2-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4d4c2-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
