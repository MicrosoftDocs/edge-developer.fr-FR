---
description: Définit le prototype d’un objet.
title: Fonction JsSetPrototype | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 88e1e421-4ae5-4e3b-b377-19256cc80e9f
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 625269c5f9f459a5c7eecb6cfc31cb85fc24214b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566154"
---
# <span data-ttu-id="0f5a1-103">Fonction JsSetPrototype</span><span class="sxs-lookup"><span data-stu-id="0f5a1-103">JsSetPrototype Function</span></span>
<span data-ttu-id="0f5a1-104">Définit le prototype d’un objet.</span><span class="sxs-lookup"><span data-stu-id="0f5a1-104">Sets the prototype of an object.</span></span>  
  
## <span data-ttu-id="0f5a1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f5a1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPrototype(  
   _In_ JsValueRef object,  
   _In_ JsValueRef prototypeObject  
);  
```  
  
#### <span data-ttu-id="0f5a1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f5a1-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="0f5a1-107">Objet dont le prototype doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="0f5a1-107">The object whose prototype is to be changed.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="0f5a1-108">Le nouveau prototype de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0f5a1-108">The object's new prototype.</span></span>  
  
## <span data-ttu-id="0f5a1-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0f5a1-109">Return Value</span></span>  
 <span data-ttu-id="0f5a1-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0f5a1-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0f5a1-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="0f5a1-111">Remarks</span></span>  
 <span data-ttu-id="0f5a1-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="0f5a1-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0f5a1-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f5a1-113">Requirements</span></span>  
 <span data-ttu-id="0f5a1-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0f5a1-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0f5a1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f5a1-115">See Also</span></span>  
 [<span data-ttu-id="0f5a1-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0f5a1-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)