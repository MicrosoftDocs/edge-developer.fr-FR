---
description: Crée une nouvelle fonction JavaScript.
title: Fonction JsCreateFunction | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateFunction
helpviewer_keywords:
- JsCreateFunction function
ms.assetid: b298a96a-5ef7-4203-a8c8-55f9bfc6d2bb
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f7e67e86e6d8055664bfb1b58e6d5653f6d75d1b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233333"
---
# <span data-ttu-id="f1dae-103">JsCreateFunction Function</span><span class="sxs-lookup"><span data-stu-id="f1dae-103">JsCreateFunction Function</span></span>

<span data-ttu-id="f1dae-104">Crée une nouvelle fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f1dae-104">Creates a new JavaScript function.</span></span>
  
## <span data-ttu-id="f1dae-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1dae-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateFunction(  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="f1dae-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1dae-106">Parameters</span></span>  
 `nativeFunction`  
 <span data-ttu-id="f1dae-107">Méthode à appeler lors de l’appel de la fonction.</span><span class="sxs-lookup"><span data-stu-id="f1dae-107">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="f1dae-108">État fourni par l’utilisateur qui sera renvoyé au rappel.</span><span class="sxs-lookup"><span data-stu-id="f1dae-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="f1dae-109">Nouvel objet fonction.</span><span class="sxs-lookup"><span data-stu-id="f1dae-109">The new function object.</span></span>  
  
## <span data-ttu-id="f1dae-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f1dae-110">Return Value</span></span>  
 <span data-ttu-id="f1dae-111">Le résultat de l’appel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="f1dae-111">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="f1dae-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="f1dae-112">Remarks</span></span>  
 <span data-ttu-id="f1dae-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="f1dae-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f1dae-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="f1dae-114">Requirements</span></span>  
 <span data-ttu-id="f1dae-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f1dae-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f1dae-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1dae-116">See Also</span></span>  
 [<span data-ttu-id="f1dae-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f1dae-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
