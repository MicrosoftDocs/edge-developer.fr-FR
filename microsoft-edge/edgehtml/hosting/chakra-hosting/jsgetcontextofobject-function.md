---
description: Obtient le contexte de script auquel appartient l’objet.
title: Fonction JsGetContextOfObject | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: cea6cdcd-790f-455c-af04-026af8ae2eb7
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9085f9156e4e0ca9e952fe51447185239082f975
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233231"
---
# <span data-ttu-id="1b873-103">JsGetContextOfObject Function</span><span class="sxs-lookup"><span data-stu-id="1b873-103">JsGetContextOfObject Function</span></span>

<span data-ttu-id="1b873-104">Obtient le contexte de script auquel appartient l’objet.</span><span class="sxs-lookup"><span data-stu-id="1b873-104">Gets the script context that the object belongs to.</span></span>  
  
## <span data-ttu-id="1b873-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b873-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextOfObject(  
  _In_ JsValueRef object,  
  _Out_ JsContextRef *context  
);  
```  
  
#### <span data-ttu-id="1b873-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b873-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="1b873-107">Objet duquel obtenir le contexte.</span><span class="sxs-lookup"><span data-stu-id="1b873-107">The object to get the context from.</span></span>  
  
 `context`  
 <span data-ttu-id="1b873-108">Contexte auquel l’objet appartient.</span><span class="sxs-lookup"><span data-stu-id="1b873-108">The context the object belongs to.</span></span>  
  
## <span data-ttu-id="1b873-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1b873-109">Return Value</span></span>  
 <span data-ttu-id="1b873-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1b873-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1b873-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="1b873-111">Remarks</span></span>  
 <span data-ttu-id="1b873-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="1b873-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="1b873-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="1b873-113">Requirements</span></span>  
 <span data-ttu-id="1b873-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1b873-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1b873-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b873-115">See Also</span></span>  
 [<span data-ttu-id="1b873-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1b873-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
