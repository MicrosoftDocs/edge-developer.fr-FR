---
description: 'Active l’exécution de script dans un Runtime. '
title: Fonction JsEnableRuntimeExecution | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEnableRuntimeExecution
helpviewer_keywords:
- JsEnableRuntimeExecution function
ms.assetid: daa2036b-aef6-497d-a8ce-5a006b6ed13f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e87191197f70898b2f69d138026edd4e75cd5114
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233174"
---
# <span data-ttu-id="7f081-103">JsEnableRuntimeExecution Function</span><span class="sxs-lookup"><span data-stu-id="7f081-103">JsEnableRuntimeExecution Function</span></span>

<span data-ttu-id="7f081-104">Active l’exécution de script dans un Runtime.</span><span class="sxs-lookup"><span data-stu-id="7f081-104">Enables script execution in a runtime.</span></span>  
  
## <span data-ttu-id="7f081-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f081-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="7f081-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f081-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="7f081-107">Activation du Runtime.</span><span class="sxs-lookup"><span data-stu-id="7f081-107">The runtime to be enabled.</span></span>  
  
## <span data-ttu-id="7f081-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7f081-108">Return Value</span></span>  
 <span data-ttu-id="7f081-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7f081-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7f081-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="7f081-110">Remarks</span></span>  
 <span data-ttu-id="7f081-111">Le fait d’activer l’exécution de script dans un Runtime qui est déjà activé pour l’exécution de script est un non-op.</span><span class="sxs-lookup"><span data-stu-id="7f081-111">Enabling script execution in a runtime that already has script execution enabled is a no-op.</span></span>  
  
## <span data-ttu-id="7f081-112">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="7f081-112">Requirements</span></span>  
 <span data-ttu-id="7f081-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7f081-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7f081-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f081-114">See Also</span></span>  
 [<span data-ttu-id="7f081-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7f081-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
