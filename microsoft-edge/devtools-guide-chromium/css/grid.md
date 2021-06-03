---
description: Découvrez comment utiliser Microsoft Edge DevTools pour afficher et modifier le CSS d’une page CSS.
title: Inspecter la grille CSS dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 68493fae5e96ef1b2c7ed1205d67fd2b4cf67df5
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564454"
---
# <a name="inspect-css-grid"></a><span data-ttu-id="6460d-104">Inspecter la grille CSS</span><span class="sxs-lookup"><span data-stu-id="6460d-104">Inspect CSS Grid</span></span>  

<span data-ttu-id="6460d-105">Cet article vous explique en détail l’identification des grilles CSS sur un site web et le débogage des problèmes de disposition de grille à l’aide de superpositions de grille personnalisables.</span><span class="sxs-lookup"><span data-stu-id="6460d-105">This article walks you through identifying CSS grids on a website and debugging grid layout issues using customizable grid overlays.</span></span>  

<span data-ttu-id="6460d-106">Les exemples utilisés dans les figures de cet article sont issus des pages web suivantes.</span><span class="sxs-lookup"><span data-stu-id="6460d-106">The examples used in the figures in this article are taken from the following webpages.</span></span>  

*   [<span data-ttu-id="6460d-107">Zone de fruit</span><span class="sxs-lookup"><span data-stu-id="6460d-107">Fruit box</span></span>][JecFyiDemoCssGridFruit]  
*   [<span data-ttu-id="6460d-108">Zone de box</span><span class="sxs-lookup"><span data-stu-id="6460d-108">Snack box</span></span>][JecFyiDemoCssGridSnack]  

## <a name="before-you-begin"></a><span data-ttu-id="6460d-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="6460d-109">Before you begin</span></span>  

<span data-ttu-id="6460d-110">CSS Grid est un paradigme de disposition puissant pour le web.</span><span class="sxs-lookup"><span data-stu-id="6460d-110">CSS Grid is a powerful layout paradigm for the web.</span></span>  <span data-ttu-id="6460d-111">Le guide de disposition de la grille [CSS][MdnCssGridLayout] sur MDN est un excellent point de départ pour apprendre à connaître CSS Grid et les nombreuses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="6460d-111">A great place to get started learning about CSS Grid and the many features is the [CSS Grid Layout guide][MdnCssGridLayout] on MDN.</span></span>  

## <a name="discover-css-grids"></a><span data-ttu-id="6460d-112">Découvrir les grilles CSS</span><span class="sxs-lookup"><span data-stu-id="6460d-112">Discover CSS grids</span></span>  

<span data-ttu-id="6460d-113">Lorsqu’un élément HTML de votre page s’y est appliqué, un badge s’affiche à côté de celui-ci dans le `display: grid` `display: inline-grid` panneau `grid` [Éléments.][DevtoolsGuideChromiumOpen]</span><span class="sxs-lookup"><span data-stu-id="6460d-113">When an HTML element on your page has `display: grid` or `display: inline-grid` applied to it, a `grid` badge is displayed next to it in the [Elements][DevtoolsGuideChromiumOpen] panel.</span></span>  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Découvrir la grille" lightbox="../media/grid-discover-grid.msft.png":::
   <span data-ttu-id="6460d-115">Découvrir la grille</span><span class="sxs-lookup"><span data-stu-id="6460d-115">Discover grid</span></span>  
:::image-end:::  

<span data-ttu-id="6460d-116">Choisissez le badge pour faire bascule l’affichage d’une superposition de grille sur la page.</span><span class="sxs-lookup"><span data-stu-id="6460d-116">Choose the badge to toggle the display of a grid overlay on the page.</span></span>  <span data-ttu-id="6460d-117">La superposition apparaît sur l’élément, disposé comme une grille pour afficher la position des lignes et des pistes de la grille :</span><span class="sxs-lookup"><span data-stu-id="6460d-117">The overlay appears over the element, laid out like a grid to display the position of the grid lines and tracks:</span></span>  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Badge De grille bascule" lightbox="../media/grid-highlight-grid.msft.png":::
   <span data-ttu-id="6460d-119">Badge De grille bascule</span><span class="sxs-lookup"><span data-stu-id="6460d-119">Toggle grid badge</span></span>  
