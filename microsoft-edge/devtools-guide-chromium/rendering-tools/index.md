---
description: Les utilisateurs s’attendent à des pages interactives et fluides.  Chaque étape du pipeline de pixels représente une opportunité de présenter jank.  Découvrez les outils et les stratégies permettant d’identifier et de résoudre les problèmes courants qui ralentissent les performances d’exécution.
title: Analyser les performances runtime
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: d5c37c188ae9038a7baafc936d2a02299def6366
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564706"
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
# <a name="analyze-runtime-performance"></a><span data-ttu-id="b6340-106">Analyser les performances runtime</span><span class="sxs-lookup"><span data-stu-id="b6340-106">Analyze runtime performance</span></span>  

<span data-ttu-id="b6340-107">Les utilisateurs s’attendent à des pages interactives et fluides.</span><span class="sxs-lookup"><span data-stu-id="b6340-107">Users expects interactive and smooth pages.</span></span>  <span data-ttu-id="b6340-108">Chaque étape du pipeline de pixels représente une opportunité de présenter jank.</span><span class="sxs-lookup"><span data-stu-id="b6340-108">Each stage in the pixel pipeline represents an opportunity to introduce jank.</span></span>  <span data-ttu-id="b6340-109">Découvrez les outils et les stratégies permettant d’identifier et de résoudre les problèmes courants qui ralentissent les performances d’exécution.</span><span class="sxs-lookup"><span data-stu-id="b6340-109">Learn about tools and strategies to identify and fix common problems that slow down runtime performance.</span></span>  

### <a name="summary"></a><span data-ttu-id="b6340-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="b6340-110">Summary</span></span>  

*   <span data-ttu-id="b6340-111">N’écrivez pas javaScript qui force le navigateur à recalculer la disposition.</span><span class="sxs-lookup"><span data-stu-id="b6340-111">Do not write JavaScript that forces the browser to recalculate layout.</span></span>  <span data-ttu-id="b6340-112">Séparez les fonctions de lecture et d’écriture, puis effectuez d’abord les lectures.</span><span class="sxs-lookup"><span data-stu-id="b6340-112">Separate read and write functions, and perform reads first.</span></span>  
*   <span data-ttu-id="b6340-113">Ne compliquez pas trop votre CSS.</span><span class="sxs-lookup"><span data-stu-id="b6340-113">Do not over-complicate your CSS.</span></span>  <span data-ttu-id="b6340-114">Utilisez moins de CSS et maintenez vos sélecteurs CSS simples.</span><span class="sxs-lookup"><span data-stu-id="b6340-114">Use less CSS and keep your CSS selectors simple.</span></span>  
*   <span data-ttu-id="b6340-115">Évitez autant que possible la disposition.</span><span class="sxs-lookup"><span data-stu-id="b6340-115">Avoid layout as much as possible.</span></span>  <span data-ttu-id="b6340-116">Choisissez CSS qui ne déclenche pas du tout la disposition.</span><span class="sxs-lookup"><span data-stu-id="b6340-116">Choose CSS that does not trigger layout at all.</span></span>  
*   <span data-ttu-id="b6340-117">Le dessin peut prendre plus de temps que toute autre activité de rendu.</span><span class="sxs-lookup"><span data-stu-id="b6340-117">Painting may take up more time than any other rendering activity.</span></span>  <span data-ttu-id="b6340-118">Surveillez les goulots d’étranglement de la couleur.</span><span class="sxs-lookup"><span data-stu-id="b6340-118">Watch out for paint bottlenecks.</span></span>  
    
## <a name="javascript"></a><span data-ttu-id="b6340-119">JavaScript</span><span class="sxs-lookup"><span data-stu-id="b6340-119">JavaScript</span></span>  

<span data-ttu-id="b6340-120">Les calculs JavaScript, en particulier ceux qui déclenchent des modifications visuelles étendues, peuvent entraîner un blocage des performances de l’application.</span><span class="sxs-lookup"><span data-stu-id="b6340-120">JavaScript calculations, especially ones that trigger extensive visual changes, may stall application performance.</span></span>  <span data-ttu-id="b6340-121">Ne laissez pas un JavaScript mal timeé ou de longue durée interférer avec les interactions utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b6340-121">Do not let badly-timed or long-running JavaScript interfere with user interactions.</span></span>  

