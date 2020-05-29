---
description: Détermine s’il s’agit d’un objet externe.
title: Fonction JsHasExternalData | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasExternalData
helpviewer_keywords:
- JsHasExternalData function
ms.assetid: a077e3ac-4f6f-4d94-8398-f1b5cc4c18e0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 0ca86df09264eb82dac2e928874ca15edd2c8c8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566300"
---
# <span data-ttu-id="6631e-103">Fonction JsHasExternalData</span><span class="sxs-lookup"><span data-stu-id="6631e-103">JsHasExternalData Function</span></span>
<span data-ttu-id="6631e-104">Détermine s’il s’agit d’un objet externe.</span><span class="sxs-lookup"><span data-stu-id="6631e-104">Determines whether an object is an external object.</span></span>  
  
## <span data-ttu-id="6631e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6631e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="6631e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6631e-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="6631e-107">Objet.</span><span class="sxs-lookup"><span data-stu-id="6631e-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="6631e-108">S’il s’agit d’un objet externe.</span><span class="sxs-lookup"><span data-stu-id="6631e-108">Whether the object is an external object.</span></span>  
  
## <span data-ttu-id="6631e-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6631e-109">Return Value</span></span>  
 <span data-ttu-id="6631e-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6631e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6631e-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="6631e-111">Remarks</span></span>  
 <span data-ttu-id="6631e-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="6631e-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="6631e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6631e-113">Requirements</span></span>  
 <span data-ttu-id="6631e-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6631e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6631e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6631e-115">See Also</span></span>  
 [<span data-ttu-id="6631e-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6631e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)