---
description: Obtient le jeu de données interne sur JsrtContext.
title: Fonction JsGetContextData | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: f5d7e446-267a-4a80-a427-6e1b95a3391b
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bd85ccbc4008897643ec3840e8cdeca3611a50c8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565201"
---
# <span data-ttu-id="6ab4c-103">Fonction JsGetContextData</span><span class="sxs-lookup"><span data-stu-id="6ab4c-103">JsGetContextData Function</span></span>
<span data-ttu-id="6ab4c-104">Obtient le jeu de données interne sur JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="6ab4c-104">Gets the internal data set on JsrtContext.</span></span>  
  
## <span data-ttu-id="6ab4c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ab4c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextData(  
  _In_ JsContextRef context,  
  _Out_ void **data  
);  
```  
  
#### <span data-ttu-id="6ab4c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ab4c-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="6ab4c-107">Contexte à partir duquel obtenir les données.</span><span class="sxs-lookup"><span data-stu-id="6ab4c-107">The context to get the data from.</span></span>  
  
 `data`  
 <span data-ttu-id="6ab4c-108">Pointeur vers les données où les données seront renvoyées.</span><span class="sxs-lookup"><span data-stu-id="6ab4c-108">The pointer to the data where data will be returned.</span></span>  
  
## <span data-ttu-id="6ab4c-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6ab4c-109">Return Value</span></span>  
 <span data-ttu-id="6ab4c-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6ab4c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6ab4c-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="6ab4c-111">Remarks</span></span>  
 <span data-ttu-id="6ab4c-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="6ab4c-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="6ab4c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ab4c-113">Requirements</span></span>  
 <span data-ttu-id="6ab4c-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6ab4c-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6ab4c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ab4c-115">See Also</span></span>  
 [<span data-ttu-id="6ab4c-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6ab4c-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)