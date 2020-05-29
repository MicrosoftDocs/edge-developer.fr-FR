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
# Superposition
Le domaine superposé expose des ornements visuels et une interaction de sélection de nœud

| | |
|-|-|
| [**Méthodes**](#methods) | [activer](#enable), [Désactiver](#disable) [setInspectMode](#setinspectmode) |
| [**Événements**](#events) | [inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested) |
| [**Dépendances**](#dependencies) | [DOM](dom.md) |
## Méthodes

### activer
Active la création de rapports <code>nodeHighlightRequested</code> et des <code>inspectElementRequested</code> événements

</p>

---

### désactiver 
Désactive la création de rapports sur les événements de domaine Overlay

</p>

---

### setInspectMode
Définit le mode de sélection des éléments pour le client.

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>mode</td>
            <td><code class="flyout">string</code></td>
            <td>Le mode inspection.  Les valeurs valides sont «searchForNode» et «None».</td>
        </tr>
        <tr>
            <td>highlightConfig <br/> <i>facultatif</i></td>
            <td><a href="dom.md#highlightconfig"><code class="flyout">DOM.HighlightConfig</code></a></td>
            <td>Configuration de surbrillance à utiliser lors de l’inspection</td>
        </tr>
    </tbody>
</table>
</p>

---

## Événements

### inspectNodeRequested
Informe le client que l’utilisateur a demandé à inspecter un nœud particulier.

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>backendNodeId</td>
            <td><a href="dom.md#backendnodeid"><code class="flyout">DOM.BackendNodeId</code></a></td>
            <td>ID du nœud principal du nœud demandé.</td>
        </tr>
    </tbody>
</table>
</p>

---

### nodeHighlightRequested
Indique que l’utilisateur a pointé sur le nœud et peut vérifier le nœud

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ID</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td>ID de nœud du nœud qui est considéré comme étant</td>
        </tr>
    </tbody>
</table>
</p>

---

## Dépendances

[DOM](dom.md)