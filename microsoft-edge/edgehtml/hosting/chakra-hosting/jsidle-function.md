---
description: Indique au runtime d’effectuer tout traitement inactif qu’il doit effectuer.
title: Fonction JsIdle | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIdle
helpviewer_keywords:
- JsIdle function
ms.assetid: 372d1c62-8e19-4886-aa33-364cabc09bba
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ecba0aafb6b4dcccb4485c2956cae5ce4045355f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233487"
---
# <span data-ttu-id="0aa42-103">JsIdle Function</span><span class="sxs-lookup"><span data-stu-id="0aa42-103">JsIdle Function</span></span>

<span data-ttu-id="0aa42-104">Indique au runtime d’effectuer tout traitement inactif qu’il doit effectuer.</span><span class="sxs-lookup"><span data-stu-id="0aa42-104">Tells the runtime to do any idle processing it need to do.</span></span>  
  
## <span data-ttu-id="0aa42-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0aa42-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIdle(  
   _Out_opt_ unsigned int *nextIdleTick  
);  
```  
  
#### <span data-ttu-id="0aa42-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0aa42-106">Parameters</span></span>  
 `nextIdleTick`  
 <span data-ttu-id="0aa42-107">La prochaine coche système lorsque le fonctionnement est plus inactif.</span><span class="sxs-lookup"><span data-stu-id="0aa42-107">The next system tick when there will be more idle work to do.</span></span> <span data-ttu-id="0aa42-108">Peut être null.</span><span class="sxs-lookup"><span data-stu-id="0aa42-108">Can be null.</span></span> <span data-ttu-id="0aa42-109">Renvoie le nombre maximal de graduations s’il n’y a pas de tâches à venir.</span><span class="sxs-lookup"><span data-stu-id="0aa42-109">Returns the maximum number of ticks if there no upcoming idle work to do.</span></span>  
  
## <span data-ttu-id="0aa42-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0aa42-110">Return Value</span></span>  
 <span data-ttu-id="0aa42-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0aa42-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0aa42-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="0aa42-112">Remarks</span></span>  
 <span data-ttu-id="0aa42-113">Si le traitement inactif a été activé pour le runtime actuel, l’appel `JsIdle` informera le runtime actuel qu’il est inactif et que le runtime peut effectuer des tâches de nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="0aa42-113">If idle processing has been enabled for the current runtime, calling `JsIdle` will inform the current runtime that the host is idle and that the runtime can perform memory cleanup tasks.</span></span>  
  
 `JsIdle` <span data-ttu-id="0aa42-114">peut également renvoyer le nombre de battements système jusqu’à ce que le runtime puisse y exécuter plus de tâches.</span><span class="sxs-lookup"><span data-stu-id="0aa42-114">can also return the number of system ticks until there will be more idle work for the runtime to do.</span></span> <span data-ttu-id="0aa42-115">Les appels `JsIdle` antérieurs à ce nombre de coches ne fonctionneront pas.</span><span class="sxs-lookup"><span data-stu-id="0aa42-115">Calling `JsIdle` before this number of ticks has passed will do no work.</span></span>  
  
 <span data-ttu-id="0aa42-116">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="0aa42-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0aa42-117">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="0aa42-117">Requirements</span></span>  
 <span data-ttu-id="0aa42-118">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0aa42-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0aa42-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0aa42-119">See Also</span></span>  
 [<span data-ttu-id="0aa42-120">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0aa42-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
