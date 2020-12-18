---
description: Obtient le contexte de script actuel sur le thread.
title: Fonction JsGetCurrentContext | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetCurrentContext
helpviewer_keywords:
- JsGetCurrentContext function
ms.assetid: dd5fe0fa-d1e5-4af6-809e-e655a27519b5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a43b9a6d4413ef1dc1b66321d6078aef84a0645f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233226"
---
# <span data-ttu-id="1e3e6-103">JsGetCurrentContext Function</span><span class="sxs-lookup"><span data-stu-id="1e3e6-103">JsGetCurrentContext Function</span></span>

<span data-ttu-id="1e3e6-104">Obtient le contexte de script actuel sur le thread.</span><span class="sxs-lookup"><span data-stu-id="1e3e6-104">Gets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="1e3e6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e3e6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetCurrentContext(  
   _Out_ JsContextRef *currentContext  
);  
```  
  
#### <span data-ttu-id="1e3e6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e3e6-106">Parameters</span></span>  
 `currentContext`  
 <span data-ttu-id="1e3e6-107">Contexte de script actuel sur le thread, null s’il n’y a aucun contexte de script actuel.</span><span class="sxs-lookup"><span data-stu-id="1e3e6-107">The current script context on the thread, null if there is no current script context.</span></span>  
  
## <span data-ttu-id="1e3e6-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1e3e6-108">Return Value</span></span>  
 <span data-ttu-id="1e3e6-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1e3e6-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1e3e6-110">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="1e3e6-110">Requirements</span></span>  
 <span data-ttu-id="1e3e6-111">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1e3e6-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1e3e6-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e3e6-112">See Also</span></span>  
 [<span data-ttu-id="1e3e6-113">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1e3e6-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
