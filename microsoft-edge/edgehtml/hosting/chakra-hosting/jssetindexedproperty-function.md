---
description: Définissez la valeur à l’index spécifié d’un objet.
title: Fonction JsSetIndexedProperty | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetIndexedProperty
helpviewer_keywords:
- JsSetIndexedProperty function
ms.assetid: ccbc5bf4-d99b-485c-ab25-d2bd1ed2142e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1fa961750fa5db262e1512d8d26572280d5e726c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232955"
---
# <span data-ttu-id="6a2c4-103">JsSetIndexedProperty Function</span><span class="sxs-lookup"><span data-stu-id="6a2c4-103">JsSetIndexedProperty Function</span></span>

<span data-ttu-id="6a2c4-104">Définissez la valeur à l’index spécifié d’un objet.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-104">Set the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="6a2c4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a2c4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _In_ JsValueRef value  
);  
```  
  
#### <span data-ttu-id="6a2c4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a2c4-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="6a2c4-107">Objet sur lequel travailler.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="6a2c4-108">Index à définir.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-108">The index to set.</span></span>  
  
 `value`  
 <span data-ttu-id="6a2c4-109">Valeur à définir.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-109">The value to set.</span></span>  
  
## <span data-ttu-id="6a2c4-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6a2c4-110">Return Value</span></span>  
 <span data-ttu-id="6a2c4-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6a2c4-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="6a2c4-112">Remarks</span></span>  
 <span data-ttu-id="6a2c4-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="6a2c4-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="6a2c4-114">Requirements</span></span>  
 <span data-ttu-id="6a2c4-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6a2c4-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6a2c4-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a2c4-116">See Also</span></span>  
 [<span data-ttu-id="6a2c4-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6a2c4-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
