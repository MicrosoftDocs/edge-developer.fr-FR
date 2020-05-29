---
description: Récupère le pointeur de chaîne d’une valeur de chaîne.
title: Fonction JsStringToPointer | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStringToPointer
helpviewer_keywords:
- JsStringToPointer function
ms.assetid: c7aa7a09-489d-4435-8f8a-aeb62f8875ae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1f5997894c4ea479378a323b230492dde28ab177
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566137"
---
# <span data-ttu-id="d557e-103">Fonction JsStringToPointer</span><span class="sxs-lookup"><span data-stu-id="d557e-103">JsStringToPointer Function</span></span>
<span data-ttu-id="d557e-104">Récupère le pointeur de chaîne d’une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="d557e-104">Retrieves the string pointer of a string value.</span></span>  
  
## <span data-ttu-id="d557e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d557e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStringToPointer(  
   _In_ JsValueRef value,  
   _Outptr_result_buffer_(*stringLength) const wchar_t **stringValue,  
   _Out_ size_t *stringLength  
);  
```  
  
#### <span data-ttu-id="d557e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d557e-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="d557e-107">Valeur de chaîne à convertir en pointeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="d557e-107">The string value to convert to a string pointer.</span></span>  
  
 `stringValue`  
 <span data-ttu-id="d557e-108">Pointeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="d557e-108">The string pointer.</span></span>  
  
 `stringLength`  
 <span data-ttu-id="d557e-109">Longueur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="d557e-109">The length of the string.</span></span>  
  
## <span data-ttu-id="d557e-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d557e-110">Return Value</span></span>  
 <span data-ttu-id="d557e-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d557e-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d557e-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="d557e-112">Remarks</span></span>  
 <span data-ttu-id="d557e-113">Cette fonction récupère le pointeur de chaîne d’une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="d557e-113">This function retrieves the string pointer of a string value.</span></span> <span data-ttu-id="d557e-114">Il échouera avec `JsErrorInvalidArgument` si le type de la valeur n’est pas String.</span><span class="sxs-lookup"><span data-stu-id="d557e-114">It will fail with `JsErrorInvalidArgument` if the type of the value is not string.</span></span> <span data-ttu-id="d557e-115">La durée de vie de la chaîne renvoyée est identique à la durée de vie de la valeur dont elle provient, mais le pointeur de chaîne n’est pas considéré comme une référence à la valeur (et donc elle ne sera pas récupérée par le biais du suivi).</span><span class="sxs-lookup"><span data-stu-id="d557e-115">The lifetime of the string returned will be the same as the lifetime of the value it came from, however the string pointer is not considered a reference to the value (and so will not keep it from being collected).</span></span>  
  
 <span data-ttu-id="d557e-116">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="d557e-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d557e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d557e-117">Requirements</span></span>  
 <span data-ttu-id="d557e-118">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d557e-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d557e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d557e-119">See Also</span></span>  
 [<span data-ttu-id="d557e-120">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d557e-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)