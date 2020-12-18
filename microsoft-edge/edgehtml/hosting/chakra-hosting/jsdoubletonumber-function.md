---
description: Crée une valeur numérique à partir d’une valeur double.
title: Fonction JsDoubleToNumber | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDoubleToNumber
helpviewer_keywords:
- JsDoubleToNumber function
ms.assetid: 43eb2ee1-2789-4302-954e-c4087e1ee786
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d3385633f41c2e20c43ca865eaeec763b6ff7f43
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233176"
---
# <span data-ttu-id="d6fcb-103">JsDoubleToNumber Function</span><span class="sxs-lookup"><span data-stu-id="d6fcb-103">JsDoubleToNumber Function</span></span>

<span data-ttu-id="d6fcb-104">Crée une valeur numérique à partir d’une `double` valeur.</span><span class="sxs-lookup"><span data-stu-id="d6fcb-104">Creates a number value from a `double` value.</span></span>  
  
## <span data-ttu-id="d6fcb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6fcb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDoubleToNumber(  
   _In_ double doubleValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="d6fcb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6fcb-106">Parameters</span></span>  
 `doubleValue`  
 <span data-ttu-id="d6fcb-107">La `double` valeur à convertir en nombre.</span><span class="sxs-lookup"><span data-stu-id="d6fcb-107">The `double` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="d6fcb-108">Nouvelle valeur du numéro.</span><span class="sxs-lookup"><span data-stu-id="d6fcb-108">The new number value.</span></span>  
  
## <span data-ttu-id="d6fcb-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d6fcb-109">Return Value</span></span>  
 <span data-ttu-id="d6fcb-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d6fcb-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d6fcb-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="d6fcb-111">Remarks</span></span>  
 <span data-ttu-id="d6fcb-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="d6fcb-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d6fcb-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="d6fcb-113">Requirements</span></span>  
 <span data-ttu-id="d6fcb-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d6fcb-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d6fcb-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6fcb-115">See Also</span></span>  
 [<span data-ttu-id="d6fcb-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d6fcb-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
