---
description: Dernières fonctionnalités expérimentales de Microsoft Edge DevTools
title: Fonctionnalités expérimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, expérience
ms.openlocfilehash: ce8388e8065055e6002bd8541101bef658c7a403
ms.sourcegitcommit: 744e2ecf42bcc427ae33e5dadbf6cd48ee0ab6a5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2020
ms.locfileid: "11016744"
---
# <span data-ttu-id="9be18-104">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="9be18-104">Experimental features</span></span>  

<span data-ttu-id="9be18-105">Microsoft Edge DevTools fournit l’accès à des fonctionnalités expérimentales toujours en développement.</span><span class="sxs-lookup"><span data-stu-id="9be18-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="9be18-106">Vous pouvez tester et envoyer des[Commentaires](#providing-feedback-on-experimental-features) avant la sortie de chaque fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="9be18-106">You may test and p[provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="9be18-107">Si les fonctionnalités expérimentales sont disponibles dans tous les canaux de Microsoft Edge, vous pouvez obtenir les dernières fonctionnalités expérimentales à l’aide du canal des Canaries Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9be18-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="9be18-108">Activer les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="9be18-108">Turn on experimental features</span></span>  

<span data-ttu-id="9be18-109">Procédez comme suit pour activer ou désactiver les fonctionnalités expérimentales dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9be18-109">Use the following steps to turn on \(or off\) experimental features in Microsoft Edge.</span></span>  

