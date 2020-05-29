---
description: Définit la limite de mémoire actuelle pour un Runtime.
title: Fonction JsSetRuntimeMemoryLimit | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryLimit
helpviewer_keywords:
- JsSetRuntimeMemoryLimit function
ms.assetid: 74feb31f-19f6-43e3-b117-0694c59ac593
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ec8d098c528ac813926797280541aa2c9c4fee79
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566140"
---
# <span data-ttu-id="aff7c-103">Fonction JsSetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="aff7c-103">JsSetRuntimeMemoryLimit Function</span></span>
<span data-ttu-id="aff7c-104">Définit la limite de mémoire actuelle pour un Runtime.</span><span class="sxs-lookup"><span data-stu-id="aff7c-104">Sets the current memory limit for a runtime.</span></span>  
  
## <span data-ttu-id="aff7c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aff7c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _In_ size_t memoryLimit  
);  
```  
  
#### <span data-ttu-id="aff7c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aff7c-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="aff7c-107">Le runtime dont la limite de mémoire doit être définie.</span><span class="sxs-lookup"><span data-stu-id="aff7c-107">The runtime whose memory limit is to be set.</span></span>  
  
 `memoryLimit`  
 <span data-ttu-id="aff7c-108">La nouvelle limite de mémoire d’exécution, en octets ou-1 pour aucune limite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="aff7c-108">The new runtime memory limit, in bytes, or -1 for no memory limit.</span></span>  
  
## <span data-ttu-id="aff7c-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="aff7c-109">Return Value</span></span>  
 <span data-ttu-id="aff7c-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="aff7c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="aff7c-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="aff7c-111">Remarks</span></span>  
 <span data-ttu-id="aff7c-112">Une limite de mémoire entraîne une opération qui dépasse la limite pour l’échec de l’exécution d’une erreur «mémoire insuffisante».</span><span class="sxs-lookup"><span data-stu-id="aff7c-112">A memory limit will cause any operation which exceeds the limit to fail with an "out of memory" error.</span></span> <span data-ttu-id="aff7c-113">La définition de la limite de mémoire d’un Runtime sur-1 signifie que le runtime n’a pas de limite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="aff7c-113">Setting a runtime's memory limit to -1 means that the runtime has no memory limit.</span></span> <span data-ttu-id="aff7c-114">Par défaut, les nouveaux Runtime ne possèdent aucune limite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="aff7c-114">New runtimes default to having no memory limit.</span></span> <span data-ttu-id="aff7c-115">Si la nouvelle limite de mémoire est supérieure à l’utilisation actuelle, l’appel aboutit et toutes les attributions ultérieures dans ce Runtime échouent jusqu’à ce que l’utilisation de la mémoire du runtime reste en dessous de la limite.</span><span class="sxs-lookup"><span data-stu-id="aff7c-115">If the new memory limit exceeds current usage, the call will succeed and any future allocations in this runtime will fail until the runtime's memory usage drops below the limit.</span></span>  
  
 <span data-ttu-id="aff7c-116">Il est toujours possible de définir la limite de mémoire d’un Runtime, que le runtime soit actif ou non sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="aff7c-116">A runtime's memory limit can be always be set, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="aff7c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aff7c-117">Requirements</span></span>  
 <span data-ttu-id="aff7c-118">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="aff7c-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="aff7c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aff7c-119">See Also</span></span>  
 [<span data-ttu-id="aff7c-120">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="aff7c-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)