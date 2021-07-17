---
description: Bouton Plus d’outils, documentation en contexte pour commencer à utiliser l’extension DevTools, prise en charge accrue des lecteurs d’écran dans la console, etc.
title: Nouveautés de DevTools (Microsoft Edge 92)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 09e1438ae7fd6547a7dd14757f54f370c9008773
ms.sourcegitcommit: 1dd6376784c394087fe2938acaa069212cf7656e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/16/2021
ms.locfileid: "11659427"
---
# <a name="whats-new-in-devtools-microsoft-edge-92"></a><span data-ttu-id="2c51f-104">Nouveautés de DevTools (Microsoft Edge 92)</span><span class="sxs-lookup"><span data-stu-id="2c51f-104">What's New In DevTools (Microsoft Edge 92)</span></span>

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]

> [!TIP]
> <span data-ttu-id="2c51f-105">La **conférence Microsoft Build 2021** s’est tenue du 25 au 27 mai.</span><span class="sxs-lookup"><span data-stu-id="2c51f-105">The **Microsoft Build 2021** conference was on May 25-27.</span></span>  <span data-ttu-id="2c51f-106">Voici une vidéo de Build sur les mises à jour de DevTools : [Microsoft Edge | État de la plateforme][YoutubeEdgeStateOfThePlatform] : Microsoft Edge une plateforme attrayante et cohérente avec des outils pour les développeurs.</span><span class="sxs-lookup"><span data-stu-id="2c51f-106">Here's a video from Build about the updates to DevTools: [Microsoft Edge | State of the Platform][YoutubeEdgeStateOfThePlatform] - Microsoft Edge brings a compelling and consistent platform with tools for developers.</span></span>  <span data-ttu-id="2c51f-107">À mesure que nos navigateurs hérités ne seront plus pris en charge, Edge sera bientôt le seul navigateur pris en charge par Microsoft sur Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2c51f-107">As our legacy browsers phase out of support, Edge will soon be the only supported browser from Microsoft on Windows 10.</span></span>  <span data-ttu-id="2c51f-108">Rejoignez-nous pour en savoir plus sur la dernière version de la plateforme Edge, des outils et des applications web.</span><span class="sxs-lookup"><span data-stu-id="2c51f-108">Join us to learn about the latest across the Edge platform, tools, and web apps.</span></span>


## <a name="the-close-button-is-no-longer-hidden-when-devtools-is-narrow"></a><span data-ttu-id="2c51f-109">Le bouton Fermer n’est plus masqué lorsque DevTools est étroit</span><span class="sxs-lookup"><span data-stu-id="2c51f-109">The Close button is no longer hidden when DevTools is narrow</span></span>

<!-- Title: DevTools is now easier to close -->
<!-- Subtitle: The Close button in DevTools is always displayed, even when DevTools is docked to the right and the DevTools viewport is narrow. -->

<span data-ttu-id="2c51f-110">Dans Microsoft Edge version 91 ou antérieure, \*\*\*\* le bouton Fermer pour fermer DevTools n’est pas affiché lorsque la vue DevTools est étroite.</span><span class="sxs-lookup"><span data-stu-id="2c51f-110">In Microsoft Edge version 91 or earlier, the **Close** button to close DevTools isn't displayed when the DevTools viewport is narrow.</span></span>  <span data-ttu-id="2c51f-111">Dans Microsoft Edge version 92, \*\*\*\* le bouton Fermer dans DevTools est toujours présent, quelle que soit la largeur de laport d’affichage DevTools.</span><span class="sxs-lookup"><span data-stu-id="2c51f-111">In Microsoft Edge version 92, the **Close** button in the DevTools is always present, regardless of the DevTools viewport width.</span></span>

:::image type="complex" source="../../media/2021/05/close-devtools-button-always-displayed.msft.png" alt-text="Le bouton Fermer DevTools est désormais présent, même lorsque laport d’affichage est étroite" lightbox="../../media/2021/05/close-devtools-button-always-displayed.msft.png":::
   <span data-ttu-id="2c51f-113">Le **bouton Fermer** DevTools est désormais présent, même lorsque laport d’affichage est étroite</span><span class="sxs-lookup"><span data-stu-id="2c51f-113">The **Close** DevTools button is now present even when the viewport is narrow</span></span>
:::image-end:::


## <a name="add-tools-quickly-with-the-new-more-tools-button"></a><span data-ttu-id="2c51f-114">Ajouter rapidement des outils avec le nouveau bouton Plus d’outils</span><span class="sxs-lookup"><span data-stu-id="2c51f-114">Add tools quickly with the new More Tools button</span></span>

<!-- Title: Add tools quickly with the new More Tools button -->
<!-- Subtitle: Learn about a new convenient way to open tools in Microsoft Edge DevTools. -->

<span data-ttu-id="2c51f-115">Il existe une nouvelle façon d’ouvrir d’autres outils dans \*\*\*\* Microsoft Edge DevTools : le menu Plus d’outils `+` ().</span><span class="sxs-lookup"><span data-stu-id="2c51f-115">There's a new way to open more tools in Microsoft Edge DevTools: the **More Tools** (`+`) menu.</span></span> <span data-ttu-id="2c51f-116">Le menu **Plus d’outils** apparaît dans la barre d’outils du panneau principal et dans la barre d’outils du panneau.</span><span class="sxs-lookup"><span data-stu-id="2c51f-116">The **More Tools** menu appears on the toolbar in the main panel and on the toolbar of the drawer.</span></span> <span data-ttu-id="2c51f-117">La sélection d’un outil dans le menu **Plus d’outils** l’ajoute à la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="2c51f-117">Selecting a tool from the **More Tools** menu adds the tool to the toolbar.</span></span>

