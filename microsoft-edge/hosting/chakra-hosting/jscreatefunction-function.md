---
description: Crée une nouvelle fonction JavaScript.
title: Fonction JsCreateFunction | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateFunction
helpviewer_keywords:
- JsCreateFunction function
ms.assetid: b298a96a-5ef7-4203-a8c8-55f9bfc6d2bb
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 22585afcb379c281eda621c3b233ccf4bc278ad1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565231"
---
# <span data-ttu-id="728de-103">Fonction JsCreateFunction</span><span class="sxs-lookup"><span data-stu-id="728de-103">JsCreateFunction Function</span></span>
<span data-ttu-id="728de-104">Crée une nouvelle fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="728de-104">Creates a new JavaScript function.</span></span>
  
## <span data-ttu-id="728de-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="728de-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateFunction(  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="728de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="728de-106">Parameters</span></span>  
 `nativeFunction`  
 <span data-ttu-id="728de-107">Méthode à appeler lors de l’appel de la fonction.</span><span class="sxs-lookup"><span data-stu-id="728de-107">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="728de-108">État fourni par l’utilisateur qui sera renvoyé au rappel.</span><span class="sxs-lookup"><span data-stu-id="728de-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="728de-109">Nouvel objet fonction.</span><span class="sxs-lookup"><span data-stu-id="728de-109">The new function object.</span></span>  
  
## <span data-ttu-id="728de-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="728de-110">Return Value</span></span>  
 <span data-ttu-id="728de-111">Le résultat de l’appel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="728de-111">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="728de-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="728de-112">Remarks</span></span>  
 <span data-ttu-id="728de-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="728de-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="728de-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="728de-114">Requirements</span></span>  
 <span data-ttu-id="728de-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="728de-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="728de-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="728de-116">See Also</span></span>  
 [<span data-ttu-id="728de-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="728de-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)