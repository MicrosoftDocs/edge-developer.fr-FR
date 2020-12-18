---
description: Référence pour le domaine DOMDebugger. Le débogage DOM permet de définir des points d’arrêt sur des événements et des événements DOM spécifiques. L’exécution JavaScript s’arrêtera sur ces opérations comme s’il s’agissait d’un jeu de points d’arrêt régulier.
title: DOMDebugger Domain-DevTools Protocol version 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d97a9a8f2d0e49166f5f081e8bb0c0d5d3cdd93f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232860"
---
# <span data-ttu-id="069b1-105">DOMDebugger</span><span class="sxs-lookup"><span data-stu-id="069b1-105">DOMDebugger</span></span>

<span data-ttu-id="069b1-106">Le débogage DOM permet de définir des points d’arrêt sur des événements et des événements DOM spécifiques.</span><span class="sxs-lookup"><span data-stu-id="069b1-106">DOM debugging allows setting breakpoints on particular DOM operations and events.</span></span> <span data-ttu-id="069b1-107">L’exécution JavaScript s’arrêtera sur ces opérations comme s’il s’agissait d’un jeu de points d’arrêt régulier.</span><span class="sxs-lookup"><span data-stu-id="069b1-107">JavaScript execution will stop on these operations as if there was a regular breakpoint set.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="069b1-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="069b1-108">Methods</span></span>**](#methods) | <span data-ttu-id="069b1-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span><span class="sxs-lookup"><span data-stu-id="069b1-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span></span> |
## <span data-ttu-id="069b1-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="069b1-110">Methods</span></span>

### <span data-ttu-id="069b1-111">setInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="069b1-111">setInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="069b1-112">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="069b1-112">Experimental.</span></span> </b></span><span data-ttu-id="069b1-113">Définit un point d’arrêt sur un événement natif particulier.</span><span class="sxs-lookup"><span data-stu-id="069b1-113">Sets a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="069b1-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="069b1-114">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="069b1-115">Protégée</span><span class="sxs-lookup"><span data-stu-id="069b1-115">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="069b1-116">Nom d’instrumentation pour l’arrêter.</span><span class="sxs-lookup"><span data-stu-id="069b1-116">Instrumentation name to stop on.</span></span> <span data-ttu-id="069b1-117">Valeurs valides: 'scriptFirstStatement'.</span><span class="sxs-lookup"><span data-stu-id="069b1-117">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="069b1-118">removeInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="069b1-118">removeInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="069b1-119">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="069b1-119">Experimental.</span></span> </b></span><span data-ttu-id="069b1-120">Supprime un point d’arrêt sur un événement natif particulier.</span><span class="sxs-lookup"><span data-stu-id="069b1-120">Removes a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="069b1-121">Parameters</span><span class="sxs-lookup"><span data-stu-id="069b1-121">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="069b1-122">Protégée</span><span class="sxs-lookup"><span data-stu-id="069b1-122">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="069b1-123">Nom d’instrumentation pour l’arrêter.</span><span class="sxs-lookup"><span data-stu-id="069b1-123">Instrumentation name to stop on.</span></span> <span data-ttu-id="069b1-124">Valeurs valides: 'scriptFirstStatement'.</span><span class="sxs-lookup"><span data-stu-id="069b1-124">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
