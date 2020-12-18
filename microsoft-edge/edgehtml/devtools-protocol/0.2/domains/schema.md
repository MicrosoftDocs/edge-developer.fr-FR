---
description: Référence de la version 0,2 (EdgeHTML) du protocole DevTools pour le domaine de schéma. Fournit des informations sur le schéma de protocole.
title: Domain Schema-DevTools Protocol version 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/16/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 53038a02844fafc9550a6ac26303620a1a0183f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232854"
---
# Domain Schema-DevTools Protocol version 0,2 (EdgeHTML)  

Fournit des informations sur le schéma de protocole.

| | |
|-|-|
| [**Méthodes**](#methods) | [getDomains](#getdomains) |
| [**Types**](#types) | [Domaine](#domain) |
## Méthodes

### getDomains
Renvoie les domaines pris en charge.

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
            <td>ils</td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td>Liste des domaines pris en charge.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Types

### <a name="domain"></a> Domaine `object`

Description du domaine du protocole.

<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nom de domaine.</td>
        </tr>
        <tr>
            <td>version</td>
            <td><code class="flyout">string</code></td>
            <td>Version du domaine.</td>
        </tr>
    </tbody>
</table>
</p>

---
