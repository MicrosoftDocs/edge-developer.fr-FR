---
description: Effectue un `instanceof` test d’opérateur JavaScript.
title: Fonction JsInstanceOf | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 94399a62-b996-4fd2-82ce-1c26e7a4da08
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4d9bf2e4c3da9f83fdf7c0ef4e2c31df04670420
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751974"
---
# <span data-ttu-id="6c3b0-103">JsInstanceOf Function</span><span class="sxs-lookup"><span data-stu-id="6c3b0-103">JsInstanceOf Function</span></span>
<span data-ttu-id="6c3b0-104">Effectue un `instanceof` test d’opérateur JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6c3b0-104">Performs JavaScript `instanceof` operator test.</span></span>  
  
## <span data-ttu-id="6c3b0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c3b0-105">Syntax</span></span>  
  
```cpp  
JsInstanceOf(   
  _In_ JsValueRef object,  
  _In_ JsValueRef constructor,  
  _Out_ bool *result  
);  
  
```  
  
#### <span data-ttu-id="6c3b0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c3b0-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="6c3b0-107">Objet à tester.</span><span class="sxs-lookup"><span data-stu-id="6c3b0-107">The object to test.</span></span>  
  
 `constructor`  
 <span data-ttu-id="6c3b0-108">Fonction Constructor à tester.</span><span class="sxs-lookup"><span data-stu-id="6c3b0-108">The constructor function to test against.</span></span>  
  
 `result`  
 <span data-ttu-id="6c3b0-109">La valeur de la propriété «Object instanceof Constructor».</span><span class="sxs-lookup"><span data-stu-id="6c3b0-109">Whether the "object instanceof constructor" is true.</span></span>  
  
## <span data-ttu-id="6c3b0-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6c3b0-110">Return Value</span></span>  
 <span data-ttu-id="6c3b0-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6c3b0-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6c3b0-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="6c3b0-112">Remarks</span></span>  
 <span data-ttu-id="6c3b0-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="6c3b0-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="6c3b0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c3b0-114">Requirements</span></span>  
 <span data-ttu-id="6c3b0-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6c3b0-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6c3b0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c3b0-116">See Also</span></span>  
 [<span data-ttu-id="6c3b0-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6c3b0-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)