---
title: Inspecter des animations
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 6466c7f0e1f8680a2429b565e8022d152d05d733
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566210"
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





# <span data-ttu-id="e3093-103">Inspecter des animations</span><span class="sxs-lookup"><span data-stu-id="e3093-103">Inspect animations</span></span>   



<span data-ttu-id="e3093-104">Examinez et modifiez des animations avec l’inspecteur d’animation Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="e3093-104">Inspect and modify animations with the Microsoft Edge DevTools Animation Inspector.</span></span>  

> ##### <span data-ttu-id="e3093-105">Figure1</span><span class="sxs-lookup"><span data-stu-id="e3093-105">Figure 1</span></span>  
> <span data-ttu-id="e3093-106">Inspecteur d’animation</span><span class="sxs-lookup"><span data-stu-id="e3093-106">Animation inspector</span></span>  
> ![inspecteur d’animation][ImageAnimationInspector]  

### <span data-ttu-id="e3093-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="e3093-108">Summary</span></span>  

*   <span data-ttu-id="e3093-109">Capturez des animations en ouvrant l’inspecteur d’animation.</span><span class="sxs-lookup"><span data-stu-id="e3093-109">Capture animations by opening the Animation Inspector.</span></span>  <span data-ttu-id="e3093-110">L’inspecteur d’animation détecte et trie automatiquement les animations au sein de groupes.</span><span class="sxs-lookup"><span data-stu-id="e3093-110">The Animation Inspector automatically detects and sorts animations into groups.</span></span>  
*   <span data-ttu-id="e3093-111">Examinez les animations en ralentissant chacune d’elles, en reproduisant chacune d’elles ou en consultant le code source.</span><span class="sxs-lookup"><span data-stu-id="e3093-111">Inspect animations by slowing down each one, replaying each one, or viewing the source code.</span></span>  
*   <span data-ttu-id="e3093-112">Modifiez des animations en modifiant le minutage, le délai, la durée ou les décalages d’images clés.</span><span class="sxs-lookup"><span data-stu-id="e3093-112">Modify animations by changing the timing, delay, duration, or keyframe offsets.</span></span>  

## <span data-ttu-id="e3093-113">Présentation</span><span class="sxs-lookup"><span data-stu-id="e3093-113">Overview</span></span>   

<span data-ttu-id="e3093-114">L’inspecteur d’animation Microsoft Edge DevTools possède deux objectifs principaux.</span><span class="sxs-lookup"><span data-stu-id="e3093-114">The Microsoft Edge DevTools Animation Inspector has two main purposes.</span></span>  

*   <span data-ttu-id="e3093-115">Examen des animations.</span><span class="sxs-lookup"><span data-stu-id="e3093-115">Inspecting animations.</span></span>  <span data-ttu-id="e3093-116">Vous voulez ralentir, relire ou inspecter le code source d’un groupe d’animations.</span><span class="sxs-lookup"><span data-stu-id="e3093-116">You want to slow down, replay, or inspect the source code for an Animation Group.</span></span>  
*   <span data-ttu-id="e3093-117">Modification des animations.</span><span class="sxs-lookup"><span data-stu-id="e3093-117">Modifying animations.</span></span>  <span data-ttu-id="e3093-118">Vous souhaitez modifier les décalements minutage, délai, durée et image clé d’un groupe d’animations.</span><span class="sxs-lookup"><span data-stu-id="e3093-118">You want to modify the timing, delay, duration, or keyframe offsets of an Animation Group.</span></span>  <span data-ttu-id="e3093-119">La modification Bézier et la modification des images clés ne sont actuellement pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e3093-119">Bezier editing and keyframe editing are currently not supported.</span></span>  

<span data-ttu-id="e3093-120">L’inspecteur d’animation prend en charge des animations CSS, des transitions CSS et des animations Web.</span><span class="sxs-lookup"><span data-stu-id="e3093-120">The Animation Inspector supports CSS animations, CSS transitions, and web animations.</span></span>  `requestAnimationFrame` <span data-ttu-id="e3093-121">les animations ne sont actuellement pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e3093-121">animations are currently not supported.</span></span>  

### <span data-ttu-id="e3093-122">Qu’est-ce qu’un groupe d’animations?</span><span class="sxs-lookup"><span data-stu-id="e3093-122">What is an Animation Group?</span></span>  

