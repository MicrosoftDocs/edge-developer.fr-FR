---
description: Obtient le type JavaScript d’un JsValueRef.
title: Fonction JsGetValueType | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetValueType
helpviewer_keywords:
- JsGetValueType function
ms.assetid: f403cf7c-c8c0-4a17-bfa9-0302d00e760e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 85dc6644e26017c6085ab64d914a86196cca8080
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566298"
---
# <span data-ttu-id="91847-103">Fonction JsGetValueType</span><span class="sxs-lookup"><span data-stu-id="91847-103">JsGetValueType Function</span></span>
<span data-ttu-id="91847-104">Obtient le type JavaScript d’un JsValueRef.</span><span class="sxs-lookup"><span data-stu-id="91847-104">Gets the JavaScript type of a JsValueRef.</span></span>  
  
## <span data-ttu-id="91847-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91847-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetValueType(  
   _In_ JsValueRef value,  
   _Out_ JsValueType *type  
);  
```  
  
#### <span data-ttu-id="91847-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91847-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="91847-107">Valeur dont le type doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="91847-107">The value whose type is to be returned.</span></span>  
  
 `type`  
 <span data-ttu-id="91847-108">Type de la valeur.</span><span class="sxs-lookup"><span data-stu-id="91847-108">The type of the value.</span></span>  
  
## <span data-ttu-id="91847-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="91847-109">Return Value</span></span>  
 <span data-ttu-id="91847-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="91847-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="91847-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="91847-111">Remarks</span></span>  
 <span data-ttu-id="91847-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="91847-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="91847-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91847-113">Requirements</span></span>  
 <span data-ttu-id="91847-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="91847-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="91847-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91847-115">See Also</span></span>  
 [<span data-ttu-id="91847-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="91847-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)