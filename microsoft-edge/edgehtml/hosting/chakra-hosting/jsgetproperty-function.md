---
description: Obtient la propriété d’un objet.
title: Fonction JsGetProperty | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetProperty
helpviewer_keywords:
- JsGetProperty function
ms.assetid: 606bc14f-e849-4f88-a148-6660e923c07b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e5731fa3f889fc1b182f88e37ae90c96d3825402
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232780"
---
# <span data-ttu-id="9fcd1-103">JsGetProperty Function</span><span class="sxs-lookup"><span data-stu-id="9fcd1-103">JsGetProperty Function</span></span>

<span data-ttu-id="9fcd1-104">Obtient la propriété d’un objet.</span><span class="sxs-lookup"><span data-stu-id="9fcd1-104">Gets an object's property.</span></span>  
  
## <span data-ttu-id="9fcd1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9fcd1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="9fcd1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9fcd1-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="9fcd1-107">Objet qui contient la propriété.</span><span class="sxs-lookup"><span data-stu-id="9fcd1-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="9fcd1-108">ID de la propriété.</span><span class="sxs-lookup"><span data-stu-id="9fcd1-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="9fcd1-109">Valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="9fcd1-109">The value of the property.</span></span>  
  
## <span data-ttu-id="9fcd1-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9fcd1-110">Return Value</span></span>  
 <span data-ttu-id="9fcd1-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9fcd1-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9fcd1-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="9fcd1-112">Remarks</span></span>  
 <span data-ttu-id="9fcd1-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="9fcd1-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9fcd1-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="9fcd1-114">Requirements</span></span>  
 <span data-ttu-id="9fcd1-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9fcd1-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9fcd1-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fcd1-116">See Also</span></span>  
 [<span data-ttu-id="9fcd1-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9fcd1-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
