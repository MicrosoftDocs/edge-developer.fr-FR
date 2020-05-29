---
title: Référence d’événement de chronologie
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: e5f0807204877ce034fd52ea4535795ea80ba394
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611719"
---
<!-- Copyright Meggin Kearney and Flavio Copes

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="dbb30-103">Référence d’événement de chronologie</span><span class="sxs-lookup"><span data-stu-id="dbb30-103">Timeline Event Reference</span></span>   




<span data-ttu-id="dbb30-104">Le mode événements de chronologie affiche tous les événements déclenchés lors de la création d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="dbb30-104">The timeline events mode displays all events triggered while making a recording.</span></span>  <span data-ttu-id="dbb30-105">Utilisez la référence d’événement Timeline pour en savoir plus sur chaque type d’événement de chronologie.</span><span class="sxs-lookup"><span data-stu-id="dbb30-105">Use the timeline event reference to learn more about each timeline event type.</span></span>  

## <span data-ttu-id="dbb30-106">Propriétés d’événement de barre de Planning courantes</span><span class="sxs-lookup"><span data-stu-id="dbb30-106">Common timeline event properties</span></span>  

<span data-ttu-id="dbb30-107">Certains détails sont présents dans les événements de tous les types, mais certains s’appliquent uniquement à certains types d’événements.</span><span class="sxs-lookup"><span data-stu-id="dbb30-107">Certain details are present in events of all types, while some only apply to certain event types.</span></span>  <span data-ttu-id="dbb30-108">Cette section répertorie les propriétés communes aux différents types d’événements.</span><span class="sxs-lookup"><span data-stu-id="dbb30-108">This section lists properties common to different event types.</span></span>  <span data-ttu-id="dbb30-109">Les propriétés spécifiques à certains types d’événements sont répertoriées dans les références pour les types d’événements suivants.</span><span class="sxs-lookup"><span data-stu-id="dbb30-109">Properties specific to certain event types are listed in the references for those event types that follow.</span></span>  

| <span data-ttu-id="dbb30-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="dbb30-110">Property</span></span> | <span data-ttu-id="dbb30-111">Quand est-il affiché?</span><span class="sxs-lookup"><span data-stu-id="dbb30-111">When is it shown</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="dbb30-112">Temps agrégé</span><span class="sxs-lookup"><span data-stu-id="dbb30-112">Aggregated time</span></span> | <span data-ttu-id="dbb30-113">Pour les événements comportant des **événements imbriqués**, durée de chaque catégorie d’événements.</span><span class="sxs-lookup"><span data-stu-id="dbb30-113">For events with **nested events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="dbb30-114">Pile d’appels</span><span class="sxs-lookup"><span data-stu-id="dbb30-114">Call Stack</span></span> | <span data-ttu-id="dbb30-115">Pour les événements avec des **événements enfants**, temps pris par chaque catégorie d’événements.</span><span class="sxs-lookup"><span data-stu-id="dbb30-115">For events with **child events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="dbb30-116">Temps UC</span><span class="sxs-lookup"><span data-stu-id="dbb30-116">CPU time</span></span> | <span data-ttu-id="dbb30-117">Combien de temps processeur l’événement enregistré a duré.</span><span class="sxs-lookup"><span data-stu-id="dbb30-117">How much CPU time the recorded event took.</span></span> |  
| <span data-ttu-id="dbb30-118">Détails</span><span class="sxs-lookup"><span data-stu-id="dbb30-118">Details</span></span> | <span data-ttu-id="dbb30-119">Autres détails sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="dbb30-119">Other details about the event.</span></span> |  
| <span data-ttu-id="dbb30-120">Durée \ (au moment de l’horodatage \)</span><span class="sxs-lookup"><span data-stu-id="dbb30-120">Duration \(at time-stamp\)</span></span> | <span data-ttu-id="dbb30-121">Temps pendant lequel l’événement a duré l’ensemble de ses enfants; horodatage est l’heure à laquelle l’événement s’est produit, par rapport à la date de début de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="dbb30-121">How long it took the event with all of its children to complete; timestamp is the time at which the event occurred, relative to when the recording started.</span></span> |  
| <span data-ttu-id="dbb30-122">Temps libre</span><span class="sxs-lookup"><span data-stu-id="dbb30-122">Self time</span></span> | <span data-ttu-id="dbb30-123">Durée pendant laquelle l’événement a duré sans ses enfants.</span><span class="sxs-lookup"><span data-stu-id="dbb30-123">How long the event took without any of its children.</span></span> |  
| <span data-ttu-id="dbb30-124">Taille du tas utilisée</span><span class="sxs-lookup"><span data-stu-id="dbb30-124">Used Heap Size</span></span> | <span data-ttu-id="dbb30-125">La quantité de mémoire utilisée par l’application lorsque l’événement a été enregistré et que le delta \ (+/--\) change en taille de segment utilisée depuis le dernier échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="dbb30-125">Amount of memory being used by the application when the event was recorded, and the delta \(+/-\) change in used heap size since the last sampling.</span></span> |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <span data-ttu-id="dbb30-126">Chargement des événements</span><span class="sxs-lookup"><span data-stu-id="dbb30-126">Loading events</span></span>  

