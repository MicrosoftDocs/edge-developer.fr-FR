---
description: Appelé par le runtime lorsque toutes les ressources associées à l’exécution du script sont terminées. L’appelant doit libérer la source en cas de chargement, le code d’octet et le contexte pour le moment.
title: JsSerializedScriptUnloadCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9555b3fd8c14c9629d17c13592e3c78a78be150e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566254"
---
# <span data-ttu-id="06db1-104">JsSerializedScriptUnloadCallback typedef</span><span class="sxs-lookup"><span data-stu-id="06db1-104">JsSerializedScriptUnloadCallback typedef</span></span>
<span data-ttu-id="06db1-105">Appelé par le runtime lorsque toutes les ressources associées à l’exécution du script sont terminées.</span><span class="sxs-lookup"><span data-stu-id="06db1-105">Called by the runtime when it is finished with all resources related to the script execution.</span></span> <span data-ttu-id="06db1-106">L’appelant doit libérer la source en cas de chargement, le code d’octet et le contexte pour le moment.</span><span class="sxs-lookup"><span data-stu-id="06db1-106">The caller should free the source if loaded, the byte code, and the context at this time.</span></span>  
  
## <span data-ttu-id="06db1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06db1-107">Syntax</span></span>  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### <span data-ttu-id="06db1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06db1-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="06db1-109">Le contexte transmis à `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="06db1-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
## <span data-ttu-id="06db1-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="06db1-110">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="06db1-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06db1-111">Requirements</span></span>  
 <span data-ttu-id="06db1-112">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="06db1-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="06db1-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06db1-113">See Also</span></span>  
 [<span data-ttu-id="06db1-114">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="06db1-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)