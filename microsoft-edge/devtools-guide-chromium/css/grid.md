---
description: Découvrez comment utiliser Microsoft Edge DevTools pour afficher et modifier la CSS d’une page CSS.
title: Examiner la grille CSS dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 1fe6bd1c8efd244315fb9a38777df6ea3e9b1a4d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231096"
---
# <span data-ttu-id="618fe-104">Inspecter la grille CSS</span><span class="sxs-lookup"><span data-stu-id="618fe-104">Inspect CSS Grid</span></span>  

<span data-ttu-id="618fe-105">Cet article vous guide tout au long de l’identification des grilles de CSS sur un site Web et au débogage des problèmes de disposition de grille à l’aide de superpositions de grille personnalisées.</span><span class="sxs-lookup"><span data-stu-id="618fe-105">This article walks you through identifying CSS grids on a website and debugging grid layout issues using customizable grid overlays.</span></span>  

<span data-ttu-id="618fe-106">Les exemples présentés dans cet article sont tirés des pages Web suivantes.</span><span class="sxs-lookup"><span data-stu-id="618fe-106">The examples used in the figures in this article are taken from the following webpages.</span></span>  

*   [<span data-ttu-id="618fe-107">Champ fruit</span><span class="sxs-lookup"><span data-stu-id="618fe-107">Fruit box</span></span>][JecFyiDemoCssGridFruit]  
*   [<span data-ttu-id="618fe-108">Zone collation</span><span class="sxs-lookup"><span data-stu-id="618fe-108">Snack box</span></span>][JecFyiDemoCssGridSnack]  

## <span data-ttu-id="618fe-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="618fe-109">Before you begin</span></span>  

<span data-ttu-id="618fe-110">Grille CSS est un paradigme de disposition puissant pour le Web.</span><span class="sxs-lookup"><span data-stu-id="618fe-110">CSS Grid is a powerful layout paradigm for the web.</span></span>  <span data-ttu-id="618fe-111">Pour commencer à vous familiariser avec la grille CSS et les nombreuses fonctionnalités, consultez le Guide de disposition de la [grille CSS][MdnCssGridLayout] sur MDN.</span><span class="sxs-lookup"><span data-stu-id="618fe-111">A great place to get started learning about CSS Grid and the many features is the [CSS Grid Layout guide][MdnCssGridLayout] on MDN.</span></span>  

## <span data-ttu-id="618fe-112">Découvrir les grilles CSS</span><span class="sxs-lookup"><span data-stu-id="618fe-112">Discover CSS grids</span></span>  

<span data-ttu-id="618fe-113">Lorsqu’un élément HTML de votre page l’a `display: grid` ou `display: inline-grid` lui est appliqué, un `grid` badge s’affiche à côté de celui-ci dans le panneau [éléments][DevtoolsGuideChromiumOpen] .</span><span class="sxs-lookup"><span data-stu-id="618fe-113">When an HTML element on your page has `display: grid` or `display: inline-grid` applied to it, a `grid` badge is displayed next to it in the [Elements][DevtoolsGuideChromiumOpen] panel.</span></span>  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Découvrir la grille" lightbox="../media/grid-discover-grid.msft.png":::
   <span data-ttu-id="618fe-115">Découvrir la grille</span><span class="sxs-lookup"><span data-stu-id="618fe-115">Discover grid</span></span>  
:::image-end:::  

<span data-ttu-id="618fe-116">Sélectionnez le badge pour basculer vers l’affichage d’une superposition de grille sur la page.</span><span class="sxs-lookup"><span data-stu-id="618fe-116">Select the badge to toggle the display of a grid overlay on the page.</span></span>  <span data-ttu-id="618fe-117">La superposition s’affiche au-dessus de l’élément, disposé comme une grille pour afficher la position des lignes et des pistes de la grille:</span><span class="sxs-lookup"><span data-stu-id="618fe-117">The overlay appears over the element, laid out like a grid to display the position of the grid lines and tracks:</span></span>  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Activer/désactiver le badge de grille" lightbox="../media/grid-highlight-grid.msft.png":::
   <span data-ttu-id="618fe-119">Activer/désactiver le badge de grille</span><span class="sxs-lookup"><span data-stu-id="618fe-119">Toggle grid badge</span></span>  
