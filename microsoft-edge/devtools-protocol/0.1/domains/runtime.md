---
description: Référence pour le domaine Runtime. Le domaine d’exécution expose le runtime JavaScript au moyen de l’évaluation à distance et des objets miroirs. Les résultats d’évaluation sont retournés sous la forme d’un objet miroir exposant le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour une référence d’objet supplémentaire. Les objets d’origine sont conservés en mémoire, sauf s’ils sont explicitement émis.
title: Domain Runtime-DevTools Protocol version 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 33bc98b272aaa8831e908207b97ea7d3d0842976
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565488"
---
# <span data-ttu-id="62aff-106">Runtime</span><span class="sxs-lookup"><span data-stu-id="62aff-106">Runtime</span></span>
<span data-ttu-id="62aff-107">Le domaine d’exécution expose le runtime JavaScript au moyen de l’évaluation à distance et des objets miroirs.</span><span class="sxs-lookup"><span data-stu-id="62aff-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="62aff-108">Les résultats d’évaluation sont retournés sous la forme d’un objet miroir exposant le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour une référence d’objet supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="62aff-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="62aff-109">Les objets d’origine sont conservés en mémoire, sauf s’ils sont explicitement émis.</span><span class="sxs-lookup"><span data-stu-id="62aff-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="62aff-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="62aff-110">Methods</span></span>**](#methods) | <span data-ttu-id="62aff-111">[activer](#enable), [Désactiver](#disable), [évaluer](#evaluate), [callFunctionOn](#callfunctionon), [GetProperties](#getproperties)</span><span class="sxs-lookup"><span data-stu-id="62aff-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span></span> |
| [**<span data-ttu-id="62aff-112">Événements</span><span class="sxs-lookup"><span data-stu-id="62aff-112">Events</span></span>**](#events) | <span data-ttu-id="62aff-113">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span><span class="sxs-lookup"><span data-stu-id="62aff-113">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span></span> |
| [**<span data-ttu-id="62aff-114">Types</span><span class="sxs-lookup"><span data-stu-id="62aff-114">Types</span></span>**](#types) | <span data-ttu-id="62aff-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="62aff-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |
## <span data-ttu-id="62aff-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="62aff-116">Methods</span></span>

### <span data-ttu-id="62aff-117">activer</span><span class="sxs-lookup"><span data-stu-id="62aff-117">enable</span></span>
<span data-ttu-id="62aff-118">Autorise la création de rapports sur l' <code>executionContextsCleared</code> événement.</span><span class="sxs-lookup"><span data-stu-id="62aff-118">Enables reporting of the <code>executionContextsCleared</code> event.</span></span>


---

### <span data-ttu-id="62aff-119">désactiver </span><span class="sxs-lookup"><span data-stu-id="62aff-119">disable</span></span>
<span data-ttu-id="62aff-120">Désactive la création de rapports sur l' <code>executionContextsCleared</code> événement.</span><span class="sxs-lookup"><span data-stu-id="62aff-120">Disables reporting of the <code>executionContextsCleared</code> event.</span></span>


---

### <span data-ttu-id="62aff-121">evaluat</span><span class="sxs-lookup"><span data-stu-id="62aff-121">evaluate</span></span>
<span data-ttu-id="62aff-122">Évalue l’expression sur l’objet global.</span><span class="sxs-lookup"><span data-stu-id="62aff-122">Evaluates expression on global object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="62aff-123">Parameters</span><span class="sxs-lookup"><span data-stu-id="62aff-123">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="62aff-124">termes</span><span class="sxs-lookup"><span data-stu-id="62aff-124">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="62aff-125">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="62aff-125">Expression to evaluate.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-126">silent</span><span class="sxs-lookup"><span data-stu-id="62aff-126">silent</span></span> <br/> <i><span data-ttu-id="62aff-127">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-127">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="62aff-128">En mode silencieux, les exceptions levées lors de l’évaluation ne sont pas communiquées et n’interrompent pas l’exécution.</span><span class="sxs-lookup"><span data-stu-id="62aff-128">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="62aff-129">Remplace l' <code>setPauseOnException</code> État.</span><span class="sxs-lookup"><span data-stu-id="62aff-129">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-130">contextId</span><span class="sxs-lookup"><span data-stu-id="62aff-130">contextId</span></span> <br/> <i><span data-ttu-id="62aff-131">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-131">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="62aff-132">Spécifie le contexte d’exécution permettant d’effectuer une évaluation.</span><span class="sxs-lookup"><span data-stu-id="62aff-132">Specifies in which execution context to perform evaluation.</span></span> <span data-ttu-id="62aff-133">Si le paramètre est omis, l’évaluation sera exécutée dans le contexte de la page inspectée.</span><span class="sxs-lookup"><span data-stu-id="62aff-133">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-134">returnByValue</span><span class="sxs-lookup"><span data-stu-id="62aff-134">returnByValue</span></span> <br/> <i><span data-ttu-id="62aff-135">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-135">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="62aff-136">Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</span><span class="sxs-lookup"><span data-stu-id="62aff-136">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-137">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="62aff-137">awaitPromise</span></span> <br/> <i><span data-ttu-id="62aff-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-138">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="62aff-139">Si l’exécution doit avoir <code>await</code> pour résultat la valeur résultante et l’État retour une fois la promesse attendue résolue.</span><span class="sxs-lookup"><span data-stu-id="62aff-139">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="62aff-140">Renvoie</span><span class="sxs-lookup"><span data-stu-id="62aff-140">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="62aff-141">provoqué</span><span class="sxs-lookup"><span data-stu-id="62aff-141">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="62aff-142">Résultat de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="62aff-142">Evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="62aff-143">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="62aff-143">callFunctionOn</span></span>
<span data-ttu-id="62aff-144">Fonction appelle avec la déclaration fournie sur l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="62aff-144">Calls function with given declaration on the given object.</span></span> <span data-ttu-id="62aff-145">Le groupe d’objets du résultat est hérité de l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="62aff-145">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="62aff-146">Parameters</span><span class="sxs-lookup"><span data-stu-id="62aff-146">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="62aff-147">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="62aff-147">functionDeclaration</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="62aff-148">Déclaration de la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="62aff-148">Declaration of the function to call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-149">Algorithm</span><span class="sxs-lookup"><span data-stu-id="62aff-149">objectId</span></span> <br/> <i><span data-ttu-id="62aff-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-150">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="62aff-151">Identificateur de l’objet sur lequel appeler la fonction.</span><span class="sxs-lookup"><span data-stu-id="62aff-151">Identifier of the object to call function on.</span></span> <span data-ttu-id="62aff-152">ObjectId ou executionContextId doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="62aff-152">Either objectId or executionContextId should be specified.</span></span>  <span data-ttu-id="62aff-153">objectId doit être issu de la fonction Runtime. Evaluate ().</span><span class="sxs-lookup"><span data-stu-id="62aff-153">objectId must be from the Runtime.evaluate() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-154">arguments</span><span class="sxs-lookup"><span data-stu-id="62aff-154">arguments</span></span> <br/> <i><span data-ttu-id="62aff-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-155">optional</span></span></i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td><span data-ttu-id="62aff-156">Appeler des arguments.</span><span class="sxs-lookup"><span data-stu-id="62aff-156">Call arguments.</span></span> <span data-ttu-id="62aff-157">Tous les arguments d’appel doivent appartenir au même univers JavaScript que l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="62aff-157">All call arguments must belong to the same JavaScript world as the target object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-158">silent</span><span class="sxs-lookup"><span data-stu-id="62aff-158">silent</span></span> <br/> <i><span data-ttu-id="62aff-159">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-159">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="62aff-160">En mode silencieux, les exceptions levées lors de l’évaluation ne sont pas communiquées et n’interrompent pas l’exécution.</span><span class="sxs-lookup"><span data-stu-id="62aff-160">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="62aff-161">Remplace l' <code>setPauseOnException</code> État.</span><span class="sxs-lookup"><span data-stu-id="62aff-161">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-162">returnByValue</span><span class="sxs-lookup"><span data-stu-id="62aff-162">returnByValue</span></span> <br/> <i><span data-ttu-id="62aff-163">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-163">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="62aff-164">Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</span><span class="sxs-lookup"><span data-stu-id="62aff-164">Whether the result is expected to be a JSON object which should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-165">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="62aff-165">awaitPromise</span></span> <br/> <i><span data-ttu-id="62aff-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-166">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="62aff-167">Si l’exécution doit avoir <code>await</code> pour résultat la valeur résultante et l’État retour une fois la promesse attendue résolue.</span><span class="sxs-lookup"><span data-stu-id="62aff-167">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="62aff-168">Renvoie</span><span class="sxs-lookup"><span data-stu-id="62aff-168">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="62aff-169">provoqué</span><span class="sxs-lookup"><span data-stu-id="62aff-169">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="62aff-170">Résultat de l’appel.</span><span class="sxs-lookup"><span data-stu-id="62aff-170">Call result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="62aff-171">getProperties</span><span class="sxs-lookup"><span data-stu-id="62aff-171">getProperties</span></span>
<span data-ttu-id="62aff-172">Renvoie les propriétés d’un objet donné.</span><span class="sxs-lookup"><span data-stu-id="62aff-172">Returns properties of a given object.</span></span> <span data-ttu-id="62aff-173">Le groupe d’objets du résultat est hérité de l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="62aff-173">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="62aff-174">Parameters</span><span class="sxs-lookup"><span data-stu-id="62aff-174">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="62aff-175">Algorithm</span><span class="sxs-lookup"><span data-stu-id="62aff-175">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="62aff-176">Identificateur de l’objet dont vous souhaitez renvoyer les propriétés.</span><span class="sxs-lookup"><span data-stu-id="62aff-176">Identifier of the object to return properties for.</span></span>  <span data-ttu-id="62aff-177">objectId doit être issu de la fonction Debugger. evaluateOnCallFrame ().</span><span class="sxs-lookup"><span data-stu-id="62aff-177">objectId must be from the Debugger.evaluateOnCallFrame() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-178">ownProperties</span><span class="sxs-lookup"><span data-stu-id="62aff-178">ownProperties</span></span> <br/> <i><span data-ttu-id="62aff-179">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-179">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="62aff-180">Si la valeur est true, retourne les propriétés qui ne sont liées qu’à l’élément proprement dit, et non à sa chaîne de prototype.</span><span class="sxs-lookup"><span data-stu-id="62aff-180">If true, returns properties belonging only to the element itself, not to its prototype chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-181">accessorPropertiesOnly</span><span class="sxs-lookup"><span data-stu-id="62aff-181">accessorPropertiesOnly</span></span> <br/> <i><span data-ttu-id="62aff-182">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-182">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="62aff-183">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="62aff-183">Experimental.</span></span> </b></span><span data-ttu-id="62aff-184">Si true, retourne les propriétés d’accesseur (avec l’accesseur get/set) uniquement; les propriétés internes ne sont pas renvoyées.</span><span class="sxs-lookup"><span data-stu-id="62aff-184">If true, returns accessor properties (with getter/setter) only; internal properties are not returned either.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="62aff-185">Renvoie</span><span class="sxs-lookup"><span data-stu-id="62aff-185">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="62aff-186">provoqué</span><span class="sxs-lookup"><span data-stu-id="62aff-186">result</span></span></td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td><span data-ttu-id="62aff-187">Propriétés d’objet.</span><span class="sxs-lookup"><span data-stu-id="62aff-187">Object properties.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="62aff-188">Événements</span><span class="sxs-lookup"><span data-stu-id="62aff-188">Events</span></span>

### <span data-ttu-id="62aff-189">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="62aff-189">executionContextsCleared</span></span>
<span data-ttu-id="62aff-190">Émis lorsque tous les executionContexts étaient effacés dans le navigateur</span><span class="sxs-lookup"><span data-stu-id="62aff-190">Issued when all executionContexts were cleared in browser</span></span>


---

### <span data-ttu-id="62aff-191">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="62aff-191">exceptionThrown</span></span>
<span data-ttu-id="62aff-192">Émis quand une exception a été levée et non gérée.</span><span class="sxs-lookup"><span data-stu-id="62aff-192">Issued when exception was thrown and unhandled.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="62aff-193">Parameters</span><span class="sxs-lookup"><span data-stu-id="62aff-193">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="62aff-194">telle</span><span class="sxs-lookup"><span data-stu-id="62aff-194">timestamp</span></span></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="62aff-195">Horodatage de l’exception.</span><span class="sxs-lookup"><span data-stu-id="62aff-195">Timestamp of the exception.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-196">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="62aff-196">exceptionDetails</span></span></td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="62aff-197">Types</span><span class="sxs-lookup"><span data-stu-id="62aff-197">Types</span></span>

### <a name="scriptid"></a> <span data-ttu-id="62aff-198">ScriptId</span><span class="sxs-lookup"><span data-stu-id="62aff-198">ScriptId</span></span> `string`

<span data-ttu-id="62aff-199">Identificateur de script unique.</span><span class="sxs-lookup"><span data-stu-id="62aff-199">Unique script identifier.</span></span>


---

### <a name="remoteobjectid"></a> <span data-ttu-id="62aff-200">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="62aff-200">RemoteObjectId</span></span> `string`

<span data-ttu-id="62aff-201">Identifiant unique de l’objet.</span><span class="sxs-lookup"><span data-stu-id="62aff-201">Unique object identifier.</span></span>


---

### <a name="unserializablevalue"></a> <span data-ttu-id="62aff-202">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="62aff-202">UnserializableValue</span></span> `string`

<span data-ttu-id="62aff-203">Valeur primitive qui ne peut pas être JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="62aff-203">Primitive value which cannot be JSON-stringified.</span></span>

##### <span data-ttu-id="62aff-204">Valeurs autorisées</span><span class="sxs-lookup"><span data-stu-id="62aff-204">Allowed Values</span></span>
<span data-ttu-id="62aff-205">Infinity, NaN,-Infinity,-0</span><span class="sxs-lookup"><span data-stu-id="62aff-205">Infinity, NaN, -Infinity, -0</span></span>

---

### <a name="remoteobject"></a> <span data-ttu-id="62aff-206">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="62aff-206">RemoteObject</span></span> `object`

<span data-ttu-id="62aff-207">Objet Mirror référençant l’objet JavaScript d’origine.</span><span class="sxs-lookup"><span data-stu-id="62aff-207">Mirror object referencing original JavaScript object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="62aff-208">Propriétés</span><span class="sxs-lookup"><span data-stu-id="62aff-208">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="62aff-209">type</span><span class="sxs-lookup"><span data-stu-id="62aff-209">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="62aff-210">Valeurs autorisées: objet, fonction, non défini, chaîne, nombre, booléen, symbole</span><span class="sxs-lookup"><span data-stu-id="62aff-210">Allowed values: object, function, undefined, string, number, boolean, symbol</span></span></i></td>
            <td><span data-ttu-id="62aff-211">Type d’objet.</span><span class="sxs-lookup"><span data-stu-id="62aff-211">Object type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-212">sous-type</span><span class="sxs-lookup"><span data-stu-id="62aff-212">subtype</span></span> <br/> <i><span data-ttu-id="62aff-213">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-213">optional</span></span></i></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="62aff-214">Valeurs autorisées: null, erreur, promesse</span><span class="sxs-lookup"><span data-stu-id="62aff-214">Allowed values: null, error, promise</span></span></i></td>
            <td><span data-ttu-id="62aff-215">Indicateur de sous-type d’objet.</span><span class="sxs-lookup"><span data-stu-id="62aff-215">Object subtype hint.</span></span> <span data-ttu-id="62aff-216">Spécifié pour les <code>object</code> valeurs de type uniquement.</span><span class="sxs-lookup"><span data-stu-id="62aff-216">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-217">NomClasse</span><span class="sxs-lookup"><span data-stu-id="62aff-217">className</span></span> <br/> <i><span data-ttu-id="62aff-218">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-218">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="62aff-219">Nom de classe d’objet (constructeur).</span><span class="sxs-lookup"><span data-stu-id="62aff-219">Object class (constructor) name.</span></span> <span data-ttu-id="62aff-220">Spécifié pour les <code>object</code> valeurs de type uniquement.</span><span class="sxs-lookup"><span data-stu-id="62aff-220">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-221">value</span><span class="sxs-lookup"><span data-stu-id="62aff-221">value</span></span> <br/> <i><span data-ttu-id="62aff-222">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-222">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="62aff-223">Valeur de l’objet distant en cas de valeurs primitives ou de valeurs JSON (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="62aff-223">Remote object value in case of primitive values or JSON values (if it was requested).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-224">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="62aff-224">unserializableValue</span></span> <br/> <i><span data-ttu-id="62aff-225">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-225">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="62aff-226">Valeur primitive qui ne peut pas être JSON-stringified</span><span class="sxs-lookup"><span data-stu-id="62aff-226">Primitive value which can not be JSON-stringified does not have</span></span> <code>value</code><span data-ttu-id="62aff-227">mais obtient cette propriété.</span><span class="sxs-lookup"><span data-stu-id="62aff-227">, but gets this property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-228">description</span><span class="sxs-lookup"><span data-stu-id="62aff-228">description</span></span> <br/> <i><span data-ttu-id="62aff-229">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-229">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="62aff-230">Représentation de chaîne de l’objet.</span><span class="sxs-lookup"><span data-stu-id="62aff-230">String representation of the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-231">Algorithm</span><span class="sxs-lookup"><span data-stu-id="62aff-231">objectId</span></span> <br/> <i><span data-ttu-id="62aff-232">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-232">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="62aff-233">Identificateur d’objet unique (pour les valeurs non Primitives).</span><span class="sxs-lookup"><span data-stu-id="62aff-233">Unique object identifier (for non-primitive values).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-234">msDebuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="62aff-234">msDebuggerPropertyId</span></span> <br/> <i><span data-ttu-id="62aff-235">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-235">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="62aff-236">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="62aff-236">Experimental.</span></span> </b></span><span data-ttu-id="62aff-237">Microsoft: ID de propriété de débogueur associé pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="62aff-237">Microsoft: The associated debugger property id for this object.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="propertydescriptor"></a> <span data-ttu-id="62aff-238">PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="62aff-238">PropertyDescriptor</span></span> `object`

<span data-ttu-id="62aff-239">Descripteur de propriété objet.</span><span class="sxs-lookup"><span data-stu-id="62aff-239">Object property descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="62aff-240">Propriétés</span><span class="sxs-lookup"><span data-stu-id="62aff-240">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="62aff-241">name</span><span class="sxs-lookup"><span data-stu-id="62aff-241">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="62aff-242">Nom de la propriété ou description du symbole.</span><span class="sxs-lookup"><span data-stu-id="62aff-242">Property name or symbol description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-243">value</span><span class="sxs-lookup"><span data-stu-id="62aff-243">value</span></span> <br/> <i><span data-ttu-id="62aff-244">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-244">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="62aff-245">Valeur associée à la propriété.</span><span class="sxs-lookup"><span data-stu-id="62aff-245">The value associated with the property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-246">accès</span><span class="sxs-lookup"><span data-stu-id="62aff-246">writable</span></span> <br/> <i><span data-ttu-id="62aff-247">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-247">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="62aff-248">True si la valeur associée à la propriété est susceptible d’être modifiée (descripteurs de données uniquement).</span><span class="sxs-lookup"><span data-stu-id="62aff-248">True if the value associated with the property may be changed (data descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-249">obtenir</span><span class="sxs-lookup"><span data-stu-id="62aff-249">get</span></span> <br/> <i><span data-ttu-id="62aff-250">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-250">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="62aff-251">Fonction qui sert de Getter pour la propriété, ou <code>undefined</code> s’il n’y a pas d’accesseur get (descripteurs d’accesseur uniquement).</span><span class="sxs-lookup"><span data-stu-id="62aff-251">A function which serves as a getter for the property, or <code>undefined</code> if there is no getter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-252">set</span><span class="sxs-lookup"><span data-stu-id="62aff-252">set</span></span> <br/> <i><span data-ttu-id="62aff-253">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-253">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="62aff-254">Fonction utilisée comme une méthode setter de la propriété, ou <code>undefined</code> s’il n’y a pas de méthodes setter (descripteurs d’accesseur uniquement).</span><span class="sxs-lookup"><span data-stu-id="62aff-254">A function which serves as a setter for the property, or <code>undefined</code> if there is no setter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-255">configurables</span><span class="sxs-lookup"><span data-stu-id="62aff-255">configurable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="62aff-256">True si le type de ce descripteur de propriété est modifiable et si la propriété est susceptible d’être supprimée de l’objet correspondant.</span><span class="sxs-lookup"><span data-stu-id="62aff-256">True if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-257">tournant</span><span class="sxs-lookup"><span data-stu-id="62aff-257">enumerable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="62aff-258">True si cette propriété s’affiche lors de l’énumération des propriétés de l’objet correspondant.</span><span class="sxs-lookup"><span data-stu-id="62aff-258">True if this property shows up during enumeration of the properties on the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-259">wasThrown</span><span class="sxs-lookup"><span data-stu-id="62aff-259">wasThrown</span></span> <br/> <i><span data-ttu-id="62aff-260">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-260">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="62aff-261">True si le résultat a été levé lors de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="62aff-261">True if the result was thrown during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-262">isOwn</span><span class="sxs-lookup"><span data-stu-id="62aff-262">isOwn</span></span> <br/> <i><span data-ttu-id="62aff-263">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-263">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="62aff-264">True si la propriété est possédée pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="62aff-264">True if the property is owned for the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-265">msReturnValue</span><span class="sxs-lookup"><span data-stu-id="62aff-265">msReturnValue</span></span> <br/> <i><span data-ttu-id="62aff-266">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-266">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="62aff-267">Pratiqué.</span><span class="sxs-lookup"><span data-stu-id="62aff-267">Experimental.</span></span> </b></span><span data-ttu-id="62aff-268">Microsoft: true si la propriété est une valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="62aff-268">Microsoft: True if the property is a return value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-269">symbol</span><span class="sxs-lookup"><span data-stu-id="62aff-269">symbol</span></span> <br/> <i><span data-ttu-id="62aff-270">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-270">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="62aff-271">Objet symbol de propriété, si la propriété est de `symbol` type.</span><span class="sxs-lookup"><span data-stu-id="62aff-271">Property symbol object, if the property is of the `symbol` type.</span></span> </td>
        </tr>
    </tbody>
</table>

---

### <a name="callargument"></a> <span data-ttu-id="62aff-272">CallArgument</span><span class="sxs-lookup"><span data-stu-id="62aff-272">CallArgument</span></span> `object`

<span data-ttu-id="62aff-273">Représente l’argument appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="62aff-273">Represents function call argument.</span></span> <span data-ttu-id="62aff-274">ID d’objet distant <code>objectId</code> , primitive <code>value</code> , valeur primitive unserializable ou aucun de (pour undefined).</span><span class="sxs-lookup"><span data-stu-id="62aff-274">Either remote object id <code>objectId</code>, primitive <code>value</code>, unserializable primitive value or neither of (for undefined) them should be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="62aff-275">Propriétés</span><span class="sxs-lookup"><span data-stu-id="62aff-275">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="62aff-276">value</span><span class="sxs-lookup"><span data-stu-id="62aff-276">value</span></span> <br/> <i><span data-ttu-id="62aff-277">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-277">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="62aff-278">Valeur primitive ou objet JavaScript sérialisable.</span><span class="sxs-lookup"><span data-stu-id="62aff-278">Primitive value or serializable javascript object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-279">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="62aff-279">unserializableValue</span></span> <br/> <i><span data-ttu-id="62aff-280">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-280">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="62aff-281">Valeur primitive qui ne peut pas être JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="62aff-281">Primitive value which can not be JSON-stringified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-282">Algorithm</span><span class="sxs-lookup"><span data-stu-id="62aff-282">objectId</span></span> <br/> <i><span data-ttu-id="62aff-283">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-283">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="62aff-284">Handle d’objet distant.</span><span class="sxs-lookup"><span data-stu-id="62aff-284">Remote object handle.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="executioncontextid"></a> <span data-ttu-id="62aff-285">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="62aff-285">ExecutionContextId</span></span> `integer`

<span data-ttu-id="62aff-286">ID du contexte d’exécution.</span><span class="sxs-lookup"><span data-stu-id="62aff-286">Id of an execution context.</span></span>


---

### <a name="exceptiondetails"></a> <span data-ttu-id="62aff-287">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="62aff-287">ExceptionDetails</span></span> `object`

<span data-ttu-id="62aff-288">Informations détaillées sur l’exception (ou l’erreur) levée lors de la compilation ou de l’exécution d’un script.</span><span class="sxs-lookup"><span data-stu-id="62aff-288">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="62aff-289">Propriétés</span><span class="sxs-lookup"><span data-stu-id="62aff-289">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="62aff-290">exceptionId</span><span class="sxs-lookup"><span data-stu-id="62aff-290">exceptionId</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="62aff-291">ID de l’exception.</span><span class="sxs-lookup"><span data-stu-id="62aff-291">Exception id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-292">texte</span><span class="sxs-lookup"><span data-stu-id="62aff-292">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="62aff-293">Texte de l’exception, qui doit être utilisé avec l’objet exception lorsqu’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="62aff-293">Exception text, which should be used together with exception object when available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-294">lineNumber</span><span class="sxs-lookup"><span data-stu-id="62aff-294">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="62aff-295">Numéro de ligne de l’emplacement de l’exception (0).</span><span class="sxs-lookup"><span data-stu-id="62aff-295">Line number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-296">columnNumber</span><span class="sxs-lookup"><span data-stu-id="62aff-296">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="62aff-297">Numéro de colonne de l’emplacement de l’exception (0).</span><span class="sxs-lookup"><span data-stu-id="62aff-297">Column number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-298">scriptId</span><span class="sxs-lookup"><span data-stu-id="62aff-298">scriptId</span></span> <br/> <i><span data-ttu-id="62aff-299">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-299">optional</span></span></i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="62aff-300">ID de script de l’emplacement de l’exception.</span><span class="sxs-lookup"><span data-stu-id="62aff-300">Script ID of the exception location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-301">url</span><span class="sxs-lookup"><span data-stu-id="62aff-301">url</span></span> <br/> <i><span data-ttu-id="62aff-302">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-302">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="62aff-303">URL de l’emplacement de l’exception à utiliser lorsque le script n’a pas été communiqué.</span><span class="sxs-lookup"><span data-stu-id="62aff-303">URL of the exception location, to be used when the script was not reported.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-304">Trace</span><span class="sxs-lookup"><span data-stu-id="62aff-304">stackTrace</span></span> <br/> <i><span data-ttu-id="62aff-305">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-305">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="62aff-306">Trace de pile JavaScript, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="62aff-306">JavaScript stack trace if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-307">sauf</span><span class="sxs-lookup"><span data-stu-id="62aff-307">exception</span></span> <br/> <i><span data-ttu-id="62aff-308">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-308">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="62aff-309">Objet exception, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="62aff-309">Exception object if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-310">executionContextId</span><span class="sxs-lookup"><span data-stu-id="62aff-310">executionContextId</span></span> <br/> <i><span data-ttu-id="62aff-311">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-311">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="62aff-312">Identificateur du contexte où une exception s’est produite.</span><span class="sxs-lookup"><span data-stu-id="62aff-312">Identifier of the context where exception happened.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="timestamp"></a> <span data-ttu-id="62aff-313">Horodateur</span><span class="sxs-lookup"><span data-stu-id="62aff-313">Timestamp</span></span> `integer`

<span data-ttu-id="62aff-314">Nombre de millisecondes depuis l’époque.</span><span class="sxs-lookup"><span data-stu-id="62aff-314">Number of milliseconds since epoch.</span></span>


---

### <a name="callframe"></a> <span data-ttu-id="62aff-315">CallFrame</span><span class="sxs-lookup"><span data-stu-id="62aff-315">CallFrame</span></span> `object`

<span data-ttu-id="62aff-316">Entrée de pile pour les erreurs d’exécution et les affirmations.</span><span class="sxs-lookup"><span data-stu-id="62aff-316">Stack entry for runtime errors and assertions.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="62aff-317">Propriétés</span><span class="sxs-lookup"><span data-stu-id="62aff-317">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="62aff-318">Admises</span><span class="sxs-lookup"><span data-stu-id="62aff-318">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="62aff-319">Nom de la fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="62aff-319">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-320">scriptId</span><span class="sxs-lookup"><span data-stu-id="62aff-320">scriptId</span></span></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="62aff-321">ID de script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="62aff-321">JavaScript script id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-322">url</span><span class="sxs-lookup"><span data-stu-id="62aff-322">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="62aff-323">Nom ou URL du script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="62aff-323">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-324">lineNumber</span><span class="sxs-lookup"><span data-stu-id="62aff-324">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="62aff-325">Numéro de ligne de script JavaScript (0).</span><span class="sxs-lookup"><span data-stu-id="62aff-325">JavaScript script line number (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-326">columnNumber</span><span class="sxs-lookup"><span data-stu-id="62aff-326">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="62aff-327">Numéro de colonne de script JavaScript (0).</span><span class="sxs-lookup"><span data-stu-id="62aff-327">JavaScript script column number (0-based).</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="stacktrace"></a> <span data-ttu-id="62aff-328">Trace</span><span class="sxs-lookup"><span data-stu-id="62aff-328">StackTrace</span></span> `object`

<span data-ttu-id="62aff-329">Trames d’appel pour les affirmations ou messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="62aff-329">Call frames for assertions or error messages.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="62aff-330">Propriétés</span><span class="sxs-lookup"><span data-stu-id="62aff-330">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="62aff-331">description</span><span class="sxs-lookup"><span data-stu-id="62aff-331">description</span></span> <br/> <i><span data-ttu-id="62aff-332">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-332">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="62aff-333">Étiquette de chaîne de cette trace de pile.</span><span class="sxs-lookup"><span data-stu-id="62aff-333">String label of this stack trace.</span></span> <span data-ttu-id="62aff-334">Pour les traces Async, il s’agit du nom de la fonction qui a déclenché l’appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="62aff-334">For async traces this may be a name of the function that initiated the async call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-335">callFrames</span><span class="sxs-lookup"><span data-stu-id="62aff-335">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="62aff-336">Nom de la fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="62aff-336">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="62aff-337">dernier</span><span class="sxs-lookup"><span data-stu-id="62aff-337">parent</span></span> <br/> <i><span data-ttu-id="62aff-338">facultatif</span><span class="sxs-lookup"><span data-stu-id="62aff-338">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="62aff-339">Trace de pile JavaScript asynchrone qui précède cette pile, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="62aff-339">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span></td>
        </tr>
    </tbody>
</table>

---
