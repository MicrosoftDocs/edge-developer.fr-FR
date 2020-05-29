---
title: Référence sur l’accessibilité
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 7417388023612b6e1ca651deba28e099e3c8e3d8
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581572"
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





# <span data-ttu-id="cf18b-103">Référence sur l’accessibilité</span><span class="sxs-lookup"><span data-stu-id="cf18b-103">Accessibility Reference</span></span>   



<span data-ttu-id="cf18b-104">Cette page est une référence complète des fonctionnalités d’accessibilité dans Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="cf18b-104">This page is a comprehensive reference of accessibility features in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="cf18b-105">Ce service est destiné aux développeurs Web qui:</span><span class="sxs-lookup"><span data-stu-id="cf18b-105">It is intended for web developers who:</span></span>  

*   <span data-ttu-id="cf18b-106">Découvrir les notions de base de DevTools, par exemple pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="cf18b-106">Have a basic understanding of DevTools, such as how to open it.</span></span>  
*   <span data-ttu-id="cf18b-107">Vous connaissez les [principes et les pratiques d’accessibilité][MDNAccessibility].</span><span class="sxs-lookup"><span data-stu-id="cf18b-107">Are familiar with [accessibility principles and best practices][MDNAccessibility].</span></span>  

<span data-ttu-id="cf18b-108">Cette référence a pour but de vous aider à découvrir les outils disponibles dans DevTools qui vous aident à examiner l’accessibilité d’une page.</span><span class="sxs-lookup"><span data-stu-id="cf18b-108">The purpose of this reference is to help you discover all of the tools available in DevTools that help you examine the accessibility of a page.</span></span>  

<span data-ttu-id="cf18b-109">Pour plus d’informations sur la navigation dans DevTools à l’aide d’une technologie d’assistance telle qu’un lecteur d’écran, reportez-vous à la rubrique [navigation dans Microsoft Edge devtools avec la technologie d’assistance][DevtoolsAccessibilityNavigation] .</span><span class="sxs-lookup"><span data-stu-id="cf18b-109">See [Navigating Microsoft Edge DevTools With Assistive Technology][DevtoolsAccessibilityNavigation] if you are looking for help on navigating DevTools with an assistive technology like a screen reader.</span></span>  

## <span data-ttu-id="cf18b-110">Vue d’ensemble des fonctionnalités d’accessibilité dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cf18b-110">Overview of accessibility features in Microsoft Edge DevTools</span></span>   

<span data-ttu-id="cf18b-111">Cette section décrit la façon dont DevTools s’inscrit dans votre kit de fonctions d’accessibilité global.</span><span class="sxs-lookup"><span data-stu-id="cf18b-111">This section explains how DevTools fits into your overall accessibility toolkit.</span></span>  

<span data-ttu-id="cf18b-112">Lorsque vous déterminez s’il est possible d’accéder à une page, vous devez avoir 2 questions générales à retenir:</span><span class="sxs-lookup"><span data-stu-id="cf18b-112">When determining whether a page is accessible, you need to have 2 general questions in mind:</span></span>  

1.  <span data-ttu-id="cf18b-113">Êtes-vous en mesure de naviguer sur la page à l’aide d’un clavier ou d’un [lecteur d’écran][MDNScreenReader]?</span><span class="sxs-lookup"><span data-stu-id="cf18b-113">Are you able to navigate the page with a keyboard or [screen reader][MDNScreenReader]?</span></span>  
1.  <span data-ttu-id="cf18b-114">Les éléments de la page sont-ils correctement marqués pour les lecteurs d’écran?</span><span class="sxs-lookup"><span data-stu-id="cf18b-114">Are the elements of the page properly marked up for screen readers?</span></span>  

