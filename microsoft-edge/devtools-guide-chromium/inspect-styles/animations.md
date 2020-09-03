---
description: Examinez et modifiez des animations avec l’inspecteur d’animation Microsoft Edge DevTools.
title: Inspecter des animations
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: a74a401edf5331f2dd3c1bf574110241f616d9f6
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992826"
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





# <span data-ttu-id="76864-104">Inspecter des animations</span><span class="sxs-lookup"><span data-stu-id="76864-104">Inspect animations</span></span>   



<span data-ttu-id="76864-105">Examinez et modifiez des animations avec l’inspecteur d’animation Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="76864-105">Inspect and modify animations with the Microsoft Edge DevTools Animation Inspector.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="inspecteur d’animation" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   <span data-ttu-id="76864-107">inspecteur d’animation</span><span class="sxs-lookup"><span data-stu-id="76864-107">animation inspector</span></span>  
:::image-end:::  

### <span data-ttu-id="76864-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="76864-108">Summary</span></span>  

*   <span data-ttu-id="76864-109">Capturez des animations en ouvrant l’inspecteur d’animation.</span><span class="sxs-lookup"><span data-stu-id="76864-109">Capture animations by opening the Animation Inspector.</span></span>  <span data-ttu-id="76864-110">L’inspecteur d’animation détecte et trie automatiquement les animations au sein de groupes.</span><span class="sxs-lookup"><span data-stu-id="76864-110">The Animation Inspector automatically detects and sorts animations into groups.</span></span>  
*   <span data-ttu-id="76864-111">Examinez les animations en ralentissant chacune d’elles, en reproduisant chacune d’elles ou en consultant le code source.</span><span class="sxs-lookup"><span data-stu-id="76864-111">Inspect animations by slowing down each one, replaying each one, or viewing the source code.</span></span>  
*   <span data-ttu-id="76864-112">Modifiez des animations en modifiant le minutage, le délai, la durée ou les décalages d’images clés.</span><span class="sxs-lookup"><span data-stu-id="76864-112">Modify animations by changing the timing, delay, duration, or keyframe offsets.</span></span>  

## <span data-ttu-id="76864-113">Présentation</span><span class="sxs-lookup"><span data-stu-id="76864-113">Overview</span></span>   

<span data-ttu-id="76864-114">L’inspecteur d’animation Microsoft Edge DevTools possède deux objectifs principaux.</span><span class="sxs-lookup"><span data-stu-id="76864-114">The Microsoft Edge DevTools Animation Inspector has two main purposes.</span></span>  

*   <span data-ttu-id="76864-115">Examen des animations.</span><span class="sxs-lookup"><span data-stu-id="76864-115">Inspecting animations.</span></span>  <span data-ttu-id="76864-116">Vous voulez ralentir, relire ou inspecter le code source d’un groupe d’animations.</span><span class="sxs-lookup"><span data-stu-id="76864-116">You want to slow down, replay, or inspect the source code for an Animation Group.</span></span>  
*   <span data-ttu-id="76864-117">Modification des animations.</span><span class="sxs-lookup"><span data-stu-id="76864-117">Modifying animations.</span></span>  <span data-ttu-id="76864-118">Vous souhaitez modifier les décalements minutage, délai, durée et image clé d’un groupe d’animations.</span><span class="sxs-lookup"><span data-stu-id="76864-118">You want to modify the timing, delay, duration, or keyframe offsets of an Animation Group.</span></span>  <span data-ttu-id="76864-119">La modification Bézier et la modification des images clés ne sont actuellement pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="76864-119">Bezier editing and keyframe editing are currently not supported.</span></span>  

<span data-ttu-id="76864-120">L’inspecteur d’animation prend en charge des animations CSS, des transitions CSS et des animations Web.</span><span class="sxs-lookup"><span data-stu-id="76864-120">The Animation Inspector supports CSS animations, CSS transitions, and web animations.</span></span>  `requestAnimationFrame` <span data-ttu-id="76864-121">les animations ne sont actuellement pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="76864-121">animations are currently not supported.</span></span>  

### <span data-ttu-id="76864-122">Qu’est-ce qu’un groupe d’animations?</span><span class="sxs-lookup"><span data-stu-id="76864-122">What is an Animation Group?</span></span>  