<span data-ttu-id="dbb30-127">Cette section répertorie les événements qui appartiennent au chargement d’une catégorie et leurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="dbb30-127">This section lists events that belong to Loading category and their properties.</span></span>  

| <span data-ttu-id="dbb30-128">Événement</span><span class="sxs-lookup"><span data-stu-id="dbb30-128">Event</span></span> | <span data-ttu-id="dbb30-129">Description</span><span class="sxs-lookup"><span data-stu-id="dbb30-129">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="dbb30-130">Analyser le code HTML</span><span class="sxs-lookup"><span data-stu-id="dbb30-130">Parse HTML</span></span> |  <span data-ttu-id="dbb30-131">Microsoft Edge a exécuté l’algorithme d’analyse HTML.</span><span class="sxs-lookup"><span data-stu-id="dbb30-131">Microsoft Edge ran the HTML parsing algorithm.</span></span> |  
| <span data-ttu-id="dbb30-132">Fin du chargement</span><span class="sxs-lookup"><span data-stu-id="dbb30-132">Finish Loading</span></span> |  <span data-ttu-id="dbb30-133">Demande réseau terminée.</span><span class="sxs-lookup"><span data-stu-id="dbb30-133">A network request completed.</span></span> |  
| <span data-ttu-id="dbb30-134">Recevoir des données</span><span class="sxs-lookup"><span data-stu-id="dbb30-134">Receive Data</span></span> |  <span data-ttu-id="dbb30-135">Les données d’une demande ont été reçues.</span><span class="sxs-lookup"><span data-stu-id="dbb30-135">Data for a request was received.</span></span>  <span data-ttu-id="dbb30-136">Il existe un ou plusieurs événements de données de réception.</span><span class="sxs-lookup"><span data-stu-id="dbb30-136">There are one or more Receive Data events.</span></span> |  
| <span data-ttu-id="dbb30-137">Recevoir une réponse</span><span class="sxs-lookup"><span data-stu-id="dbb30-137">Receive Response</span></span> |  <span data-ttu-id="dbb30-138">La réponse HTTP initiale d’une demande.</span><span class="sxs-lookup"><span data-stu-id="dbb30-138">The initial HTTP response from a request.</span></span> |  
| <span data-ttu-id="dbb30-139">Envoyer la demande</span><span class="sxs-lookup"><span data-stu-id="dbb30-139">Send Request</span></span> |  <span data-ttu-id="dbb30-140">Une demande de réseau a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="dbb30-140">A network request has been sent.</span></span> |  

### <span data-ttu-id="dbb30-141">Chargement des propriétés d’événement</span><span class="sxs-lookup"><span data-stu-id="dbb30-141">Loading event properties</span></span>  

