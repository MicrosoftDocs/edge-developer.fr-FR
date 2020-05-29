---
description: Indique au runtime d’effectuer tout traitement inactif qu’il doit effectuer.
title: Fonction JsIdle | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIdle
helpviewer_keywords:
- JsIdle function
ms.assetid: 372d1c62-8e19-4886-aa33-364cabc09bba
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4da7148bf7daa3db983ab8f5bba622bfe0b19466
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566291"
---
# <span data-ttu-id="7f5ce-103">Fonction JsIdle</span><span class="sxs-lookup"><span data-stu-id="7f5ce-103">JsIdle Function</span></span>
<span data-ttu-id="7f5ce-104">Indique au runtime d’effectuer tout traitement inactif qu’il doit effectuer.</span><span class="sxs-lookup"><span data-stu-id="7f5ce-104">Tells the runtime to do any idle processing it need to do.</span></span>  
  
## <span data-ttu-id="7f5ce-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f5ce-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIdle(  
   _Out_opt_ unsigned int *nextIdleTick  
);  
```  
  
#### <span data-ttu-id="7f5ce-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f5ce-106">Parameters</span></span>  
 `nextIdleTick`  
 <span data-ttu-id="7f5ce-107">La prochaine coche système lorsque le fonctionnement est plus inactif.</span><span class="sxs-lookup"><span data-stu-id="7f5ce-107">The next system tick when there will be more idle work to do.</span></span> <span data-ttu-id="7f5ce-108">Peut être null.</span><span class="sxs-lookup"><span data-stu-id="7f5ce-108">Can be null.</span></span> <span data-ttu-id="7f5ce-109">Renvoie le nombre maximal de graduations s’il n’y a pas de tâches à venir.</span><span class="sxs-lookup"><span data-stu-id="7f5ce-109">Returns the maximum number of ticks if there no upcoming idle work to do.</span></span>  
  
## <span data-ttu-id="7f5ce-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7f5ce-110">Return Value</span></span>  
 <span data-ttu-id="7f5ce-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7f5ce-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7f5ce-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="7f5ce-112">Remarks</span></span>  
 <span data-ttu-id="7f5ce-113">Si le traitement inactif a été activé pour le runtime actuel, l’appel `JsIdle` informera le runtime actuel qu’il est inactif et que le runtime peut effectuer des tâches de nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="7f5ce-113">If idle processing has been enabled for the current runtime, calling `JsIdle` will inform the current runtime that the host is idle and that the runtime can perform memory cleanup tasks.</span></span>  
  
 `JsIdle` <span data-ttu-id="7f5ce-114">peut également renvoyer le nombre de battements système jusqu’à ce que le runtime puisse y exécuter plus de tâches.</span><span class="sxs-lookup"><span data-stu-id="7f5ce-114">can also return the number of system ticks until there will be more idle work for the runtime to do.</span></span> <span data-ttu-id="7f5ce-115">Les appels `JsIdle` antérieurs à ce nombre de coches ne fonctionneront pas.</span><span class="sxs-lookup"><span data-stu-id="7f5ce-115">Calling `JsIdle` before this number of ticks has passed will do no work.</span></span>  
  
 <span data-ttu-id="7f5ce-116">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="7f5ce-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="7f5ce-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f5ce-117">Requirements</span></span>  
 <span data-ttu-id="7f5ce-118">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7f5ce-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7f5ce-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f5ce-119">See Also</span></span>  
 [<span data-ttu-id="7f5ce-120">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7f5ce-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)