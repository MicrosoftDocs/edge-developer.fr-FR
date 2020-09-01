---
title: Inspecter des animations
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: a6970d76f4ff70031ef4cc8c6de119a41d1a5b80
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983372"
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





# <span data-ttu-id="e95fd-103">Inspecter des animations</span><span class="sxs-lookup"><span data-stu-id="e95fd-103">Inspect animations</span></span>   



<span data-ttu-id="e95fd-104">Examinez et modifiez des animations avec l’inspecteur d’animation Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="e95fd-104">Inspect and modify animations with the Microsoft Edge DevTools Animation Inspector.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="inspecteur d’animation" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   <span data-ttu-id="e95fd-106">inspecteur d’animation</span><span class="sxs-lookup"><span data-stu-id="e95fd-106">animation inspector</span></span>  
:::image-end:::  

### <span data-ttu-id="e95fd-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="e95fd-107">Summary</span></span>  

*   <span data-ttu-id="e95fd-108">Capturez des animations en ouvrant l’inspecteur d’animation.</span><span class="sxs-lookup"><span data-stu-id="e95fd-108">Capture animations by opening the Animation Inspector.</span></span>  <span data-ttu-id="e95fd-109">L’inspecteur d’animation détecte et trie automatiquement les animations au sein de groupes.</span><span class="sxs-lookup"><span data-stu-id="e95fd-109">The Animation Inspector automatically detects and sorts animations into groups.</span></span>  
*   <span data-ttu-id="e95fd-110">Examinez les animations en ralentissant chacune d’elles, en reproduisant chacune d’elles ou en consultant le code source.</span><span class="sxs-lookup"><span data-stu-id="e95fd-110">Inspect animations by slowing down each one, replaying each one, or viewing the source code.</span></span>  
*   <span data-ttu-id="e95fd-111">Modifiez des animations en modifiant le minutage, le délai, la durée ou les décalages d’images clés.</span><span class="sxs-lookup"><span data-stu-id="e95fd-111">Modify animations by changing the timing, delay, duration, or keyframe offsets.</span></span>  

## <span data-ttu-id="e95fd-112">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="e95fd-112">Overview</span></span>   

<span data-ttu-id="e95fd-113">L’inspecteur d’animation Microsoft Edge DevTools possède deux objectifs principaux.</span><span class="sxs-lookup"><span data-stu-id="e95fd-113">The Microsoft Edge DevTools Animation Inspector has two main purposes.</span></span>  

*   <span data-ttu-id="e95fd-114">Examen des animations.</span><span class="sxs-lookup"><span data-stu-id="e95fd-114">Inspecting animations.</span></span>  <span data-ttu-id="e95fd-115">Vous voulez ralentir, relire ou inspecter le code source d’un groupe d’animations.</span><span class="sxs-lookup"><span data-stu-id="e95fd-115">You want to slow down, replay, or inspect the source code for an Animation Group.</span></span>  
*   <span data-ttu-id="e95fd-116">Modification des animations.</span><span class="sxs-lookup"><span data-stu-id="e95fd-116">Modifying animations.</span></span>  <span data-ttu-id="e95fd-117">Vous souhaitez modifier les décalements minutage, délai, durée et image clé d’un groupe d’animations.</span><span class="sxs-lookup"><span data-stu-id="e95fd-117">You want to modify the timing, delay, duration, or keyframe offsets of an Animation Group.</span></span>  <span data-ttu-id="e95fd-118">La modification Bézier et la modification des images clés ne sont actuellement pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e95fd-118">Bezier editing and keyframe editing are currently not supported.</span></span>  

<span data-ttu-id="e95fd-119">L’inspecteur d’animation prend en charge des animations CSS, des transitions CSS et des animations Web.</span><span class="sxs-lookup"><span data-stu-id="e95fd-119">The Animation Inspector supports CSS animations, CSS transitions, and web animations.</span></span>  `requestAnimationFrame` <span data-ttu-id="e95fd-120">les animations ne sont actuellement pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e95fd-120">animations are currently not supported.</span></span>  

### <span data-ttu-id="e95fd-121">Qu’est-ce qu’un groupe d’animations?</span><span class="sxs-lookup"><span data-stu-id="e95fd-121">What is an Animation Group?</span></span>  

