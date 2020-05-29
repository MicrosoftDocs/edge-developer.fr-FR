---
description: Référence à un objet possédé par le récupérateur de mémoire Chakra.
title: JsRef typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 6aafc39f-6b9c-457f-8bf0-48831bffe9b8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f5ce1ada67a4530ba57345b90c0b7deba6954c7c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566273"
---
# <span data-ttu-id="892b7-103">JsRef typedef</span><span class="sxs-lookup"><span data-stu-id="892b7-103">JsRef Typedef</span></span>
<span data-ttu-id="892b7-104">Référence à un objet possédé par le récupérateur de mémoire Chakra.</span><span class="sxs-lookup"><span data-stu-id="892b7-104">A reference to an object owned by the Chakra garbage collector.</span></span>  
  
## <span data-ttu-id="892b7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="892b7-105">Syntax</span></span>  
  
```cpp  
typedef void *JsRef;  
```  
  
## <span data-ttu-id="892b7-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="892b7-106">Remarks</span></span>  
 <span data-ttu-id="892b7-107">Un Runtime Chakra effectue automatiquement le suivi des références JsRef tant que celles-ci sont stockées dans des variables locales ou dans des paramètres (c’est-à-dire sur la pile).</span><span class="sxs-lookup"><span data-stu-id="892b7-107">A Chakra runtime will automatically track JsRef references as long as they are on stored in local variables or in parameters (i.e. on the stack).</span></span> <span data-ttu-id="892b7-108">Le stockage d’un JsRef dans un autre emplacement que sur la pile nécessite l’appel de JsAddRef et JsRelease pour gérer la durée de vie de l’objet, sinon le nettoyage de la mémoire peut libérer l’objet alors qu’il est toujours en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="892b7-108">Storing a JsRef somewhere other than on the stack requires calling JsAddRef and JsRelease to manage the lifetime of the object, otherwise the garbage collector may free the object while it is still in use.</span></span>  
  
## <span data-ttu-id="892b7-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="892b7-109">Requirements</span></span>  
 <span data-ttu-id="892b7-110">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="892b7-110">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="892b7-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="892b7-111">See Also</span></span>  
 [<span data-ttu-id="892b7-112">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="892b7-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)