<span data-ttu-id="2c51f-118">Pour réorder les onglets de l’une ou l’autre barre d’outils, sélectionnez les onglets et faites-les glisser.</span><span class="sxs-lookup"><span data-stu-id="2c51f-118">To reorder the tabs on either toolbar, select and drag the tabs.</span></span>

<span data-ttu-id="2c51f-119">Le menu **Plus d’outils** était disponible sous la forme d’une expérience Microsoft Edge version 89 et est désormais toujours présent.</span><span class="sxs-lookup"><span data-stu-id="2c51f-119">The **More Tools** menu was available as an experiment in Microsoft Edge version 89, and is now always present.</span></span>

:::image type="complex" source="../../media/2021/05/more-tools-button.msft.png" alt-text="Bouton Plus d’outils dans la barre d’outils supérieure et la barre d’outils de caisse" lightbox="../../media/2021/05/more-tools-button.msft.png":::
   <span data-ttu-id="2c51f-121">Bouton **Plus d’outils** dans la barre d’outils supérieure et la barre d’outils de caisse</span><span class="sxs-lookup"><span data-stu-id="2c51f-121">The **More Tools** button on the upper toolbar and drawer toolbar</span></span>
:::image-end:::

:::image type="complex" source="../../media/2021/05/more-tools-menu.msft.png" alt-text="Menu Plus d’outils" lightbox="../../media/2021/05/more-tools-menu.msft.png":::
   <span data-ttu-id="2c51f-123">Menu **Plus d’outils**</span><span class="sxs-lookup"><span data-stu-id="2c51f-123">The **More Tools** menu</span></span>
:::image-end:::


## <a name="improvements-for-hovering-selecting-and-closing-tools"></a><span data-ttu-id="2c51f-124">Améliorations apportées aux outils de pointage, de sélection et de fermeture</span><span class="sxs-lookup"><span data-stu-id="2c51f-124">Improvements for hovering, selecting, and closing tools</span></span>

<!-- Title: Improvements to tab interactions -->
<!-- Subtitle: Interactions related to hovering, selecting, and closing tools are more predictable. -->

<span data-ttu-id="2c51f-125">Les onglets de chaque outil ont été reformatés pour réduire les risques de fermeture accidentelle d’un outil.</span><span class="sxs-lookup"><span data-stu-id="2c51f-125">Tabs for each tool have been reformatted to reduce the chance of accidentally closing a tool.</span></span>  <span data-ttu-id="2c51f-126">Dans chaque onglet de la barre d’outils principale et dans la barre d’outils du caisse, nous avons ajouté :</span><span class="sxs-lookup"><span data-stu-id="2c51f-126">On each tab in the main toolbar and in the toolbar of the drawer, we added:</span></span>
*  <span data-ttu-id="2c51f-127">Espacement autour de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="2c51f-127">Spacing around the tab.</span></span>
*  <span data-ttu-id="2c51f-128">Espacement autour du bouton fermer `x` () dans l’onglet.</span><span class="sxs-lookup"><span data-stu-id="2c51f-128">Spacing around the close (`x`) button in the tab.</span></span>
*  <span data-ttu-id="2c51f-129">Couleur d’arrière-plan lorsque vous placez le pointage sur l’onglet.</span><span class="sxs-lookup"><span data-stu-id="2c51f-129">A background color when hovering over the tab.</span></span>
*  <span data-ttu-id="2c51f-130">Une boîte à outils pour le bouton fermer ( `x` ) de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="2c51f-130">A tooltip for the close (`x`) button of the tab.</span></span>
*  <span data-ttu-id="2c51f-131">Contraste plus élevé pour le bouton fermer ( `x` ) de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="2c51f-131">Higher contrast for the close (`x`) button of the tab.</span></span>

<span data-ttu-id="2c51f-132">Par exemple, lorsque vous êtes dans l’outil **Performances** et que vous pointez sur l’onglet de l’outil Réseau, ces améliorations permettent d’éviter la fermeture accidentelle de l’outil Réseau. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2c51f-132">For example, when you are in the **Performance** tool and you hover over the **Network** tool's tab, these improvements help prevent accidentally closing the **Network** tool.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-before.msft.png" alt-text="Onglets avant la reformatage" lightbox="../../media/2021/05/hovering-on-tool-tab-before.msft.png":::
           <span data-ttu-id="2c51f-134">Onglets avant la reformatage</span><span class="sxs-lookup"><span data-stu-id="2c51f-134">Tabs before reformatting</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-after.msft.png" alt-text="Onglets après la reformatage" lightbox="../../media/2021/05/hovering-on-tool-tab-after.msft.png":::
           <span data-ttu-id="2c51f-136">Onglets après la reformatage</span><span class="sxs-lookup"><span data-stu-id="2c51f-136">Tabs after reformatting</span></span> :::image-end:::
    :::column-end:::
:::row-end:::

<span data-ttu-id="2c51f-137">Ces améliorations sont particulièrement pertinentes pour les utilisateurs de DevTools localisées, dans lesquelles les onglets peuvent être plus étroits et plus faciles à fermer accidentellement.</span><span class="sxs-lookup"><span data-stu-id="2c51f-137">These improvements are especially relevant for users of localized DevTools, in which the tabs may be narrower and easier to accidentally close.</span></span>

:::image type="complex" source="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png" alt-text="DevTools localisées avec onglets étroits" lightbox="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png":::
   <span data-ttu-id="2c51f-139">DevTools localisées avec onglets étroits</span><span class="sxs-lookup"><span data-stu-id="2c51f-139">Localized DevTools with narrow tabs</span></span>