<span data-ttu-id="76864-123">Un groupe d’animations est un groupe d’animations qui peut être lié les uns aux autres.</span><span class="sxs-lookup"><span data-stu-id="76864-123">An Animation Group is a group of animations that may be related to each other.</span></span>  <span data-ttu-id="76864-124">Pour l’instant, le Web n’ayant pas de véritable concept d’animation de groupe, les concepteurs de trajectoire et les développeurs doivent donc composer et temps des animations individuelles pour que les animations s’affichent comme un effet visuel cohérent.</span><span class="sxs-lookup"><span data-stu-id="76864-124">Currently, the web has no real concept of a group animation, so motion designers and developers have to compose and time individual animations so that the animations render as one coherent visual effect.</span></span>  <span data-ttu-id="76864-125">L’inspecteur d’animation prédit quelles animations sont liées en fonction de l’heure de début (sauf retards, etc.).</span><span class="sxs-lookup"><span data-stu-id="76864-125">The Animation Inspector predicts which animations are related based on start time \(excluding delays, and so on\).</span></span>  <span data-ttu-id="76864-126">L’inspecteur d’animation regroupe également les animations côte à côte.</span><span class="sxs-lookup"><span data-stu-id="76864-126">The Animation Inspector also groups the animations side-by-side.</span></span>  
<span data-ttu-id="76864-127">En d’autres termes, un ensemble d’animations déclenchées dans le même bloc de script est regroupé.</span><span class="sxs-lookup"><span data-stu-id="76864-127">In other words, a set of animations that are all triggered in the same script block are grouped together.</span></span>  <span data-ttu-id="76864-128">S’il s’agit d’une animation asynchrone, elle est placée dans un groupe séparé.</span><span class="sxs-lookup"><span data-stu-id="76864-128">If an animation is asynchronous, it is placed in a separate group.</span></span>  

## <span data-ttu-id="76864-129">Prise en main</span><span class="sxs-lookup"><span data-stu-id="76864-129">Get started</span></span>  

<span data-ttu-id="76864-130">Il existe deux façons d’ouvrir l’inspecteur d’animation:</span><span class="sxs-lookup"><span data-stu-id="76864-130">There are two ways to open the Animation Inspector:</span></span>  

*   <span data-ttu-id="76864-131">Ouvrir le menu **personnaliser et contrôler devtools**</span><span class="sxs-lookup"><span data-stu-id="76864-131">Open the **Customize and Control DevTools** menu</span></span>  
    1.  <span data-ttu-id="76864-132">Accédez au sous-menu **plus d’outils** .</span><span class="sxs-lookup"><span data-stu-id="76864-132">Navigate to the **More tools** sub-menu.</span></span>  
    1.  <span data-ttu-id="76864-133">Sélectionnez **animations**:</span><span class="sxs-lookup"><span data-stu-id="76864-133">Select **Animations**:</span></span>  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Animations utilisant le menu principal" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           <span data-ttu-id="76864-135">**Animations** utilisant le menu principal</span><span class="sxs-lookup"><span data-stu-id="76864-135">**Animations** using Main Menu</span></span>  
    :::image-end:::  
        
*   <span data-ttu-id="76864-136">Ouvrir le **menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="76864-136">Open the **Command Menu**</span></span>  
    1.  <span data-ttu-id="76864-137">Entrez `Drawer: Show Animations`.</span><span class="sxs-lookup"><span data-stu-id="76864-137">Type `Drawer: Show Animations`.</span></span>  

<span data-ttu-id="76864-138">L’inspecteur d’animation s’ouvre en tant qu’onglet en regard du tiroir de la console.</span><span class="sxs-lookup"><span data-stu-id="76864-138">The Animation Inspector opens up as a tab next to the Console Drawer.</span></span>  <span data-ttu-id="76864-139">Dans la mesure où l’inspecteur d’animation est l’onglet tiroir, vous pouvez utiliser l’inspecteur d’animation de n’importe quel panneau DevTools.</span><span class="sxs-lookup"><span data-stu-id="76864-139">Since the Animation Inspector is a Drawer tab, you may use the Animation Inspector from any DevTools panel.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Inspecteur d’animation vide" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   <span data-ttu-id="76864-141">Inspecteur d’animation vide</span><span class="sxs-lookup"><span data-stu-id="76864-141">Empty Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="76864-142">L’inspecteur d’animation est groupé en quatre sections principales \ (ou volets \).</span><span class="sxs-lookup"><span data-stu-id="76864-142">The Animation Inspector is grouped into four main sections \(or panes\).</span></span>  <span data-ttu-id="76864-143">Ce guide fait référence à chaque volet comme suit:</span><span class="sxs-lookup"><span data-stu-id="76864-143">This guide refers to each pane as follows:</span></span>  

