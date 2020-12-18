---
description: Obtient un descripteur de propriété pour la propriété propre d’un objet.
title: Fonction JsGetOwnPropertyDescriptor | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyDescriptor
helpviewer_keywords:
- JsGetOwnPropertyDescriptor function
ms.assetid: 44c417ce-ab63-44eb-a0ab-19838e3ab34f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 05c7a58fa12d7ca8013c512f40031963ebc8ac18
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233171"
---
# <span data-ttu-id="c342d-103">JsGetOwnPropertyDescriptor Function</span><span class="sxs-lookup"><span data-stu-id="c342d-103">JsGetOwnPropertyDescriptor Function</span></span>

<span data-ttu-id="c342d-104">Obtient un descripteur de propriété pour la propriété propre d’un objet.</span><span class="sxs-lookup"><span data-stu-id="c342d-104">Gets a property descriptor for an object's own property.</span></span>  
  
## <span data-ttu-id="c342d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c342d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyDescriptor(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *propertyDescriptor  
);  
```  
  
#### <span data-ttu-id="c342d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c342d-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="c342d-107">Objet qui comporte la propriété.</span><span class="sxs-lookup"><span data-stu-id="c342d-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="c342d-108">ID de la propriété.</span><span class="sxs-lookup"><span data-stu-id="c342d-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="c342d-109">Le descripteur de propriété.</span><span class="sxs-lookup"><span data-stu-id="c342d-109">The property descriptor.</span></span>  
  
## <span data-ttu-id="c342d-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c342d-110">Return Value</span></span>  
 <span data-ttu-id="c342d-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c342d-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c342d-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="c342d-112">Remarks</span></span>  
 <span data-ttu-id="c342d-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="c342d-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c342d-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="c342d-114">Requirements</span></span>  
 <span data-ttu-id="c342d-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c342d-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c342d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c342d-116">See Also</span></span>  
 [<span data-ttu-id="c342d-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c342d-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