:::image-end:::  

<span data-ttu-id="6460d-120">Ouvrez **le volet** Disposition.</span><span class="sxs-lookup"><span data-stu-id="6460d-120">Open the **Layout** pane.</span></span>  <span data-ttu-id="6460d-121">Lorsque des grilles sont incluses sur une page, le volet De disposition inclut une section **Grille** contenant un certain nombre d’options pour afficher les grilles. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6460d-121">When grids are included on a page, the **Layout** pane includes a **Grid** section containing a number of options for viewing the grids.</span></span>  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Volet de disposition" lightbox="../media/grid-layout-pane.msft.png":::
   <span data-ttu-id="6460d-123">**Volet** de disposition</span><span class="sxs-lookup"><span data-stu-id="6460d-123">**Layout** pane</span></span>  
:::image-end:::  

<span data-ttu-id="6460d-124">La \*\*\*\* section Grille **du** volet Disposition contient les 2 sous-sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="6460d-124">The **Grid** section in the **Layout** pane contains the following 2 sub-sections.</span></span>  

*   <span data-ttu-id="6460d-125">Paramètres d’affichage de superposition</span><span class="sxs-lookup"><span data-stu-id="6460d-125">Overlay display settings</span></span>  
*   <span data-ttu-id="6460d-126">Superpositions de grille</span><span class="sxs-lookup"><span data-stu-id="6460d-126">Grid overlays</span></span>  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## <a name="overlay-display-settings"></a><span data-ttu-id="6460d-127">Paramètres d’affichage de superposition</span><span class="sxs-lookup"><span data-stu-id="6460d-127">Overlay display settings</span></span>  

<span data-ttu-id="6460d-128">Les **paramètres d’affichage Superposition** se composent de 2 parties suivantes.</span><span class="sxs-lookup"><span data-stu-id="6460d-128">The **Overlay display settings** consists of following 2 parts.</span></span>  

*   <span data-ttu-id="6460d-129">Choisissez l’une des options suivantes dans le menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="6460d-129">Choose one of the following options from the dropdown menu.</span></span>  
    
    | <span data-ttu-id="6460d-130">Option de ligne</span><span class="sxs-lookup"><span data-stu-id="6460d-130">Line option</span></span> | <span data-ttu-id="6460d-131">Détails</span><span class="sxs-lookup"><span data-stu-id="6460d-131">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="6460d-132">Masquer les étiquettes de ligne</span><span class="sxs-lookup"><span data-stu-id="6460d-132">Hide line labels</span></span>** | <span data-ttu-id="6460d-133">Masquez les étiquettes des lignes pour chaque superposition de grille.</span><span class="sxs-lookup"><span data-stu-id="6460d-133">Hide the labels of the lines for each grid overlay.</span></span> |  
    | **<span data-ttu-id="6460d-134">Afficher les numéros de ligne</span><span class="sxs-lookup"><span data-stu-id="6460d-134">Show line numbers</span></span>** | <span data-ttu-id="6460d-135">Afficher les numéros des lignes pour chaque superposition de grille \(sélectionné par défaut\).</span><span class="sxs-lookup"><span data-stu-id="6460d-135">Display the numbers of the lines for each grid overlay \(selected by default\).</span></span> |  
    | **<span data-ttu-id="6460d-136">Afficher les noms des lignes</span><span class="sxs-lookup"><span data-stu-id="6460d-136">Show line names</span></span>** | <span data-ttu-id="6460d-137">Affichez les noms des lignes pour chaque superposition de grille lorsque des noms sont fournis.</span><span class="sxs-lookup"><span data-stu-id="6460d-137">Display the names of the lines for each grid overlay when names are provided.</span></span> |  
    
