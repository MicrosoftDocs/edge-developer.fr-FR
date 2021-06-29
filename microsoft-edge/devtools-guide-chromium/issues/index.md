---
description: Utilisez l’outil Problèmes pour identifier et résoudre les problèmes liés à la page web actuelle.
title: Rechercher et résoudre les problèmes à l’aide de l’outil Problèmes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/24/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 86277c509aa4b67635661ba3a316fb5b1e3b9d14
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624695"
---
<!-- Copyright Sam Dutton

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="find-and-fix-problems-using-the-issues-tool"></a><span data-ttu-id="aaa42-104">Rechercher et résoudre les problèmes à l’aide de l’outil Problèmes</span><span class="sxs-lookup"><span data-stu-id="aaa42-104">Find and fix problems using the Issues tool</span></span>

<span data-ttu-id="aaa42-105">Dans Microsoft Edge DevTools, l’outil **Problèmes** analyse automatiquement la page web actuelle, signale les problèmes regroupés par type et fournit une documentation pour expliquer et résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="aaa42-105">In Microsoft Edge DevTools, the **Issues** tool automatically analyzes the current webpage, reports issues grouped by type, and provides documentation to help explain and resolve the issues.</span></span>

<span data-ttu-id="aaa42-106">**L’outil Problèmes** fournit des commentaires dans les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="aaa42-106">The **Issues** tool provides feedback in the following categories:</span></span>
*  <span data-ttu-id="aaa42-107">Accessibilité.</span><span class="sxs-lookup"><span data-stu-id="aaa42-107">Accessibility.</span></span>
*  <span data-ttu-id="aaa42-108">Compatibilité entre les navigateurs.</span><span class="sxs-lookup"><span data-stu-id="aaa42-108">Compatibility across browsers.</span></span>
*  <span data-ttu-id="aaa42-109">Performances.</span><span class="sxs-lookup"><span data-stu-id="aaa42-109">Performance.</span></span>
*  <span data-ttu-id="aaa42-110">Applications web progressives.</span><span class="sxs-lookup"><span data-stu-id="aaa42-110">Progressive Web Apps.</span></span>
*  <span data-ttu-id="aaa42-111">Sécurité.</span><span class="sxs-lookup"><span data-stu-id="aaa42-111">Security.</span></span>
*  <span data-ttu-id="aaa42-112">Autre.</span><span class="sxs-lookup"><span data-stu-id="aaa42-112">Other.</span></span>

<span data-ttu-id="aaa42-113">Les commentaires \*\*\*\* dans l’outil Problèmes sont fournis par plusieurs sources, notamment la plateforme Chromium, la axe de laque, les données de compatibilité du navigateur MDN et lahint web.</span><span class="sxs-lookup"><span data-stu-id="aaa42-113">Feedback in the **Issues** tool is provided by several sources, including the Chromium platform, Deque axe, MDN browser compatibility data, and webhint.</span></span>  <span data-ttu-id="aaa42-114">Pour plus d’informations sur ces sources de commentaires qui remplit l’outil **Problèmes,** accédez à :</span><span class="sxs-lookup"><span data-stu-id="aaa42-114">For information about these sources of feedback that populate the **Issues** tool, navigate to:</span></span>
*  [<span data-ttu-id="aaa42-115">Vue d’ensemble des outils axe</span><span class="sxs-lookup"><span data-stu-id="aaa42-115">axe Tools Overview</span></span>][DequeAxe]
*  [<span data-ttu-id="aaa42-116">browser-compat-data repo</span><span class="sxs-lookup"><span data-stu-id="aaa42-116">browser-compat-data repo</span></span>][MDNCompat]
*  [<span data-ttu-id="aaa42-117">webhint</span><span class="sxs-lookup"><span data-stu-id="aaa42-117">webhint</span></span>][webhintIo]


## <a name="open-the-issues-tool"></a><span data-ttu-id="aaa42-118">Ouvrir l’outil Problèmes</span><span class="sxs-lookup"><span data-stu-id="aaa42-118">Open the Issues tool</span></span>

