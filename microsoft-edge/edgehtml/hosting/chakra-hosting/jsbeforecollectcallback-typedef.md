---
description: Rappel appelé avant la collection.
title: JsBeforeCollectCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 58bece47-4e6d-49e7-a93d-b6a8f9928b41
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 23ed386a6a28d356aa80cf85650a981d4836a6b6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232997"
---
# <span data-ttu-id="f954b-103">Typedef JsBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="f954b-103">JsBeforeCollectCallback Typedef</span></span>

<span data-ttu-id="f954b-104">Rappel appelé avant la collection.</span><span class="sxs-lookup"><span data-stu-id="f954b-104">A callback called before collection.</span></span>  
  
## <span data-ttu-id="f954b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f954b-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBeforeCollectCallback)(  
_In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="f954b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f954b-106">Parameters</span></span>  
 <span data-ttu-id="f954b-107">callbackState</span><span class="sxs-lookup"><span data-stu-id="f954b-107">callbackState</span></span>  
 <span data-ttu-id="f954b-108">État transmis à JsSetBeforeCollectCallback.</span><span class="sxs-lookup"><span data-stu-id="f954b-108">The state passed to JsSetBeforeCollectCallback.</span></span>  
  
## <span data-ttu-id="f954b-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="f954b-109">Remarks</span></span>  
 <span data-ttu-id="f954b-110">Utilisez JsSetBeforeCollectCallback pour inscrire ce rappel.</span><span class="sxs-lookup"><span data-stu-id="f954b-110">Use JsSetBeforeCollectCallback to register this callback.</span></span>  
  
## <span data-ttu-id="f954b-111">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="f954b-111">Requirements</span></span>  
 <span data-ttu-id="f954b-112">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f954b-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f954b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f954b-113">See Also</span></span>  
 [<span data-ttu-id="f954b-114">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f954b-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
