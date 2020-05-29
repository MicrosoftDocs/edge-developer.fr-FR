---
description: Obtient l’objet global du contexte de script actuel.
title: Fonction JsGetGlobalObject | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetGlobalObject
helpviewer_keywords:
- JsGetGlobalObject function
ms.assetid: d3e91e64-1ca3-4d2b-aada-725ded0fd0b1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9f8b540485e75ef80d42ba66f031b3e827b475fa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565187"
---
# <span data-ttu-id="a28a9-103">Fonction JsGetGlobalObject</span><span class="sxs-lookup"><span data-stu-id="a28a9-103">JsGetGlobalObject Function</span></span>
<span data-ttu-id="a28a9-104">Obtient l’objet global du contexte de script actuel.</span><span class="sxs-lookup"><span data-stu-id="a28a9-104">Gets the global object in the current script context.</span></span>  
  
## <span data-ttu-id="a28a9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a28a9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetGlobalObject(  
   _Out_ JsValueRef *globalObject  
);  
```  
  
#### <span data-ttu-id="a28a9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a28a9-106">Parameters</span></span>  
 `globalObject`  
 <span data-ttu-id="a28a9-107">Objet global.</span><span class="sxs-lookup"><span data-stu-id="a28a9-107">The global object.</span></span>  
  
## <span data-ttu-id="a28a9-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a28a9-108">Return Value</span></span>  
 <span data-ttu-id="a28a9-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a28a9-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a28a9-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="a28a9-110">Remarks</span></span>  
 <span data-ttu-id="a28a9-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="a28a9-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a28a9-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a28a9-112">Requirements</span></span>  
 <span data-ttu-id="a28a9-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a28a9-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a28a9-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a28a9-114">See Also</span></span>  
 [<span data-ttu-id="a28a9-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a28a9-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)