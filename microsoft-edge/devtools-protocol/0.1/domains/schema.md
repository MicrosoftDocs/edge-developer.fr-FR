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
# <span data-ttu-id="a5298-104">Schéma</span><span class="sxs-lookup"><span data-stu-id="a5298-104">Schema</span></span>
<span data-ttu-id="a5298-105">Fournit des informations sur le schéma de protocole.</span><span class="sxs-lookup"><span data-stu-id="a5298-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="a5298-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a5298-106">Methods</span></span>**](#methods) | [<span data-ttu-id="a5298-107">getDomains</span><span class="sxs-lookup"><span data-stu-id="a5298-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="a5298-108">Types</span><span class="sxs-lookup"><span data-stu-id="a5298-108">Types</span></span>**](#types) | [<span data-ttu-id="a5298-109">Domaine</span><span class="sxs-lookup"><span data-stu-id="a5298-109">Domain</span></span>](#domain) |
## <span data-ttu-id="a5298-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a5298-110">Methods</span></span>

### <span data-ttu-id="a5298-111">getDomains</span><span class="sxs-lookup"><span data-stu-id="a5298-111">getDomains</span></span>
<span data-ttu-id="a5298-112">Renvoie les domaines pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a5298-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a5298-113">Renvoie</span><span class="sxs-lookup"><span data-stu-id="a5298-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a5298-114">ils</span><span class="sxs-lookup"><span data-stu-id="a5298-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="a5298-115">Liste des domaines pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a5298-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="a5298-116">Types</span><span class="sxs-lookup"><span data-stu-id="a5298-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="a5298-117">Domaine</span><span class="sxs-lookup"><span data-stu-id="a5298-117">Domain</span></span> `object`

<span data-ttu-id="a5298-118">Description du domaine du protocole.</span><span class="sxs-lookup"><span data-stu-id="a5298-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a5298-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a5298-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a5298-120">name</span><span class="sxs-lookup"><span data-stu-id="a5298-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a5298-121">Nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="a5298-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a5298-122">version</span><span class="sxs-lookup"><span data-stu-id="a5298-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a5298-123">Version du domaine.</span><span class="sxs-lookup"><span data-stu-id="a5298-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>

---
