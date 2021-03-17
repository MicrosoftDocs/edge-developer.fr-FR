---
description: Référence complète des fonctionnalités d’accessibilité dans Microsoft Edge DevTools.
title: Référence d’accessibilité
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: fce6dec3883cbcc758780a9fedb4c0fb2a8d0a4c
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439253"
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

# <a name="accessibility-reference"></a><span data-ttu-id="0ef23-104">Référence d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="0ef23-104">Accessibility reference</span></span>  

<span data-ttu-id="0ef23-105">Cette page est une référence complète des fonctionnalités d’accessibilité dans Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="0ef23-105">This page is a comprehensive reference of accessibility features in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="0ef23-106">Il est destiné aux développeurs web qui :</span><span class="sxs-lookup"><span data-stu-id="0ef23-106">It is intended for web developers who:</span></span>  

*   <span data-ttu-id="0ef23-107">Avoir une connaissance de base de DevTools, par exemple comment l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="0ef23-107">Have a basic understanding of DevTools, such as how to open it.</span></span>  
*   <span data-ttu-id="0ef23-108">Familiarisez-vous [avec les principes d’accessibilité et les meilleures pratiques.][MDNAccessibility]</span><span class="sxs-lookup"><span data-stu-id="0ef23-108">Are familiar with [accessibility principles and best practices][MDNAccessibility].</span></span>  
    
<span data-ttu-id="0ef23-109">L’objectif de cette référence est de vous aider à découvrir tous les outils disponibles dans DevTools qui vous aident à examiner l’accessibilité d’une page.</span><span class="sxs-lookup"><span data-stu-id="0ef23-109">The purpose of this reference is to help you discover all of the tools available in DevTools that help you examine the accessibility of a page.</span></span>  

<span data-ttu-id="0ef23-110">Si vous recherchez de l’aide sur la navigation de DevTools avec une technologie d’assistance telle qu’un lecteur d’écran, accédez à Navigation dans [Microsoft Edge DevTools avec][DevtoolsAccessibilityNavigation]technologie d’assistance.</span><span class="sxs-lookup"><span data-stu-id="0ef23-110">If you are looking for help on navigating DevTools with an assistive technology like a screen reader, navigate to [Navigating Microsoft Edge DevTools With Assistive Technology][DevtoolsAccessibilityNavigation].</span></span>  

## <a name="overview-of-accessibility-features-in-microsoft-edge-devtools"></a><span data-ttu-id="0ef23-111">Vue d’ensemble des fonctionnalités d’accessibilité dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0ef23-111">Overview of accessibility features in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="0ef23-112">Cette section explique comment DevTools s’inscrit dans votre kit de ressources d’accessibilité global.</span><span class="sxs-lookup"><span data-stu-id="0ef23-112">This section explains how DevTools fits into your overall accessibility toolkit.</span></span>  

<span data-ttu-id="0ef23-113">Lorsque vous déterminez si une page est accessible, vous devez avoir 2 questions générales à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="0ef23-113">When determining whether a page is accessible, you need to have 2 general questions in mind:</span></span>  

1.  <span data-ttu-id="0ef23-114">Êtes-vous en mesure de naviguer dans la page à l’aide d’un clavier ou [d’un lecteur d’écran][MDNScreenReader]?</span><span class="sxs-lookup"><span data-stu-id="0ef23-114">Are you able to navigate the page with a keyboard or [screen reader][MDNScreenReader]?</span></span>  
1.  <span data-ttu-id="0ef23-115">Les éléments de la page sont-ils correctement marqués pour les lecteurs d’écran ?</span><span class="sxs-lookup"><span data-stu-id="0ef23-115">Are the elements of the page properly marked up for screen readers?</span></span>  
    
<span data-ttu-id="0ef23-116">En règle générale, DevTools doit vous aider à résoudre les erreurs liées aux #2, car ces erreurs sont faciles à détecter de manière automatisée.</span><span class="sxs-lookup"><span data-stu-id="0ef23-116">In general, DevTools should help you fix errors related to question #2, because these errors are easy to detect in an automated fashion.</span></span>  <span data-ttu-id="0ef23-117">La question #1 est tout aussi importante, mais malheureusement, DevTools ne vous aide pas.</span><span class="sxs-lookup"><span data-stu-id="0ef23-117">Question #1 is just as important, but unfortunately DevTools does not help you there.</span></span>  <span data-ttu-id="0ef23-118">La seule façon de rechercher les erreurs liées aux #1 question consiste à essayer d’utiliser une page avec un clavier ou un lecteur d’écran vous-même.</span><span class="sxs-lookup"><span data-stu-id="0ef23-118">The only way to find errors related to question #1 is to try using a page with a keyboard or screen reader yourself.</span></span>  <!--To learn more, navigate to [How To Do An Accessibility Review][AccessibilityReview].  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <a name="audit-the-accessibility-of-a-page"></a><span data-ttu-id="0ef23-119">Auditer l’accessibilité d’une page</span><span class="sxs-lookup"><span data-stu-id="0ef23-119">Audit the accessibility of a page</span></span>  

