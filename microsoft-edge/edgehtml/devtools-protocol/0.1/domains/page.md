---
description: Référence du 0,1 Protocole DevTools (EdgeHTML) pour le domaine de la page. Les actions et événements liés à la page inspectée appartiennent au domaine de la page.
title: Page Domain-DevTools Protocol version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55575e54b9125d7ff544c23c81da4b15d3b56fb1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233249"
---
# Page Domain-DevTools Protocol version 0,1 (EdgeHTML)  

Les actions et événements liés à la page inspectée appartiennent au domaine de la page.

| | |
|-|-|
| [**Méthodes**](#methods) | [activer](#enable), [Désactiver](#disable), [naviguer](#navigate) |
| [**Types**](#types) | [FrameId](#frameid) |
## Méthodes

### activer
Active les notifications de domaine de page.


---

### désactiver 
Désactive les notifications de domaine de la page.


---

### naviguer
Accède à la page active à l’URL donnée.

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
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>URL permettant d’accéder à la page.</td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Renvoie</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>frameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span><b>Pratiqué. </b></span>ID de cadre qui sera parcouru.</td>
        </tr>
    </tbody>
</table>

---

## Types

### <a name="frameid"></a> FrameId `string`

Identificateur de cadre unique.


---
