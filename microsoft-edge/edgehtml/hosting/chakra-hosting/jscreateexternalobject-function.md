---
description: Crée un nouvel objet qui stocke des données externes.
title: Fonction JsCreateExternalObject | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateExternalObject
helpviewer_keywords:
- JsCreateExternalObject function
ms.assetid: 6bcef506-93fb-429b-b06a-a971ff0b71f3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4d402c3d379a16186daaba601c7f830c53a9a953
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233488"
---
# <span data-ttu-id="9096b-103">JsCreateExternalObject Function</span><span class="sxs-lookup"><span data-stu-id="9096b-103">JsCreateExternalObject Function</span></span>

<span data-ttu-id="9096b-104">Crée un nouvel objet qui stocke des données externes.</span><span class="sxs-lookup"><span data-stu-id="9096b-104">Creates a new object that stores some external data.</span></span>
  
## <span data-ttu-id="9096b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9096b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalObject(  
   _In_opt_ void *data,  
   _In_opt_ JsFinalizeCallback finalizeCallback,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="9096b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9096b-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="9096b-107">Les données externes qui sont représentées par l’objet.</span><span class="sxs-lookup"><span data-stu-id="9096b-107">External data that the object will represent.</span></span> <span data-ttu-id="9096b-108">Est susceptible d’être null.</span><span class="sxs-lookup"><span data-stu-id="9096b-108">May be null.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="9096b-109">Rappel lors de la finalisation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9096b-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="9096b-110">Est susceptible d’être null.</span><span class="sxs-lookup"><span data-stu-id="9096b-110">May be null.</span></span>  
  
 `object`  
 <span data-ttu-id="9096b-111">Nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="9096b-111">The new object.</span></span>  
  
## <span data-ttu-id="9096b-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9096b-112">Return Value</span></span>  
 <span data-ttu-id="9096b-113">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9096b-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9096b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9096b-114">Remarks</span></span>  
 <span data-ttu-id="9096b-115">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="9096b-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9096b-116">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="9096b-116">Requirements</span></span>  
 <span data-ttu-id="9096b-117">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9096b-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9096b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9096b-118">See Also</span></span>  
 [<span data-ttu-id="9096b-119">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9096b-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
