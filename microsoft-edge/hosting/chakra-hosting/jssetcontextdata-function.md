---
description: Définit les données internes de JsrtContext.
title: Fonction JsSetContextData | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: be90aa6a-b001-4a6f-90c5-c2135e913be0
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 00521bafdaf6125dd15746de8a1d403eaf03b4a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566251"
---
# <span data-ttu-id="5b769-103">Fonction JsSetContextData</span><span class="sxs-lookup"><span data-stu-id="5b769-103">JsSetContextData Function</span></span>
<span data-ttu-id="5b769-104">Définit les données internes de JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="5b769-104">Sets the internal data of JsrtContext.</span></span>  
  
## <span data-ttu-id="5b769-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b769-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetContextData(  
  _In_ JsContextRef context,  
  _In_ void *data  
);  
  
```  
  
#### <span data-ttu-id="5b769-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b769-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="5b769-107">Contexte dans lequel définir les données.</span><span class="sxs-lookup"><span data-stu-id="5b769-107">The context to set the data to.</span></span>  
  
 `data`  
 <span data-ttu-id="5b769-108">Pointeur vers les données à définir.</span><span class="sxs-lookup"><span data-stu-id="5b769-108">The pointer to the data to be set.</span></span>  
  
## <span data-ttu-id="5b769-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5b769-109">Return Value</span></span>  
 <span data-ttu-id="5b769-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5b769-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5b769-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="5b769-111">Remarks</span></span>  
 <span data-ttu-id="5b769-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="5b769-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="5b769-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b769-113">Requirements</span></span>  
 <span data-ttu-id="5b769-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5b769-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5b769-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b769-115">See Also</span></span>  
 [<span data-ttu-id="5b769-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5b769-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)