---
description: Renvoie le prototype d’un objet.
title: Fonction JsGetPrototype | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetPrototype
helpviewer_keywords:
- JsGetPrototype function
ms.assetid: 05d743fc-103e-4a92-86f2-a063f39a2a6f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 12708634fea9e8f9fd1205514845b1cb9760ee9e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565182"
---
# <span data-ttu-id="ee243-103">Fonction JsGetPrototype</span><span class="sxs-lookup"><span data-stu-id="ee243-103">JsGetPrototype Function</span></span>
<span data-ttu-id="ee243-104">Renvoie le prototype d’un objet.</span><span class="sxs-lookup"><span data-stu-id="ee243-104">Returns the prototype of an object.</span></span>  
  
## <span data-ttu-id="ee243-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee243-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPrototype(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *prototypeObject  
);  
```  
  
#### <span data-ttu-id="ee243-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee243-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="ee243-107">Objet dont le prototype doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="ee243-107">The object whose prototype is to be returned.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="ee243-108">Le prototype de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ee243-108">The object's prototype.</span></span>  
  
## <span data-ttu-id="ee243-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ee243-109">Return Value</span></span>  
 <span data-ttu-id="ee243-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ee243-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ee243-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="ee243-111">Remarks</span></span>  
 <span data-ttu-id="ee243-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="ee243-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ee243-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee243-113">Requirements</span></span>  
 <span data-ttu-id="ee243-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ee243-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ee243-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee243-115">See Also</span></span>  
 [<span data-ttu-id="ee243-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ee243-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)