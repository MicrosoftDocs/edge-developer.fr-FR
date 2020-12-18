---
description: Interrompt l’exécution du script et arrête tout script en cours d’exécution dans le Runtime.
title: Fonction JsDisableRuntimeExecution | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisableRuntimeExecution
helpviewer_keywords:
- JsDisableRuntimeExecution function
ms.assetid: 4bd4670a-a9da-4f8c-b3fd-1fd366d915c3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6a08e6a7f89c724f8cf1a73afd97d2cb23c0334e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233177"
---
# <span data-ttu-id="d6cf0-103">JsDisableRuntimeExecution Function</span><span class="sxs-lookup"><span data-stu-id="d6cf0-103">JsDisableRuntimeExecution Function</span></span>

<span data-ttu-id="d6cf0-104">Interrompt l’exécution du script et arrête tout script en cours d’exécution dans le Runtime.</span><span class="sxs-lookup"><span data-stu-id="d6cf0-104">Suspends script execution and terminates any running scripts in a runtime.</span></span>  
  
## <span data-ttu-id="d6cf0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6cf0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDisableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="d6cf0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6cf0-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="d6cf0-107">Exécution du Runtime.</span><span class="sxs-lookup"><span data-stu-id="d6cf0-107">The runtime to be suspended.</span></span>  
  
## <span data-ttu-id="d6cf0-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d6cf0-108">Return Value</span></span>  
 <span data-ttu-id="d6cf0-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d6cf0-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d6cf0-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="d6cf0-110">Remarks</span></span>  
 <span data-ttu-id="d6cf0-111">Les appels vers un Runtime suspendu échouent jusqu’à ce qu' `JsEnableRuntimeExecution` il soit appelé.</span><span class="sxs-lookup"><span data-stu-id="d6cf0-111">Calls to a suspended runtime will fail until `JsEnableRuntimeExecution` is called.</span></span>  
  
 <span data-ttu-id="d6cf0-112">Il n’est pas nécessaire d’appeler cette API sur le thread sur lequel le runtime est actif.</span><span class="sxs-lookup"><span data-stu-id="d6cf0-112">This API does not have to be called on the thread the runtime is active on.</span></span> <span data-ttu-id="d6cf0-113">Même si le runtime est défini comme étant suspendu, un script d’exécution ne peut pas être suspendu immédiatement. le script actif sera arrêté en utilisant une exception dès que possible.</span><span class="sxs-lookup"><span data-stu-id="d6cf0-113">Although the runtime will be set into a suspended state, an executing script may not be suspended immediately; a running script will be terminated with an uncatchable exception as soon as possible.</span></span>  
  
 <span data-ttu-id="d6cf0-114">Le fait de suspendre l’exécution dans un Runtime qui est déjà suspendu est un absence d’opération.</span><span class="sxs-lookup"><span data-stu-id="d6cf0-114">Suspending execution in a runtime that is already suspended is a no-op.</span></span>  
  
## <span data-ttu-id="d6cf0-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="d6cf0-115">Requirements</span></span>  
 <span data-ttu-id="d6cf0-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d6cf0-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d6cf0-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6cf0-117">See Also</span></span>  
 [<span data-ttu-id="d6cf0-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d6cf0-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
