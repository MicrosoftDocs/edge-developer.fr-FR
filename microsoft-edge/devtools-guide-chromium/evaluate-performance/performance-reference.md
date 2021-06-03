---
description: Le mode événements de chronologie affiche tous les événements déclenchés lors de l’enregistrement.  Utilisez la référence d’événement de chronologie pour en savoir plus sur chaque type d’événement de chronologie.
title: Référence des événements de chronologie
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: b8a15dd3503a891698d1f96bdc99946163d738ff
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564209"
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
# <a name="timeline-event-reference"></a><span data-ttu-id="9883b-105">Référence des événements de chronologie</span><span class="sxs-lookup"><span data-stu-id="9883b-105">Timeline Event reference</span></span>  

<span data-ttu-id="9883b-106">Le mode événements de chronologie affiche tous les événements déclenchés lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9883b-106">The timeline events mode displays all events triggered while making a recording.</span></span>  <span data-ttu-id="9883b-107">Utilisez la référence d’événement de chronologie pour en savoir plus sur chaque type d’événement de chronologie.</span><span class="sxs-lookup"><span data-stu-id="9883b-107">Use the timeline event reference to learn more about each timeline event type.</span></span>  

## <a name="common-timeline-event-properties"></a><span data-ttu-id="9883b-108">Propriétés courantes des événements de chronologie</span><span class="sxs-lookup"><span data-stu-id="9883b-108">Common timeline event properties</span></span>  

<span data-ttu-id="9883b-109">Certains détails sont présents dans les événements de tous types, tandis que d’autres s’appliquent uniquement à certains types d’événements.</span><span class="sxs-lookup"><span data-stu-id="9883b-109">Certain details are present in events of all types, while some only apply to certain event types.</span></span>  <span data-ttu-id="9883b-110">Cette section répertorie les propriétés communes à différents types d’événements.</span><span class="sxs-lookup"><span data-stu-id="9883b-110">This section lists properties common to different event types.</span></span>  <span data-ttu-id="9883b-111">Les propriétés spécifiques à certains types d’événements sont répertoriées dans les références pour les types d’événements qui suivent.</span><span class="sxs-lookup"><span data-stu-id="9883b-111">Properties specific to certain event types are listed in the references for those event types that follow.</span></span>  

| <span data-ttu-id="9883b-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="9883b-112">Property</span></span> | <span data-ttu-id="9883b-113">Quand s’affiche-t-elle ?</span><span class="sxs-lookup"><span data-stu-id="9883b-113">When is it shown</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="9883b-114">Heure agrégée</span><span class="sxs-lookup"><span data-stu-id="9883b-114">Aggregated time</span></span> | <span data-ttu-id="9883b-115">Pour les événements avec **des événements**imbrmbrés, le temps pris par chaque catégorie d’événements.</span><span class="sxs-lookup"><span data-stu-id="9883b-115">For events with **nested events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="9883b-116">Pile des appels</span><span class="sxs-lookup"><span data-stu-id="9883b-116">Call Stack</span></span> | <span data-ttu-id="9883b-117">Pour les événements avec **des événements enfants,** le temps pris par chaque catégorie d’événements.</span><span class="sxs-lookup"><span data-stu-id="9883b-117">For events with **child events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="9883b-118">Temps processeur</span><span class="sxs-lookup"><span data-stu-id="9883b-118">CPU time</span></span> | <span data-ttu-id="9883b-119">Temps processeur de l’événement enregistré.</span><span class="sxs-lookup"><span data-stu-id="9883b-119">How much CPU time the recorded event took.</span></span> |  
| <span data-ttu-id="9883b-120">Détails</span><span class="sxs-lookup"><span data-stu-id="9883b-120">Details</span></span> | <span data-ttu-id="9883b-121">Autres détails sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="9883b-121">Other details about the event.</span></span> |  
| <span data-ttu-id="9883b-122">Duration \(at time-stamp\)</span><span class="sxs-lookup"><span data-stu-id="9883b-122">Duration \(at time-stamp\)</span></span> | <span data-ttu-id="9883b-123">Le temps qu’il a fallu à l’événement avec tous ses enfants pour se terminer ; est l’heure à laquelle l’événement s’est produit, par rapport au début de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9883b-123">How long it took the event with all of its children to complete; timestamp is the time at which the event occurred, relative to when the recording started.</span></span> |  
| <span data-ttu-id="9883b-124">Temps libre</span><span class="sxs-lookup"><span data-stu-id="9883b-124">Self time</span></span> | <span data-ttu-id="9883b-125">Durée de l’événement sans aucun de ses enfants.</span><span class="sxs-lookup"><span data-stu-id="9883b-125">How long the event took without any of its children.</span></span> |  
| <span data-ttu-id="9883b-126">Taille de tas utilisée</span><span class="sxs-lookup"><span data-stu-id="9883b-126">Used Heap Size</span></span> | <span data-ttu-id="9883b-127">Quantité de mémoire utilisée par l’application lors de l’enregistrement de l’événement, et le delta \(+/-\) change en taille de tas utilisée depuis le dernier échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="9883b-127">Amount of memory being used by the application when the event was recorded, and the delta \(+/-\) change in used heap size since the last sampling.</span></span> |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <a name="loading-events"></a><span data-ttu-id="9883b-128">Chargement d’événements</span><span class="sxs-lookup"><span data-stu-id="9883b-128">Loading events</span></span>  

