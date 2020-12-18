---
description: Un rappel du finaliseur.
title: JsFinalizeCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: aa7a0269-b9d4-4717-97ac-8da7eb6ced15
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 794edbb3a61c8c213c0908740ed0a867488a2c6d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233107"
---
# <span data-ttu-id="b58f3-103">Typedef JsFinalizeCallback</span><span class="sxs-lookup"><span data-stu-id="b58f3-103">JsFinalizeCallback Typedef</span></span>

<span data-ttu-id="b58f3-104">Un rappel du finaliseur.</span><span class="sxs-lookup"><span data-stu-id="b58f3-104">A finalizer callback.</span></span>  
  
## <span data-ttu-id="b58f3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b58f3-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsFinalizeCallback)(  
   _In_opt_ void *data  
);  
```  
  
#### <span data-ttu-id="b58f3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b58f3-106">Parameters</span></span>  
 <span data-ttu-id="b58f3-107">data</span><span class="sxs-lookup"><span data-stu-id="b58f3-107">data</span></span>  
 <span data-ttu-id="b58f3-108">Données externes transmises lors de la création de l’objet finalisé.</span><span class="sxs-lookup"><span data-stu-id="b58f3-108">The external data that was passed in when creating the object being finalized.</span></span>  
  
## <span data-ttu-id="b58f3-109">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="b58f3-109">Requirements</span></span>  
 <span data-ttu-id="b58f3-110">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b58f3-110">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b58f3-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b58f3-111">See Also</span></span>  
 [<span data-ttu-id="b58f3-112">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b58f3-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
