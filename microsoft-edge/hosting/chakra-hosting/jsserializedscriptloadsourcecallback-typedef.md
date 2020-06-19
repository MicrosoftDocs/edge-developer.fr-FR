---
description: Appelé par le runtime pour charger le code source du script sérialisé. L’appelant doit conserver le tampon de script valide jusqu’au `JsSerializedScriptUnloadCallback` .
title: JsSerializedScriptLoadSourceCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 571314145cc19513f04174a9a1c93822a5795b29
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752198"
---
# <span data-ttu-id="87b52-104">Typedef JsSerializedScriptLoadSourceCallback</span><span class="sxs-lookup"><span data-stu-id="87b52-104">JsSerializedScriptLoadSourceCallback Typedef</span></span>
<span data-ttu-id="87b52-105">Appelé par le runtime pour charger le code source du script sérialisé.</span><span class="sxs-lookup"><span data-stu-id="87b52-105">Called by the runtime to load the source code of the serialized script.</span></span> <span data-ttu-id="87b52-106">L’appelant doit conserver le tampon de script valide jusqu’au `JsSerializedScriptUnloadCallback` .</span><span class="sxs-lookup"><span data-stu-id="87b52-106">The caller must keep the script buffer valid until the `JsSerializedScriptUnloadCallback`.</span></span>  
  
## <span data-ttu-id="87b52-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87b52-107">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### <span data-ttu-id="87b52-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87b52-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="87b52-109">Le contexte transmis à `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="87b52-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
 `scriptBuffer`  
 <span data-ttu-id="87b52-110">Le script renvoyé.</span><span class="sxs-lookup"><span data-stu-id="87b52-110">The script returned.</span></span>  
  
## <span data-ttu-id="87b52-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="87b52-111">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="87b52-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87b52-112">Requirements</span></span>  
 <span data-ttu-id="87b52-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="87b52-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="87b52-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87b52-114">See Also</span></span>  
 [<span data-ttu-id="87b52-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="87b52-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)