| | <span data-ttu-id="76864-144">Volet</span><span class="sxs-lookup"><span data-stu-id="76864-144">Pane</span></span> | <span data-ttu-id="76864-145">Description</span><span class="sxs-lookup"><span data-stu-id="76864-145">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="76864-146">1</span><span class="sxs-lookup"><span data-stu-id="76864-146">1</span></span> | **<span data-ttu-id="76864-147">Contrôles</span><span class="sxs-lookup"><span data-stu-id="76864-147">Controls</span></span>** | <span data-ttu-id="76864-148">Vous pouvez alors effacer tous les groupes d’animations actuellement capturées ou changer la vitesse du groupe d’animation actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="76864-148">From here you may clear all currently captured Animation Groups, or change the speed of the currently selected Animation Group.</span></span> |  
| <span data-ttu-id="76864-149">deuxième</span><span class="sxs-lookup"><span data-stu-id="76864-149">2</span></span> | **<span data-ttu-id="76864-150">Présentation</span><span class="sxs-lookup"><span data-stu-id="76864-150">Overview</span></span>** | <span data-ttu-id="76864-151">Sélectionnez un groupe d’animations pour l’inspecter et le modifier dans le volet **Détails** .</span><span class="sxs-lookup"><span data-stu-id="76864-151">Select an Animation Group here to inspect and modify it in the **Details** pane.</span></span> |  
| <span data-ttu-id="76864-152">3D</span><span class="sxs-lookup"><span data-stu-id="76864-152">3</span></span> | **<span data-ttu-id="76864-153">Chronologie</span><span class="sxs-lookup"><span data-stu-id="76864-153">Timeline</span></span>** | <span data-ttu-id="76864-154">Interrompez et démarrez une animation à partir de cet emplacement, ou accédez à un point spécifique de l’animation.</span><span class="sxs-lookup"><span data-stu-id="76864-154">Pause and start an animation from here, or jump to a specific point in the animation.</span></span> |  
| <span data-ttu-id="76864-155">n°4</span><span class="sxs-lookup"><span data-stu-id="76864-155">4</span></span> | **<span data-ttu-id="76864-156">Détails</span><span class="sxs-lookup"><span data-stu-id="76864-156">Details</span></span>** | <span data-ttu-id="76864-157">Inspecter et modifier le groupe d’animations actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="76864-157">Inspect and modify the currently selected Animation Group.</span></span> |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Inspecteur d’animation annoté" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   <span data-ttu-id="76864-159">Inspecteur d’animation annoté</span><span class="sxs-lookup"><span data-stu-id="76864-159">Annotated Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="76864-160">Pour capturer une animation, il vous suffit d’effectuer l’interaction déclenchant l’animation lorsque l’inspecteur d’animation est ouvert.</span><span class="sxs-lookup"><span data-stu-id="76864-160">To capture an animation, just perform the interaction that triggers the animation while the Animation Inspector is open.</span></span>  <span data-ttu-id="76864-161">Si une animation est déclenchée lors du chargement de la page, rechargez la page avec l’inspecteur d’animation ouvert pour détecter l’animation.</span><span class="sxs-lookup"><span data-stu-id="76864-161">If an animation is triggered on page load, reload the page with the Animation Inspector open to detect the animation.</span></span>  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <span data-ttu-id="76864-162">Inspecter des animations</span><span class="sxs-lookup"><span data-stu-id="76864-162">Inspect animations</span></span>   

<span data-ttu-id="76864-163">Après avoir capturé une animation, plusieurs méthodes s’offrent à vous pour les relire:</span><span class="sxs-lookup"><span data-stu-id="76864-163">After you capture an animation, there are a few ways to replay it:</span></span>  

