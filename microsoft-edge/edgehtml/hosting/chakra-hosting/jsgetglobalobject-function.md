---
description: Obtient l’objet global du contexte de script actuel.
title: Fonction JsGetGlobalObject | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetGlobalObject
helpviewer_keywords:
- JsGetGlobalObject function
ms.assetid: d3e91e64-1ca3-4d2b-aada-725ded0fd0b1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cda960710180c135b99abd359d0cc76776ff0225
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233218"
---
# <span data-ttu-id="fe98a-103">JsGetGlobalObject Function</span><span class="sxs-lookup"><span data-stu-id="fe98a-103">JsGetGlobalObject Function</span></span>

<span data-ttu-id="fe98a-104">Obtient l’objet global du contexte de script actuel.</span><span class="sxs-lookup"><span data-stu-id="fe98a-104">Gets the global object in the current script context.</span></span>  
  
## <span data-ttu-id="fe98a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe98a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetGlobalObject(  
   _Out_ JsValueRef *globalObject  
);  
```  
  
#### <span data-ttu-id="fe98a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe98a-106">Parameters</span></span>  
 `globalObject`  
 <span data-ttu-id="fe98a-107">Objet global.</span><span class="sxs-lookup"><span data-stu-id="fe98a-107">The global object.</span></span>  
  
## <span data-ttu-id="fe98a-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fe98a-108">Return Value</span></span>  
 <span data-ttu-id="fe98a-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="fe98a-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fe98a-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="fe98a-110">Remarks</span></span>  
 <span data-ttu-id="fe98a-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="fe98a-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="fe98a-112">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="fe98a-112">Requirements</span></span>  
 <span data-ttu-id="fe98a-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fe98a-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fe98a-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe98a-114">See Also</span></span>  
 [<span data-ttu-id="fe98a-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fe98a-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
