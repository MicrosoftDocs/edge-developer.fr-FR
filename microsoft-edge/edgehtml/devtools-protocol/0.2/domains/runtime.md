---
description: Référence du protocole DevTools version 0.2 (EdgeHTML) pour le domaine d’runtime. Le domaine runtime expose le runtime JavaScript au moyen d’objets miroir et d’évaluation à distance. Les résultats de l’évaluation sont renvoyés en tant qu’objet miroir qui exposent le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour d’autres références d’objet. Les objets d’origine sont conservés en mémoire, sauf s’ils sont libérés explicitement.
title: Domaine d’runtime - DevTools Protocol Version 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: afc79a17c5002f60806872a9add57f518ff6cb45
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398139"
---
# <a name="runtime-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="c0a57-106">Domaine d’runtime - DevTools Protocol Version 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="c0a57-106">Runtime Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="c0a57-107">Le domaine d’runtime expose le runtime JavaScript au moyen d’objets d’évaluation et de miroir distants.</span><span class="sxs-lookup"><span data-stu-id="c0a57-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="c0a57-108">Les résultats de l’évaluation sont renvoyés en tant qu’objet miroir qui exposent le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour d’autres références d’objet.</span><span class="sxs-lookup"><span data-stu-id="c0a57-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="c0a57-109">Les objets d’origine sont conservés en mémoire, sauf s’ils sont libérés explicitement.</span><span class="sxs-lookup"><span data-stu-id="c0a57-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>  