### <a name="javascript-tools"></a><span data-ttu-id="b6340-122">JavaScript : Outils</span><span class="sxs-lookup"><span data-stu-id="b6340-122">JavaScript: Tools</span></span>  

<span data-ttu-id="b6340-123">Prenez un enregistrement dans l’outil **Performance** et recherchez des événements de longue `Evaluate Script` durée suspects.</span><span class="sxs-lookup"><span data-stu-id="b6340-123">Take a recording in the **Performance** tool and look for suspiciously long `Evaluate Script` events.</span></span>  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

<span data-ttu-id="b6340-124">si vous notez un peu de jank dans votre javaScript, vous devrez peut-être prendre votre analyse au niveau suivant et collecter un profil de processeur JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b6340-124">f you noticing quite a bit of jank in your JavaScript, you may need to take your analysis to the next level and collect a JavaScript CPU profile.</span></span>  <span data-ttu-id="b6340-125">Les profils de processeur indiquent où le runtime est passé dans les fonctions de votre page.</span><span class="sxs-lookup"><span data-stu-id="b6340-125">CPU profiles show where runtime is spent within the functions of your page.</span></span>  <span data-ttu-id="b6340-126">Découvrez comment créer des profils d’UC [dans Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].</span><span class="sxs-lookup"><span data-stu-id="b6340-126">Learn how to create CPU profiles in [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].</span></span>

### <a name="javascript-problems"></a><span data-ttu-id="b6340-127">JavaScript : problèmes</span><span class="sxs-lookup"><span data-stu-id="b6340-127">JavaScript: Problems</span></span>  

<span data-ttu-id="b6340-128">Le tableau suivant décrit certains problèmes JavaScript courants et les solutions potentielles.</span><span class="sxs-lookup"><span data-stu-id="b6340-128">The following table describes some common JavaScript problems and potential solutions.</span></span>  

