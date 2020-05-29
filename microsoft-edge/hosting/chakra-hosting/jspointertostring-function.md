---
description: Crée une valeur de chaîne à partir d’un pointeur de chaîne.
title: Fonction JsPointerToString | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsPointerToString
helpviewer_keywords:
- JsPointerToString function
ms.assetid: c71ce07e-4359-450c-afbf-a6ab7d48dddf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b3c5b2d6439244bc9584e15c361412c8a1e87557
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566281"
---
# <span data-ttu-id="05f33-103">Fonction JsPointerToString</span><span class="sxs-lookup"><span data-stu-id="05f33-103">JsPointerToString Function</span></span>
<span data-ttu-id="05f33-104">Crée une valeur de chaîne à partir d’un pointeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="05f33-104">Creates a string value from a string pointer.</span></span>  
  
## <span data-ttu-id="05f33-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05f33-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPointerToString(  
   _In_reads_(stringLength) const wchar_t *stringValue,  
   _In_ size_t stringLength,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="05f33-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05f33-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="05f33-107">Pointeur de chaîne à convertir en valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="05f33-107">The string pointer to convert to a string value.</span></span>  
  
 `stringLength`  
 <span data-ttu-id="05f33-108">Longueur de la chaîne à convertir.</span><span class="sxs-lookup"><span data-stu-id="05f33-108">The length of the string to convert.</span></span>  
  
 `value`  
 <span data-ttu-id="05f33-109">Nouvelle valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="05f33-109">The new string value.</span></span>  
  
## <span data-ttu-id="05f33-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="05f33-110">Return Value</span></span>  
 <span data-ttu-id="05f33-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="05f33-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="05f33-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="05f33-112">Remarks</span></span>  
 <span data-ttu-id="05f33-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="05f33-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="05f33-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05f33-114">Requirements</span></span>  
 <span data-ttu-id="05f33-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="05f33-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="05f33-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05f33-116">See Also</span></span>  
 [<span data-ttu-id="05f33-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="05f33-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)