*   <span data-ttu-id="76864-164">Placez le pointeur de la souris sur la miniature dans le volet **vue d’ensemble** pour en afficher un aperçu.</span><span class="sxs-lookup"><span data-stu-id="76864-164">Hover over the thumbnail in the **Overview** pane to view a preview of it.</span></span>  
*   <span data-ttu-id="76864-165">Sélectionnez le groupe animation dans le volet **vue d’ensemble** \ (pour qu’il s’affiche dans le volet d' **informations** ), puis appuyez sur l’icône **relire** ![ ][ImageReplayButtonIcon] .</span><span class="sxs-lookup"><span data-stu-id="76864-165">Select the Animation Group from the **Overview** pane \(so that it is displayed in the **Details** pane\) and press the **replay** \(![replay icon][ImageReplayButtonIcon]\) icon.</span></span>  <span data-ttu-id="76864-166">L’animation est relues dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="76864-166">The animation is replayed in the viewport.</span></span>  <span data-ttu-id="76864-167">Cliquez sur l’icône **Vitesse d’animation** \ (icônes de ![ Vitesse ][ImageAnimationSpeedButtonsIcon] d’animation \) pour modifier la vitesse d’aperçu du groupe d’animation actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="76864-167">Click on the **animation speed** \(![animation speed icons][ImageAnimationSpeedButtonsIcon]\) icons to change the preview speed of the currently selected Animation Group.</span></span>  <span data-ttu-id="76864-168">Vous pouvez utiliser la barre verticale rouge pour modifier votre position actuelle.</span><span class="sxs-lookup"><span data-stu-id="76864-168">You may use the red vertical bar to change your current position.</span></span>  
*   <span data-ttu-id="76864-169">Cliquez et faites glisser la barre verticale rouge pour faire défiler l’animation d’affichage.</span><span class="sxs-lookup"><span data-stu-id="76864-169">Click and drag the red vertical bar to scrub the viewport animation.</span></span>  
    
### <span data-ttu-id="76864-170">Afficher les détails d’une animation</span><span class="sxs-lookup"><span data-stu-id="76864-170">View animation details</span></span>  

<span data-ttu-id="76864-171">Une fois le groupe d’animations capturé, cliquez dessus dans le volet **vue d’ensemble** pour afficher les détails.</span><span class="sxs-lookup"><span data-stu-id="76864-171">After you capture an Animation Group, click on it from the **Overview** pane to view the details.</span></span>  <span data-ttu-id="76864-172">Dans le volet d' **informations** , chaque animation individuelle est affectée à une ligne.</span><span class="sxs-lookup"><span data-stu-id="76864-172">In the **Details** pane each individual animation is assigned the a row.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Détails sur le groupe d’animations" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="76864-174">Détails sur le groupe d’animations</span><span class="sxs-lookup"><span data-stu-id="76864-174">Animation Group details</span></span>  
:::image-end:::  

<span data-ttu-id="76864-175">Placez le pointeur sur une animation pour la mettre en surbrillance dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="76864-175">Hover over an animation to highlight it in the viewport.</span></span>  <span data-ttu-id="76864-176">Cliquez sur l’animation pour la sélectionner dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="76864-176">Click on the animation to select it in the **Elements** panel.</span></span>  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Survol de l’animation pour la mettre en surbrillance dans la fenêtre d’affichage" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="76864-178">Survol de l’animation pour la mettre en surbrillance dans la fenêtre d’affichage</span><span class="sxs-lookup"><span data-stu-id="76864-178">Hover over the animation to highlight it in viewport</span></span>  
:::image-end:::  

<span data-ttu-id="76864-179">La section la plus à gauche d’une animation est la définition.</span><span class="sxs-lookup"><span data-stu-id="76864-179">The leftmost, darker section of an animation is the definition.</span></span>  <span data-ttu-id="76864-180">La section à droite, plus ternie représente des itérations.</span><span class="sxs-lookup"><span data-stu-id="76864-180">The right, more faded section represents iterations.</span></span>  <span data-ttu-id="76864-181">Par exemple, dans l’illustration suivante, les sections deux et trois représentent des itérations de la section One.</span><span class="sxs-lookup"><span data-stu-id="76864-181">For example, in the following figure, sections two and three represent iterations of section one.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Diagramme d’itérations d’animation" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   <span data-ttu-id="76864-183">Diagramme d’itérations d’animation</span><span class="sxs-lookup"><span data-stu-id="76864-183">Diagram of animation iterations</span></span>  
:::image-end:::  

<span data-ttu-id="76864-184">Si deux éléments ont la même animation appliquée, l’inspecteur d’animation affecte la même couleur aux éléments.</span><span class="sxs-lookup"><span data-stu-id="76864-184">If two elements have the same animation applied, the Animation Inspector assigns the same color to the elements.</span></span>  <span data-ttu-id="76864-185">La couleur est aléatoire et n’a aucune précision.</span><span class="sxs-lookup"><span data-stu-id="76864-185">The color is random and has no significance.</span></span>  <span data-ttu-id="76864-186">Par exemple, dans l’illustration suivante, les deux éléments `div.cwccw.earlier` et `div.cwccw.later` ont la même animation \ ( `spinrightleft` \) appliquée, comme les `div.ccwcw.earlier` éléments et `div.ccwcw.later` .</span><span class="sxs-lookup"><span data-stu-id="76864-186">For example, in the following figure, the two elements `div.cwccw.earlier` and `div.cwccw.later` have the same animation \(`spinrightleft`\) applied, as do the `div.ccwcw.earlier` and `div.ccwcw.later` elements.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Animations à code couleur" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   <span data-ttu-id="76864-188">Animations à code couleur</span><span class="sxs-lookup"><span data-stu-id="76864-188">Color-coded animations</span></span>  
:::image-end:::  

## <span data-ttu-id="76864-189">Modifier des animations</span><span class="sxs-lookup"><span data-stu-id="76864-189">Modify animations</span></span>   

<span data-ttu-id="76864-190">Il existe trois façons de modifier une animation à l’aide de l’inspecteur d’animation.</span><span class="sxs-lookup"><span data-stu-id="76864-190">There are three ways you are able to modify an animation with the Animation Inspector.</span></span>  

*   <span data-ttu-id="76864-191">Durée de l’animation.</span><span class="sxs-lookup"><span data-stu-id="76864-191">Animation duration.</span></span>  
*   <span data-ttu-id="76864-192">Minutage des images clés.</span><span class="sxs-lookup"><span data-stu-id="76864-192">Keyframe timings.</span></span>  
*   <span data-ttu-id="76864-193">Délai de début</span><span class="sxs-lookup"><span data-stu-id="76864-193">Start time delay.</span></span>  
    
<span data-ttu-id="76864-194">Dans l’illustration suivante, l’animation d’origine est représentée.</span><span class="sxs-lookup"><span data-stu-id="76864-194">In the following figure, the original animation is represented.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Animation d’origine avant modification" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   <span data-ttu-id="76864-196">Animation d’origine avant modification</span><span class="sxs-lookup"><span data-stu-id="76864-196">Original animation before modification</span></span>  
:::image-end:::  

<span data-ttu-id="76864-197">Pour modifier la durée d’une animation, cliquez sur le premier ou le dernier cercle et faites-le glisser.</span><span class="sxs-lookup"><span data-stu-id="76864-197">To change the duration of an animation, click and drag the first or last circle.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Durée modifiée" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   <span data-ttu-id="76864-199">Durée modifiée</span><span class="sxs-lookup"><span data-stu-id="76864-199">Modified duration</span></span>  
:::image-end:::  

<span data-ttu-id="76864-200">Si l’animation définit des règles d’images clés, celles-ci sont représentées sous forme de cercles intérieurs blancs.</span><span class="sxs-lookup"><span data-stu-id="76864-200">If the animation defines any keyframe rules, then these are represented as white inner circles.</span></span>  <span data-ttu-id="76864-201">Cliquez sur l’un des éléments suivants pour modifier le minutage de l’image clé.</span><span class="sxs-lookup"><span data-stu-id="76864-201">Click and drag one of these to change the timing of the keyframe.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Image clé modifiée" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   <span data-ttu-id="76864-203">Image clé modifiée</span><span class="sxs-lookup"><span data-stu-id="76864-203">Modified keyframe</span></span>  
:::image-end:::  

<span data-ttu-id="76864-204">Pour ajouter un délai à une animation, cliquez dessus et faites-la glisser n’importe où, à l’exception des cercles.</span><span class="sxs-lookup"><span data-stu-id="76864-204">To add a delay to an animation, click and drag it anywhere except the circles.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Retard modifié" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   <span data-ttu-id="76864-206">Retard modifié</span><span class="sxs-lookup"><span data-stu-id="76864-206">Modified delay</span></span>  
:::image-end:::  

<!--  
  


-->  

<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: ../media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: ../media/replay-button-icon.msft.png  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="76864-207">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="76864-207">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="76864-208">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="76864-208">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="76864-210">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="76864-210">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
