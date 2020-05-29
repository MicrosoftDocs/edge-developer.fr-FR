---
description: Crée une valeur JavaScript qui est une projection de la transmission `VARIANT` .
title: Fonction JsVariantToValue | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsVariantToValue
helpviewer_keywords:
- JsVariantToValue function
ms.assetid: e8f9eb8b-55b3-4b65-927e-cad5b482edee
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 01796bc38548cf56b500731d899541ef214ec4e3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565124"
---
# <span data-ttu-id="a2bf4-103">Fonction JsVariantToValue</span><span class="sxs-lookup"><span data-stu-id="a2bf4-103">JsVariantToValue Function</span></span>
<span data-ttu-id="a2bf4-104">Crée une valeur JavaScript qui est une projection de la transmission `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="a2bf4-104">Creates a JavaScript value that is a projection of the passed in `VARIANT`.</span></span>  
  
## <span data-ttu-id="a2bf4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2bf4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsVariantToValue(  
   _In_ VARIANT *variant,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="a2bf4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2bf4-106">Parameters</span></span>  
 `variant`  
 <span data-ttu-id="a2bf4-107">A `VARIANT` à projeter.</span><span class="sxs-lookup"><span data-stu-id="a2bf4-107">A `VARIANT` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="a2bf4-108">Valeur JavaScript qui est une projection de la `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="a2bf4-108">A JavaScript value that is a projection of the `VARIANT`.</span></span>  
  
## <span data-ttu-id="a2bf4-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a2bf4-109">Return Value</span></span>  
 <span data-ttu-id="a2bf4-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a2bf4-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a2bf4-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="a2bf4-111">Remarks</span></span>  
 <span data-ttu-id="a2bf4-112">La valeur projetée peut être utilisée par le script pour appeler un objet Automation COM à partir d’un script.</span><span class="sxs-lookup"><span data-stu-id="a2bf4-112">The projected value can be used by script to call a COM automation object from script.</span></span> <span data-ttu-id="a2bf4-113">Les hôtes sont chargés d’appliquer les règles de thread COM.</span><span class="sxs-lookup"><span data-stu-id="a2bf4-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="a2bf4-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="a2bf4-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a2bf4-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2bf4-115">Requirements</span></span>  
 <span data-ttu-id="a2bf4-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a2bf4-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a2bf4-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2bf4-117">See Also</span></span>  
 [<span data-ttu-id="a2bf4-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a2bf4-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)