<span data-ttu-id="e95fd-122">Un groupe d’animations est un groupe d’animations qui peut être lié les uns aux autres.</span><span class="sxs-lookup"><span data-stu-id="e95fd-122">An Animation Group is a group of animations that may be related to each other.</span></span>  <span data-ttu-id="e95fd-123">Pour l’instant, le Web n’ayant pas de véritable concept d’animation de groupe, les concepteurs de trajectoire et les développeurs doivent donc composer et temps des animations individuelles pour que les animations s’affichent comme un effet visuel cohérent.</span><span class="sxs-lookup"><span data-stu-id="e95fd-123">Currently, the web has no real concept of a group animation, so motion designers and developers have to compose and time individual animations so that the animations render as one coherent visual effect.</span></span>  <span data-ttu-id="e95fd-124">L’inspecteur d’animation prédit quelles animations sont liées en fonction de l’heure de début (sauf retards, etc.).</span><span class="sxs-lookup"><span data-stu-id="e95fd-124">The Animation Inspector predicts which animations are related based on start time \(excluding delays, and so on\).</span></span>  <span data-ttu-id="e95fd-125">L’inspecteur d’animation regroupe également les animations côte à côte.</span><span class="sxs-lookup"><span data-stu-id="e95fd-125">The Animation Inspector also groups the animations side-by-side.</span></span>  
<span data-ttu-id="e95fd-126">En d’autres termes, un ensemble d’animations déclenchées dans le même bloc de script est regroupé.</span><span class="sxs-lookup"><span data-stu-id="e95fd-126">In other words, a set of animations that are all triggered in the same script block are grouped together.</span></span>  <span data-ttu-id="e95fd-127">S’il s’agit d’une animation asynchrone, elle est placée dans un groupe séparé.</span><span class="sxs-lookup"><span data-stu-id="e95fd-127">If an animation is asynchronous, it is placed in a separate group.</span></span>  

## <span data-ttu-id="e95fd-128">Prise en main</span><span class="sxs-lookup"><span data-stu-id="e95fd-128">Get started</span></span>  

<span data-ttu-id="e95fd-129">Il existe deux façons d’ouvrir l’inspecteur d’animation:</span><span class="sxs-lookup"><span data-stu-id="e95fd-129">There are two ways to open the Animation Inspector:</span></span>  

*   <span data-ttu-id="e95fd-130">Ouvrir le menu **personnaliser et contrôler devtools**</span><span class="sxs-lookup"><span data-stu-id="e95fd-130">Open the **Customize and Control DevTools** menu</span></span>  
    1.  <span data-ttu-id="e95fd-131">Accédez au sous-menu **plus d’outils** .</span><span class="sxs-lookup"><span data-stu-id="e95fd-131">Navigate to the **More tools** sub-menu.</span></span>  
    1.  <span data-ttu-id="e95fd-132">Sélectionnez **animations**:</span><span class="sxs-lookup"><span data-stu-id="e95fd-132">Select **Animations**:</span></span>  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Animations utilisant le menu principal" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           <span data-ttu-id="e95fd-134">**Animations** utilisant le menu principal</span><span class="sxs-lookup"><span data-stu-id="e95fd-134">**Animations** using Main Menu</span></span>  
    :::image-end:::  
        
*   <span data-ttu-id="e95fd-135">Ouvrir le **menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="e95fd-135">Open the **Command Menu**</span></span>  
    1.  <span data-ttu-id="e95fd-136">Entrez `Drawer: Show Animations`.</span><span class="sxs-lookup"><span data-stu-id="e95fd-136">Type `Drawer: Show Animations`.</span></span>  

<span data-ttu-id="e95fd-137">L’inspecteur d’animation s’ouvre en tant qu’onglet en regard du tiroir de la console.</span><span class="sxs-lookup"><span data-stu-id="e95fd-137">The Animation Inspector opens up as a tab next to the Console Drawer.</span></span>  <span data-ttu-id="e95fd-138">Dans la mesure où l’inspecteur d’animation est l’onglet tiroir, vous pouvez utiliser l’inspecteur d’animation de n’importe quel panneau DevTools.</span><span class="sxs-lookup"><span data-stu-id="e95fd-138">Since the Animation Inspector is a Drawer tab, you may use the Animation Inspector from any DevTools panel.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Inspecteur d’animation vide" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   <span data-ttu-id="e95fd-140">Inspecteur d’animation vide</span><span class="sxs-lookup"><span data-stu-id="e95fd-140">Empty Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="e95fd-141">L’inspecteur d’animation est groupé en quatre sections principales \ (ou volets \).</span><span class="sxs-lookup"><span data-stu-id="e95fd-141">The Animation Inspector is grouped into four main sections \(or panes\).</span></span>  <span data-ttu-id="e95fd-142">Ce guide fait référence à chaque volet comme suit:</span><span class="sxs-lookup"><span data-stu-id="e95fd-142">This guide refers to each pane as follows:</span></span>  

