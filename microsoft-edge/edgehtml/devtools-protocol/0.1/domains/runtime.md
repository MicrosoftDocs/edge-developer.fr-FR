---
description: Référence du protocole DevTools version 0.1 (EdgeHTML) pour le domaine d’runtime.  Le domaine runtime expose le runtime JavaScript au moyen d’objets miroir et d’évaluation à distance.  Les résultats de l’évaluation sont renvoyés en tant qu’objet miroir qui exposent le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour d’autres références d’objet.  Les objets d’origine sont conservés en mémoire, sauf s’ils sont libérés explicitement.
title: Domaine d’runtime - DevTools Protocol Version 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9aa87c1c289452844ef3442811f84881fc752b4
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397691"
---
# <a name="runtime-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="71be5-106">Domaine d’runtime - DevTools Protocol Version 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="71be5-106">Runtime Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="71be5-107">Le domaine d’runtime expose le runtime JavaScript au moyen d’objets d’évaluation et de miroir distants.</span><span class="sxs-lookup"><span data-stu-id="71be5-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span>  <span data-ttu-id="71be5-108">Les résultats de l’évaluation sont renvoyés en tant qu’objet miroir qui exposent le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour d’autres références d’objet.</span><span class="sxs-lookup"><span data-stu-id="71be5-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span>  <span data-ttu-id="71be5-109">Les objets d’origine sont conservés en mémoire, sauf s’ils sont libérés explicitement.</span><span class="sxs-lookup"><span data-stu-id="71be5-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>  

