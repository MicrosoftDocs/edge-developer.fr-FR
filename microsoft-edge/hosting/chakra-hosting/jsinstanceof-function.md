---
description: Effectue un `instanceof` test d’opérateur JavaScript.
title: Fonction JsInstanceOf | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 94399a62-b996-4fd2-82ce-1c26e7a4da08
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 3a7e2397abe5dcb25346e583a0fdab301b8b45f4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565164"
---
# <span data-ttu-id="5d5a7-103">Fonction JsInstanceOf</span><span class="sxs-lookup"><span data-stu-id="5d5a7-103">JsInstanceOf Function</span></span>
<span data-ttu-id="5d5a7-104">Effectue un `instanceof` test d’opérateur JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5d5a7-104">Performs JavaScript `instanceof` operator test.</span></span>  
  
## <span data-ttu-id="5d5a7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d5a7-105">Syntax</span></span>  
  
```cpp  
JsInstanceOf(   
  _In_ JsValueRef object,  
  _In_ JsValueRef constructor,  
  _Out_ bool *result  
);  
  
```  
  
#### <span data-ttu-id="5d5a7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d5a7-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="5d5a7-107">Objet à tester.</span><span class="sxs-lookup"><span data-stu-id="5d5a7-107">The object to test.</span></span>  
  
 `constructor`  
 <span data-ttu-id="5d5a7-108">Fonction Constructor à tester.</span><span class="sxs-lookup"><span data-stu-id="5d5a7-108">The constructor function to test against.</span></span>  
  
 `result`  
 <span data-ttu-id="5d5a7-109">La valeur de la propriété «Object instanceof Constructor».</span><span class="sxs-lookup"><span data-stu-id="5d5a7-109">Whether the "object instanceof constructor" is true.</span></span>  
  
## <span data-ttu-id="5d5a7-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5d5a7-110">Return Value</span></span>  
 <span data-ttu-id="5d5a7-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5d5a7-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5d5a7-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="5d5a7-112">Remarks</span></span>  
 <span data-ttu-id="5d5a7-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="5d5a7-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="5d5a7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d5a7-114">Requirements</span></span>  
 <span data-ttu-id="5d5a7-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5d5a7-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5d5a7-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d5a7-116">See Also</span></span>  
 [<span data-ttu-id="5d5a7-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5d5a7-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)