:::image-end:::

<span data-ttu-id="2c51f-140">Nous avons également facilité la ré-ajout d’un outil que vous avez fermé en ajoutant un [menu](#add-tools-quickly-with-the-new-more-tools-button) Plus d’outils à la barre d’outils principale et à la barre d’outils des caisses.</span><span class="sxs-lookup"><span data-stu-id="2c51f-140">We also made it easier to re-add a tool that you closed by adding a [More Tools menu](#add-tools-quickly-with-the-new-more-tools-button) to the main toolbar and drawer toolbar.</span></span>


## <a name="better-support-for-screen-readers-in-the-console"></a><span data-ttu-id="2c51f-141">Meilleure prise en charge des lecteurs d’écran dans la console</span><span class="sxs-lookup"><span data-stu-id="2c51f-141">Better support for screen readers in the Console</span></span>

<!-- Title: Better screen reader support in the Console -->
<!-- Subtitle: Assistive technologies can now announce autocomplete suggestions and evaluated expressions in the Console. -->

<span data-ttu-id="2c51f-142">Avant Microsoft Edge version 92, dans la **console,** les technologies d’assistance telles que les lecteurs d’écran n’annoncaient pas les suggestions de mise à jour automatique ou les résultats des expressions évaluées.</span><span class="sxs-lookup"><span data-stu-id="2c51f-142">Prior to Microsoft Edge version 92, in the **Console**, assistive technologies such as screen readers didn't announce autocomplete suggestions or the results of evaluated expressions.</span></span> <span data-ttu-id="2c51f-143">This has been fixed now.</span><span class="sxs-lookup"><span data-stu-id="2c51f-143">This has been fixed now.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png" alt-text="Dans la console, les lecteurs d’écran annoncent maintenant la suggestion de mise à l’écran sélectionnée" lightbox="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png":::
           <span data-ttu-id="2c51f-145">Dans la **console,** les lecteurs d’écran annoncent désormais la suggestion de mise à l’écran sélectionnée</span><span class="sxs-lookup"><span data-stu-id="2c51f-145">In the **Console**, screen readers now announce the currently selected autocomplete suggestion</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png" alt-text="Dans la console, les lecteurs d’écran annoncent désormais le résultat d’une expression évaluée" lightbox="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png":::
           <span data-ttu-id="2c51f-147">Dans la **console,** les lecteurs d’écran annoncent désormais le résultat d’une expression évaluée</span><span class="sxs-lookup"><span data-stu-id="2c51f-147">In the **Console**, screen readers now announce the result of an evaluated expression</span></span> :::image-end:::
    :::column-end:::
:::row-end:::


## <a name="source-order-viewer"></a><span data-ttu-id="2c51f-148">Visionneuse de commandes source</span><span class="sxs-lookup"><span data-stu-id="2c51f-148">Source Order Viewer</span></span>

<!--  Title: Source Order Viewer -->
<!--  Subtitle: The new Source Order Viewer displays numbers on the webpage indicating the order of page elements in the source file, independently of how the page sections are positioned by CSS. -->

<span data-ttu-id="2c51f-149">Vous pouvez désormais afficher l’ordre des éléments source superposés sur la page web rendue, pour une meilleure inspection de l’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="2c51f-149">You can now view the order of source elements overlaid on the rendered webpage, for better accessibility inspection.</span></span>

<span data-ttu-id="2c51f-150">L’ordre du contenu dans un document HTML est important pour l’optimisation et l’accessibilité du moteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="2c51f-150">The order of content in an HTML document is important for search engine optimization and accessibility.</span></span>  <span data-ttu-id="2c51f-151">CSS permet aux développeurs de créer du contenu dont l’ordre à l’écran est différent de celui du document source HTML.</span><span class="sxs-lookup"><span data-stu-id="2c51f-151">CSS allows developers to create content that looks different in its on-screen order than the order in the HTML source document.</span></span>  <span data-ttu-id="2c51f-152">Il s’agit d’un problème d’accessibilité, car les utilisateurs de lecteur d’écran peuvent obtenir une expérience confuse.</span><span class="sxs-lookup"><span data-stu-id="2c51f-152">This is an accessibility problem, because screen-reader users could get a confusing experience.</span></span>

:::image type="complex" source="../../media/2021/05/source-order-viewer.msft.png" alt-text="L’activation de l’Afficheur des commandes sources affiche l’ordre des éléments dans la source sous la la mesure où ils sont superposés sur la page" lightbox="../../media/2021/05/source-order-viewer.msft.png":::
   <span data-ttu-id="2c51f-154">L’activation de **l’Afficheur** des commandes sources affiche l’ordre des éléments dans la source sous la mesure de superpositions sur la page</span><span class="sxs-lookup"><span data-stu-id="2c51f-154">Activating the **Source Order Viewer** shows the order of the elements in the source as overlays on the page</span></span>
:::image-end:::

<span data-ttu-id="2c51f-155">Pour plus d’informations, accédez à Tester la [prise en charge du clavier à l’aide de l’Observateur de commandes source.](../../../accessibility/test-tab-key-source-order-viewer.md)</span><span class="sxs-lookup"><span data-stu-id="2c51f-155">For more information, navigate to [Test keyboard support using the Source Order Viewer](../../../accessibility/test-tab-key-source-order-viewer.md).</span></span>

<span data-ttu-id="2c51f-156">Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1094406][CR1094406].</span><span class="sxs-lookup"><span data-stu-id="2c51f-156">To review the history of this feature in the Chromium open-source project, navigate to Issue [1094406][CR1094406].</span></span>