> [!NOTE]
> <span data-ttu-id="0ef23-120">**L’outil Audits** fournit des liens vers du contenu hébergé sur des sites web tiers.</span><span class="sxs-lookup"><span data-stu-id="0ef23-120">The **Audits** tool provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="0ef23-121">Microsoft n’est pas responsable et n’a aucun contrôle sur le contenu de ces sites et les données qui peuvent être collectées.</span><span class="sxs-lookup"><span data-stu-id="0ef23-121">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="0ef23-122">En règle générale, utilisez le panneau Audits pour déterminer si :</span><span class="sxs-lookup"><span data-stu-id="0ef23-122">In general, use the Audits panel to determine if:</span></span>  

*   <span data-ttu-id="0ef23-123">Une page est correctement marquée pour les lecteurs d’écran.</span><span class="sxs-lookup"><span data-stu-id="0ef23-123">A page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="0ef23-124">Les éléments de texte d’une page ont des coefficients de contraste suffisants.</span><span class="sxs-lookup"><span data-stu-id="0ef23-124">The text elements on a page have sufficient contrast ratios.</span></span>  <span data-ttu-id="0ef23-125">Accédez [à Afficher le coefficient de contraste d’un élément de texte dans le s sélectionneur de couleurs.](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker)</span><span class="sxs-lookup"><span data-stu-id="0ef23-125">Navigate to [View the contrast ratio of a text element in the Color Picker](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span></span>  

<span data-ttu-id="0ef23-126">Pour auditer une page :</span><span class="sxs-lookup"><span data-stu-id="0ef23-126">To audit a page:</span></span>  

1.  <span data-ttu-id="0ef23-127">Accédez à l’URL que vous souhaitez auditer.</span><span class="sxs-lookup"><span data-stu-id="0ef23-127">Navigate to the URL that you want to audit.</span></span>  
1.  <span data-ttu-id="0ef23-128">Dans DevTools, choisissez **l’outil Audits.**</span><span class="sxs-lookup"><span data-stu-id="0ef23-128">In DevTools, choose the **Audits** tool.</span></span>  <span data-ttu-id="0ef23-129">DevTools vous présente différentes options de configuration.</span><span class="sxs-lookup"><span data-stu-id="0ef23-129">DevTools shows you various configuration options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Configurer les audits" lightbox="../media/accessibility-audits-pane.msft.png":::
       <span data-ttu-id="0ef23-131">Configurer les audits</span><span class="sxs-lookup"><span data-stu-id="0ef23-131">Configure audits</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="0ef23-132">Les captures d’écran de cette section ont été prises avec Microsoft Edge version 79.</span><span class="sxs-lookup"><span data-stu-id="0ef23-132">The screenshots in this section were taken with Microsoft Edge version 79.</span></span>  <span data-ttu-id="0ef23-133">Vous pouvez vérifier la version à partir de quelle version vous `edge://version` exécutez.</span><span class="sxs-lookup"><span data-stu-id="0ef23-133">You may check what version you are running at `edge://version`.</span></span>  <span data-ttu-id="0ef23-134">L’interface utilisateur de l’outil **Audits** est différente dans les versions antérieures de Microsoft Edge, mais le flux de travail général est le même.</span><span class="sxs-lookup"><span data-stu-id="0ef23-134">The **Audits** tool UI looks different in earlier versions of Microsoft Edge, but the general workflow is the same.</span></span>  
    
1.  <span data-ttu-id="0ef23-135">Pour **l’appareil,** **choisissez Mobile** si vous souhaitez simuler un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="0ef23-135">For **Device**, choose **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="0ef23-136">Cette option modifie la chaîne de votre agent utilisateur et resize laport d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0ef23-136">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="0ef23-137">Si la version mobile de la page s’affiche différemment de la version de bureau, cette option peut avoir un impact significatif sur les résultats de votre audit.</span><span class="sxs-lookup"><span data-stu-id="0ef23-137">If the mobile version of the page displays differently than the desktop version, this option may have a significant effect on the results of your audit.</span></span>  
1.  <span data-ttu-id="0ef23-138">Dans la section **Audits,** assurez-vous que **l’accessibilité** est activée.</span><span class="sxs-lookup"><span data-stu-id="0ef23-138">In the **Audits** section, make sure that **Accessibility** is enabled.</span></span>  <span data-ttu-id="0ef23-139">Désactivez les autres catégories si vous souhaitez les exclure de votre rapport.</span><span class="sxs-lookup"><span data-stu-id="0ef23-139">Disable the other categories if you want to exclude them from your report.</span></span>  <span data-ttu-id="0ef23-140">Laissez-les activées si vous souhaitez découvrir d’autres façons d’améliorer la qualité de votre page.</span><span class="sxs-lookup"><span data-stu-id="0ef23-140">Leave them enabled if you want to discover other ways to improve the quality of your page.</span></span>  
1.  <span data-ttu-id="0ef23-141">La section **Limitation vous** permet de limiter le réseau et le processeur, ce qui est utile lors de l’analyse des performances de charge.</span><span class="sxs-lookup"><span data-stu-id="0ef23-141">The **Throttling** section lets you throttle the network and CPU, which is useful when analyzing load performance.</span></span>  <span data-ttu-id="0ef23-142">Cette option ne doit pas être pertinente pour votre score d’accessibilité. Vous pouvez donc utiliser ce que vous préférez.</span><span class="sxs-lookup"><span data-stu-id="0ef23-142">This option should be irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="0ef23-143">La **case à cocher** Effacer le stockage vous permet d’effacer tout le stockage avant de charger la page ou de conserver le stockage entre les chargements de page.</span><span class="sxs-lookup"><span data-stu-id="0ef23-143">The **Clear Storage** checkbox lets you clear all storage before loading the page, or preserve storage between page loads.</span></span>  <span data-ttu-id="0ef23-144">Cette option n’est probablement pas pertinente pour votre score d’accessibilité. Vous pouvez donc utiliser ce que vous préférez.</span><span class="sxs-lookup"><span data-stu-id="0ef23-144">This option is also probably irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="0ef23-145">Choose **Run Audits**.</span><span class="sxs-lookup"><span data-stu-id="0ef23-145">Choose **Run Audits**.</span></span> <span data-ttu-id="0ef23-146">Après 10 à 30 secondes, DevTools fournit un rapport.</span><span class="sxs-lookup"><span data-stu-id="0ef23-146">After 10 to 30 seconds, DevTools provides a report.</span></span>  <span data-ttu-id="0ef23-147">Votre rapport vous donne différents conseils sur l’amélioration de l’accessibilité de la page.</span><span class="sxs-lookup"><span data-stu-id="0ef23-147">Your report gives you various tips on how to improve the accessibility of the page.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Un rapport" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       <span data-ttu-id="0ef23-149">Un rapport</span><span class="sxs-lookup"><span data-stu-id="0ef23-149">A report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0ef23-150">Choisissez un audit pour en savoir plus à ce sujet.</span><span class="sxs-lookup"><span data-stu-id="0ef23-150">Choose an audit to learn more about it.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Plus d’informations sur un audit" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       <span data-ttu-id="0ef23-152">Plus d’informations sur un audit</span><span class="sxs-lookup"><span data-stu-id="0ef23-152">More information about an audit</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0ef23-153">Sélectionnez **En savoir plus** pour afficher la documentation de cet audit.</span><span class="sxs-lookup"><span data-stu-id="0ef23-153">Choose **Learn More** to view the documentation of that audit.</span></span>  
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Afficher la documentation d’un audit" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       <span data-ttu-id="0ef23-155">Afficher la documentation d’un audit</span><span class="sxs-lookup"><span data-stu-id="0ef23-155">View the documentation of an audit</span></span>  
    :::image-end:::  
    
### <a name="see-also-axe-extension"></a><span data-ttu-id="0ef23-156">Voir aussi : extension aXe</span><span class="sxs-lookup"><span data-stu-id="0ef23-156">See also: aXe extension</span></span>  

<span data-ttu-id="0ef23-157">Vous pouvez préférer utiliser [l’extension aXe plutôt][ChromeWebStoreAxe] que l’outil **Audits.**</span><span class="sxs-lookup"><span data-stu-id="0ef23-157">You may prefer to use the [aXe extension][ChromeWebStoreAxe] rather than the **Audits** tool.</span></span>  
<span data-ttu-id="0ef23-158">L’extension aXe fournit généralement les mêmes informations, car il s’agit du moteur sous-jacent qui alimente le panneau Audits.</span><span class="sxs-lookup"><span data-stu-id="0ef23-158">The aXe extension generally provides the same information, since it is the underlying engine that powers the Audits panel.</span></span>  <span data-ttu-id="0ef23-159">L’extension aXe a une interface utilisateur différente et décrit les audits légèrement différemment.</span><span class="sxs-lookup"><span data-stu-id="0ef23-159">The aXe extension has a different UI and describes audits slightly differently.</span></span>  
<span data-ttu-id="0ef23-160">L’un des avantages de l’extension aXe par rapport à l’outil **Audits** est qu’elle vous permet d’inspecter et de mettre en surbrillez les points d’échec.</span><span class="sxs-lookup"><span data-stu-id="0ef23-160">One advantage that the aXe extension has over the **Audits** tool is that it enables you to inspect and highlight failing nodes.</span></span>  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="Extension aXe" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   <span data-ttu-id="0ef23-162">Extension aXe</span><span class="sxs-lookup"><span data-stu-id="0ef23-162">The aXe extension</span></span>  
:::image-end:::  

## <a name="the-accessibility-panel"></a><span data-ttu-id="0ef23-163">Panneau Accessibilité</span><span class="sxs-lookup"><span data-stu-id="0ef23-163">The Accessibility panel</span></span>  

<span data-ttu-id="0ef23-164">Le **panneau Accessibilité** vous permet d’afficher l’arborescence d’accessibilité, les attributs ARIA et les propriétés d’accessibilité calculées des nodes DOM.</span><span class="sxs-lookup"><span data-stu-id="0ef23-164">The **Accessibility** panel is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="0ef23-165">Pour ouvrir le panneau **Accessibilité** :</span><span class="sxs-lookup"><span data-stu-id="0ef23-165">To open the **Accessibility** panel:</span></span>  

1.  <span data-ttu-id="0ef23-166">Choisissez **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="0ef23-166">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="0ef23-167">Dans **l’arborescence DOM,** sélectionnez l’élément que vous souhaitez inspecter.</span><span class="sxs-lookup"><span data-stu-id="0ef23-167">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="0ef23-168">Choisissez le **panneau Accessibilité.**</span><span class="sxs-lookup"><span data-stu-id="0ef23-168">Choose the **Accessibility** panel.</span></span>  <span data-ttu-id="0ef23-169">Ce panneau peut être masqué derrière le bouton **Autres onglets** \( ![ Autres onglets ](../media/more-tabs-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="0ef23-169">This panel may be hidden behind the **More Tabs** \(![More Tabs](../media/more-tabs-icon.msft.png)\) button.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Inspecter l’élément h1 de la page d’accueil DevTools dans le panneau Accessibilité" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   <span data-ttu-id="0ef23-171">Inspecter `h1` l’élément de la page d’accueil DevTools dans le **panneau Accessibilité**</span><span class="sxs-lookup"><span data-stu-id="0ef23-171">Inspect the `h1` element of the DevTools homepage in the **Accessibility** panel</span></span>  
:::image-end:::  

### <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a><span data-ttu-id="0ef23-172">Afficher la position d’un élément dans l’arborescence d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="0ef23-172">View the position of an element in the accessibility tree</span></span>  

<span data-ttu-id="0ef23-173">[L’arborescence d’accessibilité][MDNAccessibilityTree] est un sous-ensemble de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="0ef23-173">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="0ef23-174">Il contient uniquement les éléments de l’arborescence DOM qui sont pertinents et utiles pour afficher le contenu d’une page dans un lecteur d’écran.</span><span class="sxs-lookup"><span data-stu-id="0ef23-174">It only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  

<span data-ttu-id="0ef23-175">Inspectez la position d’un élément dans l’arborescence d’accessibilité à partir du [panneau Accessibilité.](#the-accessibility-panel)</span><span class="sxs-lookup"><span data-stu-id="0ef23-175">Inspect the position of an element in the accessibility tree from the [Accessibility](#the-accessibility-panel) panel.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Section Arborescence de l’accessibilité" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   <span data-ttu-id="0ef23-177">Section Arborescence **de l’accessibilité**</span><span class="sxs-lookup"><span data-stu-id="0ef23-177">The **Accessibility Tree** section</span></span>  
:::image-end:::  

### <a name="view-the-aria-attributes-of-an-element"></a><span data-ttu-id="0ef23-178">Afficher les attributs ARIA d’un élément</span><span class="sxs-lookup"><span data-stu-id="0ef23-178">View the ARIA attributes of an element</span></span>  

<span data-ttu-id="0ef23-179">Les attributs ARIA garantissent que les lecteurs d’écran ont toutes les informations dont ils ont besoin pour représenter correctement le contenu d’une page.</span><span class="sxs-lookup"><span data-stu-id="0ef23-179">ARIA attributes ensure that screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="0ef23-180">Afficher les attributs ARIA d’un élément dans le [panneau Accessibilité.](#the-accessibility-panel)</span><span class="sxs-lookup"><span data-stu-id="0ef23-180">View the ARIA attributes of an element in the [Accessibility](#the-accessibility-panel) panel.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Section Attributs ARIA" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   <span data-ttu-id="0ef23-182">Section **Attributs ARIA**</span><span class="sxs-lookup"><span data-stu-id="0ef23-182">The **ARIA Attributes** section</span></span>  
:::image-end:::  

### <a name="view-the-computed-accessibility-properties-of-an-element"></a><span data-ttu-id="0ef23-183">Afficher les propriétés d’accessibilité calculées d’un élément</span><span class="sxs-lookup"><span data-stu-id="0ef23-183">View the computed accessibility properties of an element</span></span>  

> [!NOTE]
> <span data-ttu-id="0ef23-184">Si vous recherchez des propriétés CSS calculées, accédez au [panneau][DevtoolsCssReferenceViewActuallyAppliedElements] calculé.</span><span class="sxs-lookup"><span data-stu-id="0ef23-184">If you are looking for computed CSS properties, navigate to [Computed][DevtoolsCssReferenceViewActuallyAppliedElements] panel.</span></span>  

<span data-ttu-id="0ef23-185">Certaines propriétés d’accessibilité sont calculées dynamiquement par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="0ef23-185">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="0ef23-186">Ces propriétés sont affichées dans la section **Propriétés** calculées du panneau **Accessibilité.**</span><span class="sxs-lookup"><span data-stu-id="0ef23-186">These properties are displayed in the **Computed Properties** section of the **Accessibility** panel.</span></span>  

<span data-ttu-id="0ef23-187">Afficher les propriétés d’accessibilité calculées d’un élément dans le [panneau Accessibilité.](#the-accessibility-panel)</span><span class="sxs-lookup"><span data-stu-id="0ef23-187">View the computed accessibility properties of an element in the [Accessibility](#the-accessibility-panel) panel.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Section Propriétés calculées du panneau Accessibilité" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   <span data-ttu-id="0ef23-189">Section **Propriétés calculées** du panneau **Accessibilité**</span><span class="sxs-lookup"><span data-stu-id="0ef23-189">The **Computed Properties** section of the **Accessibility** panel</span></span>  
:::image-end:::  

## <a name="view-the-contrast-ratio-of-a-text-element-in-the-color-picker"></a><span data-ttu-id="0ef23-190">Afficher le coefficient de contraste d’un élément de texte dans le s sélectionneur de couleurs</span><span class="sxs-lookup"><span data-stu-id="0ef23-190">View the contrast ratio of a text element in the Color Picker</span></span>  

<span data-ttu-id="0ef23-191">Certaines personnes ayant une vision faible ne voient pas les zones comme étant très claires ou très sombres.</span><span class="sxs-lookup"><span data-stu-id="0ef23-191">Some people with low vision do not see areas as very bright or very dark.</span></span>  <span data-ttu-id="0ef23-192">Tout a tendance à apparaître à peu près à la même luminosité, ce qui rend difficile la distinction entre les contours et les bords.</span><span class="sxs-lookup"><span data-stu-id="0ef23-192">Everything tends to appear at about the same brightness, which makes it hard to distinguish outlines and edges.</span></span>  

<span data-ttu-id="0ef23-193">Le coefficient de contraste mesure la différence de luminosité entre le premier plan et l’arrière-plan du texte.</span><span class="sxs-lookup"><span data-stu-id="0ef23-193">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="0ef23-194">Si votre texte présente un faible coefficient de contraste, ces utilisateurs à faible vision peuvent littéralement voir votre site comme un écran vide.</span><span class="sxs-lookup"><span data-stu-id="0ef23-194">If your text has a low contrast ratio, then these low vision users may literally experience your site as a blank screen.</span></span>  

<span data-ttu-id="0ef23-195">Le s picker de couleur vous permet de vérifier que votre texte répond aux niveaux de coefficient de contraste recommandés :</span><span class="sxs-lookup"><span data-stu-id="0ef23-195">The Color Picker helps you verify that your text meets recommended contrast ratio levels:</span></span>  

1.  <span data-ttu-id="0ef23-196">Choisissez **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="0ef23-196">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="0ef23-197">Dans **l’arborescence DOM,** sélectionnez l’élément de texte à inspecter.</span><span class="sxs-lookup"><span data-stu-id="0ef23-197">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Inspecter un paragraphe dans l’arborescence DOM" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       <span data-ttu-id="0ef23-199">Inspecter un paragraphe dans l’arborescence **DOM**</span><span class="sxs-lookup"><span data-stu-id="0ef23-199">Inspect a paragraph in the **DOM Tree**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0ef23-200">Dans le **panneau Styles,** choisissez le carré de couleur en face de la `color` valeur de l’élément.</span><span class="sxs-lookup"><span data-stu-id="0ef23-200">In the **Styles** panel, choose the color square next to the `color` value of the element.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="Propriété de couleur de l’élément" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       <span data-ttu-id="0ef23-202">Propriété `color` de l’élément</span><span class="sxs-lookup"><span data-stu-id="0ef23-202">The `color` property of the element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0ef23-203">Consultez la section **Coefficient de** contraste du s sélectionneur de couleurs.</span><span class="sxs-lookup"><span data-stu-id="0ef23-203">Check the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="0ef23-204">Une coche signifie que l’élément répond à la [recommandation minimale.][W3CContrastMinimum]</span><span class="sxs-lookup"><span data-stu-id="0ef23-204">One checkmark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="0ef23-205">Deux coches signifient qu’elle répond à la [recommandation améliorée][W3CContrastEnhanced].</span><span class="sxs-lookup"><span data-stu-id="0ef23-205">Two checkmarks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="La section Coefficient de contraste du s picker de couleur affiche 2 coches et une valeur de 13,97" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       <span data-ttu-id="0ef23-207">La section **Coefficient de** contraste du s picker de couleur affiche 2 coches et une valeur de</span><span class="sxs-lookup"><span data-stu-id="0ef23-207">The **Contrast Ratio** section of the Color Picker shows 2 checkmarks and a value of</span></span> `13.97`  
    :::image-end:::  
    
1.  <span data-ttu-id="0ef23-208">Pour plus d’informations, sélectionnez la section **Coefficient de** contraste.</span><span class="sxs-lookup"><span data-stu-id="0ef23-208">For more information, choose the **Contrast Ratio** section.</span></span>  <span data-ttu-id="0ef23-209">Une ligne apparaît dans le s picker visuel en haut du s picker de couleurs.</span><span class="sxs-lookup"><span data-stu-id="0ef23-209">A line appears in the visual picker at the top of the Color Picker.</span></span>  <span data-ttu-id="0ef23-210">Si la couleur actuelle répond aux recommandations, tout ce qui se place du même côté de la ligne répond également à des recommandations.</span><span class="sxs-lookup"><span data-stu-id="0ef23-210">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="0ef23-211">Si la couleur actuelle ne répond pas aux recommandations, tout ce qui se présente du même côté ne répond pas non plus aux recommandations.</span><span class="sxs-lookup"><span data-stu-id="0ef23-211">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Ligne coefficient de contraste dans le s picker visuel" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       <span data-ttu-id="0ef23-213">Ligne **coefficient de contraste** dans le s picker visuel</span><span class="sxs-lookup"><span data-stu-id="0ef23-213">The **Contrast Ratio** Line in the visual picker</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="0ef23-214">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="0ef23-214">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Naviguer dans Microsoft Edge DevTools avec la technologie d’assistance | Documents Microsoft"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Afficher uniquement le CSS réellement appliqué à un élément - CSS Reference | Documents Microsoft"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "axe - Test d’accessibilité web - Chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Arborescence d’accessibilité (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Accessibilité | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Lecteur d’écran | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Contraste (amélioré) Niveau AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Contraste (Minimum) Niveau AA | W3C"  

> [!NOTE]
> <span data-ttu-id="0ef23-223">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0ef23-223">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0ef23-224">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="0ef23-224">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="0ef23-226">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0ef23-226">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
