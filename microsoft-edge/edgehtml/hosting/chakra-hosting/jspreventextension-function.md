---
description: Rend un objet non extensible.
title: Fonction JsPreventExtension | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsPreventExtension
helpviewer_keywords:
- JsPreventExtension function
ms.assetid: 8da07e20-d076-4ae4-9fb0-3f3c141518c2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1904756a932bd581e05ec474004af7107da3f64b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233304"
---
# <span data-ttu-id="5a401-103">JsPreventExtension Function</span><span class="sxs-lookup"><span data-stu-id="5a401-103">JsPreventExtension Function</span></span>

<span data-ttu-id="5a401-104">Rend un objet non extensible.</span><span class="sxs-lookup"><span data-stu-id="5a401-104">Makes an object non-extensible.</span></span>  
  
## <span data-ttu-id="5a401-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a401-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPreventExtension(  
   _In_ JsValueRef object  
);  
```  
  
#### <span data-ttu-id="5a401-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a401-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="5a401-107">Objet à rendre non extensible.</span><span class="sxs-lookup"><span data-stu-id="5a401-107">The object to make non-extensible.</span></span>  
  
## <span data-ttu-id="5a401-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5a401-108">Return Value</span></span>  
 <span data-ttu-id="5a401-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5a401-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5a401-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="5a401-110">Remarks</span></span>  
 <span data-ttu-id="5a401-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="5a401-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="5a401-112">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="5a401-112">Requirements</span></span>  
 <span data-ttu-id="5a401-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5a401-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5a401-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a401-114">See Also</span></span>  
 [<span data-ttu-id="5a401-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5a401-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
