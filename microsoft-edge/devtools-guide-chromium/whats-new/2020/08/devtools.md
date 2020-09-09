---
description: Faites correspondre les raccourcis clavier aux éléments Visual Studio, à l’émulation du pli en surface Duo et au Samsung Galaxy, ainsi qu’aux améliorations apportées aux grilles CSS
title: Nouveautés de DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 943eca7e73385513b264feb74ec37c450d5c5a2f
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "11004132"
---
# <span data-ttu-id="4ee22-104">Nouveautés de DevTools (Microsoft Edge 86)</span><span class="sxs-lookup"><span data-stu-id="4ee22-104">What's New In DevTools (Microsoft Edge 86)</span></span>  

## <span data-ttu-id="4ee22-105">Annonces de l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4ee22-105">Announcements from the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### <span data-ttu-id="4ee22-106">Faire correspondre des raccourcis clavier dans DevTools au code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4ee22-106">Match keyboard shortcuts in DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="4ee22-107">Dans Microsoft Edge 86, il est possible que les raccourcis clavier figurant dans le DevTools correspondent à vos raccourcis dans le [code Visual Studio][VisualStudioCode].</span><span class="sxs-lookup"><span data-stu-id="4ee22-107">In Microsoft Edge 86, you may match keyboard shortcuts in the DevTools to your shortcuts in [Visual Studio Code][VisualStudioCode].</span></span> 

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   <span data-ttu-id="4ee22-109">Faire correspondre les raccourcis clavier du DevTools au code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4ee22-109">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-110">Pour activer cette fonctionnalité, accédez à [personnaliser les raccourcis clavier dans Microsoft Edge devtools][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="4ee22-110">To activate this feature, navigate to [Customize keyboard shortcuts in the Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span></span>  

<span data-ttu-id="4ee22-111">Par exemple, le raccourci clavier pour suspendre ou continuer à exécuter un script dans le [code Visual Studio][VisualStudioCodeShortcutsKeyboardWindows] est `F5` .</span><span class="sxs-lookup"><span data-stu-id="4ee22-111">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="4ee22-112">Avec la valeur prédéfinie **devtools (par défaut)** , le même raccourci dans devtools est `F8` , mais lorsque vous choisissez le **code prédéfini Visual Studio** , ce raccourci est désormais également disponible `F5` .</span><span class="sxs-lookup"><span data-stu-id="4ee22-112">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8`, but when you choose the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="4ee22-113">[#174309][CR174309] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="4ee22-113">Chromium issue [#174309][CR174309]</span></span>  

### <span data-ttu-id="4ee22-114">Emulation surface Duo et Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="4ee22-114">Emulate Surface Duo and Samsung Galaxy Fold</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   <span data-ttu-id="4ee22-116">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="4ee22-116">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-117">Vous pouvez maintenant tester l’apparence de votre site Web ou de votre application sur deux nouveaux appareils:  [surface Duo][MicrosoftSurfaceDevicesDuo] et [Samsung Galaxy Fold][SamsungMobileGalaxyFold] dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4ee22-117">You are now able to test the look and feel of your website or app on two new devices:  [Surface Duo][MicrosoftSurfaceDevicesDuo] and [Samsung Galaxy Fold][SamsungMobileGalaxyFold] in Microsoft Edge.</span></span>  

<span data-ttu-id="4ee22-118">Pour vous aider à améliorer votre site Web ou votre application pour les appareils à double écran et pliant, utilisez les fonctionnalités suivantes lors de [l’émulation de l’appareil][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="4ee22-118">To help enhance your website or app for the dual-screen and foldable devices, use the following features when [emulating the device][DevtoolsDeviceModeIndex].</span></span>  

*   <span data-ttu-id="4ee22-119">[Fractionnées][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], c’est-à-dire lorsque votre site Web (ou l’application) s’affiche sur les deux écrans.</span><span class="sxs-lookup"><span data-stu-id="4ee22-119">[Spanning][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], which is when your website \(or app\) appears across both screens.</span></span>
*   <span data-ttu-id="4ee22-120">[Rendu de la couture][DualScreenIntroductionHowWorkSeam], qui est l’espace entre les deux écrans.</span><span class="sxs-lookup"><span data-stu-id="4ee22-120">[Rendering the seam][DualScreenIntroductionHowWorkSeam], which is the space between the two screens.</span></span>
*   <span data-ttu-id="4ee22-121">[Activation d’API de plateforme Web expérimentale][DevtoolsExperimentalFeaturesEnableExperimentalApis] pour accéder à la nouvelle [fonctionnalité d’affichage de contenu multimédia CSS][DualScreenWebCssMediaSpanning] et à l' [API getWindowSegments JavaScript][DualScreenWebJavascriptGetwindowsegments].</span><span class="sxs-lookup"><span data-stu-id="4ee22-121">[Enabling experimental Web Platform APIs][DevtoolsExperimentalFeaturesEnableExperimentalApis] to access the new [CSS media screen-spanning feature][DualScreenWebCssMediaSpanning] and [JavaScript getWindowSegments API][DualScreenWebJavascriptGetwindowsegments].</span></span>  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Émulation d’appareil pour le duo de surface" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   <span data-ttu-id="4ee22-123">Émulation d’appareil pour le duo de surface</span><span class="sxs-lookup"><span data-stu-id="4ee22-123">Device emulation for Surface Duo</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-124">Pour activer cette fonctionnalité expérimentale, naviguez jusqu’à [activation des fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] , puis cochez la case en regard de **émulation: prise en charge du mode double écran**.</span><span class="sxs-lookup"><span data-stu-id="4ee22-124">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Emulation: Support dual screen mode**.</span></span>  

<span data-ttu-id="4ee22-125">Pour plus d’informations sur cette expérience, accédez à [émulation: prise en charge du mode double écran][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].</span><span class="sxs-lookup"><span data-stu-id="4ee22-125">For more information about this experiment, navigate to [Emulation: Support dual screen mode][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].</span></span>  

<span data-ttu-id="4ee22-126">Problème de chrome: [#1054281][CR1054281]</span><span class="sxs-lookup"><span data-stu-id="4ee22-126">Chromium issue: [#1054281][CR1054281]</span></span>  

### <span data-ttu-id="4ee22-127">Améliorations de la superposition de grille CSS et nouvelles fonctionnalités de grille expérimentale</span><span class="sxs-lookup"><span data-stu-id="4ee22-127">CSS grid overlay improvements and new experimental grid features</span></span>  

<span data-ttu-id="4ee22-128">Nous vous remercions des commentaires positifs relatifs aux superpositions de grille CSS améliorées.</span><span class="sxs-lookup"><span data-stu-id="4ee22-128">Thank you for the positive feedback about the improved CSS grid overlays.</span></span>  <span data-ttu-id="4ee22-129">Les superpositions de grille CSS sont désormais activées par défaut et ne nécessitent pas d’activation d’une expérience.</span><span class="sxs-lookup"><span data-stu-id="4ee22-129">The CSS grid overlays are now enabled by default and do not require you to turn on an experiment.</span></span>  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Superposition de grille CSS pour l’élément article" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   <span data-ttu-id="4ee22-131">Superposition de grille CSS pour un `article` élément</span><span class="sxs-lookup"><span data-stu-id="4ee22-131">CSS grid overlay for `article` element</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="4ee22-132">Pour plus d’informations sur les superpositions de grille, voir [fonctionnalités de débogage de grille CSS][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].</span><span class="sxs-lookup"><span data-stu-id="4ee22-132">For more information about grid overlays, go to [CSS grid debugging features][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="4ee22-133">L’équipe Microsoft Edge DevTools et l’équipe chrome DevTools collaborent sur des fonctionnalités supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4ee22-133">The Microsoft Edge DevTools team and the Chrome DevTools team collaborate on additional features.</span></span>  <span data-ttu-id="4ee22-134">Les nouvelles fonctionnalités incluent plusieurs superpositions qui sont permanentes et configurables à partir d’un nouveau volet de **disposition** dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="4ee22-134">The new features include multiple overlays that are persistent and configurable from a new **Layout** pane on the **Elements** panel.</span></span>  

<span data-ttu-id="4ee22-135">Pour activer cette fonctionnalité expérimentale, accédez à [activer les fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] , puis activez la case à cocher en regard de **activer les nouvelles fonctionnalités de débogage de grille CSS (options de configuration disponibles dans le volet barre latérale des éléments après redémarrage)**.</span><span class="sxs-lookup"><span data-stu-id="4ee22-135">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable new CSS Grid debugging features (configuration options available in Layout sidebar pane in Elements after restart)**.</span></span>  

<span data-ttu-id="4ee22-136">Pour plus d’informations sur cette expérience, accédez aux [nouvelles fonctionnalités de débogage de grille CSS][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].</span><span class="sxs-lookup"><span data-stu-id="4ee22-136">For more information about this experiment, navigate to [Enable new CSS grid debugging features][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="4ee22-137">Problème de chrome: [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="4ee22-137">Chromium issue: [#1047356][CR1047356]</span></span>  

### <span data-ttu-id="4ee22-138">Le tableau copié à partir de la console conserve la mise en forme</span><span class="sxs-lookup"><span data-stu-id="4ee22-138">Table copied from the Console preserves formatting</span></span>  

<span data-ttu-id="4ee22-139">Dans Microsoft Edge 85 ou version antérieure, la mise en forme d’un copié `console.table` a été perdue.</span><span class="sxs-lookup"><span data-stu-id="4ee22-139">In Microsoft Edge 85 or earlier, the formatting of a copied `console.table` was lost.</span></span>  <span data-ttu-id="4ee22-140">Si vous avez copié la sortie de l’API de la console [table][DevtoolsConsoleApiTable] et collé celle-ci, seul le texte du tableau a été conservé.</span><span class="sxs-lookup"><span data-stu-id="4ee22-140">If you copied the output from the [table][DevtoolsConsoleApiTable] Console API, and pasted it, only the text of the table was kept.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="sortie de l’API de table table dans Microsoft Edge 85 ou version antérieure" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` <span data-ttu-id="4ee22-142">Sortie de l’API de console dans Microsoft Edge 85 ou version antérieure</span><span class="sxs-lookup"><span data-stu-id="4ee22-142">Console API output in Microsoft Edge 85 or earlier</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="sortie de l’API de la console de tableau de Microsoft Edge 85 ou antérieure collée dans le code Visual Studio" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="4ee22-144">Sortie de l’API de console de Microsoft Edge 85 ou antérieure collée dans le code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4ee22-144">Console API output from Microsoft Edge 85 or earlier pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="4ee22-145">Dans Microsoft Edge 86 ou version ultérieure, lorsque vous copiez une table à partir de la **console**, la mise en forme est désormais préservée.</span><span class="sxs-lookup"><span data-stu-id="4ee22-145">In Microsoft Edge 86 or later, when you copy a table from the **Console**, the formatting is now preserved.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="sortie de l’API de table table dans Microsoft Edge 86 ou version ultérieure" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` <span data-ttu-id="4ee22-147">Sortie de l’API de console dans Microsoft Edge 86 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="4ee22-147">Console API output in Microsoft Edge 86 or later</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="sortie de l’API de table table de Microsoft Edge 86 ou version ultérieure collée dans le code Visual Studio" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="4ee22-149">Sortie de l’API de console de Microsoft Edge 86 ou version ultérieure collée dans le code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4ee22-149">Console API output from Microsoft Edge 86 or later pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="4ee22-150">Problème de chrome: [#1115011] [CR1115011]</span><span class="sxs-lookup"><span data-stu-id="4ee22-150">Chromium issue: [#1115011][CR1115011]</span></span>  

### <span data-ttu-id="4ee22-151">Visionneuse de commandes sources pour faciliter les tests d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="4ee22-151">Source Order Viewer for easier accessibility testing</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   <span data-ttu-id="4ee22-153">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="4ee22-153">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-154">Le nouveau programme d’assistance d’accessibilité affiche l’ordre des éléments dans la source.</span><span class="sxs-lookup"><span data-stu-id="4ee22-154">The new accessibility helper displays the order of elements in the source.</span></span>  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Activer l’ordre d’affichage des sources" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   <span data-ttu-id="4ee22-156">Activer l' **ordre d’affichage des sources**</span><span class="sxs-lookup"><span data-stu-id="4ee22-156">Activate **Show source order**</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-157">Cette fonctionnalité permet de tester plus facilement la façon dont les utilisateurs du lecteur d’écran et du clavier connaissent votre site Web ou votre application.</span><span class="sxs-lookup"><span data-stu-id="4ee22-157">This feature makes it easier to test the way screen reader and keyboard users experience your website or app.</span></span>  <span data-ttu-id="4ee22-158">Les lecteurs d’écran et la navigation au clavier dépendent du contenu placé dans un ordre particulier dans le code source de votre site Web ou de votre application, de manière à ce qu’il corresponde à la page rendue.</span><span class="sxs-lookup"><span data-stu-id="4ee22-158">Screen readers and keyboard navigation depend on content being placed in a particular order in the source code of your website or app, so that it matches the rendered page.</span></span>  <span data-ttu-id="4ee22-159">La visionneuse de commandes source affiche des différences potentielles dans l’ordre entre la page affichée et le code source.</span><span class="sxs-lookup"><span data-stu-id="4ee22-159">The Source Order Viewer displays potential differences in order between the rendered page and the source code.</span></span>  

<span data-ttu-id="4ee22-160">Pour activer cette fonctionnalité expérimentale, accédez à l’option Activer les [fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] , puis activez la case à cocher en regard de **activer la visionneuse de commandes sources**.</span><span class="sxs-lookup"><span data-stu-id="4ee22-160">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Source Order Viewer**.</span></span>  

<span data-ttu-id="4ee22-161">Pour plus d’informations sur cette expérience, naviguez jusqu’à [activer la visionneuse de commandes sources][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].</span><span class="sxs-lookup"><span data-stu-id="4ee22-161">For more information about this experiment, navigate to [Enable Source Order Viewer][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].</span></span>  

<span data-ttu-id="4ee22-162">Problème de chrome: [#1094406][CR1094406]</span><span class="sxs-lookup"><span data-stu-id="4ee22-162">Chromium issue: [#1094406][CR1094406]</span></span>  

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

### <span data-ttu-id="4ee22-163">Sélectionner tous les résultats de recherche dans l’outil éléments</span><span class="sxs-lookup"><span data-stu-id="4ee22-163">Highlight all search results in Elements tool</span></span>  

<span data-ttu-id="4ee22-164">Dans Microsoft Edge 84 et 85, le premier résultat de recherche dans le panneau **éléments** n’a pas été mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="4ee22-164">In Microsoft Edge 84 and 85, the first search result in the **Elements** panel did not highlight.</span></span>  <span data-ttu-id="4ee22-165">Les résultats de recherche restants ont été correctement mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="4ee22-165">The remaining search results were highlighted correctly.</span></span>  

<span data-ttu-id="4ee22-166">Nous vous remercions d’avoir envoyé vos commentaires et de nous aider à améliorer le chrome.</span><span class="sxs-lookup"><span data-stu-id="4ee22-166">Thank you for sending your feedback and helping improve Chromium.</span></span>  <span data-ttu-id="4ee22-167">Votre commentaire n’a pas été détecté [#1103316][CR1103316] dans le projet de chrome Open-source.</span><span class="sxs-lookup"><span data-stu-id="4ee22-167">Your feedback uncovered Issue [#1103316][CR1103316] in the open-source Chromium project.</span></span>  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Premiers résultats de recherche du panneau éléments dans Microsoft Edge 84 ou version ultérieure" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   <span data-ttu-id="4ee22-169">Premiers résultats de recherche du panneau **éléments** dans Microsoft Edge 84 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="4ee22-169">Highlighted first search result on **Elements** panel in Microsoft Edge 84 or later</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-170">Le problème est désormais résolu dans toutes les versions de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4ee22-170">The issue is now fixed in all versions of Microsoft Edge.</span></span>  

<span data-ttu-id="4ee22-171">Problème de chrome: [#1103316][CR1103316]</span><span class="sxs-lookup"><span data-stu-id="4ee22-171">Chromium issue: [#1103316][CR1103316]</span></span>  

## <span data-ttu-id="4ee22-172">Annonces du projet de chrome</span><span class="sxs-lookup"><span data-stu-id="4ee22-172">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="4ee22-173">Nouvelle fenêtre multimédia</span><span class="sxs-lookup"><span data-stu-id="4ee22-173">New Media panel</span></span>  

<span data-ttu-id="4ee22-174">DevTools affiche désormais les informations sur les lecteurs multimédias dans le panneau [média][DevtoolsMediaIndex] .</span><span class="sxs-lookup"><span data-stu-id="4ee22-174">DevTools now displays media players information in the [Media][DevtoolsMediaIndex] panel.</span></span>  

<span data-ttu-id="4ee22-175">Pour ouvrir le nouveau panneau **multimédia** , exécutez l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="4ee22-175">To open the new **Media** panel, complete the following step.</span></span>  

1.  <span data-ttu-id="4ee22-176">Sélectionnez **personnaliser et contrôler devtools** \ ( `...` \) > **plus d’outils**  >  **multimédia**.</span><span class="sxs-lookup"><span data-stu-id="4ee22-176">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Nouvelle fenêtre multimédia" lightbox="../../media/2020/08/media-panel.msft.png":::
       <span data-ttu-id="4ee22-178">Nouvelle fenêtre **multimédia**</span><span class="sxs-lookup"><span data-stu-id="4ee22-178">New **Media** panel</span></span>  
    :::image-end:::  

<span data-ttu-id="4ee22-179">Avant le nouveau panneau **multimédia** dans devtools, les informations de journalisation et de débogage relatives aux lecteurs vidéo se trouvent sous le paramètre **lecteurs récents** .</span><span class="sxs-lookup"><span data-stu-id="4ee22-179">Before the new **Media** panel in DevTools, the logging and debug information about video players was located under the **Recent Players** setting.</span></span>  <span data-ttu-id="4ee22-180">Pour ouvrir le paramètre **lecteurs récents** , accédez à `edge://media-internals` l’onglet **adversaires** et sélectionnez l’onglet adversaires.</span><span class="sxs-lookup"><span data-stu-id="4ee22-180">To open the **Recent Players** setting, go to `edge://media-internals` and choose the **Players** tab.</span></span>  

<span data-ttu-id="4ee22-181">Affichez le contenu en direct et examinez les problèmes potentiels plus rapidement, en incluant les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="4ee22-181">View live content and inspect potential issues more quickly, including the following examples.</span></span>  

*   <span data-ttu-id="4ee22-182">Pourquoi les images sont-elles supprimées?</span><span class="sxs-lookup"><span data-stu-id="4ee22-182">Why frames are dropped?</span></span>  
*   <span data-ttu-id="4ee22-183">Pourquoi JavaScript interagit-il avec le joueur d’une manière inattendue?</span><span class="sxs-lookup"><span data-stu-id="4ee22-183">Why JavaScript is interacting with the player in an unexpected way?</span></span>  

### <span data-ttu-id="4ee22-184">Capture d’écran de nœud à l’aide du menu contextuel du panneau éléments</span><span class="sxs-lookup"><span data-stu-id="4ee22-184">Capture node screenshots using the Elements panel context menu</span></span>  

<span data-ttu-id="4ee22-185">Vous pouvez désormais capturer les captures d’écran de nœud à l’aide du menu contextuel dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="4ee22-185">You may now capture node screenshots using the context menu in the **Elements** panel.</span></span>  

<span data-ttu-id="4ee22-186">Par exemple, pour prendre une capture d’écran de la table des matières, pointez sur l’élément, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **capturer le nœud de capture**.</span><span class="sxs-lookup"><span data-stu-id="4ee22-186">For example, to take a screenshot of the table of contents, hover on the element, open the contextual menu \(right-click\), and select **Capture node screenshot**.</span></span>  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Capture d’écran de nœuds" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   <span data-ttu-id="4ee22-188">Capture d’écran de nœuds</span><span class="sxs-lookup"><span data-stu-id="4ee22-188">Capture node screenshots</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-189">Problème de chrome: [#1100253][CR1100253]</span><span class="sxs-lookup"><span data-stu-id="4ee22-189">Chromium issue: [#1100253][CR1100253]</span></span>  

### <span data-ttu-id="4ee22-190">Mises à jour de l’outil de sortie</span><span class="sxs-lookup"><span data-stu-id="4ee22-190">Issues tool updates</span></span>  

<span data-ttu-id="4ee22-191">La barre d’avertissement problèmes du panneau de la **console** est désormais remplacée par un message normal.</span><span class="sxs-lookup"><span data-stu-id="4ee22-191">The Issues warning bar on the **Console** panel is now replaced with a regular message.</span></span>  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Problèmes dans le message de la console" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   <span data-ttu-id="4ee22-193">Problèmes dans le message de la console</span><span class="sxs-lookup"><span data-stu-id="4ee22-193">Issues in console message</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-194">Les problèmes de cookie tiers sont désormais cachés par défaut dans l’outil **problèmes** .</span><span class="sxs-lookup"><span data-stu-id="4ee22-194">Third-party cookie issues are now hidden by default in the **Issues** tool.</span></span>  <span data-ttu-id="4ee22-195">Activez la nouvelle case à cocher **inclure les problèmes de cookie tiers** pour afficher les problèmes.</span><span class="sxs-lookup"><span data-stu-id="4ee22-195">Enable the new **Include third-party cookie issues** checkbox to view the issues.</span></span>  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="case à cocher problèmes de cookie tiers" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   <span data-ttu-id="4ee22-197">case à cocher problèmes de cookie tiers</span><span class="sxs-lookup"><span data-stu-id="4ee22-197">third-party cookie issues checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-198">Problèmes de chrome: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span><span class="sxs-lookup"><span data-stu-id="4ee22-198">Chromium issues: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span></span>  

### <span data-ttu-id="4ee22-199">Émuler des polices locales manquantes</span><span class="sxs-lookup"><span data-stu-id="4ee22-199">Emulate missing local fonts</span></span>  

<span data-ttu-id="4ee22-200">Ouvrez l' [outil de rendu][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] et utilisez la nouvelle fonctionnalité **Désactiver les polices locales** pour émuler les sources manquantes `local()` dans les `@font-face` règles.</span><span class="sxs-lookup"><span data-stu-id="4ee22-200">Open the [Rendering tool][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] and use the new **Disable local fonts** feature to emulate missing `local()` sources in `@font-face` rules.</span></span>  

<span data-ttu-id="4ee22-201">Par exemple, lorsque la `Rubik` police est installée sur votre appareil et qu' `@font-face src` elle l’utilise comme `local()` police, Microsoft Edge utilise le fichier de police local de votre appareil.</span><span class="sxs-lookup"><span data-stu-id="4ee22-201">For example, when the `Rubik` font is installed on your device and the `@font-face src` rule uses it as a `local()` font, Microsoft Edge uses the local font file from your device.</span></span>  

<span data-ttu-id="4ee22-202">Lorsque l’option **Désactiver les polices locales** est activée, devtools ignore les `local()` polices et récupère chacune du réseau.</span><span class="sxs-lookup"><span data-stu-id="4ee22-202">When **Disable local fonts** is enabled, DevTools ignores the `local()` fonts and fetches each from the network.</span></span>  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Émuler des polices locales manquantes" lightbox="../../media/2020/08/disable-font.msft.png":::
   <span data-ttu-id="4ee22-204">Émuler des polices locales manquantes</span><span class="sxs-lookup"><span data-stu-id="4ee22-204">Emulate missing local fonts</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-205">Si vous utilisez deux copies différentes de la même police lors du développement, comme dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="4ee22-205">If you use two different copies of the same font during development, such as the following examples.</span></span>  

*   <span data-ttu-id="4ee22-206">Police locale pour vos outils de conception.</span><span class="sxs-lookup"><span data-stu-id="4ee22-206">A local font for your design tools.</span></span>  
*   <span data-ttu-id="4ee22-207">Une police Web pour votre code.</span><span class="sxs-lookup"><span data-stu-id="4ee22-207">A web font for your code.</span></span>  

<span data-ttu-id="4ee22-208">Utilisez **Désactiver les polices locales** pour faciliter l’accomplissement des tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="4ee22-208">Use **Disable local fonts** to make it easier for you to complete the following tasks.</span></span>  

*   <span data-ttu-id="4ee22-209">Déboguer et mesurer les performances de chargement et l’optimisation des polices Web.</span><span class="sxs-lookup"><span data-stu-id="4ee22-209">Debug and measure loading performance and optimization of web fonts.</span></span>  
*   <span data-ttu-id="4ee22-210">Vérifiez la précision de vos `@font-face` règles CSS.</span><span class="sxs-lookup"><span data-stu-id="4ee22-210">Verify accuracy of your CSS `@font-face` rules.</span></span>  
*   <span data-ttu-id="4ee22-211">Découvrez les différences entre les versions locales installées sur votre appareil et une police Web.</span><span class="sxs-lookup"><span data-stu-id="4ee22-211">Discover differences between local versions installed on your device and a web font.</span></span>  

<span data-ttu-id="4ee22-212">Problème de chrome: [#384968][CR384968]</span><span class="sxs-lookup"><span data-stu-id="4ee22-212">Chromium issue: [#384968][CR384968]</span></span>  

### <span data-ttu-id="4ee22-213">Émuler des utilisateurs inactifs</span><span class="sxs-lookup"><span data-stu-id="4ee22-213">Emulate inactive users</span></span>  

<span data-ttu-id="4ee22-214">L' [API de détection de veille][WebDevIdleDetection] permet aux développeurs de détecter les utilisateurs inactifs et de réagir aux changements d’État inactifs.</span><span class="sxs-lookup"><span data-stu-id="4ee22-214">The [Idle Detection API][WebDevIdleDetection] allows developers to detect inactive users and react on idle state changes.</span></span>  <span data-ttu-id="4ee22-215">Vous pouvez maintenant utiliser DevTools pour émuler les changements d’état inactif dans l’outil **capteurs** pour l’état de l’utilisateur et l’état de l’écran, au lieu d’attendre que l’état d’inactivité réelle change.</span><span class="sxs-lookup"><span data-stu-id="4ee22-215">You are now able to use DevTools to emulate idle state changes in the **Sensors** tool for both the user state and the screen state instead of waiting for the actual idle state to change.</span></span>  <span data-ttu-id="4ee22-216">Vous pouvez ouvrir l’outil **capteurs** à partir du [tiroir][DevtoolsCustomizeIndexDrawer].</span><span class="sxs-lookup"><span data-stu-id="4ee22-216">You may open the **Sensors** tool from the [Drawer][DevtoolsCustomizeIndexDrawer].</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Émuler des utilisateurs inactifs" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   <span data-ttu-id="4ee22-218">Émuler des utilisateurs inactifs</span><span class="sxs-lookup"><span data-stu-id="4ee22-218">Emulate inactive users</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-219">Problème de chrome: [#1090802][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="4ee22-219">Chromium issue: [#1090802][CR1090802]</span></span>  

### <span data-ttu-id="4ee22-220">Imitez les préférences-Reduced-Data</span><span class="sxs-lookup"><span data-stu-id="4ee22-220">Emulate prefers-reduced-data</span></span>  

> [!NOTE]
> <span data-ttu-id="4ee22-221">Dans le 86 de Microsoft Edge, pour activer cette fonctionnalité, accédez à `edge://flags#enable-experimental-web-platform-features` l’indicateur **features sur les fonctionnalités de plateforme Web expérimentale** et activez-le.</span><span class="sxs-lookup"><span data-stu-id="4ee22-221">In Microsoft Edge 86, to enable this feature, go to `edge://flags#enable-experimental-web-platform-features` and turn on the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="4ee22-222">L’option d’émulation est uniquement affichée si l’indicateur est activé.</span><span class="sxs-lookup"><span data-stu-id="4ee22-222">The emulation option is only displayed if the flag is enabled.</span></span>  

<span data-ttu-id="4ee22-223">La requête Media [-Reduced-Data][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] détecte les préférences de contenu utilisateur pour réduire les données.</span><span class="sxs-lookup"><span data-stu-id="4ee22-223">The [prefers-reduced-data][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] media query detects user content preferences for reduced data.</span></span>  <span data-ttu-id="4ee22-224">Si cette option est sélectionnée, l’utilisateur reçoit du contenu de page alternatif qui utilise moins de données.</span><span class="sxs-lookup"><span data-stu-id="4ee22-224">If selected, the user receives alternate page content that uses less data.</span></span>  

<span data-ttu-id="4ee22-225">Vous pouvez maintenant utiliser DevTools pour émuler la `prefers-reduced-data` requête multimédia.</span><span class="sxs-lookup"><span data-stu-id="4ee22-225">You may now use DevTools to emulate the `prefers-reduced-data` media query.</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Imitez les préférences-Reduced-Data" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   <span data-ttu-id="4ee22-227">Imitez les préférences-Reduced-Data</span><span class="sxs-lookup"><span data-stu-id="4ee22-227">Emulate prefers-reduced-data</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-228">Problème de chrome: [#1096068][CR1096068]</span><span class="sxs-lookup"><span data-stu-id="4ee22-228">Chromium issue: [#1096068][CR1096068]</span></span>  

### <span data-ttu-id="4ee22-229">Prise en charge des nouvelles fonctionnalités JavaScript</span><span class="sxs-lookup"><span data-stu-id="4ee22-229">Support for new JavaScript features</span></span>  

<span data-ttu-id="4ee22-230">DevTools ont désormais une meilleure prise en charge des fonctionnalités de langage JavaScript suivantes.</span><span class="sxs-lookup"><span data-stu-id="4ee22-230">DevTools now have better supported the following JavaScript language features.</span></span>  

| <span data-ttu-id="4ee22-231">Fonctionnalité de langage JavaScript</span><span class="sxs-lookup"><span data-stu-id="4ee22-231">JavaScript language feature</span></span> | <span data-ttu-id="4ee22-232">Détails</span><span class="sxs-lookup"><span data-stu-id="4ee22-232">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="4ee22-233">Opérateurs d’affectation logique</span><span class="sxs-lookup"><span data-stu-id="4ee22-233">Logical assignment operators</span></span>][V8FeaturesLogicalAssignment] | <span data-ttu-id="4ee22-234">DevTools prend désormais en charge l’affectation logique avec les opérateurs nouveau et `&&=` `||=` et `??=` dans les panneaux **console** et **sources** .</span><span class="sxs-lookup"><span data-stu-id="4ee22-234">DevTools now supports logical assignment with the new `&&=`, `||=`, and `??=` operators in the **Console** and **Sources** panels.</span></span>  |  
| <span data-ttu-id="4ee22-235">[Séparateur numérique][V8FeaturesNumericSeparators] à imprimer</span><span class="sxs-lookup"><span data-stu-id="4ee22-235">Pretty-print [numeric separators][V8FeaturesNumericSeparators]</span></span> | <span data-ttu-id="4ee22-236">DevTools est désormais correctement à l’impression des séparateurs numériques dans le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="4ee22-236">DevTools now properly pretty-prints the numeric separators in the **Sources** panel.</span></span>  |  

<span data-ttu-id="4ee22-237">Problèmes de chrome: [1086817][CR1086817], [1080569][CR1080569]</span><span class="sxs-lookup"><span data-stu-id="4ee22-237">Chromium issues: [1086817][CR1086817], [1080569][CR1080569]</span></span>  

### <span data-ttu-id="4ee22-238">Panneau de signalisation 6,2</span><span class="sxs-lookup"><span data-stu-id="4ee22-238">Lighthouse 6.2 in the Lighthouse panel</span></span>  

<span data-ttu-id="4ee22-239">Le panneau de signalisation est désormais exécuté sur le panneau de **signalisation** 6,2.</span><span class="sxs-lookup"><span data-stu-id="4ee22-239">The **Lighthouse** panel is now running Lighthouse 6.2.</span></span>  <span data-ttu-id="4ee22-240">Pour obtenir la liste complète des modifications, accédez aux [notes de publication][GithubGooglechromeLighthouseV620]de votre phare.</span><span class="sxs-lookup"><span data-stu-id="4ee22-240">For a full list of changes, go to the [Lighthouse release notes][GithubGooglechromeLighthouseV620].</span></span>  

<span data-ttu-id="4ee22-241">Problème de chrome: [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="4ee22-241">Chromium issue: [#772558][CR772558]</span></span>  

### <span data-ttu-id="4ee22-242">Dépréciation du Listing Other origines dans le volet travailleurs de services</span><span class="sxs-lookup"><span data-stu-id="4ee22-242">Deprecation of other origins listing in the Service Workers pane</span></span>  

<span data-ttu-id="4ee22-243">DevTools propose désormais un lien dans le volet **travailleurs de services** \ (panneau d'**application** > volet des travailleurs de **service** ) pour afficher la liste complète des travailleurs de services d’autres origines.</span><span class="sxs-lookup"><span data-stu-id="4ee22-243">DevTools now provides a link from the **Service workers** pane \(**Application** panel > **Service workers** pane\) to view the full list of service workers from other origins.</span></span>  <span data-ttu-id="4ee22-244">Pour accéder à la liste sans ouvrir le DevTools, accédez à `edge://service-worker-internals/?devtools` .</span><span class="sxs-lookup"><span data-stu-id="4ee22-244">To access the list without opening the DevTools, go to `edge://service-worker-internals/?devtools`.</span></span>  

<span data-ttu-id="4ee22-245">Auparavant DevTools afficher une liste imbriquée dans le volet de l' **Application** > volet **travailleurs du service** .</span><span class="sxs-lookup"><span data-stu-id="4ee22-245">Previously DevTools displayed a list nested under the **Application** panel > **Service workers** pane.</span></span>  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Créer un lien vers d’autres origines" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   <span data-ttu-id="4ee22-247">Créer un lien vers d’autres origines</span><span class="sxs-lookup"><span data-stu-id="4ee22-247">Link to other origins</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-248">Problème de chrome: [#807440][CR807440]</span><span class="sxs-lookup"><span data-stu-id="4ee22-248">Chromium issue: [#807440][CR807440]</span></span>  

### <span data-ttu-id="4ee22-249">Afficher le résumé de couverture des éléments filtrés</span><span class="sxs-lookup"><span data-stu-id="4ee22-249">Show coverage summary for filtered items</span></span>  

<span data-ttu-id="4ee22-250">DevTools désormais recalculer et afficher une synthèse dynamique des informations de couverture.</span><span class="sxs-lookup"><span data-stu-id="4ee22-250">DevTools now recalculate and display a summary of coverage information dynamically.</span></span>  <span data-ttu-id="4ee22-251">L’affichage dynamique est déclenché lorsque des filtres sont appliqués dans l’outil de [couverture][DevtoolsCoverageIndex] .</span><span class="sxs-lookup"><span data-stu-id="4ee22-251">The dynamic display is triggered when filters are applied in the [Coverage][DevtoolsCoverageIndex] tool.</span></span>  <span data-ttu-id="4ee22-252">Pour que l’outil de **couverture** affiche toujours un résumé de toutes les informations de couverture.</span><span class="sxs-lookup"><span data-stu-id="4ee22-252">Before the **Coverage** tool always displayed a summary of all coverage information.</span></span>  

<span data-ttu-id="4ee22-253">Dans la première des illustrations suivantes, le résumé s’affiche initialement `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` et dans les deux figures suivantes, le résumé s’affiche `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` lorsque le filtrage CSS est appliqué.</span><span class="sxs-lookup"><span data-stu-id="4ee22-253">In the first of the following figures, the summary initially displays `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` and in the second of the following figures, the summary displays `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` after CSS filtering is applied.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Résumé de couverture" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         <span data-ttu-id="4ee22-255">Résumé de couverture</span><span class="sxs-lookup"><span data-stu-id="4ee22-255">Coverage summary</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Résumé de couverture des éléments filtrés" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         <span data-ttu-id="4ee22-257">Résumé de couverture des éléments filtrés</span><span class="sxs-lookup"><span data-stu-id="4ee22-257">Coverage summary for filtered items</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="4ee22-258">Problème de chrome: [#1061385][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="4ee22-258">Chromium issue: [#1061385][CR1090802]</span></span>  

### <span data-ttu-id="4ee22-259">Nouvelle vue Détails du cadre dans le panneau application</span><span class="sxs-lookup"><span data-stu-id="4ee22-259">New frame details view in Application panel</span></span>  

<span data-ttu-id="4ee22-260">DevTools affiche désormais une vue détaillée pour chaque image.</span><span class="sxs-lookup"><span data-stu-id="4ee22-260">DevTools now show a detailed view for each frame.</span></span>  <span data-ttu-id="4ee22-261">Pour y accéder, sélectionnez un cadre sous le menu **cadres** dans le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="4ee22-261">To access it, choose a frame under the **Frames** menu in the **Application** panel.</span></span>  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Nouvelle vue détaillée d’une image dans le panneau application" lightbox="../../media/2020/08/frame-details.msft.png":::
   <span data-ttu-id="4ee22-263">Nouvelle vue détaillée d’une image dans le panneau **application**</span><span class="sxs-lookup"><span data-stu-id="4ee22-263">New detailed view for a frame in **Application** panel</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-264">Problème de chrome: [#1093247][CR1093247]</span><span class="sxs-lookup"><span data-stu-id="4ee22-264">Chromium issue: [#1093247][CR1093247]</span></span>  

#### <span data-ttu-id="4ee22-265">Détails du cadre pour les fenêtres ouvertes</span><span class="sxs-lookup"><span data-stu-id="4ee22-265">Frame details for opened windows</span></span>  

<span data-ttu-id="4ee22-266">Les fenêtres et fenêtres contextuelles ouvertes s’affichent désormais sous l’arborescence de trames.</span><span class="sxs-lookup"><span data-stu-id="4ee22-266">Open windows and pop-up windows now display under the frame tree as well.</span></span>  <span data-ttu-id="4ee22-267">Le mode d’affichage détaillé des fenêtres ouvertes inclut des informations supplémentaires sur la sécurité.</span><span class="sxs-lookup"><span data-stu-id="4ee22-267">The detailed view of the opened windows includes additional security information.</span></span>  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Nouvelle vue détaillée du cadre pour les fenêtres ouvertes" lightbox="../../media/2020/08/window-opener.msft.png":::
   <span data-ttu-id="4ee22-269">Nouvelle vue détaillée du cadre pour les fenêtres ouvertes</span><span class="sxs-lookup"><span data-stu-id="4ee22-269">New frame detailed view for opened windows</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-270">Problème de chrome: [#1107766] [CR1107766]</span><span class="sxs-lookup"><span data-stu-id="4ee22-270">Chromium issue: [#1107766][CR1107766]</span></span>  

#### <span data-ttu-id="4ee22-271">Informations de sécurité et d’isolement</span><span class="sxs-lookup"><span data-stu-id="4ee22-271">Security and isolation information</span></span>  

<span data-ttu-id="4ee22-272">Context sécurisée, [Cross-Origin-Integration-Policy (COEP)][WebDevCoopCoep]et [Cross-Origin-Open-Policy (Coop)][WebDevCoopCoep] s’affichent désormais dans les détails de trame.</span><span class="sxs-lookup"><span data-stu-id="4ee22-272">Secure context, [Cross-Origin-Embedder-Policy (COEP)][WebDevCoopCoep], and [Cross-Origin-Opener-Policy (COOP)][WebDevCoopCoep] are now displayed in the frame details.</span></span>  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Informations de sécurité et d’isolement" lightbox="../../media/2020/08/coep-coop.msft.png":::
   <span data-ttu-id="4ee22-274">Informations de sécurité et d’isolement</span><span class="sxs-lookup"><span data-stu-id="4ee22-274">Security and isolation information</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-275">À l’avenir, l’équipe Microsoft Edge DevTools et l’équipe chrome DevTools sont en voie d’ajouter des informations de sécurité aux détails de trames.</span><span class="sxs-lookup"><span data-stu-id="4ee22-275">In the future, the Microsoft Edge DevTools team and the Chrome DevTools team are planning to add more security information to the frame details.</span></span>  

<span data-ttu-id="4ee22-276">Problème de chrome: [#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="4ee22-276">Chromium issue: [#1051466][CR1051466]</span></span>  

### <span data-ttu-id="4ee22-277">Éléments et mises à jour du panneau réseau</span><span class="sxs-lookup"><span data-stu-id="4ee22-277">Elements and Network panel updates</span></span>  

#### <span data-ttu-id="4ee22-278">Suggestions de couleurs accessibles dans le volet styles</span><span class="sxs-lookup"><span data-stu-id="4ee22-278">Accessible color suggestion in the Styles pane</span></span>  

<span data-ttu-id="4ee22-279">DevTools propose désormais des suggestions de couleurs pour le texte de faible contraste de couleurs.</span><span class="sxs-lookup"><span data-stu-id="4ee22-279">DevTools now provides color suggestions for low color contrast text.</span></span>  

<span data-ttu-id="4ee22-280">Dans l’exemple ci-dessous, vous `h1` avez du texte à contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="4ee22-280">In the example below, `h1` has low contrast text.</span></span>  <span data-ttu-id="4ee22-281">Pour résoudre ce problème, ouvrez le sélecteur de couleurs de la `color` propriété dans le volet **styles** .</span><span class="sxs-lookup"><span data-stu-id="4ee22-281">To fix it, open the color picker of the `color` property in the **Styles** pane.</span></span>  <span data-ttu-id="4ee22-282">Une fois que vous avez développé la section **coefficient de contraste** , devtools fournit des suggestions couleur AA et AAA.</span><span class="sxs-lookup"><span data-stu-id="4ee22-282">After you expand the **Contrast ratio** section, DevTools provides AA and AAA color suggestions.</span></span>  <span data-ttu-id="4ee22-283">Pour appliquer la couleur, sélectionnez la couleur suggérée.</span><span class="sxs-lookup"><span data-stu-id="4ee22-283">Select the suggested color to apply the color.</span></span>  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="Le sélecteur de couleurs suggère des suggestions couleur AA et AAA" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   <span data-ttu-id="4ee22-285">Le sélecteur de couleurs suggère des suggestions couleur AA et AAA</span><span class="sxs-lookup"><span data-stu-id="4ee22-285">Color picker suggests AA and AAA color suggestions</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-286">Problème de chrome: [#1093227][CR1093227]</span><span class="sxs-lookup"><span data-stu-id="4ee22-286">Chromium issue: [#1093227][CR1093227]</span></span>  

#### <span data-ttu-id="4ee22-287">Volet de rétablissement des propriétés dans le panneau éléments</span><span class="sxs-lookup"><span data-stu-id="4ee22-287">Reinstate Properties pane in the Elements panel</span></span>  

<span data-ttu-id="4ee22-288">Le volet **Propriétés** est en retour.</span><span class="sxs-lookup"><span data-stu-id="4ee22-288">The **Properties** pane is back.</span></span>  <span data-ttu-id="4ee22-289">Elle a été [déconseillée dans Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span><span class="sxs-lookup"><span data-stu-id="4ee22-289">It was [deprecated in Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span></span>  <span data-ttu-id="4ee22-290">L’équipe Microsoft Edge DevTools et l’équipe DevTools chrome présentent des améliorations en matière d’examen des propriétés des éléments.</span><span class="sxs-lookup"><span data-stu-id="4ee22-290">The Microsoft Edge DevTools team and the Chrome DevTools team are planning improvements for inspecting properties of elements.</span></span>  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Volet Propriétés dans le panneau éléments" lightbox="../../media/2020/08/properties-pane.msft.png":::
   <span data-ttu-id="4ee22-292">Volet **Propriétés** dans le panneau **éléments**</span><span class="sxs-lookup"><span data-stu-id="4ee22-292">**Properties** pane in the **Elements** panel</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-293">Problème de chrome:</span><span class="sxs-lookup"><span data-stu-id="4ee22-293">Chromium issue:</span></span>  <!--  [#1105205][CR1105205],  -->  <span data-ttu-id="4ee22-294">[#1116085] [CR1116085]</span><span class="sxs-lookup"><span data-stu-id="4ee22-294">[#1116085][CR1116085]</span></span>  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Human-readable `X-Client-Data` header values" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### <span data-ttu-id="4ee22-295">Saisie semi-automatique de polices personnalisées dans le volet styles</span><span class="sxs-lookup"><span data-stu-id="4ee22-295">Autocomplete custom fonts in the Styles pane</span></span>  

<span data-ttu-id="4ee22-296">Les polices importées sont désormais ajoutées à la liste de la saisie semi-automatique CSS lors de la modification `font-family` de la propriété dans le volet **styles** .</span><span class="sxs-lookup"><span data-stu-id="4ee22-296">Imported font faces are now added to the list of CSS autocompletion when editing the `font-family` property in the **Styles** pane.</span></span>  

<span data-ttu-id="4ee22-297">Par exemple, si `monospace` vous disposez d’une police personnalisée installée sur l’ordinateur local, celle-ci apparaît dans la liste de saisie semi-automatique CSS.</span><span class="sxs-lookup"><span data-stu-id="4ee22-297">For example, if `monospace` is a custom font installed on the local machine, it's displayed in the CSS completion list.</span></span> <span data-ttu-id="4ee22-298">Dans les versions précédentes de Microsoft Edge, la police n’est pas affichée.</span><span class="sxs-lookup"><span data-stu-id="4ee22-298">In previous versions of Microsoft Edge, the font wasn't displayed.</span></span>

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Saisie semi-automatique de polices personnalisées" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   <span data-ttu-id="4ee22-300">Saisie semi-automatique de polices personnalisées</span><span class="sxs-lookup"><span data-stu-id="4ee22-300">Autocomplete custom fonts</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-301">Problème de chrome: [#1106221] [CR1106221]</span><span class="sxs-lookup"><span data-stu-id="4ee22-301">Chromium issue: [#1106221][CR1106221]</span></span>  

#### <span data-ttu-id="4ee22-302">Affichage cohérent du type de ressource dans le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="4ee22-302">Consistently display resource type in Network panel</span></span>  

<span data-ttu-id="4ee22-303">DevTools affichent désormais systématiquement le même type de ressource que la requête réseau d’origine et est ajouté `/ Redirect` à la valeur de la colonne **type** lorsque la redirection \ (code d’État http 302 \) se produit.</span><span class="sxs-lookup"><span data-stu-id="4ee22-303">DevTools now consistently display the same resource type as the original network request and appends `/ Redirect` to the **Type** column value when redirection \(HTTP status code 302\) happens.</span></span>  

<span data-ttu-id="4ee22-304">Auparavant DevTools modifié ce type sur `Other` parfois.</span><span class="sxs-lookup"><span data-stu-id="4ee22-304">Previously DevTools changed the type to `Other` sometimes.</span></span>  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Afficher le type de ressource rediriger" lightbox="../../media/2020/08/network-redirect.msft.png":::
   <span data-ttu-id="4ee22-306">Afficher le type de ressource rediriger</span><span class="sxs-lookup"><span data-stu-id="4ee22-306">Display redirect resource type</span></span>  
:::image-end:::  

<span data-ttu-id="4ee22-307">Problème de chrome: [#997694][CR997694]</span><span class="sxs-lookup"><span data-stu-id="4ee22-307">Chromium issue: [#997694][CR997694]</span></span>  

#### <span data-ttu-id="4ee22-308">Boutons clairs dans les panneaux éléments et réseau</span><span class="sxs-lookup"><span data-stu-id="4ee22-308">Clear buttons in the Elements and Network panels</span></span>  

<span data-ttu-id="4ee22-309">Les zones de texte suivantes disposent désormais de boutons **clairs** .</span><span class="sxs-lookup"><span data-stu-id="4ee22-309">The following text boxes now have **Clear** buttons.</span></span>  

*   <span data-ttu-id="4ee22-310">Les zones de texte de filtre dans le volet **styles** et le panneau **réseau** .</span><span class="sxs-lookup"><span data-stu-id="4ee22-310">The filter text boxes in the **Styles** pane and **Network** panel.</span></span>  
*   <span data-ttu-id="4ee22-311">Zone de texte de recherche DOM dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="4ee22-311">The DOM search text box in the **Elements** panel.</span></span>  

<span data-ttu-id="4ee22-312">Cliquez sur le bouton **Effacer** pour supprimer du texte entré.</span><span class="sxs-lookup"><span data-stu-id="4ee22-312">Choose the **Clear** button to remove any inputted text.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Boutons effacer dans les panneaux d’éléments" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         <span data-ttu-id="4ee22-314">Boutons effacer dans les panneaux d' **éléments**</span><span class="sxs-lookup"><span data-stu-id="4ee22-314">Clear buttons in the **Elements** panels</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Boutons effacer dans les panneaux réseau" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         <span data-ttu-id="4ee22-316">Boutons effacer dans les panneaux **réseau**</span><span class="sxs-lookup"><span data-stu-id="4ee22-316">Clear buttons in the  **Network** panels</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="4ee22-317">Problème de chrome: [#1067184][CR1067184]</span><span class="sxs-lookup"><span data-stu-id="4ee22-317">Chromium issue: [#1067184][CR1067184]</span></span>  

## <span data-ttu-id="4ee22-318">Télécharger les canaux Microsoft Edge preview</span><span class="sxs-lookup"><span data-stu-id="4ee22-318">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="4ee22-319">Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="4ee22-319">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="4ee22-320">Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="4ee22-320">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="4ee22-321">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4ee22-321">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Icône Paramètres de DevTools"  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Désapprobation du volet Propriétés dans le panneau éléments nouveautés de DevTools (Microsoft Edge 84) | Documents Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Fonctionnalités de débogage de grille CSS-nouveautés dans DevTools (Microsoft Edge 85) | Documents Microsoft"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personnaliser les raccourcis clavier dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Activer les API expérimentales-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Émulation: prise en charge du mode double affichage-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Activer la visionneuse de commandes sources-fonctionnalités expérimentales | Documents Microsoft"
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: https://review.docs.microsoft.com/microsoft-edge/devtools-guide-chromium/experimental-features?branch=user/zoghadya/dual-screen-experiment#emulation-support-dual-screen-mode "Émulation: prise en charge du mode double affichage-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Tests sur les périphériques pliants et à deux écrans-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activer les fonctionnalités expérimentales-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "référence sur les API table-console | Documents Microsoft"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Recherchez du code JavaScript et CSS inutilisé avec l’onglet couverture dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Tiroir-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analyser les performances de rendu à l’aide de l’onglet rendu-référence d’analyse des performances | Documents Microsoft"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Afficher et déboguer les informations sur les lecteurs multimédias | Documents Microsoft"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Comment utiliser la couture-Introduction aux périphériques à écran double Documents Microsoft"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Fonctionnalité de répartition d’écran de média CSS pour la détection sur deux écrans | Documents Microsoft"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments pour les appareils à deux écrans | Documents Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux Microsoft Edge preview"  

[VisualStudioCode]: https://code.visualstudio.com "Code Visual Studio "  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Raccourcis clavier dans Visual Studio code pour Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Nouvelle surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools compte Twitter"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs du chrome"  

[CR174309]: https://crbug.com/174309 "DevTools: autoriser pour personnaliser les raccourcis clavier/les combinaisons de touches | Bugs du chrome"
[CR384968]: https://crbug.com/384968 "Option permettant d’ignorer les polices locales () | Bugs du chrome"  
[CR772558]: https://crbug.com/772558 "DevTools: mise à jour vers la dernière version de phare | Bugs du chrome"  
[CR807440]: https://crbug.com/807440 "Blocage de chrome avec un grand nombre de SWs | Bugs du chrome"  
[CR997694]: https://crbug.com/997694 "Les requêtes XHR avec le statut 302 ne sont pas affichées sous le filtre \ «XHR \» dans le panneau réseau | Bugs du chrome"  
[CR1047356]: https://crbug.com/1047356 "Outils CSS Grid/Flexbox/table"  
[CR1051466]: https://crbug.com/1051466 "Prendre en charge le débogage COOP/COEP dans DevTools | Bugs du chrome"  
[CR1054281]: https://crbug.com/1054281 "Demande de fonctionnalité: DevTools doit émuler les périphériques pliants et à deux écrans | Bugs du chrome"  
[CR1067184]: https://crbug.com/1067184 "Demande de fonctionnalité: bouton Effacer le filtre sur réseau & les éléments-> entrées de filtre de style Bugs du chrome"  
[CR1068116]: https://crbug.com/1068116 "☂ Le panneau problèmes d’expédition | Bugs du chrome"  
[CR1080569]: https://crbug.com/1080569 "Acorn ne prend pas en charge les opérateurs d’affectation logiques | Bugs du chrome"  
[CR1080589]: https://crbug.com/1080589 "Classifier les problèmes par tiers/tierce partie | Bugs du chrome"  
[CR1086817]: https://crbug.com/1086817 "Acorn ne prend pas en charge les séparateurs numériques | Bugs du chrome"  
[CR1090802]: https://crbug.com/1090802 "Simuler les changements d’état d’inactivité de l’API de détection d’inactivité | Bugs du chrome"  
[CR1093227]: https://crbug.com/1093227 "DevTools: suggérer une couleur d’accessibilité plus proche | Bugs du chrome"  
[CR1093247]: https://crbug.com/1093247 "Afficher des informations sur les trames dans le panneau application | Bugs du chrome"  
[CR1094406]: https://crbug.com/1094406 "Les développeurs doivent utiliser une visionneuse de commandes sources au https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: prise en charge de l’émulation de la fonctionnalité de média-Reduced-Data. Bugs du chrome"  
[CR1096481]: https://crbug.com/1096481 "Positionnement des bannières de problèmes | Bugs du chrome"  
[CR1100253]: https://crbug.com/1100253 "Raccourci du nœud ajouter une capture d’écran dans le menu contextuel de l’élément | Bugs du chrome"  
[CR1103316]: https://crbug.com/1103316 "La recherche d’éléments n’resolveNode (texte en surbrillance, etc.) sur le premier résultat de la recherche | Bugs du chrome"  
[CR1103854]: https://crbug.com/1103854 "Dé-brouiller X-client-valeurs de données dans les outils de développement | Bugs du chrome"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: https://crbug.com/1106221 "Ajoutez des polices importées à la saisie semi-automatique de la famille de polices dans le panneau Styles | Bugs du chrome  
[CR1107766]: https://crbug.com/1107766 "afficher des informations sur les trames générées par’Window. Open () 'dans l’arborescence Bugs du chrome  
[CR1115011]: https://crbug.com/1115011 "lors de la copie d’une table à partir de la console la structure de la table n’est pas conservée | Bugs du chrome  
[CR1116085]: https://crbug.com/1116085 "Retournez l’inspecteur Propriétés devtools | Bugs du chrome  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "préfère-Reduce-des requêtes de données multimédia niveau 5 | Brouillons de l’éditeur de groupe de travail CSS W3C"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v 6.2.0-GoogleChrome/phare | GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Mémoires tampons de protocole | Développeurs Google"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Pli Galaxy | Samsung US"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Attribution logique | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Séparateurs numériques | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Faire de votre site Web «Cross-Origin isolated» à l’aide de COOP et COEP | Web. dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Détecter les utilisateurs inactifs à l’aide de l’API de détection d’activité Web. dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Évitez les animations non composites | Web. dev"  

> [!NOTE]
> <span data-ttu-id="4ee22-382">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4ee22-382">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4ee22-383">La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/08/devtools/index) et est créée par [Jecelyn Yeen][JecelynYeen] \ (développeurs, chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="4ee22-383">The original page is found [here](https://developers.google.com/web/updates/2020/08/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="4ee22-385">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4ee22-385">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