## <a name="user-agent-client-hints-for-devices-in-the-network-conditions-tab"></a><span data-ttu-id="2c51f-157">User-Agent client pour les appareils dans l’onglet Conditions réseau</span><span class="sxs-lookup"><span data-stu-id="2c51f-157">User-Agent Client Hints for devices in the Network conditions tab</span></span>

<!--  Title: User-Agent Client Hints -->
<!--  Subtitle: Access information about a user's browser in an ergonomic way that preserves privacy. -->

<span data-ttu-id="2c51f-158">User-Agent conseils client sont désormais appliqués pour les appareils dans le champ **Agent** utilisateur de l’outil **Conditions réseau.**</span><span class="sxs-lookup"><span data-stu-id="2c51f-158">User-Agent Client Hints are now applied for devices in the **User agent** field in the **Network conditions** tool.</span></span>  <span data-ttu-id="2c51f-159">User-Agent conseils au client est une nouvelle extension de l’API Client Hints qui vous permet d’accéder aux informations sur le navigateur d’un utilisateur de manière conviviale, tout en préservez la confidentialité.</span><span class="sxs-lookup"><span data-stu-id="2c51f-159">User-Agent Client Hints are a new expansion to the Client Hints API that enables you to access information about a user's browser in an ergonomic way that preserves privacy.</span></span>

:::image type="complex" source="../../media/2021/05/user-agent.msft.png" alt-text="Agent utilisateur" lightbox="../../media/2021/05/user-agent.msft.png":::
   <span data-ttu-id="2c51f-161">Agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="2c51f-161">User agent</span></span>
:::image-end:::

<span data-ttu-id="2c51f-162">Pour plus d’informations, accédez [à User-Agent Client Hints](../../../../web-platform/user-agent-guidance.md#user-agent-client-hints).</span><span class="sxs-lookup"><span data-stu-id="2c51f-162">For more information, navigate to [User-Agent Client Hints](../../../../web-platform/user-agent-guidance.md#user-agent-client-hints).</span></span>

<span data-ttu-id="2c51f-163">Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1174299][CR1174299].</span><span class="sxs-lookup"><span data-stu-id="2c51f-163">To review the history of this feature in the Chromium open-source project, navigate to Issue [1174299][CR1174299].</span></span>


## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-118"></a><span data-ttu-id="2c51f-164">Microsoft Edge Outils de développement Visual Studio Code version 1.1.8</span><span class="sxs-lookup"><span data-stu-id="2c51f-164">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.8</span></span>

