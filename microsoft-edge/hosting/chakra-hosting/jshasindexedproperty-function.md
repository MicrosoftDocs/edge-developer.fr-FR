---
description: Teste si un objet possède une valeur à l’index spécifié.
title: Fonction JsHasIndexedProperty | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasIndexedProperty
helpviewer_keywords:
- JsHasIndexedProperty function
ms.assetid: 30436a3d-fda0-407e-aba2-142be2310372
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 85d9fa12c44bd1d961ec2a7ba494484873635586
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566294"
---
# <span data-ttu-id="06dca-103">Fonction JsHasIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="06dca-103">JsHasIndexedProperty Function</span></span>
<span data-ttu-id="06dca-104">Teste si un objet possède une valeur à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="06dca-104">Tests whether an object has a value at the specified index.</span></span>  
  
## <span data-ttu-id="06dca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06dca-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="06dca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06dca-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="06dca-107">Objet sur lequel travailler.</span><span class="sxs-lookup"><span data-stu-id="06dca-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="06dca-108">Index à tester.</span><span class="sxs-lookup"><span data-stu-id="06dca-108">The index to test.</span></span>  
  
 `result`  
 <span data-ttu-id="06dca-109">Si l’objet a une valeur à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="06dca-109">Whether the object has an value at the specified index.</span></span>  
  
## <span data-ttu-id="06dca-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="06dca-110">Return Value</span></span>  
 <span data-ttu-id="06dca-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="06dca-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="06dca-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="06dca-112">Remarks</span></span>  
 <span data-ttu-id="06dca-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="06dca-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="06dca-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06dca-114">Requirements</span></span>  
 <span data-ttu-id="06dca-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="06dca-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="06dca-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06dca-116">See Also</span></span>  
 [<span data-ttu-id="06dca-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="06dca-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)