---
description: Détermine s’il s’agit d’un objet externe.
title: Fonction JsHasExternalData | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasExternalData
helpviewer_keywords:
- JsHasExternalData function
ms.assetid: a077e3ac-4f6f-4d94-8398-f1b5cc4c18e0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d73333215a33fc409190a0e33fa616b6350fb2a3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232836"
---
# <span data-ttu-id="bed44-103">JsHasExternalData Function</span><span class="sxs-lookup"><span data-stu-id="bed44-103">JsHasExternalData Function</span></span>

<span data-ttu-id="bed44-104">Détermine s’il s’agit d’un objet externe.</span><span class="sxs-lookup"><span data-stu-id="bed44-104">Determines whether an object is an external object.</span></span>  
  
## <span data-ttu-id="bed44-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bed44-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="bed44-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bed44-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="bed44-107">Objet.</span><span class="sxs-lookup"><span data-stu-id="bed44-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="bed44-108">S’il s’agit d’un objet externe.</span><span class="sxs-lookup"><span data-stu-id="bed44-108">Whether the object is an external object.</span></span>  
  
## <span data-ttu-id="bed44-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bed44-109">Return Value</span></span>  
 <span data-ttu-id="bed44-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="bed44-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bed44-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="bed44-111">Remarks</span></span>  
 <span data-ttu-id="bed44-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="bed44-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bed44-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="bed44-113">Requirements</span></span>  
 <span data-ttu-id="bed44-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bed44-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bed44-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bed44-115">See Also</span></span>  
 [<span data-ttu-id="bed44-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bed44-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
