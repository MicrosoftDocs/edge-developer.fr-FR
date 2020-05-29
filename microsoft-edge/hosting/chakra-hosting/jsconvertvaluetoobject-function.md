---
description: Convertit la valeur en objet à l’aide de la sémantique JavaScript standard.
title: Fonction JsConvertValueToObject | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToObject
helpviewer_keywords:
- JsConvertValueToObject function
ms.assetid: 6528b28a-1d2b-417f-bf78-bf05547c52e1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6a8b1a8933cdcaaf250a2e28ed8fc758ea66cc0e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565249"
---
# <span data-ttu-id="ebf2a-103">Fonction JsConvertValueToObject</span><span class="sxs-lookup"><span data-stu-id="ebf2a-103">JsConvertValueToObject Function</span></span>
<span data-ttu-id="ebf2a-104">Convertit la valeur en objet à l’aide de la sémantique JavaScript standard.</span><span class="sxs-lookup"><span data-stu-id="ebf2a-104">Converts the value to object using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="ebf2a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebf2a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToObject(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="ebf2a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebf2a-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="ebf2a-107">Valeur à convertir.</span><span class="sxs-lookup"><span data-stu-id="ebf2a-107">The value to be converted.</span></span>  
  
 `object`  
 <span data-ttu-id="ebf2a-108">Valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="ebf2a-108">The converted value.</span></span>  
  
## <span data-ttu-id="ebf2a-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ebf2a-109">Return Value</span></span>  
 <span data-ttu-id="ebf2a-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ebf2a-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ebf2a-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="ebf2a-111">Remarks</span></span>  
 <span data-ttu-id="ebf2a-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="ebf2a-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ebf2a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebf2a-113">Requirements</span></span>  
 <span data-ttu-id="ebf2a-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ebf2a-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ebf2a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebf2a-115">See Also</span></span>  
 [<span data-ttu-id="ebf2a-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ebf2a-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)