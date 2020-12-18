---
description: Référence pour le domaine DOM. Ce domaine expose les opérations en lecture/écriture DOM. Chaque nœud DOM est représenté avec son objet Mirror contenant un objet `id` . Cela `id` peut être utilisé pour obtenir des informations supplémentaires sur le nœud, le résoudre dans le wrapper d’objet JavaScript, etc. Il est important que le client reçoit les événements DOM uniquement pour les nœuds connus du client. Le principal effectue le suivi des nœuds envoyés au client et n’envoie jamais le même nœud deux fois. Il incombe au client de recueillir des informations sur les nœuds envoyés au client.<p>Notez que les `iframe` éléments de propriétaire renvoient les éléments de document correspondants comme leurs nœuds enfants.</p>
title: DOM Domain-DevTools Protocol version 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7d9861a2395f7b24142a41efea9ac599907dec27
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233238"
---
# <span data-ttu-id="057fe-109">DOM</span><span class="sxs-lookup"><span data-stu-id="057fe-109">DOM</span></span>

<span data-ttu-id="057fe-110">Ce domaine expose les opérations en lecture/écriture DOM.</span><span class="sxs-lookup"><span data-stu-id="057fe-110">This domain exposes DOM read/write operations.</span></span> <span data-ttu-id="057fe-111">Chaque nœud DOM est représenté avec son objet Mirror contenant un objet `id` .</span><span class="sxs-lookup"><span data-stu-id="057fe-111">Each DOM Node is represented with its mirror object that has an `id`.</span></span> <span data-ttu-id="057fe-112">Cela `id` peut être utilisé pour obtenir des informations supplémentaires sur le nœud, le résoudre dans le wrapper d’objet JavaScript, etc. Il est important que le client reçoit les événements DOM uniquement pour les nœuds connus du client.</span><span class="sxs-lookup"><span data-stu-id="057fe-112">This `id` can be used to get additional information on the Node, resolve it into the JavaScript object wrapper, etc. It is important that client receives DOM events only for the nodes that are known to the client.</span></span> <span data-ttu-id="057fe-113">Le principal effectue le suivi des nœuds envoyés au client et n’envoie jamais le même nœud deux fois.</span><span class="sxs-lookup"><span data-stu-id="057fe-113">Backend keeps track of the nodes that were sent to the client and never sends the same node twice.</span></span> <span data-ttu-id="057fe-114">Il incombe au client de recueillir des informations sur les nœuds envoyés au client.</span><span class="sxs-lookup"><span data-stu-id="057fe-114">It is client's responsibility to collect information about the nodes that were sent to the client.</span></span><p><span data-ttu-id="057fe-115">Notez que les `iframe` éléments de propriétaire renvoient les éléments de document correspondants comme leurs nœuds enfants.</span><span class="sxs-lookup"><span data-stu-id="057fe-115">Note that `iframe` owner elements will return corresponding document elements as their child nodes.</span></span></p>