<span data-ttu-id="cf18b-115">En général, DevTools devrait vous aider à résoudre les erreurs liées aux questions #2, car ces erreurs sont faciles à détecter de manière automatisée.</span><span class="sxs-lookup"><span data-stu-id="cf18b-115">In general, DevTools should help you fix errors related to question #2, because these errors are easy to detect in an automated fashion.</span></span>  <span data-ttu-id="cf18b-116">Le #1 de questions est comme important, mais malheureusement DevTools ne vous permet pas de le faire.</span><span class="sxs-lookup"><span data-stu-id="cf18b-116">Question #1 is just as important, but unfortunately DevTools does not help you there.</span></span>  <span data-ttu-id="cf18b-117">La seule façon de rechercher les erreurs liées aux questions #1 est d’essayer d’utiliser une page à l’aide d’un clavier ou d’un lecteur d’écran.</span><span class="sxs-lookup"><span data-stu-id="cf18b-117">The only way to find errors related to question #1 is to try using a page with a keyboard or screen reader yourself.</span></span>  <!--See [How To Do An Accessibility Review][AccessibilityReview] to learn more.  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <span data-ttu-id="cf18b-118">Auditer l’accessibilité d’une page</span><span class="sxs-lookup"><span data-stu-id="cf18b-118">Audit the accessibility of a page</span></span>   

> [!NOTE]
> <span data-ttu-id="cf18b-119">Le volet **audits** fournit des liens vers du contenu hébergé sur des sites Web tiers.</span><span class="sxs-lookup"><span data-stu-id="cf18b-119">The **Audits** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="cf18b-120">Microsoft n’est pas responsable et n’a aucun contrôle sur le contenu de ces sites et sur les données qui pourraient être collectées.</span><span class="sxs-lookup"><span data-stu-id="cf18b-120">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="cf18b-121">En règle générale, utilisez le volet audits pour déterminer si:</span><span class="sxs-lookup"><span data-stu-id="cf18b-121">In general, use the Audits panel to determine if:</span></span>  

