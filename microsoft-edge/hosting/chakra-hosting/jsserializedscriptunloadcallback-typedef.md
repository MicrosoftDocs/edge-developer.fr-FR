---
description: Appelé par le runtime lorsque toutes les ressources associées à l’exécution du script sont terminées. L’appelant doit libérer la source en cas de chargement, le code d’octet et le contexte pour le moment.
title: JsSerializedScriptUnloadCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c3da27af18ebc7a1913980a865d926bac6a29d11
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751939"
---
# <span data-ttu-id="5b0d0-104">Typedef JsSerializedScriptUnloadCallback</span><span class="sxs-lookup"><span data-stu-id="5b0d0-104">JsSerializedScriptUnloadCallback typedef</span></span>
<span data-ttu-id="5b0d0-105">Appelé par le runtime lorsque toutes les ressources associées à l’exécution du script sont terminées.</span><span class="sxs-lookup"><span data-stu-id="5b0d0-105">Called by the runtime when it is finished with all resources related to the script execution.</span></span> <span data-ttu-id="5b0d0-106">L’appelant doit libérer la source en cas de chargement, le code d’octet et le contexte pour le moment.</span><span class="sxs-lookup"><span data-stu-id="5b0d0-106">The caller should free the source if loaded, the byte code, and the context at this time.</span></span>  
  
## <span data-ttu-id="5b0d0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b0d0-107">Syntax</span></span>  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### <span data-ttu-id="5b0d0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b0d0-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="5b0d0-109">Le contexte transmis à `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="5b0d0-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
## <span data-ttu-id="5b0d0-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="5b0d0-110">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="5b0d0-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b0d0-111">Requirements</span></span>  
 <span data-ttu-id="5b0d0-112">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5b0d0-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5b0d0-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b0d0-113">See Also</span></span>  
 [<span data-ttu-id="5b0d0-114">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5b0d0-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)