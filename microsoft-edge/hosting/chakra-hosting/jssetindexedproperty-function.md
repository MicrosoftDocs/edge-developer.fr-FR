---
description: Définissez la valeur à l’index spécifié d’un objet.
title: Fonction JsSetIndexedProperty | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetIndexedProperty
helpviewer_keywords:
- JsSetIndexedProperty function
ms.assetid: ccbc5bf4-d99b-485c-ab25-d2bd1ed2142e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 893849c42d9cbf0de160846d3397fcd5d7c77b7b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566241"
---
# <span data-ttu-id="60d57-103">Fonction JsSetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="60d57-103">JsSetIndexedProperty Function</span></span>
<span data-ttu-id="60d57-104">Définissez la valeur à l’index spécifié d’un objet.</span><span class="sxs-lookup"><span data-stu-id="60d57-104">Set the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="60d57-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60d57-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _In_ JsValueRef value  
);  
```  
  
#### <span data-ttu-id="60d57-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60d57-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="60d57-107">Objet sur lequel travailler.</span><span class="sxs-lookup"><span data-stu-id="60d57-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="60d57-108">Index à définir.</span><span class="sxs-lookup"><span data-stu-id="60d57-108">The index to set.</span></span>  
  
 `value`  
 <span data-ttu-id="60d57-109">Valeur à définir.</span><span class="sxs-lookup"><span data-stu-id="60d57-109">The value to set.</span></span>  
  
## <span data-ttu-id="60d57-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="60d57-110">Return Value</span></span>  
 <span data-ttu-id="60d57-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="60d57-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="60d57-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="60d57-112">Remarks</span></span>  
 <span data-ttu-id="60d57-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="60d57-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="60d57-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60d57-114">Requirements</span></span>  
 <span data-ttu-id="60d57-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="60d57-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="60d57-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60d57-116">See Also</span></span>  
 [<span data-ttu-id="60d57-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="60d57-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)