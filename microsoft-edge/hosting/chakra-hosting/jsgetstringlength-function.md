---
description: Obtient la longueur d’une valeur de chaîne.
title: Fonction JsGetStringLength | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetStringLength
helpviewer_keywords:
- JsGetStringLength function
ms.assetid: e9f9f28c-e644-439c-aee5-7ce362f71347
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6b562b2dc58341523910db41fb8b748453b2a836
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565175"
---
# <span data-ttu-id="4f7d5-103">Fonction JsGetStringLength</span><span class="sxs-lookup"><span data-stu-id="4f7d5-103">JsGetStringLength Function</span></span>
<span data-ttu-id="4f7d5-104">Obtient la longueur d’une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="4f7d5-104">Gets the length of a string value.</span></span>  
  
## <span data-ttu-id="4f7d5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f7d5-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetStringLength(  
   _In_ JsValueRef stringValue,  
   _Out_ int *length  
);  
```  
  
#### <span data-ttu-id="4f7d5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f7d5-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="4f7d5-107">Valeur de chaîne dont la longueur est égale à.</span><span class="sxs-lookup"><span data-stu-id="4f7d5-107">The string value to get the length of.</span></span>  
  
 `length`  
 <span data-ttu-id="4f7d5-108">Longueur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="4f7d5-108">The length of the string.</span></span>  
  
## <span data-ttu-id="4f7d5-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4f7d5-109">Return Value</span></span>  
 <span data-ttu-id="4f7d5-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4f7d5-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4f7d5-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="4f7d5-111">Remarks</span></span>  
 <span data-ttu-id="4f7d5-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="4f7d5-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4f7d5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f7d5-113">Requirements</span></span>  
 <span data-ttu-id="4f7d5-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4f7d5-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4f7d5-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f7d5-115">See Also</span></span>  
 [<span data-ttu-id="4f7d5-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4f7d5-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)