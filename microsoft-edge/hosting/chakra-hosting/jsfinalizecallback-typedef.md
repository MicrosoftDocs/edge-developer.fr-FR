---
description: Un rappel du finaliseur.
title: JsFinalizeCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: aa7a0269-b9d4-4717-97ac-8da7eb6ced15
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d2ee2c2c11e85094010cd15be59aa7ac587b614f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566332"
---
# <span data-ttu-id="74b4c-103">JsFinalizeCallback typedef</span><span class="sxs-lookup"><span data-stu-id="74b4c-103">JsFinalizeCallback Typedef</span></span>
<span data-ttu-id="74b4c-104">Un rappel du finaliseur.</span><span class="sxs-lookup"><span data-stu-id="74b4c-104">A finalizer callback.</span></span>  
  
## <span data-ttu-id="74b4c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74b4c-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsFinalizeCallback)(  
   _In_opt_ void *data  
);  
```  
  
#### <span data-ttu-id="74b4c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74b4c-106">Parameters</span></span>  
 <span data-ttu-id="74b4c-107">data</span><span class="sxs-lookup"><span data-stu-id="74b4c-107">data</span></span>  
 <span data-ttu-id="74b4c-108">Données externes transmises lors de la création de l’objet finalisé.</span><span class="sxs-lookup"><span data-stu-id="74b4c-108">The external data that was passed in when creating the object being finalized.</span></span>  
  
## <span data-ttu-id="74b4c-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74b4c-109">Requirements</span></span>  
 <span data-ttu-id="74b4c-110">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="74b4c-110">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="74b4c-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74b4c-111">See Also</span></span>  
 [<span data-ttu-id="74b4c-112">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="74b4c-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)