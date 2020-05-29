---
description: Référence pour le domaine DOMDebugger. Le débogage DOM permet de définir des points d’arrêt sur des événements et des événements DOM spécifiques. L’exécution JavaScript s’arrêtera sur ces opérations comme s’il s’agissait d’un jeu de points d’arrêt régulier.
title: DOMDebugger Domain-DevTools Protocol version 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 437a88ff93bda36d85a8f5632c1a02aa205d049b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565466"
---
# <span data-ttu-id="33807-105">DOMDebugger</span><span class="sxs-lookup"><span data-stu-id="33807-105">DOMDebugger</span></span>
<span data-ttu-id="33807-106">Le débogage DOM permet de définir des points d’arrêt sur des événements et des événements DOM spécifiques.</span><span class="sxs-lookup"><span data-stu-id="33807-106">DOM debugging allows setting breakpoints on particular DOM operations and events.</span></span> <span data-ttu-id="33807-107">L’exécution JavaScript s’arrêtera sur ces opérations comme s’il s’agissait d’un jeu de points d’arrêt régulier.</span><span class="sxs-lookup"><span data-stu-id="33807-107">JavaScript execution will stop on these operations as if there was a regular breakpoint set.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="33807-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="33807-108">Methods</span></span>**](#methods) | <span data-ttu-id="33807-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span><span class="sxs-lookup"><span data-stu-id="33807-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span></span> |
## <span data-ttu-id="33807-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="33807-110">Methods</span></span>

### <span data-ttu-id="33807-111">setInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="33807-111">setInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="33807-112">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="33807-112">Experimental.</span></span> </b></span><span data-ttu-id="33807-113">Définit un point d’arrêt sur un événement natif particulier.</span><span class="sxs-lookup"><span data-stu-id="33807-113">Sets a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="33807-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="33807-114">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="33807-115">Protégée</span><span class="sxs-lookup"><span data-stu-id="33807-115">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="33807-116">Nom d’instrumentation pour l’arrêter.</span><span class="sxs-lookup"><span data-stu-id="33807-116">Instrumentation name to stop on.</span></span> <span data-ttu-id="33807-117">Valeurs valides: 'scriptFirstStatement'.</span><span class="sxs-lookup"><span data-stu-id="33807-117">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="33807-118">removeInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="33807-118">removeInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="33807-119">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="33807-119">Experimental.</span></span> </b></span><span data-ttu-id="33807-120">Supprime un point d’arrêt sur un événement natif particulier.</span><span class="sxs-lookup"><span data-stu-id="33807-120">Removes a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="33807-121">Parameters</span><span class="sxs-lookup"><span data-stu-id="33807-121">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="33807-122">Protégée</span><span class="sxs-lookup"><span data-stu-id="33807-122">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="33807-123">Nom d’instrumentation pour l’arrêter.</span><span class="sxs-lookup"><span data-stu-id="33807-123">Instrumentation name to stop on.</span></span> <span data-ttu-id="33807-124">Valeurs valides: 'scriptFirstStatement'.</span><span class="sxs-lookup"><span data-stu-id="33807-124">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
