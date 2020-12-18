---
description: Obtient le jeu de données interne sur JsrtContext.
title: Fonction JsGetContextData | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: f5d7e446-267a-4a80-a427-6e1b95a3391b
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8f5f70a9c36fea355792050c1a2a810bca2d07b3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233099"
---
# <span data-ttu-id="bb7e3-103">JsGetContextData Function</span><span class="sxs-lookup"><span data-stu-id="bb7e3-103">JsGetContextData Function</span></span>

<span data-ttu-id="bb7e3-104">Obtient le jeu de données interne sur JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="bb7e3-104">Gets the internal data set on JsrtContext.</span></span>  
  
## <span data-ttu-id="bb7e3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb7e3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextData(  
  _In_ JsContextRef context,  
  _Out_ void **data  
);  
```  
  
#### <span data-ttu-id="bb7e3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb7e3-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="bb7e3-107">Contexte à partir duquel obtenir les données.</span><span class="sxs-lookup"><span data-stu-id="bb7e3-107">The context to get the data from.</span></span>  
  
 `data`  
 <span data-ttu-id="bb7e3-108">Pointeur vers les données où les données seront renvoyées.</span><span class="sxs-lookup"><span data-stu-id="bb7e3-108">The pointer to the data where data will be returned.</span></span>  
  
## <span data-ttu-id="bb7e3-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bb7e3-109">Return Value</span></span>  
 <span data-ttu-id="bb7e3-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="bb7e3-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bb7e3-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="bb7e3-111">Remarks</span></span>  
 <span data-ttu-id="bb7e3-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="bb7e3-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bb7e3-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="bb7e3-113">Requirements</span></span>  
 <span data-ttu-id="bb7e3-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bb7e3-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bb7e3-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb7e3-115">See Also</span></span>  
 [<span data-ttu-id="bb7e3-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bb7e3-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
