---
description: Récupérer la valeur à l’index spécifié d’un objet.
title: Fonction JsGetIndexedProperty | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetIndexedProperty
helpviewer_keywords:
- JsGetIndexedProperty function
ms.assetid: f61ea388-0ae6-4a19-b3b5-75ed49a3f32d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 7bb048b841462e27604ab169c69e4c051209a67d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566319"
---
# <span data-ttu-id="2b29e-103">Fonction JsGetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="2b29e-103">JsGetIndexedProperty Function</span></span>
<span data-ttu-id="2b29e-104">Récupérer la valeur à l’index spécifié d’un objet.</span><span class="sxs-lookup"><span data-stu-id="2b29e-104">Retrieve the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="2b29e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b29e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="2b29e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b29e-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="2b29e-107">Objet sur lequel travailler.</span><span class="sxs-lookup"><span data-stu-id="2b29e-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="2b29e-108">Index à récupérer.</span><span class="sxs-lookup"><span data-stu-id="2b29e-108">The index to retrieve.</span></span>  
  
 `result`  
 <span data-ttu-id="2b29e-109">Valeur récupérée.</span><span class="sxs-lookup"><span data-stu-id="2b29e-109">The retrieved value.</span></span>  
  
## <span data-ttu-id="2b29e-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2b29e-110">Return Value</span></span>  
 <span data-ttu-id="2b29e-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2b29e-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2b29e-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="2b29e-112">Remarks</span></span>  
 <span data-ttu-id="2b29e-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="2b29e-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="2b29e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b29e-114">Requirements</span></span>  
 <span data-ttu-id="2b29e-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2b29e-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2b29e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b29e-116">See Also</span></span>  
 [<span data-ttu-id="2b29e-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2b29e-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)