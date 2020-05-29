---
description: Obtient un descripteur de propriété pour la propriété propre d’un objet.
title: Fonction JsGetOwnPropertyDescriptor | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyDescriptor
helpviewer_keywords:
- JsGetOwnPropertyDescriptor function
ms.assetid: 44c417ce-ab63-44eb-a0ab-19838e3ab34f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6f500aec8b892cb2ad437bd7159ab14165a8bfb4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566323"
---
# <span data-ttu-id="d250d-103">Fonction JsGetOwnPropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="d250d-103">JsGetOwnPropertyDescriptor Function</span></span>
<span data-ttu-id="d250d-104">Obtient un descripteur de propriété pour la propriété propre d’un objet.</span><span class="sxs-lookup"><span data-stu-id="d250d-104">Gets a property descriptor for an object's own property.</span></span>  
  
## <span data-ttu-id="d250d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d250d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyDescriptor(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *propertyDescriptor  
);  
```  
  
#### <span data-ttu-id="d250d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d250d-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="d250d-107">Objet qui comporte la propriété.</span><span class="sxs-lookup"><span data-stu-id="d250d-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="d250d-108">ID de la propriété.</span><span class="sxs-lookup"><span data-stu-id="d250d-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="d250d-109">Le descripteur de propriété.</span><span class="sxs-lookup"><span data-stu-id="d250d-109">The property descriptor.</span></span>  
  
## <span data-ttu-id="d250d-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d250d-110">Return Value</span></span>  
 <span data-ttu-id="d250d-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d250d-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d250d-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="d250d-112">Remarks</span></span>  
 <span data-ttu-id="d250d-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="d250d-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d250d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d250d-114">Requirements</span></span>  
 <span data-ttu-id="d250d-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d250d-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d250d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d250d-116">See Also</span></span>  
 [<span data-ttu-id="d250d-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d250d-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)