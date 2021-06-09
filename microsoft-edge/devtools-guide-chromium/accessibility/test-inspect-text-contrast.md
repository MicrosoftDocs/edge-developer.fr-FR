---
description: Vérifiez le contraste de couleur du texte dans l’état par défaut à l’aide de la superposition d’informations de l’outil Inspect sur la page, qui comporte une section Accessibilité qui inclut les informations de contraste.
title: Vérifier le contraste de couleur du texte à l’état par défaut à l’aide de l’outil Inspect
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: ade9fd6d685f6f7cea6311b1645a527ece352a38
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597332"
---
# <a name="check-text-color-contrast-in-the-default-state-using-the-inspect-tool"></a><span data-ttu-id="f43af-104">Vérifier le contraste de couleur du texte à l’état par défaut à l’aide de l’outil Inspect</span><span class="sxs-lookup"><span data-stu-id="f43af-104">Check text-color contrast in the default state using the Inspect tool</span></span>

<!-- Inspect tool: information overlay: Accessibility section: Contrast row -->

<span data-ttu-id="f43af-105">Vérifiez le contraste de couleur du texte dans l’état par défaut à l’aide de **l’outil Inspect.**</span><span class="sxs-lookup"><span data-stu-id="f43af-105">Check text color contrast in the default state by using the **Inspect** tool.</span></span>  <span data-ttu-id="f43af-106">La **superposition** des informations de l’outil Inspect sur la page web comporte une section **Accessibilité** qui inclut les **informations de** contraste.</span><span class="sxs-lookup"><span data-stu-id="f43af-106">The **Inspect** tool's information overlay on the webpage has an **Accessibility** section that includes **Contrast** information.</span></span>

<span data-ttu-id="f43af-107">Pour vérifier le contraste de couleur du texte à l’état par défaut à l’aide de la superposition d’informations de l’outil Inspect, effectuez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f43af-107">To check text-color contrast in the default state using the Inspect tool's information overlay, perform the following steps.</span></span>

<!-- Inspect tool -->
<span data-ttu-id="f43af-108">Pour les éléments qui ont du texte, **la** superposition des informations de l’outil Inspect affiche les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="f43af-108">For elements that have text, the **Inspect** tool's information overlay shows the following:</span></span>
*  <span data-ttu-id="f43af-109">Coefficient de contraste entre les couleurs de texte et d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f43af-109">The contrast ratio of text versus background colors.</span></span>
*  <span data-ttu-id="f43af-110">Icône de coche verte pour les éléments avec un contraste suffisant.</span><span class="sxs-lookup"><span data-stu-id="f43af-110">A green check mark icon for elements with enough contrast.</span></span>
*  <span data-ttu-id="f43af-111">Icône d’alerte jaune pour les éléments qui n’ont pas assez de contraste.</span><span class="sxs-lookup"><span data-stu-id="f43af-111">A yellow alert icon for elements that don't have enough contrast.</span></span>

<span data-ttu-id="f43af-112">Dans certains cas, le contraste est affecté par la définition du navigateur sur le thème clair ou le thème foncé.</span><span class="sxs-lookup"><span data-stu-id="f43af-112">In some cases, contrast is affected by setting the browser to light theme or dark theme.</span></span>

<span data-ttu-id="f43af-113">Par exemple, sur la page de démonstration, les liens bleus du menu \*\*\*\* de navigation de la barre latérale ont un contraste suffisant, mais le lien vert De la **section** État du don n’a pas assez de contraste.</span><span class="sxs-lookup"><span data-stu-id="f43af-113">As an example, on the demo page, the blue links of the sidebar navigation menu have enough contrast, but the green **Dogs** link in the **Donation status** section does not have enough contrast.</span></span>  <span data-ttu-id="f43af-114">Examinez ces éléments à l’aide **de l’outil Inspect,** comme suit :</span><span class="sxs-lookup"><span data-stu-id="f43af-114">Review those elements using the **Inspect** tool, as follows:</span></span>

