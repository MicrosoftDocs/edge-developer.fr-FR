---
description: Prise en charge du débogage de CSS Flexbox, affichage des performances sur la page web, mise à jour des outils de résolution des problèmes, etc.
title: Nouveautés de DevTools (Microsoft Edge 90)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, développement web, outils f12, devtools
ms.localizationpriority: high
ms.openlocfilehash: a6682043166909bf75a875b72058cc9839c5b43b
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564846"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-90"></a><span data-ttu-id="a39ea-104">Quoi de neuf dans DevTools (Microsoft Edge 90)</span><span class="sxs-lookup"><span data-stu-id="a39ea-104">What's New In DevTools (Microsoft Edge 90)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="group-tools-together-in-focus-mode"></a><span data-ttu-id="a39ea-105">Regrouper les outils en mode Focus</span><span class="sxs-lookup"><span data-stu-id="a39ea-105">Group tools together in Focus Mode</span></span>  

<!-- Title: Grouping the tools in Focus Mode  -->  
<!-- Subtitle: Organize your favorite tools into groups with the new Focus Mode UI.  -->  

<span data-ttu-id="a39ea-106">Focus Mode est une interface expérimentale qui vous permet de regrouper différents outils en fonction de vos propres scénarios de débogage.</span><span class="sxs-lookup"><span data-stu-id="a39ea-106">Focus Mode is an experimental interface that allows you to group different tools together based on your own debugging scenarios.</span></span>  <span data-ttu-id="a39ea-107">La nouvelle **barre d'activités** affichée à gauche comprend des groupes d'outils prédéfinis tels que la **disposition** et le **débogage**.</span><span class="sxs-lookup"><span data-stu-id="a39ea-107">The new **Activity Bar** displayed on the left includes predefined tool groups such as **Layout** and **Debugging**.</span></span>  <span data-ttu-id="a39ea-108">Pour personnaliser chaque groupe d'outils, fermez les outils à l'aide de l'icône **Fermer** ((`X`\ )) ou ajoutez de nouveaux outils à l'aide de l'icône **Autres outils** (`+`\ ).</span><span class="sxs-lookup"><span data-stu-id="a39ea-108">To customize each tool group, close tools with the **Close** \(`X`\) icon or add new tools with the **More tools** \(`+`\) icon.</span></span>  

<span data-ttu-id="a39ea-109">Pour activer l'expérience, naviguez jusqu'à [Activer les fonctions][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] expérimentales et cochez les cases situées à côté de **Focus Mode et DevTools Tooltips** et \*\*Activez les menus de l'onglet du bouton + pour ouvrir plus d'outils \*\*.</span><span class="sxs-lookup"><span data-stu-id="a39ea-109">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkboxes next to **Focus Mode and DevTools Tooltips** and **Enable + button tab menus to open more tools**.</span></span>  <span data-ttu-id="a39ea-110">Pour plus d'informations sur cette fonctionnalité ou pour commenter avec des questions et des idées, naviguez vers [DevTools : Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span><span class="sxs-lookup"><span data-stu-id="a39ea-110">For more information about this feature or to comment with questions and ideas, navigate to [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span></span>  

:::image type="complex" source="../../media/2021/02/focus-mode.msft.png" alt-text="Afficher la barre d'activité" lightbox="../../media/2021/02/focus-mode.msft.png":::
   <span data-ttu-id="a39ea-112">Afficher la barre **d'activité** </span><span class="sxs-lookup"><span data-stu-id="a39ea-112">Display the **Activity Bar**</span></span>  
:::image-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a><span data-ttu-id="a39ea-113">En savoir plus sur DevTools grâce à des infobulles informatives</span><span class="sxs-lookup"><span data-stu-id="a39ea-113">Learn about DevTools with informative tooltips</span></span>  

<!-- Title: DevTools Tooltips  -->  
<!-- Subtitle: Learn more about how to use DevTools with informative DevTools tooltips.  -->  

<span data-ttu-id="a39ea-114">La fonctionnalité DevTools Tooltips vous aide à connaître les différents outils et volets.</span><span class="sxs-lookup"><span data-stu-id="a39ea-114">The DevTools Tooltips feature helps you learn about all the different tools and panes.</span></span>  <span data-ttu-id="a39ea-115">Cliquez sur l'icône Aide \(`?`\) en bas de la **barre d'activités** pour activer les infobulles dans les outils de développement.</span><span class="sxs-lookup"><span data-stu-id="a39ea-115">Choose the Help \(`?`\) icon at the bottom of the **Activity Bar** to toggle tooltips in the DevTools.</span></span>  <span data-ttu-id="a39ea-116">Lorsque les infobulles sont activées, passez la souris sur chaque région délimitée de DevTools pour en savoir plus sur l'utilisation de l'outil.</span><span class="sxs-lookup"><span data-stu-id="a39ea-116">When tooltips are on, hover over each outlined region of DevTools to learn more about how to use the tool.</span></span>  <span data-ttu-id="a39ea-117">Pour activer l'expérience, naviguez jusqu'à [Activer les fonctions][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] expérimentales et cochez les cases situées à côté de **Focus Mode et DevTools Tooltips** et \*\*Activez les menus de l'onglet du bouton + pour ouvrir plus d'outils \*\*.</span><span class="sxs-lookup"><span data-stu-id="a39ea-117">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkboxes next to **Focus Mode and DevTools Tooltips** and **Enable + button tab menus to open more tools**.</span></span>  <span data-ttu-id="a39ea-118">Pour plus d'informations sur cette fonctionnalité ou pour commenter avec des questions et des idées, naviguez vers [DevTools : Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span><span class="sxs-lookup"><span data-stu-id="a39ea-118">For more information about this feature or to comment with questions and ideas, navigate to [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span></span>  

:::image type="complex" source="../../media/2021/02/focus-mode-and-tooltips-help.msft.png" alt-text="Choisissez l'icône d'aide ( ?) dans la barre d'activités pour afficher les infobulles." lightbox="../../media/2021/02/focus-mode-and-tooltips-help.msft.png":::
   <span data-ttu-id="a39ea-120">Choisissez l'icône Aide \(`?`\) dans la **barre d'activités** pour afficher les infobulles.</span><span class="sxs-lookup"><span data-stu-id="a39ea-120">Choose the Help \(`?`\) icon in the **Activity Bar** to display tooltips</span></span>  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a><span data-ttu-id="a39ea-121">Personnaliser les raccourcis clavier dans les paramètres</span><span class="sxs-lookup"><span data-stu-id="a39ea-121">Customize keyboard shortcuts in Settings</span></span>  

