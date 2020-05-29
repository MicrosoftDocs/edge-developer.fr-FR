---
description: Exécute un script sérialisé.
title: Fonction JsRunSerializedScript | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRunSerializedScript
helpviewer_keywords:
- JsRunSerializedScript function
ms.assetid: 3fd3f6f1-eb3e-4751-92a5-c93b1035f3b2
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bc1e2fb7fdc5df52fde3b7cc59cf9173d658782a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566269"
---
# <span data-ttu-id="9d64c-103">Fonction JsRunSerializedScript</span><span class="sxs-lookup"><span data-stu-id="9d64c-103">JsRunSerializedScript Function</span></span>
<span data-ttu-id="9d64c-104">Exécute un script sérialisé.</span><span class="sxs-lookup"><span data-stu-id="9d64c-104">Runs a serialized script.</span></span>  
  
## <span data-ttu-id="9d64c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d64c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="9d64c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d64c-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="9d64c-107">Code source du script sérialisé.</span><span class="sxs-lookup"><span data-stu-id="9d64c-107">The source code of the serialized script.</span></span>  
  
 `buffer`  
 <span data-ttu-id="9d64c-108">Script sérialisé.</span><span class="sxs-lookup"><span data-stu-id="9d64c-108">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="9d64c-109">Un cookie identifiant le script qui peut être utilisé par les contextes de script déboguables.</span><span class="sxs-lookup"><span data-stu-id="9d64c-109">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="9d64c-110">Emplacement à partir duquel provient le script.</span><span class="sxs-lookup"><span data-stu-id="9d64c-110">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="9d64c-111">Résultat de l’exécution du script, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="9d64c-111">The result of running the script, if any.</span></span> <span data-ttu-id="9d64c-112">Ce paramètre peut être null.</span><span class="sxs-lookup"><span data-stu-id="9d64c-112">This parameter can be null.</span></span>  
  
## <span data-ttu-id="9d64c-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9d64c-113">Return Value</span></span>  
 <span data-ttu-id="9d64c-114">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9d64c-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9d64c-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="9d64c-115">Remarks</span></span>  
 <span data-ttu-id="9d64c-116">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="9d64c-116">Requires an active script context.</span></span>  
  
 <span data-ttu-id="9d64c-117">La mémoire tampon n’est pas conservée en mémoire par le moteur de script, de sorte que votre code doit rester actif tant qu’il peut être utilisé pour exécuter des scripts.</span><span class="sxs-lookup"><span data-stu-id="9d64c-117">The buffer is not persisted in memory by the scripting engine, so your code must keep it alive for as long as it might be used to execute scripts.</span></span>  
  
## <span data-ttu-id="9d64c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d64c-118">Requirements</span></span>  
 <span data-ttu-id="9d64c-119">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9d64c-119">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9d64c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d64c-120">See Also</span></span>  
 [<span data-ttu-id="9d64c-121">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9d64c-121">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)