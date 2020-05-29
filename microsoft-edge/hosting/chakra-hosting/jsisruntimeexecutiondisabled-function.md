---
description: Renvoie une valeur indiquant si l’exécution du script est désactivée dans le Runtime.
title: Fonction JsIsRuntimeExecutionDisabled | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6968a31c9acab70589fe58c86cc566e631778c3c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565156"
---
# <span data-ttu-id="e81f6-103">Fonction JsIsRuntimeExecutionDisabled</span><span class="sxs-lookup"><span data-stu-id="e81f6-103">JsIsRuntimeExecutionDisabled Function</span></span>
<span data-ttu-id="e81f6-104">Renvoie une valeur indiquant si l’exécution du script est désactivée dans le Runtime.</span><span class="sxs-lookup"><span data-stu-id="e81f6-104">Returns a value that indicates whether script execution is disabled in the runtime.</span></span>  
  
## <span data-ttu-id="e81f6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e81f6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsRuntimeExecutionDisabled(    _In_ JsRuntimeHandle runtime,    _Out_ bool *isDisabled);  
```  
  
#### <span data-ttu-id="e81f6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e81f6-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="e81f6-107">Spécifie le runtime pour vérifier si l’exécution est désactivée.</span><span class="sxs-lookup"><span data-stu-id="e81f6-107">Specifies the runtime to check if execution is disabled.</span></span>  
  
 `isDisabled`  
 `true` <span data-ttu-id="e81f6-108">dans le cas contraire, l’exécution est désactivée `false` .</span><span class="sxs-lookup"><span data-stu-id="e81f6-108">if execution is disabled, `false` otherwise.</span></span>  
  
## <span data-ttu-id="e81f6-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e81f6-109">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="e81f6-110">Si l’opération a réussi, le code d’erreur est contraire.</span><span class="sxs-lookup"><span data-stu-id="e81f6-110">if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e81f6-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e81f6-111">Requirements</span></span>  
 <span data-ttu-id="e81f6-112">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e81f6-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e81f6-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e81f6-113">See Also</span></span>  
 [<span data-ttu-id="e81f6-114">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e81f6-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)