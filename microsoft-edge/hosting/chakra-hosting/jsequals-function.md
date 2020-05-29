---
description: Comparez deux valeurs JavaScript pour l’égalité.
title: Fonction JsEquals | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsEquals
helpviewer_keywords:
- JsEquals function
ms.assetid: 8377a7b6-12ff-43e4-8cc8-5a5a198a168b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 84416584a048512ab20754a3b59eb8ec255901c4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566334"
---
# <span data-ttu-id="5755a-103">Fonction JsEquals</span><span class="sxs-lookup"><span data-stu-id="5755a-103">JsEquals Function</span></span>
<span data-ttu-id="5755a-104">Comparez deux valeurs JavaScript pour l’égalité.</span><span class="sxs-lookup"><span data-stu-id="5755a-104">Compare two JavaScript values for equality.</span></span>  
  
## <span data-ttu-id="5755a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5755a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="5755a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5755a-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="5755a-107">Premier objet à comparer.</span><span class="sxs-lookup"><span data-stu-id="5755a-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="5755a-108">Deuxième objet à comparer.</span><span class="sxs-lookup"><span data-stu-id="5755a-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="5755a-109">Si les valeurs sont égales.</span><span class="sxs-lookup"><span data-stu-id="5755a-109">Whether the values are equal.</span></span>  
  
## <span data-ttu-id="5755a-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5755a-110">Return Value</span></span>  
 <span data-ttu-id="5755a-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5755a-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5755a-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="5755a-112">Remarks</span></span>  
 <span data-ttu-id="5755a-113">Cette fonction équivaut à l' `==` opérateur dans JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5755a-113">This function is equivalent to the `==` operator in Javascript.</span></span>  
  
 <span data-ttu-id="5755a-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="5755a-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="5755a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5755a-115">Requirements</span></span>  
 <span data-ttu-id="5755a-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5755a-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5755a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5755a-117">See Also</span></span>  
 [<span data-ttu-id="5755a-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5755a-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)