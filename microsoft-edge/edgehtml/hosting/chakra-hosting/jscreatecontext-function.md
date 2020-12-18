---
description: Crée un contexte de script pour exécuter des scripts.
title: Fonction JsCreateContext | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateContext
helpviewer_keywords:
- JsCreateContext function
ms.assetid: aceca043-2c73-4029-a06c-8ad6695109cf
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5d6c8149b8a5e5fee7cbc8dac821713b1d9649ee
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232976"
---
# <span data-ttu-id="0f4b7-103">JsCreateContext Function</span><span class="sxs-lookup"><span data-stu-id="0f4b7-103">JsCreateContext Function</span></span>

<span data-ttu-id="0f4b7-104">Crée un contexte de script pour exécuter des scripts.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-104">Creates a script context for running scripts.</span></span>  
  
## <span data-ttu-id="0f4b7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f4b7-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ JsContextRef *newContext);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _In_ IDebugApplication *debugApplication,  
   _Out_ JsContextRef *newContext  
);  
```  
  
#### <span data-ttu-id="0f4b7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f4b7-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="0f4b7-107">Exécution du contexte de script en cours de création.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-107">The runtime the script context is being created in.</span></span>  
  
 `debugApplication`  
 <span data-ttu-id="0f4b7-108">Application de débogage à utiliser pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-108">The debug application to use for debugging.</span></span> <span data-ttu-id="0f4b7-109">Ce paramètre peut être null, auquel cas le débogage n’est pas activé pour le contexte.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-109">This parameter can be null, in which case debugging is not enabled for the context.</span></span>  
  
 `newContext`  
 <span data-ttu-id="0f4b7-110">Contexte de script créé.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-110">The created script context.</span></span>  
  
## <span data-ttu-id="0f4b7-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0f4b7-111">Return Value</span></span>  
 <span data-ttu-id="0f4b7-112">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0f4b7-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="0f4b7-113">Remarks</span></span>  
 <span data-ttu-id="0f4b7-114">Chaque contexte de script possède son propre objet global qui est isolé des autres contextes de script.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-114">Each script context has its own global object that is isolated from all other script contexts.</span></span>  
  
 <span data-ttu-id="0f4b7-115">Le `debugApplication` paramètre n’est pas pris en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-115">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="0f4b7-116">Pour plus d’informations sur l’utilisation de cette API dans le mode Microsoft Edge, consultez [ciblage des moteurs Microsoft Edge et hérités](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="0f4b7-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="0f4b7-117">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="0f4b7-117">Requirements</span></span>  
 <span data-ttu-id="0f4b7-118">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0f4b7-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0f4b7-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f4b7-119">See Also</span></span>  
 [<span data-ttu-id="0f4b7-120">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0f4b7-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
