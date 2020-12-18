---
description: Rappel de continuation de promesse.
title: JsPromiseContinuationCallback typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da121d186cd9d0ab1a9770be08c9a92b52cf3366
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233536"
---
# <span data-ttu-id="3f577-103">Typedef JsPromiseContinuationCallback</span><span class="sxs-lookup"><span data-stu-id="3f577-103">JsPromiseContinuationCallback Typedef</span></span>

<span data-ttu-id="3f577-104">Rappel de continuation de promesse.</span><span class="sxs-lookup"><span data-stu-id="3f577-104">A promise continuation callback.</span></span>  
  
## <span data-ttu-id="3f577-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f577-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsPromiseContinuationCallback)(  
  _In_ JsValueRef task,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="3f577-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f577-106">Parameters</span></span>  
 `task`  
  `callbackState`  
  
## <span data-ttu-id="3f577-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="3f577-107">Remarks</span></span>  
 <span data-ttu-id="3f577-108">L’hôte peut spécifier un rappel de continuation de promesse en `JsSetPromiseContinuationCallback` .</span><span class="sxs-lookup"><span data-stu-id="3f577-108">The host can specify a promise continuation callback in `JsSetPromiseContinuationCallback`.</span></span> <span data-ttu-id="3f577-109">Si un script crée une tâche à exécuter par la suite, le rappel de continuation à la suite sera appelé par la tâche et la tâche doit être placée dans une file d’attente FIFO pour être exécutée à la fin de l’exécution du script actuel.</span><span class="sxs-lookup"><span data-stu-id="3f577-109">If a script creates a task to be run later, then the promise continuation callback will be called with the task and the task should be put in a FIFO queue, to be run when the current script is done executing.</span></span>  
  
 <span data-ttu-id="3f577-110">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="3f577-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="3f577-111">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="3f577-111">Requirements</span></span>  
 <span data-ttu-id="3f577-112">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3f577-112">jsrt.h</span></span>  
  
## <span data-ttu-id="3f577-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f577-113">See Also</span></span>  
 [<span data-ttu-id="3f577-114">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3f577-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