1.  <span data-ttu-id="f43af-115">Ouvrez la [page web de démonstration des tests d’accessibilité][DevToolsA11yErrorsDemopage] dans un nouvel onglet.  Sélectionnez **ensuite F12** pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="f43af-115">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.  Then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="f43af-116">Sélectionnez **le bouton Inspect** \( Inspect button \) dans le coin supérieur gauche de ![ DevTools afin que l’icône soit mise en surbrillant ](../media/inspect-icon.msft.png) (bleu).</span><span class="sxs-lookup"><span data-stu-id="f43af-116">Select the **Inspect** \(![Inspect button](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

1.  <span data-ttu-id="f43af-117">Dans la page web rendue, pointez sur le lien **chats** bleus du menu de navigation de la barre latérale.</span><span class="sxs-lookup"><span data-stu-id="f43af-117">In the rendered webpage, hover over the blue **Cats** link of the sidebar navigation menu.</span></span>  <span data-ttu-id="f43af-118">La **superposition des** informations de l’outil Inspect s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f43af-118">The **Inspect** tool's information overlay appears.</span></span>  <span data-ttu-id="f43af-119">Dans la section **Accessibilité** de la superposition d’informations, une coche verte apparaît sur la ligne **Contrast,** indiquant que cet élément présente un contraste suffisant entre la couleur du texte et la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f43af-119">In the **Accessibility** section of the information overlay, a green checkmark appears on the **Contrast** row, indicating that this element has enough contrast of text color versus background color.</span></span>

    :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Les éléments de menu ont un contraste suffisant, comme illustré dans l’outil Inspect" lightbox="../media/a11y-testing-enough-contrast.msft.png":::
        <span data-ttu-id="f43af-121">Les éléments de menu ont un contraste suffisant, comme illustré dans l’outil Inspect</span><span class="sxs-lookup"><span data-stu-id="f43af-121">The menu items have enough contrast, as shown in the Inspect tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="f43af-122">Dans la page web rendue, dans la section **État du** don, pointez sur le lien **Chiens.**</span><span class="sxs-lookup"><span data-stu-id="f43af-122">In the rendered webpage, in the **Donation Status** section, hover over the **Dogs** link.</span></span>  <span data-ttu-id="f43af-123">La **superposition** des informations de l’outil Inspect affiche un point d’exclamation orange sur la ligne **Contrast,** indiquant que cet élément ne présente pas suffisamment de contraste entre le texte et les couleurs d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f43af-123">The **Inspect** tool's information overlay shows an orange exclamation point on the **Contrast** row, indicating that this element doesn't have enough contrast of text versus background colors.</span></span>

    :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Un élément qui n’a pas assez de contraste, comme illustré par l’avertissement dans l’outil Inspect" lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
        <span data-ttu-id="f43af-125">Un élément qui n’a pas assez de contraste, comme illustré par l’avertissement dans l’outil Inspect</span><span class="sxs-lookup"><span data-stu-id="f43af-125">An element that doesn't have enough contrast, as shown by the warning in the Inspect tool</span></span>
    :::image-end:::


## <a name="different-options-to-inspect-text-color-contrast-in-devtools"></a><span data-ttu-id="f43af-126">Différentes options pour inspecter le contraste de couleur du texte dans DevTools</span><span class="sxs-lookup"><span data-stu-id="f43af-126">Different options to inspect text-color contrast in DevTools</span></span>

<span data-ttu-id="f43af-127">Utilisez les fonctionnalités DevTools suivantes pour inspecter le contraste de couleur du texte.</span><span class="sxs-lookup"><span data-stu-id="f43af-127">Use the following DevTools features to inspect text-color contrast.</span></span>

*  <span data-ttu-id="f43af-128">Utilisez **l’outil Inspect** (comme superposition d’informations sur la page web) pour vérifier si un élément de page individuel possède un contraste de couleur de texte suffisant.</span><span class="sxs-lookup"><span data-stu-id="f43af-128">Use the **Inspect** tool (as an information overlay on the webpage) to check whether an individual page element has enough text-color contrast.</span></span>  <span data-ttu-id="f43af-129">La **superposition** des informations de l’outil Inspect inclut une section **Accessibilité** qui comporte une ligne **d’informations** de contraste.</span><span class="sxs-lookup"><span data-stu-id="f43af-129">The **Inspect** tool's information overlay includes an **Accessibility** section that has a **Contrast** information row.</span></span>  <span data-ttu-id="f43af-130">**L’outil Inspect** affiche uniquement les informations de contraste de texte pour l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="f43af-130">The **Inspect** tool only shows text-contrast information for the current state.</span></span>  <span data-ttu-id="f43af-131">Cette approche est décrite dans l’article actuel.</span><span class="sxs-lookup"><span data-stu-id="f43af-131">This approach is described in the current article.</span></span>

*  <span data-ttu-id="f43af-132">**L’outil Problèmes** signale automatiquement les problèmes de contraste de couleur pour la page web entière, lorsque le texte et la couleur d’arrière-plan ne sont pas suffisamment contrastées.</span><span class="sxs-lookup"><span data-stu-id="f43af-132">The **Issues** tool automatically reports any color-contrast issues for the entire webpage, when text and background color don't contrast enough.</span></span>  <span data-ttu-id="f43af-133">Cette approche est décrite dans [Vérifier que les couleurs du texte ont un contraste suffisant.](test-issues-tool.md#verify-that-text-colors-have-enough-contrast)</span><span class="sxs-lookup"><span data-stu-id="f43af-133">This approach is described in [Verify that text colors have enough contrast](test-issues-tool.md#verify-that-text-colors-have-enough-contrast).</span></span>

*  <span data-ttu-id="f43af-134">Émuler un état autre que l’état par défaut, tel que l’état, en utilisant l’état de l’élément bascule dans le volet Styles, décrit dans Vérifier l’accessibilité de tous les états des `hover` [éléments.](test-inspect-states.md) \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f43af-134">Emulate a non-default state, such as the `hover` state, by using **Toggle Element State** in the **Styles** pane, described in [Verify accessibility of all states of elements](test-inspect-states.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="f43af-135">Articles associés</span><span class="sxs-lookup"><span data-stu-id="f43af-135">See also</span></span>

*  [<span data-ttu-id="f43af-136">Vérifier l’accessibilité de tous les états d’éléments</span><span class="sxs-lookup"><span data-stu-id="f43af-136">Verify accessibility of all states of elements</span></span>][DevtoolsAccessibilityTestInspectStates]
*  [<span data-ttu-id="f43af-137">Utiliser l’outil Inspect pour détecter les problèmes d’accessibilité en pointant sur la page web</span><span class="sxs-lookup"><span data-stu-id="f43af-137">Use the Inspect tool to detect accessibility issues by hovering over the webpage</span></span>](test-inspect-tool.md)
*  [<span data-ttu-id="f43af-138">Vue d’ensemble des tests d’accessibilité à l’aide de DevTools</span><span class="sxs-lookup"><span data-stu-id="f43af-138">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f43af-139">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="f43af-139">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevtoolsAccessibilityTestInspectStates]: test-inspect-states.md "Vérifier l’accessibilité de tous les états des éléments | Documents Microsoft"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