*  <span data-ttu-id="6460d-138">Cochez la case en regard des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="6460d-138">Choose the checkbox next the following options.</span></span>  
    
    | <span data-ttu-id="6460d-139">Option</span><span class="sxs-lookup"><span data-stu-id="6460d-139">Option</span></span> | <span data-ttu-id="6460d-140">Détails</span><span class="sxs-lookup"><span data-stu-id="6460d-140">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="6460d-141">Afficher les tailles des pistes</span><span class="sxs-lookup"><span data-stu-id="6460d-141">Show track sizes</span></span>**  | <span data-ttu-id="6460d-142">Affichez \(ou masquez\) les tailles des pistes.</span><span class="sxs-lookup"><span data-stu-id="6460d-142">Display \(or hide\) the sizes of the tracks.</span></span> |  
    | **<span data-ttu-id="6460d-143">Afficher les noms de zone</span><span class="sxs-lookup"><span data-stu-id="6460d-143">Show area names</span></span>** | <span data-ttu-id="6460d-144">Affichez \(ou masquez\) les noms de la zone, lorsque des noms sont fournis.</span><span class="sxs-lookup"><span data-stu-id="6460d-144">Display \(or hide\) the names of the area, when names are provided.</span></span> |  
    | **<span data-ttu-id="6460d-145">Étendre les lignes de grille</span><span class="sxs-lookup"><span data-stu-id="6460d-145">Extend grid lines</span></span>** | <span data-ttu-id="6460d-146">Affiche \(ou masque\) les extensions de la grille le long de chaque axe.</span><span class="sxs-lookup"><span data-stu-id="6460d-146">Displays \(or hides\) the extensions of the grid dimensions along each axis.</span></span>  <span data-ttu-id="6460d-147">Par défaut, les lignes de grille sont affichées uniquement à l’intérieur de l’élément avec `display: grid` `display: inline-grid` ou CSS définie sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="6460d-147">By default, grid lines are only shown inside the element with `display: grid` or `display: inline-grid` CSS set on it.</span></span> |  
    
<span data-ttu-id="6460d-148">Les sections suivantes fournissent des détails pour chacun des **paramètres d’affichage Superposition.**</span><span class="sxs-lookup"><span data-stu-id="6460d-148">The following sections provide details for each of the **Overlay display settings**.</span></span>  

### <a name="show-line-numbers"></a><span data-ttu-id="6460d-149">Afficher les numéros de ligne</span><span class="sxs-lookup"><span data-stu-id="6460d-149">Show line numbers</span></span>  

<span data-ttu-id="6460d-150">Par défaut, les numéros de ligne positifs et négatifs sont affichés sur la superposition de la grille.</span><span class="sxs-lookup"><span data-stu-id="6460d-150">By default, the positive and negative line numbers are displayed on the grid overlay.</span></span>  

<span data-ttu-id="6460d-151">Pour plus d’informations sur les nombres négatifs dans la superposition de la grille, accédez au placement basé sur une ligne [avec la grille CSS.][MdnLineBasedPlacementCssGrid]</span><span class="sxs-lookup"><span data-stu-id="6460d-151">For more information about negative numbers in the grid overlay, navigate to [Line-based placement with CSS Grid][MdnLineBasedPlacementCssGrid].</span></span>  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Afficher les numéros de ligne" lightbox="../media/grid-show-line-numbers.msft.png":::
   <span data-ttu-id="6460d-153">Afficher les numéros de ligne</span><span class="sxs-lookup"><span data-stu-id="6460d-153">Display line numbers</span></span>  
:::image-end:::  

### <a name="hide-line-labels"></a><span data-ttu-id="6460d-154">Masquer les étiquettes de ligne</span><span class="sxs-lookup"><span data-stu-id="6460d-154">Hide line labels</span></span>  

<span data-ttu-id="6460d-155">Choisissez **Masquer les étiquettes de** ligne pour masquer les numéros de ligne.</span><span class="sxs-lookup"><span data-stu-id="6460d-155">Choose **Hide line labels** to hide the line numbers.</span></span>  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Masquer les étiquettes de ligne" lightbox="../media/grid-hide-line-labels.msft.png":::
   <span data-ttu-id="6460d-157">Masquer les étiquettes de ligne</span><span class="sxs-lookup"><span data-stu-id="6460d-157">Hide line labels</span></span>  
:::image-end:::  

### <a name="show-line-names"></a><span data-ttu-id="6460d-158">Afficher les noms des lignes</span><span class="sxs-lookup"><span data-stu-id="6460d-158">Show line names</span></span>  

<span data-ttu-id="6460d-159">Pour plus d’informations sur les noms de lignes dans la superposition de grille, accédez à Disposition à l’aide de [lignes de grille nommées.][MdnLayoutUsingNamedGridLines]</span><span class="sxs-lookup"><span data-stu-id="6460d-159">For more information about line names in the grid overlay, navigate to [Layout using named grid lines][MdnLayoutUsingNamedGridLines].</span></span>  

