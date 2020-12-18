---
description: Référence de la version 0,1 (EdgeHTML) du protocole DevTools pour le domaine de schéma. Fournit des informations sur le schéma de protocole.
title: Domain Schema-DevTools Protocol version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7b4ec71b7799ae099c673bd81fa5b15a8ddd5d27
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233242"
---
# <span data-ttu-id="246c3-104">Domain Schema-DevTools Protocol version 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="246c3-104">Schema Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="246c3-105">Fournit des informations sur le schéma de protocole.</span><span class="sxs-lookup"><span data-stu-id="246c3-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="246c3-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="246c3-106">Methods</span></span>**](#methods) | [<span data-ttu-id="246c3-107">getDomains</span><span class="sxs-lookup"><span data-stu-id="246c3-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="246c3-108">Types</span><span class="sxs-lookup"><span data-stu-id="246c3-108">Types</span></span>**](#types) | [<span data-ttu-id="246c3-109">Domaine</span><span class="sxs-lookup"><span data-stu-id="246c3-109">Domain</span></span>](#domain) |
## <span data-ttu-id="246c3-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="246c3-110">Methods</span></span>

### <span data-ttu-id="246c3-111">getDomains</span><span class="sxs-lookup"><span data-stu-id="246c3-111">getDomains</span></span>
<span data-ttu-id="246c3-112">Renvoie les domaines pris en charge.</span><span class="sxs-lookup"><span data-stu-id="246c3-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="246c3-113">Renvoie</span><span class="sxs-lookup"><span data-stu-id="246c3-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="246c3-114">ils</span><span class="sxs-lookup"><span data-stu-id="246c3-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="246c3-115">Liste des domaines pris en charge.</span><span class="sxs-lookup"><span data-stu-id="246c3-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="246c3-116">Types</span><span class="sxs-lookup"><span data-stu-id="246c3-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="246c3-117">Domaine</span><span class="sxs-lookup"><span data-stu-id="246c3-117">Domain</span></span> `object`

<span data-ttu-id="246c3-118">Description du domaine du protocole.</span><span class="sxs-lookup"><span data-stu-id="246c3-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="246c3-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="246c3-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="246c3-120">name</span><span class="sxs-lookup"><span data-stu-id="246c3-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="246c3-121">Nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="246c3-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="246c3-122">version</span><span class="sxs-lookup"><span data-stu-id="246c3-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="246c3-123">Version du domaine.</span><span class="sxs-lookup"><span data-stu-id="246c3-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>

---
