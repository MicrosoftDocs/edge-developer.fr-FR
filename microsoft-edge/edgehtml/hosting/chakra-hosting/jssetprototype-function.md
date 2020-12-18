---
description: Définit le prototype d’un objet.
title: Fonction JsSetPrototype | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 88e1e421-4ae5-4e3b-b377-19256cc80e9f
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 860a7b8d85e043c87d554e09de50d0cb642b273a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232958"
---
# <span data-ttu-id="9ea61-103">JsSetPrototype Function</span><span class="sxs-lookup"><span data-stu-id="9ea61-103">JsSetPrototype Function</span></span>

<span data-ttu-id="9ea61-104">Définit le prototype d’un objet.</span><span class="sxs-lookup"><span data-stu-id="9ea61-104">Sets the prototype of an object.</span></span>  
  
## <span data-ttu-id="9ea61-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ea61-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPrototype(  
   _In_ JsValueRef object,  
   _In_ JsValueRef prototypeObject  
);  
```  
  
#### <span data-ttu-id="9ea61-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ea61-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="9ea61-107">Objet dont le prototype doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="9ea61-107">The object whose prototype is to be changed.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="9ea61-108">Le nouveau prototype de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9ea61-108">The object's new prototype.</span></span>  
  
## <span data-ttu-id="9ea61-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9ea61-109">Return Value</span></span>  
 <span data-ttu-id="9ea61-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9ea61-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9ea61-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="9ea61-111">Remarks</span></span>  
 <span data-ttu-id="9ea61-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="9ea61-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9ea61-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="9ea61-113">Requirements</span></span>  
 <span data-ttu-id="9ea61-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9ea61-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9ea61-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ea61-115">See Also</span></span>  
 [<span data-ttu-id="9ea61-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9ea61-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
