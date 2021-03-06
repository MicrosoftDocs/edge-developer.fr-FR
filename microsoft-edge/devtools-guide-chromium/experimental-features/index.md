---
description: Dernières fonctionnalités expérimentales de Microsoft Edge DevTools
title: Fonctionnalités expérimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools, expérimentation
ms.openlocfilehash: b366cfeccafe874bc9e76d3b66659122c5d07c69
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398678"
---
# <a name="experimental-features"></a><span data-ttu-id="bc40a-104">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="bc40a-104">Experimental features</span></span>  

<span data-ttu-id="bc40a-105">Microsoft Edge DevTools permet d’accéder aux fonctionnalités expérimentales qui sont encore en développement.</span><span class="sxs-lookup"><span data-stu-id="bc40a-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="bc40a-106">Vous pouvez tester et [fournir des commentaires](#providing-feedback-on-experimental-features) avant la publication de chaque fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="bc40a-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="bc40a-107">Bien que les fonctionnalités expérimentales soient disponibles dans tous les canaux de Microsoft Edge, vous pouvez obtenir les dernières fonctionnalités expérimentales à l’aide du canal Canary de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bc40a-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="bc40a-108">Activer les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="bc40a-108">Turn on experimental features</span></span>  

<span data-ttu-id="bc40a-109">Pour activer \(ou désactiver\) les fonctionnalités expérimentales dans Microsoft Edge, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bc40a-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="bc40a-110">[Ouvrez DevTools][DevtoolsOpenMain].</span><span class="sxs-lookup"><span data-stu-id="bc40a-110">[Open DevTools][DevtoolsOpenMain].</span></span>  
    *   <span data-ttu-id="bc40a-111">Sélectionnez `Control` + `Shift` + `I` \(Windows, Linux\) ou `Command` + `Option` + `I` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="bc40a-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="bc40a-112">Pour plus d’informations, accédez aux raccourcis clavier de [Microsoft Edge DevTools.][DevToolsShortcuts]</span><span class="sxs-lookup"><span data-stu-id="bc40a-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="bc40a-113">Ouvrez [le volet Paramètres.][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="bc40a-113">Open the [Settings][DevToolsCustomizeIndexSettings] pane.</span></span>  
    *   <span data-ttu-id="bc40a-114">Sélectionnez `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="bc40a-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="bc40a-115">Pour plus d’informations, accédez aux raccourcis clavier de [Microsoft Edge DevTools.][DevToolsShortcuts]</span><span class="sxs-lookup"><span data-stu-id="bc40a-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="bc40a-116">Sur le côté gauche du volet **Paramètres,** choisissez la section **Expériences.**</span><span class="sxs-lookup"><span data-stu-id="bc40a-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Page Expériences dans Paramètres" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="bc40a-118">Page **Expériences** dans **Paramètres**</span><span class="sxs-lookup"><span data-stu-id="bc40a-118">The **Experiments** page in **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bc40a-119">Dans la page **Expériences,** parcourez la liste de toutes les fonctionnalités expérimentales disponibles et cochez la case en regard de chaque fonctionnalité à tester.</span><span class="sxs-lookup"><span data-stu-id="bc40a-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="bc40a-120">Fermez et rouvrez Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="bc40a-121">Les fonctionnalités expérimentales sont constamment mises à jour et peuvent entraîner des problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="bc40a-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="bc40a-122">Pour désactiver une fonctionnalité expérimentale, ouvrez la page **Expériences** et cochez la case de la fonctionnalité expérimentale que vous souhaitez désactiver.</span><span class="sxs-lookup"><span data-stu-id="bc40a-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <a name="highlighted-experimental-features"></a><span data-ttu-id="bc40a-123">Fonctionnalités expérimentales mises en évidence</span><span class="sxs-lookup"><span data-stu-id="bc40a-123">Highlighted experimental features</span></span>  

<span data-ttu-id="bc40a-124">Les sections suivantes décrivent les nouvelles fonctionnalités expérimentales disponibles dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bc40a-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="bc40a-125">Fonctionnalité expérimentale</span><span class="sxs-lookup"><span data-stu-id="bc40a-125">Experimental feature</span></span> | <span data-ttu-id="bc40a-126">Version de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bc40a-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="bc40a-127">Activer webhint</span><span class="sxs-lookup"><span data-stu-id="bc40a-127">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="bc40a-128">85 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bc40a-128">85 or later</span></span> |  
| [<span data-ttu-id="bc40a-129">Activer la console réseau</span><span class="sxs-lookup"><span data-stu-id="bc40a-129">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="bc40a-130">85 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bc40a-130">85 or later</span></span> |  
| [<span data-ttu-id="bc40a-131">Visionneuse de commandes source</span><span class="sxs-lookup"><span data-stu-id="bc40a-131">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="bc40a-132">86 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bc40a-132">86 or later</span></span> |  
| [<span data-ttu-id="bc40a-133">Activer l’éditeur de raccourci clavier</span><span class="sxs-lookup"><span data-stu-id="bc40a-133">Enable keyboard shortcut editor</span></span>](#enable-keyboard-shortcut-editor) | <span data-ttu-id="bc40a-134">87 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bc40a-134">87 or later</span></span> |  
| [<span data-ttu-id="bc40a-135">Activer les couches composites en vue 3D</span><span class="sxs-lookup"><span data-stu-id="bc40a-135">Enable Composited Layers in 3D View</span></span>](#enable-composited-layers-in-3d-view) | <span data-ttu-id="bc40a-136">87 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bc40a-136">87 or later</span></span> |  
| [<span data-ttu-id="bc40a-137">Activer le nouvel outil Éditeur de polices dans le volet Styles</span><span class="sxs-lookup"><span data-stu-id="bc40a-137">Enable new Font Editor tool within the Styles pane</span></span>](#enable-new-font-editor-tool-within-the-styles-pane) | <span data-ttu-id="bc40a-138">89 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bc40a-138">89 or later</span></span> |  
| [<span data-ttu-id="bc40a-139">Activer les nouvelles fonctionnalités de débogage Flexbox CSS</span><span class="sxs-lookup"><span data-stu-id="bc40a-139">Enable new CSS Flexbox debugging features</span></span>](#enable-new-css-flexbox-debugging-features) | <span data-ttu-id="bc40a-140">89 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bc40a-140">89 or later</span></span> |  
| [<span data-ttu-id="bc40a-141">Activer les menus + onglet de bouton pour ouvrir d’autres outils</span><span class="sxs-lookup"><span data-stu-id="bc40a-141">Enable + button tab menus to open more tools</span></span>](#enable--button-tab-menus-to-open-more-tools) | <span data-ttu-id="bc40a-142">89 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bc40a-142">89 or later</span></span> |  
| [<span data-ttu-id="bc40a-143">Activer l’onglet Bienvenue</span><span class="sxs-lookup"><span data-stu-id="bc40a-143">Enable Welcome tab</span></span>](#enable-welcome-tool) | <span data-ttu-id="bc40a-144">89 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="bc40a-144">89 or later</span></span> |  

### <a name="enable-new-css-grid-debugging-features"></a><span data-ttu-id="bc40a-145">Activer les nouvelles fonctionnalités de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="bc40a-145">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="bc40a-146">Cette fonctionnalité expérimentale fournit un certain nombre de nouvelles visualisations pour vous aider à déboguer les dispositions de grille CSS.</span><span class="sxs-lookup"><span data-stu-id="bc40a-146">This experimental feature provides a number of new visualizations to help you debug CSS grid layouts.</span></span>  <span data-ttu-id="bc40a-147">Pour afficher un aperçu des dernières fonctionnalités expérimentales, [activez cette expérience](#turn-on-experimental-features) et rechargez DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-147">To preview the latest experimental features, [enable this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  <span data-ttu-id="bc40a-148">Cette expérience est en cours par défaut dans Microsoft Edge version 87 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bc40a-148">This experiment is on by default in Microsoft Edge version 87 or later.</span></span>  

#### <a name="viewing-on-hover-grid-overlays-with-the-inspect-tool"></a><span data-ttu-id="bc40a-149">Affichage des superpositions de grille sur pointage à l’aide de l’outil Inspect</span><span class="sxs-lookup"><span data-stu-id="bc40a-149">Viewing on-hover grid overlays with the Inspect tool</span></span>  

<span data-ttu-id="bc40a-150">**L’outil Inspect** permet d’identifier et de visualiser rapidement les dispositions de grille CSS dans un site web en pointant dessus avec la souris.</span><span class="sxs-lookup"><span data-stu-id="bc40a-150">The **Inspect** tool provides a quick way to identify and visualize CSS Grid layouts in a website by hovering over them with the mouse.</span></span>  <span data-ttu-id="bc40a-151">Choisissez **l’icône Inspect** \( Inspect \) dans le coin supérieur gauche ![ de ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-151">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="bc40a-152">Ensuite, pointez sur `Grid` un élément de la page web que vous déboguer.</span><span class="sxs-lookup"><span data-stu-id="bc40a-152">Then, hover on a `Grid` element on the webpage you are debugging.</span></span>  <span data-ttu-id="bc40a-153">Les contours sont affichés autour de la grille, et l’inglage indique l’emplacement des espaces vides de la grille s’il est présent.</span><span class="sxs-lookup"><span data-stu-id="bc40a-153">Outlines are displayed around the grid, and hatching indicates the location of grid gaps if present.</span></span>  

:::image type="complex" source="../media/grid-inspect.msft.png" alt-text="Affichage des grilles à l’aide de l’outil Inspect" lightbox="../media/grid-inspect.msft.png":::
   <span data-ttu-id="bc40a-155">Affichage des grilles à l’aide de **l’outil Inspect**</span><span class="sxs-lookup"><span data-stu-id="bc40a-155">Viewing grids with the **Inspect** tool</span></span>  
:::image-end:::  

#### <a name="viewing-persistent-grid-overlays"></a><span data-ttu-id="bc40a-156">Affichage des superpositions de grilles persistantes</span><span class="sxs-lookup"><span data-stu-id="bc40a-156">Viewing persistent grid overlays</span></span>  

<span data-ttu-id="bc40a-157">Dans Microsoft Edge version 86 ou ultérieure, la fonctionnalité de grille CSS expérimentale offre également la possibilité d’activer les superpositions de grille persistantes.</span><span class="sxs-lookup"><span data-stu-id="bc40a-157">In Microsoft Edge version 86 or later, the experimental CSS grid feature also offers the option to enable persistent Grid overlays.</span></span>  <span data-ttu-id="bc40a-158">Les superpositions persistantes offrent plusieurs avantages.</span><span class="sxs-lookup"><span data-stu-id="bc40a-158">The persistent overlays provide several benefits.</span></span>  

*   <span data-ttu-id="bc40a-159">Les superpositions persistantes restent visibles sur la page lorsque vous faites défiler, déplacez votre souris et utilisez d’autres fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-159">The persistent overlays remain visible on the page as you scroll, move your mouse, and use other features of the DevTools.</span></span>  
*   <span data-ttu-id="bc40a-160">Plusieurs superpositions persistantes peuvent être allumées en même temps, ce qui vous permet de passer en revue plusieurs dispositions de grille à la fois.</span><span class="sxs-lookup"><span data-stu-id="bc40a-160">Multiple persistent overlays may be turned on at the same time, allowing you to review several grid layouts at once.</span></span>  
*   <span data-ttu-id="bc40a-161">Les superpositions persistantes offrent de nombreuses options de configuration, telles que le masquage ou l’affichage de noms dans la zone de grille, les intervalles de grille, les tailles de suivi, etc.</span><span class="sxs-lookup"><span data-stu-id="bc40a-161">Persistent overlays offer many configuration options, such as hiding or showing names in the grid area, grid gaps, track sizes, and so on.</span></span>  
    
<span data-ttu-id="bc40a-162">Les deux façons de faire basculer une superposition de grille persistante.</span><span class="sxs-lookup"><span data-stu-id="bc40a-162">The two ways to toggle a persistent grid overlay.</span></span>  

*   <span data-ttu-id="bc40a-163">Choisissez **l’icône ovale Grid** en face de tout élément Grid affiché dans l’arborescence DOM de **l’outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="bc40a-163">Choose the **Grid** oval icon next to any Grid element shown in the DOM tree of the **Elements** tool.</span></span>  
    
    :::image type="complex" source="../media/grid-adorner.msft.png" alt-text="Icône Ovale de grille dans l’outil Éléments" lightbox="../media/grid-adorner.msft.png":::
       <span data-ttu-id="bc40a-165">Icône Ovale de grille dans **l’outil Éléments**</span><span class="sxs-lookup"><span data-stu-id="bc40a-165">Grid oval icon in **Elements** tool</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="bc40a-166">Ouvrez le nouveau **panneau de** disposition situé dans l’outil Éléments, puis cochez la case en regard de chaque élément Grid que vous souhaitez mettre en surbrillez.</span><span class="sxs-lookup"><span data-stu-id="bc40a-166">Open the new **Layout** panel located in the Elements tool, and choose the checkbox next to each Grid element you want to highlight.</span></span>  
    
    :::image type="complex" source="../media/grid-layout-zoom.msft.png" alt-text="Panneau de disposition dans DevTools" lightbox="../media/grid-layout-zoom.msft.png":::
       <span data-ttu-id="bc40a-168">**Panneau** de disposition dans DevTools</span><span class="sxs-lookup"><span data-stu-id="bc40a-168">**Layout** panel in DevTools</span></span>  
    :::image-end:::  
    
#### <a name="configuring-persistent-overlays"></a><span data-ttu-id="bc40a-169">Configuration des superpositions persistantes</span><span class="sxs-lookup"><span data-stu-id="bc40a-169">Configuring persistent overlays</span></span>  

<span data-ttu-id="bc40a-170">Dans Microsoft Edge version 86 \*\*\*\* ou ultérieure, le nouveau panneau de disposition se trouve dans l’outil **Éléments** avec les panneaux **Styles** **et** Calculés.</span><span class="sxs-lookup"><span data-stu-id="bc40a-170">In Microsoft Edge version 86 or later, the new **Layout** panel is located in the **Elements** tool alongside the **Styles** and **Computed** panels.</span></span>  <span data-ttu-id="bc40a-171">Le **panneau de** disposition offre des options de configuration pour les superpositions persistantes.</span><span class="sxs-lookup"><span data-stu-id="bc40a-171">The **Layout** panel surfaces configuration options for persistent overlays.</span></span>  

:::image type="complex" source="../media/experiments-grid.msft.png" alt-text="Fonctionnalité de débogage de grille CSS" lightbox="../media/experiments-grid.msft.png":::
   <span data-ttu-id="bc40a-173">Fonctionnalité de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="bc40a-173">CSS grid debugging feature</span></span>  
:::image-end:::  

### <a name="enable-support-to-move-tabs-between-panels"></a><span data-ttu-id="bc40a-174">Activer la prise en charge du déplacement des onglets entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="bc40a-174">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="bc40a-175">Normalement, les outils \*\*\*\* tels que **Éléments** et Réseau ne peuvent s’ouvrir que dans le panneau principal situé en haut de DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-175">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="bc40a-176">Des **outils** **tels que l’affichage 3D** et les problèmes qui s’ouvrent normalement uniquement dans le panneau de caisse situé en bas de DevTools. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="bc40a-176">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="bc40a-177">Après avoir choisi l’expérience, vous pouvez déplacer les outils entre les panneaux supérieur et inférieur.</span><span class="sxs-lookup"><span data-stu-id="bc40a-177">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="bc40a-178">Pour déplacer un outil, pointez sur l’onglet, ouvrez le \*\*\*\* menu contextuel \(clic droit\), puis choisissez Déplacer vers le haut ou Vers **le bas.**</span><span class="sxs-lookup"><span data-stu-id="bc40a-178">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="bc40a-179">Cette expérience vous permet de personnaliser votre disposition DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-179">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="bc40a-180">Pour afficher ou masquer le **panneau de caisse,** sélectionnez `Escape` .</span><span class="sxs-lookup"><span data-stu-id="bc40a-180">To display or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Déplacement d’outils entre des panneaux" lightbox="../media/experiments-move-panels.msft.png":::
   <span data-ttu-id="bc40a-182">Déplacement d’outils entre des panneaux</span><span class="sxs-lookup"><span data-stu-id="bc40a-182">Moving tools between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-webhint"></a><span data-ttu-id="bc40a-183">Activer webhint</span><span class="sxs-lookup"><span data-stu-id="bc40a-183">Enable webhint</span></span>  

<span data-ttu-id="bc40a-184">[webhint est][WebhintMain] un outil open source qui fournit des commentaires en temps réel pour les sites web et les pages web locales.</span><span class="sxs-lookup"><span data-stu-id="bc40a-184">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="bc40a-185">Type de commentaires fourni par [webhint][WebhintMain].</span><span class="sxs-lookup"><span data-stu-id="bc40a-185">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="bc40a-186">accessibilité</span><span class="sxs-lookup"><span data-stu-id="bc40a-186">accessibility</span></span>  
*   <span data-ttu-id="bc40a-187">compatibilité entre navigateurs</span><span class="sxs-lookup"><span data-stu-id="bc40a-187">cross-browser compatibility</span></span>  
*   <span data-ttu-id="bc40a-188">sécurité</span><span class="sxs-lookup"><span data-stu-id="bc40a-188">security</span></span>  
*   <span data-ttu-id="bc40a-189">performance</span><span class="sxs-lookup"><span data-stu-id="bc40a-189">performance</span></span>  
*   <span data-ttu-id="bc40a-190">Applications web progressives (P.A.S.)</span><span class="sxs-lookup"><span data-stu-id="bc40a-190">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="bc40a-191">autres problèmes courants de développement web</span><span class="sxs-lookup"><span data-stu-id="bc40a-191">other common web development issues</span></span>  
    
<span data-ttu-id="bc40a-192">[L’expérience webhint][WebhintMain] affiche les commentaires sur le web dans le [panneau Problèmes.][DevtoolsIssues]</span><span class="sxs-lookup"><span data-stu-id="bc40a-192">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="bc40a-193">Choisissez un problème pour afficher la documentation de la solution et une liste des ressources affectées sur votre site web.</span><span class="sxs-lookup"><span data-stu-id="bc40a-193">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="bc40a-194">Choisissez un lien de ressource pour ouvrir \*\*\*\* le volet **Réseau,** **Sources**ou Éléments approprié dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-194">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="commentaires webhint dans le panneau Problèmes" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="bc40a-196">commentaires webhint dans le **panneau Problèmes**</span><span class="sxs-lookup"><span data-stu-id="bc40a-196">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-network-console"></a><span data-ttu-id="bc40a-197">Activer la console réseau</span><span class="sxs-lookup"><span data-stu-id="bc40a-197">Enable Network Console</span></span>  

<span data-ttu-id="bc40a-198">**Network Console est** le titre de travail d’une expérience pour effectuer des demandes de réseau synthétiques sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="bc40a-198">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="bc40a-199">Vous pouvez utiliser l’expérience **console** réseau pour envoyer des demandes d’API web.</span><span class="sxs-lookup"><span data-stu-id="bc40a-199">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="bc40a-200">Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-200">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="bc40a-201">Pour utiliser la **console réseau,** complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bc40a-201">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="bc40a-202">Ouvrez **le volet** Réseau.</span><span class="sxs-lookup"><span data-stu-id="bc40a-202">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="bc40a-203">Recherchez la demande réseau que vous souhaitez modifier et renvoyer.</span><span class="sxs-lookup"><span data-stu-id="bc40a-203">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="bc40a-204">Ouvrez le menu contextuel \(clic droit\), puis choisissez **Modifier et relire.**</span><span class="sxs-lookup"><span data-stu-id="bc40a-204">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="bc40a-205">Lorsque la **console réseau s’ouvre,** modifiez les informations de demande réseau.</span><span class="sxs-lookup"><span data-stu-id="bc40a-205">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="bc40a-206">Choose **Send**.</span><span class="sxs-lookup"><span data-stu-id="bc40a-206">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Console réseau dans le caisse de la console" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="bc40a-208">**Console réseau dans** le caisse **de la** console</span><span class="sxs-lookup"><span data-stu-id="bc40a-208">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="source-order-viewer"></a><span data-ttu-id="bc40a-209">Visionneuse de commandes source</span><span class="sxs-lookup"><span data-stu-id="bc40a-209">Source Order Viewer</span></span>  

<span data-ttu-id="bc40a-210">**L’Afficheur des** commandes source est une expérience qui affiche l’ordre des éléments dans la source de la page web.</span><span class="sxs-lookup"><span data-stu-id="bc40a-210">**Source Order Viewer** is an experiment that displays the order of elements in the webpage source.</span></span>  <span data-ttu-id="bc40a-211">L’ordre d’affichage à l’écran peut différer de l’ordre de la source, ce qui peut dérouter les utilisateurs du lecteur d’écran et du clavier.</span><span class="sxs-lookup"><span data-stu-id="bc40a-211">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="bc40a-212">Utilisez **l’expérience de l’Afficheur** des commandes source pour rechercher les différences entre l’ordre d’affichage à l’écran et l’ordre de la source.</span><span class="sxs-lookup"><span data-stu-id="bc40a-212">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="bc40a-213">Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-213">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="bc40a-214">Pour utiliser **l’Observateur de commandes source,** complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bc40a-214">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="bc40a-215">Ouvrez **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="bc40a-215">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="bc40a-216">Ouvrez **le volet Accessibilité** dans le panneau de caisse \(bas\).</span><span class="sxs-lookup"><span data-stu-id="bc40a-216">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="bc40a-217">Sous la section **Visionneuse de commandes** source, cochez la case Afficher la **commande source.**</span><span class="sxs-lookup"><span data-stu-id="bc40a-217">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="bc40a-218">Mettez en surbrillez n’importe quel élément HTML pour afficher une superposition que l’ordre dans la source de la page web.</span><span class="sxs-lookup"><span data-stu-id="bc40a-218">Highlight any HTML element to display an overlay that the order in the webpage source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Visionneuse de commandes source dans le volet Accessibilité" lightbox="../media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="bc40a-220">**Visionneuse de commandes source** dans **le volet** Accessibilité</span><span class="sxs-lookup"><span data-stu-id="bc40a-220">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <a name="enable-keyboard-shortcut-editor"></a><span data-ttu-id="bc40a-221">Activer l’éditeur de raccourci clavier</span><span class="sxs-lookup"><span data-stu-id="bc40a-221">Enable keyboard shortcut editor</span></span>

<span data-ttu-id="bc40a-222">Une fois **l’expérience** d’éditeur de raccourci clavier activée, vous pouvez personnaliser les raccourcis clavier pour toute action dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-222">With the **Enable keyboard shortcut editor** experiment turned on, you may customize keyboard shortcuts for any action in the DevTools.</span></span>  <span data-ttu-id="bc40a-223">Pour personnaliser le raccourci clavier pour une action spécifique, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bc40a-223">To customize the keyboard shortcut for a specific action, complete the following steps.</span></span>  

1.  <span data-ttu-id="bc40a-224">[Ouvrez DevTools][DevtoolsOpenMain].</span><span class="sxs-lookup"><span data-stu-id="bc40a-224">[Open DevTools][DevtoolsOpenMain].</span></span>  
1.  <span data-ttu-id="bc40a-225">Ouvrez [Paramètres.][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="bc40a-225">Open [Settings][DevToolsCustomizeIndexSettings].</span></span>  
    *   <span data-ttu-id="bc40a-226">Sélectionnez `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="bc40a-226">Select `Shift`+`?`.</span></span>  
1.  <span data-ttu-id="bc40a-227">Accédez à la page **Raccourcis.**</span><span class="sxs-lookup"><span data-stu-id="bc40a-227">Navigate to the **Shortcuts** page.</span></span>  
1.  <span data-ttu-id="bc40a-228">Choisissez l’action que vous souhaitez personnaliser.</span><span class="sxs-lookup"><span data-stu-id="bc40a-228">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="bc40a-229">Sélectionnez **l’icône** Modifier \( ![ EditKeyboardShortcut ](../media/edit-keyboard-shortcut-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="bc40a-229">Choose the **Edit** \(![EditKeyboardShortcut](../media/edit-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Choisir l’action à personnaliser à partir de la page Raccourcis dans Paramètres" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       <span data-ttu-id="bc40a-231">Choisir l’action à personnaliser à partir de la page **Raccourcis** dans [Paramètres][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="bc40a-231">Choose the action to customize from the **Shortcuts** page in [Settings][DevToolsCustomizeIndexSettings]</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bc40a-232">Sur le clavier, sélectionnez les touches à lier à l’action.</span><span class="sxs-lookup"><span data-stu-id="bc40a-232">On the keyboard, select the keys to bind to the action.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Choisissez les clés que vous souhaitez affecter à l’action" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="bc40a-234">Choisissez les clés que vous souhaitez affecter à l’action</span><span class="sxs-lookup"><span data-stu-id="bc40a-234">Choose the keys you want to assign to the action</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bc40a-235">Pour enregistrer votre nouveau raccourci clavier, sélectionnez la coche \(</span><span class="sxs-lookup"><span data-stu-id="bc40a-235">To save your new keyboard shortcut, choose the checkmark \(</span></span>![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)<span data-ttu-id="bc40a-237">\) icône.</span><span class="sxs-lookup"><span data-stu-id="bc40a-237">\) icon.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Sélectionnez l’icône de coche pour enregistrer votre nouveau raccourci clavier" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="bc40a-239">Sélectionnez l’icône de coche pour enregistrer votre nouveau raccourci clavier</span><span class="sxs-lookup"><span data-stu-id="bc40a-239">Choose the checkmark icon to save your new keyboard shortcut</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bc40a-240">Sélectionnez votre nouveau raccourci clavier pour déclencher l’action dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-240">Select your new keyboard shortcut to trigger the action in the DevTools.</span></span>  
    
<span data-ttu-id="bc40a-241">Dans la page **Raccourcis,** l’icône Raccourci clavier personnalisé **\(** ![ CustomKeyboardShortcut \) affiche les raccourcis clavier que vous ](../media/custom-keyboard-shortcut-icon.msft.png) avez personnalisés.</span><span class="sxs-lookup"><span data-stu-id="bc40a-241">On the **Shortcuts** page, the **Custom Keyboard Shortcut** \(![CustomKeyboardShortcut](../media/custom-keyboard-shortcut-icon.msft.png)\) icon displays keyboard shortcuts you customized.</span></span>  <span data-ttu-id="bc40a-242">Pour réinitialiser tous les raccourcis, **sélectionnez Restaurer les raccourcis par défaut.**</span><span class="sxs-lookup"><span data-stu-id="bc40a-242">To reset all shortcuts, choose **Restore default shortcuts**.</span></span>  

<span data-ttu-id="bc40a-243">Pour ignorer vos modifications pendant que vous modifiez les raccourcis clavier d’une action, choisissez l’icône X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="bc40a-243">To discard your changes while you edit the keyboard shortcuts for an action, choose the X \(![XKeyboardShortcut](../media/discard-changes-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="bc40a-244">Pour supprimer les raccourcis d’une action spécifique, sélectionnez l’icône Supprimer le **raccourci** \( ![ DeleteKeyboardShortcut ](../media/delete-keyboard-shortcut-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="bc40a-244">To remove shortcuts for a specific action, choose the **Delete shortcut** \(![DeleteKeyboardShortcut](../media/delete-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="bc40a-245">Pour ajouter plusieurs raccourcis pour une action, choisissez **Ajouter un raccourci.**</span><span class="sxs-lookup"><span data-stu-id="bc40a-245">To add multiple shortcuts for an action, choose **Add a shortcut**.</span></span>  

> [!NOTE]
> <span data-ttu-id="bc40a-246">Si un raccourci clavier est actuellement affecté à une autre action, il se peut que vous ne l’enregistrez pas pour une nouvelle action.</span><span class="sxs-lookup"><span data-stu-id="bc40a-246">If a keyboard shortcut is currently assigned to another action, you may not save it for a new action.</span></span>  <span data-ttu-id="bc40a-247">Vous devez d’abord supprimer le raccourci clavier de l’action précédente, puis l’ajouter à la nouvelle action.</span><span class="sxs-lookup"><span data-stu-id="bc40a-247">You must first delete the keyboard shortcut for the previous action and then add it to the new action.</span></span>  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-composited-layers-in-3d-view"></a><span data-ttu-id="bc40a-248">Activer les couches composites en vue 3D</span><span class="sxs-lookup"><span data-stu-id="bc40a-248">Enable Composited Layers in 3D View</span></span>  

<span data-ttu-id="bc40a-249">Vous pouvez maintenant visualiser calques avec les index z et le modèle objet de document \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="bc40a-249">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="bc40a-250">Cette fonctionnalité vous permet de déboguer sans changer de contexte aussi souvent.</span><span class="sxs-lookup"><span data-stu-id="bc40a-250">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="bc40a-251">Vous avez identifié que la réduction du basculement de contexte était un problème majeur.</span><span class="sxs-lookup"><span data-stu-id="bc40a-251">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="bc40a-252">Il n’est pas toujours clair comment le code que vous écrivez affecte votre application web.</span><span class="sxs-lookup"><span data-stu-id="bc40a-252">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="bc40a-253">Pour une expérience complète de débogage, l’affichage 3D et les couches composites sont désormais combinés.</span><span class="sxs-lookup"><span data-stu-id="bc40a-253">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  

<span data-ttu-id="bc40a-254">Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-254">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="bc40a-255">Pour utiliser **les couches composites,** complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bc40a-255">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="bc40a-256">Dans le caisse, choisissez **l’outil d’affichage 3D.**</span><span class="sxs-lookup"><span data-stu-id="bc40a-256">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="bc40a-257">Ouvrez **le volet Calques composites.**</span><span class="sxs-lookup"><span data-stu-id="bc40a-257">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="bc40a-258">Toutes les couches peints de l’application sont affichées.</span><span class="sxs-lookup"><span data-stu-id="bc40a-258">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="bc40a-259">Essayez cette fonctionnalité avec vos propres applications web.</span><span class="sxs-lookup"><span data-stu-id="bc40a-259">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Volet des couches composites" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="bc40a-261">Volet des **couches composites**</span><span class="sxs-lookup"><span data-stu-id="bc40a-261">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-new-font-editor-tool-within-the-styles-pane"></a><span data-ttu-id="bc40a-262">Activer le nouvel outil Éditeur de polices dans le volet Styles</span><span class="sxs-lookup"><span data-stu-id="bc40a-262">Enable new Font Editor tool within the Styles pane</span></span>  

<span data-ttu-id="bc40a-263">Vous pouvez désormais utiliser le nouvel éditeur de [polices][DevtoolsInspectStylesEditFonts] visuel pour modifier les polices.</span><span class="sxs-lookup"><span data-stu-id="bc40a-263">You may now use the new visual [Font Editor][DevtoolsInspectStylesEditFonts] to edit fonts.</span></span>  <span data-ttu-id="bc40a-264">Utilisez-la pour définir les polices et les caractéristiques de police.</span><span class="sxs-lookup"><span data-stu-id="bc40a-264">Use it define fonts and font characteristics.</span></span>  <span data-ttu-id="bc40a-265">Visual **Font Editor vous** aide à effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="bc40a-265">The visual **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="bc40a-266">Basculer entre les unités pour différentes propriétés de police</span><span class="sxs-lookup"><span data-stu-id="bc40a-266">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="bc40a-267">Basculer entre les mots clés pour différentes propriétés de police</span><span class="sxs-lookup"><span data-stu-id="bc40a-267">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="bc40a-268">Convertir des unités</span><span class="sxs-lookup"><span data-stu-id="bc40a-268">Convert units</span></span>  
*   <span data-ttu-id="bc40a-269">Générer un code CSS précis</span><span class="sxs-lookup"><span data-stu-id="bc40a-269">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="bc40a-270">Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-270">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="bc40a-271">Pour utiliser le nouvel éditeur de **polices**visuel, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bc40a-271">To use the new visual **Font Editor**, complete the following steps.</span></span>  

1.  <span data-ttu-id="bc40a-272">Ouvrez **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="bc40a-272">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="bc40a-273">Ouvrez **le volet Styles.**</span><span class="sxs-lookup"><span data-stu-id="bc40a-273">Open the **Styles** pane.</span></span>  
1.  <span data-ttu-id="bc40a-274">Sélectionnez **l’icône Éditeur de** polices.</span><span class="sxs-lookup"><span data-stu-id="bc40a-274">Choose the **Font Editor** icon.</span></span>  
    
<span data-ttu-id="bc40a-275">Pour plus d’informations sur le nouvel éditeur de **polices**visuel, accédez à Modifier les styles de police CSS et les paramètres dans le volet Styles dans [DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="bc40a-275">For more information about the new visual **Font Editor**, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Le volet Visual Font Editor est mis en surbrill" lightbox="../media/font-editor-open.msft.png":::
   <span data-ttu-id="bc40a-277">Le volet **Visual Font Editor** est mis en surbrill</span><span class="sxs-lookup"><span data-stu-id="bc40a-277">The visual **Font Editor** pane is highlighted</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-new-css-flexbox-debugging-features"></a><span data-ttu-id="bc40a-278">Activer les nouvelles fonctionnalités de débogage Flexbox CSS</span><span class="sxs-lookup"><span data-stu-id="bc40a-278">Enable new CSS Flexbox debugging features</span></span>  

<span data-ttu-id="bc40a-279">Cette fonctionnalité expérimentale fournit de nombreuses nouvelles visualisations pour vous aider à déboguer les dispositions flexbox CSS.</span><span class="sxs-lookup"><span data-stu-id="bc40a-279">This experimental feature provides many new visualizations to help you debug CSS Flexbox layouts.</span></span>  <span data-ttu-id="bc40a-280">Pour afficher un aperçu des dernières fonctionnalités expérimentales, [activer cette expérience](#turn-on-experimental-features) et recharger DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-280">To preview the latest experimental features, [turn on this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a><span data-ttu-id="bc40a-281">Afficher des superpositions persistantes sur les dispositions Flexbox à l’aide de l’outil Inspect</span><span class="sxs-lookup"><span data-stu-id="bc40a-281">Display persistent overlays on Flexbox layouts with the Inspect tool</span></span>  

<span data-ttu-id="bc40a-282">**L’outil Inspect** permet d’identifier et de visualiser rapidement les dispositions flexbox CSS dans un site web en pointant dessus avec la souris.</span><span class="sxs-lookup"><span data-stu-id="bc40a-282">The **Inspect** tool provides a quick way to identify and visualize CSS Flexbox layouts in a website by hovering on them with the mouse.</span></span>  <span data-ttu-id="bc40a-283">Choisissez **l’icône Inspect** \( Inspect \) dans le coin supérieur gauche ![ de ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-283">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="bc40a-284">Ensuite, lors du débogage du site web, pointez sur un conteneur flexible pour afficher les contours autour du conteneur flexible.</span><span class="sxs-lookup"><span data-stu-id="bc40a-284">Then, while debugging the website, hover on a flex container to display outlines around the flex container.</span></span>  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Afficher les conteneurs Flexbox avec l’outil Inspect" lightbox="../media/flexbox-hover.msft.png":::
   <span data-ttu-id="bc40a-286">Afficher les conteneurs Flexbox avec **l’outil Inspect**</span><span class="sxs-lookup"><span data-stu-id="bc40a-286">Display Flexbox containers with the **Inspect** tool</span></span>  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a><span data-ttu-id="bc40a-287">Afficher des superpositions persistantes sur les dispositions Flexbox</span><span class="sxs-lookup"><span data-stu-id="bc40a-287">Display persistent overlays on Flexbox layouts</span></span>  

<span data-ttu-id="bc40a-288">Dans Microsoft Edge version 89 ou ultérieure, la fonctionnalité expérimentale CSS Flexbox offre également la possibilité d’activer les superpositions persistantes sur les dispositions Flexbox.</span><span class="sxs-lookup"><span data-stu-id="bc40a-288">In Microsoft Edge version 89 or later, the experimental CSS Flexbox feature also offers the option to turn on persistent overlays on Flexbox layouts.</span></span>  <span data-ttu-id="bc40a-289">Les superpositions persistantes offrent les avantages suivants.</span><span class="sxs-lookup"><span data-stu-id="bc40a-289">Persistent overlays provide the following benefits.</span></span>  

*   <span data-ttu-id="bc40a-290">Les superpositions persistantes restent visibles sur la page web lorsque vous faites défiler, déplacez votre souris et utilisez d’autres fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-290">Persistent overlays remain visible on the webpage as you scroll, move your mouse, and use other features of the DevTools.</span></span>
*   <span data-ttu-id="bc40a-291">Plusieurs superpositions persistantes peuvent être utilisées en même temps, pour vous permettre de passer en revue plusieurs dispositions Flexbox à la fois.</span><span class="sxs-lookup"><span data-stu-id="bc40a-291">Multiple persistent overlays may be used at the same time, to allow you to review several Flexbox layouts at once.</span></span>  
*   <span data-ttu-id="bc40a-292">Les superpositions persistantes offrent des options de configuration des couleurs.</span><span class="sxs-lookup"><span data-stu-id="bc40a-292">Persistent overlays offer color configuration options.</span></span>  
    
<span data-ttu-id="bc40a-293">Pour faire bascule les superpositions persistantes sur la disposition Flexbox, utilisez l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="bc40a-293">To toggle persistent overlays on Flexbox layout, use one of following actions.</span></span>  

*   <span data-ttu-id="bc40a-294">Choisissez **l’icône ovale Flexbox** en face de n’importe quel conteneur Flexbox affiché dans l’arborescence DOM de **l’outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="bc40a-294">Choose the **Flexbox** oval icon next to any Flexbox container displayed in the DOM tree of the **Elements** tool.</span></span>  
*   <span data-ttu-id="bc40a-295">Ouvrez le nouveau **panneau de** disposition situé dans l’outil **Éléments,** puis cochez la case en regard de chaque conteneur Flexbox à mettre en surbrillion.</span><span class="sxs-lookup"><span data-stu-id="bc40a-295">Open the new **Layout** panel located in the **Elements** tool, and choose the checkbox next to each Flexbox container you want to highlight.</span></span>  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Icônes flexibles et panneau de disposition dans DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   <span data-ttu-id="bc40a-297">Icônes flexibles et **panneau de** disposition dans DevTools</span><span class="sxs-lookup"><span data-stu-id="bc40a-297">Flex icons and **Layout** panel in DevTools</span></span>  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a><span data-ttu-id="bc40a-298">Configurer des superpositions persistantes</span><span class="sxs-lookup"><span data-stu-id="bc40a-298">Configure persistent overlays</span></span>  

<span data-ttu-id="bc40a-299">Pour configurer les options des superpositions persistantes pour les grilles CSS ou les dispositions Flexbox, utilisez **le** volet De disposition.</span><span class="sxs-lookup"><span data-stu-id="bc40a-299">To configure options for persistent overlays for CSS grids or Flexbox layouts, use the **Layout** pane.</span></span>  <span data-ttu-id="bc40a-300">Le **volet** Disposition se trouve dans l’outil **Éléments** en côté des **volets Styles** **et** Calculés.</span><span class="sxs-lookup"><span data-stu-id="bc40a-300">The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.</span></span>  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Panneau de disposition" lightbox="../media/flexbox-layout.msft.png":::
   <span data-ttu-id="bc40a-302">Panneau de disposition</span><span class="sxs-lookup"><span data-stu-id="bc40a-302">Layout panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable--button-tab-menus-to-open-more-tools"></a><span data-ttu-id="bc40a-303">Activer les menus + onglet de bouton pour ouvrir d’autres outils</span><span class="sxs-lookup"><span data-stu-id="bc40a-303">Enable + button tab menus to open more tools</span></span>  

<span data-ttu-id="bc40a-304">Vous pouvez maintenant ouvrir d’autres outils à l’aide de la nouvelle icône **Plus d’outils** `+` \( \).</span><span class="sxs-lookup"><span data-stu-id="bc40a-304">You may now open more tools using the new **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="bc40a-305">Une fois que vous avez activé les menus Onglet Activer **+** bouton pour ouvrir d’autres outils et recharger DevTools, un signe plus \( \) s’affiche à droite du groupe d’onglets en haut de `+` DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-305">After you turn on the **Enable + button tab menus to open more tools** experiment and reload DevTools, a plus sign \(`+`\) displays to the right of the tab group at the top of the DevTools.</span></span>  <span data-ttu-id="bc40a-306">Pour afficher la liste des autres outils que vous pouvez ajouter à la barre d’onglets, choisissez la nouvelle icône Outils plus **\(** `+` \).</span><span class="sxs-lookup"><span data-stu-id="bc40a-306">To display a list of other tools that you may add to the tab bar, choose the new **More Tools** \(`+`\) icon.</span></span>  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Autres outils dans le volet supérieur" lightbox="../media/experiments-more-tools-button.msft.png":::
   <span data-ttu-id="bc40a-308">**Autres outils** dans le volet supérieur</span><span class="sxs-lookup"><span data-stu-id="bc40a-308">**More Tools** in the top pane</span></span>
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-welcome-tool"></a><span data-ttu-id="bc40a-309">Activer l’outil d’accueil</span><span class="sxs-lookup"><span data-stu-id="bc40a-309">Enable Welcome tool</span></span>

<span data-ttu-id="bc40a-310">Cette expérience remplace **l’outil Nouveautés** par le nouvel **outil Welcome.**</span><span class="sxs-lookup"><span data-stu-id="bc40a-310">This experiment replaces the **What's New** tool with the new **Welcome** tool.</span></span>  <span data-ttu-id="bc40a-311">Il affiche une conception actualisée pour le contenu suivant.</span><span class="sxs-lookup"><span data-stu-id="bc40a-311">It displays a refreshed design for the following content.</span></span>  

*   <span data-ttu-id="bc40a-312">Liens vers des documents de développement</span><span class="sxs-lookup"><span data-stu-id="bc40a-312">Links to developer docs</span></span>  
*   <span data-ttu-id="bc40a-313">fonctionnalités les plus récentes</span><span class="sxs-lookup"><span data-stu-id="bc40a-313">the latest features</span></span>  
*   <span data-ttu-id="bc40a-314">notes de publication</span><span class="sxs-lookup"><span data-stu-id="bc40a-314">release notes</span></span>  
*   <span data-ttu-id="bc40a-315">Option de contact de l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bc40a-315">Option to contact the Microsoft Edge DevTools team</span></span>  
    
<span data-ttu-id="bc40a-316">**L’outil** Welcome s’ouvre automatiquement après chaque mise à jour de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bc40a-316">The **Welcome** tool opens automatically after each update to Microsoft Edge.</span></span>  <span data-ttu-id="bc40a-317">Pour empêcher l’affichage de l’outil **Welcome** après \*\*\*\* chaque mise à jour, cochez la case en regard de l’onglet Ouvrir après chaque mise à jour sous le titre de **l’outil** Welcome.</span><span class="sxs-lookup"><span data-stu-id="bc40a-317">To prevent the display of the **Welcome** tool after each update, clear the checkbox next to **Open tab after each update** under the **Welcome** tool title.</span></span>  

<span data-ttu-id="bc40a-318">Si vous préférez **l’outil Nouveautés d’origine,** accédez à [Expériences][DevtoolsCustomizeIndexSettings]de paramètres et supprimez la case à cocher en regard de l’onglet  >  \*\*\*\* **Activer l’accueil.**</span><span class="sxs-lookup"><span data-stu-id="bc40a-318">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Outil d’accueil" lightbox="../media/experiments-welcome.msft.png":::
   <span data-ttu-id="bc40a-320">**Outil d’accueil**</span><span class="sxs-lookup"><span data-stu-id="bc40a-320">**Welcome** tool</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a><span data-ttu-id="bc40a-321">Fonctionnalités expérimentales précédentes</span><span class="sxs-lookup"><span data-stu-id="bc40a-321">Previous experimental features</span></span>  

*   <span data-ttu-id="bc40a-322">[L’affichage 3D][Devtools3dViewIndex] est désormais disponible et est allumé par défaut dans Microsoft Edge version 83 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bc40a-322">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="bc40a-323">[Activer la prise en charge pour déplacer des onglets][DevtoolsMoveTabs] entre les panneaux est désormais disponible et est désactivée par défaut dans Microsoft Edge version 85 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bc40a-323">[Turn on support to move tabs between panels][DevtoolsMoveTabs] is now available and turned on by default in Microsoft Edge version 85 or later.</span></span>  
*   <span data-ttu-id="bc40a-324">[Personnaliser les raccourcis clavier][DevtoolsCustomKeyboardShortcuts] est désormais disponible et est allumé par défaut dans Microsoft Edge version 86 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bc40a-324">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  
*   <span data-ttu-id="bc40a-325">[Émulation : le mode double écran][DevtoolsDeviceModeDualScreenAndFoldables] de prise en charge est désormais disponible et est allumé par défaut dans Microsoft Edge version 89 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bc40a-325">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="bc40a-326">[Activer les nouvelles fonctionnalités][DevtoolsCssGrid] de débogage de grille CSS est désormais disponible et est désactivé par défaut dans Microsoft Edge version 89 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bc40a-326">[Turn on new CSS grid debugging features][DevtoolsCssGrid] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
    
## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="bc40a-327">Commentaires sur les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="bc40a-327">Providing feedback on experimental features</span></span>  

<span data-ttu-id="bc40a-328">Pour fournir des commentaires sur les expériences DevTools de Microsoft Edge ou sur tout autre point lié à DevTools.</span><span class="sxs-lookup"><span data-stu-id="bc40a-328">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="bc40a-329">Envoyez vos commentaires à l’aide **de l’icône** Envoyer des commentaires dans DevTools</span><span class="sxs-lookup"><span data-stu-id="bc40a-329">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="bc40a-330">Tweet à [l'@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="bc40a-330">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="L’Icône Envoyer des commentaires dans Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="bc40a-332">L’Icône **Envoyer des commentaires** dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bc40a-332">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Affichage 3D | Documents Microsoft"  
[DevtoolsCssGrid]: ../css/grid.md "Inspect CSS Grid in Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsMoveTabs]: ../customize/index.md "Personnaliser microsoft Edge DevTools | Documents Microsoft"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Modifier les styles et paramètres de police CSS dans le volet Styles de DevTools | Documents Microsoft"  
[DevtoolsIssues]: ../issues/index.md "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsShortcuts]: ../shortcuts/index.md "Raccourcis clavier Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Personnaliser les raccourcis clavier dans la | Microsoft Edge DevTools Documents Microsoft"  
[DevtoolsOpenMain]: ../open/index.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[DualScreenWebIndex]: /dual-screen/web/index "Expériences web à double écran | Documents Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtenir l’émulateur Surface Duo | Documents Microsoft"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Comment travailler avec le seam : introduction aux appareils à double écran | Documents Microsoft"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Utiliser l’émulateur Surface Duo | Documents Microsoft"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Fonctionnalité d’écran multimédia CSS pour la détection à double écran | Documents Microsoft"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "L’API JavaScript getWindowSegments pour les appareils à double écran | Documents Microsoft"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clients Bureau à distance | Documents Microsoft"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "| Samsung"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Émuler les appareils à double écran et pliables dans Microsoft Edge DevTools | Documents Microsoft"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