<span data-ttu-id="aaa42-119">Effectuez les étapes suivantes pour ouvrir **l’outil Problèmes** à l’aide d’une page de démonstration.</span><span class="sxs-lookup"><span data-stu-id="aaa42-119">Perform the following steps to open the **Issues** tool using a demo page.</span></span>


1.  <span data-ttu-id="aaa42-120">Accédez à une page web qui contient des problèmes à résoudre.</span><span class="sxs-lookup"><span data-stu-id="aaa42-120">Navigate to a webpage that contains issues to fix.</span></span>  <span data-ttu-id="aaa42-121">Par exemple, ouvrez la [page de][A11ytestingPagewitherrors] démonstration des tests d’accessibilité dans un nouvel onglet ou une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="aaa42-121">For example, open the [accessibility-testing demo page][A11ytestingPagewitherrors] in a new tab or window.</span></span>

1.  <span data-ttu-id="aaa42-122">Ouvrez DevTools.</span><span class="sxs-lookup"><span data-stu-id="aaa42-122">Open DevTools.</span></span>  <span data-ttu-id="aaa42-123">Après quelques **secondes,** le compteur Problèmes \( Compteur de problèmes \) apparaît dans le coin supérieur droit ![ ](../media/issues-counter-icon.msft.png) de DevTools.</span><span class="sxs-lookup"><span data-stu-id="aaa42-123">After a few seconds, the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\) appears, in the upper right corner of DevTools.</span></span>  <span data-ttu-id="aaa42-124">Le nombre de problèmes dans votre compteur Problèmes peut être différent.</span><span class="sxs-lookup"><span data-stu-id="aaa42-124">The number of issues in your Issues counter might be different.</span></span>

1.  <span data-ttu-id="aaa42-125">Sélectionnez **le compteur Problèmes.**</span><span class="sxs-lookup"><span data-stu-id="aaa42-125">Select the **Issues counter**.</span></span>  <span data-ttu-id="aaa42-126">**L’outil Problèmes** s’ouvre avec des problèmes regroupés en différentes catégories.</span><span class="sxs-lookup"><span data-stu-id="aaa42-126">The **Issues** tool opens with issues grouped into different categories.</span></span>

    :::image type="complex" source="../media/issues-tool-categories.msft.png" alt-text="Catégories de problèmes dans l’outil Problèmes de la page de démonstration" lightbox="../media/issues-tool-categories.msft.png":::
       <span data-ttu-id="aaa42-128">Catégories de problèmes dans l’outil Problèmes de la page de démonstration</span><span class="sxs-lookup"><span data-stu-id="aaa42-128">Categories of issues in the Issues tool on the demo page</span></span>
    :::image-end:::

### <a name="other-ways-to-open-the-issues-tool"></a><span data-ttu-id="aaa42-129">Autres façons d’ouvrir l’outil Problèmes</span><span class="sxs-lookup"><span data-stu-id="aaa42-129">Other ways to open the Issues tool</span></span>

<span data-ttu-id="aaa42-130">Il existe plusieurs façons supplémentaires d’ouvrir **l’outil Problèmes** :</span><span class="sxs-lookup"><span data-stu-id="aaa42-130">There are several additional ways to open the **Issues** tool:</span></span>
*  <span data-ttu-id="aaa42-131">Sélectionnez le menu **Plus d’outils** ( ) dans le panneau principal ou le panneau, puis **+** sélectionnez **Problèmes.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="aaa42-131">Select the **More Tools** (**+**) menu in the main panel or the **Drawer**, and then select **Issues**.</span></span>
*  <span data-ttu-id="aaa42-132">Sélectionnez **Personnaliser et contrôler les problèmes des outils DevTools**  >  **More.**  >  \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="aaa42-132">Select **Customize and control DevTools** > **More tools** > **Issues**.</span></span>
*  <span data-ttu-id="aaa42-133">Dans l’arborescence DOM de l’outil **Elements,** sélectionnez, puis cliquez sur un nom d’élément souligné de forme `Shift` ondulée.</span><span class="sxs-lookup"><span data-stu-id="aaa42-133">In the DOM tree in the **Elements** tool, select `Shift` and then click a wavy-underlined element name.</span></span>  <span data-ttu-id="aaa42-134">Vous pouvez également ouvrir le menu contextif sur un élément souligné de forme ondulée, puis sélectionner **Afficher les problèmes.**</span><span class="sxs-lookup"><span data-stu-id="aaa42-134">Or, open the context menu on a wavy-underlined element and then select **View issues**.</span></span>

