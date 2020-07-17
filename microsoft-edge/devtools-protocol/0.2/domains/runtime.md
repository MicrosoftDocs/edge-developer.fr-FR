---
description: Référence pour le domaine Runtime. Le domaine d’exécution expose le runtime JavaScript au moyen de l’évaluation à distance et des objets miroirs. Les résultats d’évaluation sont retournés sous la forme d’un objet miroir exposant le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour une référence d’objet supplémentaire. Les objets d’origine sont conservés en mémoire, sauf s’ils sont explicitement émis.
title: Domain Runtime-DevTools Protocol version 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 710b3b3e0383f1f6feb7947e0468730d2e0b0e66
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882861"
---
# <span data-ttu-id="bfab8-106">Domain Runtime-DevTools Protocol version 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="bfab8-106">Runtime Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="bfab8-107">Le domaine d’exécution expose le runtime JavaScript au moyen de l’évaluation à distance et des objets miroirs.</span><span class="sxs-lookup"><span data-stu-id="bfab8-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="bfab8-108">Les résultats d’évaluation sont retournés sous la forme d’un objet miroir exposant le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour une référence d’objet supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="bfab8-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="bfab8-109">Les objets d’origine sont conservés en mémoire, sauf s’ils sont explicitement émis.</span><span class="sxs-lookup"><span data-stu-id="bfab8-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="bfab8-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bfab8-110">Methods</span></span>**](#methods) | <span data-ttu-id="bfab8-111">[activer](#enable), [Désactiver](#disable), [évaluer](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [GetProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span><span class="sxs-lookup"><span data-stu-id="bfab8-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span></span> |
| [**<span data-ttu-id="bfab8-112">Événements</span><span class="sxs-lookup"><span data-stu-id="bfab8-112">Events</span></span>**](#events) | <span data-ttu-id="bfab8-113">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span><span class="sxs-lookup"><span data-stu-id="bfab8-113">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span></span> |
| [**<span data-ttu-id="bfab8-114">Types</span><span class="sxs-lookup"><span data-stu-id="bfab8-114">Types</span></span>**](#types) | <span data-ttu-id="bfab8-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="bfab8-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |
## <span data-ttu-id="bfab8-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bfab8-116">Methods</span></span>

### <span data-ttu-id="bfab8-117">activer</span><span class="sxs-lookup"><span data-stu-id="bfab8-117">enable</span></span>
<span data-ttu-id="bfab8-118">Active la création de rapports sur les <code>executionContextCreated</code> <code>executionContextDestroyed</code> <code>executionContextsCleared</code> événements et.</span><span class="sxs-lookup"><span data-stu-id="bfab8-118">Enables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span> <span data-ttu-id="bfab8-119">Lorsque la création de rapports est activée <code>executionContextCreated</code> , l’événement est envoyé immédiatement pour chaque contexte d’exécution existant.</span><span class="sxs-lookup"><span data-stu-id="bfab8-119">When the reporting gets enabled the <code>executionContextCreated</code> event will be sent immediately for each existing execution context.</span></span>

</p>

---

### <span data-ttu-id="bfab8-120">désactiver </span><span class="sxs-lookup"><span data-stu-id="bfab8-120">disable</span></span>
<span data-ttu-id="bfab8-121">Désactive la création de rapports sur <code>executionContextCreated</code> les <code>executionContextDestroyed</code> <code>executionContextsCleared</code> événements et.</span><span class="sxs-lookup"><span data-stu-id="bfab8-121">Disables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span>

</p>

---

### <span data-ttu-id="bfab8-122">evaluat</span><span class="sxs-lookup"><span data-stu-id="bfab8-122">evaluate</span></span>
<span data-ttu-id="bfab8-123">Évalue l’expression sur l’objet global.</span><span class="sxs-lookup"><span data-stu-id="bfab8-123">Evaluates expression on global object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-124">Parameters</span><span class="sxs-lookup"><span data-stu-id="bfab8-124">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-125">termes</span><span class="sxs-lookup"><span data-stu-id="bfab8-125">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bfab8-126">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="bfab8-126">Expression to evaluate.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-127">includeCommandLineAPI</span><span class="sxs-lookup"><span data-stu-id="bfab8-127">includeCommandLineAPI</span></span> <br/> <i><span data-ttu-id="bfab8-128">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-128">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="bfab8-129">Détermine si une API de ligne de commande doit être disponible au cours de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="bfab8-129">Determines whether Command Line API should be available during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-130">objectGroup</span><span class="sxs-lookup"><span data-stu-id="bfab8-130">objectGroup</span></span> <br/> <i><span data-ttu-id="bfab8-131">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-131">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bfab8-132">Nom du groupe de symboles qui peut être utilisé pour libérer plusieurs objets.</span><span class="sxs-lookup"><span data-stu-id="bfab8-132">Symbolic group name that can be used to release multiple objects.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-133">silent</span><span class="sxs-lookup"><span data-stu-id="bfab8-133">silent</span></span> <br/> <i><span data-ttu-id="bfab8-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-134">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="bfab8-135">En mode silencieux, les exceptions levées lors de l’évaluation ne sont pas communiquées et n’interrompent pas l’exécution.</span><span class="sxs-lookup"><span data-stu-id="bfab8-135">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="bfab8-136">Remplace l' <code>setPauseOnException</code> État.</span><span class="sxs-lookup"><span data-stu-id="bfab8-136">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-137">contextId</span><span class="sxs-lookup"><span data-stu-id="bfab8-137">contextId</span></span> <br/> <i><span data-ttu-id="bfab8-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-138">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="bfab8-139">Spécifie le contexte d’exécution permettant d’effectuer une évaluation.</span><span class="sxs-lookup"><span data-stu-id="bfab8-139">Specifies in which execution context to perform evaluation.</span></span> <span data-ttu-id="bfab8-140">Si le paramètre est omis, l’évaluation sera exécutée dans le contexte de la page inspectée.</span><span class="sxs-lookup"><span data-stu-id="bfab8-140">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-141">returnByValue</span><span class="sxs-lookup"><span data-stu-id="bfab8-141">returnByValue</span></span> <br/> <i><span data-ttu-id="bfab8-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-142">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="bfab8-143">Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</span><span class="sxs-lookup"><span data-stu-id="bfab8-143">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-144">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="bfab8-144">awaitPromise</span></span> <br/> <i><span data-ttu-id="bfab8-145">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-145">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="bfab8-146">Si l’exécution doit avoir <code>await</code> pour résultat la valeur résultante et l’État retour une fois la promesse attendue résolue.</span><span class="sxs-lookup"><span data-stu-id="bfab8-146">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-147">Renvoie</span><span class="sxs-lookup"><span data-stu-id="bfab8-147">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-148">provoqué</span><span class="sxs-lookup"><span data-stu-id="bfab8-148">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="bfab8-149">Résultat de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="bfab8-149">Evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="bfab8-150">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="bfab8-150">callFunctionOn</span></span>
<span data-ttu-id="bfab8-151">Fonction appelle avec la déclaration fournie sur l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="bfab8-151">Calls function with given declaration on the given object.</span></span> <span data-ttu-id="bfab8-152">Le groupe d’objets du résultat est hérité de l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="bfab8-152">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-153">Parameters</span><span class="sxs-lookup"><span data-stu-id="bfab8-153">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-154">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="bfab8-154">functionDeclaration</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bfab8-155">Déclaration de la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="bfab8-155">Declaration of the function to call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-156">Algorithm</span><span class="sxs-lookup"><span data-stu-id="bfab8-156">objectId</span></span> <br/> <i><span data-ttu-id="bfab8-157">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-157">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="bfab8-158">Identificateur de l’objet sur lequel appeler la fonction.</span><span class="sxs-lookup"><span data-stu-id="bfab8-158">Identifier of the object to call function on.</span></span> <span data-ttu-id="bfab8-159">ObjectId ou executionContextId doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="bfab8-159">Either objectId or executionContextId should be specified.</span></span>  <span data-ttu-id="bfab8-160">objectId doit être issu de la fonction Runtime. Evaluate ().</span><span class="sxs-lookup"><span data-stu-id="bfab8-160">objectId must be from the Runtime.evaluate() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-161">arguments</span><span class="sxs-lookup"><span data-stu-id="bfab8-161">arguments</span></span> <br/> <i><span data-ttu-id="bfab8-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-162">optional</span></span></i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td><span data-ttu-id="bfab8-163">Appeler des arguments.</span><span class="sxs-lookup"><span data-stu-id="bfab8-163">Call arguments.</span></span> <span data-ttu-id="bfab8-164">Tous les arguments d’appel doivent appartenir au même univers JavaScript que l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="bfab8-164">All call arguments must belong to the same JavaScript world as the target object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-165">silent</span><span class="sxs-lookup"><span data-stu-id="bfab8-165">silent</span></span> <br/> <i><span data-ttu-id="bfab8-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-166">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="bfab8-167">En mode silencieux, les exceptions levées lors de l’évaluation ne sont pas communiquées et n’interrompent pas l’exécution.</span><span class="sxs-lookup"><span data-stu-id="bfab8-167">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="bfab8-168">Remplace l' <code>setPauseOnException</code> État.</span><span class="sxs-lookup"><span data-stu-id="bfab8-168">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-169">returnByValue</span><span class="sxs-lookup"><span data-stu-id="bfab8-169">returnByValue</span></span> <br/> <i><span data-ttu-id="bfab8-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-170">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="bfab8-171">Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</span><span class="sxs-lookup"><span data-stu-id="bfab8-171">Whether the result is expected to be a JSON object which should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-172">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="bfab8-172">awaitPromise</span></span> <br/> <i><span data-ttu-id="bfab8-173">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-173">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="bfab8-174">Si l’exécution doit avoir <code>await</code> pour résultat la valeur résultante et l’État retour une fois la promesse attendue résolue.</span><span class="sxs-lookup"><span data-stu-id="bfab8-174">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-175">executionContextId</span><span class="sxs-lookup"><span data-stu-id="bfab8-175">executionContextId</span></span> <br/> <i><span data-ttu-id="bfab8-176">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-176">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="bfab8-177">Spécifie le contexte d’exécution sur lequel l’objet global sera utilisé pour appeler la fonction.</span><span class="sxs-lookup"><span data-stu-id="bfab8-177">Specifies execution context which global object will be used to call function on.</span></span> <span data-ttu-id="bfab8-178">La valeur executionContextId ou objectId doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bfab8-178">Either executionContextId or objectId should be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-179">objectGroup</span><span class="sxs-lookup"><span data-stu-id="bfab8-179">objectGroup</span></span> <br/> <i><span data-ttu-id="bfab8-180">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-180">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bfab8-181">Nom du groupe de symboles qui peut être utilisé pour libérer plusieurs objets.</span><span class="sxs-lookup"><span data-stu-id="bfab8-181">Symbolic group name that can be used to release multiple objects.</span></span> <span data-ttu-id="bfab8-182">Si objectGroup n’est pas spécifié et que objectId est, objectGroup sera hérité de Object.</span><span class="sxs-lookup"><span data-stu-id="bfab8-182">If objectGroup is not specified and objectId is, objectGroup will be inherited from object.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-183">Renvoie</span><span class="sxs-lookup"><span data-stu-id="bfab8-183">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-184">provoqué</span><span class="sxs-lookup"><span data-stu-id="bfab8-184">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="bfab8-185">Résultat de l’appel.</span><span class="sxs-lookup"><span data-stu-id="bfab8-185">Call result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="bfab8-186">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="bfab8-186">awaitPromise</span></span>
<span data-ttu-id="bfab8-187">Ajoutez le gestionnaire à la promesse avec ID d’objet promise.</span><span class="sxs-lookup"><span data-stu-id="bfab8-187">Add handler to promise with given promise object id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-188">Parameters</span><span class="sxs-lookup"><span data-stu-id="bfab8-188">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-189">promiseObjectId</span><span class="sxs-lookup"><span data-stu-id="bfab8-189">promiseObjectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="bfab8-190">Identificateur de la promesse.</span><span class="sxs-lookup"><span data-stu-id="bfab8-190">Identifier of the promise.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-191">returnByValue</span><span class="sxs-lookup"><span data-stu-id="bfab8-191">returnByValue</span></span> <br/> <i><span data-ttu-id="bfab8-192">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-192">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="bfab8-193">Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</span><span class="sxs-lookup"><span data-stu-id="bfab8-193">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-194">Renvoie</span><span class="sxs-lookup"><span data-stu-id="bfab8-194">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-195">provoqué</span><span class="sxs-lookup"><span data-stu-id="bfab8-195">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="bfab8-196">Résultat de la promesse.</span><span class="sxs-lookup"><span data-stu-id="bfab8-196">Promise result.</span></span>  <span data-ttu-id="bfab8-197">Va contenir la valeur rejetée si la promesse a été refusée.</span><span class="sxs-lookup"><span data-stu-id="bfab8-197">Will contain rejected value if promise was rejected.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="bfab8-198">getProperties</span><span class="sxs-lookup"><span data-stu-id="bfab8-198">getProperties</span></span>
<span data-ttu-id="bfab8-199">Renvoie les propriétés d’un objet donné.</span><span class="sxs-lookup"><span data-stu-id="bfab8-199">Returns properties of a given object.</span></span> <span data-ttu-id="bfab8-200">Le groupe d’objets du résultat est hérité de l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="bfab8-200">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-201">Parameters</span><span class="sxs-lookup"><span data-stu-id="bfab8-201">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-202">Algorithm</span><span class="sxs-lookup"><span data-stu-id="bfab8-202">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="bfab8-203">Identificateur de l’objet dont vous souhaitez renvoyer les propriétés.</span><span class="sxs-lookup"><span data-stu-id="bfab8-203">Identifier of the object to return properties for.</span></span> <span data-ttu-id="bfab8-204">objectId doit être issu de la fonction Debugger. evaluateOnCallFrame ().</span><span class="sxs-lookup"><span data-stu-id="bfab8-204">objectId must be from the Debugger.evaluateOnCallFrame() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-205">ownProperties</span><span class="sxs-lookup"><span data-stu-id="bfab8-205">ownProperties</span></span> <br/> <i><span data-ttu-id="bfab8-206">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-206">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="bfab8-207">Si la valeur est true, retourne les propriétés qui ne sont liées qu’à l’élément proprement dit, et non à sa chaîne de prototype.</span><span class="sxs-lookup"><span data-stu-id="bfab8-207">If true, returns properties belonging only to the element itself, not to its prototype chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-208">accessorPropertiesOnly</span><span class="sxs-lookup"><span data-stu-id="bfab8-208">accessorPropertiesOnly</span></span> <br/> <i><span data-ttu-id="bfab8-209">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-209">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="bfab8-210">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="bfab8-210">Experimental.</span></span> </b></span><span data-ttu-id="bfab8-211">Si true, retourne les propriétés d’accesseur (avec l’accesseur get/set) uniquement; les propriétés internes ne sont pas renvoyées.</span><span class="sxs-lookup"><span data-stu-id="bfab8-211">If true, returns accessor properties (with getter/setter) only; internal properties are not returned either.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-212">Renvoie</span><span class="sxs-lookup"><span data-stu-id="bfab8-212">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-213">provoqué</span><span class="sxs-lookup"><span data-stu-id="bfab8-213">result</span></span></td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td><span data-ttu-id="bfab8-214">Propriétés d’objet.</span><span class="sxs-lookup"><span data-stu-id="bfab8-214">Object properties.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="bfab8-215">globalLexicalScopeNames</span><span class="sxs-lookup"><span data-stu-id="bfab8-215">globalLexicalScopeNames</span></span>
<span data-ttu-id="bfab8-216">Renvoie toutes les variables de type, de constante et de classe à partir de l’étendue globale de la console.</span><span class="sxs-lookup"><span data-stu-id="bfab8-216">Returns all let, const, and class variables from the console global scope.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-217">Renvoie</span><span class="sxs-lookup"><span data-stu-id="bfab8-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-218">leurs</span><span class="sxs-lookup"><span data-stu-id="bfab8-218">names</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="bfab8-219">releaseObject</span><span class="sxs-lookup"><span data-stu-id="bfab8-219">releaseObject</span></span>
<span data-ttu-id="bfab8-220">Libère l’objet distant avec l’ID donné.</span><span class="sxs-lookup"><span data-stu-id="bfab8-220">Releases remote object with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-221">Parameters</span><span class="sxs-lookup"><span data-stu-id="bfab8-221">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-222">Algorithm</span><span class="sxs-lookup"><span data-stu-id="bfab8-222">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="bfab8-223">Identificateur de l’objet à libérer.</span><span class="sxs-lookup"><span data-stu-id="bfab8-223">Identifier of the object to release.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="bfab8-224">releaseObjectGroup</span><span class="sxs-lookup"><span data-stu-id="bfab8-224">releaseObjectGroup</span></span>
<span data-ttu-id="bfab8-225">Libère tous les objets distants appartenant à un groupe donné.</span><span class="sxs-lookup"><span data-stu-id="bfab8-225">Releases all remote objects that belong to a given group.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-226">Parameters</span><span class="sxs-lookup"><span data-stu-id="bfab8-226">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-227">objectGroup</span><span class="sxs-lookup"><span data-stu-id="bfab8-227">objectGroup</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bfab8-228">Nom du groupe d’objets symboliques.</span><span class="sxs-lookup"><span data-stu-id="bfab8-228">Symbolic object group name.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="bfab8-229">discardConsoleEntries</span><span class="sxs-lookup"><span data-stu-id="bfab8-229">discardConsoleEntries</span></span>
<span data-ttu-id="bfab8-230">Supprime les exceptions collectées et les appels d’API de console.</span><span class="sxs-lookup"><span data-stu-id="bfab8-230">Discards collected exceptions and console API calls.</span></span>

</p>

---

## <span data-ttu-id="bfab8-231">Événements</span><span class="sxs-lookup"><span data-stu-id="bfab8-231">Events</span></span>

### <span data-ttu-id="bfab8-232">executionContextCreated</span><span class="sxs-lookup"><span data-stu-id="bfab8-232">executionContextCreated</span></span>
<span data-ttu-id="bfab8-233">Émis lors de la création du contexte d’exécution.</span><span class="sxs-lookup"><span data-stu-id="bfab8-233">Issued when new execution context is created.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-234">Parameters</span><span class="sxs-lookup"><span data-stu-id="bfab8-234">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-235">contexte</span><span class="sxs-lookup"><span data-stu-id="bfab8-235">context</span></span></td>
            <td><a href="#executioncontextdescription"><code class="flyout">ExecutionContextDescription</code></a></td>
            <td><span data-ttu-id="bfab8-236">Contexte d’exécution nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="bfab8-236">A newly created execution context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="bfab8-237">executionContextDestroyed</span><span class="sxs-lookup"><span data-stu-id="bfab8-237">executionContextDestroyed</span></span>
<span data-ttu-id="bfab8-238">Émis lorsque le contexte d’exécution est détruit.</span><span class="sxs-lookup"><span data-stu-id="bfab8-238">Issued when execution context is destroyed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-239">Parameters</span><span class="sxs-lookup"><span data-stu-id="bfab8-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-240">executionContextId</span><span class="sxs-lookup"><span data-stu-id="bfab8-240">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="bfab8-241">ID du contexte détruit</span><span class="sxs-lookup"><span data-stu-id="bfab8-241">Id of the destroyed context</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="bfab8-242">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="bfab8-242">executionContextsCleared</span></span>
<span data-ttu-id="bfab8-243">Émis lorsque tous les executionContexts étaient effacés dans le navigateur</span><span class="sxs-lookup"><span data-stu-id="bfab8-243">Issued when all executionContexts were cleared in browser</span></span>

</p>

---

### <span data-ttu-id="bfab8-244">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="bfab8-244">exceptionThrown</span></span>
<span data-ttu-id="bfab8-245">Émis quand une exception a été levée et non gérée.</span><span class="sxs-lookup"><span data-stu-id="bfab8-245">Issued when exception was thrown and unhandled.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-246">Parameters</span><span class="sxs-lookup"><span data-stu-id="bfab8-246">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-247">telle</span><span class="sxs-lookup"><span data-stu-id="bfab8-247">timestamp</span></span></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="bfab8-248">Horodatage de l’exception.</span><span class="sxs-lookup"><span data-stu-id="bfab8-248">Timestamp of the exception.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-249">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="bfab8-249">exceptionDetails</span></span></td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="bfab8-250">consoleAPICalled</span><span class="sxs-lookup"><span data-stu-id="bfab8-250">consoleAPICalled</span></span>


<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-251">Parameters</span><span class="sxs-lookup"><span data-stu-id="bfab8-251">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-252">type</span><span class="sxs-lookup"><span data-stu-id="bfab8-252">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="bfab8-253">Valeurs autorisées: Journal, informations, avertissement, erreur, déboguer, assertion, table, trace, dir, DirXML, Clear, Select, Count, countReset, timeEnd, timeStamp, startGroup, startGroupCollapsed, endGroup</span><span class="sxs-lookup"><span data-stu-id="bfab8-253">Allowed values: log, info, warning, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, timeStamp, startGroup, startGroupCollapsed, endGroup</span></span></i></td>
            <td><span data-ttu-id="bfab8-254">Type de l’appel.</span><span class="sxs-lookup"><span data-stu-id="bfab8-254">Type of the call.</span></span> <span data-ttu-id="bfab8-255">Il s’agit de journaux, d’informations, d’avertissement, d’erreur, de débogage, d’assertion, de table, de suivi, de Rép, de DirXML, d’effacement, de countReset, d’timeEnd, d’exception, d’horodatage, de groupe, groupCollapsed, groupEnd.</span><span class="sxs-lookup"><span data-stu-id="bfab8-255">This includes log, info, warn, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, exception, timeStamp, group, groupCollapsed, groupEnd.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-256">args</span><span class="sxs-lookup"><span data-stu-id="bfab8-256">args</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject[]</code></a></td>
            <td><span data-ttu-id="bfab8-257">Appeler des arguments.</span><span class="sxs-lookup"><span data-stu-id="bfab8-257">Call arguments.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-258">executionContextId</span><span class="sxs-lookup"><span data-stu-id="bfab8-258">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="bfab8-259">Identificateur du contexte dans lequel l’appel de console a été effectué.</span><span class="sxs-lookup"><span data-stu-id="bfab8-259">Identifier of the context where console call was made</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-260">telle</span><span class="sxs-lookup"><span data-stu-id="bfab8-260">timestamp</span></span> <br/> <i><span data-ttu-id="bfab8-261">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-261">optional</span></span></i></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="bfab8-262">Horodatage de l’appel.</span><span class="sxs-lookup"><span data-stu-id="bfab8-262">Call timestamp.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-263">Trace</span><span class="sxs-lookup"><span data-stu-id="bfab8-263">stackTrace</span></span> <br/> <i><span data-ttu-id="bfab8-264">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-264">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="bfab8-265">Trace de pile capturée, le cas échéant</span><span class="sxs-lookup"><span data-stu-id="bfab8-265">Stack trace captured if available</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="bfab8-266">Types</span><span class="sxs-lookup"><span data-stu-id="bfab8-266">Types</span></span>

### <a name="scriptid"></a> <span data-ttu-id="bfab8-267">ScriptId</span><span class="sxs-lookup"><span data-stu-id="bfab8-267">ScriptId</span></span> `string`

<span data-ttu-id="bfab8-268">Identificateur de script unique.</span><span class="sxs-lookup"><span data-stu-id="bfab8-268">Unique script identifier.</span></span>

</p>

---

### <a name="remoteobjectid"></a> <span data-ttu-id="bfab8-269">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="bfab8-269">RemoteObjectId</span></span> `string`

<span data-ttu-id="bfab8-270">Identifiant unique de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bfab8-270">Unique object identifier.</span></span>

</p>

---

### <a name="unserializablevalue"></a> <span data-ttu-id="bfab8-271">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="bfab8-271">UnserializableValue</span></span> `string`

<span data-ttu-id="bfab8-272">Valeur primitive qui ne peut pas être JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="bfab8-272">Primitive value which cannot be JSON-stringified.</span></span>

##### <span data-ttu-id="bfab8-273">Valeurs autorisées</span><span class="sxs-lookup"><span data-stu-id="bfab8-273">Allowed Values</span></span>
<span data-ttu-id="bfab8-274">Infinity, NaN,-Infinity,-0</span><span class="sxs-lookup"><span data-stu-id="bfab8-274">Infinity, NaN, -Infinity, -0</span></span>
</p>

---

### <a name="remoteobject"></a> <span data-ttu-id="bfab8-275">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="bfab8-275">RemoteObject</span></span> `object`

<span data-ttu-id="bfab8-276">Objet Mirror référençant l’objet JavaScript d’origine.</span><span class="sxs-lookup"><span data-stu-id="bfab8-276">Mirror object referencing original JavaScript object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-277">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bfab8-277">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-278">type</span><span class="sxs-lookup"><span data-stu-id="bfab8-278">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="bfab8-279">Valeurs autorisées: objet, fonction, non défini, chaîne, nombre, booléen, symbole</span><span class="sxs-lookup"><span data-stu-id="bfab8-279">Allowed values: object, function, undefined, string, number, boolean, symbol</span></span></i></td>
            <td><span data-ttu-id="bfab8-280">Type d’objet.</span><span class="sxs-lookup"><span data-stu-id="bfab8-280">Object type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-281">sous-type</span><span class="sxs-lookup"><span data-stu-id="bfab8-281">subtype</span></span> <br/> <i><span data-ttu-id="bfab8-282">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-282">optional</span></span></i></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="bfab8-283">Valeurs autorisées: null, erreur, promesse, nœud</span><span class="sxs-lookup"><span data-stu-id="bfab8-283">Allowed values: null, error, promise, node</span></span></i></td>
            <td><span data-ttu-id="bfab8-284">Indicateur de sous-type d’objet.</span><span class="sxs-lookup"><span data-stu-id="bfab8-284">Object subtype hint.</span></span> <span data-ttu-id="bfab8-285">Spécifié pour les <code>object</code> valeurs de type uniquement.</span><span class="sxs-lookup"><span data-stu-id="bfab8-285">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-286">NomClasse</span><span class="sxs-lookup"><span data-stu-id="bfab8-286">className</span></span> <br/> <i><span data-ttu-id="bfab8-287">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-287">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bfab8-288">Nom de classe d’objet (constructeur).</span><span class="sxs-lookup"><span data-stu-id="bfab8-288">Object class (constructor) name.</span></span> <span data-ttu-id="bfab8-289">Spécifié pour les <code>object</code> valeurs de type uniquement.</span><span class="sxs-lookup"><span data-stu-id="bfab8-289">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-290">value</span><span class="sxs-lookup"><span data-stu-id="bfab8-290">value</span></span> <br/> <i><span data-ttu-id="bfab8-291">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-291">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="bfab8-292">Valeur de l’objet distant en cas de valeurs primitives ou de valeurs JSON (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="bfab8-292">Remote object value in case of primitive values or JSON values (if it was requested).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-293">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="bfab8-293">unserializableValue</span></span> <br/> <i><span data-ttu-id="bfab8-294">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-294">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="bfab8-295">Valeur primitive qui ne peut pas être JSON-stringified</span><span class="sxs-lookup"><span data-stu-id="bfab8-295">Primitive value which can not be JSON-stringified does not have</span></span> <code>value</code><span data-ttu-id="bfab8-296">mais obtient cette propriété.</span><span class="sxs-lookup"><span data-stu-id="bfab8-296">, but gets this property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-297">description</span><span class="sxs-lookup"><span data-stu-id="bfab8-297">description</span></span> <br/> <i><span data-ttu-id="bfab8-298">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-298">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bfab8-299">Représentation de chaîne de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bfab8-299">String representation of the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-300">Algorithm</span><span class="sxs-lookup"><span data-stu-id="bfab8-300">objectId</span></span> <br/> <i><span data-ttu-id="bfab8-301">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-301">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="bfab8-302">Identificateur d’objet unique (pour les valeurs non Primitives).</span><span class="sxs-lookup"><span data-stu-id="bfab8-302">Unique object identifier (for non-primitive values).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-303">msDebuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="bfab8-303">msDebuggerPropertyId</span></span> <br/> <i><span data-ttu-id="bfab8-304">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-304">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="bfab8-305">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="bfab8-305">Experimental.</span></span> </b></span><span data-ttu-id="bfab8-306">Microsoft: ID de propriété de débogueur associé pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="bfab8-306">Microsoft: The associated debugger property id for this object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="propertydescriptor"></a> <span data-ttu-id="bfab8-307">PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="bfab8-307">PropertyDescriptor</span></span> `object`

<span data-ttu-id="bfab8-308">Descripteur de propriété objet.</span><span class="sxs-lookup"><span data-stu-id="bfab8-308">Object property descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-309">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bfab8-309">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-310">name</span><span class="sxs-lookup"><span data-stu-id="bfab8-310">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bfab8-311">Nom de la propriété ou description du symbole.</span><span class="sxs-lookup"><span data-stu-id="bfab8-311">Property name or symbol description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-312">value</span><span class="sxs-lookup"><span data-stu-id="bfab8-312">value</span></span> <br/> <i><span data-ttu-id="bfab8-313">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-313">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="bfab8-314">Valeur associée à la propriété.</span><span class="sxs-lookup"><span data-stu-id="bfab8-314">The value associated with the property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-315">accès</span><span class="sxs-lookup"><span data-stu-id="bfab8-315">writable</span></span> <br/> <i><span data-ttu-id="bfab8-316">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-316">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="bfab8-317">True si la valeur associée à la propriété est susceptible d’être modifiée (descripteurs de données uniquement).</span><span class="sxs-lookup"><span data-stu-id="bfab8-317">True if the value associated with the property may be changed (data descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-318">obtenir</span><span class="sxs-lookup"><span data-stu-id="bfab8-318">get</span></span> <br/> <i><span data-ttu-id="bfab8-319">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-319">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="bfab8-320">Fonction qui sert de Getter pour la propriété, ou <code>undefined</code> s’il n’y a pas d’accesseur get (descripteurs d’accesseur uniquement).</span><span class="sxs-lookup"><span data-stu-id="bfab8-320">A function which serves as a getter for the property, or <code>undefined</code> if there is no getter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-321">set</span><span class="sxs-lookup"><span data-stu-id="bfab8-321">set</span></span> <br/> <i><span data-ttu-id="bfab8-322">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-322">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="bfab8-323">Fonction utilisée comme une méthode setter de la propriété, ou <code>undefined</code> s’il n’y a pas de méthodes setter (descripteurs d’accesseur uniquement).</span><span class="sxs-lookup"><span data-stu-id="bfab8-323">A function which serves as a setter for the property, or <code>undefined</code> if there is no setter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-324">configurables</span><span class="sxs-lookup"><span data-stu-id="bfab8-324">configurable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="bfab8-325">True si le type de ce descripteur de propriété est modifiable et si la propriété est susceptible d’être supprimée de l’objet correspondant.</span><span class="sxs-lookup"><span data-stu-id="bfab8-325">True if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-326">tournant</span><span class="sxs-lookup"><span data-stu-id="bfab8-326">enumerable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="bfab8-327">True si cette propriété s’affiche lors de l’énumération des propriétés de l’objet correspondant.</span><span class="sxs-lookup"><span data-stu-id="bfab8-327">True if this property shows up during enumeration of the properties on the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-328">wasThrown</span><span class="sxs-lookup"><span data-stu-id="bfab8-328">wasThrown</span></span> <br/> <i><span data-ttu-id="bfab8-329">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-329">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="bfab8-330">True si le résultat a été levé lors de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="bfab8-330">True if the result was thrown during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-331">isOwn</span><span class="sxs-lookup"><span data-stu-id="bfab8-331">isOwn</span></span> <br/> <i><span data-ttu-id="bfab8-332">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-332">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="bfab8-333">True si la propriété est possédée pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="bfab8-333">True if the property is owned for the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-334">msReturnValue</span><span class="sxs-lookup"><span data-stu-id="bfab8-334">msReturnValue</span></span> <br/> <i><span data-ttu-id="bfab8-335">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-335">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="bfab8-336">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="bfab8-336">Experimental.</span></span> </b></span><span data-ttu-id="bfab8-337">Microsoft: true si la propriété est une valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="bfab8-337">Microsoft: True if the property is a return value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-338">symbol</span><span class="sxs-lookup"><span data-stu-id="bfab8-338">symbol</span></span> <br/> <i><span data-ttu-id="bfab8-339">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-339">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="bfab8-340">Objet symbol de propriété, si la propriété est de `symbol` type.</span><span class="sxs-lookup"><span data-stu-id="bfab8-340">Property symbol object, if the property is of the `symbol` type.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callargument"></a> <span data-ttu-id="bfab8-341">CallArgument</span><span class="sxs-lookup"><span data-stu-id="bfab8-341">CallArgument</span></span> `object`

<span data-ttu-id="bfab8-342">Représente l’argument appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="bfab8-342">Represents function call argument.</span></span> <span data-ttu-id="bfab8-343">ID d’objet distant <code>objectId</code> , primitive <code>value</code> , valeur primitive unserializable ou aucun de (pour undefined).</span><span class="sxs-lookup"><span data-stu-id="bfab8-343">Either remote object id <code>objectId</code>, primitive <code>value</code>, unserializable primitive value or neither of (for undefined) them should be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-344">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bfab8-344">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-345">value</span><span class="sxs-lookup"><span data-stu-id="bfab8-345">value</span></span> <br/> <i><span data-ttu-id="bfab8-346">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-346">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="bfab8-347">Valeur primitive ou objet JavaScript sérialisable.</span><span class="sxs-lookup"><span data-stu-id="bfab8-347">Primitive value or serializable javascript object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-348">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="bfab8-348">unserializableValue</span></span> <br/> <i><span data-ttu-id="bfab8-349">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-349">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="bfab8-350">Valeur primitive qui ne peut pas être JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="bfab8-350">Primitive value which can not be JSON-stringified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-351">Algorithm</span><span class="sxs-lookup"><span data-stu-id="bfab8-351">objectId</span></span> <br/> <i><span data-ttu-id="bfab8-352">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-352">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="bfab8-353">Handle d’objet distant.</span><span class="sxs-lookup"><span data-stu-id="bfab8-353">Remote object handle.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="executioncontextid"></a> <span data-ttu-id="bfab8-354">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="bfab8-354">ExecutionContextId</span></span> `integer`

<span data-ttu-id="bfab8-355">ID du contexte d’exécution.</span><span class="sxs-lookup"><span data-stu-id="bfab8-355">Id of an execution context.</span></span>

</p>

---

### <a name="executioncontextdescription"></a> <span data-ttu-id="bfab8-356">ExecutionContextDescription</span><span class="sxs-lookup"><span data-stu-id="bfab8-356">ExecutionContextDescription</span></span> `object`

<span data-ttu-id="bfab8-357">Description d’un monde isolé.</span><span class="sxs-lookup"><span data-stu-id="bfab8-357">Description of an isolated world.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-358">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bfab8-358">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-359">id</span><span class="sxs-lookup"><span data-stu-id="bfab8-359">id</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="bfab8-360">ID unique du contexte d’exécution.</span><span class="sxs-lookup"><span data-stu-id="bfab8-360">Unique id of the execution context.</span></span> <span data-ttu-id="bfab8-361">Il peut être utilisé pour spécifier l’évaluation du script de contexte d’exécution qui doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="bfab8-361">It can be used to specify in which execution context script evaluation should be performed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-362">prêts</span><span class="sxs-lookup"><span data-stu-id="bfab8-362">origin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bfab8-363">Origine du contexte d’exécution.</span><span class="sxs-lookup"><span data-stu-id="bfab8-363">Execution context origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-364">name</span><span class="sxs-lookup"><span data-stu-id="bfab8-364">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bfab8-365">Nom lisible par le humain décrivant le contexte donné.</span><span class="sxs-lookup"><span data-stu-id="bfab8-365">Human readable name describing given context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="exceptiondetails"></a> <span data-ttu-id="bfab8-366">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="bfab8-366">ExceptionDetails</span></span> `object`

<span data-ttu-id="bfab8-367">Informations détaillées sur l’exception (ou l’erreur) levée lors de la compilation ou de l’exécution d’un script.</span><span class="sxs-lookup"><span data-stu-id="bfab8-367">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-368">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bfab8-368">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-369">exceptionId</span><span class="sxs-lookup"><span data-stu-id="bfab8-369">exceptionId</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="bfab8-370">ID de l’exception.</span><span class="sxs-lookup"><span data-stu-id="bfab8-370">Exception id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-371">texte</span><span class="sxs-lookup"><span data-stu-id="bfab8-371">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bfab8-372">Texte de l’exception, qui doit être utilisé avec l’objet exception lorsqu’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="bfab8-372">Exception text, which should be used together with exception object when available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-373">lineNumber</span><span class="sxs-lookup"><span data-stu-id="bfab8-373">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="bfab8-374">Numéro de ligne de l’emplacement de l’exception (0).</span><span class="sxs-lookup"><span data-stu-id="bfab8-374">Line number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-375">columnNumber</span><span class="sxs-lookup"><span data-stu-id="bfab8-375">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="bfab8-376">Numéro de colonne de l’emplacement de l’exception (0).</span><span class="sxs-lookup"><span data-stu-id="bfab8-376">Column number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-377">scriptId</span><span class="sxs-lookup"><span data-stu-id="bfab8-377">scriptId</span></span> <br/> <i><span data-ttu-id="bfab8-378">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-378">optional</span></span></i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="bfab8-379">ID de script de l’emplacement de l’exception.</span><span class="sxs-lookup"><span data-stu-id="bfab8-379">Script ID of the exception location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-380">url</span><span class="sxs-lookup"><span data-stu-id="bfab8-380">url</span></span> <br/> <i><span data-ttu-id="bfab8-381">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-381">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bfab8-382">URL de l’emplacement de l’exception à utiliser lorsque le script n’a pas été communiqué.</span><span class="sxs-lookup"><span data-stu-id="bfab8-382">URL of the exception location, to be used when the script was not reported.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-383">Trace</span><span class="sxs-lookup"><span data-stu-id="bfab8-383">stackTrace</span></span> <br/> <i><span data-ttu-id="bfab8-384">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-384">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="bfab8-385">Trace de pile JavaScript, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="bfab8-385">JavaScript stack trace if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-386">sauf</span><span class="sxs-lookup"><span data-stu-id="bfab8-386">exception</span></span> <br/> <i><span data-ttu-id="bfab8-387">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-387">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="bfab8-388">Objet exception, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="bfab8-388">Exception object if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-389">executionContextId</span><span class="sxs-lookup"><span data-stu-id="bfab8-389">executionContextId</span></span> <br/> <i><span data-ttu-id="bfab8-390">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-390">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="bfab8-391">Identificateur du contexte où une exception s’est produite.</span><span class="sxs-lookup"><span data-stu-id="bfab8-391">Identifier of the context where exception happened.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="timestamp"></a> <span data-ttu-id="bfab8-392">Horodateur</span><span class="sxs-lookup"><span data-stu-id="bfab8-392">Timestamp</span></span> `integer`

<span data-ttu-id="bfab8-393">Nombre de millisecondes depuis l’époque.</span><span class="sxs-lookup"><span data-stu-id="bfab8-393">Number of milliseconds since epoch.</span></span>

</p>

---

### <a name="callframe"></a> <span data-ttu-id="bfab8-394">CallFrame</span><span class="sxs-lookup"><span data-stu-id="bfab8-394">CallFrame</span></span> `object`

<span data-ttu-id="bfab8-395">Entrée de pile pour les erreurs d’exécution et les affirmations.</span><span class="sxs-lookup"><span data-stu-id="bfab8-395">Stack entry for runtime errors and assertions.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-396">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bfab8-396">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-397">Admises</span><span class="sxs-lookup"><span data-stu-id="bfab8-397">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bfab8-398">Nom de la fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bfab8-398">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-399">scriptId</span><span class="sxs-lookup"><span data-stu-id="bfab8-399">scriptId</span></span></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="bfab8-400">ID de script JavaScript. ScriptId est vide si le débogueur n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="bfab8-400">JavaScript script id. ScriptId will be empty if debugger is not enabled.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-401">url</span><span class="sxs-lookup"><span data-stu-id="bfab8-401">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bfab8-402">Nom ou URL du script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bfab8-402">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-403">lineNumber</span><span class="sxs-lookup"><span data-stu-id="bfab8-403">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="bfab8-404">Numéro de ligne de script JavaScript (0).</span><span class="sxs-lookup"><span data-stu-id="bfab8-404">JavaScript script line number (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-405">columnNumber</span><span class="sxs-lookup"><span data-stu-id="bfab8-405">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="bfab8-406">Numéro de colonne de script JavaScript (0).</span><span class="sxs-lookup"><span data-stu-id="bfab8-406">JavaScript script column number (0-based).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="stacktrace"></a> <span data-ttu-id="bfab8-407">Trace</span><span class="sxs-lookup"><span data-stu-id="bfab8-407">StackTrace</span></span> `object`

<span data-ttu-id="bfab8-408">Trames d’appel pour les affirmations ou messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="bfab8-408">Call frames for assertions or error messages.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bfab8-409">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bfab8-409">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bfab8-410">description</span><span class="sxs-lookup"><span data-stu-id="bfab8-410">description</span></span> <br/> <i><span data-ttu-id="bfab8-411">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-411">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bfab8-412">Étiquette de chaîne de cette trace de pile.</span><span class="sxs-lookup"><span data-stu-id="bfab8-412">String label of this stack trace.</span></span> <span data-ttu-id="bfab8-413">Pour les traces Async, il s’agit du nom de la fonction qui a déclenché l’appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="bfab8-413">For async traces this may be a name of the function that initiated the async call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-414">callFrames</span><span class="sxs-lookup"><span data-stu-id="bfab8-414">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="bfab8-415">Nom de la fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bfab8-415">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bfab8-416">dernier</span><span class="sxs-lookup"><span data-stu-id="bfab8-416">parent</span></span> <br/> <i><span data-ttu-id="bfab8-417">facultatif</span><span class="sxs-lookup"><span data-stu-id="bfab8-417">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="bfab8-418">Trace de pile JavaScript asynchrone qui précède cette pile, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="bfab8-418">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
