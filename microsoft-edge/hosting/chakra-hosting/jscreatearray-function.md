---
description: Crée un objet tableau JavaScript.
title: Fonction JsCreateArray | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateArray
helpviewer_keywords:
- JsCreateArray function
ms.assetid: a119949a-e427-4349-9d00-5ec20fb9319c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: fb6a65df1484eb308224a42bb5a65443855c6215
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565245"
---
# <span data-ttu-id="c7c1f-103">Fonction JsCreateArray</span><span class="sxs-lookup"><span data-stu-id="c7c1f-103">JsCreateArray Function</span></span>
<span data-ttu-id="c7c1f-104">Crée un objet tableau JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-104">Creates a Javascript array object.</span></span>  
  
## <span data-ttu-id="c7c1f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7c1f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArray(  
   _In_ unsigned int length,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="c7c1f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7c1f-106">Parameters</span></span>  
 `length`  
 <span data-ttu-id="c7c1f-107">Longueur initiale de la matrice.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-107">The initial length of the array.</span></span>  
  
 `result`  
 <span data-ttu-id="c7c1f-108">Nouvel objet tableau.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-108">The new array object.</span></span>  
  
## <span data-ttu-id="c7c1f-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c7c1f-109">Return Value</span></span>  
 <span data-ttu-id="c7c1f-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c7c1f-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="c7c1f-111">Remarks</span></span>  
 <span data-ttu-id="c7c1f-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c7c1f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7c1f-113">Requirements</span></span>  
 <span data-ttu-id="c7c1f-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c7c1f-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c7c1f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7c1f-115">See Also</span></span>  
 [<span data-ttu-id="c7c1f-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c7c1f-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)