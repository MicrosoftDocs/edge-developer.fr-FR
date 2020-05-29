---
description: Convertit la valeur en chaîne à l’aide d’une sémantique JavaScript standard.
title: Fonction JsConvertValueToString | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToString
helpviewer_keywords:
- JsConvertValueToString function
ms.assetid: a97aca04-b2ce-446a-acf4-49cd6777a85c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 21c77ca3050773c07572665c6d58e0ebc05d8ee9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565247"
---
# <span data-ttu-id="13c9e-103">Fonction JsConvertValueToString</span><span class="sxs-lookup"><span data-stu-id="13c9e-103">JsConvertValueToString Function</span></span>
<span data-ttu-id="13c9e-104">Convertit la valeur en chaîne à l’aide d’une sémantique JavaScript standard.</span><span class="sxs-lookup"><span data-stu-id="13c9e-104">Converts the value to string using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="13c9e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13c9e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToString(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *stringValue  
);  
```  
  
#### <span data-ttu-id="13c9e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13c9e-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="13c9e-107">Valeur à convertir.</span><span class="sxs-lookup"><span data-stu-id="13c9e-107">The value to be converted.</span></span>  
  
 `stringValue`  
 <span data-ttu-id="13c9e-108">Valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="13c9e-108">The converted value.</span></span>  
  
## <span data-ttu-id="13c9e-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="13c9e-109">Return Value</span></span>  
 <span data-ttu-id="13c9e-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="13c9e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="13c9e-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="13c9e-111">Remarks</span></span>  
 <span data-ttu-id="13c9e-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="13c9e-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="13c9e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13c9e-113">Requirements</span></span>  
 <span data-ttu-id="13c9e-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="13c9e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="13c9e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13c9e-115">See Also</span></span>  
 [<span data-ttu-id="13c9e-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="13c9e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)