<span data-ttu-id="9883b-129">Cette section répertorie les événements qui appartiennent à la catégorie Loading et leurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="9883b-129">This section lists events that belong to Loading category and their properties.</span></span>  

| <span data-ttu-id="9883b-130">Événement</span><span class="sxs-lookup"><span data-stu-id="9883b-130">Event</span></span> | <span data-ttu-id="9883b-131">Description</span><span class="sxs-lookup"><span data-stu-id="9883b-131">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="9883b-132">Code HTML d’parse</span><span class="sxs-lookup"><span data-stu-id="9883b-132">Parse HTML</span></span> |  <span data-ttu-id="9883b-133">Microsoft Edge l’algorithme d’analyse HTML.</span><span class="sxs-lookup"><span data-stu-id="9883b-133">Microsoft Edge ran the HTML parsing algorithm.</span></span> |  
| <span data-ttu-id="9883b-134">Terminer le chargement</span><span class="sxs-lookup"><span data-stu-id="9883b-134">Finish Loading</span></span> |  <span data-ttu-id="9883b-135">Demande réseau terminée.</span><span class="sxs-lookup"><span data-stu-id="9883b-135">A network request completed.</span></span> |  
| <span data-ttu-id="9883b-136">Recevoir des données</span><span class="sxs-lookup"><span data-stu-id="9883b-136">Receive Data</span></span> |  <span data-ttu-id="9883b-137">Les données d’une demande ont été reçues.</span><span class="sxs-lookup"><span data-stu-id="9883b-137">Data for a request was received.</span></span>  <span data-ttu-id="9883b-138">Il existe un ou plusieurs événements De réception de données.</span><span class="sxs-lookup"><span data-stu-id="9883b-138">There are one or more Receive Data events.</span></span> |  
| <span data-ttu-id="9883b-139">Recevoir une réponse</span><span class="sxs-lookup"><span data-stu-id="9883b-139">Receive Response</span></span> |  <span data-ttu-id="9883b-140">Réponse HTTP initiale d’une requête.</span><span class="sxs-lookup"><span data-stu-id="9883b-140">The initial HTTP response from a request.</span></span> |  
| <span data-ttu-id="9883b-141">Envoyer une demande</span><span class="sxs-lookup"><span data-stu-id="9883b-141">Send Request</span></span> |  <span data-ttu-id="9883b-142">Une demande réseau a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="9883b-142">A network request has been sent.</span></span> |  

### <a name="loading-event-properties"></a><span data-ttu-id="9883b-143">Chargement des propriétés de l’événement</span><span class="sxs-lookup"><span data-stu-id="9883b-143">Loading event properties</span></span>  

