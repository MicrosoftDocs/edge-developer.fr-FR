---
title: Nouveautés de DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: f07639d3c5cd246704f3d489c0e59714a938f13d
ms.sourcegitcommit: a5392ab44133d742c0e1fa500ad9a872989b7c3f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684805"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <span data-ttu-id="39556-103">Nouveautés de DevTools (Microsoft Edge 84)</span><span class="sxs-lookup"><span data-stu-id="39556-103">What's new in DevTools (Microsoft Edge 84)</span></span>  

## <span data-ttu-id="39556-104">Annonces de l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="39556-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="39556-105">Les sections suivantes répertorient les annonces que vous pouvez avoir manquées de l’équipe Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="39556-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="39556-106">Découvrez-les pour essayer de nouvelles fonctionnalités dans les extensions de code DevTools, VS, etc.</span><span class="sxs-lookup"><span data-stu-id="39556-106">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="39556-107">Pour vous tenir au courant de toutes les fonctionnalités les plus récentes et les plus récentes de vos outils de développement, téléchargez les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] et [Suivez-nous sur Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="39556-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="39556-108">Utiliser le DevTools en mode contraste élevé Windows</span><span class="sxs-lookup"><span data-stu-id="39556-108">Use the DevTools in Windows high contrast mode</span></span>

<span data-ttu-id="39556-109">Le DevTools de Microsoft Edge est désormais affiché en mode contraste élevé lorsque Windows est en mode contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="39556-109">The Microsoft Edge DevTools are now displayed in high contrast mode when Windows is in high contrast mode.</span></span>  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Microsoft Edge DevTools en mode de contraste élevé" lightbox="../../media/2020/05/high-contrast.msft.png":::
   <span data-ttu-id="39556-111">Microsoft Edge DevTools en mode de contraste élevé</span><span class="sxs-lookup"><span data-stu-id="39556-111">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="39556-112">[Suivez les instructions pour activer le mode contraste élevé dans Windows][MicrosoftSupportWindows10HighContrastMode].</span><span class="sxs-lookup"><span data-stu-id="39556-112">[Follow the instructions to turn on high contrast mode in Windows][MicrosoftSupportWindows10HighContrastMode].</span></span>  <span data-ttu-id="39556-113">Ouvrez le DevTools dans Microsoft Edge en appuyant sur `F12` ou `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="39556-113">Open the DevTools in Microsoft Edge by pressing `F12` or `Ctrl`+`Shift`+`I`.</span></span>  <span data-ttu-id="39556-114">Le DevTools est affiché en mode contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="39556-114">The DevTools are displayed in high contrast mode.</span></span>  

> [!NOTE]
> <span data-ttu-id="39556-115">Le Microsoft Edge DevTools prend actuellement en charge le mode de contraste élevé sur Windows, mais pas sur macOS.</span><span class="sxs-lookup"><span data-stu-id="39556-115">The Microsoft Edge DevTools currently support high contrast mode on Windows but not on macOS.</span></span> 

<span data-ttu-id="39556-116">[#1048378][CR1048378] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="39556-116">Chromium issue [#1048378][CR1048378]</span></span>  

### <span data-ttu-id="39556-117">Faire correspondre les raccourcis clavier du DevTools au code VS</span><span class="sxs-lookup"><span data-stu-id="39556-117">Match keyboard shortcuts in the DevTools to VS Code</span></span>  

<span data-ttu-id="39556-118">À partir de vos [Commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) et du suivi d’une [émission publique de chrome][CRIssuesList], l’équipe Microsoft Edge devtools a appris à la possibilité de personnaliser les raccourcis clavier dans devtools.</span><span class="sxs-lookup"><span data-stu-id="39556-118">From your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) and the [Chromium public issue tracker][CRIssuesList], the Microsoft Edge DevTools team learned that you wanted the ability to customize keyboard shortcuts in the DevTools.</span></span>  <span data-ttu-id="39556-119">Dans Microsoft Edge 84, vous pouvez maintenant faire correspondre les raccourcis clavier du DevTools au [code vs][VSCode], qui est uniquement l’une des fonctionnalités sur lesquelles l’équipe travaille pour la personnalisation du raccourci.</span><span class="sxs-lookup"><span data-stu-id="39556-119">In Microsoft Edge 84, you are now able to match keyboard shortcuts in the DevTools to [VS Code][VSCode], which is just one of the features the team is working on for shortcut customization.</span></span>  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code VS" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   <span data-ttu-id="39556-121">Microsoft Edge DevTools en mode de contraste élevé</span><span class="sxs-lookup"><span data-stu-id="39556-121">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="39556-122">Pour tester l’expérience, ouvrez DevTools paramètres en appuyant sur `?` ou en sélectionnant l' ![ icône d’icône Paramètres devtools ][ImageSettingsIcon] dans le coin supérieur droit du devtools.</span><span class="sxs-lookup"><span data-stu-id="39556-122">To try the experiment, open DevTools Settings by pressing `?` or selecting the ![DevTools Settings icon][ImageSettingsIcon] icon in the top-right corner of the DevTools.</span></span>  <span data-ttu-id="39556-123">Accédez à la section **expérimentations** et **activez l’option Activer l’onglet Paramètres des raccourcis clavier personnalisés (nécessite un recharge)**.</span><span class="sxs-lookup"><span data-stu-id="39556-123">Navigate to the **Experiments** section and check **Enable custom keyboard shortcuts settings tab (requires reload)**.</span></span>  <span data-ttu-id="39556-124">Rechargez maintenant le DevTools, rouvrez paramètres, puis accédez à la section **raccourcis** .</span><span class="sxs-lookup"><span data-stu-id="39556-124">Now reload the DevTools, open Settings again, and navigate to the **Shortcuts** section.</span></span>  

<span data-ttu-id="39556-125">Sélectionnez **devtools (par défaut)** dans le menu déroulant **correspondant aux raccourcis de** la liste déroulante, puis sélectionnez **Visual Studio code**.</span><span class="sxs-lookup"><span data-stu-id="39556-125">Select **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="39556-126">Les raccourcis clavier dans le DevTools correspondent désormais aux raccourcis pour les actions équivalentes dans le code VS.</span><span class="sxs-lookup"><span data-stu-id="39556-126">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in VS Code.</span></span>  

<span data-ttu-id="39556-127">Par exemple, le raccourci clavier pour suspendre ou continuer à exécuter un script en [code vs][VSCodeShortcuts] est `F5` .</span><span class="sxs-lookup"><span data-stu-id="39556-127">For example, the keyboard shortcut for pausing or continuing running a script in [VS Code][VSCodeShortcuts] is `F5`.</span></span>  <span data-ttu-id="39556-128">Avec la valeur prédéfinie **devtools (par défaut)** , ce raccourci est le même dans devtools qu' `F8` avec le **code prédéfini Visual Studio** , ce raccourci est désormais également disponible `F5` .</span><span class="sxs-lookup"><span data-stu-id="39556-128">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8` but with the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="39556-129">Pour l’instant, cette fonctionnalité est actuellement disponible dans le [cadre de l'](#getting-in-touch-with-microsoft-edge-devtools-team) expérience Microsoft Edge 84.</span><span class="sxs-lookup"><span data-stu-id="39556-129">The feature is currently available in Microsoft Edge 84 as an experiment, so please share your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) with the team!</span></span>  

<span data-ttu-id="39556-130">[#174309][CR174309] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="39556-130">Chromium issue [#174309][CR174309]</span></span>  

### <span data-ttu-id="39556-131">Émulateurs de surface duo de débogage à distance</span><span class="sxs-lookup"><span data-stu-id="39556-131">Remote debug Surface Duo emulators</span></span>  

<span data-ttu-id="39556-132">Vous pouvez maintenant déboguer à distance votre contenu Web exécuté dans l' [émulateur de surface Duo][DualScreensAndroidEmulator] en utilisant toute la puissance de [Microsoft Edge devtools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="39556-132">You are now able to remotely debug your web content running in the [Surface Duo emulator][DualScreensAndroidEmulator] using the full power of the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

<span data-ttu-id="39556-133">Avec l' [émulateur de surface Duo][DualScreensAndroidEmulator], vous pouvez tester le rendu de votre contenu Web sur une nouvelle classe de périphériques pliants et à deux écrans.</span><span class="sxs-lookup"><span data-stu-id="39556-133">With the [Surface Duo emulator][DualScreensAndroidEmulator], you are able to test how your web content renders on a new class of foldable and dual-screen devices.</span></span>  <span data-ttu-id="39556-134">L’émulateur exécute le système d’exploitation Android et fournit l' [application Android Microsoft Edge][AndroidEdge].</span><span class="sxs-lookup"><span data-stu-id="39556-134">The emulator runs the Android operating system and provides the [Microsoft Edge Android app][AndroidEdge].</span></span>  <span data-ttu-id="39556-135">Chargez votre contenu Web dans l' [application Microsoft Edge][AndroidEdge] et déboguez-le avec [Microsoft Edge devtools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="39556-135">Load your web content in the [Microsoft Edge app][AndroidEdge] and debug it with the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="Application Microsoft Edge en cours d’exécution sur l’émulateur Duo surface" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   <span data-ttu-id="39556-137">Application Microsoft Edge sur l’émulateur de surface Duo</span><span class="sxs-lookup"><span data-stu-id="39556-137">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="39556-138">La `edge://inspect` page dans une instance de bureau de [Microsoft Edge][DesktopEdge] affiche le **SurfaceDuoEmulator** avec une liste des onglets ouverts ou [PWAS][PwaIndex] qui s’exécutent sur l’émulateur de [surface Duo][DualScreensAndroidEmulator].</span><span class="sxs-lookup"><span data-stu-id="39556-138">The `edge://inspect` page in a desktop instance of [Microsoft Edge][DesktopEdge] shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][PwaIndex] that are running on the [Surface Duo emulator][DualScreensAndroidEmulator].</span></span>  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="La page edge://inspect affiche une liste des onglets ouverts dans l’application Microsoft Edge qui s’exécute sur l’émulateur." lightbox="../../media/2020/05/edge-inspect.msft.png":::
   <span data-ttu-id="39556-140">La `edge://inspect` page affiche une liste des onglets ouverts dans l’application Microsoft Edge qui s’exécute sur l’émulateur.</span><span class="sxs-lookup"><span data-stu-id="39556-140">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>
:::image-end:::  

<span data-ttu-id="39556-141">Sélectionner **Inspect** pour l’onglet ou PWA que vous voulez déboguer ouvre le [Microsoft Edge devtools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="39556-141">Selecting **inspect** for the tab or PWA that you want to debug opens the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  <span data-ttu-id="39556-142">[Suivez le guide étape par étape pour déboguer à distance votre contenu Web sur l’émulateur de surface Duo][DevToolsRemoteDebugDuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="39556-142">[Follow the step-by-step guide to remotely debug your web content on the Surface Duo emulator][DevToolsRemoteDebugDuoEmulator].</span></span>  

### <span data-ttu-id="39556-143">Redimensionnez le tiroir DevTools plus facilement</span><span class="sxs-lookup"><span data-stu-id="39556-143">Resize the DevTools drawer more easily</span></span>  

<span data-ttu-id="39556-144">Dans Microsoft Edge 83 ou version antérieure, vous pouvez uniquement redimensionner le [tiroir-devtools][DevToolsDrawer] en pointant à l’intérieur de la barre d’outils du tiroir.</span><span class="sxs-lookup"><span data-stu-id="39556-144">In Microsoft Edge 83 or earlier, you were only able to resize the [DevTools Drawer][DevToolsDrawer] by hovering inside the Drawer's toolbar.</span></span>  <span data-ttu-id="39556-145">Le tiroir ne se comporte pas de la même façon que les autres commandes de redimensionnement pour les volets du DevTools où vous placez le pointeur sur la bordure du volet pour le redimensionner.</span><span class="sxs-lookup"><span data-stu-id="39556-145">The Drawer behaved differently than the other resize controls for panes in the DevTools where you hover over the border of the pane to resize it.</span></span>  <span data-ttu-id="39556-146">Sélectionnez l’image suivante pour voir comment le redimensionnement du tiroir a fonctionné dans la version 83 ou une version antérieure de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="39556-146">Select the following image to see how resizing the Drawer worked in version 83 or earlier of Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Redimensionnement du tiroir DevTools dans Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   <span data-ttu-id="39556-148">Redimensionnement du tiroir DevTools dans Microsoft Edge 83</span><span class="sxs-lookup"><span data-stu-id="39556-148">Resizing the DevTools Drawer in Microsoft Edge 83</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="39556-149">À partir de Microsoft Edge 84, vous pouvez désormais redimensionner le tiroir en pointant sur la bordure du tiroir.</span><span class="sxs-lookup"><span data-stu-id="39556-149">Starting with Microsoft Edge 84, you are now able to resize the Drawer by hovering over the border of the Drawer.</span></span>  <span data-ttu-id="39556-150">Cette modification aligne le comportement redimensionnement du tiroir DevTools avec la façon dont vous redimensionnez d’autres volets dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="39556-150">This change aligns the behavior resizing the DevTools Drawer with the way you resize other panes in the DevTools.</span></span>  <span data-ttu-id="39556-151">Sélectionnez l’image suivante pour afficher le redimensionnement en action dans Microsoft Edge 84.</span><span class="sxs-lookup"><span data-stu-id="39556-151">Select the following image to see resizing in action in Microsoft Edge 84.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Redimensionnement du tiroir DevTools dans Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   <span data-ttu-id="39556-153">Redimensionnement du tiroir DevTools dans Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="39556-153">Resizing the DevTools Drawer in Microsoft Edge 84</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="39556-154">[#1076112][CR1076112] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="39556-154">Chromium issue [#1076112][CR1076112]</span></span>  

### <span data-ttu-id="39556-155">Les boutons de navigation de capture d’écran indiquent le focus</span><span class="sxs-lookup"><span data-stu-id="39556-155">Screencasting navigation buttons display focus</span></span>  

<span data-ttu-id="39556-156">Lors du débogage à distance d’un [appareil Android][DevToolsRemoteDebugAndroid], d’un [appareil Windows 10][DevToolsRemoteDebugWindows]ou d’un [émulateur duo de surface][DevToolsRemoteDebugDuoEmulator], vous pouvez activer ou désactiver la vidéo à l’aide de l' ![ icône d’enregistrement de la capture d’écran située ][ImageScreencastingIcon] dans le coin supérieur gauche du devtools.</span><span class="sxs-lookup"><span data-stu-id="39556-156">When remote debugging an [Android device][DevToolsRemoteDebugAndroid], a [Windows 10 device][DevToolsRemoteDebugWindows], or a [Surface Duo emulator][DevToolsRemoteDebugDuoEmulator], you are able to toggle screencasting with the ![Toggle Screencast][ImageScreencastingIcon] icon in the top-left corner of the DevTools.</span></span>  <span data-ttu-id="39556-157">Lorsque la fonction de capture d’écran est activée, vous pouvez naviguer dans l’onglet dans Microsoft Edge sur l’appareil distant à partir de la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="39556-157">With screencasting enabled, you are able to navigate the tab in Microsoft Edge on the remote device from the DevTools window.</span></span>  <span data-ttu-id="39556-158">Dans Microsoft Edge 84, ces boutons de navigation sont désormais également accessibles au clavier.</span><span class="sxs-lookup"><span data-stu-id="39556-158">In Microsoft Edge 84, these navigation buttons are now also keyboard accessible.</span></span>  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Appuyer sur les touches Maj + Tab de la barre d’URL de capture d’image affiche le focus sur le bouton actualiser" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   <span data-ttu-id="39556-160">`Shift` + `Tab` Le bouton Actualiser de la barre d’URL de capture d’image indique le focus sur le bouton **Actualiser**</span><span class="sxs-lookup"><span data-stu-id="39556-160">Pressing `Shift`+`Tab` from the screencasted URL bar shows focus on the **Refresh** button</span></span>
:::image-end:::  

<span data-ttu-id="39556-161">[#1081486][CR1081486] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="39556-161">Chromium issue [#1081486][CR1081486]</span></span>  

### <span data-ttu-id="39556-162">Le volet des détails du panneau réseau prend le focus</span><span class="sxs-lookup"><span data-stu-id="39556-162">Network panel Details pane takes focus</span></span>  

<span data-ttu-id="39556-163">Dans Microsoft Edge 84, le [volet d’informations][DevToolsNetworkDetails] du panneau **réseau** prend le focus lorsque vous l’ouvrez pour une ressource dans le [Journal du réseau][DevToolsNetworkLog].</span><span class="sxs-lookup"><span data-stu-id="39556-163">In Microsoft Edge 84, the [Details pane][DevToolsNetworkDetails] in the **Network** panel now takes focus when you open it for a resource in the [Network Log][DevToolsNetworkLog].</span></span>  <span data-ttu-id="39556-164">Cette modification permet aux lecteurs d’écran de lire et d’interagir avec le contenu du volet **Détails** .</span><span class="sxs-lookup"><span data-stu-id="39556-164">This change allows screen readers to read out and interact with the content of the **Details** pane.</span></span>  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="Le volet Détails du panneau réseau prend le focus lorsqu’il est ouvert" lightbox="../../media/2020/05/network-details.msft.png":::
   <span data-ttu-id="39556-166">Le volet **Détails** du panneau **réseau** prend le focus lorsqu’il est ouvert</span><span class="sxs-lookup"><span data-stu-id="39556-166">The **Details** pane in the **Network** panel takes focus when opened</span></span>
:::image-end:::  

<span data-ttu-id="39556-167">[#963183][CR963183] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="39556-167">Chromium issue [#963183][CR963183]</span></span>  

## <span data-ttu-id="39556-168">Annonces du projet de chrome</span><span class="sxs-lookup"><span data-stu-id="39556-168">Announcements from the Chromium project</span></span>  

<span data-ttu-id="39556-169">Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 84 qui ont été fournies au projet de chrome Open source.</span><span class="sxs-lookup"><span data-stu-id="39556-169">The following sections announce additional features available in Microsoft Edge 84 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="39556-170">Résoudre les problèmes de site grâce au nouvel outil problèmes du tiroir DevTools</span><span class="sxs-lookup"><span data-stu-id="39556-170">Fix site issues with the new Issues tool in the DevTools Drawer</span></span>

<span data-ttu-id="39556-171">L’outil nouveaux **problèmes** du tiroir-devtools a été conçu pour vous aider à réduire la fatigue de la **console**.</span><span class="sxs-lookup"><span data-stu-id="39556-171">The new **Issues** tool in the DevTools Drawer was built to help reduce the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="39556-172">Pour l’instant, la **console** est l’emplacement central pour les développeurs, les bibliothèques, les infrastructures et Microsoft Edge pour consigner des messages, des avertissements et des erreurs.</span><span class="sxs-lookup"><span data-stu-id="39556-172">Currently, the **Console** is the central place for website developers, libraries, frameworks, and Microsoft Edge to log messages, warnings, and errors.</span></span>  <span data-ttu-id="39556-173">L’outil **problèmes** agrège les avertissements du navigateur dans un sens structuré, agrégé et interactif, des liens vers les ressources affectées dans Microsoft Edge devtools et fournit des recommandations pour la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="39556-173">The **Issues** tool aggregates warnings from the browser in a structured, aggregated, and actionable way, links to affected resources within Microsoft Edge DevTools, and provides guidance on how to fix the issues.</span></span>  <span data-ttu-id="39556-174">Au fil du temps, vous devriez voir d’autres avertissements dans l’environnement Microsoft Edge dans l’outil **problèmes** plutôt que la **console**, ce qui devrait vous aider à réduire le encombrement de la **console**.</span><span class="sxs-lookup"><span data-stu-id="39556-174">Over time, you should see more and more warnings in Microsoft Edge surfacing in the **Issues** tool rather than the **Console**, which should help reduce the clutter in the **Console**.</span></span>  

<span data-ttu-id="39556-175">Pour commencer, voir [Rechercher et corriger les problèmes liés à l’outil problèmes dans Microsoft Edge devtools][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="39556-175">To get started, see [Find And Fix Problems With The Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="Outil problèmes dans le tiroir DevTools" lightbox="../../media/2020/05/issues.msft.png":::
   <span data-ttu-id="39556-177">Outil **problèmes** dans le tiroir devtools</span><span class="sxs-lookup"><span data-stu-id="39556-177">The **Issues** tool in the DevTools Drawer</span></span>  
:::image-end:::  

<span data-ttu-id="39556-178">[#1068116][CR1068116] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="39556-178">Chromium issue [#1068116][CR1068116]</span></span>  

### <span data-ttu-id="39556-179">Afficher les informations sur l’accessibilité dans l’info-bulle du mode Inspect</span><span class="sxs-lookup"><span data-stu-id="39556-179">View accessibility information in the Inspect Mode tooltip</span></span>  

<span data-ttu-id="39556-180">L’info-bulle du **mode Inspect** indique désormais si l’élément a un [nom et un rôle][WebhintHintsAxeNameRoleValue] accessibles et qu’il est [actif au clavier][WebhintHintsAxeKeyboard].</span><span class="sxs-lookup"><span data-stu-id="39556-180">The **Inspect Mode** tooltip now indicates whether the element has an accessible [name and role][WebhintHintsAxeNameRoleValue] and is [keyboard-focusable][WebhintHintsAxeKeyboard].</span></span>  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Info-bulle du mode Inspect avec les informations d’accessibilité" lightbox="../../media/2020/05/a11y.msft.png":::
  <span data-ttu-id="39556-182">Info-bulle du **mode Inspect** avec les informations d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="39556-182">The **Inspect Mode** tooltip with accessibility information</span></span>  
:::image-end:::  

<span data-ttu-id="39556-183">[#1040025][CR1040025] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="39556-183">Chromium issue [#1040025][CR1040025]</span></span>  

### <span data-ttu-id="39556-184">Mises à jour du panneau de performance</span><span class="sxs-lookup"><span data-stu-id="39556-184">Performance panel updates</span></span>  

#### <span data-ttu-id="39556-185">Afficher les informations de temps de blocage total dans le pied de page</span><span class="sxs-lookup"><span data-stu-id="39556-185">View Total Blocking Time information in the footer</span></span>  

<span data-ttu-id="39556-186">Après avoir enregistré vos performances de chargement, le panneau de **performance** montre désormais le temps de blocage total \ (TBT \) informations du pied de page.</span><span class="sxs-lookup"><span data-stu-id="39556-186">After recording your load performance, the **Performance** panel now shows Total Blocking Time \(TBT\) information in the footer.</span></span>  <span data-ttu-id="39556-187">TBT est une métrique de performance de chargement qui permet de mesurer le temps nécessaire pour rendre la page plus lisible.</span><span class="sxs-lookup"><span data-stu-id="39556-187">TBT is a load performance metric that helps quantify how long a page takes to become usable.</span></span>  <span data-ttu-id="39556-188">Il mesure essentiellement la durée pendant laquelle une page s’affiche, dont le contenu est affiché à l’écran. mais il n’est pas vraiment utilisable, car JavaScript bloque le thread principal et par conséquent, la page ne répond pas aux entrées de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="39556-188">It essentially measures how long a page appears to be usable \(because the content is rendered to the screen\); but is not actually usable, because JavaScript is blocking the main thread and therefore the page does not respond to user input.</span></span>  <span data-ttu-id="39556-189">Le TBT est la principale mesure pour un délai approximatif de première entrée.</span><span class="sxs-lookup"><span data-stu-id="39556-189">TBT is the main metric for approximating First Input Delay.</span></span>  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

<span data-ttu-id="39556-190">Pour obtenir des informations **sur le temps** de blocage total, n’utilisez pas le ![ flux de travail d’icône Actualiser la page actualiser la page ][ImageRefreshPageIcon] pour l’enregistrement des performances de chargement des pages.</span><span class="sxs-lookup"><span data-stu-id="39556-190">To get Total Blocking Time information, do not use the **Refresh Page** ![Refresh page icon][ImageRefreshPageIcon] workflow for recording page load performance.</span></span>  

<span data-ttu-id="39556-191">Au lieu de cela, sélectionnez l’icône **Enregistrer** ![ ][ImageRecordIcon] l’enregistrement, rechargez manuellement la page, attendez que la page se charge, puis arrêtez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="39556-191">Instead, select **Record** ![Record icon][ImageRecordIcon], manually reload the page, wait for the page to load, and then stop recording.</span></span>  

<span data-ttu-id="39556-192">Si vous voyez `Total Blocking Time: Unavailable` , Microsoft Edge devtools n’a pas reçu les informations requises des données de profilage internes dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="39556-192">If you see `Total Blocking Time: Unavailable`, Microsoft Edge DevTools did not get the required information from the internal profiling data in Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Total du temps de blocage dans le pied de page d’un enregistrement du panneau de performance" lightbox="../../media/2020/05/tbt.msft.png":::
   <span data-ttu-id="39556-194">Total du temps de blocage dans le pied de page d’un enregistrement du panneau de **performance**</span><span class="sxs-lookup"><span data-stu-id="39556-194">Total Blocking Time information in the footer of a **Performance** panel recording</span></span>  
:::image-end:::  

<span data-ttu-id="39556-195">[#1054381][CR1054381] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="39556-195">Chromium issue [#1054381][CR1054381]</span></span>  

#### <span data-ttu-id="39556-196">Événements de décalage de disposition dans la section nouvelle expertise</span><span class="sxs-lookup"><span data-stu-id="39556-196">Layout Shift events in the new Experience section</span></span>  

<span data-ttu-id="39556-197">La nouvelle section de l' **interface** du panneau **performances** permet de détecter les décalages de disposition.</span><span class="sxs-lookup"><span data-stu-id="39556-197">The new **Experience** section of the **Performance** panel helps you detect layout shifts.</span></span>  <span data-ttu-id="39556-198">Le décalage de disposition cumulé \ (CLS \) est une métrique qui vous permet de quantifier l’instabilité visuelle indésirable.</span><span class="sxs-lookup"><span data-stu-id="39556-198">Cumulative Layout Shift \(CLS\) is a metric that helps you quantify unwanted visual instability.</span></span>

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

<span data-ttu-id="39556-199">Pour afficher les détails de la mise en page dans le volet **Résumé** , sélectionnez l’événement de **décalage de disposition** .</span><span class="sxs-lookup"><span data-stu-id="39556-199">Select the **Layout Shift** event to see the details of the layout shift in the **Summary** pane.</span></span>  <span data-ttu-id="39556-200">Placez le pointeur sur les champs **déplacé de** et **déplacé vers** pour visualiser l’emplacement de la disposition.</span><span class="sxs-lookup"><span data-stu-id="39556-200">Hover over the **Moved from** and **Moved to** fields to visualize where the layout shift occurred.</span></span>  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Détails d’une équipe de disposition" lightbox="../../media/2020/05/cls.msft.png":::
   <span data-ttu-id="39556-202">Détails d’une équipe de disposition</span><span class="sxs-lookup"><span data-stu-id="39556-202">The details of a layout shift</span></span>  
:::image-end:::  

### <span data-ttu-id="39556-203">Terminologie d’une promesse plus précise dans la console</span><span class="sxs-lookup"><span data-stu-id="39556-203">More accurate promise terminology in the Console</span></span>  

<span data-ttu-id="39556-204">Lors de l’enregistrement de a `Promise` , la **console** n’est pas correctement fournie `PromiseStatus` avec la valeur `resolved` .</span><span class="sxs-lookup"><span data-stu-id="39556-204">When logging a `Promise`, the **Console** incorrectly provided `PromiseStatus` value set to `resolved`.</span></span>  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Exemple de la console à l’aide de l’ancienne terminologie résolue" lightbox="../../media/2020/05/resolved.msft.png":::
   <span data-ttu-id="39556-206">Exemple de **console** utilisant l’ancienne `resolved` terminologie</span><span class="sxs-lookup"><span data-stu-id="39556-206">An example of the **Console** using the old `resolved` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="39556-207">La **console** utilise désormais le terme `fulfilled` , qui s’aligne avec la `Promise` spécification.</span><span class="sxs-lookup"><span data-stu-id="39556-207">The **Console** now uses the term `fulfilled`, which aligns with the `Promise` specification.</span></span>  <span data-ttu-id="39556-208">Pour plus d’informations sur la `Promise` spécification, voir [États et devenir sur GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span><span class="sxs-lookup"><span data-stu-id="39556-208">For more information about the `Promise` specification, see [States and Fates on GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span></span>  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Exemple de console utilisant la nouvelle terminologie satisfaite" lightbox="../../media/2020/05/fulfilled.msft.png":::
  <span data-ttu-id="39556-210">Exemple de la **console** utilisant la nouvelle `fulfilled` terminologie</span><span class="sxs-lookup"><span data-stu-id="39556-210">An example of the **Console** using the new `fulfilled` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="39556-211">V8 problème [#6751][CRV86751]</span><span class="sxs-lookup"><span data-stu-id="39556-211">V8 issue [#6751][CRV86751]</span></span>  

### <span data-ttu-id="39556-212">Mises à jour du volet styles</span><span class="sxs-lookup"><span data-stu-id="39556-212">Styles pane updates</span></span>  

#### <span data-ttu-id="39556-213">Prise en charge du mot-clé de rétablissement</span><span class="sxs-lookup"><span data-stu-id="39556-213">Support for the revert keyword</span></span>  

<span data-ttu-id="39556-214">L’interface utilisateur de saisie semi-automatique du volet **styles** détecte désormais le mot clé CSS de [rétablissement][MDNRevert] , qui ramène la valeur en cascade d’une propriété à la valeur précédente appliquée au style de l’élément.</span><span class="sxs-lookup"><span data-stu-id="39556-214">The autocomplete UI of the **Styles** pane now detects the [revert][MDNRevert] CSS keyword, which reverts the cascaded value of a property to the previous value applied to the styling of the element.</span></span>  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Définition de la valeur d’une propriété pour la rétablir" lightbox="../../media/2020/05/revert.msft.png":::
  <span data-ttu-id="39556-216">Définition de la valeur d’une propriété pour la rétablir</span><span class="sxs-lookup"><span data-stu-id="39556-216">Setting the value of a property to revert</span></span>  
:::image-end:::  

<span data-ttu-id="39556-217">[#1075437][CR1075437] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="39556-217">Chromium issue [#1075437][CR1075437]</span></span>  

#### <span data-ttu-id="39556-218">Aperçus d’images</span><span class="sxs-lookup"><span data-stu-id="39556-218">Image previews</span></span>  

<span data-ttu-id="39556-219">Pointez sur une `background-image` valeur dans le volet **styles** pour afficher un aperçu de l’image dans une info-bulle.</span><span class="sxs-lookup"><span data-stu-id="39556-219">Hover over a `background-image` value in the **Styles** pane to see a preview of the image in a tooltip.</span></span>  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Survol d’une valeur d’image d’arrière-plan" lightbox="../../media/2020/05/image-preview.msft.png":::
  <span data-ttu-id="39556-221">Survol d’une `background-image` valeur</span><span class="sxs-lookup"><span data-stu-id="39556-221">Hovering over a `background-image` value</span></span>  
:::image-end:::  

<span data-ttu-id="39556-222">[#1040019][CR1040019] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="39556-222">Chromium issue [#1040019][CR1040019]</span></span>  

#### <span data-ttu-id="39556-223">Le sélecteur de couleurs utilise désormais une notation de couleur fonctionnelle séparée par des espaces</span><span class="sxs-lookup"><span data-stu-id="39556-223">Color Picker now uses space-separated functional color notation</span></span>  

<span data-ttu-id="39556-224">Le [module de couleurs CSS-niveau 4][CSSWGDraftsColor4Changes3] spécifie que les fonctions de couleur, telles que `rgb()` , doivent prendre en charge les arguments séparés par des espaces.</span><span class="sxs-lookup"><span data-stu-id="39556-224">[CSS Color Module Level 4][CSSWGDraftsColor4Changes3] specifies that color functions, such as `rgb()`, should support space-separated arguments.</span></span>  <span data-ttu-id="39556-225">Par exemple, `rgb(0, 0, 0)` revient à spécifier `rbg(0 0 0)`.</span><span class="sxs-lookup"><span data-stu-id="39556-225">For example, `rgb(0, 0, 0)` is equivalent to `rbg(0 0 0)`.</span></span>  

<span data-ttu-id="39556-226">Lorsque vous choisissez des couleurs à l’aide du [Sélecteur de couleurs][DevtoolsCssReferenceColorPicker] ou alterner entre les représentations de couleurs dans le volet **styles** , en maintenant la touche enfoncée `Shift` et en sélectionnant la `background-color` valeur, vous devez voir la syntaxe d’argument séparée par un espace.</span><span class="sxs-lookup"><span data-stu-id="39556-226">When you choose colors with the [Color Picker][DevtoolsCssReferenceColorPicker] or alternate between color representations in the **Styles** pane by holding `Shift` and selecting the `background-color` value, you should see the space-separated argument syntax.</span></span>  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Utilisation d’arguments séparés par des espaces dans le volet styles" lightbox="../../media/2020/05/color.msft.png":::
  <span data-ttu-id="39556-228">Utilisation d’arguments séparés par des espaces dans le volet **styles**</span><span class="sxs-lookup"><span data-stu-id="39556-228">Using space-separated arguments in the **Styles** pane</span></span>  
:::image-end:::  

<span data-ttu-id="39556-229">Vous devez également voir la syntaxe dans le volet **calculé** et l’info-bulle du **mode inspecter** .</span><span class="sxs-lookup"><span data-stu-id="39556-229">You should also see the syntax in the **Computed** pane and the **Inspect Mode** tooltip.</span></span>  

<span data-ttu-id="39556-230">Microsoft Edge DevTools utilise la nouvelle syntaxe, car les fonctionnalités CSS à venir, telles que [Color ()][CSSWGDraftsColor4Property] ne prennent pas en charge la syntaxe d’argument séparée par des virgules.</span><span class="sxs-lookup"><span data-stu-id="39556-230">Microsoft Edge DevTools is using the new syntax because upcoming CSS features such as [color()][CSSWGDraftsColor4Property] do not support the deprecated comma-separated argument syntax.</span></span>  

<span data-ttu-id="39556-231">La syntaxe d’argument séparée par un espace est prise en charge dans la plupart des navigateurs pendant un certain temps.</span><span class="sxs-lookup"><span data-stu-id="39556-231">The space-separated argument syntax has been supported in most browsers for a while.</span></span>  <span data-ttu-id="39556-232">Pour plus d’informations, reportez-vous à la section [puis-je utiliser des notations de couleur fonctionnelle séparées par un espace.][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span><span class="sxs-lookup"><span data-stu-id="39556-232">For more information, see [Can I use: Space-separated functional color notations?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span></span>  

<span data-ttu-id="39556-233">[#1072952][CR1072952] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="39556-233">Chromium issue [#1072952][CR1072952]</span></span>  

### <span data-ttu-id="39556-234">Déconseillé du volet Propriétés dans le panneau éléments</span><span class="sxs-lookup"><span data-stu-id="39556-234">Deprecation of the Properties pane in the Elements panel</span></span>  

<span data-ttu-id="39556-235">Le volet **Propriétés** du panneau **éléments** est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="39556-235">The **Properties** pane in the **Elements** panel is deprecated.</span></span>  <span data-ttu-id="39556-236">Exécutez `console.dir($0)` plutôt sur la **console** .</span><span class="sxs-lookup"><span data-stu-id="39556-236">Run `console.dir($0)` in the **Console** instead.</span></span>  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="Volet de propriétés déconseillées" lightbox="../../media/2020/05/properties.msft.png":::
   <span data-ttu-id="39556-238">Volet de **Propriétés** déconseillées</span><span class="sxs-lookup"><span data-stu-id="39556-238">The deprecated **Properties** pane</span></span>  
:::image-end:::  

#### <span data-ttu-id="39556-239">Références</span><span class="sxs-lookup"><span data-stu-id="39556-239">References</span></span>  

*   [<span data-ttu-id="39556-240">Console. dir ()</span><span class="sxs-lookup"><span data-stu-id="39556-240">console.dir()</span></span>][DevtoolsConsoleApiDir]  
*   [<span data-ttu-id="39556-241">$0</span><span class="sxs-lookup"><span data-stu-id="39556-241">$0</span></span>][DevtoolsConsoleUtilitiesDom]  

### <span data-ttu-id="39556-242">Prise en charge des raccourcis d’application dans le volet manifeste</span><span class="sxs-lookup"><span data-stu-id="39556-242">App shortcuts support in the Manifest pane</span></span>  

<span data-ttu-id="39556-243">Les raccourcis d’application permettent aux utilisateurs de démarrer rapidement des tâches courantes ou recommandées au sein d’une application Web.</span><span class="sxs-lookup"><span data-stu-id="39556-243">App shortcuts help users quickly start common or recommended tasks within a web app.</span></span>  <span data-ttu-id="39556-244">Le menu Raccourcis de l’application s’affiche uniquement pour les [applications Web progressives][PwaIndex] installées sur le bureau ou l’appareil mobile de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="39556-244">The app shortcuts menu is shown only for [Progressive Web Apps][PwaIndex] that are installed on the user's desktop or mobile device.</span></span>  

<!--For more information, see [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Raccourcis d’application dans le volet manifeste" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  <span data-ttu-id="39556-246">Raccourcis d’application dans le volet **manifeste**</span><span class="sxs-lookup"><span data-stu-id="39556-246">App shortcuts in the **Manifest** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="39556-247">Télécharger les canaux Microsoft Edge preview</span><span class="sxs-lookup"><span data-stu-id="39556-247">Download the Microsoft Edge preview channels</span></span>   

<span data-ttu-id="39556-248">Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="39556-248">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="39556-249">Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="39556-249">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="39556-250">Contacter l’équipe Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="39556-250">Getting in touch with Microsoft Edge Devtools team</span></span>  

  

<span data-ttu-id="39556-251">Découvrir les nouvelles fonctionnalités et les modifications apportées au billet ou tout autre sujet lié à DevTools:</span><span class="sxs-lookup"><span data-stu-id="39556-251">To discuss the new features and changes in the post, or anything else related to DevTools:</span></span>  

*   <span data-ttu-id="39556-252">Envoyez vos commentaires à l’aide de l’icône de **Commentaires** dans le devtools</span><span class="sxs-lookup"><span data-stu-id="39556-252">Send your feedback using the **Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="39556-253">Tweeter sur [@EdgeDevTools][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="39556-253">Tweet at [@EdgeDevTools][PostTweetEdgeDevTools]</span></span>  
*   <span data-ttu-id="39556-254">Envoyez une suggestion au [site Web de votre choix][TheWebWeWant]</span><span class="sxs-lookup"><span data-stu-id="39556-254">Submit a suggestion to [The Web We Want][TheWebWeWant]</span></span>  
*   <span data-ttu-id="39556-255">Classer les bogues sur cette page dans le référentiel [Edge-développeurs][GitHubMicrosoftDocsEdgeDeveloperNewIssue]</span><span class="sxs-lookup"><span data-stu-id="39556-255">File bugs on this page in the [edge-developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue] repository</span></span>  

:::image type="complex" source="../../media/2020/05/feedback-icon.msft.png" alt-text="Icône de commentaires dans le Microsoft Edge DevTools" lightbox="../../media/2020/05/feedback-icon.msft.png":::
  <span data-ttu-id="39556-257">Icône de **Commentaires** dans le Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="39556-257">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Icône Paramètres de DevTools"
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/images/toggle-screencast-icon.msft.png "Icône de DevTools bascule"
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-page-icon.msft.png "Icône de page actualiser du panneau performances DevTools"
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png "Icône d’enregistrement du panneau de performance DevTools"

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Utiliser l’émulateur de surface Duo | Documents Microsoft"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "Référence sur l’API dir-console | Documents Microsoft"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Éléments récemment sélectionnés ou JavaScript objet-référence des API des utilitaires de la console | Documents Microsoft"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Changer les couleurs à l’aide du sélecteur de couleurs-Référence CSS | Documents Microsoft"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Tiroir-présentation de la personnalisation | Documents Microsoft"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Recherchez et corrigez les problèmes liés à l’onglet problèmes dans Microsoft Edge DevTools Documents Microsoft"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Commencer à utiliser le débogage à distance des appareils Android | Documents Microsoft"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Commencer avec les émulateurs de surface duo pour le débogage à distance Documents Microsoft"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Commencer à utiliser le débogage à distance des appareils Windows 10 | Documents Microsoft"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Inspecter les détails de la ressource | Documents Microsoft"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Journalisation de l’activité du réseau | Documents Microsoft"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Applications Web progressives sur Windows | Documents Microsoft"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Application Microsoft Edge Android"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Notations de couleur fonctionnelle séparées par un espace-MDN | Puis-je utiliser"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs du chrome"

[CR174309]: https://crbug.com/174309 "DevTools: autoriser pour personnaliser les raccourcis clavier/les combinaisons de touches | Bugs du chrome"  
[CR963183]: https://crbug.com/963183 "DevTools ne respectent pas la norme WCAG | Bugs du chrome"  
[CR1040019]: https://crbug.com/1040019 "DevTools: Affichez un aperçu des images et images d’arrière-plan facilement dans le volet styles | Bugs du chrome"  
[CR1040025]: https://crbug.com/1040025 "DevTools: afficher les informations a11y de base dans l’élément popover | Bugs du chrome"  
[CR1048378]: https://crbug.com/1048378 "Prise en charge de l’interface utilisateur DevTools pour le mode contraste élevé | Bugs du chrome"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Bugs du chrome"  
[CR1068116]: https://crbug.com/1068116 "Panneau problèmes d’expédition | Bugs du chrome"  
[CR1072952]: https://crbug.com/1072952 "DevTools: le sélecteur de couleurs doit générer une syntaxe de couleur CSS moderne | Bugs du chrome"  
[CR1075437]: https://crbug.com/1075437 "DevTools: ajoutez la prise en charge du mot-clé/valeur CSS «rétablir». Bugs du chrome"  
[CR1076112]: https://crbug.com/1076112 "Personalization devtools-tiroir du tiroir"  
[CR1081486]: https://crbug.com/1081486 "Le focus clavier n’est pas visible pour les boutons de navigation en mode screencast | Bugs du chrome"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus doit être «respecté», et non «résolu» | V8 bogues"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Modifications des couleurs 3-CSS-module de couleurs-niveau 4 | Brouillons de l’éditeur de groupe de travail CSS W3C"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. couleur de premier plan: «couleur»-module de couleur CSS-niveau 4 | Brouillons de l’éditeur de groupe de travail CSS W3C"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Présentation du nouveau Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "États et-Domenic/promet-déconditionnement | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "rétablir | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Compatibilité du navigateur | MDN"  

[VSCode]: https://code.visualstudio.com/ "Code Visual Studio"  
[VSCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Raccourcis clavier dans Visual Studio code pour Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe: clavier | Astuce"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: valeur du rôle de nom | Astuce"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Activer ou désactiver le mode contraste élevé dans Windows | Support Windows"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publiez un tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools compte Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nouveau problème-MicrosoftDocs/Edge-développeur"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canaux Microsoft Edge preview"  
[TheWebWeWant]: https://aka.ms/webwewant "Le site Web de votre choix"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> <span data-ttu-id="39556-306">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="39556-306">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="39556-307">La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/05/devtools/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="39556-307">The original page is found [here](https://developers.google.com/web/updates/2020/05/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="39556-309">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="39556-309">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
