---
description: Démarre le débogage dans le contexte actuel.
title: Fonction JsStartDebugging | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStartDebugging
helpviewer_keywords:
- JsStartDebugging function
ms.assetid: c48ba02d-6d47-466f-a970-02f087d525f3
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 2c94a6f36ad72bfb9354c85d98ae0b5b4e9c77fb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566139"
---
# <span data-ttu-id="0f6c8-103">Fonction JsStartDebugging</span><span class="sxs-lookup"><span data-stu-id="0f6c8-103">JsStartDebugging Function</span></span>
<span data-ttu-id="0f6c8-104">Démarre le débogage dans le contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-104">Starts debugging in the current context.</span></span>  
  
## <span data-ttu-id="0f6c8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f6c8-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsStartDebugging();  
  
// Legacy mode signature  
STDAPI_(JsErrorCode)  JsStartDebugging(  
   _In_ IDebugApplication *debugApplication  
);  
```  
  
#### <span data-ttu-id="0f6c8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f6c8-106">Parameters</span></span>  
 `debugApplication`  
 <span data-ttu-id="0f6c8-107">Application de débogage à utiliser pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-107">The debug application to use for debugging.</span></span>  
  
## <span data-ttu-id="0f6c8-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0f6c8-108">Return Value</span></span>  
 <span data-ttu-id="0f6c8-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0f6c8-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="0f6c8-110">Remarks</span></span>  
 <span data-ttu-id="0f6c8-111">L’hôte doit s’assurer qu’il `CoInitializeEx` est appelé `COINIT_MULTITHREADED` ou `COINIT_APARTMENTTHREADED` au moins une fois avant d’utiliser cette API.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-111">The host should make sure that `CoInitializeEx` is called with `COINIT_MULTITHREADED` or `COINIT_APARTMENTTHREADED` at least once before using this API</span></span>  
  
 <span data-ttu-id="0f6c8-112">Le `debugApplication` paramètre n’est pas pris en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-112">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="0f6c8-113">Pour plus d’informations sur l’utilisation de cette API dans le mode Microsoft Edge, consultez [ciblage des moteurs Microsoft Edge et hérités](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="0f6c8-113">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="0f6c8-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f6c8-114">Requirements</span></span>  
 <span data-ttu-id="0f6c8-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0f6c8-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0f6c8-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f6c8-116">See Also</span></span>  
 [<span data-ttu-id="0f6c8-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0f6c8-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)