1.  <span data-ttu-id="9be18-110">[Ouvrez devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="9be18-110">[Open DevTools][DevtoolsOpen].</span></span>  
     *   <span data-ttu-id="9be18-111">Sélectionnez `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="9be18-111">Select `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="9be18-112">Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="9be18-112">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="9be18-113">Ouvrez le volet [paramètres][DevToolsCustomizeSettings] .</span><span class="sxs-lookup"><span data-stu-id="9be18-113">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="9be18-114">Sélectionnez `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="9be18-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="9be18-115">Pour plus d’informations, accédez à [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="9be18-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="9be18-116">Sur le côté gauche du volet **paramètres** , sélectionnez la section **expériences** .</span><span class="sxs-lookup"><span data-stu-id="9be18-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.msft.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/experiments-devtools.msft.png":::
       <span data-ttu-id="9be18-118">Liste des expériences dans les paramètres de DevTools</span><span class="sxs-lookup"><span data-stu-id="9be18-118">List of experiments in DevTools Settings</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9be18-119">Sur la page **expériences** , faites défiler la liste de toutes les fonctionnalités expérimentales disponibles, puis cochez la case en regard de chaque fonctionnalité que vous voulez tester.</span><span class="sxs-lookup"><span data-stu-id="9be18-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="9be18-120">Fermez et rouvrez Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="9be18-120">Close and reopen Microsoft Edge DevTools.</span></span>  

> [!NOTE]
> <span data-ttu-id="9be18-121">Les fonctionnalités expérimentales sont constamment mises à jour et peuvent entraîner des problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="9be18-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="9be18-122">Pour désactiver une fonctionnalité expérimentale, ouvrez la page **expériences** , puis décochez la case de la fonctionnalité expérimental que vous souhaitez désactiver.</span><span class="sxs-lookup"><span data-stu-id="9be18-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="9be18-123">Fonctionnalités expérimentales mises en évidence</span><span class="sxs-lookup"><span data-stu-id="9be18-123">Highlighted experimental features</span></span>  

<span data-ttu-id="9be18-124">Les sections suivantes décrivent les nouvelles fonctionnalités expérimentales disponibles dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9be18-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="9be18-125">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="9be18-125">Experimental feature</span></span> | <span data-ttu-id="9be18-126">Version de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9be18-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="9be18-127">Émulation: prise en charge du mode double écran</span><span class="sxs-lookup"><span data-stu-id="9be18-127">Emulation: Support dual screen mode</span></span>](#emulation-support-dual-screen-mode) | <span data-ttu-id="9be18-128">84 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9be18-128">84 or later</span></span> |  
| [<span data-ttu-id="9be18-129">Activer les nouvelles fonctionnalités de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="9be18-129">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="9be18-130">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9be18-130">85 or later</span></span> |  
| [<span data-ttu-id="9be18-131">Activer la prise en charge du déplacement des onglets entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="9be18-131">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="9be18-132">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9be18-132">85 or later</span></span> |  
| [<span data-ttu-id="9be18-133">Activer webhint</span><span class="sxs-lookup"><span data-stu-id="9be18-133">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="9be18-134">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9be18-134">85 or later</span></span> |  
| [<span data-ttu-id="9be18-135">Activer la console réseau</span><span class="sxs-lookup"><span data-stu-id="9be18-135">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="9be18-136">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9be18-136">85 or later</span></span> |  
| [<span data-ttu-id="9be18-137">Activer la visionneuse de commandes sources</span><span class="sxs-lookup"><span data-stu-id="9be18-137">Enable Source Order Viewer</span></span>](#enable-source-order-viewer) | <span data-ttu-id="9be18-138">86 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9be18-138">86 or later</span></span> |  

### <span data-ttu-id="9be18-139">Émulation: prise en charge du mode double écran</span><span class="sxs-lookup"><span data-stu-id="9be18-139">Emulation: Support dual screen mode</span></span>  

<span data-ttu-id="9be18-140">Fournit des fonctionnalités supplémentaires pour l’émulation de deux nouveaux périphériques à écran double et pliant dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9be18-140">Provides additional features for emulating two new dual-screen and foldable devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="9be18-141">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="9be18-141">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="9be18-142">Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="9be18-142">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  

<span data-ttu-id="9be18-143">Émuler les appareils et basculer entre les positions suivantes.</span><span class="sxs-lookup"><span data-stu-id="9be18-143">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="9be18-144">un écran ou une position pliée</span><span class="sxs-lookup"><span data-stu-id="9be18-144">single-screen or folded posture</span></span>  
*   <span data-ttu-id="9be18-145">position à deux écrans ou dépliées</span><span class="sxs-lookup"><span data-stu-id="9be18-145">dual-screen or unfolded posture</span></span>  
 
<span data-ttu-id="9be18-146">[Activez les API de plateforme Web expérimentales](#enable-experimental-apis) et utilisez la [fonctionnalité de répartition d’écran de média CSS][DualScreenDocsCssMedia] et l' [API getWindowSegments JavaScript][DualScreenDocsJSAPI] pour améliorer votre site Web \ (ou l’application \) pour les appareils à double écran et pliant.</span><span class="sxs-lookup"><span data-stu-id="9be18-146">[Enable experimental Web Platform APIs](#enable-experimental-apis) and use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI] to enhance your website \(or app\) for dual-screen and foldable devices.</span></span>

:::image type="complex" source="./media/experiments-surface-duo-emulation.msft.png" alt-text="Émuler surface duo dans Microsoft Edge" lightbox="./media/experiments-surface-duo-emulation.msft.png":::  
   <span data-ttu-id="9be18-148">Émuler surface duo dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9be18-148">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

#### <span data-ttu-id="9be18-149">Activer les API expérimentales</span><span class="sxs-lookup"><span data-stu-id="9be18-149">Enable experimental APIs</span></span>  

<span data-ttu-id="9be18-150">Pour utiliser la [fonctionnalité de répartition d’écran de média CSS][DualScreenDocsCssMedia] et l' [API getWindowSegments JavaScript][DualScreenDocsJSAPI], activez l' `Experimental Web Platform features` indicateur dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9be18-150">To use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI], turn on the `Experimental Web Platform features` flag in Microsoft Edge.</span></span>  <span data-ttu-id="9be18-151">Procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="9be18-151">Complete the following steps.</span></span>

1.  <span data-ttu-id="9be18-152">Accédez à `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="9be18-152">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="9be18-153">Dans la zone de texte **indicateurs de recherche** , entrez `Experimental Web Platform features` , sélectionnez l’indicateur **fonctionnalités de plateforme Web expérimentales** , puis **désactivez** l' **option**désactivé.</span><span class="sxs-lookup"><span data-stu-id="9be18-153">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="9be18-154">Redémarrez MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="9be18-154">Restart Microsoft Edge.</span></span>  

:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Activer l’indicateur de fonctionnalités de plateforme Web expérimentale" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="9be18-156">Activer l’indicateur de fonctionnalités de plateforme Web expérimentale</span><span class="sxs-lookup"><span data-stu-id="9be18-156">Enable the Experimental Web Platform features flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="9be18-157">Si vous utilisez des [requêtes multimédias CSS][DualScreenDocsCssMedia] ou l’API d' [énumération de segment Windows JavaScript][DualScreenDocsJSAPI] pour améliorer votre site Web ou votre application pour le duo de [surface][SurfaceDevicesDuo], vous devez également activer l' [Android Microsoft Edge app][GooglePlayMicrosoftEdge] indicateur de **fonctionnalités de plateforme Web** [Surface Duo][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="9be18-157">If you are using [CSS media queries][DualScreenDocsCssMedia] or the [JavaScript Windows Segment Enumeration API][DualScreenDocsJSAPI] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also enable the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>
> 
> <span data-ttu-id="9be18-158">Si l’indicateur fonctionnalités de la **plateforme Web expérimentée** est activé dans la version de [Bureau de Microsoft Edge][MicrosoftEdge] et désactivée dans l' [application Microsoft Edge pour Android][GooglePlayMicrosoftEdge], le comportement de votre site Web ou de votre application dans l’émulateur de surface duo dans l’application de bureau Microsoft Edge ne correspond pas à l' [application Microsoft Edge pour Android][GooglePlayMicrosoftEdge] sur [surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="9be18-158">If the **Experimental Web Platform features** flag is enabled in [desktop Microsoft Edge][MicrosoftEdge] and disabled in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge will not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="9be18-159">Assurez-vous que les indicateurs sont mis en correspondance entre Android et Microsoft Edge pour pouvoir utiliser l’émulateur de surface duo dans [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="9be18-159">Ensure that the flags are matching across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

#### <span data-ttu-id="9be18-160">Tests sur des appareils à écran double et pliant</span><span class="sxs-lookup"><span data-stu-id="9be18-160">Testing on foldable and dual-screen devices</span></span>  

<span data-ttu-id="9be18-161">Lorsque vous émulez le [duo de surface][SurfaceDevicesDuo] dans une position sur deux écrans dans Microsoft Edge, la couture (espace entre les deux écrans \) est tracée sur votre site Web ou votre application.</span><span class="sxs-lookup"><span data-stu-id="9be18-161">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the seam \(the space between the two screens\) is drawn over your website or app.</span></span>  

<span data-ttu-id="9be18-162">L’affichage émulé correspond au mode d’affichage de votre site Web (ou de l’application) dans l' [application Microsoft Edge Android][GooglePlayMicrosoftEdge] sur [surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="9be18-162">The emulated display matches the way your website \(or app\) will render in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="9be18-163">Il est possible que vous deviez mettre à jour votre site Web \ (ou l’application \) pour l’afficher mieux le long de la couture.</span><span class="sxs-lookup"><span data-stu-id="9be18-163">You may have to update your website \(or app\) to display better along the seam.</span></span>  <span data-ttu-id="9be18-164">Pour plus d’informations sur l’adaptation de votre site Web (ou de l’application \) à la couture, accédez à l' [utilisation de la couture][DualScreenIntroductionHowWorkSeam] dans la documentation surface Duo.</span><span class="sxs-lookup"><span data-stu-id="9be18-164">For more information about adapting your website \(or app\) to the seam, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam] in the Surface Duo documentation.</span></span>  

<span data-ttu-id="9be18-165">La [barre d’outils][DevtoolsDeviceModeIndexSimulateMobileViewport] de l’appareil inclut des fonctionnalités supplémentaires pour vous aider à tester votre site Web ou votre application en plusieurs positions et orientations.</span><span class="sxs-lookup"><span data-stu-id="9be18-165">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="9be18-166">Sélectionnez **faire pivoter** \ ( ![ faire pivoter ][ImageRotateIcon] ) pour faire pivoter la fenêtre d’affichage en orientation paysage.</span><span class="sxs-lookup"><span data-stu-id="9be18-166">Choose **Rotate** \(![Rotate][ImageRotateIcon]\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="9be18-167">Combinez la fonctionnalité avec la **plage** \ ( ![ span ][ImageSpanIcon] \) pour basculer entre les positions à un seul écran ou pliées en deux ou non pliées.</span><span class="sxs-lookup"><span data-stu-id="9be18-167">Combine the feature with **Span** \(![Span][ImageSpanIcon]\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="9be18-168">Ensemble, les fonctionnalités permettent le test de votre site Web ou de votre application dans les quatre positions et orientations possibles.</span><span class="sxs-lookup"><span data-stu-id="9be18-168">Together, the features enable testing your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matrice de positions et d’orientations pour les appareils à écran double et pliant" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="9be18-170">Matrice de positions et d’orientations pour les appareils à écran double et pliant</span><span class="sxs-lookup"><span data-stu-id="9be18-170">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="9be18-171">Les **fonctionnalités de la plateforme Web expérimentales** \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \) affichent l’état de l’indicateur de **fonctionnalités de plateforme Web expérimentale** .</span><span class="sxs-lookup"><span data-stu-id="9be18-171">The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="9be18-172">Si l’indicateur est activé, l’icône est mise en évidence.</span><span class="sxs-lookup"><span data-stu-id="9be18-172">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="9be18-173">Si l’indicateur est désactivé, l’icône n’est pas mise en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="9be18-173">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="9be18-174">Pour activer \ (ou désactivé) l’indicateur, accédez à l’indicateur `edge://flags` et activez-le.</span><span class="sxs-lookup"><span data-stu-id="9be18-174">To turn on \(or off\) the flag, navigate to `edge://flags` and toggle the flag.</span></span>  

<!-- Commenting out until the icon issue is fixed in Edge Canary
The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.  If the flag is turned on, the icon is highlighted.  If the flag is turned off, the icon is not highlighted.  To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.   -->

<span data-ttu-id="9be18-175">Voici d’autres ressources qui peuvent vous aider à améliorer votre site Web \ (ou l’application \) pour les périphériques à deux écrans:</span><span class="sxs-lookup"><span data-stu-id="9be18-175">Here are additional resources that may help you enhance your website \(or app\) for dual-screen devices:</span></span>
*   <span data-ttu-id="9be18-176">Pour plus d’informations sur le développement Web sur les appareils à deux écrans, voir [expériences sur le Web à deux écrans][DualScreenWebIndex].</span><span class="sxs-lookup"><span data-stu-id="9be18-176">For more information about web development on dual-screen devices, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="9be18-177">Installez l' [émulateur de surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="9be18-177">Install the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="9be18-178">Il est différent de l’émulateur dans Microsoft Edge, émule le duo de surface sur lequel s’exécute Android et intégré à [Android Studio][AndroidDeveloperStudio].</span><span class="sxs-lookup"><span data-stu-id="9be18-178">It is different from the emulator in Microsoft Edge, emulates the Surface Duo running Android, and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="9be18-179">Pour plus d’informations, accédez au [Kit de développement logiciel (SDK) surface Duo][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="9be18-179">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

> [!NOTE]
> <span data-ttu-id="9be18-180">Vous trouverez ci-dessous la liste des problèmes connus actuellement:</span><span class="sxs-lookup"><span data-stu-id="9be18-180">The following is a list of current known issues:</span></span>
> *   <span data-ttu-id="9be18-181">Lorsque vous utilisez un [client de bureau à distance Microsoft][RemoteDesktopClientDocs] pour vous connecter à un PC distant et émuler le pli de [surface Duo][SurfaceDevicesDuo] ou [Samsung Galaxy][SamsungMobileGalaxyFold], le pointeur risque de secouer ou d’interruption.</span><span class="sxs-lookup"><span data-stu-id="9be18-181">When using a [Microsoft Remote Desktop client][RemoteDesktopClientDocs] to connect to a remote PC and emulate the [Surface Duo][SurfaceDevicesDuo] or [Samsung Galaxy Fold][SamsungMobileGalaxyFold], the pointer may shake or stutter.</span></span>  <span data-ttu-id="9be18-182">Si vous rencontrez ce problème, [envoyez des commentaires](#providing-feedback-on-experimental-features).</span><span class="sxs-lookup"><span data-stu-id="9be18-182">If you run into this issue, [send feedback](#providing-feedback-on-experimental-features).</span></span>  

### <span data-ttu-id="9be18-183">Activer les nouvelles fonctionnalités de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="9be18-183">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="9be18-184">Permet d’améliorer les visualisations sur la page lorsque vous déboguez des sites Web dotés de dispositions CSS.</span><span class="sxs-lookup"><span data-stu-id="9be18-184">Improves on-page visualizations when you debug websites that have CSS grid layouts.</span></span>  <span data-ttu-id="9be18-185">Vous pouvez personnaliser davantage les superpositions dans les paramètres de DevTools.</span><span class="sxs-lookup"><span data-stu-id="9be18-185">You may further customize the overlays in DevTools Settings.</span></span>  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="Fonctionnalité de débogage de grille CSS" lightbox="./media/experiments-grid.msft.png":::
   <span data-ttu-id="9be18-187">Fonctionnalité de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="9be18-187">CSS grid debugging feature</span></span>  
:::image-end:::  

<span data-ttu-id="9be18-188">Pour afficher un aperçu des dernières fonctionnalités expérimentales, effectuez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="9be18-188">To preview the latest experimental features, complete the following actions.</span></span>  

1.  <span data-ttu-id="9be18-189">Dans la section **expériences** , sélectionnez l’option **activer les nouvelles fonctionnalités de débogage de grille CSS (options de configuration disponibles dans le volet barre latérale des éléments après le redémarrage)** .</span><span class="sxs-lookup"><span data-stu-id="9be18-189">In the **Experiments** section, choose the **Enable new CSS Grid debugging features (configuration options available in Layout sidebar pane in Elements after restart)** checkbox.</span></span>  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="9be18-190">Activer la prise en charge du déplacement des onglets entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="9be18-190">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="9be18-191">En règle générale, il est possible que les outils tels que les **éléments** et le **réseau** s’ouvrent uniquement dans le panneau principal qui se trouve en haut du devtools.</span><span class="sxs-lookup"><span data-stu-id="9be18-191">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="9be18-192">Outils tels que l' **affichage 3D** et les **problèmes** qui s’ouvrent normalement uniquement dans le panneau du **tiroir** situé en bas du devtools.</span><span class="sxs-lookup"><span data-stu-id="9be18-192">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="9be18-193">Après avoir choisi l’expérience, vous pouvez déplacer des outils entre les volets supérieur et inférieur.</span><span class="sxs-lookup"><span data-stu-id="9be18-193">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="9be18-194">Pour déplacer un outil, pointez sur celui-ci, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **déplacer vers le haut** ou **déplacer vers le bas**.</span><span class="sxs-lookup"><span data-stu-id="9be18-194">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="9be18-195">Cette expérience vous permet de personnaliser la disposition de votre DevTools.</span><span class="sxs-lookup"><span data-stu-id="9be18-195">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="9be18-196">Pour afficher ou masquer le panneau de la **tiroir** , sélectionnez `Escape` .</span><span class="sxs-lookup"><span data-stu-id="9be18-196">To show or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Déplacement d’un onglet entre les panneaux" lightbox="./media/experiments-move-panels.msft.png":::
   <span data-ttu-id="9be18-198">Déplacement d’un onglet entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="9be18-198">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="9be18-199">Activer webhint</span><span class="sxs-lookup"><span data-stu-id="9be18-199">Enable webhint</span></span>  

<span data-ttu-id="9be18-200">[webhint][WebhintMain] est un outil open source qui fournit des commentaires en temps réel sur les sites Web et les pages Web locales.</span><span class="sxs-lookup"><span data-stu-id="9be18-200">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local web pages.</span></span>  <span data-ttu-id="9be18-201">Type de commentaires fourni par [webhint][WebhintMain].</span><span class="sxs-lookup"><span data-stu-id="9be18-201">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="9be18-202">accessibilité</span><span class="sxs-lookup"><span data-stu-id="9be18-202">accessibility</span></span>  
*   <span data-ttu-id="9be18-203">compatibilité entre les navigateurs</span><span class="sxs-lookup"><span data-stu-id="9be18-203">cross-browser compatibility</span></span>  
*   <span data-ttu-id="9be18-204">sécurité</span><span class="sxs-lookup"><span data-stu-id="9be18-204">security</span></span>  
*   <span data-ttu-id="9be18-205">les</span><span class="sxs-lookup"><span data-stu-id="9be18-205">performance</span></span>  
*   <span data-ttu-id="9be18-206">PWA</span><span class="sxs-lookup"><span data-stu-id="9be18-206">PWAs</span></span>  
*   <span data-ttu-id="9be18-207">autres problèmes courants liés au développement Web</span><span class="sxs-lookup"><span data-stu-id="9be18-207">other common web development issues</span></span>  

<span data-ttu-id="9be18-208">L’expérience [webhint][WebhintMain] affiche le commentaire de webhint dans le volet [problèmes][DevtoolsIssues] .</span><span class="sxs-lookup"><span data-stu-id="9be18-208">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="9be18-209">Sélectionnez un problème pour afficher la documentation de la solution et une liste des ressources affectées sur votre site Web.</span><span class="sxs-lookup"><span data-stu-id="9be18-209">Select an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="9be18-210">Sélectionnez un lien vers une ressource pour ouvrir le volet **réseau**, **sources**ou **éléments** approprié dans devtools.</span><span class="sxs-lookup"><span data-stu-id="9be18-210">Select a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="Commentaires de webhint dans le volet problèmes" lightbox="./media/experiments-webhint.msft.png":::
   <span data-ttu-id="9be18-212">Commentaires de webhint dans le volet **problèmes**</span><span class="sxs-lookup"><span data-stu-id="9be18-212">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="9be18-213">Activer la console réseau</span><span class="sxs-lookup"><span data-stu-id="9be18-213">Enable Network Console</span></span>  

<span data-ttu-id="9be18-214">**Network console** est le titre d’une expérience visant à faire des requêtes réseau synthétiques sur http.</span><span class="sxs-lookup"><span data-stu-id="9be18-214">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="9be18-215">Vous pouvez utiliser l’expérience de la **console réseau** pour envoyer des demandes d’API Web.</span><span class="sxs-lookup"><span data-stu-id="9be18-215">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="9be18-216">Après avoir activé l’expérience, assurez-vous de redémarrer l’DevTools.</span><span class="sxs-lookup"><span data-stu-id="9be18-216">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="9be18-217">Pour utiliser la **console réseau**, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="9be18-217">To use the **Network Console**, use the following steps.</span></span>    

1.  <span data-ttu-id="9be18-218">Ouvrez le volet **réseau** .</span><span class="sxs-lookup"><span data-stu-id="9be18-218">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="9be18-219">Recherchez la demande réseau que vous souhaitez modifier et renvoyer.</span><span class="sxs-lookup"><span data-stu-id="9be18-219">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="9be18-220">Ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **modifier, puis relire**.</span><span class="sxs-lookup"><span data-stu-id="9be18-220">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="9be18-221">Lorsque la **console réseau** s’ouvre, modifiez les informations de requête réseau.</span><span class="sxs-lookup"><span data-stu-id="9be18-221">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="9be18-222">Sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="9be18-222">Select **Send**.</span></span>  

:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Console réseau dans le tiroir de la console" lightbox="./media/network-network-console.msft.png":::
   <span data-ttu-id="9be18-224">**Console réseau** dans le tiroir de la **console**</span><span class="sxs-lookup"><span data-stu-id="9be18-224">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="9be18-225">Activer la visionneuse de commandes sources</span><span class="sxs-lookup"><span data-stu-id="9be18-225">Enable Source Order Viewer</span></span>  

<span data-ttu-id="9be18-226">La **visionneuse de commandes source** est une expérience qui affiche l’ordre des éléments dans la source de la page.</span><span class="sxs-lookup"><span data-stu-id="9be18-226">**Source Order Viewer** is an experiment that displays the order of elements in the page source.</span></span>  <span data-ttu-id="9be18-227">L’ordre de l’affichage à l’écran risque de différer de l’ordre de la source, ce qui déconcerte le lecteur d’écran et les utilisateurs du clavier.</span><span class="sxs-lookup"><span data-stu-id="9be18-227">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="9be18-228">Utilisez l’expérience de la **visionneuse de commandes sources** pour trouver les différences entre l’ordre d’affichage à l’écran et l’ordre de la source.</span><span class="sxs-lookup"><span data-stu-id="9be18-228">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="9be18-229">Après avoir activé l’expérience, assurez-vous de redémarrer l’DevTools.</span><span class="sxs-lookup"><span data-stu-id="9be18-229">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="9be18-230">Pour utiliser la visionneuse de commandes source:</span><span class="sxs-lookup"><span data-stu-id="9be18-230">To use Source Order Viewer:</span></span>  

1.  <span data-ttu-id="9be18-231">Ouvrir le volet des **éléments** .</span><span class="sxs-lookup"><span data-stu-id="9be18-231">Open the **Elements** pane.</span></span>  
1.  <span data-ttu-id="9be18-232">Ouvrez le volet **accessibilité** dans le panneau du tiroir.</span><span class="sxs-lookup"><span data-stu-id="9be18-232">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="9be18-233">Dans la section **visionneuse de commandes sources** , activez la case à cocher **afficher l’ordre source** .</span><span class="sxs-lookup"><span data-stu-id="9be18-233">Under the **Source Order Viewer** section, select the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="9be18-234">Mettez en surbrillance un élément HTML pour afficher une superposition de l’ordre dans la source de la page.</span><span class="sxs-lookup"><span data-stu-id="9be18-234">Highlight any HTML element to display an overlay that the order in the page source.</span></span>  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Visionneuse de commandes source dans le volet accessibilité" lightbox="./media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="9be18-236">**Visionneuse de commandes source** dans le volet **accessibilité**</span><span class="sxs-lookup"><span data-stu-id="9be18-236">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## <span data-ttu-id="9be18-237">Fonctionnalités expérimentales antérieures</span><span class="sxs-lookup"><span data-stu-id="9be18-237">Previous experimental features</span></span>  

*   <span data-ttu-id="9be18-238">la [vue 3D][Devtools3dViewIndex] est désormais disponible et activée par défaut dans Microsoft Edge version 83 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9be18-238">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="9be18-239">La [Personnalisation des raccourcis clavier][DevtoolsCustomKeyboardShortcuts] est désormais disponible et activée par défaut dans Microsoft Edge version 86 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9be18-239">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  

## <span data-ttu-id="9be18-240">Fourniture de commentaires sur les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="9be18-240">Providing feedback on experimental features</span></span>  

<span data-ttu-id="9be18-241">Pour transmettre des commentaires sur les expériences DevTools Microsoft Edge, ou tout autre élément associé à DevTools.</span><span class="sxs-lookup"><span data-stu-id="9be18-241">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="9be18-242">Envoyez vos commentaires à l’aide de l’icône **Envoyer des commentaires** dans le devtools</span><span class="sxs-lookup"><span data-stu-id="9be18-242">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="9be18-243">Tweeter sur [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="9be18-243">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Icône Envoyer des commentaires dans Microsoft Edge DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="9be18-245">Icône **Envoyer des commentaires** dans Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="9be18-245">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  
-->  

<!-- image links -->  

[ImageRotateIcon]: ./media/rotate-dark-icon.msft.png  
[ImageSpanIcon]: ./media/span-dark-icon.msft.png  
[ImageExperimentalApisIcon]: ./media/experimental-apis-dark-icon.msft.png  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Affichage 3D | Documents Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ./device-mode/index.md#simulate-a-mobile-viewport "Simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsIssues]: ./issues/index.md "Recherchez et corrigez les problèmes liés à l’outil problèmes dans Microsoft Edge DevTools Documents Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Raccourcis clavier dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsOpen]: ./open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomKeyboardShortcuts]: ./customize/shortcuts.md "Personnaliser les raccourcis clavier dans Microsoft Edge DevTools | Documents Microsoft"

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
