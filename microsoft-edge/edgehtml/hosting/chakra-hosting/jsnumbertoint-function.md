---
description: Récupère la `int` valeur d’une valeur numérique.
title: Fonction JsNumberToInt | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 928be9a7cc5cd3e26e8b8df99af1e08a6c50209c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233315"
---
# <span data-ttu-id="ddd51-103">JsNumberToInt Function</span><span class="sxs-lookup"><span data-stu-id="ddd51-103">JsNumberToInt Function</span></span>

<span data-ttu-id="ddd51-104">Récupère la `int` valeur d’une valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="ddd51-104">Retrieves the `int` value of a number value.</span></span>  
  
## <span data-ttu-id="ddd51-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ddd51-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToInt(  
      _In_ JsValueRef value,  
      _Out_ int *intValue  
);  
```  
  
#### <span data-ttu-id="ddd51-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddd51-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="ddd51-107">Valeur numérique à convertir en `int` valeur.</span><span class="sxs-lookup"><span data-stu-id="ddd51-107">The number value to convert to an `int` value.</span></span>  
  
 `intValue`  
 <span data-ttu-id="ddd51-108">`int`Valeur.</span><span class="sxs-lookup"><span data-stu-id="ddd51-108">The `int` value.</span></span>  
  
## <span data-ttu-id="ddd51-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ddd51-109">Return Value</span></span>  
  
## <span data-ttu-id="ddd51-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="ddd51-110">Remarks</span></span>  
 <span data-ttu-id="ddd51-111">Cette fonction récupère la valeur d’une valeur numérique et la convertit en une `int` valeur.</span><span class="sxs-lookup"><span data-stu-id="ddd51-111">This function retrieves the value of a number value and converts to an `int` value.</span></span> <span data-ttu-id="ddd51-112">Il échouera avec `JsErrorInvalidArgument` si le type de la valeur n’est pas numérique.</span><span class="sxs-lookup"><span data-stu-id="ddd51-112">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="ddd51-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="ddd51-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="ddd51-114">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="ddd51-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="ddd51-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="ddd51-115">Requirements</span></span>  
 <span data-ttu-id="ddd51-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ddd51-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ddd51-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddd51-117">See Also</span></span>  
 [<span data-ttu-id="ddd51-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ddd51-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
