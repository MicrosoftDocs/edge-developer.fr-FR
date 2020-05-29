---
description: Crée une valeur numérique à partir d’une `int` valeur.
title: Fonction JsIntToNumber | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 1393c4ac-7189-4e9c-8e54-b0e041c22112
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: dd8f51638292346ec3058f9537d72b8fd21bebc6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565163"
---
# <span data-ttu-id="fb97d-103">Fonction JsIntToNumber</span><span class="sxs-lookup"><span data-stu-id="fb97d-103">JsIntToNumber Function</span></span>
<span data-ttu-id="fb97d-104">Crée une valeur numérique à partir d’une `int` valeur.</span><span class="sxs-lookup"><span data-stu-id="fb97d-104">Creates a number value from an `int` value.</span></span>  
  
## <span data-ttu-id="fb97d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb97d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIntToNumber(  
   _In_ int intValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="fb97d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb97d-106">Parameters</span></span>  
 `intValue`  
 <span data-ttu-id="fb97d-107">La `int` valeur à convertir en nombre.</span><span class="sxs-lookup"><span data-stu-id="fb97d-107">The `int` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="fb97d-108">Nouvelle valeur du numéro.</span><span class="sxs-lookup"><span data-stu-id="fb97d-108">The new number value.</span></span>  
  
## <span data-ttu-id="fb97d-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fb97d-109">Return Value</span></span>  
 <span data-ttu-id="fb97d-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="fb97d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fb97d-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="fb97d-111">Remarks</span></span>  
 <span data-ttu-id="fb97d-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="fb97d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="fb97d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb97d-113">Requirements</span></span>  
 <span data-ttu-id="fb97d-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fb97d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fb97d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb97d-115">See Also</span></span>  
 [<span data-ttu-id="fb97d-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fb97d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)