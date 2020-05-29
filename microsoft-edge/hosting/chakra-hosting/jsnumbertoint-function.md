---
description: Récupère la `int` valeur d’une valeur numérique.
title: Fonction JsNumberToInt | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: cf4c8cb42c737cfb9efee5422fe6bb3c1389cbfd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566289"
---
# <span data-ttu-id="00b0f-103">Fonction JsNumberToInt</span><span class="sxs-lookup"><span data-stu-id="00b0f-103">JsNumberToInt Function</span></span>
<span data-ttu-id="00b0f-104">Récupère la `int` valeur d’une valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="00b0f-104">Retrieves the `int` value of a number value.</span></span>  
  
## <span data-ttu-id="00b0f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00b0f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToInt(  
      _In_ JsValueRef value,  
      _Out_ int *intValue  
);  
```  
  
#### <span data-ttu-id="00b0f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00b0f-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="00b0f-107">Valeur numérique à convertir en `int` valeur.</span><span class="sxs-lookup"><span data-stu-id="00b0f-107">The number value to convert to an `int` value.</span></span>  
  
 `intValue`  
 <span data-ttu-id="00b0f-108">`int`Valeur.</span><span class="sxs-lookup"><span data-stu-id="00b0f-108">The `int` value.</span></span>  
  
## <span data-ttu-id="00b0f-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="00b0f-109">Return Value</span></span>  
  
## <span data-ttu-id="00b0f-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="00b0f-110">Remarks</span></span>  
 <span data-ttu-id="00b0f-111">Cette fonction récupère la valeur d’une valeur numérique et la convertit en une `int` valeur.</span><span class="sxs-lookup"><span data-stu-id="00b0f-111">This function retrieves the value of a number value and converts to an `int` value.</span></span> <span data-ttu-id="00b0f-112">Il échouera avec `JsErrorInvalidArgument` si le type de la valeur n’est pas numérique.</span><span class="sxs-lookup"><span data-stu-id="00b0f-112">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="00b0f-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="00b0f-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="00b0f-114">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="00b0f-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="00b0f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00b0f-115">Requirements</span></span>  
 <span data-ttu-id="00b0f-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="00b0f-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="00b0f-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00b0f-117">See Also</span></span>  
 [<span data-ttu-id="00b0f-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="00b0f-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)