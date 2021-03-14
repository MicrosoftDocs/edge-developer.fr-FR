---
description: Prise en charge du débogage de CSS Flexbox, affichage à tête haute des performances sur la page web, mises à jour de l’outil problèmes, et bien plus encore
title: Nouveautés de DevTools (Microsoft Edge 90)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 4222bcf7284b69269691ec9fb78094e5efb95793
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408483"
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
# <a name="whats-new-in-devtools-microsoft-edge-90"></a><span data-ttu-id="8c2cf-104">Nouveautés de DevTools (Microsoft Edge 90)</span><span class="sxs-lookup"><span data-stu-id="8c2cf-104">What's New In DevTools (Microsoft Edge 90)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="group-tools-together-in-focus-mode"></a><span data-ttu-id="8c2cf-105">Regroupement d’outils en mode Focus</span><span class="sxs-lookup"><span data-stu-id="8c2cf-105">Group tools together in Focus Mode</span></span>  

<!-- Title: Grouping the tools in Focus Mode  -->  
<!-- Subtitle: Organize your favorite tools into groups with the new Focus Mode UI.  -->  

<span data-ttu-id="8c2cf-106">Le mode Focus est une interface expérimentale qui vous permet de grouper différents outils en fonction de vos propres scénarios de débogage.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-106">Focus Mode is an experimental interface that allows you to group different tools together based on your own debugging scenarios.</span></span>  <span data-ttu-id="8c2cf-107">La nouvelle **barre d’activité** affichée à gauche inclut des groupes d’outils prédéfinie tels que **la** disposition et **le débogage.**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-107">The new **Activity Bar** displayed on the left includes predefined tool groups such as **Layout** and **Debugging**.</span></span>  <span data-ttu-id="8c2cf-108">Pour personnaliser chaque groupe d’outils, fermez les outils avec l’icône **Fermer** \( \) ou ajoutez de nouveaux outils avec l’icône Plus d’outils `X` \*\*\*\* `+` \( \).</span><span class="sxs-lookup"><span data-stu-id="8c2cf-108">To customize each tool group, close tools with the **Close** \(`X`\) icon or add new tools with the **More tools** \(`+`\) icon.</span></span>  

<span data-ttu-id="8c2cf-109">Pour activer l’expérience, [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] accédez à Activer les fonctionnalités expérimentales et activez les case à cocher en regard du mode Focus et des **bulles d’outils DevTools** et activez **les menus**onglets de bouton + pour ouvrir d’autres outils.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-109">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkboxes next to **Focus Mode and DevTools Tooltips** and **Enable + button tab menus to open more tools**.</span></span>  <span data-ttu-id="8c2cf-110">Pour plus d’informations sur cette fonctionnalité ou pour commenter avec des questions et des idées, accédez à [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span><span class="sxs-lookup"><span data-stu-id="8c2cf-110">For more information about this feature or to comment with questions and ideas, navigate to [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span></span>  

:::image type="complex" source="../../media/2021/02/focus-mode.msft.png" alt-text="Afficher la barre d’activité" lightbox="../../media/2021/02/focus-mode.msft.png":::
   <span data-ttu-id="8c2cf-112">Afficher la barre **d’activité**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-112">Display the **Activity Bar**</span></span>  
:::image-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a><span data-ttu-id="8c2cf-113">En savoir plus sur DevTools avec des conseils d’information</span><span class="sxs-lookup"><span data-stu-id="8c2cf-113">Learn about DevTools with informative tooltips</span></span>  

<!-- Title: DevTools Tooltips  -->  
<!-- Subtitle: Learn more about how to use DevTools with informative DevTools tooltips.  -->  