<span data-ttu-id="e3093-123">Un groupe d’animations est un groupe d’animations qui peut être lié les uns aux autres.</span><span class="sxs-lookup"><span data-stu-id="e3093-123">An Animation Group is a group of animations that may be related to each other.</span></span>  <span data-ttu-id="e3093-124">Pour l’instant, le Web n’ayant pas de véritable concept d’animation de groupe, les concepteurs de trajectoire et les développeurs doivent donc composer et temps des animations individuelles pour que les animations s’affichent comme un effet visuel cohérent.</span><span class="sxs-lookup"><span data-stu-id="e3093-124">Currently, the web has no real concept of a group animation, so motion designers and developers have to compose and time individual animations so that the animations render as one coherent visual effect.</span></span>  <span data-ttu-id="e3093-125">L’inspecteur d’animation prédit quelles animations sont liées en fonction de l’heure de début (sauf retards, etc.).</span><span class="sxs-lookup"><span data-stu-id="e3093-125">The Animation Inspector predicts which animations are related based on start time \(excluding delays, and so on\).</span></span>  <span data-ttu-id="e3093-126">L’inspecteur d’animation regroupe également les animations côte à côte.</span><span class="sxs-lookup"><span data-stu-id="e3093-126">The Animation Inspector also groups the animations side-by-side.</span></span>  
<span data-ttu-id="e3093-127">En d’autres termes, un ensemble d’animations déclenchées dans le même bloc de script est regroupé.</span><span class="sxs-lookup"><span data-stu-id="e3093-127">In other words, a set of animations that are all triggered in the same script block are grouped together.</span></span>  <span data-ttu-id="e3093-128">S’il s’agit d’une animation asynchrone, elle est placée dans un groupe séparé.</span><span class="sxs-lookup"><span data-stu-id="e3093-128">If an animation is asynchronous, it is placed in a separate group.</span></span>  

## <span data-ttu-id="e3093-129">Prise en main</span><span class="sxs-lookup"><span data-stu-id="e3093-129">Get started</span></span>  

<span data-ttu-id="e3093-130">Il existe deux façons d’ouvrir l’inspecteur d’animation:</span><span class="sxs-lookup"><span data-stu-id="e3093-130">There are two ways to open the Animation Inspector:</span></span>  

*   <span data-ttu-id="e3093-131">Ouvrir le menu **personnaliser et contrôler devtools**</span><span class="sxs-lookup"><span data-stu-id="e3093-131">Open the **Customize and Control DevTools** menu</span></span>  
    1.  <span data-ttu-id="e3093-132">Accédez au sous-menu **plus d’outils** .</span><span class="sxs-lookup"><span data-stu-id="e3093-132">Navigate to the **More tools** sub-menu.</span></span>  
    1.  <span data-ttu-id="e3093-133">Sélectionnez **animations**:</span><span class="sxs-lookup"><span data-stu-id="e3093-133">Select **Animations**:</span></span>  
        
        > ##### <span data-ttu-id="e3093-134">Figure 2</span><span class="sxs-lookup"><span data-stu-id="e3093-134">Figure 2</span></span>  
        > <span data-ttu-id="e3093-135">Animations via le menu principal</span><span class="sxs-lookup"><span data-stu-id="e3093-135">Animations via Main Menu</span></span>  
        > ![Animations via le menu principal][ImageAnimationsViaMainMenu]  
        
*   <span data-ttu-id="e3093-137">Ouvrir le **menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="e3093-137">Open the **Command Menu**</span></span>  
    1.  <span data-ttu-id="e3093-138">Entrez `Drawer: Show Animations`.</span><span class="sxs-lookup"><span data-stu-id="e3093-138">Type `Drawer: Show Animations`.</span></span>  

<span data-ttu-id="e3093-139">L’inspecteur d’animation s’ouvre en tant qu’onglet en regard du tiroir de la console.</span><span class="sxs-lookup"><span data-stu-id="e3093-139">The Animation Inspector opens up as a tab next to the Console Drawer.</span></span>  <span data-ttu-id="e3093-140">Dans la mesure où l’inspecteur d’animation est l’onglet tiroir, vous pouvez utiliser l’inspecteur d’animation de n’importe quel panneau DevTools.</span><span class="sxs-lookup"><span data-stu-id="e3093-140">Since the Animation Inspector is a Drawer tab, you may use the Animation Inspector from any DevTools panel.</span></span>  

