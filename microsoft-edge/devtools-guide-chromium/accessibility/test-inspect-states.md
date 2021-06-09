---
description: Inspectez l’accessibilité de tous les états des éléments, tels que le contraste du texte pendant l’état de pointage, dans le volet Styles à l’aide de l’état de l’élément Bascule.
title: Vérifier l’accessibilité de tous les états d’éléments
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 129a89f94925de24a4e649bd91f513de031d6b4a
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597362"
---
# <a name="verify-accessibility-of-all-states-of-elements"></a><span data-ttu-id="eb769-104">Vérifier l’accessibilité de tous les états d’éléments</span><span class="sxs-lookup"><span data-stu-id="eb769-104">Verify accessibility of all states of elements</span></span>

<!-- 5. STYLES: TOGGLE STATE -->

<span data-ttu-id="eb769-105">Vérifiez l’accessibilité de tous les états des éléments, tels que le contraste de couleur du texte pendant `hover` l’état.</span><span class="sxs-lookup"><span data-stu-id="eb769-105">Check the accessibility of all states of elements, such as text color contrast during the `hover` state.</span></span>  <span data-ttu-id="eb769-106">**L’outil Inspect** signale les problèmes d’accessibilité pour un état à la fois.</span><span class="sxs-lookup"><span data-stu-id="eb769-106">The **Inspect** tool reports accessibility issues for one state at a time.</span></span>  <span data-ttu-id="eb769-107">Pour vérifier l’accessibilité des différents états des éléments, dans l’onglet **Styles,** sélectionnez **\:hov** (**Toggle Element State**), comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="eb769-107">To check accessibility of the various states of elements, in the **Styles** tab, select **\:hov** (**Toggle Element State**), as described in this article.</span></span> <span data-ttu-id="eb769-108">Nous montrons d’abord pourquoi la simulation d’état est nécessaire à l’aide de l’outil **Inspect,** puis nous montrons comment utiliser la simulation d’état.</span><span class="sxs-lookup"><span data-stu-id="eb769-108">We first show why state simulation is necessary using the **Inspect** tool, and then we show how to use state simulation.</span></span>


## <a name="checking-text-color-contrast-in-the-default-state"></a><span data-ttu-id="eb769-109">Vérification du contraste de couleur du texte dans l’état par défaut</span><span class="sxs-lookup"><span data-stu-id="eb769-109">Checking text color contrast in the default state</span></span>

<!-- Inspect tool: information overlay: Accessibility section: Contrast row -->

<span data-ttu-id="eb769-110">Outre les tests **automatiques** de contraste de couleur dans l’outil Problèmes, vous pouvez également utiliser l’outil **Inspect** pour vérifier si les éléments de page individuels ont un contraste suffisant.</span><span class="sxs-lookup"><span data-stu-id="eb769-110">In addition to the automatic color-contrast tests in the **Issues** tool, you can also use the **Inspect** tool to check whether individual page elements have enough contrast.</span></span>  <span data-ttu-id="eb769-111">Si des informations de contraste sont disponibles, la superposition **Inspect** affiche le coefficient de contraste et un élément de case à cocher.</span><span class="sxs-lookup"><span data-stu-id="eb769-111">If contrast information is available, the **Inspect** overlay shows the contrast ratio and a checkbox item.</span></span>  <span data-ttu-id="eb769-112">Une icône de coche verte indique qu’il y a suffisamment de contraste et une icône d’alerte jaune indique qu’il n’y en a pas assez.</span><span class="sxs-lookup"><span data-stu-id="eb769-112">A green check mark icon indicates there's enough contrast, and a yellow alert icon indicates that there's not enough contrast.</span></span>

