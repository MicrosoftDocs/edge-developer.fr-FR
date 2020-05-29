---
description: Crée un nouveau Runtime.
title: Fonction JsCreateRuntime | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRuntime
helpviewer_keywords:
- JsCreateRuntime function
ms.assetid: 92d09b89-6593-4d73-a562-88f9fec10228
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d25c1b46354be1fda0ce906dc68c3643989fe2c6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565222"
---
# <span data-ttu-id="7f981-103">Fonction JsCreateRuntime</span><span class="sxs-lookup"><span data-stu-id="7f981-103">JsCreateRuntime Function</span></span>
<span data-ttu-id="7f981-104">Crée un nouveau Runtime.</span><span class="sxs-lookup"><span data-stu-id="7f981-104">Creates a new runtime.</span></span>
  
## <span data-ttu-id="7f981-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f981-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_ JsRuntimeVersion version,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### <span data-ttu-id="7f981-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f981-106">Parameters</span></span>  
 `attributes`  
 <span data-ttu-id="7f981-107">Attributs du runtime à créer.</span><span class="sxs-lookup"><span data-stu-id="7f981-107">The attributes of the runtime to be created.</span></span>  
  
 `version`  
 <span data-ttu-id="7f981-108">Version du runtime à créer.</span><span class="sxs-lookup"><span data-stu-id="7f981-108">The version of the runtime to be created.</span></span>  
  
 `threadService`  
 <span data-ttu-id="7f981-109">Service de thread pour le Runtime.</span><span class="sxs-lookup"><span data-stu-id="7f981-109">The thread service for the runtime.</span></span> <span data-ttu-id="7f981-110">Peut être null.</span><span class="sxs-lookup"><span data-stu-id="7f981-110">Can be null.</span></span>  
  
 `runtime`  
 <span data-ttu-id="7f981-111">Le runtime a été créé.</span><span class="sxs-lookup"><span data-stu-id="7f981-111">The runtime created.</span></span>  
  
## <span data-ttu-id="7f981-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7f981-112">Return Value</span></span>  
 <span data-ttu-id="7f981-113">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7f981-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7f981-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7f981-114">Remarks</span></span>  
 <span data-ttu-id="7f981-115">Le `version` paramètre n’est pas pris en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7f981-115">The `version` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="7f981-116">Pour plus d’informations sur l’utilisation de cette API dans le mode Microsoft Edge, consultez [ciblage des moteurs Microsoft Edge et hérités](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="7f981-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="7f981-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f981-117">Requirements</span></span>  
 <span data-ttu-id="7f981-118">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7f981-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7f981-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f981-119">See Also</span></span>  
 [<span data-ttu-id="7f981-120">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7f981-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)