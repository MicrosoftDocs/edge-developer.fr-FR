---
description: Inspectez et modifiez les animations à l’aide de l’inspecteur d’animation Microsoft Edge DevTools.
title: Inspecter les animations
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: dba948087ca06015f686d17ba48584199373805a
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439541"
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

# <a name="inspect-animations"></a><span data-ttu-id="f1ac3-104">Inspecter les animations</span><span class="sxs-lookup"><span data-stu-id="f1ac3-104">Inspect animations</span></span>  

<span data-ttu-id="f1ac3-105">Inspectez et modifiez les animations à l’aide de l’inspecteur d’animation Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-105">Inspect and modify animations with the Microsoft Edge DevTools Animation Inspector.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="inspecteur d’animation" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   <span data-ttu-id="f1ac3-107">inspecteur d’animation</span><span class="sxs-lookup"><span data-stu-id="f1ac3-107">animation inspector</span></span>  
:::image-end:::  

### <a name="summary"></a><span data-ttu-id="f1ac3-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="f1ac3-108">Summary</span></span>  

*   <span data-ttu-id="f1ac3-109">Capturez les animations en ouvrant l’Inspecteur d’animation.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-109">Capture animations by opening the Animation Inspector.</span></span>  <span data-ttu-id="f1ac3-110">L’Inspecteur d’animation détecte et trie automatiquement les animations en groupes.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-110">The Animation Inspector automatically detects and sorts animations into groups.</span></span>  
*   <span data-ttu-id="f1ac3-111">Inspectez les animations en ralentissant chacune d’elles, en relisant chacune d’elles ou en visualxant le code source.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-111">Inspect animations by slowing down each one, replaying each one, or viewing the source code.</span></span>  
*   <span data-ttu-id="f1ac3-112">Modifiez les animations en modifiant le minutage, le retard, la durée ou les décalages de l’image clé.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-112">Modify animations by changing the timing, delay, duration, or keyframe offsets.</span></span>  

## <a name="overview"></a><span data-ttu-id="f1ac3-113">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="f1ac3-113">Overview</span></span>  

<span data-ttu-id="f1ac3-114">L’inspecteur d’animation Microsoft Edge DevTools a deux objectifs principaux.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-114">The Microsoft Edge DevTools Animation Inspector has two main purposes.</span></span>  

*   <span data-ttu-id="f1ac3-115">Inspection des animations.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-115">Inspecting animations.</span></span>  <span data-ttu-id="f1ac3-116">Vous souhaitez ralentir, relire ou inspecter le code source d’un groupe d’animations.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-116">You want to slow down, replay, or inspect the source code for an Animation Group.</span></span>  
*   <span data-ttu-id="f1ac3-117">Modification des animations.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-117">Modifying animations.</span></span>  <span data-ttu-id="f1ac3-118">Vous souhaitez modifier le minutage, le délai, la durée ou les décalages d’images clés d’un groupe d’animations.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-118">You want to modify the timing, delay, duration, or keyframe offsets of an Animation Group.</span></span>  <span data-ttu-id="f1ac3-119">La modification de Bézier et la modification d’images clés ne sont actuellement pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-119">Bezier editing and keyframe editing are currently not supported.</span></span>  

<span data-ttu-id="f1ac3-120">L’Inspecteur d’animation prend en charge les animations CSS, les transitions CSS et les animations web.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-120">The Animation Inspector supports CSS animations, CSS transitions, and web animations.</span></span>  `requestAnimationFrame` <span data-ttu-id="f1ac3-121">les animations ne sont actuellement pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-121">animations are currently not supported.</span></span>  

### <a name="what-is-an-animation-group"></a><span data-ttu-id="f1ac3-122">Qu’est-ce qu’un groupe d’animations ?</span><span class="sxs-lookup"><span data-stu-id="f1ac3-122">What is an Animation Group?</span></span>  

