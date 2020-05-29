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
# <span data-ttu-id="e6c01-104">Schéma</span><span class="sxs-lookup"><span data-stu-id="e6c01-104">Schema</span></span>
<span data-ttu-id="e6c01-105">Fournit des informations sur le schéma de protocole.</span><span class="sxs-lookup"><span data-stu-id="e6c01-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="e6c01-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e6c01-106">Methods</span></span>**](#methods) | [<span data-ttu-id="e6c01-107">getDomains</span><span class="sxs-lookup"><span data-stu-id="e6c01-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="e6c01-108">Types</span><span class="sxs-lookup"><span data-stu-id="e6c01-108">Types</span></span>**](#types) | [<span data-ttu-id="e6c01-109">Domaine</span><span class="sxs-lookup"><span data-stu-id="e6c01-109">Domain</span></span>](#domain) |
## <span data-ttu-id="e6c01-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e6c01-110">Methods</span></span>

### <span data-ttu-id="e6c01-111">getDomains</span><span class="sxs-lookup"><span data-stu-id="e6c01-111">getDomains</span></span>
<span data-ttu-id="e6c01-112">Renvoie les domaines pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e6c01-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e6c01-113">Renvoie</span><span class="sxs-lookup"><span data-stu-id="e6c01-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e6c01-114">ils</span><span class="sxs-lookup"><span data-stu-id="e6c01-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="e6c01-115">Liste des domaines pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e6c01-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="e6c01-116">Types</span><span class="sxs-lookup"><span data-stu-id="e6c01-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="e6c01-117">Domaine</span><span class="sxs-lookup"><span data-stu-id="e6c01-117">Domain</span></span> `object`

<span data-ttu-id="e6c01-118">Description du domaine du protocole.</span><span class="sxs-lookup"><span data-stu-id="e6c01-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e6c01-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e6c01-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e6c01-120">name</span><span class="sxs-lookup"><span data-stu-id="e6c01-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e6c01-121">Nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="e6c01-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e6c01-122">version</span><span class="sxs-lookup"><span data-stu-id="e6c01-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e6c01-123">Version du domaine.</span><span class="sxs-lookup"><span data-stu-id="e6c01-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
