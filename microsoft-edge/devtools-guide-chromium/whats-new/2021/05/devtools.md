---
description: Bouton Plus d’outils, documentation en contexte pour commencer à utiliser l’extension DevTools, prise en charge accrue des lecteurs d’écran dans la console, etc.
title: Nouveautés de DevTools (Microsoft Edge 92)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: ebd512800b8e55b5e9c0001c314a7c08fd242d5d
ms.sourcegitcommit: 30817cd9ae187a716d14d06962eb23b32dd54548
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "11590857"
---
# <a name="whats-new-in-devtools-microsoft-edge-92"></a><span data-ttu-id="70240-104">Nouveautés de DevTools (Microsoft Edge 92)</span><span class="sxs-lookup"><span data-stu-id="70240-104">What's New In DevTools (Microsoft Edge 92)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

> [!TIP]
> <span data-ttu-id="70240-105">La **conférence Microsoft Build 2021** s’est tenue du 25 au 27 mai.</span><span class="sxs-lookup"><span data-stu-id="70240-105">The **Microsoft Build 2021** conference was on May 25-27.</span></span>  <span data-ttu-id="70240-106">Voici une vidéo de Build sur les mises à jour de DevTools : [Microsoft Edge | État de la plateforme :][YoutubeEdgeStateOfThePlatform] Microsoft Edge une plateforme attrayante et cohérente avec des outils pour les développeurs.</span><span class="sxs-lookup"><span data-stu-id="70240-106">Here's a video from Build about the updates to DevTools: [Microsoft Edge | State of the Platform][YoutubeEdgeStateOfThePlatform] - Microsoft Edge brings a compelling and consistent platform with tools for developers.</span></span>  <span data-ttu-id="70240-107">À mesure que nos navigateurs hérités ne seront plus pris en charge, Edge sera bientôt le seul navigateur pris en charge par Microsoft sur Windows 10.</span><span class="sxs-lookup"><span data-stu-id="70240-107">As our legacy browsers phase out of support, Edge will soon be the only supported browser from Microsoft on Windows 10.</span></span>  <span data-ttu-id="70240-108">Rejoignez-nous pour en savoir plus sur la dernière version de la plateforme Edge, des outils et des applications web.</span><span class="sxs-lookup"><span data-stu-id="70240-108">Join us to learn about the latest across the Edge platform, tools, and web apps.</span></span>


## <a name="the-close-button-is-no-longer-hidden-when-devtools-is-narrow"></a><span data-ttu-id="70240-109">Le bouton Fermer n’est plus masqué lorsque DevTools est étroit</span><span class="sxs-lookup"><span data-stu-id="70240-109">The Close button is no longer hidden when DevTools is narrow</span></span>

<!-- Title: DevTools is now easier to close -->  
<!-- Subtitle: The Close button in DevTools is always displayed, even when DevTools is docked to the right and the DevTools viewport is narrow. -->  

<span data-ttu-id="70240-110">Dans Microsoft Edge version 91 ou antérieure, \*\*\*\* le bouton Fermer pour fermer DevTools n’est pas affiché lorsque la vue DevTools est étroite.</span><span class="sxs-lookup"><span data-stu-id="70240-110">In Microsoft Edge version 91 or earlier, the **Close** button to close DevTools isn't displayed when the DevTools viewport is narrow.</span></span>  <span data-ttu-id="70240-111">Dans Microsoft Edge version 92, \*\*\*\* le bouton Fermer dans DevTools est toujours présent, quelle que soit la largeur de laport d’affichage DevTools.</span><span class="sxs-lookup"><span data-stu-id="70240-111">In Microsoft Edge version 92, the **Close** button in the DevTools is always present, regardless of the DevTools viewport width.</span></span>

:::image type="complex" source="../../media/2021/05/close-devtools-button-always-displayed.msft.png" alt-text="Le bouton Fermer DevTools est désormais présent même lorsque la vue est étroite" lightbox="../../media/2021/05/close-devtools-button-always-displayed.msft.png":::
   <span data-ttu-id="70240-113">Le **bouton Fermer** DevTools est désormais présent même lorsque la vue est étroite</span><span class="sxs-lookup"><span data-stu-id="70240-113">The **Close** DevTools button is now present even when the viewport is narrow</span></span>  
:::image-end:::  


## <a name="add-tools-quickly-with-the-new-more-tools-button"></a><span data-ttu-id="70240-114">Ajouter rapidement des outils avec le nouveau bouton Plus d’outils</span><span class="sxs-lookup"><span data-stu-id="70240-114">Add tools quickly with the new More Tools button</span></span>

<!-- Title: Add tools quickly with the new More Tools button -->  
<!-- Subtitle: Learn about a new convenient way to open tools in Microsoft Edge DevTools. -->  

