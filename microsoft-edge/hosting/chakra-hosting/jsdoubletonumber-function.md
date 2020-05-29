---
description: Crée une valeur numérique à partir d’une valeur double.
title: Fonction JsDoubleToNumber | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDoubleToNumber
helpviewer_keywords:
- JsDoubleToNumber function
ms.assetid: 43eb2ee1-2789-4302-954e-c4087e1ee786
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c33adbe217f27f77e348fc56e87c4587c6a6ec4c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566338"
---
# <span data-ttu-id="a4a51-103">Fonction JsDoubleToNumber</span><span class="sxs-lookup"><span data-stu-id="a4a51-103">JsDoubleToNumber Function</span></span>
<span data-ttu-id="a4a51-104">Crée une valeur numérique à partir d’une `double` valeur.</span><span class="sxs-lookup"><span data-stu-id="a4a51-104">Creates a number value from a `double` value.</span></span>  
  
## <span data-ttu-id="a4a51-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4a51-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDoubleToNumber(  
   _In_ double doubleValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="a4a51-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4a51-106">Parameters</span></span>  
 `doubleValue`  
 <span data-ttu-id="a4a51-107">La `double` valeur à convertir en nombre.</span><span class="sxs-lookup"><span data-stu-id="a4a51-107">The `double` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="a4a51-108">Nouvelle valeur du numéro.</span><span class="sxs-lookup"><span data-stu-id="a4a51-108">The new number value.</span></span>  
  
## <span data-ttu-id="a4a51-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a4a51-109">Return Value</span></span>  
 <span data-ttu-id="a4a51-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a4a51-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a4a51-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="a4a51-111">Remarks</span></span>  
 <span data-ttu-id="a4a51-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="a4a51-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a4a51-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4a51-113">Requirements</span></span>  
 <span data-ttu-id="a4a51-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a4a51-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a4a51-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4a51-115">See Also</span></span>  
 [<span data-ttu-id="a4a51-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a4a51-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)