### <a name="issues-are-automatically-ordered-by-severity"></a><span data-ttu-id="aaa42-135">Les problèmes sont automatiquement ordonnés par gravité</span><span class="sxs-lookup"><span data-stu-id="aaa42-135">Issues are automatically ordered by severity</span></span>

<span data-ttu-id="aaa42-136">Dans chaque catégorie de problèmes, les erreurs sont d’abord répertoriées, puis les avertissements, puis les conseils.</span><span class="sxs-lookup"><span data-stu-id="aaa42-136">Within each category of issues, first the errors are listed, then warnings, and then tips.</span></span>

:::image type="complex" source="../media/issues-ordered-by-severity.msft.png" alt-text="L’outil Problèmes affiche les problèmes de performances triés par gravité" lightbox="../media/issues-ordered-by-severity.msft.png":::
   <span data-ttu-id="aaa42-138">**L’outil Problèmes** affiche les problèmes de performances triés par gravité</span><span class="sxs-lookup"><span data-stu-id="aaa42-138">The **Issues** tool displays Performance issues sorted by severity</span></span>
:::image-end:::

### <a name="include-third-party-issues"></a><span data-ttu-id="aaa42-139">Inclure des problèmes de tiers</span><span class="sxs-lookup"><span data-stu-id="aaa42-139">Include third-party issues</span></span>

<span data-ttu-id="aaa42-140">Pour inclure les problèmes causés par des sites tiers, en haut \*\*\*\* de l’outil Problèmes, cochez la case Inclure les problèmes tiers. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="aaa42-140">To include issues that are caused by third-party sites, at the top of the **Issues** tool, select the **Include third-party issues** checkbox.</span></span>


## <a name="expand-entries-in-the-issues-tool"></a><span data-ttu-id="aaa42-141">Développer les entrées dans l’outil Problèmes</span><span class="sxs-lookup"><span data-stu-id="aaa42-141">Expand entries in the Issues tool</span></span>

<span data-ttu-id="aaa42-142">**L’outil Problèmes** présente une documentation supplémentaire et des correctifs recommandés à appliquer à chaque problème.</span><span class="sxs-lookup"><span data-stu-id="aaa42-142">The **Issues** tool presents additional documentation and recommended fixes to apply to each issue.</span></span>  <span data-ttu-id="aaa42-143">Pour développer un problème afin d’obtenir ces informations supplémentaires, sélectionnez un problème, comme suit.</span><span class="sxs-lookup"><span data-stu-id="aaa42-143">To expand an issue to get this additional information, select an issue, as follows.</span></span>

1.  <span data-ttu-id="aaa42-144">Ouvrez la [page de démonstration][A11ytestingPagewitherrors] dans une nouvelle fenêtre ou nouvel onglet, puis ouvrez DevTools.</span><span class="sxs-lookup"><span data-stu-id="aaa42-144">Open the [demo page][A11ytestingPagewitherrors] in a new window or tab, and then open DevTools.</span></span>

