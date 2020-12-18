---
description: Crée une valeur de chaîne à partir d’un pointeur de chaîne.
title: Fonction JsPointerToString | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsPointerToString
helpviewer_keywords:
- JsPointerToString function
ms.assetid: c71ce07e-4359-450c-afbf-a6ab7d48dddf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c00a060098f0b021afca27b300f3e0578e992cb9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233306"
---
# <span data-ttu-id="7176d-103">JsPointerToString Function</span><span class="sxs-lookup"><span data-stu-id="7176d-103">JsPointerToString Function</span></span>

<span data-ttu-id="7176d-104">Crée une valeur de chaîne à partir d’un pointeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="7176d-104">Creates a string value from a string pointer.</span></span>  
  
## <span data-ttu-id="7176d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7176d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPointerToString(  
   _In_reads_(stringLength) const wchar_t *stringValue,  
   _In_ size_t stringLength,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="7176d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7176d-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="7176d-107">Pointeur de chaîne à convertir en valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="7176d-107">The string pointer to convert to a string value.</span></span>  
  
 `stringLength`  
 <span data-ttu-id="7176d-108">Longueur de la chaîne à convertir.</span><span class="sxs-lookup"><span data-stu-id="7176d-108">The length of the string to convert.</span></span>  
  
 `value`  
 <span data-ttu-id="7176d-109">Nouvelle valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="7176d-109">The new string value.</span></span>  
  
## <span data-ttu-id="7176d-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7176d-110">Return Value</span></span>  
 <span data-ttu-id="7176d-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7176d-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7176d-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="7176d-112">Remarks</span></span>  
 <span data-ttu-id="7176d-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="7176d-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="7176d-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="7176d-114">Requirements</span></span>  
 <span data-ttu-id="7176d-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7176d-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7176d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7176d-116">See Also</span></span>  
 [<span data-ttu-id="7176d-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7176d-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