<span data-ttu-id="f1ac3-123">Un groupe d’animations est un groupe d’animations qui peuvent être liées les unes aux autres.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-123">An Animation Group is a group of animations that may be related to each other.</span></span>  <span data-ttu-id="f1ac3-124">Pour l’instant, le web n’a pas de concept réel d’animation de groupe, de sorte que les concepteurs de mouvement et les développeurs doivent composer et timer des animations individuelles afin que les animations s’restituer comme un seul effet visuel cohérent.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-124">Currently, the web has no real concept of a group animation, so motion designers and developers have to compose and time individual animations so that the animations render as one coherent visual effect.</span></span>  <span data-ttu-id="f1ac3-125">L’Inspecteur d’animations prévoit les animations qui sont liées en fonction de l’heure de début \(à l’exclusion des retards, et ainsi de suite\).</span><span class="sxs-lookup"><span data-stu-id="f1ac3-125">The Animation Inspector predicts which animations are related based on start time \(excluding delays, and so on\).</span></span>  <span data-ttu-id="f1ac3-126">L’Inspecteur d’animations groupe également les animations côte à côte.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-126">The Animation Inspector also groups the animations side-by-side.</span></span>  
<span data-ttu-id="f1ac3-127">En d’autres termes, un ensemble d’animations qui sont toutes déclenchées dans le même bloc de scripts sont regroupées.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-127">In other words, a set of animations that are all triggered in the same script block are grouped together.</span></span>  <span data-ttu-id="f1ac3-128">Si une animation est asynchrone, elle est placée dans un groupe distinct.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-128">If an animation is asynchronous, it is placed in a separate group.</span></span>  

## <a name="get-started"></a><span data-ttu-id="f1ac3-129">Prise en main</span><span class="sxs-lookup"><span data-stu-id="f1ac3-129">Get started</span></span>  

<span data-ttu-id="f1ac3-130">Il existe deux façons d’ouvrir l’Inspecteur d’animation :</span><span class="sxs-lookup"><span data-stu-id="f1ac3-130">There are two ways to open the Animation Inspector:</span></span>  

*   <span data-ttu-id="f1ac3-131">Ouvrir le menu Personnaliser et contrôler **DevTools**</span><span class="sxs-lookup"><span data-stu-id="f1ac3-131">Open the **Customize and Control DevTools** menu</span></span>  
    1.  <span data-ttu-id="f1ac3-132">Accédez au **sous-menu Outils** Plus.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-132">Navigate to the **More tools** sub-menu.</span></span>  
    1.  <span data-ttu-id="f1ac3-133">Choisissez **animations**:</span><span class="sxs-lookup"><span data-stu-id="f1ac3-133">Choose **Animations**:</span></span>  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Animations à l’aide du menu principal" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           <span data-ttu-id="f1ac3-135">**Animations à l’aide** du menu principal</span><span class="sxs-lookup"><span data-stu-id="f1ac3-135">**Animations** using Main Menu</span></span>  
    :::image-end:::  
        
*   <span data-ttu-id="f1ac3-136">Ouvrir le **menu Commande**</span><span class="sxs-lookup"><span data-stu-id="f1ac3-136">Open the **Command Menu**</span></span>  
    1.  <span data-ttu-id="f1ac3-137">Entrez `Drawer: Show Animations`.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-137">Type `Drawer: Show Animations`.</span></span>  

<span data-ttu-id="f1ac3-138">L’Inspecteur d’animation s’ouvre à côté de **l’outil Console.**</span><span class="sxs-lookup"><span data-stu-id="f1ac3-138">The Animation Inspector opens next to the **Console** tool.</span></span>  <span data-ttu-id="f1ac3-139">Étant donné que l’Inspecteur d’animation est un outil DevTools, vous pouvez utiliser l’Inspecteur d’animation à partir de n’importe quel panneau DevTools.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-139">Since the Animation Inspector is a Drawer tool, you may use the Animation Inspector from any DevTools panel.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Inspecteur d’animation vide" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   <span data-ttu-id="f1ac3-141">Inspecteur d’animation vide</span><span class="sxs-lookup"><span data-stu-id="f1ac3-141">Empty Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="f1ac3-142">L’Inspecteur d’animation est regroupé en quatre sections principales \(ou volets\).</span><span class="sxs-lookup"><span data-stu-id="f1ac3-142">The Animation Inspector is grouped into four main sections \(or panes\).</span></span>  <span data-ttu-id="f1ac3-143">Ce guide fait référence à chaque volet comme suit :</span><span class="sxs-lookup"><span data-stu-id="f1ac3-143">This guide refers to each pane as follows:</span></span>  

