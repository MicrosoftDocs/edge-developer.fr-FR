---
description: Rappel de continuation de promesse.
title: JsPromiseContinuationCallback typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 023d88af5ff82056d8f57453e0a53b91b34565a6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565137"
---
# <span data-ttu-id="75c8f-103">JsPromiseContinuationCallback typedef</span><span class="sxs-lookup"><span data-stu-id="75c8f-103">JsPromiseContinuationCallback Typedef</span></span>
<span data-ttu-id="75c8f-104">Rappel de continuation de promesse.</span><span class="sxs-lookup"><span data-stu-id="75c8f-104">A promise continuation callback.</span></span>  
  
## <span data-ttu-id="75c8f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75c8f-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsPromiseContinuationCallback)(  
  _In_ JsValueRef task,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="75c8f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75c8f-106">Parameters</span></span>  
 `task`  
  `callbackState`  
  
## <span data-ttu-id="75c8f-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="75c8f-107">Remarks</span></span>  
 <span data-ttu-id="75c8f-108">L’hôte peut spécifier un rappel de continuation de promesse en `JsSetPromiseContinuationCallback` .</span><span class="sxs-lookup"><span data-stu-id="75c8f-108">The host can specify a promise continuation callback in `JsSetPromiseContinuationCallback`.</span></span> <span data-ttu-id="75c8f-109">Si un script crée une tâche à exécuter par la suite, le rappel de continuation à la suite sera appelé par la tâche et la tâche doit être placée dans une file d’attente FIFO pour être exécutée à la fin de l’exécution du script actuel.</span><span class="sxs-lookup"><span data-stu-id="75c8f-109">If a script creates a task to be run later, then the promise continuation callback will be called with the task and the task should be put in a FIFO queue, to be run when the current script is done executing.</span></span>  
  
 <span data-ttu-id="75c8f-110">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="75c8f-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="75c8f-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75c8f-111">Requirements</span></span>  
 <span data-ttu-id="75c8f-112">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="75c8f-112">jsrt.h</span></span>  
  
## <span data-ttu-id="75c8f-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75c8f-113">See Also</span></span>  
 [<span data-ttu-id="75c8f-114">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="75c8f-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)