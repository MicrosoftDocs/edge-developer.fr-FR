---
description: Référence à un contexte de script.
title: JsContextRef typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c8a8fcbd67afb150d682cfc19321f0f13acfe3a6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232995"
---
# <span data-ttu-id="7fb1a-103">Typedef JsContextRef</span><span class="sxs-lookup"><span data-stu-id="7fb1a-103">JsContextRef Typedef</span></span>

<span data-ttu-id="7fb1a-104">Référence à un contexte de script.</span><span class="sxs-lookup"><span data-stu-id="7fb1a-104">A reference to a script context.</span></span>  
  
## <span data-ttu-id="7fb1a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7fb1a-105">Syntax</span></span>  
  
```cpp  
typedef JsRef JsContextRef;  
```  
  
## <span data-ttu-id="7fb1a-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="7fb1a-106">Remarks</span></span>  
 <span data-ttu-id="7fb1a-107">Chaque contexte de script contient son propre objet global, distinct de l’objet global dans d’autres contextes de script.</span><span class="sxs-lookup"><span data-stu-id="7fb1a-107">Each script context contains its own global object, distinct from the global object in other script contexts.</span></span>  
  
 <span data-ttu-id="7fb1a-108">De nombreuses API d’hébergement Chakra requièrent un contexte de script «actif», qui peut être défini à l’aide de `JsSetCurrentContext` .</span><span class="sxs-lookup"><span data-stu-id="7fb1a-108">Many Chakra hosting APIs require an "active" script context, which can be set using `JsSetCurrentContext`.</span></span> <span data-ttu-id="7fb1a-109">Les API d’hébergement chakra qui nécessitent la définition d’un contexte actuel seront signalées explicitement dans leurs documents.</span><span class="sxs-lookup"><span data-stu-id="7fb1a-109">Chakra hosting APIs that require a current context to be set will note that explicitly in their documentation.</span></span>  
  
## <span data-ttu-id="7fb1a-110">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="7fb1a-110">Requirements</span></span>  
 <span data-ttu-id="7fb1a-111">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7fb1a-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7fb1a-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fb1a-112">See Also</span></span>  
 [<span data-ttu-id="7fb1a-113">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7fb1a-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
