---
description: Obtient le runtime auquel appartient le contexte.
title: Fonction JsGetRuntime | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntime
helpviewer_keywords:
- JsGetRuntime function
ms.assetid: 5b62e940-a885-405a-9fdd-0495fb391b95
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6eeb132dd35fcb5104828bef8e8f27334a5f34e4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565179"
---
# <span data-ttu-id="532ed-103">Fonction JsGetRuntime</span><span class="sxs-lookup"><span data-stu-id="532ed-103">JsGetRuntime Function</span></span>
<span data-ttu-id="532ed-104">Obtient le runtime auquel appartient le contexte.</span><span class="sxs-lookup"><span data-stu-id="532ed-104">Gets the runtime that the context belongs to.</span></span>  
  
## <span data-ttu-id="532ed-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="532ed-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntime(  
   _In_ JsContextRef context,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### <span data-ttu-id="532ed-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="532ed-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="532ed-107">Contexte à partir duquel obtenir le Runtime.</span><span class="sxs-lookup"><span data-stu-id="532ed-107">The context to get the runtime from.</span></span>  
  
 `runtime`  
 <span data-ttu-id="532ed-108">Runtime auquel le contexte appartient.</span><span class="sxs-lookup"><span data-stu-id="532ed-108">The runtime the context belongs to.</span></span>  
  
## <span data-ttu-id="532ed-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="532ed-109">Return Value</span></span>  
 <span data-ttu-id="532ed-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="532ed-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="532ed-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="532ed-111">Requirements</span></span>  
 <span data-ttu-id="532ed-112">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="532ed-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="532ed-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="532ed-113">See Also</span></span>  
 [<span data-ttu-id="532ed-114">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="532ed-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)