<span data-ttu-id="eb769-113">Par exemple, les liens du menu de navigation de la barre latérale ont un contraste suffisant.</span><span class="sxs-lookup"><span data-stu-id="eb769-113">For example, the links in the sidebar navigation menu have enough contrast.</span></span>  <span data-ttu-id="eb769-114">Toutefois, \*\*\*\* l’élément vert de la **liste** État du don ne présente pas suffisamment de contraste et est donc marqué par un avertissement dans la superposition **Inspect.**</span><span class="sxs-lookup"><span data-stu-id="eb769-114">But the green **Dogs** list item in the **Donation status** section doesn't have enough contrast, and so is flagged by a warning in the **Inspect** overlay.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Le contraste des liens dans le menu de navigation de la barre latérale est suffisant, comme illustré dans la superposition Inspect" lightbox="../media/a11y-testing-enough-contrast.msft.png":::
            <span data-ttu-id="eb769-116">Le contraste des liens dans le menu de navigation de la barre latérale est suffisant, comme illustré dans la superposition **Inspect**</span><span class="sxs-lookup"><span data-stu-id="eb769-116">The links in the sidebar navigation menu have enough contrast, as shown in the **Inspect** overlay</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Un élément qui n’a pas assez de contraste est marqué par un avertissement dans la superposition Inspect" lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
            <span data-ttu-id="eb769-118">Un élément qui n’a pas assez de contraste est marqué par un avertissement dans la superposition **Inspect**</span><span class="sxs-lookup"><span data-stu-id="eb769-118">An element that doesn't have enough contrast is flagged by a warning in the **Inspect** overlay</span></span> :::image-end:::
    :::column-end:::
:::row-end:::
        

## <a name="hovering-when-the-inspect-tool-is-active-doesnt-show-the-text-color-contrast-for-the-hover-state"></a><span data-ttu-id="eb769-119">Le fait de pointer lorsque l’outil Inspect est actif n’affiche pas le contraste de couleur du texte pour l’état de pointage</span><span class="sxs-lookup"><span data-stu-id="eb769-119">Hovering when the Inspect tool is active doesn't show the text-color contrast for the hover state</span></span>

<span data-ttu-id="eb769-120">La **superposition** des informations de l’outil Inspect ne représente qu’un seul état.</span><span class="sxs-lookup"><span data-stu-id="eb769-120">The **Inspect** tool's information overlay only represents a single state.</span></span>  <span data-ttu-id="eb769-121">Les éléments de la page peuvent avoir différents états, qui doivent tous être testés.</span><span class="sxs-lookup"><span data-stu-id="eb769-121">Elements on the page can have different states, all of which need to be tested.</span></span>  <span data-ttu-id="eb769-122">Par exemple, lorsque vous placez le pointeur de la souris sur le menu de la page de démonstration de test d’accessibilité, vous obtenez une animation qui modifie les couleurs.</span><span class="sxs-lookup"><span data-stu-id="eb769-122">For example, when you hover the mouse pointer over the menu of the accessibility-testing demo page, you get an animation that changes the colors.</span></span> <span data-ttu-id="eb769-123">Effectuez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="eb769-123">Perform the following steps.</span></span>

1.  <span data-ttu-id="eb769-124">Ouvrez la [page web de démonstration des tests d’accessibilité][DevToolsA11yErrorsDemopage] dans un nouvel onglet.</span><span class="sxs-lookup"><span data-stu-id="eb769-124">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.</span></span>

1.  <span data-ttu-id="eb769-125">Pointez sur les éléments de menu bleu dans le menu de navigation de la barre latérale.</span><span class="sxs-lookup"><span data-stu-id="eb769-125">Hover over the blue menu items in the sidebar navigation menu.</span></span>  <span data-ttu-id="eb769-126">Notez que chaque élément possède une animation.</span><span class="sxs-lookup"><span data-stu-id="eb769-126">Notice that each item has an animation.</span></span>

    :::image type="complex" source="../media/a11y-testing-hover.msft.png" alt-text="Élément de menu affichant différentes couleurs lorsque le pointeur de la souris est sur celui-ci" lightbox="../media/a11y-testing-hover.msft.png":::
        <span data-ttu-id="eb769-128">Élément de menu affichant différentes couleurs lorsque le pointeur de la souris est sur celui-ci</span><span class="sxs-lookup"><span data-stu-id="eb769-128">The menu item showing different colors when the mouse pointer is over it</span></span>
    :::image-end:::
    
<span data-ttu-id="eb769-129">À présent, utilisez l’outil Inspect.</span><span class="sxs-lookup"><span data-stu-id="eb769-129">Now, use the Inspect tool.</span></span> <span data-ttu-id="eb769-130">Lorsque l’outil Inspect est utilisé, les animations sur les éléments de menu ne s’exécutent pas lorsque vous pointez dessus.</span><span class="sxs-lookup"><span data-stu-id="eb769-130">When the Inspect tool is used, animations on the menu items won't run when you hover over them.</span></span>  <span data-ttu-id="eb769-131">Lorsque vous utilisez l’outil Inspect, vous ne pouvez pas atteindre l’état des éléments de menu pour tester le coefficient de contraste, car l’état de vos `hover` `hover` styles n’est pas déclenché.</span><span class="sxs-lookup"><span data-stu-id="eb769-131">When using the Inspect tool, you can't reach the `hover` state on menu items to test the contrast ratio, because the `hover` state in your styles isn't triggered.</span></span>  
    
