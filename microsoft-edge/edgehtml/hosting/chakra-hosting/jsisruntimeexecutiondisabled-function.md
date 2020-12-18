---
description: Renvoie une valeur indiquant si l’exécution du script est désactivée dans le Runtime.
title: Fonction JsIsRuntimeExecutionDisabled | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0ce59c77525abdb2dd6cac71dde1378264395e79
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232798"
---
# <span data-ttu-id="a79ef-103">JsIsRuntimeExecutionDisabled Function</span><span class="sxs-lookup"><span data-stu-id="a79ef-103">JsIsRuntimeExecutionDisabled Function</span></span>

<span data-ttu-id="a79ef-104">Renvoie une valeur indiquant si l’exécution du script est désactivée dans le Runtime.</span><span class="sxs-lookup"><span data-stu-id="a79ef-104">Returns a value that indicates whether script execution is disabled in the runtime.</span></span>  
  
## <span data-ttu-id="a79ef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a79ef-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsRuntimeExecutionDisabled(    _In_ JsRuntimeHandle runtime,    _Out_ bool *isDisabled);  
```  
  
#### <span data-ttu-id="a79ef-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a79ef-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="a79ef-107">Spécifie le runtime pour vérifier si l’exécution est désactivée.</span><span class="sxs-lookup"><span data-stu-id="a79ef-107">Specifies the runtime to check if execution is disabled.</span></span>  
  
 `isDisabled`  
 `true` <span data-ttu-id="a79ef-108">dans le cas contraire, l’exécution est désactivée `false` .</span><span class="sxs-lookup"><span data-stu-id="a79ef-108">if execution is disabled, `false` otherwise.</span></span>  
  
## <span data-ttu-id="a79ef-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a79ef-109">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="a79ef-110">Si l’opération a réussi, le code d’erreur est contraire.</span><span class="sxs-lookup"><span data-stu-id="a79ef-110">if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a79ef-111">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="a79ef-111">Requirements</span></span>  
 <span data-ttu-id="a79ef-112">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a79ef-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a79ef-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a79ef-113">See Also</span></span>  
 [<span data-ttu-id="a79ef-114">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a79ef-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
