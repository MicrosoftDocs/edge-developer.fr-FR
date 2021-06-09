---
description: Utilisez l’outil Inspect pour détecter les problèmes d’accessibilité en pointant sur la page web.
title: Utiliser l’outil Inspect pour détecter les problèmes d’accessibilité en pointant sur la page web
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: c95116d38e5b0bda88af43ef8bfde4204b8cb372
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597336"
---
# <a name="use-the-inspect-tool-to-detect-accessibility-issues-by-hovering-over-the-webpage"></a><span data-ttu-id="5340a-104">Utiliser l’outil Inspect pour détecter les problèmes d’accessibilité en pointant sur la page web</span><span class="sxs-lookup"><span data-stu-id="5340a-104">Use the Inspect tool to detect accessibility issues by hovering over the webpage</span></span>

<span data-ttu-id="5340a-105">**L’outil Inspect** affiche des informations sur les éléments individuels lorsque vous pointez sur la page web affichée, y compris les informations d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="5340a-105">The **Inspect** tool displays information about individual elements as you hover over the rendered webpage, including accessibility information.</span></span>
<span data-ttu-id="5340a-106">En revanche, **l’outil Problèmes** signale automatiquement les problèmes pour la page web entière.</span><span class="sxs-lookup"><span data-stu-id="5340a-106">In contrast, the **Issues** tool automatically reports issues for the entire webpage.</span></span>

