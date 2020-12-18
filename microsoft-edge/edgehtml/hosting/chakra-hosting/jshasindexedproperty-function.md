---
description: Teste si un objet possède une valeur à l’index spécifié.
title: Fonction JsHasIndexedProperty | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasIndexedProperty
helpviewer_keywords:
- JsHasIndexedProperty function
ms.assetid: 30436a3d-fda0-407e-aba2-142be2310372
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9eb1794c465b4b116978a2150285e2fed3ae1d9b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233187"
---
# <span data-ttu-id="f4b0c-103">JsHasIndexedProperty Function</span><span class="sxs-lookup"><span data-stu-id="f4b0c-103">JsHasIndexedProperty Function</span></span>

<span data-ttu-id="f4b0c-104">Teste si un objet possède une valeur à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="f4b0c-104">Tests whether an object has a value at the specified index.</span></span>  
  
## <span data-ttu-id="f4b0c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4b0c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="f4b0c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4b0c-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="f4b0c-107">Objet sur lequel travailler.</span><span class="sxs-lookup"><span data-stu-id="f4b0c-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="f4b0c-108">Index à tester.</span><span class="sxs-lookup"><span data-stu-id="f4b0c-108">The index to test.</span></span>  
  
 `result`  
 <span data-ttu-id="f4b0c-109">Si l’objet a une valeur à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="f4b0c-109">Whether the object has an value at the specified index.</span></span>  
  
## <span data-ttu-id="f4b0c-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f4b0c-110">Return Value</span></span>  
 <span data-ttu-id="f4b0c-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f4b0c-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f4b0c-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="f4b0c-112">Remarks</span></span>  
 <span data-ttu-id="f4b0c-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="f4b0c-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f4b0c-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="f4b0c-114">Requirements</span></span>  
 <span data-ttu-id="f4b0c-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f4b0c-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f4b0c-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4b0c-116">See Also</span></span>  
 [<span data-ttu-id="f4b0c-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f4b0c-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
