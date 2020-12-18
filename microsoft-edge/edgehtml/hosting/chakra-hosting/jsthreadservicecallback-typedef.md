---
description: Un rappel de service de thread.
title: JsThreadServiceCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5f1fe416e158e9524bdd1caab847977a5dd21b8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233128"
---
# <span data-ttu-id="f1c98-103">Typedef JsThreadServiceCallback</span><span class="sxs-lookup"><span data-stu-id="f1c98-103">JsThreadServiceCallback Typedef</span></span>

<span data-ttu-id="f1c98-104">Un rappel de service de thread.</span><span class="sxs-lookup"><span data-stu-id="f1c98-104">A thread service callback.</span></span>  
  
## <span data-ttu-id="f1c98-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1c98-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK *JsThreadServiceCallback)(  
   _In_ JsBackgroundWorkItemCallback callback,  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="f1c98-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1c98-106">Parameters</span></span>  
 <span data-ttu-id="f1c98-107">rappeler</span><span class="sxs-lookup"><span data-stu-id="f1c98-107">callback</span></span>  
 <span data-ttu-id="f1c98-108">Rappel pour l’élément de tâche en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f1c98-108">The callback for the background work item.</span></span>  
  
 <span data-ttu-id="f1c98-109">callbackData</span><span class="sxs-lookup"><span data-stu-id="f1c98-109">callbackData</span></span>  
 <span data-ttu-id="f1c98-110">L’argument Data à transmettre au rappel.</span><span class="sxs-lookup"><span data-stu-id="f1c98-110">The data argument to be passed to the callback.</span></span>  
  
## <span data-ttu-id="f1c98-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="f1c98-111">Remarks</span></span>  
 <span data-ttu-id="f1c98-112">L’hôte peut spécifier un service de thread en arrière-plan lors de l’appel de JsCreateRuntime.</span><span class="sxs-lookup"><span data-stu-id="f1c98-112">The host can specify a background thread service when calling JsCreateRuntime.</span></span> <span data-ttu-id="f1c98-113">Si ce paramètre est spécifié, les éléments de tâche en arrière-plan sont transmis à l’hôte à l’aide de ce rappel.</span><span class="sxs-lookup"><span data-stu-id="f1c98-113">If specified, then background work items will be passed to the host using this callback.</span></span> <span data-ttu-id="f1c98-114">L’hôte doit commencer immédiatement exécuter l’élément de tâche en arrière-plan et retourner true ou false, et le runtime doit gérer l’élément de bureau en thread.</span><span class="sxs-lookup"><span data-stu-id="f1c98-114">The host is expected to either begin executing the background work item immediately and return true or return false and the runtime will handle the work item in-thread.</span></span>  
  
## <span data-ttu-id="f1c98-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="f1c98-115">Requirements</span></span>  
 <span data-ttu-id="f1c98-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f1c98-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f1c98-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1c98-117">See Also</span></span>  
 [<span data-ttu-id="f1c98-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f1c98-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