1.  <span data-ttu-id="aaa42-145">Ouvrez **l’outil Problèmes** en sélectionnant le compteur **Problèmes** \( Compteur de ![ problèmes ](../media/issues-counter-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="aaa42-145">Open the **Issues** tool by selecting the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\).</span></span>

1.  <span data-ttu-id="aaa42-146">Sélectionnez un problème pour développer le problème.</span><span class="sxs-lookup"><span data-stu-id="aaa42-146">Select an issue to expand the issue.</span></span>

    :::image type="complex" source="../media/issues-tool-initial-view-accessibility-page.msft.png" alt-text="Outil Problèmes affichant des informations supplémentaires sur la façon de résoudre le problème" lightbox="../media/issues-tool-initial-view-accessibility-page.msft.png":::
       <span data-ttu-id="aaa42-148">Outil **Problèmes affichant** des informations supplémentaires sur la façon de résoudre le problème</span><span class="sxs-lookup"><span data-stu-id="aaa42-148">The **Issues** tool displaying additional information on how to fix the issue</span></span>
    :::image-end:::

<span data-ttu-id="aaa42-149">Chaque problème affiché présente les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="aaa42-149">Each displayed issue has the following components:</span></span>
*   <span data-ttu-id="aaa42-150">Titre décrivant le problème.</span><span class="sxs-lookup"><span data-stu-id="aaa42-150">A headline describing the issue.</span></span>
*   <span data-ttu-id="aaa42-151">Description fournissant davantage de contexte et des solutions proposées.</span><span class="sxs-lookup"><span data-stu-id="aaa42-151">A description providing more context and proposed solutions.</span></span>
*   <span data-ttu-id="aaa42-152">Section **RESSOURCES AFFECTÉEs** qui fait lien vers des ressources dans DevTools, telles que l’outil **Éléments,** **Sources** **ou** Réseau.</span><span class="sxs-lookup"><span data-stu-id="aaa42-152">An **AFFECTED RESOURCES** section that links to resources in DevTools, such as the **Elements**, **Sources**, or **Network** tool.</span></span>
*   <span data-ttu-id="aaa42-153">Liens vers une documentation plus complète.</span><span class="sxs-lookup"><span data-stu-id="aaa42-153">Links to further documentation.</span></span>


## <a name="view-issues-in-context-of-an-associated-tool"></a><span data-ttu-id="aaa42-154">Afficher les problèmes dans le contexte d’un outil associé</span><span class="sxs-lookup"><span data-stu-id="aaa42-154">View issues in context of an associated tool</span></span>

<span data-ttu-id="aaa42-155">Un problème dans l’outil Problèmes peut inclure un ou plusieurs liens qui ouvrent différents **outils,** tels que l’outil **Éléments,** **Sources** **ou** Réseau.</span><span class="sxs-lookup"><span data-stu-id="aaa42-155">An issue in the **Issues** tool may include one or more links that open different tools, such as the **Elements**, **Sources**, or **Network** tool.</span></span> <span data-ttu-id="aaa42-156">Vous pouvez ouvrir l’un de ces outils pour effectuer des étapes de dépannage supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="aaa42-156">You can open one of these tools to perform additional troubleshooting steps.</span></span> <span data-ttu-id="aaa42-157">Pour ouvrir un outil lié à partir de **l’outil Problèmes,** effectuez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="aaa42-157">To open a linked tool from the **Issues** tool, perform the following steps.</span></span>

1.  <span data-ttu-id="aaa42-158">Comme décrit dans la section précédente, ouvrez la page de démonstration, puis développez un problème dans **l’outil** Problèmes.</span><span class="sxs-lookup"><span data-stu-id="aaa42-158">As described in the previous section, open the demo page and then expand an issue in the **Issues** tool.</span></span>

1.  <span data-ttu-id="aaa42-159">Dans **RESSOURCES AFFECTÉEs,**  >  **ouvrez**dans , sélectionnez le nom de l’outil.</span><span class="sxs-lookup"><span data-stu-id="aaa42-159">In **AFFECTED RESOURCES** > **Open in**, select the tool name.</span></span>  <span data-ttu-id="aaa42-160">La ressource affectée s’affiche dans l’outil sélectionné.</span><span class="sxs-lookup"><span data-stu-id="aaa42-160">The affected resource is displayed in the selected tool.</span></span>

    :::image type="complex" source="../media/issues-tool-affected-resource-opens-elements-tool.msft.png" alt-text="Sélectionner un outil pour ouvrir une ressource concernée à partir de l’outil Problèmes" lightbox="../media/issues-tool-affected-resource-opens-elements-tool.msft.png":::
       <span data-ttu-id="aaa42-162">Sélectionner un outil pour ouvrir une ressource concernée à partir de l’outil Problèmes</span><span class="sxs-lookup"><span data-stu-id="aaa42-162">Select a tool to open an affected resource from within the Issues tool</span></span>
    :::image-end:::

    <span data-ttu-id="aaa42-163">Un problème développé peut avoir une **liaison** réseau pour afficher la ressource concernée dans **l’outil** Réseau.</span><span class="sxs-lookup"><span data-stu-id="aaa42-163">An expanded issue may have a **Network** link, to display the affected resource in the **Network** tool.</span></span>

    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="L’outil Réseau s’ouvre lorsque vous sélectionnez un lien de ressources réseau" lightbox="../media/issues-tab-view-issue.msft.png":::
    <span data-ttu-id="aaa42-165">**L’outil** Réseau s’ouvre lorsque vous sélectionnez un **lien de** ressources réseau</span><span class="sxs-lookup"><span data-stu-id="aaa42-165">The **Network** tool opens when you select a **Network** resource link</span></span>
    :::image-end:::


## <a name="open-issues-from-the-dom-tree"></a><span data-ttu-id="aaa42-166">Problèmes d’ouverture à partir de l’arborescence DOM</span><span class="sxs-lookup"><span data-stu-id="aaa42-166">Open issues from the DOM tree</span></span>

<span data-ttu-id="aaa42-167">Si un élément est associé à un problème, l’arborescence DOM de l’outil **Elements** affiche un soulignement ondulé sous le nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="aaa42-167">If an element has an associated issue, the DOM tree in the **Elements** tool shows a wavy underline under the element name.</span></span>  <span data-ttu-id="aaa42-168">Vous pouvez ouvrir le menu contextif (clic droit) sur l’élément, puis sélectionner Afficher les **problèmes,** ou sélectionner et cliquer avec le bouton gauche sur l’élément avec le `Shift` soulignement ondulé.</span><span class="sxs-lookup"><span data-stu-id="aaa42-168">You can open the context menu (right-click) on the element and then select **View issues**, or select `Shift` and left-click the element with the wavy underline.</span></span>

<span data-ttu-id="aaa42-169">Pour afficher un problème pour les éléments avec des soulignements ondulés dans l’arborescence DOM, effectuez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="aaa42-169">To display an issue for elements with wavy underlines in the DOM tree, perform the following steps.</span></span>

1.  <span data-ttu-id="aaa42-170">Ouvrez une page, telle que la [page de démonstration,][A11ytestingPagewitherrors]dans un nouvel onglet ou une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="aaa42-170">Open a page, such as the [demo page][A11ytestingPagewitherrors], in a new tab or window.</span></span>

1.  <span data-ttu-id="aaa42-171">Ouvrez DevTools, puis sélectionnez **l’onglet Éléments.**</span><span class="sxs-lookup"><span data-stu-id="aaa42-171">Open DevTools and then select the **Elements** tab.</span></span>

1.  <span data-ttu-id="aaa42-172">Dans l’arborescence DOM, développez `<body>`  >  `<header>`  >  `<form>` .</span><span class="sxs-lookup"><span data-stu-id="aaa42-172">In the DOM tree, expand `<body>` > `<header>` > `<form>`.</span></span>  <span data-ttu-id="aaa42-173">Notez que `<input>` l’élément présente un soulignement ondulé.</span><span class="sxs-lookup"><span data-stu-id="aaa42-173">Notice that the `<input>` element has a wavy underline.</span></span>

    :::image type="complex" source="../media/issues-wavy-underlines-dom-tree.msft.png" alt-text="Problèmes soulignés ondulés dans l’arborescence DOM de l’outil Elements" lightbox="../media/issues-wavy-underlines-dom-tree.msft.png":::
       <span data-ttu-id="aaa42-175">Problèmes soulignés ondulés dans l’arborescence **DOM de** **l’outil Elements**</span><span class="sxs-lookup"><span data-stu-id="aaa42-175">Wavy-underlined issues in the **DOM tree** in the **Elements** tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="aaa42-176">Pointez sur `<input>` l’élément.</span><span class="sxs-lookup"><span data-stu-id="aaa42-176">Hover over the `<input>` element.</span></span>  <span data-ttu-id="aaa42-177">Une info-bulle affiche des informations sur le problème.</span><span class="sxs-lookup"><span data-stu-id="aaa42-177">A tooltip displays information about the issue.</span></span>

1.  <span data-ttu-id="aaa42-178">Ouvrez le menu contextif sur l’élément avec le soulignement ondulé, puis sélectionnez **Afficher les problèmes.**</span><span class="sxs-lookup"><span data-stu-id="aaa42-178">Open the context menu on the element with the wavy underline, and then select **View issues**.</span></span>  <span data-ttu-id="aaa42-179">**L’outil** Problèmes s’ouvre et affiche le problème associé à cet élément.</span><span class="sxs-lookup"><span data-stu-id="aaa42-179">The **Issues** tool opens and displays the issue that's associated with that element.</span></span>

    :::image type="complex" source="../media/issues-opened-from-dom-tree-wavy-underline.msft.png" alt-text="Détails sur les problèmes sur un élément ondulé souligné dans l’arborescence DOM" lightbox="../media/issues-opened-from-dom-tree-wavy-underline.msft.png":::
       <span data-ttu-id="aaa42-181">Détails sur les problèmes sur un élément ondulé souligné dans **l’arborescence DOM**</span><span class="sxs-lookup"><span data-stu-id="aaa42-181">Details about issues on a wavy-underlined element in the **DOM tree**</span></span>
    :::image-end:::


## <a name="see-also"></a><span data-ttu-id="aaa42-182">Voir également</span><span class="sxs-lookup"><span data-stu-id="aaa42-182">See also</span></span>

* [<span data-ttu-id="aaa42-183">Tester automatiquement les problèmes d’accessibilité d’une page web</span><span class="sxs-lookup"><span data-stu-id="aaa42-183">Automatically test a webpage for accessibility issues</span></span>](../accessibility/test-issues-tool.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="aaa42-184">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="aaa42-184">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]

<!-- links -->
[DevtoolsOpenIndex]: ../open/index.md "Ouvrez Microsoft Edge devTools | Documents Microsoft"
<!-- external links -->
[A11ytestingPagewitherrors]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page de démonstration des tests d’accessibilité | Documents Microsoft"
[DequeAxe]: https://www.deque.com/axe "Vue d’ensemble des outils axe | Deque"
[MDNCompat]: https://github.com/mdn/browser-compat-data "Gestion des données de compatibilité des navigateurs MDN | GitHub"
[webhintIo]: https://webhint.io "webhint.io"

> [!NOTE]
> <span data-ttu-id="aaa42-190">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aaa42-190">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>
> <span data-ttu-id="aaa42-191">La page d’origine est [trouvée ici](https://developers.google.com/web/tools/chrome-devtools/issues/index) et est cochée par [Sam Dutton][SamDutton] \(Developer Advocate\).</span><span class="sxs-lookup"><span data-stu-id="aaa42-191">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/issues/index) and is authored by [Sam Dutton][SamDutton] \(Developer Advocate\).</span></span>
<span data-ttu-id="aaa42-192">[ ![ Creative Commons License][CCby4Image]][CCA4IL] This work is licensed under a Creative Commons Attribution [4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aaa42-192">[![Creative Commons License][CCby4Image]][CCA4IL] This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>

[CCA4IL]: https://creativecommons.org/licenses/by/4.0
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques
[SamDutton]: https://developers.google.com/web/resources/contributors#sam-dutton
