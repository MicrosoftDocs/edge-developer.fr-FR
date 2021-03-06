---
description: Utilisez les DevTools en mode de contraste élevé Windows, faire correspondre les raccourcis clavier dans DevTools à Visual Studio Code, et bien plus encore.
title: Nouveautés de DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 701c328c1dc975a81129049fe2931139757205c3
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398573"
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

# <a name="whats-new-in-devtools-microsoft-edge-84"></a><span data-ttu-id="64511-104">Nouveautés de DevTools (Microsoft Edge 84)</span><span class="sxs-lookup"><span data-stu-id="64511-104">What's new in DevTools (Microsoft Edge 84)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="64511-105">Annonces de l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="64511-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="64511-106">Les sections suivantes sont une liste des annonces que vous avez peut-être manquées de l’équipe Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="64511-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="64511-107">Consultez les annonces pour essayer les nouvelles fonctionnalités des extensions DevTools, Microsoft Visual Studio Code, etc.</span><span class="sxs-lookup"><span data-stu-id="64511-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="64511-108">Pour rester à jour sur toutes les fonctionnalités les plus récentes et les plus importantes de vos outils de développement, téléchargez les canaux d’aperçu [microsoft Edge][MicrosoftEdgePreviewChannels] et suivez-nous [sur Twitter.][EdgeDevToolsTwitterAccount]</span><span class="sxs-lookup"><span data-stu-id="64511-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="use-the-devtools-in-windows-high-contrast-mode"></a><span data-ttu-id="64511-109">Utiliser les DevTools en mode de contraste élevé Windows</span><span class="sxs-lookup"><span data-stu-id="64511-109">Use the DevTools in Windows high contrast mode</span></span>

