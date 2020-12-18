---
description: Crée une valeur booléenne à partir d’une `bool` valeur.
title: Fonction JsBoolToBoolean | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsBoolToBoolean
helpviewer_keywords:
- JsBoolToBoolean function
ms.assetid: 24322ea3-0638-40a3-9b4c-fc912ebed3ff
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3d6ec9f85d53e0d78c6bbe1c7d3282971831717b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232994"
---
# <span data-ttu-id="1aede-103">JsBoolToBoolean Function</span><span class="sxs-lookup"><span data-stu-id="1aede-103">JsBoolToBoolean Function</span></span>

<span data-ttu-id="1aede-104">Crée une valeur booléenne à partir d’une `bool` valeur.</span><span class="sxs-lookup"><span data-stu-id="1aede-104">Creates a Boolean value from a `bool` value.</span></span>  
  
## <span data-ttu-id="1aede-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1aede-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode JsBoolToBoolean(  
   _In_ bool value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="1aede-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1aede-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="1aede-107">Valeur à convertir.</span><span class="sxs-lookup"><span data-stu-id="1aede-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="1aede-108">Valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="1aede-108">The converted value.</span></span>  
  
## <span data-ttu-id="1aede-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1aede-109">Return Value</span></span>  
 <span data-ttu-id="1aede-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1aede-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1aede-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="1aede-111">Remarks</span></span>  
 <span data-ttu-id="1aede-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="1aede-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="1aede-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="1aede-113">Requirements</span></span>  
 <span data-ttu-id="1aede-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1aede-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1aede-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1aede-115">See Also</span></span>  
 [<span data-ttu-id="1aede-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1aede-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
