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
# DOMDebugger

Le débogage DOM permet de définir des points d’arrêt sur des événements et des événements DOM spécifiques. L’exécution JavaScript s’arrêtera sur ces opérations comme s’il s’agissait d’un jeu de points d’arrêt régulier.

| | |
|-|-|
| [**Méthodes**](#methods) | [setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint) |
## Méthodes

### setInstrumentationBreakpoint
<span><b>Pratiqué. </b></span>Définit un point d’arrêt sur un événement natif particulier.

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
            <td>Protégée</td>
            <td><code class="flyout">string</code></td>
            <td>Nom d’instrumentation pour l’arrêter. Valeurs valides: 'scriptFirstStatement'.</td>
        </tr>
    </tbody>
</table>
</p>

---

### removeInstrumentationBreakpoint
<span><b>Pratiqué. </b></span>Supprime un point d’arrêt sur un événement natif particulier.

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
            <td>Protégée</td>
            <td><code class="flyout">string</code></td>
            <td>Nom d’instrumentation pour l’arrêter. Valeurs valides: 'scriptFirstStatement'.</td>
        </tr>
    </tbody>
</table>
</p>

---
