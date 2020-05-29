---
description: Référence pour le domaine superposé. Le domaine superposé expose des ornements visuels et une interaction de sélection de nœud
title: Overlay Domain-DevTools Protocol version 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: a7657e2abc99e45894f19f6557f12f78f8ee9c75
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565465"
---
# <span data-ttu-id="cd65a-104">Superposition</span><span class="sxs-lookup"><span data-stu-id="cd65a-104">Overlay</span></span>
<span data-ttu-id="cd65a-105">Le domaine superposé expose des ornements visuels et une interaction de sélection de nœud</span><span class="sxs-lookup"><span data-stu-id="cd65a-105">Overlay domain exposes visual adornments and node selection interaction</span></span>

| | |
|-|-|
| [**<span data-ttu-id="cd65a-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cd65a-106">Methods</span></span>**](#methods) | <span data-ttu-id="cd65a-107">[activer](#enable), [Désactiver](#disable) [setInspectMode](#setinspectmode)</span><span class="sxs-lookup"><span data-stu-id="cd65a-107">[enable](#enable), [disable](#disable), [setInspectMode](#setinspectmode)</span></span> |
| [**<span data-ttu-id="cd65a-108">Événements</span><span class="sxs-lookup"><span data-stu-id="cd65a-108">Events</span></span>**](#events) | <span data-ttu-id="cd65a-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span><span class="sxs-lookup"><span data-stu-id="cd65a-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span></span> |
| [**<span data-ttu-id="cd65a-110">Dépendances</span><span class="sxs-lookup"><span data-stu-id="cd65a-110">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="cd65a-111">DOM</span><span class="sxs-lookup"><span data-stu-id="cd65a-111">DOM</span></span>](dom.md) |
## <span data-ttu-id="cd65a-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cd65a-112">Methods</span></span>

### <span data-ttu-id="cd65a-113">activer</span><span class="sxs-lookup"><span data-stu-id="cd65a-113">enable</span></span>
<span data-ttu-id="cd65a-114">Active la création de rapports <code>nodeHighlightRequested</code> et des <code>inspectElementRequested</code> événements</span><span class="sxs-lookup"><span data-stu-id="cd65a-114">Enables reporting of <code>nodeHighlightRequested</code> and <code>inspectElementRequested</code> events</span></span>

</p>

---

### <span data-ttu-id="cd65a-115">désactiver </span><span class="sxs-lookup"><span data-stu-id="cd65a-115">disable</span></span>
<span data-ttu-id="cd65a-116">Désactive la création de rapports sur les événements de domaine Overlay</span><span class="sxs-lookup"><span data-stu-id="cd65a-116">Disables reporting of Overlay domain events</span></span>

</p>

---

### <span data-ttu-id="cd65a-117">setInspectMode</span><span class="sxs-lookup"><span data-stu-id="cd65a-117">setInspectMode</span></span>
<span data-ttu-id="cd65a-118">Définit le mode de sélection des éléments pour le client.</span><span class="sxs-lookup"><span data-stu-id="cd65a-118">Sets the element selection mode for the client</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="cd65a-119">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd65a-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="cd65a-120">mode</span><span class="sxs-lookup"><span data-stu-id="cd65a-120">mode</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="cd65a-121">Le mode inspection.</span><span class="sxs-lookup"><span data-stu-id="cd65a-121">The inspection mode.</span></span>  <span data-ttu-id="cd65a-122">Les valeurs valides sont «searchForNode» et «None».</span><span class="sxs-lookup"><span data-stu-id="cd65a-122">Valid values are 'searchForNode' and 'none'.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="cd65a-123">highlightConfig</span><span class="sxs-lookup"><span data-stu-id="cd65a-123">highlightConfig</span></span> <br/> <i><span data-ttu-id="cd65a-124">facultatif</span><span class="sxs-lookup"><span data-stu-id="cd65a-124">optional</span></span></i></td>
            <td><a href="dom.md#highlightconfig"><code class="flyout">DOM.HighlightConfig</code></a></td>
            <td><span data-ttu-id="cd65a-125">Configuration de surbrillance à utiliser lors de l’inspection</span><span class="sxs-lookup"><span data-stu-id="cd65a-125">The highlight configuration to use while inspecting</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="cd65a-126">Événements</span><span class="sxs-lookup"><span data-stu-id="cd65a-126">Events</span></span>

### <span data-ttu-id="cd65a-127">inspectNodeRequested</span><span class="sxs-lookup"><span data-stu-id="cd65a-127">inspectNodeRequested</span></span>
<span data-ttu-id="cd65a-128">Informe le client que l’utilisateur a demandé à inspecter un nœud particulier.</span><span class="sxs-lookup"><span data-stu-id="cd65a-128">Notifies the client that the user has asked to inspect a particular node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="cd65a-129">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd65a-129">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="cd65a-130">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="cd65a-130">backendNodeId</span></span></td>
            <td><a href="dom.md#backendnodeid"><code class="flyout">DOM.BackendNodeId</code></a></td>
            <td><span data-ttu-id="cd65a-131">ID du nœud principal du nœud demandé.</span><span class="sxs-lookup"><span data-stu-id="cd65a-131">The backend node ID of node requested</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="cd65a-132">nodeHighlightRequested</span><span class="sxs-lookup"><span data-stu-id="cd65a-132">nodeHighlightRequested</span></span>
<span data-ttu-id="cd65a-133">Indique que l’utilisateur a pointé sur le nœud et peut vérifier le nœud</span><span class="sxs-lookup"><span data-stu-id="cd65a-133">Indicates that the user has hovered over the node and may inspect the node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="cd65a-134">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd65a-134">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="cd65a-135">ID</span><span class="sxs-lookup"><span data-stu-id="cd65a-135">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td><span data-ttu-id="cd65a-136">ID de nœud du nœud qui est considéré comme étant</span><span class="sxs-lookup"><span data-stu-id="cd65a-136">The node ID of the node being considered</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="cd65a-137">Dépendances</span><span class="sxs-lookup"><span data-stu-id="cd65a-137">Dependencies</span></span>

[<span data-ttu-id="cd65a-138">DOM</span><span class="sxs-lookup"><span data-stu-id="cd65a-138">DOM</span></span>](dom.md)