> ##### <span data-ttu-id="e3093-141">Figure3</span><span class="sxs-lookup"><span data-stu-id="e3093-141">Figure 3</span></span>  
> <span data-ttu-id="e3093-142">Inspecteur d’animation vide</span><span class="sxs-lookup"><span data-stu-id="e3093-142">Empty Animation Inspector</span></span>  
> ![Inspecteur d’animation vide][ImageEmptyAnimationInspector]  

<span data-ttu-id="e3093-144">L’inspecteur d’animation est groupé en quatre sections principales \ (ou volets \).</span><span class="sxs-lookup"><span data-stu-id="e3093-144">The Animation Inspector is grouped into four main sections \(or panes\).</span></span>  <span data-ttu-id="e3093-145">Ce guide fait référence à chaque volet comme suit:</span><span class="sxs-lookup"><span data-stu-id="e3093-145">This guide refers to each pane as follows:</span></span>  

| | <span data-ttu-id="e3093-146">Volet</span><span class="sxs-lookup"><span data-stu-id="e3093-146">Pane</span></span> | <span data-ttu-id="e3093-147">Description</span><span class="sxs-lookup"><span data-stu-id="e3093-147">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="e3093-148">1</span><span class="sxs-lookup"><span data-stu-id="e3093-148">1</span></span> | **<span data-ttu-id="e3093-149">Contrôles</span><span class="sxs-lookup"><span data-stu-id="e3093-149">Controls</span></span>** | <span data-ttu-id="e3093-150">Vous pouvez alors effacer tous les groupes d’animations actuellement capturées ou changer la vitesse du groupe d’animation actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e3093-150">From here you may clear all currently captured Animation Groups, or change the speed of the currently selected Animation Group.</span></span> |  
| <span data-ttu-id="e3093-151">deuxième</span><span class="sxs-lookup"><span data-stu-id="e3093-151">2</span></span> | **<span data-ttu-id="e3093-152">Présentation</span><span class="sxs-lookup"><span data-stu-id="e3093-152">Overview</span></span>** | <span data-ttu-id="e3093-153">Sélectionnez un groupe d’animations pour l’inspecter et le modifier dans le volet **Détails** .</span><span class="sxs-lookup"><span data-stu-id="e3093-153">Select an Animation Group here to inspect and modify it in the **Details** pane.</span></span> |  
| <span data-ttu-id="e3093-154">3D</span><span class="sxs-lookup"><span data-stu-id="e3093-154">3</span></span> | **<span data-ttu-id="e3093-155">Chronologie</span><span class="sxs-lookup"><span data-stu-id="e3093-155">Timeline</span></span>** | <span data-ttu-id="e3093-156">Interrompez et démarrez une animation à partir de cet emplacement, ou accédez à un point spécifique de l’animation.</span><span class="sxs-lookup"><span data-stu-id="e3093-156">Pause and start an animation from here, or jump to a specific point in the animation.</span></span> |  
| <span data-ttu-id="e3093-157">n°4</span><span class="sxs-lookup"><span data-stu-id="e3093-157">4</span></span> | **<span data-ttu-id="e3093-158">Détails</span><span class="sxs-lookup"><span data-stu-id="e3093-158">Details</span></span>** | <span data-ttu-id="e3093-159">Inspecter et modifier le groupe d’animations actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e3093-159">Inspect and modify the currently selected Animation Group.</span></span> |  

> ##### <span data-ttu-id="e3093-160">Figure 4</span><span class="sxs-lookup"><span data-stu-id="e3093-160">Figure 4</span></span>  
> <span data-ttu-id="e3093-161">Inspecteur d’animation annoté</span><span class="sxs-lookup"><span data-stu-id="e3093-161">Annotated Animation Inspector</span></span>  
> ![Inspecteur d’animation annoté][ImageAnnotatedAnimationInspector]  

