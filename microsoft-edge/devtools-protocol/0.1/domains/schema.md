---
description: Référence pour le domaine de schéma. Fournit des informations sur le schéma de protocole.
title: Domain Schema-DevTools Protocol version 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 83d7019d18ccce1c81b67aafdcafe1a8566694ea
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565485"
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
