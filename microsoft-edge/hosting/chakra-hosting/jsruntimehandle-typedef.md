---
description: Handle vers un Runtime Chakra.
title: JsRuntimeHandle typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4ccdcf39ec6062db47e1b9de249d75c8804de405
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566256"
---
# <span data-ttu-id="9af81-103">JsRuntimeHandle typedef</span><span class="sxs-lookup"><span data-stu-id="9af81-103">JsRuntimeHandle Typedef</span></span>
<span data-ttu-id="9af81-104">Handle vers un Runtime Chakra.</span><span class="sxs-lookup"><span data-stu-id="9af81-104">A handle to a Chakra runtime.</span></span>  
  
## <span data-ttu-id="9af81-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9af81-105">Syntax</span></span>  
  
```cpp  
typedef void *JsRuntimeHandle;  
```  
  
## <span data-ttu-id="9af81-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="9af81-106">Remarks</span></span>  
 <span data-ttu-id="9af81-107">Chaque Runtime Chakra possède son propre moteur d’exécution indépendant, son compilateur JIT et son segment de mémoire récupéré.</span><span class="sxs-lookup"><span data-stu-id="9af81-107">Each Chakra runtime has its own independent execution engine, JIT compiler, and garbage collected heap.</span></span> <span data-ttu-id="9af81-108">Ainsi, chaque Runtime est complètement isolé des autres runtimes.</span><span class="sxs-lookup"><span data-stu-id="9af81-108">As such, each runtime is completely isolated from other runtimes.</span></span>  
  
 <span data-ttu-id="9af81-109">Les Runtime peuvent être utilisés sur n’importe quel thread, mais un seul thread peut appeler à tout moment dans le Runtime.</span><span class="sxs-lookup"><span data-stu-id="9af81-109">Runtimes can be used on any thread, but only one thread can call into a runtime at any time.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="9af81-110">Contrairement à d’autres références d’objet dans l’API d’hébergement chakra, il n’y a pas de nettoyage de la mémoire car il contient le tas récupéré par le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="9af81-110">A JsRuntimeHandle, unlike other object references in the Chakra hosting API, is not garbage collected since it contains the garbage collected heap itself.</span></span> <span data-ttu-id="9af81-111">Un Runtime restera disponible tant que JsDisposeRuntime n’est pas appelé.</span><span class="sxs-lookup"><span data-stu-id="9af81-111">A runtime will continue to exist until JsDisposeRuntime is called.</span></span>  
  
## <span data-ttu-id="9af81-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9af81-112">Requirements</span></span>  
 <span data-ttu-id="9af81-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9af81-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9af81-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9af81-114">See Also</span></span>  
 [<span data-ttu-id="9af81-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9af81-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)