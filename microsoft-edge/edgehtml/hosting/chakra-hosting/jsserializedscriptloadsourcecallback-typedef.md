---
description: Appelé par le runtime pour charger le code source du script sérialisé. L’appelant doit conserver le tampon de script valide jusqu’au `JsSerializedScriptUnloadCallback` .
title: JsSerializedScriptLoadSourceCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2bb30befc61003d20cdeaa293fd1fdfdc95b36f7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233535"
---
# <span data-ttu-id="cf73b-104">Typedef JsSerializedScriptLoadSourceCallback</span><span class="sxs-lookup"><span data-stu-id="cf73b-104">JsSerializedScriptLoadSourceCallback Typedef</span></span>

<span data-ttu-id="cf73b-105">Appelé par le runtime pour charger le code source du script sérialisé.</span><span class="sxs-lookup"><span data-stu-id="cf73b-105">Called by the runtime to load the source code of the serialized script.</span></span> <span data-ttu-id="cf73b-106">L’appelant doit conserver le tampon de script valide jusqu’au `JsSerializedScriptUnloadCallback` .</span><span class="sxs-lookup"><span data-stu-id="cf73b-106">The caller must keep the script buffer valid until the `JsSerializedScriptUnloadCallback`.</span></span>  
  
## <span data-ttu-id="cf73b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf73b-107">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### <span data-ttu-id="cf73b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf73b-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="cf73b-109">Le contexte transmis à `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="cf73b-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
 `scriptBuffer`  
 <span data-ttu-id="cf73b-110">Le script renvoyé.</span><span class="sxs-lookup"><span data-stu-id="cf73b-110">The script returned.</span></span>  
  
## <span data-ttu-id="cf73b-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="cf73b-111">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="cf73b-112">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="cf73b-112">Requirements</span></span>  
 <span data-ttu-id="cf73b-113">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cf73b-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cf73b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf73b-114">See Also</span></span>  
 [<span data-ttu-id="cf73b-115">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="cf73b-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
