---
description: Obtient l’utilisation de la mémoire actuelle pour un Runtime.
title: Fonction JsGetRuntimeMemoryUsage | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryUsage
helpviewer_keywords:
- JsGetRuntimeMemoryUsage function
ms.assetid: b9bd4146-bfbc-4cb1-a0e9-a0ded7fb09bd
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9ec8472132b4c50b279ee95f36995bf46c0e29e5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565172"
---
# <span data-ttu-id="c76f6-103">Fonction JsGetRuntimeMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="c76f6-103">JsGetRuntimeMemoryUsage Function</span></span>
<span data-ttu-id="c76f6-104">Obtient l’utilisation de la mémoire actuelle pour un Runtime.</span><span class="sxs-lookup"><span data-stu-id="c76f6-104">Gets the current memory usage for a runtime.</span></span>  
  
## <span data-ttu-id="c76f6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c76f6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryUsage(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryUsage  
);  
```  
  
#### <span data-ttu-id="c76f6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c76f6-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="c76f6-107">Le runtime dont l’utilisation de la mémoire doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="c76f6-107">The runtime whose memory usage is to be retrieved.</span></span>  
  
 `memoryUsage`  
 <span data-ttu-id="c76f6-108">L’utilisation de la mémoire actuelle du runtime, en octets.</span><span class="sxs-lookup"><span data-stu-id="c76f6-108">The runtime's current memory usage, in bytes.</span></span>  
  
## <span data-ttu-id="c76f6-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c76f6-109">Return Value</span></span>  
 <span data-ttu-id="c76f6-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c76f6-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c76f6-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="c76f6-111">Remarks</span></span>  
 <span data-ttu-id="c76f6-112">L’utilisation de la mémoire peut être toujours Récupérée, même si le runtime est actif ou non sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="c76f6-112">Memory usage can be always be retrieved, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="c76f6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c76f6-113">Requirements</span></span>  
 <span data-ttu-id="c76f6-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c76f6-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c76f6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c76f6-115">See Also</span></span>  
 [<span data-ttu-id="c76f6-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c76f6-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)