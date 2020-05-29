---
description: Obtient le contexte de script auquel appartient l’objet.
title: Fonction JsGetContextOfObject | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: cea6cdcd-790f-455c-af04-026af8ae2eb7
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4f1b996954e877d9c98ac0caf06f255af629a386
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565199"
---
# <span data-ttu-id="9f88b-103">Fonction JsGetContextOfObject</span><span class="sxs-lookup"><span data-stu-id="9f88b-103">JsGetContextOfObject Function</span></span>
<span data-ttu-id="9f88b-104">Obtient le contexte de script auquel appartient l’objet.</span><span class="sxs-lookup"><span data-stu-id="9f88b-104">Gets the script context that the object belongs to.</span></span>  
  
## <span data-ttu-id="9f88b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f88b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextOfObject(  
  _In_ JsValueRef object,  
  _Out_ JsContextRef *context  
);  
```  
  
#### <span data-ttu-id="9f88b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f88b-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="9f88b-107">Objet duquel obtenir le contexte.</span><span class="sxs-lookup"><span data-stu-id="9f88b-107">The object to get the context from.</span></span>  
  
 `context`  
 <span data-ttu-id="9f88b-108">Contexte auquel l’objet appartient.</span><span class="sxs-lookup"><span data-stu-id="9f88b-108">The context the object belongs to.</span></span>  
  
## <span data-ttu-id="9f88b-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9f88b-109">Return Value</span></span>  
 <span data-ttu-id="9f88b-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9f88b-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9f88b-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="9f88b-111">Remarks</span></span>  
 <span data-ttu-id="9f88b-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="9f88b-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9f88b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f88b-113">Requirements</span></span>  
 <span data-ttu-id="9f88b-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9f88b-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9f88b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f88b-115">See Also</span></span>  
 [<span data-ttu-id="9f88b-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9f88b-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)