| | |
|-|-|
| [**<span data-ttu-id="057fe-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="057fe-116">Methods</span></span>**](#methods) | <span data-ttu-id="057fe-117">[activer](#enable), [Désactiver](#disable), [GetDocument](#getdocument), [highlightNode](#highlightnode), [hideHighlight](#hidehighlight), [requestChildNodes](#requestchildnodes), [GetAttributes](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector), [querySelectorAll](#queryselectorall), [requestNode](#requestnode), [resolveNode](#resolvenode), [setInspectedNode](#setinspectednode)</span><span class="sxs-lookup"><span data-stu-id="057fe-117">[enable](#enable), [disable](#disable), [getDocument](#getdocument), [highlightNode](#highlightnode), [hideHighlight](#hidehighlight), [requestChildNodes](#requestchildnodes), [getAttributes](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector), [querySelectorAll](#queryselectorall), [requestNode](#requestnode), [resolveNode](#resolvenode), [setInspectedNode](#setinspectednode)</span></span> |
| [**<span data-ttu-id="057fe-118">Événements</span><span class="sxs-lookup"><span data-stu-id="057fe-118">Events</span></span>**](#events) | <span data-ttu-id="057fe-119">[setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated)</span><span class="sxs-lookup"><span data-stu-id="057fe-119">[setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated)</span></span> |
| [**<span data-ttu-id="057fe-120">Types</span><span class="sxs-lookup"><span data-stu-id="057fe-120">Types</span></span>**](#types) | <span data-ttu-id="057fe-121">[RVBA](#rgba), [HighlightConfig](#highlightconfig), [NodeId](#nodeid), [nœud](#node), [BackendNodeId](#backendnodeid), [PseudoType](#pseudotype)</span><span class="sxs-lookup"><span data-stu-id="057fe-121">[RGBA](#rgba), [HighlightConfig](#highlightconfig), [NodeId](#nodeid), [Node](#node), [BackendNodeId](#backendnodeid), [PseudoType](#pseudotype)</span></span> |
| [**<span data-ttu-id="057fe-122">Dépendances</span><span class="sxs-lookup"><span data-stu-id="057fe-122">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="057fe-123">Runtime</span><span class="sxs-lookup"><span data-stu-id="057fe-123">Runtime</span></span>](runtime.md) |
## <span data-ttu-id="057fe-124">Méthodes</span><span class="sxs-lookup"><span data-stu-id="057fe-124">Methods</span></span>

### <span data-ttu-id="057fe-125">activer</span><span class="sxs-lookup"><span data-stu-id="057fe-125">enable</span></span>
<span data-ttu-id="057fe-126">Active l’agent DOM pour la page donnée.</span><span class="sxs-lookup"><span data-stu-id="057fe-126">Enables DOM agent for the given page.</span></span>

</p>

---

### <span data-ttu-id="057fe-127">désactiver </span><span class="sxs-lookup"><span data-stu-id="057fe-127">disable</span></span>
<span data-ttu-id="057fe-128">Désactive l’agent DOM pour la page donnée.</span><span class="sxs-lookup"><span data-stu-id="057fe-128">Disables DOM agent for the given page.</span></span> <span data-ttu-id="057fe-129">La désactivation du DOM rendra non valide tout nodeIds précédemment valide.</span><span class="sxs-lookup"><span data-stu-id="057fe-129">Disabling the DOM will invalidate any previously valid nodeIds.</span></span>

</p>

---

### <span data-ttu-id="057fe-130">getDocument</span><span class="sxs-lookup"><span data-stu-id="057fe-130">getDocument</span></span>
<span data-ttu-id="057fe-131">Renvoie le nœud DOM racine (et éventuellement la sous-arborescence) pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="057fe-131">Returns the root DOM node (and optionally the subtree) to the caller.</span></span> <span data-ttu-id="057fe-132">`getDocument`Les appels seront non valides pour les nodeIdss précédemment valides.</span><span class="sxs-lookup"><span data-stu-id="057fe-132">Calling `getDocument` will invalidate any previously valid nodeIds</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-133">Parameters</span><span class="sxs-lookup"><span data-stu-id="057fe-133">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-134">expertise</span><span class="sxs-lookup"><span data-stu-id="057fe-134">depth</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="057fe-135">La profondeur maximale de récupération des enfants, par défaut de 2.</span><span class="sxs-lookup"><span data-stu-id="057fe-135">The maximum depth at which children should be retrieved, defaults to 2.</span></span> <span data-ttu-id="057fe-136">Utilisez-1 pour l’ensemble de la sous-arborescence.</span><span class="sxs-lookup"><span data-stu-id="057fe-136">Use -1 for entire subtree.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-137">traverser</span><span class="sxs-lookup"><span data-stu-id="057fe-137">pierce</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="057fe-138">Si les iframes doivent être parcourus lors du retour de la sous-arborescence (false par défaut).</span><span class="sxs-lookup"><span data-stu-id="057fe-138">Whether or not iframes should be traversed when returning the subtree (default is false).</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-139">Renvoie</span><span class="sxs-lookup"><span data-stu-id="057fe-139">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-140">associé</span><span class="sxs-lookup"><span data-stu-id="057fe-140">root</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="057fe-141">Nœud obtenu.</span><span class="sxs-lookup"><span data-stu-id="057fe-141">Resulting Node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="057fe-142">highlightNode</span><span class="sxs-lookup"><span data-stu-id="057fe-142">highlightNode</span></span>
<span data-ttu-id="057fe-143">Nœud DOM higlights avec ID donné ou wrapper d’objet.</span><span class="sxs-lookup"><span data-stu-id="057fe-143">Higlights DOM node with given id or object wrapper.</span></span> <span data-ttu-id="057fe-144">l’argument nodeId, backendNodeId ou objectId doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="057fe-144">nodeId, backendNodeId, or objectId must be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-145">Parameters</span><span class="sxs-lookup"><span data-stu-id="057fe-145">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-146">ID</span><span class="sxs-lookup"><span data-stu-id="057fe-146">nodeId</span></span> <br/> <i><span data-ttu-id="057fe-147">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-147">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-148">Identificateur du nœud à mettre en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="057fe-148">Identifier of the node to highlight.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-149">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="057fe-149">backendNodeId</span></span> <br/> <i><span data-ttu-id="057fe-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-150">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="057fe-151">Identificateur du nœud principal à mettre en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="057fe-151">Identifier of the backend node to highlight.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-152">Algorithm</span><span class="sxs-lookup"><span data-stu-id="057fe-152">objectId</span></span> <br/> <i><span data-ttu-id="057fe-153">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-153">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="057fe-154">ID d’objet JavaScript du nœud à mettre en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="057fe-154">JavaScript object id of the node to be highlighted.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-155">higlightConfig</span><span class="sxs-lookup"><span data-stu-id="057fe-155">higlightConfig</span></span></td>
            <td><a href="#highlightconfig"><code class="flyout">HighlightConfig</code></a></td>
            <td><span data-ttu-id="057fe-156">Descripteur de l’apparence de surlignage.</span><span class="sxs-lookup"><span data-stu-id="057fe-156">Descriptor of the highlight appearance.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-157">Renvoie</span><span class="sxs-lookup"><span data-stu-id="057fe-157">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-158">associé</span><span class="sxs-lookup"><span data-stu-id="057fe-158">root</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="057fe-159">Nœud obtenu.</span><span class="sxs-lookup"><span data-stu-id="057fe-159">Resulting Node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="057fe-160">hideHighlight</span><span class="sxs-lookup"><span data-stu-id="057fe-160">hideHighlight</span></span>
<span data-ttu-id="057fe-161">Masque la surbrillance du nœud DOM actuel.</span><span class="sxs-lookup"><span data-stu-id="057fe-161">Hides any current DOM node highlight.</span></span>

</p>

---

### <span data-ttu-id="057fe-162">requestChildNodes</span><span class="sxs-lookup"><span data-stu-id="057fe-162">requestChildNodes</span></span>
<span data-ttu-id="057fe-163">Demande que les enfants du nœud avec ID donné soient renvoyés à l’appelant gué sous la forme d' `setChildNodes` événements.</span><span class="sxs-lookup"><span data-stu-id="057fe-163">Requests that children of the node with given id are returned to ghe caller in the form of `setChildNodes` events.</span></span> `setChildNodes` <span data-ttu-id="057fe-164">sera déclenché pour tous les nœuds qui n’ont pas encore renvoyé leurs enfants, en partant du nœud requis vers la profondeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="057fe-164">will be fired for each node that has not previously returned it's children, starting from the requested node down to the specified depth.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-165">Parameters</span><span class="sxs-lookup"><span data-stu-id="057fe-165">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-166">ID</span><span class="sxs-lookup"><span data-stu-id="057fe-166">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-167">ID du nœud à partir duquel obtenir des enfants.</span><span class="sxs-lookup"><span data-stu-id="057fe-167">Id of the node to get children from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-168">expertise</span><span class="sxs-lookup"><span data-stu-id="057fe-168">depth</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="057fe-169">La profondeur maximale de récupération des enfants, par défaut de 1.</span><span class="sxs-lookup"><span data-stu-id="057fe-169">The maximum depth at which children should be retrieved, defaults to 1.</span></span> <span data-ttu-id="057fe-170">Utilisez-1 pour l’ensemble de la sous-arborescence.</span><span class="sxs-lookup"><span data-stu-id="057fe-170">Use -1 for entire subtree.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-171">traverser</span><span class="sxs-lookup"><span data-stu-id="057fe-171">pierce</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="057fe-172">Si les iframes doivent être parcourus lors du retour de la sous-arborescence (false par défaut).</span><span class="sxs-lookup"><span data-stu-id="057fe-172">Whether or not iframes should be traversed when returning the subtree (default is false).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="057fe-173">getAttributes</span><span class="sxs-lookup"><span data-stu-id="057fe-173">getAttributes</span></span>
<span data-ttu-id="057fe-174">Renvoie les attributs du nœud spécifié.</span><span class="sxs-lookup"><span data-stu-id="057fe-174">Returns attributes for the specified node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-175">Parameters</span><span class="sxs-lookup"><span data-stu-id="057fe-175">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-176">ID</span><span class="sxs-lookup"><span data-stu-id="057fe-176">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-177">ID du nœud duquel récupérer attibutes.</span><span class="sxs-lookup"><span data-stu-id="057fe-177">Id of the node to retrieve attibutes for.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-178">Renvoie</span><span class="sxs-lookup"><span data-stu-id="057fe-178">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-179">Propriétés</span><span class="sxs-lookup"><span data-stu-id="057fe-179">attributes</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="057fe-180">Tableau entrelacé de noms et de valeurs d’attributs de nœud.</span><span class="sxs-lookup"><span data-stu-id="057fe-180">An interleaved array of node attribute names and values.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="057fe-181">getOuterHTML</span><span class="sxs-lookup"><span data-stu-id="057fe-181">getOuterHTML</span></span>
<span data-ttu-id="057fe-182">Renvoie le balisage HTML du nœud.</span><span class="sxs-lookup"><span data-stu-id="057fe-182">Returns node's HTML markup.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-183">Parameters</span><span class="sxs-lookup"><span data-stu-id="057fe-183">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-184">ID</span><span class="sxs-lookup"><span data-stu-id="057fe-184">nodeId</span></span> <br/> <i><span data-ttu-id="057fe-185">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-185">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-186">Identificateur du nœud.</span><span class="sxs-lookup"><span data-stu-id="057fe-186">Identifier of the node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-187">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="057fe-187">backendNodeId</span></span> <br/> <i><span data-ttu-id="057fe-188">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-188">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="057fe-189">Identificateur du nœud principal.</span><span class="sxs-lookup"><span data-stu-id="057fe-189">Identifier of the backend node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-190">Algorithm</span><span class="sxs-lookup"><span data-stu-id="057fe-190">objectId</span></span> <br/> <i><span data-ttu-id="057fe-191">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-191">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="057fe-192">ID d’objet JavaScript du wrapper de nœud.</span><span class="sxs-lookup"><span data-stu-id="057fe-192">JavaScript object id of the node wrapper.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-193">Renvoie</span><span class="sxs-lookup"><span data-stu-id="057fe-193">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-194">outerHTML</span><span class="sxs-lookup"><span data-stu-id="057fe-194">outerHTML</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="057fe-195">Balisage HTML externe.</span><span class="sxs-lookup"><span data-stu-id="057fe-195">Outer HTML markup.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="057fe-196">pushNodesByBackendIdsToFrontend</span><span class="sxs-lookup"><span data-stu-id="057fe-196">pushNodesByBackendIdsToFrontend</span></span>
<span data-ttu-id="057fe-197">Recherche les ID de nœud et résolve tous les parents pour les ID de nœud principal spécifiés.</span><span class="sxs-lookup"><span data-stu-id="057fe-197">Looks up Node Ids and resolves all parents for the specified Backend Node Ids</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-198">Parameters</span><span class="sxs-lookup"><span data-stu-id="057fe-198">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-199">backendNodeIds</span><span class="sxs-lookup"><span data-stu-id="057fe-199">backendNodeIds</span></span></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId[]</code></a></td>
            <td><span data-ttu-id="057fe-200">ID de nœud principal des nœuds à résoudre</span><span class="sxs-lookup"><span data-stu-id="057fe-200">Backend Node IDs of the nodes to resolve</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-201">Renvoie</span><span class="sxs-lookup"><span data-stu-id="057fe-201">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-202">nodeIds</span><span class="sxs-lookup"><span data-stu-id="057fe-202">nodeIds</span></span></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td><span data-ttu-id="057fe-203">ID de nœud des nœuds résolus</span><span class="sxs-lookup"><span data-stu-id="057fe-203">Node Ids of the resolved nodes</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="057fe-204">querySelector</span><span class="sxs-lookup"><span data-stu-id="057fe-204">querySelector</span></span>
<span data-ttu-id="057fe-205">S’exécute `querySelector` sur un nœud donné.</span><span class="sxs-lookup"><span data-stu-id="057fe-205">Executes `querySelector` on a given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-206">Parameters</span><span class="sxs-lookup"><span data-stu-id="057fe-206">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-207">ID</span><span class="sxs-lookup"><span data-stu-id="057fe-207">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-208">ID du nœud sur lequel interroger.</span><span class="sxs-lookup"><span data-stu-id="057fe-208">Id of the node to query upon.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-209">sélecteur</span><span class="sxs-lookup"><span data-stu-id="057fe-209">selector</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="057fe-210">Chaîne de sélecteur.</span><span class="sxs-lookup"><span data-stu-id="057fe-210">The selector string.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-211">Renvoie</span><span class="sxs-lookup"><span data-stu-id="057fe-211">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-212">ID</span><span class="sxs-lookup"><span data-stu-id="057fe-212">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-213">Résultat du sélecteur de requête.</span><span class="sxs-lookup"><span data-stu-id="057fe-213">Query selector result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="057fe-214">querySelectorAll</span><span class="sxs-lookup"><span data-stu-id="057fe-214">querySelectorAll</span></span>
<span data-ttu-id="057fe-215">S’exécute `querySelectorAll` sur un nœud donné.</span><span class="sxs-lookup"><span data-stu-id="057fe-215">Executes `querySelectorAll` on a given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-216">Parameters</span><span class="sxs-lookup"><span data-stu-id="057fe-216">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-217">ID</span><span class="sxs-lookup"><span data-stu-id="057fe-217">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-218">ID du nœud sur lequel interroger.</span><span class="sxs-lookup"><span data-stu-id="057fe-218">Id of the node to query upon.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-219">sélecteur</span><span class="sxs-lookup"><span data-stu-id="057fe-219">selector</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="057fe-220">Chaîne de sélecteur.</span><span class="sxs-lookup"><span data-stu-id="057fe-220">The selector string.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-221">Renvoie</span><span class="sxs-lookup"><span data-stu-id="057fe-221">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-222">nodeIds</span><span class="sxs-lookup"><span data-stu-id="057fe-222">nodeIds</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td><span data-ttu-id="057fe-223">Résultats du sélecteur de requête.</span><span class="sxs-lookup"><span data-stu-id="057fe-223">Query selector results.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="057fe-224">requestNode</span><span class="sxs-lookup"><span data-stu-id="057fe-224">requestNode</span></span>
<span data-ttu-id="057fe-225">Demande que le nœud avec l’ID d’objet distant fourni soit envoyé à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="057fe-225">Requests that the node with given remote object Id is sent to caller.</span></span> <span data-ttu-id="057fe-226">Tous les nœuds qui constituent le chemin d’accès du nœud à la racine sont également envoyés au client dans le cadre d’une série de `setChildNodes` notifications.</span><span class="sxs-lookup"><span data-stu-id="057fe-226">All nodes that form the path from the node to the root are also sent to the client as a series of `setChildNodes` notifications.</span></span> <span data-ttu-id="057fe-227">renvoie 0 si le document contenant le nœud demandé n’a pas encore été demandé par le client.</span><span class="sxs-lookup"><span data-stu-id="057fe-227">returns 0 if the document containing the requested node has not previously been requested by the client.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-228">Parameters</span><span class="sxs-lookup"><span data-stu-id="057fe-228">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-229">Algorithm</span><span class="sxs-lookup"><span data-stu-id="057fe-229">objectId</span></span></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="057fe-230">ID d’objet JavaScript à convertir en nœud.</span><span class="sxs-lookup"><span data-stu-id="057fe-230">JavaScript object Id to convert into node.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-231">Renvoie</span><span class="sxs-lookup"><span data-stu-id="057fe-231">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-232">ID</span><span class="sxs-lookup"><span data-stu-id="057fe-232">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-233">ID de nœud pour l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="057fe-233">Node Id for given object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="057fe-234">resolveNode</span><span class="sxs-lookup"><span data-stu-id="057fe-234">resolveNode</span></span>
<span data-ttu-id="057fe-235">Résout l’objet de nœud JavaScript pour une NodeId ou BackendNodeId donnée.</span><span class="sxs-lookup"><span data-stu-id="057fe-235">Resolves the JavaScript node object for a given NodeId or BackendNodeId.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-236">Parameters</span><span class="sxs-lookup"><span data-stu-id="057fe-236">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-237">ID</span><span class="sxs-lookup"><span data-stu-id="057fe-237">nodeId</span></span> <br/> <i><span data-ttu-id="057fe-238">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-238">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-239">ID du nœud à résoudre.</span><span class="sxs-lookup"><span data-stu-id="057fe-239">Id of the node to resolve.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-240">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="057fe-240">backendNodeId</span></span> <br/> <i><span data-ttu-id="057fe-241">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-241">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="057fe-242">ID du nœud principal du nœud à résoudre.</span><span class="sxs-lookup"><span data-stu-id="057fe-242">Backend Node Id of the node to resolve.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-243">objectGroup</span><span class="sxs-lookup"><span data-stu-id="057fe-243">objectGroup</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="057fe-244">Nom du groupe de symboles qui peut être utilisé pour libérer plusieurs objets.</span><span class="sxs-lookup"><span data-stu-id="057fe-244">Symbolic group name that can be used to release multiple objects.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-245">Renvoie</span><span class="sxs-lookup"><span data-stu-id="057fe-245">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-246">object</span><span class="sxs-lookup"><span data-stu-id="057fe-246">object</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="057fe-247">Wrapper d’objet JavaScript pour le nœud donné.</span><span class="sxs-lookup"><span data-stu-id="057fe-247">JavaScript object wrapper for given node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="057fe-248">setInspectedNode</span><span class="sxs-lookup"><span data-stu-id="057fe-248">setInspectedNode</span></span>
<span><b><span data-ttu-id="057fe-249">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="057fe-249">Experimental.</span></span> </b></span><span data-ttu-id="057fe-250">Autorise la console à faire référence au nœud inspecté précédent avec l’ID donné via $0-$ 4.</span><span class="sxs-lookup"><span data-stu-id="057fe-250">Enables console to refer to the previous inspected node with given id via $0-$4.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-251">Parameters</span><span class="sxs-lookup"><span data-stu-id="057fe-251">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-252">ID</span><span class="sxs-lookup"><span data-stu-id="057fe-252">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-253">ID de nœud DOM à rendre accessible par le biais de $0-$ 4 dans l’API de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="057fe-253">DOM node id to be accessible by means of $0-$4 in command line API.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="057fe-254">Événements</span><span class="sxs-lookup"><span data-stu-id="057fe-254">Events</span></span>

### <span data-ttu-id="057fe-255">setChildNodes</span><span class="sxs-lookup"><span data-stu-id="057fe-255">setChildNodes</span></span>
<span data-ttu-id="057fe-256">Déclenché lorsque le serveur principal souhaite fournir un client avec une structure DOM introuvable.</span><span class="sxs-lookup"><span data-stu-id="057fe-256">Fired when the backend wishes to provide client with missing DOM structure.</span></span> <span data-ttu-id="057fe-257">Ce problème se produit sur la plupart des appels demandant nodeIds</span><span class="sxs-lookup"><span data-stu-id="057fe-257">This happens upon most calls requesting nodeIds</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-258">Parameters</span><span class="sxs-lookup"><span data-stu-id="057fe-258">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-259">Parent</span><span class="sxs-lookup"><span data-stu-id="057fe-259">parentId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-260">Nœud parent à poplate avec des enfants.</span><span class="sxs-lookup"><span data-stu-id="057fe-260">Parent node to poplate with children.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-261">ceux</span><span class="sxs-lookup"><span data-stu-id="057fe-261">nodes</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td><span data-ttu-id="057fe-262">Tableau de nœuds enfants.</span><span class="sxs-lookup"><span data-stu-id="057fe-262">Child nodes array.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="057fe-263">attributeModified</span><span class="sxs-lookup"><span data-stu-id="057fe-263">attributeModified</span></span>
<span data-ttu-id="057fe-264">Déclenché lorsque `Element` l’attribut a été modifié.</span><span class="sxs-lookup"><span data-stu-id="057fe-264">Fired when `Element`'s attribute is modified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-265">Parameters</span><span class="sxs-lookup"><span data-stu-id="057fe-265">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-266">ID</span><span class="sxs-lookup"><span data-stu-id="057fe-266">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-267">ID du nœud qui a changé.</span><span class="sxs-lookup"><span data-stu-id="057fe-267">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-268">name</span><span class="sxs-lookup"><span data-stu-id="057fe-268">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="057fe-269">Nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="057fe-269">Attribute name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-270">value</span><span class="sxs-lookup"><span data-stu-id="057fe-270">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="057fe-271">Valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="057fe-271">Attribute value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="057fe-272">attributeRemoved</span><span class="sxs-lookup"><span data-stu-id="057fe-272">attributeRemoved</span></span>
<span data-ttu-id="057fe-273">Déclenché lorsque `Element` l’attribut est supprimé.</span><span class="sxs-lookup"><span data-stu-id="057fe-273">Fired when `Element`'s attribute is removed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-274">Parameters</span><span class="sxs-lookup"><span data-stu-id="057fe-274">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-275">ID</span><span class="sxs-lookup"><span data-stu-id="057fe-275">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-276">ID du nœud qui a changé.</span><span class="sxs-lookup"><span data-stu-id="057fe-276">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-277">name</span><span class="sxs-lookup"><span data-stu-id="057fe-277">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="057fe-278">Nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="057fe-278">Attribute name.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="057fe-279">characterDataModified</span><span class="sxs-lookup"><span data-stu-id="057fe-279">characterDataModified</span></span>
<span data-ttu-id="057fe-280">`DOMCharacterDataModified`Événement miroirs.</span><span class="sxs-lookup"><span data-stu-id="057fe-280">Mirrors `DOMCharacterDataModified` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-281">Parameters</span><span class="sxs-lookup"><span data-stu-id="057fe-281">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-282">ID</span><span class="sxs-lookup"><span data-stu-id="057fe-282">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-283">ID du nœud qui a changé.</span><span class="sxs-lookup"><span data-stu-id="057fe-283">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-284">charcterData</span><span class="sxs-lookup"><span data-stu-id="057fe-284">charcterData</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="057fe-285">Nouvelle valeur de texte.</span><span class="sxs-lookup"><span data-stu-id="057fe-285">New text value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="057fe-286">childNodeInserted</span><span class="sxs-lookup"><span data-stu-id="057fe-286">childNodeInserted</span></span>
<span data-ttu-id="057fe-287">`DOMNodeInserted`Événement miroirs.</span><span class="sxs-lookup"><span data-stu-id="057fe-287">Mirrors `DOMNodeInserted` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-288">Parameters</span><span class="sxs-lookup"><span data-stu-id="057fe-288">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-289">parentNodeId</span><span class="sxs-lookup"><span data-stu-id="057fe-289">parentNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-290">ID du nœud qui a changé.</span><span class="sxs-lookup"><span data-stu-id="057fe-290">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-291">previousNodeId</span><span class="sxs-lookup"><span data-stu-id="057fe-291">previousNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-292">ID du frère précédent du nœud inséré.</span><span class="sxs-lookup"><span data-stu-id="057fe-292">Id of the inserted node's previous sibling.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-293">nœud</span><span class="sxs-lookup"><span data-stu-id="057fe-293">node</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="057fe-294">Données de nœud insérées.</span><span class="sxs-lookup"><span data-stu-id="057fe-294">Inserted node data.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="057fe-295">childNodeRemoved</span><span class="sxs-lookup"><span data-stu-id="057fe-295">childNodeRemoved</span></span>
<span data-ttu-id="057fe-296">`DOMNodeRemoved`Événement miroirs.</span><span class="sxs-lookup"><span data-stu-id="057fe-296">Mirrors `DOMNodeRemoved` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-297">Parameters</span><span class="sxs-lookup"><span data-stu-id="057fe-297">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-298">parentNodeId</span><span class="sxs-lookup"><span data-stu-id="057fe-298">parentNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-299">ID du nœud qui a changé.</span><span class="sxs-lookup"><span data-stu-id="057fe-299">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-300">ID</span><span class="sxs-lookup"><span data-stu-id="057fe-300">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-301">ID du nœud qui a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="057fe-301">Id of the node that has been removed.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="057fe-302">documentUpdated</span><span class="sxs-lookup"><span data-stu-id="057fe-302">documentUpdated</span></span>
<span data-ttu-id="057fe-303">Déclenché lors de la `Document` mise à jour.</span><span class="sxs-lookup"><span data-stu-id="057fe-303">Fired when `Document` has been totally updated.</span></span> <span data-ttu-id="057fe-304">Les ID de nœud ne sont plus valides.</span><span class="sxs-lookup"><span data-stu-id="057fe-304">Node ids are no longer valid.</span></span>

</p>

---

## <span data-ttu-id="057fe-305">Types</span><span class="sxs-lookup"><span data-stu-id="057fe-305">Types</span></span>

### <a name="rgba"></a> <span data-ttu-id="057fe-306">RVBA</span><span class="sxs-lookup"><span data-stu-id="057fe-306">RGBA</span></span> `object`

<span data-ttu-id="057fe-307">Structure contenant une couleur RVBA.</span><span class="sxs-lookup"><span data-stu-id="057fe-307">A Structure holding an RGBA color.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-308">Propriétés</span><span class="sxs-lookup"><span data-stu-id="057fe-308">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-309">v</span><span class="sxs-lookup"><span data-stu-id="057fe-309">r</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="057fe-310">Composant rouge dans la plage [0-255].</span><span class="sxs-lookup"><span data-stu-id="057fe-310">The red component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-311">grand</span><span class="sxs-lookup"><span data-stu-id="057fe-311">g</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="057fe-312">Composant vert dans la plage [0-255].</span><span class="sxs-lookup"><span data-stu-id="057fe-312">The green component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-313">p</span><span class="sxs-lookup"><span data-stu-id="057fe-313">b</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="057fe-314">Composant bleu dans la plage [0-255].</span><span class="sxs-lookup"><span data-stu-id="057fe-314">The blue component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-315">a</span><span class="sxs-lookup"><span data-stu-id="057fe-315">a</span></span> <br/> <i><span data-ttu-id="057fe-316">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-316">optional</span></span></i></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="057fe-317">Composant alpha dans la plage [0-1].</span><span class="sxs-lookup"><span data-stu-id="057fe-317">The alpha component, in the [0-1] range.</span></span> <span data-ttu-id="057fe-318">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="057fe-318">Default is 1.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="highlightconfig"></a> <span data-ttu-id="057fe-319">HighlightConfig</span><span class="sxs-lookup"><span data-stu-id="057fe-319">HighlightConfig</span></span> `object`

<span data-ttu-id="057fe-320">Données de configuration pour la mise en surbrillance des éléments de page.</span><span class="sxs-lookup"><span data-stu-id="057fe-320">Configuration data for highlighting of page elements.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-321">Propriétés</span><span class="sxs-lookup"><span data-stu-id="057fe-321">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-322">contentColor</span><span class="sxs-lookup"><span data-stu-id="057fe-322">contentColor</span></span> <br/> <i><span data-ttu-id="057fe-323">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-323">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="057fe-324">La zone de contenu surligne la couleur de remplissage.</span><span class="sxs-lookup"><span data-stu-id="057fe-324">The content box highlight fill color.</span></span> <span data-ttu-id="057fe-325">La valeur par défaut est transparent.</span><span class="sxs-lookup"><span data-stu-id="057fe-325">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-326">paddingColor</span><span class="sxs-lookup"><span data-stu-id="057fe-326">paddingColor</span></span> <br/> <i><span data-ttu-id="057fe-327">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-327">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="057fe-328">Couleur de remplissage de la mise en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="057fe-328">The padding highlight fill color.</span></span> <span data-ttu-id="057fe-329">La valeur par défaut est transparent.</span><span class="sxs-lookup"><span data-stu-id="057fe-329">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-330">Bordure</span><span class="sxs-lookup"><span data-stu-id="057fe-330">borderColor</span></span> <br/> <i><span data-ttu-id="057fe-331">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-331">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="057fe-332">Couleur de remplissage de la bordure surlignée.</span><span class="sxs-lookup"><span data-stu-id="057fe-332">The border highlight fill color.</span></span> <span data-ttu-id="057fe-333">La valeur par défaut est transparent.</span><span class="sxs-lookup"><span data-stu-id="057fe-333">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-334">marginColor</span><span class="sxs-lookup"><span data-stu-id="057fe-334">marginColor</span></span> <br/> <i><span data-ttu-id="057fe-335">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-335">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="057fe-336">Couleur de remplissage de l’accentuation des marges</span><span class="sxs-lookup"><span data-stu-id="057fe-336">The margin highlight fill color.</span></span> <span data-ttu-id="057fe-337">La valeur par défaut est transparent.</span><span class="sxs-lookup"><span data-stu-id="057fe-337">Default is transparent.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="nodeid"></a> <span data-ttu-id="057fe-338">ID</span><span class="sxs-lookup"><span data-stu-id="057fe-338">NodeId</span></span> `integer`

<span data-ttu-id="057fe-339">Identificateur de nœud DOM unique</span><span class="sxs-lookup"><span data-stu-id="057fe-339">Unique DOM node identifier</span></span>

</p>

---

### <a name="node"></a> <span data-ttu-id="057fe-340">Nœud</span><span class="sxs-lookup"><span data-stu-id="057fe-340">Node</span></span> `object`

<span data-ttu-id="057fe-341">Objet Mirror qui représente les nœuds DOM réels.</span><span class="sxs-lookup"><span data-stu-id="057fe-341">Mirror object that represents the actual DOM nodes.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="057fe-342">Propriétés</span><span class="sxs-lookup"><span data-stu-id="057fe-342">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="057fe-343">ID</span><span class="sxs-lookup"><span data-stu-id="057fe-343">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-344">Identificateur de nœud utilisé pour référencer ce nœud.</span><span class="sxs-lookup"><span data-stu-id="057fe-344">Node Identifier used to reference this node.</span></span> <span data-ttu-id="057fe-345">Le système principal déclenche les événements DOM pour les nœuds ayant un ID de nœud dont le nom est connu par le client.</span><span class="sxs-lookup"><span data-stu-id="057fe-345">Backend will fire DOM events for nodes that have a nodeId that is known to the client</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-346">Parent</span><span class="sxs-lookup"><span data-stu-id="057fe-346">parentId</span></span> <br/> <i><span data-ttu-id="057fe-347">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-347">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-348">Identificateur de nœud du nœud parent, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="057fe-348">Node Identifier of the parent Node, if any.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-349">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="057fe-349">backendNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="057fe-350">Identificateur du nœud principal du nœud.</span><span class="sxs-lookup"><span data-stu-id="057fe-350">Backend Node identifier of the node.</span></span> <span data-ttu-id="057fe-351">Les nœuds de référence BackendNodeIds qui peuvent être connus du client, mais qui ne renvoient pas d’événements DOM sur ce nœud.</span><span class="sxs-lookup"><span data-stu-id="057fe-351">BackendNodeIds reference Nodes that can be known to the client, but do not push DOM events about this node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-352">nodeType</span><span class="sxs-lookup"><span data-stu-id="057fe-352">nodeType</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td>`Node`<span data-ttu-id="057fe-353">nodeType.</span><span class="sxs-lookup"><span data-stu-id="057fe-353">'s nodeType.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-354">nodeName</span><span class="sxs-lookup"><span data-stu-id="057fe-354">nodeName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="057fe-355">nodeName.</span><span class="sxs-lookup"><span data-stu-id="057fe-355">'s nodeName.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-356">Local</span><span class="sxs-lookup"><span data-stu-id="057fe-356">localName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="057fe-357">localName du</span><span class="sxs-lookup"><span data-stu-id="057fe-357">'s localName</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-358">nodeValue</span><span class="sxs-lookup"><span data-stu-id="057fe-358">nodeValue</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="057fe-359">nodeValue du</span><span class="sxs-lookup"><span data-stu-id="057fe-359">'s nodeValue</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-360">childNodeCount</span><span class="sxs-lookup"><span data-stu-id="057fe-360">childNodeCount</span></span> <br/> <i><span data-ttu-id="057fe-361">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-361">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="057fe-362">Nombre enfant de `Container` nœuds.</span><span class="sxs-lookup"><span data-stu-id="057fe-362">Child count for `Container` nodes.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-363">enfants</span><span class="sxs-lookup"><span data-stu-id="057fe-363">children</span></span> <br/> <i><span data-ttu-id="057fe-364">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-364">optional</span></span></i></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td><span data-ttu-id="057fe-365">Nœud enfant de ce nœud lors de la demande avec des enfants.</span><span class="sxs-lookup"><span data-stu-id="057fe-365">Child nodes of this node when requested with children.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-366">Propriétés</span><span class="sxs-lookup"><span data-stu-id="057fe-366">attributes</span></span> <br/> <i><span data-ttu-id="057fe-367">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-367">optional</span></span></i></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="057fe-368">Attributs des `Element` nœuds sous la forme d’un tableau à plat' [nom1, valeur1, nom2, valeur2]</span><span class="sxs-lookup"><span data-stu-id="057fe-368">Attributes of `Element` nodes in the form of a flat array \`[name1, value1, name2, value2]</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-369">documentURL</span><span class="sxs-lookup"><span data-stu-id="057fe-369">documentURL</span></span> <br/> <i><span data-ttu-id="057fe-370">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-370">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="057fe-371">URL du document `Document` pointant vers le nœud.</span><span class="sxs-lookup"><span data-stu-id="057fe-371">Document URL that `Document` nodes point to.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-372">baseURL</span><span class="sxs-lookup"><span data-stu-id="057fe-372">baseURL</span></span> <br/> <i><span data-ttu-id="057fe-373">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-373">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="057fe-374">URL du document que `Document` les nœuds utilisent pour la fin des URL.</span><span class="sxs-lookup"><span data-stu-id="057fe-374">Document URL that `Document` nodes use for URL completion.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-375">publicId</span><span class="sxs-lookup"><span data-stu-id="057fe-375">publicId</span></span> <br/> <i><span data-ttu-id="057fe-376">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-376">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="057fe-377">PublicId du nœud.</span><span class="sxs-lookup"><span data-stu-id="057fe-377">Node's publicId.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-378">systemId</span><span class="sxs-lookup"><span data-stu-id="057fe-378">systemId</span></span> <br/> <i><span data-ttu-id="057fe-379">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-379">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="057fe-380">SystemId du nœud.</span><span class="sxs-lookup"><span data-stu-id="057fe-380">Node's systemId.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-381">internalSubset</span><span class="sxs-lookup"><span data-stu-id="057fe-381">internalSubset</span></span> <br/> <i><span data-ttu-id="057fe-382">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-382">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="057fe-383">InternalSubset du nœud.</span><span class="sxs-lookup"><span data-stu-id="057fe-383">Node's internalSubset.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-384">xmlVersion</span><span class="sxs-lookup"><span data-stu-id="057fe-384">xmlVersion</span></span> <br/> <i><span data-ttu-id="057fe-385">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-385">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Document` <span data-ttu-id="057fe-386">Version XML du nœud dans le cas de documents XML.</span><span class="sxs-lookup"><span data-stu-id="057fe-386">Node's xml version in the case of XML documents.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-387">name</span><span class="sxs-lookup"><span data-stu-id="057fe-387">name</span></span> <br/> <i><span data-ttu-id="057fe-388">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-388">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` <span data-ttu-id="057fe-389">Nom du nœud.</span><span class="sxs-lookup"><span data-stu-id="057fe-389">Node's name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-390">value</span><span class="sxs-lookup"><span data-stu-id="057fe-390">value</span></span> <br/> <i><span data-ttu-id="057fe-391">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-391">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` <span data-ttu-id="057fe-392">Valeur du nœud.</span><span class="sxs-lookup"><span data-stu-id="057fe-392">Node's value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-393">frameId</span><span class="sxs-lookup"><span data-stu-id="057fe-393">frameId</span></span> <br/> <i><span data-ttu-id="057fe-394">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-394">optional</span></span></i></td>
            <td><a href="page.md#frameid"><code class="flyout">Page.FrameId</code></a></td>
            <td><span data-ttu-id="057fe-395">ID de frame pour les éléments de propriétaire de frame.</span><span class="sxs-lookup"><span data-stu-id="057fe-395">Frame ID for frame owner elements.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-396">contentDocument</span><span class="sxs-lookup"><span data-stu-id="057fe-396">contentDocument</span></span> <br/> <i><span data-ttu-id="057fe-397">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-397">optional</span></span></i></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="057fe-398">Document de contenu pour les éléments de propriétaire de frame.</span><span class="sxs-lookup"><span data-stu-id="057fe-398">Content document for frame owner elements.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="057fe-399">isSVG</span><span class="sxs-lookup"><span data-stu-id="057fe-399">isSVG</span></span> <br/> <i><span data-ttu-id="057fe-400">facultatif</span><span class="sxs-lookup"><span data-stu-id="057fe-400">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="057fe-401">True si le nœud est SVG.</span><span class="sxs-lookup"><span data-stu-id="057fe-401">True if the node is SVG.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="backendnodeid"></a> <span data-ttu-id="057fe-402">BackendNodeId</span><span class="sxs-lookup"><span data-stu-id="057fe-402">BackendNodeId</span></span> `integer`

<span data-ttu-id="057fe-403">Identificateur de nœud DOM unique utilisé pour référencer un nœud qui n’a pas pu être envoyé au premier plan.</span><span class="sxs-lookup"><span data-stu-id="057fe-403">Unique DOM node identifier used to reference a node that may not have been pushed to the front-end.</span></span>

</p>

---

### <a name="pseudotype"></a> <span data-ttu-id="057fe-404">PseudoType</span><span class="sxs-lookup"><span data-stu-id="057fe-404">PseudoType</span></span> `string`

<span data-ttu-id="057fe-405">Type de pseudo-élément.</span><span class="sxs-lookup"><span data-stu-id="057fe-405">Pseudo element type.</span></span>

##### <span data-ttu-id="057fe-406">Valeurs autorisées</span><span class="sxs-lookup"><span data-stu-id="057fe-406">Allowed Values</span></span>
<span data-ttu-id="057fe-407">première ligne, première lettre avant, après, sélection</span><span class="sxs-lookup"><span data-stu-id="057fe-407">first-line, first-letter, before, after, selection</span></span>
</p>

---

## <span data-ttu-id="057fe-408">Dépendances</span><span class="sxs-lookup"><span data-stu-id="057fe-408">Dependencies</span></span>

[<span data-ttu-id="057fe-409">Runtime</span><span class="sxs-lookup"><span data-stu-id="057fe-409">Runtime</span></span>](runtime.md)