<span data-ttu-id="70240-115">Il existe une nouvelle façon d’ouvrir d’autres outils dans \*\*\*\* Microsoft Edge DevTools : le menu Plus d’outils `+` ().</span><span class="sxs-lookup"><span data-stu-id="70240-115">There's a new way to open more tools in Microsoft Edge DevTools: the **More Tools** (`+`) menu.</span></span> <span data-ttu-id="70240-116">Le menu **Plus d’outils** apparaît dans la barre d’outils du panneau principal et dans la barre d’outils du panneau.</span><span class="sxs-lookup"><span data-stu-id="70240-116">The **More Tools** menu appears on the toolbar in the main panel and on the toolbar of the drawer.</span></span> <span data-ttu-id="70240-117">La sélection d’un outil dans le menu **Plus d’outils** l’ajoute à la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="70240-117">Selecting a tool from the **More Tools** menu adds the tool to the toolbar.</span></span>

<span data-ttu-id="70240-118">Pour réorder les onglets de l’une ou l’autre barre d’outils, sélectionnez et faites glisser les onglets.</span><span class="sxs-lookup"><span data-stu-id="70240-118">To reorder the tabs on either toolbar, select and drag the tabs.</span></span>  

<span data-ttu-id="70240-119">Le menu **Plus d’outils** était disponible sous la forme d’une expérience Microsoft Edge version 89 et est désormais toujours présent.</span><span class="sxs-lookup"><span data-stu-id="70240-119">The **More Tools** menu was available as an experiment in Microsoft Edge version 89, and is now always present.</span></span>

:::image type="complex" source="../../media/2021/05/more-tools-button.msft.png" alt-text="Bouton Plus d’outils dans la barre d’outils supérieure et la barre d’outils de caisse" lightbox="../../media/2021/05/more-tools-button.msft.png":::
   <span data-ttu-id="70240-121">Bouton **Plus d’outils** dans la barre d’outils supérieure et la barre d’outils de caisse</span><span class="sxs-lookup"><span data-stu-id="70240-121">The **More Tools** button on the upper toolbar and drawer toolbar</span></span>
:::image-end:::  

:::image type="complex" source="../../media/2021/05/more-tools-menu.msft.png" alt-text="Menu Plus d’outils" lightbox="../../media/2021/05/more-tools-menu.msft.png":::
   <span data-ttu-id="70240-123">Menu **Plus d’outils**</span><span class="sxs-lookup"><span data-stu-id="70240-123">The **More Tools** menu</span></span>
:::image-end:::  


## <a name="improvements-for-hovering-selecting-and-closing-tools"></a><span data-ttu-id="70240-124">Améliorations apportées aux outils de pointage, de sélection et de fermeture</span><span class="sxs-lookup"><span data-stu-id="70240-124">Improvements for hovering, selecting, and closing tools</span></span>

<!-- Title: Improvements to tab interactions -->
<!-- Subtitle: Interactions related to hovering, selecting, and closing tools are more predictable. -->

<span data-ttu-id="70240-125">Les onglets de chaque outil ont été reformatés pour réduire les risques de fermeture accidentelle d’un outil.</span><span class="sxs-lookup"><span data-stu-id="70240-125">Tabs for each tool have been reformatted to reduce the chance of accidentally closing a tool.</span></span>  <span data-ttu-id="70240-126">Dans chaque onglet de la barre d’outils principale et de la barre d’outils du caisse, nous avons ajouté :</span><span class="sxs-lookup"><span data-stu-id="70240-126">On each tab in the main toolbar and in the toolbar of the drawer, we added:</span></span>
*  <span data-ttu-id="70240-127">Espacement autour de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="70240-127">Spacing around the tab.</span></span>
*  <span data-ttu-id="70240-128">Espacement autour du bouton fermer ( `x` ) dans l’onglet.</span><span class="sxs-lookup"><span data-stu-id="70240-128">Spacing around the close (`x`) button in the tab.</span></span>
*  <span data-ttu-id="70240-129">Couleur d’arrière-plan lorsque vous placez le pointage sur l’onglet.</span><span class="sxs-lookup"><span data-stu-id="70240-129">A background color when hovering over the tab.</span></span>
*  <span data-ttu-id="70240-130">Une boîte à outils pour le bouton fermer ( `x` ) de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="70240-130">A tooltip for the close (`x`) button of the tab.</span></span>
*  <span data-ttu-id="70240-131">Contraste plus élevé pour le bouton fermer ( `x` ) de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="70240-131">Higher contrast for the close (`x`) button of the tab.</span></span>

