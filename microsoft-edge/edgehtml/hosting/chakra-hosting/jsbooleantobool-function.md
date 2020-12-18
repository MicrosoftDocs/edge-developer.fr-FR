---
description: Récupère la `bool` valeur d’une valeur booléenne.
title: Fonction JsBooleanToBool | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsBooleanToBool
helpviewer_keywords:
- JsBooleanToBool function
ms.assetid: ab16ac71-fe47-475d-a7ee-46e4643dee60
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 36bf2dc32b94466d8cdea37886e86a42c4ec01d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232990"
---
# <span data-ttu-id="11921-103">JsBooleanToBool Function</span><span class="sxs-lookup"><span data-stu-id="11921-103">JsBooleanToBool Function</span></span>

<span data-ttu-id="11921-104">Récupère la `bool` valeur d’une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="11921-104">Retrieves the `bool` value of a Boolean value.</span></span>  
  
## <span data-ttu-id="11921-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11921-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsBooleanToBool(  
   _In_ JsValueRef value,  
   _Out_ bool *boolValue  
);  
```  
  
#### <span data-ttu-id="11921-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11921-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="11921-107">Valeur à convertir.</span><span class="sxs-lookup"><span data-stu-id="11921-107">The value to be converted.</span></span>  
  
 `boolValue`  
 <span data-ttu-id="11921-108">Valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="11921-108">The converted value.</span></span>  
  
## <span data-ttu-id="11921-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="11921-109">Return Value</span></span>  
 <span data-ttu-id="11921-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="11921-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="11921-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="11921-111">Remarks</span></span>  
 <span data-ttu-id="11921-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="11921-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="11921-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="11921-113">Requirements</span></span>  
 <span data-ttu-id="11921-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="11921-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="11921-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11921-115">See Also</span></span>  
 [<span data-ttu-id="11921-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="11921-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
