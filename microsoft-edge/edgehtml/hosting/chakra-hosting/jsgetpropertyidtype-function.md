---
description: Obtient le type de propriété.
title: Fonction JsGetPropertyIdType | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2b6e85ad-c630-4a07-a759-3b344d06faaa
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 93ee11bf74014361c89aa93bbb58361b426f573f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233359"
---
# <span data-ttu-id="03358-103">JsGetPropertyIdType Function</span><span class="sxs-lookup"><span data-stu-id="03358-103">JsGetPropertyIdType Function</span></span>

<span data-ttu-id="03358-104">Obtient le type de propriété.</span><span class="sxs-lookup"><span data-stu-id="03358-104">Gets the type of property.</span></span>  
  
## <span data-ttu-id="03358-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03358-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdType(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsPropertyIdType* propertyIdType  
);  
```  
  
#### <span data-ttu-id="03358-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03358-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="03358-107">ID de propriété pour obtenir le type de.</span><span class="sxs-lookup"><span data-stu-id="03358-107">The property ID to get the type of.</span></span>  
  
 `propertyIdType`  
 <span data-ttu-id="03358-108">`JsPropertyIdType`ID de propriété donné.</span><span class="sxs-lookup"><span data-stu-id="03358-108">The `JsPropertyIdType` of the given property ID.</span></span>  
  
## <span data-ttu-id="03358-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="03358-109">Return Value</span></span>  
 <span data-ttu-id="03358-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="03358-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="03358-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="03358-111">Remarks</span></span>  
 <span data-ttu-id="03358-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="03358-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="03358-113">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="03358-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="03358-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="03358-114">Requirements</span></span>  
 <span data-ttu-id="03358-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="03358-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="03358-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03358-116">See Also</span></span>  
 [<span data-ttu-id="03358-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="03358-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