<span data-ttu-id="2c51f-165">Les [outils Microsoft Edge][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] développeur pour Visual Studio Code version 1.1.8 pour Microsoft Visual Studio Code ont les modifications suivantes depuis la version précédente.</span><span class="sxs-lookup"><span data-stu-id="2c51f-165">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.8 for Microsoft Visual Studio Code has the following changes since the previous release.</span></span>  <span data-ttu-id="2c51f-166">Microsoft Visual Studio Code met automatiquement à jour les extensions.</span><span class="sxs-lookup"><span data-stu-id="2c51f-166">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="2c51f-167">Pour mettre à jour manuellement la version 1.1.8, accédez à Mettre à jour [une extension manuellement.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="2c51f-167">To manually update to version 1.1.8, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>

<span data-ttu-id="2c51f-168">Vous pouvez déposer des problèmes et contribuer à l’extension sur le GitHub [vscode-edge-devtools.][GithubMicrosoftVscodeEdgeDevtools]</span><span class="sxs-lookup"><span data-stu-id="2c51f-168">You can file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>

### <a name="in-context-documentation-and-ui-to-make-it-easier-to-use-the-devtools-extension"></a><span data-ttu-id="2c51f-169">Documentation et interface utilisateur en contexte pour faciliter l’utilisation de l’extension DevTools</span><span class="sxs-lookup"><span data-stu-id="2c51f-169">In-context documentation and UI to make it easier to use the DevTools extension</span></span>

<!-- Title: In-context documentation and UI make it easier to get started using the Developer Tools extension -->
<!-- Subtitle: The Microsoft Edge Developer Tools for Visual Studio Code extension now presents helpful text, buttons, and links, and opens a documentation page with guidance on how to get started. -->

<span data-ttu-id="2c51f-170">La version 1.1.8 de l’extension [outils][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] de développement Microsoft Edge pour Visual Studio Code offre désormais un moyen plus simple de démarrer une nouvelle instance de Microsoft Edge, en présentant des instructions, des boutons, des liens et une page de documentation pour vous guider.</span><span class="sxs-lookup"><span data-stu-id="2c51f-170">Version 1.1.8 of the [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension now features a simpler way to start a new instance of Microsoft Edge, by presenting instructions, buttons, links, and a documentation page to guide you.</span></span>

*  <span data-ttu-id="2c51f-171">Lorsque vous sélectionnez le bouton **Outils Microsoft Edge** dans la barre d’activité de Visual Studio Code, le panneau \*\*\*\* **Outils Microsoft Edge** : Cibles présente désormais un texte explicatif, des boutons et des liens pour vous guider, au lieu d’un panneau vide.</span><span class="sxs-lookup"><span data-stu-id="2c51f-171">When you select the **Microsoft Edge Tools** button in the **Activity Bar** of Visual Studio Code, the **Microsoft Edge Tools: Targets** panel now presents explanatory text, buttons, and links to guide you, instead of a blank panel.</span></span>

*  <span data-ttu-id="2c51f-172">Lorsque vous ouvrez une nouvelle instance de Microsoft Edge à partir de Visual Studio Code, Microsoft Edge affiche désormais une page de démarrage qui explique comment utiliser l’extension Outils de développement, au lieu d’une page vierge.</span><span class="sxs-lookup"><span data-stu-id="2c51f-172">When you open a new instance of Microsoft Edge from within Visual Studio Code, Microsoft Edge now shows a start page that explains how to use the Developer Tools extension, instead of a blank page.</span></span>

*  <span data-ttu-id="2c51f-173">Le **panneau Microsoft Edge Outils** : Cibles possède désormais une launch.jsgénérer une **launch.js** sur le bouton et des instructions, pour vous aider à lancer votre projet pour le débogage dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2c51f-173">The **Microsoft Edge Tools: Targets** panel now has a **Generate launch.json** button and instructions, to help launch your project for debugging in Microsoft Edge.</span></span>

<span data-ttu-id="2c51f-174">Pour plus d’informations, accédez à [Utiliser les outils.][GithubIoDevToolsUsing]</span><span class="sxs-lookup"><span data-stu-id="2c51f-174">For more information, navigate to [Using the tools][GithubIoDevToolsUsing].</span></span>


## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="2c51f-175">Annonces du projet de Chromium</span><span class="sxs-lookup"><span data-stu-id="2c51f-175">Announcements from the Chromium project</span></span>

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]


### <a name="css-grid-editor"></a><span data-ttu-id="2c51f-176">Éditeur CSS Grid</span><span class="sxs-lookup"><span data-stu-id="2c51f-176">CSS Grid editor</span></span>

<span data-ttu-id="2c51f-177">Vous pouvez désormais prévisualiser et éditer des dispositions de grille CSS à l’aide du nouvel éditeur CSS Grid.</span><span class="sxs-lookup"><span data-stu-id="2c51f-177">You can now preview and author CSS Grid layouts, using the new CSS Grid editor.</span></span>

<span data-ttu-id="2c51f-178">Lorsqu’un élément HTML de votre page s’y est appliqué, une icône de grille s’affiche en de côté dans l’onglet Styles. Cliquez sur l’icône de grille pour afficher ou masquer l’éditeur de grille `display: grid` `display: inline-grid` CSS. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2c51f-178">When an HTML element on your page has `display: grid` or `display: inline-grid` applied to it, a grid icon is displayed next to it in the **Styles** tab. Click the grid icon to display or hide the CSS grid editor.</span></span> <span data-ttu-id="2c51f-179">Dans l’éditeur de grille CSS, sélectionnez l’une des icônes (par exemple) pour afficher un aperçu de la mise en page dans `justify-content: space-around` la page rendue.</span><span class="sxs-lookup"><span data-stu-id="2c51f-179">In the CSS grid editor, select any of the icons (such as `justify-content: space-around`) to preview the layout in the rendered page.</span></span>  <span data-ttu-id="2c51f-180">La disposition flexible fonctionne de la même manière.</span><span class="sxs-lookup"><span data-stu-id="2c51f-180">Flex layout works similarly.</span></span>

:::image type="complex" source="../../media/2021/05/css-grid-editor.msft.png" alt-text="Éditeur CSS Grid" lightbox="../../media/2021/05/css-grid-editor.msft.png":::
   <span data-ttu-id="2c51f-182">Éditeur CSS Grid</span><span class="sxs-lookup"><span data-stu-id="2c51f-182">CSS Grid editor</span></span>
:::image-end:::

<!-- screenshot uses https://jec.fyi -->

<span data-ttu-id="2c51f-183">Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1203241][CR1203241].</span><span class="sxs-lookup"><span data-stu-id="2c51f-183">To review the history of this feature in the Chromium open-source project, navigate to Issue [1203241][CR1203241].</span></span>


### <a name="support-for-const-redeclarations-in-the-console"></a><span data-ttu-id="2c51f-184">Prise en charge des déclarations de const dans la console</span><span class="sxs-lookup"><span data-stu-id="2c51f-184">Support for const redeclarations in the Console</span></span>

<span data-ttu-id="2c51f-185">La console prend désormais en charge la déclaration des variables dans des scripts REPL distincts (par exemple, lorsque vous exécutez une instruction dans la console), en plus des `const` `let` déclarations existantes et `class` redéclarations.</span><span class="sxs-lookup"><span data-stu-id="2c51f-185">The Console now supports redeclaration of `const` variables across separate REPL scripts (such as when you run a statement in the Console), in addition to the existing `let` and `class` redeclarations.</span></span>  <span data-ttu-id="2c51f-186">Cette prise en charge vous permet d’expérimenter différentes déclarations pour `const` les variables sans actualisation de la page.</span><span class="sxs-lookup"><span data-stu-id="2c51f-186">This support allows you to experiment with different declarations for `const` variables without refreshing the page.</span></span>  <span data-ttu-id="2c51f-187">Auparavant, DevTools a lancé une erreur de syntaxe si vous avez redéclaré une `const` liaison.</span><span class="sxs-lookup"><span data-stu-id="2c51f-187">Previously, DevTools threw a syntax error if you redeclared a `const` binding.</span></span>

<span data-ttu-id="2c51f-188">Reportez-vous à l’exemple ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="2c51f-188">Refer to the example below.</span></span> `const` <span data-ttu-id="2c51f-189">la redéclaration est prise en charge dans des scripts REPL distincts (reportez-vous à la `a` variable).</span><span class="sxs-lookup"><span data-stu-id="2c51f-189">redeclaration is supported across separate REPL scripts (refer to variable `a`).</span></span>  <span data-ttu-id="2c51f-190">Notez que les scénarios suivants ne sont pas pris en charge, par conception :</span><span class="sxs-lookup"><span data-stu-id="2c51f-190">Note that the following scenarios are not supported, by design:</span></span>