<span data-ttu-id="70240-132">Par exemple, lorsque vous êtes dans l’outil **Performances** et que vous pointez sur l’onglet de l’outil Réseau, ces améliorations permettent d’éviter la fermeture accidentelle de l’outil Réseau. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="70240-132">For example, when you are in the **Performance** tool and you hover over the **Network** tool's tab, these improvements help prevent accidentally closing the **Network** tool.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-before.msft.png" alt-text="Onglets avant la reformatage" lightbox="../../media/2021/05/hovering-on-tool-tab-before.msft.png":::
           <span data-ttu-id="70240-134">Onglets avant la reformatage</span><span class="sxs-lookup"><span data-stu-id="70240-134">Tabs before reformatting</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-after.msft.png" alt-text="Onglets après la reformatage" lightbox="../../media/2021/05/hovering-on-tool-tab-after.msft.png":::
           <span data-ttu-id="70240-136">Onglets après la reformatage</span><span class="sxs-lookup"><span data-stu-id="70240-136">Tabs after reformatting</span></span> :::image-end:::
    :::column-end:::
:::row-end:::

<span data-ttu-id="70240-137">Ces améliorations sont particulièrement pertinentes pour les utilisateurs de DevTools localisées, dans lesquelles les onglets peuvent être plus étroits et plus faciles à fermer accidentellement.</span><span class="sxs-lookup"><span data-stu-id="70240-137">These improvements are especially relevant for users of localized DevTools, in which the tabs may be narrower and easier to accidentally close.</span></span>

:::image type="complex" source="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png" alt-text="DevTools localisées avec des onglets étroits" lightbox="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png":::
   <span data-ttu-id="70240-139">DevTools localisées avec des onglets étroits</span><span class="sxs-lookup"><span data-stu-id="70240-139">Localized DevTools with narrow tabs</span></span>
:::image-end:::

