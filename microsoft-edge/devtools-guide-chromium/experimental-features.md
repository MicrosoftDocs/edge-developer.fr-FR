---
description: Dernières fonctionnalités expérimentales de Microsoft Edge DevTools
title: Fonctionnalités expérimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, expérience
ms.openlocfilehash: b2b2e591834f1c75d51ec98523e2752d67a2d354
ms.sourcegitcommit: 6571bcc0b7f1c4c9d6ead65081374bab87cd4469
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/09/2020
ms.locfileid: "11203898"
---
# <span data-ttu-id="05a6d-104">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="05a6d-104">Experimental features</span></span>  

<span data-ttu-id="05a6d-105">Microsoft Edge DevTools fournit l’accès à des fonctionnalités expérimentales toujours en développement.</span><span class="sxs-lookup"><span data-stu-id="05a6d-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="05a6d-106">Vous pouvez tester et [fournir des commentaires](#providing-feedback-on-experimental-features) avant la sortie de chaque fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="05a6d-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="05a6d-107">Si les fonctionnalités expérimentales sont disponibles dans tous les canaux de Microsoft Edge, vous pouvez obtenir les dernières fonctionnalités expérimentales à l’aide du canal des Canaries Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="05a6d-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="05a6d-108">Activer les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="05a6d-108">Turn on experimental features</span></span>  

<span data-ttu-id="05a6d-109">Pour activer les fonctionnalités expérimentales de \ (ou de désactivation) dans Microsoft Edge, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="05a6d-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="05a6d-110">[Ouvrez devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="05a6d-110">[Open DevTools][DevtoolsOpen].</span></span>  
    *   <span data-ttu-id="05a6d-111">Sélectionnez `Control` + `Shift` + `I` \ (Windows, Linux \) ou `Command` + `Option` + `I` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="05a6d-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="05a6d-112">Pour plus d’informations, accédez à [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="05a6d-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="05a6d-113">Ouvrez le volet [paramètres][DevToolsCustomizeSettings] .</span><span class="sxs-lookup"><span data-stu-id="05a6d-113">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="05a6d-114">Sélectionnez `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="05a6d-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="05a6d-115">Pour plus d’informations, accédez à [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="05a6d-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="05a6d-116">Sur le côté gauche du volet **paramètres** , sélectionnez la section **expériences** .</span><span class="sxs-lookup"><span data-stu-id="05a6d-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.msft.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/experiments-devtools.msft.png":::
       <span data-ttu-id="05a6d-118">Liste des expériences dans les **paramètres** de devtools</span><span class="sxs-lookup"><span data-stu-id="05a6d-118">List of experiments in DevTools **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="05a6d-119">Sur la page **expériences** , faites défiler la liste de toutes les fonctionnalités expérimentales disponibles, puis cochez la case en regard de chaque fonctionnalité que vous voulez tester.</span><span class="sxs-lookup"><span data-stu-id="05a6d-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="05a6d-120">Fermez et rouvrez Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="05a6d-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="05a6d-121">Les fonctionnalités expérimentales sont constamment mises à jour et peuvent entraîner des problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="05a6d-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="05a6d-122">Pour désactiver une fonctionnalité expérimentale, ouvrez la page **expériences** , puis décochez la case de la fonctionnalité expérimental que vous souhaitez désactiver.</span><span class="sxs-lookup"><span data-stu-id="05a6d-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="05a6d-123">Fonctionnalités expérimentales mises en évidence</span><span class="sxs-lookup"><span data-stu-id="05a6d-123">Highlighted experimental features</span></span>  

<span data-ttu-id="05a6d-124">Les sections suivantes décrivent les nouvelles fonctionnalités expérimentales disponibles dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="05a6d-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="05a6d-125">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="05a6d-125">Experimental feature</span></span> | <span data-ttu-id="05a6d-126">Version de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="05a6d-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="05a6d-127">Émulation: prise en charge du mode double écran</span><span class="sxs-lookup"><span data-stu-id="05a6d-127">Emulation: Support dual screen mode</span></span>](#emulation-support-dual-screen-mode) | <span data-ttu-id="05a6d-128">84 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="05a6d-128">84 or later</span></span> |  
| [<span data-ttu-id="05a6d-129">Activer les nouvelles fonctionnalités de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="05a6d-129">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="05a6d-130">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="05a6d-130">85 or later</span></span> |  
| [<span data-ttu-id="05a6d-131">Activer la prise en charge du déplacement des onglets entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="05a6d-131">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="05a6d-132">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="05a6d-132">85 or later</span></span> |  
| [<span data-ttu-id="05a6d-133">Activer webhint</span><span class="sxs-lookup"><span data-stu-id="05a6d-133">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="05a6d-134">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="05a6d-134">85 or later</span></span> |  
| [<span data-ttu-id="05a6d-135">Activer la console réseau</span><span class="sxs-lookup"><span data-stu-id="05a6d-135">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="05a6d-136">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="05a6d-136">85 or later</span></span> |  
| [<span data-ttu-id="05a6d-137">Visionneuse de commandes source</span><span class="sxs-lookup"><span data-stu-id="05a6d-137">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="05a6d-138">86 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="05a6d-138">86 or later</span></span> |  
| [<span data-ttu-id="05a6d-139">Activer l’éditeur de raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="05a6d-139">Enable keyboard shortcut editor</span></span>](#enable-keyboard-shortcut-editor) | <span data-ttu-id="05a6d-140">87 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="05a6d-140">87 or later</span></span> |  
| [<span data-ttu-id="05a6d-141">Activer les calques composites dans l’affichage 3D</span><span class="sxs-lookup"><span data-stu-id="05a6d-141">Turn on Composited Layers in 3D View</span></span>](#turn-on-composited-layers-in-3d-view) | <span data-ttu-id="05a6d-142">87 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="05a6d-142">87 or later</span></span> |  

### <span data-ttu-id="05a6d-143">Émulation: prise en charge du mode double écran</span><span class="sxs-lookup"><span data-stu-id="05a6d-143">Emulation: Support dual screen mode</span></span>  

<span data-ttu-id="05a6d-144">Fournit des fonctionnalités supplémentaires pour l’émulation de deux nouveaux périphériques à écran double et pliant dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="05a6d-144">Provides additional features for emulating two new dual-screen and foldable devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="05a6d-145">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="05a6d-145">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="05a6d-146">Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="05a6d-146">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  
    
<span data-ttu-id="05a6d-147">Émuler les appareils et basculer entre les positions suivantes.</span><span class="sxs-lookup"><span data-stu-id="05a6d-147">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="05a6d-148">un écran ou une position pliée</span><span class="sxs-lookup"><span data-stu-id="05a6d-148">single-screen or folded posture</span></span>  
*   <span data-ttu-id="05a6d-149">position à deux écrans ou dépliées</span><span class="sxs-lookup"><span data-stu-id="05a6d-149">dual-screen or unfolded posture</span></span>  
    
<span data-ttu-id="05a6d-150">[Activez les API de plateforme Web expérimentales](#enable-experimental-apis) et utilisez la [fonctionnalité de répartition d’écran de média CSS][DualScreenDocsCssMedia] et l' [API getWindowSegments JavaScript][DualScreenDocsJSAPI] pour améliorer votre site Web \ (ou l’application \) pour les appareils à double écran et pliant.</span><span class="sxs-lookup"><span data-stu-id="05a6d-150">[Enable experimental Web Platform APIs](#enable-experimental-apis) and use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI] to enhance your website \(or app\) for dual-screen and foldable devices.</span></span>  

:::image type="complex" source="./media/experiments-surface-duo-emulation.msft.png" alt-text="Émuler surface duo dans Microsoft Edge" lightbox="./media/experiments-surface-duo-emulation.msft.png":::  
   <span data-ttu-id="05a6d-152">Émuler surface duo dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="05a6d-152">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

#### <span data-ttu-id="05a6d-153">Activer les API expérimentales</span><span class="sxs-lookup"><span data-stu-id="05a6d-153">Enable experimental APIs</span></span>  

<span data-ttu-id="05a6d-154">Pour utiliser la [fonctionnalité de répartition d’écran de média CSS][DualScreenDocsCssMedia] et l' [API getWindowSegments JavaScript][DualScreenDocsJSAPI], activez l' `Experimental Web Platform features` indicateur dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="05a6d-154">To use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI], turn on the `Experimental Web Platform features` flag in Microsoft Edge.</span></span>  <span data-ttu-id="05a6d-155">Procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="05a6d-155">Complete the following steps.</span></span>  

1.  <span data-ttu-id="05a6d-156">Accédez à `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="05a6d-156">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="05a6d-157">Dans la zone de texte **indicateurs de recherche** , entrez `Experimental Web Platform features` , sélectionnez l’indicateur **fonctionnalités de plateforme Web expérimentales** , puis **désactivez** l' **option**désactivé.</span><span class="sxs-lookup"><span data-stu-id="05a6d-157">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="05a6d-158">Redémarrez MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="05a6d-158">Restart Microsoft Edge.</span></span>  
    
:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Activer l’indicateur de fonctionnalités de plateforme Web expérimentale" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="05a6d-160">Activer l’indicateur de fonctionnalités de plateforme Web expérimentale</span><span class="sxs-lookup"><span data-stu-id="05a6d-160">Enable the Experimental Web Platform features flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="05a6d-161">Si vous utilisez des [requêtes multimédias CSS][DualScreenDocsCssMedia] ou l’API d' [énumération de segment Windows JavaScript][DualScreenDocsJSAPI] pour améliorer votre site Web ou votre application pour le duo de [surface][SurfaceDevicesDuo], vous devez également activer l' [][GooglePlayMicrosoftEdge] indicateur de **fonctionnalités de plateforme Web** [][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="05a6d-161">If you are using [CSS media queries][DualScreenDocsCssMedia] or the [JavaScript Windows Segment Enumeration API][DualScreenDocsJSAPI] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also enable the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>  
> 
> <span data-ttu-id="05a6d-162">Si l’indicateur fonctionnalités de la **plateforme Web expérimentée** est activé dans la version de [Bureau de Microsoft Edge][MicrosoftEdge] et désactivée dans l' [application Microsoft Edge Android][GooglePlayMicrosoftEdge], le comportement de votre site Web ou de votre application dans l’émulateur de surface duo dans l’application de bureau Microsoft Edge ne correspond pas à l' [application Android Microsoft Edge][GooglePlayMicrosoftEdge] sur le [Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="05a6d-162">If the **Experimental Web Platform features** flag is enabled in [desktop Microsoft Edge][MicrosoftEdge] and disabled in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge does not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="05a6d-163">Assurez-vous que les indicateurs sont mis en correspondance entre Android et Microsoft Edge pour pouvoir utiliser l’émulateur de surface duo dans [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="05a6d-163">Ensure that the flags are matching across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

#### <span data-ttu-id="05a6d-164">Tests sur des appareils à écran double et pliant</span><span class="sxs-lookup"><span data-stu-id="05a6d-164">Testing on foldable and dual-screen devices</span></span>  

<span data-ttu-id="05a6d-165">Lorsque vous émulez le [duo de surface][SurfaceDevicesDuo] dans une position sur deux écrans dans Microsoft Edge, la couture (espace entre les deux écrans \) est tracée sur votre site Web ou votre application.</span><span class="sxs-lookup"><span data-stu-id="05a6d-165">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the seam \(the space between the two screens\) is drawn over your website or app.</span></span>  

<span data-ttu-id="05a6d-166">L’affichage émulé correspond au mode de rendu de votre site Web (ou de l’application) dans l' [application Microsoft Edge Android][GooglePlayMicrosoftEdge] exécuté sur [surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="05a6d-166">The emulated display matches the way your website \(or app\) renders in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] running on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="05a6d-167">Il est possible que vous deviez mettre à jour votre site Web \ (ou l’application \) pour l’afficher mieux le long de la couture.</span><span class="sxs-lookup"><span data-stu-id="05a6d-167">You may have to update your website \(or app\) to display better along the seam.</span></span>  <span data-ttu-id="05a6d-168">Pour plus d’informations sur l’adaptation de votre site Web (ou de l’application) à la couture, accédez à l' [utilisation de la couture][DualScreenIntroductionHowWorkSeam].</span><span class="sxs-lookup"><span data-stu-id="05a6d-168">For more information about adapting your website \(or app\) to the seam, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam].</span></span>  

<span data-ttu-id="05a6d-169">La [barre d’outils][DevtoolsDeviceModeIndexSimulateMobileViewport] de l’appareil inclut des fonctionnalités supplémentaires pour vous aider à tester votre site Web ou votre application en plusieurs positions et orientations.</span><span class="sxs-lookup"><span data-stu-id="05a6d-169">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="05a6d-170">Sélectionnez **faire pivoter** \ ( ![ faire pivoter ][ImageRotateIcon] ) pour faire pivoter la fenêtre d’affichage en orientation paysage.</span><span class="sxs-lookup"><span data-stu-id="05a6d-170">Choose **Rotate** \(![Rotate][ImageRotateIcon]\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="05a6d-171">Combinez la fonctionnalité avec la **plage** \ ( ![ span ][ImageSpanIcon] \) pour basculer entre les positions à un seul écran ou pliées en deux ou non pliées.</span><span class="sxs-lookup"><span data-stu-id="05a6d-171">Combine the feature with **Span** \(![Span][ImageSpanIcon]\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="05a6d-172">Ensemble, les fonctionnalités permettent le test de votre site Web ou de votre application dans les quatre positions et orientations possibles.</span><span class="sxs-lookup"><span data-stu-id="05a6d-172">Together, the features enable testing your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matrice de positions et d’orientations pour les appareils à écran double et pliant" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="05a6d-174">Matrice de positions et d’orientations pour les appareils à écran double et pliant</span><span class="sxs-lookup"><span data-stu-id="05a6d-174">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="05a6d-175">Les **fonctionnalités de la plateforme Web expérimentales** \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \) affichent l’état de l’indicateur de **fonctionnalités de plateforme Web expérimentale** .</span><span class="sxs-lookup"><span data-stu-id="05a6d-175">The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="05a6d-176">Si l’indicateur est activé, l’icône est mise en évidence.</span><span class="sxs-lookup"><span data-stu-id="05a6d-176">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="05a6d-177">Si l’indicateur est désactivé, l’icône n’est pas mise en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="05a6d-177">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="05a6d-178">Pour activer \ (ou désactivé) l’indicateur, accédez à l’indicateur `edge://flags` et activez-le.</span><span class="sxs-lookup"><span data-stu-id="05a6d-178">To turn on \(or off\) the flag, navigate to `edge://flags` and toggle the flag.</span></span>  

<!-- Commenting out until the icon issue is fixed in Edge Canary
The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.  If the flag is turned on, the icon is highlighted.  If the flag is turned off, the icon is not highlighted.  To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.   -->  

<span data-ttu-id="05a6d-179">Voici d’autres ressources qui peuvent vous aider à améliorer votre site Web \ (ou votre application \) pour les appareils à deux écrans.</span><span class="sxs-lookup"><span data-stu-id="05a6d-179">Here are additional resources that may help you enhance your website \(or app\) for dual-screen devices.</span></span>  

*   <span data-ttu-id="05a6d-180">Pour plus d’informations sur le développement Web sur les appareils à deux écrans, voir [expériences sur le Web à deux écrans][DualScreenWebIndex].</span><span class="sxs-lookup"><span data-stu-id="05a6d-180">For more information about web development on dual-screen devices, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="05a6d-181">Installez l' [émulateur de surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="05a6d-181">Install the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="05a6d-182">Il est différent de l’émulateur dans Microsoft Edge, émule le duo de surface sur lequel s’exécute Android et intégré à [Android Studio][AndroidDeveloperStudio].</span><span class="sxs-lookup"><span data-stu-id="05a6d-182">It is different from the emulator in Microsoft Edge, emulates the Surface Duo running Android, and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="05a6d-183">Pour plus d’informations, accédez au [Kit de développement logiciel (SDK) surface Duo][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="05a6d-183">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  
    
> [!NOTE]
> <span data-ttu-id="05a6d-184">Voici une liste des problèmes connus actuels.</span><span class="sxs-lookup"><span data-stu-id="05a6d-184">The following is a list of current known issues.</span></span>  
> 
> *   <span data-ttu-id="05a6d-185">Lorsque vous utilisez un [client de bureau à distance Microsoft][RemoteDesktopClientDocs] pour vous connecter à un PC distant et émuler le pli de [surface Duo][SurfaceDevicesDuo] ou [Samsung Galaxy][SamsungMobileGalaxyFold], le pointeur risque de secouer ou d’interruption.</span><span class="sxs-lookup"><span data-stu-id="05a6d-185">When using a [Microsoft Remote Desktop client][RemoteDesktopClientDocs] to connect to a remote PC and emulate the [Surface Duo][SurfaceDevicesDuo] or [Samsung Galaxy Fold][SamsungMobileGalaxyFold], the pointer may shake or stutter.</span></span>  <span data-ttu-id="05a6d-186">Si vous rencontrez ce problème, [envoyez des commentaires](#providing-feedback-on-experimental-features).</span><span class="sxs-lookup"><span data-stu-id="05a6d-186">If you run into the issue, [send feedback](#providing-feedback-on-experimental-features).</span></span>  

### <span data-ttu-id="05a6d-187">Activer les nouvelles fonctionnalités de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="05a6d-187">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="05a6d-188">Cette fonctionnalité expérimentale fournit un certain nombre de nouvelles visualisations pour vous aider à déboguer des dispositions de grille CSS.</span><span class="sxs-lookup"><span data-stu-id="05a6d-188">This experimental feature provides a number of new visualizations to help you debug CSS grid layouts.</span></span>  <span data-ttu-id="05a6d-189">Pour afficher un aperçu des dernières fonctionnalités expérimentales, [activez cette expérience](#turn-on-experimental-features) et rechargez devtools.</span><span class="sxs-lookup"><span data-stu-id="05a6d-189">To preview the latest experimental features, [enable this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  <span data-ttu-id="05a6d-190">Cette expérience est activée par défaut dans Microsoft Edge version 87 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="05a6d-190">This experiment is on by default in Microsoft Edge version 87 or later.</span></span>  

#### <span data-ttu-id="05a6d-191">Affichage des superpositions de la grille sur le survol avec l’outil inspecter</span><span class="sxs-lookup"><span data-stu-id="05a6d-191">Viewing on-hover grid overlays with the Inspect tool</span></span>  

<span data-ttu-id="05a6d-192">L’outil **Inspect** vous permet d’identifier et de visualiser rapidement les dispositions d’une grille CSS dans un site Web en les plaçant au-dessus à l’aide de la souris.</span><span class="sxs-lookup"><span data-stu-id="05a6d-192">The **Inspect** tool provides a quick way to identify and visualize CSS Grid layouts in a website by hovering over them with the mouse.</span></span>  <span data-ttu-id="05a6d-193">\*\*\*\* ![ ](./media/inspect-icon.msft.png) Dans le coin supérieur gauche de devtools, sélectionnez l’icône inspecter \ (Inspect \).</span><span class="sxs-lookup"><span data-stu-id="05a6d-193">Choose the **Inspect** \(![Inspect](./media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="05a6d-194">Ensuite, pointez sur un élément Grid sur le site Web que vous déboguez.</span><span class="sxs-lookup"><span data-stu-id="05a6d-194">Then, hover over a Grid element on the website you are debugging.</span></span>  <span data-ttu-id="05a6d-195">Les plans sont affichés dans la grille, et l’ombrage indique l’emplacement des espaces de la grille, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="05a6d-195">Outlines are displayed around the grid, and shading indicates the location of grid gaps if present.</span></span>  

:::image type="complex" source="./media/grid-inspect.msft.png" alt-text="Affichage de grilles avec l’outil Inspect" lightbox="./media/grid-inspect.msft.png":::
   <span data-ttu-id="05a6d-197">Affichage de grilles avec l’outil Inspect</span><span class="sxs-lookup"><span data-stu-id="05a6d-197">Viewing grids with the Inspect tool</span></span>  
:::image-end:::  

#### <span data-ttu-id="05a6d-198">Affichage de superpositions de grille persistante</span><span class="sxs-lookup"><span data-stu-id="05a6d-198">Viewing persistent grid overlays</span></span>  

<span data-ttu-id="05a6d-199">Dans la version 86 de Microsoft Edge ou version ultérieure, la fonctionnalité de grille de feuilles de style</span><span class="sxs-lookup"><span data-stu-id="05a6d-199">In Microsoft Edge version 86 or later, the experimental CSS grid feature also offers the option to enable persistent Grid overlays.</span></span>  <span data-ttu-id="05a6d-200">Les superpositions persistantes offrent plusieurs avantages.</span><span class="sxs-lookup"><span data-stu-id="05a6d-200">The persistent overlays provide several benefits.</span></span>  

*   <span data-ttu-id="05a6d-201">Les superpositions persistantes restent visibles sur la page lorsque vous faites défiler, déplacez la souris et utilisez les autres fonctionnalités du DevTools.</span><span class="sxs-lookup"><span data-stu-id="05a6d-201">The persistent overlays remain visible on the page as you scroll, move your mouse, and use other features of the DevTools.</span></span>  
*   <span data-ttu-id="05a6d-202">Plusieurs superpositions persistantes peuvent être activées en même temps, ce qui vous permet de revoir différentes dispositions de grille en une seule fois.</span><span class="sxs-lookup"><span data-stu-id="05a6d-202">Multiple persistent overlays can be enabled at the same time, allowing you to review several grid layouts at once.</span></span>  
*   <span data-ttu-id="05a6d-203">Les superpositions persistantes proposent de nombreuses options de configuration, telles que le masquage et l’affichage des noms dans la zone de grille, les espaces de grille, les tailles de suivi, etc.</span><span class="sxs-lookup"><span data-stu-id="05a6d-203">Persistent overlays offer many configuration options, such as hiding or showing names in the grid area, grid gaps, track sizes, and so on.</span></span>  
    
<span data-ttu-id="05a6d-204">Il existe deux façons d’activer ou de désactiver une superposition de grille persistante.</span><span class="sxs-lookup"><span data-stu-id="05a6d-204">The two ways to toggle a persistent grid overlay.</span></span>  

*   <span data-ttu-id="05a6d-205">Cliquez sur l’icône ovale de **grille** en regard d’un élément Grid affiché dans l’arborescence DOM de l’outil **éléments** .</span><span class="sxs-lookup"><span data-stu-id="05a6d-205">Choose the **Grid** oval icon next to any Grid element shown in the DOM tree of the **Elements** tool.</span></span>  
    
    :::image type="complex" source="./media/grid-adorner.msft.png" alt-text="Icône ovale de grille dans l’outil éléments" lightbox="./media/grid-adorner.msft.png":::
       <span data-ttu-id="05a6d-207">Icône ovale de grille dans l’outil **éléments**</span><span class="sxs-lookup"><span data-stu-id="05a6d-207">Grid oval icon in **Elements** tool</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="05a6d-208">Ouvrez le nouveau panneau de **disposition** situé dans l’outil éléments, puis activez la case à cocher en regard de chaque élément de grille que vous souhaitez mettre en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="05a6d-208">Open the new **Layout** panel located in the Elements tool, and choose the checkbox next to each Grid element you want to highlight.</span></span>  
    
    :::image type="complex" source="./media/grid-layout-zoom.msft.png" alt-text="Panneau de disposition dans DevTools" lightbox="./media/grid-layout-zoom.msft.png":::
       <span data-ttu-id="05a6d-210">Panneau de **disposition** dans devtools</span><span class="sxs-lookup"><span data-stu-id="05a6d-210">**Layout** panel in DevTools</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="05a6d-211">Configuration de la superposition persistante</span><span class="sxs-lookup"><span data-stu-id="05a6d-211">Configuring persistent overlays</span></span>  

<span data-ttu-id="05a6d-212">Dans la version 86 de Microsoft Edge ou version ultérieure, le nouveau panneau de **disposition** se trouve dans l’outil **éléments** , à côté des **styles** et des onglets **calculés** .</span><span class="sxs-lookup"><span data-stu-id="05a6d-212">In Microsoft Edge version 86 or later, the new **Layout** panel is located in the **Elements** tool alongside the **Styles** and **Computed** tabs.</span></span>  <span data-ttu-id="05a6d-213">Les options de configuration du panneau de **disposition** pour les superpositions persistantes.</span><span class="sxs-lookup"><span data-stu-id="05a6d-213">The **Layout** panel surfaces configuration options for persistent overlays.</span></span>  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="Fonctionnalité de débogage de grille CSS" lightbox="./media/experiments-grid.msft.png":::
   <span data-ttu-id="05a6d-215">Fonctionnalité de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="05a6d-215">CSS grid debugging feature</span></span>  
:::image-end:::  

### <span data-ttu-id="05a6d-216">Activer la prise en charge du déplacement des onglets entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="05a6d-216">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="05a6d-217">En règle générale, il est possible que les outils tels que les **éléments** et le **réseau** s’ouvrent uniquement dans le panneau principal qui se trouve en haut du devtools.</span><span class="sxs-lookup"><span data-stu-id="05a6d-217">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="05a6d-218">Outils tels que l' **affichage 3D** et les **problèmes** qui s’ouvrent normalement uniquement dans le panneau du **tiroir** situé en bas du devtools.</span><span class="sxs-lookup"><span data-stu-id="05a6d-218">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="05a6d-219">Après avoir choisi l’expérience, vous pouvez déplacer des outils entre les volets supérieur et inférieur.</span><span class="sxs-lookup"><span data-stu-id="05a6d-219">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="05a6d-220">Pour déplacer un outil, pointez sur celui-ci, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **déplacer vers le haut** ou **déplacer vers le bas**.</span><span class="sxs-lookup"><span data-stu-id="05a6d-220">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="05a6d-221">Cette expérience vous permet de personnaliser la disposition de votre DevTools.</span><span class="sxs-lookup"><span data-stu-id="05a6d-221">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="05a6d-222">Pour afficher ou masquer le panneau de la **tiroir** , sélectionnez `Escape` .</span><span class="sxs-lookup"><span data-stu-id="05a6d-222">To show or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Déplacement d’un onglet entre les panneaux" lightbox="./media/experiments-move-panels.msft.png":::
   <span data-ttu-id="05a6d-224">Déplacement d’un onglet entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="05a6d-224">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="05a6d-225">Activer webhint</span><span class="sxs-lookup"><span data-stu-id="05a6d-225">Enable webhint</span></span>  

<span data-ttu-id="05a6d-226">[webhint][WebhintMain] est un outil open source qui fournit des commentaires en temps réel sur les sites Web et les pages Web locales.</span><span class="sxs-lookup"><span data-stu-id="05a6d-226">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local web pages.</span></span>  <span data-ttu-id="05a6d-227">Type de commentaires fourni par [webhint][WebhintMain].</span><span class="sxs-lookup"><span data-stu-id="05a6d-227">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="05a6d-228">accessibilité</span><span class="sxs-lookup"><span data-stu-id="05a6d-228">accessibility</span></span>  
*   <span data-ttu-id="05a6d-229">compatibilité entre les navigateurs</span><span class="sxs-lookup"><span data-stu-id="05a6d-229">cross-browser compatibility</span></span>  
*   <span data-ttu-id="05a6d-230">sécurité</span><span class="sxs-lookup"><span data-stu-id="05a6d-230">security</span></span>  
*   <span data-ttu-id="05a6d-231">les</span><span class="sxs-lookup"><span data-stu-id="05a6d-231">performance</span></span>  
*   <span data-ttu-id="05a6d-232">Applications Web progressives (PWAs)</span><span class="sxs-lookup"><span data-stu-id="05a6d-232">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="05a6d-233">autres problèmes courants liés au développement Web</span><span class="sxs-lookup"><span data-stu-id="05a6d-233">other common web development issues</span></span>  
    
<span data-ttu-id="05a6d-234">L’expérience [webhint][WebhintMain] affiche le commentaire de webhint dans le volet [problèmes][DevtoolsIssues] .</span><span class="sxs-lookup"><span data-stu-id="05a6d-234">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="05a6d-235">Sélectionnez un problème pour afficher la documentation de la solution et une liste des ressources affectées sur votre site Web.</span><span class="sxs-lookup"><span data-stu-id="05a6d-235">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="05a6d-236">Cliquez sur le lien d’une ressource pour ouvrir le volet **réseau**, **sources**ou **éléments** approprié dans devtools.</span><span class="sxs-lookup"><span data-stu-id="05a6d-236">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="Commentaires de webhint dans le volet problèmes" lightbox="./media/experiments-webhint.msft.png":::
   <span data-ttu-id="05a6d-238">Commentaires de webhint dans le volet **problèmes**</span><span class="sxs-lookup"><span data-stu-id="05a6d-238">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="05a6d-239">Activer la console réseau</span><span class="sxs-lookup"><span data-stu-id="05a6d-239">Enable Network Console</span></span>  

<span data-ttu-id="05a6d-240">**Network console** est le titre d’une expérience visant à faire des requêtes réseau synthétiques sur http.</span><span class="sxs-lookup"><span data-stu-id="05a6d-240">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="05a6d-241">Vous pouvez utiliser l’expérience de la **console réseau** pour envoyer des demandes d’API Web.</span><span class="sxs-lookup"><span data-stu-id="05a6d-241">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="05a6d-242">Après avoir activé l’expérience, assurez-vous de redémarrer l’DevTools.</span><span class="sxs-lookup"><span data-stu-id="05a6d-242">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="05a6d-243">Pour utiliser la **console réseau**, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="05a6d-243">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="05a6d-244">Ouvrez le volet **réseau** .</span><span class="sxs-lookup"><span data-stu-id="05a6d-244">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="05a6d-245">Recherchez la demande réseau que vous souhaitez modifier et renvoyer.</span><span class="sxs-lookup"><span data-stu-id="05a6d-245">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="05a6d-246">Ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **modifier, puis relire**.</span><span class="sxs-lookup"><span data-stu-id="05a6d-246">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="05a6d-247">Lorsque la **console réseau** s’ouvre, modifiez les informations de requête réseau.</span><span class="sxs-lookup"><span data-stu-id="05a6d-247">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="05a6d-248">Cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="05a6d-248">Choose **Send**.</span></span>  
    
:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Console réseau dans le tiroir de la console" lightbox="./media/network-network-console.msft.png":::
   <span data-ttu-id="05a6d-250">**Console réseau** dans le tiroir de la **console**</span><span class="sxs-lookup"><span data-stu-id="05a6d-250">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="05a6d-251">Visionneuse de commandes source</span><span class="sxs-lookup"><span data-stu-id="05a6d-251">Source Order Viewer</span></span>  

<span data-ttu-id="05a6d-252">La **visionneuse de commandes source** est une expérience qui affiche l’ordre des éléments dans la source de la page.</span><span class="sxs-lookup"><span data-stu-id="05a6d-252">**Source Order Viewer** is an experiment that displays the order of elements in the page source.</span></span>  <span data-ttu-id="05a6d-253">L’ordre de l’affichage à l’écran risque de différer de l’ordre de la source, ce qui déconcerte le lecteur d’écran et les utilisateurs du clavier.</span><span class="sxs-lookup"><span data-stu-id="05a6d-253">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="05a6d-254">Utilisez l’expérience de la **visionneuse de commandes sources** pour trouver les différences entre l’ordre d’affichage à l’écran et l’ordre de la source.</span><span class="sxs-lookup"><span data-stu-id="05a6d-254">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="05a6d-255">Après avoir activé l’expérience, assurez-vous de redémarrer l’DevTools.</span><span class="sxs-lookup"><span data-stu-id="05a6d-255">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="05a6d-256">Pour utiliser la **visionneuse de commandes sources**, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="05a6d-256">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="05a6d-257">Ouvrir le volet des **éléments** .</span><span class="sxs-lookup"><span data-stu-id="05a6d-257">Open the **Elements** pane.</span></span>  
1.  <span data-ttu-id="05a6d-258">Ouvrez le volet **accessibilité** dans le panneau du tiroir.</span><span class="sxs-lookup"><span data-stu-id="05a6d-258">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="05a6d-259">Dans la section **visionneuse de commandes sources** , activez la case à cocher **afficher l’ordre source** .</span><span class="sxs-lookup"><span data-stu-id="05a6d-259">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="05a6d-260">Mettez en surbrillance un élément HTML pour afficher une superposition de l’ordre dans la source de la page.</span><span class="sxs-lookup"><span data-stu-id="05a6d-260">Highlight any HTML element to display an overlay that the order in the page source.</span></span>  
    
:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Visionneuse de commandes source dans le volet accessibilité" lightbox="./media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="05a6d-262">**Visionneuse de commandes source** dans le volet **accessibilité**</span><span class="sxs-lookup"><span data-stu-id="05a6d-262">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <span data-ttu-id="05a6d-263">Activer l’éditeur de raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="05a6d-263">Enable keyboard shortcut editor</span></span>

<span data-ttu-id="05a6d-264">Lorsque l’expérience d’activation de l' **éditeur de raccourcis clavier** est activée, vous pouvez désormais personnaliser les raccourcis clavier pour n’importe quelle action dans le devtools.</span><span class="sxs-lookup"><span data-stu-id="05a6d-264">With the **Enable keyboard shortcut editor** experiment turned on, you are now able to customize keyboard shortcuts for any action in the DevTools.</span></span>  <span data-ttu-id="05a6d-265">Pour personnaliser le raccourci clavier pour une action spécifique, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="05a6d-265">To customize the keyboard shortcut for a specific action, complete the following steps.</span></span>  

1.  <span data-ttu-id="05a6d-266">[Ouvrez devtools][DevtoolsOpenMain].</span><span class="sxs-lookup"><span data-stu-id="05a6d-266">[Open DevTools][DevtoolsOpenMain].</span></span>  
1.  <span data-ttu-id="05a6d-267">Ouvrez [paramètres][DevToolsCustomizeSettings].</span><span class="sxs-lookup"><span data-stu-id="05a6d-267">Open [Settings][DevToolsCustomizeSettings].</span></span>
    *   <span data-ttu-id="05a6d-268">Sélectionnez `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="05a6d-268">Select `Shift`+`?`.</span></span>  
1.  <span data-ttu-id="05a6d-269">Accédez à la page **raccourcis** .</span><span class="sxs-lookup"><span data-stu-id="05a6d-269">Navigate to the **Shortcuts** page.</span></span>  
1.  <span data-ttu-id="05a6d-270">Choisissez l’action que vous voulez personnaliser.</span><span class="sxs-lookup"><span data-stu-id="05a6d-270">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="05a6d-271">Cliquez sur l’icône **Edit** \ ( ![ EditKeyboardShortcut ][ImageEditKeyboardShortcutIcon] \).</span><span class="sxs-lookup"><span data-stu-id="05a6d-271">Choose the **Edit** \(![EditKeyboardShortcut][ImageEditKeyboardShortcutIcon]\) icon.</span></span>  
    
    :::image type="complex" source="./media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Sélectionner l’action à personnaliser dans la page raccourcis dans les paramètres" lightbox="./media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       <span data-ttu-id="05a6d-273">Sélectionner l’action à personnaliser dans la page **raccourcis** dans les [paramètres][DevToolsCustomizeSettings]</span><span class="sxs-lookup"><span data-stu-id="05a6d-273">Choose the action to customize from the **Shortcuts** page in [Settings][DevToolsCustomizeSettings]</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="05a6d-274">Sur le clavier, sélectionnez les touches que vous souhaitez lier à l’action.</span><span class="sxs-lookup"><span data-stu-id="05a6d-274">On the keyboard, select the keys you want to bind to the action.</span></span>
    
    :::image type="complex" source="./media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Sélectionner les touches que vous voulez affecter à l’action" lightbox="./media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="05a6d-276">Sélectionner les touches que vous voulez affecter à l’action</span><span class="sxs-lookup"><span data-stu-id="05a6d-276">Select the keys you want to assign to the action</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="05a6d-277">Pour enregistrer votre nouveau raccourci clavier, activez la case à cocher</span><span class="sxs-lookup"><span data-stu-id="05a6d-277">To save your new keyboard shortcut, choose the checkmark \(</span></span>![CheckmarkKeyboardShortcut][ImageCheckmarkKeyboardShortcutIcon]<span data-ttu-id="05a6d-279">\) icône.</span><span class="sxs-lookup"><span data-stu-id="05a6d-279">\) icon.</span></span>
    
    :::image type="complex" source="./media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Cliquez sur l’icône de coche pour enregistrer votre nouveau raccourci clavier" lightbox="./media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="05a6d-281">Cliquez sur l’icône de coche pour enregistrer votre nouveau raccourci clavier</span><span class="sxs-lookup"><span data-stu-id="05a6d-281">Choose the checkmark icon to save your new keyboard shortcut</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="05a6d-282">Sélectionnez votre nouveau raccourci clavier pour déclencher l’action dans le DevTools.</span><span class="sxs-lookup"><span data-stu-id="05a6d-282">Select your new keyboard shortcut to trigger the action in the DevTools.</span></span>  
    
<span data-ttu-id="05a6d-283">Sur la page **raccourcis** , l’icône du **raccourci clavier personnalisé** \ ( ![ CustomKeyboardShortcut ][ImageCustomKeyboardShortcutIcon] \) affiche les raccourcis clavier que vous avez personnalisés.</span><span class="sxs-lookup"><span data-stu-id="05a6d-283">On the **Shortcuts** page, the **Custom Keyboard Shortcut** \(![CustomKeyboardShortcut][ImageCustomKeyboardShortcutIcon]\) icon displays keyboard shortcuts that you have customized.</span></span>  <span data-ttu-id="05a6d-284">Pour rétablir tous les raccourcis, sélectionnez **rétablir les raccourcis par défaut**.</span><span class="sxs-lookup"><span data-stu-id="05a6d-284">To reset all shortcuts, choose **Restore default shortcuts**.</span></span>  

<span data-ttu-id="05a6d-285">Lorsque vous modifiez les raccourcis clavier pour une action, pour ignorer vos modifications, sélectionnez l’icône X \ ( ![ XKeyboardShortcut ][ImageXKeyboardShortcutIcon] \).</span><span class="sxs-lookup"><span data-stu-id="05a6d-285">When you are editing the keyboard shortcuts for an action, to discard your changes, choose the X \(![XKeyboardShortcut][ImageXKeyboardShortcutIcon]\) icon.</span></span>  <span data-ttu-id="05a6d-286">Pour supprimer les raccourcis pour une action spécifique, sélectionnez l’icône **supprimer le raccourci** \ ( ![ DeleteKeyboardShortcut ][ImageDeleteKeyboardShortcutIcon] \).</span><span class="sxs-lookup"><span data-stu-id="05a6d-286">To remove shortcuts for a specific action, choose the **Delete shortcut** \(![DeleteKeyboardShortcut][ImageDeleteKeyboardShortcutIcon]\) icon.</span></span>  <span data-ttu-id="05a6d-287">Pour ajouter plusieurs raccourcis pour une action, sélectionnez **Ajouter un raccourci**.</span><span class="sxs-lookup"><span data-stu-id="05a6d-287">To add multiple shortcuts for an action, choose **Add a shortcut**.</span></span>

> [!NOTE]
> <span data-ttu-id="05a6d-288">Si un raccourci clavier est actuellement affecté à une autre action, vous ne pouvez pas l’enregistrer pour une nouvelle action.</span><span class="sxs-lookup"><span data-stu-id="05a6d-288">If a keyboard shortcut is currently assigned to another action, you are not able to save it for a new action.</span></span>  <span data-ttu-id="05a6d-289">Vous devez d’abord supprimer le raccourci clavier pour l’action précédente, puis l’ajouter à la nouvelle action.</span><span class="sxs-lookup"><span data-stu-id="05a6d-289">You must first delete the keyboard shortcut for the previous action and then add it to the new action.</span></span>  

<!--Available in Microsoft Edge version 87 and later.  -->

### <span data-ttu-id="05a6d-290">Activer les calques composites dans l’affichage 3D</span><span class="sxs-lookup"><span data-stu-id="05a6d-290">Turn on Composited Layers in 3D View</span></span>

<span data-ttu-id="05a6d-291">Il est possible que vous souhaitiez visualiser des couches en plus des index z et du modèle d’objet document (DOM).</span><span class="sxs-lookup"><span data-stu-id="05a6d-291">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="05a6d-292">Cette fonctionnalité vous permet de déboguer sans basculer entre les contextes.</span><span class="sxs-lookup"><span data-stu-id="05a6d-292">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="05a6d-293">Vous avez identifié que le changement de contexte de réduction était un point essentiel.</span><span class="sxs-lookup"><span data-stu-id="05a6d-293">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="05a6d-294">Il n’est pas toujours évident de savoir comment le code que vous écrivez affecte votre application Web.</span><span class="sxs-lookup"><span data-stu-id="05a6d-294">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="05a6d-295">Pour une interface de débogage complète, l’affichage 3D et les couches composites sont désormais combinés.</span><span class="sxs-lookup"><span data-stu-id="05a6d-295">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  <span data-ttu-id="05a6d-296">Après avoir activé l’expérience, assurez-vous de redémarrer l’DevTools.</span><span class="sxs-lookup"><span data-stu-id="05a6d-296">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="05a6d-297">Pour utiliser des **couches composites**, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="05a6d-297">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="05a6d-298">Sur le tiroir, sélectionnez l’outil **affichage 3D** .</span><span class="sxs-lookup"><span data-stu-id="05a6d-298">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="05a6d-299">Ouvrez le volet **couches composites** .</span><span class="sxs-lookup"><span data-stu-id="05a6d-299">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="05a6d-300">Toutes les couches peintes de l’application sont affichées.</span><span class="sxs-lookup"><span data-stu-id="05a6d-300">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="05a6d-301">Essayez cette fonctionnalité avec vos propres applications Web.</span><span class="sxs-lookup"><span data-stu-id="05a6d-301">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="./media/experiments-layers.msft.png" alt-text="Volet couches composites" lightbox="./media/experiments-layers.msft.png":::
   <span data-ttu-id="05a6d-303">Volet **couches composites**</span><span class="sxs-lookup"><span data-stu-id="05a6d-303">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

## <span data-ttu-id="05a6d-304">Fonctionnalités expérimentales antérieures</span><span class="sxs-lookup"><span data-stu-id="05a6d-304">Previous experimental features</span></span>  

*   <span data-ttu-id="05a6d-305">la [vue 3D][Devtools3dViewIndex] est désormais disponible et activée par défaut dans Microsoft Edge version 83 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="05a6d-305">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="05a6d-306">La [Personnalisation des raccourcis clavier][DevtoolsCustomKeyboardShortcuts] est désormais disponible et activée par défaut dans Microsoft Edge version 86 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="05a6d-306">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  

## <span data-ttu-id="05a6d-307">Fourniture de commentaires sur les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="05a6d-307">Providing feedback on experimental features</span></span>  

<span data-ttu-id="05a6d-308">Pour transmettre des commentaires sur les expériences DevTools Microsoft Edge, ou tout autre élément associé à DevTools.</span><span class="sxs-lookup"><span data-stu-id="05a6d-308">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="05a6d-309">Envoyez vos commentaires à l’aide de l’icône **Envoyer des commentaires** dans le devtools</span><span class="sxs-lookup"><span data-stu-id="05a6d-309">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="05a6d-310">Tweeter sur [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="05a6d-310">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Icône Envoyer des commentaires dans Microsoft Edge DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="05a6d-312">Icône **Envoyer des commentaires** dans Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="05a6d-312">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  
-->  

<!-- image links -->  

[ImageRotateIcon]: ./media/rotate-dark-icon.msft.png  
[ImageSpanIcon]: ./media/span-dark-icon.msft.png  
[ImageExperimentalApisIcon]: ./media/experimental-apis-dark-icon.msft.png  
[ImageEditKeyboardShortcutIcon]: ./media/edit-keyboard-shortcut-icon.msft.png  
[ImageCheckmarkKeyboardShortcutIcon]: ./media/checkmark-keyboard-shortcut-icon.msft.png  
[ImageCustomKeyboardShortcutIcon]: ./media/custom-keyboard-shortcut-icon.msft.png  
[ImageDeleteKeyboardShortcutIcon]: ./media/delete-keyboard-shortcut-icon.msft.png  
[ImageXKeyboardShortcutIcon]: ./media/discard-changes-keyboard-shortcut-icon.msft.png  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Affichage 3D | Documents Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ./device-mode/index.md#simulate-a-mobile-viewport "Simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsIssues]: ./issues/index.md "Recherchez et corrigez les problèmes liés à l’outil problèmes dans Microsoft Edge DevTools Documents Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Raccourcis clavier dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsOpen]: ./open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomKeyboardShortcuts]: ./customize/shortcuts.md "Personnaliser les raccourcis clavier dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsOpenMain]: ./open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[DualScreenWebIndex]: /dual-screen/web/index "Expérience Web sur deux écrans | Documents Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtenez l’émulateur Duo surface | Documents Microsoft"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Comment utiliser la couture-Introduction aux périphériques à écran double Documents Microsoft"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Utiliser l’émulateur de surface Duo | Documents Microsoft"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Fonctionnalité de répartition d’écran de média CSS pour la détection sur deux écrans | Documents Microsoft"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments pour les appareils à deux écrans | Documents Microsoft"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clients Bureau à distance | Documents Microsoft"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Pli Galaxy | Magnétoscope"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "Astuce"  
