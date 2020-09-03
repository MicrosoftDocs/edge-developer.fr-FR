---
description: Les utilisateurs s’attendent à disposer d’une page interactive et lisse.  Chaque étape du pipeline de pixels représente une opportunité de présenter Jank.  Apprenez-en davantage sur les outils et les stratégies permettant d’identifier et de résoudre les problèmes courants qui ralentissent les performances de l’exécution.
title: Analyser les performances du Runtime
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: f7ca848712268110700fac2c5fb75fe1751812bf
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992703"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <span data-ttu-id="5c905-106">Analyser les performances du Runtime</span><span class="sxs-lookup"><span data-stu-id="5c905-106">Analyze runtime performance</span></span> 

<span data-ttu-id="5c905-107">Les utilisateurs s’attendent à disposer d’une page interactive et lisse.</span><span class="sxs-lookup"><span data-stu-id="5c905-107">Users expects interactive and smooth pages.</span></span>  <span data-ttu-id="5c905-108">Chaque étape du pipeline de pixels représente une opportunité de présenter Jank.</span><span class="sxs-lookup"><span data-stu-id="5c905-108">Each stage in the pixel pipeline represents an opportunity to introduce jank.</span></span>  <span data-ttu-id="5c905-109">Apprenez-en davantage sur les outils et les stratégies permettant d’identifier et de résoudre les problèmes courants qui ralentissent les performances de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="5c905-109">Learn about tools and strategies to identify and fix common problems that slow down runtime performance.</span></span>  

### <span data-ttu-id="5c905-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="5c905-110">Summary</span></span>  

*   <span data-ttu-id="5c905-111">N’écrivez pas de code JavaScript qui force le navigateur à recalculer la mise en page.</span><span class="sxs-lookup"><span data-stu-id="5c905-111">Do not write JavaScript that forces the browser to recalculate layout.</span></span>  <span data-ttu-id="5c905-112">Séparez les fonctions de lecture et d’écriture, et effectuez d’abord les lectures.</span><span class="sxs-lookup"><span data-stu-id="5c905-112">Separate read and write functions, and perform reads first.</span></span>  
*   <span data-ttu-id="5c905-113">Ne surchargez pas votre CSS.</span><span class="sxs-lookup"><span data-stu-id="5c905-113">Do not over-complicate your CSS.</span></span>  <span data-ttu-id="5c905-114">Utilisez moins de feuilles de style CSS et conservez les sélecteurs CSS en toute simplicité.</span><span class="sxs-lookup"><span data-stu-id="5c905-114">Use less CSS and keep your CSS selectors simple.</span></span>  
*   <span data-ttu-id="5c905-115">Evitez autant que possible une disposition.</span><span class="sxs-lookup"><span data-stu-id="5c905-115">Avoid layout as much as possible.</span></span>  <span data-ttu-id="5c905-116">Sélectionnez CSS qui ne déclenche aucun déclenchement de disposition.</span><span class="sxs-lookup"><span data-stu-id="5c905-116">Choose CSS that does not trigger layout at all.</span></span>  
*   <span data-ttu-id="5c905-117">Le dessin a pu prendre plus de temps que d’autres activités de rendu.</span><span class="sxs-lookup"><span data-stu-id="5c905-117">Painting may take up more time than any other rendering activity.</span></span>  <span data-ttu-id="5c905-118">Méfiez-vous des goulets d’étranglement.</span><span class="sxs-lookup"><span data-stu-id="5c905-118">Watch out for paint bottlenecks.</span></span>  
    
## <span data-ttu-id="5c905-119">JavaScript</span><span class="sxs-lookup"><span data-stu-id="5c905-119">JavaScript</span></span>  

<span data-ttu-id="5c905-120">Les calculs JavaScript, en particulier ceux qui déclenchent de nombreuses modifications visuelles, risquent de bloquer les performances de l’application.</span><span class="sxs-lookup"><span data-stu-id="5c905-120">JavaScript calculations, especially ones that trigger extensive visual changes, may stall application performance.</span></span>  <span data-ttu-id="5c905-121">Ne laissez pas du temps trop chronométré ou un code JavaScript en cours d’exécution pour les interactions utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5c905-121">Do not let badly-timed or long-running JavaScript interfere with user interactions.</span></span>  

### <span data-ttu-id="5c905-122">JavaScript: outils</span><span class="sxs-lookup"><span data-stu-id="5c905-122">JavaScript: Tools</span></span>  