*  `const` <span data-ttu-id="2c51f-191">la redéclaration des scripts de page n’est pas autorisée dans les scripts REPL.</span><span class="sxs-lookup"><span data-stu-id="2c51f-191">redeclaration of page scripts is not allowed in REPL scripts.</span></span>
*  `const` <span data-ttu-id="2c51f-192">la redéclaration dans le même script REPL n’est pas autorisée (faire référence à la variable `b` ).</span><span class="sxs-lookup"><span data-stu-id="2c51f-192">redeclaration within the same REPL script is not allowed (refer to variable `b`).</span></span>

:::image type="complex" source="../../media/2021/05/support-for-const-redeclaration.msft.png" alt-text="La déclaration d’une variable const est autorisée dans la console" lightbox="../../media/2021/05/support-for-const-redeclaration.msft.png":::
   <span data-ttu-id="2c51f-194">La déclaration d’une variable const est autorisée dans la console</span><span class="sxs-lookup"><span data-stu-id="2c51f-194">Redeclaring a const variable is allowed in the console</span></span>
:::image-end:::

<span data-ttu-id="2c51f-195">Pour découvrir comment exécuter un script REPL unique ou un script REPL multi-ligne, accédez à la console en tant [qu’environnement JavaScript.](../../../console/console-javascript.md)</span><span class="sxs-lookup"><span data-stu-id="2c51f-195">To learn how to run a single REPL script or a multi-line REPL script, navigate to [The Console as a JavaScript environment](../../../console/console-javascript.md).</span></span>
    
<span data-ttu-id="2c51f-196">Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1076427][CR1076427].</span><span class="sxs-lookup"><span data-stu-id="2c51f-196">To review the history of this feature in the Chromium open-source project, navigate to Issue [1076427][CR1076427].</span></span>


### <a name="new-shortcut-to-view-iframe-details"></a><span data-ttu-id="2c51f-197">Nouveau raccourci pour afficher les détails de l’iframe</span><span class="sxs-lookup"><span data-stu-id="2c51f-197">New shortcut to view iframe details</span></span>

<span data-ttu-id="2c51f-198">Pour afficher rapidement les détails, vous pouvez maintenant cliquer avec le bouton droit sur un élément dans l’outil Éléments, puis sélectionner Afficher les `iframe` `iframe` **détails de l’iframe.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2c51f-198">To quickly view `iframe` details, you can now right-click an `iframe` element in the **Elements** tool, and then select **Show iframe details**.</span></span>

:::image type="complex" source="../../media/2021/05/show-iframe-details.msft.png" alt-text="Affichage des détails de l’iframe" lightbox="../../media/2021/05/show-iframe-details.msft.png":::
   <span data-ttu-id="2c51f-200">Affichage des détails de l’iframe</span><span class="sxs-lookup"><span data-stu-id="2c51f-200">iframe details view</span></span>
:::image-end:::

<span data-ttu-id="2c51f-201">Cela permet d’afficher les détails sur `iframe` l’outil **Application.**</span><span class="sxs-lookup"><span data-stu-id="2c51f-201">This displays the details about the `iframe` in the **Application** tool.</span></span>  <span data-ttu-id="2c51f-202">Dans **l’outil Application,** vous pouvez examiner les détails du document, l’état de sécurité et d’isolation, la stratégie d’autorisations, etc., pour déboguer les problèmes potentiels.</span><span class="sxs-lookup"><span data-stu-id="2c51f-202">In the **Application** tool, you can examine document details, security and isolation status, permissions policy, and more, to debug potential issues.</span></span>

:::image type="complex" source="../../media/2021/05/show-iframe-details-application-tool.msft.png" alt-text="Détails du cadre dans l’outil Application" lightbox="../../media/2021/05/show-iframe-details-application-tool.msft.png":::
   <span data-ttu-id="2c51f-204">Détails du cadre dans **l’outil Application**</span><span class="sxs-lookup"><span data-stu-id="2c51f-204">Frame details in the **Application** tool</span></span>
:::image-end:::

<!-- demo page: https://wolfib.github.io/web-demos/ esp https://wolfib.github.io/web-demos/jsIframe.html -->

<span data-ttu-id="2c51f-205">Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1192084][CR1192084].</span><span class="sxs-lookup"><span data-stu-id="2c51f-205">To review the history of this feature in the Chromium open-source project, navigate to Issue [1192084][CR1192084].</span></span>


### <a name="enhanced-cors-debugging-support"></a><span data-ttu-id="2c51f-206">Prise en charge améliorée du débogage CORS</span><span class="sxs-lookup"><span data-stu-id="2c51f-206">Enhanced CORS debugging support</span></span>

<span data-ttu-id="2c51f-207">Les erreurs de partage de ressources d’origine croisée (CORS) sont désormais **émises** dans l’onglet Problèmes.  Il existe différentes causes potentielles d’erreurs CORS.</span><span class="sxs-lookup"><span data-stu-id="2c51f-207">Cross-origin resource sharing (CORS) errors are now surfaced in the **Issues** tab.  There are various potential causes of CORS errors.</span></span>  <span data-ttu-id="2c51f-208">Cliquez pour développer chaque problème afin de comprendre les causes et solutions potentielles.</span><span class="sxs-lookup"><span data-stu-id="2c51f-208">Click to expand each issue to understand the potential causes and solutions.</span></span>

