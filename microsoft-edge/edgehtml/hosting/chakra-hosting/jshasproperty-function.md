---
description: Détermine si un objet a une propriété.
title: Fonction JsHasProperty | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasProperty
helpviewer_keywords:
- JsHasProperty function
ms.assetid: 26c94c3d-aae6-4257-8644-df63c7e714fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e45ecfaafb06c49a6a3773eb798ee93a19fd6d6e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233185"
---
# <span data-ttu-id="40330-103">JsHasProperty Function</span><span class="sxs-lookup"><span data-stu-id="40330-103">JsHasProperty Function</span></span>

<span data-ttu-id="40330-104">Détermine si un objet a une propriété.</span><span class="sxs-lookup"><span data-stu-id="40330-104">Determines whether an object has a property.</span></span>  
  
## <span data-ttu-id="40330-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40330-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ bool *hasProperty  
);  
```  
  
#### <span data-ttu-id="40330-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40330-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="40330-107">Objet qui pourrait contenir la propriété.</span><span class="sxs-lookup"><span data-stu-id="40330-107">The object that may contain the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="40330-108">ID de la propriété.</span><span class="sxs-lookup"><span data-stu-id="40330-108">The ID of the property.</span></span>  
  
 `hasProperty`  
 <span data-ttu-id="40330-109">Si l’objet (ou un prototype) possède la propriété.</span><span class="sxs-lookup"><span data-stu-id="40330-109">Whether the object (or a prototype) has the property.</span></span>  
  
## <span data-ttu-id="40330-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="40330-110">Return Value</span></span>  
 <span data-ttu-id="40330-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="40330-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="40330-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="40330-112">Remarks</span></span>  
 <span data-ttu-id="40330-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="40330-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="40330-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="40330-114">Requirements</span></span>  
 <span data-ttu-id="40330-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="40330-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="40330-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40330-116">See Also</span></span>  
 [<span data-ttu-id="40330-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="40330-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
