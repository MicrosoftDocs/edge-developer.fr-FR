---
description: Le mode événements de chronologie affiche tous les événements déclenchés lors de la création d’un enregistrement.  Utilisez la référence d’événement Timeline pour en savoir plus sur chaque type d’événement de chronologie.
title: Référence d’événement de chronologie
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 624035636e2231cf1f3cd1e2ba0fdda7e2e4fa00
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992847"
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





# <span data-ttu-id="38d12-105">Référence d’événement de chronologie</span><span class="sxs-lookup"><span data-stu-id="38d12-105">Timeline Event Reference</span></span>   




<span data-ttu-id="38d12-106">Le mode événements de chronologie affiche tous les événements déclenchés lors de la création d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="38d12-106">The timeline events mode displays all events triggered while making a recording.</span></span>  <span data-ttu-id="38d12-107">Utilisez la référence d’événement Timeline pour en savoir plus sur chaque type d’événement de chronologie.</span><span class="sxs-lookup"><span data-stu-id="38d12-107">Use the timeline event reference to learn more about each timeline event type.</span></span>  

## <span data-ttu-id="38d12-108">Propriétés d’événement de barre de Planning courantes</span><span class="sxs-lookup"><span data-stu-id="38d12-108">Common timeline event properties</span></span>  

<span data-ttu-id="38d12-109">Certains détails sont présents dans les événements de tous les types, mais certains s’appliquent uniquement à certains types d’événements.</span><span class="sxs-lookup"><span data-stu-id="38d12-109">Certain details are present in events of all types, while some only apply to certain event types.</span></span>  <span data-ttu-id="38d12-110">Cette section répertorie les propriétés communes aux différents types d’événements.</span><span class="sxs-lookup"><span data-stu-id="38d12-110">This section lists properties common to different event types.</span></span>  <span data-ttu-id="38d12-111">Les propriétés spécifiques à certains types d’événements sont répertoriées dans les références pour les types d’événements suivants.</span><span class="sxs-lookup"><span data-stu-id="38d12-111">Properties specific to certain event types are listed in the references for those event types that follow.</span></span>  

| <span data-ttu-id="38d12-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="38d12-112">Property</span></span> | <span data-ttu-id="38d12-113">Quand est-il affiché?</span><span class="sxs-lookup"><span data-stu-id="38d12-113">When is it shown</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="38d12-114">Temps agrégé</span><span class="sxs-lookup"><span data-stu-id="38d12-114">Aggregated time</span></span> | <span data-ttu-id="38d12-115">Pour les événements comportant des **événements imbriqués**, durée de chaque catégorie d’événements.</span><span class="sxs-lookup"><span data-stu-id="38d12-115">For events with **nested events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="38d12-116">Pile d’appels</span><span class="sxs-lookup"><span data-stu-id="38d12-116">Call Stack</span></span> | <span data-ttu-id="38d12-117">Pour les événements avec des **événements enfants**, temps pris par chaque catégorie d’événements.</span><span class="sxs-lookup"><span data-stu-id="38d12-117">For events with **child events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="38d12-118">Temps UC</span><span class="sxs-lookup"><span data-stu-id="38d12-118">CPU time</span></span> | <span data-ttu-id="38d12-119">Combien de temps processeur l’événement enregistré a duré.</span><span class="sxs-lookup"><span data-stu-id="38d12-119">How much CPU time the recorded event took.</span></span> |  
| <span data-ttu-id="38d12-120">Détails</span><span class="sxs-lookup"><span data-stu-id="38d12-120">Details</span></span> | <span data-ttu-id="38d12-121">Autres détails sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="38d12-121">Other details about the event.</span></span> |  
| <span data-ttu-id="38d12-122">Durée \ (au moment de l’horodatage \)</span><span class="sxs-lookup"><span data-stu-id="38d12-122">Duration \(at time-stamp\)</span></span> | <span data-ttu-id="38d12-123">Temps pendant lequel l’événement a duré l’ensemble de ses enfants; horodatage est l’heure à laquelle l’événement s’est produit, par rapport à la date de début de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="38d12-123">How long it took the event with all of its children to complete; timestamp is the time at which the event occurred, relative to when the recording started.</span></span> |  
| <span data-ttu-id="38d12-124">Temps libre</span><span class="sxs-lookup"><span data-stu-id="38d12-124">Self time</span></span> | <span data-ttu-id="38d12-125">Durée pendant laquelle l’événement a duré sans ses enfants.</span><span class="sxs-lookup"><span data-stu-id="38d12-125">How long the event took without any of its children.</span></span> |  
| <span data-ttu-id="38d12-126">Taille du tas utilisée</span><span class="sxs-lookup"><span data-stu-id="38d12-126">Used Heap Size</span></span> | <span data-ttu-id="38d12-127">La quantité de mémoire utilisée par l’application lorsque l’événement a été enregistré et que le delta \ (+/--\) change en taille de segment utilisée depuis le dernier échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="38d12-127">Amount of memory being used by the application when the event was recorded, and the delta \(+/-\) change in used heap size since the last sampling.</span></span> |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <span data-ttu-id="38d12-128">Chargement des événements</span><span class="sxs-lookup"><span data-stu-id="38d12-128">Loading events</span></span>  

