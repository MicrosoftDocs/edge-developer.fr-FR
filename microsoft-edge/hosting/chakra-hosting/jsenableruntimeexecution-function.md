---
description: 'Active l’exécution de script dans un Runtime. '
title: Fonction JsEnableRuntimeExecution | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsEnableRuntimeExecution
helpviewer_keywords:
- JsEnableRuntimeExecution function
ms.assetid: daa2036b-aef6-497d-a8ce-5a006b6ed13f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: dd8071fd3c120d1c2029a3c7a3d9c39e68c4cfd2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566340"
---
# <span data-ttu-id="cd746-103">Fonction JsEnableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="cd746-103">JsEnableRuntimeExecution Function</span></span>
<span data-ttu-id="cd746-104">Active l’exécution de script dans un Runtime.</span><span class="sxs-lookup"><span data-stu-id="cd746-104">Enables script execution in a runtime.</span></span>  
  
## <span data-ttu-id="cd746-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd746-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="cd746-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd746-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="cd746-107">Activation du Runtime.</span><span class="sxs-lookup"><span data-stu-id="cd746-107">The runtime to be enabled.</span></span>  
  
## <span data-ttu-id="cd746-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cd746-108">Return Value</span></span>  
 <span data-ttu-id="cd746-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="cd746-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="cd746-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="cd746-110">Remarks</span></span>  
 <span data-ttu-id="cd746-111">Le fait d’activer l’exécution de script dans un Runtime qui est déjà activé pour l’exécution de script est un non-op.</span><span class="sxs-lookup"><span data-stu-id="cd746-111">Enabling script execution in a runtime that already has script execution enabled is a no-op.</span></span>  
  
## <span data-ttu-id="cd746-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd746-112">Requirements</span></span>  
 <span data-ttu-id="cd746-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cd746-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cd746-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd746-114">See Also</span></span>  
 [<span data-ttu-id="cd746-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="cd746-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)