| <span data-ttu-id="9883b-144">Propriété</span><span class="sxs-lookup"><span data-stu-id="9883b-144">Property</span></span> | <span data-ttu-id="9883b-145">Description</span><span class="sxs-lookup"><span data-stu-id="9883b-145">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="9883b-146">Ressource</span><span class="sxs-lookup"><span data-stu-id="9883b-146">Resource</span></span> | <span data-ttu-id="9883b-147">URL de la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="9883b-147">The URL of the requested resource.</span></span> |  
| <span data-ttu-id="9883b-148">Preview</span><span class="sxs-lookup"><span data-stu-id="9883b-148">Preview</span></span> | <span data-ttu-id="9883b-149">Aperçu de la ressource demandée \(images uniquement\).</span><span class="sxs-lookup"><span data-stu-id="9883b-149">Preview of the requested resource \(images only\).</span></span> |  
| <span data-ttu-id="9883b-150">Request, méthode</span><span class="sxs-lookup"><span data-stu-id="9883b-150">Request Method</span></span> | <span data-ttu-id="9883b-151">Méthode HTTP utilisée pour la requête \( `GET` ou `POST` , par exemple\).</span><span class="sxs-lookup"><span data-stu-id="9883b-151">HTTP method used for the request \(`GET` or `POST`, for example\).</span></span> |  
| <span data-ttu-id="9883b-152">Code d’état</span><span class="sxs-lookup"><span data-stu-id="9883b-152">Status Code</span></span> | <span data-ttu-id="9883b-153">Code de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="9883b-153">HTTP response code.</span></span> |  
| <span data-ttu-id="9883b-154">MIME Type</span><span class="sxs-lookup"><span data-stu-id="9883b-154">MIME Type</span></span> | <span data-ttu-id="9883b-155">Type MIME de la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="9883b-155">MIME type of the requested resource.</span></span> |  
| <span data-ttu-id="9883b-156">Longueur des données codées</span><span class="sxs-lookup"><span data-stu-id="9883b-156">Encoded Data Length</span></span> | <span data-ttu-id="9883b-157">Longueur de la ressource demandée en octets.</span><span class="sxs-lookup"><span data-stu-id="9883b-157">Length of requested resource in bytes.</span></span> |  

## <a name="scripting-events"></a><span data-ttu-id="9883b-158">Événements de script</span><span class="sxs-lookup"><span data-stu-id="9883b-158">Scripting events</span></span>  

<span data-ttu-id="9883b-159">Cette section répertorie les événements qui appartiennent à la catégorie Scripting et leurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="9883b-159">This section lists events that belong to the Scripting category and their properties.</span></span>  