<span data-ttu-id="6460d-160">Choisissez **Afficher les noms de ligne** pour afficher les noms de ligne au lieu des nombres.</span><span class="sxs-lookup"><span data-stu-id="6460d-160">Choose **Show line names** to view the line names instead of numbers.</span></span>  <span data-ttu-id="6460d-161">Dans l’exemple, 4 lignes ont des noms `left` : , , et `middle1` `middle2` `right` .</span><span class="sxs-lookup"><span data-stu-id="6460d-161">In the example, 4 lines have names: `left`, `middle1`, `middle2`, and `right`.</span></span>  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Afficher les noms des lignes" lightbox="../media/grid-show-line-names.msft.png":::
   **<span data-ttu-id="6460d-163">Afficher les noms des lignes</span><span class="sxs-lookup"><span data-stu-id="6460d-163">Show line names</span></span>**  
:::image-end:::  

### <a name="show-track-sizes"></a><span data-ttu-id="6460d-164">Afficher les tailles des pistes</span><span class="sxs-lookup"><span data-stu-id="6460d-164">Show track sizes</span></span>  

<span data-ttu-id="6460d-165">Activez la **case à cocher Afficher les tailles** des pistes pour afficher les tailles de piste de la grille.</span><span class="sxs-lookup"><span data-stu-id="6460d-165">Enable the **Show track sizes** checkbox to view the track sizes of the grid.</span></span>  

<span data-ttu-id="6460d-166">DevTools s’affiche `[authored size]` et dans chaque étiquette de `[computed size]` ligne.</span><span class="sxs-lookup"><span data-stu-id="6460d-166">DevTools displays `[authored size]` and `[computed size]` in each line label.</span></span>  

| <span data-ttu-id="6460d-167">Taille</span><span class="sxs-lookup"><span data-stu-id="6460d-167">Size</span></span> | <span data-ttu-id="6460d-168">Détails</span><span class="sxs-lookup"><span data-stu-id="6460d-168">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="6460d-169">taille d’auteur</span><span class="sxs-lookup"><span data-stu-id="6460d-169">authored size</span></span>** | <span data-ttu-id="6460d-170">Taille définie dans la feuille de style \(omise si elle n’est pas définie\).</span><span class="sxs-lookup"><span data-stu-id="6460d-170">The size defined in stylesheet \(omitted if not defined\).</span></span> |  
| **<span data-ttu-id="6460d-171">taille calculée</span><span class="sxs-lookup"><span data-stu-id="6460d-171">computed size</span></span>** | <span data-ttu-id="6460d-172">Taille réelle à l’écran.</span><span class="sxs-lookup"><span data-stu-id="6460d-172">The actual size on screen.</span></span> |  

<span data-ttu-id="6460d-173">Dans la démonstration, les `snack-box` tailles de colonne sont définies dans `grid-template-columns:1fr 2fr;` le CSS.</span><span class="sxs-lookup"><span data-stu-id="6460d-173">In the demo, the `snack-box` column sizes are defined in the `grid-template-columns:1fr 2fr;` CSS.</span></span>  <span data-ttu-id="6460d-174">Par conséquent, les étiquettes de ligne de colonne affichent les tailles calculées et les tailles.</span><span class="sxs-lookup"><span data-stu-id="6460d-174">Therefore, the column line labels display both authored and computed sizes.</span></span>  

| <span data-ttu-id="6460d-175">Suivre la taille</span><span class="sxs-lookup"><span data-stu-id="6460d-175">Track size</span></span> | <span data-ttu-id="6460d-176">Taille de la forme</span><span class="sxs-lookup"><span data-stu-id="6460d-176">Authored size</span></span> | <span data-ttu-id="6460d-177">Taille calculée</span><span class="sxs-lookup"><span data-stu-id="6460d-177">Computed size</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="6460d-178">**1fr** &#x2022; **96,66 px**</span><span class="sxs-lookup"><span data-stu-id="6460d-178">**1fr** &#x2022; **96.66px**</span></span> | <span data-ttu-id="6460d-179">1fr</span><span class="sxs-lookup"><span data-stu-id="6460d-179">1fr</span></span> | <span data-ttu-id="6460d-180">96,66 px</span><span class="sxs-lookup"><span data-stu-id="6460d-180">96.66px</span></span> |  
| <span data-ttu-id="6460d-181">**2fr** &#x2022; **193,32 px**</span><span class="sxs-lookup"><span data-stu-id="6460d-181">**2fr** &#x2022; **193.32px**</span></span> | <span data-ttu-id="6460d-182">2fr</span><span class="sxs-lookup"><span data-stu-id="6460d-182">2fr</span></span> | <span data-ttu-id="6460d-183">193,32 px</span><span class="sxs-lookup"><span data-stu-id="6460d-183">193.32px</span></span> |  