<span data-ttu-id="5c905-123">Prenez un enregistrement dans le panneau **performance** et recherchez des événements suspects longs `Evaluate Script` .</span><span class="sxs-lookup"><span data-stu-id="5c905-123">Take a recording in the **Performance** panel and look for suspiciously long `Evaluate Script` events.</span></span>  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

<span data-ttu-id="5c905-124">Si vous vous injankz dans votre langage JavaScript, il est possible que vous deviez effectuer votre analyse à un niveau avancé et obtenir un profil d’UC JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5c905-124">f you noticing quite a bit of jank in your JavaScript, you may need to take your analysis to the next level and collect a JavaScript CPU profile.</span></span>  <span data-ttu-id="5c905-125">Les profils d’UC indiquent où le runtime est passé dans les fonctions de votre page.</span><span class="sxs-lookup"><span data-stu-id="5c905-125">CPU profiles show where runtime is spent within the functions of your page.</span></span>  <span data-ttu-id="5c905-126">Apprenez à créer des profils d’UC pour [accélérer le runtime JavaScript][DevtoolsRenderingToolsJavascriptRuntime].</span><span class="sxs-lookup"><span data-stu-id="5c905-126">Learn how to create CPU profiles in [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].</span></span>

### <span data-ttu-id="5c905-127">JavaScript: problèmes</span><span class="sxs-lookup"><span data-stu-id="5c905-127">JavaScript: Problems</span></span>  

<span data-ttu-id="5c905-128">Le tableau suivant décrit certains problèmes courants liés à JavaScript et aux solutions potentielles:</span><span class="sxs-lookup"><span data-stu-id="5c905-128">The following table describes some common JavaScript problems and potential solutions:</span></span>  

