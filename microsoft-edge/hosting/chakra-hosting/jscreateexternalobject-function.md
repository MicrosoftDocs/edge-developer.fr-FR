---
description: Crée un nouvel objet qui stocke des données externes.
title: Fonction JsCreateExternalObject | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateExternalObject
helpviewer_keywords:
- JsCreateExternalObject function
ms.assetid: 6bcef506-93fb-429b-b06a-a971ff0b71f3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9a68f4befea7dc7c3369bcade475e29d53342730
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565232"
---
# <span data-ttu-id="0c443-103">Fonction JsCreateExternalObject</span><span class="sxs-lookup"><span data-stu-id="0c443-103">JsCreateExternalObject Function</span></span>
<span data-ttu-id="0c443-104">Crée un nouvel objet qui stocke des données externes.</span><span class="sxs-lookup"><span data-stu-id="0c443-104">Creates a new object that stores some external data.</span></span>
  
## <span data-ttu-id="0c443-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c443-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalObject(  
   _In_opt_ void *data,  
   _In_opt_ JsFinalizeCallback finalizeCallback,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="0c443-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c443-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="0c443-107">Les données externes qui sont représentées par l’objet.</span><span class="sxs-lookup"><span data-stu-id="0c443-107">External data that the object will represent.</span></span> <span data-ttu-id="0c443-108">Est susceptible d’être null.</span><span class="sxs-lookup"><span data-stu-id="0c443-108">May be null.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="0c443-109">Rappel lors de la finalisation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0c443-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="0c443-110">Est susceptible d’être null.</span><span class="sxs-lookup"><span data-stu-id="0c443-110">May be null.</span></span>  
  
 `object`  
 <span data-ttu-id="0c443-111">Nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="0c443-111">The new object.</span></span>  
  
## <span data-ttu-id="0c443-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0c443-112">Return Value</span></span>  
 <span data-ttu-id="0c443-113">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0c443-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0c443-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0c443-114">Remarks</span></span>  
 <span data-ttu-id="0c443-115">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="0c443-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0c443-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c443-116">Requirements</span></span>  
 <span data-ttu-id="0c443-117">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0c443-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0c443-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c443-118">See Also</span></span>  
 [<span data-ttu-id="0c443-119">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0c443-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)