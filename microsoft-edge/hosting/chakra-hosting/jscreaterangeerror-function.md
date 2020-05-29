---
description: Crée un nouvel objet d’erreur RangeError JavaScript.
title: Fonction JsCreateRangeError | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRangeError
helpviewer_keywords:
- JsCreateRangeError function
ms.assetid: 0ab05de7-57af-4cfd-9aa5-0a69a893cc97
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 3759f1c04a2eb13488f756ae2c135373d9db1f74
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565226"
---
# <span data-ttu-id="d8be8-103">Fonction JsCreateRangeError</span><span class="sxs-lookup"><span data-stu-id="d8be8-103">JsCreateRangeError Function</span></span>
<span data-ttu-id="d8be8-104">Crée un nouvel objet d’erreur RangeError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d8be8-104">Creates a new JavaScript RangeError error object.</span></span>
  
## <span data-ttu-id="d8be8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8be8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateRangeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="d8be8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8be8-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="d8be8-107">Message de l’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d8be8-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="d8be8-108">Nouvel objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d8be8-108">The new error object.</span></span>  
  
## <span data-ttu-id="d8be8-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d8be8-109">Return Value</span></span>  
 <span data-ttu-id="d8be8-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d8be8-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d8be8-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="d8be8-111">Remarks</span></span>  
 <span data-ttu-id="d8be8-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="d8be8-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d8be8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8be8-113">Requirements</span></span>  
 <span data-ttu-id="d8be8-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d8be8-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d8be8-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8be8-115">See Also</span></span>  
 [<span data-ttu-id="d8be8-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d8be8-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)