<span data-ttu-id="70240-140">Nous avons également facilité la ré-ajout d’un outil que vous avez fermé en ajoutant un [menu](#add-tools-quickly-with-the-new-more-tools-button) Plus d’outils à la barre d’outils principale et à la barre d’outils des caisses.</span><span class="sxs-lookup"><span data-stu-id="70240-140">We also made it easier to re-add a tool that you closed by adding a [More Tools menu](#add-tools-quickly-with-the-new-more-tools-button) to the main toolbar and drawer toolbar.</span></span>


## <a name="better-support-for-screen-readers-in-the-console"></a><span data-ttu-id="70240-141">Meilleure prise en charge des lecteurs d’écran dans la console</span><span class="sxs-lookup"><span data-stu-id="70240-141">Better support for screen readers in the Console</span></span>

<!-- Title: Better screen reader support in the Console -->
<!-- Subtitle: Assistive technologies can now announce autocomplete suggestions and evaluated expressions in the Console. -->

<span data-ttu-id="70240-142">Avant Microsoft Edge version 92, dans la **console,** les technologies d’assistance telles que les lecteurs d’écran n’annoncaient pas les suggestions de mise à jour automatique ou les résultats des expressions évaluées.</span><span class="sxs-lookup"><span data-stu-id="70240-142">Prior to Microsoft Edge version 92, in the **Console**, assistive technologies such as screen readers didn't announce autocomplete suggestions or the results of evaluated expressions.</span></span> <span data-ttu-id="70240-143">This has been fixed now.</span><span class="sxs-lookup"><span data-stu-id="70240-143">This has been fixed now.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png" alt-text="Dans la console, les lecteurs d’écran annoncent désormais la suggestion de mise à l’écran sélectionnée" lightbox="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png":::
           <span data-ttu-id="70240-145">Dans la **console,** les lecteurs d’écran annoncent désormais la suggestion de mise à l’écran sélectionnée</span><span class="sxs-lookup"><span data-stu-id="70240-145">In the **Console**, screen readers now announce the currently selected autocomplete suggestion</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png" alt-text="Dans la console, les lecteurs d’écran annoncent désormais le résultat d’une expression évaluée" lightbox="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png":::
           <span data-ttu-id="70240-147">Dans la **console,** les lecteurs d’écran annoncent désormais le résultat d’une expression évaluée</span><span class="sxs-lookup"><span data-stu-id="70240-147">In the **Console**, screen readers now announce the result of an evaluated expression</span></span> :::image-end:::
    :::column-end:::
:::row-end:::


## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-118"></a><span data-ttu-id="70240-148">Microsoft Edge Outils de développement Visual Studio Code version 1.1.8</span><span class="sxs-lookup"><span data-stu-id="70240-148">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.8</span></span>

<span data-ttu-id="70240-149">Les [outils Microsoft Edge développeur][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] Visual Studio Code version 1.1.8 pour Microsoft Visual Studio Code ont les modifications suivantes depuis la version précédente.</span><span class="sxs-lookup"><span data-stu-id="70240-149">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.8 for Microsoft Visual Studio Code has the following changes since the previous release.</span></span>  <span data-ttu-id="70240-150">Microsoft Visual Studio Code met automatiquement à jour les extensions.</span><span class="sxs-lookup"><span data-stu-id="70240-150">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="70240-151">Pour mettre à jour manuellement la version 1.1.8, accédez à Mettre à jour [une extension manuellement.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="70240-151">To manually update to version 1.1.8, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  

<span data-ttu-id="70240-152">Vous pouvez déposer des problèmes et contribuer à l’extension sur le GitHub [vscode-edge-devtools.][GithubMicrosoftVscodeEdgeDevtools]</span><span class="sxs-lookup"><span data-stu-id="70240-152">You can file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

### <a name="in-context-documentation-and-ui-to-make-it-easier-to-use-the-devtools-extension"></a><span data-ttu-id="70240-153">Documentation en contexte et interface utilisateur pour faciliter l’utilisation de l’extension DevTools</span><span class="sxs-lookup"><span data-stu-id="70240-153">In-context documentation and UI to make it easier to use the DevTools extension</span></span>

<!-- Title: In-context documentation and UI make it easier to get started using the Developer Tools extension -->  
<!-- Subtitle: The Microsoft Edge Developer Tools for Visual Studio Code extension now presents helpful text, buttons, and links, and opens a documentation page with guidance on how to get started. -->  

<span data-ttu-id="70240-154">La version 1.1.8 de l’extension [outils][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] de développement Microsoft Edge pour Visual Studio Code offre désormais un moyen plus simple de démarrer une nouvelle instance de Microsoft Edge, en présentant des instructions, des boutons, des liens et une page de documentation pour vous guider.</span><span class="sxs-lookup"><span data-stu-id="70240-154">Version 1.1.8 of the [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension now features a simpler way to start a new instance of Microsoft Edge, by presenting instructions, buttons, links, and a documentation page to guide you.</span></span>

*  <span data-ttu-id="70240-155">Lorsque vous sélectionnez le bouton **Outils Microsoft Edge** dans la barre d’activité de Visual Studio Code, le panneau \*\*\*\* **Outils Microsoft Edge** : Cibles présente désormais un texte explicatif, des boutons et des liens pour vous guider, au lieu d’un panneau vide.</span><span class="sxs-lookup"><span data-stu-id="70240-155">When you select the **Microsoft Edge Tools** button in the **Activity Bar** of Visual Studio Code, the **Microsoft Edge Tools: Targets** panel now presents explanatory text, buttons, and links to guide you, instead of a blank panel.</span></span>

*  <span data-ttu-id="70240-156">Lorsque vous ouvrez une nouvelle instance de Microsoft Edge à partir de Visual Studio Code, Microsoft Edge affiche désormais une page de démarrage qui explique comment utiliser l’extension Outils de développement, au lieu d’une page vierge.</span><span class="sxs-lookup"><span data-stu-id="70240-156">When you open a new instance of Microsoft Edge from within Visual Studio Code, Microsoft Edge now shows a start page that explains how to use the Developer Tools extension, instead of a blank page.</span></span>

*  <span data-ttu-id="70240-157">Le **panneau Microsoft Edge Outils** : Cibles possède désormais une launch.jsgénérer une **launch.js** sur le bouton et des instructions, pour vous aider à lancer votre projet pour le débogage dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="70240-157">The **Microsoft Edge Tools: Targets** panel now has a **Generate launch.json** button and instructions, to help launch your project for debugging in Microsoft Edge.</span></span>

<span data-ttu-id="70240-158">Pour plus d’informations, accédez à [Utiliser les outils.][GithubIoDevToolsUsing]</span><span class="sxs-lookup"><span data-stu-id="70240-158">For more information, navigate to [Using the tools][GithubIoDevToolsUsing].</span></span>


## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="70240-159">Télécharger les canaux d’aperçu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="70240-159">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="70240-160">Si vous êtes sous Windows, Linux ou macOS, envisagez d'utiliser les [canaux d'aperçu de Microsoft][MicrosoftEdgePreviewChannels] Edge comme navigateur de développement par défaut.</span><span class="sxs-lookup"><span data-stu-id="70240-160">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="70240-161">Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="70240-161">The preview channels give you access to the latest DevTools features.</span></span>  


## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="70240-162">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="70240-162">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubIoDevToolsUsing]: https://microsoft.github.io/vscode-edge-devtools/using.html "Utilisation des outils | GitHub"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux de préversion de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Mettre à jour une extension manuellement - Extension Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Outils de développement pour Visual Studio Code | Visual Studio Marketplace"  

[YoutubeEdgeStateOfThePlatform]: https://www.youtube.com/watch?v=sU0WRZ0kkNo "Microsoft Edge : état de la plateforme | YouTube"

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="70240-170">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="70240-170">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
