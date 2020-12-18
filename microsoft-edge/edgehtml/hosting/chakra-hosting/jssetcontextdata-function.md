---
description: Définit les données internes de JsrtContext.
title: Fonction JsSetContextData | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: be90aa6a-b001-4a6f-90c5-c2135e913be0
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cac404b9e79bafb5a8eafb47e893dbdf38a02405
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233295"
---
# <span data-ttu-id="30b1f-103">JsSetContextData Function</span><span class="sxs-lookup"><span data-stu-id="30b1f-103">JsSetContextData Function</span></span>

<span data-ttu-id="30b1f-104">Définit les données internes de JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="30b1f-104">Sets the internal data of JsrtContext.</span></span>  
  
## <span data-ttu-id="30b1f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30b1f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetContextData(  
  _In_ JsContextRef context,  
  _In_ void *data  
);  
  
```  
  
#### <span data-ttu-id="30b1f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30b1f-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="30b1f-107">Contexte dans lequel définir les données.</span><span class="sxs-lookup"><span data-stu-id="30b1f-107">The context to set the data to.</span></span>  
  
 `data`  
 <span data-ttu-id="30b1f-108">Pointeur vers les données à définir.</span><span class="sxs-lookup"><span data-stu-id="30b1f-108">The pointer to the data to be set.</span></span>  
  
## <span data-ttu-id="30b1f-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="30b1f-109">Return Value</span></span>  
 <span data-ttu-id="30b1f-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="30b1f-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="30b1f-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="30b1f-111">Remarks</span></span>  
 <span data-ttu-id="30b1f-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="30b1f-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="30b1f-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="30b1f-113">Requirements</span></span>  
 <span data-ttu-id="30b1f-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="30b1f-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="30b1f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30b1f-115">See Also</span></span>  
 [<span data-ttu-id="30b1f-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="30b1f-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