<span data-ttu-id="64511-110">Les devTools Microsoft Edge sont désormais affichés en mode de contraste élevé lorsque Windows est en mode de contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="64511-110">The Microsoft Edge DevTools are now displayed in high contrast mode when Windows is in high contrast mode.</span></span>  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Microsoft Edge DevTools en mode de contraste élevé" lightbox="../../media/2020/05/high-contrast.msft.png":::
   <span data-ttu-id="64511-112">Microsoft Edge DevTools en mode de contraste élevé</span><span class="sxs-lookup"><span data-stu-id="64511-112">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="64511-113">[Suivez les instructions pour activer le mode de contraste élevé dans Windows.][MicrosoftSupportWindows10HighContrastMode]</span><span class="sxs-lookup"><span data-stu-id="64511-113">[Follow the instructions to turn on high contrast mode in Windows][MicrosoftSupportWindows10HighContrastMode].</span></span>  <span data-ttu-id="64511-114">Pour ouvrir devTools dans Microsoft Edge, sélectionnez `F12` ou `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="64511-114">To open the DevTools in Microsoft Edge, select `F12` or `Ctrl`+`Shift`+`I`.</span></span>  <span data-ttu-id="64511-115">Les DevTools sont affichés en mode de contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="64511-115">The DevTools are displayed in high contrast mode.</span></span>  

> [!NOTE]
> <span data-ttu-id="64511-116">Microsoft Edge DevTools permet actuellement la prise en charge du mode contraste élevé sur Windows, mais pas sur macOS.</span><span class="sxs-lookup"><span data-stu-id="64511-116">The Microsoft Edge DevTools currently support high contrast mode on Windows but not on macOS.</span></span>  

<span data-ttu-id="64511-117">Problème de chrome [#1048378][CR1048378]</span><span class="sxs-lookup"><span data-stu-id="64511-117">Chromium issue [#1048378][CR1048378]</span></span>  

### <a name="match-keyboard-shortcuts-in-the-devtools-to-visual-studio-code"></a><span data-ttu-id="64511-118">Faire correspondre les raccourcis clavier dans DevTools à Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="64511-118">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="64511-119">À [](#getting-in-touch-with-microsoft-edge-devtools-team) partir de vos commentaires et du suivi des problèmes publics [Chromium,][CRIssuesList]l’équipe Microsoft Edge DevTools a appris que vous souhaitiez pouvoir personnaliser les raccourcis clavier dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="64511-119">From your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) and the [Chromium public issue tracker][CRIssuesList], the Microsoft Edge DevTools team learned that you wanted the ability to customize keyboard shortcuts in the DevTools.</span></span>  <span data-ttu-id="64511-120">Dans Microsoft Edge 84, vous pouvez désormais faire correspondre les raccourcis clavier de DevTools à [Visual Studio Code,][VisualStudioCode]qui n’est qu’une des fonctionnalités sur lesquelles l’équipe travaille pour la personnalisation des raccourcis.</span><span class="sxs-lookup"><span data-stu-id="64511-120">In Microsoft Edge 84, you are now able to match keyboard shortcuts in the DevTools to [Visual Studio Code][VisualStudioCode], which is just one of the features the team is working on for shortcut customization.</span></span>  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Faire correspondre les raccourcis clavier dans DevTools à Visual Studio Code" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   <span data-ttu-id="64511-122">Microsoft Edge DevTools en mode de contraste élevé</span><span class="sxs-lookup"><span data-stu-id="64511-122">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="64511-123">Pour essayer l’expérience, ouvrez Paramètres de DevTools en sélectionnant ou en choisissant l’icône DevTools Settings dans le coin supérieur droit de `?` ![ ][ImageSettingsIcon] DevTools.</span><span class="sxs-lookup"><span data-stu-id="64511-123">To try the experiment, open DevTools Settings by selecting `?` or choosing the ![DevTools Settings icon][ImageSettingsIcon] icon in the top-right corner of the DevTools.</span></span>  <span data-ttu-id="64511-124">Accédez à la section **Expériences** et cochez l’onglet Activer les paramètres des **raccourcis clavier personnalisés (nécessite un rechargement).**</span><span class="sxs-lookup"><span data-stu-id="64511-124">Navigate to the **Experiments** section and check **Enable custom keyboard shortcuts settings tab (requires reload)**.</span></span>  <span data-ttu-id="64511-125">Rechargez à présent les DevTools, ouvrez de nouveau Paramètres et accédez à la section **Raccourcis.**</span><span class="sxs-lookup"><span data-stu-id="64511-125">Now reload the DevTools, open Settings again, and navigate to the **Shortcuts** section.</span></span>  

<span data-ttu-id="64511-126">Choose **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span><span class="sxs-lookup"><span data-stu-id="64511-126">Choose **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="64511-127">Les raccourcis clavier des DevTools correspondent désormais aux raccourcis des actions équivalentes dans Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="64511-127">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in Visual Studio Code.</span></span>  

<span data-ttu-id="64511-128">Par exemple, le raccourci clavier pour mettre en pause ou poursuivre l’exécution d’un script [dans Visual Studio Code][VisualStudioCodeShortcuts] est `F5` .</span><span class="sxs-lookup"><span data-stu-id="64511-128">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualStudioCodeShortcuts] is `F5`.</span></span>  <span data-ttu-id="64511-129">Avec **devTools (par défaut)** prédéfiny, ce même raccourci dans devTools est, mais avec le `F8` **code Visual Studio** prédéfiny, ce raccourci est maintenant également `F5` .</span><span class="sxs-lookup"><span data-stu-id="64511-129">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8` but with the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="64511-130">La fonctionnalité est actuellement disponible dans Microsoft Edge 84 en tant qu’expérience. Veuillez donc partager vos commentaires [avec](#getting-in-touch-with-microsoft-edge-devtools-team) l’équipe !</span><span class="sxs-lookup"><span data-stu-id="64511-130">The feature is currently available in Microsoft Edge 84 as an experiment, so please share your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) with the team!</span></span>  

<span data-ttu-id="64511-131">Problème de chrome [#174309][CR174309]</span><span class="sxs-lookup"><span data-stu-id="64511-131">Chromium issue [#174309][CR174309]</span></span>  

### <a name="remote-debug-surface-duo-emulators"></a><span data-ttu-id="64511-132">Débogage à distance des émulateurs Surface Duo</span><span class="sxs-lookup"><span data-stu-id="64511-132">Remote debug Surface Duo emulators</span></span>  

<span data-ttu-id="64511-133">Vous pouvez désormais déboguer à distance votre contenu web en cours d’exécution dans l’émulateur [Surface Duo][DualScreensAndroidEmulator] à l’aide de la puissance totale de Microsoft [Edge DevTools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="64511-133">You are now able to remotely debug your web content running in the [Surface Duo emulator][DualScreensAndroidEmulator] using the full power of the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

<span data-ttu-id="64511-134">Avec [l’émulateur Surface Duo,][DualScreensAndroidEmulator]vous pouvez tester le rendu de votre contenu web sur une nouvelle classe d’appareils pliables et à double écran.</span><span class="sxs-lookup"><span data-stu-id="64511-134">With the [Surface Duo emulator][DualScreensAndroidEmulator], you are able to test how your web content renders on a new class of foldable and dual-screen devices.</span></span>  <span data-ttu-id="64511-135">L’émulateur exécute le système d’exploitation Android et fournit [l’application Microsoft Edge Android.][AndroidEdge]</span><span class="sxs-lookup"><span data-stu-id="64511-135">The emulator runs the Android operating system and provides the [Microsoft Edge Android app][AndroidEdge].</span></span>  <span data-ttu-id="64511-136">Chargez votre contenu web dans [l’application Microsoft Edge][AndroidEdge] et déboguer avec Microsoft Edge [DevTools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="64511-136">Load your web content in the [Microsoft Edge app][AndroidEdge] and debug it with the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="Application Microsoft Edge en cours d’exécution sur l’émulateur Surface Duo" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   <span data-ttu-id="64511-138">Application Microsoft Edge sur l’émulateur Surface Duo</span><span class="sxs-lookup"><span data-stu-id="64511-138">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="64511-139">La page d’une instance de bureau de Microsoft Edge affiche l’émulateur `edge://inspect` **SurfaceDuoEmulator** [][DesktopEdge] avec une liste des onglets ouverts ou des PLAN en cours d’exécution sur l’émulateur [Surface Duo.][DualScreensAndroidEmulator] [][PwaIndex]</span><span class="sxs-lookup"><span data-stu-id="64511-139">The `edge://inspect` page in a desktop instance of [Microsoft Edge][DesktopEdge] shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][PwaIndex] that are running on the [Surface Duo emulator][DualScreensAndroidEmulator].</span></span>  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="La page edge://inspect affiche la liste des onglets ouverts dans l’application Microsoft Edge en cours d’exécution sur l’émulateur" lightbox="../../media/2020/05/edge-inspect.msft.png":::
   <span data-ttu-id="64511-141">La page affiche la liste des onglets ouverts dans l’application Microsoft Edge en cours `edge://inspect` d’exécution sur l’émulateur</span><span class="sxs-lookup"><span data-stu-id="64511-141">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>
:::image-end:::  

<span data-ttu-id="64511-142">Choisissez **inspectez** l’onglet ou PWA que vous souhaitez déboguer pour ouvrir [Microsoft Edge DevTools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="64511-142">Choose **inspect** for the tab or PWA that you want to debug to open the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  <span data-ttu-id="64511-143">Suivez le guide pas à pas pour déboguer à distance votre contenu [web sur l’émulateur Surface Duo.][DevToolsRemoteDebugDuoEmulator]</span><span class="sxs-lookup"><span data-stu-id="64511-143">[Follow the step-by-step guide to remotely debug your web content on the Surface Duo emulator][DevToolsRemoteDebugDuoEmulator].</span></span>  

### <a name="resize-the-devtools-drawer-more-easily"></a><span data-ttu-id="64511-144">Resize the DevTools drawer more easily</span><span class="sxs-lookup"><span data-stu-id="64511-144">Resize the DevTools drawer more easily</span></span>  

<span data-ttu-id="64511-145">Dans Microsoft Edge 83 ou une antérieure, vous n’avez pu resizer le caisse [DevTools][DevToolsDrawer] qu’en pointant à l’intérieur de la barre d’outils du caisse.</span><span class="sxs-lookup"><span data-stu-id="64511-145">In Microsoft Edge 83 or earlier, you were only able to resize the [DevTools Drawer][DevToolsDrawer] by hovering inside the toolbar of the Drawer.</span></span>  <span data-ttu-id="64511-146">Le drawer se comporte différemment des autres contrôles de re resize pour les volets des DevTools où vous placez le pointeur sur la bordure du volet pour le resizer.</span><span class="sxs-lookup"><span data-stu-id="64511-146">The Drawer behaved differently than the other resize controls for panes in the DevTools where you hover on the border of the pane to resize it.</span></span>  <span data-ttu-id="64511-147">Sélectionnez l’image suivante pour afficher le resizing the Drawer worked in version 83 or earlier of Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="64511-147">Choose the following image to display how resizing the Drawer worked in version 83 or earlier of Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Resizing the DevTools Drawer in Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   <span data-ttu-id="64511-149">Resizing the DevTools Drawer in Microsoft Edge 83</span><span class="sxs-lookup"><span data-stu-id="64511-149">Resizing the DevTools Drawer in Microsoft Edge 83</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="64511-150">À partir de Microsoft Edge 84, vous pouvez maintenant resizer le caisse en pointant sur la bordure du caisse.</span><span class="sxs-lookup"><span data-stu-id="64511-150">Starting with Microsoft Edge 84, you are now able to resize the Drawer by hovering over the border of the Drawer.</span></span>  <span data-ttu-id="64511-151">Cette modification aligne le comportement de resizing the DevTools Drawer with the way you resize other panes in the DevTools.</span><span class="sxs-lookup"><span data-stu-id="64511-151">This change aligns the behavior resizing the DevTools Drawer with the way you resize other panes in the DevTools.</span></span>  <span data-ttu-id="64511-152">Sélectionnez l’image suivante pour afficher le re resserrement en action dans Microsoft Edge 84.</span><span class="sxs-lookup"><span data-stu-id="64511-152">Choose the following image to display resizing in action in Microsoft Edge 84.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Resizing the DevTools Drawer in Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   <span data-ttu-id="64511-154">Resizing the DevTools Drawer in Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="64511-154">Resizing the DevTools Drawer in Microsoft Edge 84</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="64511-155">Problème de chrome [#1076112][CR1076112]</span><span class="sxs-lookup"><span data-stu-id="64511-155">Chromium issue [#1076112][CR1076112]</span></span>  

### <a name="screencasting-navigation-buttons-display-focus"></a><span data-ttu-id="64511-156">Les boutons de navigation par capture vidéo affichent le focus</span><span class="sxs-lookup"><span data-stu-id="64511-156">Screencasting navigation buttons display focus</span></span>  

<span data-ttu-id="64511-157">Lors du débogage à distance d’un appareil [Android,][DevToolsRemoteDebugAndroid]d’un appareil [Windows 10][DevToolsRemoteDebugWindows]ou d’un émulateur [Surface Duo,][DevToolsRemoteDebugDuoEmulator]vous pouvez faire basculer la capture vidéo avec l’icône Deggle Screencast dans le coin supérieur gauche des ![ ][ImageScreencastingIcon] DevTools.</span><span class="sxs-lookup"><span data-stu-id="64511-157">When remote debugging an [Android device][DevToolsRemoteDebugAndroid], a [Windows 10 device][DevToolsRemoteDebugWindows], or a [Surface Duo emulator][DevToolsRemoteDebugDuoEmulator], you are able to toggle screencasting with the ![Toggle Screencast][ImageScreencastingIcon] icon in the top-left corner of the DevTools.</span></span>  <span data-ttu-id="64511-158">Avec la capture vidéo activée, vous pouvez naviguer dans l’onglet de Microsoft Edge sur l’appareil distant à partir de la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="64511-158">With screencasting enabled, you are able to navigate the tab in Microsoft Edge on the remote device from the DevTools window.</span></span>  <span data-ttu-id="64511-159">Dans Microsoft Edge 84, ces boutons de navigation sont désormais également accessibles au clavier.</span><span class="sxs-lookup"><span data-stu-id="64511-159">In Microsoft Edge 84, these navigation buttons are now also keyboard accessible.</span></span>  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Select Shift+Tab from the screencasted URL bar shows focus on the Refresh button" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   <span data-ttu-id="64511-161">La `Shift` + `Tab` sélection dans la barre d’URL par capture vidéo affiche le focus sur le **bouton Actualiser**</span><span class="sxs-lookup"><span data-stu-id="64511-161">Select `Shift`+`Tab` from the screencasted URL bar shows focus on the **Refresh** button</span></span>
:::image-end:::  

<span data-ttu-id="64511-162">Problème de chrome [#1081486][CR1081486]</span><span class="sxs-lookup"><span data-stu-id="64511-162">Chromium issue [#1081486][CR1081486]</span></span>  

### <a name="network-panel-details-pane-is-now-accessible"></a><span data-ttu-id="64511-163">Le volet Détails du panneau réseau est désormais accessible</span><span class="sxs-lookup"><span data-stu-id="64511-163">Network panel Details pane is now accessible</span></span>  

<span data-ttu-id="64511-164">Dans Microsoft Edge 84, le volet \*\*\*\* [Détails][DevToolsNetworkDetails] de l’outil Réseau prend désormais le focus lorsque vous l’ouvrez pour une ressource dans le [journal réseau.][DevToolsNetworkLog]</span><span class="sxs-lookup"><span data-stu-id="64511-164">In Microsoft Edge 84, the [Details pane][DevToolsNetworkDetails] in the **Network** tool now takes focus when you open it for a resource in the [Network Log][DevToolsNetworkLog].</span></span>  <span data-ttu-id="64511-165">Cette modification permet aux lecteurs d’écran de lire et d’interagir avec le contenu du volet **d’informations.**</span><span class="sxs-lookup"><span data-stu-id="64511-165">This change allows screen readers to read out and interact with the content of the **Details** pane.</span></span>  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="Le volet Détails du panneau Réseau prend le focus à l’ouverture" lightbox="../../media/2020/05/network-details.msft.png":::
   <span data-ttu-id="64511-167">Le **volet Détails** de **l’outil** Réseau prend le focus à l’ouverture</span><span class="sxs-lookup"><span data-stu-id="64511-167">The **Details** pane in the **Network** tool takes focus when opened</span></span>
:::image-end:::  

<span data-ttu-id="64511-168">Problème de chrome [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="64511-168">Chromium issue [#963183][CR963183]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="64511-169">Annonces du projet de Chromium</span><span class="sxs-lookup"><span data-stu-id="64511-169">Announcements from the Chromium project</span></span>  

<span data-ttu-id="64511-170">Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 84 qui ont été contribués au projet Chromium open source.</span><span class="sxs-lookup"><span data-stu-id="64511-170">The following sections announce additional features available in Microsoft Edge 84 that were contributed to the open source Chromium project.</span></span>  

### <a name="fix-site-issues-with-the-new-issues-tool-in-the-devtools-drawer"></a><span data-ttu-id="64511-171">Résoudre les problèmes de site avec le nouvel outil Problèmes dans le caisse DevTools</span><span class="sxs-lookup"><span data-stu-id="64511-171">Fix site issues with the new Issues tool in the DevTools Drawer</span></span>

<span data-ttu-id="64511-172">Le nouvel outil Problèmes dans le caisse DevTools a été conçu pour vous aider à réduire la fatigue et l’encombrement des **notifications** de la **console.**</span><span class="sxs-lookup"><span data-stu-id="64511-172">The new **Issues** tool in the DevTools Drawer was built to help reduce the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="64511-173">Actuellement, la **console** est l’endroit central pour les développeurs de sites web, les bibliothèques, les frameworks et Microsoft Edge pour enregistrer les messages, les avertissements et les erreurs.</span><span class="sxs-lookup"><span data-stu-id="64511-173">Currently, the **Console** is the central place for website developers, libraries, frameworks, and Microsoft Edge to log messages, warnings, and errors.</span></span>  <span data-ttu-id="64511-174">L’outil Problèmes regroupe les avertissements du navigateur de manière structurée, agrégée et actionnable, des liens vers les ressources affectées dans Microsoft Edge DevTools et fournit des conseils sur la façon de résoudre les problèmes. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="64511-174">The **Issues** tool aggregates warnings from the browser in a structured, aggregated, and actionable way, links to affected resources within Microsoft Edge DevTools, and provides guidance on how to fix the issues.</span></span>  <span data-ttu-id="64511-175">Au fil du temps, de plus en plus d’avertissements sont **publiés** dans Microsoft Edge dans l’outil Problèmes plutôt que dans la **console,** ce qui devrait aider à réduire l’encombrement dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="64511-175">Over time, more and more warnings are surfaced in Microsoft Edge in the **Issues** tool rather than the **Console**, which should help reduce the clutter in the **Console**.</span></span>  

<span data-ttu-id="64511-176">To get started, navigate to [Find and Fix Problems With the Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="64511-176">To get started, navigate to [Find And Fix Problems With The Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="L’outil Problèmes dans le caisse de DevTools" lightbox="../../media/2020/05/issues.msft.png":::
   <span data-ttu-id="64511-178">**L’outil Problèmes** dans le caisse de DevTools</span><span class="sxs-lookup"><span data-stu-id="64511-178">The **Issues** tool in the DevTools Drawer</span></span>  
:::image-end:::  

<span data-ttu-id="64511-179">Problème de chrome [#1068116][CR1068116]</span><span class="sxs-lookup"><span data-stu-id="64511-179">Chromium issue [#1068116][CR1068116]</span></span>  

### <a name="view-accessibility-information-in-the-inspect-mode-tooltip"></a><span data-ttu-id="64511-180">Afficher les informations d’accessibilité dans l’info-bulle Inspect Mode</span><span class="sxs-lookup"><span data-stu-id="64511-180">View accessibility information in the Inspect Mode tooltip</span></span>  

<span data-ttu-id="64511-181">**L’tip d’outils** Inspect Mode indique maintenant si l’élément a un nom [et][WebhintHintsAxeNameRoleValue] un rôle accessibles et est accessible [au clavier.][WebhintHintsAxeKeyboard]</span><span class="sxs-lookup"><span data-stu-id="64511-181">The **Inspect Mode** tooltip now indicates whether the element has an accessible [name and role][WebhintHintsAxeNameRoleValue] and is [keyboard-focusable][WebhintHintsAxeKeyboard].</span></span>  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Info-bulle Inspecter le mode avec des informations d’accessibilité" lightbox="../../media/2020/05/a11y.msft.png":::
  <span data-ttu-id="64511-183">**Info-bulle Inspecter le mode** avec des informations d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="64511-183">The **Inspect Mode** tooltip with accessibility information</span></span>  
:::image-end:::  

<span data-ttu-id="64511-184">Problème de chrome [#1040025][CR1040025]</span><span class="sxs-lookup"><span data-stu-id="64511-184">Chromium issue [#1040025][CR1040025]</span></span>  

### <a name="performance-panel-updates"></a><span data-ttu-id="64511-185">Mises à jour du panneau de performances</span><span class="sxs-lookup"><span data-stu-id="64511-185">Performance panel updates</span></span>  

#### <a name="view-total-blocking-time-information-in-the-footer"></a><span data-ttu-id="64511-186">Afficher les informations sur le temps total de blocage dans le pied de groupe</span><span class="sxs-lookup"><span data-stu-id="64511-186">View Total Blocking Time information in the footer</span></span>  

<span data-ttu-id="64511-187">Après avoir enregistré vos performances de chargement, le panneau **Performances** affiche désormais les informations sur le temps de blocage total \(TBT\) dans le pied de groupe.</span><span class="sxs-lookup"><span data-stu-id="64511-187">After recording your load performance, the **Performance** panel now shows Total Blocking Time \(TBT\) information in the footer.</span></span>  <span data-ttu-id="64511-188">TBT est une mesure de performances de charge qui permet de quantifier le temps qu’une page prend pour devenir utilisable.</span><span class="sxs-lookup"><span data-stu-id="64511-188">TBT is a load performance metric that helps quantify how long a page takes to become usable.</span></span>  <span data-ttu-id="64511-189">Elle mesure essentiellement la durée pendant combien de temps une page semble utilisable \(car le contenu est restituer à l’écran\) ; mais n’est pas réellement utilisable, car JavaScript bloque le thread principal et par conséquent, la page ne répond pas aux entrées de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="64511-189">It essentially measures how long a page appears to be usable \(because the content is rendered to the screen\); but is not actually usable, because JavaScript is blocking the main thread and therefore the page does not respond to user input.</span></span>  <span data-ttu-id="64511-190">TBT est la mesure principale pour l’approximation du premier délai d’entrée.</span><span class="sxs-lookup"><span data-stu-id="64511-190">TBT is the main metric for approximating First Input Delay.</span></span>  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

<span data-ttu-id="64511-191">Pour obtenir les informations sur le \*\*\*\* temps total de blocage, n’utilisez pas le flux de travail d’icône Actualiser la page Actualiser la page pour enregistrer les ![ performances de chargement de ][ImageRefreshPageIcon] page.</span><span class="sxs-lookup"><span data-stu-id="64511-191">To get Total Blocking Time information, do not use the **Refresh Page** ![Refresh page icon][ImageRefreshPageIcon] workflow for recording page load performance.</span></span>  

<span data-ttu-id="64511-192">Sélectionnez plutôt **l’icône Enregistrement** , rechargez manuellement la page, attendez le chargement de la ![ ][ImageRecordIcon] page, puis arrêtez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="64511-192">Instead, select **Record** ![Record icon][ImageRecordIcon], manually reload the page, wait for the page to load, and then stop recording.</span></span>  

<span data-ttu-id="64511-193">`Total Blocking Time: Unavailable`S’il est affiché, Microsoft Edge DevTools n’a pas eu les informations requises à partir des données de profilage internes dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="64511-193">If `Total Blocking Time: Unavailable` is displayed, Microsoft Edge DevTools did not get the required information from the internal profiling data in Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Total Blocking Time information in the footer of a Performance panel recording" lightbox="../../media/2020/05/tbt.msft.png":::
   <span data-ttu-id="64511-195">Total Blocking Time information in the footer of a **Performance** panel recording</span><span class="sxs-lookup"><span data-stu-id="64511-195">Total Blocking Time information in the footer of a **Performance** panel recording</span></span>  
:::image-end:::  

<span data-ttu-id="64511-196">Problème de chrome [#1054381][CR1054381]</span><span class="sxs-lookup"><span data-stu-id="64511-196">Chromium issue [#1054381][CR1054381]</span></span>  

#### <a name="layout-shift-events-in-the-new-experience-section"></a><span data-ttu-id="64511-197">Événements Layout Shift dans la nouvelle section Expérience</span><span class="sxs-lookup"><span data-stu-id="64511-197">Layout Shift events in the new Experience section</span></span>  

<span data-ttu-id="64511-198">La nouvelle section **Expérience** du panneau **Performances** vous permet de détecter les changements de disposition.</span><span class="sxs-lookup"><span data-stu-id="64511-198">The new **Experience** section of the **Performance** panel helps you detect layout shifts.</span></span>  <span data-ttu-id="64511-199">La mise en page cumulative Shift \(CLS\) est une mesure qui vous permet de quantifier l’instabilité visuelle indésirable.</span><span class="sxs-lookup"><span data-stu-id="64511-199">Cumulative Layout Shift \(CLS\) is a metric that helps you quantify unwanted visual instability.</span></span>

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

<span data-ttu-id="64511-200">Choisissez **l’événement Layout Shift** pour afficher les détails de l’équipe de disposition dans le **volet** Résumé.</span><span class="sxs-lookup"><span data-stu-id="64511-200">Choose the **Layout Shift** event to display the details of the layout shift in the **Summary** pane.</span></span>  <span data-ttu-id="64511-201">Pointez sur **les champs Déplacé d’et** Déplacé **vers** pour visualiser l’endroit où le changement de disposition s’est produit.</span><span class="sxs-lookup"><span data-stu-id="64511-201">Hover on the **Moved from** and **Moved to** fields to visualize where the layout shift occurred.</span></span>  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Détails d’un changement de disposition" lightbox="../../media/2020/05/cls.msft.png":::
   <span data-ttu-id="64511-203">Détails d’un changement de disposition</span><span class="sxs-lookup"><span data-stu-id="64511-203">The details of a layout shift</span></span>  
:::image-end:::  

### <a name="more-accurate-promise-terminology-in-the-console"></a><span data-ttu-id="64511-204">Terminologie des promesses plus précise dans la console</span><span class="sxs-lookup"><span data-stu-id="64511-204">More accurate promise terminology in the Console</span></span>  

<span data-ttu-id="64511-205">Lors de la `Promise` journalisation d’un , **la console** a fourni de `PromiseStatus` manière incorrecte la valeur définie sur `resolved` .</span><span class="sxs-lookup"><span data-stu-id="64511-205">When logging a `Promise`, the **Console** incorrectly provided `PromiseStatus` value set to `resolved`.</span></span>  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Exemple de console utilisant l’ancienne terminologie résolue" lightbox="../../media/2020/05/resolved.msft.png":::
   <span data-ttu-id="64511-207">Exemple de console **utilisant** l’ancienne `resolved` terminologie</span><span class="sxs-lookup"><span data-stu-id="64511-207">An example of the **Console** using the old `resolved` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="64511-208">La **console** utilise désormais le terme `fulfilled` , qui s’aligne sur la `Promise` spécification.</span><span class="sxs-lookup"><span data-stu-id="64511-208">The **Console** now uses the term `fulfilled`, which aligns with the `Promise` specification.</span></span>  <span data-ttu-id="64511-209">Pour plus d’informations sur `Promise` la spécification, accédez à [États et à Sons sur GitHub.](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md)</span><span class="sxs-lookup"><span data-stu-id="64511-209">For more information about the `Promise` specification, navigate to [States and Fates on GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span></span>  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Exemple de console utilisant la nouvelle terminologie utilisée" lightbox="../../media/2020/05/fulfilled.msft.png":::
  <span data-ttu-id="64511-211">Exemple de console **utilisant** la nouvelle `fulfilled` terminologie</span><span class="sxs-lookup"><span data-stu-id="64511-211">An example of the **Console** using the new `fulfilled` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="64511-212">Problème V8 [#6751][CRV86751]</span><span class="sxs-lookup"><span data-stu-id="64511-212">V8 issue [#6751][CRV86751]</span></span>  

### <a name="styles-pane-updates"></a><span data-ttu-id="64511-213">Mises à jour du volet Styles</span><span class="sxs-lookup"><span data-stu-id="64511-213">Styles pane updates</span></span>  

#### <a name="support-for-the-revert-keyword"></a><span data-ttu-id="64511-214">Prise en charge du mot clé de revert</span><span class="sxs-lookup"><span data-stu-id="64511-214">Support for the revert keyword</span></span>  

<span data-ttu-id="64511-215">L’interface utilisateur de la mise à jour automatique du volet **Styles** détecte désormais le mot clé [CSS][MDNRevert] qui permet de revenir à la valeur en cascade d’une propriété à la valeur précédente appliquée au style de l’élément.</span><span class="sxs-lookup"><span data-stu-id="64511-215">The autocomplete UI of the **Styles** pane now detects the [revert][MDNRevert] CSS keyword, which reverts the cascaded value of a property to the previous value applied to the styling of the element.</span></span>  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Définition de la valeur d’une propriété à inverser" lightbox="../../media/2020/05/revert.msft.png":::
  <span data-ttu-id="64511-217">Définition de la valeur d’une propriété à inverser</span><span class="sxs-lookup"><span data-stu-id="64511-217">Setting the value of a property to revert</span></span>  
:::image-end:::  

<span data-ttu-id="64511-218">Problème de chrome [#1075437][CR1075437]</span><span class="sxs-lookup"><span data-stu-id="64511-218">Chromium issue [#1075437][CR1075437]</span></span>  

#### <a name="image-previews"></a><span data-ttu-id="64511-219">Aperçus d’image</span><span class="sxs-lookup"><span data-stu-id="64511-219">Image previews</span></span>  

<span data-ttu-id="64511-220">Pointez sur une valeur dans le volet Styles pour afficher un aperçu de `background-image` l’image \*\*\*\* dans une boîte à outils.</span><span class="sxs-lookup"><span data-stu-id="64511-220">Hover on a `background-image` value in the **Styles** pane to display a preview of the image in a tooltip.</span></span>  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Pointage sur une valeur d’image d’arrière-plan" lightbox="../../media/2020/05/image-preview.msft.png":::
  <span data-ttu-id="64511-222">Pointage sur une `background-image` valeur</span><span class="sxs-lookup"><span data-stu-id="64511-222">Hovering over a `background-image` value</span></span>  
:::image-end:::  

<span data-ttu-id="64511-223">Problème de chrome [#1040019][CR1040019]</span><span class="sxs-lookup"><span data-stu-id="64511-223">Chromium issue [#1040019][CR1040019]</span></span>  

#### <a name="color-picker-now-uses-space-separated-functional-color-notation"></a><span data-ttu-id="64511-224">Le s sélectionneur de couleurs utilise désormais la notation de couleur fonctionnelle séparée par des espaces</span><span class="sxs-lookup"><span data-stu-id="64511-224">Color Picker now uses space-separated functional color notation</span></span>  

<span data-ttu-id="64511-225">Le module [de couleur CSS de niveau 4][CSSWGDraftsColor4Changes3] spécifie que les fonctions de couleur, telles que , doivent prendre en charge les `rgb()` arguments séparés par des espaces.</span><span class="sxs-lookup"><span data-stu-id="64511-225">[CSS Color Module Level 4][CSSWGDraftsColor4Changes3] specifies that color functions, such as `rgb()`, should support space-separated arguments.</span></span>  <span data-ttu-id="64511-226">Par exemple, `rgb(0, 0, 0)` revient à spécifier `rbg(0 0 0)`.</span><span class="sxs-lookup"><span data-stu-id="64511-226">For example, `rgb(0, 0, 0)` is equivalent to `rbg(0 0 0)`.</span></span>  

<span data-ttu-id="64511-227">Lorsque vous choisissez [][DevtoolsCssReferenceColorPicker] des couleurs avec le sélecateur de couleurs ou si vous choisissez une autre représentation des couleurs dans le volet **Styles** en maintenant et en sélectionnant la valeur, la syntaxe de l’argument séparé par des espaces `Shift` `background-color` s’affiche.</span><span class="sxs-lookup"><span data-stu-id="64511-227">When you choose colors with the [Color Picker][DevtoolsCssReferenceColorPicker] or alternate between color representations in the **Styles** pane by holding `Shift` and selecting the `background-color` value, the space-separated argument syntax is displayed.</span></span>  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Utilisation d’arguments séparés par des espaces dans le volet Styles" lightbox="../../media/2020/05/color.msft.png":::
  <span data-ttu-id="64511-229">Utilisation d’arguments séparés par des espaces dans le **volet Styles**</span><span class="sxs-lookup"><span data-stu-id="64511-229">Using space-separated arguments in the **Styles** pane</span></span>  
:::image-end:::  

<span data-ttu-id="64511-230">Vous devez également afficher la syntaxe dans le volet **Calculé** et **l’info-bulle du mode** Inspect.</span><span class="sxs-lookup"><span data-stu-id="64511-230">You should also display the syntax in the **Computed** pane and the **Inspect Mode** tooltip.</span></span>  

<span data-ttu-id="64511-231">Microsoft Edge DevTools utilise la nouvelle syntaxe, car les fonctionnalités CSS à venir, telles que [color()][CSSWGDraftsColor4Property] ne la prise en charge de la syntaxe d’arguments séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="64511-231">Microsoft Edge DevTools is using the new syntax because upcoming CSS features such as [color()][CSSWGDraftsColor4Property] do not support the deprecated comma-separated argument syntax.</span></span>  

<span data-ttu-id="64511-232">La syntaxe de l’argument séparé par des espaces est prise en charge dans la plupart des navigateurs depuis un certain temps.</span><span class="sxs-lookup"><span data-stu-id="64511-232">The space-separated argument syntax has been supported in most browsers for a while.</span></span>  <span data-ttu-id="64511-233">Pour plus d’informations, accédez à [Can I use: Space-separated functional color notations?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span><span class="sxs-lookup"><span data-stu-id="64511-233">For more information, navigate to [Can I use: Space-separated functional color notations?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span></span>  

<span data-ttu-id="64511-234">Problème de chrome [#1072952][CR1072952]</span><span class="sxs-lookup"><span data-stu-id="64511-234">Chromium issue [#1072952][CR1072952]</span></span>  

### <a name="deprecation-of-the-properties-pane-in-the-elements-panel"></a><span data-ttu-id="64511-235">Désopation du volet Propriétés dans le panneau Éléments</span><span class="sxs-lookup"><span data-stu-id="64511-235">Deprecation of the Properties pane in the Elements panel</span></span>  

<span data-ttu-id="64511-236">Le **volet Propriétés** de **l’outil Éléments** est supprimé.</span><span class="sxs-lookup"><span data-stu-id="64511-236">The **Properties** pane in the **Elements** tool is deprecated.</span></span>  <span data-ttu-id="64511-237">`console.dir($0)`Exécutez-la **dans la console** à la place.</span><span class="sxs-lookup"><span data-stu-id="64511-237">Run `console.dir($0)` in the **Console** instead.</span></span>  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="Volet Propriétés déprécié" lightbox="../../media/2020/05/properties.msft.png":::
   <span data-ttu-id="64511-239">Volet Propriétés \*\*\*\* déprécié</span><span class="sxs-lookup"><span data-stu-id="64511-239">The deprecated **Properties** pane</span></span>  
:::image-end:::  

#### <a name="references"></a><span data-ttu-id="64511-240">Références</span><span class="sxs-lookup"><span data-stu-id="64511-240">References</span></span>  

*   [<span data-ttu-id="64511-241">console.dir()</span><span class="sxs-lookup"><span data-stu-id="64511-241">console.dir()</span></span>][DevtoolsConsoleApiDir]  
*   [<span data-ttu-id="64511-242">$0</span><span class="sxs-lookup"><span data-stu-id="64511-242">$0</span></span>][DevtoolsConsoleUtilitiesDom]  

### <a name="app-shortcuts-support-in-the-manifest-pane"></a><span data-ttu-id="64511-243">Prise en charge des raccourcis d’application dans le volet manifeste</span><span class="sxs-lookup"><span data-stu-id="64511-243">App shortcuts support in the Manifest pane</span></span>  

<span data-ttu-id="64511-244">Les raccourcis d’application aident les utilisateurs à démarrer rapidement des tâches courantes ou recommandées dans une application web.</span><span class="sxs-lookup"><span data-stu-id="64511-244">App shortcuts help users quickly start common or recommended tasks within a web app.</span></span>  <span data-ttu-id="64511-245">Le menu des raccourcis de l’application s’affiche uniquement pour les applications [web][PwaIndex] progressives installées sur le bureau ou l’appareil mobile de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="64511-245">The app shortcuts menu is shown only for [Progressive Web Apps][PwaIndex] that are installed on the user's desktop or mobile device.</span></span>  

<!--For more information, navigate to [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Raccourcis d’application dans le volet manifeste" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  <span data-ttu-id="64511-247">Raccourcis d’application dans le **volet** manifeste</span><span class="sxs-lookup"><span data-stu-id="64511-247">App shortcuts in the **Manifest** pane</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="64511-248">Télécharger les canaux d’aperçu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="64511-248">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="64511-249">Si vous utilisez Windows ou macOS, envisagez d’utiliser les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.</span><span class="sxs-lookup"><span data-stu-id="64511-249">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="64511-250">Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="64511-250">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="64511-251">Mise en contact avec l’équipe Devtools de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="64511-251">Getting in touch with Microsoft Edge Devtools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/settings-icon.msft.png  
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/toggle-screencast-icon.msft.png  
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/refresh-page-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/record-icon.msft.png  

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Utiliser l’émulateur Surface Duo | Documents Microsoft"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir - Console API Reference | Documents Microsoft"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Élément récemment sélectionné ou objet JavaScript - Référence de l’API des utilitaires de console | Documents Microsoft"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Modifier les couleurs à l'| Documents Microsoft"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Drawer - Customize Overview | Documents Microsoft"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Rechercher et résoudre les problèmes liés à l’onglet Problèmes de Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Mise en place du débogage à distance des appareils Android | Documents Microsoft"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Mise en route des émulateurs Surface Duo de débogage à distance | Documents Microsoft"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Mise en place du débogage à distance des appareils Windows 10 | Documents Microsoft"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Inspecter les détails de la ressource | Documents Microsoft"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Journal de l’activité réseau | Documents Microsoft"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Applications web progressives sur Windows | Documents Microsoft"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Application Microsoft Edge Android"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Notations de couleur fonctionnelles séparées par des espaces : | Puis-je utiliser"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"

[CR174309]: https://crbug.com/174309 "DevTools : autoriser la personnalisation des raccourcis clavier/des liaisons de touches | Bogues Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools ne sont pas conformes WCAG | Bogues Chromium"  
[CR1040019]: https://crbug.com/1040019 "DevTools : afficher facilement un aperçu des images et des images d’arrière-plan dans le volet Styles | Bogues Chromium"  
[CR1040025]: https://crbug.com/1040025 "DevTools : afficher des informations a11y de base dans la fenêtre de | Bogues Chromium"  
[CR1048378]: https://crbug.com/1048378 "Prise en charge de l’interface utilisateur DevTools pour les | Bogues Chromium"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Bogues Chromium"  
[CR1068116]: https://crbug.com/1068116 "Ship issues panel | Bogues Chromium"  
[CR1072952]: https://crbug.com/1072952 "DevTools: color picker should produce modern CSS color syntax | Bogues Chromium"  
[CR1075437]: https://crbug.com/1075437 "DevTools : ajoutez la prise en charge du mot clé/valeur CSS « revert » | Bogues Chromium"  
[CR1076112]: https://crbug.com/1076112 "Personnalisation des devtools : resiseur de caisse"  
[CR1081486]: https://crbug.com/1081486 "Le focus du clavier n’est pas visible pour les boutons de navigation en mode de capture d’écran | Bogues Chromium"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus doit être « rempli » et non « résolu » | Bogues V8"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Modifications apportées à Couleurs 3 - Module de couleur CSS niveau 4 | Brouillons de l’éditeur de groupe de travail CSS W3C"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. Couleur de premier plan : la couleur - Module de couleur CSS niveau 4 | Brouillons de l’éditeur de groupe de travail CSS W3C"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Présentation du nouveau Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "États-et-Unis - domenic/promises-unwrapping | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "| MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Compatibilité des navigateurs | MDN"  

[VisualStudioCode]: https://code.visualstudio.com/ "Visual Studio Code"  
[VisualStudioCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio clavier du code pour Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe : clavier | WebHint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe : valeur de rôle de nom | WebHint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Activer ou désactiver le mode contraste élevé dans Windows | Prise en charge de Windows"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publier un Tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nouveau problème : MicrosoftDocs/edge-developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canaux d’aperçu Microsoft Edge"  
[TheWebWeWant]: https://aka.ms/webwewant "Le site Web de votre choix"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> <span data-ttu-id="64511-296">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="64511-296">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="64511-297">La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/05/devtools/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="64511-297">The original page is found [here](https://developers.google.com/web/updates/2020/05/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="64511-299">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="64511-299">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