:::image type="complex" source="../../media/2021/05/cors-debugging-support.msft.png" alt-text="Problèmes CORS dans l’onglet Problèmes" lightbox="../../media/2021/05/cors-debugging-support.msft.png":::
   <span data-ttu-id="2c51f-210">Problèmes CORS dans l’onglet Problèmes</span><span class="sxs-lookup"><span data-stu-id="2c51f-210">CORS issues in the Issues tab</span></span>
:::image-end:::

<!-- screenshot uses http://cors-errors.glitch.me -->

<span data-ttu-id="2c51f-211">Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1141824][CR1141824].</span><span class="sxs-lookup"><span data-stu-id="2c51f-211">To review the history of this feature in the Chromium open-source project, navigate to Issue [1141824][CR1141824].</span></span>


### <a name="renamed-xhr-filter-to-fetchxhr"></a><span data-ttu-id="2c51f-212">Filtre XHR renommé Fetch\/XHR</span><span class="sxs-lookup"><span data-stu-id="2c51f-212">Renamed XHR filter to Fetch\/XHR</span></span>

<span data-ttu-id="2c51f-213">Dans **l’outil** Réseau, le **filtre XHR** est maintenant renommé **Fetch/XHR**.</span><span class="sxs-lookup"><span data-stu-id="2c51f-213">In the **Network** tool, the **XHR** filter is now renamed to **Fetch/XHR**.</span></span> <span data-ttu-id="2c51f-214">Cette modification rend plus clair que ce filtre inclut les demandes réseau `XMLHttpRequest` `Fetch` d’API et à la fois.</span><span class="sxs-lookup"><span data-stu-id="2c51f-214">This change makes it clearer that this filter includes both `XMLHttpRequest` and `Fetch` API network requests.</span></span>

:::image type="complex" source="../../media/2021/05/fetch-xhr.msft.png" alt-text="L’outil Réseau affiche désormais Fetch/XHR au lieu de XHR" lightbox="../../media/2021/05/fetch-xhr.msft.png":::
   <span data-ttu-id="2c51f-216">**L’outil** Réseau affiche désormais **Fetch/XHR** au lieu de **XHR**</span><span class="sxs-lookup"><span data-stu-id="2c51f-216">The **Network** tool now shows **Fetch/XHR** instead of **XHR**</span></span>
:::image-end:::

<span data-ttu-id="2c51f-217">Pour plus d’informations, accédez à :</span><span class="sxs-lookup"><span data-stu-id="2c51f-217">For more information, navigate to:</span></span>
*  [<span data-ttu-id="2c51f-218">Spécifications XMLHttpRequest</span><span class="sxs-lookup"><span data-stu-id="2c51f-218">XMLHttpRequest spec</span></span>][XhrSpecWhatwgOrg]
*  [<span data-ttu-id="2c51f-219">Fetch spec</span><span class="sxs-lookup"><span data-stu-id="2c51f-219">Fetch spec</span></span>][FetchSpecWhatwgOrg]

<span data-ttu-id="2c51f-220">Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1201398][CR1201398].</span><span class="sxs-lookup"><span data-stu-id="2c51f-220">To review the history of this feature in the Chromium open-source project, navigate to Issue [1201398][CR1201398].</span></span>


### <a name="filter-wasm-resource-type-in-the-network-tool"></a><span data-ttu-id="2c51f-221">Type de ressource Filter Wasm dans l’outil Réseau</span><span class="sxs-lookup"><span data-stu-id="2c51f-221">Filter Wasm resource type in the Network tool</span></span>

<span data-ttu-id="2c51f-222">Dans **l’outil** Réseau, vous pouvez maintenant sélectionner le nouveau filtre **Wasm** pour filtrer les demandes réseau WebAssembly.</span><span class="sxs-lookup"><span data-stu-id="2c51f-222">In the **Network** tool, you can now select the new **Wasm** filter to filter the WebAssembly network requests.</span></span>

:::image type="complex" source="../../media/2021/05/wasm-network-requests.msft.png" alt-text="Filtrer par Wasm" lightbox="../../media/2021/05/wasm-network-requests.msft.png":::
   <span data-ttu-id="2c51f-224">Filtrer par Wasm</span><span class="sxs-lookup"><span data-stu-id="2c51f-224">Filter by Wasm</span></span>
:::image-end:::

<!-- screenshot uses http://memory-inspector.glitch.me/demo-wasm.html -->

<span data-ttu-id="2c51f-225">Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1103638][CR1103638].</span><span class="sxs-lookup"><span data-stu-id="2c51f-225">To review the history of this feature in the Chromium open-source project, navigate to Issue [1103638][CR1103638].</span></span>


### <a name="compute-intersections-are-now-included-in-the-performance-tool"></a><span data-ttu-id="2c51f-226">Les intersections de calcul sont désormais incluses dans l’outil Performance</span><span class="sxs-lookup"><span data-stu-id="2c51f-226">Compute Intersections are now included in the Performance tool</span></span>

<span data-ttu-id="2c51f-227">Dans **l’outil Performance,** DevTools affiche désormais **les intersections** de calcul dans le graphique graphique.</span><span class="sxs-lookup"><span data-stu-id="2c51f-227">In the **Performance** tool, DevTools now displays **Compute Intersections** in the flame chart.</span></span> <span data-ttu-id="2c51f-228">Ces modifications vous aident à identifier les événements d’observateurs d’intersections et à déboguer la charge de performances potentielle des observateurs d’intersections.</span><span class="sxs-lookup"><span data-stu-id="2c51f-228">These changes help you identify intersection observers events and debug the potential performance overhead of intersection observers.</span></span>

