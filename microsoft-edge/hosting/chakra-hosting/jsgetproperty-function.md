---
description: Obtient la propriété d’un objet.
title: Fonction JsGetProperty | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetProperty
helpviewer_keywords:
- JsGetProperty function
ms.assetid: 606bc14f-e849-4f88-a148-6660e923c07b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ea0e5a3bad9363800d2b4a3a18ab932ecc384486
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566314"
---
# <span data-ttu-id="e019b-103">Fonction JsGetProperty</span><span class="sxs-lookup"><span data-stu-id="e019b-103">JsGetProperty Function</span></span>
<span data-ttu-id="e019b-104">Obtient la propriété d’un objet.</span><span class="sxs-lookup"><span data-stu-id="e019b-104">Gets an object's property.</span></span>  
  
## <span data-ttu-id="e019b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e019b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="e019b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e019b-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="e019b-107">Objet qui contient la propriété.</span><span class="sxs-lookup"><span data-stu-id="e019b-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="e019b-108">ID de la propriété.</span><span class="sxs-lookup"><span data-stu-id="e019b-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="e019b-109">Valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="e019b-109">The value of the property.</span></span>  
  
## <span data-ttu-id="e019b-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e019b-110">Return Value</span></span>  
 <span data-ttu-id="e019b-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e019b-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e019b-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="e019b-112">Remarks</span></span>  
 <span data-ttu-id="e019b-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="e019b-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e019b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e019b-114">Requirements</span></span>  
 <span data-ttu-id="e019b-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e019b-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e019b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e019b-116">See Also</span></span>  
 [<span data-ttu-id="e019b-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e019b-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)