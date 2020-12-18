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
# <span data-ttu-id="a8f04-104">Domain Schema-DevTools Protocol version 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="a8f04-104">Schema Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="a8f04-105">Fournit des informations sur le schéma de protocole.</span><span class="sxs-lookup"><span data-stu-id="a8f04-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="a8f04-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a8f04-106">Methods</span></span>**](#methods) | [<span data-ttu-id="a8f04-107">getDomains</span><span class="sxs-lookup"><span data-stu-id="a8f04-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="a8f04-108">Types</span><span class="sxs-lookup"><span data-stu-id="a8f04-108">Types</span></span>**](#types) | [<span data-ttu-id="a8f04-109">Domaine</span><span class="sxs-lookup"><span data-stu-id="a8f04-109">Domain</span></span>](#domain) |
## <span data-ttu-id="a8f04-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a8f04-110">Methods</span></span>

### <span data-ttu-id="a8f04-111">getDomains</span><span class="sxs-lookup"><span data-stu-id="a8f04-111">getDomains</span></span>
<span data-ttu-id="a8f04-112">Renvoie les domaines pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a8f04-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a8f04-113">Renvoie</span><span class="sxs-lookup"><span data-stu-id="a8f04-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a8f04-114">ils</span><span class="sxs-lookup"><span data-stu-id="a8f04-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="a8f04-115">Liste des domaines pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a8f04-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="a8f04-116">Types</span><span class="sxs-lookup"><span data-stu-id="a8f04-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="a8f04-117">Domaine</span><span class="sxs-lookup"><span data-stu-id="a8f04-117">Domain</span></span> `object`

<span data-ttu-id="a8f04-118">Description du domaine du protocole.</span><span class="sxs-lookup"><span data-stu-id="a8f04-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a8f04-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a8f04-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a8f04-120">name</span><span class="sxs-lookup"><span data-stu-id="a8f04-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a8f04-121">Nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="a8f04-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a8f04-122">version</span><span class="sxs-lookup"><span data-stu-id="a8f04-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a8f04-123">Version du domaine.</span><span class="sxs-lookup"><span data-stu-id="a8f04-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
