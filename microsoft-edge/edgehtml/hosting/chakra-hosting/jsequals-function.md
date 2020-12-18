---
description: Comparez deux valeurs JavaScript pour l’égalité.
title: Fonction JsEquals | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEquals
helpviewer_keywords:
- JsEquals function
ms.assetid: 8377a7b6-12ff-43e4-8cc8-5a5a198a168b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 88f906419e73ed0de6ddde0a872becbd18908997
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233550"
---
# <span data-ttu-id="e58fe-103">JsEquals Function</span><span class="sxs-lookup"><span data-stu-id="e58fe-103">JsEquals Function</span></span>

<span data-ttu-id="e58fe-104">Comparez deux valeurs JavaScript pour l’égalité.</span><span class="sxs-lookup"><span data-stu-id="e58fe-104">Compare two JavaScript values for equality.</span></span>  
  
## <span data-ttu-id="e58fe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e58fe-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="e58fe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e58fe-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="e58fe-107">Premier objet à comparer.</span><span class="sxs-lookup"><span data-stu-id="e58fe-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="e58fe-108">Deuxième objet à comparer.</span><span class="sxs-lookup"><span data-stu-id="e58fe-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="e58fe-109">Si les valeurs sont égales.</span><span class="sxs-lookup"><span data-stu-id="e58fe-109">Whether the values are equal.</span></span>  
  
## <span data-ttu-id="e58fe-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e58fe-110">Return Value</span></span>  
 <span data-ttu-id="e58fe-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e58fe-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e58fe-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="e58fe-112">Remarks</span></span>  
 <span data-ttu-id="e58fe-113">Cette fonction équivaut à l' `==` opérateur dans JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e58fe-113">This function is equivalent to the `==` operator in Javascript.</span></span>  
  
 <span data-ttu-id="e58fe-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="e58fe-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e58fe-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="e58fe-115">Requirements</span></span>  
 <span data-ttu-id="e58fe-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e58fe-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e58fe-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e58fe-117">See Also</span></span>  
 [<span data-ttu-id="e58fe-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e58fe-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