<span data-ttu-id="38d12-129">Cette section répertorie les événements qui appartiennent au chargement d’une catégorie et leurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="38d12-129">This section lists events that belong to Loading category and their properties.</span></span>  

| <span data-ttu-id="38d12-130">Événement</span><span class="sxs-lookup"><span data-stu-id="38d12-130">Event</span></span> | <span data-ttu-id="38d12-131">Description</span><span class="sxs-lookup"><span data-stu-id="38d12-131">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="38d12-132">Analyser le code HTML</span><span class="sxs-lookup"><span data-stu-id="38d12-132">Parse HTML</span></span> |  <span data-ttu-id="38d12-133">Microsoft Edge a exécuté l’algorithme d’analyse HTML.</span><span class="sxs-lookup"><span data-stu-id="38d12-133">Microsoft Edge ran the HTML parsing algorithm.</span></span> |  
| <span data-ttu-id="38d12-134">Fin du chargement</span><span class="sxs-lookup"><span data-stu-id="38d12-134">Finish Loading</span></span> |  <span data-ttu-id="38d12-135">Demande réseau terminée.</span><span class="sxs-lookup"><span data-stu-id="38d12-135">A network request completed.</span></span> |  
| <span data-ttu-id="38d12-136">Recevoir des données</span><span class="sxs-lookup"><span data-stu-id="38d12-136">Receive Data</span></span> |  <span data-ttu-id="38d12-137">Les données d’une demande ont été reçues.</span><span class="sxs-lookup"><span data-stu-id="38d12-137">Data for a request was received.</span></span>  <span data-ttu-id="38d12-138">Il existe un ou plusieurs événements de données de réception.</span><span class="sxs-lookup"><span data-stu-id="38d12-138">There are one or more Receive Data events.</span></span> |  
| <span data-ttu-id="38d12-139">Recevoir une réponse</span><span class="sxs-lookup"><span data-stu-id="38d12-139">Receive Response</span></span> |  <span data-ttu-id="38d12-140">La réponse HTTP initiale d’une demande.</span><span class="sxs-lookup"><span data-stu-id="38d12-140">The initial HTTP response from a request.</span></span> |  
| <span data-ttu-id="38d12-141">Envoyer la demande</span><span class="sxs-lookup"><span data-stu-id="38d12-141">Send Request</span></span> |  <span data-ttu-id="38d12-142">Une demande de réseau a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="38d12-142">A network request has been sent.</span></span> |  

### <span data-ttu-id="38d12-143">Chargement des propriétés d’événement</span><span class="sxs-lookup"><span data-stu-id="38d12-143">Loading event properties</span></span>  