| <span data-ttu-id="b6340-129">Problème</span><span class="sxs-lookup"><span data-stu-id="b6340-129">Problem</span></span> | <span data-ttu-id="b6340-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="b6340-130">Example</span></span> | <span data-ttu-id="b6340-131">Solution</span><span class="sxs-lookup"><span data-stu-id="b6340-131">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="b6340-132">Des handlers d’entrée coûteux affectent la réponse ou l’animation.</span><span class="sxs-lookup"><span data-stu-id="b6340-132">Expensive input handlers affecting response or animation.</span></span>  | <span data-ttu-id="b6340-133">Tactile, défilement parallaxe.</span><span class="sxs-lookup"><span data-stu-id="b6340-133">Touch, parallax scrolling.</span></span>  | <span data-ttu-id="b6340-134">Laissez le navigateur gérer les effets tactiles et les défilements, ou lier l’écoute aussi tard que possible.</span><span class="sxs-lookup"><span data-stu-id="b6340-134">Let the browser handle touch and scrolls, or bind the listener as late as possible.</span></span>  <span data-ttu-id="b6340-135">Accédez à [Des handlers d’entrée coûteux dans la][WebPerformanceCalendarRuntimeChecklist]liste de contrôle des performances d’exécution de Paul Contrôle.</span><span class="sxs-lookup"><span data-stu-id="b6340-135">Navigate to [Expensive Input Handlers in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  
| <span data-ttu-id="b6340-136">JavaScript mal timed affectant la réponse, l’animation, le chargement.</span><span class="sxs-lookup"><span data-stu-id="b6340-136">Badly-timed JavaScript affecting response, animation, load.</span></span>  | <span data-ttu-id="b6340-137">L’utilisateur défile immédiatement après le chargement de la page, setTimeout/setInterval.</span><span class="sxs-lookup"><span data-stu-id="b6340-137">User scrolls right after page load, setTimeout / setInterval.</span></span>  | <span data-ttu-id="b6340-138">Optimiser le runtime JavaScript : utiliser `requestAnimationFrame` , répartir la manipulation DOM sur des images, utiliser les travailleurs [web][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="b6340-138">Optimize JavaScript runtime: use `requestAnimationFrame`, spread DOM manipulation over frames, use [Web Workers][MDNUsingWebWorkers].</span></span>  |  
| <span data-ttu-id="b6340-139">JavaScript de longue durée affectant la réponse.</span><span class="sxs-lookup"><span data-stu-id="b6340-139">Long-running JavaScript affecting response.</span></span>  | <span data-ttu-id="b6340-140">[L’événement DOMContentLoaded][MDNUsingWebWorkers] se bloque au cours de son travail JS.</span><span class="sxs-lookup"><span data-stu-id="b6340-140">The [DOMContentLoaded event][MDNUsingWebWorkers] stalls as it is swamped with JS work.</span></span>  | <span data-ttu-id="b6340-141">Déplacez le travail de calcul pur vers les [travailleurs web.][MDNUsingWebWorkers]</span><span class="sxs-lookup"><span data-stu-id="b6340-141">Move pure computational work to [Web Workers][MDNUsingWebWorkers].</span></span>  <span data-ttu-id="b6340-142">Si vous avez besoin d’un accès DOM, utilisez `requestAnimationFrame` .</span><span class="sxs-lookup"><span data-stu-id="b6340-142">If you need DOM access, use `requestAnimationFrame`.</span></span>  <!--Navigate to [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| <span data-ttu-id="b6340-143">Scripts garbage-y affectant la réponse ou l’animation.</span><span class="sxs-lookup"><span data-stu-id="b6340-143">Garbage-y scripts affecting response or animation.</span></span>  | <span data-ttu-id="b6340-144">Le garbage collection peut se produire n’importe où.</span><span class="sxs-lookup"><span data-stu-id="b6340-144">Garbage collection may happen anywhere.</span></span>  | <span data-ttu-id="b6340-145">Écrivez moins de scripts garbage-y.</span><span class="sxs-lookup"><span data-stu-id="b6340-145">Write less garbage-y scripts.</span></span>  <span data-ttu-id="b6340-146">Accédez au garbage collection dans Animation dans la liste de contrôle des [performances runtime de Paul Contrôle.][WebPerformanceCalendarRuntimeChecklist]</span><span class="sxs-lookup"><span data-stu-id="b6340-146">Navigate to [Garbage Collection in Animation in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <a name="style"></a><span data-ttu-id="b6340-147">Style</span><span class="sxs-lookup"><span data-stu-id="b6340-147">Style</span></span>  

<span data-ttu-id="b6340-148">Les modifications de style sont coûteuses, en particulier si ces modifications affectent plusieurs éléments dans le DOM.</span><span class="sxs-lookup"><span data-stu-id="b6340-148">Style changes are costly, especially if those changes affect more than one element in the DOM.</span></span>  <span data-ttu-id="b6340-149">Chaque fois que vous appliquez des styles à un élément, le navigateur calcule l’impact sur tous les éléments associés, recalcule la disposition et les repessaint.</span><span class="sxs-lookup"><span data-stu-id="b6340-149">Any time you apply styles to an element, the browser figures out the impact on all related elements, recalculates the layout, and repaints.</span></span>  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <a name="style-tools"></a><span data-ttu-id="b6340-150">Style : Outils</span><span class="sxs-lookup"><span data-stu-id="b6340-150">Style: Tools</span></span>  

<span data-ttu-id="b6340-151">Prenez un enregistrement dans **l’outil Performance.**</span><span class="sxs-lookup"><span data-stu-id="b6340-151">Take a recording in the **Performance** tool.</span></span>  <span data-ttu-id="b6340-152">Vérifiez l’enregistrement des grands `Recalculate Style` événements \(affichés en violet\).</span><span class="sxs-lookup"><span data-stu-id="b6340-152">Check the recording for large `Recalculate Style` events \(displayed in purple\).</span></span>  

<!--todo: add Recording section when available  -->  

<span data-ttu-id="b6340-153">Choisissez un `Recalculate Style` événement pour afficher plus d’informations à son sujet dans le volet **d’informations.**</span><span class="sxs-lookup"><span data-stu-id="b6340-153">Choose a `Recalculate Style` event to view more information about it in the **Details** pane.</span></span>  <span data-ttu-id="b6340-154">Si les modifications de style prennent beaucoup de temps, cela a un effet sur les performances.</span><span class="sxs-lookup"><span data-stu-id="b6340-154">If the style changes are taking a long time, that is a performance hit.</span></span>  <span data-ttu-id="b6340-155">Si les calculs de style affectent un grand nombre d’éléments, il s’agit d’un autre domaine qui peut être amélioré.</span><span class="sxs-lookup"><span data-stu-id="b6340-155">If the style calculations are affecting a large number of elements, that is another area with room for improvement.</span></span>  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Style recalcul long" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="b6340-157">Style recalcul long</span><span class="sxs-lookup"><span data-stu-id="b6340-157">Long recalculate style</span></span>  
:::image-end:::  

<span data-ttu-id="b6340-158">Pour réduire l’impact des `Recalculate Style` événements :</span><span class="sxs-lookup"><span data-stu-id="b6340-158">To reduce the impact of `Recalculate Style` events:</span></span>  

*   <span data-ttu-id="b6340-159">Utilisez les [déclencheurs CSS][CssTriggers] pour savoir quelles propriétés CSS déclenchent la disposition, la couleur et la composite.</span><span class="sxs-lookup"><span data-stu-id="b6340-159">Use the [CSS Triggers][CssTriggers] to learn which CSS properties trigger layout, paint, and composite.</span></span>  <span data-ttu-id="b6340-160">Ces propriétés ont le pire impact sur les performances de rendu.</span><span class="sxs-lookup"><span data-stu-id="b6340-160">These properties have the worst impact on rendering performance.</span></span>  
*   <span data-ttu-id="b6340-161">Basculez vers des propriétés qui ont moins d’impact.</span><span class="sxs-lookup"><span data-stu-id="b6340-161">Switch to properties that have less impact.</span></span>  <!--For more guidance, navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <a name="style-problems"></a><span data-ttu-id="b6340-162">Style : problèmes</span><span class="sxs-lookup"><span data-stu-id="b6340-162">Style: Problems</span></span>  

<span data-ttu-id="b6340-163">Le tableau suivant décrit certains problèmes de style courants et les solutions potentielles.</span><span class="sxs-lookup"><span data-stu-id="b6340-163">The following table describes some common style problems and potential solutions.</span></span>  

| <span data-ttu-id="b6340-164">Problème</span><span class="sxs-lookup"><span data-stu-id="b6340-164">Problem</span></span> | <span data-ttu-id="b6340-165">Exemple</span><span class="sxs-lookup"><span data-stu-id="b6340-165">Example</span></span> | <span data-ttu-id="b6340-166">Solution</span><span class="sxs-lookup"><span data-stu-id="b6340-166">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="b6340-167">Calculs de style coûteux affectant la réponse ou l’animation.</span><span class="sxs-lookup"><span data-stu-id="b6340-167">Expensive style calculations affecting response or animation.</span></span>  | <span data-ttu-id="b6340-168">Toute propriété CSS qui modifie la géométrie d’un élément, comme la largeur, la hauteur ou la position ; le navigateur vérifie tous les autres éléments et recalcule la disposition.</span><span class="sxs-lookup"><span data-stu-id="b6340-168">Any CSS property that changes the geometry of an element, like the width, height, or position; the browser checks all other elements and recalculates the layout.</span></span>  | <span data-ttu-id="b6340-169">Éviter les CSS qui déclenchent des dispositions</span><span class="sxs-lookup"><span data-stu-id="b6340-169">Avoid CSS that triggers layouts</span></span> |  
| <span data-ttu-id="b6340-170">Sélecteurs complexes affectant la réponse ou l’animation.</span><span class="sxs-lookup"><span data-stu-id="b6340-170">Complex selectors affecting response or animation.</span></span>  | <span data-ttu-id="b6340-171">Les sélecteurs imbrmbrés forcent le navigateur à tout savoir sur tous les autres éléments, y compris les parents et les enfants.</span><span class="sxs-lookup"><span data-stu-id="b6340-171">Nested selectors force the browser to know everything about all the other elements, including parents and children.</span></span>  | <span data-ttu-id="b6340-172">Référencez un élément dans votre CSS avec une simple classe.</span><span class="sxs-lookup"><span data-stu-id="b6340-172">Reference an element in your CSS with just a class.</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <a name="layout"></a><span data-ttu-id="b6340-173">Disposition</span><span class="sxs-lookup"><span data-stu-id="b6340-173">Layout</span></span>  

<span data-ttu-id="b6340-174">La disposition (ou le réaflow dans Firefox) est le processus par lequel le navigateur calcule les positions et les tailles de tous les éléments d’une page.</span><span class="sxs-lookup"><span data-stu-id="b6340-174">Layout (or reflow in Firefox) is the process by which the browser calculates the positions and sizes of all the elements on a page.</span></span>  <span data-ttu-id="b6340-175">Le modèle de disposition du site web signifie qu’un élément peut affecter d’autres éléments ; Par exemple, la largeur de l’élément affecte généralement la largeur des éléments enfants, et ainsi de suite, tout en haut et en bas de `<body>` l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="b6340-175">The layout model of the web means that one element may affect others; for example, the width of the `<body>` element typically affects the widths of any child elements, and so on, all the way up and down the tree.</span></span>  <span data-ttu-id="b6340-176">Le processus peut être assez complexe pour le navigateur.</span><span class="sxs-lookup"><span data-stu-id="b6340-176">The process may be quite involved for the browser.</span></span>  

<span data-ttu-id="b6340-177">En règle générale, si vous demandez une valeur géométrique à partir du DOM avant la fin d’une image, vous vous retrouverez avec des « dispositions synchrones forcées », ce qui peut être un goulot d’étranglement important en cas de répétition fréquente ou d’exécution pour une arborescence DOM de grande taille.</span><span class="sxs-lookup"><span data-stu-id="b6340-177">As a general rule of thumb, if you ask for a geometric value back from the DOM before a frame is complete, you are going to find yourself with "forced synchronous layouts", which may be a big performance bottleneck if repeated frequently or performed for a large DOM tree.</span></span>  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <a name="layout-tools"></a><span data-ttu-id="b6340-178">Disposition : outils</span><span class="sxs-lookup"><span data-stu-id="b6340-178">Layout: Tools</span></span>  

<span data-ttu-id="b6340-179">Le **volet Performances** identifie quand une page provoque des mises en page synchrones forcées.</span><span class="sxs-lookup"><span data-stu-id="b6340-179">The **Performance** pane identifies when a page causes forced synchronous layouts.</span></span>  <span data-ttu-id="b6340-180">Ces `Layout` événements sont marqués avec des barres rouges.</span><span class="sxs-lookup"><span data-stu-id="b6340-180">These `Layout` events are marked with red bars.</span></span>  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Disposition synchrone forcée" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="b6340-182">Disposition synchrone forcée</span><span class="sxs-lookup"><span data-stu-id="b6340-182">Forced synchronous layout</span></span>  
:::image-end:::  

<span data-ttu-id="b6340-183">La « disposition de disposition » est une répétition de conditions de disposition synchrones forcées.</span><span class="sxs-lookup"><span data-stu-id="b6340-183">"Layout thrashing" is a repetition of forced synchronous layout conditions.</span></span>  <span data-ttu-id="b6340-184">Cela se produit lorsque JavaScript écrit et lit le DOM à plusieurs reprises, ce qui force le navigateur à recalculer la disposition à plusieurs reprises.</span><span class="sxs-lookup"><span data-stu-id="b6340-184">This occurs when JavaScript writes and reads from the DOM repeatedly, which forces the browser to recalculate the layout over and over.</span></span>  <span data-ttu-id="b6340-185">Pour identifier la disposition, recherchez un modèle de plusieurs avertissements de disposition synchrone forcés.</span><span class="sxs-lookup"><span data-stu-id="b6340-185">To identify layout thrashing, look for a pattern of multiple forced synchronous layout warnings.</span></span>  <span data-ttu-id="b6340-186">Examinez la figure précédente.</span><span class="sxs-lookup"><span data-stu-id="b6340-186">Review the previous figure.</span></span>  

### <a name="layout-problems"></a><span data-ttu-id="b6340-187">Disposition : problèmes</span><span class="sxs-lookup"><span data-stu-id="b6340-187">Layout: Problems</span></span>  

<span data-ttu-id="b6340-188">Le tableau suivant décrit certains problèmes courants de disposition et les solutions potentielles.</span><span class="sxs-lookup"><span data-stu-id="b6340-188">The following table describes some common layout problems and potential solutions.</span></span>  

| <span data-ttu-id="b6340-189">Problème</span><span class="sxs-lookup"><span data-stu-id="b6340-189">Problem</span></span> | <span data-ttu-id="b6340-190">Exemple</span><span class="sxs-lookup"><span data-stu-id="b6340-190">Example</span></span> | <span data-ttu-id="b6340-191">Solution</span><span class="sxs-lookup"><span data-stu-id="b6340-191">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="b6340-192">Disposition synchrone forcée affectant la réponse ou l’animation.</span><span class="sxs-lookup"><span data-stu-id="b6340-192">Forced synchronous layout affecting response or animation.</span></span>  | <span data-ttu-id="b6340-193">Forcer le navigateur à effectuer la disposition plus tôt dans le pipeline de pixels, ce qui entraîne des étapes répétées dans le processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="b6340-193">Forcing the browser to perform layout earlier in the pixel pipeline, resulting in repeating steps in the rendering process.</span></span>  | <span data-ttu-id="b6340-194">Traitement par lots des premières lectures de votre style, puis écritures.</span><span class="sxs-lookup"><span data-stu-id="b6340-194">Batch your style reads first, then do any writes.</span></span>  <!--Navigate to [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| <span data-ttu-id="b6340-195">Disposition affectant la réponse ou l’animation.</span><span class="sxs-lookup"><span data-stu-id="b6340-195">Layout thrashing affecting response or animation.</span></span>  | <span data-ttu-id="b6340-196">Boucle qui place le navigateur dans un cycle de lecture-écriture-lecture-écriture, forçant le navigateur à recalculer la disposition encore et encore.</span><span class="sxs-lookup"><span data-stu-id="b6340-196">A loop that puts the browser into a read-write-read-write cycle, forcing the browser to recalculate layout over and over again.</span></span>  | <span data-ttu-id="b6340-197">Traitement par lot automatique des opérations de lecture-écriture à [l’aide de la bibliothèque FastDom.][GitHubWilsonpageFastdom]</span><span class="sxs-lookup"><span data-stu-id="b6340-197">Automatically batch read-write operations using [FastDom library][GitHubWilsonpageFastdom].</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <a name="paint-and-composite"></a><span data-ttu-id="b6340-198">Paint et composite</span><span class="sxs-lookup"><span data-stu-id="b6340-198">Paint and composite</span></span>  

<span data-ttu-id="b6340-199">Paint est le processus de remplissage des pixels.</span><span class="sxs-lookup"><span data-stu-id="b6340-199">Paint is the process of filling in pixels.</span></span>  <span data-ttu-id="b6340-200">Il s’agit souvent de la partie la plus coûteuse du processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="b6340-200">It is often the most costly part of the rendering process.</span></span>  <span data-ttu-id="b6340-201">Si vous avez remarqué que votre page ne fonctionne pas comme prévu, il est probable que vous avez des problèmes de pinceau.</span><span class="sxs-lookup"><span data-stu-id="b6340-201">If you noticed that your page is not working as designed in any way, it is likely that you have paint problems.</span></span>  

<span data-ttu-id="b6340-202">La composition est l’endroit où les parties peints de la page sont rassemblées pour s’afficher à l’écran.</span><span class="sxs-lookup"><span data-stu-id="b6340-202">Compositing is where the painted parts of the page are put together for displaying on screen.</span></span>  <span data-ttu-id="b6340-203">En grande partie, si vous vous entenez aux propriétés de composition uniquement et que vous évitez de peindre complètement, vous devez remarquer une amélioration majeure des performances, mais vous devez surveiller les nombres excessifs de calques.</span><span class="sxs-lookup"><span data-stu-id="b6340-203">For the most part, if you stick to compositor-only properties and avoid paint altogether, you should notice a major improvement in performance, but you need to watch out for excessive layer counts.</span></span>  <!--Navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <a name="paint-and-composite-tools"></a><span data-ttu-id="b6340-204">Paint composite : outils</span><span class="sxs-lookup"><span data-stu-id="b6340-204">Paint and composite: Tools</span></span>  

<span data-ttu-id="b6340-205">Vous souhaitez savoir combien de temps la peinture prend ou à quelle fréquence le dessin se produit-il ?</span><span class="sxs-lookup"><span data-stu-id="b6340-205">Want to know how long painting takes or how often painting occurs?</span></span>  <span data-ttu-id="b6340-206">Vérifiez le [paramètre Activer l’instrumentation de pinceau][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] avancée dans le panneau **Performances,** puis prenez un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b6340-206">Check the [Enable advanced paint instrumentation][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] setting in the **Performance** panel and then take a recording.</span></span>  <span data-ttu-id="b6340-207">Si la majeure partie de votre temps de rendu est consacrée à la peinture, vous avez des problèmes de dessin.</span><span class="sxs-lookup"><span data-stu-id="b6340-207">If most of your rendering time is spent painting, you have paint problems.</span></span>  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <a name="paint-and-composite-problems"></a><span data-ttu-id="b6340-208">Paint composite : problèmes</span><span class="sxs-lookup"><span data-stu-id="b6340-208">Paint and composite: Problems</span></span>  

<span data-ttu-id="b6340-209">Le tableau suivant décrit certains problèmes courants liés aux images et aux composites, ainsi que les solutions potentielles.</span><span class="sxs-lookup"><span data-stu-id="b6340-209">The following table describes some common paint and composite problems and potential solutions.</span></span>  

| <span data-ttu-id="b6340-210">Problème</span><span class="sxs-lookup"><span data-stu-id="b6340-210">Problem</span></span> | <span data-ttu-id="b6340-211">Exemple</span><span class="sxs-lookup"><span data-stu-id="b6340-211">Example</span></span> | <span data-ttu-id="b6340-212">Solution</span><span class="sxs-lookup"><span data-stu-id="b6340-212">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="b6340-213">Paint tempêtes affectant la réponse ou l’animation.</span><span class="sxs-lookup"><span data-stu-id="b6340-213">Paint storms affecting response or animation.</span></span>  | <span data-ttu-id="b6340-214">Les grandes zones de dessin ou les pinceaux coûteux affectant la réponse ou l’animation.</span><span class="sxs-lookup"><span data-stu-id="b6340-214">Big paint areas or expensive paints affecting response or animation.</span></span>  | <span data-ttu-id="b6340-215">Évitez de peindre, promouvoir les éléments qui se déplacent vers leur propre couche, utiliser des transformations et l’opacité.</span><span class="sxs-lookup"><span data-stu-id="b6340-215">Avoid paint, promote elements that are moving to their own layer, use transforms and opacity.</span></span>  <!--Navigate to [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| <span data-ttu-id="b6340-216">Explosions de couches affectant les animations.</span><span class="sxs-lookup"><span data-stu-id="b6340-216">Layer explosions affecting animations.</span></span>  | <span data-ttu-id="b6340-217">La surpromotion d’un trop grand nombre d’éléments `translateZ(0)` avec une incidence importante sur les performances de l’animation.</span><span class="sxs-lookup"><span data-stu-id="b6340-217">Overpromotion of too many elements with `translateZ(0)` greatly affects animation performance.</span></span>  | <span data-ttu-id="b6340-218">Faites une promotion aux couches avec parcimonie, et uniquement lorsque vous savez qu’elle offre des améliorations concrètes.</span><span class="sxs-lookup"><span data-stu-id="b6340-218">Promote to layers sparingly, and only when you know it offers tangible improvements.</span></span>  <!--Navigate to [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="b6340-219">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="b6340-219">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Accélérer le runtime JavaScript | Documents Microsoft"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#turn-on-advanced-paint-instrumentation "Activer l’instrumentation de pinceau avancée : référence de l’analyse des performances | Documents Microsoft"

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

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Utilisation des outils de | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Liste de vérification des performances d’exécution - Calendrier des performances web"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> <span data-ttu-id="b6340-226">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b6340-226">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b6340-227">La page d’origine est trouvée ici et est co-auteure par [Les Basques DeCénais (Rédacteur][KayceBasques] technique, Chrome DevTools \& Writer\) et [Meggin Kearney][MegginKearney] \(Tech Writer\). [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index)</span><span class="sxs-lookup"><span data-stu-id="b6340-227">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="b6340-229">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b6340-229">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
