---
description: Récupérer la valeur à l’index spécifié d’un objet.
title: Fonction JsGetIndexedProperty | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetIndexedProperty
helpviewer_keywords:
- JsGetIndexedProperty function
ms.assetid: f61ea388-0ae6-4a19-b3b5-75ed49a3f32d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bd0246464d00884ca71fd8d3564ce775415f6267
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232804"
---
# <span data-ttu-id="ce48a-103">JsGetIndexedProperty Function</span><span class="sxs-lookup"><span data-stu-id="ce48a-103">JsGetIndexedProperty Function</span></span>

<span data-ttu-id="ce48a-104">Récupérer la valeur à l’index spécifié d’un objet.</span><span class="sxs-lookup"><span data-stu-id="ce48a-104">Retrieve the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="ce48a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce48a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="ce48a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce48a-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="ce48a-107">Objet sur lequel travailler.</span><span class="sxs-lookup"><span data-stu-id="ce48a-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="ce48a-108">Index à récupérer.</span><span class="sxs-lookup"><span data-stu-id="ce48a-108">The index to retrieve.</span></span>  
  
 `result`  
 <span data-ttu-id="ce48a-109">Valeur récupérée.</span><span class="sxs-lookup"><span data-stu-id="ce48a-109">The retrieved value.</span></span>  
  
## <span data-ttu-id="ce48a-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ce48a-110">Return Value</span></span>  
 <span data-ttu-id="ce48a-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ce48a-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ce48a-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="ce48a-112">Remarks</span></span>  
 <span data-ttu-id="ce48a-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="ce48a-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ce48a-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="ce48a-114">Requirements</span></span>  
 <span data-ttu-id="ce48a-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ce48a-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ce48a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce48a-116">See Also</span></span>  
 [<span data-ttu-id="ce48a-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ce48a-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
