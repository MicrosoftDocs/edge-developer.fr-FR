---
description: 'Attributs d’un Runtime. '
title: Énumération JsRuntimeAttributes | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRuntimeAttributes
helpviewer_keywords:
- JsRuntimeAttributes enumeration
ms.assetid: f76d82e9-a695-4d6a-96c1-b3a4d27fed68
caps.latest.revision: 14
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bbc5341c3214d9796278d334507e284989ff45dd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233098"
---
# <span data-ttu-id="50631-103">Énumération JsRuntimeAttributes</span><span class="sxs-lookup"><span data-stu-id="50631-103">JsRuntimeAttributes Enumeration</span></span>

<span data-ttu-id="50631-104">Attributs d’un Runtime.</span><span class="sxs-lookup"><span data-stu-id="50631-104">Attributes of a runtime.</span></span>  
  
## <span data-ttu-id="50631-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50631-105">Syntax</span></span>  
  
```cpp  
enum JsRuntimeAttributes;  
```  
  
## <span data-ttu-id="50631-106">Ses</span><span class="sxs-lookup"><span data-stu-id="50631-106">Members</span></span>  
  
### <span data-ttu-id="50631-107">Doubl</span><span class="sxs-lookup"><span data-stu-id="50631-107">Values</span></span>  
  
|<span data-ttu-id="50631-108">Nom</span><span class="sxs-lookup"><span data-stu-id="50631-108">Name</span></span>|<span data-ttu-id="50631-109">Description</span><span class="sxs-lookup"><span data-stu-id="50631-109">Description</span></span>|  
|----------|-----------------|  
|`JsRuntimeAttributeAllowScriptInterrupt`|<span data-ttu-id="50631-110">Le Runtime doit prendre en charge l’interruption du script fiable.</span><span class="sxs-lookup"><span data-stu-id="50631-110">The runtime should support reliable script interruption.</span></span> <span data-ttu-id="50631-111">Cela augmente le nombre d’emplacements dans lesquels le runtime recherche une requête d’interruption de script au coût d’une petite quantité de performances d’exécution.</span><span class="sxs-lookup"><span data-stu-id="50631-111">This increases the number of places where the runtime will check for a script interrupt request at the cost of a small amount of runtime performance.</span></span>|  
|`JsRuntimeAttributeDisableBackgroundWork`|<span data-ttu-id="50631-112">Le runtime ne fonctionnera pas (par exemple, le nettoyage de la mémoire) sur les threads d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="50631-112">The runtime will not do any work (such as garbage collection) on background threads.</span></span>|  
|`JsRuntimeAttributeDisableEval`|<span data-ttu-id="50631-113">L’utilisation `eval` de ou du `function` constructeur lèvera une exception.</span><span class="sxs-lookup"><span data-stu-id="50631-113">Using `eval` or `function` constructor will throw an exception.</span></span>|  
|`JsRuntimeAttributeDisableNativeCodeGeneration`|<span data-ttu-id="50631-114">Runtime ne génère pas de code natif.</span><span class="sxs-lookup"><span data-stu-id="50631-114">Runtime will not generate native code.</span></span>|  
|`JsRuntimeAttributeEnableExperimentalFeatures`|<span data-ttu-id="50631-115">Runtime active toutes les fonctionnalités expérimentales.</span><span class="sxs-lookup"><span data-stu-id="50631-115">Runtime will enable all experimental features.</span></span>|  
|`JsRuntimeAttributeEnableIdleProcessing`|<span data-ttu-id="50631-116">L’hôte appelle alors le `JsIdle` traitement inactif.</span><span class="sxs-lookup"><span data-stu-id="50631-116">Host will call `JsIdle`, so enable idle processing.</span></span> <span data-ttu-id="50631-117">Dans le cas contraire, le runtime va gérer la mémoire de manière légèrement plus agressive.</span><span class="sxs-lookup"><span data-stu-id="50631-117">Otherwise, the runtime will manage memory slightly more aggressively.</span></span>|  
|`JsRuntimeAttributeDispatchSetExceptionsToDebugger`|<span data-ttu-id="50631-118">Les appels `JsSetException` sont également distribués à l’exception sur le débogueur de script (le cas échéant), ce qui donne au débogueur la possibilité de s’arrêter sur l’exception.</span><span class="sxs-lookup"><span data-stu-id="50631-118">Calling `JsSetException` will also dispatch the exception to the script debugger (if any) giving the debugger a chance to break on the exception.</span></span>|  
|`JsRuntimeAttributeNone`|<span data-ttu-id="50631-119">Aucun attribut spécial.</span><span class="sxs-lookup"><span data-stu-id="50631-119">No special attributes.</span></span>|  
  
## <span data-ttu-id="50631-120">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="50631-120">Requirements</span></span>  
 <span data-ttu-id="50631-121">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="50631-121">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="50631-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50631-122">See Also</span></span>  
 [<span data-ttu-id="50631-123">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="50631-123">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