<span data-ttu-id="eb769-132">Pour confirmer que vos animations ne s’exécutent pas, effectuez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="eb769-132">To confirm that your animations don't run, perform the following steps.</span></span>
    
1.  <span data-ttu-id="eb769-133">Sélectionnez **le bouton Inspect** \( le bouton Inspect \) dans le coin supérieur gauche de ![ DevTools afin que l’icône soit en surbrillant ](../media/inspect-icon.msft.png) (bleu).</span><span class="sxs-lookup"><span data-stu-id="eb769-133">Select the **Inspect** \(![the Inspect button](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

1.  <span data-ttu-id="eb769-134">Pointez sur les liens bleus dans le menu de navigation de la barre latérale.</span><span class="sxs-lookup"><span data-stu-id="eb769-134">Hover over the blue links on the sidebar navigation menu.</span></span>  <span data-ttu-id="eb769-135">Les animations des éléments de menu ne s’exécutent pas.</span><span class="sxs-lookup"><span data-stu-id="eb769-135">The animations for the menu items don't run.</span></span> <span data-ttu-id="eb769-136">Au lieu de cela, les éléments de menu sont affichés à l’aide de couleurs et de sur-points forts pour la superposition flexbox.</span><span class="sxs-lookup"><span data-stu-id="eb769-136">Instead, the menu items are displayed using colors and highlights for the flexbox overlay.</span></span>

<span data-ttu-id="eb769-137">La recherche d’un contraste de texte suffisant de cette façon n’est pas suffisante, car les éléments de la page peuvent avoir des états différents.</span><span class="sxs-lookup"><span data-stu-id="eb769-137">Checking for sufficient text contrast this way isn't enough, because the elements on the page could have different states.</span></span>


## <a name="use-state-simulation-to-simulate-the-hover-state-of-an-animated-menu-item"></a><span data-ttu-id="eb769-138">Utiliser la simulation d’état pour simuler l’état de pointer d’un élément de menu animé</span><span class="sxs-lookup"><span data-stu-id="eb769-138">Use state simulation to simulate the hover state of an animated menu item</span></span> 

<!-- Elements tool: Styles pane: Toggle Element State -->

<span data-ttu-id="eb769-139">Lorsque **l’outil Inspect** est actif, au lieu de pointer sur un élément animé, vous devez simuler l’état de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="eb769-139">When the **Inspect** tool is active, instead of hovering over an animated element, you need to simulate the state of the menu item.</span></span>  <span data-ttu-id="eb769-140">Pour simuler l’état d’un élément de menu, utilisez la simulation d’état dans le **volet Styles.**</span><span class="sxs-lookup"><span data-stu-id="eb769-140">To simulate the state of a menu item, use the state simulation in the **Styles** pane.</span></span>  <span data-ttu-id="eb769-141">Le **volet Styles** possède un bouton **\:hov** (**Toggle Element State**), qui affiche un groupe de case à cocher avec l’état de l’élément **Force**.</span><span class="sxs-lookup"><span data-stu-id="eb769-141">The **Styles** pane has a **\:hov** (**Toggle Element State**) button, which displays a group of checkboxes labeled **Force element state**.</span></span>

<span data-ttu-id="eb769-142">Pour activer l’état de pointer lors de l’utilisation de l’outil Inspect :</span><span class="sxs-lookup"><span data-stu-id="eb769-142">To turn on the hover state while using the Inspect tool:</span></span>

1.  <span data-ttu-id="eb769-143">S’il n’est pas déjà ouvert, ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration de test d’accessibilité dans un nouvel onglet.  Sélectionnez **ensuite F12** pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="eb769-143">If it's not open already, open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.  Then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="eb769-144">Sélectionnez **le bouton Inspect** \( Inspect tool button \) dans le coin supérieur gauche de ![ DevTools afin que l’icône soit mise en surbrillant ](../media/inspect-icon.msft.png) (bleu).</span><span class="sxs-lookup"><span data-stu-id="eb769-144">Select the **Inspect** \(![Inspect tool button](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

1.  <span data-ttu-id="eb769-145">Dans la page web rendue, sélectionnez le lien **chats** bleus dans le menu de navigation de la barre latérale.</span><span class="sxs-lookup"><span data-stu-id="eb769-145">In the rendered webpage, select the blue **Cats** link in the sidebar navigation menu.</span></span>  <span data-ttu-id="eb769-146">**L’outil Elements** s’ouvre, avec l’élément `<a href="#cats">Cats</a>` sélectionné.</span><span class="sxs-lookup"><span data-stu-id="eb769-146">The **Elements** tool opens, with the element `<a href="#cats">Cats</a>` selected.</span></span>

    :::image type="complex" source="../media/a11y-testing-inspecting-link-to-hover.msft.png" alt-text="Inspection de l’élément dont l’état de pointage est dans l’outil Elements" lightbox="../media/a11y-testing-inspecting-link-to-hover.msft.png":::
        <span data-ttu-id="eb769-148">Inspection de l’élément dont l’état de pointage est dans l’outil Elements</span><span class="sxs-lookup"><span data-stu-id="eb769-148">Inspecting the element that has a hover state in the Elements tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="eb769-149">Sélectionnez **l’onglet Styles.**  L’élément sélectionné possède un état dans le CSS qui lui est appliqué, mais qui n’est pas visible dans le `a` `hover` volet **Styles.**</span><span class="sxs-lookup"><span data-stu-id="eb769-149">Select the **Styles** tab.  The selected `a` element has a `hover` state in the CSS that is applied to it, but that's not visible in the **Styles** pane.</span></span> 

1.  <span data-ttu-id="eb769-150">Dans le **volet Styles,** à droite de la règle de `#sidebar nav li a` style, sélectionnez le `styles.css` lien.</span><span class="sxs-lookup"><span data-stu-id="eb769-150">In the **Styles** pane, to the right of the style rule `#sidebar nav li a`, select the `styles.css` link.</span></span>  <span data-ttu-id="eb769-151">**L’outil Sources** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="eb769-151">The **Sources** tool opens.</span></span>  <span data-ttu-id="eb769-152">Recherchez ensuite la règle de pseudo-classe CSS `#sidebar nav li a:hover` .</span><span class="sxs-lookup"><span data-stu-id="eb769-152">Then find the CSS pseudo-class rule `#sidebar nav li a:hover`.</span></span>  <span data-ttu-id="eb769-153">Cette règle ne s’exécute pas lorsque **l’outil Inspect** est actif.</span><span class="sxs-lookup"><span data-stu-id="eb769-153">This rule doesn't run when the **Inspect** tool is active.</span></span>  <span data-ttu-id="eb769-154">Nous allons simuler l’exécution de cette règle d’état dans les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="eb769-154">We'll simulate running this state rule in the next steps.</span></span>

1.  <span data-ttu-id="eb769-155">Sélectionnez **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="eb769-155">Select the **Elements** tool.</span></span>  <span data-ttu-id="eb769-156">Ensuite, dans **le volet Styles,** sélectionnez le bouton **:hov** (**Toggle Element State**).</span><span class="sxs-lookup"><span data-stu-id="eb769-156">Then in the **Styles** pane, select the **:hov** (**Toggle Element State**) button.</span></span>  <span data-ttu-id="eb769-157">Le **groupe d’états d’élément Force** des case à cocher s’affiche.</span><span class="sxs-lookup"><span data-stu-id="eb769-157">The **Force element state** group of checkboxes is displayed.</span></span>

    :::image type="complex" source="../media/a11y-testing-state-simulation.msft.png" alt-text="Outil de simulation d’état affichant toutes les options" lightbox="../media/a11y-testing-state-simulation.msft.png":::
        <span data-ttu-id="eb769-159">Outil de simulation d’état affichant toutes les options</span><span class="sxs-lookup"><span data-stu-id="eb769-159">The state simulation tool showing all the options</span></span>
    :::image-end:::

1.  <span data-ttu-id="eb769-160">**Cochez la case :hover.**</span><span class="sxs-lookup"><span data-stu-id="eb769-160">Select the **:hover** checkbox.</span></span>  <span data-ttu-id="eb769-161">Dans le DOM, à gauche de l’élément, un point jaune s’affiche, indiquant que l’élément `<a href="#cats">Cats</a>` a un état simulé.</span><span class="sxs-lookup"><span data-stu-id="eb769-161">In the DOM, to the left of the element `<a href="#cats">Cats</a>`, a yellow dot appears, indicating that the element has a simulated state.</span></span>  <span data-ttu-id="eb769-162">**L’élément** de menu Chats apparaît maintenant dans la page web comme si le pointeur pointait sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="eb769-162">The **Cats** menu item now appears in the webpage as if the pointer were hovering over it.</span></span>  <span data-ttu-id="eb769-163">L’animation sur l’élément de menu peut s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="eb769-163">The animation on the menu item might run.</span></span>

    :::image type="complex" source="../media/a11y-testing-hover-simulated.msft.png" alt-text="DevTools simulant un état de pointage" lightbox="../media/a11y-testing-hover-simulated.msft.png":::
        <span data-ttu-id="eb769-165">DevTools simulant un état de pointage</span><span class="sxs-lookup"><span data-stu-id="eb769-165">DevTools simulating a hover state</span></span>
    :::image-end:::

    <span data-ttu-id="eb769-166">Une fois l’état simulé appliqué, vous pouvez à nouveau utiliser l’outil **Inspect** pour vérifier le contraste de l’élément lorsque l’utilisateur passe dessus, comme suit.</span><span class="sxs-lookup"><span data-stu-id="eb769-166">After the simulated state is applied, you can use the **Inspect** tool again to check the contrast of the element when the user hovers over it, as follows.</span></span>

1.  <span data-ttu-id="eb769-167">Sélectionnez **le bouton Inspect** \( Inspector icon \) dans le coin supérieur gauche de ![ DevTools afin que l’icône soit en surbrillant ](../media/inspect-icon.msft.png) (bleu).</span><span class="sxs-lookup"><span data-stu-id="eb769-167">Select the **Inspect** \(![Inspector icon](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

1.  <span data-ttu-id="eb769-168">Pointez sur le lien **chats** bleus dans le menu de navigation de la barre latérale.</span><span class="sxs-lookup"><span data-stu-id="eb769-168">Hover over the blue **Cats** link in the sidebar navigation menu.</span></span>  <span data-ttu-id="eb769-169">Le lien est désormais bleu clair, en raison de l’animation de pointation simulée.</span><span class="sxs-lookup"><span data-stu-id="eb769-169">The link is now light blue, because of the simulated hover animation.</span></span>  <span data-ttu-id="eb769-170">La **superposition** des informations de l’outil Inspect s’affiche, affichant un point d’exclamation orange dans la ligne **Contraste,** indiquant que le contraste n’est pas assez élevé.</span><span class="sxs-lookup"><span data-stu-id="eb769-170">The **Inspect** tool's information overlay appears, showing an orange exclamation point in the **Contrast** row, indicating that the contrast isn't high enough.</span></span>

    :::image type="complex" source="../media/a11y-testing-hover-contrast-testing.msft.png" alt-text="Test du contraste d’un élément dans un état de pointer simulé" lightbox="../media/a11y-testing-hover-contrast-testing.msft.png":::
        <span data-ttu-id="eb769-172">Test du contraste d’un élément dans un état de pointer simulé</span><span class="sxs-lookup"><span data-stu-id="eb769-172">Testing the contrast of an element in a simulated hover state</span></span>
    :::image-end:::

<span data-ttu-id="eb769-173">La simulation d’état est également un bon moyen de vérifier si vous avez pris en compte différents besoins des utilisateurs, tels que les besoins des utilisateurs du clavier.</span><span class="sxs-lookup"><span data-stu-id="eb769-173">State simulation is also a good way to check whether you considered different user needs, such as the needs of keyboard users.</span></span>  <span data-ttu-id="eb769-174">En utilisant les case à cocher d’état de l’élément **Force,** vous pouvez simuler l’état pour découvrir que l’interface utilisateur reste inchangée `:focus` lorsqu’elle a le focus.</span><span class="sxs-lookup"><span data-stu-id="eb769-174">By using the **Force element state** checkboxes, you can simulate the `:focus` state to discover that the UI remains unchanged when it has focus.</span></span> <span data-ttu-id="eb769-175">Cette absence d’indicateur lorsqu’un élément a le focus est un problème.</span><span class="sxs-lookup"><span data-stu-id="eb769-175">This lack of an indicator when an element has focus is a problem.</span></span>


## <a name="see-also"></a><span data-ttu-id="eb769-176">Articles associés</span><span class="sxs-lookup"><span data-stu-id="eb769-176">See also</span></span>

*  [<span data-ttu-id="eb769-177">Vue d’ensemble des tests d’accessibilité à l’aide de DevTools</span><span class="sxs-lookup"><span data-stu-id="eb769-177">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="eb769-178">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="eb769-178">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
