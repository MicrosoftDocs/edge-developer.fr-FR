---
description: Démarre le débogage dans le contexte actuel.
title: Fonction JsStartDebugging | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStartDebugging
helpviewer_keywords:
- JsStartDebugging function
ms.assetid: c48ba02d-6d47-466f-a970-02f087d525f3
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9685779911db8e3045986682b66d13e38c70fe8d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233469"
---
# <span data-ttu-id="0f379-103">JsStartDebugging Function</span><span class="sxs-lookup"><span data-stu-id="0f379-103">JsStartDebugging Function</span></span>

<span data-ttu-id="0f379-104">Démarre le débogage dans le contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="0f379-104">Starts debugging in the current context.</span></span>  
  
## <span data-ttu-id="0f379-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f379-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsStartDebugging();  
  
// Legacy mode signature  
STDAPI_(JsErrorCode)  JsStartDebugging(  
   _In_ IDebugApplication *debugApplication  
);  
```  
  
#### <span data-ttu-id="0f379-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f379-106">Parameters</span></span>  
 `debugApplication`  
 <span data-ttu-id="0f379-107">Application de débogage à utiliser pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="0f379-107">The debug application to use for debugging.</span></span>  
  
## <span data-ttu-id="0f379-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0f379-108">Return Value</span></span>  
 <span data-ttu-id="0f379-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0f379-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0f379-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="0f379-110">Remarks</span></span>  
 <span data-ttu-id="0f379-111">L’hôte doit s’assurer qu’il `CoInitializeEx` est appelé `COINIT_MULTITHREADED` ou `COINIT_APARTMENTTHREADED` au moins une fois avant d’utiliser cette API.</span><span class="sxs-lookup"><span data-stu-id="0f379-111">The host should make sure that `CoInitializeEx` is called with `COINIT_MULTITHREADED` or `COINIT_APARTMENTTHREADED` at least once before using this API</span></span>  
  
 <span data-ttu-id="0f379-112">Le `debugApplication` paramètre n’est pas pris en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0f379-112">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="0f379-113">Pour plus d’informations sur l’utilisation de cette API dans le mode Microsoft Edge, consultez [ciblage des moteurs Microsoft Edge et hérités](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="0f379-113">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="0f379-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="0f379-114">Requirements</span></span>  
 <span data-ttu-id="0f379-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0f379-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0f379-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f379-116">See Also</span></span>  
 [<span data-ttu-id="0f379-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0f379-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