<span data-ttu-id="8c2cf-114">La fonctionnalité d’outils DevTools vous permet d’en savoir plus sur les différents outils et volets.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-114">The DevTools Tooltips feature helps you learn about all the different tools and panes.</span></span>  <span data-ttu-id="8c2cf-115">Choisissez l’icône Aide \( \) en bas de la barre d’activité pour faire bascule les bulles dans `?` DevTools. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8c2cf-115">Choose the Help \(`?`\) icon at the bottom of the **Activity Bar** to toggle tooltips in the DevTools.</span></span>  <span data-ttu-id="8c2cf-116">Lorsque des bulles sont en cours, pointez sur chaque région de DevTools en plan pour en savoir plus sur l’utilisation de l’outil.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-116">When tooltips are on, hover over each outlined region of DevTools to learn more about how to use the tool.</span></span>  <span data-ttu-id="8c2cf-117">Pour activer l’expérience, [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] accédez à Activer les fonctionnalités expérimentales et activez les case à cocher en regard du mode Focus et des **bulles d’outils DevTools** et activez **les menus**d’onglets de bouton + pour ouvrir d’autres outils.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-117">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkboxes next to **Focus Mode and DevTools Tooltips** and **Enable + button tab menus to open more tools**.</span></span>  <span data-ttu-id="8c2cf-118">Pour plus d’informations sur cette fonctionnalité ou pour commenter avec des questions et des idées, accédez à [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span><span class="sxs-lookup"><span data-stu-id="8c2cf-118">For more information about this feature or to comment with questions and ideas, navigate to [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span></span>  

:::image type="complex" source="../../media/2021/02/focus-mode-and-tooltips-help.msft.png" alt-text="Sélectionnez l’icône Aide (?) dans la barre d’activité pour afficher des bulles" lightbox="../../media/2021/02/focus-mode-and-tooltips-help.msft.png":::
   <span data-ttu-id="8c2cf-120">Sélectionnez l’icône Aide \( \) dans la barre `?` **d’activité** pour afficher des bulles</span><span class="sxs-lookup"><span data-stu-id="8c2cf-120">Choose the Help \(`?`\) icon in the **Activity Bar** to display tooltips</span></span>  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a><span data-ttu-id="8c2cf-121">Personnaliser les raccourcis clavier dans paramètres</span><span class="sxs-lookup"><span data-stu-id="8c2cf-121">Customize keyboard shortcuts in Settings</span></span>  

<!-- Title: Change keyboard shortcuts in Settings  -->  
<!-- TODO:  Rachel's feedback is about the fact that this experimental feature is turned on by default, may have separate section in What's New for experimental features)  -->  
<!-- Subtitle: Make DevTools work better for you by creating new keyboard shortcuts for any action in the DevTools.  -->  

<span data-ttu-id="8c2cf-122">Vous pouvez maintenant personnaliser le raccourci clavier pour toute action dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-122">You may now customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="8c2cf-123">Pour modifier un raccourci clavier, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-123">To edit a keyboard shortcut, complete the following actions.</span></span>  

1.  <span data-ttu-id="8c2cf-124">Ouvrez DevTools, puis \*\*\*\* choisissez  >  **Raccourcis des paramètres.**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-124">Open the DevTools, and then choose **Settings** > **Shortcuts**.</span></span>  
1.  <span data-ttu-id="8c2cf-125">Choisissez l’action que vous souhaitez personnaliser.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-125">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="8c2cf-126">Choose the Edit \(</span><span class="sxs-lookup"><span data-stu-id="8c2cf-126">Choose the Edit \(</span></span>![Icône Modifier le raccourci clavier](../../media/2021/02/edit-keyboard-shortcut-icon.msft.png)<span data-ttu-id="8c2cf-128">\) icône.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-128">\) icon.</span></span>  
1.  <span data-ttu-id="8c2cf-129">Sélectionnez les clés que vous souhaitez lier à l’action.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-129">Select the keys you want to bind to the action.</span></span>  
1.  <span data-ttu-id="8c2cf-130">Sélectionnez la coche \(</span><span class="sxs-lookup"><span data-stu-id="8c2cf-130">Choose the checkmark \(</span></span>![Cochez l’icône Raccourci clavier](../../media/2021/02/checkmark-keyboard-shortcut-icon.msft.png)<span data-ttu-id="8c2cf-132">\) icône.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-132">\) icon.</span></span>  
    
<span data-ttu-id="8c2cf-133">Pour plus d’informations sur la personnalisation et la modification des raccourcis, accédez à Personnaliser les raccourcis clavier dans [Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="8c2cf-133">For more information about customizing and editing shortcuts, navigate to [Customize keyboard shortcuts in the Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="8c2cf-134">Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez au problème [174309.][CR174309]</span><span class="sxs-lookup"><span data-stu-id="8c2cf-134">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png" alt-text="Personnaliser les raccourcis clavier dans les paramètres DevTools sur les raccourcis à l’aide d’un raccourci en mode édition" lightbox="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png":::
   <span data-ttu-id="8c2cf-136">Personnaliser les raccourcis clavier dans les [paramètres DevTools][DevtoolsCustomizeIndexSettings] sur les raccourcis à l’aide d’un raccourci en mode édition</span><span class="sxs-lookup"><span data-stu-id="8c2cf-136">Customize keyboard shortcuts in the [DevTools Settings][DevtoolsCustomizeIndexSettings] on Shortcuts with a shortcut in edit mode</span></span>  
:::image-end:::  

## <a name="microsoft-edge-devtools-for-visual-studio-code-extension-update-114"></a><span data-ttu-id="8c2cf-137">Microsoft Edge DevTools for Visual Studio Code extension update 1.1.4</span><span class="sxs-lookup"><span data-stu-id="8c2cf-137">Microsoft Edge DevTools for Visual Studio Code extension update 1.1.4</span></span>  

<!-- Title: Edge Devtools for Visual Studio code extension update 1.1.4  -->  
<!-- Subtitle: Latest changes including a favicon is displayed next to each of the instances and console messages from the browser are displayed in the console of Visual Studio Code.  -->  

<span data-ttu-id="8c2cf-138">Les outils de développement Microsoft Edge pour [l’extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] de code Visual Studio version 1.1.4 pour Microsoft Visual Studio Code affichent désormais un côté favorite à côté de chacune des instances DevTools.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-138">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.4 for Microsoft Visual Studio Code now displays a favicon next to each of the DevTools instances.</span></span>  <span data-ttu-id="8c2cf-139">Les messages de console de Microsoft Edge s’affichent désormais dans la **console DevTools** sous **Sortie** de Microsoft Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-139">Console messages from Microsoft Edge now display in the **DevTools Console** under **Output** of Microsoft Visual Studio Code.</span></span>  <span data-ttu-id="8c2cf-140">Microsoft Visual Studio code met automatiquement à jour les extensions.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-140">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="8c2cf-141">Pour mettre à jour manuellement la version 1.1.4, accédez à Mettre à jour [une extension manuellement.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="8c2cf-141">To manually update to version 1.1.4, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  <span data-ttu-id="8c2cf-142">Vous pouvez déposer des problèmes et contribuer à l’extension sur le référentiel GitHub [vscode-edge-devtools.][GithubMicrosoftVscodeEdgeDevtools]</span><span class="sxs-lookup"><span data-stu-id="8c2cf-142">You may file issues and contribute to the extension on the [vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools] GitHub repo.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="8c2cf-143">La figure suivante affiche les messages d’un exemple de page web enregistrée dans l’outil **Console** dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-143">The following figure displays messages from an example webpage logged in the **Console** tool in Microsoft Edge.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8c2cf-144">La figure suivante affiche les mêmes messages de l’exemple de page \*\*\*\* web enregistrée dans la **console DevTools** sous Sortie de Microsoft Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-144">The following figure displays the same messages from the example webpage logged in the **DevTools Console** under **Output** of Microsoft Visual Studio Code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png" alt-text="Afficher un message dans la console dans Microsoft Edge DevTools" lightbox="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png":::
         <span data-ttu-id="8c2cf-146">Afficher un message dans la console dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8c2cf-146">Display a message in Console in Microsoft Edge DevTools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png" alt-text="Afficher le même message dans la console DevTools sous Sortie de Microsoft Visual Studio Code" lightbox="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png":::
         <span data-ttu-id="8c2cf-148">Afficher le même message dans la console DevTools sous Sortie de Microsoft Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="8c2cf-148">Display the same message in the DevTools Console under Output of Microsoft Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-flexbox-editing-with-visual-flexbox-editor-and-multiple-overlays"></a><span data-ttu-id="8c2cf-149">Modification améliorée de la flexbox CSS avec l’éditeur visual flexbox et plusieurs superpositions</span><span class="sxs-lookup"><span data-stu-id="8c2cf-149">Improved CSS flexbox editing with visual flexbox editor and multiple overlays</span></span>  

<!-- Title: Try different CSS flexbox layouts with the visual flexbox editor  -->  
<!-- Subtitle: In the Styles pane, choose the icon that appears next to display: flex to try different layout properties for flex containers.  -->  

<span data-ttu-id="8c2cf-150">DevTools dispose désormais d’outils de débogage flexbox CSS dédiés.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-150">DevTools now has dedicated CSS flexbox debugging tools.</span></span>  <span data-ttu-id="8c2cf-151">Si le style ou CSS est appliqué à un élément HTML, une icône s’affiche à côté de cet élément `display: flex` `display: inline-flex` dans `flex` **l’outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-151">If the `display: flex` or `display: inline-flex` CSS style is applied to an HTML element, a `flex` icon displays next to that element in the **Elements** tool.</span></span>  <span data-ttu-id="8c2cf-152">Pour afficher \(ou masquer\) une superposition flexible sur la page web, choisissez `flex` l’icône.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-152">To display \(or hide\) a flex overlay on the webpage, choose the `flex` icon.</span></span>  <span data-ttu-id="8c2cf-153">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [1166710][CR1166710] et [1175699][CR1175699].</span><span class="sxs-lookup"><span data-stu-id="8c2cf-153">To review the history of this feature in the Chromium open-source project, navigate to Issues [1166710][CR1166710] and [1175699][CR1175699].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="8c2cf-154">Pour ouvrir **l’éditeur Flexbox,** accédez au volet **Styles** et choisissez la nouvelle icône à côté du `display: flex` style ou du `display: inline-flex` style.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-154">To open the **Flexbox** editor, navigate to the **Styles** pane and choose the new icon next to the `display: flex` or `display: inline-flex` style.</span></span>  <span data-ttu-id="8c2cf-155">**L’éditeur Flexbox** permet de modifier rapidement les propriétés de flexbox.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-155">The **Flexbox** editor provides a quick way to edit the flexbox properties.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8c2cf-156">En outre, la section \*\*\*\* **Flexbox** du volet Disposition affiche tous les éléments flexbox sur la page web.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-156">In addition, the **Flexbox** section in the **Layout** pane displays all of the flexbox elements on the webpage.</span></span>  <span data-ttu-id="8c2cf-157">Vous pouvez faire bascule la superposition de chaque élément.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-157">You may toggle the overlay of each element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-styles-display-flex-window.msft.png" alt-text="Outils de débogage CSS flexbox" lightbox="../../media/2021/02/elements-styles-display-flex-window.msft.png":::
         <span data-ttu-id="8c2cf-159">Outils de débogage CSS flexbox</span><span class="sxs-lookup"><span data-stu-id="8c2cf-159">CSS flexbox debugging tools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png" alt-text="Section Flexbox dans le volet De disposition" lightbox="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png":::
         <span data-ttu-id="8c2cf-161">**Section Flexbox** dans le **volet** De disposition</span><span class="sxs-lookup"><span data-stu-id="8c2cf-161">**Flexbox** section in the **Layout** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="keyboard-navigation-improvements-for-network-requests"></a><span data-ttu-id="8c2cf-162">Améliorations de la navigation au clavier pour les demandes réseau</span><span class="sxs-lookup"><span data-stu-id="8c2cf-162">Keyboard navigation improvements for network requests</span></span>  

<!-- Title: Navigate the request initiator chain in the Network tool with the keyboard  -->  
<!-- Subtitle: The Initiator pane may now be expanded or collapsed with the arrow keys.  -->  

<span data-ttu-id="8c2cf-163">Auparavant, vous n’étiez pas en mesure de développer ou \*\*\*\* de réduire la chaîne de demandes à l’aide des touches de direction du clavier dans le volet Initiateur, contrairement au DOM de l’outil **Elements.**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-163">Previously, you were not able to expand or collapse the chain of requests using the arrow keys on the keyboard in the **Initiator** pane, unlike the DOM in the **Elements** tool.</span></span>  <span data-ttu-id="8c2cf-164">Lorsqu’une demande réseau est \*\*\*\* sélectionnée dans l’outil Réseau, le volet **Initiateur** affiche la chaîne de demandes qui a initié la demande actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-164">When a network request is selected in the **Network** tool, the **Initiator** pane displays the chain of requests that initiated the currently selected request.</span></span>  

<span data-ttu-id="8c2cf-165">Dans Microsoft Edge version 90, vous pouvez développer ou réduire la chaîne de demandes à l’aide des touches de direction du clavier dans le **volet Initiateur.**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-165">In Microsoft Edge version 90, you may expand or collapse the chain of requests using the arrow keys on the keyboard in the **Initiator** pane.</span></span>  <span data-ttu-id="8c2cf-166">La demande réseau mise en évidence dans la chaîne est désormais également mise en évidence.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-166">The focused network request in the chain is also now highlighted.</span></span>  <span data-ttu-id="8c2cf-167">Pour en savoir plus sur les initiateurs dans l’outil **Réseau,** accédez à [Afficher les initiateurs et les dépendances.][DevtoolsNetworkReferenceDisplayInitiatorsDependencies]</span><span class="sxs-lookup"><span data-stu-id="8c2cf-167">To learn more about initiators in the **Network** tool, navigate to [Display initiators and dependencies][DevtoolsNetworkReferenceDisplayInitiatorsDependencies].</span></span>  <span data-ttu-id="8c2cf-168">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [1158276][CR1158276] et [1160637][CR1160637].</span><span class="sxs-lookup"><span data-stu-id="8c2cf-168">To review the history of this feature in the Chromium open-source project, navigate to Issues [1158276][CR1158276] and [1160637][CR1160637].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain.msft.png" alt-text="Choose a Network request and choose the Initiator pane" lightbox="../../media/2021/02/network-request-initiator-chain.msft.png":::
         <span data-ttu-id="8c2cf-170">Choose a Network request and choose the **Initiator** pane</span><span class="sxs-lookup"><span data-stu-id="8c2cf-170">Choose a Network request and choose the **Initiator** pane</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png" alt-text="Développer ou réduire la chaîne de l’initiateur de la demande et suivre la ligne mise en surbrill" lightbox="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png":::
         <span data-ttu-id="8c2cf-172">Développer ou réduire la chaîne de l’initiateur de la demande et suivre la ligne mise en surbrill</span><span class="sxs-lookup"><span data-stu-id="8c2cf-172">Expand or collapse the request initiator chain and follow the highlighted row</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="filtering-in-the-console-is-more-consistent"></a><span data-ttu-id="8c2cf-173">Le filtrage dans la console est plus cohérent</span><span class="sxs-lookup"><span data-stu-id="8c2cf-173">Filtering in the Console is more consistent</span></span>  

<!-- Title: Console improvements make filtering more consistent  -->  
<!-- Subtitle: The Log Levels dropdown is more clearly disabled when using filters in the Console sidebar.  -->  

<span data-ttu-id="8c2cf-174">Pendant que vous filtrez avec la [barre latérale de la console,][DevtoolsConsoleReferenceOpenConsoleSidebar]les filtres de la dropdown Log [Levels][DevtoolsConsoleReferenceFilterByLogLevel] ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-174">While you filter with the [Console Sidebar][DevtoolsConsoleReferenceOpenConsoleSidebar], the filters in the [Log Levels][DevtoolsConsoleReferenceFilterByLogLevel] dropdown are not available.</span></span>  <span data-ttu-id="8c2cf-175">Auparavant, la dropdown **Log Levels** (Niveaux des journaux) était mise en surbrilllette lorsque vous pointiez dessus, même lorsqu’un filtre de la barre latérale de **la console** a été choisi.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-175">Previously, the **Log Levels** dropdown highlighted when you hovered on it, even while a filter from the **Console Sidebar** was chosen.</span></span>  <span data-ttu-id="8c2cf-176">Dans Microsoft Edge version 90, la dropdown **Log Levels** n’est plus sélectionnée lorsque vous pointez dessus pendant qu’un filtre de la **barre latérale de la console** est choisi.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-176">In Microsoft Edge version 90, the **Log Levels** dropdown no longer highlights when you hover on it while a filter from the **Console Sidebar** is chosen.</span></span>  <span data-ttu-id="8c2cf-177">Pour en savoir plus sur le filtrage dans la **console,** accédez [à Filtrer les messages.][DevtoolsConsoleReferenceFilterMessages]</span><span class="sxs-lookup"><span data-stu-id="8c2cf-177">To learn more about filtering in the **Console**, navigate to [Filter Messages][DevtoolsConsoleReferenceFilterMessages].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-old.msft.png" alt-text="Auparavant, si vous ouvrez la barre latérale de la console et que vous pointez sur les niveaux par défaut, elle a été mise en surbrill" lightbox="../../media/2021/02/console-sidebar-default-levels-old.msft.png":::
         <span data-ttu-id="8c2cf-179">Auparavant, si vous ouvrez la **barre latérale de la console** et que vous pointez sur les **niveaux par défaut,** elle a été mise en surbrill</span><span class="sxs-lookup"><span data-stu-id="8c2cf-179">Previously, if you open the **Console sidebar** and hover on **Default levels** it was highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-new.msft.png" alt-text="À partir de Microsoft Edge 90, si vous choisissez la barre latérale console et que vous pointez sur les niveaux par défaut, elle ne se met pas en surbrill" lightbox="../../media/2021/02/console-sidebar-default-levels-new.msft.png":::
         <span data-ttu-id="8c2cf-181">À partir de Microsoft Edge 90, si vous choisissez la **barre** latérale console et que vous pointez sur les niveaux par **défaut,** elle ne met pas en surbrill</span><span class="sxs-lookup"><span data-stu-id="8c2cf-181">Starting in Microsoft Edge 90, if you choose the **Console sidebar** and hover on **Default levels**, it does not highlight</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="8c2cf-182">Annonces du projet de Chromium</span><span class="sxs-lookup"><span data-stu-id="8c2cf-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="the-console-now-escapes-double-quote-characters"></a><span data-ttu-id="8c2cf-183">La console échappe désormais les guillemets doubles</span><span class="sxs-lookup"><span data-stu-id="8c2cf-183">The Console now escapes double quote characters</span></span>  

<span data-ttu-id="8c2cf-184">Auparavant, la **console n’a** pas produit de guillemets doubles valides \( `"` \) caractères dans les chaînes JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-184">Previously, the **Console** did not output valid double quote \(`"`\) characters in JavaScript strings.</span></span>  <span data-ttu-id="8c2cf-185">À partir de La version 90 de Microsoft Edge, la **console** produit des chaînes JavaScript à l’aide de guillemets doubles d’échadé \( `"` \).</span><span class="sxs-lookup"><span data-stu-id="8c2cf-185">Starting in Microsoft Edge version 90, the **Console** outputs JavaScript strings using escaped double quote \(`"`\) characters.</span></span>  <span data-ttu-id="8c2cf-186">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1178530][CR1178530].</span><span class="sxs-lookup"><span data-stu-id="8c2cf-186">To review the history of this feature in the Chromium open-source project, navigate to Issue [1178530][CR1178530].</span></span>  

:::image type="complex" source="../../media/2021/02/console-string-formatted-double-quotes.msft.png" alt-text="La console produit des chaînes JavaScript à l’aide de guillemets doubles (&#0022;)" lightbox="../../media/2021/02/console-string-formatted-double-quotes.msft.png":::
   <span data-ttu-id="8c2cf-188">La **console produit des** chaînes JavaScript à l’aide de guillemets doubles d’échadé \( `"` \) caractères</span><span class="sxs-lookup"><span data-stu-id="8c2cf-188">The **Console** outputs JavaScript strings using escaped double quote \(`"`\) characters</span></span>  
:::image-end:::  

### <a name="emulate-the-css-color-gamut-media-feature"></a><span data-ttu-id="8c2cf-189">Émuler la fonctionnalité multimédia de palette de couleurs CSS</span><span class="sxs-lookup"><span data-stu-id="8c2cf-189">Emulate the CSS color-gamut media feature</span></span>  

<span data-ttu-id="8c2cf-190">La [requête multimédia de gamme][ChromestatusFeature5354410980933632] de couleurs émule la plage approximative de couleurs prise en charge par le navigateur et l’appareil que vous testez.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-190">The [color-gamut][ChromestatusFeature5354410980933632] media query emulates the approximate range of colors supported by the browser and the device you are testing.</span></span>  <span data-ttu-id="8c2cf-191">La dropdown sous Émuler la gamme de couleurs des fonctionnalités multimédias **CSS** contient des espaces de couleur que DevTools peut émuler.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-191">The dropdown under **Emulate CSS media feature color-gamut** contains color spaces that DevTools may emulate.</span></span>  <span data-ttu-id="8c2cf-192">Par exemple, pour déclencher une requête `color-gamut: p3` multimédia, choisissez **color-gamut: p3** dans ladown.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-192">For example, to trigger a `color-gamut: p3` media query, choose **color-gamut: p3** from the dropdown.</span></span>  

<span data-ttu-id="8c2cf-193">Pour émuler la fonctionnalité multimédia de palette de couleurs CSS, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-193">To emulate the CSS color-gamut media feature, complete the following actions.</span></span>  

1.  <span data-ttu-id="8c2cf-194">Ouvrez [le menu Commande.][DevtoolsCommandMenuIndex]</span><span class="sxs-lookup"><span data-stu-id="8c2cf-194">Open the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
1.  <span data-ttu-id="8c2cf-195">Entrez `Rendering`.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-195">Type `Rendering`.</span></span>  
1.  <span data-ttu-id="8c2cf-196">Exécutez la **commande Afficher le rendu.**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-196">Run the **Show Rendering** command.</span></span>  
1.  <span data-ttu-id="8c2cf-197">Accédez à Émuler la gamme de couleurs des fonctionnalités multimédias **CSS** et choisissez une option.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-197">Navigate to **Emulate CSS media feature color-gamut** and choose an option.</span></span>  

<span data-ttu-id="8c2cf-198">Pour en savoir plus sur la fonctionnalité, accédez à Qualité de l’affichage des couleurs : la fonctionnalité `color-gamut` [« color-gamut][CsswgDraftsMediaqueries4ColorGamut]».</span><span class="sxs-lookup"><span data-stu-id="8c2cf-198">To learn more about the `color-gamut` feature, navigate to [Color Display Quality: the 'color-gamut' feature][CsswgDraftsMediaqueries4ColorGamut].</span></span>  <span data-ttu-id="8c2cf-199">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1073887][CR1073887].</span><span class="sxs-lookup"><span data-stu-id="8c2cf-199">To review the history of this feature in the Chromium open-source project, navigate to Issue [1073887][CR1073887].</span></span>  

:::image type="complex" source="../../media/2021/02/rendering-css-color-gamut.msft.png" alt-text="Émuler la fonctionnalité multimédia de palette de couleurs CSS" lightbox="../../media/2021/02/rendering-css-color-gamut.msft.png":::
   <span data-ttu-id="8c2cf-201">Émuler la fonctionnalité multimédia de palette de couleurs CSS</span><span class="sxs-lookup"><span data-stu-id="8c2cf-201">Emulate the CSS color-gamut media feature</span></span>  
:::image-end:::  

### <a name="improved-progressive-web-apps-tooling"></a><span data-ttu-id="8c2cf-202">Outils d’applications web progressives améliorés</span><span class="sxs-lookup"><span data-stu-id="8c2cf-202">Improved Progressive Web Apps tooling</span></span>  

#### <a name="pwa-installability-warning-in-the-console"></a><span data-ttu-id="8c2cf-203">Avertissement d’installabilité PWA dans la console</span><span class="sxs-lookup"><span data-stu-id="8c2cf-203">PWA installability warning in the Console</span></span>  

<span data-ttu-id="8c2cf-204">La **console affiche** désormais un message d’avertissement d’installation [PWA (Progressive Web Apps)][ProgressiveWebAppsIndex] plus détaillé avec un lien vers l’amélioration de la détection de prise en charge en mode hors connexion de [l’application web progressive.][ChromeDeveloperBlogImprovedPwaOfflineDetection]</span><span class="sxs-lookup"><span data-stu-id="8c2cf-204">The **Console** now displays a more detailed [Progressive Web Apps (PWA)][ProgressiveWebAppsIndex] installability warning message with a link to [Improving Progressive Web App offline support detection][ChromeDeveloperBlogImprovedPwaOfflineDetection].</span></span>  

:::image type="complex" source="../../media/2021/02/console-pwa-installability.msft.png" alt-text="Avertissement d’installabilité PWA dans l’outil Console" lightbox="../../media/2021/02/console-pwa-installability.msft.png":::
   <span data-ttu-id="8c2cf-206">Avertissement d’installabilité PWA dans **l’outil Console**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-206">PWA installability warning in **Console** tool</span></span>  
:::image-end:::  

#### <a name="pwa-description-length-warning-in-the-manifest-pane"></a><span data-ttu-id="8c2cf-207">Avertissement de longueur de description PWA dans le volet manifeste</span><span class="sxs-lookup"><span data-stu-id="8c2cf-207">PWA description length warning in the Manifest pane</span></span>

<span data-ttu-id="8c2cf-208">Le **volet** Manifeste affiche maintenant un message d’avertissement si la description du manifeste dépasse 324 caractères.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-208">The **Manifest** pane now displays a warning message if the manifest description exceeds 324 characters.</span></span>  

:::image type="complex" source="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png" alt-text="Avertissement de tronqué de description PWA" lightbox="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png":::
   <span data-ttu-id="8c2cf-210">Avertissement de tronqué de description PWA</span><span class="sxs-lookup"><span data-stu-id="8c2cf-210">PWA description truncate warning</span></span>  
:::image-end:::  

<span data-ttu-id="8c2cf-211">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [965802][CR965802], [1146450][CR1146450]et [1169689][CR1169689].</span><span class="sxs-lookup"><span data-stu-id="8c2cf-211">To review the history of this feature in the Chromium open-source project, navigate to Issues [965802][CR965802], [1146450][CR1146450], and [1169689][CR1169689].</span></span>  

### <a name="new-remote-address-space-column-in-the-network-tool"></a><span data-ttu-id="8c2cf-212">Nouvelle colonne Espace d’adressalage distant dans l’outil Réseau</span><span class="sxs-lookup"><span data-stu-id="8c2cf-212">New Remote Address Space column in the Network tool</span></span>  

<!-- does not work in canary 90.0.813.0 -->  
<span data-ttu-id="8c2cf-213">La nouvelle **colonne Espace d’adressag** distant affiche l’espace d’adressag IP réseau de chaque ressource réseau.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-213">The new **Remote Address Space** column displays the network IP address space of each network resource.</span></span>  <span data-ttu-id="8c2cf-214">Pour afficher la nouvelle colonne Espace d’adressas distant, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-214">To display the new Remote Address Space column, complete the following actions.</span></span>  

1.  <span data-ttu-id="8c2cf-215">Accédez à **l’outil** Réseau.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-215">Navigate to the **Network** tool.</span></span>  
1.  <span data-ttu-id="8c2cf-216">Dans le tableau Demandes, pointez sur la ligne d’en-tête et ouvrez le menu contextuel \(clic droit\).</span><span class="sxs-lookup"><span data-stu-id="8c2cf-216">In the Requests table, hover on the header row, and open the contextual menu \(right-click\).</span></span>  <span data-ttu-id="8c2cf-217">Pour savoir comment ajouter ou supprimer des colonnes de la table Requests, accédez [à Ajouter ou supprimer des colonnes.][DevtoolsNetworkReferenceAddRemoveColumns]</span><span class="sxs-lookup"><span data-stu-id="8c2cf-217">To learn how to add or remove columns from the Requests table, navigate to [Add or remove columns][DevtoolsNetworkReferenceAddRemoveColumns].</span></span>  
1.  <span data-ttu-id="8c2cf-218">Choose **Remote Address Space**.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-218">Choose **Remote Address Space**.</span></span>  
    
<span data-ttu-id="8c2cf-219">La table Requests affiche désormais une nouvelle colonne avec l’en-tête nommé **Espace d’adressare distant.**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-219">The Requests table now displays a new column with the header named **Remote Address Space**.</span></span>  <span data-ttu-id="8c2cf-220">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1128885.][CR1128885]</span><span class="sxs-lookup"><span data-stu-id="8c2cf-220">To review the history of this feature in the Chromium open-source project, navigate to Issue [1128885][CR1128885].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png" alt-text="Dans le menu contextuel, choisissez Espace d’adressas distant" lightbox="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png":::
         <span data-ttu-id="8c2cf-222">Dans le menu contextuel, choisissez **l’espace d’adressas distant**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-222">In the contextual menu, choose the **Remote Address Space**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-remote-address-space.msft.png" alt-text="La table Demandes affiche désormais la colonne Espace d’adressas distant" lightbox="../../media/2021/02/network-requests-remote-address-space.msft.png":::
         <span data-ttu-id="8c2cf-224">La table Demandes affiche désormais la colonne **Espace d’adressas distant**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-224">The Requests table now displays the **Remote Address Space** column</span></span> :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-allowed-and-disallowed-features-in-the-frame-details-view"></a><span data-ttu-id="8c2cf-225">Afficher les fonctionnalités autorisées et non autorisées dans l’affichage Détails de l’image</span><span class="sxs-lookup"><span data-stu-id="8c2cf-225">Display allowed and disallowed features in the Frame details view</span></span>  

<span data-ttu-id="8c2cf-226">L’affichage Détails de l’image affiche désormais une liste des fonctionnalités de navigateur autorisées et non autorisées contrôlées par la stratégie [d’autorisations.][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]</span><span class="sxs-lookup"><span data-stu-id="8c2cf-226">The Frame details view now displays a list of allowed and disallowed browser features controlled by the [Permissions Policy][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer].</span></span>  <span data-ttu-id="8c2cf-227">La stratégie d’autorisations est une API de plateforme web qui autorise \(ou bloque\) une page web à utiliser les fonctionnalités de navigateur dans une image individuelle ou dans des iframes qu’elle incorpore.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-227">Permissions Policy is a web platform API that allows \(or blocks\) a webpage the use of browser features in an individual frame or in iframes that it embeds.</span></span>  <span data-ttu-id="8c2cf-228">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1158827][CR1158827].</span><span class="sxs-lookup"><span data-stu-id="8c2cf-228">To review the history of this feature in the Chromium open-source project, navigate to Issue [1158827][CR1158827].</span></span>  

:::image type="complex" source="../../media/2021/02/application-frames-permissions-policy.msft.png" alt-text="Fonctionnalités autorisées et non autorisées basées sur la stratégie d’autorisation" lightbox="../../media/2021/02/application-frames-permissions-policy.msft.png":::
   <span data-ttu-id="8c2cf-230">Fonctionnalités autorisées et non autorisées basées sur la stratégie d’autorisation</span><span class="sxs-lookup"><span data-stu-id="8c2cf-230">Allowed and disallowed features based on the Permission Policy</span></span>  
:::image-end:::  

### <a name="new-sameparty-column-in-the-cookies-pane"></a><span data-ttu-id="8c2cf-231">Nouvelle colonne SameParty dans le volet Cookies</span><span class="sxs-lookup"><span data-stu-id="8c2cf-231">New SameParty column in the Cookies pane</span></span>  

<span data-ttu-id="8c2cf-232">Le **volet Cookies** de l’outil **Application** affiche désormais l’attribut de `SameParty` chaque cookie.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-232">The **Cookies** pane in the **Application** tool now displays the `SameParty` attribute for each cookie.</span></span>  <span data-ttu-id="8c2cf-233">L’attribut est un nouvel attribut booléen pour indiquer si un cookie est inclus dans les demandes aux origines des mêmes jeux de première `SameParty` [partie][GithubPrivacycgFirstPartySets].</span><span class="sxs-lookup"><span data-stu-id="8c2cf-233">The `SameParty` attribute is a new boolean attribute to indicate whether a cookie is included in requests to origins of the same [First-Party Sets][GithubPrivacycgFirstPartySets].</span></span>  <span data-ttu-id="8c2cf-234">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1161427][CR1161427].</span><span class="sxs-lookup"><span data-stu-id="8c2cf-234">To review the history of this feature in the Chromium open-source project, navigate to Issue [1161427][CR1161427].</span></span>  

:::image type="complex" source="../../media/2021/02/application-storage-cookies-sameparty.msft.png" alt-text="Colonne SameParty dans le volet Cookies" lightbox="../../media/2021/02/application-storage-cookies-sameparty.msft.png":::
   <span data-ttu-id="8c2cf-236">**Colonne SameParty** dans le **volet Cookies**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-236">**SameParty** column in the **Cookies** pane</span></span>  
:::image-end:::  

### <a name="fndisplayname-property-in-the-console-tool-is-now-deprecated"></a><span data-ttu-id="8c2cf-237">la propriété fn.displayName dans l’outil Console est désormais désacdessée</span><span class="sxs-lookup"><span data-stu-id="8c2cf-237">fn.displayName property in the Console tool is now deprecated</span></span>  

<span data-ttu-id="8c2cf-238">Auparavant, la propriété vous permettait de contrôler les noms de débogage pour les fonctions à afficher dans et dans les traces de pile `fn.displayName` `error.stack` DevTools.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-238">Previously, the `fn.displayName` property allowed you to control debug names for functions to display in `error.stack` and in DevTools stack traces.</span></span>  <span data-ttu-id="8c2cf-239">À compter de la version 90 de Microsoft Edge, la propriété est désormais remplacée par la `fn.displayName` `fn.name` propriété.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-239">Starting in Microsoft Edge version 90, the `fn.displayName` property is now deprecated, and replaced by the `fn.name` property.</span></span>  <span data-ttu-id="8c2cf-240">Utilisez la méthode standard `Object.defineProperty` pour définir la `fn.name` propriété.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-240">Use the standard `Object.defineProperty` method to define the `fn.name` property.</span></span>  <span data-ttu-id="8c2cf-241">Pour en savoir `fn.name` plus, accédez [à Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].</span><span class="sxs-lookup"><span data-stu-id="8c2cf-241">To learn more about `fn.name`, navigate to [Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].</span></span>  <span data-ttu-id="8c2cf-242">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1177685.][CR1177685]</span><span class="sxs-lookup"><span data-stu-id="8c2cf-242">To review the history of this feature in the Chromium open-source project, navigate to Issue [1177685][CR1177685].</span></span>  

:::image type="complex" source="../../media/2021/02/console-display-name-name.msft.png" alt-text="Exemple de propriété fn.name pour contrôler les noms de débogage pour les fonctions" lightbox="../../media/2021/02/console-display-name-name.msft.png":::
   <span data-ttu-id="8c2cf-244">Exemple de propriété `fn.name` pour contrôler les noms de débogage pour les fonctions</span><span class="sxs-lookup"><span data-stu-id="8c2cf-244">An example of the `fn.name` property to control debug names for functions</span></span>  
:::image-end:::  

### <a name="full-accessibility-tree-view-in-the-elements-tool"></a><span data-ttu-id="8c2cf-245">Arborescence d’accessibilité complète dans l’outil Éléments</span><span class="sxs-lookup"><span data-stu-id="8c2cf-245">Full accessibility tree view in the Elements tool</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="8c2cf-246">Cette expérience fournit une arborescence **d’accessibilité complète** dans **l’outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-246">This experiment provides a **full accessibility tree view** in the **Elements** tool.</span></span>  <span data-ttu-id="8c2cf-247">Le [volet Accessibilité][DevtoolsAccessibilityReferenceTheAccessibilityPane] fournit une arborescence d’accessibilité partielle, qui affiche la chaîne ancêtre direct du nœud racine au nœud inspecté.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-247">The [Accessibility][DevtoolsAccessibilityReferenceTheAccessibilityPane] pane provides a partial accessibility tree view, that displays the direct ancestor chain from the root node to the inspected node.</span></span>  
<span data-ttu-id="8c2cf-248">Après avoir activer cette expérience et rechargé de DevTools, choisissez l’un des boutons suivants pour basculer l’affichage dans l’outil Éléments pour tous les éléments de la page web.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-248">After you turn on this experiment and reload the DevTools, choose one of the following buttons to switch the display in the Elements tool for all elements on the webpage.</span></span>  

*   <span data-ttu-id="8c2cf-249">Pour afficher l’arborescence d’accessibilité complète, choisissez l’arborescence Basculer vers **l’arborescence d’accessibilité.**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-249">To display the full accessibility tree view , choose the **Switch to Accessibility Tree view**.</span></span>  
*   <span data-ttu-id="8c2cf-250">Pour afficher l’arborescence DOM, choisissez l’arborescence Basculer vers **l’arborescence DOM.**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-250">To display the DOM tree view, choose the **Switch to DOM Tree view**.</span></span>  
    
<span data-ttu-id="8c2cf-251">Pour activer l’expérience, [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] accédez à Activer les fonctionnalités expérimentales et activez la case à cocher en regard de l’arborescence Activer l’accessibilité complète dans le **volet Éléments.**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-251">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkbox next to **Enable full accessibility tree view in Elements pane**.</span></span>  <span data-ttu-id="8c2cf-252">Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au [problème 887173][CR887173].</span><span class="sxs-lookup"><span data-stu-id="8c2cf-252">To review the history of this feature in the Chromium open-source project, navigate to Issue [887173][CR887173].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png" alt-text="Afficher l’arborescence DOM" lightbox="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png":::
         <span data-ttu-id="8c2cf-254">Affichage de **l’affichage DOM**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-254">Display the **DOM view**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png" alt-text="Afficher l’arborescence d’accessibilité complète" lightbox="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png":::
         <span data-ttu-id="8c2cf-256">Afficher **l’arborescence d’accessibilité complète**</span><span class="sxs-lookup"><span data-stu-id="8c2cf-256">Display the **Full Accessibility Tree view**</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="8c2cf-257">Télécharger les canaux d’aperçu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8c2cf-257">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="8c2cf-258">Si vous utilisez Windows, Linux ou macOS, envisagez d’utiliser les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-258">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="8c2cf-259">Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="8c2cf-259">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="8c2cf-260">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8c2cf-260">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsAccessibilityReferenceTheAccessibilityPane]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#the-accessibility-pane "Volet Accessibilité : référence sur l’accessibilité | Documents Microsoft"  
[DevtoolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes avec le menu de commande Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsConsoleReferenceFilterByLogLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrer par niveau de journal - Référence de la console | Documents Microsoft"  
[DevtoolsConsoleReferenceFilterMessages]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-messages "Filter messages - Console Reference | Documents Microsoft"  
[DevtoolsConsoleReferenceOpenConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/console/reference#open-the-console-sidebar "Ouvrez la barre latérale de la console - Référence de la console | Documents Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personnaliser les raccourcis clavier dans l'| Microsoft Edge DevTools Documents Microsoft"  
[DevtoolsExperimentalFeaturesIndexEnablePlusButtonTabMenusToOpenMoreTools]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#enable--button-tab-menus-to-open-more-tools "Activer + les menus onglet de bouton pour ouvrir d’autres outils - Fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#turn-on-experimental-features "Activer les fonctionnalités expérimentales : fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsNetworkReferenceAddRemoveColumns]: /microsoft-edge/devtools-guide-chromium/network/reference#add-or-remove-columns "Ajouter ou supprimer des colonnes : référence de l’analyse | Documents Microsoft"  
[DevtoolsNetworkReferenceDisplayInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#display-initiators-and-dependencies "Afficher les initiateurs et les dépendances - Référence de l’analyse | Documents Microsoft"  

[ProgressiveWebAppsIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Présentation progressive des applications web sur Windows | Documents Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux d’aperçu Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Mettre à jour une extension manuellement - Extension Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Outils Microsoft Edge pour Visual Studio code | Visual Studio Marketplace"  

[ChromeDeveloperBlogImprovedPwaOfflineDetection]: https://developer.chrome.com/blog/improved-pwa-offline-detection "Amélioration de la détection de détection de la prise en charge en mode hors connexion de Progressive Web App | Développeurs Chrome"  

[ChromestatusFeature5354410980933632]: https://www.chromestatus.com/feature/5354410980933632 "color-gamut media query | État de la plateforme Chrome"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  
[CR174309]: https://crbug.com/174309 "Problème 174309: DevTools: Autoriser la personnalisation des raccourcis clavier/les combinaisons de touches | Bogues Chromium"  
[CR887173]: https://crbug.com/887173 "Problème 887173 : DevTools : inspection complète de l’arborescence d’accessibilité | Bogues Chromium"  
[CR965802]: https://crbug.com/965802 "Problème 965802 : implémenter la détection des fonctionnalités hors connexion du service plus précise | Bogues Chromium"  
[CR1073887]: https://crbug.com/1073887 "Problème 1073887 : DevTools : @media (color-gamut: ...) colorspace emulation | Bogues Chromium"  
[CR1128885]: https://crbug.com/1128885 "Problème 1128885 : Prise en charge de DevTools pour cors-RFC1918 | Bogues Chromium"  
[CR1146450]: https://crbug.com/1146450 "Problème 1146450 : [Android] Implémenter les installations de feuille inférieure | Bogues Chromium"  
[CR1158276]: https://crbug.com/1158276 "Problème 1158276 : Impossible de développer/de contracter le volet « Chaîne de l’initiateur de la demande » à l’aide des touches de direction dans la section « Réseau » de DevTools | Bogues Chromium"  
[CR1158827]: https://crbug.com/1158827 "Problème 1158827 : [Stratégie d’autorisations] Implémenter la prise en charge de la dévtool pour les stratégies d’autorisations | Bogues Chromium"  
[CR1160637]: https://crbug.com/1160637 "Problème 1160637 : la section « Réseau » de la fenêtre « Outils de développement » de la fenêtre « Demander une chaîne d’initiateur » est incomplète | Bogues Chromium"  
[CR1161427]: https://crbug.com/1161427 "Problème 1161427 : &#9730; prise en charge du débogage d’attribut de cookie SameParty dans DevTools | Bogues Chromium"  
[CR1166710]: https://crbug.com/1166710 "Problème 1166710 : activer l’expérience d’outils flexbox par défaut | Bogues Chromium"  
[CR1169689]: https://crbug.com/1169689 "Problème 1169689 : la feuille inférieure de l’installation PWA ne doit pas être une catégorie de fonctionnalités | Bogues Chromium"  
[CR1175699]: https://crbug.com/1175699 "Problème 1175699 : éditeur Flexbox | Bogues Chromium"  
[CR1177685]: https://crbug.com/1177685 "Problème 1177685 : supprimer la prise en charge de fn.displayName non standard | Bogues Chromium"  
[CR1178530]: https://crbug.com/1178530 "Problème 1178530 : la console n’échappe pas aux doublequotes lors de l’impression de chaînes | Bogues Chromium"  

[CsswgDraftsMediaqueries4ColorGamut]: https://drafts.csswg.org/mediaqueries-4#color-gamut "Qualité de l’affichage des couleurs : fonctionnalité « color-gamut » | Brouillons de l’éditeur de groupe de travail CSS"  

[GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/DevTools/FocusMode/explainer.md "DevTools : interface utilisateur du mode Focus - MicrosoftEdge/MSEdgeExplainers | GitHub"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubPrivacycgFirstPartySets]: https://github.com/privacycg/first-party-sets "Jeux de groupes | GitHub"  

[GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Expliqueur de stratégie d’autorisations | GitHub"  

[MdnJavascriptReferenceGlobalObjectsFunctionName]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/name "Function.name | MDN"  

> [!NOTE]
> <span data-ttu-id="8c2cf-300">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8c2cf-300">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8c2cf-301">La page d’origine est disponible [ici](https://developers.google.com/web/updates/2021/02/devtools/index) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)</span><span class="sxs-lookup"><span data-stu-id="8c2cf-301">The original page is found [here](https://developers.google.com/web/updates/2021/02/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="8c2cf-303">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8c2cf-303">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  