:::image-end:::  

<span data-ttu-id="618fe-120">Ouvrir le volet **disposition**</span><span class="sxs-lookup"><span data-stu-id="618fe-120">Open the **Layout** pane.</span></span>  <span data-ttu-id="618fe-121">Lorsque les grilles sont incluses sur une page, le volet **disposition** inclut une section **grille** contenant un certain nombre d’options pour afficher les grilles.</span><span class="sxs-lookup"><span data-stu-id="618fe-121">When grids are included on a page, the **Layout** pane includes a **Grid** section containing a number of options for viewing the grids.</span></span>  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Volet disposition" lightbox="../media/grid-layout-pane.msft.png":::
   <span data-ttu-id="618fe-123">Volet **disposition**</span><span class="sxs-lookup"><span data-stu-id="618fe-123">**Layout** pane</span></span>  
:::image-end:::  

<span data-ttu-id="618fe-124">La section **grille** du volet **disposition** contient les 2 sous-sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="618fe-124">The **Grid** section in the **Layout** pane contains the following 2 sub-sections.</span></span>  

*   <span data-ttu-id="618fe-125">Paramètres d’affichage de la superposition</span><span class="sxs-lookup"><span data-stu-id="618fe-125">Overlay display settings</span></span>  
*   <span data-ttu-id="618fe-126">Superpositions de grille</span><span class="sxs-lookup"><span data-stu-id="618fe-126">Grid overlays</span></span>  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## <span data-ttu-id="618fe-127">Paramètres d’affichage de la superposition</span><span class="sxs-lookup"><span data-stu-id="618fe-127">Overlay display settings</span></span>  

<span data-ttu-id="618fe-128">Les **paramètres d’affichage de la superposition** se composent de 2 parties suivantes.</span><span class="sxs-lookup"><span data-stu-id="618fe-128">The **Overlay display settings** consists of following 2 parts.</span></span>  

*   <span data-ttu-id="618fe-129">Dans le menu déroulant, choisissez l’une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="618fe-129">Choose one of the following options from the dropdown menu.</span></span>  
    
    | <span data-ttu-id="618fe-130">Option ligne</span><span class="sxs-lookup"><span data-stu-id="618fe-130">Line option</span></span> | <span data-ttu-id="618fe-131">Détails</span><span class="sxs-lookup"><span data-stu-id="618fe-131">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="618fe-132">Masquer les étiquettes de lignes</span><span class="sxs-lookup"><span data-stu-id="618fe-132">Hide line labels</span></span>** | <span data-ttu-id="618fe-133">Masquez les étiquettes des lignes pour chaque superposition de grille.</span><span class="sxs-lookup"><span data-stu-id="618fe-133">Hide the labels of the lines for each grid overlay.</span></span> |  
    | **<span data-ttu-id="618fe-134">Afficher les numéros de ligne</span><span class="sxs-lookup"><span data-stu-id="618fe-134">Show line numbers</span></span>** | <span data-ttu-id="618fe-135">Afficher les numéros des lignes pour chaque superposition de la grille \ (option activée par défaut).</span><span class="sxs-lookup"><span data-stu-id="618fe-135">Display the numbers of the lines for each grid overlay \(selected by default\).</span></span> |  
    | **<span data-ttu-id="618fe-136">Afficher les noms de lignes</span><span class="sxs-lookup"><span data-stu-id="618fe-136">Show line names</span></span>** | <span data-ttu-id="618fe-137">Afficher les noms des lignes pour chaque superposition de grille lorsque les noms sont fournis.</span><span class="sxs-lookup"><span data-stu-id="618fe-137">Display the names of the lines for each grid overlay when names are provided.</span></span> |  
    
