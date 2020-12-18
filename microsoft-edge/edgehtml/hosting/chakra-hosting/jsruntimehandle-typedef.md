---
description: Handle vers un Runtime Chakra.
title: JsRuntimeHandle typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ab08243505b9699fe07ca2e80f7294adf9eb78ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232959"
---
# <span data-ttu-id="32038-103">Typedef JsRuntimeHandle</span><span class="sxs-lookup"><span data-stu-id="32038-103">JsRuntimeHandle Typedef</span></span>

<span data-ttu-id="32038-104">Handle vers un Runtime Chakra.</span><span class="sxs-lookup"><span data-stu-id="32038-104">A handle to a Chakra runtime.</span></span>  
  
## <span data-ttu-id="32038-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32038-105">Syntax</span></span>  
  
```cpp  
typedef void *JsRuntimeHandle;  
```  
  
## <span data-ttu-id="32038-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="32038-106">Remarks</span></span>  
 <span data-ttu-id="32038-107">Chaque Runtime Chakra possède son propre moteur d’exécution indépendant, son compilateur JIT et son segment de mémoire récupéré.</span><span class="sxs-lookup"><span data-stu-id="32038-107">Each Chakra runtime has its own independent execution engine, JIT compiler, and garbage collected heap.</span></span> <span data-ttu-id="32038-108">Ainsi, chaque Runtime est complètement isolé des autres runtimes.</span><span class="sxs-lookup"><span data-stu-id="32038-108">As such, each runtime is completely isolated from other runtimes.</span></span>  
  
 <span data-ttu-id="32038-109">Les Runtime peuvent être utilisés sur n’importe quel thread, mais un seul thread peut appeler à tout moment dans le Runtime.</span><span class="sxs-lookup"><span data-stu-id="32038-109">Runtimes can be used on any thread, but only one thread can call into a runtime at any time.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="32038-110">Contrairement à d’autres références d’objet dans l’API d’hébergement chakra, il n’y a pas de nettoyage de la mémoire car il contient le tas récupéré par le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="32038-110">A JsRuntimeHandle, unlike other object references in the Chakra hosting API, is not garbage collected since it contains the garbage collected heap itself.</span></span> <span data-ttu-id="32038-111">Un Runtime restera disponible tant que JsDisposeRuntime n’est pas appelé.</span><span class="sxs-lookup"><span data-stu-id="32038-111">A runtime will continue to exist until JsDisposeRuntime is called.</span></span>  
  
## <span data-ttu-id="32038-112">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="32038-112">Requirements</span></span>  
 <span data-ttu-id="32038-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="32038-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="32038-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32038-114">See Also</span></span>  
 [<span data-ttu-id="32038-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="32038-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
