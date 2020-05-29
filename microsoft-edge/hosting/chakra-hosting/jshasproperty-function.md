---
description: Détermine si un objet a une propriété.
title: Fonction JsHasProperty | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasProperty
helpviewer_keywords:
- JsHasProperty function
ms.assetid: 26c94c3d-aae6-4257-8644-df63c7e714fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c6cc195ae02c28500f0a018256d24278ad4b47d8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566293"
---
# <span data-ttu-id="b2f01-103">Fonction JsHasProperty</span><span class="sxs-lookup"><span data-stu-id="b2f01-103">JsHasProperty Function</span></span>
<span data-ttu-id="b2f01-104">Détermine si un objet a une propriété.</span><span class="sxs-lookup"><span data-stu-id="b2f01-104">Determines whether an object has a property.</span></span>  
  
## <span data-ttu-id="b2f01-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2f01-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ bool *hasProperty  
);  
```  
  
#### <span data-ttu-id="b2f01-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2f01-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="b2f01-107">Objet qui pourrait contenir la propriété.</span><span class="sxs-lookup"><span data-stu-id="b2f01-107">The object that may contain the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="b2f01-108">ID de la propriété.</span><span class="sxs-lookup"><span data-stu-id="b2f01-108">The ID of the property.</span></span>  
  
 `hasProperty`  
 <span data-ttu-id="b2f01-109">Si l’objet (ou un prototype) possède la propriété.</span><span class="sxs-lookup"><span data-stu-id="b2f01-109">Whether the object (or a prototype) has the property.</span></span>  
  
## <span data-ttu-id="b2f01-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b2f01-110">Return Value</span></span>  
 <span data-ttu-id="b2f01-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b2f01-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b2f01-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="b2f01-112">Remarks</span></span>  
 <span data-ttu-id="b2f01-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="b2f01-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b2f01-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2f01-114">Requirements</span></span>  
 <span data-ttu-id="b2f01-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b2f01-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b2f01-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2f01-116">See Also</span></span>  
 [<span data-ttu-id="b2f01-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b2f01-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)