*  <span data-ttu-id="618fe-138">Cochez la case en regard des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="618fe-138">Choose the checkbox next the following options.</span></span>  
    
    | <span data-ttu-id="618fe-139">Option</span><span class="sxs-lookup"><span data-stu-id="618fe-139">Option</span></span> | <span data-ttu-id="618fe-140">Détails</span><span class="sxs-lookup"><span data-stu-id="618fe-140">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="618fe-141">Afficher les tailles de suivi</span><span class="sxs-lookup"><span data-stu-id="618fe-141">Show track sizes</span></span>**  | <span data-ttu-id="618fe-142">Afficher \ (ou masquer \) les tailles des pistes.</span><span class="sxs-lookup"><span data-stu-id="618fe-142">Display \(or hide\) the sizes of the tracks.</span></span> |  
    | **<span data-ttu-id="618fe-143">Afficher les noms des zones</span><span class="sxs-lookup"><span data-stu-id="618fe-143">Show area names</span></span>** | <span data-ttu-id="618fe-144">Afficher \ (ou masquer \) le nom de la zone lorsque des noms sont fournis.</span><span class="sxs-lookup"><span data-stu-id="618fe-144">Display \(or hide\) the names of the area, when names are provided.</span></span> |  
    | **<span data-ttu-id="618fe-145">Prolonger le quadrillage</span><span class="sxs-lookup"><span data-stu-id="618fe-145">Extend grid lines</span></span>** | <span data-ttu-id="618fe-146">Affiche \ (ou masque) les extensions des dimensions de la grille le long de chaque axe.</span><span class="sxs-lookup"><span data-stu-id="618fe-146">Displays \(or hides\) the extensions of the grid dimensions along each axis.</span></span>  <span data-ttu-id="618fe-147">Par défaut, les lignes de grille apparaissent uniquement à l’intérieur de l’élément avec `display: grid` ou des `display: inline-grid` styles CSS définis sur celle-ci.</span><span class="sxs-lookup"><span data-stu-id="618fe-147">By default, grid lines are only shown inside the element with `display: grid` or `display: inline-grid` CSS set on it.</span></span> |  
    
<span data-ttu-id="618fe-148">Les sections suivantes fournissent des détails sur chacun des **paramètres d’affichage de la superposition**.</span><span class="sxs-lookup"><span data-stu-id="618fe-148">The following sections provide details for each of the **Overlay display settings**.</span></span>  

### <span data-ttu-id="618fe-149">Afficher les numéros de ligne</span><span class="sxs-lookup"><span data-stu-id="618fe-149">Show line numbers</span></span>  

<span data-ttu-id="618fe-150">Par défaut, les nombres de lignes positifs et négatifs sont affichés dans la superposition de la grille.</span><span class="sxs-lookup"><span data-stu-id="618fe-150">By default, the positive and negative line numbers are displayed on the grid overlay.</span></span>  

<span data-ttu-id="618fe-151">Pour plus d’informations sur les nombres négatifs dans la superposition de la grille, voir [placement en ligne avec CSS Grid][MdnLineBasedPlacementCssGrid].</span><span class="sxs-lookup"><span data-stu-id="618fe-151">For more information about negative numbers in the grid overlay, navigate to [Line-based placement with CSS Grid][MdnLineBasedPlacementCssGrid].</span></span>  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Afficher les numéros de ligne" lightbox="../media/grid-show-line-numbers.msft.png":::
   <span data-ttu-id="618fe-153">Afficher les numéros de ligne</span><span class="sxs-lookup"><span data-stu-id="618fe-153">Display line numbers</span></span>  
:::image-end:::  

### <span data-ttu-id="618fe-154">Masquer les étiquettes de lignes</span><span class="sxs-lookup"><span data-stu-id="618fe-154">Hide line labels</span></span>  

<span data-ttu-id="618fe-155">Pour masquer les numéros de ligne, sélectionnez **Masquer les étiquettes de lignes** .</span><span class="sxs-lookup"><span data-stu-id="618fe-155">Select **Hide line labels** to hide the line numbers.</span></span>  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Masquer les étiquettes de lignes" lightbox="../media/grid-hide-line-labels.msft.png":::
   <span data-ttu-id="618fe-157">Masquer les étiquettes de lignes</span><span class="sxs-lookup"><span data-stu-id="618fe-157">Hide line labels</span></span>  
:::image-end:::  

### <span data-ttu-id="618fe-158">Afficher les noms de lignes</span><span class="sxs-lookup"><span data-stu-id="618fe-158">Show line names</span></span>  

<span data-ttu-id="618fe-159">Pour plus d’informations sur les noms de lignes dans la superposition de grille, accédez à [disposition à l’aide de l’intitulé lignes de grille][MdnLayoutUsingNamedGridLines].</span><span class="sxs-lookup"><span data-stu-id="618fe-159">For more information about line names in the grid overlay, navigate to [Layout using named grid lines][MdnLayoutUsingNamedGridLines].</span></span>  

