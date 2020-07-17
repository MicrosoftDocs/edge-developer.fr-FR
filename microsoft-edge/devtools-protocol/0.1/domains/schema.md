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
# <span data-ttu-id="a660a-104">Domain Schema-DevTools Protocol version 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="a660a-104">Schema Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="a660a-105">Fournit des informations sur le schéma de protocole.</span><span class="sxs-lookup"><span data-stu-id="a660a-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="a660a-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a660a-106">Methods</span></span>**](#methods) | [<span data-ttu-id="a660a-107">getDomains</span><span class="sxs-lookup"><span data-stu-id="a660a-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="a660a-108">Types</span><span class="sxs-lookup"><span data-stu-id="a660a-108">Types</span></span>**](#types) | [<span data-ttu-id="a660a-109">Domaine</span><span class="sxs-lookup"><span data-stu-id="a660a-109">Domain</span></span>](#domain) |
## <span data-ttu-id="a660a-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a660a-110">Methods</span></span>

### <span data-ttu-id="a660a-111">getDomains</span><span class="sxs-lookup"><span data-stu-id="a660a-111">getDomains</span></span>
<span data-ttu-id="a660a-112">Renvoie les domaines pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a660a-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a660a-113">Renvoie</span><span class="sxs-lookup"><span data-stu-id="a660a-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a660a-114">ils</span><span class="sxs-lookup"><span data-stu-id="a660a-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="a660a-115">Liste des domaines pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a660a-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="a660a-116">Types</span><span class="sxs-lookup"><span data-stu-id="a660a-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="a660a-117">Domaine</span><span class="sxs-lookup"><span data-stu-id="a660a-117">Domain</span></span> `object`

<span data-ttu-id="a660a-118">Description du domaine du protocole.</span><span class="sxs-lookup"><span data-stu-id="a660a-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a660a-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a660a-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a660a-120">name</span><span class="sxs-lookup"><span data-stu-id="a660a-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a660a-121">Nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="a660a-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a660a-122">version</span><span class="sxs-lookup"><span data-stu-id="a660a-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a660a-123">Version du domaine.</span><span class="sxs-lookup"><span data-stu-id="a660a-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>

---
