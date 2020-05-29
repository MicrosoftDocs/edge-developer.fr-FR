---
description: Référence pour le domaine Runtime. Le domaine d’exécution expose le runtime JavaScript au moyen de l’évaluation à distance et des objets miroirs. Les résultats d’évaluation sont retournés sous la forme d’un objet miroir exposant le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour une référence d’objet supplémentaire. Les objets d’origine sont conservés en mémoire, sauf s’ils sont explicitement émis.
title: Domain Runtime-DevTools Protocol version 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 504f944f7a8389450685b40cdd010b54c3a7ba4e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565462"
---
# <span data-ttu-id="2d4b3-106">Runtime</span><span class="sxs-lookup"><span data-stu-id="2d4b3-106">Runtime</span></span>
<span data-ttu-id="2d4b3-107">Le domaine d’exécution expose le runtime JavaScript au moyen de l’évaluation à distance et des objets miroirs.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="2d4b3-108">Les résultats d’évaluation sont retournés sous la forme d’un objet miroir exposant le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour une référence d’objet supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="2d4b3-109">Les objets d’origine sont conservés en mémoire, sauf s’ils sont explicitement émis.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="2d4b3-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2d4b3-110">Methods</span></span>**](#methods) | <span data-ttu-id="2d4b3-111">[activer](#enable), [Désactiver](#disable), [évaluer](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [GetProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span><span class="sxs-lookup"><span data-stu-id="2d4b3-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span></span> |
| [**<span data-ttu-id="2d4b3-112">Événements</span><span class="sxs-lookup"><span data-stu-id="2d4b3-112">Events</span></span>**](#events) | <span data-ttu-id="2d4b3-113">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span><span class="sxs-lookup"><span data-stu-id="2d4b3-113">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span></span> |
| [**<span data-ttu-id="2d4b3-114">Types</span><span class="sxs-lookup"><span data-stu-id="2d4b3-114">Types</span></span>**](#types) | <span data-ttu-id="2d4b3-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="2d4b3-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |
## <span data-ttu-id="2d4b3-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2d4b3-116">Methods</span></span>

### <span data-ttu-id="2d4b3-117">activer</span><span class="sxs-lookup"><span data-stu-id="2d4b3-117">enable</span></span>
<span data-ttu-id="2d4b3-118">Active la création de rapports sur les <code>executionContextCreated</code> <code>executionContextDestroyed</code> <code>executionContextsCleared</code> événements et.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-118">Enables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span> <span data-ttu-id="2d4b3-119">Lorsque la création de rapports est activée <code>executionContextCreated</code> , l’événement est envoyé immédiatement pour chaque contexte d’exécution existant.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-119">When the reporting gets enabled the <code>executionContextCreated</code> event will be sent immediately for each existing execution context.</span></span>

</p>

---

### <span data-ttu-id="2d4b3-120">désactiver </span><span class="sxs-lookup"><span data-stu-id="2d4b3-120">disable</span></span>
<span data-ttu-id="2d4b3-121">Désactive la création de rapports sur <code>executionContextCreated</code> les <code>executionContextDestroyed</code> <code>executionContextsCleared</code> événements et.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-121">Disables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span>

</p>

---

### <span data-ttu-id="2d4b3-122">evaluat</span><span class="sxs-lookup"><span data-stu-id="2d4b3-122">evaluate</span></span>
<span data-ttu-id="2d4b3-123">Évalue l’expression sur l’objet global.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-123">Evaluates expression on global object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-124">Parameters</span><span class="sxs-lookup"><span data-stu-id="2d4b3-124">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-125">termes</span><span class="sxs-lookup"><span data-stu-id="2d4b3-125">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2d4b3-126">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-126">Expression to evaluate.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-127">includeCommandLineAPI</span><span class="sxs-lookup"><span data-stu-id="2d4b3-127">includeCommandLineAPI</span></span> <br/> <i><span data-ttu-id="2d4b3-128">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-128">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="2d4b3-129">Détermine si une API de ligne de commande doit être disponible au cours de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-129">Determines whether Command Line API should be available during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-130">objectGroup</span><span class="sxs-lookup"><span data-stu-id="2d4b3-130">objectGroup</span></span> <br/> <i><span data-ttu-id="2d4b3-131">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-131">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2d4b3-132">Nom du groupe de symboles qui peut être utilisé pour libérer plusieurs objets.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-132">Symbolic group name that can be used to release multiple objects.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-133">silent</span><span class="sxs-lookup"><span data-stu-id="2d4b3-133">silent</span></span> <br/> <i><span data-ttu-id="2d4b3-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-134">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="2d4b3-135">En mode silencieux, les exceptions levées lors de l’évaluation ne sont pas communiquées et n’interrompent pas l’exécution.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-135">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="2d4b3-136">Remplace l' <code>setPauseOnException</code> État.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-136">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-137">contextId</span><span class="sxs-lookup"><span data-stu-id="2d4b3-137">contextId</span></span> <br/> <i><span data-ttu-id="2d4b3-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-138">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="2d4b3-139">Spécifie le contexte d’exécution permettant d’effectuer une évaluation.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-139">Specifies in which execution context to perform evaluation.</span></span> <span data-ttu-id="2d4b3-140">Si le paramètre est omis, l’évaluation sera exécutée dans le contexte de la page inspectée.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-140">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-141">returnByValue</span><span class="sxs-lookup"><span data-stu-id="2d4b3-141">returnByValue</span></span> <br/> <i><span data-ttu-id="2d4b3-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-142">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="2d4b3-143">Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-143">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-144">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="2d4b3-144">awaitPromise</span></span> <br/> <i><span data-ttu-id="2d4b3-145">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-145">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="2d4b3-146">Si l’exécution doit avoir <code>await</code> pour résultat la valeur résultante et l’État retour une fois la promesse attendue résolue.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-146">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-147">Renvoie</span><span class="sxs-lookup"><span data-stu-id="2d4b3-147">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-148">provoqué</span><span class="sxs-lookup"><span data-stu-id="2d4b3-148">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="2d4b3-149">Résultat de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-149">Evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2d4b3-150">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="2d4b3-150">callFunctionOn</span></span>
<span data-ttu-id="2d4b3-151">Fonction appelle avec la déclaration fournie sur l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-151">Calls function with given declaration on the given object.</span></span> <span data-ttu-id="2d4b3-152">Le groupe d’objets du résultat est hérité de l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-152">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-153">Parameters</span><span class="sxs-lookup"><span data-stu-id="2d4b3-153">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-154">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="2d4b3-154">functionDeclaration</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2d4b3-155">Déclaration de la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-155">Declaration of the function to call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-156">Algorithm</span><span class="sxs-lookup"><span data-stu-id="2d4b3-156">objectId</span></span> <br/> <i><span data-ttu-id="2d4b3-157">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-157">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="2d4b3-158">Identificateur de l’objet sur lequel appeler la fonction.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-158">Identifier of the object to call function on.</span></span> <span data-ttu-id="2d4b3-159">ObjectId ou executionContextId doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-159">Either objectId or executionContextId should be specified.</span></span>  <span data-ttu-id="2d4b3-160">objectId doit être issu de la fonction Runtime. Evaluate ().</span><span class="sxs-lookup"><span data-stu-id="2d4b3-160">objectId must be from the Runtime.evaluate() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-161">arguments</span><span class="sxs-lookup"><span data-stu-id="2d4b3-161">arguments</span></span> <br/> <i><span data-ttu-id="2d4b3-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-162">optional</span></span></i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td><span data-ttu-id="2d4b3-163">Appeler des arguments.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-163">Call arguments.</span></span> <span data-ttu-id="2d4b3-164">Tous les arguments d’appel doivent appartenir au même univers JavaScript que l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-164">All call arguments must belong to the same JavaScript world as the target object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-165">silent</span><span class="sxs-lookup"><span data-stu-id="2d4b3-165">silent</span></span> <br/> <i><span data-ttu-id="2d4b3-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-166">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="2d4b3-167">En mode silencieux, les exceptions levées lors de l’évaluation ne sont pas communiquées et n’interrompent pas l’exécution.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-167">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="2d4b3-168">Remplace l' <code>setPauseOnException</code> État.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-168">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-169">returnByValue</span><span class="sxs-lookup"><span data-stu-id="2d4b3-169">returnByValue</span></span> <br/> <i><span data-ttu-id="2d4b3-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-170">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="2d4b3-171">Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-171">Whether the result is expected to be a JSON object which should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-172">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="2d4b3-172">awaitPromise</span></span> <br/> <i><span data-ttu-id="2d4b3-173">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-173">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="2d4b3-174">Si l’exécution doit avoir <code>await</code> pour résultat la valeur résultante et l’État retour une fois la promesse attendue résolue.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-174">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-175">executionContextId</span><span class="sxs-lookup"><span data-stu-id="2d4b3-175">executionContextId</span></span> <br/> <i><span data-ttu-id="2d4b3-176">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-176">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="2d4b3-177">Spécifie le contexte d’exécution sur lequel l’objet global sera utilisé pour appeler la fonction.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-177">Specifies execution context which global object will be used to call function on.</span></span> <span data-ttu-id="2d4b3-178">La valeur executionContextId ou objectId doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-178">Either executionContextId or objectId should be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-179">objectGroup</span><span class="sxs-lookup"><span data-stu-id="2d4b3-179">objectGroup</span></span> <br/> <i><span data-ttu-id="2d4b3-180">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-180">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2d4b3-181">Nom du groupe de symboles qui peut être utilisé pour libérer plusieurs objets.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-181">Symbolic group name that can be used to release multiple objects.</span></span> <span data-ttu-id="2d4b3-182">Si objectGroup n’est pas spécifié et que objectId est, objectGroup sera hérité de Object.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-182">If objectGroup is not specified and objectId is, objectGroup will be inherited from object.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-183">Renvoie</span><span class="sxs-lookup"><span data-stu-id="2d4b3-183">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-184">provoqué</span><span class="sxs-lookup"><span data-stu-id="2d4b3-184">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="2d4b3-185">Résultat de l’appel.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-185">Call result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2d4b3-186">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="2d4b3-186">awaitPromise</span></span>
<span data-ttu-id="2d4b3-187">Ajoutez le gestionnaire à la promesse avec ID d’objet promise.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-187">Add handler to promise with given promise object id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-188">Parameters</span><span class="sxs-lookup"><span data-stu-id="2d4b3-188">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-189">promiseObjectId</span><span class="sxs-lookup"><span data-stu-id="2d4b3-189">promiseObjectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="2d4b3-190">Identificateur de la promesse.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-190">Identifier of the promise.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-191">returnByValue</span><span class="sxs-lookup"><span data-stu-id="2d4b3-191">returnByValue</span></span> <br/> <i><span data-ttu-id="2d4b3-192">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-192">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="2d4b3-193">Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-193">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-194">Renvoie</span><span class="sxs-lookup"><span data-stu-id="2d4b3-194">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-195">provoqué</span><span class="sxs-lookup"><span data-stu-id="2d4b3-195">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="2d4b3-196">Résultat de la promesse.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-196">Promise result.</span></span>  <span data-ttu-id="2d4b3-197">Va contenir la valeur rejetée si la promesse a été refusée.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-197">Will contain rejected value if promise was rejected.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2d4b3-198">getProperties</span><span class="sxs-lookup"><span data-stu-id="2d4b3-198">getProperties</span></span>
<span data-ttu-id="2d4b3-199">Renvoie les propriétés d’un objet donné.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-199">Returns properties of a given object.</span></span> <span data-ttu-id="2d4b3-200">Le groupe d’objets du résultat est hérité de l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-200">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-201">Parameters</span><span class="sxs-lookup"><span data-stu-id="2d4b3-201">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-202">Algorithm</span><span class="sxs-lookup"><span data-stu-id="2d4b3-202">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="2d4b3-203">Identificateur de l’objet dont vous souhaitez renvoyer les propriétés.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-203">Identifier of the object to return properties for.</span></span> <span data-ttu-id="2d4b3-204">objectId doit être issu de la fonction Debugger. evaluateOnCallFrame ().</span><span class="sxs-lookup"><span data-stu-id="2d4b3-204">objectId must be from the Debugger.evaluateOnCallFrame() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-205">ownProperties</span><span class="sxs-lookup"><span data-stu-id="2d4b3-205">ownProperties</span></span> <br/> <i><span data-ttu-id="2d4b3-206">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-206">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="2d4b3-207">Si la valeur est true, retourne les propriétés qui ne sont liées qu’à l’élément proprement dit, et non à sa chaîne de prototype.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-207">If true, returns properties belonging only to the element itself, not to its prototype chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-208">accessorPropertiesOnly</span><span class="sxs-lookup"><span data-stu-id="2d4b3-208">accessorPropertiesOnly</span></span> <br/> <i><span data-ttu-id="2d4b3-209">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-209">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="2d4b3-210">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-210">Experimental.</span></span> </b></span><span data-ttu-id="2d4b3-211">Si true, retourne les propriétés d’accesseur (avec l’accesseur get/set) uniquement; les propriétés internes ne sont pas renvoyées.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-211">If true, returns accessor properties (with getter/setter) only; internal properties are not returned either.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-212">Renvoie</span><span class="sxs-lookup"><span data-stu-id="2d4b3-212">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-213">provoqué</span><span class="sxs-lookup"><span data-stu-id="2d4b3-213">result</span></span></td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td><span data-ttu-id="2d4b3-214">Propriétés d’objet.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-214">Object properties.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2d4b3-215">globalLexicalScopeNames</span><span class="sxs-lookup"><span data-stu-id="2d4b3-215">globalLexicalScopeNames</span></span>
<span data-ttu-id="2d4b3-216">Renvoie toutes les variables de type, de constante et de classe à partir de l’étendue globale de la console.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-216">Returns all let, const, and class variables from the console global scope.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-217">Renvoie</span><span class="sxs-lookup"><span data-stu-id="2d4b3-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-218">leurs</span><span class="sxs-lookup"><span data-stu-id="2d4b3-218">names</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2d4b3-219">releaseObject</span><span class="sxs-lookup"><span data-stu-id="2d4b3-219">releaseObject</span></span>
<span data-ttu-id="2d4b3-220">Libère l’objet distant avec l’ID donné.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-220">Releases remote object with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-221">Parameters</span><span class="sxs-lookup"><span data-stu-id="2d4b3-221">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-222">Algorithm</span><span class="sxs-lookup"><span data-stu-id="2d4b3-222">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="2d4b3-223">Identificateur de l’objet à libérer.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-223">Identifier of the object to release.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2d4b3-224">releaseObjectGroup</span><span class="sxs-lookup"><span data-stu-id="2d4b3-224">releaseObjectGroup</span></span>
<span data-ttu-id="2d4b3-225">Libère tous les objets distants appartenant à un groupe donné.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-225">Releases all remote objects that belong to a given group.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-226">Parameters</span><span class="sxs-lookup"><span data-stu-id="2d4b3-226">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-227">objectGroup</span><span class="sxs-lookup"><span data-stu-id="2d4b3-227">objectGroup</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2d4b3-228">Nom du groupe d’objets symboliques.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-228">Symbolic object group name.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2d4b3-229">discardConsoleEntries</span><span class="sxs-lookup"><span data-stu-id="2d4b3-229">discardConsoleEntries</span></span>
<span data-ttu-id="2d4b3-230">Supprime les exceptions collectées et les appels d’API de console.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-230">Discards collected exceptions and console API calls.</span></span>

</p>

---

## <span data-ttu-id="2d4b3-231">Événements</span><span class="sxs-lookup"><span data-stu-id="2d4b3-231">Events</span></span>

### <span data-ttu-id="2d4b3-232">executionContextCreated</span><span class="sxs-lookup"><span data-stu-id="2d4b3-232">executionContextCreated</span></span>
<span data-ttu-id="2d4b3-233">Émis lors de la création du contexte d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-233">Issued when new execution context is created.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-234">Parameters</span><span class="sxs-lookup"><span data-stu-id="2d4b3-234">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-235">contexte</span><span class="sxs-lookup"><span data-stu-id="2d4b3-235">context</span></span></td>
            <td><a href="#executioncontextdescription"><code class="flyout">ExecutionContextDescription</code></a></td>
            <td><span data-ttu-id="2d4b3-236">Contexte d’exécution nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-236">A newly created execution context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2d4b3-237">executionContextDestroyed</span><span class="sxs-lookup"><span data-stu-id="2d4b3-237">executionContextDestroyed</span></span>
<span data-ttu-id="2d4b3-238">Émis lorsque le contexte d’exécution est détruit.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-238">Issued when execution context is destroyed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-239">Parameters</span><span class="sxs-lookup"><span data-stu-id="2d4b3-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-240">executionContextId</span><span class="sxs-lookup"><span data-stu-id="2d4b3-240">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="2d4b3-241">ID du contexte détruit</span><span class="sxs-lookup"><span data-stu-id="2d4b3-241">Id of the destroyed context</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2d4b3-242">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="2d4b3-242">executionContextsCleared</span></span>
<span data-ttu-id="2d4b3-243">Émis lorsque tous les executionContexts étaient effacés dans le navigateur</span><span class="sxs-lookup"><span data-stu-id="2d4b3-243">Issued when all executionContexts were cleared in browser</span></span>

</p>

---

### <span data-ttu-id="2d4b3-244">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="2d4b3-244">exceptionThrown</span></span>
<span data-ttu-id="2d4b3-245">Émis quand une exception a été levée et non gérée.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-245">Issued when exception was thrown and unhandled.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-246">Parameters</span><span class="sxs-lookup"><span data-stu-id="2d4b3-246">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-247">telle</span><span class="sxs-lookup"><span data-stu-id="2d4b3-247">timestamp</span></span></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="2d4b3-248">Horodatage de l’exception.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-248">Timestamp of the exception.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-249">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="2d4b3-249">exceptionDetails</span></span></td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2d4b3-250">consoleAPICalled</span><span class="sxs-lookup"><span data-stu-id="2d4b3-250">consoleAPICalled</span></span>


<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-251">Parameters</span><span class="sxs-lookup"><span data-stu-id="2d4b3-251">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-252">type</span><span class="sxs-lookup"><span data-stu-id="2d4b3-252">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="2d4b3-253">Valeurs autorisées: Journal, informations, avertissement, erreur, déboguer, assertion, table, trace, dir, DirXML, Clear, Select, Count, countReset, timeEnd, timeStamp, startGroup, startGroupCollapsed, endGroup</span><span class="sxs-lookup"><span data-stu-id="2d4b3-253">Allowed values: log, info, warning, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, timeStamp, startGroup, startGroupCollapsed, endGroup</span></span></i></td>
            <td><span data-ttu-id="2d4b3-254">Type de l’appel.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-254">Type of the call.</span></span> <span data-ttu-id="2d4b3-255">Il s’agit de journaux, d’informations, d’avertissement, d’erreur, de débogage, d’assertion, de table, de suivi, de Rép, de DirXML, d’effacement, de countReset, d’timeEnd, d’exception, d’horodatage, de groupe, groupCollapsed, groupEnd.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-255">This includes log, info, warn, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, exception, timeStamp, group, groupCollapsed, groupEnd.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-256">args</span><span class="sxs-lookup"><span data-stu-id="2d4b3-256">args</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject[]</code></a></td>
            <td><span data-ttu-id="2d4b3-257">Appeler des arguments.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-257">Call arguments.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-258">executionContextId</span><span class="sxs-lookup"><span data-stu-id="2d4b3-258">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="2d4b3-259">Identificateur du contexte dans lequel l’appel de console a été effectué.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-259">Identifier of the context where console call was made</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-260">telle</span><span class="sxs-lookup"><span data-stu-id="2d4b3-260">timestamp</span></span> <br/> <i><span data-ttu-id="2d4b3-261">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-261">optional</span></span></i></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="2d4b3-262">Horodatage de l’appel.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-262">Call timestamp.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-263">Trace</span><span class="sxs-lookup"><span data-stu-id="2d4b3-263">stackTrace</span></span> <br/> <i><span data-ttu-id="2d4b3-264">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-264">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="2d4b3-265">Trace de pile capturée, le cas échéant</span><span class="sxs-lookup"><span data-stu-id="2d4b3-265">Stack trace captured if available</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="2d4b3-266">Types</span><span class="sxs-lookup"><span data-stu-id="2d4b3-266">Types</span></span>

### <a name="scriptid"></a> <span data-ttu-id="2d4b3-267">ScriptId</span><span class="sxs-lookup"><span data-stu-id="2d4b3-267">ScriptId</span></span> `string`

<span data-ttu-id="2d4b3-268">Identificateur de script unique.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-268">Unique script identifier.</span></span>

</p>

---

### <a name="remoteobjectid"></a> <span data-ttu-id="2d4b3-269">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="2d4b3-269">RemoteObjectId</span></span> `string`

<span data-ttu-id="2d4b3-270">Identifiant unique de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-270">Unique object identifier.</span></span>

</p>

---

### <a name="unserializablevalue"></a> <span data-ttu-id="2d4b3-271">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="2d4b3-271">UnserializableValue</span></span> `string`

<span data-ttu-id="2d4b3-272">Valeur primitive qui ne peut pas être JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-272">Primitive value which cannot be JSON-stringified.</span></span>

##### <span data-ttu-id="2d4b3-273">Valeurs autorisées</span><span class="sxs-lookup"><span data-stu-id="2d4b3-273">Allowed Values</span></span>
<span data-ttu-id="2d4b3-274">Infinity, NaN,-Infinity,-0</span><span class="sxs-lookup"><span data-stu-id="2d4b3-274">Infinity, NaN, -Infinity, -0</span></span>
</p>

---

### <a name="remoteobject"></a> <span data-ttu-id="2d4b3-275">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="2d4b3-275">RemoteObject</span></span> `object`

<span data-ttu-id="2d4b3-276">Objet Mirror référençant l’objet JavaScript d’origine.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-276">Mirror object referencing original JavaScript object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-277">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2d4b3-277">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-278">type</span><span class="sxs-lookup"><span data-stu-id="2d4b3-278">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="2d4b3-279">Valeurs autorisées: objet, fonction, non défini, chaîne, nombre, booléen, symbole</span><span class="sxs-lookup"><span data-stu-id="2d4b3-279">Allowed values: object, function, undefined, string, number, boolean, symbol</span></span></i></td>
            <td><span data-ttu-id="2d4b3-280">Type d’objet.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-280">Object type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-281">sous-type</span><span class="sxs-lookup"><span data-stu-id="2d4b3-281">subtype</span></span> <br/> <i><span data-ttu-id="2d4b3-282">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-282">optional</span></span></i></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="2d4b3-283">Valeurs autorisées: null, erreur, promesse, nœud</span><span class="sxs-lookup"><span data-stu-id="2d4b3-283">Allowed values: null, error, promise, node</span></span></i></td>
            <td><span data-ttu-id="2d4b3-284">Indicateur de sous-type d’objet.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-284">Object subtype hint.</span></span> <span data-ttu-id="2d4b3-285">Spécifié pour les <code>object</code> valeurs de type uniquement.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-285">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-286">NomClasse</span><span class="sxs-lookup"><span data-stu-id="2d4b3-286">className</span></span> <br/> <i><span data-ttu-id="2d4b3-287">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-287">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2d4b3-288">Nom de classe d’objet (constructeur).</span><span class="sxs-lookup"><span data-stu-id="2d4b3-288">Object class (constructor) name.</span></span> <span data-ttu-id="2d4b3-289">Spécifié pour les <code>object</code> valeurs de type uniquement.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-289">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-290">value</span><span class="sxs-lookup"><span data-stu-id="2d4b3-290">value</span></span> <br/> <i><span data-ttu-id="2d4b3-291">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-291">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="2d4b3-292">Valeur de l’objet distant en cas de valeurs primitives ou de valeurs JSON (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="2d4b3-292">Remote object value in case of primitive values or JSON values (if it was requested).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-293">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="2d4b3-293">unserializableValue</span></span> <br/> <i><span data-ttu-id="2d4b3-294">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-294">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="2d4b3-295">Valeur primitive qui ne peut pas être JSON-stringified</span><span class="sxs-lookup"><span data-stu-id="2d4b3-295">Primitive value which can not be JSON-stringified does not have</span></span> <code>value</code><span data-ttu-id="2d4b3-296">mais obtient cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-296">, but gets this property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-297">description</span><span class="sxs-lookup"><span data-stu-id="2d4b3-297">description</span></span> <br/> <i><span data-ttu-id="2d4b3-298">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-298">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2d4b3-299">Représentation de chaîne de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-299">String representation of the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-300">Algorithm</span><span class="sxs-lookup"><span data-stu-id="2d4b3-300">objectId</span></span> <br/> <i><span data-ttu-id="2d4b3-301">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-301">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="2d4b3-302">Identificateur d’objet unique (pour les valeurs non Primitives).</span><span class="sxs-lookup"><span data-stu-id="2d4b3-302">Unique object identifier (for non-primitive values).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-303">msDebuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="2d4b3-303">msDebuggerPropertyId</span></span> <br/> <i><span data-ttu-id="2d4b3-304">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-304">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="2d4b3-305">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-305">Experimental.</span></span> </b></span><span data-ttu-id="2d4b3-306">Microsoft: ID de propriété de débogueur associé pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-306">Microsoft: The associated debugger property id for this object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="propertydescriptor"></a> <span data-ttu-id="2d4b3-307">PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="2d4b3-307">PropertyDescriptor</span></span> `object`

<span data-ttu-id="2d4b3-308">Descripteur de propriété objet.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-308">Object property descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-309">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2d4b3-309">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-310">name</span><span class="sxs-lookup"><span data-stu-id="2d4b3-310">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2d4b3-311">Nom de la propriété ou description du symbole.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-311">Property name or symbol description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-312">value</span><span class="sxs-lookup"><span data-stu-id="2d4b3-312">value</span></span> <br/> <i><span data-ttu-id="2d4b3-313">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-313">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="2d4b3-314">Valeur associée à la propriété.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-314">The value associated with the property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-315">accès</span><span class="sxs-lookup"><span data-stu-id="2d4b3-315">writable</span></span> <br/> <i><span data-ttu-id="2d4b3-316">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-316">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="2d4b3-317">True si la valeur associée à la propriété est susceptible d’être modifiée (descripteurs de données uniquement).</span><span class="sxs-lookup"><span data-stu-id="2d4b3-317">True if the value associated with the property may be changed (data descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-318">obtenir</span><span class="sxs-lookup"><span data-stu-id="2d4b3-318">get</span></span> <br/> <i><span data-ttu-id="2d4b3-319">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-319">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="2d4b3-320">Fonction qui sert de Getter pour la propriété, ou <code>undefined</code> s’il n’y a pas d’accesseur get (descripteurs d’accesseur uniquement).</span><span class="sxs-lookup"><span data-stu-id="2d4b3-320">A function which serves as a getter for the property, or <code>undefined</code> if there is no getter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-321">set</span><span class="sxs-lookup"><span data-stu-id="2d4b3-321">set</span></span> <br/> <i><span data-ttu-id="2d4b3-322">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-322">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="2d4b3-323">Fonction utilisée comme une méthode setter de la propriété, ou <code>undefined</code> s’il n’y a pas de méthodes setter (descripteurs d’accesseur uniquement).</span><span class="sxs-lookup"><span data-stu-id="2d4b3-323">A function which serves as a setter for the property, or <code>undefined</code> if there is no setter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-324">configurables</span><span class="sxs-lookup"><span data-stu-id="2d4b3-324">configurable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="2d4b3-325">True si le type de ce descripteur de propriété est modifiable et si la propriété est susceptible d’être supprimée de l’objet correspondant.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-325">True if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-326">tournant</span><span class="sxs-lookup"><span data-stu-id="2d4b3-326">enumerable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="2d4b3-327">True si cette propriété s’affiche lors de l’énumération des propriétés de l’objet correspondant.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-327">True if this property shows up during enumeration of the properties on the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-328">wasThrown</span><span class="sxs-lookup"><span data-stu-id="2d4b3-328">wasThrown</span></span> <br/> <i><span data-ttu-id="2d4b3-329">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-329">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="2d4b3-330">True si le résultat a été levé lors de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-330">True if the result was thrown during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-331">isOwn</span><span class="sxs-lookup"><span data-stu-id="2d4b3-331">isOwn</span></span> <br/> <i><span data-ttu-id="2d4b3-332">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-332">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="2d4b3-333">True si la propriété est possédée pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-333">True if the property is owned for the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-334">msReturnValue</span><span class="sxs-lookup"><span data-stu-id="2d4b3-334">msReturnValue</span></span> <br/> <i><span data-ttu-id="2d4b3-335">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-335">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="2d4b3-336">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-336">Experimental.</span></span> </b></span><span data-ttu-id="2d4b3-337">Microsoft: true si la propriété est une valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-337">Microsoft: True if the property is a return value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-338">symbol</span><span class="sxs-lookup"><span data-stu-id="2d4b3-338">symbol</span></span> <br/> <i><span data-ttu-id="2d4b3-339">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-339">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="2d4b3-340">Objet symbol de propriété, si la propriété est de `symbol` type.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-340">Property symbol object, if the property is of the `symbol` type.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callargument"></a> <span data-ttu-id="2d4b3-341">CallArgument</span><span class="sxs-lookup"><span data-stu-id="2d4b3-341">CallArgument</span></span> `object`

<span data-ttu-id="2d4b3-342">Représente l’argument appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-342">Represents function call argument.</span></span> <span data-ttu-id="2d4b3-343">ID d’objet distant <code>objectId</code> , primitive <code>value</code> , valeur primitive unserializable ou aucun de (pour undefined).</span><span class="sxs-lookup"><span data-stu-id="2d4b3-343">Either remote object id <code>objectId</code>, primitive <code>value</code>, unserializable primitive value or neither of (for undefined) them should be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-344">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2d4b3-344">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-345">value</span><span class="sxs-lookup"><span data-stu-id="2d4b3-345">value</span></span> <br/> <i><span data-ttu-id="2d4b3-346">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-346">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="2d4b3-347">Valeur primitive ou objet JavaScript sérialisable.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-347">Primitive value or serializable javascript object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-348">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="2d4b3-348">unserializableValue</span></span> <br/> <i><span data-ttu-id="2d4b3-349">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-349">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="2d4b3-350">Valeur primitive qui ne peut pas être JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-350">Primitive value which can not be JSON-stringified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-351">Algorithm</span><span class="sxs-lookup"><span data-stu-id="2d4b3-351">objectId</span></span> <br/> <i><span data-ttu-id="2d4b3-352">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-352">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="2d4b3-353">Handle d’objet distant.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-353">Remote object handle.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="executioncontextid"></a> <span data-ttu-id="2d4b3-354">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="2d4b3-354">ExecutionContextId</span></span> `integer`

<span data-ttu-id="2d4b3-355">ID du contexte d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-355">Id of an execution context.</span></span>

</p>

---

### <a name="executioncontextdescription"></a> <span data-ttu-id="2d4b3-356">ExecutionContextDescription</span><span class="sxs-lookup"><span data-stu-id="2d4b3-356">ExecutionContextDescription</span></span> `object`

<span data-ttu-id="2d4b3-357">Description d’un monde isolé.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-357">Description of an isolated world.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-358">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2d4b3-358">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-359">id</span><span class="sxs-lookup"><span data-stu-id="2d4b3-359">id</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="2d4b3-360">ID unique du contexte d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-360">Unique id of the execution context.</span></span> <span data-ttu-id="2d4b3-361">Il peut être utilisé pour spécifier l’évaluation du script de contexte d’exécution qui doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-361">It can be used to specify in which execution context script evaluation should be performed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-362">prêts</span><span class="sxs-lookup"><span data-stu-id="2d4b3-362">origin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2d4b3-363">Origine du contexte d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-363">Execution context origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-364">name</span><span class="sxs-lookup"><span data-stu-id="2d4b3-364">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2d4b3-365">Nom lisible par le humain décrivant le contexte donné.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-365">Human readable name describing given context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="exceptiondetails"></a> <span data-ttu-id="2d4b3-366">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="2d4b3-366">ExceptionDetails</span></span> `object`

<span data-ttu-id="2d4b3-367">Informations détaillées sur l’exception (ou l’erreur) levée lors de la compilation ou de l’exécution d’un script.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-367">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-368">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2d4b3-368">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-369">exceptionId</span><span class="sxs-lookup"><span data-stu-id="2d4b3-369">exceptionId</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2d4b3-370">ID de l’exception.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-370">Exception id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-371">texte</span><span class="sxs-lookup"><span data-stu-id="2d4b3-371">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2d4b3-372">Texte de l’exception, qui doit être utilisé avec l’objet exception lorsqu’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-372">Exception text, which should be used together with exception object when available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-373">lineNumber</span><span class="sxs-lookup"><span data-stu-id="2d4b3-373">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2d4b3-374">Numéro de ligne de l’emplacement de l’exception (0).</span><span class="sxs-lookup"><span data-stu-id="2d4b3-374">Line number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-375">columnNumber</span><span class="sxs-lookup"><span data-stu-id="2d4b3-375">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2d4b3-376">Numéro de colonne de l’emplacement de l’exception (0).</span><span class="sxs-lookup"><span data-stu-id="2d4b3-376">Column number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-377">scriptId</span><span class="sxs-lookup"><span data-stu-id="2d4b3-377">scriptId</span></span> <br/> <i><span data-ttu-id="2d4b3-378">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-378">optional</span></span></i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="2d4b3-379">ID de script de l’emplacement de l’exception.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-379">Script ID of the exception location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-380">url</span><span class="sxs-lookup"><span data-stu-id="2d4b3-380">url</span></span> <br/> <i><span data-ttu-id="2d4b3-381">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-381">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2d4b3-382">URL de l’emplacement de l’exception à utiliser lorsque le script n’a pas été communiqué.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-382">URL of the exception location, to be used when the script was not reported.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-383">Trace</span><span class="sxs-lookup"><span data-stu-id="2d4b3-383">stackTrace</span></span> <br/> <i><span data-ttu-id="2d4b3-384">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-384">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="2d4b3-385">Trace de pile JavaScript, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-385">JavaScript stack trace if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-386">sauf</span><span class="sxs-lookup"><span data-stu-id="2d4b3-386">exception</span></span> <br/> <i><span data-ttu-id="2d4b3-387">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-387">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="2d4b3-388">Objet exception, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-388">Exception object if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-389">executionContextId</span><span class="sxs-lookup"><span data-stu-id="2d4b3-389">executionContextId</span></span> <br/> <i><span data-ttu-id="2d4b3-390">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-390">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="2d4b3-391">Identificateur du contexte où une exception s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-391">Identifier of the context where exception happened.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="timestamp"></a> <span data-ttu-id="2d4b3-392">Horodateur</span><span class="sxs-lookup"><span data-stu-id="2d4b3-392">Timestamp</span></span> `integer`

<span data-ttu-id="2d4b3-393">Nombre de millisecondes depuis l’époque.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-393">Number of milliseconds since epoch.</span></span>

</p>

---

### <a name="callframe"></a> <span data-ttu-id="2d4b3-394">CallFrame</span><span class="sxs-lookup"><span data-stu-id="2d4b3-394">CallFrame</span></span> `object`

<span data-ttu-id="2d4b3-395">Entrée de pile pour les erreurs d’exécution et les affirmations.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-395">Stack entry for runtime errors and assertions.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-396">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2d4b3-396">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-397">Admises</span><span class="sxs-lookup"><span data-stu-id="2d4b3-397">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2d4b3-398">Nom de la fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-398">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-399">scriptId</span><span class="sxs-lookup"><span data-stu-id="2d4b3-399">scriptId</span></span></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="2d4b3-400">ID de script JavaScript. ScriptId est vide si le débogueur n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-400">JavaScript script id. ScriptId will be empty if debugger is not enabled.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-401">url</span><span class="sxs-lookup"><span data-stu-id="2d4b3-401">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2d4b3-402">Nom ou URL du script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-402">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-403">lineNumber</span><span class="sxs-lookup"><span data-stu-id="2d4b3-403">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2d4b3-404">Numéro de ligne de script JavaScript (0).</span><span class="sxs-lookup"><span data-stu-id="2d4b3-404">JavaScript script line number (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-405">columnNumber</span><span class="sxs-lookup"><span data-stu-id="2d4b3-405">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2d4b3-406">Numéro de colonne de script JavaScript (0).</span><span class="sxs-lookup"><span data-stu-id="2d4b3-406">JavaScript script column number (0-based).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="stacktrace"></a> <span data-ttu-id="2d4b3-407">Trace</span><span class="sxs-lookup"><span data-stu-id="2d4b3-407">StackTrace</span></span> `object`

<span data-ttu-id="2d4b3-408">Trames d’appel pour les affirmations ou messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-408">Call frames for assertions or error messages.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2d4b3-409">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2d4b3-409">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2d4b3-410">description</span><span class="sxs-lookup"><span data-stu-id="2d4b3-410">description</span></span> <br/> <i><span data-ttu-id="2d4b3-411">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-411">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2d4b3-412">Étiquette de chaîne de cette trace de pile.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-412">String label of this stack trace.</span></span> <span data-ttu-id="2d4b3-413">Pour les traces Async, il s’agit du nom de la fonction qui a déclenché l’appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-413">For async traces this may be a name of the function that initiated the async call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-414">callFrames</span><span class="sxs-lookup"><span data-stu-id="2d4b3-414">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="2d4b3-415">Nom de la fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-415">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2d4b3-416">dernier</span><span class="sxs-lookup"><span data-stu-id="2d4b3-416">parent</span></span> <br/> <i><span data-ttu-id="2d4b3-417">facultatif</span><span class="sxs-lookup"><span data-stu-id="2d4b3-417">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="2d4b3-418">Trace de pile JavaScript asynchrone qui précède cette pile, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="2d4b3-418">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
