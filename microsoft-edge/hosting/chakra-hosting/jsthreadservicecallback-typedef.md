---
description: Un rappel de service de thread.
title: JsThreadServiceCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5eb9f2986c79db024f01f4d22050f79c9689400c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565135"
---
# <span data-ttu-id="a82d2-103">JsThreadServiceCallback typedef</span><span class="sxs-lookup"><span data-stu-id="a82d2-103">JsThreadServiceCallback Typedef</span></span>
<span data-ttu-id="a82d2-104">Un rappel de service de thread.</span><span class="sxs-lookup"><span data-stu-id="a82d2-104">A thread service callback.</span></span>  
  
## <span data-ttu-id="a82d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a82d2-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK *JsThreadServiceCallback)(  
   _In_ JsBackgroundWorkItemCallback callback,  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="a82d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a82d2-106">Parameters</span></span>  
 <span data-ttu-id="a82d2-107">rappeler</span><span class="sxs-lookup"><span data-stu-id="a82d2-107">callback</span></span>  
 <span data-ttu-id="a82d2-108">Rappel pour l’élément de tâche en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="a82d2-108">The callback for the background work item.</span></span>  
  
 <span data-ttu-id="a82d2-109">callbackData</span><span class="sxs-lookup"><span data-stu-id="a82d2-109">callbackData</span></span>  
 <span data-ttu-id="a82d2-110">L’argument Data à transmettre au rappel.</span><span class="sxs-lookup"><span data-stu-id="a82d2-110">The data argument to be passed to the callback.</span></span>  
  
## <span data-ttu-id="a82d2-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="a82d2-111">Remarks</span></span>  
 <span data-ttu-id="a82d2-112">L’hôte peut spécifier un service de thread en arrière-plan lors de l’appel de JsCreateRuntime.</span><span class="sxs-lookup"><span data-stu-id="a82d2-112">The host can specify a background thread service when calling JsCreateRuntime.</span></span> <span data-ttu-id="a82d2-113">Si ce paramètre est spécifié, les éléments de tâche en arrière-plan sont transmis à l’hôte à l’aide de ce rappel.</span><span class="sxs-lookup"><span data-stu-id="a82d2-113">If specified, then background work items will be passed to the host using this callback.</span></span> <span data-ttu-id="a82d2-114">L’hôte doit commencer immédiatement exécuter l’élément de tâche en arrière-plan et retourner true ou false, et le runtime doit gérer l’élément de bureau en thread.</span><span class="sxs-lookup"><span data-stu-id="a82d2-114">The host is expected to either begin executing the background work item immediately and return true or return false and the runtime will handle the work item in-thread.</span></span>  
  
## <span data-ttu-id="a82d2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a82d2-115">Requirements</span></span>  
 <span data-ttu-id="a82d2-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a82d2-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a82d2-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a82d2-117">See Also</span></span>  
 [<span data-ttu-id="a82d2-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a82d2-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)