<span data-ttu-id="e3093-163">Pour capturer une animation, il vous suffit d’effectuer l’interaction déclenchant l’animation lorsque l’inspecteur d’animation est ouvert.</span><span class="sxs-lookup"><span data-stu-id="e3093-163">To capture an animation, just perform the interaction that triggers the animation while the Animation Inspector is open.</span></span>  <span data-ttu-id="e3093-164">Si une animation est déclenchée lors du chargement de la page, rechargez la page avec l’inspecteur d’animation ouvert pour détecter l’animation.</span><span class="sxs-lookup"><span data-stu-id="e3093-164">If an animation is triggered on page load, reload the page with the Animation Inspector open to detect the animation.</span></span>  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <span data-ttu-id="e3093-165">Inspecter des animations</span><span class="sxs-lookup"><span data-stu-id="e3093-165">Inspect animations</span></span>   

<span data-ttu-id="e3093-166">Après avoir capturé une animation, plusieurs méthodes s’offrent à vous pour les relire:</span><span class="sxs-lookup"><span data-stu-id="e3093-166">After you capture an animation, there are a few ways to replay it:</span></span>  

*   <span data-ttu-id="e3093-167">Placez le pointeur de la souris sur la miniature dans le volet **vue d’ensemble** pour en afficher un aperçu.</span><span class="sxs-lookup"><span data-stu-id="e3093-167">Hover over the thumbnail in the **Overview** pane to view a preview of it.</span></span>  
*   <span data-ttu-id="e3093-168">Sélectionnez le groupe animation dans le volet **vue d’ensemble** \ (pour qu’il s’affiche dans le volet d' **informations** ), puis appuyez sur l’icône **réexécuter** l' ![ icône de lecture ][ImageReplayButtonIcon] .</span><span class="sxs-lookup"><span data-stu-id="e3093-168">Select the Animation Group from the **Overview** pane \(so that it is displayed in the **Details** pane\) and press the **replay** ![replay icon][ImageReplayButtonIcon] icon.</span></span>  <span data-ttu-id="e3093-169">L’animation est relues dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e3093-169">The animation is replayed in the viewport.</span></span>  <span data-ttu-id="e3093-170">Cliquez sur l’icône de vitesse de l' **animation vitesse d'** animation ![ ][ImageAnimationSpeedButtonsIcon] pour modifier la vitesse d’aperçu du groupe d’animation actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e3093-170">Click on the **animation speed** ![animation speed icons][ImageAnimationSpeedButtonsIcon] icons to change the preview speed of the currently selected Animation Group.</span></span>  <span data-ttu-id="e3093-171">Vous pouvez utiliser la barre verticale rouge pour modifier votre position actuelle.</span><span class="sxs-lookup"><span data-stu-id="e3093-171">You may use the red vertical bar to change your current position.</span></span>  
*   <span data-ttu-id="e3093-172">Cliquez et faites glisser la barre verticale rouge pour faire défiler l’animation d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e3093-172">Click and drag the red vertical bar to scrub the viewport animation.</span></span>  

### <span data-ttu-id="e3093-173">Afficher les détails d’une animation</span><span class="sxs-lookup"><span data-stu-id="e3093-173">View animation details</span></span>  

<span data-ttu-id="e3093-174">Une fois le groupe d’animations capturé, cliquez dessus dans le volet **vue d’ensemble** pour afficher les détails.</span><span class="sxs-lookup"><span data-stu-id="e3093-174">After you capture an Animation Group, click on it from the **Overview** pane to view the details.</span></span>  <span data-ttu-id="e3093-175">Dans le volet d' **informations** , chaque animation individuelle est affectée à une ligne.</span><span class="sxs-lookup"><span data-stu-id="e3093-175">In the **Details** pane each individual animation is assigned the a row.</span></span>  

> ##### <span data-ttu-id="e3093-176">Figure 5</span><span class="sxs-lookup"><span data-stu-id="e3093-176">Figure 5</span></span>  
> <span data-ttu-id="e3093-177">Détails sur le groupe d’animations</span><span class="sxs-lookup"><span data-stu-id="e3093-177">Animation Group details</span></span>  
> ![Détails sur le groupe d’animations][ImageAnimationGroupDetails]  

<span data-ttu-id="e3093-179">Placez le pointeur sur une animation pour la mettre en surbrillance dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e3093-179">Hover over an animation to highlight it in the viewport.</span></span>  <span data-ttu-id="e3093-180">Cliquez sur l’animation pour la sélectionner dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="e3093-180">Click on the animation to select it in the **Elements** panel.</span></span>  

> ##### <span data-ttu-id="e3093-181">Figure 6</span><span class="sxs-lookup"><span data-stu-id="e3093-181">Figure 6</span></span>  
> <span data-ttu-id="e3093-182">Survol de l’animation pour la mettre en surbrillance dans la fenêtre d’affichage</span><span class="sxs-lookup"><span data-stu-id="e3093-182">Hover over the animation to highlight it in viewport</span></span>  
> ![Survol de l’animation pour la mettre en surbrillance dans la fenêtre d’affichage][ImageHoverOverAnimationHighlightViewport]  

<span data-ttu-id="e3093-184">La section la plus à gauche d’une animation est la définition.</span><span class="sxs-lookup"><span data-stu-id="e3093-184">The leftmost, darker section of an animation is the definition.</span></span>  <span data-ttu-id="e3093-185">La section à droite, plus ternie représente des itérations.</span><span class="sxs-lookup"><span data-stu-id="e3093-185">The right, more faded section represents iterations.</span></span>  <span data-ttu-id="e3093-186">Par exemple, dans la [figure 7](#figure-7), les sections deux et trois représentent des itérations de la section One.</span><span class="sxs-lookup"><span data-stu-id="e3093-186">For example, in [Figure 7](#figure-7), sections two and three represent iterations of section one.</span></span>  

> ##### <span data-ttu-id="e3093-187">Figure 7</span><span class="sxs-lookup"><span data-stu-id="e3093-187">Figure 7</span></span>  
> <span data-ttu-id="e3093-188">Diagramme d’itérations d’animation</span><span class="sxs-lookup"><span data-stu-id="e3093-188">Diagram of animation iterations</span></span>  
> ![Diagramme d’itérations d’animation][ImageDiagramAnimationIterations]  

<span data-ttu-id="e3093-190">Si deux éléments ont la même animation appliquée, l’inspecteur d’animation affecte la même couleur aux éléments.</span><span class="sxs-lookup"><span data-stu-id="e3093-190">If two elements have the same animation applied, the Animation Inspector assigns the same color to the elements.</span></span>  <span data-ttu-id="e3093-191">La couleur est aléatoire et n’a aucune précision.</span><span class="sxs-lookup"><span data-stu-id="e3093-191">The color is random and has no significance.</span></span>  <span data-ttu-id="e3093-192">Par exemple, dans [figure 8](#figure-8) les deux éléments `div.cwccw.earlier` et `div.cwccw.later` ont la même animation \ ( `spinrightleft` \) appliquée, comme les `div.ccwcw.earlier` éléments et `div.ccwcw.later` .</span><span class="sxs-lookup"><span data-stu-id="e3093-192">For example, in [Figure 8](#figure-8) the two elements `div.cwccw.earlier` and `div.cwccw.later` have the same animation \(`spinrightleft`\) applied, as do the `div.ccwcw.earlier` and `div.ccwcw.later` elements.</span></span>  

> ##### <span data-ttu-id="e3093-193">Figure8</span><span class="sxs-lookup"><span data-stu-id="e3093-193">Figure 8</span></span>  
> <span data-ttu-id="e3093-194">Animations à code couleur</span><span class="sxs-lookup"><span data-stu-id="e3093-194">Color-coded animations</span></span>  
> ![Animations à code couleur][ImageColorCodedAnimations]  

## <span data-ttu-id="e3093-196">Modifier des animations</span><span class="sxs-lookup"><span data-stu-id="e3093-196">Modify animations</span></span>   

<span data-ttu-id="e3093-197">Il existe trois façons de modifier une animation à l’aide de l’inspecteur d’animation:</span><span class="sxs-lookup"><span data-stu-id="e3093-197">There are three ways you are able to modify an animation with the Animation Inspector:</span></span>  

*   <span data-ttu-id="e3093-198">Durée de l’animation.</span><span class="sxs-lookup"><span data-stu-id="e3093-198">Animation duration.</span></span>  
*   <span data-ttu-id="e3093-199">Minutage des images clés.</span><span class="sxs-lookup"><span data-stu-id="e3093-199">Keyframe timings.</span></span>  
*   <span data-ttu-id="e3093-200">Délai de début</span><span class="sxs-lookup"><span data-stu-id="e3093-200">Start time delay.</span></span>  

<span data-ttu-id="e3093-201">Pour cette section, supposez que la [figure 9](#figure-9) représente l’animation d’origine:</span><span class="sxs-lookup"><span data-stu-id="e3093-201">For this section suppose that [Figure 9](#figure-9) represents the original animation:</span></span>  

> ##### <span data-ttu-id="e3093-202">Figure9</span><span class="sxs-lookup"><span data-stu-id="e3093-202">Figure 9</span></span>  
> <span data-ttu-id="e3093-203">Animation d’origine avant modification</span><span class="sxs-lookup"><span data-stu-id="e3093-203">Original animation before modification</span></span>  
> ![Animation d’origine avant modification][ImageOriginalAnimationBeforeModification]  

<span data-ttu-id="e3093-205">Pour modifier la durée d’une animation, cliquez sur le premier ou le dernier cercle et faites-le glisser.</span><span class="sxs-lookup"><span data-stu-id="e3093-205">To change the duration of an animation, click and drag the first or last circle.</span></span>  

> ##### <span data-ttu-id="e3093-206">Figure10</span><span class="sxs-lookup"><span data-stu-id="e3093-206">Figure 10</span></span>  
> <span data-ttu-id="e3093-207">Durée modifiée</span><span class="sxs-lookup"><span data-stu-id="e3093-207">Modified duration</span></span>  
> ![Durée modifiée][ImageModifiedDuration]  

<span data-ttu-id="e3093-209">Si l’animation définit des règles d’images clés, celles-ci sont représentées sous forme de cercles intérieurs blancs.</span><span class="sxs-lookup"><span data-stu-id="e3093-209">If the animation defines any keyframe rules, then these are represented as white inner circles.</span></span>  <span data-ttu-id="e3093-210">Cliquez sur l’un des éléments suivants pour modifier le minutage de l’image clé.</span><span class="sxs-lookup"><span data-stu-id="e3093-210">Click and drag one of these to change the timing of the keyframe.</span></span>  

> ##### <span data-ttu-id="e3093-211">Figure11</span><span class="sxs-lookup"><span data-stu-id="e3093-211">Figure 11</span></span>  
> <span data-ttu-id="e3093-212">Image clé modifiée</span><span class="sxs-lookup"><span data-stu-id="e3093-212">Modified keyframe</span></span>  
> ![Image clé modifiée][ImageModifiedKeyframe]  

<span data-ttu-id="e3093-214">Pour ajouter un délai à une animation, cliquez dessus et faites-la glisser n’importe où, à l’exception des cercles.</span><span class="sxs-lookup"><span data-stu-id="e3093-214">To add a delay to an animation, click and drag it anywhere except the circles.</span></span>  

> ##### <span data-ttu-id="e3093-215">Figure12</span><span class="sxs-lookup"><span data-stu-id="e3093-215">Figure 12</span></span>  
> <span data-ttu-id="e3093-216">Retard modifié</span><span class="sxs-lookup"><span data-stu-id="e3093-216">Modified delay</span></span>  
> ![Retard modifié][ImageModifiedDelay]  

<!--   -->  



<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: /microsoft-edge/devtools-guide-chromium/media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/replay-button-icon.msft.png  

[ImageAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-completed.msft.png "Figure 1: inspecteur d’animation"  
[ImageAnimationsViaMainMenu]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-more-tools-animations.msft.png "Figure 2: animations via le menu principal"  
[ImageEmptyAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations.msft.png "Figure 3: inspecteur d’animation vide"  
[ImageAnnotatedAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png "Figure 4: inspecteur d’animation annoté"  
[ImageAnimationGroupDetails]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png "Figure 5: détails sur le groupe d’animations"  
[ImageHoverOverAnimationHighlightViewport]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png "Figure 6: survol de l’animation pour la mettre en surbrillance dans la fenêtre d’affichage"  
[ImageDiagramAnimationIterations]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-display-animations-highlight.msft.png "Figure 7: diagramme d’itérations d’animation"  
[ImageColorCodedAnimations]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-display-animations.msft.png "Figure 8: animations à code couleur"  
[ImageOriginalAnimationBeforeModification]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations.msft.png "Figure 9: animation d’origine avant modification"  
[ImageModifiedDuration]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png "Figure 10: durée de modification"  
[ImageModifiedKeyframe]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png "Figure 11: image clé modifiée"  
[ImageModifiedDelay]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png "Figure 12: délai modifié"  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="e3093-230">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e3093-230">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e3093-231">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="e3093-231">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="e3093-233">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e3093-233">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