<span data-ttu-id="5340a-107">Le **bouton d’outil** Inspect \( Inspect \) se trouve dans le coin supérieur gauche ![ de ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="5340a-107">The **Inspect** tool button \(![Inspect](../media/inspect-icon.msft.png)\) is in the upper-left corner of DevTools.</span></span>  <span data-ttu-id="5340a-108">Lorsque vous sélectionnez le **bouton Inspecter** l’outil, le bouton devient bleu, ce qui indique que l’outil **Inspect** est actif.</span><span class="sxs-lookup"><span data-stu-id="5340a-108">When you select the **Inspect** tool button, the button turns blue, indicating that the **Inspect** tool is active.</span></span>

<span data-ttu-id="5340a-109">Lorsque **l’outil Inspect** est actif, le fait de pointer sur un élément de la page web affichée affiche la superposition **Inspect.**</span><span class="sxs-lookup"><span data-stu-id="5340a-109">When the **Inspect** tool is active, hovering over any element on the rendered webpage displays the **Inspect** overlay.</span></span> <span data-ttu-id="5340a-110">Cette superposition affiche des informations générales et des informations d’accessibilité sur cet élément.</span><span class="sxs-lookup"><span data-stu-id="5340a-110">This overlay displays general information and accessibility information about that element.</span></span>  <span data-ttu-id="5340a-111">La section **Accessibilité de** la superposition **Inspect** affiche des informations sur le contraste de couleur du texte, le texte du lecteur d’écran et la prise en charge du clavier.</span><span class="sxs-lookup"><span data-stu-id="5340a-111">The **Accessibility** section of the **Inspect** overlay displays information about text-color contrast, screen reader text, and keyboard support.</span></span>

:::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="L’outil Inspect, montrant la zone de l’élément sous la mesure d’une superposition multicolore, et montrant les détails de l’élément sous la mesure d’une superposition d’informations importante" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
    <span data-ttu-id="5340a-113">**L’outil Inspect,** montrant la zone de l’élément sous la mesure d’une superposition multicolore, et montrant les détails de l’élément sous la mesure d’une superposition d’informations importante</span><span class="sxs-lookup"><span data-stu-id="5340a-113">The **Inspect** tool, showing the element's area as a multicolor overlay, and showing the element's details as a large information overlay</span></span>
:::image-end:::


## <a name="check-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support"></a><span data-ttu-id="5340a-114">Vérifier le contraste du texte, le texte du lecteur d’écran et la prise en charge du clavier pour chaque élément</span><span class="sxs-lookup"><span data-stu-id="5340a-114">Check individual elements for text contrast, screen reader text, and keyboard support</span></span>

<!-- Inspect tool: Accessibility section of overlay -->

1.  <span data-ttu-id="5340a-115">Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="5340a-115">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="5340a-116">Sélectionnez **le bouton Inspect** \( Inspect \) dans le coin supérieur gauche de ![ DevTools afin que l’icône soit mise en surbrillant ](../media/inspect-icon.msft.png) (bleu).</span><span class="sxs-lookup"><span data-stu-id="5340a-116">Select the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

    :::image type="complex" source="../media/a11y-testing-basics-inspector.msft.png" alt-text="Pour activer l’outil Inspect, sélectionnez le bouton Inspecter" lightbox="../media/a11y-testing-basics-inspector.msft.png":::
        <span data-ttu-id="5340a-118">Pour activer l’outil **Inspect,** sélectionnez le **bouton Inspecter**</span><span class="sxs-lookup"><span data-stu-id="5340a-118">To turn on the **Inspect** tool, select the **Inspect** button</span></span>
    :::image-end:::

1.  <span data-ttu-id="5340a-119">Pointez sur n’importe quel élément de la page web de démonstration rendue.</span><span class="sxs-lookup"><span data-stu-id="5340a-119">Hover over any element in the rendered demo webpage.</span></span>  <span data-ttu-id="5340a-120">**L’outil Inspect** affiche une superposition d’informations sous l’élément dans la page web rendue.</span><span class="sxs-lookup"><span data-stu-id="5340a-120">The **Inspect** tool shows an information overlay below the element within the rendered webpage.</span></span>

    :::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="Outil Inspect, montrant la disposition de l’élément sous forme de superposition multicolore et montrant les détails de l’élément sous la forme d’une superposition d’informations importante" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
        <span data-ttu-id="5340a-122">Outil **Inspect,** montrant la disposition de l’élément sous forme de superposition multicolore et montrant les détails de l’élément sous la forme d’une superposition d’informations importante</span><span class="sxs-lookup"><span data-stu-id="5340a-122">The **Inspect** tool, showing the element's layout as a multicolor overlay, and showing the element's details as a large information overlay</span></span>
    :::image-end:::

<span data-ttu-id="5340a-123">La partie inférieure de la superposition **Inspect** comporte une section **Accessibilité** qui contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5340a-123">The bottom part of the **Inspect** overlay has an **Accessibility** section that contains the following information:</span></span>

*   <span data-ttu-id="5340a-124">**Le** contraste définit si un élément peut être compris par les personnes ayant une vision faible.</span><span class="sxs-lookup"><span data-stu-id="5340a-124">**Contrast** defines whether an element can be understood by people with low vision.</span></span>  <span data-ttu-id="5340a-125">Le [coefficient de contraste][W3CContrastRatio] défini par les directives [WCAG][WCAG] indique s’il y a suffisamment de contraste (icône de coche verte) ou pas assez (icône de point d’exclamation orange).</span><span class="sxs-lookup"><span data-stu-id="5340a-125">The [contrast ratio][W3CContrastRatio] as defined by the [WCAG Guidelines][WCAG] indicates whether there is enough contrast (a green check mark icon) or not enough (an orange exclamation-point icon).</span></span>

*   <span data-ttu-id="5340a-126">**Les technologies** **d’assistance** telles que les lecteurs d’écran signalent l’élément en fonction du nom et du rôle.</span><span class="sxs-lookup"><span data-stu-id="5340a-126">**Name** and **Role** are what assistive technology such as screen readers will report about the element.</span></span>
    *   <span data-ttu-id="5340a-127">Le **nom est** le contenu de texte d’un `a` élément.</span><span class="sxs-lookup"><span data-stu-id="5340a-127">The **Name** is the text content of an `a` element.</span></span>  <span data-ttu-id="5340a-128">Pour l’élément, `<a href="/">About Us</a>` le nom **affiché** dans l’outil Inspect est « À propos de nous ».</span><span class="sxs-lookup"><span data-stu-id="5340a-128">For the element `<a href="/">About Us</a>`, the **Name** shown in the Inspect tool is "About Us".</span></span>
    *   <span data-ttu-id="5340a-129">Rôle **de** l’élément.</span><span class="sxs-lookup"><span data-stu-id="5340a-129">The **Role** of the element.</span></span>  <span data-ttu-id="5340a-130">Il s’agit généralement du nom de l’élément, tel `article` que , , ou `img` `link` `heading` .</span><span class="sxs-lookup"><span data-stu-id="5340a-130">This is usually the element name, such as `article`, `img` , `link`, or `heading`.</span></span>  <span data-ttu-id="5340a-131">Les `div` éléments et les éléments sont `span` appelés `generic` .</span><span class="sxs-lookup"><span data-stu-id="5340a-131">The `div` and `span` elements are referred to as `generic`.</span></span>

*   <span data-ttu-id="5340a-132">**La mise au point du clavier** indique si les utilisateurs peuvent accéder à l’élément quel que soit le périphérique d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5340a-132">**Keyboard-focusable** indicates whether users can reach the element regardless of input device.</span></span>
    *   <span data-ttu-id="5340a-133">Une icône de coche verte indique que l’élément est focusable au clavier.</span><span class="sxs-lookup"><span data-stu-id="5340a-133">A green check mark icon indicates that the element is keyboard-focusable.</span></span>
    *   <span data-ttu-id="5340a-134">Un cercle gris avec une ligne diagonale indique que l’élément ne peut pas être mis au point au clavier.</span><span class="sxs-lookup"><span data-stu-id="5340a-134">A gray circle with diagonal line indicates that the element isn't keyboard-focusable.</span></span>


## <a name="additional-information-in-the-inspect-overlay"></a><span data-ttu-id="5340a-135">Informations supplémentaires dans la superposition Inspect</span><span class="sxs-lookup"><span data-stu-id="5340a-135">Additional information in the Inspect overlay</span></span>

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

<span data-ttu-id="5340a-136">La partie supérieure de la superposition **Inspect,** qui se trouve au-dessus de la section **Accessibilité,** répertorie les détails suivants de l’élément.</span><span class="sxs-lookup"><span data-stu-id="5340a-136">The top part of the **Inspect** overlay, which is above the **Accessibility** section, lists the following details of the element.</span></span>

*   <span data-ttu-id="5340a-137">Type de disposition.</span><span class="sxs-lookup"><span data-stu-id="5340a-137">Layout type.</span></span> <span data-ttu-id="5340a-138">Si l’élément est positionné à l’aide d’une flexbox ou d’une grille, une icône \(</span><span class="sxs-lookup"><span data-stu-id="5340a-138">If the element is positioned using a flexbox or grid, an icon \(</span></span>![Icône De disposition de la grille](../media/grid-icon.msft.png)<span data-ttu-id="5340a-140">\) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="5340a-140">\) is displayed.</span></span>
*   <span data-ttu-id="5340a-141">Nom de l’élément, tel `h1` que `h2` , ou `div` .</span><span class="sxs-lookup"><span data-stu-id="5340a-141">Name of the element, such as `h1`, `h2`, or `div`.</span></span>
*   <span data-ttu-id="5340a-142">Dimensions de l’élément en pixels.</span><span class="sxs-lookup"><span data-stu-id="5340a-142">The dimensions of the element in pixels.</span></span>
*   <span data-ttu-id="5340a-143">Couleur sous la forme d’un échantillon de couleur (ou d’un petit carré de couleur) et sous forme de chaîne (par `#336699` exemple).</span><span class="sxs-lookup"><span data-stu-id="5340a-143">The color as a color swatch (or a small, colored square) and as a string (such as `#336699`).</span></span>
*   <span data-ttu-id="5340a-144">Informations sur les polices, telles que la taille et les familles de polices.</span><span class="sxs-lookup"><span data-stu-id="5340a-144">Font information, such as size and font families.</span></span>
*   <span data-ttu-id="5340a-145">Marge et remplissage en pixels.</span><span class="sxs-lookup"><span data-stu-id="5340a-145">Margin and padding in pixels.</span></span>


## <a name="identify-nested-regions-using-color-highlighting"></a><span data-ttu-id="5340a-146">Identifier les régions imbrmbrées à l’aide de la mise en surbrillance des couleurs</span><span class="sxs-lookup"><span data-stu-id="5340a-146">Identify nested regions using color highlighting</span></span> 

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

<span data-ttu-id="5340a-147">En plus de la superposition d’informations, l’outil **Inspect** fournit également une couleur de région similaire au pointage dans l’arborescence DOM de l’outil **Elements.**</span><span class="sxs-lookup"><span data-stu-id="5340a-147">In addition to the information overlay, the **Inspect** tool also provides region-coloring that's similar to hovering in the DOM tree in the **Elements** tool.</span></span>

1.  <span data-ttu-id="5340a-148">Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="5340a-148">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="5340a-149">Sélectionnez **le bouton Inspecter** \( Inspecter l’icône de l’outil \) dans le coin supérieur gauche de ![ DevTools, afin que le bouton soit mis en surbrillant ](../media/inspect-icon.msft.png) (bleu).</span><span class="sxs-lookup"><span data-stu-id="5340a-149">Select the **Inspect** button \(![Inspect tool icon](../media/inspect-icon.msft.png)\) in the top-left corner of DevTools, so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="5340a-150">Pointez sur différentes parties de la page web de démonstration rendue.</span><span class="sxs-lookup"><span data-stu-id="5340a-150">Hover over different parts of the rendered demo webpage.</span></span>  <span data-ttu-id="5340a-151">Chaque élément de la page web s’affiche désormais avec une superposition multicolore.</span><span class="sxs-lookup"><span data-stu-id="5340a-151">Each element in the webpage now displays with a multicolor overlay.</span></span> <span data-ttu-id="5340a-152">Cette superposition multicolore peut afficher des régions imbrmbrées à l’intérieur d’un élément.</span><span class="sxs-lookup"><span data-stu-id="5340a-152">This multicolor overlay can display nested regions inside of an element.</span></span> <span data-ttu-id="5340a-153">Par exemple, pointez sur la marge gauche des **chats**.</span><span class="sxs-lookup"><span data-stu-id="5340a-153">For example, hover over the left margin of **Cats**.</span></span>  <span data-ttu-id="5340a-154">**L’outil Inspect** met en évidence plusieurs parties rectangulaires de la section **Chats** avec des couleurs différentes, montrant la disposition qui résulte des définitions de flexbox CSS sur votre page web.</span><span class="sxs-lookup"><span data-stu-id="5340a-154">The **Inspect** tool highlights several rectangular portions of the **Cats** section with different colors, showing the layout that results from the CSS flexbox definitions on your webpage.</span></span>

:::image type="complex" source="../media/inspect-tool-flexbox-overlay.msft.png" alt-text="Superposition de flexbox multicolore et superposition d’informations lors de l’utilisation de l’outil Inspect" lightbox="../media/inspect-tool-flexbox-overlay.msft.png":::
    <span data-ttu-id="5340a-156">Superposition de flexbox multicolore et superposition d’informations lors de l’utilisation de **l’outil Inspect**</span><span class="sxs-lookup"><span data-stu-id="5340a-156">Multicolor flexbox overlay and information overlay when using the **Inspect** tool</span></span>
:::image-end:::

<span data-ttu-id="5340a-157">Pour configurer la superposition de la grille ou la superposition flexbox, dans l’outil **Éléments,** sélectionnez **l’onglet** Disposition.  Pour plus d’informations, [accédez à Inspect CSS Grid](..\css\grid.md).</span><span class="sxs-lookup"><span data-stu-id="5340a-157">To configure the grid overlay or flexbox overlay, in the **Elements** tool, select the **Layout** tab.  For more information, navigate to [Inspect CSS Grid](..\css\grid.md).</span></span>


## <a name="use-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css"></a><span data-ttu-id="5340a-158">Utiliser l’outil Inspect pour pointer sur la page web afin de mettre en évidence le DOM et le CSS</span><span class="sxs-lookup"><span data-stu-id="5340a-158">Use the Inspect tool to hover over the webpage to highlight the DOM and CSS</span></span>

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

1.  <span data-ttu-id="5340a-159">Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="5340a-159">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="5340a-160">Sélectionnez **le bouton** Inspecter \( l’outil Inspect \) dans le coin supérieur gauche de ![ DevTools, afin que le bouton soit mis en surbrillant ](../media/inspect-icon.msft.png) (bleu).</span><span class="sxs-lookup"><span data-stu-id="5340a-160">Select the **Inspect** button \(![the Inspect tool](../media/inspect-icon.msft.png)\) in the top-left corner of DevTools, so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="5340a-161">Sélectionnez **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="5340a-161">Select the **Elements** tool.</span></span>

1.  <span data-ttu-id="5340a-162">Avec **l’outil Inspect** actif, pointez sur différentes parties de la page web rendue.</span><span class="sxs-lookup"><span data-stu-id="5340a-162">With the **Inspect** tool active, hover over different parts of the rendered webpage.</span></span>  <span data-ttu-id="5340a-163">Dans **l’outil Elements,** l’arborescence DOM HTML se développe automatiquement pour afficher des informations sur l’élément sur quoi vous pointez.</span><span class="sxs-lookup"><span data-stu-id="5340a-163">In the **Elements** tool, the HTML DOM tree automatically expands to show information about the element you hover over.</span></span>  <span data-ttu-id="5340a-164">Le survol n’entraîne pas la mise à jour du volet **Styles.**</span><span class="sxs-lookup"><span data-stu-id="5340a-164">Hovering doesn't cause the **Styles** pane to update.</span></span>

1.  <span data-ttu-id="5340a-165">Sélectionnez maintenant n’importe quel élément dans la page web rendue.</span><span class="sxs-lookup"><span data-stu-id="5340a-165">Now select any element within the rendered webpage.</span></span>  <span data-ttu-id="5340a-166">**L’outil** Elements s’ouvre et affiche automatiquement le code HTML de l’élément dans l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="5340a-166">The **Elements** tool automatically opens and displays the HTML of the element in the DOM tree.</span></span> <span data-ttu-id="5340a-167">L’outil affiche également le CSS appliqué sur l’élément dans le **volet Styles.**</span><span class="sxs-lookup"><span data-stu-id="5340a-167">The tool also displays the applied CSS on the element in the **Styles** pane.</span></span>  <span data-ttu-id="5340a-168">La sélection d’un élément sur la page web rendue permet de mettre hors service **l’outil Inspect.**</span><span class="sxs-lookup"><span data-stu-id="5340a-168">Selecting an element on the rendered webpage turns off the **Inspect** tool.</span></span>

:::image type="complex" source="../media/a11y-testing-basics-inspector-selected-element.msft.png" alt-text="Les détails sur l’élément sélectionné sont affichés dans l’outil Éléments" lightbox="../media/a11y-testing-basics-inspector-selected-element.msft.png":::
    <span data-ttu-id="5340a-170">Les détails sur l’élément sélectionné sont affichés dans **l’outil Éléments**</span><span class="sxs-lookup"><span data-stu-id="5340a-170">Details about the selected element are displayed in the **Elements** tool</span></span>
:::image-end:::

<span data-ttu-id="5340a-171">Après avoir sélectionné un élément dans la page \*\*\*\* rendue, vous pouvez utiliser l’onglet \*\*\*\* Accessibilité (près de l’onglet **Styles)** pour afficher l’arborescence d’accessibilité et utiliser l’Afficheur des commandes **source.**</span><span class="sxs-lookup"><span data-stu-id="5340a-171">After selecting an element in the rendered page, you could then use the **Accessibility** tab (near the **Styles** tab) to view the **Accessibility Tree** and use the **Source Order Viewer**.</span></span>


## <a name="see-also"></a><span data-ttu-id="5340a-172">Articles associés</span><span class="sxs-lookup"><span data-stu-id="5340a-172">See also</span></span>

*  [<span data-ttu-id="5340a-173">Inspecter un nœud</span><span class="sxs-lookup"><span data-stu-id="5340a-173">Inspect a node</span></span>](../dom/index.md#inspect-a-node)
*  [<span data-ttu-id="5340a-174">Vérifier le contraste de couleur du texte à l’état par défaut à l’aide de l’outil Inspect</span><span class="sxs-lookup"><span data-stu-id="5340a-174">Check text-color contrast in the default state using the Inspect tool</span></span>](test-inspect-text-contrast.md)
*  [<span data-ttu-id="5340a-175">Vue d’ensemble des tests d’accessibilité à l’aide de DevTools</span><span class="sxs-lookup"><span data-stu-id="5340a-175">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="5340a-176">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="5340a-176">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
[W3CContrastRatio]: https://www.w3.org/TR/WCAG21/#dfn-contrast-ratio "taux de contraste | W3C"
[WCAG]: https://www.w3.org/TR/WCAG21/ "Recommandations en matière d’accessibilité du contenu web | W3C"
