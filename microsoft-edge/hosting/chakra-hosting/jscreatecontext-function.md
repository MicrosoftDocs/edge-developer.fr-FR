---
description: Crée un contexte de script pour exécuter des scripts.
title: Fonction JsCreateContext | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateContext
helpviewer_keywords:
- JsCreateContext function
ms.assetid: aceca043-2c73-4029-a06c-8ad6695109cf
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 06bd4c4780a8c7610ebc95cfc0da058306ce5b78
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565242"
---
# <span data-ttu-id="cfe9b-103">Fonction JsCreateContext</span><span class="sxs-lookup"><span data-stu-id="cfe9b-103">JsCreateContext Function</span></span>
<span data-ttu-id="cfe9b-104">Crée un contexte de script pour exécuter des scripts.</span><span class="sxs-lookup"><span data-stu-id="cfe9b-104">Creates a script context for running scripts.</span></span>  
  
## <span data-ttu-id="cfe9b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfe9b-105">Syntax</span></span>  
  
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
  
#### <span data-ttu-id="cfe9b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfe9b-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="cfe9b-107">Exécution du contexte de script en cours de création.</span><span class="sxs-lookup"><span data-stu-id="cfe9b-107">The runtime the script context is being created in.</span></span>  
  
 `debugApplication`  
 <span data-ttu-id="cfe9b-108">Application de débogage à utiliser pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="cfe9b-108">The debug application to use for debugging.</span></span> <span data-ttu-id="cfe9b-109">Ce paramètre peut être null, auquel cas le débogage n’est pas activé pour le contexte.</span><span class="sxs-lookup"><span data-stu-id="cfe9b-109">This parameter can be null, in which case debugging is not enabled for the context.</span></span>  
  
 `newContext`  
 <span data-ttu-id="cfe9b-110">Contexte de script créé.</span><span class="sxs-lookup"><span data-stu-id="cfe9b-110">The created script context.</span></span>  
  
## <span data-ttu-id="cfe9b-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cfe9b-111">Return Value</span></span>  
 <span data-ttu-id="cfe9b-112">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="cfe9b-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="cfe9b-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="cfe9b-113">Remarks</span></span>  
 <span data-ttu-id="cfe9b-114">Chaque contexte de script possède son propre objet global qui est isolé des autres contextes de script.</span><span class="sxs-lookup"><span data-stu-id="cfe9b-114">Each script context has its own global object that is isolated from all other script contexts.</span></span>  
  
 <span data-ttu-id="cfe9b-115">Le `debugApplication` paramètre n’est pas pris en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cfe9b-115">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="cfe9b-116">Pour plus d’informations sur l’utilisation de cette API dans le mode Microsoft Edge, consultez [ciblage des moteurs Microsoft Edge et hérités](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="cfe9b-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="cfe9b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cfe9b-117">Requirements</span></span>  
 <span data-ttu-id="cfe9b-118">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cfe9b-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cfe9b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfe9b-119">See Also</span></span>  
 [<span data-ttu-id="cfe9b-120">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="cfe9b-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)