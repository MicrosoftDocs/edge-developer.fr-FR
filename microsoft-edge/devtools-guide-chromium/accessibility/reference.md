---
title: Référence sur l’accessibilité
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 190890b43cff97ae0f379426b68a688534ebda95
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983635"
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





# <span data-ttu-id="60a33-103">Référence sur l’accessibilité</span><span class="sxs-lookup"><span data-stu-id="60a33-103">Accessibility Reference</span></span>   



<span data-ttu-id="60a33-104">Cette page est une référence complète des fonctionnalités d’accessibilité dans Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="60a33-104">This page is a comprehensive reference of accessibility features in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="60a33-105">Ce service est destiné aux développeurs Web qui:</span><span class="sxs-lookup"><span data-stu-id="60a33-105">It is intended for web developers who:</span></span>  

*   <span data-ttu-id="60a33-106">Découvrir les notions de base de DevTools, par exemple pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="60a33-106">Have a basic understanding of DevTools, such as how to open it.</span></span>  
*   <span data-ttu-id="60a33-107">Vous connaissez les [principes et les pratiques d’accessibilité][MDNAccessibility].</span><span class="sxs-lookup"><span data-stu-id="60a33-107">Are familiar with [accessibility principles and best practices][MDNAccessibility].</span></span>  
    
<span data-ttu-id="60a33-108">Cette référence a pour but de vous aider à découvrir les outils disponibles dans DevTools qui vous aident à examiner l’accessibilité d’une page.</span><span class="sxs-lookup"><span data-stu-id="60a33-108">The purpose of this reference is to help you discover all of the tools available in DevTools that help you examine the accessibility of a page.</span></span>  

<span data-ttu-id="60a33-109">Pour plus d’informations sur la navigation dans DevTools à l’aide d’une technologie d’assistance telle qu’un lecteur d’écran, reportez-vous à la rubrique [navigation dans Microsoft Edge devtools avec la technologie d’assistance][DevtoolsAccessibilityNavigation] .</span><span class="sxs-lookup"><span data-stu-id="60a33-109">See [Navigating Microsoft Edge DevTools With Assistive Technology][DevtoolsAccessibilityNavigation] if you are looking for help on navigating DevTools with an assistive technology like a screen reader.</span></span>  

## <span data-ttu-id="60a33-110">Vue d’ensemble des fonctionnalités d’accessibilité dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="60a33-110">Overview of accessibility features in Microsoft Edge DevTools</span></span>   

<span data-ttu-id="60a33-111">Cette section décrit la façon dont DevTools s’inscrit dans votre kit de fonctions d’accessibilité global.</span><span class="sxs-lookup"><span data-stu-id="60a33-111">This section explains how DevTools fits into your overall accessibility toolkit.</span></span>  

<span data-ttu-id="60a33-112">Lorsque vous déterminez s’il est possible d’accéder à une page, vous devez avoir 2 questions générales à retenir:</span><span class="sxs-lookup"><span data-stu-id="60a33-112">When determining whether a page is accessible, you need to have 2 general questions in mind:</span></span>  

1.  <span data-ttu-id="60a33-113">Êtes-vous en mesure de naviguer sur la page à l’aide d’un clavier ou d’un [lecteur d’écran][MDNScreenReader]?</span><span class="sxs-lookup"><span data-stu-id="60a33-113">Are you able to navigate the page with a keyboard or [screen reader][MDNScreenReader]?</span></span>  
1.  <span data-ttu-id="60a33-114">Les éléments de la page sont-ils correctement marqués pour les lecteurs d’écran?</span><span class="sxs-lookup"><span data-stu-id="60a33-114">Are the elements of the page properly marked up for screen readers?</span></span>  
    
