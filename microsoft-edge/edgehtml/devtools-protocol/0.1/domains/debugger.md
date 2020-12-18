---
description: Référence de la version 0,1 (EdgeHTML) du protocole DevTools pour le domaine du débogueur. Le domaine du débogueur expose les fonctionnalités de débogage JavaScript. Elle permet de définir et de supprimer des points d’arrêt, de parcourir l’exécution, d’explorer les traces de pile, etc.
title: Debugger Domain-DevTools Protocol version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 12/16/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5160e6e69ec76f8c584f1bdb969464d805c7afa7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233250"
---
# <span data-ttu-id="5be61-105">Debugger Domain-DevTools Protocol version 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="5be61-105">Debugger Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  
  
<span data-ttu-id="5be61-106">Le domaine du débogueur expose les fonctionnalités de débogage JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5be61-106">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="5be61-107">Elle permet de définir et de supprimer des points d’arrêt, de parcourir l’exécution, d’explorer les traces de pile, etc.</span><span class="sxs-lookup"><span data-stu-id="5be61-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="5be61-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5be61-108">Methods</span></span>**](#methods) | <span data-ttu-id="5be61-109">[activer](#enable), [Désactiver](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [décalage](#stepover)automatique [, stepInto](#stepinto), [stepOut](#stepout), [suspendre](#pause), [reprendre](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions,](#setpauseonexceptions) [evaluateOnCallFrame](#evaluateoncallframe)et [setVariableValue](#setvariablevalue), setBlackboxPatterns [, msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue) [](#setblackboxpatterns)</span><span class="sxs-lookup"><span data-stu-id="5be61-109">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |
| [**<span data-ttu-id="5be61-110">Événements</span><span class="sxs-lookup"><span data-stu-id="5be61-110">Events</span></span>**](#events) | <span data-ttu-id="5be61-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), en [Pause](#paused), [reprise](#resumed)</span><span class="sxs-lookup"><span data-stu-id="5be61-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |
| [**<span data-ttu-id="5be61-112">Types</span><span class="sxs-lookup"><span data-stu-id="5be61-112">Types</span></span>**](#types) | <span data-ttu-id="5be61-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [scope](#scope)</span><span class="sxs-lookup"><span data-stu-id="5be61-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |
| [**<span data-ttu-id="5be61-114">Dépendances</span><span class="sxs-lookup"><span data-stu-id="5be61-114">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="5be61-115">Runtime</span><span class="sxs-lookup"><span data-stu-id="5be61-115">Runtime</span></span>](runtime.md) |
## <span data-ttu-id="5be61-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5be61-116">Methods</span></span>

### <span data-ttu-id="5be61-117">activer</span><span class="sxs-lookup"><span data-stu-id="5be61-117">enable</span></span>
<span data-ttu-id="5be61-118">Autorise le débogueur pour la page donnée.</span><span class="sxs-lookup"><span data-stu-id="5be61-118">Enables debugger for the given page.</span></span> <span data-ttu-id="5be61-119">Les clients ne doivent pas supposer que le débogage a été activé tant que le résultat de cette commande n’a pas été reçu.</span><span class="sxs-lookup"><span data-stu-id="5be61-119">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>


---

### <span data-ttu-id="5be61-120">désactiver </span><span class="sxs-lookup"><span data-stu-id="5be61-120">disable</span></span>
<span data-ttu-id="5be61-121">Désactive le débogueur pour une page donnée.</span><span class="sxs-lookup"><span data-stu-id="5be61-121">Disables debugger for given page.</span></span>


---

### <span data-ttu-id="5be61-122">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="5be61-122">getPossibleBreakpoints</span></span>
<span data-ttu-id="5be61-123">Renvoie les emplacements possibles pour le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5be61-123">Returns possible locations for breakpoint.</span></span> <span data-ttu-id="5be61-124">scriptId les emplacements de début et de fin doivent être identiques.</span><span class="sxs-lookup"><span data-stu-id="5be61-124">scriptId in start and end range locations should be the same.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-125">Parameters</span><span class="sxs-lookup"><span data-stu-id="5be61-125">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-126">start</span><span class="sxs-lookup"><span data-stu-id="5be61-126">start</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="5be61-127">Début de la plage pour rechercher des emplacements de point d’arrêt possibles dans.</span><span class="sxs-lookup"><span data-stu-id="5be61-127">Start of range to search possible breakpoint locations in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-128">terminer</span><span class="sxs-lookup"><span data-stu-id="5be61-128">end</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="5be61-129">Fin de plage pour rechercher des emplacements de point d’arrêt possibles (à l’exception de).</span><span class="sxs-lookup"><span data-stu-id="5be61-129">End of range to search possible breakpoint locations in (excluding).</span></span> <span data-ttu-id="5be61-130">En l’absence de spécification, la fin des scripts est utilisée en tant que fin de plage.</span><span class="sxs-lookup"><span data-stu-id="5be61-130">When not specified, end of scripts is used as end of range.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-131">Renvoie</span><span class="sxs-lookup"><span data-stu-id="5be61-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-132">régions</span><span class="sxs-lookup"><span data-stu-id="5be61-132">locations</span></span></td>
            <td><a href="#breaklocation"><code class="flyout">BreakLocation</code></a></td>
            <td><span data-ttu-id="5be61-133">Liste des emplacements de points d’arrêt possibles.</span><span class="sxs-lookup"><span data-stu-id="5be61-133">List of the possible breakpoint locations.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="5be61-134">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="5be61-134">setBreakpointsActive</span></span>
<span data-ttu-id="5be61-135">Active/désactive tous les points d’arrêt de la page.</span><span class="sxs-lookup"><span data-stu-id="5be61-135">Activates / deactivates all breakpoints on the page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-136">Parameters</span><span class="sxs-lookup"><span data-stu-id="5be61-136">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-137">active</span><span class="sxs-lookup"><span data-stu-id="5be61-137">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="5be61-138">Nouvelle valeur pour l’état actif de points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5be61-138">New value for breakpoints active state.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="5be61-139">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="5be61-139">setBreakpointByUrl</span></span>
<span data-ttu-id="5be61-140">Définit le point d’arrêt JavaScript à l’emplacement indiqué par URL ou expression Regex.</span><span class="sxs-lookup"><span data-stu-id="5be61-140">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span> <span data-ttu-id="5be61-141">Dès que cette commande est lancée, tous les scripts analysés existants disposent de points d’arrêt résolus et renvoyés dans <code>locations</code> propriété.</span><span class="sxs-lookup"><span data-stu-id="5be61-141">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in <code>locations</code> property.</span></span> <span data-ttu-id="5be61-142">La recherche de script correspondante entraînera davantage d' <code>breakpointResolved</code> événements consécutifs.</span><span class="sxs-lookup"><span data-stu-id="5be61-142">Further matching script parsing will result in subsequent <code>breakpointResolved</code> events issued.</span></span> <span data-ttu-id="5be61-143">Ce point d’arrêt logique survivrea les recharges de la page.</span><span class="sxs-lookup"><span data-stu-id="5be61-143">This logical breakpoint will survive page reloads.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-144">Parameters</span><span class="sxs-lookup"><span data-stu-id="5be61-144">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-145">lineNumber</span><span class="sxs-lookup"><span data-stu-id="5be61-145">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5be61-146">Numéro de ligne sur lequel définir le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5be61-146">Line number to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-147">url</span><span class="sxs-lookup"><span data-stu-id="5be61-147">url</span></span> <br/> <i><span data-ttu-id="5be61-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-148">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5be61-149">URL des ressources sur lesquelles définir le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5be61-149">URL of the resources to set breakpoint on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-150">urlRegex</span><span class="sxs-lookup"><span data-stu-id="5be61-150">urlRegex</span></span> <br/> <i><span data-ttu-id="5be61-151">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-151">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5be61-152">Modèle Regex pour les URL des ressources sur lesquelles définir des points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5be61-152">Regex pattern for the URLs of the resources to set breakpoints on.</span></span> <span data-ttu-id="5be61-153">La valeur <code>url</code> or <code>urlRegex</code> doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5be61-153">Either <code>url</code> or <code>urlRegex</code> must be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-154">columnNumber</span><span class="sxs-lookup"><span data-stu-id="5be61-154">columnNumber</span></span> <br/> <i><span data-ttu-id="5be61-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-155">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5be61-156">Décalage dans la ligne où définir le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5be61-156">Offset in the line to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-157">autant</span><span class="sxs-lookup"><span data-stu-id="5be61-157">condition</span></span> <br/> <i><span data-ttu-id="5be61-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-158">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5be61-159">Expression à utiliser comme condition de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5be61-159">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="5be61-160">Lorsque ce paramètre est spécifié, le débogueur s’arrêtera sur le point d’arrêt uniquement si cette expression a pour résultat la valeur vrai.</span><span class="sxs-lookup"><span data-stu-id="5be61-160">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-161">Renvoie</span><span class="sxs-lookup"><span data-stu-id="5be61-161">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-162">breakpointId</span><span class="sxs-lookup"><span data-stu-id="5be61-162">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="5be61-163">ID du point d’arrêt créé pour référence.</span><span class="sxs-lookup"><span data-stu-id="5be61-163">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-164">régions</span><span class="sxs-lookup"><span data-stu-id="5be61-164">locations</span></span></td>
            <td><a href="#location"><code class="flyout">Location[]</code></a></td>
            <td><span data-ttu-id="5be61-165">Liste des emplacements résolus par le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5be61-165">List of the locations this breakpoint resolved into upon addition.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="5be61-166">setBreakpoint</span><span class="sxs-lookup"><span data-stu-id="5be61-166">setBreakpoint</span></span>
<span data-ttu-id="5be61-167">Définit un point d’arrêt JavaScript à un emplacement donné.</span><span class="sxs-lookup"><span data-stu-id="5be61-167">Sets JavaScript breakpoint at a given location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-168">Parameters</span><span class="sxs-lookup"><span data-stu-id="5be61-168">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-169">ventilation</span><span class="sxs-lookup"><span data-stu-id="5be61-169">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="5be61-170">Emplacement dans lequel définir le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5be61-170">Location to set breakpoint in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-171">autant</span><span class="sxs-lookup"><span data-stu-id="5be61-171">condition</span></span> <br/> <i><span data-ttu-id="5be61-172">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-172">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5be61-173">Expression à utiliser comme condition de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5be61-173">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="5be61-174">Lorsque ce paramètre est spécifié, le débogueur s’arrêtera sur le point d’arrêt uniquement si cette expression a pour résultat la valeur vrai.</span><span class="sxs-lookup"><span data-stu-id="5be61-174">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-175">Renvoie</span><span class="sxs-lookup"><span data-stu-id="5be61-175">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-176">breakpointId</span><span class="sxs-lookup"><span data-stu-id="5be61-176">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="5be61-177">ID du point d’arrêt créé pour référence.</span><span class="sxs-lookup"><span data-stu-id="5be61-177">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-178">actualLocation</span><span class="sxs-lookup"><span data-stu-id="5be61-178">actualLocation</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="5be61-179">Emplacement dans lequel ce point d’arrêt a été résolu.</span><span class="sxs-lookup"><span data-stu-id="5be61-179">Location this breakpoint resolved into.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="5be61-180">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="5be61-180">removeBreakpoint</span></span>
<span data-ttu-id="5be61-181">Supprime le point d’arrêt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5be61-181">Removes JavaScript breakpoint.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-182">Parameters</span><span class="sxs-lookup"><span data-stu-id="5be61-182">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-183">breakpointId</span><span class="sxs-lookup"><span data-stu-id="5be61-183">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="5be61-184">3D</span><span class="sxs-lookup"><span data-stu-id="5be61-184">stepOver</span></span>
<span data-ttu-id="5be61-185">Étapes sur l’instruction.</span><span class="sxs-lookup"><span data-stu-id="5be61-185">Steps over the statement.</span></span>


---

### <span data-ttu-id="5be61-186">stepInto</span><span class="sxs-lookup"><span data-stu-id="5be61-186">stepInto</span></span>
<span data-ttu-id="5be61-187">Étapes dans l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="5be61-187">Steps into the function call.</span></span>


---

### <span data-ttu-id="5be61-188">stepOut</span><span class="sxs-lookup"><span data-stu-id="5be61-188">stepOut</span></span>
<span data-ttu-id="5be61-189">Étapes de l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="5be61-189">Steps out of the function call.</span></span>


---

### <span data-ttu-id="5be61-190">pause</span><span class="sxs-lookup"><span data-stu-id="5be61-190">pause</span></span>
<span data-ttu-id="5be61-191">S’arrête sur l’instruction JavaScript suivante.</span><span class="sxs-lookup"><span data-stu-id="5be61-191">Stops on the next JavaScript statement.</span></span>


---

### <span data-ttu-id="5be61-192">resume</span><span class="sxs-lookup"><span data-stu-id="5be61-192">resume</span></span>
<span data-ttu-id="5be61-193">Réactive l’exécution JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5be61-193">Resumes JavaScript execution.</span></span>


---

### <span data-ttu-id="5be61-194">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="5be61-194">getScriptSource</span></span>
<span data-ttu-id="5be61-195">Renvoie la source du script avec l’ID donné.</span><span class="sxs-lookup"><span data-stu-id="5be61-195">Returns source for the script with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-196">Parameters</span><span class="sxs-lookup"><span data-stu-id="5be61-196">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-197">scriptId</span><span class="sxs-lookup"><span data-stu-id="5be61-197">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="5be61-198">ID du script pour lequel obtenir la source.</span><span class="sxs-lookup"><span data-stu-id="5be61-198">Id of the script to get source for.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-199">Renvoie</span><span class="sxs-lookup"><span data-stu-id="5be61-199">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-200">scriptSource</span><span class="sxs-lookup"><span data-stu-id="5be61-200">scriptSource</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5be61-201">Source de script.</span><span class="sxs-lookup"><span data-stu-id="5be61-201">Script source.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="5be61-202">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="5be61-202">setPauseOnExceptions</span></span>
<span data-ttu-id="5be61-203">Définit une pause sur l’État exceptions.</span><span class="sxs-lookup"><span data-stu-id="5be61-203">Defines pause on exceptions state.</span></span> <span data-ttu-id="5be61-204">Peut être défini pour s’arrêter sur toutes les exceptions, ou aucune exception.</span><span class="sxs-lookup"><span data-stu-id="5be61-204">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span> <span data-ttu-id="5be61-205">Le point d’interruption initial est <code>none</code> .</span><span class="sxs-lookup"><span data-stu-id="5be61-205">Initial pause on exceptions state is <code>none</code>.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-206">Parameters</span><span class="sxs-lookup"><span data-stu-id="5be61-206">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-207">traité</span><span class="sxs-lookup"><span data-stu-id="5be61-207">state</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="5be61-208">Valeurs autorisées: aucun, non intercepté, tous</span><span class="sxs-lookup"><span data-stu-id="5be61-208">Allowed values: none, uncaught, all</span></span></i></td>
            <td><span data-ttu-id="5be61-209">Placez le pointeur sur le mode exceptions.</span><span class="sxs-lookup"><span data-stu-id="5be61-209">Pause on exceptions mode.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="5be61-210">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="5be61-210">evaluateOnCallFrame</span></span>
<span data-ttu-id="5be61-211">Évalue l’expression sur un cadre d’appel donné.</span><span class="sxs-lookup"><span data-stu-id="5be61-211">Evaluates expression on a given call frame.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-212">Parameters</span><span class="sxs-lookup"><span data-stu-id="5be61-212">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-213">callFrameId</span><span class="sxs-lookup"><span data-stu-id="5be61-213">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="5be61-214">Identifiant de l’identification de l’appel.</span><span class="sxs-lookup"><span data-stu-id="5be61-214">Call frame identifier to evaluate on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-215">termes</span><span class="sxs-lookup"><span data-stu-id="5be61-215">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5be61-216">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="5be61-216">Expression to evaluate.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-217">Renvoie</span><span class="sxs-lookup"><span data-stu-id="5be61-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-218">provoqué</span><span class="sxs-lookup"><span data-stu-id="5be61-218">result</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="5be61-219">Wrapper d’objet pour le résultat d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="5be61-219">Object wrapper for the evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="5be61-220">setVariableValue</span><span class="sxs-lookup"><span data-stu-id="5be61-220">setVariableValue</span></span>
<span data-ttu-id="5be61-221">Change la valeur de la variable dans un callframe.</span><span class="sxs-lookup"><span data-stu-id="5be61-221">Changes value of variable in a callframe.</span></span> <span data-ttu-id="5be61-222">Les étendues basées sur les objets ne sont pas prises en charge et doivent être mutées manuellement.</span><span class="sxs-lookup"><span data-stu-id="5be61-222">Object-based scopes are not supported and must be mutated manually.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-223">Parameters</span><span class="sxs-lookup"><span data-stu-id="5be61-223">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-224">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="5be61-224">scopeNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5be61-225">un nombre d’étendues égal à zéro tel qu’il apparaît dans la chaîne d’étendue.</span><span class="sxs-lookup"><span data-stu-id="5be61-225">0-based number of scope as was listed in scope chain.</span></span> <span data-ttu-id="5be61-226">Seuls les types d’étendue’local', de fermeture et de capture sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="5be61-226">Only 'local', 'closure' and 'catch' scope types are allowed.</span></span> <span data-ttu-id="5be61-227">Les autres étendues peuvent être manipulées manuellement.</span><span class="sxs-lookup"><span data-stu-id="5be61-227">Other scopes could be manipulated manually.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-228">NomVariable</span><span class="sxs-lookup"><span data-stu-id="5be61-228">variableName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5be61-229">Nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="5be61-229">Variable name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-230">NouvelleValeur</span><span class="sxs-lookup"><span data-stu-id="5be61-230">newValue</span></span></td>
            <td><a href="runtime.md#callargument"><code class="flyout">Runtime.CallArgument</code></a></td>
            <td><span data-ttu-id="5be61-231">Valeur de la nouvelle variable.</span><span class="sxs-lookup"><span data-stu-id="5be61-231">New variable value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-232">callFrameId</span><span class="sxs-lookup"><span data-stu-id="5be61-232">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="5be61-233">ID de callframe qui contient la variable.</span><span class="sxs-lookup"><span data-stu-id="5be61-233">Id of callframe that holds variable.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="5be61-234">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="5be61-234">setBlackboxPatterns</span></span>
<span><b><span data-ttu-id="5be61-235">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="5be61-235">Experimental.</span></span> </b></span><span data-ttu-id="5be61-236">Remplacer les modèles de Blackbox</span><span class="sxs-lookup"><span data-stu-id="5be61-236">Replace previous blackbox patterns with passed ones.</span></span> <span data-ttu-id="5be61-237">Force le serveur principal à ignorer l’étape/la suspension dans les scripts avec une URL qui correspond à l’un des modèles.</span><span class="sxs-lookup"><span data-stu-id="5be61-237">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span> <span data-ttu-id="5be61-238">Le débogueur tente de quitter le script Blackbox en exécutant plusieurs fois «étape», ce qui a pour fin en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="5be61-238">The debugger will try to leave blackboxed script by performing 'step in' several times, finally resorting to 'step out' if unsuccessful.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-239">Parameters</span><span class="sxs-lookup"><span data-stu-id="5be61-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-240">masques</span><span class="sxs-lookup"><span data-stu-id="5be61-240">patterns</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="5be61-241">Tableau d’regexps qui seront utilisés pour vérifier l’URL du script pour l’État Blackbox.</span><span class="sxs-lookup"><span data-stu-id="5be61-241">Array of regexps that will be used to check script url for blackbox state.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="5be61-242">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="5be61-242">msSetDebuggerPropertyValue</span></span>
<span><b><span data-ttu-id="5be61-243">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="5be61-243">Experimental.</span></span> </b></span><span data-ttu-id="5be61-244">Microsoft: définit la propriété Debugger spécifiée sur la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5be61-244">Microsoft: Sets the specified debugger property to the specified value.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-245">Parameters</span><span class="sxs-lookup"><span data-stu-id="5be61-245">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-246">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="5be61-246">debuggerPropertyId</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5be61-247">Microsoft: ID de propriété (par exemple, msDebuggerPropertyId) à définir.</span><span class="sxs-lookup"><span data-stu-id="5be61-247">Microsoft: The property id (i.e. msDebuggerPropertyId) to set.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-248">NouvelleValeur</span><span class="sxs-lookup"><span data-stu-id="5be61-248">newValue</span></span></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="5be61-249">Événements</span><span class="sxs-lookup"><span data-stu-id="5be61-249">Events</span></span>

### <span data-ttu-id="5be61-250">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="5be61-250">scriptParsed</span></span>
<span data-ttu-id="5be61-251">Déclenché lorsque le script est analysé.</span><span class="sxs-lookup"><span data-stu-id="5be61-251">Fired when the script is parsed.</span></span> <span data-ttu-id="5be61-252">Cet événement est également déclenché pour tous les scripts connus et non perçus lors de l’activation du débogueur.</span><span class="sxs-lookup"><span data-stu-id="5be61-252">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-253">Parameters</span><span class="sxs-lookup"><span data-stu-id="5be61-253">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-254">scriptId</span><span class="sxs-lookup"><span data-stu-id="5be61-254">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="5be61-255">Identificateur du script analysé.</span><span class="sxs-lookup"><span data-stu-id="5be61-255">Identifier of the script parsed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-256">url</span><span class="sxs-lookup"><span data-stu-id="5be61-256">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5be61-257">URL ou nom du script analysé (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="5be61-257">URL or name of the script parsed (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-258">startLine</span><span class="sxs-lookup"><span data-stu-id="5be61-258">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5be61-259">Décalage de ligne du script dans la ressource avec l’URL donnée (pour les balises de script).</span><span class="sxs-lookup"><span data-stu-id="5be61-259">Line offset of the script within the resource with given URL (for script tags).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-260">ColonneDébut</span><span class="sxs-lookup"><span data-stu-id="5be61-260">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5be61-261">Décalage de colonne du script dans la ressource avec l’URL donnée.</span><span class="sxs-lookup"><span data-stu-id="5be61-261">Column offset of the script within the resource with given URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-262">lignefin</span><span class="sxs-lookup"><span data-stu-id="5be61-262">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5be61-263">Dernière ligne du script.</span><span class="sxs-lookup"><span data-stu-id="5be61-263">Last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-264">ColonneFin</span><span class="sxs-lookup"><span data-stu-id="5be61-264">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5be61-265">Longueur de la dernière ligne du script.</span><span class="sxs-lookup"><span data-stu-id="5be61-265">Length of the last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-266">executionContextId</span><span class="sxs-lookup"><span data-stu-id="5be61-266">executionContextId</span></span></td>
            <td><a href="runtime.md#executioncontextid"><code class="flyout">Runtime.ExecutionContextId</code></a></td>
            <td><span data-ttu-id="5be61-267">Spécifie le contexte de création de script.</span><span class="sxs-lookup"><span data-stu-id="5be61-267">Specifies script creation context.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-268">sourceMapURL</span><span class="sxs-lookup"><span data-stu-id="5be61-268">sourceMapURL</span></span> <br/> <i><span data-ttu-id="5be61-269">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-269">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5be61-270">URL du mappage source associé au script (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="5be61-270">URL of source map associated with script (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-271">nombre</span><span class="sxs-lookup"><span data-stu-id="5be61-271">length</span></span> <br/> <i><span data-ttu-id="5be61-272">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-272">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="5be61-273">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="5be61-273">Experimental.</span></span> </b></span><span data-ttu-id="5be61-274">Cette longueur de script.</span><span class="sxs-lookup"><span data-stu-id="5be61-274">This script length.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-275">msParentId</span><span class="sxs-lookup"><span data-stu-id="5be61-275">msParentId</span></span> <br/> <i><span data-ttu-id="5be61-276">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-276">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="5be61-277">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="5be61-277">Experimental.</span></span> </b></span><span data-ttu-id="5be61-278">Il s’agit de l’ID de document parent.</span><span class="sxs-lookup"><span data-stu-id="5be61-278">This is the parent document ID.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-279">msMimeType</span><span class="sxs-lookup"><span data-stu-id="5be61-279">msMimeType</span></span> <br/> <i><span data-ttu-id="5be61-280">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-280">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="5be61-281">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="5be61-281">Experimental.</span></span> </b></span><span data-ttu-id="5be61-282">Il s’agit du type MIME.</span><span class="sxs-lookup"><span data-stu-id="5be61-282">This is the mime type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-283">msIsDynamicCode</span><span class="sxs-lookup"><span data-stu-id="5be61-283">msIsDynamicCode</span></span> <br/> <i><span data-ttu-id="5be61-284">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-284">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="5be61-285">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="5be61-285">Experimental.</span></span> </b></span><span data-ttu-id="5be61-286">Cela indique s’il s’agit d’un code dynamique.</span><span class="sxs-lookup"><span data-stu-id="5be61-286">This indicates whether it is dynamic code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-287">msLongDocumentId</span><span class="sxs-lookup"><span data-stu-id="5be61-287">msLongDocumentId</span></span> <br/> <i><span data-ttu-id="5be61-288">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-288">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="5be61-289">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="5be61-289">Experimental.</span></span> </b></span><span data-ttu-id="5be61-290">Il s’agit de l’ID de document long.</span><span class="sxs-lookup"><span data-stu-id="5be61-290">This is the long document ID.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="5be61-291">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="5be61-291">breakpointResolved</span></span>
<span data-ttu-id="5be61-292">Déclenché lorsque le point d’arrêt est résolu en un script et un emplacement réels.</span><span class="sxs-lookup"><span data-stu-id="5be61-292">Fired when breakpoint is resolved to an actual script and location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-293">Parameters</span><span class="sxs-lookup"><span data-stu-id="5be61-293">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-294">breakpointId</span><span class="sxs-lookup"><span data-stu-id="5be61-294">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="5be61-295">Identificateur unique de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5be61-295">Breakpoint unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-296">ventilation</span><span class="sxs-lookup"><span data-stu-id="5be61-296">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="5be61-297">Emplacement du point d’arrêt réel.</span><span class="sxs-lookup"><span data-stu-id="5be61-297">Actual breakpoint location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-298">msLength</span><span class="sxs-lookup"><span data-stu-id="5be61-298">msLength</span></span> <br/> <i><span data-ttu-id="5be61-299">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-299">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="5be61-300">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="5be61-300">Experimental.</span></span> </b></span><span data-ttu-id="5be61-301">Microsoft: longueur du code (par exemple, nombre de caractères) à l’emplacement du point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5be61-301">Microsoft: Length of code (i.e. number of characters) at the breakpoint location.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="5be61-302">en pause</span><span class="sxs-lookup"><span data-stu-id="5be61-302">paused</span></span>
<span data-ttu-id="5be61-303">Déclenché lorsque les débogueurs s’interrompent pour un point d’arrêt ou une exception.</span><span class="sxs-lookup"><span data-stu-id="5be61-303">Fired when the debuggers breaks for a breakpoint or exception.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-304">Parameters</span><span class="sxs-lookup"><span data-stu-id="5be61-304">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-305">callFrames</span><span class="sxs-lookup"><span data-stu-id="5be61-305">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="5be61-306">Pile d’appels sur laquelle le débogueur a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="5be61-306">Call stack the debugger stopped on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-307">tient</span><span class="sxs-lookup"><span data-stu-id="5be61-307">reason</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="5be61-308">Valeurs autorisées: point d’arrêt, étape, exception, autres</span><span class="sxs-lookup"><span data-stu-id="5be61-308">Allowed values: breakpoint, step, exception, other</span></span></i></td>
            <td><span data-ttu-id="5be61-309">Raison du pause.</span><span class="sxs-lookup"><span data-stu-id="5be61-309">Pause reason.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-310">data</span><span class="sxs-lookup"><span data-stu-id="5be61-310">data</span></span> <br/> <i><span data-ttu-id="5be61-311">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-311">optional</span></span></i></td>
            <td><code class="flyout">object</code></td>
            <td><span data-ttu-id="5be61-312">Objet contenant des propriétés auxiliaires spécifiques de rupture.</span><span class="sxs-lookup"><span data-stu-id="5be61-312">Object containing break-specific auxiliary properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-313">hitBreakpoints</span><span class="sxs-lookup"><span data-stu-id="5be61-313">hitBreakpoints</span></span> <br/> <i><span data-ttu-id="5be61-314">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-314">optional</span></span></i></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="5be61-315">ID d’arrêt du positionnement</span><span class="sxs-lookup"><span data-stu-id="5be61-315">Hit breakpoints IDs</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="5be61-316">reprend</span><span class="sxs-lookup"><span data-stu-id="5be61-316">resumed</span></span>
<span data-ttu-id="5be61-317">Déclenché lorsque le débogueur reprend l’exécution.</span><span class="sxs-lookup"><span data-stu-id="5be61-317">Fired when the debugger resumes execution.</span></span>


---

## <span data-ttu-id="5be61-318">Types</span><span class="sxs-lookup"><span data-stu-id="5be61-318">Types</span></span>

### <a name="breakpointid"></a> <span data-ttu-id="5be61-319">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="5be61-319">BreakpointId</span></span> `string`

<span data-ttu-id="5be61-320">Identificateur de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5be61-320">Breakpoint identifier.</span></span>


---

### <a name="callframeid"></a> <span data-ttu-id="5be61-321">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="5be61-321">CallFrameId</span></span> `string`

<span data-ttu-id="5be61-322">Identificateur d’image d’appel.</span><span class="sxs-lookup"><span data-stu-id="5be61-322">Call frame identifier.</span></span>


---

### <a name="location"></a> <span data-ttu-id="5be61-323">Location</span><span class="sxs-lookup"><span data-stu-id="5be61-323">Location</span></span> `object`

<span data-ttu-id="5be61-324">Emplacement dans le code source.</span><span class="sxs-lookup"><span data-stu-id="5be61-324">Location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-325">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5be61-325">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-326">scriptId</span><span class="sxs-lookup"><span data-stu-id="5be61-326">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="5be61-327">ID de script tel qu’indiqué dans le <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="5be61-327">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-328">lineNumber</span><span class="sxs-lookup"><span data-stu-id="5be61-328">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5be61-329">Numéro de ligne dans le script (0).</span><span class="sxs-lookup"><span data-stu-id="5be61-329">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-330">columnNumber</span><span class="sxs-lookup"><span data-stu-id="5be61-330">columnNumber</span></span> <br/> <i><span data-ttu-id="5be61-331">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-331">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5be61-332">Numéro de colonne dans le script (0).</span><span class="sxs-lookup"><span data-stu-id="5be61-332">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-333">msLength</span><span class="sxs-lookup"><span data-stu-id="5be61-333">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5be61-334">Microsoft: longueur de code (par exemple, nombre de caractères) à cette image d’appel.</span><span class="sxs-lookup"><span data-stu-id="5be61-334">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="breaklocation"></a> <span data-ttu-id="5be61-335">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="5be61-335">BreakLocation</span></span> `object`

<span data-ttu-id="5be61-336">Emplacement d’arrêt dans le code source.</span><span class="sxs-lookup"><span data-stu-id="5be61-336">Break location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-337">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5be61-337">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-338">scriptId</span><span class="sxs-lookup"><span data-stu-id="5be61-338">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="5be61-339">ID de script tel qu’indiqué dans le <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="5be61-339">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-340">lineNumber</span><span class="sxs-lookup"><span data-stu-id="5be61-340">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5be61-341">Numéro de ligne dans le script (0).</span><span class="sxs-lookup"><span data-stu-id="5be61-341">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-342">columnNumber</span><span class="sxs-lookup"><span data-stu-id="5be61-342">columnNumber</span></span> <br/> <i><span data-ttu-id="5be61-343">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-343">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5be61-344">Numéro de colonne dans le script (0).</span><span class="sxs-lookup"><span data-stu-id="5be61-344">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-345">msLength</span><span class="sxs-lookup"><span data-stu-id="5be61-345">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5be61-346">Microsoft: longueur de code (par exemple, nombre de caractères) à cette image d’appel.</span><span class="sxs-lookup"><span data-stu-id="5be61-346">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-347">type</span><span class="sxs-lookup"><span data-stu-id="5be61-347">type</span></span> <br/> <i><span data-ttu-id="5be61-348">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-348">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5be61-349">Valeurs autorisées: debuggerStatement, Call, retour.</span><span class="sxs-lookup"><span data-stu-id="5be61-349">Allowed values: debuggerStatement, call, return.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="callframe"></a> <span data-ttu-id="5be61-350">CallFrame</span><span class="sxs-lookup"><span data-stu-id="5be61-350">CallFrame</span></span> `object`

<span data-ttu-id="5be61-351">Image d’un appel JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5be61-351">JavaScript call frame.</span></span> <span data-ttu-id="5be61-352">Tableau de trames d’appel qui forment la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="5be61-352">Array of call frames form the call stack.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-353">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5be61-353">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-354">callFrameId</span><span class="sxs-lookup"><span data-stu-id="5be61-354">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="5be61-355">Identificateur d’image d’appel.</span><span class="sxs-lookup"><span data-stu-id="5be61-355">Call frame identifier.</span></span> <span data-ttu-id="5be61-356">Cet identificateur est valide uniquement lorsque le débogueur est en pause.</span><span class="sxs-lookup"><span data-stu-id="5be61-356">This identifier is only valid while the debugger is paused.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-357">Admises</span><span class="sxs-lookup"><span data-stu-id="5be61-357">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5be61-358">Nom de la fonction JavaScript appelée sur cette image d’appel.</span><span class="sxs-lookup"><span data-stu-id="5be61-358">Name of the JavaScript function called on this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-359">functionLocation</span><span class="sxs-lookup"><span data-stu-id="5be61-359">functionLocation</span></span> <br/> <i><span data-ttu-id="5be61-360">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-360">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span><b><span data-ttu-id="5be61-361">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="5be61-361">Experimental.</span></span> </b></span><span data-ttu-id="5be61-362">Emplacement dans le code source.</span><span class="sxs-lookup"><span data-stu-id="5be61-362">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-363">ventilation</span><span class="sxs-lookup"><span data-stu-id="5be61-363">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="5be61-364">Emplacement dans le code source.</span><span class="sxs-lookup"><span data-stu-id="5be61-364">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-365">url</span><span class="sxs-lookup"><span data-stu-id="5be61-365">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5be61-366">Nom ou URL du script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5be61-366">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-367">scopeChain</span><span class="sxs-lookup"><span data-stu-id="5be61-367">scopeChain</span></span></td>
            <td><a href="#scope"><code class="flyout">Scope[]</code></a></td>
            <td><span data-ttu-id="5be61-368">Chaîne d’étendue pour cette image d’appel.</span><span class="sxs-lookup"><span data-stu-id="5be61-368">Scope chain for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-369">elle</span><span class="sxs-lookup"><span data-stu-id="5be61-369">this</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><code>this</code> <span data-ttu-id="5be61-370">objet pour cette image d’appel.</span><span class="sxs-lookup"><span data-stu-id="5be61-370">object for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-371">returnValue</span><span class="sxs-lookup"><span data-stu-id="5be61-371">returnValue</span></span> <br/> <i><span data-ttu-id="5be61-372">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-372">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="5be61-373">Valeur renvoyée, si la fonction est à la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="5be61-373">The value being returned, if the function is at return point.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="scope"></a> <span data-ttu-id="5be61-374">Étendue</span><span class="sxs-lookup"><span data-stu-id="5be61-374">Scope</span></span> `object`

<span data-ttu-id="5be61-375">Description de l’étendue.</span><span class="sxs-lookup"><span data-stu-id="5be61-375">Scope description.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5be61-376">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5be61-376">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5be61-377">type</span><span class="sxs-lookup"><span data-stu-id="5be61-377">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="5be61-378">Valeurs autorisées: global, local, avec, fermeture, catch, bloc, script, Eval, module</span><span class="sxs-lookup"><span data-stu-id="5be61-378">Allowed values: global, local, with, closure, catch, block, script, eval, module</span></span></i></td>
            <td><span data-ttu-id="5be61-379">Type d’étendue.</span><span class="sxs-lookup"><span data-stu-id="5be61-379">Scope type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-380">object</span><span class="sxs-lookup"><span data-stu-id="5be61-380">object</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="5be61-381">Objet représentant la portée.</span><span class="sxs-lookup"><span data-stu-id="5be61-381">Object representing the scope.</span></span> <span data-ttu-id="5be61-382">Pour <code>global</code> les <code>with</code> étendues, il s’agit de l’objet réel; pour les autres étendues, il s’agit d’un objet temporaire artificiel qui énumère les variables d’étendue en tant que propriétés.</span><span class="sxs-lookup"><span data-stu-id="5be61-382">For <code>global</code> and <code>with</code> scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-383">name</span><span class="sxs-lookup"><span data-stu-id="5be61-383">name</span></span> <br/> <i><span data-ttu-id="5be61-384">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-384">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-385">startLocation</span><span class="sxs-lookup"><span data-stu-id="5be61-385">startLocation</span></span> <br/> <i><span data-ttu-id="5be61-386">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-386">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="5be61-387">Emplacement dans le code source où l’étendue commence</span><span class="sxs-lookup"><span data-stu-id="5be61-387">Location in the source code where scope starts</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5be61-388">endLocation</span><span class="sxs-lookup"><span data-stu-id="5be61-388">endLocation</span></span> <br/> <i><span data-ttu-id="5be61-389">facultatif</span><span class="sxs-lookup"><span data-stu-id="5be61-389">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="5be61-390">Emplacement dans le code source où l’étendue se termine</span><span class="sxs-lookup"><span data-stu-id="5be61-390">Location in the source code where scope ends</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="5be61-391">Dépendances</span><span class="sxs-lookup"><span data-stu-id="5be61-391">Dependencies</span></span>

[<span data-ttu-id="5be61-392">Runtime</span><span class="sxs-lookup"><span data-stu-id="5be61-392">Runtime</span></span>](runtime.md)