| <span data-ttu-id="5c905-129">Problème</span><span class="sxs-lookup"><span data-stu-id="5c905-129">Problem</span></span> | <span data-ttu-id="5c905-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="5c905-130">Example</span></span> | <span data-ttu-id="5c905-131">Solution</span><span class="sxs-lookup"><span data-stu-id="5c905-131">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5c905-132">Gestionnaires d’entrée coûteux affectant la réponse ou l’animation.</span><span class="sxs-lookup"><span data-stu-id="5c905-132">Expensive input handlers affecting response or animation.</span></span>  | <span data-ttu-id="5c905-133">Défilement du son et de la parallaxe.</span><span class="sxs-lookup"><span data-stu-id="5c905-133">Touch, parallax scrolling.</span></span>  | <span data-ttu-id="5c905-134">Laissez le navigateur manipuler les fonctions d’interécouter et de faire défiler ou lier l’écouteur le plus tard possible.</span><span class="sxs-lookup"><span data-stu-id="5c905-134">Let the browser handle touch and scrolls, or bind the listener as late as possible.</span></span>  <span data-ttu-id="5c905-135">Pour plus d' [informations, voir gestionnaires d’entrée coûteux dans la liste de contrôle des performances d’exécution de Paul Lewis][WebPerformanceCalendarRuntimeChecklist].</span><span class="sxs-lookup"><span data-stu-id="5c905-135">See [Expensive Input Handlers in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  
| <span data-ttu-id="5c905-136">JavaScript ayant une temporisation médiocre affectant la réponse, l’animation ou le chargement.</span><span class="sxs-lookup"><span data-stu-id="5c905-136">Badly-timed JavaScript affecting response, animation, load.</span></span>  | <span data-ttu-id="5c905-137">Un utilisateur fait défiler vers la droite après le chargement de la page, setTimeout/setInterval.</span><span class="sxs-lookup"><span data-stu-id="5c905-137">User scrolls right after page load, setTimeout / setInterval.</span></span>  | <span data-ttu-id="5c905-138">Optimiser le runtime JavaScript: utilisez la `requestAnimationFrame` manipulation de Dom par rapport aux trames, utilisez des [travailleurs Web][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="5c905-138">Optimize JavaScript runtime: use `requestAnimationFrame`, spread DOM manipulation over frames, use [Web Workers][MDNUsingWebWorkers].</span></span>  |  
| <span data-ttu-id="5c905-139">JavaScript à exécution longue affectant la réponse.</span><span class="sxs-lookup"><span data-stu-id="5c905-139">Long-running JavaScript affecting response.</span></span>  | <span data-ttu-id="5c905-140">L' [événement DOMContentLoaded][MDNUsingWebWorkers] se bloque car il est libérer avec JS Work.</span><span class="sxs-lookup"><span data-stu-id="5c905-140">The [DOMContentLoaded event][MDNUsingWebWorkers] stalls as it is swamped with JS work.</span></span>  | <span data-ttu-id="5c905-141">Déplacez le travail de calcul pur vers des [travailleurs Web][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="5c905-141">Move pure computational work to [Web Workers][MDNUsingWebWorkers].</span></span>  <span data-ttu-id="5c905-142">Si vous avez besoin d’un accès DOM, utilisez `requestAnimationFrame` .</span><span class="sxs-lookup"><span data-stu-id="5c905-142">If you need DOM access, use `requestAnimationFrame`.</span></span>  <!--See also [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| <span data-ttu-id="5c905-143">Scripts de garbage-y affectant la réponse ou l’animation.</span><span class="sxs-lookup"><span data-stu-id="5c905-143">Garbage-y scripts affecting response or animation.</span></span>  | <span data-ttu-id="5c905-144">Le nettoyage de la mémoire est susceptible de se produire n’importe où.</span><span class="sxs-lookup"><span data-stu-id="5c905-144">Garbage collection may happen anywhere.</span></span>  | <span data-ttu-id="5c905-145">Écrire moins de scripts de nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="5c905-145">Write less garbage-y scripts.</span></span>  <span data-ttu-id="5c905-146">Pour plus d’en voir la [liste de vérification de performance du runtime, voir Nettoyage de][WebPerformanceCalendarRuntimeChecklist]la mémoire dans l’animation.</span><span class="sxs-lookup"><span data-stu-id="5c905-146">See [Garbage Collection in Animation in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <span data-ttu-id="5c905-147">Style</span><span class="sxs-lookup"><span data-stu-id="5c905-147">Style</span></span>  

<span data-ttu-id="5c905-148">Les changements de style sont coûteux, en particulier si ces modifications affectent plusieurs éléments du DOM.</span><span class="sxs-lookup"><span data-stu-id="5c905-148">Style changes are costly, especially if those changes affect more than one element in the DOM.</span></span>  <span data-ttu-id="5c905-149">Chaque fois que vous appliquez des styles à un élément, le navigateur détermine l’impact sur tous les éléments associés, recalcule la disposition et redessine.</span><span class="sxs-lookup"><span data-stu-id="5c905-149">Any time you apply styles to an element, the browser figures out the impact on all related elements, recalculates the layout, and repaints.</span></span>  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <span data-ttu-id="5c905-150">Style: outils</span><span class="sxs-lookup"><span data-stu-id="5c905-150">Style: Tools</span></span>  

<span data-ttu-id="5c905-151">Prenez un enregistrement dans le panneau **performance** .</span><span class="sxs-lookup"><span data-stu-id="5c905-151">Take a recording in the **Performance** panel.</span></span>  <span data-ttu-id="5c905-152">Vérifiez si l’enregistrement comporte des `Recalculate Style` événements volumineux \ (affiché dans Purple \).</span><span class="sxs-lookup"><span data-stu-id="5c905-152">Check the recording for large `Recalculate Style` events \(displayed in purple\).</span></span>  

<!--todo: add Recording section when available  -->  

<span data-ttu-id="5c905-153">Cliquez sur un `Recalculate Style` événement pour afficher des informations supplémentaires le concernant dans le volet **Détails** .</span><span class="sxs-lookup"><span data-stu-id="5c905-153">Click on a `Recalculate Style` event to view more information about it in the **Details** pane.</span></span>  <span data-ttu-id="5c905-154">Si les modifications apportées au style prennent du temps, il s’agit d’un impact sur les performances.</span><span class="sxs-lookup"><span data-stu-id="5c905-154">If the style changes are taking a long time, that is a performance hit.</span></span>  <span data-ttu-id="5c905-155">Si les calculs de style affectent un grand nombre d’éléments, il s’agit d’une autre zone permettant d’améliorer l’espace.</span><span class="sxs-lookup"><span data-stu-id="5c905-155">If the style calculations are affecting a large number of elements, that is another area with room for improvement.</span></span>  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Nouveau style de recalcul" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="5c905-157">Nouveau style de recalcul</span><span class="sxs-lookup"><span data-stu-id="5c905-157">Long recalculate style</span></span>  
:::image-end:::  

<span data-ttu-id="5c905-158">Pour réduire l’impact des `Recalculate Style` événements:</span><span class="sxs-lookup"><span data-stu-id="5c905-158">To reduce the impact of `Recalculate Style` events:</span></span>  

*   <span data-ttu-id="5c905-159">Utilisez les [déclencheurs CSS][CssTriggers] pour découvrir les propriétés CSS déclenchant la mise en page, Paint et composite.</span><span class="sxs-lookup"><span data-stu-id="5c905-159">Use the [CSS Triggers][CssTriggers] to learn which CSS properties trigger layout, paint, and composite.</span></span>  <span data-ttu-id="5c905-160">Ces propriétés présentent le moins d’impact sur les performances de rendu.</span><span class="sxs-lookup"><span data-stu-id="5c905-160">These properties have the worst impact on rendering performance.</span></span>  
*   <span data-ttu-id="5c905-161">Basculez vers les propriétés qui ont moins d’impact.</span><span class="sxs-lookup"><span data-stu-id="5c905-161">Switch to properties that have less impact.</span></span>  <!--See [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties] for more guidance.  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <span data-ttu-id="5c905-162">Style: problèmes</span><span class="sxs-lookup"><span data-stu-id="5c905-162">Style: Problems</span></span>  

<span data-ttu-id="5c905-163">Le tableau suivant décrit certains problèmes de style courants et les solutions possibles:</span><span class="sxs-lookup"><span data-stu-id="5c905-163">The following table describes some common style problems and potential solutions:</span></span>  

| <span data-ttu-id="5c905-164">Problème</span><span class="sxs-lookup"><span data-stu-id="5c905-164">Problem</span></span> | <span data-ttu-id="5c905-165">Exemple</span><span class="sxs-lookup"><span data-stu-id="5c905-165">Example</span></span> | <span data-ttu-id="5c905-166">Solution</span><span class="sxs-lookup"><span data-stu-id="5c905-166">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5c905-167">Calculs de styles coûteux affectant la réponse ou l’animation.</span><span class="sxs-lookup"><span data-stu-id="5c905-167">Expensive style calculations affecting response or animation.</span></span>  | <span data-ttu-id="5c905-168">Toute propriété CSS qui modifie la géométrie d’un élément, comme la largeur, la hauteur ou la position; le navigateur vérifie tous les autres éléments et recalcule la disposition.</span><span class="sxs-lookup"><span data-stu-id="5c905-168">Any CSS property that changes the geometry of an element, like the width, height, or position; the browser checks all other elements and recalculates the layout.</span></span>  | <span data-ttu-id="5c905-169">Éviter les feuilles CSS qui déclenchent des dispositions</span><span class="sxs-lookup"><span data-stu-id="5c905-169">Avoid CSS that triggers layouts</span></span> |  
| <span data-ttu-id="5c905-170">Les sélecteurs complexes affectant la réponse ou l’animation;</span><span class="sxs-lookup"><span data-stu-id="5c905-170">Complex selectors affecting response or animation.</span></span>  | <span data-ttu-id="5c905-171">Les sélecteurs imbriqués forcent le navigateur à savoir tout ce qui se passe sur tous les autres éléments, y compris les parents et les enfants.</span><span class="sxs-lookup"><span data-stu-id="5c905-171">Nested selectors force the browser to know everything about all the other elements, including parents and children.</span></span>  | <span data-ttu-id="5c905-172">Référencez un élément de votre feuille de style CSS en une seule classe.</span><span class="sxs-lookup"><span data-stu-id="5c905-172">Reference an element in your CSS with just a class.</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <span data-ttu-id="5c905-173">Disposition</span><span class="sxs-lookup"><span data-stu-id="5c905-173">Layout</span></span>  

<span data-ttu-id="5c905-174">Le processus de mise en page (ou de réorganisation en Firefox) consiste à faire en sorte que le navigateur calcule les positions et tailles de tous les éléments d’une page.</span><span class="sxs-lookup"><span data-stu-id="5c905-174">Layout (or reflow in Firefox) is the process by which the browser calculates the positions and sizes of all the elements on a page.</span></span>  <span data-ttu-id="5c905-175">Le modèle de disposition du Web signifie qu’un élément est susceptible d’affecter d’autres personnes; par exemple, la largeur de l' `<body>` élément affecte en général la largeur de tout élément enfant, et ainsi de suite, vers le haut et le bas de l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="5c905-175">The layout model of the web means that one element may affect others; for example, the width of the `<body>` element typically affects the widths of any child elements, and so on, all the way up and down the tree.</span></span>  <span data-ttu-id="5c905-176">Le processus risque d’être relativement important pour le navigateur.</span><span class="sxs-lookup"><span data-stu-id="5c905-176">The process may be quite involved for the browser.</span></span>  

<span data-ttu-id="5c905-177">En règle générale, si vous demandez une valeur géométrique à partir du DOM avant la fin de l’opération, vous devez vous trouver avec les «dispositions asynchrones forcées», ce qui peut s’avérer un goulet d’étranglement important des performances s’il est répété fréquemment ou exécuté pour une grande arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="5c905-177">As a general rule of thumb, if you ask for a geometric value back from the DOM before a frame is complete, you are going to find yourself with "forced synchronous layouts", which may be a big performance bottleneck if repeated frequently or performed for a large DOM tree.</span></span>  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <span data-ttu-id="5c905-178">Mise en page: outils</span><span class="sxs-lookup"><span data-stu-id="5c905-178">Layout: Tools</span></span>  

<span data-ttu-id="5c905-179">Le volet **performances** détermine quand une page génère des dispositions asynchrones forcées.</span><span class="sxs-lookup"><span data-stu-id="5c905-179">The **Performance** pane identifies when a page causes forced synchronous layouts.</span></span>  <span data-ttu-id="5c905-180">Ces `Layout` événements sont signalés par des barres rouges.</span><span class="sxs-lookup"><span data-stu-id="5c905-180">These `Layout` events are marked with red bars.</span></span>  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Disposition asynchrone forcée" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="5c905-182">Disposition asynchrone forcée</span><span class="sxs-lookup"><span data-stu-id="5c905-182">Forced synchronous layout</span></span>  
:::image-end:::  

<span data-ttu-id="5c905-183">«La surcharge de disposition» est une répétition de conditions de disposition asynchrones forcées.</span><span class="sxs-lookup"><span data-stu-id="5c905-183">"Layout thrashing" is a repetition of forced synchronous layout conditions.</span></span>  <span data-ttu-id="5c905-184">Cela se produit lorsque JavaScript écrit et lit à plusieurs reprises du DOM, ce qui force le navigateur à recalculer la mise en page.</span><span class="sxs-lookup"><span data-stu-id="5c905-184">This occurs when JavaScript writes and reads from the DOM repeatedly, which forces the browser to recalculate the layout over and over.</span></span>  <span data-ttu-id="5c905-185">Pour identifier la surcharge de la disposition, recherchez un modèle de multiples avertissements relatifs à la disposition asynchrone forcés.</span><span class="sxs-lookup"><span data-stu-id="5c905-185">To identify layout thrashing, look for a pattern of multiple forced synchronous layout warnings.</span></span>  <span data-ttu-id="5c905-186">Voir la figure précédente.</span><span class="sxs-lookup"><span data-stu-id="5c905-186">See the previous figure.</span></span>  

### <span data-ttu-id="5c905-187">Mise en page: problèmes</span><span class="sxs-lookup"><span data-stu-id="5c905-187">Layout: Problems</span></span>  

<span data-ttu-id="5c905-188">Le tableau suivant décrit certains problèmes courants liés à la mise en page et les solutions potentielles:</span><span class="sxs-lookup"><span data-stu-id="5c905-188">The following table describes some common layout problems and potential solutions:</span></span>  

| <span data-ttu-id="5c905-189">Problème</span><span class="sxs-lookup"><span data-stu-id="5c905-189">Problem</span></span> | <span data-ttu-id="5c905-190">Exemple</span><span class="sxs-lookup"><span data-stu-id="5c905-190">Example</span></span> | <span data-ttu-id="5c905-191">Solution</span><span class="sxs-lookup"><span data-stu-id="5c905-191">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5c905-192">Disposition asynchrone forcée affectant une réponse ou une animation.</span><span class="sxs-lookup"><span data-stu-id="5c905-192">Forced synchronous layout affecting response or animation.</span></span>  | <span data-ttu-id="5c905-193">Forcer le navigateur à effectuer une disposition antérieure dans le pipeline de pixels, ce qui se traduit par des étapes répétées dans le processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="5c905-193">Forcing the browser to perform layout earlier in the pixel pipeline, resulting in repeating steps in the rendering process.</span></span>  | <span data-ttu-id="5c905-194">Par lot, le style est lu en premier, puis les écritures éventuelles.</span><span class="sxs-lookup"><span data-stu-id="5c905-194">Batch your style reads first, then do any writes.</span></span>  <!--See also [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| <span data-ttu-id="5c905-195">Surcharge de disposition affectant la réponse ou l’animation.</span><span class="sxs-lookup"><span data-stu-id="5c905-195">Layout thrashing affecting response or animation.</span></span>  | <span data-ttu-id="5c905-196">Boucle qui place le navigateur dans un cycle en lecture/écriture en lecture/écriture, ce qui force le navigateur à recalculer la mise en page.</span><span class="sxs-lookup"><span data-stu-id="5c905-196">A loop that puts the browser into a read-write-read-write cycle, forcing the browser to recalculate layout over and over again.</span></span>  | <span data-ttu-id="5c905-197">Effectuer automatiquement des opérations par lot en lecture/écriture à l’aide de la [bibliothèque FastDom][GitHubWilsonpageFastdom].</span><span class="sxs-lookup"><span data-stu-id="5c905-197">Automatically batch read-write operations using [FastDom library][GitHubWilsonpageFastdom].</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <span data-ttu-id="5c905-198">Peintures et composites</span><span class="sxs-lookup"><span data-stu-id="5c905-198">Paint and composite</span></span>  

<span data-ttu-id="5c905-199">Paint est le processus de remplissage en pixels.</span><span class="sxs-lookup"><span data-stu-id="5c905-199">Paint is the process of filling in pixels.</span></span>  <span data-ttu-id="5c905-200">Il s’agit souvent de la partie la plus coûteuse du processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="5c905-200">It is often the most costly part of the rendering process.</span></span>  <span data-ttu-id="5c905-201">Si vous avez remarqué que votre page est Janky de quelque manière que ce soit, il est probable que vous rencontriez des problèmes de peintures.</span><span class="sxs-lookup"><span data-stu-id="5c905-201">If you noticed that your page is janky in any way, it is likely that you have paint problems.</span></span>  

<span data-ttu-id="5c905-202">La composition consiste à placer les parties peintes de la page pour l’affichage à l’écran.</span><span class="sxs-lookup"><span data-stu-id="5c905-202">Compositing is where the painted parts of the page are put together for displaying on screen.</span></span>  <span data-ttu-id="5c905-203">Dans la plupart des cas, si vous respectez les propriétés de composition unique et que vous n’êtes pas obligé de peindre entièrement, vous devriez constater une amélioration majeure de la performance, mais vous devez prendre en compte pour un nombre excessif de couches.</span><span class="sxs-lookup"><span data-stu-id="5c905-203">For the most part, if you stick to compositor-only properties and avoid paint altogether, you should see a major improvement in performance, but you need to watch out for excessive layer counts.</span></span>  <!--See also [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <span data-ttu-id="5c905-204">Peintures et composites: outils</span><span class="sxs-lookup"><span data-stu-id="5c905-204">Paint and composite: Tools</span></span>  

<span data-ttu-id="5c905-205">Vous voulez connaître le nombre de fois que le dessin a lieu ou la fréquence à laquelle le dessin se produit?</span><span class="sxs-lookup"><span data-stu-id="5c905-205">Want to know how long painting takes or how often painting occurs?</span></span>  <span data-ttu-id="5c905-206">Activez le paramètre [activer l’instrumentation avancée de peinture][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] dans le panneau de **performance** , puis prenez un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="5c905-206">Check the [Enable advanced paint instrumentation][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] setting in the **Performance** panel and then take a recording.</span></span>  <span data-ttu-id="5c905-207">Si la plupart du temps de rendu est dépensé, vous rencontrez des problèmes de peinture.</span><span class="sxs-lookup"><span data-stu-id="5c905-207">If most of your rendering time is spent painting, you have paint problems.</span></span>  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <span data-ttu-id="5c905-208">Peintures et composites: problèmes</span><span class="sxs-lookup"><span data-stu-id="5c905-208">Paint and composite: Problems</span></span>  

<span data-ttu-id="5c905-209">Le tableau suivant décrit certains problèmes courants liés aux peintures et composites et aux solutions potentielles:</span><span class="sxs-lookup"><span data-stu-id="5c905-209">The following table describes some common paint and composite problems and potential solutions:</span></span>  

| <span data-ttu-id="5c905-210">Problème</span><span class="sxs-lookup"><span data-stu-id="5c905-210">Problem</span></span> | <span data-ttu-id="5c905-211">Exemple</span><span class="sxs-lookup"><span data-stu-id="5c905-211">Example</span></span> | <span data-ttu-id="5c905-212">Solution</span><span class="sxs-lookup"><span data-stu-id="5c905-212">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5c905-213">Les orages de peintures affectant la réponse ou l’animation.</span><span class="sxs-lookup"><span data-stu-id="5c905-213">Paint storms affecting response or animation.</span></span>  | <span data-ttu-id="5c905-214">Des grandes zones de peinture ou des peintures onéreuses affectant une réponse ou une animation.</span><span class="sxs-lookup"><span data-stu-id="5c905-214">Big paint areas or expensive paints affecting response or animation.</span></span>  | <span data-ttu-id="5c905-215">Evitez de peindre, promouvez des éléments qui se déplacent vers leur propre calque, utilisez les transformations et l’opacité.</span><span class="sxs-lookup"><span data-stu-id="5c905-215">Avoid paint, promote elements that are moving to their own layer, use transforms and opacity.</span></span>  <!--See [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| <span data-ttu-id="5c905-216">Explosions de couches affectant les animations.</span><span class="sxs-lookup"><span data-stu-id="5c905-216">Layer explosions affecting animations.</span></span>  | <span data-ttu-id="5c905-217">La promotion d’un trop grand nombre d’éléments `translateZ(0)` affectait sensiblement les performances de l’animation.</span><span class="sxs-lookup"><span data-stu-id="5c905-217">Overpromotion of too many elements with `translateZ(0)` greatly affects animation performance.</span></span>  | <span data-ttu-id="5c905-218">Promouvez vos couches avec modération, et ce n’est qu’une seule fois que vous savez qu’elle offre des améliorations tangibles.</span><span class="sxs-lookup"><span data-stu-id="5c905-218">Promote to layers sparingly, and only when you know it offers tangible improvements.</span></span>  <!--See [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## <span data-ttu-id="5c905-219">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="5c905-219">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Accélérer le runtime JavaScript | Documents Microsoft"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#enable-advanced-paint-instrumentation "Activer l’instrumentation avancée de peinture-référence d’analyse des performances | Documents Microsoft"

<!--[DevtoolsRenderingToolsForcedSynchronousLayouts]: ./rendering-tools/forced-synchronous-layouts.md "Diagnose Forced Synchronous Layouts | Microsoft Docs"  -->  

<!-- The Timeline Tool page is deprecated  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfileJavascript]: ../evaluate-performance/timeline-tool#profile-javascript "Profile JavaScript - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfilePainting]: ../evaluate-performance/timeline-tool#profile-painting "Profile painting - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRecording]: ../evaluate-performance/timeline-tool#make-a-recording "Make a recording - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRenderingSettings]: ../evaluate-performance/timeline-tool#rendering-settings "Rendering settings - How to Use the Timeline Tool | Microsoft Docs"  -->  

<!--[WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing "Avoid Large, Complex Layouts, and Layout Thrashing"  -->  
<!--[WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime]: /web/fundamentals/performance/rendering/optimize-javascript-execution "Optimize JavaScript Runtime"  -->  
<!--[WebFundamentalsPerformanceRenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations "Reduce the Scope and Complexity of Style Calculations"  -->  
<!--[WebFundamentalsPerformanceRenderingSimplifyPaintComplexity]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas "Simplify Paint Complexity and Reduce Paint Areas"  -->  
<!--[WebFundamentalsPerformanceRenderingCompositorOnlyProperties]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count "Stick to Compositor-Only Properties and Manage Layer Count"  -->  

[CssTriggers]: https://csstriggers.com "Déclencheurs CSS"  

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Utilisation des travailleurs sur le Web | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Liste de contrôle de performance du runtime-calendrier des performances du Web"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> <span data-ttu-id="5c905-226">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5c905-226">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5c905-227">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \) et [Meggin Kearney][MegginKearney] \ (Technical Writer \).</span><span class="sxs-lookup"><span data-stu-id="5c905-227">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="5c905-229">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5c905-229">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
