---
description: Rend un objet non extensible.
title: Fonction JsPreventExtension | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsPreventExtension
helpviewer_keywords:
- JsPreventExtension function
ms.assetid: 8da07e20-d076-4ae4-9fb0-3f3c141518c2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: baa001b2fd26133ef3a20c88213ac6aaf34a2e0d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566275"
---
# <span data-ttu-id="3017b-103">Fonction JsPreventExtension</span><span class="sxs-lookup"><span data-stu-id="3017b-103">JsPreventExtension Function</span></span>
<span data-ttu-id="3017b-104">Rend un objet non extensible.</span><span class="sxs-lookup"><span data-stu-id="3017b-104">Makes an object non-extensible.</span></span>  
  
## <span data-ttu-id="3017b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3017b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPreventExtension(  
   _In_ JsValueRef object  
);  
```  
  
#### <span data-ttu-id="3017b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3017b-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="3017b-107">Objet à rendre non extensible.</span><span class="sxs-lookup"><span data-stu-id="3017b-107">The object to make non-extensible.</span></span>  
  
## <span data-ttu-id="3017b-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3017b-108">Return Value</span></span>  
 <span data-ttu-id="3017b-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3017b-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3017b-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="3017b-110">Remarks</span></span>  
 <span data-ttu-id="3017b-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="3017b-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="3017b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3017b-112">Requirements</span></span>  
 <span data-ttu-id="3017b-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3017b-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3017b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3017b-114">See Also</span></span>  
 [<span data-ttu-id="3017b-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3017b-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)