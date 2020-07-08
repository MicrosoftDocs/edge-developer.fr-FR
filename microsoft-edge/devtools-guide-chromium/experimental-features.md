---
description: Dernières fonctionnalités expérimentales de Microsoft Edge DevTools
title: Fonctionnalités expérimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, expérience
ms.openlocfilehash: 19fd59c5dd9f18a681c69250fdcddb22e2796565
ms.sourcegitcommit: f92bf0b50812b43228990b794611daa2144e431c
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2020
ms.locfileid: "10858051"
---
# <span data-ttu-id="8841a-104">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="8841a-104">Experimental features</span></span>  

<span data-ttu-id="8841a-105">Vous pouvez utiliser les fonctionnalités expérimentales qui sont toujours en cours de développement dans Microsoft Edge DevTools pour tester et [transmettre des commentaires](#providing-feedback-on-experimental-features) avant chaque sortie.</span><span class="sxs-lookup"><span data-stu-id="8841a-105">You may use the experimental features that are still under development in the Microsoft Edge DevTools to test and [provide feedback](#providing-feedback-on-experimental-features) before each is released broadly.</span></span>  

<span data-ttu-id="8841a-106">Si les fonctionnalités expérimentales sont disponibles dans tous les canaux de Microsoft Edge, vous pouvez obtenir les dernières fonctionnalités expérimentales à l’aide du canal des Canaries Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8841a-106">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="8841a-107">Activer les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="8841a-107">Turn on experimental features</span></span>  

<span data-ttu-id="8841a-108">Procédez comme suit pour activer ou désactiver les fonctionnalités expérimentales dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8841a-108">Use the following steps to turn on \(or off\) experimental features in Microsoft Edge.</span></span>  

1.  <span data-ttu-id="8841a-109">[Ouvrez devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="8841a-109">[Open DevTools][DevtoolsOpen].</span></span>  
     *   <span data-ttu-id="8841a-110">Appuyez sur `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="8841a-110">Press `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="8841a-111">Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="8841a-111">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="8841a-112">Ouvrez le volet [paramètres][DevToolsCustomizeSettings] .</span><span class="sxs-lookup"><span data-stu-id="8841a-112">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="8841a-113">Appuyez sur `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="8841a-113">Press `Shift`+`?`.</span></span>  <span data-ttu-id="8841a-114">Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="8841a-114">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="8841a-115">Sur le côté gauche du volet **paramètres** , sélectionnez la section **expériences** .</span><span class="sxs-lookup"><span data-stu-id="8841a-115">On the left side of the **Settings** pane, select the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/experiments-devtools.png":::
       <span data-ttu-id="8841a-117">Liste des expériences dans les paramètres de DevTools</span><span class="sxs-lookup"><span data-stu-id="8841a-117">List of experiments in DevTools Settings</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8841a-118">Sur la page **expériences** , faites défiler la liste de toutes les fonctionnalités expérimentales disponibles, puis cochez la case en regard de chaque fonctionnalité que vous voulez tester.</span><span class="sxs-lookup"><span data-stu-id="8841a-118">On the **Experiments** page, scroll through the list of all available experimental features and select the checkbox next to each features that you want to test.</span></span>  
1.  <span data-ttu-id="8841a-119">Fermez et rouvrez Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="8841a-119">Close and reopen Microsoft Edge DevTools.</span></span>  

> [!NOTE]
> <span data-ttu-id="8841a-120">Les fonctionnalités expérimentales sont constamment mises à jour et peuvent entraîner des problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="8841a-120">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="8841a-121">Pour désactiver une fonctionnalité expérimentale, ouvrez la page **expériences** , puis décochez la case de la fonctionnalité expérimental que vous souhaitez désactiver.</span><span class="sxs-lookup"><span data-stu-id="8841a-121">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="8841a-122">Fonctionnalités expérimentales mises en évidence</span><span class="sxs-lookup"><span data-stu-id="8841a-122">Highlighted experimental features</span></span>  

<span data-ttu-id="8841a-123">Les sections suivantes décrivent les nouvelles fonctionnalités expérimentales disponibles dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8841a-123">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="8841a-124">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="8841a-124">Experimental feature</span></span> | <span data-ttu-id="8841a-125">Version de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8841a-125">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="8841a-126">Activer l’onglet Paramètres de raccourcis clavier personnalisés</span><span class="sxs-lookup"><span data-stu-id="8841a-126">Enable custom keyboard shortcuts settings tab</span></span>](#enable-custom-keyboard-shortcuts-settings-tab) | <span data-ttu-id="8841a-127">84 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8841a-127">84 or later</span></span> |
| [<span data-ttu-id="8841a-128">Activer les nouvelles fonctionnalités de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="8841a-128">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="8841a-129">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8841a-129">85 or later</span></span> |  
| [<span data-ttu-id="8841a-130">Activer la prise en charge du déplacement des onglets entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="8841a-130">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="8841a-131">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8841a-131">85 or later</span></span> |  
| [<span data-ttu-id="8841a-132">Activer webhint</span><span class="sxs-lookup"><span data-stu-id="8841a-132">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="8841a-133">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8841a-133">85 or later</span></span> |  

### <span data-ttu-id="8841a-134">Activer l’onglet Paramètres de raccourcis clavier personnalisés</span><span class="sxs-lookup"><span data-stu-id="8841a-134">Enable custom keyboard shortcuts settings tab</span></span>

<span data-ttu-id="8841a-135">Fournit une nouvelle page de **raccourcis** dans les [paramètres de devtools][DevToolsCustomizeSettings] qui permet d’associer des [raccourcis clavier][DevToolsShortcuts] dans le devtools au [code vs][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="8841a-135">Provides a new **Shortcuts** page in [DevTools Settings][DevToolsCustomizeSettings] that enables matching [keyboard shortcuts][DevToolsShortcuts] in the DevTools to [VS Code][VisualstudioCode].</span></span>  

<span data-ttu-id="8841a-136">Une fois que vous avez activé cette expérience, ouvrez de nouveau [devtools paramètres][DevToolsCustomizeSettings] en appuyant sur `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="8841a-136">Once you have enabled this experiment, open [DevTools Settings][DevToolsCustomizeSettings] again by pressing `Shift`+`?`.</span></span>  <span data-ttu-id="8841a-137">Accédez à la page nouveau **raccourcis** .</span><span class="sxs-lookup"><span data-stu-id="8841a-137">Navigate to the new **Shortcuts** page.</span></span>  <span data-ttu-id="8841a-138">Sélectionnez **devtools (par défaut)** dans le menu déroulant **correspondant aux raccourcis de** la liste déroulante, puis sélectionnez **Visual Studio code**.</span><span class="sxs-lookup"><span data-stu-id="8841a-138">Select **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="8841a-139">Les raccourcis clavier dans le DevTools correspondent désormais aux raccourcis pour les actions équivalentes dans le code VS.</span><span class="sxs-lookup"><span data-stu-id="8841a-139">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in VS Code.</span></span>  

:::image type="complex" source="./media/experiments-keyboard-shortcut.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code VS" lightbox="./media/experiments-keyboard-shortcut.png":::
   <span data-ttu-id="8841a-141">Faire correspondre les raccourcis clavier du DevTools au code VS</span><span class="sxs-lookup"><span data-stu-id="8841a-141">Match keyboard shortcuts in the DevTools to VS Code</span></span>
:::image-end:::  

<span data-ttu-id="8841a-142">Par exemple, dans Windows, le raccourci clavier pour suspendre ou continuer à exécuter un script en [code vs][VisualstudioCodeShortcutsKeyboardWindows] est `F5` .</span><span class="sxs-lookup"><span data-stu-id="8841a-142">For example, on Windows the keyboard shortcut for pausing or continuing running a script in [VS Code][VisualstudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="8841a-143">Avec la valeur prédéfinie **devtools (par défaut)** , ce raccourci est le même dans devtools qu' `F8` avec le **code prédéfini Visual Studio** , ce raccourci est désormais également disponible `F5` .</span><span class="sxs-lookup"><span data-stu-id="8841a-143">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8` but with the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

### <span data-ttu-id="8841a-144">Activer les nouvelles fonctionnalités de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="8841a-144">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="8841a-145">Permet d’améliorer les visualisations sur la page lorsque vous déboguez des sites Web dotés de dispositions CSS.</span><span class="sxs-lookup"><span data-stu-id="8841a-145">Improves on-page visualizations when you debug websites that have CSS grid layouts.</span></span>  <span data-ttu-id="8841a-146">Vous pouvez personnaliser davantage les superpositions dans les paramètres de DevTools.</span><span class="sxs-lookup"><span data-stu-id="8841a-146">You may further customize the overlays in DevTools Settings.</span></span>  

:::image type="complex" source="./media/experiments-grid.png" alt-text="Fonctionnalité de débogage de grille CSS" lightbox="./media/experiments-grid.png":::
   <span data-ttu-id="8841a-148">Fonctionnalité de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="8841a-148">CSS grid debugging feature</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="8841a-149">Activer la prise en charge du déplacement des onglets entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="8841a-149">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="8841a-150">En règle générale, il est possible d’ouvrir des outils tels que des **éléments** et un **réseau** uniquement dans le panneau principal \ (Top \) de devtools.</span><span class="sxs-lookup"><span data-stu-id="8841a-150">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="8841a-151">De même, il est possible d’ouvrir des outils tels que la vue et les **problèmes** en **3D** uniquement dans le panneau tiroir \ (en bas) de devtools.</span><span class="sxs-lookup"><span data-stu-id="8841a-151">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="8841a-152">Lorsque cette expérience est sélectionnée, vous pouvez déplacer des outils entre les volets supérieur et inférieur en pointant sur l’onglet, en ouvrant le menu contextuel \ (clic droit sur \) et en sélectionnant **déplacer vers le haut** ou **déplacer vers le bas**.</span><span class="sxs-lookup"><span data-stu-id="8841a-152">When this experiment is selected, you may move tools between the top and bottom panels by hovering on the tab, opening the contextual menu \(right-click\), and selecting **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="8841a-153">Cette expérience vous permet de personnaliser la disposition de votre DevTools.</span><span class="sxs-lookup"><span data-stu-id="8841a-153">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="8841a-154">Pour afficher ou masquer le panneau inférieur, appuyez sur `Escape` .</span><span class="sxs-lookup"><span data-stu-id="8841a-154">To show or hide the bottom panel, press `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Déplacement d’un onglet entre les panneaux" lightbox="./media/experiments-move-panels.png":::
   <span data-ttu-id="8841a-156">Déplacement d’un onglet entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="8841a-156">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="8841a-157">Activer webhint</span><span class="sxs-lookup"><span data-stu-id="8841a-157">Enable webhint</span></span>  

<span data-ttu-id="8841a-158">[webhint][WebhintMain] est un outil open source qui fournit des commentaires en temps réel sur l’accessibilité, la compatibilité entre les navigateurs, la sécurité, les performances, PWAS, ainsi que d’autres problèmes courants liés au développement Web sur les sites Web.</span><span class="sxs-lookup"><span data-stu-id="8841a-158">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="8841a-159">Cette expérience apporte le commentaire de webhint à DevTools dans le volet des [problèmes][DevtoolsIssues] .</span><span class="sxs-lookup"><span data-stu-id="8841a-159">This experiment brings the webhint feedback into DevTools in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="8841a-160">Vous pouvez sélectionner le problème pour voir la documentation relative à la résolution du problème ainsi qu’une liste des ressources affectées sur votre site Web.</span><span class="sxs-lookup"><span data-stu-id="8841a-160">You may select the issue to see documentation on how to fix the issue and a list of the affected resources on your website.</span></span>  <span data-ttu-id="8841a-161">Sélectionnez un lien vers une ressource pour ouvrir le volet **réseau**, **sources**ou **éléments** approprié dans devtools.</span><span class="sxs-lookup"><span data-stu-id="8841a-161">Select a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="Commentaires de webhint dans le volet problèmes" lightbox="./media/experiments-webhint.png":::
   <span data-ttu-id="8841a-163">Commentaires de webhint dans le volet problèmes</span><span class="sxs-lookup"><span data-stu-id="8841a-163">webhint feedback in the Issues panel</span></span>  
:::image-end:::      

<!--Available in Microsoft Edge version 85 and later.  -->  

## <span data-ttu-id="8841a-164">Fonctionnalités expérimentales antérieures</span><span class="sxs-lookup"><span data-stu-id="8841a-164">Previous experimental features</span></span>  

*   <span data-ttu-id="8841a-165">la [vue 3D][Devtools3dViewIndex] est désormais disponible et activée par défaut dans Microsoft Edge version 83 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8841a-165">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  

## <span data-ttu-id="8841a-166">Fourniture de commentaires sur les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="8841a-166">Providing feedback on experimental features</span></span>  

<span data-ttu-id="8841a-167">Pour transmettre des commentaires sur les expériences DevTools Microsoft Edge, ou tout autre élément associé à DevTools.</span><span class="sxs-lookup"><span data-stu-id="8841a-167">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="8841a-168">Envoyez vos commentaires à l’aide de l’icône de commentaires dans le DevTools</span><span class="sxs-lookup"><span data-stu-id="8841a-168">Send your feedback using the Feedback icon in the DevTools</span></span>  
*   <span data-ttu-id="8841a-169">Tweeter sur [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="8841a-169">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="./media/devtools-feedback.png" alt-text="Icône de commentaires dans le Microsoft Edge DevTools" lightbox="./media/devtools-feedback.png":::
   <span data-ttu-id="8841a-171">Icône de commentaires dans le Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8841a-171">Feedback icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Affichage 3D | Documents Microsoft"  
[DevtoolsIssues]: ./issues/index.md "Recherchez et corrigez les problèmes liés à l’outil problèmes dans Microsoft Edge DevTools Documents Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Raccourcis clavier dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsOpen]: ./open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[VisualstudioCode]: https://code.visualstudio.com "Code Visual Studio"  
[VisualstudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Raccourcis clavier dans Visual Studio pour Windows | Code Visual Studio"  

[WebhintMain]: https://webhint.io "Astuce" 
