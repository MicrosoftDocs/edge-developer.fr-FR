---
description: Appelé par le runtime lorsque toutes les ressources associées à l’exécution du script sont terminées. L’appelant doit libérer la source en cas de chargement, le code d’octet et le contexte pour le moment.
title: JsSerializedScriptUnloadCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5c63f2ff3faf21a19e31f2f6fd1692e21d59fc0b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233485"
---
# <span data-ttu-id="c7ff2-104">Typedef JsSerializedScriptUnloadCallback</span><span class="sxs-lookup"><span data-stu-id="c7ff2-104">JsSerializedScriptUnloadCallback typedef</span></span>

<span data-ttu-id="c7ff2-105">Appelé par le runtime lorsque toutes les ressources associées à l’exécution du script sont terminées.</span><span class="sxs-lookup"><span data-stu-id="c7ff2-105">Called by the runtime when it is finished with all resources related to the script execution.</span></span> <span data-ttu-id="c7ff2-106">L’appelant doit libérer la source en cas de chargement, le code d’octet et le contexte pour le moment.</span><span class="sxs-lookup"><span data-stu-id="c7ff2-106">The caller should free the source if loaded, the byte code, and the context at this time.</span></span>  
  
## <span data-ttu-id="c7ff2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7ff2-107">Syntax</span></span>  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### <span data-ttu-id="c7ff2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7ff2-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="c7ff2-109">Le contexte transmis à `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="c7ff2-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
## <span data-ttu-id="c7ff2-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="c7ff2-110">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="c7ff2-111">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="c7ff2-111">Requirements</span></span>  
 <span data-ttu-id="c7ff2-112">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c7ff2-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c7ff2-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7ff2-113">See Also</span></span>  
 [<span data-ttu-id="c7ff2-114">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c7ff2-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