| <span data-ttu-id="f1ac3-144">Index</span><span class="sxs-lookup"><span data-stu-id="f1ac3-144">Index</span></span> | <span data-ttu-id="f1ac3-145">Volet</span><span class="sxs-lookup"><span data-stu-id="f1ac3-145">Pane</span></span> | <span data-ttu-id="f1ac3-146">Description</span><span class="sxs-lookup"><span data-stu-id="f1ac3-146">Description</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="f1ac3-147">1</span><span class="sxs-lookup"><span data-stu-id="f1ac3-147">1</span></span> | **<span data-ttu-id="f1ac3-148">Contrôles</span><span class="sxs-lookup"><span data-stu-id="f1ac3-148">Controls</span></span>** | <span data-ttu-id="f1ac3-149">À partir de là, vous pouvez effacer tous les groupes d’animations actuellement capturés ou modifier la vitesse du groupe d’animations actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-149">From here you may clear all currently captured Animation Groups, or change the speed of the currently selected Animation Group.</span></span> |  
| <span data-ttu-id="f1ac3-150">2</span><span class="sxs-lookup"><span data-stu-id="f1ac3-150">2</span></span> | **<span data-ttu-id="f1ac3-151">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="f1ac3-151">Overview</span></span>** | <span data-ttu-id="f1ac3-152">Choisissez un groupe d’animations ici pour l’inspecter et le modifier dans le **volet d’informations.**</span><span class="sxs-lookup"><span data-stu-id="f1ac3-152">Choose an Animation Group here to inspect and modify it in the **Details** pane.</span></span> |  
| <span data-ttu-id="f1ac3-153">3</span><span class="sxs-lookup"><span data-stu-id="f1ac3-153">3</span></span> | **<span data-ttu-id="f1ac3-154">Chronologie</span><span class="sxs-lookup"><span data-stu-id="f1ac3-154">Timeline</span></span>** | <span data-ttu-id="f1ac3-155">Suspendez et démarrez une animation à partir d’ici, ou faites un saut vers un point spécifique de l’animation.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-155">Pause and start an animation from here, or jump to a specific point in the animation.</span></span> |  
| <span data-ttu-id="f1ac3-156">4</span><span class="sxs-lookup"><span data-stu-id="f1ac3-156">4</span></span> | **<span data-ttu-id="f1ac3-157">Détails</span><span class="sxs-lookup"><span data-stu-id="f1ac3-157">Details</span></span>** | <span data-ttu-id="f1ac3-158">Inspectez et modifiez le groupe d’animations actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-158">Inspect and modify the currently selected Animation Group.</span></span> |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Inspecteur d’animation annotée" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   <span data-ttu-id="f1ac3-160">Inspecteur d’animation annotée</span><span class="sxs-lookup"><span data-stu-id="f1ac3-160">Annotated Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="f1ac3-161">Pour capturer une animation, il vous suffit d’effectuer l’interaction qui déclenche l’animation lorsque l’Inspecteur d’animation est ouvert.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-161">To capture an animation, just perform the interaction that triggers the animation while the Animation Inspector is open.</span></span>  <span data-ttu-id="f1ac3-162">Si une animation est déclenchée lors du chargement de la page, actualisez la page avec l’Inspecteur d’animation ouvert pour détecter l’animation.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-162">If an animation is triggered on page load, refresh the page with the Animation Inspector open to detect the animation.</span></span>  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <a name="inspect-animations"></a><span data-ttu-id="f1ac3-163">Inspecter les animations</span><span class="sxs-lookup"><span data-stu-id="f1ac3-163">Inspect animations</span></span>  

<span data-ttu-id="f1ac3-164">Une fois que vous avez capturé une animation, vous pouvez la relire de plusieurs façons :</span><span class="sxs-lookup"><span data-stu-id="f1ac3-164">After you capture an animation, there are a few ways to replay it:</span></span>  

