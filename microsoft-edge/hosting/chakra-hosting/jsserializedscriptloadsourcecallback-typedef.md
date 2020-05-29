---
description: Appelé par le runtime pour charger le code source du script sérialisé. L’appelant doit conserver le tampon de script valide jusqu’au `JsSerializedScriptUnloadCallback` .
title: JsSerializedScriptLoadSourceCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bc1264bdc77da10cadb44a570ae37e7f3cd9ce6b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566255"
---
# <span data-ttu-id="b4901-104">JsSerializedScriptLoadSourceCallback typedef</span><span class="sxs-lookup"><span data-stu-id="b4901-104">JsSerializedScriptLoadSourceCallback Typedef</span></span>
<span data-ttu-id="b4901-105">Appelé par le runtime pour charger le code source du script sérialisé.</span><span class="sxs-lookup"><span data-stu-id="b4901-105">Called by the runtime to load the source code of the serialized script.</span></span> <span data-ttu-id="b4901-106">L’appelant doit conserver le tampon de script valide jusqu’au `JsSerializedScriptUnloadCallback` .</span><span class="sxs-lookup"><span data-stu-id="b4901-106">The caller must keep the script buffer valid until the `JsSerializedScriptUnloadCallback`.</span></span>  
  
## <span data-ttu-id="b4901-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4901-107">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### <span data-ttu-id="b4901-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4901-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="b4901-109">Le contexte transmis à `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="b4901-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
 `scriptBuffer`  
 <span data-ttu-id="b4901-110">Le script renvoyé.</span><span class="sxs-lookup"><span data-stu-id="b4901-110">The script returned.</span></span>  
  
## <span data-ttu-id="b4901-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="b4901-111">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="b4901-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4901-112">Requirements</span></span>  
 <span data-ttu-id="b4901-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b4901-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b4901-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4901-114">See Also</span></span>  
 [<span data-ttu-id="b4901-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b4901-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)