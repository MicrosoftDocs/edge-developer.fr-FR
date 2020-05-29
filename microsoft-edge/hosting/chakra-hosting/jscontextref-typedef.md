---
description: Référence à un contexte de script.
title: JsContextRef typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 80e4b5034079f4f0d26da070bd209aa41bf3475f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565256"
---
# <span data-ttu-id="94b8f-103">JsContextRef typedef</span><span class="sxs-lookup"><span data-stu-id="94b8f-103">JsContextRef Typedef</span></span>
<span data-ttu-id="94b8f-104">Référence à un contexte de script.</span><span class="sxs-lookup"><span data-stu-id="94b8f-104">A reference to a script context.</span></span>  
  
## <span data-ttu-id="94b8f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94b8f-105">Syntax</span></span>  
  
```cpp  
typedef JsRef JsContextRef;  
```  
  
## <span data-ttu-id="94b8f-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="94b8f-106">Remarks</span></span>  
 <span data-ttu-id="94b8f-107">Chaque contexte de script contient son propre objet global, distinct de l’objet global dans d’autres contextes de script.</span><span class="sxs-lookup"><span data-stu-id="94b8f-107">Each script context contains its own global object, distinct from the global object in other script contexts.</span></span>  
  
 <span data-ttu-id="94b8f-108">De nombreuses API d’hébergement Chakra requièrent un contexte de script «actif», qui peut être défini à l’aide de `JsSetCurrentContext` .</span><span class="sxs-lookup"><span data-stu-id="94b8f-108">Many Chakra hosting APIs require an "active" script context, which can be set using `JsSetCurrentContext`.</span></span> <span data-ttu-id="94b8f-109">Les API d’hébergement chakra qui nécessitent la définition d’un contexte actuel seront signalées explicitement dans leurs documents.</span><span class="sxs-lookup"><span data-stu-id="94b8f-109">Chakra hosting APIs that require a current context to be set will note that explicitly in their documentation.</span></span>  
  
## <span data-ttu-id="94b8f-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94b8f-110">Requirements</span></span>  
 <span data-ttu-id="94b8f-111">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="94b8f-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="94b8f-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94b8f-112">See Also</span></span>  
 [<span data-ttu-id="94b8f-113">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="94b8f-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)