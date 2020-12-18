---
description: Référence de la version 0,2 (EdgeHTML) du protocole DevTools pour le domaine du débogueur. Le domaine du débogueur expose les fonctionnalités de débogage JavaScript. Elle permet de définir et de supprimer des points d’arrêt, de parcourir l’exécution, d’explorer les traces de pile, etc.
title: Debugger Domain-DevTools Protocol version 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 24571b3a32acf085dd9ccbd641b1e5b06b3b9504
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232862"
---
# <span data-ttu-id="a795b-105">Debugger Domain-DevTools Protocol version 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="a795b-105">Debugger Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="a795b-106">Le domaine du débogueur expose les fonctionnalités de débogage JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a795b-106">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="a795b-107">Elle permet de définir et de supprimer des points d’arrêt, de parcourir l’exécution, d’explorer les traces de pile, etc.</span><span class="sxs-lookup"><span data-stu-id="a795b-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="a795b-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a795b-108">Methods</span></span>**](#methods) | <span data-ttu-id="a795b-109">[activer](#enable), [Désactiver](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [décalage](#stepover)automatique [, stepInto](#stepinto), [stepOut](#stepout), [suspendre](#pause), [reprendre](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions,](#setpauseonexceptions) [evaluateOnCallFrame](#evaluateoncallframe)et [setVariableValue](#setvariablevalue), setBlackboxPatterns [, msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue) [](#setblackboxpatterns)</span><span class="sxs-lookup"><span data-stu-id="a795b-109">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |
| [**<span data-ttu-id="a795b-110">Événements</span><span class="sxs-lookup"><span data-stu-id="a795b-110">Events</span></span>**](#events) | <span data-ttu-id="a795b-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), en [Pause](#paused), [reprise](#resumed)</span><span class="sxs-lookup"><span data-stu-id="a795b-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |
| [**<span data-ttu-id="a795b-112">Types</span><span class="sxs-lookup"><span data-stu-id="a795b-112">Types</span></span>**](#types) | <span data-ttu-id="a795b-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [scope](#scope)</span><span class="sxs-lookup"><span data-stu-id="a795b-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |
| [**<span data-ttu-id="a795b-114">Dépendances</span><span class="sxs-lookup"><span data-stu-id="a795b-114">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="a795b-115">Runtime</span><span class="sxs-lookup"><span data-stu-id="a795b-115">Runtime</span></span>](runtime.md) |
## <span data-ttu-id="a795b-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a795b-116">Methods</span></span>

### <span data-ttu-id="a795b-117">activer</span><span class="sxs-lookup"><span data-stu-id="a795b-117">enable</span></span>
<span data-ttu-id="a795b-118">Autorise le débogueur pour la page donnée.</span><span class="sxs-lookup"><span data-stu-id="a795b-118">Enables debugger for the given page.</span></span> <span data-ttu-id="a795b-119">Les clients ne doivent pas supposer que le débogage a été activé tant que le résultat de cette commande n’a pas été reçu.</span><span class="sxs-lookup"><span data-stu-id="a795b-119">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>

</p>

---

### <span data-ttu-id="a795b-120">désactiver </span><span class="sxs-lookup"><span data-stu-id="a795b-120">disable</span></span>
<span data-ttu-id="a795b-121">Désactive le débogueur pour une page donnée.</span><span class="sxs-lookup"><span data-stu-id="a795b-121">Disables debugger for given page.</span></span>

</p>

---

### <span data-ttu-id="a795b-122">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="a795b-122">getPossibleBreakpoints</span></span>
<span data-ttu-id="a795b-123">Renvoie les emplacements possibles pour le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a795b-123">Returns possible locations for breakpoint.</span></span> <span data-ttu-id="a795b-124">scriptId les emplacements de début et de fin doivent être identiques.</span><span class="sxs-lookup"><span data-stu-id="a795b-124">scriptId in start and end range locations should be the same.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-125">Parameters</span><span class="sxs-lookup"><span data-stu-id="a795b-125">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-126">start</span><span class="sxs-lookup"><span data-stu-id="a795b-126">start</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="a795b-127">Début de la plage pour rechercher des emplacements de point d’arrêt possibles dans.</span><span class="sxs-lookup"><span data-stu-id="a795b-127">Start of range to search possible breakpoint locations in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-128">terminer</span><span class="sxs-lookup"><span data-stu-id="a795b-128">end</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="a795b-129">Fin de plage pour rechercher des emplacements de point d’arrêt possibles (à l’exception de).</span><span class="sxs-lookup"><span data-stu-id="a795b-129">End of range to search possible breakpoint locations in (excluding).</span></span> <span data-ttu-id="a795b-130">En l’absence de spécification, la fin des scripts est utilisée en tant que fin de plage.</span><span class="sxs-lookup"><span data-stu-id="a795b-130">When not specified, end of scripts is used as end of range.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-131">Renvoie</span><span class="sxs-lookup"><span data-stu-id="a795b-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-132">régions</span><span class="sxs-lookup"><span data-stu-id="a795b-132">locations</span></span></td>
            <td><a href="#breaklocation"><code class="flyout">BreakLocation</code></a></td>
            <td><span data-ttu-id="a795b-133">Liste des emplacements de points d’arrêt possibles.</span><span class="sxs-lookup"><span data-stu-id="a795b-133">List of the possible breakpoint locations.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a795b-134">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="a795b-134">setBreakpointsActive</span></span>
<span data-ttu-id="a795b-135">Active/désactive tous les points d’arrêt de la page.</span><span class="sxs-lookup"><span data-stu-id="a795b-135">Activates / deactivates all breakpoints on the page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-136">Parameters</span><span class="sxs-lookup"><span data-stu-id="a795b-136">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-137">active</span><span class="sxs-lookup"><span data-stu-id="a795b-137">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="a795b-138">Nouvelle valeur pour l’état actif de points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a795b-138">New value for breakpoints active state.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a795b-139">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="a795b-139">setBreakpointByUrl</span></span>
<span data-ttu-id="a795b-140">Définit le point d’arrêt JavaScript à l’emplacement indiqué par URL ou expression Regex.</span><span class="sxs-lookup"><span data-stu-id="a795b-140">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span> <span data-ttu-id="a795b-141">Dès que cette commande est lancée, tous les scripts analysés existants disposent de points d’arrêt résolus et renvoyés dans <code>locations</code> propriété.</span><span class="sxs-lookup"><span data-stu-id="a795b-141">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in <code>locations</code> property.</span></span> <span data-ttu-id="a795b-142">La recherche de script correspondante entraînera davantage d' <code>breakpointResolved</code> événements consécutifs.</span><span class="sxs-lookup"><span data-stu-id="a795b-142">Further matching script parsing will result in subsequent <code>breakpointResolved</code> events issued.</span></span> <span data-ttu-id="a795b-143">Ce point d’arrêt logique survivrea les recharges de la page.</span><span class="sxs-lookup"><span data-stu-id="a795b-143">This logical breakpoint will survive page reloads.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-144">Parameters</span><span class="sxs-lookup"><span data-stu-id="a795b-144">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-145">lineNumber</span><span class="sxs-lookup"><span data-stu-id="a795b-145">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="a795b-146">Numéro de ligne sur lequel définir le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a795b-146">Line number to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-147">url</span><span class="sxs-lookup"><span data-stu-id="a795b-147">url</span></span> <br/> <i><span data-ttu-id="a795b-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-148">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a795b-149">URL des ressources sur lesquelles définir le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a795b-149">URL of the resources to set breakpoint on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-150">urlRegex</span><span class="sxs-lookup"><span data-stu-id="a795b-150">urlRegex</span></span> <br/> <i><span data-ttu-id="a795b-151">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-151">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a795b-152">Modèle Regex pour les URL des ressources sur lesquelles définir des points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a795b-152">Regex pattern for the URLs of the resources to set breakpoints on.</span></span> <span data-ttu-id="a795b-153">La valeur <code>url</code> or <code>urlRegex</code> doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a795b-153">Either <code>url</code> or <code>urlRegex</code> must be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-154">columnNumber</span><span class="sxs-lookup"><span data-stu-id="a795b-154">columnNumber</span></span> <br/> <i><span data-ttu-id="a795b-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-155">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="a795b-156">Décalage dans la ligne où définir le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a795b-156">Offset in the line to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-157">autant</span><span class="sxs-lookup"><span data-stu-id="a795b-157">condition</span></span> <br/> <i><span data-ttu-id="a795b-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-158">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a795b-159">Expression à utiliser comme condition de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a795b-159">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="a795b-160">Lorsque ce paramètre est spécifié, le débogueur s’arrêtera sur le point d’arrêt uniquement si cette expression a pour résultat la valeur vrai.</span><span class="sxs-lookup"><span data-stu-id="a795b-160">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-161">Renvoie</span><span class="sxs-lookup"><span data-stu-id="a795b-161">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-162">breakpointId</span><span class="sxs-lookup"><span data-stu-id="a795b-162">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="a795b-163">ID du point d’arrêt créé pour référence.</span><span class="sxs-lookup"><span data-stu-id="a795b-163">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-164">régions</span><span class="sxs-lookup"><span data-stu-id="a795b-164">locations</span></span></td>
            <td><a href="#location"><code class="flyout">Location[]</code></a></td>
            <td><span data-ttu-id="a795b-165">Liste des emplacements résolus par le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a795b-165">List of the locations this breakpoint resolved into upon addition.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a795b-166">setBreakpoint</span><span class="sxs-lookup"><span data-stu-id="a795b-166">setBreakpoint</span></span>
<span data-ttu-id="a795b-167">Définit un point d’arrêt JavaScript à un emplacement donné.</span><span class="sxs-lookup"><span data-stu-id="a795b-167">Sets JavaScript breakpoint at a given location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-168">Parameters</span><span class="sxs-lookup"><span data-stu-id="a795b-168">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-169">ventilation</span><span class="sxs-lookup"><span data-stu-id="a795b-169">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="a795b-170">Emplacement dans lequel définir le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a795b-170">Location to set breakpoint in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-171">autant</span><span class="sxs-lookup"><span data-stu-id="a795b-171">condition</span></span> <br/> <i><span data-ttu-id="a795b-172">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-172">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a795b-173">Expression à utiliser comme condition de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a795b-173">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="a795b-174">Lorsque ce paramètre est spécifié, le débogueur s’arrêtera sur le point d’arrêt uniquement si cette expression a pour résultat la valeur vrai.</span><span class="sxs-lookup"><span data-stu-id="a795b-174">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-175">Renvoie</span><span class="sxs-lookup"><span data-stu-id="a795b-175">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-176">breakpointId</span><span class="sxs-lookup"><span data-stu-id="a795b-176">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="a795b-177">ID du point d’arrêt créé pour référence.</span><span class="sxs-lookup"><span data-stu-id="a795b-177">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-178">actualLocation</span><span class="sxs-lookup"><span data-stu-id="a795b-178">actualLocation</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="a795b-179">Emplacement dans lequel ce point d’arrêt a été résolu.</span><span class="sxs-lookup"><span data-stu-id="a795b-179">Location this breakpoint resolved into.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a795b-180">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="a795b-180">removeBreakpoint</span></span>
<span data-ttu-id="a795b-181">Supprime le point d’arrêt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a795b-181">Removes JavaScript breakpoint.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-182">Parameters</span><span class="sxs-lookup"><span data-stu-id="a795b-182">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-183">breakpointId</span><span class="sxs-lookup"><span data-stu-id="a795b-183">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a795b-184">3D</span><span class="sxs-lookup"><span data-stu-id="a795b-184">stepOver</span></span>
<span data-ttu-id="a795b-185">Étapes sur l’instruction.</span><span class="sxs-lookup"><span data-stu-id="a795b-185">Steps over the statement.</span></span>

</p>

---

### <span data-ttu-id="a795b-186">stepInto</span><span class="sxs-lookup"><span data-stu-id="a795b-186">stepInto</span></span>
<span data-ttu-id="a795b-187">Étapes dans l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="a795b-187">Steps into the function call.</span></span>

</p>

---

### <span data-ttu-id="a795b-188">stepOut</span><span class="sxs-lookup"><span data-stu-id="a795b-188">stepOut</span></span>
<span data-ttu-id="a795b-189">Étapes de l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="a795b-189">Steps out of the function call.</span></span>

</p>

---

### <span data-ttu-id="a795b-190">pause</span><span class="sxs-lookup"><span data-stu-id="a795b-190">pause</span></span>
<span data-ttu-id="a795b-191">S’arrête sur l’instruction JavaScript suivante.</span><span class="sxs-lookup"><span data-stu-id="a795b-191">Stops on the next JavaScript statement.</span></span>

</p>

---

### <span data-ttu-id="a795b-192">resume</span><span class="sxs-lookup"><span data-stu-id="a795b-192">resume</span></span>
<span data-ttu-id="a795b-193">Réactive l’exécution JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a795b-193">Resumes JavaScript execution.</span></span>

</p>

---

### <span data-ttu-id="a795b-194">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="a795b-194">getScriptSource</span></span>
<span data-ttu-id="a795b-195">Renvoie la source du script avec l’ID donné.</span><span class="sxs-lookup"><span data-stu-id="a795b-195">Returns source for the script with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-196">Parameters</span><span class="sxs-lookup"><span data-stu-id="a795b-196">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-197">scriptId</span><span class="sxs-lookup"><span data-stu-id="a795b-197">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="a795b-198">ID du script pour lequel obtenir la source.</span><span class="sxs-lookup"><span data-stu-id="a795b-198">Id of the script to get source for.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-199">Renvoie</span><span class="sxs-lookup"><span data-stu-id="a795b-199">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-200">scriptSource</span><span class="sxs-lookup"><span data-stu-id="a795b-200">scriptSource</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a795b-201">Source de script.</span><span class="sxs-lookup"><span data-stu-id="a795b-201">Script source.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a795b-202">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="a795b-202">setPauseOnExceptions</span></span>
<span data-ttu-id="a795b-203">Définit une pause sur l’État exceptions.</span><span class="sxs-lookup"><span data-stu-id="a795b-203">Defines pause on exceptions state.</span></span> <span data-ttu-id="a795b-204">Peut être défini pour s’arrêter sur toutes les exceptions, ou aucune exception.</span><span class="sxs-lookup"><span data-stu-id="a795b-204">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span> <span data-ttu-id="a795b-205">Le point d’interruption initial est <code>none</code> .</span><span class="sxs-lookup"><span data-stu-id="a795b-205">Initial pause on exceptions state is <code>none</code>.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-206">Parameters</span><span class="sxs-lookup"><span data-stu-id="a795b-206">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-207">traité</span><span class="sxs-lookup"><span data-stu-id="a795b-207">state</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="a795b-208">Valeurs autorisées: aucun, non intercepté, tous</span><span class="sxs-lookup"><span data-stu-id="a795b-208">Allowed values: none, uncaught, all</span></span></i></td>
            <td><span data-ttu-id="a795b-209">Placez le pointeur sur le mode exceptions.</span><span class="sxs-lookup"><span data-stu-id="a795b-209">Pause on exceptions mode.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a795b-210">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="a795b-210">evaluateOnCallFrame</span></span>
<span data-ttu-id="a795b-211">Évalue l’expression sur un cadre d’appel donné.</span><span class="sxs-lookup"><span data-stu-id="a795b-211">Evaluates expression on a given call frame.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-212">Parameters</span><span class="sxs-lookup"><span data-stu-id="a795b-212">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-213">callFrameId</span><span class="sxs-lookup"><span data-stu-id="a795b-213">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="a795b-214">Identifiant de l’identification de l’appel.</span><span class="sxs-lookup"><span data-stu-id="a795b-214">Call frame identifier to evaluate on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-215">termes</span><span class="sxs-lookup"><span data-stu-id="a795b-215">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a795b-216">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="a795b-216">Expression to evaluate.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-217">Renvoie</span><span class="sxs-lookup"><span data-stu-id="a795b-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-218">provoqué</span><span class="sxs-lookup"><span data-stu-id="a795b-218">result</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="a795b-219">Wrapper d’objet pour le résultat d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="a795b-219">Object wrapper for the evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a795b-220">setVariableValue</span><span class="sxs-lookup"><span data-stu-id="a795b-220">setVariableValue</span></span>
<span data-ttu-id="a795b-221">Change la valeur de la variable dans un callframe.</span><span class="sxs-lookup"><span data-stu-id="a795b-221">Changes value of variable in a callframe.</span></span> <span data-ttu-id="a795b-222">Les étendues basées sur les objets ne sont pas prises en charge et doivent être mutées manuellement.</span><span class="sxs-lookup"><span data-stu-id="a795b-222">Object-based scopes are not supported and must be mutated manually.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-223">Parameters</span><span class="sxs-lookup"><span data-stu-id="a795b-223">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-224">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="a795b-224">scopeNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="a795b-225">un nombre d’étendues égal à zéro tel qu’il apparaît dans la chaîne d’étendue.</span><span class="sxs-lookup"><span data-stu-id="a795b-225">0-based number of scope as was listed in scope chain.</span></span> <span data-ttu-id="a795b-226">Seuls les types d’étendue’local', de fermeture et de capture sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="a795b-226">Only 'local', 'closure' and 'catch' scope types are allowed.</span></span> <span data-ttu-id="a795b-227">Les autres étendues peuvent être manipulées manuellement.</span><span class="sxs-lookup"><span data-stu-id="a795b-227">Other scopes could be manipulated manually.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-228">NomVariable</span><span class="sxs-lookup"><span data-stu-id="a795b-228">variableName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a795b-229">Nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="a795b-229">Variable name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-230">NouvelleValeur</span><span class="sxs-lookup"><span data-stu-id="a795b-230">newValue</span></span></td>
            <td><a href="runtime.md#callargument"><code class="flyout">Runtime.CallArgument</code></a></td>
            <td><span data-ttu-id="a795b-231">Valeur de la nouvelle variable.</span><span class="sxs-lookup"><span data-stu-id="a795b-231">New variable value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-232">callFrameId</span><span class="sxs-lookup"><span data-stu-id="a795b-232">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="a795b-233">ID de callframe qui contient la variable.</span><span class="sxs-lookup"><span data-stu-id="a795b-233">Id of callframe that holds variable.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a795b-234">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="a795b-234">setBlackboxPatterns</span></span>
<span><b><span data-ttu-id="a795b-235">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="a795b-235">Experimental.</span></span> </b></span><span data-ttu-id="a795b-236">Remplacer les modèles de Blackbox</span><span class="sxs-lookup"><span data-stu-id="a795b-236">Replace previous blackbox patterns with passed ones.</span></span> <span data-ttu-id="a795b-237">Force le serveur principal à ignorer l’étape/la suspension dans les scripts avec une URL qui correspond à l’un des modèles.</span><span class="sxs-lookup"><span data-stu-id="a795b-237">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span> <span data-ttu-id="a795b-238">Le débogueur tente de quitter le script Blackbox en exécutant plusieurs fois «étape», ce qui a pour fin en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="a795b-238">The debugger will try to leave blackboxed script by performing 'step in' several times, finally resorting to 'step out' if unsuccessful.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-239">Parameters</span><span class="sxs-lookup"><span data-stu-id="a795b-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-240">masques</span><span class="sxs-lookup"><span data-stu-id="a795b-240">patterns</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="a795b-241">Tableau d’regexps qui seront utilisés pour vérifier l’URL du script pour l’État Blackbox.</span><span class="sxs-lookup"><span data-stu-id="a795b-241">Array of regexps that will be used to check script url for blackbox state.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a795b-242">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="a795b-242">msSetDebuggerPropertyValue</span></span>
<span><b><span data-ttu-id="a795b-243">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="a795b-243">Experimental.</span></span> </b></span><span data-ttu-id="a795b-244">Microsoft: définit la propriété Debugger spécifiée sur la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a795b-244">Microsoft: Sets the specified debugger property to the specified value.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-245">Parameters</span><span class="sxs-lookup"><span data-stu-id="a795b-245">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-246">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="a795b-246">debuggerPropertyId</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a795b-247">Microsoft: ID de propriété (par exemple, msDebuggerPropertyId) à définir.</span><span class="sxs-lookup"><span data-stu-id="a795b-247">Microsoft: The property id (i.e. msDebuggerPropertyId) to set.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-248">NouvelleValeur</span><span class="sxs-lookup"><span data-stu-id="a795b-248">newValue</span></span></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="a795b-249">Événements</span><span class="sxs-lookup"><span data-stu-id="a795b-249">Events</span></span>

### <span data-ttu-id="a795b-250">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="a795b-250">scriptParsed</span></span>
<span data-ttu-id="a795b-251">Déclenché lorsque le script est analysé.</span><span class="sxs-lookup"><span data-stu-id="a795b-251">Fired when the script is parsed.</span></span> <span data-ttu-id="a795b-252">Cet événement est également déclenché pour tous les scripts connus et non perçus lors de l’activation du débogueur.</span><span class="sxs-lookup"><span data-stu-id="a795b-252">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-253">Parameters</span><span class="sxs-lookup"><span data-stu-id="a795b-253">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-254">scriptId</span><span class="sxs-lookup"><span data-stu-id="a795b-254">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="a795b-255">Identificateur du script analysé.</span><span class="sxs-lookup"><span data-stu-id="a795b-255">Identifier of the script parsed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-256">url</span><span class="sxs-lookup"><span data-stu-id="a795b-256">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a795b-257">URL ou nom du script analysé (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="a795b-257">URL or name of the script parsed (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-258">startLine</span><span class="sxs-lookup"><span data-stu-id="a795b-258">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="a795b-259">Décalage de ligne du script dans la ressource avec l’URL donnée (pour les balises de script).</span><span class="sxs-lookup"><span data-stu-id="a795b-259">Line offset of the script within the resource with given URL (for script tags).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-260">ColonneDébut</span><span class="sxs-lookup"><span data-stu-id="a795b-260">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="a795b-261">Décalage de colonne du script dans la ressource avec l’URL donnée.</span><span class="sxs-lookup"><span data-stu-id="a795b-261">Column offset of the script within the resource with given URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-262">lignefin</span><span class="sxs-lookup"><span data-stu-id="a795b-262">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="a795b-263">Dernière ligne du script.</span><span class="sxs-lookup"><span data-stu-id="a795b-263">Last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-264">ColonneFin</span><span class="sxs-lookup"><span data-stu-id="a795b-264">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="a795b-265">Longueur de la dernière ligne du script.</span><span class="sxs-lookup"><span data-stu-id="a795b-265">Length of the last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-266">executionContextId</span><span class="sxs-lookup"><span data-stu-id="a795b-266">executionContextId</span></span></td>
            <td><a href="runtime.md#executioncontextid"><code class="flyout">Runtime.ExecutionContextId</code></a></td>
            <td><span data-ttu-id="a795b-267">Spécifie le contexte de création de script.</span><span class="sxs-lookup"><span data-stu-id="a795b-267">Specifies script creation context.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-268">sourceMapURL</span><span class="sxs-lookup"><span data-stu-id="a795b-268">sourceMapURL</span></span> <br/> <i><span data-ttu-id="a795b-269">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-269">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a795b-270">URL du mappage source associé au script (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="a795b-270">URL of source map associated with script (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-271">nombre</span><span class="sxs-lookup"><span data-stu-id="a795b-271">length</span></span> <br/> <i><span data-ttu-id="a795b-272">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-272">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="a795b-273">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="a795b-273">Experimental.</span></span> </b></span><span data-ttu-id="a795b-274">Cette longueur de script.</span><span class="sxs-lookup"><span data-stu-id="a795b-274">This script length.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-275">msParentId</span><span class="sxs-lookup"><span data-stu-id="a795b-275">msParentId</span></span> <br/> <i><span data-ttu-id="a795b-276">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-276">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="a795b-277">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="a795b-277">Experimental.</span></span> </b></span><span data-ttu-id="a795b-278">Il s’agit de l’ID de document parent.</span><span class="sxs-lookup"><span data-stu-id="a795b-278">This is the parent document ID.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-279">msMimeType</span><span class="sxs-lookup"><span data-stu-id="a795b-279">msMimeType</span></span> <br/> <i><span data-ttu-id="a795b-280">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-280">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="a795b-281">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="a795b-281">Experimental.</span></span> </b></span><span data-ttu-id="a795b-282">Il s’agit du type MIME.</span><span class="sxs-lookup"><span data-stu-id="a795b-282">This is the mime type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-283">msIsDynamicCode</span><span class="sxs-lookup"><span data-stu-id="a795b-283">msIsDynamicCode</span></span> <br/> <i><span data-ttu-id="a795b-284">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-284">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="a795b-285">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="a795b-285">Experimental.</span></span> </b></span><span data-ttu-id="a795b-286">Cela indique s’il s’agit d’un code dynamique.</span><span class="sxs-lookup"><span data-stu-id="a795b-286">This indicates whether it is dynamic code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-287">msLongDocumentId</span><span class="sxs-lookup"><span data-stu-id="a795b-287">msLongDocumentId</span></span> <br/> <i><span data-ttu-id="a795b-288">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-288">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="a795b-289">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="a795b-289">Experimental.</span></span> </b></span><span data-ttu-id="a795b-290">Il s’agit de l’ID de document long.</span><span class="sxs-lookup"><span data-stu-id="a795b-290">This is the long document ID.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a795b-291">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="a795b-291">breakpointResolved</span></span>
<span data-ttu-id="a795b-292">Déclenché lorsque le point d’arrêt est résolu en un script et un emplacement réels.</span><span class="sxs-lookup"><span data-stu-id="a795b-292">Fired when breakpoint is resolved to an actual script and location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-293">Parameters</span><span class="sxs-lookup"><span data-stu-id="a795b-293">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-294">breakpointId</span><span class="sxs-lookup"><span data-stu-id="a795b-294">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="a795b-295">Identificateur unique de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a795b-295">Breakpoint unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-296">ventilation</span><span class="sxs-lookup"><span data-stu-id="a795b-296">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="a795b-297">Emplacement du point d’arrêt réel.</span><span class="sxs-lookup"><span data-stu-id="a795b-297">Actual breakpoint location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-298">msLength</span><span class="sxs-lookup"><span data-stu-id="a795b-298">msLength</span></span> <br/> <i><span data-ttu-id="a795b-299">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-299">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="a795b-300">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="a795b-300">Experimental.</span></span> </b></span><span data-ttu-id="a795b-301">Microsoft: longueur du code (par exemple, nombre de caractères) à l’emplacement du point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a795b-301">Microsoft: Length of code (i.e. number of characters) at the breakpoint location.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a795b-302">en pause</span><span class="sxs-lookup"><span data-stu-id="a795b-302">paused</span></span>
<span data-ttu-id="a795b-303">Déclenché lorsque les débogueurs s’interrompent pour un point d’arrêt ou une exception.</span><span class="sxs-lookup"><span data-stu-id="a795b-303">Fired when the debuggers breaks for a breakpoint or exception.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-304">Parameters</span><span class="sxs-lookup"><span data-stu-id="a795b-304">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-305">callFrames</span><span class="sxs-lookup"><span data-stu-id="a795b-305">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="a795b-306">Pile d’appels sur laquelle le débogueur a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="a795b-306">Call stack the debugger stopped on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-307">tient</span><span class="sxs-lookup"><span data-stu-id="a795b-307">reason</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="a795b-308">Valeurs autorisées: point d’arrêt, étape, exception, other, EventListener</span><span class="sxs-lookup"><span data-stu-id="a795b-308">Allowed values: breakpoint, step, exception, other, EventListener</span></span></i></td>
            <td><span data-ttu-id="a795b-309">Raison du pause.</span><span class="sxs-lookup"><span data-stu-id="a795b-309">Pause reason.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-310">data</span><span class="sxs-lookup"><span data-stu-id="a795b-310">data</span></span> <br/> <i><span data-ttu-id="a795b-311">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-311">optional</span></span></i></td>
            <td><code class="flyout">object</code></td>
            <td><span data-ttu-id="a795b-312">Objet contenant des propriétés auxiliaires spécifiques de rupture.</span><span class="sxs-lookup"><span data-stu-id="a795b-312">Object containing break-specific auxiliary properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-313">hitBreakpoints</span><span class="sxs-lookup"><span data-stu-id="a795b-313">hitBreakpoints</span></span> <br/> <i><span data-ttu-id="a795b-314">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-314">optional</span></span></i></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="a795b-315">ID d’arrêt du positionnement</span><span class="sxs-lookup"><span data-stu-id="a795b-315">Hit breakpoints IDs</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-316">asyncStackTrace</span><span class="sxs-lookup"><span data-stu-id="a795b-316">asyncStackTrace</span></span> <br/> <i><span data-ttu-id="a795b-317">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-317">optional</span></span></i></td>
            <td><!--  <a href="#stacktrace">  --><code class="flyout">StackTrace</code><!--  </a>  --></td>
            <td><span data-ttu-id="a795b-318">Trace de pile asynchrone JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a795b-318">JavaScript async stack trace.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a795b-319">reprend</span><span class="sxs-lookup"><span data-stu-id="a795b-319">resumed</span></span>
<span data-ttu-id="a795b-320">Déclenché lorsque le débogueur reprend l’exécution.</span><span class="sxs-lookup"><span data-stu-id="a795b-320">Fired when the debugger resumes execution.</span></span>

</p>

---

## <span data-ttu-id="a795b-321">Types</span><span class="sxs-lookup"><span data-stu-id="a795b-321">Types</span></span>

### <a name="breakpointid"></a> <span data-ttu-id="a795b-322">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="a795b-322">BreakpointId</span></span> `string`

<span data-ttu-id="a795b-323">Identificateur de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a795b-323">Breakpoint identifier.</span></span>

</p>

---

### <a name="callframeid"></a> <span data-ttu-id="a795b-324">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="a795b-324">CallFrameId</span></span> `string`

<span data-ttu-id="a795b-325">Identificateur d’image d’appel.</span><span class="sxs-lookup"><span data-stu-id="a795b-325">Call frame identifier.</span></span>

</p>

---

### <a name="location"></a> <span data-ttu-id="a795b-326">Location</span><span class="sxs-lookup"><span data-stu-id="a795b-326">Location</span></span> `object`

<span data-ttu-id="a795b-327">Emplacement dans le code source.</span><span class="sxs-lookup"><span data-stu-id="a795b-327">Location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-328">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a795b-328">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-329">scriptId</span><span class="sxs-lookup"><span data-stu-id="a795b-329">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="a795b-330">ID de script tel qu’indiqué dans le <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="a795b-330">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-331">lineNumber</span><span class="sxs-lookup"><span data-stu-id="a795b-331">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="a795b-332">Numéro de ligne dans le script (0).</span><span class="sxs-lookup"><span data-stu-id="a795b-332">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-333">columnNumber</span><span class="sxs-lookup"><span data-stu-id="a795b-333">columnNumber</span></span> <br/> <i><span data-ttu-id="a795b-334">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-334">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="a795b-335">Numéro de colonne dans le script (0).</span><span class="sxs-lookup"><span data-stu-id="a795b-335">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-336">msLength</span><span class="sxs-lookup"><span data-stu-id="a795b-336">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="a795b-337">Microsoft: longueur de code (par exemple, nombre de caractères) à cette image d’appel.</span><span class="sxs-lookup"><span data-stu-id="a795b-337">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="breaklocation"></a> <span data-ttu-id="a795b-338">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="a795b-338">BreakLocation</span></span> `object`

<span data-ttu-id="a795b-339">Emplacement d’arrêt dans le code source.</span><span class="sxs-lookup"><span data-stu-id="a795b-339">Break location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-340">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a795b-340">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-341">scriptId</span><span class="sxs-lookup"><span data-stu-id="a795b-341">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="a795b-342">ID de script tel qu’indiqué dans le <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="a795b-342">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-343">lineNumber</span><span class="sxs-lookup"><span data-stu-id="a795b-343">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="a795b-344">Numéro de ligne dans le script (0).</span><span class="sxs-lookup"><span data-stu-id="a795b-344">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-345">columnNumber</span><span class="sxs-lookup"><span data-stu-id="a795b-345">columnNumber</span></span> <br/> <i><span data-ttu-id="a795b-346">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-346">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="a795b-347">Numéro de colonne dans le script (0).</span><span class="sxs-lookup"><span data-stu-id="a795b-347">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-348">msLength</span><span class="sxs-lookup"><span data-stu-id="a795b-348">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="a795b-349">Microsoft: longueur de code (par exemple, nombre de caractères) à cette image d’appel.</span><span class="sxs-lookup"><span data-stu-id="a795b-349">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-350">type</span><span class="sxs-lookup"><span data-stu-id="a795b-350">type</span></span> <br/> <i><span data-ttu-id="a795b-351">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-351">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a795b-352">Valeurs autorisées: debuggerStatement, Call, retour.</span><span class="sxs-lookup"><span data-stu-id="a795b-352">Allowed values: debuggerStatement, call, return.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callframe"></a> <span data-ttu-id="a795b-353">CallFrame</span><span class="sxs-lookup"><span data-stu-id="a795b-353">CallFrame</span></span> `object`

<span data-ttu-id="a795b-354">Image d’un appel JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a795b-354">JavaScript call frame.</span></span> <span data-ttu-id="a795b-355">Tableau de trames d’appel qui forment la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="a795b-355">Array of call frames form the call stack.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-356">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a795b-356">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-357">callFrameId</span><span class="sxs-lookup"><span data-stu-id="a795b-357">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="a795b-358">Identificateur d’image d’appel.</span><span class="sxs-lookup"><span data-stu-id="a795b-358">Call frame identifier.</span></span> <span data-ttu-id="a795b-359">Cet identificateur est valide uniquement lorsque le débogueur est en pause.</span><span class="sxs-lookup"><span data-stu-id="a795b-359">This identifier is only valid while the debugger is paused.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-360">Admises</span><span class="sxs-lookup"><span data-stu-id="a795b-360">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a795b-361">Nom de la fonction JavaScript appelée sur cette image d’appel.</span><span class="sxs-lookup"><span data-stu-id="a795b-361">Name of the JavaScript function called on this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-362">functionLocation</span><span class="sxs-lookup"><span data-stu-id="a795b-362">functionLocation</span></span> <br/> <i><span data-ttu-id="a795b-363">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-363">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span><b><span data-ttu-id="a795b-364">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="a795b-364">Experimental.</span></span> </b></span><span data-ttu-id="a795b-365">Emplacement dans le code source.</span><span class="sxs-lookup"><span data-stu-id="a795b-365">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-366">ventilation</span><span class="sxs-lookup"><span data-stu-id="a795b-366">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="a795b-367">Emplacement dans le code source.</span><span class="sxs-lookup"><span data-stu-id="a795b-367">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-368">url</span><span class="sxs-lookup"><span data-stu-id="a795b-368">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a795b-369">Nom ou URL du script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a795b-369">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-370">scopeChain</span><span class="sxs-lookup"><span data-stu-id="a795b-370">scopeChain</span></span></td>
            <td><a href="#scope"><code class="flyout">Scope[]</code></a></td>
            <td><span data-ttu-id="a795b-371">Chaîne d’étendue pour cette image d’appel.</span><span class="sxs-lookup"><span data-stu-id="a795b-371">Scope chain for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-372">elle</span><span class="sxs-lookup"><span data-stu-id="a795b-372">this</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><code>this</code> <span data-ttu-id="a795b-373">objet pour cette image d’appel.</span><span class="sxs-lookup"><span data-stu-id="a795b-373">object for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-374">returnValue</span><span class="sxs-lookup"><span data-stu-id="a795b-374">returnValue</span></span> <br/> <i><span data-ttu-id="a795b-375">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-375">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="a795b-376">Valeur renvoyée, si la fonction est à la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="a795b-376">The value being returned, if the function is at return point.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="scope"></a> <span data-ttu-id="a795b-377">Étendue</span><span class="sxs-lookup"><span data-stu-id="a795b-377">Scope</span></span> `object`

<span data-ttu-id="a795b-378">Description de l’étendue.</span><span class="sxs-lookup"><span data-stu-id="a795b-378">Scope description.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a795b-379">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a795b-379">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a795b-380">type</span><span class="sxs-lookup"><span data-stu-id="a795b-380">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="a795b-381">Valeurs autorisées: global, local, avec, clôture, catch, bloc, script, Eval, module, retour</span><span class="sxs-lookup"><span data-stu-id="a795b-381">Allowed values: global, local, with, closure, catch, block, script, eval, module, return</span></span></i></td>
            <td><span data-ttu-id="a795b-382">Type d’étendue.</span><span class="sxs-lookup"><span data-stu-id="a795b-382">Scope type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-383">object</span><span class="sxs-lookup"><span data-stu-id="a795b-383">object</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="a795b-384">Objet représentant la portée.</span><span class="sxs-lookup"><span data-stu-id="a795b-384">Object representing the scope.</span></span> <span data-ttu-id="a795b-385">Pour <code>global</code> les <code>with</code> étendues, il s’agit de l’objet réel; pour les autres étendues, il s’agit d’un objet temporaire artificiel qui énumère les variables d’étendue en tant que propriétés.</span><span class="sxs-lookup"><span data-stu-id="a795b-385">For <code>global</code> and <code>with</code> scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-386">name</span><span class="sxs-lookup"><span data-stu-id="a795b-386">name</span></span> <br/> <i><span data-ttu-id="a795b-387">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-387">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-388">startLocation</span><span class="sxs-lookup"><span data-stu-id="a795b-388">startLocation</span></span> <br/> <i><span data-ttu-id="a795b-389">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-389">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="a795b-390">Emplacement dans le code source où l’étendue commence</span><span class="sxs-lookup"><span data-stu-id="a795b-390">Location in the source code where scope starts</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a795b-391">endLocation</span><span class="sxs-lookup"><span data-stu-id="a795b-391">endLocation</span></span> <br/> <i><span data-ttu-id="a795b-392">facultatif</span><span class="sxs-lookup"><span data-stu-id="a795b-392">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="a795b-393">Emplacement dans le code source où l’étendue se termine</span><span class="sxs-lookup"><span data-stu-id="a795b-393">Location in the source code where scope ends</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="a795b-394">Dépendances</span><span class="sxs-lookup"><span data-stu-id="a795b-394">Dependencies</span></span>

[<span data-ttu-id="a795b-395">Runtime</span><span class="sxs-lookup"><span data-stu-id="a795b-395">Runtime</span></span>](runtime.md)
