---
description: Crée un objet.
title: Fonction JsCreateObject | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateObject
helpviewer_keywords:
- JsCreateObject function
ms.assetid: 6c1d01a4-9254-443e-b974-6f0b0c861ca2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9ed988aae0921978819d379562d4a966e4a082a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565227"
---
# <span data-ttu-id="f0e16-103">Fonction JsCreateObject</span><span class="sxs-lookup"><span data-stu-id="f0e16-103">JsCreateObject Function</span></span>
<span data-ttu-id="f0e16-104">Crée un objet.</span><span class="sxs-lookup"><span data-stu-id="f0e16-104">Creates a new object.</span></span>
  
## <span data-ttu-id="f0e16-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0e16-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateObject(  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="f0e16-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0e16-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="f0e16-107">Nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="f0e16-107">The new object.</span></span>  
  
## <span data-ttu-id="f0e16-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f0e16-108">Return Value</span></span>  
 <span data-ttu-id="f0e16-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f0e16-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f0e16-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="f0e16-110">Remarks</span></span>  
 <span data-ttu-id="f0e16-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="f0e16-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f0e16-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0e16-112">Requirements</span></span>  
 <span data-ttu-id="f0e16-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f0e16-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f0e16-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0e16-114">See Also</span></span>  
 [<span data-ttu-id="f0e16-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f0e16-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)