| | <span data-ttu-id="e95fd-143">Volet</span><span class="sxs-lookup"><span data-stu-id="e95fd-143">Pane</span></span> | <span data-ttu-id="e95fd-144">Description</span><span class="sxs-lookup"><span data-stu-id="e95fd-144">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="e95fd-145">1</span><span class="sxs-lookup"><span data-stu-id="e95fd-145">1</span></span> | **<span data-ttu-id="e95fd-146">Contrôles</span><span class="sxs-lookup"><span data-stu-id="e95fd-146">Controls</span></span>** | <span data-ttu-id="e95fd-147">Vous pouvez alors effacer tous les groupes d’animations actuellement capturées ou changer la vitesse du groupe d’animation actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e95fd-147">From here you may clear all currently captured Animation Groups, or change the speed of the currently selected Animation Group.</span></span> |  
| <span data-ttu-id="e95fd-148">deuxième</span><span class="sxs-lookup"><span data-stu-id="e95fd-148">2</span></span> | **<span data-ttu-id="e95fd-149">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="e95fd-149">Overview</span></span>** | <span data-ttu-id="e95fd-150">Sélectionnez un groupe d’animations pour l’inspecter et le modifier dans le volet **Détails** .</span><span class="sxs-lookup"><span data-stu-id="e95fd-150">Select an Animation Group here to inspect and modify it in the **Details** pane.</span></span> |  
| <span data-ttu-id="e95fd-151">3D</span><span class="sxs-lookup"><span data-stu-id="e95fd-151">3</span></span> | **<span data-ttu-id="e95fd-152">Chronologie</span><span class="sxs-lookup"><span data-stu-id="e95fd-152">Timeline</span></span>** | <span data-ttu-id="e95fd-153">Interrompez et démarrez une animation à partir de cet emplacement, ou accédez à un point spécifique de l’animation.</span><span class="sxs-lookup"><span data-stu-id="e95fd-153">Pause and start an animation from here, or jump to a specific point in the animation.</span></span> |  
| <span data-ttu-id="e95fd-154">n°4</span><span class="sxs-lookup"><span data-stu-id="e95fd-154">4</span></span> | **<span data-ttu-id="e95fd-155">Détails</span><span class="sxs-lookup"><span data-stu-id="e95fd-155">Details</span></span>** | <span data-ttu-id="e95fd-156">Inspecter et modifier le groupe d’animations actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e95fd-156">Inspect and modify the currently selected Animation Group.</span></span> |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Inspecteur d’animation annoté" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   <span data-ttu-id="e95fd-158">Inspecteur d’animation annoté</span><span class="sxs-lookup"><span data-stu-id="e95fd-158">Annotated Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="e95fd-159">Pour capturer une animation, il vous suffit d’effectuer l’interaction déclenchant l’animation lorsque l’inspecteur d’animation est ouvert.</span><span class="sxs-lookup"><span data-stu-id="e95fd-159">To capture an animation, just perform the interaction that triggers the animation while the Animation Inspector is open.</span></span>  <span data-ttu-id="e95fd-160">Si une animation est déclenchée lors du chargement de la page, rechargez la page avec l’inspecteur d’animation ouvert pour détecter l’animation.</span><span class="sxs-lookup"><span data-stu-id="e95fd-160">If an animation is triggered on page load, reload the page with the Animation Inspector open to detect the animation.</span></span>  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <span data-ttu-id="e95fd-161">Inspecter des animations</span><span class="sxs-lookup"><span data-stu-id="e95fd-161">Inspect animations</span></span>   

<span data-ttu-id="e95fd-162">Après avoir capturé une animation, plusieurs méthodes s’offrent à vous pour les relire:</span><span class="sxs-lookup"><span data-stu-id="e95fd-162">After you capture an animation, there are a few ways to replay it:</span></span>  

