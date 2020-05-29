---
description: Récupère la `double` valeur d’une valeur numérique.
title: Fonction JsNumberToDouble | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsNumberToDouble
helpviewer_keywords:
- JsNumberToDouble function
ms.assetid: 5f52e8b6-2b70-49a3-879a-bd83ebf2ac33
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: fc99e02aa0376bb100b4e1302c29532a57bd539f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565149"
---
# <span data-ttu-id="035f3-103">Fonction JsNumberToDouble</span><span class="sxs-lookup"><span data-stu-id="035f3-103">JsNumberToDouble Function</span></span>
<span data-ttu-id="035f3-104">Récupère la `double` valeur d’une valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="035f3-104">Retrieves the `double` value of a number value.</span></span>  
  
## <span data-ttu-id="035f3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="035f3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToDouble(  
   _In_ JsValueRef value,  
   _Out_ double *doubleValue  
);  
```  
  
#### <span data-ttu-id="035f3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="035f3-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="035f3-107">Valeur numérique à convertir en `double` valeur.</span><span class="sxs-lookup"><span data-stu-id="035f3-107">The number value to convert to a `double` value.</span></span>  
  
 `doubleValue`  
 <span data-ttu-id="035f3-108">`double`Valeur.</span><span class="sxs-lookup"><span data-stu-id="035f3-108">The `double` value.</span></span>  
  
## <span data-ttu-id="035f3-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="035f3-109">Return Value</span></span>  
 <span data-ttu-id="035f3-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="035f3-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="035f3-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="035f3-111">Remarks</span></span>  
 <span data-ttu-id="035f3-112">Cette fonction récupère la valeur d’une valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="035f3-112">This function retrieves the value of a number value.</span></span> <span data-ttu-id="035f3-113">Il échouera avec `JsErrorInvalidArgument` si le type de la valeur n’est pas numérique.</span><span class="sxs-lookup"><span data-stu-id="035f3-113">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="035f3-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="035f3-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="035f3-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="035f3-115">Requirements</span></span>  
 <span data-ttu-id="035f3-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="035f3-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="035f3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="035f3-117">See Also</span></span>  
 [<span data-ttu-id="035f3-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="035f3-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)