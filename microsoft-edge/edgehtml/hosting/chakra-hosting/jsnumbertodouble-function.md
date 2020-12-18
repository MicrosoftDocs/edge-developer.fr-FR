---
description: Récupère la `double` valeur d’une valeur numérique.
title: Fonction JsNumberToDouble | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsNumberToDouble
helpviewer_keywords:
- JsNumberToDouble function
ms.assetid: 5f52e8b6-2b70-49a3-879a-bd83ebf2ac33
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e4ae744f091045116a639aff619c475c7c7025f3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233317"
---
# <span data-ttu-id="2473a-103">JsNumberToDouble Function</span><span class="sxs-lookup"><span data-stu-id="2473a-103">JsNumberToDouble Function</span></span>

<span data-ttu-id="2473a-104">Récupère la `double` valeur d’une valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="2473a-104">Retrieves the `double` value of a number value.</span></span>  
  
## <span data-ttu-id="2473a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2473a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToDouble(  
   _In_ JsValueRef value,  
   _Out_ double *doubleValue  
);  
```  
  
#### <span data-ttu-id="2473a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2473a-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="2473a-107">Valeur numérique à convertir en `double` valeur.</span><span class="sxs-lookup"><span data-stu-id="2473a-107">The number value to convert to a `double` value.</span></span>  
  
 `doubleValue`  
 <span data-ttu-id="2473a-108">`double`Valeur.</span><span class="sxs-lookup"><span data-stu-id="2473a-108">The `double` value.</span></span>  
  
## <span data-ttu-id="2473a-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2473a-109">Return Value</span></span>  
 <span data-ttu-id="2473a-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2473a-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2473a-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="2473a-111">Remarks</span></span>  
 <span data-ttu-id="2473a-112">Cette fonction récupère la valeur d’une valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="2473a-112">This function retrieves the value of a number value.</span></span> <span data-ttu-id="2473a-113">Il échouera avec `JsErrorInvalidArgument` si le type de la valeur n’est pas numérique.</span><span class="sxs-lookup"><span data-stu-id="2473a-113">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="2473a-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="2473a-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="2473a-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="2473a-115">Requirements</span></span>  
 <span data-ttu-id="2473a-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2473a-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2473a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2473a-117">See Also</span></span>  
 [<span data-ttu-id="2473a-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2473a-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
