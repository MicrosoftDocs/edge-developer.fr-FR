---
description: Crée une valeur JavaScript qui est une projection de la transmission `VARIANT` .
title: Fonction JsVariantToValue | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsVariantToValue
helpviewer_keywords:
- JsVariantToValue function
ms.assetid: e8f9eb8b-55b3-4b65-927e-cad5b482edee
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 58c928b519b5a9a678b6cd6ad367e1db2332f021
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233123"
---
# <span data-ttu-id="58f1d-103">JsVariantToValue Function</span><span class="sxs-lookup"><span data-stu-id="58f1d-103">JsVariantToValue Function</span></span>

<span data-ttu-id="58f1d-104">Crée une valeur JavaScript qui est une projection de la transmission `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="58f1d-104">Creates a JavaScript value that is a projection of the passed in `VARIANT`.</span></span>  
  
## <span data-ttu-id="58f1d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58f1d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsVariantToValue(  
   _In_ VARIANT *variant,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="58f1d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58f1d-106">Parameters</span></span>  
 `variant`  
 <span data-ttu-id="58f1d-107">A `VARIANT` à projeter.</span><span class="sxs-lookup"><span data-stu-id="58f1d-107">A `VARIANT` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="58f1d-108">Valeur JavaScript qui est une projection de la `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="58f1d-108">A JavaScript value that is a projection of the `VARIANT`.</span></span>  
  
## <span data-ttu-id="58f1d-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="58f1d-109">Return Value</span></span>  
 <span data-ttu-id="58f1d-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="58f1d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="58f1d-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="58f1d-111">Remarks</span></span>  
 <span data-ttu-id="58f1d-112">La valeur projetée peut être utilisée par le script pour appeler un objet Automation COM à partir d’un script.</span><span class="sxs-lookup"><span data-stu-id="58f1d-112">The projected value can be used by script to call a COM automation object from script.</span></span> <span data-ttu-id="58f1d-113">Les hôtes sont chargés d’appliquer les règles de thread COM.</span><span class="sxs-lookup"><span data-stu-id="58f1d-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="58f1d-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="58f1d-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="58f1d-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="58f1d-115">Requirements</span></span>  
 <span data-ttu-id="58f1d-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="58f1d-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="58f1d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58f1d-117">See Also</span></span>  
 [<span data-ttu-id="58f1d-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="58f1d-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
