---
description: Référence du protocole DevTools version 0.1 (EdgeHTML) pour le domaine du débogueur.  Le domaine du déboguer expose les fonctionnalités de débogage JavaScript.  Il permet de définir et de supprimer des points d’arrêt, d’exécuter pas à pas, d’explorer les traces de pile, etc.
title: Domaine du débogueur - DevTools Protocol Version 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d63408e23fd8912cf617bfefae2b991387b45a38
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397677"
---
# <a name="debugger-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="5722b-105">Domaine du débogueur - DevTools Protocol Version 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="5722b-105">Debugger Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  
  
<span data-ttu-id="5722b-106">Le domaine du déboguer expose les fonctionnalités de débogage JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5722b-106">Debugger domain exposes JavaScript debugging capabilities.</span></span>  <span data-ttu-id="5722b-107">Il permet de définir et de supprimer des points d’arrêt, d’exécuter pas à pas, d’explorer les traces de pile, etc.</span><span class="sxs-lookup"><span data-stu-id="5722b-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| <span data-ttu-id="5722b-108">Classification</span><span class="sxs-lookup"><span data-stu-id="5722b-108">Classification</span></span> | <span data-ttu-id="5722b-109">Membres</span><span class="sxs-lookup"><span data-stu-id="5722b-109">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="5722b-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5722b-110">Methods</span></span>](#methods) | <span data-ttu-id="5722b-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue) [](#stepout)</span><span class="sxs-lookup"><span data-stu-id="5722b-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |  
| [<span data-ttu-id="5722b-112">Événements</span><span class="sxs-lookup"><span data-stu-id="5722b-112">Events</span></span>](#events) | <span data-ttu-id="5722b-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span><span class="sxs-lookup"><span data-stu-id="5722b-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |  
| [<span data-ttu-id="5722b-114">Types</span><span class="sxs-lookup"><span data-stu-id="5722b-114">Types</span></span>](#types) | <span data-ttu-id="5722b-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span><span class="sxs-lookup"><span data-stu-id="5722b-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |  
| [<span data-ttu-id="5722b-116">Dépendances</span><span class="sxs-lookup"><span data-stu-id="5722b-116">Dependencies</span></span>](#dependencies) | [<span data-ttu-id="5722b-117">Runtime</span><span class="sxs-lookup"><span data-stu-id="5722b-117">Runtime</span></span>](./runtime.md) |  

## <a name="methods"></a><span data-ttu-id="5722b-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5722b-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="5722b-119">activer</span><span class="sxs-lookup"><span data-stu-id="5722b-119">enable</span></span>  

<span data-ttu-id="5722b-120">Active le débogger pour la page donnée.</span><span class="sxs-lookup"><span data-stu-id="5722b-120">Enables debugger for the given page.</span></span>  <span data-ttu-id="5722b-121">Les clients ne doivent pas supposer que le débogage a été activé jusqu’à ce que le résultat de cette commande soit reçu.</span><span class="sxs-lookup"><span data-stu-id="5722b-121">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="5722b-122">désactiver </span><span class="sxs-lookup"><span data-stu-id="5722b-122">disable</span></span>  

<span data-ttu-id="5722b-123">Désactive le débogger pour une page donnée.</span><span class="sxs-lookup"><span data-stu-id="5722b-123">Disables debugger for given page.</span></span>  

&nbsp;  

---  

### <a name="getpossiblebreakpoints"></a><span data-ttu-id="5722b-124">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="5722b-124">getPossibleBreakpoints</span></span>  

<span data-ttu-id="5722b-125">Renvoie les emplacements possibles pour le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5722b-125">Returns possible locations for breakpoint.</span></span>  <span data-ttu-id="5722b-126">ScriptId dans les emplacements de plage de début et de fin doit être identique.</span><span class="sxs-lookup"><span data-stu-id="5722b-126">scriptId in start and end range locations should be the same.</span></span>  

| <span data-ttu-id="5722b-127">Parameters</span><span class="sxs-lookup"><span data-stu-id="5722b-127">Parameters</span></span> | <span data-ttu-id="5722b-128">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-128">Type</span></span> | <span data-ttu-id="5722b-129">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-129">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-130">start</span><span class="sxs-lookup"><span data-stu-id="5722b-130">start</span></span> | [<span data-ttu-id="5722b-131">Emplacement</span><span class="sxs-lookup"><span data-stu-id="5722b-131">Location</span></span>](#location) | <span data-ttu-id="5722b-132">Début de la plage pour rechercher les emplacements de points d’arrêt possibles.</span><span class="sxs-lookup"><span data-stu-id="5722b-132">Start of range to search possible breakpoint locations in.</span></span> |  
| <span data-ttu-id="5722b-133">terminer</span><span class="sxs-lookup"><span data-stu-id="5722b-133">end</span></span> | [<span data-ttu-id="5722b-134">Emplacement</span><span class="sxs-lookup"><span data-stu-id="5722b-134">Location</span></span>](#location) | <span data-ttu-id="5722b-135">Fin de la plage pour rechercher les emplacements de points d’arrêt possibles dans \(à l’exclusion de\).</span><span class="sxs-lookup"><span data-stu-id="5722b-135">End of range to search possible breakpoint locations in \(excluding\).</span></span>  <span data-ttu-id="5722b-136">Lorsqu’il n’est pas spécifié, la fin des scripts est utilisée comme fin de plage.</span><span class="sxs-lookup"><span data-stu-id="5722b-136">When not specified, end of scripts is used as end of range.</span></span> |  

| <span data-ttu-id="5722b-137">Renvoie</span><span class="sxs-lookup"><span data-stu-id="5722b-137">Returns</span></span> | <span data-ttu-id="5722b-138">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-138">Type</span></span> | <span data-ttu-id="5722b-139">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-139">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-140">emplacements</span><span class="sxs-lookup"><span data-stu-id="5722b-140">locations</span></span> | [<span data-ttu-id="5722b-141">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="5722b-141">BreakLocation</span></span>](#breaklocation) | <span data-ttu-id="5722b-142">Liste des emplacements de points d’arrêt possibles.</span><span class="sxs-lookup"><span data-stu-id="5722b-142">List of the possible breakpoint locations.</span></span> |  

---  

### <a name="setbreakpointsactive"></a><span data-ttu-id="5722b-143">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="5722b-143">setBreakpointsActive</span></span>  

<span data-ttu-id="5722b-144">Active/désactive tous les points d’arrêt sur la page.</span><span class="sxs-lookup"><span data-stu-id="5722b-144">Activates / deactivates all breakpoints on the page.</span></span>  

| <span data-ttu-id="5722b-145">Parameters</span><span class="sxs-lookup"><span data-stu-id="5722b-145">Parameters</span></span> | <span data-ttu-id="5722b-146">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-146">Type</span></span> | <span data-ttu-id="5722b-147">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-147">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-148">active</span><span class="sxs-lookup"><span data-stu-id="5722b-148">active</span></span> | `boolean` | <span data-ttu-id="5722b-149">Nouvelle valeur pour l’état actif des points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5722b-149">New value for breakpoints active state.</span></span> |  

---  

### <a name="setbreakpointbyurl"></a><span data-ttu-id="5722b-150">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="5722b-150">setBreakpointByUrl</span></span>  

<span data-ttu-id="5722b-151">Définit le point d’arrêt JavaScript à un emplacement donné spécifié par l’URL ou l’URL regex.</span><span class="sxs-lookup"><span data-stu-id="5722b-151">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span>  <span data-ttu-id="5722b-152">Une fois cette commande émise, tous les scripts déjà assués ont des points d’arrêt résolus et renvoyés dans la `locations` propriété.</span><span class="sxs-lookup"><span data-stu-id="5722b-152">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in `locations` property.</span></span>  <span data-ttu-id="5722b-153">Une autre correspondance de l’examen des scripts entraîne l’émission `breakpointResolved` d’événements ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="5722b-153">Further matching script parsing will result in subsequent `breakpointResolved` events issued.</span></span>  <span data-ttu-id="5722b-154">Ce point d’arrêt logique survivra au rechargement des pages.</span><span class="sxs-lookup"><span data-stu-id="5722b-154">This logical breakpoint will survive page reloads.</span></span>  

| <span data-ttu-id="5722b-155">Parameters</span><span class="sxs-lookup"><span data-stu-id="5722b-155">Parameters</span></span> | <span data-ttu-id="5722b-156">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-156">Type</span></span> | <span data-ttu-id="5722b-157">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-157">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-158">lineNumber</span><span class="sxs-lookup"><span data-stu-id="5722b-158">lineNumber</span></span> | `integer` | <span data-ttu-id="5722b-159">Numéro de ligne sur le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5722b-159">Line number to set breakpoint at.</span></span> |  
| <span data-ttu-id="5722b-160">url \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-160">url  \(optional\)</span></span> | `string` | <span data-ttu-id="5722b-161">URL des ressources pour définir le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5722b-161">URL of the resources to set breakpoint on.</span></span> |  
| <span data-ttu-id="5722b-162">urlRegex \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="5722b-162">urlRegex  \(optional\)</span></span> | `string` | <span data-ttu-id="5722b-163">Modèle d’regex pour les URL des ressources sur les points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5722b-163">Regex pattern for the URLs of the resources to set breakpoints on.</span></span>  <span data-ttu-id="5722b-164">`url` `urlRegex` L’un ou l’autre doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="5722b-164">Either `url` or `urlRegex` must be specified.</span></span> |  
| <span data-ttu-id="5722b-165">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-165">columnNumber  \(optional\)</span></span> | `integer` | <span data-ttu-id="5722b-166">Décalez la ligne pour définir le point d’arrêt sur.</span><span class="sxs-lookup"><span data-stu-id="5722b-166">Offset in the line to set breakpoint at.</span></span> |  
| <span data-ttu-id="5722b-167">condition \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-167">condition  \(optional\)</span></span> | `string` | <span data-ttu-id="5722b-168">Expression à utiliser comme condition de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5722b-168">Expression to use as a breakpoint condition.</span></span>  <span data-ttu-id="5722b-169">Lorsqu’il est spécifié, le débogger s’arrête uniquement sur le point d’arrêt si cette expression est évaluée à true.</span><span class="sxs-lookup"><span data-stu-id="5722b-169">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="5722b-170">Renvoie</span><span class="sxs-lookup"><span data-stu-id="5722b-170">Returns</span></span> | <span data-ttu-id="5722b-171">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-171">Type</span></span> | <span data-ttu-id="5722b-172">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-172">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-173">breakpointId</span><span class="sxs-lookup"><span data-stu-id="5722b-173">breakpointId</span></span> | [<span data-ttu-id="5722b-174">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="5722b-174">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="5722b-175">ID du point d’arrêt créé pour référence supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="5722b-175">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="5722b-176">emplacements</span><span class="sxs-lookup"><span data-stu-id="5722b-176">locations</span></span> | [<span data-ttu-id="5722b-177">Location[]</span><span class="sxs-lookup"><span data-stu-id="5722b-177">Location[]</span></span>](#location) | <span data-ttu-id="5722b-178">Liste des emplacements où ce point d’arrêt a été résolu lors de l’ajout.</span><span class="sxs-lookup"><span data-stu-id="5722b-178">List of the locations this breakpoint resolved into upon addition.</span></span> |  

---  

### <a name="setbreakpoint"></a><span data-ttu-id="5722b-179">setBreakpoint</span><span class="sxs-lookup"><span data-stu-id="5722b-179">setBreakpoint</span></span>  

<span data-ttu-id="5722b-180">Définit le point d’arrêt JavaScript à un emplacement donné.</span><span class="sxs-lookup"><span data-stu-id="5722b-180">Sets JavaScript breakpoint at a given location.</span></span>  

| <span data-ttu-id="5722b-181">Parameters</span><span class="sxs-lookup"><span data-stu-id="5722b-181">Parameters</span></span> | <span data-ttu-id="5722b-182">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-182">Type</span></span> | <span data-ttu-id="5722b-183">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-183">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-184">location</span><span class="sxs-lookup"><span data-stu-id="5722b-184">location</span></span> | [<span data-ttu-id="5722b-185">Emplacement</span><span class="sxs-lookup"><span data-stu-id="5722b-185">Location</span></span>](#location) | <span data-ttu-id="5722b-186">Emplacement dans le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5722b-186">Location to set breakpoint in.</span></span> |  
| <span data-ttu-id="5722b-187">condition \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-187">condition  \(optional\)</span></span> | `string` | <span data-ttu-id="5722b-188">Expression à utiliser comme condition de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5722b-188">Expression to use as a breakpoint condition.</span></span>  <span data-ttu-id="5722b-189">Lorsqu’il est spécifié, le débogger s’arrête uniquement sur le point d’arrêt si cette expression est évaluée à true.</span><span class="sxs-lookup"><span data-stu-id="5722b-189">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="5722b-190">Renvoie</span><span class="sxs-lookup"><span data-stu-id="5722b-190">Returns</span></span> | <span data-ttu-id="5722b-191">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-191">Type</span></span> | <span data-ttu-id="5722b-192">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-192">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-193">breakpointId</span><span class="sxs-lookup"><span data-stu-id="5722b-193">breakpointId</span></span> | [<span data-ttu-id="5722b-194">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="5722b-194">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="5722b-195">ID du point d’arrêt créé pour référence supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="5722b-195">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="5722b-196">actualLocation</span><span class="sxs-lookup"><span data-stu-id="5722b-196">actualLocation</span></span> | [<span data-ttu-id="5722b-197">Emplacement</span><span class="sxs-lookup"><span data-stu-id="5722b-197">Location</span></span>](#location) | <span data-ttu-id="5722b-198">Emplacement où ce point d’arrêt a été résolu.</span><span class="sxs-lookup"><span data-stu-id="5722b-198">Location this breakpoint resolved into.</span></span> |  

---  

### <a name="removebreakpoint"></a><span data-ttu-id="5722b-199">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="5722b-199">removeBreakpoint</span></span>  

<span data-ttu-id="5722b-200">Supprime le point d’arrêt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5722b-200">Removes JavaScript breakpoint.</span></span>  

| <span data-ttu-id="5722b-201">Parameters</span><span class="sxs-lookup"><span data-stu-id="5722b-201">Parameters</span></span> | <span data-ttu-id="5722b-202">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-202">Type</span></span> | <span data-ttu-id="5722b-203">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-203">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-204">breakpointId</span><span class="sxs-lookup"><span data-stu-id="5722b-204">breakpointId</span></span> | [<span data-ttu-id="5722b-205">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="5722b-205">BreakpointId</span></span>](#breakpointid) | &nbsp; |  

---  

### <a name="stepover"></a><span data-ttu-id="5722b-206">stepOver</span><span class="sxs-lookup"><span data-stu-id="5722b-206">stepOver</span></span>  

<span data-ttu-id="5722b-207">Étapes au-dessus de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="5722b-207">Steps over the statement.</span></span>  

&nbsp;  

---  

### <a name="stepinto"></a><span data-ttu-id="5722b-208">stepInto</span><span class="sxs-lookup"><span data-stu-id="5722b-208">stepInto</span></span>  

<span data-ttu-id="5722b-209">Étapes de l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="5722b-209">Steps into the function call.</span></span>  

&nbsp;  

---  

### <a name="stepout"></a><span data-ttu-id="5722b-210">stepOut</span><span class="sxs-lookup"><span data-stu-id="5722b-210">stepOut</span></span>  

<span data-ttu-id="5722b-211">Sort de l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="5722b-211">Steps out of the function call.</span></span>  

&nbsp;  

---  

### <a name="pause"></a><span data-ttu-id="5722b-212">pause</span><span class="sxs-lookup"><span data-stu-id="5722b-212">pause</span></span>  

<span data-ttu-id="5722b-213">S’arrête sur l’instruction JavaScript suivante.</span><span class="sxs-lookup"><span data-stu-id="5722b-213">Stops on the next JavaScript statement.</span></span>  

&nbsp;  

---  

### <a name="resume"></a><span data-ttu-id="5722b-214">resume</span><span class="sxs-lookup"><span data-stu-id="5722b-214">resume</span></span>  

<span data-ttu-id="5722b-215">Reprend l’exécution de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5722b-215">Resumes JavaScript execution.</span></span>  

&nbsp;  

---  

### <a name="getscriptsource"></a><span data-ttu-id="5722b-216">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="5722b-216">getScriptSource</span></span>  

<span data-ttu-id="5722b-217">Renvoie la source du script avec l’ID donné.</span><span class="sxs-lookup"><span data-stu-id="5722b-217">Returns source for the script with given ID.</span></span>  

| <span data-ttu-id="5722b-218">Parameters</span><span class="sxs-lookup"><span data-stu-id="5722b-218">Parameters</span></span> | <span data-ttu-id="5722b-219">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-219">Type</span></span> | <span data-ttu-id="5722b-220">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-220">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-221">scriptId</span><span class="sxs-lookup"><span data-stu-id="5722b-221">scriptId</span></span> | [<span data-ttu-id="5722b-222">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="5722b-222">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="5722b-223">ID du script pour obtenir la source.</span><span class="sxs-lookup"><span data-stu-id="5722b-223">ID of the script to get source for.</span></span> |  
| <span data-ttu-id="5722b-224">Renvoie</span><span class="sxs-lookup"><span data-stu-id="5722b-224">Returns</span></span> | <span data-ttu-id="5722b-225">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-225">Type</span></span> | <span data-ttu-id="5722b-226">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-226">Details</span></span> |  
|<span data-ttu-id="5722b-227">:---</span><span class="sxs-lookup"><span data-stu-id="5722b-227">:---</span></span> |<span data-ttu-id="5722b-228">:---</span><span class="sxs-lookup"><span data-stu-id="5722b-228">:---</span></span> |<span data-ttu-id="5722b-229">:---</span><span class="sxs-lookup"><span data-stu-id="5722b-229">:---</span></span> |  
| <span data-ttu-id="5722b-230">scriptSource</span><span class="sxs-lookup"><span data-stu-id="5722b-230">scriptSource</span></span> | `string` | <span data-ttu-id="5722b-231">Source du script.</span><span class="sxs-lookup"><span data-stu-id="5722b-231">Script source.</span></span> |  

---  

### <a name="setpauseonexceptions"></a><span data-ttu-id="5722b-232">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="5722b-232">setPauseOnExceptions</span></span>  

<span data-ttu-id="5722b-233">Définit une pause sur l’état des exceptions.</span><span class="sxs-lookup"><span data-stu-id="5722b-233">Defines pause on exceptions state.</span></span>  <span data-ttu-id="5722b-234">Peut être définie pour s’arrêter sur toutes les exceptions, les exceptions non détailles ou aucune exception.</span><span class="sxs-lookup"><span data-stu-id="5722b-234">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span>  <span data-ttu-id="5722b-235">La pause initiale sur l’état des exceptions est `none` .</span><span class="sxs-lookup"><span data-stu-id="5722b-235">Initial pause on exceptions state is `none`.</span></span>  

| <span data-ttu-id="5722b-236">Parameters</span><span class="sxs-lookup"><span data-stu-id="5722b-236">Parameters</span></span> | <span data-ttu-id="5722b-237">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-237">Type</span></span> | <span data-ttu-id="5722b-238">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-238">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-239">state</span><span class="sxs-lookup"><span data-stu-id="5722b-239">state</span></span> | `string` | <span data-ttu-id="5722b-240">Mettre en pause le mode exceptions.</span><span class="sxs-lookup"><span data-stu-id="5722b-240">Pause on exceptions mode.</span></span>  <span data-ttu-id="5722b-241">Valeurs autorisées  `none` : `uncaught` , et</span><span class="sxs-lookup"><span data-stu-id="5722b-241">Allowed values:  `none`, `uncaught`, and</span></span> `all` |  

---  

### <a name="evaluateoncallframe"></a><span data-ttu-id="5722b-242">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="5722b-242">evaluateOnCallFrame</span></span>  

<span data-ttu-id="5722b-243">Évalue l’expression sur une trame d’appel donnée.</span><span class="sxs-lookup"><span data-stu-id="5722b-243">Evaluates expression on a given call frame.</span></span>  

| <span data-ttu-id="5722b-244">Parameters</span><span class="sxs-lookup"><span data-stu-id="5722b-244">Parameters</span></span> | <span data-ttu-id="5722b-245">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-245">Type</span></span> | <span data-ttu-id="5722b-246">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-246">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-247">callFrameId</span><span class="sxs-lookup"><span data-stu-id="5722b-247">callFrameId</span></span> | [<span data-ttu-id="5722b-248">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="5722b-248">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="5722b-249">Identificateur d’image d’appel à évaluer.</span><span class="sxs-lookup"><span data-stu-id="5722b-249">Call frame identifier to evaluate on.</span></span> |  
| <span data-ttu-id="5722b-250">expression</span><span class="sxs-lookup"><span data-stu-id="5722b-250">expression</span></span> | `string` | <span data-ttu-id="5722b-251">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="5722b-251">Expression to evaluate.</span></span> |  
| <span data-ttu-id="5722b-252">Renvoie</span><span class="sxs-lookup"><span data-stu-id="5722b-252">Returns</span></span> | <span data-ttu-id="5722b-253">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-253">Type</span></span> | <span data-ttu-id="5722b-254">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-254">Details</span></span> |  
|<span data-ttu-id="5722b-255">:---</span><span class="sxs-lookup"><span data-stu-id="5722b-255">:---</span></span> |<span data-ttu-id="5722b-256">:---</span><span class="sxs-lookup"><span data-stu-id="5722b-256">:---</span></span> |<span data-ttu-id="5722b-257">:---</span><span class="sxs-lookup"><span data-stu-id="5722b-257">:---</span></span> |  
| <span data-ttu-id="5722b-258">result</span><span class="sxs-lookup"><span data-stu-id="5722b-258">result</span></span> | [<span data-ttu-id="5722b-259">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="5722b-259">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="5722b-260">Wrapper d’objet pour le résultat d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="5722b-260">Object wrapper for the evaluation result.</span></span> |  

---  

### <a name="setvariablevalue"></a><span data-ttu-id="5722b-261">setVariableValue</span><span class="sxs-lookup"><span data-stu-id="5722b-261">setVariableValue</span></span>  

<span data-ttu-id="5722b-262">Modifie la valeur de la variable dans un callframe.</span><span class="sxs-lookup"><span data-stu-id="5722b-262">Changes value of variable in a callframe.</span></span>  <span data-ttu-id="5722b-263">Les étendues basées sur des objets ne sont pas pris en charge et doivent être désactivées manuellement.</span><span class="sxs-lookup"><span data-stu-id="5722b-263">Object-based scopes are not supported and must be mutated manually.</span></span>  

| <span data-ttu-id="5722b-264">Parameters</span><span class="sxs-lookup"><span data-stu-id="5722b-264">Parameters</span></span> | <span data-ttu-id="5722b-265">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-265">Type</span></span> | <span data-ttu-id="5722b-266">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-266">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-267">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="5722b-267">scopeNumber</span></span> | `integer` | <span data-ttu-id="5722b-268">Nombre d’étendues basé sur 0, tel qu’il était répertorié dans la chaîne d’étendue.</span><span class="sxs-lookup"><span data-stu-id="5722b-268">0-based number of scope as was listed in scope chain.</span></span>  <span data-ttu-id="5722b-269">Seuls `local` , et les types `closure` `catch` d’étendue sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="5722b-269">Only `local`, `closure`, and `catch` scope types are allowed.</span></span>  <span data-ttu-id="5722b-270">D’autres étendues peuvent être manipulées manuellement.</span><span class="sxs-lookup"><span data-stu-id="5722b-270">Other scopes could be manipulated manually.</span></span> |  
| <span data-ttu-id="5722b-271">variableName</span><span class="sxs-lookup"><span data-stu-id="5722b-271">variableName</span></span> | `string` | <span data-ttu-id="5722b-272">Nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="5722b-272">Variable name.</span></span> |  
| <span data-ttu-id="5722b-273">newValue</span><span class="sxs-lookup"><span data-stu-id="5722b-273">newValue</span></span> | [<span data-ttu-id="5722b-274">Runtime.CallArgument</span><span class="sxs-lookup"><span data-stu-id="5722b-274">Runtime.CallArgument</span></span>](./runtime.md#callargument) | <span data-ttu-id="5722b-275">Nouvelle valeur de variable.</span><span class="sxs-lookup"><span data-stu-id="5722b-275">New variable value.</span></span> |  
| <span data-ttu-id="5722b-276">callFrameId</span><span class="sxs-lookup"><span data-stu-id="5722b-276">callFrameId</span></span> | [<span data-ttu-id="5722b-277">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="5722b-277">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="5722b-278">ID de l’appel qui contient une variable.</span><span class="sxs-lookup"><span data-stu-id="5722b-278">ID of callframe that holds variable.</span></span> |  

---  

### <a name="setblackboxpatterns"></a><span data-ttu-id="5722b-279">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="5722b-279">setBlackboxPatterns</span></span>  

<span data-ttu-id="5722b-280">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="5722b-280">**Experimental**.</span></span>  <span data-ttu-id="5722b-281">Remplacez les modèles de boîte noire précédents par les modèles transmis.</span><span class="sxs-lookup"><span data-stu-id="5722b-281">Replace previous blackbox patterns with passed ones.</span></span>  <span data-ttu-id="5722b-282">Force le back-end à ignorer la mise en pause/pas à pas dans les scripts avec une URL correspondant à l’un des modèles.</span><span class="sxs-lookup"><span data-stu-id="5722b-282">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span>  <span data-ttu-id="5722b-283">Le débompeur essaiera de laisser un script en boîte noire en le faisant plusieurs fois, en y recourant en `step in` `step out` cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="5722b-283">The debugger will try to leave blackboxed script by performing `step in` several times, finally resorting to `step out` if unsuccessful.</span></span>  

| <span data-ttu-id="5722b-284">Parameters</span><span class="sxs-lookup"><span data-stu-id="5722b-284">Parameters</span></span> | <span data-ttu-id="5722b-285">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-285">Type</span></span> | <span data-ttu-id="5722b-286">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-286">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-287">patterns</span><span class="sxs-lookup"><span data-stu-id="5722b-287">patterns</span></span> | `string[]` | <span data-ttu-id="5722b-288">Tableau de regexps qui sera utilisé pour vérifier l’état de boîte aux lettres noire de l’URL du script.</span><span class="sxs-lookup"><span data-stu-id="5722b-288">Array of regexps that will be used to check script url for blackbox state.</span></span> |  

---  

### <a name="mssetdebuggerpropertyvalue"></a><span data-ttu-id="5722b-289">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="5722b-289">msSetDebuggerPropertyValue</span></span>  

<span data-ttu-id="5722b-290">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="5722b-290">**Experimental**.</span></span>  <span data-ttu-id="5722b-291">Microsoft : définit la propriété spécifiée du débogger sur la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5722b-291">Microsoft:  Sets the specified debugger property to the specified value.</span></span>  

| <span data-ttu-id="5722b-292">Parameters</span><span class="sxs-lookup"><span data-stu-id="5722b-292">Parameters</span></span> | <span data-ttu-id="5722b-293">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-293">Type</span></span> | <span data-ttu-id="5722b-294">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-294">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-295">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="5722b-295">debuggerPropertyId</span></span> | `string` | <span data-ttu-id="5722b-296">Microsoft : ID de propriété \(c’est-à-dire msDebuggerPropertyId\) à définir.</span><span class="sxs-lookup"><span data-stu-id="5722b-296">Microsoft: The property ID \(i.e. msDebuggerPropertyId\) to set.</span></span> |  
| <span data-ttu-id="5722b-297">newValue</span><span class="sxs-lookup"><span data-stu-id="5722b-297">newValue</span></span> | `string` | &nbsp; |  

---  

## <a name="events"></a><span data-ttu-id="5722b-298">Événements</span><span class="sxs-lookup"><span data-stu-id="5722b-298">Events</span></span>  

### <a name="scriptparsed"></a><span data-ttu-id="5722b-299">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="5722b-299">scriptParsed</span></span>  

<span data-ttu-id="5722b-300">Déclenché lorsque le script est interrogé.</span><span class="sxs-lookup"><span data-stu-id="5722b-300">Fired when the script is parsed.</span></span>  <span data-ttu-id="5722b-301">Cet événement est également déclenché pour tous les scripts connus et non récollects lors de l’activation du débogueur.</span><span class="sxs-lookup"><span data-stu-id="5722b-301">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>  

| <span data-ttu-id="5722b-302">Parameters</span><span class="sxs-lookup"><span data-stu-id="5722b-302">Parameters</span></span> | <span data-ttu-id="5722b-303">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-303">Type</span></span> | <span data-ttu-id="5722b-304">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-304">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-305">scriptId</span><span class="sxs-lookup"><span data-stu-id="5722b-305">scriptId</span></span> | [<span data-ttu-id="5722b-306">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="5722b-306">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="5722b-307">Identificateur du script en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="5722b-307">Identifier of the script parsed.</span></span> |  
| <span data-ttu-id="5722b-308">url</span><span class="sxs-lookup"><span data-stu-id="5722b-308">url</span></span> | `string` | <span data-ttu-id="5722b-309">URL ou nom du script lu \(le caser\).</span><span class="sxs-lookup"><span data-stu-id="5722b-309">URL or name of the script parsed \(if any\).</span></span> |  
| <span data-ttu-id="5722b-310">startLine</span><span class="sxs-lookup"><span data-stu-id="5722b-310">startLine</span></span> | `integer` | <span data-ttu-id="5722b-311">Décalage de ligne du script dans la ressource avec une URL donnée \(pour les balises de script\).</span><span class="sxs-lookup"><span data-stu-id="5722b-311">Line offset of the script within the resource with given URL \(for script tags\).</span></span> |  
| <span data-ttu-id="5722b-312">startColumn</span><span class="sxs-lookup"><span data-stu-id="5722b-312">startColumn</span></span> | `integer` | <span data-ttu-id="5722b-313">Décalage de colonne du script dans la ressource avec une URL donnée.</span><span class="sxs-lookup"><span data-stu-id="5722b-313">Column offset of the script within the resource with given URL.</span></span> |  
| <span data-ttu-id="5722b-314">endLine</span><span class="sxs-lookup"><span data-stu-id="5722b-314">endLine</span></span> | `integer` | <span data-ttu-id="5722b-315">Dernière ligne du script.</span><span class="sxs-lookup"><span data-stu-id="5722b-315">Last line of the script.</span></span> |  
| <span data-ttu-id="5722b-316">endColumn</span><span class="sxs-lookup"><span data-stu-id="5722b-316">endColumn</span></span> | `integer` | <span data-ttu-id="5722b-317">Longueur de la dernière ligne du script.</span><span class="sxs-lookup"><span data-stu-id="5722b-317">Length of the last line of the script.</span></span> |  
| <span data-ttu-id="5722b-318">executionContextId</span><span class="sxs-lookup"><span data-stu-id="5722b-318">executionContextId</span></span> | [<span data-ttu-id="5722b-319">Runtime.ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="5722b-319">Runtime.ExecutionContextId</span></span>](./runtime.md#executioncontextid) | <span data-ttu-id="5722b-320">Spécifie le contexte de création de script.</span><span class="sxs-lookup"><span data-stu-id="5722b-320">Specifies script creation context.</span></span> |  
| <span data-ttu-id="5722b-321">sourceMapURL \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="5722b-321">sourceMapURL  \(optional\)</span></span> | `string` | <span data-ttu-id="5722b-322">URL de la carte source associée au script (le cas cas).</span><span class="sxs-lookup"><span data-stu-id="5722b-322">URL of source map associated with script (if any).</span></span> |  
| <span data-ttu-id="5722b-323">length \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-323">length  \(optional\)</span></span> | `integer` | <span data-ttu-id="5722b-324">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="5722b-324">**Experimental**.</span></span>  <span data-ttu-id="5722b-325">Longueur du script.</span><span class="sxs-lookup"><span data-stu-id="5722b-325">This script length.</span></span> |  
| <span data-ttu-id="5722b-326">msParentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-326">msParentId  \(optional\)</span></span> | `string` | <span data-ttu-id="5722b-327">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="5722b-327">**Experimental**.</span></span>  <span data-ttu-id="5722b-328">Il s’agit de l’ID de document parent.</span><span class="sxs-lookup"><span data-stu-id="5722b-328">This is the parent document ID.</span></span> |  
| <span data-ttu-id="5722b-329">msMimeType \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-329">msMimeType  \(optional\)</span></span> | `string` | <span data-ttu-id="5722b-330">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="5722b-330">**Experimental**.</span></span>  <span data-ttu-id="5722b-331">Il s’agit du type mime.</span><span class="sxs-lookup"><span data-stu-id="5722b-331">This is the mime type.</span></span> |  
| <span data-ttu-id="5722b-332">msIsDynamicCode \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-332">msIsDynamicCode  \(optional\)</span></span> | `boolean` | <span data-ttu-id="5722b-333">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="5722b-333">**Experimental**.</span></span>  <span data-ttu-id="5722b-334">Cela indique s’il s’agit d’un code dynamique.</span><span class="sxs-lookup"><span data-stu-id="5722b-334">This indicates whether it is dynamic code.</span></span> |  
| <span data-ttu-id="5722b-335">msLongDocumentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-335">msLongDocumentId  \(optional\)</span></span> | `integer` | <span data-ttu-id="5722b-336">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="5722b-336">**Experimental**.</span></span>  <span data-ttu-id="5722b-337">Il s’agit de l’ID de document long.</span><span class="sxs-lookup"><span data-stu-id="5722b-337">This is the long document ID.</span></span> |  

---  

### <a name="breakpointresolved"></a><span data-ttu-id="5722b-338">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="5722b-338">breakpointResolved</span></span>  

<span data-ttu-id="5722b-339">Déclenché lorsque le point d’arrêt est résolu en un script et un emplacement réels.</span><span class="sxs-lookup"><span data-stu-id="5722b-339">Fired when breakpoint is resolved to an actual script and location.</span></span>  

| <span data-ttu-id="5722b-340">Parameters</span><span class="sxs-lookup"><span data-stu-id="5722b-340">Parameters</span></span> | <span data-ttu-id="5722b-341">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-341">Type</span></span> | <span data-ttu-id="5722b-342">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-342">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-343">breakpointId</span><span class="sxs-lookup"><span data-stu-id="5722b-343">breakpointId</span></span> | [<span data-ttu-id="5722b-344">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="5722b-344">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="5722b-345">Identificateur unique de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5722b-345">Breakpoint unique identifier.</span></span> |  
| <span data-ttu-id="5722b-346">location</span><span class="sxs-lookup"><span data-stu-id="5722b-346">location</span></span> | [<span data-ttu-id="5722b-347">Emplacement</span><span class="sxs-lookup"><span data-stu-id="5722b-347">Location</span></span>](#location) | <span data-ttu-id="5722b-348">Emplacement réel du point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5722b-348">Actual breakpoint location.</span></span> |  
| <span data-ttu-id="5722b-349">msLength \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-349">msLength  \(optional\)</span></span> | `integer` | <span data-ttu-id="5722b-350">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="5722b-350">**Experimental**.</span></span>  <span data-ttu-id="5722b-351">Microsoft : Longueur du code \(nombre de caractères\) à l’emplacement du point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5722b-351">Microsoft:  Length of code \(i.e. number of characters\) at the breakpoint location.</span></span> |  

---  

### <a name="paused"></a><span data-ttu-id="5722b-352">en pause</span><span class="sxs-lookup"><span data-stu-id="5722b-352">paused</span></span>  

<span data-ttu-id="5722b-353">Déclenché lorsque les déboggers se cassent pour un point d’arrêt ou une exception.</span><span class="sxs-lookup"><span data-stu-id="5722b-353">Fired when the debuggers breaks for a breakpoint or exception.</span></span>  

| <span data-ttu-id="5722b-354">Parameters</span><span class="sxs-lookup"><span data-stu-id="5722b-354">Parameters</span></span> | <span data-ttu-id="5722b-355">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-355">Type</span></span> | <span data-ttu-id="5722b-356">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-356">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-357">callFrames</span><span class="sxs-lookup"><span data-stu-id="5722b-357">callFrames</span></span> | [<span data-ttu-id="5722b-358">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="5722b-358">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="5722b-359">Pile d’appels où le débogger s’est arrêté.</span><span class="sxs-lookup"><span data-stu-id="5722b-359">Call stack the debugger stopped on.</span></span> |  
| <span data-ttu-id="5722b-360">reason</span><span class="sxs-lookup"><span data-stu-id="5722b-360">reason</span></span> | `string` | <span data-ttu-id="5722b-361">Motif de l’interruption.</span><span class="sxs-lookup"><span data-stu-id="5722b-361">Pause reason.</span></span>  <span data-ttu-id="5722b-362">Valeurs autorisées  `breakpoint` : , `step` `exception` et</span><span class="sxs-lookup"><span data-stu-id="5722b-362">Allowed values:  `breakpoint`, `step`, `exception`, and</span></span> `other` |  
| <span data-ttu-id="5722b-363">data \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-363">data  \(optional\)</span></span> | `object` | <span data-ttu-id="5722b-364">Objet contenant des propriétés auxiliaires spécifiques aux coupures.</span><span class="sxs-lookup"><span data-stu-id="5722b-364">Object containing break-specific auxiliary properties.</span></span> |  
| <span data-ttu-id="5722b-365">hitBreakpoints \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="5722b-365">hitBreakpoints  \(optional\)</span></span> | `string[]` | <span data-ttu-id="5722b-366">ID des points d’arrêt d’arrêt</span><span class="sxs-lookup"><span data-stu-id="5722b-366">Hit breakpoints IDs</span></span> |  

---  

### <a name="resumed"></a><span data-ttu-id="5722b-367">reprise</span><span class="sxs-lookup"><span data-stu-id="5722b-367">resumed</span></span>  

<span data-ttu-id="5722b-368">Déclenché lorsque le débogger reprend l’exécution.</span><span class="sxs-lookup"><span data-stu-id="5722b-368">Fired when the debugger resumes execution.</span></span>  

&nbsp;  

---  

## <a name="types"></a><span data-ttu-id="5722b-369">Types</span><span class="sxs-lookup"><span data-stu-id="5722b-369">Types</span></span>  

### <a name="breakpointid-string"></a><span data-ttu-id="5722b-370">Chaîne BreakpointId</span><span class="sxs-lookup"><span data-stu-id="5722b-370">BreakpointId string</span></span>  

<a name="breakpointid"></a>  

<span data-ttu-id="5722b-371">Identificateur de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5722b-371">Breakpoint identifier.</span></span>  

&nbsp;  

---  

### <a name="callframeid-string"></a><span data-ttu-id="5722b-372">Chaîne CallFrameId</span><span class="sxs-lookup"><span data-stu-id="5722b-372">CallFrameId string</span></span>  

<a name="callframeid"></a>  

<span data-ttu-id="5722b-373">Identificateur d’image d’appel.</span><span class="sxs-lookup"><span data-stu-id="5722b-373">Call frame identifier.</span></span>  

&nbsp;  

---  

### <a name="location-object"></a><span data-ttu-id="5722b-374">Location, objet</span><span class="sxs-lookup"><span data-stu-id="5722b-374">Location object</span></span>  

<a name="location"></a>  

<span data-ttu-id="5722b-375">Emplacement dans le code source.</span><span class="sxs-lookup"><span data-stu-id="5722b-375">Location in the source code.</span></span>  

| <span data-ttu-id="5722b-376">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5722b-376">Properties</span></span> | <span data-ttu-id="5722b-377">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-377">Type</span></span> | <span data-ttu-id="5722b-378">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-378">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-379">scriptId</span><span class="sxs-lookup"><span data-stu-id="5722b-379">scriptId</span></span> | [<span data-ttu-id="5722b-380">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="5722b-380">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="5722b-381">Identificateur de script tel qu’indiqué dans `Debugger.scriptParsed` le .</span><span class="sxs-lookup"><span data-stu-id="5722b-381">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="5722b-382">lineNumber</span><span class="sxs-lookup"><span data-stu-id="5722b-382">lineNumber</span></span> | `integer` | <span data-ttu-id="5722b-383">Numéro de ligne dans le script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="5722b-383">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="5722b-384">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-384">columnNumber  \(optional\)</span></span> | `integer` | <span data-ttu-id="5722b-385">Numéro de colonne dans le script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="5722b-385">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="5722b-386">msLength</span><span class="sxs-lookup"><span data-stu-id="5722b-386">msLength</span></span> | `integer` | <span data-ttu-id="5722b-387">Microsoft : Longueur du code \(c’est-à-dire le nombre de caractères\) à ce cadre d’appel.</span><span class="sxs-lookup"><span data-stu-id="5722b-387">Microsoft: Length of code \(i.e. number of characters\) at this call frame.</span></span> |  

---  

### <a name="breaklocation-object"></a><span data-ttu-id="5722b-388">Objet BreakLocation</span><span class="sxs-lookup"><span data-stu-id="5722b-388">BreakLocation object</span></span>  

<a name="breaklocation"></a>  

<span data-ttu-id="5722b-389">Emplacement de rupture dans le code source.</span><span class="sxs-lookup"><span data-stu-id="5722b-389">Break location in the source code.</span></span>  

| <span data-ttu-id="5722b-390">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5722b-390">Properties</span></span> | <span data-ttu-id="5722b-391">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-391">Type</span></span> | <span data-ttu-id="5722b-392">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-392">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-393">scriptId</span><span class="sxs-lookup"><span data-stu-id="5722b-393">scriptId</span></span> | [<span data-ttu-id="5722b-394">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="5722b-394">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="5722b-395">Identificateur de script tel qu’indiqué dans `Debugger.scriptParsed` le .</span><span class="sxs-lookup"><span data-stu-id="5722b-395">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="5722b-396">lineNumber</span><span class="sxs-lookup"><span data-stu-id="5722b-396">lineNumber</span></span> | `integer` | <span data-ttu-id="5722b-397">Numéro de ligne dans le script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="5722b-397">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="5722b-398">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-398">columnNumber  \(optional\)</span></span> | `integer` | <span data-ttu-id="5722b-399">Numéro de colonne dans le script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="5722b-399">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="5722b-400">msLength</span><span class="sxs-lookup"><span data-stu-id="5722b-400">msLength</span></span> | `integer` | <span data-ttu-id="5722b-401">Microsoft : Longueur du code \(c’est-à-dire le nombre de caractères\) à ce cadre d’appel.</span><span class="sxs-lookup"><span data-stu-id="5722b-401">Microsoft:  Length of code \(i.e. number of characters\) at this call frame.</span></span> |  
| <span data-ttu-id="5722b-402">type \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-402">type  \(optional\)</span></span> | `string` | <span data-ttu-id="5722b-403">Valeurs autorisées  `debuggerStatement` : `call` , et</span><span class="sxs-lookup"><span data-stu-id="5722b-403">Allowed values:  `debuggerStatement`, `call`, and</span></span> `return` |  

---  

### <a name="callframe-object"></a><span data-ttu-id="5722b-404">Objet CallFrame</span><span class="sxs-lookup"><span data-stu-id="5722b-404">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="5722b-405">Image d’appel JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5722b-405">JavaScript call frame.</span></span>  <span data-ttu-id="5722b-406">Un tableau de cadres d’appel forme la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="5722b-406">Array of call frames form the call stack.</span></span>  

| <span data-ttu-id="5722b-407">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5722b-407">Properties</span></span> | <span data-ttu-id="5722b-408">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-408">Type</span></span> | <span data-ttu-id="5722b-409">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-409">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-410">callFrameId</span><span class="sxs-lookup"><span data-stu-id="5722b-410">callFrameId</span></span> | [<span data-ttu-id="5722b-411">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="5722b-411">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="5722b-412">Identificateur d’image d’appel.</span><span class="sxs-lookup"><span data-stu-id="5722b-412">Call frame identifier.</span></span>  <span data-ttu-id="5722b-413">Cet identificateur n’est valide que lorsque le débogger est suspendu.</span><span class="sxs-lookup"><span data-stu-id="5722b-413">This identifier is only valid while the debugger is paused.</span></span> |  
| <span data-ttu-id="5722b-414">functionName</span><span class="sxs-lookup"><span data-stu-id="5722b-414">functionName</span></span> | `string` | <span data-ttu-id="5722b-415">Nom de la fonction JavaScript appelée sur ce cadre d’appel.</span><span class="sxs-lookup"><span data-stu-id="5722b-415">Name of the JavaScript function called on this call frame.</span></span> |  
| <span data-ttu-id="5722b-416">functionLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-416">functionLocation  \(optional\)</span></span> | [<span data-ttu-id="5722b-417">Emplacement</span><span class="sxs-lookup"><span data-stu-id="5722b-417">Location</span></span>](#location) | <span data-ttu-id="5722b-418">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="5722b-418">**Experimental**.</span></span>  <span data-ttu-id="5722b-419">Emplacement dans le code source.</span><span class="sxs-lookup"><span data-stu-id="5722b-419">Location in the source code.</span></span> |  
| <span data-ttu-id="5722b-420">location</span><span class="sxs-lookup"><span data-stu-id="5722b-420">location</span></span> | [<span data-ttu-id="5722b-421">Emplacement</span><span class="sxs-lookup"><span data-stu-id="5722b-421">Location</span></span>](#location) | <span data-ttu-id="5722b-422">Emplacement dans le code source.</span><span class="sxs-lookup"><span data-stu-id="5722b-422">Location in the source code.</span></span> |  
| <span data-ttu-id="5722b-423">url</span><span class="sxs-lookup"><span data-stu-id="5722b-423">url</span></span> | `string` | <span data-ttu-id="5722b-424">Nom ou URL du script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5722b-424">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="5722b-425">scopeChain</span><span class="sxs-lookup"><span data-stu-id="5722b-425">scopeChain</span></span> | [<span data-ttu-id="5722b-426">Scope[]</span><span class="sxs-lookup"><span data-stu-id="5722b-426">Scope[]</span></span>](#scope) | <span data-ttu-id="5722b-427">Chaîne d’étendue pour ce cadre d’appel.</span><span class="sxs-lookup"><span data-stu-id="5722b-427">Scope chain for this call frame.</span></span> |  
| <span data-ttu-id="5722b-428">this</span><span class="sxs-lookup"><span data-stu-id="5722b-428">this</span></span> | [<span data-ttu-id="5722b-429">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="5722b-429">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | `this` <span data-ttu-id="5722b-430">pour ce cadre d’appel.</span><span class="sxs-lookup"><span data-stu-id="5722b-430">object for this call frame.</span></span> |  
| <span data-ttu-id="5722b-431">returnValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-431">returnValue  \(optional\)</span></span> | [<span data-ttu-id="5722b-432">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="5722b-432">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="5722b-433">Valeur renvoyée, si la fonction est au point de retour.</span><span class="sxs-lookup"><span data-stu-id="5722b-433">The value being returned, if the function is at return point.</span></span> |  

---  

### <a name="scope-object"></a><span data-ttu-id="5722b-434">Objet Scope</span><span class="sxs-lookup"><span data-stu-id="5722b-434">Scope object</span></span>  

<a name="scope"></a>  

<span data-ttu-id="5722b-435">Description de l’étendue.</span><span class="sxs-lookup"><span data-stu-id="5722b-435">Scope description.</span></span>  

| <span data-ttu-id="5722b-436">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5722b-436">Properties</span></span> | <span data-ttu-id="5722b-437">Type</span><span class="sxs-lookup"><span data-stu-id="5722b-437">Type</span></span> | <span data-ttu-id="5722b-438">Détails</span><span class="sxs-lookup"><span data-stu-id="5722b-438">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5722b-439">type</span><span class="sxs-lookup"><span data-stu-id="5722b-439">type</span></span> | `string` | <span data-ttu-id="5722b-440">Type d’étendue.</span><span class="sxs-lookup"><span data-stu-id="5722b-440">Scope type.</span></span>  <span data-ttu-id="5722b-441">Valeurs autorisées  `global` : , , , , , `local` , `with` `closure` `catch` `block` `script` `eval` et</span><span class="sxs-lookup"><span data-stu-id="5722b-441">Allowed values:  `global`, `local`, `with`, `closure`, `catch`, `block`, `script`, `eval`, and</span></span> `module` |  
| <span data-ttu-id="5722b-442">object</span><span class="sxs-lookup"><span data-stu-id="5722b-442">object</span></span> | [<span data-ttu-id="5722b-443">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="5722b-443">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="5722b-444">Objet représentant l’étendue.</span><span class="sxs-lookup"><span data-stu-id="5722b-444">Object representing the scope.</span></span>  <span data-ttu-id="5722b-445">Pour et les étendues, il représente l’objet réel ; pour le reste des étendues, il s’agit d’objets temporaires artificielles qui édent les variables d’étendue en tant `global` `with` que propriétés.</span><span class="sxs-lookup"><span data-stu-id="5722b-445">For `global` and `with` scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span> |  
| <span data-ttu-id="5722b-446">name \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-446">name  \(optional\)</span></span> | `string` | &nbsp; |  
| <span data-ttu-id="5722b-447">startLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-447">startLocation  \(optional\)</span></span> | [<span data-ttu-id="5722b-448">Emplacement</span><span class="sxs-lookup"><span data-stu-id="5722b-448">Location</span></span>](#location) | <span data-ttu-id="5722b-449">Emplacement dans le code source où commence l’étendue.</span><span class="sxs-lookup"><span data-stu-id="5722b-449">Location in the source code where scope starts.</span></span> |  
| <span data-ttu-id="5722b-450">endLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="5722b-450">endLocation  \(optional\)</span></span> | [<span data-ttu-id="5722b-451">Emplacement</span><span class="sxs-lookup"><span data-stu-id="5722b-451">Location</span></span>](#location) | <span data-ttu-id="5722b-452">Emplacement dans le code source où l’étendue se termine.</span><span class="sxs-lookup"><span data-stu-id="5722b-452">Location in the source code where scope ends.</span></span> |  

---  

## <a name="dependencies"></a><span data-ttu-id="5722b-453">Dépendances</span><span class="sxs-lookup"><span data-stu-id="5722b-453">Dependencies</span></span>  

[<span data-ttu-id="5722b-454">Runtime</span><span class="sxs-lookup"><span data-stu-id="5722b-454">Runtime</span></span>](./runtime.md)  
