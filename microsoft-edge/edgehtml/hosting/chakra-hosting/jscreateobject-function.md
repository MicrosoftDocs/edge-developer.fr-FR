---
description: Crée un objet.
title: Fonction JsCreateObject | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateObject
helpviewer_keywords:
- JsCreateObject function
ms.assetid: 6c1d01a4-9254-443e-b974-6f0b0c861ca2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d5effe7ade1679392fcad7f2bb5cea880712ef7f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233115"
---
# <span data-ttu-id="f14c1-103">JsCreateObject Function</span><span class="sxs-lookup"><span data-stu-id="f14c1-103">JsCreateObject Function</span></span>

<span data-ttu-id="f14c1-104">Crée un objet.</span><span class="sxs-lookup"><span data-stu-id="f14c1-104">Creates a new object.</span></span>
  
## <span data-ttu-id="f14c1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f14c1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateObject(  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="f14c1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f14c1-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="f14c1-107">Nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="f14c1-107">The new object.</span></span>  
  
## <span data-ttu-id="f14c1-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f14c1-108">Return Value</span></span>  
 <span data-ttu-id="f14c1-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f14c1-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f14c1-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="f14c1-110">Remarks</span></span>  
 <span data-ttu-id="f14c1-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="f14c1-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f14c1-112">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="f14c1-112">Requirements</span></span>  
 <span data-ttu-id="f14c1-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f14c1-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f14c1-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f14c1-114">See Also</span></span>  
 [<span data-ttu-id="f14c1-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f14c1-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