<span data-ttu-id="60a33-115">En général, DevTools devrait vous aider à résoudre les erreurs liées aux questions #2, car ces erreurs sont faciles à détecter de manière automatisée.</span><span class="sxs-lookup"><span data-stu-id="60a33-115">In general, DevTools should help you fix errors related to question #2, because these errors are easy to detect in an automated fashion.</span></span>  <span data-ttu-id="60a33-116">Le #1 de questions est comme important, mais malheureusement DevTools ne vous permet pas de le faire.</span><span class="sxs-lookup"><span data-stu-id="60a33-116">Question #1 is just as important, but unfortunately DevTools does not help you there.</span></span>  <span data-ttu-id="60a33-117">La seule façon de rechercher les erreurs liées aux questions #1 est d’essayer d’utiliser une page à l’aide d’un clavier ou d’un lecteur d’écran.</span><span class="sxs-lookup"><span data-stu-id="60a33-117">The only way to find errors related to question #1 is to try using a page with a keyboard or screen reader yourself.</span></span>  <!--See [How To Do An Accessibility Review][AccessibilityReview] to learn more.  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <span data-ttu-id="60a33-118">Auditer l’accessibilité d’une page</span><span class="sxs-lookup"><span data-stu-id="60a33-118">Audit the accessibility of a page</span></span>   

> [!NOTE]
> <span data-ttu-id="60a33-119">Le volet **audits** fournit des liens vers du contenu hébergé sur des sites Web tiers.</span><span class="sxs-lookup"><span data-stu-id="60a33-119">The **Audits** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="60a33-120">Microsoft n’est pas responsable et n’a aucun contrôle sur le contenu de ces sites et sur les données qui pourraient être collectées.</span><span class="sxs-lookup"><span data-stu-id="60a33-120">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="60a33-121">En règle générale, utilisez le volet audits pour déterminer si:</span><span class="sxs-lookup"><span data-stu-id="60a33-121">In general, use the Audits panel to determine if:</span></span>  

