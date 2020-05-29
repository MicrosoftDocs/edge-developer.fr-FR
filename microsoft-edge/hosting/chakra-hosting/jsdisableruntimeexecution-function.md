---
description: Interrompt l’exécution du script et arrête tout script en cours d’exécution dans le Runtime.
title: Fonction JsDisableRuntimeExecution | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDisableRuntimeExecution
helpviewer_keywords:
- JsDisableRuntimeExecution function
ms.assetid: 4bd4670a-a9da-4f8c-b3fd-1fd366d915c3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 575947d3038eaa136e9d6ae62507501bc768eabe
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565205"
---
# <span data-ttu-id="85e48-103">Fonction JsDisableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="85e48-103">JsDisableRuntimeExecution Function</span></span>
<span data-ttu-id="85e48-104">Interrompt l’exécution du script et arrête tout script en cours d’exécution dans le Runtime.</span><span class="sxs-lookup"><span data-stu-id="85e48-104">Suspends script execution and terminates any running scripts in a runtime.</span></span>  
  
## <span data-ttu-id="85e48-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85e48-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDisableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="85e48-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85e48-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="85e48-107">Exécution du Runtime.</span><span class="sxs-lookup"><span data-stu-id="85e48-107">The runtime to be suspended.</span></span>  
  
## <span data-ttu-id="85e48-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="85e48-108">Return Value</span></span>  
 <span data-ttu-id="85e48-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="85e48-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="85e48-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="85e48-110">Remarks</span></span>  
 <span data-ttu-id="85e48-111">Les appels vers un Runtime suspendu échouent jusqu’à ce qu' `JsEnableRuntimeExecution` il soit appelé.</span><span class="sxs-lookup"><span data-stu-id="85e48-111">Calls to a suspended runtime will fail until `JsEnableRuntimeExecution` is called.</span></span>  
  
 <span data-ttu-id="85e48-112">Il n’est pas nécessaire d’appeler cette API sur le thread sur lequel le runtime est actif.</span><span class="sxs-lookup"><span data-stu-id="85e48-112">This API does not have to be called on the thread the runtime is active on.</span></span> <span data-ttu-id="85e48-113">Même si le runtime est défini comme étant suspendu, un script d’exécution ne peut pas être suspendu immédiatement. le script actif sera arrêté en utilisant une exception dès que possible.</span><span class="sxs-lookup"><span data-stu-id="85e48-113">Although the runtime will be set into a suspended state, an executing script may not be suspended immediately; a running script will be terminated with an uncatchable exception as soon as possible.</span></span>  
  
 <span data-ttu-id="85e48-114">Le fait de suspendre l’exécution dans un Runtime qui est déjà suspendu est un absence d’opération.</span><span class="sxs-lookup"><span data-stu-id="85e48-114">Suspending execution in a runtime that is already suspended is a no-op.</span></span>  
  
## <span data-ttu-id="85e48-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85e48-115">Requirements</span></span>  
 <span data-ttu-id="85e48-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="85e48-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="85e48-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85e48-117">See Also</span></span>  
 [<span data-ttu-id="85e48-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="85e48-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)