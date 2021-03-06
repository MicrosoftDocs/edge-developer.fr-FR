---
description: Référence du protocole DevTools Version 0.2 (EdgeHTML) pour le domaine de page. Les actions et événements liés à la page inspectée appartiennent au domaine de page.
title: Domaine de page - DevTools Protocol Version 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d969dd100164ace61445a4618174cfa943dcfd2b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398846"
---
# <a name="page-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="8e90e-104">Domaine de page - DevTools Protocol Version 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="8e90e-104">Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="8e90e-105">Les actions et événements liés à la page inspectée appartiennent au domaine de page.</span><span class="sxs-lookup"><span data-stu-id="8e90e-105">Actions and events related to the inspected page belong to the page domain.</span></span>  

| <span data-ttu-id="8e90e-106">Classification</span><span class="sxs-lookup"><span data-stu-id="8e90e-106">Classification</span></span> | <span data-ttu-id="8e90e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="8e90e-107">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="8e90e-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8e90e-108">Methods</span></span>](#methods) | <span data-ttu-id="8e90e-109">[activer,](#enable) [désactiver,](#disable) [naviguer,](#navigate) [getFrameTree](#getframetree)</span><span class="sxs-lookup"><span data-stu-id="8e90e-109">[enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree)</span></span> |  
| [<span data-ttu-id="8e90e-110">Événements</span><span class="sxs-lookup"><span data-stu-id="8e90e-110">Events</span></span>](#events) | <span data-ttu-id="8e90e-111">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span><span class="sxs-lookup"><span data-stu-id="8e90e-111">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span></span> |  
| [<span data-ttu-id="8e90e-112">Types</span><span class="sxs-lookup"><span data-stu-id="8e90e-112">Types</span></span>](#types) | <span data-ttu-id="8e90e-113">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span><span class="sxs-lookup"><span data-stu-id="8e90e-113">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span></span> |  

## <a name="methods"></a><span data-ttu-id="8e90e-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8e90e-114">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="8e90e-115">activer</span><span class="sxs-lookup"><span data-stu-id="8e90e-115">enable</span></span>  

<span data-ttu-id="8e90e-116">Active les notifications de domaine de page.</span><span class="sxs-lookup"><span data-stu-id="8e90e-116">Enables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="8e90e-117">désactiver </span><span class="sxs-lookup"><span data-stu-id="8e90e-117">disable</span></span>  

<span data-ttu-id="8e90e-118">Désactive les notifications de domaine de page.</span><span class="sxs-lookup"><span data-stu-id="8e90e-118">Disables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="navigate"></a><span data-ttu-id="8e90e-119">naviguer</span><span class="sxs-lookup"><span data-stu-id="8e90e-119">navigate</span></span>  

<span data-ttu-id="8e90e-120">Navigue vers la page actuelle jusqu’à l’URL donnée.</span><span class="sxs-lookup"><span data-stu-id="8e90e-120">Navigates current page to the given URL.</span></span>  

| <span data-ttu-id="8e90e-121">Parameters</span><span class="sxs-lookup"><span data-stu-id="8e90e-121">Parameters</span></span> | <span data-ttu-id="8e90e-122">Type</span><span class="sxs-lookup"><span data-stu-id="8e90e-122">Type</span></span> | <span data-ttu-id="8e90e-123">Détails</span><span class="sxs-lookup"><span data-stu-id="8e90e-123">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="8e90e-124">url</span><span class="sxs-lookup"><span data-stu-id="8e90e-124">url</span></span> | `string` | <span data-ttu-id="8e90e-125">URL vers qui accéder à la page.</span><span class="sxs-lookup"><span data-stu-id="8e90e-125">URL to navigate the page to.</span></span> |  
| <span data-ttu-id="8e90e-126">frameId \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="8e90e-126">frameId \(optional\)</span></span> | [<span data-ttu-id="8e90e-127">FrameId</span><span class="sxs-lookup"><span data-stu-id="8e90e-127">FrameId</span></span>](#frameid) | <span data-ttu-id="8e90e-128">ID d’image à parcourir.</span><span class="sxs-lookup"><span data-stu-id="8e90e-128">Frame id to navigate.</span></span>  <span data-ttu-id="8e90e-129">S’il n’est pas spécifié, navigue vers la page supérieure.</span><span class="sxs-lookup"><span data-stu-id="8e90e-129">If not specified, will navigate the top page.</span></span> |  

| <span data-ttu-id="8e90e-130">Renvoie</span><span class="sxs-lookup"><span data-stu-id="8e90e-130">Returns</span></span> | <span data-ttu-id="8e90e-131">Type</span><span class="sxs-lookup"><span data-stu-id="8e90e-131">Type</span></span> | <span data-ttu-id="8e90e-132">Détails</span><span class="sxs-lookup"><span data-stu-id="8e90e-132">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="8e90e-133">frameId</span><span class="sxs-lookup"><span data-stu-id="8e90e-133">frameId</span></span> | [<span data-ttu-id="8e90e-134">FrameId</span><span class="sxs-lookup"><span data-stu-id="8e90e-134">FrameId</span></span>](#frameid) | <span data-ttu-id="8e90e-135">ID d’image à parcourir.</span><span class="sxs-lookup"><span data-stu-id="8e90e-135">Frame id that will be navigated.</span></span> |  

---  

### <a name="getframetree"></a><span data-ttu-id="8e90e-136">getFrameTree</span><span class="sxs-lookup"><span data-stu-id="8e90e-136">getFrameTree</span></span>  

<span data-ttu-id="8e90e-137">Renvoie la structure de l’arborescence d’images présente.</span><span class="sxs-lookup"><span data-stu-id="8e90e-137">Returns present frame tree structure.</span></span>  

| <span data-ttu-id="8e90e-138">Renvoie</span><span class="sxs-lookup"><span data-stu-id="8e90e-138">Returns</span></span> | <span data-ttu-id="8e90e-139">Type</span><span class="sxs-lookup"><span data-stu-id="8e90e-139">Type</span></span> | <span data-ttu-id="8e90e-140">Détails</span><span class="sxs-lookup"><span data-stu-id="8e90e-140">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="8e90e-141">frameTree</span><span class="sxs-lookup"><span data-stu-id="8e90e-141">frameTree</span></span> | [<span data-ttu-id="8e90e-142">FrameTree</span><span class="sxs-lookup"><span data-stu-id="8e90e-142">FrameTree</span></span>](#frametree) | <span data-ttu-id="8e90e-143">Structure d’arborescence de cadres présente.</span><span class="sxs-lookup"><span data-stu-id="8e90e-143">Present frame tree structure.</span></span> |  

---  

## <a name="events"></a><span data-ttu-id="8e90e-144">Événements</span><span class="sxs-lookup"><span data-stu-id="8e90e-144">Events</span></span>  

### <a name="frameattached"></a><span data-ttu-id="8e90e-145">frameAttached</span><span class="sxs-lookup"><span data-stu-id="8e90e-145">frameAttached</span></span>  

<span data-ttu-id="8e90e-146">Déclenché lorsque l’image a été attachée à son parent.</span><span class="sxs-lookup"><span data-stu-id="8e90e-146">Fired when frame has been attached to its parent.</span></span>  

| <span data-ttu-id="8e90e-147">Parameters</span><span class="sxs-lookup"><span data-stu-id="8e90e-147">Parameters</span></span> | <span data-ttu-id="8e90e-148">Type</span><span class="sxs-lookup"><span data-stu-id="8e90e-148">Type</span></span> | <span data-ttu-id="8e90e-149">Détails</span><span class="sxs-lookup"><span data-stu-id="8e90e-149">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="8e90e-150">frameId</span><span class="sxs-lookup"><span data-stu-id="8e90e-150">frameId</span></span> | [<span data-ttu-id="8e90e-151">FrameId</span><span class="sxs-lookup"><span data-stu-id="8e90e-151">FrameId</span></span>](#frameid) | <span data-ttu-id="8e90e-152">ID du cadre attaché.</span><span class="sxs-lookup"><span data-stu-id="8e90e-152">Id of the frame that has been attached.</span></span> |  
| <span data-ttu-id="8e90e-153">parentFrameId</span><span class="sxs-lookup"><span data-stu-id="8e90e-153">parentFrameId</span></span> | [<span data-ttu-id="8e90e-154">FrameId</span><span class="sxs-lookup"><span data-stu-id="8e90e-154">FrameId</span></span>](#frameid) | <span data-ttu-id="8e90e-155">Identificateur d’image parent.</span><span class="sxs-lookup"><span data-stu-id="8e90e-155">Parent frame identifier.</span></span> |  
| <span data-ttu-id="8e90e-156">stack \(optional\)</span><span class="sxs-lookup"><span data-stu-id="8e90e-156">stack \(optional\)</span></span> | [<span data-ttu-id="8e90e-157">Runtime.StackTrace</span><span class="sxs-lookup"><span data-stu-id="8e90e-157">Runtime.StackTrace</span></span>](./runtime.md#stacktrace) | <span data-ttu-id="8e90e-158">Suivi de la pile JavaScript du moment où l’image a été attachée, uniquement définie si l’image a été initiée à partir d’un script.</span><span class="sxs-lookup"><span data-stu-id="8e90e-158">JavaScript stack trace of when frame was attached, only set if frame initiated from script.</span></span> |  

---  

### <a name="framedetached"></a><span data-ttu-id="8e90e-159">frameDetached</span><span class="sxs-lookup"><span data-stu-id="8e90e-159">frameDetached</span></span>  

<span data-ttu-id="8e90e-160">Déclenché lorsque l’image a été détachée de son parent.</span><span class="sxs-lookup"><span data-stu-id="8e90e-160">Fired when frame has been detached from its parent.</span></span>  

| <span data-ttu-id="8e90e-161">Parameters</span><span class="sxs-lookup"><span data-stu-id="8e90e-161">Parameters</span></span> | <span data-ttu-id="8e90e-162">Type</span><span class="sxs-lookup"><span data-stu-id="8e90e-162">Type</span></span> | <span data-ttu-id="8e90e-163">Détails</span><span class="sxs-lookup"><span data-stu-id="8e90e-163">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="8e90e-164">frameId</span><span class="sxs-lookup"><span data-stu-id="8e90e-164">frameId</span></span> | [<span data-ttu-id="8e90e-165">FrameId</span><span class="sxs-lookup"><span data-stu-id="8e90e-165">FrameId</span></span>](#frameid) | <span data-ttu-id="8e90e-166">ID du cadre qui a été détaché.</span><span class="sxs-lookup"><span data-stu-id="8e90e-166">ID of the frame that has been detached.</span></span> |  

---  

### <a name="framenavigated"></a><span data-ttu-id="8e90e-167">frameNavigated</span><span class="sxs-lookup"><span data-stu-id="8e90e-167">frameNavigated</span></span>  

<span data-ttu-id="8e90e-168">Déclenché une fois la navigation de l’image terminée.</span><span class="sxs-lookup"><span data-stu-id="8e90e-168">Fired once navigation of the frame has completed.</span></span>  

| <span data-ttu-id="8e90e-169">Parameters</span><span class="sxs-lookup"><span data-stu-id="8e90e-169">Parameters</span></span> | <span data-ttu-id="8e90e-170">Type</span><span class="sxs-lookup"><span data-stu-id="8e90e-170">Type</span></span> | <span data-ttu-id="8e90e-171">Détails</span><span class="sxs-lookup"><span data-stu-id="8e90e-171">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="8e90e-172">frame</span><span class="sxs-lookup"><span data-stu-id="8e90e-172">frame</span></span> | [<span data-ttu-id="8e90e-173">Trame</span><span class="sxs-lookup"><span data-stu-id="8e90e-173">Frame</span></span>](#frame) | <span data-ttu-id="8e90e-174">Objet Frame.</span><span class="sxs-lookup"><span data-stu-id="8e90e-174">Frame object.</span></span> |  

---  

### <a name="loadeventfired"></a><span data-ttu-id="8e90e-175">loadEventFired</span><span class="sxs-lookup"><span data-stu-id="8e90e-175">loadEventFired</span></span>  

<span data-ttu-id="8e90e-176">Correspond à `window.onload` l’événement.</span><span class="sxs-lookup"><span data-stu-id="8e90e-176">Corresponds to the `window.onload` event.</span></span>  

| <span data-ttu-id="8e90e-177">Parameters</span><span class="sxs-lookup"><span data-stu-id="8e90e-177">Parameters</span></span> | <span data-ttu-id="8e90e-178">Type</span><span class="sxs-lookup"><span data-stu-id="8e90e-178">Type</span></span> | <span data-ttu-id="8e90e-179">Détails</span><span class="sxs-lookup"><span data-stu-id="8e90e-179">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="8e90e-180">timestamp</span><span class="sxs-lookup"><span data-stu-id="8e90e-180">timestamp</span></span> | `number` | <span data-ttu-id="8e90e-181">Nombre de millisecondes depuis l’époque.</span><span class="sxs-lookup"><span data-stu-id="8e90e-181">Number of milliseconds since epoch.</span></span> |  

---  

### <a name="domcontenteventfired"></a><span data-ttu-id="8e90e-182">domContentEventFired</span><span class="sxs-lookup"><span data-stu-id="8e90e-182">domContentEventFired</span></span>  

<span data-ttu-id="8e90e-183">Correspond à `document.onDOMContentLoaded` l’événement.</span><span class="sxs-lookup"><span data-stu-id="8e90e-183">Corresponds to the `document.onDOMContentLoaded` event.</span></span>  

| <span data-ttu-id="8e90e-184">Parameters</span><span class="sxs-lookup"><span data-stu-id="8e90e-184">Parameters</span></span> | <span data-ttu-id="8e90e-185">Type</span><span class="sxs-lookup"><span data-stu-id="8e90e-185">Type</span></span> | <span data-ttu-id="8e90e-186">Détails</span><span class="sxs-lookup"><span data-stu-id="8e90e-186">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="8e90e-187">timestamp</span><span class="sxs-lookup"><span data-stu-id="8e90e-187">timestamp</span></span> | `number` | <span data-ttu-id="8e90e-188">Nombre de millisecondes depuis l’époque.</span><span class="sxs-lookup"><span data-stu-id="8e90e-188">Number of milliseconds since epoch.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="8e90e-189">Types</span><span class="sxs-lookup"><span data-stu-id="8e90e-189">Types</span></span>  

### <a name="frameid-string"></a><span data-ttu-id="8e90e-190">Chaîne FrameId</span><span class="sxs-lookup"><span data-stu-id="8e90e-190">FrameId string</span></span>  

<a name="frameid"></a>  

<span data-ttu-id="8e90e-191">Identificateur d’image unique.</span><span class="sxs-lookup"><span data-stu-id="8e90e-191">Unique frame identifier.</span></span>  

&nbsp;  

---  

### <a name="frame-object"></a><span data-ttu-id="8e90e-192">Objet Frame</span><span class="sxs-lookup"><span data-stu-id="8e90e-192">Frame object</span></span>  

<a name="frame"></a>  

<span data-ttu-id="8e90e-193">Informations sur le cadre de la page.</span><span class="sxs-lookup"><span data-stu-id="8e90e-193">Information about the Frame on the Page.</span></span>  

| <span data-ttu-id="8e90e-194">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8e90e-194">Properties</span></span> | <span data-ttu-id="8e90e-195">Type</span><span class="sxs-lookup"><span data-stu-id="8e90e-195">Type</span></span> | <span data-ttu-id="8e90e-196">Détails</span><span class="sxs-lookup"><span data-stu-id="8e90e-196">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="8e90e-197">id</span><span class="sxs-lookup"><span data-stu-id="8e90e-197">id</span></span> | [<span data-ttu-id="8e90e-198">FrameId</span><span class="sxs-lookup"><span data-stu-id="8e90e-198">FrameId</span></span>](#frameid) | <span data-ttu-id="8e90e-199">Identificateur unique de trame.</span><span class="sxs-lookup"><span data-stu-id="8e90e-199">Frame unique identifier.</span></span> |  
| <span data-ttu-id="8e90e-200">parentId \(facultatif\)</span><span class="sxs-lookup"><span data-stu-id="8e90e-200">parentId \(optional\)</span></span> | [<span data-ttu-id="8e90e-201">FrameId</span><span class="sxs-lookup"><span data-stu-id="8e90e-201">FrameId</span></span>](#frameid) | <span data-ttu-id="8e90e-202">Identificateur unique du cadre parent.</span><span class="sxs-lookup"><span data-stu-id="8e90e-202">Parent frame unique identifier.</span></span> |  
| <span data-ttu-id="8e90e-203">name \(optional\)</span><span class="sxs-lookup"><span data-stu-id="8e90e-203">name \(optional\)</span></span> | `string` | <span data-ttu-id="8e90e-204">Nom du cadre tel que spécifié dans la balise.</span><span class="sxs-lookup"><span data-stu-id="8e90e-204">Frame's name as specified in the tag.</span></span> |  
| <span data-ttu-id="8e90e-205">url</span><span class="sxs-lookup"><span data-stu-id="8e90e-205">url</span></span> | `string` | <span data-ttu-id="8e90e-206">URL du document frame.</span><span class="sxs-lookup"><span data-stu-id="8e90e-206">Frame document's URL.</span></span> |  
| <span data-ttu-id="8e90e-207">securityOrigin</span><span class="sxs-lookup"><span data-stu-id="8e90e-207">securityOrigin</span></span> | `string` | <span data-ttu-id="8e90e-208">Origine de la sécurité du document frame.</span><span class="sxs-lookup"><span data-stu-id="8e90e-208">Frame document's security origin.</span></span> |  
| <span data-ttu-id="8e90e-209">mimeType</span><span class="sxs-lookup"><span data-stu-id="8e90e-209">mimeType</span></span> | `string` | <span data-ttu-id="8e90e-210">MimeType du document frame tel que déterminé par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="8e90e-210">Frame document's mimeType as determined by the browser.</span></span> |  

---  

### <a name="frametree-object"></a><span data-ttu-id="8e90e-211">Objet FrameTree</span><span class="sxs-lookup"><span data-stu-id="8e90e-211">FrameTree object</span></span>  

<a name="frametree"></a>  

<span data-ttu-id="8e90e-212">Informations sur la hiérarchie frame.</span><span class="sxs-lookup"><span data-stu-id="8e90e-212">Information about the Frame hierarchy.</span></span>  

| <span data-ttu-id="8e90e-213">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8e90e-213">Properties</span></span> | <span data-ttu-id="8e90e-214">Type</span><span class="sxs-lookup"><span data-stu-id="8e90e-214">Type</span></span> | <span data-ttu-id="8e90e-215">Détails</span><span class="sxs-lookup"><span data-stu-id="8e90e-215">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="8e90e-216">frame</span><span class="sxs-lookup"><span data-stu-id="8e90e-216">frame</span></span> | [<span data-ttu-id="8e90e-217">Trame</span><span class="sxs-lookup"><span data-stu-id="8e90e-217">Frame</span></span>](#frame) | <span data-ttu-id="8e90e-218">Informations d’image pour cet élément d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="8e90e-218">Frame information for this tree item.</span></span> |  
| <span data-ttu-id="8e90e-219">childFrames \(optional\)</span><span class="sxs-lookup"><span data-stu-id="8e90e-219">childFrames \(optional\)</span></span> | [<span data-ttu-id="8e90e-220">FrameTree[]</span><span class="sxs-lookup"><span data-stu-id="8e90e-220">FrameTree[]</span></span>](#frametree) | <span data-ttu-id="8e90e-221">Images enfants.</span><span class="sxs-lookup"><span data-stu-id="8e90e-221">Child frames.</span></span> |  

---  
