---
description: Analyse un script sérialisé et retourne une fonction qui représente le script.
title: Fonction JsParseSerializedScript | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsParseSerializedScript
helpviewer_keywords:
- JsParseSerializedScript function
ms.assetid: 40d0c7c4-fd5b-46ed-9e65-38c2db2fc859
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 66ecabb9d96c3f339625f93858444f55d25fd4d7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233308"
---
# <span data-ttu-id="5ce3a-103">JsParseSerializedScript Function</span><span class="sxs-lookup"><span data-stu-id="5ce3a-103">JsParseSerializedScript Function</span></span>

<span data-ttu-id="5ce3a-104">Analyse un script sérialisé et retourne une fonction qui représente le script.</span><span class="sxs-lookup"><span data-stu-id="5ce3a-104">Parses a serialized script and returns a function representing the script.</span></span>  
  
## <span data-ttu-id="5ce3a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ce3a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="5ce3a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ce3a-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="5ce3a-107">Script à analyser.</span><span class="sxs-lookup"><span data-stu-id="5ce3a-107">The script to parse.</span></span>  
  
 `buffer`  
 <span data-ttu-id="5ce3a-108">Script sérialisé.</span><span class="sxs-lookup"><span data-stu-id="5ce3a-108">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="5ce3a-109">Un cookie identifiant le script qui peut être utilisé par les contextes de script déboguables.</span><span class="sxs-lookup"><span data-stu-id="5ce3a-109">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="5ce3a-110">Emplacement à partir duquel provient le script.</span><span class="sxs-lookup"><span data-stu-id="5ce3a-110">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="5ce3a-111">Fonction qui représente le code de script.</span><span class="sxs-lookup"><span data-stu-id="5ce3a-111">A function representing the script code.</span></span>  
  
## <span data-ttu-id="5ce3a-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5ce3a-112">Return Value</span></span>  
 <span data-ttu-id="5ce3a-113">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5ce3a-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5ce3a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5ce3a-114">Remarks</span></span>  
 <span data-ttu-id="5ce3a-115">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="5ce3a-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="5ce3a-116">La mémoire tampon n’est pas conservée en mémoire par le moteur de script, de sorte que votre code doit rester actif tant qu’il peut être utilisé pour exécuter des scripts.</span><span class="sxs-lookup"><span data-stu-id="5ce3a-116">The buffer is not persisted in memory by the scripting engine, so your code must keep it alive for as long as it might be used to execute scripts.</span></span>  
  
## <span data-ttu-id="5ce3a-117">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="5ce3a-117">Requirements</span></span>  
 <span data-ttu-id="5ce3a-118">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5ce3a-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5ce3a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ce3a-119">See Also</span></span>  
 [<span data-ttu-id="5ce3a-120">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5ce3a-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
