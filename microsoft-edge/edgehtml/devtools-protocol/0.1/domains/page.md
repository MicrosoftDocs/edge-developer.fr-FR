---
description: Référence du 0,1 Protocole DevTools (EdgeHTML) pour le domaine de la page. Les actions et événements liés à la page inspectée appartiennent au domaine de la page.
title: Page Domain-DevTools Protocol version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55575e54b9125d7ff544c23c81da4b15d3b56fb1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233249"
---
# <span data-ttu-id="b5f93-104">Page Domain-DevTools Protocol version 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="b5f93-104">Page Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="b5f93-105">Les actions et événements liés à la page inspectée appartiennent au domaine de la page.</span><span class="sxs-lookup"><span data-stu-id="b5f93-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="b5f93-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b5f93-106">Methods</span></span>**](#methods) | <span data-ttu-id="b5f93-107">[activer](#enable), [Désactiver](#disable), [naviguer](#navigate)</span><span class="sxs-lookup"><span data-stu-id="b5f93-107">[enable](#enable), [disable](#disable), [navigate](#navigate)</span></span> |
| [**<span data-ttu-id="b5f93-108">Types</span><span class="sxs-lookup"><span data-stu-id="b5f93-108">Types</span></span>**](#types) | [<span data-ttu-id="b5f93-109">FrameId</span><span class="sxs-lookup"><span data-stu-id="b5f93-109">FrameId</span></span>](#frameid) |
## <span data-ttu-id="b5f93-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b5f93-110">Methods</span></span>

### <span data-ttu-id="b5f93-111">activer</span><span class="sxs-lookup"><span data-stu-id="b5f93-111">enable</span></span>
<span data-ttu-id="b5f93-112">Active les notifications de domaine de page.</span><span class="sxs-lookup"><span data-stu-id="b5f93-112">Enables page domain notifications.</span></span>


---

### <span data-ttu-id="b5f93-113">désactiver </span><span class="sxs-lookup"><span data-stu-id="b5f93-113">disable</span></span>
<span data-ttu-id="b5f93-114">Désactive les notifications de domaine de la page.</span><span class="sxs-lookup"><span data-stu-id="b5f93-114">Disables page domain notifications.</span></span>


---

### <span data-ttu-id="b5f93-115">naviguer</span><span class="sxs-lookup"><span data-stu-id="b5f93-115">navigate</span></span>
<span data-ttu-id="b5f93-116">Accède à la page active à l’URL donnée.</span><span class="sxs-lookup"><span data-stu-id="b5f93-116">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b5f93-117">Parameters</span><span class="sxs-lookup"><span data-stu-id="b5f93-117">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b5f93-118">url</span><span class="sxs-lookup"><span data-stu-id="b5f93-118">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b5f93-119">URL permettant d’accéder à la page.</span><span class="sxs-lookup"><span data-stu-id="b5f93-119">URL to navigate the page to.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b5f93-120">Renvoie</span><span class="sxs-lookup"><span data-stu-id="b5f93-120">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b5f93-121">frameId</span><span class="sxs-lookup"><span data-stu-id="b5f93-121">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span><b><span data-ttu-id="b5f93-122">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="b5f93-122">Experimental.</span></span> </b></span><span data-ttu-id="b5f93-123">ID de cadre qui sera parcouru.</span><span class="sxs-lookup"><span data-stu-id="b5f93-123">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="b5f93-124">Types</span><span class="sxs-lookup"><span data-stu-id="b5f93-124">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="b5f93-125">FrameId</span><span class="sxs-lookup"><span data-stu-id="b5f93-125">FrameId</span></span> `string`

<span data-ttu-id="b5f93-126">Identificateur de cadre unique.</span><span class="sxs-lookup"><span data-stu-id="b5f93-126">Unique frame identifier.</span></span>


---