| <span data-ttu-id="38d12-144">Propriété</span><span class="sxs-lookup"><span data-stu-id="38d12-144">Property</span></span> | <span data-ttu-id="38d12-145">Description</span><span class="sxs-lookup"><span data-stu-id="38d12-145">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="38d12-146">Ressource</span><span class="sxs-lookup"><span data-stu-id="38d12-146">Resource</span></span> | <span data-ttu-id="38d12-147">URL de la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="38d12-147">The URL of the requested resource.</span></span> |  
| <span data-ttu-id="38d12-148">Preview</span><span class="sxs-lookup"><span data-stu-id="38d12-148">Preview</span></span> | <span data-ttu-id="38d12-149">Préversion de la ressource demandée (images uniquement \).</span><span class="sxs-lookup"><span data-stu-id="38d12-149">Preview of the requested resource \(images only\).</span></span> |  
| <span data-ttu-id="38d12-150">Méthode de requête</span><span class="sxs-lookup"><span data-stu-id="38d12-150">Request Method</span></span> | <span data-ttu-id="38d12-151">Méthode HTTP utilisée pour la requête ( `GET` ou `POST` , par exemple).</span><span class="sxs-lookup"><span data-stu-id="38d12-151">HTTP method used for the request \(`GET` or `POST`, for example\).</span></span> |  
| <span data-ttu-id="38d12-152">Code d’État</span><span class="sxs-lookup"><span data-stu-id="38d12-152">Status Code</span></span> | <span data-ttu-id="38d12-153">Code de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="38d12-153">HTTP response code.</span></span> |  
| <span data-ttu-id="38d12-154">Type MIME</span><span class="sxs-lookup"><span data-stu-id="38d12-154">MIME Type</span></span> | <span data-ttu-id="38d12-155">Type MIME de la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="38d12-155">MIME type of the requested resource.</span></span> |  
| <span data-ttu-id="38d12-156">Longueur des données codées</span><span class="sxs-lookup"><span data-stu-id="38d12-156">Encoded Data Length</span></span> | <span data-ttu-id="38d12-157">Durée de la ressource demandée en octets.</span><span class="sxs-lookup"><span data-stu-id="38d12-157">Length of requested resource in bytes.</span></span> |  

## <span data-ttu-id="38d12-158">Événements de script</span><span class="sxs-lookup"><span data-stu-id="38d12-158">Scripting events</span></span>  

<span data-ttu-id="38d12-159">Cette section répertorie les événements qui appartiennent à la catégorie script et leurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="38d12-159">This section lists events that belong to the Scripting category and their properties.</span></span>  