<span data-ttu-id="618fe-160">Sélectionnez **afficher les noms des lignes** pour afficher les noms de lignes au lieu de nombres.</span><span class="sxs-lookup"><span data-stu-id="618fe-160">Select **Show line names** to view the line names instead of numbers.</span></span>  <span data-ttu-id="618fe-161">Dans l’exemple, quatre lignes portent des noms: `left` , `middle1` ,, `middle2` et `right` .</span><span class="sxs-lookup"><span data-stu-id="618fe-161">In the example, 4 lines have names: `left`, `middle1`, `middle2`, and `right`.</span></span>  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Afficher les noms de lignes" lightbox="../media/grid-show-line-names.msft.png":::
   **<span data-ttu-id="618fe-163">Afficher les noms de lignes</span><span class="sxs-lookup"><span data-stu-id="618fe-163">Show line names</span></span>**  
:::image-end:::  

### <span data-ttu-id="618fe-164">Afficher les tailles de suivi</span><span class="sxs-lookup"><span data-stu-id="618fe-164">Show track sizes</span></span>  

<span data-ttu-id="618fe-165">Activez la case à cocher **afficher les tailles de suivi** pour afficher les tailles de suivi de la grille.</span><span class="sxs-lookup"><span data-stu-id="618fe-165">Enable the **Show track sizes** checkbox to view the track sizes of the grid.</span></span>  

<span data-ttu-id="618fe-166">DevTools affiche `[authored size]` et `[computed size]` dans chaque étiquette de ligne.</span><span class="sxs-lookup"><span data-stu-id="618fe-166">DevTools displays `[authored size]` and `[computed size]` in each line label.</span></span>  

| <span data-ttu-id="618fe-167">Taille</span><span class="sxs-lookup"><span data-stu-id="618fe-167">Size</span></span> | <span data-ttu-id="618fe-168">Détails</span><span class="sxs-lookup"><span data-stu-id="618fe-168">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="618fe-169">taille créée</span><span class="sxs-lookup"><span data-stu-id="618fe-169">authored size</span></span>** | <span data-ttu-id="618fe-170">Taille définie dans la feuille de style \ (omise si non définie \).</span><span class="sxs-lookup"><span data-stu-id="618fe-170">The size defined in stylesheet \(omitted if not defined\).</span></span> |  
| **<span data-ttu-id="618fe-171">taille calculée</span><span class="sxs-lookup"><span data-stu-id="618fe-171">computed size</span></span>** | <span data-ttu-id="618fe-172">Taille réelle à l’écran.</span><span class="sxs-lookup"><span data-stu-id="618fe-172">The actual size on screen.</span></span> |  

<span data-ttu-id="618fe-173">Dans la démonstration, les `snack-box` tailles de colonnes sont définies dans la `grid-template-columns:1fr 2fr;` feuille de style en cascade (CSS).</span><span class="sxs-lookup"><span data-stu-id="618fe-173">In the demo, the `snack-box` column sizes are defined in the `grid-template-columns:1fr 2fr;` CSS.</span></span>  <span data-ttu-id="618fe-174">Par conséquent, les étiquettes des lignes de colonnes affichent des tailles créées et calculées.</span><span class="sxs-lookup"><span data-stu-id="618fe-174">Therefore, the column line labels display both authored and computed sizes.</span></span>  

| <span data-ttu-id="618fe-175">Taille du suivi</span><span class="sxs-lookup"><span data-stu-id="618fe-175">Track size</span></span> | <span data-ttu-id="618fe-176">Taille créée</span><span class="sxs-lookup"><span data-stu-id="618fe-176">Authored size</span></span> | <span data-ttu-id="618fe-177">Taille calculée</span><span class="sxs-lookup"><span data-stu-id="618fe-177">Computed size</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="618fe-178">**1fr** &#x2022; **96.66 PX**</span><span class="sxs-lookup"><span data-stu-id="618fe-178">**1fr** &#x2022; **96.66px**</span></span> | <span data-ttu-id="618fe-179">1fr</span><span class="sxs-lookup"><span data-stu-id="618fe-179">1fr</span></span> | <span data-ttu-id="618fe-180">96.66 PX</span><span class="sxs-lookup"><span data-stu-id="618fe-180">96.66px</span></span> |  
| <span data-ttu-id="618fe-181">**2fr** &#x2022; **193.32 PX**</span><span class="sxs-lookup"><span data-stu-id="618fe-181">**2fr** &#x2022; **193.32px**</span></span> | <span data-ttu-id="618fe-182">2fr</span><span class="sxs-lookup"><span data-stu-id="618fe-182">2fr</span></span> | <span data-ttu-id="618fe-183">193.32 PX</span><span class="sxs-lookup"><span data-stu-id="618fe-183">193.32px</span></span> |  

