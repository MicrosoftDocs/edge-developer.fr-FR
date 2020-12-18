---
description: Crée un nouvel objet d’erreur ReferenceError JavaScript.
title: Fonction JsCreateReferenceError | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateReferenceError
helpviewer_keywords:
- JsCreateReferenceError function
ms.assetid: 1d0b2339-4bea-4dd0-a46a-4dcbf0be3bd8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fc8f10c443d6ca019c1460c84344bf04513e44b9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233196"
---
# <span data-ttu-id="2bfbd-103">JsCreateReferenceError Function</span><span class="sxs-lookup"><span data-stu-id="2bfbd-103">JsCreateReferenceError Function</span></span>

<span data-ttu-id="2bfbd-104">Crée un nouvel objet d’erreur ReferenceError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-104">Creates a new JavaScript ReferenceError error object.</span></span>
  
## <span data-ttu-id="2bfbd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2bfbd-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateReferenceError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="2bfbd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2bfbd-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="2bfbd-107">Message de l’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="2bfbd-108">Nouvel objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-108">The new error object.</span></span>  
  
## <span data-ttu-id="2bfbd-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2bfbd-109">Return Value</span></span>  
 <span data-ttu-id="2bfbd-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2bfbd-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="2bfbd-111">Remarks</span></span>  
 <span data-ttu-id="2bfbd-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="2bfbd-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="2bfbd-113">Requirements</span></span>  
 <span data-ttu-id="2bfbd-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2bfbd-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2bfbd-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bfbd-115">See Also</span></span>  
 [<span data-ttu-id="2bfbd-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2bfbd-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
