---
description: Dernières fonctionnalités expérimentales de Microsoft Edge DevTools
title: Fonctionnalités expérimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/21/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, expérience
ms.openlocfilehash: 6b3e1c06d6b8ed79054c28df483fcca93e5751d6
ms.sourcegitcommit: 19ef1422733ef1fd051d2b4f0263ce191e8d67bc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/31/2020
ms.locfileid: "10902851"
---
# <span data-ttu-id="9a472-104">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="9a472-104">Experimental features</span></span>  

<span data-ttu-id="9a472-105">Vous pouvez utiliser les fonctionnalités expérimentales qui sont toujours en cours de développement dans Microsoft Edge DevTools pour tester et [transmettre des commentaires](#providing-feedback-on-experimental-features) avant chaque sortie.</span><span class="sxs-lookup"><span data-stu-id="9a472-105">You may use the experimental features that are still under development in the Microsoft Edge DevTools to test and [provide feedback](#providing-feedback-on-experimental-features) before each is released broadly.</span></span>  

<span data-ttu-id="9a472-106">Si les fonctionnalités expérimentales sont disponibles dans tous les canaux de Microsoft Edge, vous pouvez obtenir les dernières fonctionnalités expérimentales à l’aide du canal des Canaries Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a472-106">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="9a472-107">Activer les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="9a472-107">Turn on experimental features</span></span>  

<span data-ttu-id="9a472-108">Procédez comme suit pour activer ou désactiver les fonctionnalités expérimentales dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a472-108">Use the following steps to turn on \(or off\) experimental features in Microsoft Edge.</span></span>  

1.  <span data-ttu-id="9a472-109">[Ouvrez devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="9a472-109">[Open DevTools][DevtoolsOpen].</span></span>  
     *   <span data-ttu-id="9a472-110">Sélectionnez `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="9a472-110">Select `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="9a472-111">Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="9a472-111">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="9a472-112">Ouvrez le volet [paramètres][DevToolsCustomizeSettings] .</span><span class="sxs-lookup"><span data-stu-id="9a472-112">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="9a472-113">Sélectionnez `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="9a472-113">Select `Shift`+`?`.</span></span>  <span data-ttu-id="9a472-114">Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="9a472-114">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="9a472-115">Sur le côté gauche du volet **paramètres** , sélectionnez la section **expériences** .</span><span class="sxs-lookup"><span data-stu-id="9a472-115">On the left side of the **Settings** pane, select the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/experiments-devtools.png":::
       <span data-ttu-id="9a472-117">Liste des expériences dans les paramètres de DevTools</span><span class="sxs-lookup"><span data-stu-id="9a472-117">List of experiments in DevTools Settings</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9a472-118">Sur la page **expériences** , faites défiler la liste de toutes les fonctionnalités expérimentales disponibles, puis cochez la case en regard de chaque fonctionnalité que vous voulez tester.</span><span class="sxs-lookup"><span data-stu-id="9a472-118">On the **Experiments** page, scroll through the list of all available experimental features and select the checkbox next to each features that you want to test.</span></span>  
1.  <span data-ttu-id="9a472-119">Fermez et rouvrez Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="9a472-119">Close and reopen Microsoft Edge DevTools.</span></span>  

> [!NOTE]
> <span data-ttu-id="9a472-120">Les fonctionnalités expérimentales sont constamment mises à jour et peuvent entraîner des problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="9a472-120">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="9a472-121">Pour désactiver une fonctionnalité expérimentale, ouvrez la page **expériences** , puis décochez la case de la fonctionnalité expérimental que vous souhaitez désactiver.</span><span class="sxs-lookup"><span data-stu-id="9a472-121">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="9a472-122">Fonctionnalités expérimentales mises en évidence</span><span class="sxs-lookup"><span data-stu-id="9a472-122">Highlighted experimental features</span></span>  

<span data-ttu-id="9a472-123">Les sections suivantes décrivent les nouvelles fonctionnalités expérimentales disponibles dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a472-123">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="9a472-124">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="9a472-124">Experimental feature</span></span> | <span data-ttu-id="9a472-125">Version de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9a472-125">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="9a472-126">Activer l’onglet Paramètres de raccourcis clavier personnalisés</span><span class="sxs-lookup"><span data-stu-id="9a472-126">Enable custom keyboard shortcuts settings tab</span></span>](#enable-custom-keyboard-shortcuts-settings-tab) | <span data-ttu-id="9a472-127">84 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9a472-127">84 or later</span></span> |
| [<span data-ttu-id="9a472-128">Activer les nouvelles fonctionnalités de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="9a472-128">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="9a472-129">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9a472-129">85 or later</span></span> |  
| [<span data-ttu-id="9a472-130">Activer la prise en charge du déplacement des onglets entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="9a472-130">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="9a472-131">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9a472-131">85 or later</span></span> |  
| [<span data-ttu-id="9a472-132">Activer webhint</span><span class="sxs-lookup"><span data-stu-id="9a472-132">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="9a472-133">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9a472-133">85 or later</span></span> | 
| [<span data-ttu-id="9a472-134">Activer la console réseau</span><span class="sxs-lookup"><span data-stu-id="9a472-134">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="9a472-135">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9a472-135">85 or later</span></span> |

### <span data-ttu-id="9a472-136">Activer l’onglet Paramètres de raccourcis clavier personnalisés</span><span class="sxs-lookup"><span data-stu-id="9a472-136">Enable custom keyboard shortcuts settings tab</span></span>

<span data-ttu-id="9a472-137">Fournit une nouvelle page de **raccourcis** dans les [paramètres de devtools][DevToolsCustomizeSettings] qui permet d’associer des [raccourcis clavier][DevToolsShortcuts] dans le devtools au [code vs][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="9a472-137">Provides a new **Shortcuts** page in [DevTools Settings][DevToolsCustomizeSettings] that enables matching [keyboard shortcuts][DevToolsShortcuts] in the DevTools to [VS Code][VisualstudioCode].</span></span>  

<span data-ttu-id="9a472-138">Une fois que vous avez activé l’expérience, rouvrez les [paramètres de devtools][DevToolsCustomizeSettings] à l’aide de la sélection `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="9a472-138">Once you have enabled the experiment, open [DevTools Settings][DevToolsCustomizeSettings] again using select `Shift`+`?`.</span></span>  <span data-ttu-id="9a472-139">Accédez à la page nouveau **raccourcis** .</span><span class="sxs-lookup"><span data-stu-id="9a472-139">Navigate to the new **Shortcuts** page.</span></span>  <span data-ttu-id="9a472-140">Sélectionnez **devtools (par défaut)** dans le menu déroulant **correspondant aux raccourcis de** la liste déroulante, puis sélectionnez **Visual Studio code**.</span><span class="sxs-lookup"><span data-stu-id="9a472-140">Select **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="9a472-141">Les raccourcis clavier dans le DevTools correspondent désormais aux raccourcis pour les actions équivalentes dans le code VS.</span><span class="sxs-lookup"><span data-stu-id="9a472-141">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in VS Code.</span></span>  

:::image type="complex" source="./media/experiments-keyboard-shortcut.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code VS" lightbox="./media/experiments-keyboard-shortcut.png":::
   <span data-ttu-id="9a472-143">Faire correspondre les raccourcis clavier du DevTools au code VS</span><span class="sxs-lookup"><span data-stu-id="9a472-143">Match keyboard shortcuts in the DevTools to VS Code</span></span>
:::image-end:::  

<span data-ttu-id="9a472-144">Par exemple, dans Windows, le raccourci clavier pour suspendre ou continuer à exécuter un script en [code vs][VisualstudioCodeShortcutsKeyboardWindows] est `F5` .</span><span class="sxs-lookup"><span data-stu-id="9a472-144">For example, on Windows the keyboard shortcut for pausing or continuing running a script in [VS Code][VisualstudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="9a472-145">Avec la valeur prédéfinie **devtools (par défaut)** , le même raccourci dans devtools est `F8` .</span><span class="sxs-lookup"><span data-stu-id="9a472-145">With the **DevTools (Default)** preset, the same shortcut in the DevTools is `F8`.</span></span>  <span data-ttu-id="9a472-146">Le raccourci est également associé au **code Visual Studio** prédéfini `F5` .</span><span class="sxs-lookup"><span data-stu-id="9a472-146">With the **Visual Studio Code** preset, the shortcut is also `F5`.</span></span>  

### <span data-ttu-id="9a472-147">Activer les nouvelles fonctionnalités de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="9a472-147">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="9a472-148">Permet d’améliorer les visualisations sur la page lorsque vous déboguez des sites Web dotés de dispositions CSS.</span><span class="sxs-lookup"><span data-stu-id="9a472-148">Improves on-page visualizations when you debug websites that have CSS grid layouts.</span></span>  <span data-ttu-id="9a472-149">Vous pouvez personnaliser davantage les superpositions dans les paramètres de DevTools.</span><span class="sxs-lookup"><span data-stu-id="9a472-149">You may further customize the overlays in DevTools Settings.</span></span>  

:::image type="complex" source="./media/experiments-grid.png" alt-text="Fonctionnalité de débogage de grille CSS" lightbox="./media/experiments-grid.png":::
   <span data-ttu-id="9a472-151">Fonctionnalité de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="9a472-151">CSS grid debugging feature</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="9a472-152">Activer la prise en charge du déplacement des onglets entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="9a472-152">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="9a472-153">En règle générale, il est possible d’ouvrir des outils tels que des **éléments** et un **réseau** uniquement dans le panneau principal \ (Top \) de devtools.</span><span class="sxs-lookup"><span data-stu-id="9a472-153">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="9a472-154">De même, il est possible d’ouvrir des outils tels que la vue et les **problèmes** en **3D** uniquement dans le panneau tiroir \ (en bas) de devtools.</span><span class="sxs-lookup"><span data-stu-id="9a472-154">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="9a472-155">Lorsque vous sélectionnez l’expérience, vous pouvez déplacer des outils entre les volets supérieur et inférieur en pointant sur l’onglet, en ouvrant le menu contextuel \ (clic droit sur \), puis en **haut** ou **en bas**.</span><span class="sxs-lookup"><span data-stu-id="9a472-155">When you choose the experiment, you may move tools between the top and bottom panels by hovering on the tab, opening the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="9a472-156">Cette expérience vous permet de personnaliser la disposition de votre DevTools.</span><span class="sxs-lookup"><span data-stu-id="9a472-156">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="9a472-157">Pour afficher ou masquer le panneau inférieur, sélectionnez `Escape` .</span><span class="sxs-lookup"><span data-stu-id="9a472-157">To show or hide the bottom panel, select `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Déplacement d’un onglet entre les panneaux" lightbox="./media/experiments-move-panels.png":::
   <span data-ttu-id="9a472-159">Déplacement d’un onglet entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="9a472-159">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="9a472-160">Activer webhint</span><span class="sxs-lookup"><span data-stu-id="9a472-160">Enable webhint</span></span>  

<span data-ttu-id="9a472-161">[webhint][WebhintMain] est un outil open source qui fournit des commentaires en temps réel sur l’accessibilité, la compatibilité entre les navigateurs, la sécurité, les performances, PWAS, ainsi que d’autres problèmes courants liés au développement Web sur les sites Web.</span><span class="sxs-lookup"><span data-stu-id="9a472-161">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="9a472-162">L’expérience [webhint][WebhintMain] a pour résultat le devtools de commentaires webhint dans le volet [problèmes][DevtoolsIssues] .</span><span class="sxs-lookup"><span data-stu-id="9a472-162">The [webhint][WebhintMain] experiment brings the webhint feedback into DevTools in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="9a472-163">Vous pouvez sélectionner le problème pour voir la documentation relative à la résolution du problème ainsi qu’une liste des ressources affectées sur votre site Web.</span><span class="sxs-lookup"><span data-stu-id="9a472-163">You may select the issue to see documentation on how to fix the issue and a list of the affected resources on your website.</span></span>  <span data-ttu-id="9a472-164">Sélectionnez un lien vers une ressource pour ouvrir le volet **réseau**, **sources**ou **éléments** approprié dans devtools.</span><span class="sxs-lookup"><span data-stu-id="9a472-164">Select a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="Commentaires de webhint dans le volet problèmes" lightbox="./media/experiments-webhint.png":::
   <span data-ttu-id="9a472-166">Commentaires de webhint dans le volet problèmes</span><span class="sxs-lookup"><span data-stu-id="9a472-166">webhint feedback in the Issues panel</span></span>  
:::image-end:::      

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="9a472-167">Activer la console réseau</span><span class="sxs-lookup"><span data-stu-id="9a472-167">Enable Network Console</span></span>

<span data-ttu-id="9a472-168">**Network console** est le titre d’une expérience visant à faire des requêtes réseau synthétiques sur http.</span><span class="sxs-lookup"><span data-stu-id="9a472-168">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="9a472-169">Vous pouvez utiliser l’expérience de la **console réseau** pour envoyer des demandes d’API Web.</span><span class="sxs-lookup"><span data-stu-id="9a472-169">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="9a472-170">Après avoir activé l’expérience, assurez-vous de redémarrer l’DevTools.</span><span class="sxs-lookup"><span data-stu-id="9a472-170">After enabling the experiment, ensure you restart the DevTools.</span></span> <span data-ttu-id="9a472-171">Pour utiliser la console réseau:</span><span class="sxs-lookup"><span data-stu-id="9a472-171">To use the Network Console:</span></span>
1.  <span data-ttu-id="9a472-172">Ouvrez le volet **réseau** .</span><span class="sxs-lookup"><span data-stu-id="9a472-172">Open the **Network** pane.</span></span>
1.  <span data-ttu-id="9a472-173">Recherchez la demande réseau que vous souhaitez modifier et renvoyer.</span><span class="sxs-lookup"><span data-stu-id="9a472-173">Find the network request that you want to change and resend.</span></span>
1.  <span data-ttu-id="9a472-174">Ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **modifier, puis relire**.</span><span class="sxs-lookup"><span data-stu-id="9a472-174">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span> 
1.  <span data-ttu-id="9a472-175">Lorsque la **console réseau** s’ouvre, modifiez les informations de requête réseau.</span><span class="sxs-lookup"><span data-stu-id="9a472-175">When the **Network Console** opens, edit the network request information.</span></span>
1.  <span data-ttu-id="9a472-176">Sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="9a472-176">Select **Send**.</span></span>  

:::image type="complex" source="./media/network-network-console.png" alt-text="Console réseau dans le tiroir de la console" lightbox="./media/network-network-console.png":::
<span data-ttu-id="9a472-178">Console réseau dans le tiroir de la console</span><span class="sxs-lookup"><span data-stu-id="9a472-178">Network Console in the Console drawer</span></span>
:::image-end::: 

<!--Available in Microsoft Edge version 85 and later.  --> 

## <span data-ttu-id="9a472-179">Fonctionnalités expérimentales antérieures</span><span class="sxs-lookup"><span data-stu-id="9a472-179">Previous experimental features</span></span>  

*   <span data-ttu-id="9a472-180">la [vue 3D][Devtools3dViewIndex] est désormais disponible et activée par défaut dans Microsoft Edge version 83 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9a472-180">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  

## <span data-ttu-id="9a472-181">Fourniture de commentaires sur les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="9a472-181">Providing feedback on experimental features</span></span>  

<span data-ttu-id="9a472-182">Pour transmettre des commentaires sur les expériences DevTools Microsoft Edge, ou tout autre élément associé à DevTools.</span><span class="sxs-lookup"><span data-stu-id="9a472-182">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="9a472-183">Envoyez vos commentaires à l’aide de l’icône de commentaires dans le DevTools</span><span class="sxs-lookup"><span data-stu-id="9a472-183">Send your feedback using the Feedback icon in the DevTools</span></span>  
*   <span data-ttu-id="9a472-184">Tweeter sur [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="9a472-184">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="./media/devtools-feedback.png" alt-text="Icône de commentaires dans le Microsoft Edge DevTools" lightbox="./media/devtools-feedback.png":::
   <span data-ttu-id="9a472-186">Icône de commentaires dans le Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9a472-186">Feedback icon in the Microsoft Edge DevTools</span></span>  
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
