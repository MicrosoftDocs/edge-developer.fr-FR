---
description: Renvoie une valeur qui indique si un objet est extensible ou non.
title: Fonction JsGetExtensionAllowed | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetExtensionAllowed
helpviewer_keywords:
- JsGetExtensionAllowed function
ms.assetid: 839054a1-d643-47d9-89db-6a015bba0d91
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7bc9e3265b48a27d0da4bc4646b2b5e3b1765b86
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233221"
---
# <span data-ttu-id="9c197-103">JsGetExtensionAllowed Function</span><span class="sxs-lookup"><span data-stu-id="9c197-103">JsGetExtensionAllowed Function</span></span>

<span data-ttu-id="9c197-104">Renvoie une valeur qui indique si un objet est extensible ou non.</span><span class="sxs-lookup"><span data-stu-id="9c197-104">Returns a value that indicates whether an object is extensible or not.</span></span>  
  
## <span data-ttu-id="9c197-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c197-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExtensionAllowed(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="9c197-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c197-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="9c197-107">Objet à tester.</span><span class="sxs-lookup"><span data-stu-id="9c197-107">The object to test.</span></span>  
  
 `value`  
 <span data-ttu-id="9c197-108">Si l’objet est extensible ou non.</span><span class="sxs-lookup"><span data-stu-id="9c197-108">Whether the object is extensible or not.</span></span>  
  
## <span data-ttu-id="9c197-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9c197-109">Return Value</span></span>  
 <span data-ttu-id="9c197-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9c197-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9c197-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="9c197-111">Remarks</span></span>  
 <span data-ttu-id="9c197-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="9c197-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9c197-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="9c197-113">Requirements</span></span>  
 <span data-ttu-id="9c197-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9c197-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9c197-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c197-115">See Also</span></span>  
 [<span data-ttu-id="9c197-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9c197-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