*   <span data-ttu-id="cf18b-122">Une page est correctement marquée pour les lecteurs d’écran.</span><span class="sxs-lookup"><span data-stu-id="cf18b-122">A page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="cf18b-123">Les éléments de texte sur une page présentent des coefficients de contraste suffisants.</span><span class="sxs-lookup"><span data-stu-id="cf18b-123">The text elements on a page have sufficient contrast ratios.</span></span> <span data-ttu-id="cf18b-124">Voir également [afficher le coefficient de contraste d’un élément de texte dans le sélecteur de couleurs](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span><span class="sxs-lookup"><span data-stu-id="cf18b-124">See also [View the contrast ratio of a text element in the Color Picker](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span></span>  

<span data-ttu-id="cf18b-125">Pour auditer une page:</span><span class="sxs-lookup"><span data-stu-id="cf18b-125">To audit a page:</span></span>  

1.  <span data-ttu-id="cf18b-126">Accédez à l’URL que vous voulez auditer.</span><span class="sxs-lookup"><span data-stu-id="cf18b-126">Go to the URL that you want to audit.</span></span>  
1.  <span data-ttu-id="cf18b-127">Dans DevTools, cliquez sur l’onglet **audits** .  DevTools vous présente diverses options de configuration.</span><span class="sxs-lookup"><span data-stu-id="cf18b-127">In DevTools, click the **Audits** tab.  DevTools shows you various configuration options.</span></span>  
    
    > ##### <span data-ttu-id="cf18b-128">Figure1</span><span class="sxs-lookup"><span data-stu-id="cf18b-128">Figure 1</span></span>  
    > <span data-ttu-id="cf18b-129">Configuration d’audits</span><span class="sxs-lookup"><span data-stu-id="cf18b-129">Configuring audits</span></span>  
    > ![Configuration d’audits][ImageConfiguringAudits]  
    
    > [!NOTE]
    > <span data-ttu-id="cf18b-131">Les captures d’écran de cette section ont été effectuées avec la version 79 de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cf18b-131">The screenshots in this section were taken with version 79 of Microsoft Edge.</span></span>  <span data-ttu-id="cf18b-132">Vous pouvez vérifier la version que vous utilisez `edge://version` .</span><span class="sxs-lookup"><span data-stu-id="cf18b-132">You may check what version you are running at `edge://version`.</span></span>  <span data-ttu-id="cf18b-133">L’interface utilisateur du panneau **audits** est différente dans les versions antérieures de Microsoft Edge, mais le flux de travail général est le même.</span><span class="sxs-lookup"><span data-stu-id="cf18b-133">The **Audits** panel UI looks different in earlier versions of Microsoft Edge, but the general workflow is the same.</span></span>  
    
1.  <span data-ttu-id="cf18b-134">Pour **appareil**, sélectionnez **mobile** si vous voulez simuler un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="cf18b-134">For **Device**, select **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="cf18b-135">Cette option modifie votre chaîne d’agent utilisateur et redimensionne la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="cf18b-135">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="cf18b-136">Si la version mobile de la page ne s’affiche pas comme la version de bureau, cette option peut avoir un effet notable sur les résultats de votre audit.</span><span class="sxs-lookup"><span data-stu-id="cf18b-136">If the mobile version of the page displays differently than the desktop version, this option could have a significant effect on the results of your audit.</span></span>  
1.  <span data-ttu-id="cf18b-137">Dans la section **audits** , vérifiez que l’option **accessibilité** est activée.</span><span class="sxs-lookup"><span data-stu-id="cf18b-137">In the **Audits** section, make sure that **Accessibility** is enabled.</span></span>  <span data-ttu-id="cf18b-138">Désactivez les autres catégories si vous voulez les exclure de votre rapport.</span><span class="sxs-lookup"><span data-stu-id="cf18b-138">Disable the other categories if you want to exclude them from your report.</span></span>  <span data-ttu-id="cf18b-139">Laissez-les activés si vous voulez découvrir d’autres façons d’améliorer la qualité de votre page.</span><span class="sxs-lookup"><span data-stu-id="cf18b-139">Leave them enabled if you want to discover other ways to improve the quality of your page.</span></span>  
1.  <span data-ttu-id="cf18b-140">La section **limitation** vous permet de limiter le réseau et le processeur, ce qui est utile lors de l’analyse des performances de chargement.</span><span class="sxs-lookup"><span data-stu-id="cf18b-140">The **Throttling** section lets you throttle the network and CPU, which is useful when analyzing load performance.</span></span>  <span data-ttu-id="cf18b-141">Cette option n’est pas adaptée à votre score d’accessibilité, donc vous pouvez utiliser ce que vous préférez.</span><span class="sxs-lookup"><span data-stu-id="cf18b-141">This option should be irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="cf18b-142">La case à cocher **Clear Storage** vous permet d’effacer tout le stockage avant de charger la page ou de conserver le stockage entre les chargements de pages.</span><span class="sxs-lookup"><span data-stu-id="cf18b-142">The **Clear Storage** checkbox lets you clear all storage before loading the page, or preserve storage between page loads.</span></span>  <span data-ttu-id="cf18b-143">Cette option n’est pas non plus pertinente pour votre score d’accessibilité, vous pouvez donc utiliser ce que vous préférez.</span><span class="sxs-lookup"><span data-stu-id="cf18b-143">This option is also probably irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="cf18b-144">Cliquez sur **exécuter les audits**.</span><span class="sxs-lookup"><span data-stu-id="cf18b-144">Click **Run Audits**.</span></span> <span data-ttu-id="cf18b-145">Après 10 à 30 secondes, DevTools fournit un rapport.</span><span class="sxs-lookup"><span data-stu-id="cf18b-145">After 10 to 30 seconds, DevTools provides a report.</span></span>  <span data-ttu-id="cf18b-146">Votre rapport vous donne différentes astuces pour améliorer l’accessibilité de la page.</span><span class="sxs-lookup"><span data-stu-id="cf18b-146">Your report gives you various tips on how to improve the accessibility of the page.</span></span>  
    
    > ##### <span data-ttu-id="cf18b-147">Figure 2</span><span class="sxs-lookup"><span data-stu-id="cf18b-147">Figure 2</span></span>  
    > <span data-ttu-id="cf18b-148">Un rapport</span><span class="sxs-lookup"><span data-stu-id="cf18b-148">A report</span></span>  
    > ![Un rapport][ImageReport]  
    
1.  <span data-ttu-id="cf18b-150">Cliquez sur un audit pour en savoir plus à son sujet.</span><span class="sxs-lookup"><span data-stu-id="cf18b-150">Click an audit to learn more about it.</span></span>  
    
    > ##### <span data-ttu-id="cf18b-151">Figure3</span><span class="sxs-lookup"><span data-stu-id="cf18b-151">Figure 3</span></span>  
    > <span data-ttu-id="cf18b-152">Plus d’informations sur un audit</span><span class="sxs-lookup"><span data-stu-id="cf18b-152">More information about an audit</span></span>  
    > ![Plus d’informations sur un audit][ImageAttributes]  
    
1.  <span data-ttu-id="cf18b-154">Cliquez sur **en savoir plus** pour afficher la documentation de ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="cf18b-154">Click **Learn More** to view the documentation of that audit.</span></span>
    
    > ##### <span data-ttu-id="cf18b-155">Figure 4</span><span class="sxs-lookup"><span data-stu-id="cf18b-155">Figure 4</span></span>  
    > <span data-ttu-id="cf18b-156">Affichage de la documentation d’un audit</span><span class="sxs-lookup"><span data-stu-id="cf18b-156">Viewing the documentation of an audit</span></span>  
    > ![Affichage de la documentation d’un audit][ImageAuditDocumentation]  
    
### <span data-ttu-id="cf18b-158">Voir aussi: extension de la hache</span><span class="sxs-lookup"><span data-stu-id="cf18b-158">See also: aXe extension</span></span>   

<span data-ttu-id="cf18b-159">Il est possible que vous préfériez utiliser l’extension de la [hache][ChromeWebStoreAxe] plutôt que le panneau **audits** .</span><span class="sxs-lookup"><span data-stu-id="cf18b-159">You may prefer to use the [aXe extension][ChromeWebStoreAxe] rather than the **Audits** panel.</span></span>  
<span data-ttu-id="cf18b-160">L’extension de la hache fournit généralement les mêmes informations, car il s’agit du moteur sous-jacent qui alimente le panneau audits.</span><span class="sxs-lookup"><span data-stu-id="cf18b-160">The aXe extension generally provides the same information, since it is the underlying engine that powers the Audits panel.</span></span>  <span data-ttu-id="cf18b-161">L’extension de aXe a une interface utilisateur différente et décrit les audits légèrement différemment.</span><span class="sxs-lookup"><span data-stu-id="cf18b-161">The aXe extension has a different UI and describes audits slightly differently.</span></span>  
<span data-ttu-id="cf18b-162">Un des avantages que l’extension de aXe a sur le panneau **d’audit** est qu’il vous permet d’inspecter et de mettre en surbrillance les nœuds défectueux.</span><span class="sxs-lookup"><span data-stu-id="cf18b-162">One advantage that the aXe extension has over the **Audits** panel is that it enables you to inspect and highlight failing nodes.</span></span>  

> ##### <span data-ttu-id="cf18b-163">Figure 5</span><span class="sxs-lookup"><span data-stu-id="cf18b-163">Figure 5</span></span>  
> <span data-ttu-id="cf18b-164">Extension de la hache</span><span class="sxs-lookup"><span data-stu-id="cf18b-164">The aXe extension</span></span>  
> ![Extension de la hache][ImageAxeExtension]  

## <span data-ttu-id="cf18b-166">Volet accessibilité</span><span class="sxs-lookup"><span data-stu-id="cf18b-166">The Accessibility pane</span></span>   

<span data-ttu-id="cf18b-167">Le volet **accessibilité** vous permet d’afficher l’arborescence d’accessibilité, les attributs Aria et les propriétés d’accessibilité calculée des nœuds DOM.</span><span class="sxs-lookup"><span data-stu-id="cf18b-167">The **Accessibility** pane is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="cf18b-168">Pour ouvrir le volet **accessibilité** :</span><span class="sxs-lookup"><span data-stu-id="cf18b-168">To open the **Accessibility** pane:</span></span>  

1.  <span data-ttu-id="cf18b-169">Cliquez sur l’onglet **éléments** .</span><span class="sxs-lookup"><span data-stu-id="cf18b-169">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="cf18b-170">Dans l' **arborescence DOM**, sélectionnez l’élément que vous voulez inspecter.</span><span class="sxs-lookup"><span data-stu-id="cf18b-170">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="cf18b-171">Cliquez sur l’onglet **accessibilité** .  Cet onglet est parfois masqué derrière le bouton **plus** d’onglets ![ ][ImageMoreTabsIcon] .</span><span class="sxs-lookup"><span data-stu-id="cf18b-171">Click the **Accessibility** tab.  This tab may be hidden behind the **More Tabs** ![More Tabs][ImageMoreTabsIcon] button.</span></span>  

> ##### <span data-ttu-id="cf18b-172">Figure 6</span><span class="sxs-lookup"><span data-stu-id="cf18b-172">Figure 6</span></span>  
> <span data-ttu-id="cf18b-173">Inspecter l' `h1` élément de la page d’accueil devtools dans le volet **accessibilité**</span><span class="sxs-lookup"><span data-stu-id="cf18b-173">Inspecting the `h1` element of the DevTools homepage in the **Accessibility** pane</span></span>  
> ![Inspecter l’élément H1 de la page d’accueil de DevTools dans le volet accessibilité][ImageA11yPane]  

### <span data-ttu-id="cf18b-175">Afficher la position d’un élément dans l’arborescence d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="cf18b-175">View the position of an element in the accessibility tree</span></span>   

<span data-ttu-id="cf18b-176">L' [arborescence d’accessibilité][MDNAccessibilityTree] est un sous-ensemble de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="cf18b-176">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="cf18b-177">Il contient uniquement des éléments de l’arborescence DOM qui sont pertinents et utiles pour afficher le contenu d’une page dans un lecteur d’écran.</span><span class="sxs-lookup"><span data-stu-id="cf18b-177">It only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  

<span data-ttu-id="cf18b-178">Inspectez la position d’un élément dans l’arborescence d’accessibilité à partir du [volet accessibilité](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="cf18b-178">Inspect the position of an element in the accessibility tree from the [Accessibility pane](#the-accessibility-pane).</span></span>  

> ##### <span data-ttu-id="cf18b-179">Figure 7</span><span class="sxs-lookup"><span data-stu-id="cf18b-179">Figure 7</span></span>  
> <span data-ttu-id="cf18b-180">Section arborescence d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="cf18b-180">The Accessibility Tree section</span></span>  
> ![Section arborescence d’accessibilité][ImageAllyTree]  

### <span data-ttu-id="cf18b-182">Afficher les attributs ARIA d’un élément</span><span class="sxs-lookup"><span data-stu-id="cf18b-182">View the ARIA attributes of an element</span></span>   

<span data-ttu-id="cf18b-183">Les attributs ARIA garantissent que les lecteurs d’écran disposent de toutes les informations dont ils ont besoin pour représenter correctement le contenu d’une page.</span><span class="sxs-lookup"><span data-stu-id="cf18b-183">ARIA attributes ensure that screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="cf18b-184">Affichez les attributs ARIA d’un élément dans le [volet accessibilité](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="cf18b-184">View the ARIA attributes of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

> ##### <span data-ttu-id="cf18b-185">Figure8</span><span class="sxs-lookup"><span data-stu-id="cf18b-185">Figure 8</span></span>  
> <span data-ttu-id="cf18b-186">Section attributs ARIA</span><span class="sxs-lookup"><span data-stu-id="cf18b-186">The ARIA Attributes section</span></span>  
> ![Section attributs ARIA][ImageAriaAttributesSection]  

### <span data-ttu-id="cf18b-188">Afficher les propriétés d’accessibilité calculées d’un élément</span><span class="sxs-lookup"><span data-stu-id="cf18b-188">View the computed accessibility properties of an element</span></span>   

> [!NOTE]
> <span data-ttu-id="cf18b-189">Si vous recherchez des propriétés CSS calculées, voir l' [onglet calculé][DevtoolsCssReferenceViewActuallyAppliedElements].</span><span class="sxs-lookup"><span data-stu-id="cf18b-189">If you are looking for computed CSS properties, see the [Computed tab][DevtoolsCssReferenceViewActuallyAppliedElements].</span></span>  

<span data-ttu-id="cf18b-190">Certaines propriétés d’accessibilité sont calculées de manière dynamique par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="cf18b-190">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="cf18b-191">Ces propriétés sont affichées dans la section **propriétés calculées** du volet **accessibilité** .</span><span class="sxs-lookup"><span data-stu-id="cf18b-191">These properties are displayed in the **Computed Properties** section of the **Accessibility** pane.</span></span>  

<span data-ttu-id="cf18b-192">Afficher les propriétés d’accessibilité calculées d’un élément dans le [volet accessibilité](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="cf18b-192">View the computed accessibility properties of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

> ##### <span data-ttu-id="cf18b-193">Figure9</span><span class="sxs-lookup"><span data-stu-id="cf18b-193">Figure 9</span></span>  
> <span data-ttu-id="cf18b-194">Section Propriétés calculées (accessibilité)</span><span class="sxs-lookup"><span data-stu-id="cf18b-194">The Computed (Accessibility) Properties section</span></span>  
> ![Section Propriétés calculées (accessibilité)][ImageComputedA11yPropertiesSection]  

## <span data-ttu-id="cf18b-196">Afficher le coefficient de contraste d’un élément de texte dans le sélecteur de couleurs</span><span class="sxs-lookup"><span data-stu-id="cf18b-196">View the contrast ratio of a text element in the Color Picker</span></span>   

<span data-ttu-id="cf18b-197">Certaines personnes souffrant de troubles de la vue ne voient pas les zones comme très brillantes ou très sombres.</span><span class="sxs-lookup"><span data-stu-id="cf18b-197">Some people with low vision do not see areas as very bright or very dark.</span></span>  <span data-ttu-id="cf18b-198">Tout a tendance à apparaître à la même luminosité, ce qui permet de distinguer les plans et les bords.</span><span class="sxs-lookup"><span data-stu-id="cf18b-198">Everything tends to appear at about the same brightness, which makes it hard to distinguish outlines and edges.</span></span>  
<span data-ttu-id="cf18b-199">Coefficient de contraste mesure la différence de luminosité entre le premier plan et l’arrière-plan du texte.</span><span class="sxs-lookup"><span data-stu-id="cf18b-199">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="cf18b-200">Si votre texte a un coefficient de contraste faible, il est possible que les utilisateurs malvoyants puissent littéralement voir votre site comme un écran vierge.</span><span class="sxs-lookup"><span data-stu-id="cf18b-200">If your text has a low contrast ratio, then these low vision users may literally experience your site as a blank screen.</span></span>  

<span data-ttu-id="cf18b-201">Le sélecteur de couleurs permet de vérifier que votre texte répond aux niveaux de contraste recommandés:</span><span class="sxs-lookup"><span data-stu-id="cf18b-201">The Color Picker helps you verify that your text meets recommended contrast ratio levels:</span></span>  

1.  <span data-ttu-id="cf18b-202">Cliquez sur l’onglet **éléments** .</span><span class="sxs-lookup"><span data-stu-id="cf18b-202">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="cf18b-203">Dans l' **arborescence DOM**, sélectionnez l’élément de texte que vous voulez inspecter.</span><span class="sxs-lookup"><span data-stu-id="cf18b-203">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    > ##### <span data-ttu-id="cf18b-204">Figure10</span><span class="sxs-lookup"><span data-stu-id="cf18b-204">Figure 10</span></span>  
    > <span data-ttu-id="cf18b-205">Examen d’un paragraphe dans l’arborescence DOM</span><span class="sxs-lookup"><span data-stu-id="cf18b-205">Inspecting a paragraph in the DOM Tree</span></span>  
    > ![Examen d’un paragraphe dans l’arborescence DOM][ImageInspectDomTree]  
    
1.  <span data-ttu-id="cf18b-207">Dans le volet **styles** , cliquez sur le carré de couleur en regard de la `color` valeur de l’élément.</span><span class="sxs-lookup"><span data-stu-id="cf18b-207">In the **Styles** pane, click the color square next to the `color` value of the element.</span></span>  
    
    > ##### <span data-ttu-id="cf18b-208">Figure11</span><span class="sxs-lookup"><span data-stu-id="cf18b-208">Figure 11</span></span>  
    > <span data-ttu-id="cf18b-209">La `color` propriété de l’élément</span><span class="sxs-lookup"><span data-stu-id="cf18b-209">The `color` property of the element</span></span>  
    > ![La propriété Color de l’élément][ImageColorElement]  
    
1.  <span data-ttu-id="cf18b-211">Vérifiez la section **coefficient de contraste** du sélecteur de couleurs.</span><span class="sxs-lookup"><span data-stu-id="cf18b-211">Check the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="cf18b-212">Une coche signifie que l’élément est conforme à la [recommandation minimum][W3CContrastMinimum].</span><span class="sxs-lookup"><span data-stu-id="cf18b-212">One checkmark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="cf18b-213">Deux coches signifient qu’il est conforme à la [recommandation améliorée][W3CContrastEnhanced].</span><span class="sxs-lookup"><span data-stu-id="cf18b-213">Two checkmarks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>
    
    > ##### <span data-ttu-id="cf18b-214">Figure12</span><span class="sxs-lookup"><span data-stu-id="cf18b-214">Figure 12</span></span>  
    > <span data-ttu-id="cf18b-215">La section coefficient de contraste du sélecteur de couleurs affiche 2 coches et une valeur de</span><span class="sxs-lookup"><span data-stu-id="cf18b-215">The Contrast Ratio section of the Color Picker shows 2 checkmarks and a value of</span></span> `13.97`  
    > ![La section coefficient de contraste du sélecteur de couleurs affiche 2 coches et une valeur de 13,97][ImageColorPickerContrastRatio]  
    
1.  <span data-ttu-id="cf18b-217">Cliquez sur la section **coefficient de contraste** pour afficher des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="cf18b-217">Click the **Contrast Ratio** section to see more information.</span></span>  <span data-ttu-id="cf18b-218">Une ligne s’affiche dans le sélecteur de visuels en haut du sélecteur de couleurs.</span><span class="sxs-lookup"><span data-stu-id="cf18b-218">A line appears in the visual picker at the top of the Color Picker.</span></span>  <span data-ttu-id="cf18b-219">Si la couleur actuelle répond aux recommandations, tout ce qui se trouve sur le même côté de la ligne répond également aux recommandations.</span><span class="sxs-lookup"><span data-stu-id="cf18b-219">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="cf18b-220">Si la couleur en cours ne répond pas aux recommandations, tout ce qui se trouve dans le même côté ne répond pas aux recommandations.</span><span class="sxs-lookup"><span data-stu-id="cf18b-220">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  
    
    > ##### <span data-ttu-id="cf18b-221">Figure13</span><span class="sxs-lookup"><span data-stu-id="cf18b-221">Figure 13</span></span>  
    > <span data-ttu-id="cf18b-222">Ligne de coefficient de contraste dans le sélecteur visuel</span><span class="sxs-lookup"><span data-stu-id="cf18b-222">The Contrast Ratio Line in the visual picker</span></span>  
    > ![Ligne de coefficient de contraste dans le sélecteur visuel][ImageContrastRatioLine]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageMoreTabsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-tabs-icon.msft.png  

[ImageConfiguringAudits]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-pane.msft.png "Figure 1: configuration des audits"  
[ImageReport]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-run-audits-result.msft.png "Figure 2: une figure"  
[ImageAttributes]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-run-audits-result-issues-expanded.msft.png "Figure 3: informations supplémentaires sur un audit"  
[ImageAuditDocumentation]: /microsoft-edge/devtools-guide-chromium/media/accessibility-web-dev-accessibility-audits-learn-more.msft.png "Figure 4: affichage de la documentation d’un audit"  
[ImageAxeExtension]: /microsoft-edge/devtools-guide-chromium/media/accessibility-devtools-extension-axe-panel.msft.png "Figure 5: extension de la hache"  
[ImageA11yPane]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility.msft.png "Figure 6: inspecter l’élément H1 de la page d’accueil de DevTools dans le volet accessibilité"  
[ImageAllyTree]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-tree.msft.png "Figure 7: section de l’arborescence de l’accessibilité"  
[ImageAriaAttributesSection]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-aria-attributes.msft.png "Figure 8: section attributs ARIA"  
[ImageComputedA11yPropertiesSection]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-computed-properties.msft.png "Figure 9: section Propriétés calculées (accessibilité)"  
[ImageInspectDomTree]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-paragraph-highlight.msft.png "Figure 10: examen d’un paragraphe dans l’arborescence DOM"  
[ImageColorElement]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color.msft.png "Figure 11: propriété Color de l’élément"  
[ImageColorPickerContrastRatio]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png "Figure 12: la section coefficient de contraste du sélecteur de couleurs affiche 2 coches et une valeur de 13,97"  
[ImageContrastRatioLine]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png "Figure 13: ligne de coefficient de contraste dans le sélecteur visuel"  
<!-- links -->  

[DevtoolsAccessibilityNavigation]: navigation.md "Navigation dans Microsoft Edge DevTools avec la technologie d’assistance"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Afficher uniquement les feuilles CSS appliquées actuellement à une référence d’élément CSS"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "axe-tests d’accessibilité sur le Web-chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Arborescence d’accessibilité (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Accessibilité | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Lecteur d’écran | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Niveau de contraste (amélioré) AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Contraste (minimum) niveau AA | W3C"  

> [!NOTE]
> <span data-ttu-id="cf18b-245">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cf18b-245">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cf18b-246">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="cf18b-246">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="cf18b-248">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cf18b-248">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
