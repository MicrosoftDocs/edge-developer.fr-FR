---
description: Référence du protocole DevTools Version 0.2 (EdgeHTML) pour le domaine du débogueur. Le domaine du déboguer expose les fonctionnalités de débogage JavaScript. Il permet de définir et de supprimer des points d’arrêt, d’exécuter pas à pas, d’explorer les traces de pile, etc.
title: Domaine du débogueur - DevTools Protocol Version 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 00c410812edd4d11e9904a489955e7fd218a7e5d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398174"
---
# <a name="debugger-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="66e7f-105">Domaine du débogueur - DevTools Protocol Version 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="66e7f-105">Debugger Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="66e7f-106">Le domaine du déboguer expose les fonctionnalités de débogage JavaScript.</span><span class="sxs-lookup"><span data-stu-id="66e7f-106">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="66e7f-107">Il permet de définir et de supprimer des points d’arrêt, d’exécuter pas à pas, d’explorer les traces de pile, etc.</span><span class="sxs-lookup"><span data-stu-id="66e7f-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| <span data-ttu-id="66e7f-108">Classification</span><span class="sxs-lookup"><span data-stu-id="66e7f-108">Classification</span></span> | <span data-ttu-id="66e7f-109">Membres</span><span class="sxs-lookup"><span data-stu-id="66e7f-109">Members</span></span> |  
|:--- |:--- |  
| [**<span data-ttu-id="66e7f-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="66e7f-110">Methods</span></span>**](#methods) | <span data-ttu-id="66e7f-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue) [](#stepout)</span><span class="sxs-lookup"><span data-stu-id="66e7f-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |  
| [**<span data-ttu-id="66e7f-112">Événements</span><span class="sxs-lookup"><span data-stu-id="66e7f-112">Events</span></span>**](#events) | <span data-ttu-id="66e7f-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span><span class="sxs-lookup"><span data-stu-id="66e7f-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |  
| [**<span data-ttu-id="66e7f-114">Types</span><span class="sxs-lookup"><span data-stu-id="66e7f-114">Types</span></span>**](#types) | <span data-ttu-id="66e7f-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span><span class="sxs-lookup"><span data-stu-id="66e7f-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |  
| [**<span data-ttu-id="66e7f-116">Dépendances</span><span class="sxs-lookup"><span data-stu-id="66e7f-116">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="66e7f-117">Runtime</span><span class="sxs-lookup"><span data-stu-id="66e7f-117">Runtime</span></span>](./runtime.md) |  

## <a name="methods"></a><span data-ttu-id="66e7f-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="66e7f-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="66e7f-119">activer</span><span class="sxs-lookup"><span data-stu-id="66e7f-119">enable</span></span>  

<span data-ttu-id="66e7f-120">Active le débogger pour la page donnée.</span><span class="sxs-lookup"><span data-stu-id="66e7f-120">Enables debugger for the given page.</span></span> <span data-ttu-id="66e7f-121">Les clients ne doivent pas supposer que le débogage a été activé jusqu’à ce que le résultat de cette commande soit reçu.</span><span class="sxs-lookup"><span data-stu-id="66e7f-121">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="66e7f-122">désactiver </span><span class="sxs-lookup"><span data-stu-id="66e7f-122">disable</span></span>  

<span data-ttu-id="66e7f-123">Désactive le débogger pour une page donnée.</span><span class="sxs-lookup"><span data-stu-id="66e7f-123">Disables debugger for given page.</span></span>  

&nbsp;  

---  

### <a name="getpossiblebreakpoints"></a><span data-ttu-id="66e7f-124">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="66e7f-124">getPossibleBreakpoints</span></span>  

<span data-ttu-id="66e7f-125">Renvoie les emplacements possibles pour le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="66e7f-125">Returns possible locations for breakpoint.</span></span> <span data-ttu-id="66e7f-126">ScriptId dans les emplacements de plage de début et de fin doit être identique.</span><span class="sxs-lookup"><span data-stu-id="66e7f-126">scriptId in start and end range locations should be the same.</span></span>  

| <span data-ttu-id="66e7f-127">Parameters</span><span class="sxs-lookup"><span data-stu-id="66e7f-127">Parameters</span></span> | <span data-ttu-id="66e7f-128">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-128">Type</span></span> | <span data-ttu-id="66e7f-129">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-129">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-130">start</span><span class="sxs-lookup"><span data-stu-id="66e7f-130">start</span></span> | [<span data-ttu-id="66e7f-131">Emplacement</span><span class="sxs-lookup"><span data-stu-id="66e7f-131">Location</span></span>](#location) | <span data-ttu-id="66e7f-132">Début de la plage pour rechercher les emplacements de points d’arrêt possibles.</span><span class="sxs-lookup"><span data-stu-id="66e7f-132">Start of range to search possible breakpoint locations in.</span></span> |  
| <span data-ttu-id="66e7f-133">terminer</span><span class="sxs-lookup"><span data-stu-id="66e7f-133">end</span></span> | [<span data-ttu-id="66e7f-134">Emplacement</span><span class="sxs-lookup"><span data-stu-id="66e7f-134">Location</span></span>](#location) | <span data-ttu-id="66e7f-135">Fin de la plage pour rechercher les emplacements de points d’arrêt possibles dans \(à l’exclusion de\).</span><span class="sxs-lookup"><span data-stu-id="66e7f-135">End of range to search possible breakpoint locations in \(excluding\).</span></span>  <span data-ttu-id="66e7f-136">Lorsqu’il n’est pas spécifié, la fin des scripts est utilisée comme fin de plage.</span><span class="sxs-lookup"><span data-stu-id="66e7f-136">When not specified, end of scripts is used as end of range.</span></span> |  

| <span data-ttu-id="66e7f-137">Renvoie</span><span class="sxs-lookup"><span data-stu-id="66e7f-137">Returns</span></span> | <span data-ttu-id="66e7f-138">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-138">Type</span></span> | <span data-ttu-id="66e7f-139">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-139">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-140">emplacements</span><span class="sxs-lookup"><span data-stu-id="66e7f-140">locations</span></span> | [<span data-ttu-id="66e7f-141">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="66e7f-141">BreakLocation</span></span>](#breaklocation) | <span data-ttu-id="66e7f-142">Liste des emplacements de points d’arrêt possibles.</span><span class="sxs-lookup"><span data-stu-id="66e7f-142">List of the possible breakpoint locations.</span></span> |  

---  

### <a name="setbreakpointsactive"></a><span data-ttu-id="66e7f-143">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="66e7f-143">setBreakpointsActive</span></span>  

<span data-ttu-id="66e7f-144">Active/désactive tous les points d’arrêt sur la page.</span><span class="sxs-lookup"><span data-stu-id="66e7f-144">Activates / deactivates all breakpoints on the page.</span></span>  

| <span data-ttu-id="66e7f-145">Parameters</span><span class="sxs-lookup"><span data-stu-id="66e7f-145">Parameters</span></span> | <span data-ttu-id="66e7f-146">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-146">Type</span></span> | <span data-ttu-id="66e7f-147">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-147">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-148">active</span><span class="sxs-lookup"><span data-stu-id="66e7f-148">active</span></span> | `boolean` | <span data-ttu-id="66e7f-149">Nouvelle valeur pour l’état actif des points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="66e7f-149">New value for breakpoints active state.</span></span> | 

---  

### <a name="setbreakpointbyurl"></a><span data-ttu-id="66e7f-150">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="66e7f-150">setBreakpointByUrl</span></span>  

<span data-ttu-id="66e7f-151">Définit le point d’arrêt JavaScript à un emplacement donné spécifié par l’URL ou l’URL regex.</span><span class="sxs-lookup"><span data-stu-id="66e7f-151">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span>  <span data-ttu-id="66e7f-152">Une fois cette commande émise, tous les scripts d’évaluation existants ont des points d’arrêt résolus et renvoyés dans la `locations` propriété.</span><span class="sxs-lookup"><span data-stu-id="66e7f-152">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in `locations` property.</span></span>  <span data-ttu-id="66e7f-153">Une autre correspondance de l’examen des scripts entraîne l’émission `breakpointResolved` d’événements ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="66e7f-153">Further matching script parsing will result in subsequent `breakpointResolved` events issued.</span></span>  <span data-ttu-id="66e7f-154">Ce point d’arrêt logique survivra au rechargement des pages.</span><span class="sxs-lookup"><span data-stu-id="66e7f-154">This logical breakpoint will survive page reloads.</span></span>  

| <span data-ttu-id="66e7f-155">Parameters</span><span class="sxs-lookup"><span data-stu-id="66e7f-155">Parameters</span></span> | <span data-ttu-id="66e7f-156">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-156">Type</span></span> | <span data-ttu-id="66e7f-157">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-157">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-158">lineNumber</span><span class="sxs-lookup"><span data-stu-id="66e7f-158">lineNumber</span></span> | `integer` | <span data-ttu-id="66e7f-159">Numéro de ligne sur le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="66e7f-159">Line number to set breakpoint at.</span></span> | 
| <span data-ttu-id="66e7f-160">url \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-160">url \(optional\)</span></span> | `string` | <span data-ttu-id="66e7f-161">URL des ressources pour définir le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="66e7f-161">URL of the resources to set breakpoint on.</span></span> |  
| <span data-ttu-id="66e7f-162">urlRegex \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-162">urlRegex \(optional\)</span></span> | `string` | <span data-ttu-id="66e7f-163">Modèle d’regex pour les URL des ressources sur les points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="66e7f-163">Regex pattern for the URLs of the resources to set breakpoints on.</span></span>  <span data-ttu-id="66e7f-164">`url` `urlRegex` L’un ou l’autre doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="66e7f-164">Either `url` or `urlRegex` must be specified.</span></span> |  
| <span data-ttu-id="66e7f-165">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-165">columnNumber \(optional\)</span></span> | `integer` | <span data-ttu-id="66e7f-166">Décalez la ligne pour définir le point d’arrêt sur.</span><span class="sxs-lookup"><span data-stu-id="66e7f-166">Offset in the line to set breakpoint at.</span></span> |  
| <span data-ttu-id="66e7f-167">condition \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-167">condition \(optional\)</span></span> | `string` | <span data-ttu-id="66e7f-168">Expression à utiliser comme condition de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="66e7f-168">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="66e7f-169">Lorsqu’il est spécifié, le débogger s’arrête uniquement sur le point d’arrêt si cette expression est évaluée à true.</span><span class="sxs-lookup"><span data-stu-id="66e7f-169">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="66e7f-170">Renvoie</span><span class="sxs-lookup"><span data-stu-id="66e7f-170">Returns</span></span> | <span data-ttu-id="66e7f-171">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-171">Type</span></span> | <span data-ttu-id="66e7f-172">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-172">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-173">breakpointId</span><span class="sxs-lookup"><span data-stu-id="66e7f-173">breakpointId</span></span> | [<span data-ttu-id="66e7f-174">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="66e7f-174">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="66e7f-175">ID du point d’arrêt créé pour référence supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="66e7f-175">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="66e7f-176">emplacements</span><span class="sxs-lookup"><span data-stu-id="66e7f-176">locations</span></span> | [<span data-ttu-id="66e7f-177">Location[]</span><span class="sxs-lookup"><span data-stu-id="66e7f-177">Location[]</span></span>](#location) | <span data-ttu-id="66e7f-178">Liste des emplacements où ce point d’arrêt a été résolu lors de l’ajout.</span><span class="sxs-lookup"><span data-stu-id="66e7f-178">List of the locations this breakpoint resolved into upon addition.</span></span> |  

---  

### <a name="setbreakpoint"></a><span data-ttu-id="66e7f-179">setBreakpoint</span><span class="sxs-lookup"><span data-stu-id="66e7f-179">setBreakpoint</span></span>  

<span data-ttu-id="66e7f-180">Définit le point d’arrêt JavaScript à un emplacement donné.</span><span class="sxs-lookup"><span data-stu-id="66e7f-180">Sets JavaScript breakpoint at a given location.</span></span>  

| <span data-ttu-id="66e7f-181">Parameters</span><span class="sxs-lookup"><span data-stu-id="66e7f-181">Parameters</span></span> | <span data-ttu-id="66e7f-182">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-182">Type</span></span> | <span data-ttu-id="66e7f-183">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-183">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-184">location</span><span class="sxs-lookup"><span data-stu-id="66e7f-184">location</span></span> | [<span data-ttu-id="66e7f-185">Emplacement</span><span class="sxs-lookup"><span data-stu-id="66e7f-185">Location</span></span>](#location) | <span data-ttu-id="66e7f-186">Emplacement dans le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="66e7f-186">Location to set breakpoint in.</span></span> |  
| <span data-ttu-id="66e7f-187">condition \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-187">condition \(optional\)</span></span> | `string` | <span data-ttu-id="66e7f-188">Expression à utiliser comme condition de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="66e7f-188">Expression to use as a breakpoint condition.</span></span>  <span data-ttu-id="66e7f-189">Lorsqu’il est spécifié, le débogger s’arrête uniquement sur le point d’arrêt si cette expression est évaluée à true.</span><span class="sxs-lookup"><span data-stu-id="66e7f-189">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="66e7f-190">Renvoie</span><span class="sxs-lookup"><span data-stu-id="66e7f-190">Returns</span></span> | <span data-ttu-id="66e7f-191">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-191">Type</span></span> | <span data-ttu-id="66e7f-192">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-192">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-193">breakpointId</span><span class="sxs-lookup"><span data-stu-id="66e7f-193">breakpointId</span></span> | [<span data-ttu-id="66e7f-194">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="66e7f-194">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="66e7f-195">ID du point d’arrêt créé pour référence supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="66e7f-195">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="66e7f-196">actualLocation</span><span class="sxs-lookup"><span data-stu-id="66e7f-196">actualLocation</span></span> | [<span data-ttu-id="66e7f-197">Emplacement</span><span class="sxs-lookup"><span data-stu-id="66e7f-197">Location</span></span>](#location) | <span data-ttu-id="66e7f-198">Emplacement où ce point d’arrêt a été résolu.</span><span class="sxs-lookup"><span data-stu-id="66e7f-198">Location this breakpoint resolved into.</span></span> |  

---  

### <a name="removebreakpoint"></a><span data-ttu-id="66e7f-199">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="66e7f-199">removeBreakpoint</span></span>  

<span data-ttu-id="66e7f-200">Supprime le point d’arrêt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="66e7f-200">Removes JavaScript breakpoint.</span></span>  

| <span data-ttu-id="66e7f-201">Parameters</span><span class="sxs-lookup"><span data-stu-id="66e7f-201">Parameters</span></span> | <span data-ttu-id="66e7f-202">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-202">Type</span></span> | <span data-ttu-id="66e7f-203">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-203">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-204">breakpointId</span><span class="sxs-lookup"><span data-stu-id="66e7f-204">breakpointId</span></span> | [<span data-ttu-id="66e7f-205">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="66e7f-205">BreakpointId</span></span>](#breakpointid) | &nbsp; |  

---  

### <a name="stepover"></a><span data-ttu-id="66e7f-206">stepOver</span><span class="sxs-lookup"><span data-stu-id="66e7f-206">stepOver</span></span>  

<span data-ttu-id="66e7f-207">Étapes au-dessus de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="66e7f-207">Steps over the statement.</span></span>  

&nbsp;  

---  

### <a name="stepinto"></a><span data-ttu-id="66e7f-208">stepInto</span><span class="sxs-lookup"><span data-stu-id="66e7f-208">stepInto</span></span>  

<span data-ttu-id="66e7f-209">Étapes de l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="66e7f-209">Steps into the function call.</span></span>  

&nbsp;  

---  

### <a name="stepout"></a><span data-ttu-id="66e7f-210">stepOut</span><span class="sxs-lookup"><span data-stu-id="66e7f-210">stepOut</span></span>  

<span data-ttu-id="66e7f-211">Sort de l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="66e7f-211">Steps out of the function call.</span></span>  

&nbsp;  

---  

### <a name="pause"></a><span data-ttu-id="66e7f-212">pause</span><span class="sxs-lookup"><span data-stu-id="66e7f-212">pause</span></span>  

<span data-ttu-id="66e7f-213">S’arrête sur l’instruction JavaScript suivante.</span><span class="sxs-lookup"><span data-stu-id="66e7f-213">Stops on the next JavaScript statement.</span></span>  

&nbsp;  

---  

### <a name="resume"></a><span data-ttu-id="66e7f-214">resume</span><span class="sxs-lookup"><span data-stu-id="66e7f-214">resume</span></span>  

<span data-ttu-id="66e7f-215">Reprend l’exécution de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="66e7f-215">Resumes JavaScript execution.</span></span>  

&nbsp;  

---  

### <a name="getscriptsource"></a><span data-ttu-id="66e7f-216">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="66e7f-216">getScriptSource</span></span>  

<span data-ttu-id="66e7f-217">Renvoie la source du script avec l’ID donné.</span><span class="sxs-lookup"><span data-stu-id="66e7f-217">Returns source for the script with given id.</span></span>  

| <span data-ttu-id="66e7f-218">Parameters</span><span class="sxs-lookup"><span data-stu-id="66e7f-218">Parameters</span></span> | <span data-ttu-id="66e7f-219">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-219">Type</span></span> | <span data-ttu-id="66e7f-220">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-220">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-221">scriptId</span><span class="sxs-lookup"><span data-stu-id="66e7f-221">scriptId</span></span> | [<span data-ttu-id="66e7f-222">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="66e7f-222">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="66e7f-223">ID du script pour obtenir la source.</span><span class="sxs-lookup"><span data-stu-id="66e7f-223">ID of the script to get source for.</span></span> |  

| <span data-ttu-id="66e7f-224">Renvoie</span><span class="sxs-lookup"><span data-stu-id="66e7f-224">Returns</span></span> | <span data-ttu-id="66e7f-225">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-225">Type</span></span> | <span data-ttu-id="66e7f-226">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-226">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-227">scriptSource</span><span class="sxs-lookup"><span data-stu-id="66e7f-227">scriptSource</span></span> | `string` | <span data-ttu-id="66e7f-228">Source du script.</span><span class="sxs-lookup"><span data-stu-id="66e7f-228">Script source.</span></span> | 

---  

### <a name="setpauseonexceptions"></a><span data-ttu-id="66e7f-229">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="66e7f-229">setPauseOnExceptions</span></span>  

<span data-ttu-id="66e7f-230">Définit une pause sur l’état des exceptions.</span><span class="sxs-lookup"><span data-stu-id="66e7f-230">Defines pause on exceptions state.</span></span>  <span data-ttu-id="66e7f-231">Peut être définie pour s’arrêter sur toutes les exceptions, les exceptions non détailles ou aucune exception.</span><span class="sxs-lookup"><span data-stu-id="66e7f-231">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span>  <span data-ttu-id="66e7f-232">La pause initiale sur l’état des exceptions est `none` .</span><span class="sxs-lookup"><span data-stu-id="66e7f-232">Initial pause on exceptions state is `none`.</span></span>  

| <span data-ttu-id="66e7f-233">Parameters</span><span class="sxs-lookup"><span data-stu-id="66e7f-233">Parameters</span></span> | <span data-ttu-id="66e7f-234">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-234">Type</span></span> | <span data-ttu-id="66e7f-235">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-235">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-236">state</span><span class="sxs-lookup"><span data-stu-id="66e7f-236">state</span></span> | `string` | <span data-ttu-id="66e7f-237">Mettre en pause le mode exceptions.</span><span class="sxs-lookup"><span data-stu-id="66e7f-237">Pause on exceptions mode.</span></span>  <span data-ttu-id="66e7f-238">Valeurs autorisées  `none` : , `uncaught` ,</span><span class="sxs-lookup"><span data-stu-id="66e7f-238">Allowed values:  `none`, `uncaught`,</span></span> `all` |  

---  

### <a name="evaluateoncallframe"></a><span data-ttu-id="66e7f-239">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="66e7f-239">evaluateOnCallFrame</span></span>  

<span data-ttu-id="66e7f-240">Évalue l’expression sur une trame d’appel donnée.</span><span class="sxs-lookup"><span data-stu-id="66e7f-240">Evaluates expression on a given call frame.</span></span>  

| <span data-ttu-id="66e7f-241">Parameters</span><span class="sxs-lookup"><span data-stu-id="66e7f-241">Parameters</span></span> | <span data-ttu-id="66e7f-242">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-242">Type</span></span> | <span data-ttu-id="66e7f-243">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-243">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-244">callFrameId</span><span class="sxs-lookup"><span data-stu-id="66e7f-244">callFrameId</span></span> | [<span data-ttu-id="66e7f-245">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="66e7f-245">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="66e7f-246">Identificateur d’image d’appel à évaluer.</span><span class="sxs-lookup"><span data-stu-id="66e7f-246">Call frame identifier to evaluate on.</span></span> |  
| <span data-ttu-id="66e7f-247">expression</span><span class="sxs-lookup"><span data-stu-id="66e7f-247">expression</span></span> | `string` | <span data-ttu-id="66e7f-248">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="66e7f-248">Expression to evaluate.</span></span> | 

| <span data-ttu-id="66e7f-249">Renvoie</span><span class="sxs-lookup"><span data-stu-id="66e7f-249">Returns</span></span> | <span data-ttu-id="66e7f-250">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-250">Type</span></span> | <span data-ttu-id="66e7f-251">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-251">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-252">result</span><span class="sxs-lookup"><span data-stu-id="66e7f-252">result</span></span> | [<span data-ttu-id="66e7f-253">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="66e7f-253">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="66e7f-254">Wrapper d’objet pour le résultat d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="66e7f-254">Object wrapper for the evaluation result.</span></span> |  

---  

### <a name="setvariablevalue"></a><span data-ttu-id="66e7f-255">setVariableValue</span><span class="sxs-lookup"><span data-stu-id="66e7f-255">setVariableValue</span></span>  

<span data-ttu-id="66e7f-256">Modifie la valeur de la variable dans un callframe.</span><span class="sxs-lookup"><span data-stu-id="66e7f-256">Changes value of variable in a callframe.</span></span>  <span data-ttu-id="66e7f-257">Les étendues basées sur des objets ne sont pas pris en charge et doivent être désactivées manuellement.</span><span class="sxs-lookup"><span data-stu-id="66e7f-257">Object-based scopes are not supported and must be mutated manually.</span></span>  

| <span data-ttu-id="66e7f-258">Parameters</span><span class="sxs-lookup"><span data-stu-id="66e7f-258">Parameters</span></span> | <span data-ttu-id="66e7f-259">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-259">Type</span></span> | <span data-ttu-id="66e7f-260">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-260">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-261">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="66e7f-261">scopeNumber</span></span> | `integer` | <span data-ttu-id="66e7f-262">Nombre d’étendues basé sur 0, tel qu’il était répertorié dans la chaîne d’étendue.</span><span class="sxs-lookup"><span data-stu-id="66e7f-262">0-based number of scope as was listed in scope chain.</span></span>  <span data-ttu-id="66e7f-263">Seuls `local` , et les types `closure` `catch` d’étendue sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="66e7f-263">Only `local`, `closure`, and `catch` scope types are allowed.</span></span>  <span data-ttu-id="66e7f-264">D’autres étendues peuvent être manipulées manuellement.</span><span class="sxs-lookup"><span data-stu-id="66e7f-264">Other scopes could be manipulated manually.</span></span> | 
| <span data-ttu-id="66e7f-265">variableName</span><span class="sxs-lookup"><span data-stu-id="66e7f-265">variableName</span></span> | `string` | <span data-ttu-id="66e7f-266">Nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="66e7f-266">Variable name.</span></span> | 
| <span data-ttu-id="66e7f-267">newValue</span><span class="sxs-lookup"><span data-stu-id="66e7f-267">newValue</span></span> | [<span data-ttu-id="66e7f-268">Runtime.CallArgument</span><span class="sxs-lookup"><span data-stu-id="66e7f-268">Runtime.CallArgument</span></span>](./runtime.md#callargument) | <span data-ttu-id="66e7f-269">Nouvelle valeur de variable.</span><span class="sxs-lookup"><span data-stu-id="66e7f-269">New variable value.</span></span> |  
| <span data-ttu-id="66e7f-270">callFrameId</span><span class="sxs-lookup"><span data-stu-id="66e7f-270">callFrameId</span></span> | [<span data-ttu-id="66e7f-271">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="66e7f-271">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="66e7f-272">ID de l’appel qui contient une variable.</span><span class="sxs-lookup"><span data-stu-id="66e7f-272">ID of callframe that holds variable.</span></span> |  

---  

### <a name="setblackboxpatterns"></a><span data-ttu-id="66e7f-273">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="66e7f-273">setBlackboxPatterns</span></span>  

<span data-ttu-id="66e7f-274">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="66e7f-274">**Experimental**.</span></span>  <span data-ttu-id="66e7f-275">Remplacez les modèles de boîte noire précédents par les modèles transmis.</span><span class="sxs-lookup"><span data-stu-id="66e7f-275">Replace previous blackbox patterns with passed ones.</span></span>  <span data-ttu-id="66e7f-276">Force le back-end à ignorer la mise en pause/pas à pas dans les scripts avec une URL correspondant à l’un des modèles.</span><span class="sxs-lookup"><span data-stu-id="66e7f-276">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span>  <span data-ttu-id="66e7f-277">Le débompeur essaiera de laisser le script en boîte noire plusieurs fois en « pas à pas » et en recourant à « pas à pas » en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="66e7f-277">The debugger will try to leave blackboxed script by performing 'step in' several times, finally resorting to 'step out' if unsuccessful.</span></span>  


| <span data-ttu-id="66e7f-278">Parameters</span><span class="sxs-lookup"><span data-stu-id="66e7f-278">Parameters</span></span> | <span data-ttu-id="66e7f-279">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-279">Type</span></span> | <span data-ttu-id="66e7f-280">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-280">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-281">patterns</span><span class="sxs-lookup"><span data-stu-id="66e7f-281">patterns</span></span> | `string[]` | <span data-ttu-id="66e7f-282">Tableau de regexps qui sera utilisé pour vérifier l’url du script pour l’état de la boîte aux lettres noire.</span><span class="sxs-lookup"><span data-stu-id="66e7f-282">Array of regexps that will be used to check script url for blackbox state.</span></span> | 

---  

### <a name="mssetdebuggerpropertyvalue"></a><span data-ttu-id="66e7f-283">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="66e7f-283">msSetDebuggerPropertyValue</span></span>  

<span data-ttu-id="66e7f-284">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="66e7f-284">**Experimental**.</span></span>  <span data-ttu-id="66e7f-285">Microsoft : définit la propriété spécifiée du débogger sur la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="66e7f-285">Microsoft: Sets the specified debugger property to the specified value.</span></span>  

| <span data-ttu-id="66e7f-286">Parameters</span><span class="sxs-lookup"><span data-stu-id="66e7f-286">Parameters</span></span> | <span data-ttu-id="66e7f-287">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-287">Type</span></span> | <span data-ttu-id="66e7f-288">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-288">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-289">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="66e7f-289">debuggerPropertyId</span></span> | <span data-ttu-id="66e7f-290">chaîne</span><span class="sxs-lookup"><span data-stu-id="66e7f-290">string</span></span> | <span data-ttu-id="66e7f-291">Microsoft : ID de propriété \(c’est-à-dire `msDebuggerPropertyId` \) à définir.</span><span class="sxs-lookup"><span data-stu-id="66e7f-291">Microsoft:  The property id \(i.e. `msDebuggerPropertyId`\) to set.</span></span> | 
| <span data-ttu-id="66e7f-292">newValue</span><span class="sxs-lookup"><span data-stu-id="66e7f-292">newValue</span></span> | `string` | &nbsp; |  

---  

## <a name="events"></a><span data-ttu-id="66e7f-293">Événements</span><span class="sxs-lookup"><span data-stu-id="66e7f-293">Events</span></span>  

### <a name="scriptparsed"></a><span data-ttu-id="66e7f-294">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="66e7f-294">scriptParsed</span></span>  

<span data-ttu-id="66e7f-295">Déclenché lorsque le script est interrogé.</span><span class="sxs-lookup"><span data-stu-id="66e7f-295">Fired when the script is parsed.</span></span> <span data-ttu-id="66e7f-296">Cet événement est également déclenché pour tous les scripts connus et non récollects lors de l’activation du débogueur.</span><span class="sxs-lookup"><span data-stu-id="66e7f-296">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>  

| <span data-ttu-id="66e7f-297">Parameters</span><span class="sxs-lookup"><span data-stu-id="66e7f-297">Parameters</span></span> | <span data-ttu-id="66e7f-298">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-298">Type</span></span> | <span data-ttu-id="66e7f-299">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-299">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-300">scriptId</span><span class="sxs-lookup"><span data-stu-id="66e7f-300">scriptId</span></span> | [<span data-ttu-id="66e7f-301">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="66e7f-301">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="66e7f-302">Identificateur du script en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="66e7f-302">Identifier of the script parsed.</span></span> |  
| <span data-ttu-id="66e7f-303">url</span><span class="sxs-lookup"><span data-stu-id="66e7f-303">url</span></span> | `string` | <span data-ttu-id="66e7f-304">URL ou nom du script lu \(le caser\).</span><span class="sxs-lookup"><span data-stu-id="66e7f-304">URL or name of the script parsed \(if any\).</span></span> | 
| <span data-ttu-id="66e7f-305">startLine</span><span class="sxs-lookup"><span data-stu-id="66e7f-305">startLine</span></span> | `integer` | <span data-ttu-id="66e7f-306">Décalage de ligne du script dans la ressource avec une URL donnée \(pour les balises de script\).</span><span class="sxs-lookup"><span data-stu-id="66e7f-306">Line offset of the script within the resource with given URL \(for script tags\).</span></span> | 
| <span data-ttu-id="66e7f-307">startColumn</span><span class="sxs-lookup"><span data-stu-id="66e7f-307">startColumn</span></span> | `integer` | <span data-ttu-id="66e7f-308">Décalage de colonne du script dans la ressource avec une URL donnée.</span><span class="sxs-lookup"><span data-stu-id="66e7f-308">Column offset of the script within the resource with given URL.</span></span> | 
| <span data-ttu-id="66e7f-309">endLine</span><span class="sxs-lookup"><span data-stu-id="66e7f-309">endLine</span></span> | `integer` | <span data-ttu-id="66e7f-310">Dernière ligne du script.</span><span class="sxs-lookup"><span data-stu-id="66e7f-310">Last line of the script.</span></span> | 
| <span data-ttu-id="66e7f-311">endColumn</span><span class="sxs-lookup"><span data-stu-id="66e7f-311">endColumn</span></span> | `integer` | <span data-ttu-id="66e7f-312">Longueur de la dernière ligne du script.</span><span class="sxs-lookup"><span data-stu-id="66e7f-312">Length of the last line of the script.</span></span> | 
| <span data-ttu-id="66e7f-313">executionContextId</span><span class="sxs-lookup"><span data-stu-id="66e7f-313">executionContextId</span></span> | [<span data-ttu-id="66e7f-314">Runtime.ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="66e7f-314">Runtime.ExecutionContextId</span></span>](./runtime.md#executioncontextid) | <span data-ttu-id="66e7f-315">Spécifie le contexte de création de script.</span><span class="sxs-lookup"><span data-stu-id="66e7f-315">Specifies script creation context.</span></span> |  
| <span data-ttu-id="66e7f-316">sourceMapURL \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-316">sourceMapURL \(optional\)</span></span> | `string` | <span data-ttu-id="66e7f-317">URL de la carte source associée au script (le cas cas).</span><span class="sxs-lookup"><span data-stu-id="66e7f-317">URL of source map associated with script (if any).</span></span> |  
| <span data-ttu-id="66e7f-318">length \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-318">length \(optional\)</span></span> | `integer` | <span data-ttu-id="66e7f-319">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="66e7f-319">**Experimental**.</span></span>  <span data-ttu-id="66e7f-320">Longueur du script.</span><span class="sxs-lookup"><span data-stu-id="66e7f-320">This script length.</span></span> |  
| <span data-ttu-id="66e7f-321">msParentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-321">msParentId \(optional\)</span></span> | `string` | <span data-ttu-id="66e7f-322">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="66e7f-322">**Experimental**.</span></span>  <span data-ttu-id="66e7f-323">Il s’agit de l’ID de document parent.</span><span class="sxs-lookup"><span data-stu-id="66e7f-323">This is the parent document ID.</span></span> |  
| <span data-ttu-id="66e7f-324">msMimeType \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-324">msMimeType \(optional\)</span></span> | `string` | <span data-ttu-id="66e7f-325">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="66e7f-325">**Experimental**.</span></span>  <span data-ttu-id="66e7f-326">Il s’agit du type mime.</span><span class="sxs-lookup"><span data-stu-id="66e7f-326">This is the mime type.</span></span> |  
| <span data-ttu-id="66e7f-327">msIsDynamicCode \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-327">msIsDynamicCode \(optional\)</span></span> | `boolean` | <span data-ttu-id="66e7f-328">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="66e7f-328">**Experimental**.</span></span>  <span data-ttu-id="66e7f-329">Cela indique s’il s’agit d’un code dynamique.</span><span class="sxs-lookup"><span data-stu-id="66e7f-329">This indicates whether it is dynamic code.</span></span> |  
| <span data-ttu-id="66e7f-330">msLongDocumentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-330">msLongDocumentId \(optional\)</span></span> | `integer` | <span data-ttu-id="66e7f-331">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="66e7f-331">**Experimental**.</span></span>  <span data-ttu-id="66e7f-332">Il s’agit de l’ID de document long.</span><span class="sxs-lookup"><span data-stu-id="66e7f-332">This is the long document ID.</span></span> |  

---  

### <a name="breakpointresolved"></a><span data-ttu-id="66e7f-333">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="66e7f-333">breakpointResolved</span></span>  

<span data-ttu-id="66e7f-334">Déclenché lorsque le point d’arrêt est résolu en un script et un emplacement réels.</span><span class="sxs-lookup"><span data-stu-id="66e7f-334">Fired when breakpoint is resolved to an actual script and location.</span></span>  

| <span data-ttu-id="66e7f-335">Parameters</span><span class="sxs-lookup"><span data-stu-id="66e7f-335">Parameters</span></span> | <span data-ttu-id="66e7f-336">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-336">Type</span></span> | <span data-ttu-id="66e7f-337">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-337">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-338">breakpointId</span><span class="sxs-lookup"><span data-stu-id="66e7f-338">breakpointId</span></span> | [<span data-ttu-id="66e7f-339">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="66e7f-339">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="66e7f-340">Identificateur unique de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="66e7f-340">Breakpoint unique identifier.</span></span> |  
| <span data-ttu-id="66e7f-341">location</span><span class="sxs-lookup"><span data-stu-id="66e7f-341">location</span></span> | [<span data-ttu-id="66e7f-342">Emplacement</span><span class="sxs-lookup"><span data-stu-id="66e7f-342">Location</span></span>](#location) | <span data-ttu-id="66e7f-343">Emplacement réel du point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="66e7f-343">Actual breakpoint location.</span></span> |  
| <span data-ttu-id="66e7f-344">msLength \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-344">msLength \(optional\)</span></span> | `integer` | <span data-ttu-id="66e7f-345">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="66e7f-345">**Experimental**.</span></span>  <span data-ttu-id="66e7f-346">Microsoft : Longueur du code \(nombre de caractères\) à l’emplacement du point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="66e7f-346">Microsoft:  Length of code \(i.e. number of characters\) at the breakpoint location.</span></span> |  

---  

### <a name="paused"></a><span data-ttu-id="66e7f-347">en pause</span><span class="sxs-lookup"><span data-stu-id="66e7f-347">paused</span></span>  

<span data-ttu-id="66e7f-348">Déclenché lorsque les débompeurs se cassent pour un point d’arrêt ou une exception.</span><span class="sxs-lookup"><span data-stu-id="66e7f-348">Fired when the debuggers breaks for a breakpoint or exception.</span></span>  

| <span data-ttu-id="66e7f-349">Parameters</span><span class="sxs-lookup"><span data-stu-id="66e7f-349">Parameters</span></span> | <span data-ttu-id="66e7f-350">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-350">Type</span></span> | <span data-ttu-id="66e7f-351">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-351">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-352">callFrames</span><span class="sxs-lookup"><span data-stu-id="66e7f-352">callFrames</span></span> | [<span data-ttu-id="66e7f-353">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="66e7f-353">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="66e7f-354">Pile d’appels sur le débogger arrêté.</span><span class="sxs-lookup"><span data-stu-id="66e7f-354">Call stack the debugger stopped on.</span></span> |  
| <span data-ttu-id="66e7f-355">reason</span><span class="sxs-lookup"><span data-stu-id="66e7f-355">reason</span></span> | `string` |  <span data-ttu-id="66e7f-356">Motif de l’interruption.</span><span class="sxs-lookup"><span data-stu-id="66e7f-356">Pause reason.</span></span>  <span data-ttu-id="66e7f-357">Valeurs autorisées  `breakpoint` : `step` , , `exception` `other` et</span><span class="sxs-lookup"><span data-stu-id="66e7f-357">Allowed values:  `breakpoint`, `step`, `exception`, `other`, and</span></span> `EventListener` |  
| <span data-ttu-id="66e7f-358">data \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-358">data \(optional\)</span></span> | `object` | <span data-ttu-id="66e7f-359">Objet contenant des propriétés auxiliaires spécifiques aux coupures.</span><span class="sxs-lookup"><span data-stu-id="66e7f-359">Object containing break-specific auxiliary properties.</span></span> |  
| <span data-ttu-id="66e7f-360">hitBreakpoints \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-360">hitBreakpoints \(optional\)</span></span> | `string[]` | <span data-ttu-id="66e7f-361">ID des points d’arrêt d’arrêt</span><span class="sxs-lookup"><span data-stu-id="66e7f-361">Hit breakpoints IDs</span></span> |  
| <span data-ttu-id="66e7f-362">asyncStackTrace \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-362">asyncStackTrace \(optional\)</span></span> | `StackTrace` | <span data-ttu-id="66e7f-363">Suivi de pile async JavaScript.</span><span class="sxs-lookup"><span data-stu-id="66e7f-363">JavaScript async stack trace.</span></span> |  

---  

### <a name="resumed"></a><span data-ttu-id="66e7f-364">reprise</span><span class="sxs-lookup"><span data-stu-id="66e7f-364">resumed</span></span>  

<span data-ttu-id="66e7f-365">Déclenché lorsque le débogger reprend l’exécution.</span><span class="sxs-lookup"><span data-stu-id="66e7f-365">Fired when the debugger resumes execution.</span></span>  

&nbsp;  

---  

## <a name="types"></a><span data-ttu-id="66e7f-366">Types</span><span class="sxs-lookup"><span data-stu-id="66e7f-366">Types</span></span>  

### <a name="breakpointid-string"></a><span data-ttu-id="66e7f-367">Chaîne BreakpointId</span><span class="sxs-lookup"><span data-stu-id="66e7f-367">BreakpointId string</span></span>  

<a name="breakpointid"></a>  

<span data-ttu-id="66e7f-368">Identificateur de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="66e7f-368">Breakpoint identifier.</span></span>  

&nbsp;  

---  

### <a name="callframeid-string"></a><span data-ttu-id="66e7f-369">Chaîne CallFrameId</span><span class="sxs-lookup"><span data-stu-id="66e7f-369">CallFrameId string</span></span>  

<a name="callframeid"></a>  

<span data-ttu-id="66e7f-370">Identificateur d’image d’appel.</span><span class="sxs-lookup"><span data-stu-id="66e7f-370">Call frame identifier.</span></span>  

&nbsp;  

---  

### <a name="location-object"></a><span data-ttu-id="66e7f-371">Location, objet</span><span class="sxs-lookup"><span data-stu-id="66e7f-371">Location object</span></span>  

<a name="location"></a>  

<span data-ttu-id="66e7f-372">Emplacement dans le code source.</span><span class="sxs-lookup"><span data-stu-id="66e7f-372">Location in the source code.</span></span>  

| <span data-ttu-id="66e7f-373">Propriétés</span><span class="sxs-lookup"><span data-stu-id="66e7f-373">Properties</span></span> | <span data-ttu-id="66e7f-374">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-374">Type</span></span> | <span data-ttu-id="66e7f-375">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-375">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-376">scriptId</span><span class="sxs-lookup"><span data-stu-id="66e7f-376">scriptId</span></span> | [<span data-ttu-id="66e7f-377">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="66e7f-377">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="66e7f-378">Identificateur de script tel qu’indiqué dans `Debugger.scriptParsed` le .</span><span class="sxs-lookup"><span data-stu-id="66e7f-378">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="66e7f-379">lineNumber</span><span class="sxs-lookup"><span data-stu-id="66e7f-379">lineNumber</span></span> | `integer` | <span data-ttu-id="66e7f-380">Numéro de ligne dans le script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="66e7f-380">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="66e7f-381">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-381">columnNumber \(optional\)</span></span> | `integer` | <span data-ttu-id="66e7f-382">Numéro de colonne dans le script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="66e7f-382">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="66e7f-383">msLength</span><span class="sxs-lookup"><span data-stu-id="66e7f-383">msLength</span></span> | `integer` | <span data-ttu-id="66e7f-384">Microsoft : Longueur du code \(c’est-à-dire le nombre de caractères\) à ce cadre d’appel.</span><span class="sxs-lookup"><span data-stu-id="66e7f-384">Microsoft:  Length of code \(i.e. number of characters\) at this call frame.</span></span> |  

---  

### <a name="breaklocation-object"></a><span data-ttu-id="66e7f-385">Objet BreakLocation</span><span class="sxs-lookup"><span data-stu-id="66e7f-385">BreakLocation object</span></span>  

<a name="breaklocation"></a>  

<span data-ttu-id="66e7f-386">Emplacement de rupture dans le code source.</span><span class="sxs-lookup"><span data-stu-id="66e7f-386">Break location in the source code.</span></span>  

| <span data-ttu-id="66e7f-387">Propriétés</span><span class="sxs-lookup"><span data-stu-id="66e7f-387">Properties</span></span> | <span data-ttu-id="66e7f-388">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-388">Type</span></span> | <span data-ttu-id="66e7f-389">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-389">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-390">scriptId</span><span class="sxs-lookup"><span data-stu-id="66e7f-390">scriptId</span></span> | [<span data-ttu-id="66e7f-391">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="66e7f-391">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="66e7f-392">Identificateur de script tel qu’indiqué dans `Debugger.scriptParsed` le .</span><span class="sxs-lookup"><span data-stu-id="66e7f-392">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="66e7f-393">lineNumber</span><span class="sxs-lookup"><span data-stu-id="66e7f-393">lineNumber</span></span> | `integer` | <span data-ttu-id="66e7f-394">Numéro de ligne dans le script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="66e7f-394">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="66e7f-395">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-395">columnNumber \(optional\)</span></span> | `integer` | <span data-ttu-id="66e7f-396">Numéro de colonne dans le script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="66e7f-396">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="66e7f-397">msLength</span><span class="sxs-lookup"><span data-stu-id="66e7f-397">msLength</span></span> | `integer` | <span data-ttu-id="66e7f-398">Microsoft : Longueur du code \(c’est-à-dire le nombre de caractères\) à ce cadre d’appel.</span><span class="sxs-lookup"><span data-stu-id="66e7f-398">Microsoft:  Length of code \(i.e. number of characters\) at this call frame.</span></span> |  
| <span data-ttu-id="66e7f-399">type \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-399">type \(optional\)</span></span> | `string` | <span data-ttu-id="66e7f-400">Valeurs autorisées : debuggerStatement, call, return.</span><span class="sxs-lookup"><span data-stu-id="66e7f-400">Allowed values: debuggerStatement, call, return.</span></span> |  

---  

### <a name="callframe-object"></a><span data-ttu-id="66e7f-401">Objet CallFrame</span><span class="sxs-lookup"><span data-stu-id="66e7f-401">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="66e7f-402">Image d’appel JavaScript.</span><span class="sxs-lookup"><span data-stu-id="66e7f-402">JavaScript call frame.</span></span> <span data-ttu-id="66e7f-403">Le tableau des trames d’appel forme la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="66e7f-403">Array of call frames form the call stack.</span></span>  

| <span data-ttu-id="66e7f-404">Propriétés</span><span class="sxs-lookup"><span data-stu-id="66e7f-404">Properties</span></span> | <span data-ttu-id="66e7f-405">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-405">Type</span></span> | <span data-ttu-id="66e7f-406">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-406">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-407">callFrameId</span><span class="sxs-lookup"><span data-stu-id="66e7f-407">callFrameId</span></span> | [<span data-ttu-id="66e7f-408">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="66e7f-408">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="66e7f-409">Identificateur d’image d’appel.</span><span class="sxs-lookup"><span data-stu-id="66e7f-409">Call frame identifier.</span></span>  <span data-ttu-id="66e7f-410">Cet identificateur n’est valide que lorsque le débogger est suspendu.</span><span class="sxs-lookup"><span data-stu-id="66e7f-410">This identifier is only valid while the debugger is paused.</span></span> |  
| <span data-ttu-id="66e7f-411">functionName</span><span class="sxs-lookup"><span data-stu-id="66e7f-411">functionName</span></span> | `string` | <span data-ttu-id="66e7f-412">Nom de la fonction JavaScript appelée sur ce cadre d’appel.</span><span class="sxs-lookup"><span data-stu-id="66e7f-412">Name of the JavaScript function called on this call frame.</span></span> |  
| <span data-ttu-id="66e7f-413">functionLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-413">functionLocation \(optional\)</span></span> | [<span data-ttu-id="66e7f-414">Emplacement</span><span class="sxs-lookup"><span data-stu-id="66e7f-414">Location</span></span>](#location) | <span data-ttu-id="66e7f-415">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="66e7f-415">**Experimental**.</span></span>  <span data-ttu-id="66e7f-416">Emplacement dans le code source.</span><span class="sxs-lookup"><span data-stu-id="66e7f-416">Location in the source code.</span></span> |  
| <span data-ttu-id="66e7f-417">location</span><span class="sxs-lookup"><span data-stu-id="66e7f-417">location</span></span> | [<span data-ttu-id="66e7f-418">Emplacement</span><span class="sxs-lookup"><span data-stu-id="66e7f-418">Location</span></span>](#location) | <span data-ttu-id="66e7f-419">Emplacement dans le code source.</span><span class="sxs-lookup"><span data-stu-id="66e7f-419">Location in the source code.</span></span> |  
| <span data-ttu-id="66e7f-420">url</span><span class="sxs-lookup"><span data-stu-id="66e7f-420">url</span></span> | `string` | <span data-ttu-id="66e7f-421">Nom ou URL du script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="66e7f-421">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="66e7f-422">scopeChain</span><span class="sxs-lookup"><span data-stu-id="66e7f-422">scopeChain</span></span> | [<span data-ttu-id="66e7f-423">Scope[]</span><span class="sxs-lookup"><span data-stu-id="66e7f-423">Scope[]</span></span>](#scope) | <span data-ttu-id="66e7f-424">Chaîne d’étendue pour ce cadre d’appel.</span><span class="sxs-lookup"><span data-stu-id="66e7f-424">Scope chain for this call frame.</span></span> |  
| <span data-ttu-id="66e7f-425">this</span><span class="sxs-lookup"><span data-stu-id="66e7f-425">this</span></span> | [<span data-ttu-id="66e7f-426">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="66e7f-426">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | `this` <span data-ttu-id="66e7f-427">pour ce cadre d’appel.</span><span class="sxs-lookup"><span data-stu-id="66e7f-427">object for this call frame.</span></span> |  
| <span data-ttu-id="66e7f-428">returnValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-428">returnValue \(optional\)</span></span> | [<span data-ttu-id="66e7f-429">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="66e7f-429">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="66e7f-430">Valeur renvoyée, si la fonction est au point de retour.</span><span class="sxs-lookup"><span data-stu-id="66e7f-430">The value being returned, if the function is at return point.</span></span> |  

---  

### <a name="scope-object"></a><span data-ttu-id="66e7f-431">Objet Scope</span><span class="sxs-lookup"><span data-stu-id="66e7f-431">Scope object</span></span>  

<a name="scope"></a>  

<span data-ttu-id="66e7f-432">Description de l’étendue.</span><span class="sxs-lookup"><span data-stu-id="66e7f-432">Scope description.</span></span>  

| <span data-ttu-id="66e7f-433">Propriétés</span><span class="sxs-lookup"><span data-stu-id="66e7f-433">Properties</span></span> | <span data-ttu-id="66e7f-434">Type</span><span class="sxs-lookup"><span data-stu-id="66e7f-434">Type</span></span> | <span data-ttu-id="66e7f-435">Détails</span><span class="sxs-lookup"><span data-stu-id="66e7f-435">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="66e7f-436">type</span><span class="sxs-lookup"><span data-stu-id="66e7f-436">type</span></span> | `string` | <span data-ttu-id="66e7f-437">Type d’étendue.</span><span class="sxs-lookup"><span data-stu-id="66e7f-437">Scope type.</span></span>  <span data-ttu-id="66e7f-438">Valeurs autorisées  `global` : , , , , , , `local` , `with` `closure` `catch` `block` `script` `eval` `module` et</span><span class="sxs-lookup"><span data-stu-id="66e7f-438">Allowed values:  `global`, `local`, `with`, `closure`, `catch`, `block`, `script`, `eval`, `module`, and</span></span> `return` |  
| <span data-ttu-id="66e7f-439">object</span><span class="sxs-lookup"><span data-stu-id="66e7f-439">object</span></span> | [<span data-ttu-id="66e7f-440">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="66e7f-440">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="66e7f-441">Objet représentant l’étendue.</span><span class="sxs-lookup"><span data-stu-id="66e7f-441">Object representing the scope.</span></span>  <span data-ttu-id="66e7f-442">Pour et les étendues, il représente l’objet réel ; pour le reste des étendues, il s’agit d’objets temporaires artificielles qui édent les variables d’étendue en tant `global` `with` que propriétés.</span><span class="sxs-lookup"><span data-stu-id="66e7f-442">For `global` and `with` scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span> |  
| <span data-ttu-id="66e7f-443">name \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-443">name \(optional\)</span></span> | `string` | &nbsp; |  
| <span data-ttu-id="66e7f-444">startLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-444">startLocation \(optional\)</span></span> | [<span data-ttu-id="66e7f-445">Emplacement</span><span class="sxs-lookup"><span data-stu-id="66e7f-445">Location</span></span>](#location) | <span data-ttu-id="66e7f-446">Emplacement dans le code source où commence l’étendue.</span><span class="sxs-lookup"><span data-stu-id="66e7f-446">Location in the source code where scope starts.</span></span> |  
| <span data-ttu-id="66e7f-447">endLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="66e7f-447">endLocation \(optional\)</span></span> | [<span data-ttu-id="66e7f-448">Emplacement</span><span class="sxs-lookup"><span data-stu-id="66e7f-448">Location</span></span>](#location) | <span data-ttu-id="66e7f-449">Emplacement dans le code source où l’étendue se termine.</span><span class="sxs-lookup"><span data-stu-id="66e7f-449">Location in the source code where scope ends.</span></span> |  

---  

## <a name="dependencies"></a><span data-ttu-id="66e7f-450">Dépendances</span><span class="sxs-lookup"><span data-stu-id="66e7f-450">Dependencies</span></span>  

[<span data-ttu-id="66e7f-451">Runtime</span><span class="sxs-lookup"><span data-stu-id="66e7f-451">Runtime</span></span>](./runtime.md)  
