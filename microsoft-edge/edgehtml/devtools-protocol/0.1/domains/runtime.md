---
description: Référence de la version 0,1 (EdgeHTML) du protocole DevTools pour le domaine d’exécution. Le domaine d’exécution expose le runtime JavaScript au moyen de l’évaluation à distance et des objets miroirs. Les résultats d’évaluation sont retournés sous la forme d’un objet miroir exposant le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour une référence d’objet supplémentaire. Les objets d’origine sont conservés en mémoire, sauf s’ils sont explicitement émis.
title: Domain Runtime-DevTools Protocol version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 942a105199c8740fb7f7496b2a68e3eb0cc46fb4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232874"
---
# <span data-ttu-id="e0feb-106">Domain Runtime-DevTools Protocol version 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="e0feb-106">Runtime Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="e0feb-107">Le domaine d’exécution expose le runtime JavaScript au moyen de l’évaluation à distance et des objets miroirs.</span><span class="sxs-lookup"><span data-stu-id="e0feb-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="e0feb-108">Les résultats d’évaluation sont retournés sous la forme d’un objet miroir exposant le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour une référence d’objet supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="e0feb-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="e0feb-109">Les objets d’origine sont conservés en mémoire, sauf s’ils sont explicitement émis.</span><span class="sxs-lookup"><span data-stu-id="e0feb-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="e0feb-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e0feb-110">Methods</span></span>**](#methods) | <span data-ttu-id="e0feb-111">[activer](#enable), [Désactiver](#disable), [évaluer](#evaluate), [callFunctionOn](#callfunctionon), [GetProperties](#getproperties)</span><span class="sxs-lookup"><span data-stu-id="e0feb-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span></span> |
| [**<span data-ttu-id="e0feb-112">Événements</span><span class="sxs-lookup"><span data-stu-id="e0feb-112">Events</span></span>**](#events) | <span data-ttu-id="e0feb-113">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span><span class="sxs-lookup"><span data-stu-id="e0feb-113">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span></span> |
| [**<span data-ttu-id="e0feb-114">Types</span><span class="sxs-lookup"><span data-stu-id="e0feb-114">Types</span></span>**](#types) | <span data-ttu-id="e0feb-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="e0feb-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |
## <span data-ttu-id="e0feb-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e0feb-116">Methods</span></span>

### <span data-ttu-id="e0feb-117">activer</span><span class="sxs-lookup"><span data-stu-id="e0feb-117">enable</span></span>
<span data-ttu-id="e0feb-118">Autorise la création de rapports sur l' <code>executionContextsCleared</code> événement.</span><span class="sxs-lookup"><span data-stu-id="e0feb-118">Enables reporting of the <code>executionContextsCleared</code> event.</span></span>


---

### <span data-ttu-id="e0feb-119">désactiver </span><span class="sxs-lookup"><span data-stu-id="e0feb-119">disable</span></span>
<span data-ttu-id="e0feb-120">Désactive la création de rapports sur l' <code>executionContextsCleared</code> événement.</span><span class="sxs-lookup"><span data-stu-id="e0feb-120">Disables reporting of the <code>executionContextsCleared</code> event.</span></span>


---

### <span data-ttu-id="e0feb-121">evaluat</span><span class="sxs-lookup"><span data-stu-id="e0feb-121">evaluate</span></span>
<span data-ttu-id="e0feb-122">Évalue l’expression sur l’objet global.</span><span class="sxs-lookup"><span data-stu-id="e0feb-122">Evaluates expression on global object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e0feb-123">Parameters</span><span class="sxs-lookup"><span data-stu-id="e0feb-123">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e0feb-124">termes</span><span class="sxs-lookup"><span data-stu-id="e0feb-124">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e0feb-125">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="e0feb-125">Expression to evaluate.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-126">silent</span><span class="sxs-lookup"><span data-stu-id="e0feb-126">silent</span></span> <br/> <i><span data-ttu-id="e0feb-127">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-127">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e0feb-128">En mode silencieux, les exceptions levées lors de l’évaluation ne sont pas communiquées et n’interrompent pas l’exécution.</span><span class="sxs-lookup"><span data-stu-id="e0feb-128">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="e0feb-129">Remplace l' <code>setPauseOnException</code> État.</span><span class="sxs-lookup"><span data-stu-id="e0feb-129">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-130">contextId</span><span class="sxs-lookup"><span data-stu-id="e0feb-130">contextId</span></span> <br/> <i><span data-ttu-id="e0feb-131">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-131">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="e0feb-132">Spécifie le contexte d’exécution permettant d’effectuer une évaluation.</span><span class="sxs-lookup"><span data-stu-id="e0feb-132">Specifies in which execution context to perform evaluation.</span></span> <span data-ttu-id="e0feb-133">Si le paramètre est omis, l’évaluation sera exécutée dans le contexte de la page inspectée.</span><span class="sxs-lookup"><span data-stu-id="e0feb-133">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-134">returnByValue</span><span class="sxs-lookup"><span data-stu-id="e0feb-134">returnByValue</span></span> <br/> <i><span data-ttu-id="e0feb-135">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-135">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e0feb-136">Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</span><span class="sxs-lookup"><span data-stu-id="e0feb-136">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-137">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="e0feb-137">awaitPromise</span></span> <br/> <i><span data-ttu-id="e0feb-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-138">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e0feb-139">Si l’exécution doit avoir <code>await</code> pour résultat la valeur résultante et l’État retour une fois la promesse attendue résolue.</span><span class="sxs-lookup"><span data-stu-id="e0feb-139">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e0feb-140">Renvoie</span><span class="sxs-lookup"><span data-stu-id="e0feb-140">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e0feb-141">provoqué</span><span class="sxs-lookup"><span data-stu-id="e0feb-141">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e0feb-142">Résultat de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="e0feb-142">Evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="e0feb-143">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="e0feb-143">callFunctionOn</span></span>
<span data-ttu-id="e0feb-144">Fonction appelle avec la déclaration fournie sur l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="e0feb-144">Calls function with given declaration on the given object.</span></span> <span data-ttu-id="e0feb-145">Le groupe d’objets du résultat est hérité de l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="e0feb-145">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e0feb-146">Parameters</span><span class="sxs-lookup"><span data-stu-id="e0feb-146">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e0feb-147">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="e0feb-147">functionDeclaration</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e0feb-148">Déclaration de la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="e0feb-148">Declaration of the function to call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-149">Algorithm</span><span class="sxs-lookup"><span data-stu-id="e0feb-149">objectId</span></span> <br/> <i><span data-ttu-id="e0feb-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-150">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="e0feb-151">Identificateur de l’objet sur lequel appeler la fonction.</span><span class="sxs-lookup"><span data-stu-id="e0feb-151">Identifier of the object to call function on.</span></span> <span data-ttu-id="e0feb-152">ObjectId ou executionContextId doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="e0feb-152">Either objectId or executionContextId should be specified.</span></span>  <span data-ttu-id="e0feb-153">objectId doit être issu de la fonction Runtime. Evaluate ().</span><span class="sxs-lookup"><span data-stu-id="e0feb-153">objectId must be from the Runtime.evaluate() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-154">arguments</span><span class="sxs-lookup"><span data-stu-id="e0feb-154">arguments</span></span> <br/> <i><span data-ttu-id="e0feb-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-155">optional</span></span></i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td><span data-ttu-id="e0feb-156">Appeler des arguments.</span><span class="sxs-lookup"><span data-stu-id="e0feb-156">Call arguments.</span></span> <span data-ttu-id="e0feb-157">Tous les arguments d’appel doivent appartenir au même univers JavaScript que l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="e0feb-157">All call arguments must belong to the same JavaScript world as the target object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-158">silent</span><span class="sxs-lookup"><span data-stu-id="e0feb-158">silent</span></span> <br/> <i><span data-ttu-id="e0feb-159">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-159">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e0feb-160">En mode silencieux, les exceptions levées lors de l’évaluation ne sont pas communiquées et n’interrompent pas l’exécution.</span><span class="sxs-lookup"><span data-stu-id="e0feb-160">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="e0feb-161">Remplace l' <code>setPauseOnException</code> État.</span><span class="sxs-lookup"><span data-stu-id="e0feb-161">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-162">returnByValue</span><span class="sxs-lookup"><span data-stu-id="e0feb-162">returnByValue</span></span> <br/> <i><span data-ttu-id="e0feb-163">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-163">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e0feb-164">Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</span><span class="sxs-lookup"><span data-stu-id="e0feb-164">Whether the result is expected to be a JSON object which should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-165">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="e0feb-165">awaitPromise</span></span> <br/> <i><span data-ttu-id="e0feb-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-166">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e0feb-167">Si l’exécution doit avoir <code>await</code> pour résultat la valeur résultante et l’État retour une fois la promesse attendue résolue.</span><span class="sxs-lookup"><span data-stu-id="e0feb-167">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e0feb-168">Renvoie</span><span class="sxs-lookup"><span data-stu-id="e0feb-168">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e0feb-169">provoqué</span><span class="sxs-lookup"><span data-stu-id="e0feb-169">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e0feb-170">Résultat de l’appel.</span><span class="sxs-lookup"><span data-stu-id="e0feb-170">Call result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="e0feb-171">getProperties</span><span class="sxs-lookup"><span data-stu-id="e0feb-171">getProperties</span></span>
<span data-ttu-id="e0feb-172">Renvoie les propriétés d’un objet donné.</span><span class="sxs-lookup"><span data-stu-id="e0feb-172">Returns properties of a given object.</span></span> <span data-ttu-id="e0feb-173">Le groupe d’objets du résultat est hérité de l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="e0feb-173">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e0feb-174">Parameters</span><span class="sxs-lookup"><span data-stu-id="e0feb-174">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e0feb-175">Algorithm</span><span class="sxs-lookup"><span data-stu-id="e0feb-175">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="e0feb-176">Identificateur de l’objet dont vous souhaitez renvoyer les propriétés.</span><span class="sxs-lookup"><span data-stu-id="e0feb-176">Identifier of the object to return properties for.</span></span>  <span data-ttu-id="e0feb-177">objectId doit être issu de la fonction Debugger. evaluateOnCallFrame ().</span><span class="sxs-lookup"><span data-stu-id="e0feb-177">objectId must be from the Debugger.evaluateOnCallFrame() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-178">ownProperties</span><span class="sxs-lookup"><span data-stu-id="e0feb-178">ownProperties</span></span> <br/> <i><span data-ttu-id="e0feb-179">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-179">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e0feb-180">Si la valeur est true, retourne les propriétés qui ne sont liées qu’à l’élément proprement dit, et non à sa chaîne de prototype.</span><span class="sxs-lookup"><span data-stu-id="e0feb-180">If true, returns properties belonging only to the element itself, not to its prototype chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-181">accessorPropertiesOnly</span><span class="sxs-lookup"><span data-stu-id="e0feb-181">accessorPropertiesOnly</span></span> <br/> <i><span data-ttu-id="e0feb-182">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-182">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="e0feb-183">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="e0feb-183">Experimental.</span></span> </b></span><span data-ttu-id="e0feb-184">Si true, retourne les propriétés d’accesseur (avec l’accesseur get/set) uniquement; les propriétés internes ne sont pas renvoyées.</span><span class="sxs-lookup"><span data-stu-id="e0feb-184">If true, returns accessor properties (with getter/setter) only; internal properties are not returned either.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e0feb-185">Renvoie</span><span class="sxs-lookup"><span data-stu-id="e0feb-185">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e0feb-186">provoqué</span><span class="sxs-lookup"><span data-stu-id="e0feb-186">result</span></span></td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td><span data-ttu-id="e0feb-187">Propriétés d’objet.</span><span class="sxs-lookup"><span data-stu-id="e0feb-187">Object properties.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="e0feb-188">Événements</span><span class="sxs-lookup"><span data-stu-id="e0feb-188">Events</span></span>

### <span data-ttu-id="e0feb-189">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="e0feb-189">executionContextsCleared</span></span>
<span data-ttu-id="e0feb-190">Émis lorsque tous les executionContexts étaient effacés dans le navigateur</span><span class="sxs-lookup"><span data-stu-id="e0feb-190">Issued when all executionContexts were cleared in browser</span></span>


---

### <span data-ttu-id="e0feb-191">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="e0feb-191">exceptionThrown</span></span>
<span data-ttu-id="e0feb-192">Émis quand une exception a été levée et non gérée.</span><span class="sxs-lookup"><span data-stu-id="e0feb-192">Issued when exception was thrown and unhandled.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e0feb-193">Parameters</span><span class="sxs-lookup"><span data-stu-id="e0feb-193">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e0feb-194">telle</span><span class="sxs-lookup"><span data-stu-id="e0feb-194">timestamp</span></span></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="e0feb-195">Horodatage de l’exception.</span><span class="sxs-lookup"><span data-stu-id="e0feb-195">Timestamp of the exception.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-196">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="e0feb-196">exceptionDetails</span></span></td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="e0feb-197">Types</span><span class="sxs-lookup"><span data-stu-id="e0feb-197">Types</span></span>

### <a name="scriptid"></a> <span data-ttu-id="e0feb-198">ScriptId</span><span class="sxs-lookup"><span data-stu-id="e0feb-198">ScriptId</span></span> `string`

<span data-ttu-id="e0feb-199">Identificateur de script unique.</span><span class="sxs-lookup"><span data-stu-id="e0feb-199">Unique script identifier.</span></span>


---

### <a name="remoteobjectid"></a> <span data-ttu-id="e0feb-200">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="e0feb-200">RemoteObjectId</span></span> `string`

<span data-ttu-id="e0feb-201">Identifiant unique de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e0feb-201">Unique object identifier.</span></span>


---

### <a name="unserializablevalue"></a> <span data-ttu-id="e0feb-202">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="e0feb-202">UnserializableValue</span></span> `string`

<span data-ttu-id="e0feb-203">Valeur primitive qui ne peut pas être JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="e0feb-203">Primitive value which cannot be JSON-stringified.</span></span>

##### <span data-ttu-id="e0feb-204">Valeurs autorisées</span><span class="sxs-lookup"><span data-stu-id="e0feb-204">Allowed Values</span></span>
<span data-ttu-id="e0feb-205">Infinity, NaN,-Infinity,-0</span><span class="sxs-lookup"><span data-stu-id="e0feb-205">Infinity, NaN, -Infinity, -0</span></span>

---

### <a name="remoteobject"></a> <span data-ttu-id="e0feb-206">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="e0feb-206">RemoteObject</span></span> `object`

<span data-ttu-id="e0feb-207">Objet Mirror référençant l’objet JavaScript d’origine.</span><span class="sxs-lookup"><span data-stu-id="e0feb-207">Mirror object referencing original JavaScript object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e0feb-208">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0feb-208">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e0feb-209">type</span><span class="sxs-lookup"><span data-stu-id="e0feb-209">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="e0feb-210">Valeurs autorisées: objet, fonction, non défini, chaîne, nombre, booléen, symbole</span><span class="sxs-lookup"><span data-stu-id="e0feb-210">Allowed values: object, function, undefined, string, number, boolean, symbol</span></span></i></td>
            <td><span data-ttu-id="e0feb-211">Type d’objet.</span><span class="sxs-lookup"><span data-stu-id="e0feb-211">Object type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-212">sous-type</span><span class="sxs-lookup"><span data-stu-id="e0feb-212">subtype</span></span> <br/> <i><span data-ttu-id="e0feb-213">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-213">optional</span></span></i></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="e0feb-214">Valeurs autorisées: null, erreur, promesse</span><span class="sxs-lookup"><span data-stu-id="e0feb-214">Allowed values: null, error, promise</span></span></i></td>
            <td><span data-ttu-id="e0feb-215">Indicateur de sous-type d’objet.</span><span class="sxs-lookup"><span data-stu-id="e0feb-215">Object subtype hint.</span></span> <span data-ttu-id="e0feb-216">Spécifié pour les <code>object</code> valeurs de type uniquement.</span><span class="sxs-lookup"><span data-stu-id="e0feb-216">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-217">NomClasse</span><span class="sxs-lookup"><span data-stu-id="e0feb-217">className</span></span> <br/> <i><span data-ttu-id="e0feb-218">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-218">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e0feb-219">Nom de classe d’objet (constructeur).</span><span class="sxs-lookup"><span data-stu-id="e0feb-219">Object class (constructor) name.</span></span> <span data-ttu-id="e0feb-220">Spécifié pour les <code>object</code> valeurs de type uniquement.</span><span class="sxs-lookup"><span data-stu-id="e0feb-220">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-221">value</span><span class="sxs-lookup"><span data-stu-id="e0feb-221">value</span></span> <br/> <i><span data-ttu-id="e0feb-222">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-222">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="e0feb-223">Valeur de l’objet distant en cas de valeurs primitives ou de valeurs JSON (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="e0feb-223">Remote object value in case of primitive values or JSON values (if it was requested).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-224">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="e0feb-224">unserializableValue</span></span> <br/> <i><span data-ttu-id="e0feb-225">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-225">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="e0feb-226">Valeur primitive qui ne peut pas être JSON-stringified</span><span class="sxs-lookup"><span data-stu-id="e0feb-226">Primitive value which can not be JSON-stringified does not have</span></span> <code>value</code><span data-ttu-id="e0feb-227">mais obtient cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e0feb-227">, but gets this property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-228">description</span><span class="sxs-lookup"><span data-stu-id="e0feb-228">description</span></span> <br/> <i><span data-ttu-id="e0feb-229">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-229">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e0feb-230">Représentation de chaîne de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e0feb-230">String representation of the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-231">Algorithm</span><span class="sxs-lookup"><span data-stu-id="e0feb-231">objectId</span></span> <br/> <i><span data-ttu-id="e0feb-232">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-232">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="e0feb-233">Identificateur d’objet unique (pour les valeurs non Primitives).</span><span class="sxs-lookup"><span data-stu-id="e0feb-233">Unique object identifier (for non-primitive values).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-234">msDebuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="e0feb-234">msDebuggerPropertyId</span></span> <br/> <i><span data-ttu-id="e0feb-235">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-235">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="e0feb-236">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="e0feb-236">Experimental.</span></span> </b></span><span data-ttu-id="e0feb-237">Microsoft: ID de propriété de débogueur associé pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="e0feb-237">Microsoft: The associated debugger property id for this object.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="propertydescriptor"></a> <span data-ttu-id="e0feb-238">PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="e0feb-238">PropertyDescriptor</span></span> `object`

<span data-ttu-id="e0feb-239">Descripteur de propriété objet.</span><span class="sxs-lookup"><span data-stu-id="e0feb-239">Object property descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e0feb-240">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0feb-240">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e0feb-241">name</span><span class="sxs-lookup"><span data-stu-id="e0feb-241">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e0feb-242">Nom de la propriété ou description du symbole.</span><span class="sxs-lookup"><span data-stu-id="e0feb-242">Property name or symbol description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-243">value</span><span class="sxs-lookup"><span data-stu-id="e0feb-243">value</span></span> <br/> <i><span data-ttu-id="e0feb-244">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-244">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e0feb-245">Valeur associée à la propriété.</span><span class="sxs-lookup"><span data-stu-id="e0feb-245">The value associated with the property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-246">accès</span><span class="sxs-lookup"><span data-stu-id="e0feb-246">writable</span></span> <br/> <i><span data-ttu-id="e0feb-247">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-247">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e0feb-248">True si la valeur associée à la propriété est susceptible d’être modifiée (descripteurs de données uniquement).</span><span class="sxs-lookup"><span data-stu-id="e0feb-248">True if the value associated with the property may be changed (data descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-249">obtenir</span><span class="sxs-lookup"><span data-stu-id="e0feb-249">get</span></span> <br/> <i><span data-ttu-id="e0feb-250">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-250">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e0feb-251">Fonction qui sert de Getter pour la propriété, ou <code>undefined</code> s’il n’y a pas d’accesseur get (descripteurs d’accesseur uniquement).</span><span class="sxs-lookup"><span data-stu-id="e0feb-251">A function which serves as a getter for the property, or <code>undefined</code> if there is no getter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-252">set</span><span class="sxs-lookup"><span data-stu-id="e0feb-252">set</span></span> <br/> <i><span data-ttu-id="e0feb-253">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-253">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e0feb-254">Fonction utilisée comme une méthode setter de la propriété, ou <code>undefined</code> s’il n’y a pas de méthodes setter (descripteurs d’accesseur uniquement).</span><span class="sxs-lookup"><span data-stu-id="e0feb-254">A function which serves as a setter for the property, or <code>undefined</code> if there is no setter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-255">configurables</span><span class="sxs-lookup"><span data-stu-id="e0feb-255">configurable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e0feb-256">True si le type de ce descripteur de propriété est modifiable et si la propriété est susceptible d’être supprimée de l’objet correspondant.</span><span class="sxs-lookup"><span data-stu-id="e0feb-256">True if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-257">tournant</span><span class="sxs-lookup"><span data-stu-id="e0feb-257">enumerable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e0feb-258">True si cette propriété s’affiche lors de l’énumération des propriétés de l’objet correspondant.</span><span class="sxs-lookup"><span data-stu-id="e0feb-258">True if this property shows up during enumeration of the properties on the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-259">wasThrown</span><span class="sxs-lookup"><span data-stu-id="e0feb-259">wasThrown</span></span> <br/> <i><span data-ttu-id="e0feb-260">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-260">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e0feb-261">True si le résultat a été levé lors de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="e0feb-261">True if the result was thrown during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-262">isOwn</span><span class="sxs-lookup"><span data-stu-id="e0feb-262">isOwn</span></span> <br/> <i><span data-ttu-id="e0feb-263">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-263">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e0feb-264">True si la propriété est possédée pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="e0feb-264">True if the property is owned for the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-265">msReturnValue</span><span class="sxs-lookup"><span data-stu-id="e0feb-265">msReturnValue</span></span> <br/> <i><span data-ttu-id="e0feb-266">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-266">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="e0feb-267">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="e0feb-267">Experimental.</span></span> </b></span><span data-ttu-id="e0feb-268">Microsoft: true si la propriété est une valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e0feb-268">Microsoft: True if the property is a return value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-269">symbol</span><span class="sxs-lookup"><span data-stu-id="e0feb-269">symbol</span></span> <br/> <i><span data-ttu-id="e0feb-270">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-270">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e0feb-271">Objet symbol de propriété, si la propriété est de `symbol` type.</span><span class="sxs-lookup"><span data-stu-id="e0feb-271">Property symbol object, if the property is of the `symbol` type.</span></span> </td>
        </tr>
    </tbody>
</table>

---

### <a name="callargument"></a> <span data-ttu-id="e0feb-272">CallArgument</span><span class="sxs-lookup"><span data-stu-id="e0feb-272">CallArgument</span></span> `object`

<span data-ttu-id="e0feb-273">Représente l’argument appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="e0feb-273">Represents function call argument.</span></span> <span data-ttu-id="e0feb-274">ID d’objet distant <code>objectId</code> , primitive <code>value</code> , valeur primitive unserializable ou aucun de (pour undefined).</span><span class="sxs-lookup"><span data-stu-id="e0feb-274">Either remote object id <code>objectId</code>, primitive <code>value</code>, unserializable primitive value or neither of (for undefined) them should be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e0feb-275">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0feb-275">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e0feb-276">value</span><span class="sxs-lookup"><span data-stu-id="e0feb-276">value</span></span> <br/> <i><span data-ttu-id="e0feb-277">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-277">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="e0feb-278">Valeur primitive ou objet JavaScript sérialisable.</span><span class="sxs-lookup"><span data-stu-id="e0feb-278">Primitive value or serializable javascript object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-279">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="e0feb-279">unserializableValue</span></span> <br/> <i><span data-ttu-id="e0feb-280">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-280">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="e0feb-281">Valeur primitive qui ne peut pas être JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="e0feb-281">Primitive value which can not be JSON-stringified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-282">Algorithm</span><span class="sxs-lookup"><span data-stu-id="e0feb-282">objectId</span></span> <br/> <i><span data-ttu-id="e0feb-283">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-283">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="e0feb-284">Handle d’objet distant.</span><span class="sxs-lookup"><span data-stu-id="e0feb-284">Remote object handle.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="executioncontextid"></a> <span data-ttu-id="e0feb-285">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="e0feb-285">ExecutionContextId</span></span> `integer`

<span data-ttu-id="e0feb-286">ID du contexte d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e0feb-286">Id of an execution context.</span></span>


---

### <a name="exceptiondetails"></a> <span data-ttu-id="e0feb-287">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="e0feb-287">ExceptionDetails</span></span> `object`

<span data-ttu-id="e0feb-288">Informations détaillées sur l’exception (ou l’erreur) levée lors de la compilation ou de l’exécution d’un script.</span><span class="sxs-lookup"><span data-stu-id="e0feb-288">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e0feb-289">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0feb-289">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e0feb-290">exceptionId</span><span class="sxs-lookup"><span data-stu-id="e0feb-290">exceptionId</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e0feb-291">ID de l’exception.</span><span class="sxs-lookup"><span data-stu-id="e0feb-291">Exception id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-292">texte</span><span class="sxs-lookup"><span data-stu-id="e0feb-292">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e0feb-293">Texte de l’exception, qui doit être utilisé avec l’objet exception lorsqu’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="e0feb-293">Exception text, which should be used together with exception object when available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-294">lineNumber</span><span class="sxs-lookup"><span data-stu-id="e0feb-294">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e0feb-295">Numéro de ligne de l’emplacement de l’exception (0).</span><span class="sxs-lookup"><span data-stu-id="e0feb-295">Line number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-296">columnNumber</span><span class="sxs-lookup"><span data-stu-id="e0feb-296">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e0feb-297">Numéro de colonne de l’emplacement de l’exception (0).</span><span class="sxs-lookup"><span data-stu-id="e0feb-297">Column number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-298">scriptId</span><span class="sxs-lookup"><span data-stu-id="e0feb-298">scriptId</span></span> <br/> <i><span data-ttu-id="e0feb-299">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-299">optional</span></span></i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="e0feb-300">ID de script de l’emplacement de l’exception.</span><span class="sxs-lookup"><span data-stu-id="e0feb-300">Script ID of the exception location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-301">url</span><span class="sxs-lookup"><span data-stu-id="e0feb-301">url</span></span> <br/> <i><span data-ttu-id="e0feb-302">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-302">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e0feb-303">URL de l’emplacement de l’exception à utiliser lorsque le script n’a pas été communiqué.</span><span class="sxs-lookup"><span data-stu-id="e0feb-303">URL of the exception location, to be used when the script was not reported.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-304">Trace</span><span class="sxs-lookup"><span data-stu-id="e0feb-304">stackTrace</span></span> <br/> <i><span data-ttu-id="e0feb-305">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-305">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="e0feb-306">Trace de pile JavaScript, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e0feb-306">JavaScript stack trace if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-307">sauf</span><span class="sxs-lookup"><span data-stu-id="e0feb-307">exception</span></span> <br/> <i><span data-ttu-id="e0feb-308">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-308">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="e0feb-309">Objet exception, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="e0feb-309">Exception object if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-310">executionContextId</span><span class="sxs-lookup"><span data-stu-id="e0feb-310">executionContextId</span></span> <br/> <i><span data-ttu-id="e0feb-311">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-311">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="e0feb-312">Identificateur du contexte où une exception s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e0feb-312">Identifier of the context where exception happened.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="timestamp"></a> <span data-ttu-id="e0feb-313">Horodateur</span><span class="sxs-lookup"><span data-stu-id="e0feb-313">Timestamp</span></span> `integer`

<span data-ttu-id="e0feb-314">Nombre de millisecondes depuis l’époque.</span><span class="sxs-lookup"><span data-stu-id="e0feb-314">Number of milliseconds since epoch.</span></span>


---

### <a name="callframe"></a> <span data-ttu-id="e0feb-315">CallFrame</span><span class="sxs-lookup"><span data-stu-id="e0feb-315">CallFrame</span></span> `object`

<span data-ttu-id="e0feb-316">Entrée de pile pour les erreurs d’exécution et les affirmations.</span><span class="sxs-lookup"><span data-stu-id="e0feb-316">Stack entry for runtime errors and assertions.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e0feb-317">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0feb-317">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e0feb-318">Admises</span><span class="sxs-lookup"><span data-stu-id="e0feb-318">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e0feb-319">Nom de la fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e0feb-319">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-320">scriptId</span><span class="sxs-lookup"><span data-stu-id="e0feb-320">scriptId</span></span></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="e0feb-321">ID de script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e0feb-321">JavaScript script id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-322">url</span><span class="sxs-lookup"><span data-stu-id="e0feb-322">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e0feb-323">Nom ou URL du script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e0feb-323">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-324">lineNumber</span><span class="sxs-lookup"><span data-stu-id="e0feb-324">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e0feb-325">Numéro de ligne de script JavaScript (0).</span><span class="sxs-lookup"><span data-stu-id="e0feb-325">JavaScript script line number (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-326">columnNumber</span><span class="sxs-lookup"><span data-stu-id="e0feb-326">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e0feb-327">Numéro de colonne de script JavaScript (0).</span><span class="sxs-lookup"><span data-stu-id="e0feb-327">JavaScript script column number (0-based).</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="stacktrace"></a> <span data-ttu-id="e0feb-328">Trace</span><span class="sxs-lookup"><span data-stu-id="e0feb-328">StackTrace</span></span> `object`

<span data-ttu-id="e0feb-329">Trames d’appel pour les affirmations ou messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e0feb-329">Call frames for assertions or error messages.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e0feb-330">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0feb-330">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e0feb-331">description</span><span class="sxs-lookup"><span data-stu-id="e0feb-331">description</span></span> <br/> <i><span data-ttu-id="e0feb-332">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-332">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e0feb-333">Étiquette de chaîne de cette trace de pile.</span><span class="sxs-lookup"><span data-stu-id="e0feb-333">String label of this stack trace.</span></span> <span data-ttu-id="e0feb-334">Pour les traces Async, il s’agit du nom de la fonction qui a déclenché l’appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e0feb-334">For async traces this may be a name of the function that initiated the async call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-335">callFrames</span><span class="sxs-lookup"><span data-stu-id="e0feb-335">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="e0feb-336">Nom de la fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e0feb-336">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e0feb-337">dernier</span><span class="sxs-lookup"><span data-stu-id="e0feb-337">parent</span></span> <br/> <i><span data-ttu-id="e0feb-338">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-338">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="e0feb-339">Trace de pile JavaScript asynchrone qui précède cette pile, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="e0feb-339">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span></td>
        </tr>
    </tbody>
</table>

---
