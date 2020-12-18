---
description: Définit la propriété propre d’un nouvel objet à partir d’un descripteur de propriété.
title: Fonction JsDefineProperty | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDefineProperty
helpviewer_keywords:
- JsDefineProperty function
ms.assetid: b2cf48d6-eb40-457c-aa8b-b16a50dc5d6a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a35dd6214190fa558c50cbb743b0f2b92b5e00b3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233324"
---
# <span data-ttu-id="7a60f-103">JsDefineProperty Function</span><span class="sxs-lookup"><span data-stu-id="7a60f-103">JsDefineProperty Function</span></span>

<span data-ttu-id="7a60f-104">Définit la propriété propre d’un nouvel objet à partir d’un descripteur de propriété.</span><span class="sxs-lookup"><span data-stu-id="7a60f-104">Defines a new object's own property from a property descriptor.</span></span>  
  
## <span data-ttu-id="7a60f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a60f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDefineProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef propertyDescriptor,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="7a60f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a60f-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="7a60f-107">Objet qui comporte la propriété.</span><span class="sxs-lookup"><span data-stu-id="7a60f-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="7a60f-108">ID de la propriété.</span><span class="sxs-lookup"><span data-stu-id="7a60f-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="7a60f-109">Le descripteur de propriété.</span><span class="sxs-lookup"><span data-stu-id="7a60f-109">The property descriptor.</span></span>  
  
 `result`  
 <span data-ttu-id="7a60f-110">Si la propriété a été définie.</span><span class="sxs-lookup"><span data-stu-id="7a60f-110">Whether the property was defined.</span></span>  
  
## <span data-ttu-id="7a60f-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7a60f-111">Return Value</span></span>  
 <span data-ttu-id="7a60f-112">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7a60f-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7a60f-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="7a60f-113">Remarks</span></span>  
 <span data-ttu-id="7a60f-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="7a60f-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="7a60f-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="7a60f-115">Requirements</span></span>  
 <span data-ttu-id="7a60f-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7a60f-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7a60f-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a60f-117">See Also</span></span>  
 [<span data-ttu-id="7a60f-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7a60f-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