<span data-ttu-id="618fe-184">Les étiquettes de ligne de ligne n’affichent que des tailles calculées, car il n’y a pas de tailles de lignes définies dans la feuille de style.</span><span class="sxs-lookup"><span data-stu-id="618fe-184">The row line labels display only computed sizes, since there are no row sizes defined in the stylesheet.</span></span>  

| <span data-ttu-id="618fe-185">Taille du suivi</span><span class="sxs-lookup"><span data-stu-id="618fe-185">Track size</span></span> | <span data-ttu-id="618fe-186">Taille créée</span><span class="sxs-lookup"><span data-stu-id="618fe-186">Authored size</span></span> | <span data-ttu-id="618fe-187">Taille calculée</span><span class="sxs-lookup"><span data-stu-id="618fe-187">Computed size</span></span> |  
|:--- |:--- |:--- |  
| **<span data-ttu-id="618fe-188">80px</span><span class="sxs-lookup"><span data-stu-id="618fe-188">80px</span></span>** | &nbsp;| <span data-ttu-id="618fe-189">80px</span><span class="sxs-lookup"><span data-stu-id="618fe-189">80px</span></span> |  
| **<span data-ttu-id="618fe-190">80px</span><span class="sxs-lookup"><span data-stu-id="618fe-190">80px</span></span>** | &nbsp;| <span data-ttu-id="618fe-191">80px</span><span class="sxs-lookup"><span data-stu-id="618fe-191">80px</span></span> |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Afficher les tailles de suivi" lightbox="../media/grid-show-track-sizes.msft.png":::
   **<span data-ttu-id="618fe-193">Afficher les tailles de suivi</span><span class="sxs-lookup"><span data-stu-id="618fe-193">Show track sizes</span></span>**  
:::image-end:::  

### <span data-ttu-id="618fe-194">Afficher les noms des zones</span><span class="sxs-lookup"><span data-stu-id="618fe-194">Show area names</span></span>  

<span data-ttu-id="618fe-195">Pour afficher les noms de zone, activez la case à cocher **afficher les noms des zones** .</span><span class="sxs-lookup"><span data-stu-id="618fe-195">To view the area names, enable the **Show area names** checkbox.</span></span>  <span data-ttu-id="618fe-196">Dans l’exemple, il existe 3 zones dans la grille: **Top**, **bottom1** et **bottom2**.</span><span class="sxs-lookup"><span data-stu-id="618fe-196">In the example, there are 3 areas in the grid: **top**, **bottom1** and **bottom2**.</span></span>  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Afficher les noms des zones" lightbox="../media/grid-show-area-names.msft.png":::
   **<span data-ttu-id="618fe-198">Afficher les noms des zones</span><span class="sxs-lookup"><span data-stu-id="618fe-198">Show area names</span></span>**  
:::image-end:::  

### <span data-ttu-id="618fe-199">Prolonger le quadrillage</span><span class="sxs-lookup"><span data-stu-id="618fe-199">Extend grid lines</span></span>  

<span data-ttu-id="618fe-200">Activez la case à cocher **prolonger les lignes de grille** pour étendre les lignes de la grille au bord de la fenêtre d’affichage, le long de chaque axe.</span><span class="sxs-lookup"><span data-stu-id="618fe-200">Enable the **Extend grid lines** checkbox to extend the grid lines to the edge of the viewport along each axis.</span></span>  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Prolonger le quadrillage" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **<span data-ttu-id="618fe-202">Prolonger le quadrillage</span><span class="sxs-lookup"><span data-stu-id="618fe-202">Extend grid lines</span></span>**  
:::image-end:::  