*   <span data-ttu-id="f1ac3-165">Pointez sur la miniature dans **le** volet Vue d’ensemble pour en afficher un aperçu.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-165">Hover on the thumbnail in the **Overview** pane to view a preview of it.</span></span>  
*   <span data-ttu-id="f1ac3-166">Choisissez le groupe  d’animations dans le volet Vue  d’ensemble \(afin qu’il s’affiche dans le volet d’informations\) et choisissez l’icône relecture **\(** icône de relecture ![ ](../media/replay-button-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="f1ac3-166">Choose the Animation Group from the **Overview** pane \(so that it is displayed in the **Details** pane\) and choose the **replay** \(![replay icon](../media/replay-button-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="f1ac3-167">L’animation est relecture dans la vue.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-167">The animation is replayed in the viewport.</span></span>  <span data-ttu-id="f1ac3-168">Choisissez les **icônes de vitesse d’animation** \( icônes de vitesse d’animation \) pour modifier la vitesse d’aperçu du groupe d’animations ![ actuellement ](../media/animation-speed-buttons-icon.msft.png) sélectionné.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-168">Choose the **animation speed** \(![animation speed icons](../media/animation-speed-buttons-icon.msft.png)\) icons to change the preview speed of the currently selected Animation Group.</span></span>  <span data-ttu-id="f1ac3-169">Vous pouvez utiliser la barre verticale rouge pour modifier votre position actuelle.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-169">You may use the red vertical bar to change your current position.</span></span>  
*   <span data-ttu-id="f1ac3-170">Choisissez et faites glisser la barre verticale rouge pour nettoyer l’animation de laport d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-170">Choose and drag the red vertical bar to scrub the viewport animation.</span></span>  
    
### <a name="view-animation-details"></a><span data-ttu-id="f1ac3-171">Afficher les détails de l’animation</span><span class="sxs-lookup"><span data-stu-id="f1ac3-171">View animation details</span></span>  

<span data-ttu-id="f1ac3-172">Après avoir capturé un groupe d’animations, choisissez-le dans le volet Vue d’ensemble pour afficher les détails. </span><span class="sxs-lookup"><span data-stu-id="f1ac3-172">After you capture an Animation Group, choose on it from the **Overview** pane to view the details.</span></span>  <span data-ttu-id="f1ac3-173">Dans le **volet Détails,** chaque animation individuelle est affectée à une ligne.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-173">In the **Details** pane each individual animation is assigned the a row.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Détails du groupe d’animations" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="f1ac3-175">Détails du groupe d’animations</span><span class="sxs-lookup"><span data-stu-id="f1ac3-175">Animation Group details</span></span>  
:::image-end:::  

<span data-ttu-id="f1ac3-176">Pointez sur une animation pour la surligner dans la vue.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-176">Hover on an animation to highlight it in the viewport.</span></span>  <span data-ttu-id="f1ac3-177">Choisissez l’animation pour la sélectionner dans **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="f1ac3-177">Choose the animation to select it in the **Elements** tool.</span></span>  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Pointer sur l’animation pour la surligner dans la vue" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="f1ac3-179">Pointer sur l’animation pour la surligner dans la vue</span><span class="sxs-lookup"><span data-stu-id="f1ac3-179">Hover on the animation to highlight it in viewport</span></span>  
:::image-end:::  

<span data-ttu-id="f1ac3-180">La section la plus sombre et la plus à gauche d’une animation est la définition.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-180">The leftmost, darker section of an animation is the definition.</span></span>  <span data-ttu-id="f1ac3-181">La section droite, plus fondue, représente des itérations.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-181">The right, more faded section represents iterations.</span></span>  <span data-ttu-id="f1ac3-182">Par exemple, dans la figure suivante, les sections 2 et 3 représentent les itérations de la première section.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-182">For example, in the following figure, sections two and three represent iterations of section one.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Diagramme des itérations d’animation" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   <span data-ttu-id="f1ac3-184">Diagramme des itérations d’animation</span><span class="sxs-lookup"><span data-stu-id="f1ac3-184">Diagram of animation iterations</span></span>  
:::image-end:::  

<span data-ttu-id="f1ac3-185">Si deux éléments ont la même animation appliquée, l’Inspecteur d’animation affecte la même couleur aux éléments.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-185">If two elements have the same animation applied, the Animation Inspector assigns the same color to the elements.</span></span>  <span data-ttu-id="f1ac3-186">La couleur est aléatoire et n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-186">The color is random and has no significance.</span></span>  <span data-ttu-id="f1ac3-187">Par exemple, dans la figure suivante, les deux éléments ont la même `div.cwccw.earlier` `div.cwccw.later` animation \( \) appliquée, tout comme les `spinrightleft` `div.ccwcw.earlier` éléments et les `div.ccwcw.later` éléments.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-187">For example, in the following figure, the two elements `div.cwccw.earlier` and `div.cwccw.later` have the same animation \(`spinrightleft`\) applied, as do the `div.ccwcw.earlier` and `div.ccwcw.later` elements.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Animations codées en couleur" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   <span data-ttu-id="f1ac3-189">Animations codées en couleur</span><span class="sxs-lookup"><span data-stu-id="f1ac3-189">Color-coded animations</span></span>  
:::image-end:::  

## <a name="modify-animations"></a><span data-ttu-id="f1ac3-190">Modifier les animations</span><span class="sxs-lookup"><span data-stu-id="f1ac3-190">Modify animations</span></span>  

<span data-ttu-id="f1ac3-191">Il existe trois façons de modifier une animation avec l’Inspecteur d’animation.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-191">There are three ways you are able to modify an animation with the Animation Inspector.</span></span>  

*   <span data-ttu-id="f1ac3-192">Durée de l’animation.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-192">Animation duration.</span></span>  
*   <span data-ttu-id="f1ac3-193">Minutage des images clés.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-193">Keyframe timings.</span></span>  
*   <span data-ttu-id="f1ac3-194">Délai de début.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-194">Start time delay.</span></span>  
    
<span data-ttu-id="f1ac3-195">Dans la figure suivante, l’animation d’origine est représentée.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-195">In the following figure, the original animation is represented.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Animation d’origine avant modification" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   <span data-ttu-id="f1ac3-197">Animation d’origine avant modification</span><span class="sxs-lookup"><span data-stu-id="f1ac3-197">Original animation before modification</span></span>  
:::image-end:::  

<span data-ttu-id="f1ac3-198">Pour modifier la durée d’une animation, choisissez et faites glisser le premier ou le dernier cercle.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-198">To change the duration of an animation, choose and drag the first or last circle.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Durée modifiée" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   <span data-ttu-id="f1ac3-200">Durée modifiée</span><span class="sxs-lookup"><span data-stu-id="f1ac3-200">Modified duration</span></span>  
:::image-end:::  

<span data-ttu-id="f1ac3-201">Si l’animation définit des règles d’image clé, celles-ci sont représentées en tant que cercles internes blancs.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-201">If the animation defines any keyframe rules, then these are represented as white inner circles.</span></span>  <span data-ttu-id="f1ac3-202">Choisissez et faites glisser l’une d’entre elles pour modifier le minutage de l’images clés.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-202">Choose and drag one of these to change the timing of the keyframe.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Images clés modifiées" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   <span data-ttu-id="f1ac3-204">Images clés modifiées</span><span class="sxs-lookup"><span data-stu-id="f1ac3-204">Modified keyframe</span></span>  
:::image-end:::  

<span data-ttu-id="f1ac3-205">Pour ajouter un délai à une animation, choisissez-la et faites-la glisser n’importe où à l’exception des cercles.</span><span class="sxs-lookup"><span data-stu-id="f1ac3-205">To add a delay to an animation, choose and drag it anywhere except the circles.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Retard modifié" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   <span data-ttu-id="f1ac3-207">Retard modifié</span><span class="sxs-lookup"><span data-stu-id="f1ac3-207">Modified delay</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f1ac3-208">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="f1ac3-208">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

<span data-ttu-id="f1ac3-209">(.. /media/animation-speed-buttons-icon.msft.png) : .. /media/animation-speed-buttons-icon.msft.png</span><span class="sxs-lookup"><span data-stu-id="f1ac3-209">(../media/animation-speed-buttons-icon.msft.png): ../media/animation-speed-buttons-icon.msft.png</span></span>  
<span data-ttu-id="f1ac3-210">(.. /media/replay-button-icon.msft.png) : .. /media/replay-button-icon.msft.png</span><span class="sxs-lookup"><span data-stu-id="f1ac3-210">(../media/replay-button-icon.msft.png): ../media/replay-button-icon.msft.png</span></span>  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="f1ac3-211">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f1ac3-211">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f1ac3-212">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="f1ac3-212">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="f1ac3-214">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f1ac3-214">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