| <span data-ttu-id="dbb30-142">Propriété</span><span class="sxs-lookup"><span data-stu-id="dbb30-142">Property</span></span> | <span data-ttu-id="dbb30-143">Description</span><span class="sxs-lookup"><span data-stu-id="dbb30-143">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="dbb30-144">Ressource</span><span class="sxs-lookup"><span data-stu-id="dbb30-144">Resource</span></span> | <span data-ttu-id="dbb30-145">URL de la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="dbb30-145">The URL of the requested resource.</span></span> |  
| <span data-ttu-id="dbb30-146">Preview</span><span class="sxs-lookup"><span data-stu-id="dbb30-146">Preview</span></span> | <span data-ttu-id="dbb30-147">Préversion de la ressource demandée (images uniquement \).</span><span class="sxs-lookup"><span data-stu-id="dbb30-147">Preview of the requested resource \(images only\).</span></span> |  
| <span data-ttu-id="dbb30-148">Méthode de requête</span><span class="sxs-lookup"><span data-stu-id="dbb30-148">Request Method</span></span> | <span data-ttu-id="dbb30-149">Méthode HTTP utilisée pour la requête ( `GET` ou `POST` , par exemple).</span><span class="sxs-lookup"><span data-stu-id="dbb30-149">HTTP method used for the request \(`GET` or `POST`, for example\).</span></span> |  
| <span data-ttu-id="dbb30-150">Code d’État</span><span class="sxs-lookup"><span data-stu-id="dbb30-150">Status Code</span></span> | <span data-ttu-id="dbb30-151">Code de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="dbb30-151">HTTP response code.</span></span> |  
| <span data-ttu-id="dbb30-152">Type MIME</span><span class="sxs-lookup"><span data-stu-id="dbb30-152">MIME Type</span></span> | <span data-ttu-id="dbb30-153">Type MIME de la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="dbb30-153">MIME type of the requested resource.</span></span> |  
| <span data-ttu-id="dbb30-154">Longueur des données codées</span><span class="sxs-lookup"><span data-stu-id="dbb30-154">Encoded Data Length</span></span> | <span data-ttu-id="dbb30-155">Durée de la ressource demandée en octets.</span><span class="sxs-lookup"><span data-stu-id="dbb30-155">Length of requested resource in bytes.</span></span> |  

## <span data-ttu-id="dbb30-156">Événements de script</span><span class="sxs-lookup"><span data-stu-id="dbb30-156">Scripting events</span></span>  

<span data-ttu-id="dbb30-157">Cette section répertorie les événements qui appartiennent à la catégorie script et leurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="dbb30-157">This section lists events that belong to the Scripting category and their properties.</span></span>  

