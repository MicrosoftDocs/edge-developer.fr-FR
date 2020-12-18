---
description: Référence pour le domaine superposé. Le domaine superposé expose des ornements visuels et une interaction de sélection de nœud
title: Overlay Domain-DevTools Protocol version 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: dcf5feff9983aa2e9e61ac0569938988812165f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232858"
---
# <span data-ttu-id="4638b-104">Overlay</span><span class="sxs-lookup"><span data-stu-id="4638b-104">Overlay</span></span>

<span data-ttu-id="4638b-105">Le domaine superposé expose des ornements visuels et une interaction de sélection de nœud</span><span class="sxs-lookup"><span data-stu-id="4638b-105">Overlay domain exposes visual adornments and node selection interaction</span></span>

| | |
|-|-|
| [**<span data-ttu-id="4638b-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4638b-106">Methods</span></span>**](#methods) | <span data-ttu-id="4638b-107">[activer](#enable), [Désactiver](#disable) [setInspectMode](#setinspectmode)</span><span class="sxs-lookup"><span data-stu-id="4638b-107">[enable](#enable), [disable](#disable), [setInspectMode](#setinspectmode)</span></span> |
| [**<span data-ttu-id="4638b-108">Événements</span><span class="sxs-lookup"><span data-stu-id="4638b-108">Events</span></span>**](#events) | <span data-ttu-id="4638b-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span><span class="sxs-lookup"><span data-stu-id="4638b-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span></span> |
| [**<span data-ttu-id="4638b-110">Dépendances</span><span class="sxs-lookup"><span data-stu-id="4638b-110">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="4638b-111">DOM</span><span class="sxs-lookup"><span data-stu-id="4638b-111">DOM</span></span>](dom.md) |
## <span data-ttu-id="4638b-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4638b-112">Methods</span></span>

### <span data-ttu-id="4638b-113">activer</span><span class="sxs-lookup"><span data-stu-id="4638b-113">enable</span></span>
<span data-ttu-id="4638b-114">Active la création de rapports <code>nodeHighlightRequested</code> et des <code>inspectElementRequested</code> événements</span><span class="sxs-lookup"><span data-stu-id="4638b-114">Enables reporting of <code>nodeHighlightRequested</code> and <code>inspectElementRequested</code> events</span></span>

</p>

---

### <span data-ttu-id="4638b-115">désactiver </span><span class="sxs-lookup"><span data-stu-id="4638b-115">disable</span></span>
<span data-ttu-id="4638b-116">Désactive la création de rapports sur les événements de domaine Overlay</span><span class="sxs-lookup"><span data-stu-id="4638b-116">Disables reporting of Overlay domain events</span></span>

</p>

---

### <span data-ttu-id="4638b-117">setInspectMode</span><span class="sxs-lookup"><span data-stu-id="4638b-117">setInspectMode</span></span>
<span data-ttu-id="4638b-118">Définit le mode de sélection des éléments pour le client.</span><span class="sxs-lookup"><span data-stu-id="4638b-118">Sets the element selection mode for the client</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4638b-119">Parameters</span><span class="sxs-lookup"><span data-stu-id="4638b-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4638b-120">mode</span><span class="sxs-lookup"><span data-stu-id="4638b-120">mode</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="4638b-121">Le mode inspection.</span><span class="sxs-lookup"><span data-stu-id="4638b-121">The inspection mode.</span></span>  <span data-ttu-id="4638b-122">Les valeurs valides sont «searchForNode» et «None».</span><span class="sxs-lookup"><span data-stu-id="4638b-122">Valid values are 'searchForNode' and 'none'.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4638b-123">highlightConfig</span><span class="sxs-lookup"><span data-stu-id="4638b-123">highlightConfig</span></span> <br/> <i><span data-ttu-id="4638b-124">facultatif</span><span class="sxs-lookup"><span data-stu-id="4638b-124">optional</span></span></i></td>
            <td><a href="dom.md#highlightconfig"><code class="flyout">DOM.HighlightConfig</code></a></td>
            <td><span data-ttu-id="4638b-125">Configuration de surbrillance à utiliser lors de l’inspection</span><span class="sxs-lookup"><span data-stu-id="4638b-125">The highlight configuration to use while inspecting</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="4638b-126">Événements</span><span class="sxs-lookup"><span data-stu-id="4638b-126">Events</span></span>

### <span data-ttu-id="4638b-127">inspectNodeRequested</span><span class="sxs-lookup"><span data-stu-id="4638b-127">inspectNodeRequested</span></span>
<span data-ttu-id="4638b-128">Informe le client que l’utilisateur a demandé à inspecter un nœud particulier.</span><span class="sxs-lookup"><span data-stu-id="4638b-128">Notifies the client that the user has asked to inspect a particular node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4638b-129">Parameters</span><span class="sxs-lookup"><span data-stu-id="4638b-129">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4638b-130">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="4638b-130">backendNodeId</span></span></td>
            <td><a href="dom.md#backendnodeid"><code class="flyout">DOM.BackendNodeId</code></a></td>
            <td><span data-ttu-id="4638b-131">ID du nœud principal du nœud demandé.</span><span class="sxs-lookup"><span data-stu-id="4638b-131">The backend node ID of node requested</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="4638b-132">nodeHighlightRequested</span><span class="sxs-lookup"><span data-stu-id="4638b-132">nodeHighlightRequested</span></span>
<span data-ttu-id="4638b-133">Indique que l’utilisateur a pointé sur le nœud et peut vérifier le nœud</span><span class="sxs-lookup"><span data-stu-id="4638b-133">Indicates that the user has hovered over the node and may inspect the node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4638b-134">Parameters</span><span class="sxs-lookup"><span data-stu-id="4638b-134">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4638b-135">ID</span><span class="sxs-lookup"><span data-stu-id="4638b-135">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td><span data-ttu-id="4638b-136">ID de nœud du nœud qui est considéré comme étant</span><span class="sxs-lookup"><span data-stu-id="4638b-136">The node ID of the node being considered</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="4638b-137">Dépendances</span><span class="sxs-lookup"><span data-stu-id="4638b-137">Dependencies</span></span>

[<span data-ttu-id="4638b-138">DOM</span><span class="sxs-lookup"><span data-stu-id="4638b-138">DOM</span></span>](dom.md)
