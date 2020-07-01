---
description: Dernières fonctionnalités expérimentales de Microsoft Edge DevTools
title: Fonctionnalités expérimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, expérience
ms.openlocfilehash: 731a289f555870eeff9cdc160965b59925b70c4d
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843952"
---
# <span data-ttu-id="5c024-104">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="5c024-104">Experimental features</span></span>  

<span data-ttu-id="5c024-105">Vous pouvez utiliser les fonctionnalités expérimentales qui sont toujours en cours de développement dans Microsoft Edge DevTools pour tester et [transmettre des commentaires](#providing-feedback-on-experimental-features) avant chaque sortie.</span><span class="sxs-lookup"><span data-stu-id="5c024-105">You may use the experimental features that are still under development in the Microsoft Edge DevTools to test and [provide feedback](#providing-feedback-on-experimental-features) before each is released broadly.</span></span>  

<span data-ttu-id="5c024-106">Si les fonctionnalités expérimentales sont disponibles dans tous les canaux de Microsoft Edge, vous pouvez obtenir les dernières fonctionnalités expérimentales à l’aide du canal des Canaries Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5c024-106">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="5c024-107">Activer les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="5c024-107">Turn on experimental features</span></span>  

<span data-ttu-id="5c024-108">Procédez comme suit pour activer ou désactiver les fonctionnalités expérimentales dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5c024-108">Use the following steps to turn on \(or off\) experimental features in Microsoft Edge.</span></span>  

1.  <span data-ttu-id="5c024-109">[Ouvrez devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="5c024-109">[Open DevTools][DevtoolsOpen].</span></span>  
     *   <span data-ttu-id="5c024-110">Appuyez sur `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="5c024-110">Press `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="5c024-111">Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="5c024-111">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="5c024-112">Ouvrez le volet **paramètres** .</span><span class="sxs-lookup"><span data-stu-id="5c024-112">Open the **Settings** pane.</span></span>  
    *   <span data-ttu-id="5c024-113">Appuyez sur `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="5c024-113">Press `Shift`+`?`.</span></span>  <span data-ttu-id="5c024-114">Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="5c024-114">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="5c024-115">Sur le côté gauche du volet **paramètres** , sélectionnez la section **expériences** .</span><span class="sxs-lookup"><span data-stu-id="5c024-115">On the left side of the **Settings** pane, select the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/experiments-devtools.png":::
       <span data-ttu-id="5c024-117">Liste des expériences dans les paramètres de DevTools</span><span class="sxs-lookup"><span data-stu-id="5c024-117">List of experiments in DevTools Settings</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5c024-118">Sur la page **expériences** , faites défiler la liste de toutes les fonctionnalités expérimentales disponibles, puis cochez la case en regard de chaque fonctionnalité que vous voulez tester.</span><span class="sxs-lookup"><span data-stu-id="5c024-118">On the **Experiments** page, scroll through the list of all available experimental features and select the checkbox next to each features that you want to test.</span></span>  
1.  <span data-ttu-id="5c024-119">Fermez et rouvrez Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="5c024-119">Close and reopen Microsoft Edge DevTools.</span></span>  

> [!NOTE]
> <span data-ttu-id="5c024-120">Les fonctionnalités expérimentales sont constamment mises à jour et peuvent entraîner des problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="5c024-120">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="5c024-121">Pour désactiver une fonctionnalité expérimentale, ouvrez la page **expériences** , puis décochez la case de la fonctionnalité expérimental que vous souhaitez désactiver.</span><span class="sxs-lookup"><span data-stu-id="5c024-121">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="5c024-122">Fonctionnalités expérimentales mises en évidence</span><span class="sxs-lookup"><span data-stu-id="5c024-122">Highlighted experimental features</span></span>  

<span data-ttu-id="5c024-123">Les sections suivantes décrivent les nouvelles fonctionnalités expérimentales disponibles dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5c024-123">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="5c024-124">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="5c024-124">Experimental feature</span></span> | <span data-ttu-id="5c024-125">Version de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5c024-125">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="5c024-126">Activer les nouvelles fonctionnalités de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="5c024-126">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="5c024-127">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5c024-127">85 or later</span></span> |  
| [<span data-ttu-id="5c024-128">Activer la prise en charge du déplacement des onglets entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="5c024-128">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="5c024-129">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5c024-129">85 or later</span></span> |  
| [<span data-ttu-id="5c024-130">Activer webhint</span><span class="sxs-lookup"><span data-stu-id="5c024-130">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="5c024-131">85 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5c024-131">85 or later</span></span> |  

### <span data-ttu-id="5c024-132">Activer les nouvelles fonctionnalités de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="5c024-132">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="5c024-133">Permet d’améliorer les visualisations sur la page lorsque vous déboguez des sites Web dotés de dispositions CSS.</span><span class="sxs-lookup"><span data-stu-id="5c024-133">Improves on-page visualizations when you debug websites that have CSS grid layouts.</span></span>  <span data-ttu-id="5c024-134">Vous pouvez personnaliser davantage les superpositions dans les paramètres de DevTools.</span><span class="sxs-lookup"><span data-stu-id="5c024-134">You may further customize the overlays in DevTools Settings.</span></span>  

:::image type="complex" source="./media/experiments-grid.png" alt-text="Fonctionnalité de débogage de grille CSS" lightbox="./media/experiments-grid.png":::
   <span data-ttu-id="5c024-136">Fonctionnalité de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="5c024-136">CSS grid debugging feature</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="5c024-137">Activer la prise en charge du déplacement des onglets entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="5c024-137">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="5c024-138">En règle générale, il est possible d’ouvrir des outils tels que des **éléments** et un **réseau** uniquement dans le panneau principal \ (Top \) de devtools.</span><span class="sxs-lookup"><span data-stu-id="5c024-138">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="5c024-139">De même, il est possible d’ouvrir des outils tels que la vue et les **problèmes** en **3D** uniquement dans le panneau tiroir \ (en bas) de devtools.</span><span class="sxs-lookup"><span data-stu-id="5c024-139">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="5c024-140">Lorsque cette expérience est sélectionnée, vous pouvez déplacer des outils entre les volets supérieur et inférieur en pointant sur l’onglet, en ouvrant le menu contextuel \ (clic droit sur \) et en sélectionnant **déplacer vers le haut** ou **déplacer vers le bas**.</span><span class="sxs-lookup"><span data-stu-id="5c024-140">When this experiment is selected, you may move tools between the top and bottom panels by hovering on the tab, opening the contextual menu \(right-click\), and selecting **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="5c024-141">Cette expérience vous permet de personnaliser la disposition de votre DevTools.</span><span class="sxs-lookup"><span data-stu-id="5c024-141">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="5c024-142">Pour afficher ou masquer le panneau inférieur, appuyez sur `Escape` .</span><span class="sxs-lookup"><span data-stu-id="5c024-142">To show or hide the bottom panel, press `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Déplacement d’un onglet entre les panneaux" lightbox="./media/experiments-move-panels.png":::
   <span data-ttu-id="5c024-144">Déplacement d’un onglet entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="5c024-144">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="5c024-145">Activer webhint</span><span class="sxs-lookup"><span data-stu-id="5c024-145">Enable webhint</span></span>  

<span data-ttu-id="5c024-146">[webhint][WebhintMain] est un outil open source qui fournit des commentaires en temps réel sur l’accessibilité, la compatibilité entre les navigateurs, la sécurité, les performances, PWAS, ainsi que d’autres problèmes courants liés au développement Web sur les sites Web.</span><span class="sxs-lookup"><span data-stu-id="5c024-146">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="5c024-147">Cette expérience apporte le commentaire de webhint à DevTools dans le volet des [problèmes][DevtoolsIssues] .</span><span class="sxs-lookup"><span data-stu-id="5c024-147">This experiment brings the webhint feedback into DevTools in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="5c024-148">Vous pouvez sélectionner le problème pour voir la documentation relative à la résolution du problème ainsi qu’une liste des ressources affectées sur votre site Web.</span><span class="sxs-lookup"><span data-stu-id="5c024-148">You may select the issue to see documentation on how to fix the issue and a list of the affected resources on your website.</span></span>  <span data-ttu-id="5c024-149">Sélectionnez un lien vers une ressource pour ouvrir le volet **réseau**, **sources**ou **éléments** approprié dans devtools.</span><span class="sxs-lookup"><span data-stu-id="5c024-149">Select a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="Commentaires de webhint dans le volet problèmes" lightbox="./media/experiments-webhint.png":::
   <span data-ttu-id="5c024-151">Commentaires de webhint dans le volet problèmes</span><span class="sxs-lookup"><span data-stu-id="5c024-151">webhint feedback in the Issues panel</span></span>  
:::image-end:::      

<!--Available in Microsoft Edge version 85 and later.  -->  

## <span data-ttu-id="5c024-152">Fonctionnalités expérimentales antérieures</span><span class="sxs-lookup"><span data-stu-id="5c024-152">Previous experimental features</span></span>  

*   <span data-ttu-id="5c024-153">la [vue 3D][Devtools3DView] est désormais disponible et activée par défaut dans Microsoft Edge version 83 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5c024-153">[3D View][Devtools3DView] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  

## <span data-ttu-id="5c024-154">Fourniture de commentaires sur les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="5c024-154">Providing feedback on experimental features</span></span>  

<span data-ttu-id="5c024-155">Pour transmettre des commentaires sur les expériences DevTools Microsoft Edge, ou tout autre élément associé à DevTools:</span><span class="sxs-lookup"><span data-stu-id="5c024-155">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools:</span></span>  

*   <span data-ttu-id="5c024-156">Envoyez vos commentaires à l’aide de l’icône de commentaires dans le DevTools</span><span class="sxs-lookup"><span data-stu-id="5c024-156">Send your feedback using the Feedback icon in the DevTools</span></span>  
*   <span data-ttu-id="5c024-157">Tweeter sur [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="5c024-157">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="./media/devtools-feedback.png" alt-text="Icône de commentaires dans le Microsoft Edge DevTools" lightbox="./media/devtools-feedback.png":::
   <span data-ttu-id="5c024-159">Icône de commentaires dans le Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5c024-159">Feedback icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[Devtools3DView]: ./3D-view.md "Affichage 3D | Documents Microsoft"  
[DevtoolsIssues]: ./issues/index.md "Recherchez et corrigez les problèmes liés à l’outil problèmes dans Microsoft Edge DevTools Documents Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Raccourcis clavier de Microsoft Edge DevTools-Microsoft documents"  
[DevtoolsOpen]: ./open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "Astuce" 
