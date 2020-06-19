---
description: Définit les données internes de JsrtContext.
title: Fonction JsSetContextData | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: be90aa6a-b001-4a6f-90c5-c2135e913be0
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e874f500ca82328dddeaaa03a0b78a188b8fd241
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751932"
---
# <span data-ttu-id="8b65d-103">JsSetContextData Function</span><span class="sxs-lookup"><span data-stu-id="8b65d-103">JsSetContextData Function</span></span>
<span data-ttu-id="8b65d-104">Définit les données internes de JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="8b65d-104">Sets the internal data of JsrtContext.</span></span>  
  
## <span data-ttu-id="8b65d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b65d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetContextData(  
  _In_ JsContextRef context,  
  _In_ void *data  
);  
  
```  
  
#### <span data-ttu-id="8b65d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b65d-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="8b65d-107">Contexte dans lequel définir les données.</span><span class="sxs-lookup"><span data-stu-id="8b65d-107">The context to set the data to.</span></span>  
  
 `data`  
 <span data-ttu-id="8b65d-108">Pointeur vers les données à définir.</span><span class="sxs-lookup"><span data-stu-id="8b65d-108">The pointer to the data to be set.</span></span>  
  
## <span data-ttu-id="8b65d-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8b65d-109">Return Value</span></span>  
 <span data-ttu-id="8b65d-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8b65d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8b65d-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="8b65d-111">Remarks</span></span>  
 <span data-ttu-id="8b65d-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="8b65d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="8b65d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b65d-113">Requirements</span></span>  
 <span data-ttu-id="8b65d-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8b65d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8b65d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b65d-115">See Also</span></span>  
 [<span data-ttu-id="8b65d-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8b65d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)