<!-- Title: Change keyboard shortcuts in Settings  -->  
<!-- TODO:  Rachel's feedback is about the fact that this experimental feature is turned on by default, may have separate section in What's New for experimental features)  -->  
<!-- Subtitle: Make DevTools work better for you by creating new keyboard shortcuts for any action in the DevTools.  -->  

<span data-ttu-id="a39ea-122">Vous pouvez désormais personnaliser le raccourci clavier pour toute action dans les DevTools.</span><span class="sxs-lookup"><span data-stu-id="a39ea-122">You may now customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="a39ea-123">Pour modifier un raccourci clavier, effectuez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="a39ea-123">To edit a keyboard shortcut, complete the following actions.</span></span>  

1.  <span data-ttu-id="a39ea-124">Ouvrez le DevTools, puis choisissez\*\* Paramètres\*\* > \*\* Raccourcis \*\*.</span><span class="sxs-lookup"><span data-stu-id="a39ea-124">Open the DevTools, and then choose **Settings** > **Shortcuts**.</span></span>  
1.  <span data-ttu-id="a39ea-125">Choisissez l'action que vous voulez personnaliser.</span><span class="sxs-lookup"><span data-stu-id="a39ea-125">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="a39ea-126">Choisissez l'option Modifier (</span><span class="sxs-lookup"><span data-stu-id="a39ea-126">Choose the Edit \(</span></span>![Icône de raccourci clavier pour l'édition](../../media/2021/02/edit-keyboard-shortcut-icon.msft.png)<span data-ttu-id="a39ea-128">\icône.</span><span class="sxs-lookup"><span data-stu-id="a39ea-128">\) icon.</span></span>  
1.  <span data-ttu-id="a39ea-129">Sélectionnez les touches que vous voulez lier à l'action.</span><span class="sxs-lookup"><span data-stu-id="a39ea-129">Select the keys you want to bind to the action.</span></span>  
1.  <span data-ttu-id="a39ea-130">Choisissez la coche \(</span><span class="sxs-lookup"><span data-stu-id="a39ea-130">Choose the checkmark \(</span></span>![Cochez l'icône du raccourci clavier](../../media/2021/02/checkmark-keyboard-shortcut-icon.msft.png)<span data-ttu-id="a39ea-132">\icône.</span><span class="sxs-lookup"><span data-stu-id="a39ea-132">\) icon.</span></span>  
    
<span data-ttu-id="a39ea-133">Pour plus d'informations sur la personnalisation et la modification des raccourcis, consultez la section [Personnaliser les raccourcis clavier dans les DevTools de Microsoft Edge ][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="a39ea-133">For more information about customizing and editing shortcuts, navigate to [Customize keyboard shortcuts in the Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="a39ea-134">Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source Chromium, consultez le numéro [174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="a39ea-134">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png" alt-text="Personnaliser les raccourcis clavier dans les Paramètres DevTools sur Raccourcis avec un raccourci en mode édition" lightbox="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png":::
   <span data-ttu-id="a39ea-136">Personnaliser les raccourcis clavier dans les [Paramètres DevTools][DevtoolsCustomizeIndexSettings] sur Raccourcis avec un raccourci en mode édition</span><span class="sxs-lookup"><span data-stu-id="a39ea-136">Customize keyboard shortcuts in the [DevTools Settings][DevtoolsCustomizeIndexSettings] on Shortcuts with a shortcut in edit mode</span></span>  
:::image-end:::  

## <a name="microsoft-edge-devtools-for-visual-studio-code-extension-update-114"></a><span data-ttu-id="a39ea-137">Mise à jour de l'extension Microsoft Edge DevTools pour Visual Studio Code 1.1.4</span><span class="sxs-lookup"><span data-stu-id="a39ea-137">Microsoft Edge DevTools for Visual Studio Code extension update 1.1.4</span></span>  

<!-- Title: Edge Devtools for Visual Studio code extension update 1.1.4  -->  
<!-- Subtitle: Latest changes including a favicon is displayed next to each of the instances and console messages from the browser are displayed in the console of Visual Studio Code.  -->  

<span data-ttu-id="a39ea-138">Les [outils de développement Microsoft Edge pour Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools], version 1.1.4 de l'extension Microsoft Visual Studio Code, affichent désormais un favicon à côté de chacune des instances DevTools.</span><span class="sxs-lookup"><span data-stu-id="a39ea-138">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.4 for Microsoft Visual Studio Code now displays a favicon next to each of the DevTools instances.</span></span>  <span data-ttu-id="a39ea-139">Les messages de console de Microsoft Edge s'affichent désormais dans la **console DevTools** sous la rubrique **Sortie** du code Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a39ea-139">Console messages from Microsoft Edge now display in the **DevTools Console** under **Output** of Microsoft Visual Studio Code.</span></span>  <span data-ttu-id="a39ea-140">Microsoft Visual Studio Code met automatiquement à jour les extensions.</span><span class="sxs-lookup"><span data-stu-id="a39ea-140">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="a39ea-141">Pour mettre à jour manuellement la version 1.1.4, naviguez [jusqu'à Mettre à jour une extension manuellement ][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span><span class="sxs-lookup"><span data-stu-id="a39ea-141">To manually update to version 1.1.4, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  <span data-ttu-id="a39ea-142">Vous pouvez déposer des questions et contribuer à l'extension sur le [repo GitHub de ][GithubMicrosoftVscodeEdgeDevtools]vscode-edge-devtools.</span><span class="sxs-lookup"><span data-stu-id="a39ea-142">You may file issues and contribute to the extension on the [vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools] GitHub repo.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="a39ea-143">La figure suivante affiche les messages d'un exemple de page Web enregistrée dans l'outil **Console** de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a39ea-143">The following figure displays messages from an example webpage logged in the **Console** tool in Microsoft Edge.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="a39ea-144">La figure suivante affiche les mêmes messages de la page Web d'exemple enregistrés dans la **DevTools Console** sous **Sortie** du code Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a39ea-144">The following figure displays the same messages from the example webpage logged in the **DevTools Console** under **Output** of Microsoft Visual Studio Code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png" alt-text="Afficher un message dans la console dans Microsoft Edge DevTools" lightbox="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png":::
         <span data-ttu-id="a39ea-146">Afficher un message dans la console dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a39ea-146">Display a message in Console in Microsoft Edge DevTools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png" alt-text="Affichez le même message dans la console DevTools sous Sortie du code Microsoft Visual Studio." lightbox="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png":::
         <span data-ttu-id="a39ea-148">Affichez le même message dans la console DevTools sous Sortie du code Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a39ea-148">Display the same message in the DevTools Console under Output of Microsoft Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-flexbox-editing-with-visual-flexbox-editor-and-multiple-overlays"></a><span data-ttu-id="a39ea-149">Amélioration de l'édition de CSS flexbox avec un éditeur visuel de flexbox et des superpositions multiples</span><span class="sxs-lookup"><span data-stu-id="a39ea-149">Improved CSS flexbox editing with visual flexbox editor and multiple overlays</span></span>  

<!-- Title: Try different CSS flexbox layouts with the visual flexbox editor  -->  
<!-- Subtitle: In the Styles pane, choose the icon that appears next to display: flex to try different layout properties for flex containers.  -->  

<span data-ttu-id="a39ea-150">DevTools dispose désormais d'outils de débogage CSS flexbox dédiés.</span><span class="sxs-lookup"><span data-stu-id="a39ea-150">DevTools now has dedicated CSS flexbox debugging tools.</span></span>  <span data-ttu-id="a39ea-151">Si le style `display: flex`ou`display: inline-flex` CSS est appliqué à un élément HTML, une `flex`icône s'affiche à côté de cet élément dans l'outil **Éléments**.</span><span class="sxs-lookup"><span data-stu-id="a39ea-151">If the `display: flex` or `display: inline-flex` CSS style is applied to an HTML element, a `flex` icon displays next to that element in the **Elements** tool.</span></span>  <span data-ttu-id="a39ea-152">Pour afficher (ou masquer) une superposition flexible sur la page Web, cliquez sur `flex`l'icône.</span><span class="sxs-lookup"><span data-stu-id="a39ea-152">To display \(or hide\) a flex overlay on the webpage, choose the `flex` icon.</span></span>  <span data-ttu-id="a39ea-153">Pour connaître l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez les numéros[1166710][CR1166710] et [1175699][CR1175699].</span><span class="sxs-lookup"><span data-stu-id="a39ea-153">To review the history of this feature in the Chromium open-source project, navigate to Issues [1166710][CR1166710] and [1175699][CR1175699].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="a39ea-154">Pour ouvrir l'éditeur **Flexbox**, accédez au volet **Styles** et cliquez sur la nouvelle icône située à côté du `display: flex`style`display: inline-flex` ou.</span><span class="sxs-lookup"><span data-stu-id="a39ea-154">To open the **Flexbox** editor, navigate to the **Styles** pane and choose the new icon next to the `display: flex` or `display: inline-flex` style.</span></span>  <span data-ttu-id="a39ea-155">L'éditeur **Flexbox** offre un moyen rapide de modifier les propriétés de la boîte flexible.</span><span class="sxs-lookup"><span data-stu-id="a39ea-155">The **Flexbox** editor provides a quick way to edit the flexbox properties.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="a39ea-156">De plus, la section **Flexbox** du volet **Mise en page affiche** tous les éléments Flexbox de la page Web.</span><span class="sxs-lookup"><span data-stu-id="a39ea-156">In addition, the **Flexbox** section in the **Layout** pane displays all of the flexbox elements on the webpage.</span></span>  <span data-ttu-id="a39ea-157">Vous pouvez basculer la superposition de chaque élément.</span><span class="sxs-lookup"><span data-stu-id="a39ea-157">You may toggle the overlay of each element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-styles-display-flex-window.msft.png" alt-text="Outils de débogage CSS flexbox" lightbox="../../media/2021/02/elements-styles-display-flex-window.msft.png":::
         <span data-ttu-id="a39ea-159">Outils de débogage CSS flexbox</span><span class="sxs-lookup"><span data-stu-id="a39ea-159">CSS flexbox debugging tools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png" alt-text="Section Flexbox dans le volet Mise en page" lightbox="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png":::
         <span data-ttu-id="a39ea-161">**Section Flexbox** dans le **volet** De disposition</span><span class="sxs-lookup"><span data-stu-id="a39ea-161">**Flexbox** section in the **Layout** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="keyboard-navigation-improvements-for-network-requests"></a><span data-ttu-id="a39ea-162">Amélioration de la navigation au clavier pour les demandes de réseau</span><span class="sxs-lookup"><span data-stu-id="a39ea-162">Keyboard navigation improvements for network requests</span></span>  

<!-- Title: Navigate the request initiator chain in the Network tool with the keyboard  -->  
<!-- Subtitle: The Initiator pane may now be expanded or collapsed with the arrow keys.  -->  

<span data-ttu-id="a39ea-163">Auparavant, vous ne pouviez pas développer ou réduire la chaîne de demandes à l'aide des touches fléchées du clavier dans le volet **Initiateur**, contrairement au DOM dans l'outil\*\* Éléments\*\*.</span><span class="sxs-lookup"><span data-stu-id="a39ea-163">Previously, you were not able to expand or collapse the chain of requests using the arrow keys on the keyboard in the **Initiator** pane, unlike the DOM in the **Elements** tool.</span></span>  <span data-ttu-id="a39ea-164">Lorsqu'une demande de **réseau** est sélectionnée dans l'outil Réseau, le volet **Initiateur** affiche la chaîne des demandes qui ont initié la demande actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="a39ea-164">When a network request is selected in the **Network** tool, the **Initiator** pane displays the chain of requests that initiated the currently selected request.</span></span>  

<span data-ttu-id="a39ea-165">Dans Microsoft Edge version 90, vous pouvez développer ou réduire la chaîne de demandes à l'aide des touches fléchées du clavier dans le volet **Initiateur**.</span><span class="sxs-lookup"><span data-stu-id="a39ea-165">In Microsoft Edge version 90, you may expand or collapse the chain of requests using the arrow keys on the keyboard in the **Initiator** pane.</span></span>  <span data-ttu-id="a39ea-166">La demande de réseau ciblée dans la chaîne est également mise en évidence.</span><span class="sxs-lookup"><span data-stu-id="a39ea-166">The focused network request in the chain is also now highlighted.</span></span>  <span data-ttu-id="a39ea-167">Pour en savoir plus sur les initiateurs dans l'outil **Réseau**, naviguez [jusqu'à Afficher les initiateurs et les dépendances][DevtoolsNetworkReferenceDisplayInitiatorsDependencies].</span><span class="sxs-lookup"><span data-stu-id="a39ea-167">To learn more about initiators in the **Network** tool, navigate to [Display initiators and dependencies][DevtoolsNetworkReferenceDisplayInitiatorsDependencies].</span></span>  <span data-ttu-id="a39ea-168">Pour revoir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez les numéros [1158276][CR1158276] et [1160637][CR1160637].</span><span class="sxs-lookup"><span data-stu-id="a39ea-168">To review the history of this feature in the Chromium open-source project, navigate to Issues [1158276][CR1158276] and [1160637][CR1160637].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain.msft.png" alt-text="Choisissez une demande de réseau et sélectionnez le volet Initiateur." lightbox="../../media/2021/02/network-request-initiator-chain.msft.png":::
         <span data-ttu-id="a39ea-170">Choisissez une demande de réseau et sélectionnez le volet **Initiateur**.</span><span class="sxs-lookup"><span data-stu-id="a39ea-170">Choose a Network request and choose the **Initiator** pane</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png" alt-text="Développez ou réduisez la chaîne des initiateurs de demande et suivez la ligne en surbrillance." lightbox="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png":::
         <span data-ttu-id="a39ea-172">Développez ou réduisez la chaîne des initiateurs de demande et suivez la ligne en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="a39ea-172">Expand or collapse the request initiator chain and follow the highlighted row</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="filtering-in-the-console-is-more-consistent"></a><span data-ttu-id="a39ea-173">Le filtrage dans la console est plus cohérent</span><span class="sxs-lookup"><span data-stu-id="a39ea-173">Filtering in the Console is more consistent</span></span>  

<!-- Title: Console improvements make filtering more consistent  -->  
<!-- Subtitle: The Log Levels dropdown is more clearly disabled when using filters in the Console sidebar.  -->  

<span data-ttu-id="a39ea-174">Lorsque vous filtrez dans la [barre latérale de la console][DevtoolsConsoleReferenceOpenConsoleSidebar], les filtres de la liste déroulante des [niveaux de journal][DevtoolsConsoleReferenceFilterByLogLevel] ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="a39ea-174">While you filter with the [Console Sidebar][DevtoolsConsoleReferenceOpenConsoleSidebar], the filters in the [Log Levels][DevtoolsConsoleReferenceFilterByLogLevel] dropdown are not available.</span></span>  <span data-ttu-id="a39ea-175">Auparavant, la liste déroulante des **niveaux de journal** s'affichait en surbrillance lorsque vous la survoliez, même si un filtre de la **barre latérale de la console** était sélectionné.</span><span class="sxs-lookup"><span data-stu-id="a39ea-175">Previously, the **Log Levels** dropdown highlighted when you hovered on it, even while a filter from the **Console Sidebar** was chosen.</span></span>  <span data-ttu-id="a39ea-176">Dans la version 90 de Microsoft Edge, la liste déroulante des **niveaux de journal** ne s'affiche plus lorsque vous la survolez alors qu'un filtre de la **barre latérale de la console** est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="a39ea-176">In Microsoft Edge version 90, the **Log Levels** dropdown no longer highlights when you hover on it while a filter from the **Console Sidebar** is chosen.</span></span>  <span data-ttu-id="a39ea-177">Pour en savoir plus sur le filtrage dans la **console**, allez à [Filtrer les messages][DevtoolsConsoleReferenceFilterMessages].</span><span class="sxs-lookup"><span data-stu-id="a39ea-177">To learn more about filtering in the **Console**, navigate to [Filter Messages][DevtoolsConsoleReferenceFilterMessages].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-old.msft.png" alt-text="Auparavant, si vous ouvrez la barre latérale de la console et que vous survolez les niveaux par défaut, ils étaient mis en évidence." lightbox="../../media/2021/02/console-sidebar-default-levels-old.msft.png":::
         <span data-ttu-id="a39ea-179">Auparavant, si vous ouvrez **la barre latérale de la console** et que vous survolez les **niveaux par défaut**, ils étaient mis en évidence.</span><span class="sxs-lookup"><span data-stu-id="a39ea-179">Previously, if you open the **Console sidebar** and hover on **Default levels** it was highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-new.msft.png" alt-text="À partir de Microsoft Edge 90, si vous choisissez la barre latérale Console et que vous survolez les niveaux par défaut, ils ne sont pas mis en évidence." lightbox="../../media/2021/02/console-sidebar-default-levels-new.msft.png":::
         <span data-ttu-id="a39ea-181">À partir de Microsoft Edge 90, si vous choisissez la **barre latérale Console** et survolez les **niveaux par défaut**, ils ne sont pas mis en évidence.</span><span class="sxs-lookup"><span data-stu-id="a39ea-181">Starting in Microsoft Edge 90, if you choose the **Console sidebar** and hover on **Default levels**, it does not highlight</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="a39ea-182">Annonces du projet Chromium</span><span class="sxs-lookup"><span data-stu-id="a39ea-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="the-console-now-escapes-double-quote-characters"></a><span data-ttu-id="a39ea-183">La console échappe désormais les caractères de guillemets doubles</span><span class="sxs-lookup"><span data-stu-id="a39ea-183">The Console now escapes double quote characters</span></span>  

<span data-ttu-id="a39ea-184">Auparavant, la **console** n'affichait pas les \(`"`\)caractères guillemets doubles valides dans les chaînes JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a39ea-184">Previously, the **Console** did not output valid double quote \(`"`\) characters in JavaScript strings.</span></span>  <span data-ttu-id="a39ea-185">À partir de la version 90 de Microsoft Edge, la **console** produit des chaînes JavaScript en utilisant des \(`"`\)caractères guillemets doubles échappés.</span><span class="sxs-lookup"><span data-stu-id="a39ea-185">Starting in Microsoft Edge version 90, the **Console** outputs JavaScript strings using escaped double quote \(`"`\) characters.</span></span>  <span data-ttu-id="a39ea-186">Pour revoir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez le numéro [1178530][CR1178530].</span><span class="sxs-lookup"><span data-stu-id="a39ea-186">To review the history of this feature in the Chromium open-source project, navigate to Issue [1178530][CR1178530].</span></span>  

:::image type="complex" source="../../media/2021/02/console-string-formatted-double-quotes.msft.png" alt-text="La console produit des chaînes JavaScript en utilisant des caractères de guillemets doubles échappés (&#0022 ;)." lightbox="../../media/2021/02/console-string-formatted-double-quotes.msft.png":::
   <span data-ttu-id="a39ea-188">La **console** produit des chaînes JavaScript en utilisant des \(`"`\)caractères échappés de type guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="a39ea-188">The **Console** outputs JavaScript strings using escaped double quote \(`"`\) characters</span></span>  
:::image-end:::  

### <a name="emulate-the-css-color-gamut-media-feature"></a><span data-ttu-id="a39ea-189">Emuler la fonction CSS color-gamut media</span><span class="sxs-lookup"><span data-stu-id="a39ea-189">Emulate the CSS color-gamut media feature</span></span>  

<span data-ttu-id="a39ea-190">La [requête média][ChromestatusFeature5354410980933632] color-gamut émule la gamme approximative de couleurs prises en charge par le navigateur et le périphérique que vous testez.</span><span class="sxs-lookup"><span data-stu-id="a39ea-190">The [color-gamut][ChromestatusFeature5354410980933632] media query emulates the approximate range of colors supported by the browser and the device you are testing.</span></span>  <span data-ttu-id="a39ea-191">La liste déroulante située sous\*\* la fonction de média CSS Emulate color-gamut\*\* contient les espaces de couleur que DevTools peut émuler.</span><span class="sxs-lookup"><span data-stu-id="a39ea-191">The dropdown under **Emulate CSS media feature color-gamut** contains color spaces that DevTools may emulate.</span></span>  <span data-ttu-id="a39ea-192">Par exemple, pour déclencher une `color-gamut: p3`requête média, choisissez **color-gamut : p3** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="a39ea-192">For example, to trigger a `color-gamut: p3` media query, choose **color-gamut: p3** from the dropdown.</span></span>  

<span data-ttu-id="a39ea-193">Pour émuler la fonction de média CSS color-gamut, effectuez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="a39ea-193">To emulate the CSS color-gamut media feature, complete the following actions.</span></span>  

1.  <span data-ttu-id="a39ea-194">Ouvrez [le menu Commande.][DevtoolsCommandMenuIndex]</span><span class="sxs-lookup"><span data-stu-id="a39ea-194">Open the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
1.  <span data-ttu-id="a39ea-195">Tapez `Rendering`.</span><span class="sxs-lookup"><span data-stu-id="a39ea-195">Type `Rendering`.</span></span>  
1.  <span data-ttu-id="a39ea-196">Exécutez la **commande Afficher le rendu**.</span><span class="sxs-lookup"><span data-stu-id="a39ea-196">Run the **Show Rendering** command.</span></span>  
1.  <span data-ttu-id="a39ea-197">Naviguez jusqu'à la fonction de média CSS **Emulate color-gamut** et choisissez une option.</span><span class="sxs-lookup"><span data-stu-id="a39ea-197">Navigate to **Emulate CSS media feature color-gamut** and choose an option.</span></span>  

<span data-ttu-id="a39ea-198">Pour en savoir plus sur cette `color-gamut`fonction, consultez la rubrique Qualité de l'affichage des [couleurs : la fonction][CsswgDraftsMediaqueries4ColorGamut] «color-gamut» .</span><span class="sxs-lookup"><span data-stu-id="a39ea-198">To learn more about the `color-gamut` feature, navigate to [Color Display Quality: the 'color-gamut' feature][CsswgDraftsMediaqueries4ColorGamut].</span></span>  <span data-ttu-id="a39ea-199">Pour revoir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez le numéro [1073887 ][CR1073887].</span><span class="sxs-lookup"><span data-stu-id="a39ea-199">To review the history of this feature in the Chromium open-source project, navigate to Issue [1073887][CR1073887].</span></span>  

:::image type="complex" source="../../media/2021/02/rendering-css-color-gamut.msft.png" alt-text="Emuler la fonction CSS color-gamut media" lightbox="../../media/2021/02/rendering-css-color-gamut.msft.png":::
   <span data-ttu-id="a39ea-201">Emuler la fonction CSS color-gamut media</span><span class="sxs-lookup"><span data-stu-id="a39ea-201">Emulate the CSS color-gamut media feature</span></span>  
:::image-end:::  

### <a name="improved-progressive-web-apps-tooling"></a><span data-ttu-id="a39ea-202">Amélioration de l'outil Progressive Web Apps</span><span class="sxs-lookup"><span data-stu-id="a39ea-202">Improved Progressive Web Apps tooling</span></span>  

#### <a name="pwa-installability-warning-in-the-console"></a><span data-ttu-id="a39ea-203">Avertissement sur l'installabilité de PWA dans la Console</span><span class="sxs-lookup"><span data-stu-id="a39ea-203">PWA installability warning in the Console</span></span>  

<span data-ttu-id="a39ea-204">La **console** affiche désormais un message [d'avertissement plus détaillé sur l' installabilité des Progressive][ProgressiveWebAppsIndex] Web Apps (PWA) avec un lien vers [l'amélioration de la détection du support hors ligne des Progressive Web Apps][ChromeDeveloperBlogImprovedPwaOfflineDetection].</span><span class="sxs-lookup"><span data-stu-id="a39ea-204">The **Console** now displays a more detailed [Progressive Web Apps (PWA)][ProgressiveWebAppsIndex] installability warning message with a link to [Improving Progressive Web App offline support detection][ChromeDeveloperBlogImprovedPwaOfflineDetection].</span></span>  

:::image type="complex" source="../../media/2021/02/console-pwa-installability.msft.png" alt-text="Avertissement sur l'installabilité de PWA dans l'outil Console" lightbox="../../media/2021/02/console-pwa-installability.msft.png":::
   <span data-ttu-id="a39ea-206">Avertissement sur l'installabilité de PWA dans l'outil **Console**</span><span class="sxs-lookup"><span data-stu-id="a39ea-206">PWA installability warning in **Console** tool</span></span>  
:::image-end:::  

#### <a name="pwa-description-length-warning-in-the-manifest-pane"></a><span data-ttu-id="a39ea-207">Avertissement sur la longueur de la description du PWA dans le volet du manifeste</span><span class="sxs-lookup"><span data-stu-id="a39ea-207">PWA description length warning in the Manifest pane</span></span>

<span data-ttu-id="a39ea-208">Le **volet Manifest** affiche désormais un message d'avertissement si la description du manifeste dépasse 324 caractères.</span><span class="sxs-lookup"><span data-stu-id="a39ea-208">The **Manifest** pane now displays a warning message if the manifest description exceeds 324 characters.</span></span>  

:::image type="complex" source="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png" alt-text="Avertissement de troncature de la description PWA" lightbox="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png":::
   <span data-ttu-id="a39ea-210">Avertissement de troncature de la description PWA</span><span class="sxs-lookup"><span data-stu-id="a39ea-210">PWA description truncate warning</span></span>  
:::image-end:::  

<span data-ttu-id="a39ea-211">Pour revoir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez les numéros [965802 ][CR965802], [1146450][CR1146450] , et [1169689][CR1169689] .</span><span class="sxs-lookup"><span data-stu-id="a39ea-211">To review the history of this feature in the Chromium open-source project, navigate to Issues [965802][CR965802], [1146450][CR1146450], and [1169689][CR1169689].</span></span>  

### <a name="new-remote-address-space-column-in-the-network-tool"></a><span data-ttu-id="a39ea-212">Nouvelle colonne Espace d'adressage distant dans l'outil Réseau</span><span class="sxs-lookup"><span data-stu-id="a39ea-212">New Remote Address Space column in the Network tool</span></span>  

<!-- does not work in canary 90.0.813.0 -->  
<span data-ttu-id="a39ea-213">La nouvelle **colonne Espace** d'adressage distant affiche l'espace d'adressage IP de chaque ressource réseau.</span><span class="sxs-lookup"><span data-stu-id="a39ea-213">The new **Remote Address Space** column displays the network IP address space of each network resource.</span></span>  <span data-ttu-id="a39ea-214">Pour afficher la nouvelle colonne Espace d'adressage distant, effectuez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="a39ea-214">To display the new Remote Address Space column, complete the following actions.</span></span>  

1.  <span data-ttu-id="a39ea-215">Naviguez vers l'outil **Réseau**.</span><span class="sxs-lookup"><span data-stu-id="a39ea-215">Navigate to the **Network** tool.</span></span>  
1.  <span data-ttu-id="a39ea-216">Dans le tableau des demandes, survolez la ligne d'en-tête et ouvrez le menu contextuel (clic droit).</span><span class="sxs-lookup"><span data-stu-id="a39ea-216">In the Requests table, hover on the header row, and open the contextual menu \(right-click\).</span></span>  <span data-ttu-id="a39ea-217">Pour savoir comment ajouter ou supprimer des colonnes dans le tableau des demandes, consultez la rubrique [Ajouter ou supprimer des colonnes][DevtoolsNetworkReferenceAddRemoveColumns].</span><span class="sxs-lookup"><span data-stu-id="a39ea-217">To learn how to add or remove columns from the Requests table, navigate to [Add or remove columns][DevtoolsNetworkReferenceAddRemoveColumns].</span></span>  
1.  <span data-ttu-id="a39ea-218">Choisissez **Espace d'adressage distant** .</span><span class="sxs-lookup"><span data-stu-id="a39ea-218">Choose **Remote Address Space**.</span></span>  
    
<span data-ttu-id="a39ea-219">Le tableau des demandes affiche maintenant une nouvelle colonne dont l'en-tête est **Espace d'adressage distant**.</span><span class="sxs-lookup"><span data-stu-id="a39ea-219">The Requests table now displays a new column with the header named **Remote Address Space**.</span></span>  <span data-ttu-id="a39ea-220">Pour revoir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez le numéro [1128885][CR1128885].</span><span class="sxs-lookup"><span data-stu-id="a39ea-220">To review the history of this feature in the Chromium open-source project, navigate to Issue [1128885][CR1128885].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png" alt-text="Dans le menu contextuel, choisissez Espace d'adressage distant." lightbox="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png":::
         <span data-ttu-id="a39ea-222">Dans le menu contextuel, choisissez **l'espace d'adressage distant**</span><span class="sxs-lookup"><span data-stu-id="a39ea-222">In the contextual menu, choose the **Remote Address Space**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-remote-address-space.msft.png" alt-text="Le tableau des demandes affiche désormais la colonne Espace d'adressage distant." lightbox="../../media/2021/02/network-requests-remote-address-space.msft.png":::
         <span data-ttu-id="a39ea-224">Le tableau des demandes affiche désormais la colonne **Espace d'adressage distant**.</span><span class="sxs-lookup"><span data-stu-id="a39ea-224">The Requests table now displays the **Remote Address Space** column</span></span> :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-allowed-and-disallowed-features-in-the-frame-details-view"></a><span data-ttu-id="a39ea-225">Afficher les fonctionnalités autorisées et non autorisées dans la vue détaillée du cadre.</span><span class="sxs-lookup"><span data-stu-id="a39ea-225">Display allowed and disallowed features in the Frame details view</span></span>  

<span data-ttu-id="a39ea-226">La vue détaillée du cadre affiche désormais une liste des fonctionnalités de navigateur autorisées et interdites, contrôlées par la [stratégie de permissions][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer].</span><span class="sxs-lookup"><span data-stu-id="a39ea-226">The Frame details view now displays a list of allowed and disallowed browser features controlled by the [Permissions Policy][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer].</span></span>  <span data-ttu-id="a39ea-227">La stratégie de permissions est une API de plate-forme Web qui permet de bloquer l'utilisation des fonctionnalités du navigateur dans un cadre individuel ou dans les iframes qu'il intègre à une page Web.</span><span class="sxs-lookup"><span data-stu-id="a39ea-227">Permissions Policy is a web platform API that allows \(or blocks\) a webpage the use of browser features in an individual frame or in iframes that it embeds.</span></span>  <span data-ttu-id="a39ea-228">Pour revoir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez le numéro [1158827][CR1158827].</span><span class="sxs-lookup"><span data-stu-id="a39ea-228">To review the history of this feature in the Chromium open-source project, navigate to Issue [1158827][CR1158827].</span></span>  

:::image type="complex" source="../../media/2021/02/application-frames-permissions-policy.msft.png" alt-text="Fonctionnalités autorisées et non autorisées en fonction de la stratégie d'autorisation." lightbox="../../media/2021/02/application-frames-permissions-policy.msft.png":::
   <span data-ttu-id="a39ea-230">Fonctionnalités autorisées et non autorisées en fonction de la stratégie d'autorisation.</span><span class="sxs-lookup"><span data-stu-id="a39ea-230">Allowed and disallowed features based on the Permission Policy</span></span>  
:::image-end:::  

### <a name="new-sameparty-column-in-the-cookies-pane"></a><span data-ttu-id="a39ea-231">Nouvelle colonne SameParty dans le volet Cookies</span><span class="sxs-lookup"><span data-stu-id="a39ea-231">New SameParty column in the Cookies pane</span></span>  

<span data-ttu-id="a39ea-232">Le **volet Cookies** de l'outil **Application** affiche désormais `SameParty`l'attribut de chaque cookie.</span><span class="sxs-lookup"><span data-stu-id="a39ea-232">The **Cookies** pane in the **Application** tool now displays the `SameParty` attribute for each cookie.</span></span>  <span data-ttu-id="a39ea-233">Cet `SameParty`attribut est un nouvel attribut booléen permettant d'indiquer si un cookie est inclus dans les demandes adressées aux origines des mêmes ensembles de [première partie][GithubPrivacycgFirstPartySets].</span><span class="sxs-lookup"><span data-stu-id="a39ea-233">The `SameParty` attribute is a new boolean attribute to indicate whether a cookie is included in requests to origins of the same [First-Party Sets][GithubPrivacycgFirstPartySets].</span></span>  <span data-ttu-id="a39ea-234">Pour revoir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez le numéro [1161427][CR1161427].</span><span class="sxs-lookup"><span data-stu-id="a39ea-234">To review the history of this feature in the Chromium open-source project, navigate to Issue [1161427][CR1161427].</span></span>  

:::image type="complex" source="../../media/2021/02/application-storage-cookies-sameparty.msft.png" alt-text="Colonne SameParty dans le volet Cookies" lightbox="../../media/2021/02/application-storage-cookies-sameparty.msft.png":::
   <span data-ttu-id="a39ea-236">**Colonne SameParty** dans le volet **Cookies**</span><span class="sxs-lookup"><span data-stu-id="a39ea-236">**SameParty** column in the **Cookies** pane</span></span>  
:::image-end:::  

### <a name="fndisplayname-property-in-the-console-tool-is-now-deprecated"></a><span data-ttu-id="a39ea-237">La propriété fn.displayName de l'outil Console est désormais obsolète.</span><span class="sxs-lookup"><span data-stu-id="a39ea-237">fn.displayName property in the Console tool is now deprecated</span></span>  

<span data-ttu-id="a39ea-238">Auparavant, cette `fn.displayName`propriété vous permettait de contrôler les noms de débogage des fonctions à afficher dans `error.stack`et dans les traces de pile de DevTools.</span><span class="sxs-lookup"><span data-stu-id="a39ea-238">Previously, the `fn.displayName` property allowed you to control debug names for functions to display in `error.stack` and in DevTools stack traces.</span></span>  <span data-ttu-id="a39ea-239">À partir de la version 90 de Microsoft Edge, cette`fn.displayName` propriété est désormais dépréciée et remplacée par la`fn.name` propriété .</span><span class="sxs-lookup"><span data-stu-id="a39ea-239">Starting in Microsoft Edge version 90, the `fn.displayName` property is now deprecated, and replaced by the `fn.name` property.</span></span>  <span data-ttu-id="a39ea-240">Utilisez la`Object.defineProperty` méthode standard pour définir la`fn.name` propriété.</span><span class="sxs-lookup"><span data-stu-id="a39ea-240">Use the standard `Object.defineProperty` method to define the `fn.name` property.</span></span>  <span data-ttu-id="a39ea-241">Pour en savoir plus`fn.name`, consultez le site [Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].</span><span class="sxs-lookup"><span data-stu-id="a39ea-241">To learn more about `fn.name`, navigate to [Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].</span></span>  <span data-ttu-id="a39ea-242">Pour revoir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez le numéro [1177685][CR1177685].</span><span class="sxs-lookup"><span data-stu-id="a39ea-242">To review the history of this feature in the Chromium open-source project, navigate to Issue [1177685][CR1177685].</span></span>  

:::image type="complex" source="../../media/2021/02/console-display-name-name.msft.png" alt-text="Un exemple de la propriété fn.name pour contrôler les noms de débogage des fonctions" lightbox="../../media/2021/02/console-display-name-name.msft.png":::
   <span data-ttu-id="a39ea-244">Un exemple de la `fn.name`propriété permettant de contrôler les noms de débogage pour les fonctions</span><span class="sxs-lookup"><span data-stu-id="a39ea-244">An example of the `fn.name` property to control debug names for functions</span></span>  
:::image-end:::  

### <a name="full-accessibility-tree-view-in-the-elements-tool"></a><span data-ttu-id="a39ea-245">Arborescence d'accessibilité complète dans l'outil Éléments</span><span class="sxs-lookup"><span data-stu-id="a39ea-245">Full accessibility tree view in the Elements tool</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="a39ea-246">Cette expérience \*\*permet d'obtenir une arborescence d'accessibilité complète \*\*dans l'outil **Éléments**.</span><span class="sxs-lookup"><span data-stu-id="a39ea-246">This experiment provides a **full accessibility tree view** in the **Elements** tool.</span></span>  <span data-ttu-id="a39ea-247">Le [volet Accessibilité][DevtoolsAccessibilityReferenceAccessibilityPanel] propose une arborescence d'accessibilité partielle, qui affiche la chaîne d'ancêtres directs du nœud racine au nœud inspecté.</span><span class="sxs-lookup"><span data-stu-id="a39ea-247">The [Accessibility][DevtoolsAccessibilityReferenceAccessibilityPanel] pane provides a partial accessibility tree view, that displays the direct ancestor chain from the root node to the inspected node.</span></span>  
<span data-ttu-id="a39ea-248">Après avoir activé cette expérience et rechargé les DevTools, choisissez l'un des boutons suivants pour changer l'affichage dans l'outil Éléments pour tous les éléments de la page Web.</span><span class="sxs-lookup"><span data-stu-id="a39ea-248">After you turn on this experiment and reload the DevTools, choose one of the following buttons to switch the display in the Elements tool for all elements on the webpage.</span></span>  

*   <span data-ttu-id="a39ea-249">Pour afficher l'arborescence d'accessibilité complète, cliquez sur le bouton **Passer à l'arborescence d'accessibilité**.</span><span class="sxs-lookup"><span data-stu-id="a39ea-249">To display the full accessibility tree view , choose the **Switch to Accessibility Tree view**.</span></span>  
*   <span data-ttu-id="a39ea-250">Pour afficher l'arborescence DOM, choisissez l'option **Passer à l'arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="a39ea-250">To display the DOM tree view, choose the **Switch to DOM Tree view**.</span></span>  
    
<span data-ttu-id="a39ea-251">Pour activer l'expérience, accédez à la [section Activer les fonctions][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] expérimentales et cochez la case située à côté de **Activer l'arborescence d'accessibilité complète dans le volet Éléments**.</span><span class="sxs-lookup"><span data-stu-id="a39ea-251">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkbox next to **Enable full accessibility tree view in Elements pane**.</span></span>  <span data-ttu-id="a39ea-252">Pour revoir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez le numéro [887173][CR887173].</span><span class="sxs-lookup"><span data-stu-id="a39ea-252">To review the history of this feature in the Chromium open-source project, navigate to Issue [887173][CR887173].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png" alt-text="Afficher l'arborescence DOM" lightbox="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png":::
         <span data-ttu-id="a39ea-254">Afficher la **vue DOM** </span><span class="sxs-lookup"><span data-stu-id="a39ea-254">Display the **DOM view**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png" alt-text="Afficher l'arborescence complète de l'accessibilité" lightbox="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png":::
         <span data-ttu-id="a39ea-256">Afficher **l'arborescence complète de l'accessibilité**</span><span class="sxs-lookup"><span data-stu-id="a39ea-256">Display the **Full Accessibility Tree view**</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="a39ea-257">Téléchargez les canaux de l'aperçu de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a39ea-257">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="a39ea-258">Si vous êtes sous Windows, Linux ou macOS, envisagez d'utiliser les [canaux d'aperçu de Microsoft][MicrosoftEdgePreviewChannels] Edge comme navigateur de développement par défaut.</span><span class="sxs-lookup"><span data-stu-id="a39ea-258">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="a39ea-259">Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="a39ea-259">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="a39ea-260">Entrer en contact avec l'équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a39ea-260">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsAccessibilityReferenceAccessibilityPanel]: ../../../accessibility/reference.md#the-accessibility-panel "Le volet d'accessibilité – Référence en matière d'accessibilité | Microsoft Docs"  
[DevtoolsCommandMenuIndex]: ../../../command-menu/index.md "Exécuter des commandes avec le menu de commande DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterByLogLevel]: ../../../console/reference.md#filter-by-log-level "Filtrer par niveau de journal – Référence de la console | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterMessages]: ../../../console/reference.md#filter-messages "Filtrer les messages – Référence Console | Microsoft Docs"  
[DevtoolsConsoleReferenceOpenConsoleSidebar]: ../../../console/reference.md#open-the-console-sidebar "Ouvrir la barre latérale de la console – Référence de la console | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Paramètres – Personnalisation de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personnaliser les raccourcis clavier dans les DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexEnablePlusButtonTabMenusToOpenMoreTools]: ../../../experimental-features/index.md#enable--button-tab-menus-to-open-more-tools "Activer les menus d'onglet du bouton + pour ouvrir plus d'outils – Fonctionnalités expérimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../../../experimental-features/index.md#turn-on-experimental-features "Activer les fonctions expérimentales – Fonctions expérimentales | Microsoft Docs"  
[DevtoolsNetworkReferenceAddRemoveColumns]: ../../../network/reference.md#add-or-remove-columns "Ajouter ou supprimer des colonnes – Référence en matière d'analyse de réseau | Microsoft Docs"  
[DevtoolsNetworkReferenceDisplayInitiatorsDependencies]: ../../../network/reference.md#display-initiators-and-dependencies "Afficher les initiateurs et les dépendances – Référence en matière d'analyse de réseau | Microsoft Docs"  

[ProgressiveWebAppsIndex]: ../../../../progressive-web-apps-chromium/index.md "Aperçu des Progressive Web Apps sur Windows | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux de l'aperçu de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Mise à jour manuelle d'une extension – Extension Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Outils Microsoft Edge pour Visual Studio Code | Visual Studio Marketplace"  

[ChromeDeveloperBlogImprovedPwaOfflineDetection]: https://developer.chrome.com/blog/improved-pwa-offline-detection "Amélioration de la détection du support hors ligne des Progressive Web App | Développeurs Chrome"  

[ChromestatusFeature5354410980933632]: https://www.chromestatus.com/feature/5354410980933632 "color-gamut media query | État de la plate-forme Chrome"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues de chrome"  
[CR174309]: https://crbug.com/174309 "Problème 174309 : DevTools : Permettre de personnaliser les raccourcis clavier/liaisons de touches | Bogues de Chromium"  
[CR887173]: https://crbug.com/887173 "Problème 887173 : DevTools : Inspection complète de l'arbre d'accessibilité | Bogues Chromium"  
[CR965802]: https://crbug.com/965802 "Problème 965802 : Implémentation d'une détection plus précise de la capacité hors ligne du travailleur de service | Bogues Chromium"  
[CR1073887]: https://crbug.com/1073887 "Problème 1073887 : DevTools : émulation de l'espace colorimétrique @media (color-gamut : ...) | bogues de Chromium"  
[CR1128885]: https://crbug.com/1128885 "Problème 1128885 : Prise en charge par DevTools de CORS-RFC1918 | Bogues de Chromium"  
[CR1146450]: https://crbug.com/1146450 "Problème 1146450 : [Android] Implémentation de l'installation de la feuille de fond | Bogues Chromium"  
[CR1158276]: https://crbug.com/1158276 "Problème 1158276 : impossible de développer/contratr le volet « Chaîne du initiateur de la demande » à l’aide des touches de direction dans la section « Réseau » des outils de développement | Bogues Chromium"  
[CR1158827]: https://crbug.com/1158827 "Problème 1158827 : [Stratégie d’autorisations] Implémenter la prise en charge des outils de développement pour les stratégies d'| Bogues Chromium"  
[CR1160637]: https://crbug.com/1160637 "Problème 1160637 : le focus sur la chaîne du initiateur de demande est considéré incomplet dans la section « Réseau » de la fenêtre « Outils de développement » | Bogues Chromium"  
[CR1161427]: https://crbug.com/1161427 "Problème 1161427 : &#9730 ; Prise en charge du débogage de l'attribut de cookie SameParty dans DevTools | Bogues Chromium"  
[CR1166710]: https://crbug.com/1166710 "Problème 1166710 : activer l'expérience de l'outil Flexbox par défaut | Bogues Chromium"  
[CR1169689]: https://crbug.com/1169689 "Problème 1169689 : La feuille de fond de l'installation de la PWA ne devrait pas comporter de catégories | Bogues de Chrome"  
[CR1175699]: https://crbug.com/1175699 "Numéro 1175699 : Éditeur Flexbox | Bogues Chromium"  
[CR1177685]: https://crbug.com/1177685 "Problème 1177685 : Suppression de la prise en charge non standard de fn.displayName | bogues Chromium"  
[CR1178530]: https://crbug.com/1178530 "Problème 1178530 : La console n'échappe pas les guillemets doubles lors de l'impression de chaînes de caractères | Bogues Chromium"  

[CsswgDraftsMediaqueries4ColorGamut]: https://drafts.csswg.org/mediaqueries-4#color-gamut "Qualité de l'affichage des couleurs : la fonction « color-gamut» | Projets de rédaction du groupe de travail CSS"  

[GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/DevTools/FocusMode/explainer.md "DevTools : Interface utilisateur du mode Focus – MicrosoftEdge/MSEdgeExplainers | GitHub"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubPrivacycgFirstPartySets]: https://github.com/privacycg/first-party-sets "Jeux de première partie | GitHub"  

[GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Explication de la stratégie d'autorisation | GitHub"  

[MdnJavascriptReferenceGlobalObjectsFunctionName]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/name "Nom de la fonction | MDN"  

> [!NOTE]
> <span data-ttu-id="a39ea-300">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a39ea-300">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a39ea-301">La page d’origine est disponible [ici](https://developer.chrome.com/blog/new-in-devtools-90) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)</span><span class="sxs-lookup"><span data-stu-id="a39ea-301">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-90) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="a39ea-303">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a39ea-303">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
