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
