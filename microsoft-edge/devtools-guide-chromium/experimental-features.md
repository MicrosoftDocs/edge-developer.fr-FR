---
description: Dernières fonctionnalités expérimentales de Microsoft Edge DevTools
title: Fonctionnalités expérimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, expérience
ms.openlocfilehash: 4c2541615700f2c637f293ee6a3fbacd9ccbc43a
ms.sourcegitcommit: 5ed791ed5423a3a4b03e8a1c7927f026307a6673
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/25/2020
ms.locfileid: "10960717"
---
# <span data-ttu-id="fadc9-104">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="fadc9-104">Experimental features</span></span>  

<span data-ttu-id="fadc9-105">Vous pouvez utiliser les fonctionnalités expérimentales qui sont toujours en cours de développement dans Microsoft Edge DevTools pour tester et [transmettre des commentaires](#providing-feedback-on-experimental-features) avant chaque sortie.</span><span class="sxs-lookup"><span data-stu-id="fadc9-105">You may use the experimental features that are still under development in the Microsoft Edge DevTools to test and [provide feedback](#providing-feedback-on-experimental-features) before each is released broadly.</span></span>  

<span data-ttu-id="fadc9-106">Si les fonctionnalités expérimentales sont disponibles dans tous les canaux de Microsoft Edge, vous pouvez obtenir les dernières fonctionnalités expérimentales à l’aide du canal des Canaries Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fadc9-106">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="fadc9-107">Activer les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="fadc9-107">Turn on experimental features</span></span>  

<span data-ttu-id="fadc9-108">Procédez comme suit pour activer ou désactiver les fonctionnalités expérimentales dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fadc9-108">Use the following steps to turn on \(or off\) experimental features in Microsoft Edge.</span></span>  

1.  <span data-ttu-id="fadc9-109">[Ouvrez devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="fadc9-109">[Open DevTools][DevtoolsOpen].</span></span>  
     *   <span data-ttu-id="fadc9-110">Sélectionnez `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="fadc9-110">Select `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="fadc9-111">Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="fadc9-111">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="fadc9-112">Ouvrez le volet [paramètres][DevToolsCustomizeSettings] .</span><span class="sxs-lookup"><span data-stu-id="fadc9-112">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="fadc9-113">Sélectionnez `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="fadc9-113">Select `Shift`+`?`.</span></span>  <span data-ttu-id="fadc9-114">Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="fadc9-114">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="fadc9-115">Sur le côté gauche du volet **paramètres** , sélectionnez la section **expériences** .</span><span class="sxs-lookup"><span data-stu-id="fadc9-115">On the left side of the **Settings** pane, select the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/experiments-devtools.png":::
       <span data-ttu-id="fadc9-117">Liste des expériences dans les paramètres de DevTools</span><span class="sxs-lookup"><span data-stu-id="fadc9-117">List of experiments in DevTools Settings</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fadc9-118">Sur la page **expériences** , faites défiler la liste de toutes les fonctionnalités expérimentales disponibles, puis cochez la case en regard de chaque fonctionnalité que vous voulez tester.</span><span class="sxs-lookup"><span data-stu-id="fadc9-118">On the **Experiments** page, scroll through the list of all available experimental features and select the checkbox next to each features that you want to test.</span></span>  
1.  <span data-ttu-id="fadc9-119">Fermez et rouvrez Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="fadc9-119">Close and reopen Microsoft Edge DevTools.</span></span>  

> [!NOTE]
> <span data-ttu-id="fadc9-120">Les fonctionnalités expérimentales sont constamment mises à jour et peuvent entraîner des problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="fadc9-120">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="fadc9-121">Pour désactiver une fonctionnalité expérimentale, ouvrez la page **expériences** , puis décochez la case de la fonctionnalité expérimental que vous souhaitez désactiver.</span><span class="sxs-lookup"><span data-stu-id="fadc9-121">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="fadc9-122">Fonctionnalités expérimentales mises en évidence</span><span class="sxs-lookup"><span data-stu-id="fadc9-122">Highlighted experimental features</span></span>  

<span data-ttu-id="fadc9-123">Les sections suivantes décrivent les nouvelles fonctionnalités expérimentales disponibles dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fadc9-123">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="fadc9-124">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="fadc9-124">Experimental feature</span></span> | <span data-ttu-id="fadc9-125">Version de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fadc9-125">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="fadc9-126">Activer l’onglet Paramètres de raccourcis clavier personnalisés</span><span class="sxs-lookup"><span data-stu-id="fadc9-126">Enable custom keyboard shortcuts settings tab</span></span>](#enable-custom-keyboard-shortcuts-settings-tab) | <span data-ttu-id="fadc9-127">84 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fadc9-127">84 or later</span></span> |
| [<span data-ttu-id="fadc9-128">Activer les nouvelles fonctionnalités de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="fadc9-128">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="fadc9-129">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fadc9-129">85 or later</span></span> |  
| [<span data-ttu-id="fadc9-130">Activer la prise en charge du déplacement des onglets entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="fadc9-130">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="fadc9-131">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fadc9-131">85 or later</span></span> |  
| [<span data-ttu-id="fadc9-132">Activer webhint</span><span class="sxs-lookup"><span data-stu-id="fadc9-132">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="fadc9-133">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fadc9-133">85 or later</span></span> |  
| [<span data-ttu-id="fadc9-134">Activer la console réseau</span><span class="sxs-lookup"><span data-stu-id="fadc9-134">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="fadc9-135">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fadc9-135">85 or later</span></span> |  
| [<span data-ttu-id="fadc9-136">Activer la visionneuse de commandes sources</span><span class="sxs-lookup"><span data-stu-id="fadc9-136">Enable Source Order Viewer</span></span>](#enable-source-order-viewer) | <span data-ttu-id="fadc9-137">86 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fadc9-137">86 or later</span></span> |  

### <span data-ttu-id="fadc9-138">Activer l’onglet Paramètres de raccourcis clavier personnalisés</span><span class="sxs-lookup"><span data-stu-id="fadc9-138">Enable custom keyboard shortcuts settings tab</span></span>  

<span data-ttu-id="fadc9-139">Propose une nouvelle page de **raccourcis** dans les [paramètres de devtools][DevToolsCustomizeSettings] qui permet d’associer des [raccourcis clavier][DevToolsShortcuts] dans devtools au [code Microsoft Visual Studio][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="fadc9-139">Provides a new **Shortcuts** page in [DevTools Settings][DevToolsCustomizeSettings] that enables matching [keyboard shortcuts][DevToolsShortcuts] in the DevTools to [Microsoft Visual Studio Code][VisualstudioCode].</span></span>  

<span data-ttu-id="fadc9-140">Une fois que vous avez activé l’expérience, rouvrez les [paramètres de devtools][DevToolsCustomizeSettings] à l’aide de la sélection `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="fadc9-140">Once you have enabled the experiment, open [DevTools Settings][DevToolsCustomizeSettings] again using select `Shift`+`?`.</span></span>  <span data-ttu-id="fadc9-141">Accédez à la page nouveau **raccourcis** .</span><span class="sxs-lookup"><span data-stu-id="fadc9-141">Navigate to the new **Shortcuts** page.</span></span>  <span data-ttu-id="fadc9-142">Sélectionnez **devtools (par défaut)** dans le menu déroulant **correspondant aux raccourcis de** la liste déroulante, puis sélectionnez **Visual Studio code**.</span><span class="sxs-lookup"><span data-stu-id="fadc9-142">Select **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="fadc9-143">Les raccourcis clavier dans le DevTools correspondent désormais aux raccourcis pour les actions équivalentes dans le code Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="fadc9-143">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in Visual Studio Code.</span></span>  

:::image type="complex" source="./media/experiments-keyboard-shortcut.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="./media/experiments-keyboard-shortcut.png":::
   <span data-ttu-id="fadc9-145">Faire correspondre les raccourcis clavier du DevTools au code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fadc9-145">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="fadc9-146">Par exemple, dans Windows, le raccourci clavier pour suspendre ou continuer à exécuter un script dans le [code Visual Studio][VisualstudioCodeShortcutsKeyboardWindows] est `F5` .</span><span class="sxs-lookup"><span data-stu-id="fadc9-146">For example, on Windows the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualstudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="fadc9-147">Avec la valeur prédéfinie **devtools (par défaut)** , le même raccourci dans devtools est `F8` .</span><span class="sxs-lookup"><span data-stu-id="fadc9-147">With the **DevTools (Default)** preset, the same shortcut in the DevTools is `F8`.</span></span>  <span data-ttu-id="fadc9-148">Le raccourci est également associé au **code Visual Studio** prédéfini `F5` .</span><span class="sxs-lookup"><span data-stu-id="fadc9-148">With the **Visual Studio Code** preset, the shortcut is also `F5`.</span></span>  

### <span data-ttu-id="fadc9-149">Activer les nouvelles fonctionnalités de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="fadc9-149">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="fadc9-150">Permet d’améliorer les visualisations sur la page lorsque vous déboguez des sites Web dotés de dispositions CSS.</span><span class="sxs-lookup"><span data-stu-id="fadc9-150">Improves on-page visualizations when you debug websites that have CSS grid layouts.</span></span>  <span data-ttu-id="fadc9-151">Vous pouvez personnaliser davantage les superpositions dans les paramètres de DevTools.</span><span class="sxs-lookup"><span data-stu-id="fadc9-151">You may further customize the overlays in DevTools Settings.</span></span>  

:::image type="complex" source="./media/experiments-grid.png" alt-text="Fonctionnalité de débogage de grille CSS" lightbox="./media/experiments-grid.png":::
   <span data-ttu-id="fadc9-153">Fonctionnalité de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="fadc9-153">CSS grid debugging feature</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="fadc9-154">Activer la prise en charge du déplacement des onglets entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="fadc9-154">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="fadc9-155">En règle générale, il est possible d’ouvrir des outils tels que des **éléments** et un **réseau** uniquement dans le panneau principal \ (Top \) de devtools.</span><span class="sxs-lookup"><span data-stu-id="fadc9-155">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="fadc9-156">De même, il est possible d’ouvrir des outils tels que la vue et les **problèmes** en **3D** uniquement dans le panneau tiroir \ (en bas) de devtools.</span><span class="sxs-lookup"><span data-stu-id="fadc9-156">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="fadc9-157">Lorsque vous sélectionnez l’expérience, vous pouvez déplacer des outils entre les volets supérieur et inférieur en pointant sur l’onglet, en ouvrant le menu contextuel \ (clic droit sur \), puis en **haut** ou **en bas**.</span><span class="sxs-lookup"><span data-stu-id="fadc9-157">When you choose the experiment, you may move tools between the top and bottom panels by hovering on the tab, opening the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="fadc9-158">Cette expérience vous permet de personnaliser la disposition de votre DevTools.</span><span class="sxs-lookup"><span data-stu-id="fadc9-158">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="fadc9-159">Pour afficher ou masquer le panneau inférieur, sélectionnez `Escape` .</span><span class="sxs-lookup"><span data-stu-id="fadc9-159">To show or hide the bottom panel, select `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Déplacement d’un onglet entre les panneaux" lightbox="./media/experiments-move-panels.png":::
   <span data-ttu-id="fadc9-161">Déplacement d’un onglet entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="fadc9-161">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="fadc9-162">Activer webhint</span><span class="sxs-lookup"><span data-stu-id="fadc9-162">Enable webhint</span></span>  

<span data-ttu-id="fadc9-163">[webhint][WebhintMain] est un outil open source qui fournit des commentaires en temps réel sur l’accessibilité, la compatibilité entre les navigateurs, la sécurité, les performances, PWAS, ainsi que d’autres problèmes courants liés au développement Web sur les sites Web.</span><span class="sxs-lookup"><span data-stu-id="fadc9-163">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="fadc9-164">L’expérience [webhint][WebhintMain] a pour résultat le devtools de commentaires webhint dans le volet [problèmes][DevtoolsIssues] .</span><span class="sxs-lookup"><span data-stu-id="fadc9-164">The [webhint][WebhintMain] experiment brings the webhint feedback into DevTools in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="fadc9-165">Vous pouvez sélectionner le problème pour voir la documentation relative à la résolution du problème ainsi qu’une liste des ressources affectées sur votre site Web.</span><span class="sxs-lookup"><span data-stu-id="fadc9-165">You may select the issue to see documentation on how to fix the issue and a list of the affected resources on your website.</span></span>  <span data-ttu-id="fadc9-166">Sélectionnez un lien vers une ressource pour ouvrir le volet **réseau**, **sources**ou **éléments** approprié dans devtools.</span><span class="sxs-lookup"><span data-stu-id="fadc9-166">Select a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="Commentaires de webhint dans le volet problèmes" lightbox="./media/experiments-webhint.png":::
   <span data-ttu-id="fadc9-168">Commentaires de webhint dans le volet **problèmes**</span><span class="sxs-lookup"><span data-stu-id="fadc9-168">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="fadc9-169">Activer la console réseau</span><span class="sxs-lookup"><span data-stu-id="fadc9-169">Enable Network Console</span></span>  

<span data-ttu-id="fadc9-170">**Network console** est le titre d’une expérience visant à faire des requêtes réseau synthétiques sur http.</span><span class="sxs-lookup"><span data-stu-id="fadc9-170">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="fadc9-171">Vous pouvez utiliser l’expérience de la **console réseau** pour envoyer des demandes d’API Web.</span><span class="sxs-lookup"><span data-stu-id="fadc9-171">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="fadc9-172">Après avoir activé l’expérience, assurez-vous de redémarrer l’DevTools.</span><span class="sxs-lookup"><span data-stu-id="fadc9-172">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="fadc9-173">Pour utiliser la console réseau:</span><span class="sxs-lookup"><span data-stu-id="fadc9-173">To use the Network Console:</span></span>  

1.  <span data-ttu-id="fadc9-174">Ouvrez le volet **réseau** .</span><span class="sxs-lookup"><span data-stu-id="fadc9-174">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="fadc9-175">Recherchez la demande réseau que vous souhaitez modifier et renvoyer.</span><span class="sxs-lookup"><span data-stu-id="fadc9-175">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="fadc9-176">Ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **modifier, puis relire**.</span><span class="sxs-lookup"><span data-stu-id="fadc9-176">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="fadc9-177">Lorsque la **console réseau** s’ouvre, modifiez les informations de requête réseau.</span><span class="sxs-lookup"><span data-stu-id="fadc9-177">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="fadc9-178">Sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="fadc9-178">Select **Send**.</span></span>  

:::image type="complex" source="./media/network-network-console.png" alt-text="Console réseau dans le tiroir de la console" lightbox="./media/network-network-console.png":::
   <span data-ttu-id="fadc9-180">**Console réseau** dans le tiroir de la **console**</span><span class="sxs-lookup"><span data-stu-id="fadc9-180">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  --> 

### <span data-ttu-id="fadc9-181">Activer la visionneuse de commandes sources</span><span class="sxs-lookup"><span data-stu-id="fadc9-181">Enable Source Order Viewer</span></span>  

<span data-ttu-id="fadc9-182">La **visionneuse de commandes source** est le titre d’une expérience permettant d’afficher l’ordre des éléments dans la source de la page.</span><span class="sxs-lookup"><span data-stu-id="fadc9-182">**Source Order Viewer** is the working title of an experiment to display the order of elements in the page source.</span></span>  <span data-ttu-id="fadc9-183">Vous pouvez utiliser l’expérience de la **visionneuse de commandes sources** pour détecter des problèmes d’accessibilité dans vos pages, car l’ordre de l’affichage à l’écran risque de différer de l’ordre de la source, ce qui déconcerte les utilisateurs de lecteurs d’écran.</span><span class="sxs-lookup"><span data-stu-id="fadc9-183">You may use the **Source Order Viewer** experiment to find accessibility issues in your pages since the display order on-screen may differ from the order of the source, which confuses screen reader users.</span></span>  

<span data-ttu-id="fadc9-184">Après avoir activé l’expérience, assurez-vous de redémarrer l’DevTools.</span><span class="sxs-lookup"><span data-stu-id="fadc9-184">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="fadc9-185">Pour utiliser la visionneuse de commandes source:</span><span class="sxs-lookup"><span data-stu-id="fadc9-185">To use Source Order Viewer:</span></span>  

1.  <span data-ttu-id="fadc9-186">Ouvrir le volet des **éléments** .</span><span class="sxs-lookup"><span data-stu-id="fadc9-186">Open the **Elements** pane.</span></span>  
1.  <span data-ttu-id="fadc9-187">Ouvrez le volet **accessibilité** dans le panneau du tiroir.</span><span class="sxs-lookup"><span data-stu-id="fadc9-187">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="fadc9-188">Dans la section **visionneuse de commandes sources** , activez la case à cocher **afficher l’ordre source** .</span><span class="sxs-lookup"><span data-stu-id="fadc9-188">Under the **Source Order Viewer** section, select the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="fadc9-189">Mettez en surbrillance un élément HTML pour afficher une superposition de l’ordre dans la source de la page.</span><span class="sxs-lookup"><span data-stu-id="fadc9-189">Highlight any HTML element to display an overlay that the order in the page source.</span></span>  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Visionneuse de commandes source dans le volet accessibilité" lightbox="./media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="fadc9-191">**Visionneuse de commandes source** dans le volet **accessibilité**</span><span class="sxs-lookup"><span data-stu-id="fadc9-191">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## <span data-ttu-id="fadc9-192">Fonctionnalités expérimentales antérieures</span><span class="sxs-lookup"><span data-stu-id="fadc9-192">Previous experimental features</span></span>  

*   <span data-ttu-id="fadc9-193">la [vue 3D][Devtools3dViewIndex] est désormais disponible et activée par défaut dans Microsoft Edge version 83 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fadc9-193">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  

## <span data-ttu-id="fadc9-194">Fourniture de commentaires sur les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="fadc9-194">Providing feedback on experimental features</span></span>  

<span data-ttu-id="fadc9-195">Pour transmettre des commentaires sur les expériences DevTools Microsoft Edge, ou tout autre élément associé à DevTools.</span><span class="sxs-lookup"><span data-stu-id="fadc9-195">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="fadc9-196">Envoyez vos commentaires à l’aide de l’icône **Envoyer des commentaires** dans le devtools</span><span class="sxs-lookup"><span data-stu-id="fadc9-196">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="fadc9-197">Tweeter sur [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="fadc9-197">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="./media/devtools-feedback.png" alt-text="Icône Envoyer des commentaires dans le Microsoft Edge DevTools" lightbox="./media/devtools-feedback.png":::
   <span data-ttu-id="fadc9-199">Icône **Envoyer des commentaires** dans le Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="fadc9-199">**Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Affichage 3D | Documents Microsoft"  
[DevtoolsIssues]: ./issues/index.md "Recherchez et corrigez les problèmes liés à l’outil problèmes dans Microsoft Edge DevTools Documents Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Raccourcis clavier dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsOpen]: ./open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[VisualstudioCode]: https://code.visualstudio.com "Code Microsoft Visual Studio"  
[VisualstudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Raccourcis clavier dans Visual Studio pour Windows | Code Microsoft Visual Studio"  

[WebhintMain]: https://webhint.io "Astuce" 
