---
description: Crée une nouvelle fonction JavaScript avec Name.
title: Fonction JsCreateNamedFunction | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 72f40d06-ab82-4fed-a632-68af6b4126c2
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b54add359422a9312a0ded641051fd04585f3d7e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233114"
---
# <span data-ttu-id="4a511-103">JsCreateNamedFunction Function</span><span class="sxs-lookup"><span data-stu-id="4a511-103">JsCreateNamedFunction Function</span></span>

<span data-ttu-id="4a511-104">Crée une nouvelle fonction JavaScript avec Name.</span><span class="sxs-lookup"><span data-stu-id="4a511-104">Creates a new JavaScript function with name.</span></span>
  
## <span data-ttu-id="4a511-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a511-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateNamedFunction(  
   _In_ JsValueRef name,  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="4a511-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a511-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="4a511-107">Nom de cette fonction qui sera utilisé à des fins de diagnostic et de stringification.</span><span class="sxs-lookup"><span data-stu-id="4a511-107">The name of this function that will be used for diagnostics and stringification purposes.</span></span>  
  
 `nativeFunction`  
 <span data-ttu-id="4a511-108">Méthode à appeler lors de l’appel de la fonction.</span><span class="sxs-lookup"><span data-stu-id="4a511-108">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="4a511-109">État fourni par l’utilisateur qui sera transmis au rappel.</span><span class="sxs-lookup"><span data-stu-id="4a511-109">User provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="4a511-110">Nouvel objet fonction.</span><span class="sxs-lookup"><span data-stu-id="4a511-110">The new function object.</span></span>  
  
## <span data-ttu-id="4a511-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4a511-111">Return Value</span></span>  
  
## <span data-ttu-id="4a511-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="4a511-112">Remarks</span></span>  
 <span data-ttu-id="4a511-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="4a511-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="4a511-114">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4a511-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="4a511-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="4a511-115">Requirements</span></span>  
 <span data-ttu-id="4a511-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4a511-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4a511-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a511-117">See Also</span></span>  
 [<span data-ttu-id="4a511-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4a511-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
