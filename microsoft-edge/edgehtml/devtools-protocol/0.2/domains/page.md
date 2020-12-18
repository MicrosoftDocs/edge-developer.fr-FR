---
description: Référence du 0,2 Protocole DevTools (EdgeHTML) pour le domaine de la page. Les actions et événements liés à la page inspectée appartiennent au domaine de la page.
title: Page Domain-DevTools Protocol version 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2f1849a2e2aa2f53cef9dff5d03ac991d368a6f3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232859"
---
# <span data-ttu-id="f90f3-104">Page Domain-DevTools Protocol version 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="f90f3-104">Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="f90f3-105">Les actions et événements liés à la page inspectée appartiennent au domaine de la page.</span><span class="sxs-lookup"><span data-stu-id="f90f3-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="f90f3-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f90f3-106">Methods</span></span>**](#methods) | <span data-ttu-id="f90f3-107">[activer](#enable), [Désactiver](#disable), [naviguer](#navigate), [getFrameTree](#getframetree)</span><span class="sxs-lookup"><span data-stu-id="f90f3-107">[enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree)</span></span> |
| [**<span data-ttu-id="f90f3-108">Événements</span><span class="sxs-lookup"><span data-stu-id="f90f3-108">Events</span></span>**](#events) | <span data-ttu-id="f90f3-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span><span class="sxs-lookup"><span data-stu-id="f90f3-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span></span> |
| [**<span data-ttu-id="f90f3-110">Types</span><span class="sxs-lookup"><span data-stu-id="f90f3-110">Types</span></span>**](#types) | <span data-ttu-id="f90f3-111">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span><span class="sxs-lookup"><span data-stu-id="f90f3-111">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span></span> |
## <span data-ttu-id="f90f3-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f90f3-112">Methods</span></span>

### <span data-ttu-id="f90f3-113">activer</span><span class="sxs-lookup"><span data-stu-id="f90f3-113">enable</span></span>
<span data-ttu-id="f90f3-114">Active les notifications de domaine de page.</span><span class="sxs-lookup"><span data-stu-id="f90f3-114">Enables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="f90f3-115">désactiver </span><span class="sxs-lookup"><span data-stu-id="f90f3-115">disable</span></span>
<span data-ttu-id="f90f3-116">Désactive les notifications de domaine de la page.</span><span class="sxs-lookup"><span data-stu-id="f90f3-116">Disables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="f90f3-117">naviguer</span><span class="sxs-lookup"><span data-stu-id="f90f3-117">navigate</span></span>
<span data-ttu-id="f90f3-118">Accède à la page active à l’URL donnée.</span><span class="sxs-lookup"><span data-stu-id="f90f3-118">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f90f3-119">Parameters</span><span class="sxs-lookup"><span data-stu-id="f90f3-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f90f3-120">url</span><span class="sxs-lookup"><span data-stu-id="f90f3-120">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f90f3-121">URL permettant d’accéder à la page.</span><span class="sxs-lookup"><span data-stu-id="f90f3-121">URL to navigate the page to.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f90f3-122">frameId</span><span class="sxs-lookup"><span data-stu-id="f90f3-122">frameId</span></span> <br/> <i><span data-ttu-id="f90f3-123">facultatif</span><span class="sxs-lookup"><span data-stu-id="f90f3-123">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="f90f3-124">ID de cadre pour naviguer.</span><span class="sxs-lookup"><span data-stu-id="f90f3-124">Frame id to navigate.</span></span> <span data-ttu-id="f90f3-125">Si ce n’est pas le cas, accède à la page du haut.</span><span class="sxs-lookup"><span data-stu-id="f90f3-125">If not specified, will navigate the top page.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f90f3-126">Renvoie</span><span class="sxs-lookup"><span data-stu-id="f90f3-126">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f90f3-127">frameId</span><span class="sxs-lookup"><span data-stu-id="f90f3-127">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="f90f3-128">ID de cadre qui sera parcouru.</span><span class="sxs-lookup"><span data-stu-id="f90f3-128">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f90f3-129">getFrameTree</span><span class="sxs-lookup"><span data-stu-id="f90f3-129">getFrameTree</span></span>
<span data-ttu-id="f90f3-130">Renvoie une structure d’arborescence de trames.</span><span class="sxs-lookup"><span data-stu-id="f90f3-130">Returns present frame tree structure.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f90f3-131">Renvoie</span><span class="sxs-lookup"><span data-stu-id="f90f3-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f90f3-132">frameTree</span><span class="sxs-lookup"><span data-stu-id="f90f3-132">frameTree</span></span></td>
            <td><a href="#frametree"><code class="flyout">FrameTree</code></a></td>
            <td><span data-ttu-id="f90f3-133">Présenter une structure d’arborescence d’images</span><span class="sxs-lookup"><span data-stu-id="f90f3-133">Present frame tree structure.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="f90f3-134">Événements</span><span class="sxs-lookup"><span data-stu-id="f90f3-134">Events</span></span>

### <span data-ttu-id="f90f3-135">frameAttached</span><span class="sxs-lookup"><span data-stu-id="f90f3-135">frameAttached</span></span>
<span data-ttu-id="f90f3-136">Déclenché lorsque le frame a été attaché à son parent.</span><span class="sxs-lookup"><span data-stu-id="f90f3-136">Fired when frame has been attached to its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f90f3-137">Parameters</span><span class="sxs-lookup"><span data-stu-id="f90f3-137">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f90f3-138">frameId</span><span class="sxs-lookup"><span data-stu-id="f90f3-138">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="f90f3-139">ID de l’image jointe.</span><span class="sxs-lookup"><span data-stu-id="f90f3-139">Id of the frame that has been attached.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f90f3-140">parentFrameId</span><span class="sxs-lookup"><span data-stu-id="f90f3-140">parentFrameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="f90f3-141">Identificateur d’image parent.</span><span class="sxs-lookup"><span data-stu-id="f90f3-141">Parent frame identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f90f3-142">graphique</span><span class="sxs-lookup"><span data-stu-id="f90f3-142">stack</span></span> <br/> <i><span data-ttu-id="f90f3-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="f90f3-143">optional</span></span></i></td>
            <td><a href="runtime.md#stacktrace"><code class="flyout">Runtime.StackTrace</code></a></td>
            <td><span data-ttu-id="f90f3-144">Trace de pile JavaScript du moment où l’image a été attachée, ne définir que le frame lancé à partir d’un script.</span><span class="sxs-lookup"><span data-stu-id="f90f3-144">JavaScript stack trace of when frame was attached, only set if frame initiated from script.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f90f3-145">frameDetached</span><span class="sxs-lookup"><span data-stu-id="f90f3-145">frameDetached</span></span>
<span data-ttu-id="f90f3-146">Déclenché lorsque le frame a été détaché du parent.</span><span class="sxs-lookup"><span data-stu-id="f90f3-146">Fired when frame has been detached from its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f90f3-147">Parameters</span><span class="sxs-lookup"><span data-stu-id="f90f3-147">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f90f3-148">frameId</span><span class="sxs-lookup"><span data-stu-id="f90f3-148">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="f90f3-149">ID de l’image qui a été dissociée.</span><span class="sxs-lookup"><span data-stu-id="f90f3-149">Id of the frame that has been detached.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f90f3-150">frameNavigated</span><span class="sxs-lookup"><span data-stu-id="f90f3-150">frameNavigated</span></span>
<span data-ttu-id="f90f3-151">Déclenché une fois que la navigation de l’image est terminée.</span><span class="sxs-lookup"><span data-stu-id="f90f3-151">Fired once navigation of the frame has completed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f90f3-152">Parameters</span><span class="sxs-lookup"><span data-stu-id="f90f3-152">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f90f3-153">séquence</span><span class="sxs-lookup"><span data-stu-id="f90f3-153">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="f90f3-154">Objet Frame.</span><span class="sxs-lookup"><span data-stu-id="f90f3-154">Frame object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f90f3-155">loadEventFired</span><span class="sxs-lookup"><span data-stu-id="f90f3-155">loadEventFired</span></span>
<span data-ttu-id="f90f3-156">Correspond à l’événement Window. OnLoad.</span><span class="sxs-lookup"><span data-stu-id="f90f3-156">Corresponds to the window.onload event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f90f3-157">Parameters</span><span class="sxs-lookup"><span data-stu-id="f90f3-157">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f90f3-158">telle</span><span class="sxs-lookup"><span data-stu-id="f90f3-158">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="f90f3-159">Nombre de millisecondes depuis l’époque.</span><span class="sxs-lookup"><span data-stu-id="f90f3-159">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f90f3-160">domContentEventFired</span><span class="sxs-lookup"><span data-stu-id="f90f3-160">domContentEventFired</span></span>
<span data-ttu-id="f90f3-161">Correspond à l’événement document. onDOMContentLoaded.</span><span class="sxs-lookup"><span data-stu-id="f90f3-161">Corresponds to the document.onDOMContentLoaded event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f90f3-162">Parameters</span><span class="sxs-lookup"><span data-stu-id="f90f3-162">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f90f3-163">telle</span><span class="sxs-lookup"><span data-stu-id="f90f3-163">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="f90f3-164">Nombre de millisecondes depuis l’époque.</span><span class="sxs-lookup"><span data-stu-id="f90f3-164">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="f90f3-165">Types</span><span class="sxs-lookup"><span data-stu-id="f90f3-165">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="f90f3-166">FrameId</span><span class="sxs-lookup"><span data-stu-id="f90f3-166">FrameId</span></span> `string`

<span data-ttu-id="f90f3-167">Identificateur de cadre unique.</span><span class="sxs-lookup"><span data-stu-id="f90f3-167">Unique frame identifier.</span></span>

</p>

---

### <a name="frame"></a> <span data-ttu-id="f90f3-168">Trame</span><span class="sxs-lookup"><span data-stu-id="f90f3-168">Frame</span></span> `object`

<span data-ttu-id="f90f3-169">Des informations sur le cadre de la page.</span><span class="sxs-lookup"><span data-stu-id="f90f3-169">Information about the Frame on the Page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f90f3-170">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f90f3-170">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f90f3-171">id</span><span class="sxs-lookup"><span data-stu-id="f90f3-171">id</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="f90f3-172">Cadre identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="f90f3-172">Frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f90f3-173">Parent</span><span class="sxs-lookup"><span data-stu-id="f90f3-173">parentId</span></span> <br/> <i><span data-ttu-id="f90f3-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="f90f3-174">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="f90f3-175">Identificateur unique du cadre parent.</span><span class="sxs-lookup"><span data-stu-id="f90f3-175">Parent frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f90f3-176">name</span><span class="sxs-lookup"><span data-stu-id="f90f3-176">name</span></span> <br/> <i><span data-ttu-id="f90f3-177">facultatif</span><span class="sxs-lookup"><span data-stu-id="f90f3-177">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f90f3-178">Nom de l’image, tel que spécifié dans la balise.</span><span class="sxs-lookup"><span data-stu-id="f90f3-178">Frame's name as specified in the tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f90f3-179">url</span><span class="sxs-lookup"><span data-stu-id="f90f3-179">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f90f3-180">URL du document Frame.</span><span class="sxs-lookup"><span data-stu-id="f90f3-180">Frame document's URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f90f3-181">securityOrigin</span><span class="sxs-lookup"><span data-stu-id="f90f3-181">securityOrigin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f90f3-182">Origine de la sécurité du document Frame.</span><span class="sxs-lookup"><span data-stu-id="f90f3-182">Frame document's security origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f90f3-183">MIME</span><span class="sxs-lookup"><span data-stu-id="f90f3-183">mimeType</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f90f3-184">Le mimeType du document de cadre déterminé par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="f90f3-184">Frame document's mimeType as determined by the browser.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="frametree"></a> <span data-ttu-id="f90f3-185">FrameTree</span><span class="sxs-lookup"><span data-stu-id="f90f3-185">FrameTree</span></span> `object`

<span data-ttu-id="f90f3-186">Des informations sur la hiérarchie de trames.</span><span class="sxs-lookup"><span data-stu-id="f90f3-186">Information about the Frame hierarchy.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f90f3-187">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f90f3-187">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f90f3-188">séquence</span><span class="sxs-lookup"><span data-stu-id="f90f3-188">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="f90f3-189">Informations d’image pour cet élément d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="f90f3-189">Frame information for this tree item.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f90f3-190">childFrames</span><span class="sxs-lookup"><span data-stu-id="f90f3-190">childFrames</span></span> <br/> <i><span data-ttu-id="f90f3-191">facultatif</span><span class="sxs-lookup"><span data-stu-id="f90f3-191">optional</span></span></i></td>
            <td><a href="#frametree"><code class="flyout">FrameTree[]</code></a></td>
            <td><span data-ttu-id="f90f3-192">Images enfants.</span><span class="sxs-lookup"><span data-stu-id="f90f3-192">Child frames.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