<span data-ttu-id="6460d-184">Les étiquettes de ligne affichent uniquement les tailles calculées, car aucune taille de ligne n’est définie dans la feuille de style.</span><span class="sxs-lookup"><span data-stu-id="6460d-184">The row line labels display only computed sizes, since there are no row sizes defined in the stylesheet.</span></span>  

| <span data-ttu-id="6460d-185">Suivre la taille</span><span class="sxs-lookup"><span data-stu-id="6460d-185">Track size</span></span> | <span data-ttu-id="6460d-186">Taille de la forme</span><span class="sxs-lookup"><span data-stu-id="6460d-186">Authored size</span></span> | <span data-ttu-id="6460d-187">Taille calculée</span><span class="sxs-lookup"><span data-stu-id="6460d-187">Computed size</span></span> |  
|:--- |:--- |:--- |  
| **<span data-ttu-id="6460d-188">80px</span><span class="sxs-lookup"><span data-stu-id="6460d-188">80px</span></span>** | &nbsp;| <span data-ttu-id="6460d-189">80px</span><span class="sxs-lookup"><span data-stu-id="6460d-189">80px</span></span> |  
| **<span data-ttu-id="6460d-190">80px</span><span class="sxs-lookup"><span data-stu-id="6460d-190">80px</span></span>** | &nbsp;| <span data-ttu-id="6460d-191">80px</span><span class="sxs-lookup"><span data-stu-id="6460d-191">80px</span></span> |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Afficher les tailles des pistes" lightbox="../media/grid-show-track-sizes.msft.png":::
   **<span data-ttu-id="6460d-193">Afficher les tailles des pistes</span><span class="sxs-lookup"><span data-stu-id="6460d-193">Show track sizes</span></span>**  
:::image-end:::  

### <a name="show-area-names"></a><span data-ttu-id="6460d-194">Afficher les noms de zone</span><span class="sxs-lookup"><span data-stu-id="6460d-194">Show area names</span></span>  

<span data-ttu-id="6460d-195">Pour afficher les noms de zone, activez la case à cocher Afficher **les noms de** zone.</span><span class="sxs-lookup"><span data-stu-id="6460d-195">To view the area names, enable the **Show area names** checkbox.</span></span>  <span data-ttu-id="6460d-196">Dans l’exemple, il y a 3 zones dans la grille : **haut,** **bas1** et **bas2**.</span><span class="sxs-lookup"><span data-stu-id="6460d-196">In the example, there are 3 areas in the grid: **top**, **bottom1** and **bottom2**.</span></span>  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Afficher les noms de zone" lightbox="../media/grid-show-area-names.msft.png":::
   **<span data-ttu-id="6460d-198">Afficher les noms de zone</span><span class="sxs-lookup"><span data-stu-id="6460d-198">Show area names</span></span>**  
:::image-end:::  

### <a name="extend-grid-lines"></a><span data-ttu-id="6460d-199">Étendre les lignes de grille</span><span class="sxs-lookup"><span data-stu-id="6460d-199">Extend grid lines</span></span>  

<span data-ttu-id="6460d-200">Activez la **case à cocher Étendre** les lignes de la grille pour étendre les lignes de grille au bord de la vue le long de chaque axe.</span><span class="sxs-lookup"><span data-stu-id="6460d-200">Enable the **Extend grid lines** checkbox to extend the grid lines to the edge of the viewport along each axis.</span></span>  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Étendre les lignes de grille" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **<span data-ttu-id="6460d-202">Étendre les lignes de grille</span><span class="sxs-lookup"><span data-stu-id="6460d-202">Extend grid lines</span></span>**  
:::image-end:::  

