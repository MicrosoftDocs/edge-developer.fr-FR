---
description: Référence pour le domaine de schéma. Fournit des informations sur le schéma de protocole.
title: Domain Schema-DevTools Protocol version 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: d0fbe9cde742d255797a2460b940732ffa5b8f27
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882876"
---
# <span data-ttu-id="08474-104">Domain Schema-DevTools Protocol version 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="08474-104">Schema Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="08474-105">Fournit des informations sur le schéma de protocole.</span><span class="sxs-lookup"><span data-stu-id="08474-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="08474-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="08474-106">Methods</span></span>**](#methods) | [<span data-ttu-id="08474-107">getDomains</span><span class="sxs-lookup"><span data-stu-id="08474-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="08474-108">Types</span><span class="sxs-lookup"><span data-stu-id="08474-108">Types</span></span>**](#types) | [<span data-ttu-id="08474-109">Domaine</span><span class="sxs-lookup"><span data-stu-id="08474-109">Domain</span></span>](#domain) |
## <span data-ttu-id="08474-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="08474-110">Methods</span></span>

### <span data-ttu-id="08474-111">getDomains</span><span class="sxs-lookup"><span data-stu-id="08474-111">getDomains</span></span>
<span data-ttu-id="08474-112">Renvoie les domaines pris en charge.</span><span class="sxs-lookup"><span data-stu-id="08474-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="08474-113">Renvoie</span><span class="sxs-lookup"><span data-stu-id="08474-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="08474-114">ils</span><span class="sxs-lookup"><span data-stu-id="08474-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="08474-115">Liste des domaines pris en charge.</span><span class="sxs-lookup"><span data-stu-id="08474-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="08474-116">Types</span><span class="sxs-lookup"><span data-stu-id="08474-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="08474-117">Domaine</span><span class="sxs-lookup"><span data-stu-id="08474-117">Domain</span></span> `object`

<span data-ttu-id="08474-118">Description du domaine du protocole.</span><span class="sxs-lookup"><span data-stu-id="08474-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="08474-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="08474-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="08474-120">name</span><span class="sxs-lookup"><span data-stu-id="08474-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="08474-121">Nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="08474-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="08474-122">version</span><span class="sxs-lookup"><span data-stu-id="08474-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="08474-123">Version du domaine.</span><span class="sxs-lookup"><span data-stu-id="08474-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
