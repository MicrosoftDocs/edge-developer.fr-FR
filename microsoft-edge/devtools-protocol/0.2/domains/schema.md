---
description: Référence pour le domaine de schéma. Fournit des informations sur le schéma de protocole.
title: Domain Schema-DevTools Protocol version 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: df86e6669956c14b7c905514fc44376f71eaa993
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565460"
---
# Schéma
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