| <span data-ttu-id="c0a57-110">Classification</span><span class="sxs-lookup"><span data-stu-id="c0a57-110">Classification</span></span> | <span data-ttu-id="c0a57-111">Membres</span><span class="sxs-lookup"><span data-stu-id="c0a57-111">Members</span></span> |  
|:--- |:--- |  
| [**<span data-ttu-id="c0a57-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c0a57-112">Methods</span></span>**](#methods) | <span data-ttu-id="c0a57-113">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span><span class="sxs-lookup"><span data-stu-id="c0a57-113">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span></span> |  
| [**<span data-ttu-id="c0a57-114">Événements</span><span class="sxs-lookup"><span data-stu-id="c0a57-114">Events</span></span>**](#events) | <span data-ttu-id="c0a57-115">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span><span class="sxs-lookup"><span data-stu-id="c0a57-115">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span></span> |  
| [**<span data-ttu-id="c0a57-116">Types</span><span class="sxs-lookup"><span data-stu-id="c0a57-116">Types</span></span>**](#types) | <span data-ttu-id="c0a57-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="c0a57-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |  

## <a name="methods"></a><span data-ttu-id="c0a57-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c0a57-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="c0a57-119">activer</span><span class="sxs-lookup"><span data-stu-id="c0a57-119">enable</span></span>  

<span data-ttu-id="c0a57-120">Permet de signaler les `executionContextCreated` événements `executionContextDestroyed` et les `executionContextsCleared` événements.</span><span class="sxs-lookup"><span data-stu-id="c0a57-120">Enables reporting of the `executionContextCreated`, `executionContextDestroyed`, and `executionContextsCleared` events.</span></span>  <span data-ttu-id="c0a57-121">Lorsque le rapport est activé, l’événement est envoyé immédiatement `executionContextCreated` pour chaque contexte d’exécution existant.</span><span class="sxs-lookup"><span data-stu-id="c0a57-121">When the reporting gets enabled the `executionContextCreated` event will be sent immediately for each existing execution context.</span></span>  

---  

### <a name="disable"></a><span data-ttu-id="c0a57-122">désactiver </span><span class="sxs-lookup"><span data-stu-id="c0a57-122">disable</span></span>  

<span data-ttu-id="c0a57-123">Désactive le signalement des `executionContextCreated` `executionContextDestroyed` événements et des `executionContextsCleared` événements.</span><span class="sxs-lookup"><span data-stu-id="c0a57-123">Disables reporting of the `executionContextCreated`, `executionContextDestroyed`, and `executionContextsCleared` events.</span></span>  

---  

### <a name="evaluate"></a><span data-ttu-id="c0a57-124">évaluer</span><span class="sxs-lookup"><span data-stu-id="c0a57-124">evaluate</span></span>  

<span data-ttu-id="c0a57-125">Évalue l’expression sur l’objet global.</span><span class="sxs-lookup"><span data-stu-id="c0a57-125">Evaluates expression on global object.</span></span>  

| <span data-ttu-id="c0a57-126">Parameters</span><span class="sxs-lookup"><span data-stu-id="c0a57-126">Parameters</span></span> | <span data-ttu-id="c0a57-127">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-127">Type</span></span> | <span data-ttu-id="c0a57-128">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-128">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-129">expression</span><span class="sxs-lookup"><span data-stu-id="c0a57-129">expression</span></span> | `string` | <span data-ttu-id="c0a57-130">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="c0a57-130">Expression to evaluate.</span></span> |  
| <span data-ttu-id="c0a57-131">includeCommandLineAPI \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-131">includeCommandLineAPI \(optional\)</span></span> | `boolean` | <span data-ttu-id="c0a57-132">Détermine si l’API de ligne de commande doit être disponible pendant l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="c0a57-132">Determines whether Command Line API should be available during the evaluation.</span></span> |  
| <span data-ttu-id="c0a57-133">objectGroup \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-133">objectGroup \(optional\)</span></span> | `string` | <span data-ttu-id="c0a57-134">Nom de groupe symbolique qui peut être utilisé pour libérer plusieurs objets.</span><span class="sxs-lookup"><span data-stu-id="c0a57-134">Symbolic group name that can be used to release multiple objects.</span></span> |  
| <span data-ttu-id="c0a57-135">silent \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-135">silent \(optional\)</span></span> | `boolean` | <span data-ttu-id="c0a57-136">En mode silencieux, les exceptions lancées lors de l’évaluation ne sont pas signalées et ne suspendent pas l’exécution.</span><span class="sxs-lookup"><span data-stu-id="c0a57-136">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span>  <span data-ttu-id="c0a57-137">Remplace `setPauseOnException` l’état.</span><span class="sxs-lookup"><span data-stu-id="c0a57-137">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="c0a57-138">contextId \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-138">contextId \(optional\)</span></span> | [<span data-ttu-id="c0a57-139">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="c0a57-139">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="c0a57-140">Spécifie dans quel contexte d’exécution effectuer l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="c0a57-140">Specifies in which execution context to perform evaluation.</span></span>  <span data-ttu-id="c0a57-141">Si le paramètre est omis, l’évaluation est effectuée dans le contexte de la page inspectée.</span><span class="sxs-lookup"><span data-stu-id="c0a57-141">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span> |  
| <span data-ttu-id="c0a57-142">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-142">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="c0a57-143">Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</span><span class="sxs-lookup"><span data-stu-id="c0a57-143">Whether the result is expected to be a JSON object that should be sent by value.</span></span> |  
| <span data-ttu-id="c0a57-144">awaitPromise \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-144">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="c0a57-145">Si l’exécution doit être résolue pour la valeur et le retour une fois `await` la promesse attendue résolue.</span><span class="sxs-lookup"><span data-stu-id="c0a57-145">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  

| <span data-ttu-id="c0a57-146">Renvoie</span><span class="sxs-lookup"><span data-stu-id="c0a57-146">Returns</span></span> | <span data-ttu-id="c0a57-147">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-147">Type</span></span> | <span data-ttu-id="c0a57-148">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-148">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-149">result</span><span class="sxs-lookup"><span data-stu-id="c0a57-149">result</span></span> | [<span data-ttu-id="c0a57-150">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="c0a57-150">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="c0a57-151">Résultat de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="c0a57-151">Evaluation result.</span></span> |  

---  

### <a name="callfunctionon"></a><span data-ttu-id="c0a57-152">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="c0a57-152">callFunctionOn</span></span>  

<span data-ttu-id="c0a57-153">Appelle la fonction avec déclaration donnée sur l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="c0a57-153">Calls function with given declaration on the given object.</span></span>  <span data-ttu-id="c0a57-154">Le groupe d’objets du résultat est hérité de l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="c0a57-154">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="c0a57-155">Parameters</span><span class="sxs-lookup"><span data-stu-id="c0a57-155">Parameters</span></span> | <span data-ttu-id="c0a57-156">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-156">Type</span></span> | <span data-ttu-id="c0a57-157">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-157">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-158">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="c0a57-158">functionDeclaration</span></span> | `string` | <span data-ttu-id="c0a57-159">Déclaration de la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="c0a57-159">Declaration of the function to call.</span></span> |  
| <span data-ttu-id="c0a57-160">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-160">objectId \(optional\)</span></span> | [<span data-ttu-id="c0a57-161">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="c0a57-161">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="c0a57-162">Identificateur de l’objet sur qui appeler la fonction.</span><span class="sxs-lookup"><span data-stu-id="c0a57-162">Identifier of the object to call function on.</span></span>  <span data-ttu-id="c0a57-163">`objectId` `executionContextId` L’une ou l’autre doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c0a57-163">Either `objectId` or `executionContextId` should be specified.</span></span>  `objectId` <span data-ttu-id="c0a57-164">doit être issu de la `Runtime.evaluate()` fonction.</span><span class="sxs-lookup"><span data-stu-id="c0a57-164">must be from the `Runtime.evaluate()` function.</span></span> |  
| <span data-ttu-id="c0a57-165">arguments \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-165">arguments \(optional\)</span></span> | [<span data-ttu-id="c0a57-166">CallArgument[]</span><span class="sxs-lookup"><span data-stu-id="c0a57-166">CallArgument[]</span></span>](#callargument) | <span data-ttu-id="c0a57-167">Arguments d’appel.</span><span class="sxs-lookup"><span data-stu-id="c0a57-167">Call arguments.</span></span>  <span data-ttu-id="c0a57-168">Tous les arguments d’appel doivent appartenir au même monde JavaScript que l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="c0a57-168">All call arguments must belong to the same JavaScript world as the target object.</span></span> |  
| <span data-ttu-id="c0a57-169">booléen \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-169">boolean \(optional\)</span></span> | `boolean` | <span data-ttu-id="c0a57-170">En mode silencieux, les exceptions lancées lors de l’évaluation ne sont pas signalées et ne suspendent pas l’exécution.</span><span class="sxs-lookup"><span data-stu-id="c0a57-170">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="c0a57-171">Remplace `setPauseOnException` l’état.</span><span class="sxs-lookup"><span data-stu-id="c0a57-171">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="c0a57-172">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-172">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="c0a57-173">Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</span><span class="sxs-lookup"><span data-stu-id="c0a57-173">Whether the result is expected to be a JSON object which should be sent by value.</span></span> |  
| <span data-ttu-id="c0a57-174">awaitPromise \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-174">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="c0a57-175">Si l’exécution doit être résolue pour la valeur et le retour une fois `await` la promesse attendue résolue.</span><span class="sxs-lookup"><span data-stu-id="c0a57-175">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  
| <span data-ttu-id="c0a57-176">executionContextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-176">executionContextId \(optional\)</span></span> | [<span data-ttu-id="c0a57-177">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="c0a57-177">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="c0a57-178">Spécifie le contexte d’exécution sur lequel l’objet global sera utilisé pour appeler la fonction.</span><span class="sxs-lookup"><span data-stu-id="c0a57-178">Specifies execution context which global object will be used to call function on.</span></span>  <span data-ttu-id="c0a57-179">Soit</span><span class="sxs-lookup"><span data-stu-id="c0a57-179">Either</span></span>
`executionContextId` <span data-ttu-id="c0a57-180">ou `objectId` doit être spécifié</span><span class="sxs-lookup"><span data-stu-id="c0a57-180">or `objectId` should be specified</span></span> |  
| <span data-ttu-id="c0a57-181">objectGroup \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-181">objectGroup \(optional\)</span></span> | `string` | <span data-ttu-id="c0a57-182">Nom de groupe symbolique qui peut être utilisé pour libérer plusieurs objets.</span><span class="sxs-lookup"><span data-stu-id="c0a57-182">Symbolic group name that can be used to release multiple objects.</span></span>  <span data-ttu-id="c0a57-183">Si `objectGroup` elle n’est pas spécifiée `objectId` et qu’elle l’est, elle `objectGroup` sera héritée de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c0a57-183">If `objectGroup` is not specified and `objectId` is, `objectGroup` will be inherited from object.</span></span> |  

| <span data-ttu-id="c0a57-184">Renvoie</span><span class="sxs-lookup"><span data-stu-id="c0a57-184">Returns</span></span> | <span data-ttu-id="c0a57-185">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-185">Type</span></span> | <span data-ttu-id="c0a57-186">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-186">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-187">result</span><span class="sxs-lookup"><span data-stu-id="c0a57-187">result</span></span> | [<span data-ttu-id="c0a57-188">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="c0a57-188">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="c0a57-189">Résultat de l’appel.</span><span class="sxs-lookup"><span data-stu-id="c0a57-189">Call result.</span></span> |  

---  

### <a name="awaitpromise"></a><span data-ttu-id="c0a57-190">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="c0a57-190">awaitPromise</span></span>  

<span data-ttu-id="c0a57-191">Ajoutez un handler à la promesse avec un ID d’objet promise donné.</span><span class="sxs-lookup"><span data-stu-id="c0a57-191">Add handler to promise with given promise object id.</span></span>  

| <span data-ttu-id="c0a57-192">Parameters</span><span class="sxs-lookup"><span data-stu-id="c0a57-192">Parameters</span></span> | <span data-ttu-id="c0a57-193">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-193">Type</span></span> | <span data-ttu-id="c0a57-194">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-194">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-195">promiseObjectId</span><span class="sxs-lookup"><span data-stu-id="c0a57-195">promiseObjectId</span></span> | [<span data-ttu-id="c0a57-196">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="c0a57-196">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="c0a57-197">Identificateur de la promesse.</span><span class="sxs-lookup"><span data-stu-id="c0a57-197">Identifier of the promise.</span></span> |  
| <span data-ttu-id="c0a57-198">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-198">returnByValue \(optional\)</span></span> | <span data-ttu-id="c0a57-199">booléen</span><span class="sxs-lookup"><span data-stu-id="c0a57-199">boolean</span></span> | <span data-ttu-id="c0a57-200">Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</span><span class="sxs-lookup"><span data-stu-id="c0a57-200">Whether the result is expected to be a JSON object that should be sent by value.</span></span> |  

| <span data-ttu-id="c0a57-201">Renvoie</span><span class="sxs-lookup"><span data-stu-id="c0a57-201">Returns</span></span> | <span data-ttu-id="c0a57-202">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-202">Type</span></span> | <span data-ttu-id="c0a57-203">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-203">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-204">result</span><span class="sxs-lookup"><span data-stu-id="c0a57-204">result</span></span> | [<span data-ttu-id="c0a57-205">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="c0a57-205">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="c0a57-206">Résultat de la promesse.</span><span class="sxs-lookup"><span data-stu-id="c0a57-206">Promise result.</span></span>  <span data-ttu-id="c0a57-207">Contient la valeur rejetée si la promesse a été rejetée.</span><span class="sxs-lookup"><span data-stu-id="c0a57-207">Will contain rejected value if promise was rejected.</span></span> |  

---  

### <a name="getproperties"></a><span data-ttu-id="c0a57-208">getProperties</span><span class="sxs-lookup"><span data-stu-id="c0a57-208">getProperties</span></span>  

<span data-ttu-id="c0a57-209">Renvoie les propriétés d’un objet donné.</span><span class="sxs-lookup"><span data-stu-id="c0a57-209">Returns properties of a given object.</span></span> <span data-ttu-id="c0a57-210">Le groupe d’objets du résultat est hérité de l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="c0a57-210">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="c0a57-211">Parameters</span><span class="sxs-lookup"><span data-stu-id="c0a57-211">Parameters</span></span> | <span data-ttu-id="c0a57-212">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-212">Type</span></span> | <span data-ttu-id="c0a57-213">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-213">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-214">objectId</span><span class="sxs-lookup"><span data-stu-id="c0a57-214">objectId</span></span> | [<span data-ttu-id="c0a57-215">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="c0a57-215">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="c0a57-216">Identificateur de l’objet pour qui renvoyer les propriétés.</span><span class="sxs-lookup"><span data-stu-id="c0a57-216">Identifier of the object to return properties for.</span></span>  `objectId` <span data-ttu-id="c0a57-217">doit être issu de la `Debugger.evaluateOnCallFrame()` fonction.</span><span class="sxs-lookup"><span data-stu-id="c0a57-217">must be from the `Debugger.evaluateOnCallFrame()` function.</span></span> |  
| <span data-ttu-id="c0a57-218">ownProperties \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-218">ownProperties \(optional\)</span></span> | `boolean` | <span data-ttu-id="c0a57-219">Si `true` , renvoie les propriétés appartenant uniquement à l’élément lui-même, et non à sa chaîne prototype.</span><span class="sxs-lookup"><span data-stu-id="c0a57-219">If `true`, returns properties belonging only to the element itself, not to its prototype chain.</span></span> |  
| <span data-ttu-id="c0a57-220">accessorPropertiesOnly \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-220">accessorPropertiesOnly \(optional\)</span></span> | `boolean` | <span data-ttu-id="c0a57-221">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="c0a57-221">**Experimental**.</span></span>  <span data-ttu-id="c0a57-222">Si `true` , renvoie les propriétés d’accesseur \(avec getter/setter\) uniquement ; les propriétés internes ne sont pas renvoyées non plus.</span><span class="sxs-lookup"><span data-stu-id="c0a57-222">If `true`, returns accessor properties \(with getter/setter\) only; internal properties are not returned either.</span></span> |  

| <span data-ttu-id="c0a57-223">Renvoie</span><span class="sxs-lookup"><span data-stu-id="c0a57-223">Returns</span></span> | <span data-ttu-id="c0a57-224">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-224">Type</span></span> | <span data-ttu-id="c0a57-225">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-225">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-226">result</span><span class="sxs-lookup"><span data-stu-id="c0a57-226">result</span></span> | [<span data-ttu-id="c0a57-227">PropertyDescriptor[]</span><span class="sxs-lookup"><span data-stu-id="c0a57-227">PropertyDescriptor[]</span></span>](#propertydescriptor) | <span data-ttu-id="c0a57-228">Propriétés de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c0a57-228">Object properties.</span></span> |  

---  

### <a name="globallexicalscopenames"></a><span data-ttu-id="c0a57-229">globalLexicalScopeNames</span><span class="sxs-lookup"><span data-stu-id="c0a57-229">globalLexicalScopeNames</span></span>  

<span data-ttu-id="c0a57-230">Renvoie toutes les variables let, const et class de l’étendue globale de la console.</span><span class="sxs-lookup"><span data-stu-id="c0a57-230">Returns all let, const, and class variables from the console global scope.</span></span>  

| <span data-ttu-id="c0a57-231">Renvoie</span><span class="sxs-lookup"><span data-stu-id="c0a57-231">Returns</span></span> | <span data-ttu-id="c0a57-232">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-232">Type</span></span> | <span data-ttu-id="c0a57-233">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-233">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-234">names</span><span class="sxs-lookup"><span data-stu-id="c0a57-234">names</span></span> | `string[]` | &nbsp; |  

---  

### <a name="releaseobject"></a><span data-ttu-id="c0a57-235">releaseObject</span><span class="sxs-lookup"><span data-stu-id="c0a57-235">releaseObject</span></span>  

<span data-ttu-id="c0a57-236">Libère l’objet distant avec un ID donné.</span><span class="sxs-lookup"><span data-stu-id="c0a57-236">Releases remote object with given ID.</span></span>  

| <span data-ttu-id="c0a57-237">Parameters</span><span class="sxs-lookup"><span data-stu-id="c0a57-237">Parameters</span></span> | <span data-ttu-id="c0a57-238">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-238">Type</span></span> | <span data-ttu-id="c0a57-239">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-239">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-240">objectId</span><span class="sxs-lookup"><span data-stu-id="c0a57-240">objectId</span></span> | [<span data-ttu-id="c0a57-241">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="c0a57-241">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="c0a57-242">Identificateur de l’objet à libérer.</span><span class="sxs-lookup"><span data-stu-id="c0a57-242">Identifier of the object to release.</span></span> |  

---  

### <a name="releaseobjectgroup"></a><span data-ttu-id="c0a57-243">releaseObjectGroup</span><span class="sxs-lookup"><span data-stu-id="c0a57-243">releaseObjectGroup</span></span>  

<span data-ttu-id="c0a57-244">Libère tous les objets distants appartenant à un groupe donné.</span><span class="sxs-lookup"><span data-stu-id="c0a57-244">Releases all remote objects that belong to a given group.</span></span>  

| <span data-ttu-id="c0a57-245">Parameters</span><span class="sxs-lookup"><span data-stu-id="c0a57-245">Parameters</span></span> | <span data-ttu-id="c0a57-246">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-246">Type</span></span> | <span data-ttu-id="c0a57-247">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-247">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-248">objectGroup</span><span class="sxs-lookup"><span data-stu-id="c0a57-248">objectGroup</span></span> | `string` | <span data-ttu-id="c0a57-249">Nom du groupe d’objets symboliques.</span><span class="sxs-lookup"><span data-stu-id="c0a57-249">Symbolic object group name.</span></span> |  

---  

### <a name="discardconsoleentries"></a><span data-ttu-id="c0a57-250">discardConsoleEntries</span><span class="sxs-lookup"><span data-stu-id="c0a57-250">discardConsoleEntries</span></span>  

<span data-ttu-id="c0a57-251">Rejette les exceptions collectées et les appels d’API de console.</span><span class="sxs-lookup"><span data-stu-id="c0a57-251">Discards collected exceptions and console API calls.</span></span>  

---  

## <a name="events"></a><span data-ttu-id="c0a57-252">Événements</span><span class="sxs-lookup"><span data-stu-id="c0a57-252">Events</span></span>  

### <a name="executioncontextcreated"></a><span data-ttu-id="c0a57-253">executionContextCreated</span><span class="sxs-lookup"><span data-stu-id="c0a57-253">executionContextCreated</span></span>  

<span data-ttu-id="c0a57-254">Émis lors de la création d’un contexte d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c0a57-254">Issued when new execution context is created.</span></span>  

| <span data-ttu-id="c0a57-255">Parameters</span><span class="sxs-lookup"><span data-stu-id="c0a57-255">Parameters</span></span> | <span data-ttu-id="c0a57-256">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-256">Type</span></span> | <span data-ttu-id="c0a57-257">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-257">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-258">context</span><span class="sxs-lookup"><span data-stu-id="c0a57-258">context</span></span> | [<span data-ttu-id="c0a57-259">ExecutionContextDescription</span><span class="sxs-lookup"><span data-stu-id="c0a57-259">ExecutionContextDescription</span></span>](#executioncontextdescription) | <span data-ttu-id="c0a57-260">Contexte d’exécution nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="c0a57-260">A newly created execution context.</span></span> |  

---  

### <a name="executioncontextdestroyed"></a><span data-ttu-id="c0a57-261">executionContextDestroyed</span><span class="sxs-lookup"><span data-stu-id="c0a57-261">executionContextDestroyed</span></span>  

<span data-ttu-id="c0a57-262">Émis lorsque le contexte d’exécution est détruit.</span><span class="sxs-lookup"><span data-stu-id="c0a57-262">Issued when execution context is destroyed.</span></span>  

| <span data-ttu-id="c0a57-263">Parameters</span><span class="sxs-lookup"><span data-stu-id="c0a57-263">Parameters</span></span> | <span data-ttu-id="c0a57-264">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-264">Type</span></span> | <span data-ttu-id="c0a57-265">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-265">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-266">executionContextId</span><span class="sxs-lookup"><span data-stu-id="c0a57-266">executionContextId</span></span> | [<span data-ttu-id="c0a57-267">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="c0a57-267">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="c0a57-268">ID du contexte détruit.</span><span class="sxs-lookup"><span data-stu-id="c0a57-268">ID of the destroyed context.</span></span> |  

---  

### <a name="executioncontextscleared"></a><span data-ttu-id="c0a57-269">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="c0a57-269">executionContextsCleared</span></span>  

<span data-ttu-id="c0a57-270">Émis lorsque tous les executionContexts ont été effacés dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="c0a57-270">Issued when all executionContexts were cleared in browser.</span></span>  

&nbsp;  

---  

### <a name="exceptionthrown"></a><span data-ttu-id="c0a57-271">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="c0a57-271">exceptionThrown</span></span>  

<span data-ttu-id="c0a57-272">Émise lorsque l’exception a été levée et nonhandée.</span><span class="sxs-lookup"><span data-stu-id="c0a57-272">Issued when exception was thrown and unhandled.</span></span>  

| <span data-ttu-id="c0a57-273">Parameters</span><span class="sxs-lookup"><span data-stu-id="c0a57-273">Parameters</span></span> | <span data-ttu-id="c0a57-274">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-274">Type</span></span> | <span data-ttu-id="c0a57-275">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-275">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-276">timestamp</span><span class="sxs-lookup"><span data-stu-id="c0a57-276">timestamp</span></span> | [<span data-ttu-id="c0a57-277">Horodateur</span><span class="sxs-lookup"><span data-stu-id="c0a57-277">Timestamp</span></span>](#timestamp) | <span data-ttu-id="c0a57-278">Timestamp de l’exception.</span><span class="sxs-lookup"><span data-stu-id="c0a57-278">Timestamp of the exception.</span></span> |  
| <span data-ttu-id="c0a57-279">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="c0a57-279">exceptionDetails</span></span> | [<span data-ttu-id="c0a57-280">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="c0a57-280">ExceptionDetails</span></span>](#exceptiondetails) | &nbsp; |  

---  

### <a name="consoleapicalled"></a><span data-ttu-id="c0a57-281">consoleAPICalled</span><span class="sxs-lookup"><span data-stu-id="c0a57-281">consoleAPICalled</span></span>  

| <span data-ttu-id="c0a57-282">Parameters</span><span class="sxs-lookup"><span data-stu-id="c0a57-282">Parameters</span></span> | <span data-ttu-id="c0a57-283">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-283">Type</span></span> | <span data-ttu-id="c0a57-284">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-284">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-285">type</span><span class="sxs-lookup"><span data-stu-id="c0a57-285">type</span></span> | `string` | <span data-ttu-id="c0a57-286">Type de l’appel.</span><span class="sxs-lookup"><span data-stu-id="c0a57-286">Type of the call.</span></span>  <span data-ttu-id="c0a57-287">Valeurs autorisées  `log` : , , , , , , , `info` , , , `warning` , , , `error` , `debug` `assert` `table` `trace` `dir` , `dirxml` `clear` `select` `count` `countReset` `timeEnd` `timeStamp` `startGroup` `startGroupCollapsed` et</span><span class="sxs-lookup"><span data-stu-id="c0a57-287">Allowed values:  `log`, `info`, `warning`, `error`, `debug`, `assert`, `table`, `trace`, `dir`, `dirxml`, `clear`, `select`, `count`, `countReset`, `timeEnd`, `timeStamp`, `startGroup`, `startGroupCollapsed`, and</span></span> `endGroup` |  
| <span data-ttu-id="c0a57-288">args</span><span class="sxs-lookup"><span data-stu-id="c0a57-288">args</span></span> | <span data-ttu-id="c0a57-289">[RemoteObject[]] (#remoteobject</span><span class="sxs-lookup"><span data-stu-id="c0a57-289">[RemoteObject[]](#remoteobject</span></span> | <span data-ttu-id="c0a57-290">Arguments d’appel.</span><span class="sxs-lookup"><span data-stu-id="c0a57-290">Call arguments.</span></span> |  
| <span data-ttu-id="c0a57-291">executionContextId</span><span class="sxs-lookup"><span data-stu-id="c0a57-291">executionContextId</span></span> | [<span data-ttu-id="c0a57-292">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="c0a57-292">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="c0a57-293">Identificateur du contexte dans lequel l’appel de console a été effectué.</span><span class="sxs-lookup"><span data-stu-id="c0a57-293">Identifier of the context where console call was made.</span></span> |  
| <span data-ttu-id="c0a57-294">timestamp \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-294">timestamp \(optional\)</span></span> | [<span data-ttu-id="c0a57-295">Horodateur</span><span class="sxs-lookup"><span data-stu-id="c0a57-295">Timestamp</span></span>](#timestamp) | <span data-ttu-id="c0a57-296">Appel de l’timestamp.</span><span class="sxs-lookup"><span data-stu-id="c0a57-296">Call timestamp.</span></span> |  
| <span data-ttu-id="c0a57-297">stackTrace \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-297">stackTrace \(optional\)</span></span> | [<span data-ttu-id="c0a57-298">StackTrace</span><span class="sxs-lookup"><span data-stu-id="c0a57-298">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="c0a57-299">Trace de pile capturée si disponible.</span><span class="sxs-lookup"><span data-stu-id="c0a57-299">Stack trace captured if available.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="c0a57-300">Types</span><span class="sxs-lookup"><span data-stu-id="c0a57-300">Types</span></span>  

### <a name="scriptid-string"></a><span data-ttu-id="c0a57-301">Chaîne ScriptId</span><span class="sxs-lookup"><span data-stu-id="c0a57-301">ScriptId string</span></span>  

<a name="scriptid"></a>

<span data-ttu-id="c0a57-302">Identificateur de script unique.</span><span class="sxs-lookup"><span data-stu-id="c0a57-302">Unique script identifier.</span></span>  

&nbsp;  

---  

### <a name="remoteobjectid-string"></a><span data-ttu-id="c0a57-303">Chaîne RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="c0a57-303">RemoteObjectId string</span></span>  

<a name="remoteobjectid"></a>

<span data-ttu-id="c0a57-304">Identificateur d’objet unique.</span><span class="sxs-lookup"><span data-stu-id="c0a57-304">Unique object identifier.</span></span>  

&nbsp;  

---  

### <a name="unserializablevalue-string"></a><span data-ttu-id="c0a57-305">Chaîne UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="c0a57-305">UnserializableValue string</span></span>  

<a name="unserializablevalue"></a>  

<span data-ttu-id="c0a57-306">Valeur de primitive qui ne peut pas être stringified JSON.</span><span class="sxs-lookup"><span data-stu-id="c0a57-306">Primitive value which cannot be JSON-stringified.</span></span>  

##### <a name="allowed-values"></a><span data-ttu-id="c0a57-307">Valeurs autorisées</span><span class="sxs-lookup"><span data-stu-id="c0a57-307">Allowed Values</span></span>  

`Infinity`<span data-ttu-id="c0a57-308">, `NaN`, `-Infinity`,</span><span class="sxs-lookup"><span data-stu-id="c0a57-308">, `NaN`, `-Infinity`,</span></span> `-0`  

---  

### <a name="remoteobject-object"></a><span data-ttu-id="c0a57-309">Objet RemoteObject</span><span class="sxs-lookup"><span data-stu-id="c0a57-309">RemoteObject object</span></span>  

<a name="remoteobject"></a>  

<span data-ttu-id="c0a57-310">Objet Miroir référencant un objet JavaScript d’origine.</span><span class="sxs-lookup"><span data-stu-id="c0a57-310">Mirror object referencing original JavaScript object.</span></span>  

| <span data-ttu-id="c0a57-311">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0a57-311">Properties</span></span> | <span data-ttu-id="c0a57-312">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-312">Type</span></span> | <span data-ttu-id="c0a57-313">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-313">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-314">type</span><span class="sxs-lookup"><span data-stu-id="c0a57-314">type</span></span> | `string` | <span data-ttu-id="c0a57-315">Type d’objet.</span><span class="sxs-lookup"><span data-stu-id="c0a57-315">Object type.</span></span>  <span data-ttu-id="c0a57-316">Valeurs autorisées  `object` : , , , , `function` `undefined` `string` `number` `boolean` et</span><span class="sxs-lookup"><span data-stu-id="c0a57-316">Allowed values:  `object`, `function`, `undefined`, `string`, `number`, `boolean`, and</span></span> `symbol` |  
| <span data-ttu-id="c0a57-317">subtype \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-317">subtype \(optional\)</span></span> | `string` | <span data-ttu-id="c0a57-318">Conseil de sous-type d’objet.</span><span class="sxs-lookup"><span data-stu-id="c0a57-318">Object subtype hint.</span></span>  <span data-ttu-id="c0a57-319">Spécifié pour les `object` valeurs de type uniquement.</span><span class="sxs-lookup"><span data-stu-id="c0a57-319">Specified for `object` type values only.</span></span>  <span data-ttu-id="c0a57-320">Valeurs autorisées  `null` : `error` , `promise` et</span><span class="sxs-lookup"><span data-stu-id="c0a57-320">Allowed values:  `null`, `error`, `promise`, and</span></span> `node` |  
| <span data-ttu-id="c0a57-321">className \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-321">className \(optional\)</span></span> | `string` | <span data-ttu-id="c0a57-322">Nom de la classe d’objet \(constructor\).</span><span class="sxs-lookup"><span data-stu-id="c0a57-322">Object class \(constructor\) name.</span></span>  <span data-ttu-id="c0a57-323">Spécifié pour les `object` valeurs de type uniquement.</span><span class="sxs-lookup"><span data-stu-id="c0a57-323">Specified for `object` type values only.</span></span> |  
| <span data-ttu-id="c0a57-324">value \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-324">value \(optional\)</span></span> | `any` | <span data-ttu-id="c0a57-325">Valeur de l’objet distant en cas de valeurs primitives ou de valeurs JSON \(si elle a été demandée\).</span><span class="sxs-lookup"><span data-stu-id="c0a57-325">Remote object value in case of primitive values or JSON values \(if it was requested\).</span></span> |  
| <span data-ttu-id="c0a57-326">unserializableValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-326">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="c0a57-327">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="c0a57-327">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="c0a57-328">La valeur primitive qui ne peut pas être stringified JSON n’a `value` pas , mais obtient cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c0a57-328">Primitive value which can not be JSON-stringified does not have `value`, but gets this property.</span></span> |  
| <span data-ttu-id="c0a57-329">description \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-329">description \(optional\)</span></span> | `string` | <span data-ttu-id="c0a57-330">Représentation sous la chaîne de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c0a57-330">String representation of the object.</span></span> |  
| <span data-ttu-id="c0a57-331">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-331">objectId \(optional\)</span></span> | [<span data-ttu-id="c0a57-332">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="c0a57-332">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="c0a57-333">Identificateur d’objet unique \(pour les valeurs non primitives\).</span><span class="sxs-lookup"><span data-stu-id="c0a57-333">Unique object identifier \(for non-primitive values\).</span></span> |  
| <span data-ttu-id="c0a57-334">msDebuggerPropertyId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-334">msDebuggerPropertyId \(optional\)</span></span> | `string` | <span data-ttu-id="c0a57-335">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="c0a57-335">**Experimental**.</span></span>  <span data-ttu-id="c0a57-336">Microsoft : ID de propriété de débogger associé pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="c0a57-336">Microsoft:  The associated debugger property ID for this object.</span></span> |  

---  

### <a name="propertydescriptor-object"></a><span data-ttu-id="c0a57-337">Objet PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="c0a57-337">PropertyDescriptor object</span></span>  

<a name="propertydescriptor"></a>  

<span data-ttu-id="c0a57-338">Descripteur de propriété d’objet.</span><span class="sxs-lookup"><span data-stu-id="c0a57-338">Object property descriptor.</span></span>  

| <span data-ttu-id="c0a57-339">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0a57-339">Properties</span></span> | <span data-ttu-id="c0a57-340">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-340">Type</span></span> | <span data-ttu-id="c0a57-341">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-341">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-342">name</span><span class="sxs-lookup"><span data-stu-id="c0a57-342">name</span></span> | `string` | <span data-ttu-id="c0a57-343">Nom de la propriété ou description du symbole.</span><span class="sxs-lookup"><span data-stu-id="c0a57-343">Property name or symbol description.</span></span> |  
| <span data-ttu-id="c0a57-344">value \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-344">value \(optional\)</span></span> | [<span data-ttu-id="c0a57-345">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="c0a57-345">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="c0a57-346">Valeur associée à la propriété.</span><span class="sxs-lookup"><span data-stu-id="c0a57-346">The value associated with the property.</span></span> |  
| <span data-ttu-id="c0a57-347">writable \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-347">writable \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="c0a57-348">si la valeur associée à la propriété peut être modifiée \(descripteurs de données uniquement\).</span><span class="sxs-lookup"><span data-stu-id="c0a57-348">if the value associated with the property may be changed \(data descriptors only\).</span></span> |  
| <span data-ttu-id="c0a57-349">get \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-349">get \(optional\)</span></span> | [<span data-ttu-id="c0a57-350">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="c0a57-350">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="c0a57-351">Fonction qui sert de getter pour la propriété, ou s’il n’existe pas de `undefined` getter \(descripteurs d’accesseurs uniquement\).</span><span class="sxs-lookup"><span data-stu-id="c0a57-351">A function which serves as a getter for the property, or `undefined` if there is no getter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="c0a57-352">set \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-352">set \(optional\)</span></span> | [<span data-ttu-id="c0a57-353">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="c0a57-353">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="c0a57-354">Fonction qui sert de setter pour la propriété, ou s’il n’y a pas de `undefined` setter \(descripteurs d’accesseurs uniquement\).</span><span class="sxs-lookup"><span data-stu-id="c0a57-354">A function which serves as a setter for the property, or `undefined` if there is no setter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="c0a57-355">configurable</span><span class="sxs-lookup"><span data-stu-id="c0a57-355">configurable</span></span> | `boolean` | `True` <span data-ttu-id="c0a57-356">si le type de ce descripteur de propriété peut être modifié et si la propriété peut être supprimée de l’objet correspondant.</span><span class="sxs-lookup"><span data-stu-id="c0a57-356">if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span> |  
| <span data-ttu-id="c0a57-357">éumerable</span><span class="sxs-lookup"><span data-stu-id="c0a57-357">enumerable</span></span> | `boolean` | `True` <span data-ttu-id="c0a57-358">si cette propriété s’affiche lors de l’éumération des propriétés sur l’objet correspondant.</span><span class="sxs-lookup"><span data-stu-id="c0a57-358">if this property shows up during enumeration of the properties on the corresponding object.</span></span> |  
| <span data-ttu-id="c0a57-359">wasThrown \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-359">wasThrown \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="c0a57-360">si le résultat a été lancé au cours de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="c0a57-360">if the result was thrown during the evaluation.</span></span> |  
| <span data-ttu-id="c0a57-361">isOwn \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-361">isOwn \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="c0a57-362">si la propriété appartient à l’objet.</span><span class="sxs-lookup"><span data-stu-id="c0a57-362">if the property is owned for the object.</span></span> |  
| <span data-ttu-id="c0a57-363">msReturnValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-363">msReturnValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="c0a57-364">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="c0a57-364">**Experimental**.</span></span>  <span data-ttu-id="c0a57-365">Microsoft :  `True` si la propriété est une valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="c0a57-365">Microsoft:  `True` if the property is a return value.</span></span> |  
| <span data-ttu-id="c0a57-366">symbol \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-366">symbol \(optional\)</span></span> | [<span data-ttu-id="c0a57-367">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="c0a57-367">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="c0a57-368">Objet symbole de propriété, si la propriété est du `symbol` type.</span><span class="sxs-lookup"><span data-stu-id="c0a57-368">Property symbol object, if the property is of the `symbol` type.</span></span> |  

---  

### <a name="callargument-object"></a><span data-ttu-id="c0a57-369">Objet CallArgument</span><span class="sxs-lookup"><span data-stu-id="c0a57-369">CallArgument object</span></span>  

<a name="callargument"></a>  

<span data-ttu-id="c0a57-370">Représente l’argument d’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="c0a57-370">Represents function call argument.</span></span>  <span data-ttu-id="c0a57-371">Soit l’ID d’objet distant, la primitive, la valeur de primitive non personnalisable, soit aucune des `objectId` `value` valeurs \(pour undefined\) ne doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c0a57-371">Either remote object ID `objectId`, primitive `value`, unserializable primitive value, or neither of \(for undefined\) them should be specified.</span></span>  

| <span data-ttu-id="c0a57-372">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0a57-372">Properties</span></span> | <span data-ttu-id="c0a57-373">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-373">Type</span></span> | <span data-ttu-id="c0a57-374">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-374">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-375">value \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-375">value \(optional\)</span></span> | `any` | <span data-ttu-id="c0a57-376">Valeur de primitive ou objet javascript sérialisable.</span><span class="sxs-lookup"><span data-stu-id="c0a57-376">Primitive value or serializable javascript object.</span></span> |  
| <span data-ttu-id="c0a57-377">unserializableValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-377">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="c0a57-378">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="c0a57-378">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="c0a57-379">Valeur de primitive qui ne peut pas être stringified JSON.</span><span class="sxs-lookup"><span data-stu-id="c0a57-379">Primitive value which can not be JSON-stringified.</span></span> |  
| <span data-ttu-id="c0a57-380">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-380">objectId \(optional\)</span></span> | <span data-ttu-id="c0a57-381">[RemoteObjectId](#remoteobjectid)]</span><span class="sxs-lookup"><span data-stu-id="c0a57-381">[RemoteObjectId](#remoteobjectid)]</span></span> | <span data-ttu-id="c0a57-382">Handle d’objet distant.</span><span class="sxs-lookup"><span data-stu-id="c0a57-382">Remote object handle.</span></span> |  

---  

### <a name="executioncontextid-integer"></a><span data-ttu-id="c0a57-383">ExecutionContextId, integer</span><span class="sxs-lookup"><span data-stu-id="c0a57-383">ExecutionContextId integer</span></span>  

<a name="executioncontextid"></a>  

<span data-ttu-id="c0a57-384">ID d’un contexte d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c0a57-384">ID of an execution context.</span></span>  

&nbsp;  

---  

### <a name="executioncontextdescription-object"></a><span data-ttu-id="c0a57-385">Objet ExecutionContextDescription</span><span class="sxs-lookup"><span data-stu-id="c0a57-385">ExecutionContextDescription object</span></span>  

<a name="executioncontextdescription"></a>  

<span data-ttu-id="c0a57-386">Description d’un monde isolé.</span><span class="sxs-lookup"><span data-stu-id="c0a57-386">Description of an isolated world.</span></span>  

| <span data-ttu-id="c0a57-387">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0a57-387">Properties</span></span> | <span data-ttu-id="c0a57-388">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-388">Type</span></span> | <span data-ttu-id="c0a57-389">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-389">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-390">id</span><span class="sxs-lookup"><span data-stu-id="c0a57-390">id</span></span> | [<span data-ttu-id="c0a57-391">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="c0a57-391">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="c0a57-392">ID unique du contexte d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c0a57-392">Unique ID of the execution context.</span></span>  <span data-ttu-id="c0a57-393">Il peut être utilisé pour spécifier dans quel contexte d’exécution</span><span class="sxs-lookup"><span data-stu-id="c0a57-393">It can be used to specify in which execution context</span></span>
<span data-ttu-id="c0a57-394">l’évaluation de script doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="c0a57-394">script evaluation should be performed.</span></span> |  
| <span data-ttu-id="c0a57-395">origin</span><span class="sxs-lookup"><span data-stu-id="c0a57-395">origin</span></span> | `string` | <span data-ttu-id="c0a57-396">Origine du contexte d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c0a57-396">Execution context origin.</span></span> |  
| <span data-ttu-id="c0a57-397">name</span><span class="sxs-lookup"><span data-stu-id="c0a57-397">name</span></span> | `string` | <span data-ttu-id="c0a57-398">Nom lisible par l’homme décrivant un contexte donné.</span><span class="sxs-lookup"><span data-stu-id="c0a57-398">Human readable name describing given context.</span></span> |  

---  

### <a name="exceptiondetails-object"></a><span data-ttu-id="c0a57-399">Objet ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="c0a57-399">ExceptionDetails object</span></span>  

<a name="exceptiondetails"></a>  

<span data-ttu-id="c0a57-400">Informations détaillées sur l’exception (ou l’erreur) qui a été lancée lors de la compilation ou de l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="c0a57-400">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>  

| <span data-ttu-id="c0a57-401">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0a57-401">Properties</span></span> | <span data-ttu-id="c0a57-402">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-402">Type</span></span> | <span data-ttu-id="c0a57-403">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-403">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-404">exceptionId</span><span class="sxs-lookup"><span data-stu-id="c0a57-404">exceptionId</span></span> | `integer` | <span data-ttu-id="c0a57-405">ID d’exception.</span><span class="sxs-lookup"><span data-stu-id="c0a57-405">Exception ID.</span></span> |  
| <span data-ttu-id="c0a57-406">texte</span><span class="sxs-lookup"><span data-stu-id="c0a57-406">text</span></span> | `string` | <span data-ttu-id="c0a57-407">Texte d’exception, qui doit être utilisé avec l’objet exception lorsqu’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="c0a57-407">Exception text, which should be used together with exception object when available.</span></span> |  
| <span data-ttu-id="c0a57-408">lineNumber</span><span class="sxs-lookup"><span data-stu-id="c0a57-408">lineNumber</span></span> | `integer` | <span data-ttu-id="c0a57-409">Numéro de ligne de l’emplacement de l’exception \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="c0a57-409">Line number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="c0a57-410">columnNumber</span><span class="sxs-lookup"><span data-stu-id="c0a57-410">columnNumber</span></span> | `integer` | <span data-ttu-id="c0a57-411">Numéro de colonne de l’emplacement de l’exception \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="c0a57-411">Column number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="c0a57-412">scriptId \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-412">scriptId \(optional\)</span></span> | [<span data-ttu-id="c0a57-413">ScriptId</span><span class="sxs-lookup"><span data-stu-id="c0a57-413">ScriptId</span></span>](#scriptid) | <span data-ttu-id="c0a57-414">ID de script de l’emplacement d’exception.</span><span class="sxs-lookup"><span data-stu-id="c0a57-414">Script ID of the exception location.</span></span> |  
| <span data-ttu-id="c0a57-415">url \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-415">url \(optional\)</span></span> | `string` | <span data-ttu-id="c0a57-416">URL de l’emplacement de l’exception, à utiliser lorsque le script n’a pas été signalé.</span><span class="sxs-lookup"><span data-stu-id="c0a57-416">URL of the exception location, to be used when the script was not reported.</span></span> |  
| <span data-ttu-id="c0a57-417">stackTrace \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-417">stackTrace \(optional\)</span></span> | [<span data-ttu-id="c0a57-418">StackTrace</span><span class="sxs-lookup"><span data-stu-id="c0a57-418">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="c0a57-419">Trace de pile JavaScript si disponible.</span><span class="sxs-lookup"><span data-stu-id="c0a57-419">JavaScript stack trace if available.</span></span> |  
| <span data-ttu-id="c0a57-420">exception \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-420">exception \(optional\)</span></span> | [<span data-ttu-id="c0a57-421">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="c0a57-421">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="c0a57-422">Objet Exception, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="c0a57-422">Exception object if available.</span></span> |  
| <span data-ttu-id="c0a57-423">executionContextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-423">executionContextId \(optional\)</span></span> | [<span data-ttu-id="c0a57-424">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="c0a57-424">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="c0a57-425">Identificateur du contexte dans lequel l’exception s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c0a57-425">Identifier of the context where exception happened.</span></span> |  

---  

### <a name="timestamp-integer"></a><span data-ttu-id="c0a57-426">Timestamp integer</span><span class="sxs-lookup"><span data-stu-id="c0a57-426">Timestamp integer</span></span>  

<a name="timestamp"></a>  

<span data-ttu-id="c0a57-427">Nombre de millisecondes depuis l’époque.</span><span class="sxs-lookup"><span data-stu-id="c0a57-427">Number of milliseconds since epoch.</span></span>  

&nbsp;  

---  

### <a name="callframe-object"></a><span data-ttu-id="c0a57-428">Objet CallFrame</span><span class="sxs-lookup"><span data-stu-id="c0a57-428">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="c0a57-429">Entrée de pile pour les erreurs d’runtime et les assertions.</span><span class="sxs-lookup"><span data-stu-id="c0a57-429">Stack entry for runtime errors and assertions.</span></span>  

| <span data-ttu-id="c0a57-430">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0a57-430">Properties</span></span> | <span data-ttu-id="c0a57-431">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-431">Type</span></span> | <span data-ttu-id="c0a57-432">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-432">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-433">functionName</span><span class="sxs-lookup"><span data-stu-id="c0a57-433">functionName</span></span> | `string` | <span data-ttu-id="c0a57-434">Nom de la fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c0a57-434">JavaScript function name.</span></span> |  
| <span data-ttu-id="c0a57-435">scriptId</span><span class="sxs-lookup"><span data-stu-id="c0a57-435">scriptId</span></span> | [<span data-ttu-id="c0a57-436">ScriptId</span><span class="sxs-lookup"><span data-stu-id="c0a57-436">ScriptId</span></span>](#scriptid) | <span data-ttu-id="c0a57-437">ID de script JavaScript. ScriptId sera vide si le débogger n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="c0a57-437">JavaScript script id. ScriptId will be empty if debugger is not enabled.</span></span> |  
| <span data-ttu-id="c0a57-438">url</span><span class="sxs-lookup"><span data-stu-id="c0a57-438">url</span></span> | `string` | <span data-ttu-id="c0a57-439">Nom ou URL du script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c0a57-439">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="c0a57-440">lineNumber</span><span class="sxs-lookup"><span data-stu-id="c0a57-440">lineNumber</span></span> | `integer` | <span data-ttu-id="c0a57-441">Numéro de ligne de script JavaScript \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="c0a57-441">JavaScript script line number \(0-based\).</span></span> |  
| <span data-ttu-id="c0a57-442">columnNumber</span><span class="sxs-lookup"><span data-stu-id="c0a57-442">columnNumber</span></span> | <span data-ttu-id="c0a57-443">entier</span><span class="sxs-lookup"><span data-stu-id="c0a57-443">integer</span></span> | <span data-ttu-id="c0a57-444">Numéro de colonne de script JavaScript \(basé sur 0\).</span><span class="sxs-lookup"><span data-stu-id="c0a57-444">JavaScript script column number \(0-based\).</span></span> |  

---  

### <a name="stacktrace-object"></a><span data-ttu-id="c0a57-445">Objet StackTrace</span><span class="sxs-lookup"><span data-stu-id="c0a57-445">StackTrace object</span></span>  

<a name="stacktrace"></a>  

<span data-ttu-id="c0a57-446">Appelez des cadres pour les assertions ou les messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c0a57-446">Call frames for assertions or error messages.</span></span>  

| <span data-ttu-id="c0a57-447">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0a57-447">Properties</span></span> | <span data-ttu-id="c0a57-448">Type</span><span class="sxs-lookup"><span data-stu-id="c0a57-448">Type</span></span> | <span data-ttu-id="c0a57-449">Détails</span><span class="sxs-lookup"><span data-stu-id="c0a57-449">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="c0a57-450">description \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-450">description \(optional\)</span></span> | `string` | <span data-ttu-id="c0a57-451">Étiquette de chaîne de cette trace de pile.</span><span class="sxs-lookup"><span data-stu-id="c0a57-451">String label of this stack trace.</span></span>  <span data-ttu-id="c0a57-452">Pour les suivis async, il peut s’agit d’un nom de la fonction qui a initié l’appel async.</span><span class="sxs-lookup"><span data-stu-id="c0a57-452">For async traces this may be a name of the function that initiated the async call.</span></span> |  
| <span data-ttu-id="c0a57-453">callFrames</span><span class="sxs-lookup"><span data-stu-id="c0a57-453">callFrames</span></span> | [<span data-ttu-id="c0a57-454">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="c0a57-454">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="c0a57-455">Nom de la fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c0a57-455">JavaScript function name.</span></span> |  
| <span data-ttu-id="c0a57-456">parent \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="c0a57-456">parent \(optional\)</span></span> | [<span data-ttu-id="c0a57-457">StackTrace</span><span class="sxs-lookup"><span data-stu-id="c0a57-457">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="c0a57-458">Trace de pile JavaScript asynchrone précédant cette pile, si disponible.</span><span class="sxs-lookup"><span data-stu-id="c0a57-458">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span> |  

---  
