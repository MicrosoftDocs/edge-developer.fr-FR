---
description: Rappel appelé avant la collecte d’un objet.
title: JsObjectBeforeCollectCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: f21a064a-579f-44cb-9d21-76b62e8c18f5
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 27bbd1aed72cc751397ac4e6734f107612653b66
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565147"
---
# <span data-ttu-id="e7eeb-103">JsObjectBeforeCollectCallback typedef</span><span class="sxs-lookup"><span data-stu-id="e7eeb-103">JsObjectBeforeCollectCallback Typedef</span></span>
<span data-ttu-id="e7eeb-104">Rappel appelé avant la collecte d’un objet.</span><span class="sxs-lookup"><span data-stu-id="e7eeb-104">A callback called before collecting an object.</span></span>  
  
## <span data-ttu-id="e7eeb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7eeb-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsObjectBeforeCollectCallback)(  
  _In_ JsRef ref,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="e7eeb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7eeb-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="e7eeb-107">Objet à collecter.</span><span class="sxs-lookup"><span data-stu-id="e7eeb-107">The object to be collected.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="e7eeb-108">État transmis `JsSetObjectBeforeCollectCallback` .</span><span class="sxs-lookup"><span data-stu-id="e7eeb-108">The state passed to `JsSetObjectBeforeCollectCallback`.</span></span>  
  
## <span data-ttu-id="e7eeb-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="e7eeb-109">Remarks</span></span>  
 <span data-ttu-id="e7eeb-110">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="e7eeb-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="e7eeb-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7eeb-111">Requirements</span></span>  
 <span data-ttu-id="e7eeb-112">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e7eeb-112">jsrt.h</span></span>  
  
## <span data-ttu-id="e7eeb-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7eeb-113">See Also</span></span>  
 [<span data-ttu-id="e7eeb-114">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e7eeb-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)