| <span data-ttu-id="9883b-160">Événement</span><span class="sxs-lookup"><span data-stu-id="9883b-160">Event</span></span> | <span data-ttu-id="9883b-161">Description</span><span class="sxs-lookup"><span data-stu-id="9883b-161">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="9883b-162">Image d’animation déclenché</span><span class="sxs-lookup"><span data-stu-id="9883b-162">Animation Frame Fired</span></span> | <span data-ttu-id="9883b-163">Une image d’animation programmée a été déclenché et son handler de rappel a été appelé.</span><span class="sxs-lookup"><span data-stu-id="9883b-163">A scheduled animation frame fired, and its callback handler invoked.</span></span> |  
| <span data-ttu-id="9883b-164">Annuler un cadre d’animation</span><span class="sxs-lookup"><span data-stu-id="9883b-164">Cancel Animation Frame</span></span> |  <span data-ttu-id="9883b-165">Une image d’animation programmée a été annulée.</span><span class="sxs-lookup"><span data-stu-id="9883b-165">A scheduled animation frame was canceled.</span></span> |  
| <span data-ttu-id="9883b-166">GC, événement</span><span class="sxs-lookup"><span data-stu-id="9883b-166">GC Event</span></span> |  <span data-ttu-id="9883b-167">Un garbage collection s’est produit.</span><span class="sxs-lookup"><span data-stu-id="9883b-167">Garbage collection occurred.</span></span> |  
| <span data-ttu-id="9883b-168">DOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="9883b-168">DOMContentLoaded</span></span> |  <span data-ttu-id="9883b-169">[L’événement DOMContentLoaded][MDNWindowDOMContentLoadedEvent] a été déclenché par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="9883b-169">The [DOMContentLoaded event][MDNWindowDOMContentLoadedEvent] was fired by the browser.</span></span>  <span data-ttu-id="9883b-170">Cet événement est déclenché lorsque tout le contenu DOM de la page est chargé et l’est également.</span><span class="sxs-lookup"><span data-stu-id="9883b-170">This event is fired when all of the DOM content of the page is loaded and parsed.</span></span> |  
| <span data-ttu-id="9883b-171">Évaluer le script</span><span class="sxs-lookup"><span data-stu-id="9883b-171">Evaluate Script</span></span> | <span data-ttu-id="9883b-172">Un script a été évalué.</span><span class="sxs-lookup"><span data-stu-id="9883b-172">A script was evaluated.</span></span> |  
| <span data-ttu-id="9883b-173">Événement</span><span class="sxs-lookup"><span data-stu-id="9883b-173">Event</span></span> | <span data-ttu-id="9883b-174">Un événement JavaScript \(par `mousedown` exemple, ou `key` \).</span><span class="sxs-lookup"><span data-stu-id="9883b-174">A JavaScript event \(for example, `mousedown`, or `key`\).</span></span> |  
| <span data-ttu-id="9883b-175">Appel de fonction</span><span class="sxs-lookup"><span data-stu-id="9883b-175">Function Call</span></span> | <span data-ttu-id="9883b-176">Un appel de fonction JavaScript de niveau supérieur a été effectué \(apparaît uniquement lorsque le navigateur entre dans le moteur JavaScript\).</span><span class="sxs-lookup"><span data-stu-id="9883b-176">A top-level JavaScript function call was made \(only appears when browser enters JavaScript engine\).</span></span> |  
| <span data-ttu-id="9883b-177">Installer le timer</span><span class="sxs-lookup"><span data-stu-id="9883b-177">Install Timer</span></span> | <span data-ttu-id="9883b-178">Un timer a été créé avec [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] ou [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span><span class="sxs-lookup"><span data-stu-id="9883b-178">A timer was created with [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] or [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span></span> |  
| <span data-ttu-id="9883b-179">Image d’animation de demande</span><span class="sxs-lookup"><span data-stu-id="9883b-179">Request Animation Frame</span></span> | <span data-ttu-id="9883b-180">Un `requestAnimationFrame()` appel a programmé une nouvelle image.</span><span class="sxs-lookup"><span data-stu-id="9883b-180">A `requestAnimationFrame()` call scheduled a new frame.</span></span> |  
| <span data-ttu-id="9883b-181">Supprimer le temps</span><span class="sxs-lookup"><span data-stu-id="9883b-181">Remove Timer</span></span> | <span data-ttu-id="9883b-182">Un timer précédemment créé a été effacé.</span><span class="sxs-lookup"><span data-stu-id="9883b-182">A previously created timer was cleared.</span></span> |  
| <span data-ttu-id="9883b-183">Heure</span><span class="sxs-lookup"><span data-stu-id="9883b-183">Time</span></span> |  <span data-ttu-id="9883b-184">Script appelé [console.time()][ConsoleApiTime].</span><span class="sxs-lookup"><span data-stu-id="9883b-184">A script called [console.time()][ConsoleApiTime].</span></span> |  
| <span data-ttu-id="9883b-185">Fin de l’heure</span><span class="sxs-lookup"><span data-stu-id="9883b-185">Time End</span></span> | <span data-ttu-id="9883b-186">Un script appelé [console.timeEnd()][ConsoleApiTimeEnd].</span><span class="sxs-lookup"><span data-stu-id="9883b-186">A script called [console.timeEnd()][ConsoleApiTimeEnd].</span></span> |  
| <span data-ttu-id="9883b-187">Timer Fired</span><span class="sxs-lookup"><span data-stu-id="9883b-187">Timer Fired</span></span> | <span data-ttu-id="9883b-188">Un timer déclenché qui a été programmé avec `setInterval()` ou `setTimeout()` .</span><span class="sxs-lookup"><span data-stu-id="9883b-188">A timer fired that was scheduled with `setInterval()` or `setTimeout()`.</span></span> |  
| <span data-ttu-id="9883b-189">XHR Ready State Change</span><span class="sxs-lookup"><span data-stu-id="9883b-189">XHR Ready State Change</span></span> | <span data-ttu-id="9883b-190">L’état prêt d’un XMLHTTPRequest a changé.</span><span class="sxs-lookup"><span data-stu-id="9883b-190">The ready state of an XMLHTTPRequest changed.</span></span> |  
| <span data-ttu-id="9883b-191">Charge XHR</span><span class="sxs-lookup"><span data-stu-id="9883b-191">XHR Load</span></span> | <span data-ttu-id="9883b-192">Chargement `XMLHTTPRequest` terminé.</span><span class="sxs-lookup"><span data-stu-id="9883b-192">An `XMLHTTPRequest` finished loading.</span></span> |  

### <a name="scripting-event-properties"></a><span data-ttu-id="9883b-193">Propriétés d’événement de script</span><span class="sxs-lookup"><span data-stu-id="9883b-193">Scripting event properties</span></span>  

| <span data-ttu-id="9883b-194">Propriété</span><span class="sxs-lookup"><span data-stu-id="9883b-194">Property</span></span> | <span data-ttu-id="9883b-195">Description</span><span class="sxs-lookup"><span data-stu-id="9883b-195">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="9883b-196">Timer ID</span><span class="sxs-lookup"><span data-stu-id="9883b-196">Timer ID</span></span> | <span data-ttu-id="9883b-197">ID du timer.</span><span class="sxs-lookup"><span data-stu-id="9883b-197">The timer ID.</span></span> |  
| <span data-ttu-id="9883b-198">Délai d’expiration dépassé</span><span class="sxs-lookup"><span data-stu-id="9883b-198">Timeout</span></span> | <span data-ttu-id="9883b-199">Délai spécifié par le timer.</span><span class="sxs-lookup"><span data-stu-id="9883b-199">The timeout specified by the timer.</span></span> |  
| <span data-ttu-id="9883b-200">Répétitions</span><span class="sxs-lookup"><span data-stu-id="9883b-200">Repeats</span></span> | <span data-ttu-id="9883b-201">Booléen qui spécifie si le timer se répète.</span><span class="sxs-lookup"><span data-stu-id="9883b-201">Boolean that specifies if the timer repeats.</span></span> |  
| <span data-ttu-id="9883b-202">Appel de fonction</span><span class="sxs-lookup"><span data-stu-id="9883b-202">Function Call</span></span> | <span data-ttu-id="9883b-203">Fonction qui a été invoquée.</span><span class="sxs-lookup"><span data-stu-id="9883b-203">A function that was invoked.</span></span> |  

## <a name="rendering-events"></a><span data-ttu-id="9883b-204">Rendu des événements</span><span class="sxs-lookup"><span data-stu-id="9883b-204">Rendering events</span></span>  

<span data-ttu-id="9883b-205">Cette section répertorie les événements qui appartiennent à la catégorie Rendering et leurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="9883b-205">This section lists events that belong to Rendering category and their properties.</span></span>  

| <span data-ttu-id="9883b-206">Événement</span><span class="sxs-lookup"><span data-stu-id="9883b-206">Event</span></span> | <span data-ttu-id="9883b-207">Description</span><span class="sxs-lookup"><span data-stu-id="9883b-207">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="9883b-208">Invalider la disposition</span><span class="sxs-lookup"><span data-stu-id="9883b-208">Invalidate layout</span></span> | <span data-ttu-id="9883b-209">La mise en page a été invalidée par une modification DU DOM.</span><span class="sxs-lookup"><span data-stu-id="9883b-209">The page layout was invalidated by a DOM change.</span></span> |  
| <span data-ttu-id="9883b-210">Disposition</span><span class="sxs-lookup"><span data-stu-id="9883b-210">Layout</span></span> | <span data-ttu-id="9883b-211">Une mise en page a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="9883b-211">A page layout was completed.</span></span> |  
| <span data-ttu-id="9883b-212">Recalculer le style</span><span class="sxs-lookup"><span data-stu-id="9883b-212">Recalculate style</span></span> | <span data-ttu-id="9883b-213">Microsoft Edge styles d’éléments recalculés.</span><span class="sxs-lookup"><span data-stu-id="9883b-213">Microsoft Edge recalculated element styles.</span></span> |  
| <span data-ttu-id="9883b-214">Scroll</span><span class="sxs-lookup"><span data-stu-id="9883b-214">Scroll</span></span> | <span data-ttu-id="9883b-215">Le contenu de l’affichage imbrmbré a été fait défiler.</span><span class="sxs-lookup"><span data-stu-id="9883b-215">The content of nested view was scrolled.</span></span> |  

### <a name="rendering-event-properties"></a><span data-ttu-id="9883b-216">Rendu des propriétés d’événement</span><span class="sxs-lookup"><span data-stu-id="9883b-216">Rendering event properties</span></span>  

| <span data-ttu-id="9883b-217">Propriété</span><span class="sxs-lookup"><span data-stu-id="9883b-217">Property</span></span> | <span data-ttu-id="9883b-218">Description</span><span class="sxs-lookup"><span data-stu-id="9883b-218">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="9883b-219">Disposition non valide</span><span class="sxs-lookup"><span data-stu-id="9883b-219">Layout invalidated</span></span> | <span data-ttu-id="9883b-220">Pour les enregistrements de disposition, la trace de pile du code qui a provoqué l’invalidation de la disposition.</span><span class="sxs-lookup"><span data-stu-id="9883b-220">For Layout records, the stack trace of the code that caused the layout to be invalidated.</span></span> |  
| <span data-ttu-id="9883b-221">Les nodes qui ont besoin d’une disposition</span><span class="sxs-lookup"><span data-stu-id="9883b-221">Nodes that need layout</span></span> | <span data-ttu-id="9883b-222">Pour les enregistrements de disposition, nombre de nodes marqués comme devant être mis en page avant le début du relais.</span><span class="sxs-lookup"><span data-stu-id="9883b-222">For Layout records, the number of nodes that were marked as needing layout before the relayout started.</span></span>  <span data-ttu-id="9883b-223">Il s’agit normalement de ces derniers qui ont été invalidés par le code du développeur, ainsi qu’un chemin vers le haut pour relayer la racine.</span><span class="sxs-lookup"><span data-stu-id="9883b-223">These are normally those nodes that were invalidated by developer code, plus a path upward to relayout root.</span></span> |  
| <span data-ttu-id="9883b-224">Taille de l’arborescence de disposition</span><span class="sxs-lookup"><span data-stu-id="9883b-224">Layout tree size</span></span> | <span data-ttu-id="9883b-225">Pour les enregistrements de disposition, le nombre total de nœuds sous la racine du relais \(le nœud qui Microsoft Edge le relais\).</span><span class="sxs-lookup"><span data-stu-id="9883b-225">For Layout records, the total number of nodes under the relayout root \(the node that Microsoft Edge starts the relayout\).</span></span> |  
| <span data-ttu-id="9883b-226">Étendue de disposition</span><span class="sxs-lookup"><span data-stu-id="9883b-226">Layout scope</span></span> | <span data-ttu-id="9883b-227">Les valeurs `Partial` possibles sont \(la limite de disposition est une partie du DOM\) ou `Whole document` .</span><span class="sxs-lookup"><span data-stu-id="9883b-227">Possible values are `Partial` \(the re-layout boundary is a portion of the DOM\) or `Whole document`.</span></span> |  
| <span data-ttu-id="9883b-228">Éléments affectés</span><span class="sxs-lookup"><span data-stu-id="9883b-228">Elements affected</span></span> | <span data-ttu-id="9883b-229">Pour recalculer les enregistrements de style, nombre d’éléments affectés par un recalcul de style.</span><span class="sxs-lookup"><span data-stu-id="9883b-229">For Recalculate style records, the number of elements affected by a style recalculation.</span></span> |  
| <span data-ttu-id="9883b-230">Styles invalidés</span><span class="sxs-lookup"><span data-stu-id="9883b-230">Styles invalidated</span></span> | <span data-ttu-id="9883b-231">Pour recalculer les enregistrements de style, fournit la trace de pile du code à l’origine de l’invalidation du style.</span><span class="sxs-lookup"><span data-stu-id="9883b-231">For Recalculate style records, provides the stack trace of the code that caused the style invalidation.</span></span> |  

## <a name="painting-events"></a><span data-ttu-id="9883b-232">Événements de dessin</span><span class="sxs-lookup"><span data-stu-id="9883b-232">Painting events</span></span>  

<span data-ttu-id="9883b-233">Cette section répertorie les événements qui appartiennent à la catégorie Painting et leurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="9883b-233">This section lists events that belong to Painting category and their properties.</span></span>  

| <span data-ttu-id="9883b-234">Événement</span><span class="sxs-lookup"><span data-stu-id="9883b-234">Event</span></span> | <span data-ttu-id="9883b-235">Description</span><span class="sxs-lookup"><span data-stu-id="9883b-235">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="9883b-236">Couches composites</span><span class="sxs-lookup"><span data-stu-id="9883b-236">Composite Layers</span></span> | <span data-ttu-id="9883b-237">Couches d’image composites pour le moteur Microsoft Edge rendu.</span><span class="sxs-lookup"><span data-stu-id="9883b-237">The composited image layers for the Microsoft Edge rendering engine.</span></span> |  
| <span data-ttu-id="9883b-238">Décodage d’image</span><span class="sxs-lookup"><span data-stu-id="9883b-238">Image Decode</span></span> | <span data-ttu-id="9883b-239">Une ressource d’image a été décodée.</span><span class="sxs-lookup"><span data-stu-id="9883b-239">An image resource was decoded.</span></span> |  
| <span data-ttu-id="9883b-240">Resize d’image</span><span class="sxs-lookup"><span data-stu-id="9883b-240">Image Resize</span></span> | <span data-ttu-id="9883b-241">Une image a été re dimensionisée à partir de ses dimensions natives.</span><span class="sxs-lookup"><span data-stu-id="9883b-241">An image was resized from its native dimensions.</span></span> |  
| <span data-ttu-id="9883b-242">Paint</span><span class="sxs-lookup"><span data-stu-id="9883b-242">Paint</span></span> | <span data-ttu-id="9883b-243">Les couches composites ont été peints dans une région de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="9883b-243">Composited layers were painted to a region of the display.</span></span>  <span data-ttu-id="9883b-244">Le fait de pointer sur un Paint met en évidence la région de l’affichage qui a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="9883b-244">Hovering over a Paint record highlights the region of the display that was updated.</span></span> |  

### <a name="painting-event-properties"></a><span data-ttu-id="9883b-245">Propriétés de l’événement Painting</span><span class="sxs-lookup"><span data-stu-id="9883b-245">Painting event properties</span></span>  

| <span data-ttu-id="9883b-246">Propriété</span><span class="sxs-lookup"><span data-stu-id="9883b-246">Property</span></span> | <span data-ttu-id="9883b-247">Description</span><span class="sxs-lookup"><span data-stu-id="9883b-247">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="9883b-248">Localisation</span><span class="sxs-lookup"><span data-stu-id="9883b-248">Location</span></span> | <span data-ttu-id="9883b-249">Pour Paint événements, les coordonnées x et y du rectangle de pinceau.</span><span class="sxs-lookup"><span data-stu-id="9883b-249">For Paint events, the x and y coordinates of the paint rectangle.</span></span> |  
| <span data-ttu-id="9883b-250">Dimensions</span><span class="sxs-lookup"><span data-stu-id="9883b-250">Dimensions</span></span> | <span data-ttu-id="9883b-251">Pour Paint événements, la hauteur et la largeur de la région peint.</span><span class="sxs-lookup"><span data-stu-id="9883b-251">For Paint events, the height and width of the painted region.</span></span> |  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="9883b-252">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="9883b-252">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "time - Référence de l’API de console"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd - Référence de l’API console"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Window : événement DOMContentLoaded | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope.setInterval() | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope.setTimeout() | MDN"  

> [!NOTE]
> <span data-ttu-id="9883b-258">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9883b-258">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9883b-259">La page d’origine est trouvée ici et est co-auteure par [Meggin Kearney][MegginKearney] \(Tech Writer\) et [ContrôleioQuets][FlavioCopes] \(Full Stack Developer\). [](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference)</span><span class="sxs-lookup"><span data-stu-id="9883b-259">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Flavio Copes][FlavioCopes] \(Full Stack Developer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="9883b-261">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9883b-261">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors#flavio-copes  
