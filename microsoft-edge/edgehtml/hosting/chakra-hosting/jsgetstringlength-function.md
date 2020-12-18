---
description: Obtient la longueur d’une valeur de chaîne.
title: Fonction JsGetStringLength | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetStringLength
helpviewer_keywords:
- JsGetStringLength function
ms.assetid: e9f9f28c-e644-439c-aee5-7ce362f71347
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 10fd6be4bb839ccb9eb64c99931cdb474e3aa7a2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233544"
---
# <span data-ttu-id="95539-103">JsGetStringLength Function</span><span class="sxs-lookup"><span data-stu-id="95539-103">JsGetStringLength Function</span></span>

<span data-ttu-id="95539-104">Obtient la longueur d’une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="95539-104">Gets the length of a string value.</span></span>  
  
## <span data-ttu-id="95539-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95539-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetStringLength(  
   _In_ JsValueRef stringValue,  
   _Out_ int *length  
);  
```  
  
#### <span data-ttu-id="95539-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95539-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="95539-107">Valeur de chaîne dont la longueur est égale à.</span><span class="sxs-lookup"><span data-stu-id="95539-107">The string value to get the length of.</span></span>  
  
 `length`  
 <span data-ttu-id="95539-108">Longueur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="95539-108">The length of the string.</span></span>  
  
## <span data-ttu-id="95539-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="95539-109">Return Value</span></span>  
 <span data-ttu-id="95539-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="95539-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="95539-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="95539-111">Remarks</span></span>  
 <span data-ttu-id="95539-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="95539-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="95539-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="95539-113">Requirements</span></span>  
 <span data-ttu-id="95539-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="95539-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="95539-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95539-115">See Also</span></span>  
 [<span data-ttu-id="95539-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="95539-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