| <span data-ttu-id="38d12-160">Événement</span><span class="sxs-lookup"><span data-stu-id="38d12-160">Event</span></span> | <span data-ttu-id="38d12-161">Description</span><span class="sxs-lookup"><span data-stu-id="38d12-161">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="38d12-162">Cadre d’animation déclenché</span><span class="sxs-lookup"><span data-stu-id="38d12-162">Animation Frame Fired</span></span> | <span data-ttu-id="38d12-163">Un cadre d’animation planifié déclenché et son gestionnaire de rappel appelé.</span><span class="sxs-lookup"><span data-stu-id="38d12-163">A scheduled animation frame fired, and its callback handler invoked.</span></span> |  
| <span data-ttu-id="38d12-164">Annuler le cadre d’une animation</span><span class="sxs-lookup"><span data-stu-id="38d12-164">Cancel Animation Frame</span></span> |  <span data-ttu-id="38d12-165">Un cadre d’animation planifié a été annulé.</span><span class="sxs-lookup"><span data-stu-id="38d12-165">A scheduled animation frame was canceled.</span></span> |  
| <span data-ttu-id="38d12-166">Événement GC</span><span class="sxs-lookup"><span data-stu-id="38d12-166">GC Event</span></span> |  <span data-ttu-id="38d12-167">Le nettoyage de la mémoire s’est produit.</span><span class="sxs-lookup"><span data-stu-id="38d12-167">Garbage collection occurred.</span></span> |  
| <span data-ttu-id="38d12-168">DOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="38d12-168">DOMContentLoaded</span></span> |  <span data-ttu-id="38d12-169">L' [événement DOMContentLoaded][MDNWindowDOMContentLoadedEvent] a été déclenché par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="38d12-169">The [DOMContentLoaded event][MDNWindowDOMContentLoadedEvent] was fired by the browser.</span></span>  <span data-ttu-id="38d12-170">Cet événement est déclenché lorsque l’ensemble du contenu DOM de la page a été chargé et analysé.</span><span class="sxs-lookup"><span data-stu-id="38d12-170">This event is fired when all of the page's DOM content has been loaded and parsed.</span></span> |  
| <span data-ttu-id="38d12-171">Évaluer le script</span><span class="sxs-lookup"><span data-stu-id="38d12-171">Evaluate Script</span></span> | <span data-ttu-id="38d12-172">Un script a été évalué.</span><span class="sxs-lookup"><span data-stu-id="38d12-172">A script was evaluated.</span></span> |  
| <span data-ttu-id="38d12-173">Événement</span><span class="sxs-lookup"><span data-stu-id="38d12-173">Event</span></span> | <span data-ttu-id="38d12-174">Un événement JavaScript (par exemple, `mousedown` ou `key` \).</span><span class="sxs-lookup"><span data-stu-id="38d12-174">A JavaScript event \(for example, `mousedown`, or `key`\).</span></span> |  
| <span data-ttu-id="38d12-175">Appel de fonction</span><span class="sxs-lookup"><span data-stu-id="38d12-175">Function Call</span></span> | <span data-ttu-id="38d12-176">Un appel de fonction JavaScript de niveau supérieur a été effectué \ (s’affiche uniquement lorsque le navigateur entre dans le moteur JavaScript \).</span><span class="sxs-lookup"><span data-stu-id="38d12-176">A top-level JavaScript function call was made \(only appears when browser enters JavaScript engine\).</span></span> |  
| <span data-ttu-id="38d12-177">Minuteur d’installation</span><span class="sxs-lookup"><span data-stu-id="38d12-177">Install Timer</span></span> | <span data-ttu-id="38d12-178">Un minuteur a été créé à l’aide de [setInterval ()][MDNWindowOrWorkerGlobalScopeSetInterval] ou [setTimeout ()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span><span class="sxs-lookup"><span data-stu-id="38d12-178">A timer was created with [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] or [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span></span> |  
| <span data-ttu-id="38d12-179">Demander une image d’animation</span><span class="sxs-lookup"><span data-stu-id="38d12-179">Request Animation Frame</span></span> | <span data-ttu-id="38d12-180">Un `requestAnimationFrame()` appel a programmé une nouvelle image.</span><span class="sxs-lookup"><span data-stu-id="38d12-180">A `requestAnimationFrame()` call scheduled a new frame.</span></span> |  
| <span data-ttu-id="38d12-181">Supprimer le minuteur</span><span class="sxs-lookup"><span data-stu-id="38d12-181">Remove Timer</span></span> | <span data-ttu-id="38d12-182">Un minuteur créé précédemment a été effacé.</span><span class="sxs-lookup"><span data-stu-id="38d12-182">A previously created timer was cleared.</span></span> |  
| <span data-ttu-id="38d12-183">Heure</span><span class="sxs-lookup"><span data-stu-id="38d12-183">Time</span></span> |  <span data-ttu-id="38d12-184">Un script appelé [console. Time ()][ConsoleApiTime].</span><span class="sxs-lookup"><span data-stu-id="38d12-184">A script called [console.time()][ConsoleApiTime].</span></span> |  
| <span data-ttu-id="38d12-185">Heure de fin</span><span class="sxs-lookup"><span data-stu-id="38d12-185">Time End</span></span> | <span data-ttu-id="38d12-186">Un script appelé [console. timeEnd ()][ConsoleApiTimeEnd].</span><span class="sxs-lookup"><span data-stu-id="38d12-186">A script called [console.timeEnd()][ConsoleApiTimeEnd].</span></span> |  
| <span data-ttu-id="38d12-187">Minuteur déclenché</span><span class="sxs-lookup"><span data-stu-id="38d12-187">Timer Fired</span></span> | <span data-ttu-id="38d12-188">Un minuteur déclenché qui était programmé avec `setInterval()` ou `setTimeout()` .</span><span class="sxs-lookup"><span data-stu-id="38d12-188">A timer fired that was scheduled with `setInterval()` or `setTimeout()`.</span></span> |  
| <span data-ttu-id="38d12-189">Modification de l’état prêt de XHR</span><span class="sxs-lookup"><span data-stu-id="38d12-189">XHR Ready State Change</span></span> | <span data-ttu-id="38d12-190">L’état prêt d’un XMLHTTPRequest a changé.</span><span class="sxs-lookup"><span data-stu-id="38d12-190">The ready state of an XMLHTTPRequest changed.</span></span> |  
| <span data-ttu-id="38d12-191">Charge XHR</span><span class="sxs-lookup"><span data-stu-id="38d12-191">XHR Load</span></span> | <span data-ttu-id="38d12-192">Un `XMLHTTPRequest` chargement fini.</span><span class="sxs-lookup"><span data-stu-id="38d12-192">An `XMLHTTPRequest` finished loading.</span></span> |  

### <span data-ttu-id="38d12-193">Script de propriétés d’événement</span><span class="sxs-lookup"><span data-stu-id="38d12-193">Scripting event properties</span></span>  

| <span data-ttu-id="38d12-194">Propriété</span><span class="sxs-lookup"><span data-stu-id="38d12-194">Property</span></span> | <span data-ttu-id="38d12-195">Description</span><span class="sxs-lookup"><span data-stu-id="38d12-195">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="38d12-196">ID du minuteur</span><span class="sxs-lookup"><span data-stu-id="38d12-196">Timer ID</span></span> | <span data-ttu-id="38d12-197">ID du minuteur.</span><span class="sxs-lookup"><span data-stu-id="38d12-197">The timer ID.</span></span> |  
| <span data-ttu-id="38d12-198">Délai d’expiration dépassé</span><span class="sxs-lookup"><span data-stu-id="38d12-198">Timeout</span></span> | <span data-ttu-id="38d12-199">Délai d’expiration spécifié par le minuteur.</span><span class="sxs-lookup"><span data-stu-id="38d12-199">The timeout specified by the timer.</span></span> |  
| <span data-ttu-id="38d12-200">Répète</span><span class="sxs-lookup"><span data-stu-id="38d12-200">Repeats</span></span> | <span data-ttu-id="38d12-201">Valeur booléenne qui indique si le minuteur se répète.</span><span class="sxs-lookup"><span data-stu-id="38d12-201">Boolean that specifies if the timer repeats.</span></span> |  
| <span data-ttu-id="38d12-202">Appel de fonction</span><span class="sxs-lookup"><span data-stu-id="38d12-202">Function Call</span></span> | <span data-ttu-id="38d12-203">Fonction qui a été appelée.</span><span class="sxs-lookup"><span data-stu-id="38d12-203">A function that was invoked.</span></span> |  

## <span data-ttu-id="38d12-204">Rendu des événements</span><span class="sxs-lookup"><span data-stu-id="38d12-204">Rendering events</span></span>  

<span data-ttu-id="38d12-205">Cette section répertorie les événements qui appartiennent à la catégorie de rendu et leurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="38d12-205">This section lists events that belong to Rendering category and their properties.</span></span>  

| <span data-ttu-id="38d12-206">Événement</span><span class="sxs-lookup"><span data-stu-id="38d12-206">Event</span></span> | <span data-ttu-id="38d12-207">Description</span><span class="sxs-lookup"><span data-stu-id="38d12-207">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="38d12-208">Disposition non valide</span><span class="sxs-lookup"><span data-stu-id="38d12-208">Invalidate layout</span></span> | <span data-ttu-id="38d12-209">La mise en page a été invalidée par un changement DOM.</span><span class="sxs-lookup"><span data-stu-id="38d12-209">The page layout was invalidated by a DOM change.</span></span> |  
| <span data-ttu-id="38d12-210">Disposition</span><span class="sxs-lookup"><span data-stu-id="38d12-210">Layout</span></span> | <span data-ttu-id="38d12-211">Une mise en page a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="38d12-211">A page layout was completed.</span></span> |  
| <span data-ttu-id="38d12-212">Recalculer le style</span><span class="sxs-lookup"><span data-stu-id="38d12-212">Recalculate style</span></span> | <span data-ttu-id="38d12-213">Styles des éléments recalculés Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="38d12-213">Microsoft Edge recalculated element styles.</span></span> |  
| <span data-ttu-id="38d12-214">Scroll</span><span class="sxs-lookup"><span data-stu-id="38d12-214">Scroll</span></span> | <span data-ttu-id="38d12-215">Le contenu du mode imbriqué a été défilé.</span><span class="sxs-lookup"><span data-stu-id="38d12-215">The content of nested view was scrolled.</span></span> |  

### <span data-ttu-id="38d12-216">Affichage des propriétés d’événement</span><span class="sxs-lookup"><span data-stu-id="38d12-216">Rendering event properties</span></span>  

| <span data-ttu-id="38d12-217">Propriété</span><span class="sxs-lookup"><span data-stu-id="38d12-217">Property</span></span> | <span data-ttu-id="38d12-218">Description</span><span class="sxs-lookup"><span data-stu-id="38d12-218">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="38d12-219">Disposition invalidée</span><span class="sxs-lookup"><span data-stu-id="38d12-219">Layout invalidated</span></span> | <span data-ttu-id="38d12-220">Pour les enregistrements de disposition, la trace de pile du code ayant entraîné l’invalidation de la disposition.</span><span class="sxs-lookup"><span data-stu-id="38d12-220">For Layout records, the stack trace of the code that caused the layout to be invalidated.</span></span> |  
| <span data-ttu-id="38d12-221">Nœuds nécessitant une disposition</span><span class="sxs-lookup"><span data-stu-id="38d12-221">Nodes that need layout</span></span> | <span data-ttu-id="38d12-222">Pour les enregistrements de disposition, nombre de nœuds marqués comme ayant besoin d’une disposition avant la redisposition.</span><span class="sxs-lookup"><span data-stu-id="38d12-222">For Layout records, the number of nodes that were marked as needing layout before the relayout started.</span></span>  <span data-ttu-id="38d12-223">En règle générale, ces nœuds ont été invalidés par du code de développeur et un chemin d’accès descendant à la racine de réorganisation.</span><span class="sxs-lookup"><span data-stu-id="38d12-223">These are normally those nodes that were invalidated by developer code, plus a path upward to relayout root.</span></span> |  
| <span data-ttu-id="38d12-224">Taille de l’arborescence de disposition</span><span class="sxs-lookup"><span data-stu-id="38d12-224">Layout tree size</span></span> | <span data-ttu-id="38d12-225">Pour les enregistrements de disposition, le nombre total de nœuds sous la racine de réorganisation \ (le nœud sur lequel Microsoft Edge démarre la redisposition \).</span><span class="sxs-lookup"><span data-stu-id="38d12-225">For Layout records, the total number of nodes under the relayout root \(the node that Microsoft Edge starts the relayout\).</span></span> |  
| <span data-ttu-id="38d12-226">Étendue de la disposition</span><span class="sxs-lookup"><span data-stu-id="38d12-226">Layout scope</span></span> | <span data-ttu-id="38d12-227">Les valeurs possibles sont `Partial` \ (la limite de nouvelle disposition est une partie du DOM \) ou `Whole document` .</span><span class="sxs-lookup"><span data-stu-id="38d12-227">Possible values are `Partial` \(the re-layout boundary is a portion of the DOM\) or `Whole document`.</span></span> |  
| <span data-ttu-id="38d12-228">Éléments affectés</span><span class="sxs-lookup"><span data-stu-id="38d12-228">Elements affected</span></span> | <span data-ttu-id="38d12-229">Pour recalculer les enregistrements de style, le nombre d’éléments affectés par un recalcul de style.</span><span class="sxs-lookup"><span data-stu-id="38d12-229">For Recalculate style records, the number of elements affected by a style recalculation.</span></span> |  
| <span data-ttu-id="38d12-230">Styles invalidés</span><span class="sxs-lookup"><span data-stu-id="38d12-230">Styles invalidated</span></span> | <span data-ttu-id="38d12-231">Pour recalculer les enregistrements de style, fournit la trace de pile du code à l’origine de l’invalidation du style.</span><span class="sxs-lookup"><span data-stu-id="38d12-231">For Recalculate style records, provides the stack trace of the code that caused the style invalidation.</span></span> |  

## <span data-ttu-id="38d12-232">Dessin d’événements</span><span class="sxs-lookup"><span data-stu-id="38d12-232">Painting events</span></span>  

<span data-ttu-id="38d12-233">Cette section répertorie les événements qui appartiennent à la catégorie Paint et leurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="38d12-233">This section lists events that belong to Painting category and their properties.</span></span>  

| <span data-ttu-id="38d12-234">Événement</span><span class="sxs-lookup"><span data-stu-id="38d12-234">Event</span></span> | <span data-ttu-id="38d12-235">Description</span><span class="sxs-lookup"><span data-stu-id="38d12-235">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="38d12-236">Calques composites</span><span class="sxs-lookup"><span data-stu-id="38d12-236">Composite Layers</span></span> | <span data-ttu-id="38d12-237">Couches d’image composites pour le moteur de rendu Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="38d12-237">The composited image layers for the Microsoft Edge rendering engine.</span></span> |  
| <span data-ttu-id="38d12-238">Décodage d’image</span><span class="sxs-lookup"><span data-stu-id="38d12-238">Image Decode</span></span> | <span data-ttu-id="38d12-239">Une ressource d’image a été décodée.</span><span class="sxs-lookup"><span data-stu-id="38d12-239">An image resource was decoded.</span></span> |  
| <span data-ttu-id="38d12-240">Redimensionnement de l’image</span><span class="sxs-lookup"><span data-stu-id="38d12-240">Image Resize</span></span> | <span data-ttu-id="38d12-241">Une image a été redimensionnée à partir de ses dimensions natives.</span><span class="sxs-lookup"><span data-stu-id="38d12-241">An image was resized from its native dimensions.</span></span> |  
| <span data-ttu-id="38d12-242">Paint</span><span class="sxs-lookup"><span data-stu-id="38d12-242">Paint</span></span> | <span data-ttu-id="38d12-243">Les couches composites ont été peintes dans une zone de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="38d12-243">Composited layers were painted to a region of the display.</span></span>  <span data-ttu-id="38d12-244">Pointez sur un enregistrement de Paint pour mettre en évidence la région de l’affichage mise à jour.</span><span class="sxs-lookup"><span data-stu-id="38d12-244">Hovering over a Paint record highlights the region of the display that was updated.</span></span> |  

### <span data-ttu-id="38d12-245">Propriétés d’événement de dessin</span><span class="sxs-lookup"><span data-stu-id="38d12-245">Painting event properties</span></span>  

| <span data-ttu-id="38d12-246">Propriété</span><span class="sxs-lookup"><span data-stu-id="38d12-246">Property</span></span> | <span data-ttu-id="38d12-247">Description</span><span class="sxs-lookup"><span data-stu-id="38d12-247">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="38d12-248">Location</span><span class="sxs-lookup"><span data-stu-id="38d12-248">Location</span></span> | <span data-ttu-id="38d12-249">Pour les événements Paint, les coordonnées x et y du rectangle de peinture.</span><span class="sxs-lookup"><span data-stu-id="38d12-249">For Paint events, the x and y coordinates of the paint rectangle.</span></span> |  
| <span data-ttu-id="38d12-250">Analytique</span><span class="sxs-lookup"><span data-stu-id="38d12-250">Dimensions</span></span> | <span data-ttu-id="38d12-251">Pour les événements Paint, hauteur et largeur de la zone peinte.</span><span class="sxs-lookup"><span data-stu-id="38d12-251">For Paint events, the height and width of the painted region.</span></span> |  

 



<!-- image links -->  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "Time-référence d’API de la console"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd-XXXXXXX XXXXXXX xxx xxxxxxxxx"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Fenêtre: événement DOMContentLoaded | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope. setInterval () | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope. setTimeout () | MDN"  

> [!NOTE]
> <span data-ttu-id="38d12-257">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="38d12-257">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="38d12-258">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) et est créée par [Meggin Kearney][MegginKearney] \ (Technical Writer \) et [Flavio][FlavioCopes] configure \ (développeur de pile complète \).</span><span class="sxs-lookup"><span data-stu-id="38d12-258">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Flavio Copes][FlavioCopes] \(Full Stack Developer\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="38d12-260">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="38d12-260">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