*   <span data-ttu-id="e95fd-163">Placez le pointeur de la souris sur la miniature dans le volet **vue d’ensemble** pour en afficher un aperçu.</span><span class="sxs-lookup"><span data-stu-id="e95fd-163">Hover over the thumbnail in the **Overview** pane to view a preview of it.</span></span>  
*   <span data-ttu-id="e95fd-164">Sélectionnez le groupe animation dans le volet **vue d’ensemble** \ (pour qu’il s’affiche dans le volet d' **informations** ), puis appuyez sur l’icône **relire** ![ ][ImageReplayButtonIcon] .</span><span class="sxs-lookup"><span data-stu-id="e95fd-164">Select the Animation Group from the **Overview** pane \(so that it is displayed in the **Details** pane\) and press the **replay** \(![replay icon][ImageReplayButtonIcon]\) icon.</span></span>  <span data-ttu-id="e95fd-165">L’animation est relues dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e95fd-165">The animation is replayed in the viewport.</span></span>  <span data-ttu-id="e95fd-166">Cliquez sur l’icône **Vitesse d’animation** \ (icônes de ![ Vitesse ][ImageAnimationSpeedButtonsIcon] d’animation \) pour modifier la vitesse d’aperçu du groupe d’animation actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e95fd-166">Click on the **animation speed** \(![animation speed icons][ImageAnimationSpeedButtonsIcon]\) icons to change the preview speed of the currently selected Animation Group.</span></span>  <span data-ttu-id="e95fd-167">Vous pouvez utiliser la barre verticale rouge pour modifier votre position actuelle.</span><span class="sxs-lookup"><span data-stu-id="e95fd-167">You may use the red vertical bar to change your current position.</span></span>  
*   <span data-ttu-id="e95fd-168">Cliquez et faites glisser la barre verticale rouge pour faire défiler l’animation d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e95fd-168">Click and drag the red vertical bar to scrub the viewport animation.</span></span>  
    
### <span data-ttu-id="e95fd-169">Afficher les détails d’une animation</span><span class="sxs-lookup"><span data-stu-id="e95fd-169">View animation details</span></span>  

<span data-ttu-id="e95fd-170">Une fois le groupe d’animations capturé, cliquez dessus dans le volet **vue d’ensemble** pour afficher les détails.</span><span class="sxs-lookup"><span data-stu-id="e95fd-170">After you capture an Animation Group, click on it from the **Overview** pane to view the details.</span></span>  <span data-ttu-id="e95fd-171">Dans le volet d' **informations** , chaque animation individuelle est affectée à une ligne.</span><span class="sxs-lookup"><span data-stu-id="e95fd-171">In the **Details** pane each individual animation is assigned the a row.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Détails sur le groupe d’animations" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="e95fd-173">Détails sur le groupe d’animations</span><span class="sxs-lookup"><span data-stu-id="e95fd-173">Animation Group details</span></span>  
:::image-end:::  

<span data-ttu-id="e95fd-174">Placez le pointeur sur une animation pour la mettre en surbrillance dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e95fd-174">Hover over an animation to highlight it in the viewport.</span></span>  <span data-ttu-id="e95fd-175">Cliquez sur l’animation pour la sélectionner dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="e95fd-175">Click on the animation to select it in the **Elements** panel.</span></span>  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Survol de l’animation pour la mettre en surbrillance dans la fenêtre d’affichage" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="e95fd-177">Survol de l’animation pour la mettre en surbrillance dans la fenêtre d’affichage</span><span class="sxs-lookup"><span data-stu-id="e95fd-177">Hover over the animation to highlight it in viewport</span></span>  
:::image-end:::  

<span data-ttu-id="e95fd-178">La section la plus à gauche d’une animation est la définition.</span><span class="sxs-lookup"><span data-stu-id="e95fd-178">The leftmost, darker section of an animation is the definition.</span></span>  <span data-ttu-id="e95fd-179">La section à droite, plus ternie représente des itérations.</span><span class="sxs-lookup"><span data-stu-id="e95fd-179">The right, more faded section represents iterations.</span></span>  <span data-ttu-id="e95fd-180">Par exemple, dans l’illustration suivante, les sections deux et trois représentent des itérations de la section One.</span><span class="sxs-lookup"><span data-stu-id="e95fd-180">For example, in the following figure, sections two and three represent iterations of section one.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Diagramme d’itérations d’animation" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   <span data-ttu-id="e95fd-182">Diagramme d’itérations d’animation</span><span class="sxs-lookup"><span data-stu-id="e95fd-182">Diagram of animation iterations</span></span>  
:::image-end:::  

<span data-ttu-id="e95fd-183">Si deux éléments ont la même animation appliquée, l’inspecteur d’animation affecte la même couleur aux éléments.</span><span class="sxs-lookup"><span data-stu-id="e95fd-183">If two elements have the same animation applied, the Animation Inspector assigns the same color to the elements.</span></span>  <span data-ttu-id="e95fd-184">La couleur est aléatoire et n’a aucune précision.</span><span class="sxs-lookup"><span data-stu-id="e95fd-184">The color is random and has no significance.</span></span>  <span data-ttu-id="e95fd-185">Par exemple, dans l’illustration suivante, les deux éléments `div.cwccw.earlier` et `div.cwccw.later` ont la même animation \ ( `spinrightleft` \) appliquée, comme les `div.ccwcw.earlier` éléments et `div.ccwcw.later` .</span><span class="sxs-lookup"><span data-stu-id="e95fd-185">For example, in the following figure, the two elements `div.cwccw.earlier` and `div.cwccw.later` have the same animation \(`spinrightleft`\) applied, as do the `div.ccwcw.earlier` and `div.ccwcw.later` elements.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Animations à code couleur" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   <span data-ttu-id="e95fd-187">Animations à code couleur</span><span class="sxs-lookup"><span data-stu-id="e95fd-187">Color-coded animations</span></span>  
:::image-end:::  

## <span data-ttu-id="e95fd-188">Modifier des animations</span><span class="sxs-lookup"><span data-stu-id="e95fd-188">Modify animations</span></span>   

<span data-ttu-id="e95fd-189">Il existe trois façons de modifier une animation à l’aide de l’inspecteur d’animation.</span><span class="sxs-lookup"><span data-stu-id="e95fd-189">There are three ways you are able to modify an animation with the Animation Inspector.</span></span>  

*   <span data-ttu-id="e95fd-190">Durée de l’animation.</span><span class="sxs-lookup"><span data-stu-id="e95fd-190">Animation duration.</span></span>  
*   <span data-ttu-id="e95fd-191">Minutage des images clés.</span><span class="sxs-lookup"><span data-stu-id="e95fd-191">Keyframe timings.</span></span>  
*   <span data-ttu-id="e95fd-192">Délai de début</span><span class="sxs-lookup"><span data-stu-id="e95fd-192">Start time delay.</span></span>  
    
<span data-ttu-id="e95fd-193">Dans l’illustration suivante, l’animation d’origine est représentée.</span><span class="sxs-lookup"><span data-stu-id="e95fd-193">In the following figure, the original animation is represented.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Animation d’origine avant modification" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   <span data-ttu-id="e95fd-195">Animation d’origine avant modification</span><span class="sxs-lookup"><span data-stu-id="e95fd-195">Original animation before modification</span></span>  
:::image-end:::  

<span data-ttu-id="e95fd-196">Pour modifier la durée d’une animation, cliquez sur le premier ou le dernier cercle et faites-le glisser.</span><span class="sxs-lookup"><span data-stu-id="e95fd-196">To change the duration of an animation, click and drag the first or last circle.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Durée modifiée" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   <span data-ttu-id="e95fd-198">Durée modifiée</span><span class="sxs-lookup"><span data-stu-id="e95fd-198">Modified duration</span></span>  
:::image-end:::  

<span data-ttu-id="e95fd-199">Si l’animation définit des règles d’images clés, celles-ci sont représentées sous forme de cercles intérieurs blancs.</span><span class="sxs-lookup"><span data-stu-id="e95fd-199">If the animation defines any keyframe rules, then these are represented as white inner circles.</span></span>  <span data-ttu-id="e95fd-200">Cliquez sur l’un des éléments suivants pour modifier le minutage de l’image clé.</span><span class="sxs-lookup"><span data-stu-id="e95fd-200">Click and drag one of these to change the timing of the keyframe.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Image clé modifiée" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   <span data-ttu-id="e95fd-202">Image clé modifiée</span><span class="sxs-lookup"><span data-stu-id="e95fd-202">Modified keyframe</span></span>  
:::image-end:::  

<span data-ttu-id="e95fd-203">Pour ajouter un délai à une animation, cliquez dessus et faites-la glisser n’importe où, à l’exception des cercles.</span><span class="sxs-lookup"><span data-stu-id="e95fd-203">To add a delay to an animation, click and drag it anywhere except the circles.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Retard modifié" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   <span data-ttu-id="e95fd-205">Retard modifié</span><span class="sxs-lookup"><span data-stu-id="e95fd-205">Modified delay</span></span>  
:::image-end:::  

<!--  
  


-->  

<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: ../media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: ../media/replay-button-icon.msft.png  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="e95fd-206">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e95fd-206">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e95fd-207">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="e95fd-207">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="e95fd-209">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e95fd-209">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