*   <span data-ttu-id="60a33-122">Une page est correctement marquée pour les lecteurs d’écran.</span><span class="sxs-lookup"><span data-stu-id="60a33-122">A page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="60a33-123">Les éléments de texte sur une page présentent des coefficients de contraste suffisants.</span><span class="sxs-lookup"><span data-stu-id="60a33-123">The text elements on a page have sufficient contrast ratios.</span></span> <span data-ttu-id="60a33-124">Voir également [afficher le coefficient de contraste d’un élément de texte dans le sélecteur de couleurs](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span><span class="sxs-lookup"><span data-stu-id="60a33-124">See also [View the contrast ratio of a text element in the Color Picker](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span></span>  
    
<span data-ttu-id="60a33-125">Pour auditer une page:</span><span class="sxs-lookup"><span data-stu-id="60a33-125">To audit a page:</span></span>  

1.  <span data-ttu-id="60a33-126">Accédez à l’URL que vous voulez auditer.</span><span class="sxs-lookup"><span data-stu-id="60a33-126">Go to the URL that you want to audit.</span></span>  
1.  <span data-ttu-id="60a33-127">Dans DevTools, cliquez sur l’onglet **audits** .  DevTools vous présente diverses options de configuration.</span><span class="sxs-lookup"><span data-stu-id="60a33-127">In DevTools, click the **Audits** tab.  DevTools shows you various configuration options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Configurer les audits" lightbox="../media/accessibility-audits-pane.msft.png":::
       <span data-ttu-id="60a33-129">Configurer les audits</span><span class="sxs-lookup"><span data-stu-id="60a33-129">Configure audits</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="60a33-130">Les captures d’écran de cette section ont été effectuées avec la version 79 de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="60a33-130">The screenshots in this section were taken with version 79 of Microsoft Edge.</span></span>  <span data-ttu-id="60a33-131">Vous pouvez vérifier la version que vous utilisez `edge://version` .</span><span class="sxs-lookup"><span data-stu-id="60a33-131">You may check what version you are running at `edge://version`.</span></span>  <span data-ttu-id="60a33-132">L’interface utilisateur du panneau **audits** est différente dans les versions antérieures de Microsoft Edge, mais le flux de travail général est le même.</span><span class="sxs-lookup"><span data-stu-id="60a33-132">The **Audits** panel UI looks different in earlier versions of Microsoft Edge, but the general workflow is the same.</span></span>  
    
1.  <span data-ttu-id="60a33-133">Pour **appareil**, sélectionnez **mobile** si vous voulez simuler un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="60a33-133">For **Device**, select **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="60a33-134">Cette option modifie votre chaîne d’agent utilisateur et redimensionne la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="60a33-134">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="60a33-135">Si la version mobile de la page ne s’affiche pas comme la version de bureau, cette option peut avoir un effet notable sur les résultats de votre audit.</span><span class="sxs-lookup"><span data-stu-id="60a33-135">If the mobile version of the page displays differently than the desktop version, this option could have a significant effect on the results of your audit.</span></span>  
1.  <span data-ttu-id="60a33-136">Dans la section **audits** , vérifiez que l’option **accessibilité** est activée.</span><span class="sxs-lookup"><span data-stu-id="60a33-136">In the **Audits** section, make sure that **Accessibility** is enabled.</span></span>  <span data-ttu-id="60a33-137">Désactivez les autres catégories si vous voulez les exclure de votre rapport.</span><span class="sxs-lookup"><span data-stu-id="60a33-137">Disable the other categories if you want to exclude them from your report.</span></span>  <span data-ttu-id="60a33-138">Laissez-les activés si vous voulez découvrir d’autres façons d’améliorer la qualité de votre page.</span><span class="sxs-lookup"><span data-stu-id="60a33-138">Leave them enabled if you want to discover other ways to improve the quality of your page.</span></span>  
1.  <span data-ttu-id="60a33-139">La section **limitation** vous permet de limiter le réseau et le processeur, ce qui est utile lors de l’analyse des performances de chargement.</span><span class="sxs-lookup"><span data-stu-id="60a33-139">The **Throttling** section lets you throttle the network and CPU, which is useful when analyzing load performance.</span></span>  <span data-ttu-id="60a33-140">Cette option n’est pas adaptée à votre score d’accessibilité, donc vous pouvez utiliser ce que vous préférez.</span><span class="sxs-lookup"><span data-stu-id="60a33-140">This option should be irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="60a33-141">La case à cocher **Clear Storage** vous permet d’effacer tout le stockage avant de charger la page ou de conserver le stockage entre les chargements de pages.</span><span class="sxs-lookup"><span data-stu-id="60a33-141">The **Clear Storage** checkbox lets you clear all storage before loading the page, or preserve storage between page loads.</span></span>  <span data-ttu-id="60a33-142">Cette option n’est pas non plus pertinente pour votre score d’accessibilité, vous pouvez donc utiliser ce que vous préférez.</span><span class="sxs-lookup"><span data-stu-id="60a33-142">This option is also probably irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="60a33-143">Cliquez sur **exécuter les audits**.</span><span class="sxs-lookup"><span data-stu-id="60a33-143">Click **Run Audits**.</span></span> <span data-ttu-id="60a33-144">Après 10 à 30 secondes, DevTools fournit un rapport.</span><span class="sxs-lookup"><span data-stu-id="60a33-144">After 10 to 30 seconds, DevTools provides a report.</span></span>  <span data-ttu-id="60a33-145">Votre rapport vous donne différentes astuces pour améliorer l’accessibilité de la page.</span><span class="sxs-lookup"><span data-stu-id="60a33-145">Your report gives you various tips on how to improve the accessibility of the page.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Un rapport" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       <span data-ttu-id="60a33-147">Un rapport</span><span class="sxs-lookup"><span data-stu-id="60a33-147">A report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="60a33-148">Cliquez sur un audit pour en savoir plus à son sujet.</span><span class="sxs-lookup"><span data-stu-id="60a33-148">Click an audit to learn more about it.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Plus d’informations sur un audit" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       <span data-ttu-id="60a33-150">Plus d’informations sur un audit</span><span class="sxs-lookup"><span data-stu-id="60a33-150">More information about an audit</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="60a33-151">Cliquez sur **en savoir plus** pour afficher la documentation de ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="60a33-151">Click **Learn More** to view the documentation of that audit.</span></span>
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Afficher la documentation d’un audit" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       <span data-ttu-id="60a33-153">Afficher la documentation d’un audit</span><span class="sxs-lookup"><span data-stu-id="60a33-153">View the documentation of an audit</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="60a33-154">Voir aussi: extension de la hache</span><span class="sxs-lookup"><span data-stu-id="60a33-154">See also: aXe extension</span></span>   

<span data-ttu-id="60a33-155">Il est possible que vous préfériez utiliser l’extension de la [hache][ChromeWebStoreAxe] plutôt que le panneau **audits** .</span><span class="sxs-lookup"><span data-stu-id="60a33-155">You may prefer to use the [aXe extension][ChromeWebStoreAxe] rather than the **Audits** panel.</span></span>  
<span data-ttu-id="60a33-156">L’extension de la hache fournit généralement les mêmes informations, car il s’agit du moteur sous-jacent qui alimente le panneau audits.</span><span class="sxs-lookup"><span data-stu-id="60a33-156">The aXe extension generally provides the same information, since it is the underlying engine that powers the Audits panel.</span></span>  <span data-ttu-id="60a33-157">L’extension de aXe a une interface utilisateur différente et décrit les audits légèrement différemment.</span><span class="sxs-lookup"><span data-stu-id="60a33-157">The aXe extension has a different UI and describes audits slightly differently.</span></span>  
<span data-ttu-id="60a33-158">Un des avantages que l’extension de aXe a sur le panneau **d’audit** est qu’il vous permet d’inspecter et de mettre en surbrillance les nœuds défectueux.</span><span class="sxs-lookup"><span data-stu-id="60a33-158">One advantage that the aXe extension has over the **Audits** panel is that it enables you to inspect and highlight failing nodes.</span></span>  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="Extension de la hache" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   <span data-ttu-id="60a33-160">Extension de la hache</span><span class="sxs-lookup"><span data-stu-id="60a33-160">The aXe extension</span></span>  
:::image-end:::  

## <span data-ttu-id="60a33-161">Volet accessibilité</span><span class="sxs-lookup"><span data-stu-id="60a33-161">The Accessibility pane</span></span>   

<span data-ttu-id="60a33-162">Le volet **accessibilité** vous permet d’afficher l’arborescence d’accessibilité, les attributs Aria et les propriétés d’accessibilité calculée des nœuds DOM.</span><span class="sxs-lookup"><span data-stu-id="60a33-162">The **Accessibility** pane is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="60a33-163">Pour ouvrir le volet **accessibilité** :</span><span class="sxs-lookup"><span data-stu-id="60a33-163">To open the **Accessibility** pane:</span></span>  

1.  <span data-ttu-id="60a33-164">Cliquez sur l’onglet **éléments** .</span><span class="sxs-lookup"><span data-stu-id="60a33-164">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="60a33-165">Dans l' **arborescence DOM**, sélectionnez l’élément que vous voulez inspecter.</span><span class="sxs-lookup"><span data-stu-id="60a33-165">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="60a33-166">Cliquez sur l’onglet **accessibilité** .  Cet onglet est parfois masqué derrière le bouton **plus** d’onglets ![ ][ImageMoreTabsIcon] .</span><span class="sxs-lookup"><span data-stu-id="60a33-166">Click the **Accessibility** tab.  This tab may be hidden behind the **More Tabs** ![More Tabs][ImageMoreTabsIcon] button.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Inspecter l’élément H1 de la page d’accueil de DevTools dans le volet accessibilité" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   <span data-ttu-id="60a33-168">Inspecter l' `h1` élément de la page d’accueil devtools dans le volet **accessibilité**</span><span class="sxs-lookup"><span data-stu-id="60a33-168">Inspect the `h1` element of the DevTools homepage in the **Accessibility** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="60a33-169">Afficher la position d’un élément dans l’arborescence d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="60a33-169">View the position of an element in the accessibility tree</span></span>   

<span data-ttu-id="60a33-170">L' [arborescence d’accessibilité][MDNAccessibilityTree] est un sous-ensemble de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="60a33-170">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="60a33-171">Il contient uniquement des éléments de l’arborescence DOM qui sont pertinents et utiles pour afficher le contenu d’une page dans un lecteur d’écran.</span><span class="sxs-lookup"><span data-stu-id="60a33-171">It only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  

<span data-ttu-id="60a33-172">Inspectez la position d’un élément dans l’arborescence d’accessibilité à partir du [volet accessibilité](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="60a33-172">Inspect the position of an element in the accessibility tree from the [Accessibility pane](#the-accessibility-pane).</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Section arborescence d’accessibilité" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   <span data-ttu-id="60a33-174">Section **arborescence d’accessibilité**</span><span class="sxs-lookup"><span data-stu-id="60a33-174">The **Accessibility Tree** section</span></span>  
:::image-end:::  

### <span data-ttu-id="60a33-175">Afficher les attributs ARIA d’un élément</span><span class="sxs-lookup"><span data-stu-id="60a33-175">View the ARIA attributes of an element</span></span>   

<span data-ttu-id="60a33-176">Les attributs ARIA garantissent que les lecteurs d’écran disposent de toutes les informations dont ils ont besoin pour représenter correctement le contenu d’une page.</span><span class="sxs-lookup"><span data-stu-id="60a33-176">ARIA attributes ensure that screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="60a33-177">Affichez les attributs ARIA d’un élément dans le [volet accessibilité](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="60a33-177">View the ARIA attributes of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Section attributs ARIA" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   <span data-ttu-id="60a33-179">Section **attributs Aria**</span><span class="sxs-lookup"><span data-stu-id="60a33-179">The **ARIA Attributes** section</span></span>  
:::image-end:::  

### <span data-ttu-id="60a33-180">Afficher les propriétés d’accessibilité calculées d’un élément</span><span class="sxs-lookup"><span data-stu-id="60a33-180">View the computed accessibility properties of an element</span></span>   

> [!NOTE]
> <span data-ttu-id="60a33-181">Si vous recherchez des propriétés CSS calculées, voir l' [onglet calculé][DevtoolsCssReferenceViewActuallyAppliedElements].</span><span class="sxs-lookup"><span data-stu-id="60a33-181">If you are looking for computed CSS properties, see the [Computed tab][DevtoolsCssReferenceViewActuallyAppliedElements].</span></span>  

<span data-ttu-id="60a33-182">Certaines propriétés d’accessibilité sont calculées de manière dynamique par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="60a33-182">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="60a33-183">Ces propriétés sont affichées dans la section **propriétés calculées** du volet **accessibilité** .</span><span class="sxs-lookup"><span data-stu-id="60a33-183">These properties are displayed in the **Computed Properties** section of the **Accessibility** pane.</span></span>  

<span data-ttu-id="60a33-184">Afficher les propriétés d’accessibilité calculées d’un élément dans le [volet accessibilité](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="60a33-184">View the computed accessibility properties of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Section Propriétés calculées du volet accessibilité" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   <span data-ttu-id="60a33-186">Section **propriétés calculées** du volet **accessibilité**</span><span class="sxs-lookup"><span data-stu-id="60a33-186">The **Computed Properties** section of the **Accessibility** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="60a33-187">Afficher le coefficient de contraste d’un élément de texte dans le sélecteur de couleurs</span><span class="sxs-lookup"><span data-stu-id="60a33-187">View the contrast ratio of a text element in the Color Picker</span></span>   

<span data-ttu-id="60a33-188">Certaines personnes souffrant de troubles de la vue ne voient pas les zones comme très brillantes ou très sombres.</span><span class="sxs-lookup"><span data-stu-id="60a33-188">Some people with low vision do not see areas as very bright or very dark.</span></span>  <span data-ttu-id="60a33-189">Tout a tendance à apparaître à la même luminosité, ce qui permet de distinguer les plans et les bords.</span><span class="sxs-lookup"><span data-stu-id="60a33-189">Everything tends to appear at about the same brightness, which makes it hard to distinguish outlines and edges.</span></span>  
<span data-ttu-id="60a33-190">Coefficient de contraste mesure la différence de luminosité entre le premier plan et l’arrière-plan du texte.</span><span class="sxs-lookup"><span data-stu-id="60a33-190">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="60a33-191">Si votre texte a un coefficient de contraste faible, il est possible que les utilisateurs malvoyants puissent littéralement voir votre site comme un écran vierge.</span><span class="sxs-lookup"><span data-stu-id="60a33-191">If your text has a low contrast ratio, then these low vision users may literally experience your site as a blank screen.</span></span>  

<span data-ttu-id="60a33-192">Le sélecteur de couleurs permet de vérifier que votre texte répond aux niveaux de contraste recommandés:</span><span class="sxs-lookup"><span data-stu-id="60a33-192">The Color Picker helps you verify that your text meets recommended contrast ratio levels:</span></span>  

1.  <span data-ttu-id="60a33-193">Cliquez sur l’onglet **éléments** .</span><span class="sxs-lookup"><span data-stu-id="60a33-193">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="60a33-194">Dans l' **arborescence DOM**, sélectionnez l’élément de texte que vous voulez inspecter.</span><span class="sxs-lookup"><span data-stu-id="60a33-194">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Examen d’un paragraphe dans l’arborescence DOM" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       <span data-ttu-id="60a33-196">Examen d’un paragraphe dans l’arborescence DOM</span><span class="sxs-lookup"><span data-stu-id="60a33-196">Inspecting a paragraph in the DOM Tree</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="60a33-197">Dans le volet **styles** , cliquez sur le carré de couleur en regard de la `color` valeur de l’élément.</span><span class="sxs-lookup"><span data-stu-id="60a33-197">In the **Styles** pane, click the color square next to the `color` value of the element.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="La propriété Color de l’élément" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       <span data-ttu-id="60a33-199">La `color` propriété de l’élément</span><span class="sxs-lookup"><span data-stu-id="60a33-199">The `color` property of the element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="60a33-200">Vérifiez la section **coefficient de contraste** du sélecteur de couleurs.</span><span class="sxs-lookup"><span data-stu-id="60a33-200">Check the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="60a33-201">Une coche signifie que l’élément est conforme à la [recommandation minimum][W3CContrastMinimum].</span><span class="sxs-lookup"><span data-stu-id="60a33-201">One checkmark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="60a33-202">Deux coches signifient qu’il est conforme à la [recommandation améliorée][W3CContrastEnhanced].</span><span class="sxs-lookup"><span data-stu-id="60a33-202">Two checkmarks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="La section coefficient de contraste du sélecteur de couleurs affiche 2 coches et une valeur de 13,97" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       <span data-ttu-id="60a33-204">La section **coefficient de contraste** du sélecteur de couleurs affiche 2 coches et une valeur de</span><span class="sxs-lookup"><span data-stu-id="60a33-204">The **Contrast Ratio** section of the Color Picker shows 2 checkmarks and a value of</span></span> `13.97`  
    :::image-end:::  
    
1.  <span data-ttu-id="60a33-205">Cliquez sur la section **coefficient de contraste** pour afficher des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="60a33-205">Click the **Contrast Ratio** section to see more information.</span></span>  <span data-ttu-id="60a33-206">Une ligne s’affiche dans le sélecteur de visuels en haut du sélecteur de couleurs.</span><span class="sxs-lookup"><span data-stu-id="60a33-206">A line appears in the visual picker at the top of the Color Picker.</span></span>  <span data-ttu-id="60a33-207">Si la couleur actuelle répond aux recommandations, tout ce qui se trouve sur le même côté de la ligne répond également aux recommandations.</span><span class="sxs-lookup"><span data-stu-id="60a33-207">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="60a33-208">Si la couleur en cours ne répond pas aux recommandations, tout ce qui se trouve dans le même côté ne répond pas aux recommandations.</span><span class="sxs-lookup"><span data-stu-id="60a33-208">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Ligne de coefficient de contraste dans le sélecteur visuel" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       <span data-ttu-id="60a33-210">Ligne de coefficient de contraste dans le sélecteur visuel</span><span class="sxs-lookup"><span data-stu-id="60a33-210">The Contrast Ratio Line in the visual picker</span></span>  
    :::image-end:::  
    
<!--## Feedback   -->  



<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Navigation dans Microsoft Edge DevTools avec la technologie d’assistance | Documents sur le"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Afficher uniquement les feuilles CSS appliquées actuellement à une référence d’élément CSS | Documents Microsoft"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "axe-tests d’accessibilité sur le Web-chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Arborescence d’accessibilité (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Accessibilité | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Lecteur d’écran | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Niveau de contraste (amélioré) AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Contraste (minimum) niveau AA | W3C"  

> [!NOTE]
> <span data-ttu-id="60a33-219">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="60a33-219">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="60a33-220">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="60a33-220">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="60a33-222">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="60a33-222">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
