---
description: Référence pour le domaine de schéma. Fournit des informations sur le schéma de protocole.
title: Domain Schema-DevTools Protocol version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a2f679f6f4bf8e82dc7298d96f798507b1338062
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882925"
---
# Domain Schema-DevTools Protocol version 0,1 (EdgeHTML)  

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

---