:::image type="complex" source="../../media/2021/05/compute-intersections-in-perf-tool.msft.png" alt-text="Calcul des intersections dans l’outil Performance" lightbox="../../media/2021/05/compute-intersections-in-perf-tool.msft.png":::
   <span data-ttu-id="2c51f-230">Calcul des intersections dans **l’outil Performance**</span><span class="sxs-lookup"><span data-stu-id="2c51f-230">Compute Intersections in the **Performance** tool</span></span>
:::image-end:::

<!-- screenshot uses https://googlechrome.github.io/samples/intersectionobserver -->

<span data-ttu-id="2c51f-231">Pour plus d’informations sur les observateurs d’intersection, [accédez à Confiance, l’observation est préférable : Intersection Observer v2][WebDevIntersectionObserverV2].</span><span class="sxs-lookup"><span data-stu-id="2c51f-231">For more about intersection observers, navigate to [Trust is good, observation is better: Intersection Observer v2][WebDevIntersectionObserverV2].</span></span>  <span data-ttu-id="2c51f-232">Pour plus d’informations sur l’utilisation du graphique graphique, accédez [à Analyser un enregistrement des performances.][DevtoolsEvaluatePerfRefAnalyzeAPerfRecording]</span><span class="sxs-lookup"><span data-stu-id="2c51f-232">For information about using the flame chart, navigate to [Analyze a performance recording][DevtoolsEvaluatePerfRefAnalyzeAPerfRecording].</span></span>  <span data-ttu-id="2c51f-233">Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1199137][CR1199137].</span><span class="sxs-lookup"><span data-stu-id="2c51f-233">To review the history of this feature in the Chromium open-source project, navigate to Issue [1199137][CR1199137].</span></span>


## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="2c51f-234">Télécharger les canaux d’aperçu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2c51f-234">Download the Microsoft Edge preview channels</span></span>

<span data-ttu-id="2c51f-235">Si vous êtes sous Windows, Linux ou macOS, envisagez d'utiliser les [canaux d'aperçu de Microsoft][MicrosoftEdgePreviewChannels] Edge comme navigateur de développement par défaut.</span><span class="sxs-lookup"><span data-stu-id="2c51f-235">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="2c51f-236">Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="2c51f-236">The preview channels give you access to the latest DevTools features.</span></span>


## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="2c51f-237">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2c51f-237">Getting in touch with Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]


<!-- links -->
[DevtoolsEvaluatePerfRefAnalyzeAPerfRecording]: ../../../evaluate-performance/reference.md#analyze-a-performance-recording "Analyser un enregistrement des performances | Documents Microsoft"
<!-- external links -->
[XhrSpecWhatwgOrg]: https://xhr.spec.whatwg.org "Spécifications XMLHttpRequest | WHATWG"
[FetchSpecWhatwgOrg]: https://fetch.spec.whatwg.org "Récupérer les spécifications | WHATWG"

[WebDevIntersectionObserverV2]: https://web.dev/intersectionobserver-v2 "La confiance est bonne, l’observation est préférable : Intersection Observer v2 | web.dev"

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"
[GithubIoDevToolsUsing]: https://microsoft.github.io/vscode-edge-devtools/using.html "Utilisation des outils | GitHub"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux de préversion de Microsoft Edge"

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Mettre à jour une extension manuellement - Extension Marketplace | Visual Studio Code"

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Outils de développement Visual Studio Code | Visual Studio Marketplace"

[YoutubeEdgeStateOfThePlatform]: https://www.youtube.com/watch?v=sU0WRZ0kkNo "Microsoft Edge : état de la plateforme | YouTube"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"
[CR1094406]: https://crbug.com/1094406 "Problème 1094406 : les développeurs souhaitent qu’une visionneuse de commandes sources soit | Chromium bogues"
[CR1174299]: https://crbug.com/1174299 "Problème 1174299 : les conseils client UA ont été supprimés lors du remplacement de la chaîne UA via l’onglet Conditions réseau de Chrome DevTools | Chromium bogues"
[CR1203241]: https://crbug.com/1203241 "Problème 1203241 : éditeur CSS Grid | Chromium bogues"
[CR1076427]: https://crbug.com/1076427 "Problème 1076427 : la console DevTools doit prendre en charge la | Chromium bogues"
[CR1192084]: https://crbug.com/1192084 "Problème 1192084 : ajouter l’option de clic droit « Afficher les détails du cadre » à des balises html/iframe dans les éléments d’affichage | Chromium bogues"
[CR1141824]: https://crbug.com/1141824 "Problème 1141824 : améliorer le signalement des erreurs CORS dans DevTools | Bogues Chromium"
[CR1201398]: https://crbug.com/1201398 "Problème 1201398 : Demande de fonctionnalité : renommer le filtre de type XHR dans le panneau | Chromium bogues"
[CR1103638]: https://crbug.com/1103638 "Problème 1103638 : panneau réseau pour l’affichage des ressources WebAssembly | Chromium bogues"
[CR1199137]: https://crbug.com/1199137 "Problème 1199137 : afficher le coût intersectionObserveur dans le panneau de | Chromium bogues"

> [!NOTE]
> <span data-ttu-id="2c51f-258">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2c51f-258">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>
> <span data-ttu-id="2c51f-259">La page d’origine est disponible [ici](https://developer.chrome.com/blog/new-in-devtools-xx) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)</span><span class="sxs-lookup"><span data-stu-id="2c51f-259">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-xx) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>

<span data-ttu-id="2c51f-260">[ ![ Creative Commons License][CCby4Image]][CCA4IL] This work is licensed under a Creative Commons Attribution [4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2c51f-260">[![Creative Commons License][CCby4Image]][CCA4IL] This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>

[CCA4IL]: https://creativecommons.org/licenses/by/4.0
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen
