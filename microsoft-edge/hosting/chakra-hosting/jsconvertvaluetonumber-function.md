---
description: Convertit la valeur en nombre à l’aide de la sémantique JavaScript standard.
title: Fonction JsConvertValueToNumber | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToNumber
helpviewer_keywords:
- JsConvertValueToNumber function
ms.assetid: c47b8653-0591-4863-b8b5-33187b315816
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 3b3f450a58aaf1c434e1d34cd51577e3a5a9ee31
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565250"
---
# <span data-ttu-id="f7d42-103">Fonction JsConvertValueToNumber</span><span class="sxs-lookup"><span data-stu-id="f7d42-103">JsConvertValueToNumber Function</span></span>
<span data-ttu-id="f7d42-104">Convertit la valeur en nombre à l’aide de la sémantique JavaScript standard.</span><span class="sxs-lookup"><span data-stu-id="f7d42-104">Converts the value to number using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="f7d42-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7d42-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToNumber(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *numberValue  
);  
```  
  
#### <span data-ttu-id="f7d42-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7d42-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="f7d42-107">Valeur à convertir.</span><span class="sxs-lookup"><span data-stu-id="f7d42-107">The value to be converted.</span></span>  
  
 `numberValue`  
 <span data-ttu-id="f7d42-108">Valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="f7d42-108">The converted value.</span></span>  
  
## <span data-ttu-id="f7d42-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f7d42-109">Return Value</span></span>  
 <span data-ttu-id="f7d42-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f7d42-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f7d42-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="f7d42-111">Remarks</span></span>  
 <span data-ttu-id="f7d42-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="f7d42-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f7d42-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7d42-113">Requirements</span></span>  
 <span data-ttu-id="f7d42-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f7d42-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f7d42-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7d42-115">See Also</span></span>  
 [<span data-ttu-id="f7d42-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f7d42-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)