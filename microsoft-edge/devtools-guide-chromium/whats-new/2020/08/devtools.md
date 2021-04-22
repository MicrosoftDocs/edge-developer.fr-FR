---
description: Match keyboard shortcuts to Visual Studio Code, emulate Surface Duo and Samsung Postal Fold, CSS grid overlay improvements, and more.
title: Nouveautés de DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: f1227f0869aa753c2d05980c712ca3453adfd041
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514381"
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
# <a name="whats-new-in-devtools-microsoft-edge-86"></a><span data-ttu-id="7dd6d-104">Nouveautés de DevTools (Microsoft Edge 86)</span><span class="sxs-lookup"><span data-stu-id="7dd6d-104">What's New In DevTools (Microsoft Edge 86)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="7dd6d-105">Annonces de l'équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7dd6d-105">Announcements from the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### <a name="match-keyboard-shortcuts-in-devtools-to-visual-studio-code"></a><span data-ttu-id="7dd6d-106">Faire correspondre les raccourcis clavier dans DevTools à Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="7dd6d-106">Match keyboard shortcuts in DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="7dd6d-107">Dans Microsoft Edge 86, vous pouvez faire correspondre les raccourcis clavier des DevTools à vos raccourcis dans [Microsoft Visual Studio Code][VisualStudioCode].</span><span class="sxs-lookup"><span data-stu-id="7dd6d-107">In Microsoft Edge 86, you may match keyboard shortcuts in the DevTools to your shortcuts in [Microsoft Visual Studio Code][VisualStudioCode].</span></span>  

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Faire correspondre les raccourcis clavier dans DevTools à Visual Studio Code" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   <span data-ttu-id="7dd6d-109">Faire correspondre les raccourcis clavier dans DevTools à Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="7dd6d-109">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-110">Pour activer cette fonctionnalité, accédez à Personnaliser les raccourcis clavier dans [Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="7dd6d-110">To activate this feature, navigate to [Customize keyboard shortcuts in the Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span></span>  

<span data-ttu-id="7dd6d-111">Par exemple, le raccourci clavier pour mettre en pause ou poursuivre l'exécution d'un script [dans Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] est `F5` .</span><span class="sxs-lookup"><span data-stu-id="7dd6d-111">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="7dd6d-112">Avec **devTools (par défaut)** prédéfiny, ce même raccourci dans devTools est , mais lorsque vous choisissez l'Visual Studio `F8` **Code** prédéfiny, ce raccourci est désormais également `F5` .</span><span class="sxs-lookup"><span data-stu-id="7dd6d-112">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8`, but when you choose the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="7dd6d-113">Problème de chrome [#174309][CR174309]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-113">Chromium issue [#174309][CR174309]</span></span>  

### <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a><span data-ttu-id="7dd6d-114">Émuler Surface Duo et Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="7dd6d-114">Emulate Surface Duo and Samsung Galaxy Fold</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   <span data-ttu-id="7dd6d-116">Fonctionnalité expérimentale</span><span class="sxs-lookup"><span data-stu-id="7dd6d-116">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-117">Vous pouvez maintenant tester l'apparence de votre site web ou de votre application sur deux nouveaux appareils :  [Surface Duo][MicrosoftSurfaceDevicesDuo] et Samsung [Contrôle Fold][SamsungMobileGalaxyFold] dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-117">You are now able to test the look and feel of your website or app on two new devices:  [Surface Duo][MicrosoftSurfaceDevicesDuo] and [Samsung Galaxy Fold][SamsungMobileGalaxyFold] in Microsoft Edge.</span></span>  

<span data-ttu-id="7dd6d-118">Pour contribuer à améliorer votre site web ou votre application pour les appareils à double écran et pliables, utilisez les fonctionnalités suivantes lors de [l’émulation de l’appareil][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="7dd6d-118">To help enhance your website or app for the dual-screen and foldable devices, use the following features when [emulating the device][DevtoolsDeviceModeIndex].</span></span>  

*   <span data-ttu-id="7dd6d-119">[Couvrant,][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], c’est-à-dire lorsque votre site web \(ou application\) apparaît sur les deux écrans.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-119">[Spanning][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], which is when your website \(or app\) appears across both screens.</span></span>
*   <span data-ttu-id="7dd6d-120">[Rendu de la jointure][DualScreenIntroductionHowWorkSeam], à savoir l’espace entre les deux écrans.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-120">[Rendering the seam][DualScreenIntroductionHowWorkSeam], which is the space between the two screens.</span></span>
*   <span data-ttu-id="7dd6d-121">[Permettre aux][DevtoolsExperimentalFeaturesEnableExperimentalApis] API de plateforme Web expérimentales d'accéder à la nouvelle fonctionnalité multimédia [CSS][DualScreenWebCssMediaSpanning] couvrant l'écran et à l'API [JavaScript getWindowSegments][DualScreenWebJavascriptGetwindowsegments].</span><span class="sxs-lookup"><span data-stu-id="7dd6d-121">[Enabling experimental Web Platform APIs][DevtoolsExperimentalFeaturesEnableExperimentalApis] to access the new [CSS media screen-spanning feature][DualScreenWebCssMediaSpanning] and [JavaScript getWindowSegments API][DualScreenWebJavascriptGetwindowsegments].</span></span>  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Émulation d'appareil pour Surface Duo" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   <span data-ttu-id="7dd6d-123">Émulation d'appareil pour Surface Duo</span><span class="sxs-lookup"><span data-stu-id="7dd6d-123">Device emulation for Surface Duo</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-124">Pour activer cette fonctionnalité expérimentale, accédez à Activer les fonctionnalités expérimentales et cochez la case en regard d'Émulation : prendre en charge le **mode double écran.** [][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-124">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Emulation: Support dual screen mode**.</span></span>  

<span data-ttu-id="7dd6d-125">Pour plus d'informations sur cette expérience, accédez à [Émulation : prendre en charge le mode double écran.][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-125">For more information about this experiment, navigate to [Emulation: Support dual screen mode][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].</span></span>  

<span data-ttu-id="7dd6d-126">Problème de chrome : [#1054281][CR1054281]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-126">Chromium issue: [#1054281][CR1054281]</span></span>  

### <a name="css-grid-overlay-improvements-and-new-experimental-grid-features"></a><span data-ttu-id="7dd6d-127">Améliorations de la superposition de grille CSS et nouvelles fonctionnalités de grille expérimentale</span><span class="sxs-lookup"><span data-stu-id="7dd6d-127">CSS grid overlay improvements and new experimental grid features</span></span>  

<span data-ttu-id="7dd6d-128">Merci pour les commentaires positifs sur les superpositions de grille CSS améliorées.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-128">Thank you for the positive feedback about the improved CSS grid overlays.</span></span>  <span data-ttu-id="7dd6d-129">Les superpositions de grille CSS sont désormais activées par défaut et ne vous obligent pas à activer une expérience.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-129">The CSS grid overlays are now enabled by default and do not require you to turn on an experiment.</span></span>  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Superposition de grille CSS pour l'élément article" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   <span data-ttu-id="7dd6d-131">Superposition de grille CSS pour `article` l'élément</span><span class="sxs-lookup"><span data-stu-id="7dd6d-131">CSS grid overlay for `article` element</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="7dd6d-132">Pour plus d'informations sur les superpositions de grille, accédez aux fonctionnalités de débogage de grille [CSS.][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-132">For more information about grid overlays, navigate to [CSS grid debugging features][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="7dd6d-133">L'équipe Microsoft Edge DevTools et l'équipe Chrome DevTools collaborent sur des fonctionnalités supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-133">The Microsoft Edge DevTools team and the Chrome DevTools team collaborate on additional features.</span></span>  <span data-ttu-id="7dd6d-134">Les nouvelles fonctionnalités incluent plusieurs superpositions persistantes et configurables à partir d'un **nouveau** volet Disposition de **l'outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-134">The new features include multiple overlays that are persistent and configurable from a new **Layout** pane on the **Elements** tool.</span></span>  

<span data-ttu-id="7dd6d-135">Pour activer cette fonctionnalité expérimentale, accédez à Activer les fonctionnalités expérimentales et activez la case à cocher en regard de Activer les nouvelles fonctionnalités de débogage de la grille **CSS (options**de configuration disponibles dans le volet de barre latérale de disposition dans les éléments après le redémarrage). [][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-135">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable new CSS Grid debugging features (configuration options available in Layout sidebar pane in Elements after restart)**.</span></span>  

<span data-ttu-id="7dd6d-136">Pour plus d'informations sur cette expérience, accédez à Activer les nouvelles fonctionnalités de débogage de grille [CSS.][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-136">For more information about this experiment, navigate to [Enable new CSS grid debugging features][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="7dd6d-137">Problème de chrome : [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-137">Chromium issue: [#1047356][CR1047356]</span></span>  

### <a name="table-copied-from-the-console-preserves-formatting"></a><span data-ttu-id="7dd6d-138">Le tableau copié à partir de la console conserve la mise en forme</span><span class="sxs-lookup"><span data-stu-id="7dd6d-138">Table copied from the Console preserves formatting</span></span>  

<span data-ttu-id="7dd6d-139">Dans Microsoft Edge 85 ou une antérieure, la mise en forme d'une copie `console.table` a été perdue.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-139">In Microsoft Edge 85 or earlier, the formatting of a copied `console.table` was lost.</span></span>  <span data-ttu-id="7dd6d-140">Si vous avez copié la sortie de l'API console de [tableau][DevtoolsConsoleApiTable] et que vous l'avez copiée, seul le texte de la table a été conservé.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-140">If you copied the output from the [table][DevtoolsConsoleApiTable] Console API, and pasted it, only the text of the table was kept.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="sortie de l'API console de tableau dans Microsoft Edge 85 ou une antérieure" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` <span data-ttu-id="7dd6d-142">Sortie de l'API console dans Microsoft Edge 85 ou une antérieure</span><span class="sxs-lookup"><span data-stu-id="7dd6d-142">Console API output in Microsoft Edge 85 or earlier</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="table Console API output from Microsoft Edge 85 or earlier pasted into Visual Studio Code" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="7dd6d-144">Sortie de l'API console à partir de Microsoft Edge 85 ou d'une Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="7dd6d-144">Console API output from Microsoft Edge 85 or earlier pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="7dd6d-145">Dans Microsoft Edge 86 ou version ultérieure, lorsque vous copiez un tableau à partir de la **console,** la mise en forme est désormais conservée.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-145">In Microsoft Edge 86 or later, when you copy a table from the **Console**, the formatting is now preserved.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="table Console API output in Microsoft Edge 86 or later" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` <span data-ttu-id="7dd6d-147">Sortie de l'API console dans Microsoft Edge 86 ou une ultérieure</span><span class="sxs-lookup"><span data-stu-id="7dd6d-147">Console API output in Microsoft Edge 86 or later</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="table Console API output from Microsoft Edge 86 or later pasted into Visual Studio Code" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="7dd6d-149">Sortie de l'API console de Microsoft Edge 86 ou ultérieurement Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="7dd6d-149">Console API output from Microsoft Edge 86 or later pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="7dd6d-150">Problème de chrome : [#1115011][CR1115011]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-150">Chromium issue: [#1115011][CR1115011]</span></span>  

### <a name="source-order-viewer-for-easier-accessibility-testing"></a><span data-ttu-id="7dd6d-151">Visionneuse d'ordre source pour faciliter les tests d'accessibilité</span><span class="sxs-lookup"><span data-stu-id="7dd6d-151">Source Order Viewer for easier accessibility testing</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   <span data-ttu-id="7dd6d-153">Fonctionnalité expérimentale</span><span class="sxs-lookup"><span data-stu-id="7dd6d-153">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-154">Le nouvel élément d'aide sur l'accessibilité affiche l'ordre des éléments dans la source.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-154">The new accessibility helper displays the order of elements in the source.</span></span>  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Activer Afficher l'ordre de la source" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   <span data-ttu-id="7dd6d-156">Activer **Afficher l'ordre de la source**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-156">Activate **Show source order**</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-157">Cette fonctionnalité facilite le test de l'expérience des utilisateurs de lecteur d'écran et de clavier sur votre site web ou votre application.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-157">This feature makes it easier to test the way screen reader and keyboard users experience your website or app.</span></span>  <span data-ttu-id="7dd6d-158">Les lecteurs d'écran et la navigation au clavier dépendent du contenu placé dans un ordre particulier dans le code source de votre site web ou de votre application, afin qu'il corresponde à la page rendue.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-158">Screen readers and keyboard navigation depend on content being placed in a particular order in the source code of your website or app, so that it matches the rendered page.</span></span>  <span data-ttu-id="7dd6d-159">L'Afficheur des commandes sources affiche les différences potentielles dans l'ordre entre la page rendue et le code source.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-159">The Source Order Viewer displays potential differences in order between the rendered page and the source code.</span></span>  

<span data-ttu-id="7dd6d-160">Pour activer cette fonctionnalité expérimentale, accédez à Activer les fonctionnalités expérimentales et activez la case à cocher en regard de Activer la visionneuse de commandes **source.** [][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-160">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Source Order Viewer**.</span></span>  

<span data-ttu-id="7dd6d-161">Pour plus d'informations sur cette expérience, accédez à [Activer l'Observateur de commandes source.][DevtoolsExperimentalFeaturesEnableSourceOrderViewer]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-161">For more information about this experiment, navigate to [Enable Source Order Viewer][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].</span></span>  

<span data-ttu-id="7dd6d-162">Problème de chrome : [#1094406][CR1094406]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-162">Chromium issue: [#1094406][CR1094406]</span></span>  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Microsoft Edge DevTools in Traditional Chinese" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Microsoft Edge DevTools in Japanese" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### <a name="highlight-all-search-results-in-elements-tool"></a><span data-ttu-id="7dd6d-163">Mettre en surbrill valeur tous les résultats de recherche dans l'outil Éléments</span><span class="sxs-lookup"><span data-stu-id="7dd6d-163">Highlight all search results in Elements tool</span></span>  

<span data-ttu-id="7dd6d-164">Dans Microsoft Edge 84 et 85, le premier résultat de recherche dans l'outil **Éléments** n'a pas été mis en surbrillant.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-164">In Microsoft Edge 84 and 85, the first search result in the **Elements** tool did not highlight.</span></span>  <span data-ttu-id="7dd6d-165">Les résultats de recherche restants ont été mis en surbrillant correctement.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-165">The remaining search results were highlighted correctly.</span></span>  

<span data-ttu-id="7dd6d-166">Merci d'avoir envoyé vos commentaires et d'avoir amélioré Chromium.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-166">Thank you for sending your feedback and helping improve Chromium.</span></span>  <span data-ttu-id="7dd6d-167">Vos commentaires ont révélé un [problème #1103316][CR1103316] dans le projet Chromium open source.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-167">Your feedback uncovered Issue [#1103316][CR1103316] in the open-source Chromium project.</span></span>  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Premier résultat de recherche mis en surbrillrillant dans le panneau Éléments dans Microsoft Edge 84 ou ultérieur" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   <span data-ttu-id="7dd6d-169">Premier résultat de recherche mis en évidence sur **l'outil Éléments** dans Microsoft Edge 84 ou ultérieur</span><span class="sxs-lookup"><span data-stu-id="7dd6d-169">Highlighted first search result on **Elements** tool in Microsoft Edge 84 or later</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-170">Le problème est désormais résolu dans toutes les versions de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-170">The issue is now fixed in all versions of Microsoft Edge.</span></span>  

<span data-ttu-id="7dd6d-171">Problème de chrome : [#1103316][CR1103316]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-171">Chromium issue: [#1103316][CR1103316]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="7dd6d-172">Annonces du projet de Chromium</span><span class="sxs-lookup"><span data-stu-id="7dd6d-172">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-media-tool"></a><span data-ttu-id="7dd6d-173">Outil Nouveau média</span><span class="sxs-lookup"><span data-stu-id="7dd6d-173">New Media tool</span></span>  

<span data-ttu-id="7dd6d-174">DevTools affiche désormais les informations des joueurs multimédias dans [l'outil Multimédia.][DevtoolsMediaPanelIndex]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-174">DevTools now displays media players information in the [Media][DevtoolsMediaPanelIndex] tool.</span></span>  

<span data-ttu-id="7dd6d-175">Pour ouvrir le nouvel **outil Multimédia,** terminez l'étape suivante.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-175">To open the new **Media** tool, complete the following step.</span></span>  

1.  <span data-ttu-id="7dd6d-176">Choose **Customize and control DevTools** \( `...` \) > More **tools**  >  **Media**.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-176">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Outil Nouveau média" lightbox="../../media/2020/08/media-panel.msft.png":::
       <span data-ttu-id="7dd6d-178">Outil **Nouveau** média</span><span class="sxs-lookup"><span data-stu-id="7dd6d-178">New **Media** tool</span></span>  
    :::image-end:::  

<span data-ttu-id="7dd6d-179">Avant le nouvel **outil Multimédia** dans DevTools, les informations de journalisation et de débogage sur les joueurs vidéo se trouvaient sous le paramètre **Joueurs récents.**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-179">Before the new **Media** tool in DevTools, the logging and debug information about video players was located under the **Recent Players** setting.</span></span>  <span data-ttu-id="7dd6d-180">Pour ouvrir le **paramètre Joueurs** récents, accédez à l'outil Players et `edge://media-internals` **choisissez-le.**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-180">To open the **Recent Players** setting, navigate to `edge://media-internals` and choose the **Players** tool.</span></span>  

<span data-ttu-id="7dd6d-181">Affichez le contenu en direct et examinez les problèmes potentiels plus rapidement, y compris les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-181">View live content and inspect potential issues more quickly, including the following examples.</span></span>  

*   <span data-ttu-id="7dd6d-182">Pourquoi les images sont-elles abandonnées ?</span><span class="sxs-lookup"><span data-stu-id="7dd6d-182">Why frames are dropped?</span></span>  
*   <span data-ttu-id="7dd6d-183">Pourquoi JavaScript interagit-il avec le joueur de manière inattendue ?</span><span class="sxs-lookup"><span data-stu-id="7dd6d-183">Why JavaScript is interacting with the player in an unexpected way?</span></span>  

### <a name="capture-node-screenshots-using-the-elements-tool-context-menu"></a><span data-ttu-id="7dd6d-184">Capture d'écran de nœud à l'aide du menu contextique de l'outil Éléments</span><span class="sxs-lookup"><span data-stu-id="7dd6d-184">Capture node screenshots using the Elements tool context menu</span></span>  

<span data-ttu-id="7dd6d-185">Vous pouvez maintenant capturer des captures d'écran de nœud à l'aide du menu contextique de **l'outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-185">You may now capture node screenshots using the context menu in the **Elements** tool.</span></span>  

<span data-ttu-id="7dd6d-186">Par exemple, pour prendre une capture d'écran de la table des matières, pointez sur l'élément, ouvrez le menu contextuel \(clic droit\), puis sélectionnez **Capture d'écran du nœud**.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-186">For example, to take a screenshot of the table of contents, hover on the element, open the contextual menu \(right-click\), and select **Capture node screenshot**.</span></span>  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Capture d'écran de nœud" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   <span data-ttu-id="7dd6d-188">Capture d'écran de nœud</span><span class="sxs-lookup"><span data-stu-id="7dd6d-188">Capture node screenshots</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-189">Problème de chrome : [#1100253][CR1100253]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-189">Chromium issue: [#1100253][CR1100253]</span></span>  

### <a name="issues-tool-updates"></a><span data-ttu-id="7dd6d-190">Mises à jour de l'outil Problèmes</span><span class="sxs-lookup"><span data-stu-id="7dd6d-190">Issues tool updates</span></span>  

<span data-ttu-id="7dd6d-191">La barre d'avertissement Problèmes de l'outil **Console** est désormais remplacée par un message normal.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-191">The Issues warning bar on the **Console** tool is now replaced with a regular message.</span></span>  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Problèmes dans le message de la console" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   <span data-ttu-id="7dd6d-193">Problèmes dans le message de la console</span><span class="sxs-lookup"><span data-stu-id="7dd6d-193">Issues in console message</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-194">Les problèmes de cookie tiers sont désormais masqués par défaut dans **l'outil Problèmes.**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-194">Third-party cookie issues are now hidden by default in the **Issues** tool.</span></span>  <span data-ttu-id="7dd6d-195">Activez la nouvelle **case à cocher Inclure les problèmes de cookie tiers** pour afficher les problèmes.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-195">Enable the new **Include third-party cookie issues** checkbox to view the issues.</span></span>  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="Case à cocher problèmes de cookie tiers" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   <span data-ttu-id="7dd6d-197">Case à cocher problèmes de cookie tiers</span><span class="sxs-lookup"><span data-stu-id="7dd6d-197">third-party cookie issues checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-198">Problèmes de chrome : [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-198">Chromium issues: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span></span>  

### <a name="emulate-missing-local-fonts"></a><span data-ttu-id="7dd6d-199">Émuler les polices locales manquantes</span><span class="sxs-lookup"><span data-stu-id="7dd6d-199">Emulate missing local fonts</span></span>  

<span data-ttu-id="7dd6d-200">Ouvrez [l'outil de rendu][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] et utilisez la nouvelle fonctionnalité Désactiver les **polices locales** pour émuler les `local()` sources manquantes dans les `@font-face` règles.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-200">Open the [Rendering tool][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] and use the new **Disable local fonts** feature to emulate missing `local()` sources in `@font-face` rules.</span></span>  

<span data-ttu-id="7dd6d-201">Par exemple, lorsque la police est installée sur votre appareil et que la règle l'utilise comme police, Microsoft Edge utilise le fichier de police `Rubik` `@font-face src` local de votre `local()` appareil.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-201">For example, when the `Rubik` font is installed on your device and the `@font-face src` rule uses it as a `local()` font, Microsoft Edge uses the local font file from your device.</span></span>  

<span data-ttu-id="7dd6d-202">Lorsque **disable local fonts** is enabled, DevTools ignores the `local()` fonts and fetches each from the network.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-202">When **Disable local fonts** is enabled, DevTools ignores the `local()` fonts and fetches each from the network.</span></span>  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Émuler les polices locales manquantes" lightbox="../../media/2020/08/disable-font.msft.png":::
   <span data-ttu-id="7dd6d-204">Émuler les polices locales manquantes</span><span class="sxs-lookup"><span data-stu-id="7dd6d-204">Emulate missing local fonts</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-205">Si vous utilisez deux copies différentes de la même police lors du développement, telles que les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-205">If you use two different copies of the same font during development, such as the following examples.</span></span>  

*   <span data-ttu-id="7dd6d-206">Police locale pour vos outils de conception.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-206">A local font for your design tools.</span></span>  
*   <span data-ttu-id="7dd6d-207">Police web pour votre code.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-207">A web font for your code.</span></span>  

<span data-ttu-id="7dd6d-208">**Désactivez les polices locales** pour faciliter l'effectuer.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-208">Use **Disable local fonts** to make it easier for you to complete the following tasks.</span></span>  

*   <span data-ttu-id="7dd6d-209">Déboguer et mesurer les performances de chargement et l'optimisation des polices web.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-209">Debug and measure loading performance and optimization of web fonts.</span></span>  
*   <span data-ttu-id="7dd6d-210">Vérifiez la précision de vos règles `@font-face` CSS.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-210">Verify accuracy of your CSS `@font-face` rules.</span></span>  
*   <span data-ttu-id="7dd6d-211">Découvrez les différences entre les versions locales installées sur votre appareil et une police web.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-211">Discover differences between local versions installed on your device and a web font.</span></span>  

<span data-ttu-id="7dd6d-212">Problème de chrome : [#384968][CR384968]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-212">Chromium issue: [#384968][CR384968]</span></span>  

### <a name="emulate-inactive-users"></a><span data-ttu-id="7dd6d-213">Émuler les utilisateurs inactifs</span><span class="sxs-lookup"><span data-stu-id="7dd6d-213">Emulate inactive users</span></span>  

<span data-ttu-id="7dd6d-214">[L'API de détection d'inactivité][WebDevIdleDetection] permet aux développeurs de détecter les utilisateurs inactifs et de réagir aux changements d'état d'inactivité.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-214">The [Idle Detection API][WebDevIdleDetection] allows developers to detect inactive users and react on idle state changes.</span></span>  <span data-ttu-id="7dd6d-215">Vous pouvez désormais utiliser DevTools pour émuler les changements d'état d'inactivité dans l'outil **Sensors** pour l'état de l'utilisateur et de l'écran au lieu d'attendre que l'état d'inactivité réel change.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-215">You are now able to use DevTools to emulate idle state changes in the **Sensors** tool for both the user state and the screen state instead of waiting for the actual idle state to change.</span></span>  <span data-ttu-id="7dd6d-216">Vous pouvez ouvrir **l'outil Capteurs** à partir du [caisse.][DevtoolsCustomizeIndexDrawer]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-216">You may open the **Sensors** tool from the [Drawer][DevtoolsCustomizeIndexDrawer].</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Émuler les utilisateurs inactifs" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   <span data-ttu-id="7dd6d-218">Émuler les utilisateurs inactifs</span><span class="sxs-lookup"><span data-stu-id="7dd6d-218">Emulate inactive users</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-219">Problème de chrome : [#1090802][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-219">Chromium issue: [#1090802][CR1090802]</span></span>  

### <a name="emulate-prefers-reduced-data"></a><span data-ttu-id="7dd6d-220">Émuler prefers-reduced-data</span><span class="sxs-lookup"><span data-stu-id="7dd6d-220">Emulate prefers-reduced-data</span></span>  

> [!NOTE]
> <span data-ttu-id="7dd6d-221">Dans Microsoft Edge 86, pour activer cette fonctionnalité, accédez à l'indicateur de fonctionnalités de plateforme Web expérimentale et `edge://flags#enable-experimental-web-platform-features` **activez-le.**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-221">In Microsoft Edge 86, to enable this feature, navigate to `edge://flags#enable-experimental-web-platform-features` and turn on the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="7dd6d-222">L'option d'émulation s'affiche uniquement si l'indicateur est activé.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-222">The emulation option is only displayed if the flag is enabled.</span></span>  

<span data-ttu-id="7dd6d-223">La requête multimédia préférer les données [réduites][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] détecte les préférences de contenu utilisateur pour les données réduites.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-223">The [prefers-reduced-data][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] media query detects user content preferences for reduced data.</span></span>  <span data-ttu-id="7dd6d-224">S'il est sélectionné, l'utilisateur reçoit un contenu de page de remplacement qui utilise moins de données.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-224">If selected, the user receives alternate page content that uses less data.</span></span>  

<span data-ttu-id="7dd6d-225">Vous pouvez maintenant utiliser DevTools pour émuler la `prefers-reduced-data` requête multimédia.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-225">You may now use DevTools to emulate the `prefers-reduced-data` media query.</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Émuler prefers-reduced-data" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   <span data-ttu-id="7dd6d-227">Émuler prefers-reduced-data</span><span class="sxs-lookup"><span data-stu-id="7dd6d-227">Emulate prefers-reduced-data</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-228">Problème de chrome : [#1096068][CR1096068]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-228">Chromium issue: [#1096068][CR1096068]</span></span>  

### <a name="support-for-new-javascript-features"></a><span data-ttu-id="7dd6d-229">Prise en charge des nouvelles fonctionnalités JavaScript</span><span class="sxs-lookup"><span data-stu-id="7dd6d-229">Support for new JavaScript features</span></span>  

<span data-ttu-id="7dd6d-230">Les devTools ont désormais mieux pris en charge les fonctionnalités de langage JavaScript suivantes.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-230">DevTools now have better supported the following JavaScript language features.</span></span>  

| <span data-ttu-id="7dd6d-231">Fonctionnalité de langage JavaScript</span><span class="sxs-lookup"><span data-stu-id="7dd6d-231">JavaScript language feature</span></span> | <span data-ttu-id="7dd6d-232">Détails</span><span class="sxs-lookup"><span data-stu-id="7dd6d-232">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="7dd6d-233">Opérateurs d'affectation logique</span><span class="sxs-lookup"><span data-stu-id="7dd6d-233">Logical assignment operators</span></span>][V8FeaturesLogicalAssignment] | <span data-ttu-id="7dd6d-234">DevTools prend désormais en charge l'affectation logique avec le nouveau , et les opérateurs dans les outils `&&=` `||=` Console et `??=` **Sources.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7dd6d-234">DevTools now supports logical assignment with the new `&&=`, `||=`, and `??=` operators in the **Console** and **Sources** tools.</span></span>  |  
| <span data-ttu-id="7dd6d-235">Séparateurs [numériques][V8FeaturesNumericSeparators] à impression courte</span><span class="sxs-lookup"><span data-stu-id="7dd6d-235">Pretty-print [numeric separators][V8FeaturesNumericSeparators]</span></span> | <span data-ttu-id="7dd6d-236">DevTools imprime maintenant correctement les séparateurs numériques dans l'outil **Sources.**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-236">DevTools now properly pretty-prints the numeric separators in the **Sources** tool.</span></span>  |  

<span data-ttu-id="7dd6d-237">Problèmes de chrome : [1086817][CR1086817], [1080569][CR1080569]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-237">Chromium issues: [1086817][CR1086817], [1080569][CR1080569]</span></span>  

### <a name="lighthouse-62-in-the-lighthouse-panel"></a><span data-ttu-id="7dd6d-238">Île 6.2 dans le panneau Panneau de sélection</span><span class="sxs-lookup"><span data-stu-id="7dd6d-238">Lighthouse 6.2 in the Lighthouse panel</span></span>  

<span data-ttu-id="7dd6d-239">**L'outil Îles** exécute à présent Ce dernier 6.2.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-239">The **Lighthouse** tool is now running Lighthouse 6.2.</span></span>  <span data-ttu-id="7dd6d-240">Pour obtenir la liste complète des modifications, accédez aux notes de [publication de Cerr.][GithubGooglechromeLighthouseV620]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-240">For a full list of changes, navigate to the [Lighthouse release notes][GithubGooglechromeLighthouseV620].</span></span>  

<span data-ttu-id="7dd6d-241">Problème de chrome : [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-241">Chromium issue: [#772558][CR772558]</span></span>  

### <a name="deprecation-of-other-origins-listing-in-the-service-workers-pane"></a><span data-ttu-id="7dd6d-242">Désérision d'autres origines dans le volet Travailleurs du service</span><span class="sxs-lookup"><span data-stu-id="7dd6d-242">Deprecation of other origins listing in the Service Workers pane</span></span>  

<span data-ttu-id="7dd6d-243">DevTools fournit désormais un \*\*\*\* lien à partir du volet Travailleurs \*\*\*\* du service \(**Outil** d'application > Volet De travail du service\) pour afficher la liste complète des travailleurs de service d'autres origines.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-243">DevTools now provides a link from the **Service workers** pane \(**Application** tool > **Service workers** pane\) to view the full list of service workers from other origins.</span></span>  <span data-ttu-id="7dd6d-244">Pour accéder à la liste sans ouvrir de DevTools, accédez à `edge://service-worker-internals/?devtools` .</span><span class="sxs-lookup"><span data-stu-id="7dd6d-244">To access the list without opening the DevTools, navigate to `edge://service-worker-internals/?devtools`.</span></span>  

<span data-ttu-id="7dd6d-245">Auparavant, DevTools affichait une liste imbriée sous l'outil **Application** pour > **de travail du service.**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-245">Previously DevTools displayed a list nested under the **Application** tool > **Service workers** pane.</span></span>  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Lien vers d'autres origines" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   <span data-ttu-id="7dd6d-247">Lien vers d'autres origines</span><span class="sxs-lookup"><span data-stu-id="7dd6d-247">Link to other origins</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-248">Problème de chrome : [#807440][CR807440]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-248">Chromium issue: [#807440][CR807440]</span></span>  

### <a name="show-coverage-summary-for-filtered-items"></a><span data-ttu-id="7dd6d-249">Afficher le résumé de la couverture pour les éléments filtrés</span><span class="sxs-lookup"><span data-stu-id="7dd6d-249">Show coverage summary for filtered items</span></span>  

<span data-ttu-id="7dd6d-250">DevTools recalcule maintenant et affiche dynamiquement un résumé des informations de couverture.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-250">DevTools now recalculate and display a summary of coverage information dynamically.</span></span>  <span data-ttu-id="7dd6d-251">L'affichage dynamique est déclenché lorsque des filtres sont appliqués dans [l'outil Couverture.][DevtoolsCoverageIndex]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-251">The dynamic display is triggered when filters are applied in the [Coverage][DevtoolsCoverageIndex] tool.</span></span>  <span data-ttu-id="7dd6d-252">Avant que **l'outil** Couverture affiche toujours un résumé de toutes les informations de couverture.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-252">Before the **Coverage** tool always displayed a summary of all coverage information.</span></span>  

<span data-ttu-id="7dd6d-253">Dans la première des figures suivantes, le résumé s'affiche initialement et, dans la seconde des figures suivantes, le résumé s'affiche après l'application du filtrage `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` CSS.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-253">In the first of the following figures, the summary initially displays `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` and in the second of the following figures, the summary displays `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` after CSS filtering is applied.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Résumé de la couverture" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         <span data-ttu-id="7dd6d-255">Résumé de la couverture</span><span class="sxs-lookup"><span data-stu-id="7dd6d-255">Coverage summary</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Résumé de la couverture pour les éléments filtrés" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         <span data-ttu-id="7dd6d-257">Résumé de la couverture pour les éléments filtrés</span><span class="sxs-lookup"><span data-stu-id="7dd6d-257">Coverage summary for filtered items</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="7dd6d-258">Problème de chrome : [#1061385][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-258">Chromium issue: [#1061385][CR1090802]</span></span>  

### <a name="new-frame-details-view-in-application-panel"></a><span data-ttu-id="7dd6d-259">Affichage des détails d'une nouvelle image dans le panneau Application</span><span class="sxs-lookup"><span data-stu-id="7dd6d-259">New frame details view in Application panel</span></span>  

<span data-ttu-id="7dd6d-260">DevTools affiche désormais une vue détaillée pour chaque image.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-260">DevTools now show a detailed view for each frame.</span></span>  <span data-ttu-id="7dd6d-261">Pour y accéder, choisissez un cadre sous le menu **Cadres** de **l'outil Application.**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-261">To access it, choose a frame under the **Frames** menu in the **Application** tool.</span></span>  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Nouvelle vue détaillée d'un cadre dans le panneau Application" lightbox="../../media/2020/08/frame-details.msft.png":::
   <span data-ttu-id="7dd6d-263">Nouvelle vue détaillée d'une image dans **l'outil Application**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-263">New detailed view for a frame in **Application** tool</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-264">Problème de chrome : [#1093247][CR1093247]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-264">Chromium issue: [#1093247][CR1093247]</span></span>  

#### <a name="frame-details-for-opened-windows"></a><span data-ttu-id="7dd6d-265">Détails du cadre pour les fenêtres ouvertes</span><span class="sxs-lookup"><span data-stu-id="7dd6d-265">Frame details for opened windows</span></span>  

<span data-ttu-id="7dd6d-266">Les fenêtres ouvertes et les fenêtres pop-up s'affichent désormais également sous l'arborescence d'images.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-266">Open windows and pop-up windows now display under the frame tree as well.</span></span>  <span data-ttu-id="7dd6d-267">L'affichage détaillé des fenêtres ouvertes inclut des informations de sécurité supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-267">The detailed view of the opened windows includes additional security information.</span></span>  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Nouveau cadre en affichage détaillé pour les fenêtres ouvertes" lightbox="../../media/2020/08/window-opener.msft.png":::
   <span data-ttu-id="7dd6d-269">Nouveau cadre en affichage détaillé pour les fenêtres ouvertes</span><span class="sxs-lookup"><span data-stu-id="7dd6d-269">New frame detailed view for opened windows</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-270">Problème de chrome : [#1107766][CR1107766]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-270">Chromium issue: [#1107766][CR1107766]</span></span>  

#### <a name="security-and-isolation-information"></a><span data-ttu-id="7dd6d-271">Informations de sécurité et d'isolation</span><span class="sxs-lookup"><span data-stu-id="7dd6d-271">Security and isolation information</span></span>  

<span data-ttu-id="7dd6d-272">Le contexte sécurisé, la stratégie [COEP (Cross-Origin-Embedder-Policy)][WebDevCoopCoep]et la stratégie [DNS (Cross-Origin-Opener-Policy)][WebDevCoopCoep] sont désormais affichés dans les détails de l'image.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-272">Secure context, [Cross-Origin-Embedder-Policy (COEP)][WebDevCoopCoep], and [Cross-Origin-Opener-Policy (COOP)][WebDevCoopCoep] are now displayed in the frame details.</span></span>  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Informations de sécurité et d'isolation" lightbox="../../media/2020/08/coep-coop.msft.png":::
   <span data-ttu-id="7dd6d-274">Informations de sécurité et d'isolation</span><span class="sxs-lookup"><span data-stu-id="7dd6d-274">Security and isolation information</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-275">À l'avenir, l'équipe Microsoft Edge DevTools et l'équipe Chrome DevTools prévoient d'ajouter des informations de sécurité supplémentaires aux détails de l'image.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-275">In the future, the Microsoft Edge DevTools team and the Chrome DevTools team are planning to add more security information to the frame details.</span></span>  

<span data-ttu-id="7dd6d-276">Problème de chrome : [#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-276">Chromium issue: [#1051466][CR1051466]</span></span>  

### <a name="elements-and-network-panel-updates"></a><span data-ttu-id="7dd6d-277">Éléments et mises à jour du panneau réseau</span><span class="sxs-lookup"><span data-stu-id="7dd6d-277">Elements and Network panel updates</span></span>  

#### <a name="accessible-color-suggestion-in-the-styles-pane"></a><span data-ttu-id="7dd6d-278">Suggestion de couleur accessible dans le volet Styles</span><span class="sxs-lookup"><span data-stu-id="7dd6d-278">Accessible color suggestion in the Styles pane</span></span>  

<span data-ttu-id="7dd6d-279">DevTools fournit désormais des suggestions de couleur pour le texte à contraste faible.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-279">DevTools now provides color suggestions for low color contrast text.</span></span>  

<span data-ttu-id="7dd6d-280">Dans l'exemple ci-dessous, `h1` le texte est à faible contraste.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-280">In the example below, `h1` has low contrast text.</span></span>  <span data-ttu-id="7dd6d-281">Pour résoudre ce problème, ouvrez le s sélectionneur de couleurs de la `color` propriété dans le volet **Styles.**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-281">To fix it, open the color picker of the `color` property in the **Styles** pane.</span></span>  <span data-ttu-id="7dd6d-282">Après avoir développé la section **Coefficient de contraste,** DevTools fournit des suggestions de couleurs AA et AAA.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-282">After you expand the **Contrast ratio** section, DevTools provides AA and AAA color suggestions.</span></span>  <span data-ttu-id="7dd6d-283">Choisissez la couleur suggérée pour appliquer la couleur.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-283">Choose the suggested color to apply the color.</span></span>  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="Le s picker de couleur suggère des suggestions de couleurS AA et AAA" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   <span data-ttu-id="7dd6d-285">Le s picker de couleur suggère des suggestions de couleurS AA et AAA</span><span class="sxs-lookup"><span data-stu-id="7dd6d-285">Color picker suggests AA and AAA color suggestions</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-286">Problème de chrome : [#1093227][CR1093227]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-286">Chromium issue: [#1093227][CR1093227]</span></span>  

#### <a name="reinstate-properties-pane-in-the-elements-panel"></a><span data-ttu-id="7dd6d-287">Volet Propriétés rétablie dans le volet Éléments</span><span class="sxs-lookup"><span data-stu-id="7dd6d-287">Reinstate Properties pane in the Elements panel</span></span>  

<span data-ttu-id="7dd6d-288">Le **volet Propriétés** est de retour.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-288">The **Properties** pane is back.</span></span>  <span data-ttu-id="7dd6d-289">Il a [été supprimé dans Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span><span class="sxs-lookup"><span data-stu-id="7dd6d-289">It was [deprecated in Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span></span>  <span data-ttu-id="7dd6d-290">L'équipe Microsoft Edge DevTools et l'équipe Chrome DevTools planifient des améliorations pour l'inspection des propriétés des éléments.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-290">The Microsoft Edge DevTools team and the Chrome DevTools team are planning improvements for inspecting properties of elements.</span></span>  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Volet Propriétés du panneau Éléments" lightbox="../../media/2020/08/properties-pane.msft.png":::
   <span data-ttu-id="7dd6d-292">**Volet Propriétés** de **l'outil Éléments**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-292">**Properties** pane in the **Elements** tool</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-293">Problème de chrome :</span><span class="sxs-lookup"><span data-stu-id="7dd6d-293">Chromium issue:</span></span>  <!--  [#1105205][CR1105205],  -->  <span data-ttu-id="7dd6d-294">[#1116085] [CR1116085]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-294">[#1116085][CR1116085]</span></span>  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Human-readable `X-Client-Data` header values" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### <a name="autocomplete-custom-fonts-in-the-styles-pane"></a><span data-ttu-id="7dd6d-295">Autocomplete custom fonts in the Styles pane</span><span class="sxs-lookup"><span data-stu-id="7dd6d-295">Autocomplete custom fonts in the Styles pane</span></span>  

<span data-ttu-id="7dd6d-296">Les polices importées sont désormais ajoutées à la liste de lacompletion automatique CSS lors de la modification de la propriété dans le `font-family` **volet Styles.**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-296">Imported font faces are now added to the list of CSS autocompletion when editing the `font-family` property in the **Styles** pane.</span></span>  

<span data-ttu-id="7dd6d-297">Par exemple, si une police personnalisée est installée sur l'ordinateur local, elle s'affiche dans la liste d'achèvement `monospace` CSS.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-297">For example, if `monospace` is a custom font installed on the local machine, it displays in the CSS completion list.</span></span>  <span data-ttu-id="7dd6d-298">Dans les versions précédentes de Microsoft Edge, la police n'était pas affichée.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-298">In previous versions of Microsoft Edge, the font was not displayed.</span></span>

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Autocomplete custom fonts" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   <span data-ttu-id="7dd6d-300">Autocomplete custom fonts</span><span class="sxs-lookup"><span data-stu-id="7dd6d-300">Autocomplete custom fonts</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-301">Problème de chrome : [#1106221][CR1106221]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-301">Chromium issue: [#1106221][CR1106221]</span></span>  

#### <a name="consistently-display-resource-type-in-network-panel"></a><span data-ttu-id="7dd6d-302">Afficher systématiquement le type de ressource dans le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="7dd6d-302">Consistently display resource type in Network panel</span></span>  

<span data-ttu-id="7dd6d-303">DevTools affiche désormais de manière cohérente le même type de ressource que la demande réseau d'origine et s'affiche à la valeur de colonne Type lorsque la redirection \(code d'état `/ Redirect` HTTP 302\) se produit. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7dd6d-303">DevTools now consistently display the same resource type as the original network request and appends `/ Redirect` to the **Type** column value when redirection \(HTTP status code 302\) happens.</span></span>  

<span data-ttu-id="7dd6d-304">Auparavant, DevTools a parfois modifié le `Other` type.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-304">Previously DevTools changed the type to `Other` sometimes.</span></span>  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Afficher le type de ressource de redirection" lightbox="../../media/2020/08/network-redirect.msft.png":::
   <span data-ttu-id="7dd6d-306">Afficher le type de ressource de redirection</span><span class="sxs-lookup"><span data-stu-id="7dd6d-306">Display redirect resource type</span></span>  
:::image-end:::  

<span data-ttu-id="7dd6d-307">Problème de chrome : [#997694][CR997694]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-307">Chromium issue: [#997694][CR997694]</span></span>  

#### <a name="clear-buttons-in-the-elements-and-network-tools"></a><span data-ttu-id="7dd6d-308">Effacer les boutons dans les outils Éléments et réseau</span><span class="sxs-lookup"><span data-stu-id="7dd6d-308">Clear buttons in the Elements and Network tools</span></span>  

<span data-ttu-id="7dd6d-309">Les zones de texte suivantes ont désormais **des boutons** Effacer.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-309">The following text boxes now have **Clear** buttons.</span></span>  

*   <span data-ttu-id="7dd6d-310">Zones de texte de filtre dans le **volet Styles** et **l'outil** Réseau.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-310">The filter text boxes in the **Styles** pane and **Network** tool.</span></span>  
*   <span data-ttu-id="7dd6d-311">Zone de texte de recherche DOM dans **l'outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-311">The DOM search text box in the **Elements** tool.</span></span>  

<span data-ttu-id="7dd6d-312">Sélectionnez **le bouton** Effacer pour supprimer tout texte en entrée.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-312">Choose the **Clear** button to remove any inputted text.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Effacer les boutons des panneaux Éléments" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         <span data-ttu-id="7dd6d-314">Effacer les boutons dans les **outils Éléments**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-314">Clear buttons in the **Elements** tools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Effacer les boutons dans les panneaux Réseau" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         <span data-ttu-id="7dd6d-316">Effacer les boutons dans les  **outils** réseau</span><span class="sxs-lookup"><span data-stu-id="7dd6d-316">Clear buttons in the  **Network** tools</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="7dd6d-317">Problème de chrome : [#1067184][CR1067184]</span><span class="sxs-lookup"><span data-stu-id="7dd6d-317">Chromium issue: [#1067184][CR1067184]</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="7dd6d-318">Télécharger les canaux d’aperçu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7dd6d-318">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="7dd6d-319">Si vous utilisez Windows ou macOS, envisagez d'utiliser les canaux d'aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-319">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="7dd6d-320">Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-320">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="7dd6d-321">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7dd6d-321">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Icône Paramètres DevTools"  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Annulation du volet Propriétés dans le panneau Éléments - Nouveautés de DevTools (Microsoft Edge 84) | Documents Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Fonctionnalités de débogage de grille CSS - Nouveautés de DevTools (Microsoft Edge 85) | Documents Microsoft"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Émuler des appareils mobiles dans Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personnaliser les raccourcis clavier dans Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Activer les API expérimentales : fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Émulation : prise en charge du mode double écran - Fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Activer la visionneuse de commandes sources - Fonctionnalités expérimentales | Documents Microsoft"
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: https://review.docs.microsoft.com/microsoft-edge/devtools-guide-chromium/experimental-features?branch=user/zoghadya/dual-screen-experiment#emulation-support-dual-screen-mode "Émulation : prise en charge du mode double écran - Fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Test sur des appareils pliables et à double écran : fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activer les fonctions expérimentales – Fonctions expérimentales | Microsoft Docs"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "tableau - Référence de l'API de console | Documents Microsoft"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Recherchez du code JavaScript et CSS inutilisé avec l'onglet Couverture dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Caisse : personnaliser les paramètres DevTools de Microsoft Edge | Documents Microsoft"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analyser les performances de rendu avec l'onglet Rendu - Référence de l'analyse des performances | Documents Microsoft"  
[DevtoolsMediaPanelIndex]: /microsoft-edge/devtools-guide-chromium/media-panel/index "Afficher et déboguer les informations des joueurs multimédias | Documents Microsoft"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Utilisation de la jointure - Introduction aux appareils à double écran | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Fonctionnalité couvrant l’écran multimédia CSS pour la détection à double écran | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments pour appareils à double écran | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux de préversion de Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code "  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio clavier du code pour Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Le nouveau Surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools compte Twitter"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools : autoriser la personnalisation des raccourcis clavier/des liaisons de touches | Bogues Chromium"
[CR384968]: https://crbug.com/384968 "Option pour ignorer les polices locales () | Bogues Chromium"  
[CR772558]: https://crbug.com/772558 "DevTools : mise à jour vers la dernière version de | Bogues Chromium"  
[CR807440]: https://crbug.com/807440 "Chrome se verrouille avec un grand nombre de SW | Bogues Chromium"  
[CR997694]: https://crbug.com/997694 "Les demandes XHR avec l'état 302 ne sont pas affichées sous le filtre \"xhr\» dans le panneau réseau | Bogues Chromium"  
[CR1047356]: https://crbug.com/1047356 "Outils Grille CSS/Flexbox/Tableau | Bogues Chromium"  
[CR1051466]: https://crbug.com/1051466 "Prise en charge du débogage PUNAISE/COEP dans DevTools | Bogues Chromium"  
[CR1054281]: https://crbug.com/1054281 "Demande de fonctionnalité : DevTools doit émuler les appareils pliables et à double écran | Bogues Chromium"  
[CR1067184]: https://crbug.com/1067184 "Demande de fonctionnalité : effacer le bouton filtre sur les éléments & réseau - > filtre de style | Bogues Chromium"  
[CR1068116]: https://crbug.com/1068116 "☂ panneau d'expédition des problèmes | Bogues Chromium"  
[CR1080569]: https://crbug.com/1080569 "acorn ne prend pas en charge les opérateurs d'affectation logique | Bogues Chromium"  
[CR1080589]: https://crbug.com/1080589 "Classifier les problèmes par des tiers/des | Bogues Chromium"  
[CR1086817]: https://crbug.com/1086817 "acorn ne prend pas en charge les séparateurs numériques | Bogues Chromium"  
[CR1090802]: https://crbug.com/1090802 "Simuler les changements d'état d'inactivité à partir des api de détection d'inactivité | Bogues Chromium"  
[CR1093227]: https://crbug.com/1093227 "DevTools : suggérer les couleurs les plus proches accessibles | Bogues Chromium"  
[CR1093247]: https://crbug.com/1093247 "Afficher des informations sur les cadres dans le panneau d'| Bogues Chromium"  
[CR1094406]: https://crbug.com/1094406 "Les développeurs veulent une visionneuse de commande source pour AT https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools : prise en charge de l'émulation de la fonctionnalité multimédia « prefers-reduced-data | Bogues Chromium"  
[CR1096481]: https://crbug.com/1096481 "Problèmes de positionnement de bannières | Bogues Chromium"  
[CR1100253]: https://crbug.com/1100253 "Ajouter un raccourci de nœud de capture d'écran dans le menu context | Bogues Chromium"  
[CR1103316]: https://crbug.com/1103316 "La recherche d'éléments ne résout pasNode (mettre en surbrillon le texte, etc.) sur le premier résultat de | Bogues Chromium"  
[CR1103854]: https://crbug.com/1103854 "De-obfuscate X-Client-Data values in Developer Tools | Bogues Chromium"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
<span data-ttu-id="7dd6d-369">[CR1106221] : « Ajouter des polices importées à lacomplétion automatique de la famille de polices dans le panneau https://crbug.com/1106221 Styles | Bogues Chromium »</span><span class="sxs-lookup"><span data-stu-id="7dd6d-369">[CR1106221]: https://crbug.com/1106221 "Add imported fonts to the font-family autocompletion in the Styles panel | Chromium bugs"</span></span>  
<span data-ttu-id="7dd6d-370">[CR1107766] : « Afficher des informations sur les images générées par ' window.open() » dans l'arborescence https://crbug.com/1107766 d'images | Bogues Chromium »</span><span class="sxs-lookup"><span data-stu-id="7dd6d-370">[CR1107766]: https://crbug.com/1107766 "Display info about frames generated by 'window.open()' in frame tree | Chromium bugs"</span></span>  
<span data-ttu-id="7dd6d-371">[CR1115011] : « Lors de la copie d'un tableau à partir de la console, la structure de la table n'est pas https://crbug.com/1115011 conservée | Bogues Chromium »</span><span class="sxs-lookup"><span data-stu-id="7dd6d-371">[CR1115011]: https://crbug.com/1115011 "When copying a table from the console the structure of the table is not preserved | Chromium bugs"</span></span>  
<span data-ttu-id="7dd6d-372">[CR1116085] : « Veuillez retourner l'inspecteur de https://crbug.com/1116085 propriétés DevTools | Bogues Chromium »</span><span class="sxs-lookup"><span data-stu-id="7dd6d-372">[CR1116085]: https://crbug.com/1116085 "Please bring back the DevTools Properties inspector | Chromium bugs"</span></span>  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "prefers-reduced-data - Media Queries Level 5 | Brouillons de l'éditeur de groupe de travail CSS W3C"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v6.2.0 - GoogleChrome/| GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Mémoires tampons de protocole | Développeurs Google"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung États-Unis"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Affectation logique | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Séparateurs numériques | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Rendre votre site web \ « cross-origin isolated\ » à l'aide de LA TECHNOLOGIE | web.dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Détecter les utilisateurs inactifs avec l'API de détection d'inactivité | web.dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Évitez les animations non composites | web.dev"  

> [!NOTE]
> <span data-ttu-id="7dd6d-382">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7dd6d-382">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7dd6d-383">La page d’origine est disponible [ici](https://developer.chrome.com/blog/new-in-devtools-86) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)</span><span class="sxs-lookup"><span data-stu-id="7dd6d-383">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-86) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="7dd6d-385">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7dd6d-385">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