## <span data-ttu-id="618fe-203">Superpositions de grille</span><span class="sxs-lookup"><span data-stu-id="618fe-203">Grid overlays</span></span>  

<span data-ttu-id="618fe-204">La section **façades de grille** contient une liste des grilles présentes dans la page, chacune avec un élément CheckBox avec des options différentes.</span><span class="sxs-lookup"><span data-stu-id="618fe-204">The **Grid overlays** section contains a list of grids that are present on the page, each with a checkbox, along with various options.</span></span>  

### <span data-ttu-id="618fe-205">Activer les vues de superposition de plusieurs grilles</span><span class="sxs-lookup"><span data-stu-id="618fe-205">Enable overlay views of multiple grids</span></span>  

<span data-ttu-id="618fe-206">Pour afficher la grille Overlay pour plusieurs grilles, activez la case à cocher en regard de chaque nom de la grille.</span><span class="sxs-lookup"><span data-stu-id="618fe-206">To display the overlay grid for multiple grids, choose the checkbox next to each name of the grid.</span></span>  <span data-ttu-id="618fe-207">Dans l’exemple, il est possible d’activer 2 superpositions de grille avec des couleurs différentes.</span><span class="sxs-lookup"><span data-stu-id="618fe-207">In the example, there are 2 grid overlays enabled that are each represented with different colors.</span></span>  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Activer les vues de superposition de plusieurs grilles" lightbox="../media/grid-grid-overlays.msft.png":::
   <span data-ttu-id="618fe-209">Activer les vues de superposition de plusieurs grilles</span><span class="sxs-lookup"><span data-stu-id="618fe-209">Enable overlay views of multiple grids</span></span>  
:::image-end:::  

### <span data-ttu-id="618fe-210">Personnaliser la couleur de superposition de la grille</span><span class="sxs-lookup"><span data-stu-id="618fe-210">Customize the grid overlay color</span></span>  

<span data-ttu-id="618fe-211">Pour ouvrir le sélecteur de couleurs et personnaliser la couleur de superposition de la grille, sélectionnez la zone en regard du nom de la superposition de la grille.</span><span class="sxs-lookup"><span data-stu-id="618fe-211">To open the color picker and customize the grid overlay color, choose the box next to the name of the grid overlay.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Personnaliser la couleur de superposition de la grille" lightbox="../media/grid-grid-overlays-color.msft.png":::
   <span data-ttu-id="618fe-213">Personnaliser la couleur de superposition de la grille</span><span class="sxs-lookup"><span data-stu-id="618fe-213">Customize the grid overlay color</span></span>  
:::image-end:::  

### <span data-ttu-id="618fe-214">Mettre en surbrillance la grille</span><span class="sxs-lookup"><span data-stu-id="618fe-214">Highlight the grid</span></span>  

<span data-ttu-id="618fe-215">Pour mettre en surbrillance l’élément HTML dans le panneau **éléments** et y faire défiler dans la page Web, sélectionnez l' **élément afficher dans le panneau éléments** \ ( ![ élément d’affichage de l’icône \) du panneau éléments ][ImageShowElementInElementsPanelIcon] .</span><span class="sxs-lookup"><span data-stu-id="618fe-215">To highlight the HTML element in the **Elements** panel and scroll to it on the webpage, choose the **Show element in the Elements panel** \(![Show element in the Elements panel icon][ImageShowElementInElementsPanelIcon]\) icon.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Mettre en surbrillance la grille" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   <span data-ttu-id="618fe-217">Mettre en surbrillance la grille</span><span class="sxs-lookup"><span data-stu-id="618fe-217">Highlight the grid</span></span>  
:::image-end:::  

## <span data-ttu-id="618fe-218">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="618fe-218">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageShowElementInElementsPanelIcon]: ../media/show-element-in-element-panel-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "Grille CSS | JEC. Money"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "Grille CSS | JEC. Money"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Disposition Grille CSS | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Mise en page à l’aide de la grille nommée MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Placement en ligne avec grille CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="618fe-225">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="618fe-225">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="618fe-226">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/grid) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)</span><span class="sxs-lookup"><span data-stu-id="618fe-226">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/grid) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="618fe-228">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="618fe-228">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