| <span data-ttu-id="71be5-110">Classification</span><span class="sxs-lookup"><span data-stu-id="71be5-110">Classification</span></span> | <span data-ttu-id="71be5-111">Membres</span><span class="sxs-lookup"><span data-stu-id="71be5-111">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="71be5-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="71be5-112">Methods</span></span>](#methods) | <span data-ttu-id="71be5-113">[activer](#enable), [désactiver](#disable), [évaluer](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span><span class="sxs-lookup"><span data-stu-id="71be5-113">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span></span> |  
| [<span data-ttu-id="71be5-114">Événements</span><span class="sxs-lookup"><span data-stu-id="71be5-114">Events</span></span>](#events) | <span data-ttu-id="71be5-115">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span><span class="sxs-lookup"><span data-stu-id="71be5-115">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span></span> |  
| [<span data-ttu-id="71be5-116">Types</span><span class="sxs-lookup"><span data-stu-id="71be5-116">Types</span></span>](#types) | <span data-ttu-id="71be5-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="71be5-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |  

## <a name="methods"></a><span data-ttu-id="71be5-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="71be5-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="71be5-119">activer</span><span class="sxs-lookup"><span data-stu-id="71be5-119">enable</span></span>  

<span data-ttu-id="71be5-120">Active la notification de `executionContextsCleared` l’événement.</span><span class="sxs-lookup"><span data-stu-id="71be5-120">Enables reporting of the `executionContextsCleared` event.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="71be5-121">désactiver </span><span class="sxs-lookup"><span data-stu-id="71be5-121">disable</span></span>  

<span data-ttu-id="71be5-122">Désactive le signalement de `executionContextsCleared` l’événement.</span><span class="sxs-lookup"><span data-stu-id="71be5-122">Disables reporting of the `executionContextsCleared` event.</span></span>  

&nbsp;  

---  

### <a name="evaluate"></a><span data-ttu-id="71be5-123">évaluer</span><span class="sxs-lookup"><span data-stu-id="71be5-123">evaluate</span></span>  

<span data-ttu-id="71be5-124">Évalue l’expression sur l’objet global.</span><span class="sxs-lookup"><span data-stu-id="71be5-124">Evaluates expression on global object.</span></span>  

| <span data-ttu-id="71be5-125">Parameters</span><span class="sxs-lookup"><span data-stu-id="71be5-125">Parameters</span></span> | <span data-ttu-id="71be5-126">Type</span><span class="sxs-lookup"><span data-stu-id="71be5-126">Type</span></span> | <span data-ttu-id="71be5-127">Détails</span><span class="sxs-lookup"><span data-stu-id="71be5-127">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="71be5-128">expression</span><span class="sxs-lookup"><span data-stu-id="71be5-128">expression</span></span> | `string` | <span data-ttu-id="71be5-129">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="71be5-129">Expression to evaluate.</span></span> |  
| <span data-ttu-id="71be5-130">silent \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-130">silent \(optional\)</span></span> | `boolean` | <span data-ttu-id="71be5-131">En mode silencieux, les exceptions lancées lors de l’évaluation ne sont pas signalées et ne suspendent pas l’exécution.</span><span class="sxs-lookup"><span data-stu-id="71be5-131">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span>  <span data-ttu-id="71be5-132">Remplace `setPauseOnException` l’état.</span><span class="sxs-lookup"><span data-stu-id="71be5-132">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="71be5-133">contextId \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="71be5-133">contextId \(optional\)</span></span> | [<span data-ttu-id="71be5-134">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="71be5-134">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="71be5-135">Spécifie dans quel contexte d’exécution effectuer l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="71be5-135">Specifies in which execution context to perform evaluation.</span></span>  <span data-ttu-id="71be5-136">Si le paramètre est omis, l’évaluation sera effectuée dans le contexte de la page inspectée.</span><span class="sxs-lookup"><span data-stu-id="71be5-136">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span> |  
| <span data-ttu-id="71be5-137">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-137">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="71be5-138">Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</span><span class="sxs-lookup"><span data-stu-id="71be5-138">Whether the result is expected to be a JSON object that should be sent by value.</span></span> |  
| <span data-ttu-id="71be5-139">awaitPromise \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-139">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="71be5-140">Si l’exécution doit être résolue pour la valeur et le retour une fois `await` la promesse attendue résolue.</span><span class="sxs-lookup"><span data-stu-id="71be5-140">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  

| <span data-ttu-id="71be5-141">Renvoie</span><span class="sxs-lookup"><span data-stu-id="71be5-141">Returns</span></span> | <span data-ttu-id="71be5-142">Type</span><span class="sxs-lookup"><span data-stu-id="71be5-142">Type</span></span> | <span data-ttu-id="71be5-143">Détails</span><span class="sxs-lookup"><span data-stu-id="71be5-143">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="71be5-144">result</span><span class="sxs-lookup"><span data-stu-id="71be5-144">result</span></span> | [<span data-ttu-id="71be5-145">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="71be5-145">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="71be5-146">Résultat de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="71be5-146">Evaluation result.</span></span> |  

---  

### <a name="callfunctionon"></a><span data-ttu-id="71be5-147">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="71be5-147">callFunctionOn</span></span>  

<span data-ttu-id="71be5-148">Appelle la fonction avec déclaration donnée sur l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="71be5-148">Calls function with given declaration on the given object.</span></span>  <span data-ttu-id="71be5-149">Le groupe d’objets du résultat est hérité de l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="71be5-149">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="71be5-150">Parameters</span><span class="sxs-lookup"><span data-stu-id="71be5-150">Parameters</span></span> | <span data-ttu-id="71be5-151">Type</span><span class="sxs-lookup"><span data-stu-id="71be5-151">Type</span></span> | <span data-ttu-id="71be5-152">Détails</span><span class="sxs-lookup"><span data-stu-id="71be5-152">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="71be5-153">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="71be5-153">functionDeclaration</span></span> | `string` | <span data-ttu-id="71be5-154">Déclaration de la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="71be5-154">Declaration of the function to call.</span></span> |  
| <span data-ttu-id="71be5-155">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-155">objectId \(optional\)</span></span> | [<span data-ttu-id="71be5-156">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="71be5-156">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="71be5-157">Identificateur de l’objet sur qui appeler la fonction.</span><span class="sxs-lookup"><span data-stu-id="71be5-157">Identifier of the object to call function on.</span></span>  <span data-ttu-id="71be5-158">`objectId` `executionContextId` L’une ou l’autre doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="71be5-158">Either `objectId` or `executionContextId` should be specified.</span></span>  <span data-ttu-id="71be5-159">objectId doit être issu de la fonction Runtime.evaluate().</span><span class="sxs-lookup"><span data-stu-id="71be5-159">objectId must be from the Runtime.evaluate() function.</span></span> |  
| <span data-ttu-id="71be5-160">arguments \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="71be5-160">arguments \(optional\)</span></span> | [<span data-ttu-id="71be5-161">CallArgument[]</span><span class="sxs-lookup"><span data-stu-id="71be5-161">CallArgument[]</span></span>](#callargument) | <span data-ttu-id="71be5-162">Arguments d’appel.</span><span class="sxs-lookup"><span data-stu-id="71be5-162">Call arguments.</span></span>  <span data-ttu-id="71be5-163">Tous les arguments d’appel doivent appartenir au même monde JavaScript que l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="71be5-163">All call arguments must belong to the same JavaScript world as the target object.</span></span> |  
| <span data-ttu-id="71be5-164">silent \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-164">silent \(optional\)</span></span> | `boolean` | <span data-ttu-id="71be5-165">En mode silencieux, les exceptions lancées lors de l’évaluation ne sont pas signalées et ne suspendent pas l’exécution.</span><span class="sxs-lookup"><span data-stu-id="71be5-165">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span>  <span data-ttu-id="71be5-166">Remplace `setPauseOnException` l’état.</span><span class="sxs-lookup"><span data-stu-id="71be5-166">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="71be5-167">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-167">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="71be5-168">Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</span><span class="sxs-lookup"><span data-stu-id="71be5-168">Whether the result is expected to be a JSON object which should be sent by value.</span></span> |  
| <span data-ttu-id="71be5-169">awaitPromise \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-169">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="71be5-170">Si l’exécution doit être résolue pour la valeur et le retour une fois `await` la promesse attendue résolue.</span><span class="sxs-lookup"><span data-stu-id="71be5-170">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  

| <span data-ttu-id="71be5-171">Renvoie</span><span class="sxs-lookup"><span data-stu-id="71be5-171">Returns</span></span> | <span data-ttu-id="71be5-172">Type</span><span class="sxs-lookup"><span data-stu-id="71be5-172">Type</span></span> | <span data-ttu-id="71be5-173">Détails</span><span class="sxs-lookup"><span data-stu-id="71be5-173">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="71be5-174">result</span><span class="sxs-lookup"><span data-stu-id="71be5-174">result</span></span> | [<span data-ttu-id="71be5-175">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="71be5-175">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="71be5-176">Résultat de l’appel.</span><span class="sxs-lookup"><span data-stu-id="71be5-176">Call result.</span></span> |  

---  

### <a name="getproperties"></a><span data-ttu-id="71be5-177">getProperties</span><span class="sxs-lookup"><span data-stu-id="71be5-177">getProperties</span></span>  

<span data-ttu-id="71be5-178">Renvoie les propriétés d’un objet donné.</span><span class="sxs-lookup"><span data-stu-id="71be5-178">Returns properties of a given object.</span></span>  <span data-ttu-id="71be5-179">Le groupe d’objets du résultat est hérité de l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="71be5-179">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="71be5-180">Parameters</span><span class="sxs-lookup"><span data-stu-id="71be5-180">Parameters</span></span> | <span data-ttu-id="71be5-181">Type</span><span class="sxs-lookup"><span data-stu-id="71be5-181">Type</span></span> | <span data-ttu-id="71be5-182">Détails</span><span class="sxs-lookup"><span data-stu-id="71be5-182">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="71be5-183">objectId</span><span class="sxs-lookup"><span data-stu-id="71be5-183">objectId</span></span> | [<span data-ttu-id="71be5-184">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="71be5-184">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="71be5-185">Identificateur de l’objet pour qui renvoyer les propriétés.</span><span class="sxs-lookup"><span data-stu-id="71be5-185">Identifier of the object to return properties for.</span></span>  `objectId` <span data-ttu-id="71be5-186">doit être issu de la `Debugger.evaluateOnCallFrame()` fonction.</span><span class="sxs-lookup"><span data-stu-id="71be5-186">must be from the `Debugger.evaluateOnCallFrame()` function.</span></span> |  
| <span data-ttu-id="71be5-187">ownProperties \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-187">ownProperties \(optional\)</span></span> | `boolean` | <span data-ttu-id="71be5-188">Si `true` , renvoie les propriétés appartenant uniquement à l’élément lui-même, et non à sa chaîne prototype.</span><span class="sxs-lookup"><span data-stu-id="71be5-188">If `true`, returns properties belonging only to the element itself, not to its prototype chain.</span></span> |  
| <span data-ttu-id="71be5-189">accessorPropertiesOnly \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-189">accessorPropertiesOnly \(optional\)</span></span> | `boolean` | <span data-ttu-id="71be5-190">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="71be5-190">**Experimental**.</span></span>  <span data-ttu-id="71be5-191">Si `true` , renvoie les propriétés d’accesseur \(avec getter/setter\) uniquement ; les propriétés internes ne sont pas renvoyées non plus.</span><span class="sxs-lookup"><span data-stu-id="71be5-191">If `true`, returns accessor properties \(with getter/setter\) only; internal properties are not returned either.</span></span> |  

| <span data-ttu-id="71be5-192">Renvoie</span><span class="sxs-lookup"><span data-stu-id="71be5-192">Returns</span></span> | <span data-ttu-id="71be5-193">Type</span><span class="sxs-lookup"><span data-stu-id="71be5-193">Type</span></span> | <span data-ttu-id="71be5-194">Détails</span><span class="sxs-lookup"><span data-stu-id="71be5-194">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="71be5-195">result</span><span class="sxs-lookup"><span data-stu-id="71be5-195">result</span></span> | [<span data-ttu-id="71be5-196">PropertyDescriptor[]</span><span class="sxs-lookup"><span data-stu-id="71be5-196">PropertyDescriptor[]</span></span>](#propertydescriptor) | <span data-ttu-id="71be5-197">Propriétés de l’objet.</span><span class="sxs-lookup"><span data-stu-id="71be5-197">Object properties.</span></span> |  

---  

## <a name="events"></a><span data-ttu-id="71be5-198">Événements</span><span class="sxs-lookup"><span data-stu-id="71be5-198">Events</span></span>  

### <a name="executioncontextscleared"></a><span data-ttu-id="71be5-199">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="71be5-199">executionContextsCleared</span></span>  

<span data-ttu-id="71be5-200">Émis lorsque tous les executionContexts ont été effacés dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="71be5-200">Issued when all executionContexts were cleared in browser.</span></span>  

&nbsp;  

---  

### <a name="exceptionthrown"></a><span data-ttu-id="71be5-201">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="71be5-201">exceptionThrown</span></span>  

<span data-ttu-id="71be5-202">Émise lorsque l’exception a été levée et nonhandée.</span><span class="sxs-lookup"><span data-stu-id="71be5-202">Issued when exception was thrown and unhandled.</span></span>  

| <span data-ttu-id="71be5-203">Parameters</span><span class="sxs-lookup"><span data-stu-id="71be5-203">Parameters</span></span> | <span data-ttu-id="71be5-204">Type</span><span class="sxs-lookup"><span data-stu-id="71be5-204">Type</span></span> | <span data-ttu-id="71be5-205">Détails</span><span class="sxs-lookup"><span data-stu-id="71be5-205">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="71be5-206">timestamp</span><span class="sxs-lookup"><span data-stu-id="71be5-206">timestamp</span></span> | [<span data-ttu-id="71be5-207">Horodateur</span><span class="sxs-lookup"><span data-stu-id="71be5-207">Timestamp</span></span>](#timestamp) | <span data-ttu-id="71be5-208">Timestamp de l’exception.</span><span class="sxs-lookup"><span data-stu-id="71be5-208">Timestamp of the exception.</span></span> |  
| <span data-ttu-id="71be5-209">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="71be5-209">exceptionDetails</span></span> | [<span data-ttu-id="71be5-210">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="71be5-210">ExceptionDetails</span></span>](#exceptiondetails) | &nbsp; |  

---  

## <a name="types"></a><span data-ttu-id="71be5-211">Types</span><span class="sxs-lookup"><span data-stu-id="71be5-211">Types</span></span>  

### <a name="scriptid-string"></a><span data-ttu-id="71be5-212">Chaîne ScriptId</span><span class="sxs-lookup"><span data-stu-id="71be5-212">ScriptId string</span></span>  

<a name="scriptid"></a>  

<span data-ttu-id="71be5-213">Identificateur de script unique.</span><span class="sxs-lookup"><span data-stu-id="71be5-213">Unique script identifier.</span></span>  

&nbsp;  

---  

### <a name="remoteobjectid-string"></a><span data-ttu-id="71be5-214">Chaîne RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="71be5-214">RemoteObjectId string</span></span>  

<a name="remoteobjectid"></a>  

<span data-ttu-id="71be5-215">Identificateur d’objet unique.</span><span class="sxs-lookup"><span data-stu-id="71be5-215">Unique object identifier.</span></span>  

&nbsp;  

---  

### <a name="unserializablevalue-string"></a><span data-ttu-id="71be5-216">Chaîne UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="71be5-216">UnserializableValue string</span></span>  

<a name="unserializablevalue"></a>  

<span data-ttu-id="71be5-217">Valeur de primitive qui ne peut pas être stringified JSON.</span><span class="sxs-lookup"><span data-stu-id="71be5-217">Primitive value which cannot be JSON-stringified.</span></span>  

##### <a name="allowed-values"></a><span data-ttu-id="71be5-218">Valeurs autorisées</span><span class="sxs-lookup"><span data-stu-id="71be5-218">Allowed Values</span></span>  

`Infinity`<span data-ttu-id="71be5-219">, `NaN`, `-Infinity`,</span><span class="sxs-lookup"><span data-stu-id="71be5-219">, `NaN`, `-Infinity`,</span></span> `-0`  

---  

### <a name="remoteobject-object"></a><span data-ttu-id="71be5-220">Objet RemoteObject</span><span class="sxs-lookup"><span data-stu-id="71be5-220">RemoteObject object</span></span>  

<a name="remoteobject"></a>  

<span data-ttu-id="71be5-221">Objet Miroir référencant un objet JavaScript d’origine.</span><span class="sxs-lookup"><span data-stu-id="71be5-221">Mirror object referencing original JavaScript object.</span></span>  

| <span data-ttu-id="71be5-222">Propriétés</span><span class="sxs-lookup"><span data-stu-id="71be5-222">Properties</span></span> | <span data-ttu-id="71be5-223">Type</span><span class="sxs-lookup"><span data-stu-id="71be5-223">Type</span></span> | <span data-ttu-id="71be5-224">Détails</span><span class="sxs-lookup"><span data-stu-id="71be5-224">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="71be5-225">type</span><span class="sxs-lookup"><span data-stu-id="71be5-225">type</span></span> | `string` | <span data-ttu-id="71be5-226">Type d’objet.</span><span class="sxs-lookup"><span data-stu-id="71be5-226">Object type.</span></span>  <span data-ttu-id="71be5-227">Valeurs autorisées  `object` : , , , , `function` `undefined` `string` `number` `boolean` et</span><span class="sxs-lookup"><span data-stu-id="71be5-227">Allowed values:  `object`, `function`, `undefined`, `string`, `number`, `boolean`, and</span></span> `symbol` |  
| <span data-ttu-id="71be5-228">subtype \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-228">subtype \(optional\)</span></span> | `string` | <span data-ttu-id="71be5-229">Conseil de sous-type d’objet.</span><span class="sxs-lookup"><span data-stu-id="71be5-229">Object subtype hint.</span></span>  <span data-ttu-id="71be5-230">Spécifié pour les `object` valeurs de type uniquement.</span><span class="sxs-lookup"><span data-stu-id="71be5-230">Specified for `object` type values only.</span></span>  <span data-ttu-id="71be5-231">Valeurs autorisées  `null` : `error` , et</span><span class="sxs-lookup"><span data-stu-id="71be5-231">Allowed values:  `null`, `error`, and</span></span> `promise` |  
| <span data-ttu-id="71be5-232">className \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-232">className \(optional\)</span></span> | `string` | <span data-ttu-id="71be5-233">Nom de la classe d’objet \(constructor\).</span><span class="sxs-lookup"><span data-stu-id="71be5-233">Object class \(constructor\) name.</span></span>  <span data-ttu-id="71be5-234">Spécifié pour les `object` valeurs de type uniquement.</span><span class="sxs-lookup"><span data-stu-id="71be5-234">Specified for `object` type values only.</span></span> |  
| <span data-ttu-id="71be5-235">value \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-235">value \(optional\)</span></span> | `any` | <span data-ttu-id="71be5-236">Valeur de l’objet distant en cas de valeurs primitives ou de valeurs JSON \(si elle a été demandée\).</span><span class="sxs-lookup"><span data-stu-id="71be5-236">Remote object value in case of primitive values or JSON values \(if it was requested\).</span></span> |  
| <span data-ttu-id="71be5-237">unserializableValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-237">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="71be5-238">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="71be5-238">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="71be5-239">La valeur primitive qui ne peut pas être stringified JSON n’a `value` pas , mais obtient cette propriété.</span><span class="sxs-lookup"><span data-stu-id="71be5-239">Primitive value which can not be JSON-stringified does not have `value`, but gets this property.</span></span> |  
| <span data-ttu-id="71be5-240">description \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="71be5-240">description \(optional\)</span></span> | `string` | <span data-ttu-id="71be5-241">Représentation sous la chaîne de l’objet.</span><span class="sxs-lookup"><span data-stu-id="71be5-241">String representation of the object.</span></span> |  
| <span data-ttu-id="71be5-242">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-242">objectId \(optional\)</span></span> | [<span data-ttu-id="71be5-243">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="71be5-243">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="71be5-244">Identificateur d’objet unique \(pour les valeurs non primitives\).</span><span class="sxs-lookup"><span data-stu-id="71be5-244">Unique object identifier \(for non-primitive values\).</span></span> |  
| <span data-ttu-id="71be5-245">msDebuggerPropertyId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-245">msDebuggerPropertyId \(optional\)</span></span> | `string` | <span data-ttu-id="71be5-246">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="71be5-246">**Experimental**.</span></span>  <span data-ttu-id="71be5-247">Microsoft : ID de propriété du débogger associé pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="71be5-247">Microsoft:  The associated debugger property ID for this object.</span></span> |  

---  

### <a name="propertydescriptor-object"></a><span data-ttu-id="71be5-248">Objet PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="71be5-248">PropertyDescriptor object</span></span>  

<a name="propertydescriptor"></a>  

<span data-ttu-id="71be5-249">Descripteur de propriété d’objet.</span><span class="sxs-lookup"><span data-stu-id="71be5-249">Object property descriptor.</span></span>  

| <span data-ttu-id="71be5-250">Propriétés</span><span class="sxs-lookup"><span data-stu-id="71be5-250">Properties</span></span> | <span data-ttu-id="71be5-251">Type</span><span class="sxs-lookup"><span data-stu-id="71be5-251">Type</span></span> | <span data-ttu-id="71be5-252">Détails</span><span class="sxs-lookup"><span data-stu-id="71be5-252">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="71be5-253">name</span><span class="sxs-lookup"><span data-stu-id="71be5-253">name</span></span> | `string` | <span data-ttu-id="71be5-254">Nom de la propriété ou description du symbole.</span><span class="sxs-lookup"><span data-stu-id="71be5-254">Property name or symbol description.</span></span> |  
| <span data-ttu-id="71be5-255">value \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-255">value \(optional\)</span></span> | [<span data-ttu-id="71be5-256">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="71be5-256">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="71be5-257">Valeur associée à la propriété.</span><span class="sxs-lookup"><span data-stu-id="71be5-257">The value associated with the property.</span></span> |  
| <span data-ttu-id="71be5-258">writable \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-258">writable \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="71be5-259">si la valeur associée à la propriété peut être modifiée \(descripteurs de données uniquement\).</span><span class="sxs-lookup"><span data-stu-id="71be5-259">if the value associated with the property may be changed \(data descriptors only\).</span></span> |  
| <span data-ttu-id="71be5-260">get \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-260">get \(optional\)</span></span> | [<span data-ttu-id="71be5-261">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="71be5-261">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="71be5-262">Fonction qui sert de getter pour la propriété, ou s’il n’existe pas de `undefined` getter \(descripteurs d’accesseurs uniquement\).</span><span class="sxs-lookup"><span data-stu-id="71be5-262">A function which serves as a getter for the property, or `undefined` if there is no getter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="71be5-263">set \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-263">set \(optional\)</span></span> | [<span data-ttu-id="71be5-264">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="71be5-264">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="71be5-265">Fonction qui sert de setter pour la propriété, ou s’il n’y a pas de `undefined` setter \(descripteurs d’accesseurs uniquement\).</span><span class="sxs-lookup"><span data-stu-id="71be5-265">A function which serves as a setter for the property, or `undefined` if there is no setter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="71be5-266">configurable</span><span class="sxs-lookup"><span data-stu-id="71be5-266">configurable</span></span> | `boolean` | `True` <span data-ttu-id="71be5-267">si le type de ce descripteur de propriété peut être modifié et si la propriété peut être supprimée de l’objet correspondant.</span><span class="sxs-lookup"><span data-stu-id="71be5-267">if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span> |  
| <span data-ttu-id="71be5-268">éumerable</span><span class="sxs-lookup"><span data-stu-id="71be5-268">enumerable</span></span> | `boolean` | `True` <span data-ttu-id="71be5-269">si cette propriété s’affiche lors de l’éumération des propriétés sur l’objet correspondant.</span><span class="sxs-lookup"><span data-stu-id="71be5-269">if this property shows up during enumeration of the properties on the corresponding object.</span></span> |  
| <span data-ttu-id="71be5-270">wasThrown \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-270">wasThrown \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="71be5-271">si le résultat a été lancé au cours de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="71be5-271">if the result was thrown during the evaluation.</span></span> |  
| <span data-ttu-id="71be5-272">isOwn \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-272">isOwn \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="71be5-273">si la propriété appartient à l’objet.</span><span class="sxs-lookup"><span data-stu-id="71be5-273">if the property is owned for the object.</span></span> |  
| <span data-ttu-id="71be5-274">msReturnValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-274">msReturnValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="71be5-275">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="71be5-275">**Experimental**.</span></span>  <span data-ttu-id="71be5-276">Microsoft :  `True` si la propriété est une valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="71be5-276">Microsoft:  `True` if the property is a return value.</span></span> |  
| <span data-ttu-id="71be5-277">symbol \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-277">symbol \(optional\)</span></span> | [<span data-ttu-id="71be5-278">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="71be5-278">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="71be5-279">Objet symbole de propriété, si la propriété est du `symbol` type.</span><span class="sxs-lookup"><span data-stu-id="71be5-279">Property symbol object, if the property is of the `symbol` type.</span></span> |  

---  

### <a name="callargument-object"></a><span data-ttu-id="71be5-280">Objet CallArgument</span><span class="sxs-lookup"><span data-stu-id="71be5-280">CallArgument object</span></span>  

<a name="callargument"></a>  

<span data-ttu-id="71be5-281">Représente l’argument appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="71be5-281">Represents function call argument.</span></span>  <span data-ttu-id="71be5-282">L’ID d’objet distant, la valeur de primitive non personnalisable ou l’un des deux `value` \(pour undefined\) doivent être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="71be5-282">Either remote object ID `value`, unserializable primitive value or neither of \(for undefined\) them should be specified.</span></span>  

| <span data-ttu-id="71be5-283">Propriétés</span><span class="sxs-lookup"><span data-stu-id="71be5-283">Properties</span></span> | <span data-ttu-id="71be5-284">Type</span><span class="sxs-lookup"><span data-stu-id="71be5-284">Type</span></span> | <span data-ttu-id="71be5-285">Détails</span><span class="sxs-lookup"><span data-stu-id="71be5-285">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="71be5-286">value \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-286">value \(optional\)</span></span> | `any` | <span data-ttu-id="71be5-287">Valeur primitive ou objet javascript sérialisable.</span><span class="sxs-lookup"><span data-stu-id="71be5-287">Primitive value or serializable javascript object.</span></span> |  
| <span data-ttu-id="71be5-288">unserializableValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-288">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="71be5-289">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="71be5-289">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="71be5-290">Valeur de primitive qui ne peut pas être stringified JSON.</span><span class="sxs-lookup"><span data-stu-id="71be5-290">Primitive value which can not be JSON-stringified.</span></span> |  
| <span data-ttu-id="71be5-291">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-291">objectId \(optional\)</span></span> | [<span data-ttu-id="71be5-292">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="71be5-292">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="71be5-293">Handle d’objet distant.</span><span class="sxs-lookup"><span data-stu-id="71be5-293">Remote object handle.</span></span> |  

---  

### <a name="executioncontextid-integer"></a><span data-ttu-id="71be5-294">ExecutionContextId, integer</span><span class="sxs-lookup"><span data-stu-id="71be5-294">ExecutionContextId integer</span></span>  

<a name="executioncontextid"></a>  

<span data-ttu-id="71be5-295">ID d’un contexte d’exécution.</span><span class="sxs-lookup"><span data-stu-id="71be5-295">ID of an execution context.</span></span>  

&nbsp;  

---  

### <a name="exceptiondetails-object"></a><span data-ttu-id="71be5-296">Objet ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="71be5-296">ExceptionDetails object</span></span>  

<a name="exceptiondetails"></a>  

<span data-ttu-id="71be5-297">Informations détaillées sur l’exception \(ou l’erreur\) qui a été lancée lors de la compilation ou de l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="71be5-297">Detailed information about exception \(or error\) that was thrown during script compilation or execution.</span></span>  

| <span data-ttu-id="71be5-298">Propriétés</span><span class="sxs-lookup"><span data-stu-id="71be5-298">Properties</span></span> | <span data-ttu-id="71be5-299">Type</span><span class="sxs-lookup"><span data-stu-id="71be5-299">Type</span></span> | <span data-ttu-id="71be5-300">Détails</span><span class="sxs-lookup"><span data-stu-id="71be5-300">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="71be5-301">exceptionId</span><span class="sxs-lookup"><span data-stu-id="71be5-301">exceptionId</span></span> | `integer` | <span data-ttu-id="71be5-302">ID d’exception.</span><span class="sxs-lookup"><span data-stu-id="71be5-302">Exception ID.</span></span> |  
| <span data-ttu-id="71be5-303">texte</span><span class="sxs-lookup"><span data-stu-id="71be5-303">text</span></span> | `string` | <span data-ttu-id="71be5-304">Texte d’exception, qui doit être utilisé avec l’objet exception lorsqu’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="71be5-304">Exception text, which should be used together with exception object when available.</span></span> |  
| <span data-ttu-id="71be5-305">lineNumber</span><span class="sxs-lookup"><span data-stu-id="71be5-305">lineNumber</span></span> | `integer` | <span data-ttu-id="71be5-306">Numéro de ligne de l’emplacement de l’exception \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="71be5-306">Line number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="71be5-307">columnNumber</span><span class="sxs-lookup"><span data-stu-id="71be5-307">columnNumber</span></span> | `integer` | <span data-ttu-id="71be5-308">Numéro de colonne de l’emplacement de l’exception \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="71be5-308">Column number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="71be5-309">scriptId \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="71be5-309">scriptId \(optional\)</span></span> | [<span data-ttu-id="71be5-310">ScriptId</span><span class="sxs-lookup"><span data-stu-id="71be5-310">ScriptId</span></span>](#scriptid) | <span data-ttu-id="71be5-311">ID de script de l’emplacement d’exception.</span><span class="sxs-lookup"><span data-stu-id="71be5-311">Script ID of the exception location.</span></span> |  
| <span data-ttu-id="71be5-312">url \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-312">url \(optional\)</span></span> | `string` | <span data-ttu-id="71be5-313">URL de l’emplacement de l’exception, à utiliser lorsque le script n’a pas été signalé.</span><span class="sxs-lookup"><span data-stu-id="71be5-313">URL of the exception location, to be used when the script was not reported.</span></span> |  
| <span data-ttu-id="71be5-314">stackTrace \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-314">stackTrace \(optional\)</span></span> | [<span data-ttu-id="71be5-315">StackTrace</span><span class="sxs-lookup"><span data-stu-id="71be5-315">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="71be5-316">Trace de pile JavaScript si disponible.</span><span class="sxs-lookup"><span data-stu-id="71be5-316">JavaScript stack trace if available.</span></span> |  
| <span data-ttu-id="71be5-317">exception \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="71be5-317">exception \(optional\)</span></span> | [<span data-ttu-id="71be5-318">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="71be5-318">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="71be5-319">Objet Exception, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="71be5-319">Exception object if available.</span></span> |  
| <span data-ttu-id="71be5-320">executionContextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="71be5-320">executionContextId \(optional\)</span></span> | [<span data-ttu-id="71be5-321">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="71be5-321">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="71be5-322">Identificateur du contexte dans lequel l’exception s’est produite.</span><span class="sxs-lookup"><span data-stu-id="71be5-322">Identifier of the context where exception happened.</span></span> |  

---  

### <a name="timestamp-integer"></a><span data-ttu-id="71be5-323">Timestamp integer</span><span class="sxs-lookup"><span data-stu-id="71be5-323">Timestamp integer</span></span>  

<a name="timestamp"></a>  

<span data-ttu-id="71be5-324">Nombre de millisecondes depuis l’époque.</span><span class="sxs-lookup"><span data-stu-id="71be5-324">Number of milliseconds since epoch.</span></span>  

&nbsp;  

---  

### <a name="callframe-object"></a><span data-ttu-id="71be5-325">Objet CallFrame</span><span class="sxs-lookup"><span data-stu-id="71be5-325">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="71be5-326">Entrée de pile pour les erreurs d’runtime et les assertions.</span><span class="sxs-lookup"><span data-stu-id="71be5-326">Stack entry for runtime errors and assertions.</span></span>  

| <span data-ttu-id="71be5-327">Propriétés</span><span class="sxs-lookup"><span data-stu-id="71be5-327">Properties</span></span> | <span data-ttu-id="71be5-328">Type</span><span class="sxs-lookup"><span data-stu-id="71be5-328">Type</span></span> | <span data-ttu-id="71be5-329">Détails</span><span class="sxs-lookup"><span data-stu-id="71be5-329">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="71be5-330">functionName</span><span class="sxs-lookup"><span data-stu-id="71be5-330">functionName</span></span> | `string` | <span data-ttu-id="71be5-331">Nom de la fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="71be5-331">JavaScript function name.</span></span> |  
| <span data-ttu-id="71be5-332">scriptId</span><span class="sxs-lookup"><span data-stu-id="71be5-332">scriptId</span></span> | [<span data-ttu-id="71be5-333">ScriptId</span><span class="sxs-lookup"><span data-stu-id="71be5-333">ScriptId</span></span>](#scriptid) | <span data-ttu-id="71be5-334">ID de script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="71be5-334">JavaScript script ID.</span></span> |  
| <span data-ttu-id="71be5-335">url</span><span class="sxs-lookup"><span data-stu-id="71be5-335">url</span></span> | `string` | <span data-ttu-id="71be5-336">Nom ou URL du script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="71be5-336">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="71be5-337">lineNumber</span><span class="sxs-lookup"><span data-stu-id="71be5-337">lineNumber</span></span> | `integer` | <span data-ttu-id="71be5-338">Numéro de ligne de script JavaScript \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="71be5-338">JavaScript script line number \(0-based\).</span></span> |  
| <span data-ttu-id="71be5-339">columnNumber</span><span class="sxs-lookup"><span data-stu-id="71be5-339">columnNumber</span></span> | `integer` | <span data-ttu-id="71be5-340">Numéro de colonne de script JavaScript \(basé sur 0\).</span><span class="sxs-lookup"><span data-stu-id="71be5-340">JavaScript script column number \(0-based\).</span></span> |  

---  

### <a name="stacktrace-object"></a><span data-ttu-id="71be5-341">Objet StackTrace</span><span class="sxs-lookup"><span data-stu-id="71be5-341">StackTrace object</span></span>  

<a name="stacktrace"></a>  

<span data-ttu-id="71be5-342">Appelez des cadres pour les assertions ou les messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="71be5-342">Call frames for assertions or error messages.</span></span>  

| <span data-ttu-id="71be5-343">Propriétés</span><span class="sxs-lookup"><span data-stu-id="71be5-343">Properties</span></span> | <span data-ttu-id="71be5-344">Type</span><span class="sxs-lookup"><span data-stu-id="71be5-344">Type</span></span> | <span data-ttu-id="71be5-345">Détails</span><span class="sxs-lookup"><span data-stu-id="71be5-345">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="71be5-346">description \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="71be5-346">description \(optional\)</span></span> | `string` | <span data-ttu-id="71be5-347">Étiquette de chaîne de cette trace de pile.</span><span class="sxs-lookup"><span data-stu-id="71be5-347">String label of this stack trace.</span></span>  <span data-ttu-id="71be5-348">Pour les suivis async, il peut s’agit d’un nom de la fonction qui a initié l’appel async.</span><span class="sxs-lookup"><span data-stu-id="71be5-348">For async traces this may be a name of the function that initiated the async call.</span></span> |  
| <span data-ttu-id="71be5-349">callFrames</span><span class="sxs-lookup"><span data-stu-id="71be5-349">callFrames</span></span> | [<span data-ttu-id="71be5-350">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="71be5-350">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="71be5-351">Nom de la fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="71be5-351">JavaScript function name.</span></span> |  
| <span data-ttu-id="71be5-352">parent \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="71be5-352">parent \(optional\)</span></span> | [<span data-ttu-id="71be5-353">StackTrace</span><span class="sxs-lookup"><span data-stu-id="71be5-353">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="71be5-354">Trace de pile JavaScript asynchrone précédant cette pile, si disponible.</span><span class="sxs-lookup"><span data-stu-id="71be5-354">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span> |  

---  
