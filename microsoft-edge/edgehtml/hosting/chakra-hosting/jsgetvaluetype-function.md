---
description: Obtient le type JavaScript d’un JsValueRef.
title: Fonction JsGetValueType | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetValueType
helpviewer_keywords:
- JsGetValueType function
ms.assetid: f403cf7c-c8c0-4a17-bfa9-0302d00e760e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b2e9937ca13bf2a680a4a33c07020d06c53efdf3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232842"
---
# <span data-ttu-id="ead83-103">JsGetValueType Function</span><span class="sxs-lookup"><span data-stu-id="ead83-103">JsGetValueType Function</span></span>

<span data-ttu-id="ead83-104">Obtient le type JavaScript d’un JsValueRef.</span><span class="sxs-lookup"><span data-stu-id="ead83-104">Gets the JavaScript type of a JsValueRef.</span></span>  
  
## <span data-ttu-id="ead83-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ead83-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetValueType(  
   _In_ JsValueRef value,  
   _Out_ JsValueType *type  
);  
```  
  
#### <span data-ttu-id="ead83-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ead83-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="ead83-107">Valeur dont le type doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="ead83-107">The value whose type is to be returned.</span></span>  
  
 `type`  
 <span data-ttu-id="ead83-108">Type de la valeur.</span><span class="sxs-lookup"><span data-stu-id="ead83-108">The type of the value.</span></span>  
  
## <span data-ttu-id="ead83-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ead83-109">Return Value</span></span>  
 <span data-ttu-id="ead83-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ead83-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ead83-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="ead83-111">Remarks</span></span>  
 <span data-ttu-id="ead83-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="ead83-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ead83-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="ead83-113">Requirements</span></span>  
 <span data-ttu-id="ead83-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ead83-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ead83-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ead83-115">See Also</span></span>  
 [<span data-ttu-id="ead83-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ead83-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
