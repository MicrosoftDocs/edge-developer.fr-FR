---
description: Renvoie le prototype d’un objet.
title: Fonction JsGetPrototype | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetPrototype
helpviewer_keywords:
- JsGetPrototype function
ms.assetid: 05d743fc-103e-4a92-86f2-a063f39a2a6f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d64e8b090753e5d0627f0d40ee8745eeadd65227
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233473"
---
# <span data-ttu-id="e3475-103">JsGetPrototype Function</span><span class="sxs-lookup"><span data-stu-id="e3475-103">JsGetPrototype Function</span></span>

<span data-ttu-id="e3475-104">Renvoie le prototype d’un objet.</span><span class="sxs-lookup"><span data-stu-id="e3475-104">Returns the prototype of an object.</span></span>  
  
## <span data-ttu-id="e3475-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3475-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPrototype(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *prototypeObject  
);  
```  
  
#### <span data-ttu-id="e3475-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3475-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="e3475-107">Objet dont le prototype doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="e3475-107">The object whose prototype is to be returned.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="e3475-108">Le prototype de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e3475-108">The object's prototype.</span></span>  
  
## <span data-ttu-id="e3475-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e3475-109">Return Value</span></span>  
 <span data-ttu-id="e3475-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e3475-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e3475-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="e3475-111">Remarks</span></span>  
 <span data-ttu-id="e3475-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="e3475-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e3475-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="e3475-113">Requirements</span></span>  
 <span data-ttu-id="e3475-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e3475-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e3475-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3475-115">See Also</span></span>  
 [<span data-ttu-id="e3475-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e3475-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