| <span data-ttu-id="dbb30-158">Événement</span><span class="sxs-lookup"><span data-stu-id="dbb30-158">Event</span></span> | <span data-ttu-id="dbb30-159">Description</span><span class="sxs-lookup"><span data-stu-id="dbb30-159">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="dbb30-160">Cadre d’animation déclenché</span><span class="sxs-lookup"><span data-stu-id="dbb30-160">Animation Frame Fired</span></span> | <span data-ttu-id="dbb30-161">Un cadre d’animation planifié déclenché et son gestionnaire de rappel appelé.</span><span class="sxs-lookup"><span data-stu-id="dbb30-161">A scheduled animation frame fired, and its callback handler invoked.</span></span> |  
| <span data-ttu-id="dbb30-162">Annuler le cadre d’une animation</span><span class="sxs-lookup"><span data-stu-id="dbb30-162">Cancel Animation Frame</span></span> |  <span data-ttu-id="dbb30-163">Un cadre d’animation planifié a été annulé.</span><span class="sxs-lookup"><span data-stu-id="dbb30-163">A scheduled animation frame was canceled.</span></span> |  
| <span data-ttu-id="dbb30-164">Événement GC</span><span class="sxs-lookup"><span data-stu-id="dbb30-164">GC Event</span></span> |  <span data-ttu-id="dbb30-165">Le nettoyage de la mémoire s’est produit.</span><span class="sxs-lookup"><span data-stu-id="dbb30-165">Garbage collection occurred.</span></span> |  
| <span data-ttu-id="dbb30-166">DOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="dbb30-166">DOMContentLoaded</span></span> |  <span data-ttu-id="dbb30-167">L' [événement DOMContentLoaded][MDNWindowDOMContentLoadedEvent] a été déclenché par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="dbb30-167">The [DOMContentLoaded event][MDNWindowDOMContentLoadedEvent] was fired by the browser.</span></span>  <span data-ttu-id="dbb30-168">Cet événement est déclenché lorsque l’ensemble du contenu DOM de la page a été chargé et analysé.</span><span class="sxs-lookup"><span data-stu-id="dbb30-168">This event is fired when all of the page's DOM content has been loaded and parsed.</span></span> |  
| <span data-ttu-id="dbb30-169">Évaluer le script</span><span class="sxs-lookup"><span data-stu-id="dbb30-169">Evaluate Script</span></span> | <span data-ttu-id="dbb30-170">Un script a été évalué.</span><span class="sxs-lookup"><span data-stu-id="dbb30-170">A script was evaluated.</span></span> |  
| <span data-ttu-id="dbb30-171">Événement</span><span class="sxs-lookup"><span data-stu-id="dbb30-171">Event</span></span> | <span data-ttu-id="dbb30-172">Un événement JavaScript (par exemple, `mousedown` ou `key` \).</span><span class="sxs-lookup"><span data-stu-id="dbb30-172">A JavaScript event \(for example, `mousedown`, or `key`\).</span></span> |  
| <span data-ttu-id="dbb30-173">Appel de fonction</span><span class="sxs-lookup"><span data-stu-id="dbb30-173">Function Call</span></span> | <span data-ttu-id="dbb30-174">Un appel de fonction JavaScript de niveau supérieur a été effectué \ (s’affiche uniquement lorsque le navigateur entre dans le moteur JavaScript \).</span><span class="sxs-lookup"><span data-stu-id="dbb30-174">A top-level JavaScript function call was made \(only appears when browser enters JavaScript engine\).</span></span> |  
| <span data-ttu-id="dbb30-175">Minuteur d’installation</span><span class="sxs-lookup"><span data-stu-id="dbb30-175">Install Timer</span></span> | <span data-ttu-id="dbb30-176">Un minuteur a été créé à l’aide de [setInterval ()][MDNWindowOrWorkerGlobalScopeSetInterval] ou [setTimeout ()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span><span class="sxs-lookup"><span data-stu-id="dbb30-176">A timer was created with [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] or [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span></span> |  
| <span data-ttu-id="dbb30-177">Demander une image d’animation</span><span class="sxs-lookup"><span data-stu-id="dbb30-177">Request Animation Frame</span></span> | <span data-ttu-id="dbb30-178">Un `requestAnimationFrame()` appel a programmé une nouvelle image.</span><span class="sxs-lookup"><span data-stu-id="dbb30-178">A `requestAnimationFrame()` call scheduled a new frame.</span></span> |  
| <span data-ttu-id="dbb30-179">Supprimer le minuteur</span><span class="sxs-lookup"><span data-stu-id="dbb30-179">Remove Timer</span></span> | <span data-ttu-id="dbb30-180">Un minuteur créé précédemment a été effacé.</span><span class="sxs-lookup"><span data-stu-id="dbb30-180">A previously created timer was cleared.</span></span> |  
| <span data-ttu-id="dbb30-181">Heure</span><span class="sxs-lookup"><span data-stu-id="dbb30-181">Time</span></span> |  <span data-ttu-id="dbb30-182">Un script appelé [console. Time ()][ConsoleApiTime].</span><span class="sxs-lookup"><span data-stu-id="dbb30-182">A script called [console.time()][ConsoleApiTime].</span></span> |  
| <span data-ttu-id="dbb30-183">Heure de fin</span><span class="sxs-lookup"><span data-stu-id="dbb30-183">Time End</span></span> | <span data-ttu-id="dbb30-184">Un script appelé [console. timeEnd ()][ConsoleApiTimeEnd].</span><span class="sxs-lookup"><span data-stu-id="dbb30-184">A script called [console.timeEnd()][ConsoleApiTimeEnd].</span></span> |  
| <span data-ttu-id="dbb30-185">Minuteur déclenché</span><span class="sxs-lookup"><span data-stu-id="dbb30-185">Timer Fired</span></span> | <span data-ttu-id="dbb30-186">Un minuteur déclenché qui était programmé avec `setInterval()` ou `setTimeout()` .</span><span class="sxs-lookup"><span data-stu-id="dbb30-186">A timer fired that was scheduled with `setInterval()` or `setTimeout()`.</span></span> |  
| <span data-ttu-id="dbb30-187">Modification de l’état prêt de XHR</span><span class="sxs-lookup"><span data-stu-id="dbb30-187">XHR Ready State Change</span></span> | <span data-ttu-id="dbb30-188">L’état prêt d’un XMLHTTPRequest a changé.</span><span class="sxs-lookup"><span data-stu-id="dbb30-188">The ready state of an XMLHTTPRequest changed.</span></span> |  
| <span data-ttu-id="dbb30-189">Charge XHR</span><span class="sxs-lookup"><span data-stu-id="dbb30-189">XHR Load</span></span> | <span data-ttu-id="dbb30-190">Un `XMLHTTPRequest` chargement fini.</span><span class="sxs-lookup"><span data-stu-id="dbb30-190">An `XMLHTTPRequest` finished loading.</span></span> |  

### <span data-ttu-id="dbb30-191">Script de propriétés d’événement</span><span class="sxs-lookup"><span data-stu-id="dbb30-191">Scripting event properties</span></span>  

| <span data-ttu-id="dbb30-192">Propriété</span><span class="sxs-lookup"><span data-stu-id="dbb30-192">Property</span></span> | <span data-ttu-id="dbb30-193">Description</span><span class="sxs-lookup"><span data-stu-id="dbb30-193">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="dbb30-194">ID du minuteur</span><span class="sxs-lookup"><span data-stu-id="dbb30-194">Timer ID</span></span> | <span data-ttu-id="dbb30-195">ID du minuteur.</span><span class="sxs-lookup"><span data-stu-id="dbb30-195">The timer ID.</span></span> |  
| <span data-ttu-id="dbb30-196">Délai d’expiration dépassé</span><span class="sxs-lookup"><span data-stu-id="dbb30-196">Timeout</span></span> | <span data-ttu-id="dbb30-197">Délai d’expiration spécifié par le minuteur.</span><span class="sxs-lookup"><span data-stu-id="dbb30-197">The timeout specified by the timer.</span></span> |  
| <span data-ttu-id="dbb30-198">Répète</span><span class="sxs-lookup"><span data-stu-id="dbb30-198">Repeats</span></span> | <span data-ttu-id="dbb30-199">Valeur booléenne qui indique si le minuteur se répète.</span><span class="sxs-lookup"><span data-stu-id="dbb30-199">Boolean that specifies if the timer repeats.</span></span> |  
| <span data-ttu-id="dbb30-200">Appel de fonction</span><span class="sxs-lookup"><span data-stu-id="dbb30-200">Function Call</span></span> | <span data-ttu-id="dbb30-201">Fonction qui a été appelée.</span><span class="sxs-lookup"><span data-stu-id="dbb30-201">A function that was invoked.</span></span> |  

## <span data-ttu-id="dbb30-202">Rendu des événements</span><span class="sxs-lookup"><span data-stu-id="dbb30-202">Rendering events</span></span>  

<span data-ttu-id="dbb30-203">Cette section répertorie les événements qui appartiennent à la catégorie de rendu et leurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="dbb30-203">This section lists events that belong to Rendering category and their properties.</span></span>  

| <span data-ttu-id="dbb30-204">Événement</span><span class="sxs-lookup"><span data-stu-id="dbb30-204">Event</span></span> | <span data-ttu-id="dbb30-205">Description</span><span class="sxs-lookup"><span data-stu-id="dbb30-205">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="dbb30-206">Disposition non valide</span><span class="sxs-lookup"><span data-stu-id="dbb30-206">Invalidate layout</span></span> | <span data-ttu-id="dbb30-207">La mise en page a été invalidée par un changement DOM.</span><span class="sxs-lookup"><span data-stu-id="dbb30-207">The page layout was invalidated by a DOM change.</span></span> |  
| <span data-ttu-id="dbb30-208">Disposition</span><span class="sxs-lookup"><span data-stu-id="dbb30-208">Layout</span></span> | <span data-ttu-id="dbb30-209">Une mise en page a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="dbb30-209">A page layout was completed.</span></span> |  
| <span data-ttu-id="dbb30-210">Recalculer le style</span><span class="sxs-lookup"><span data-stu-id="dbb30-210">Recalculate style</span></span> | <span data-ttu-id="dbb30-211">Styles des éléments recalculés Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dbb30-211">Microsoft Edge recalculated element styles.</span></span> |  
| <span data-ttu-id="dbb30-212">Scroll</span><span class="sxs-lookup"><span data-stu-id="dbb30-212">Scroll</span></span> | <span data-ttu-id="dbb30-213">Le contenu du mode imbriqué a été défilé.</span><span class="sxs-lookup"><span data-stu-id="dbb30-213">The content of nested view was scrolled.</span></span> |  

### <span data-ttu-id="dbb30-214">Affichage des propriétés d’événement</span><span class="sxs-lookup"><span data-stu-id="dbb30-214">Rendering event properties</span></span>  

| <span data-ttu-id="dbb30-215">Propriété</span><span class="sxs-lookup"><span data-stu-id="dbb30-215">Property</span></span> | <span data-ttu-id="dbb30-216">Description</span><span class="sxs-lookup"><span data-stu-id="dbb30-216">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="dbb30-217">Disposition invalidée</span><span class="sxs-lookup"><span data-stu-id="dbb30-217">Layout invalidated</span></span> | <span data-ttu-id="dbb30-218">Pour les enregistrements de disposition, la trace de pile du code ayant entraîné l’invalidation de la disposition.</span><span class="sxs-lookup"><span data-stu-id="dbb30-218">For Layout records, the stack trace of the code that caused the layout to be invalidated.</span></span> |  
| <span data-ttu-id="dbb30-219">Nœuds nécessitant une disposition</span><span class="sxs-lookup"><span data-stu-id="dbb30-219">Nodes that need layout</span></span> | <span data-ttu-id="dbb30-220">Pour les enregistrements de disposition, nombre de nœuds marqués comme ayant besoin d’une disposition avant la redisposition.</span><span class="sxs-lookup"><span data-stu-id="dbb30-220">For Layout records, the number of nodes that were marked as needing layout before the relayout started.</span></span>  <span data-ttu-id="dbb30-221">En règle générale, ces nœuds ont été invalidés par du code de développeur et un chemin d’accès descendant à la racine de réorganisation.</span><span class="sxs-lookup"><span data-stu-id="dbb30-221">These are normally those nodes that were invalidated by developer code, plus a path upward to relayout root.</span></span> |  
| <span data-ttu-id="dbb30-222">Taille de l’arborescence de disposition</span><span class="sxs-lookup"><span data-stu-id="dbb30-222">Layout tree size</span></span> | <span data-ttu-id="dbb30-223">Pour les enregistrements de disposition, le nombre total de nœuds sous la racine de réorganisation \ (le nœud sur lequel Microsoft Edge démarre la redisposition \).</span><span class="sxs-lookup"><span data-stu-id="dbb30-223">For Layout records, the total number of nodes under the relayout root \(the node that Microsoft Edge starts the relayout\).</span></span> |  
| <span data-ttu-id="dbb30-224">Étendue de la disposition</span><span class="sxs-lookup"><span data-stu-id="dbb30-224">Layout scope</span></span> | <span data-ttu-id="dbb30-225">Les valeurs possibles sont `Partial` \ (la limite de nouvelle disposition est une partie du DOM \) ou `Whole document` .</span><span class="sxs-lookup"><span data-stu-id="dbb30-225">Possible values are `Partial` \(the re-layout boundary is a portion of the DOM\) or `Whole document`.</span></span> |  
| <span data-ttu-id="dbb30-226">Éléments affectés</span><span class="sxs-lookup"><span data-stu-id="dbb30-226">Elements affected</span></span> | <span data-ttu-id="dbb30-227">Pour recalculer les enregistrements de style, le nombre d’éléments affectés par un recalcul de style.</span><span class="sxs-lookup"><span data-stu-id="dbb30-227">For Recalculate style records, the number of elements affected by a style recalculation.</span></span> |  
| <span data-ttu-id="dbb30-228">Styles invalidés</span><span class="sxs-lookup"><span data-stu-id="dbb30-228">Styles invalidated</span></span> | <span data-ttu-id="dbb30-229">Pour recalculer les enregistrements de style, fournit la trace de pile du code à l’origine de l’invalidation du style.</span><span class="sxs-lookup"><span data-stu-id="dbb30-229">For Recalculate style records, provides the stack trace of the code that caused the style invalidation.</span></span> |  

## <span data-ttu-id="dbb30-230">Dessin d’événements</span><span class="sxs-lookup"><span data-stu-id="dbb30-230">Painting events</span></span>  

<span data-ttu-id="dbb30-231">Cette section répertorie les événements qui appartiennent à la catégorie Paint et leurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="dbb30-231">This section lists events that belong to Painting category and their properties.</span></span>  

| <span data-ttu-id="dbb30-232">Événement</span><span class="sxs-lookup"><span data-stu-id="dbb30-232">Event</span></span> | <span data-ttu-id="dbb30-233">Description</span><span class="sxs-lookup"><span data-stu-id="dbb30-233">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="dbb30-234">Calques composites</span><span class="sxs-lookup"><span data-stu-id="dbb30-234">Composite Layers</span></span> | <span data-ttu-id="dbb30-235">Couches d’image composites pour le moteur de rendu Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dbb30-235">The composited image layers for the Microsoft Edge rendering engine.</span></span> |  
| <span data-ttu-id="dbb30-236">Décodage d’image</span><span class="sxs-lookup"><span data-stu-id="dbb30-236">Image Decode</span></span> | <span data-ttu-id="dbb30-237">Une ressource d’image a été décodée.</span><span class="sxs-lookup"><span data-stu-id="dbb30-237">An image resource was decoded.</span></span> |  
| <span data-ttu-id="dbb30-238">Redimensionnement de l’image</span><span class="sxs-lookup"><span data-stu-id="dbb30-238">Image Resize</span></span> | <span data-ttu-id="dbb30-239">Une image a été redimensionnée à partir de ses dimensions natives.</span><span class="sxs-lookup"><span data-stu-id="dbb30-239">An image was resized from its native dimensions.</span></span> |  
| <span data-ttu-id="dbb30-240">Paint</span><span class="sxs-lookup"><span data-stu-id="dbb30-240">Paint</span></span> | <span data-ttu-id="dbb30-241">Les couches composites ont été peintes dans une zone de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="dbb30-241">Composited layers were painted to a region of the display.</span></span>  <span data-ttu-id="dbb30-242">Pointez sur un enregistrement de Paint pour mettre en évidence la région de l’affichage mise à jour.</span><span class="sxs-lookup"><span data-stu-id="dbb30-242">Hovering over a Paint record highlights the region of the display that was updated.</span></span> |  

### <span data-ttu-id="dbb30-243">Propriétés d’événement de dessin</span><span class="sxs-lookup"><span data-stu-id="dbb30-243">Painting event properties</span></span>  

| <span data-ttu-id="dbb30-244">Propriété</span><span class="sxs-lookup"><span data-stu-id="dbb30-244">Property</span></span> | <span data-ttu-id="dbb30-245">Description</span><span class="sxs-lookup"><span data-stu-id="dbb30-245">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="dbb30-246">Services de localisation</span><span class="sxs-lookup"><span data-stu-id="dbb30-246">Location</span></span> | <span data-ttu-id="dbb30-247">Pour les événements Paint, les coordonnées x et y du rectangle de peinture.</span><span class="sxs-lookup"><span data-stu-id="dbb30-247">For Paint events, the x and y coordinates of the paint rectangle.</span></span> |  
| <span data-ttu-id="dbb30-248">Analytique</span><span class="sxs-lookup"><span data-stu-id="dbb30-248">Dimensions</span></span> | <span data-ttu-id="dbb30-249">Pour les événements Paint, hauteur et largeur de la zone peinte.</span><span class="sxs-lookup"><span data-stu-id="dbb30-249">For Paint events, the height and width of the painted region.</span></span> |  

 



<!-- image links -->  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "Time-référence d’API de la console"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd-XXXXXXX XXXXXXX xxx xxxxxxxxx"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Fenêtre: événement DOMContentLoaded | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope. setInterval () | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope. setTimeout () | MDN"  

> [!NOTE]
> <span data-ttu-id="dbb30-255">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dbb30-255">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="dbb30-256">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) et est créée par [Meggin Kearney][MegginKearney] \ (Technical Writer \) et [Flavio][FlavioCopes] configure \ (développeur de pile complète \).</span><span class="sxs-lookup"><span data-stu-id="dbb30-256">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Flavio Copes][FlavioCopes] \(Full Stack Developer\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="dbb30-258">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dbb30-258">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