## <a name="grid-overlays"></a><span data-ttu-id="6460d-203">Superpositions de grille</span><span class="sxs-lookup"><span data-stu-id="6460d-203">Grid overlays</span></span>  

<span data-ttu-id="6460d-204">La section **Superpositions** de grille contient une liste de grilles présentes sur la page, chacune avec une case à cocher, ainsi que différentes options.</span><span class="sxs-lookup"><span data-stu-id="6460d-204">The **Grid overlays** section contains a list of grids that are present on the page, each with a checkbox, along with various options.</span></span>  

### <a name="enable-overlay-views-of-multiple-grids"></a><span data-ttu-id="6460d-205">Activer les affichages de superposition de plusieurs grilles</span><span class="sxs-lookup"><span data-stu-id="6460d-205">Enable overlay views of multiple grids</span></span>  

<span data-ttu-id="6460d-206">Pour afficher la grille de superposition pour plusieurs grilles, cochez la case en regard de chaque nom de la grille.</span><span class="sxs-lookup"><span data-stu-id="6460d-206">To display the overlay grid for multiple grids, choose the checkbox next to each name of the grid.</span></span>  <span data-ttu-id="6460d-207">Dans l’exemple, il existe 2 superpositions de grilles activées qui sont chacune représentées avec des couleurs différentes.</span><span class="sxs-lookup"><span data-stu-id="6460d-207">In the example, there are 2 grid overlays enabled that are each represented with different colors.</span></span>  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Activer les affichages de superposition de plusieurs grilles" lightbox="../media/grid-grid-overlays.msft.png":::
   <span data-ttu-id="6460d-209">Activer les affichages de superposition de plusieurs grilles</span><span class="sxs-lookup"><span data-stu-id="6460d-209">Enable overlay views of multiple grids</span></span>  
:::image-end:::  

### <a name="customize-the-grid-overlay-color"></a><span data-ttu-id="6460d-210">Personnaliser la couleur de superposition de la grille</span><span class="sxs-lookup"><span data-stu-id="6460d-210">Customize the grid overlay color</span></span>  

<span data-ttu-id="6460d-211">Pour ouvrir le s picker de couleurs et personnaliser la couleur de superposition de la grille, sélectionnez la case à côté du nom de la superposition de la grille.</span><span class="sxs-lookup"><span data-stu-id="6460d-211">To open the color picker and customize the grid overlay color, choose the box next to the name of the grid overlay.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Personnaliser la couleur de superposition de la grille" lightbox="../media/grid-grid-overlays-color.msft.png":::
   <span data-ttu-id="6460d-213">Personnaliser la couleur de superposition de la grille</span><span class="sxs-lookup"><span data-stu-id="6460d-213">Customize the grid overlay color</span></span>  
:::image-end:::  

### <a name="highlight-the-grid"></a><span data-ttu-id="6460d-214">Surligner la grille</span><span class="sxs-lookup"><span data-stu-id="6460d-214">Highlight the grid</span></span>  

<span data-ttu-id="6460d-215">Pour mettre en surbrillez l’élément HTML dans l’outil **Elements** et faites-le défiler sur la page web, choisissez l’élément **Show** dans le panneau Éléments \( Afficher l’élément dans l’icône du panneau Éléments ![ ](../media/show-element-in-element-panel-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="6460d-215">To highlight the HTML element in the **Elements** tool and scroll to it on the webpage, choose the **Show element in the Elements panel** \(![Show element in the Elements panel icon](../media/show-element-in-element-panel-icon.msft.png)\) icon.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Surligner la grille" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   <span data-ttu-id="6460d-217">Surligner la grille</span><span class="sxs-lookup"><span data-stu-id="6460d-217">Highlight the grid</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6460d-218">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="6460d-218">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Ouvrez Microsoft Edge devTools | Documents Microsoft"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "Grille CSS | jec.fyi"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "Grille CSS | jec.fyi"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Modèle de disposition de grille CSS | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Disposition à l’aide de lignes de grille nommées | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Placement basé sur une ligne avec grille CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="6460d-225">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6460d-225">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6460d-226">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/grid) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)</span><span class="sxs-lookup"><span data-stu-id="6460d-226">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/grid) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="6460d-228">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6460d-228">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
