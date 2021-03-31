---
description: Découvrez comment utiliser Microsoft Edge DevTools pour afficher et modifier le CSS d’une page.
title: Prise en main de l’affichage et de la modification de CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: b3d19d34f329fec7a3903fb37e8be3558ba4d31d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399091"
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

# <a name="get-started-with-viewing-and-changing-css"></a><span data-ttu-id="c8367-104">Prise en main de l’affichage et de la modification de CSS</span><span class="sxs-lookup"><span data-stu-id="c8367-104">Get started with viewing and changing CSS</span></span>  

<span data-ttu-id="c8367-105">Complétez ces didacticiels interactifs pour découvrir les principes de base de l’affichage et de la modification du CSS d’une page à l’aide de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="c8367-105">Complete these interactive tutorials to learn the basics of viewing and changing the CSS for a page using Microsoft Edge DevTools.</span></span>  

## <a name="open-css-examples"></a><span data-ttu-id="c8367-106">Exemples open CSS</span><span class="sxs-lookup"><span data-stu-id="c8367-106">Open CSS Examples</span></span>  

1.  <span data-ttu-id="c8367-107">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **CSS Examples** to open in a new window.</span><span class="sxs-lookup"><span data-stu-id="c8367-107">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **CSS Examples** to open in a new window.</span></span>  
    
    [<span data-ttu-id="c8367-108">Exemples CSS</span><span class="sxs-lookup"><span data-stu-id="c8367-108">CSS Examples</span></span>][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > <span data-ttu-id="c8367-109">Si vous souhaitez ancrer votre [fenêtre DevTools][DevToolsCustomizePlacement] à droite de votre fenêtre d’affichage \(affichée dans la figure suivante\), choisissez Personnaliser et contrôler **DevTools.** `...`</span><span class="sxs-lookup"><span data-stu-id="c8367-109">If you want to [dock your DevTools window][DevToolsCustomizePlacement] to the right of your viewport \(displayed in the following figure\), choose **Customize and control DevTools** `...`.</span></span>  <span data-ttu-id="c8367-110">On the **Customize and control DevTools** drop-down menu, in the **Dock side** section, choose Dock **to right**.</span><span class="sxs-lookup"><span data-stu-id="c8367-110">On the **Customize and control DevTools** drop-down menu, in the **Dock side** section, choose **Dock to right**.</span></span>  
    
## <a name="view-the-css-for-an-element"></a><span data-ttu-id="c8367-111">Afficher le CSS d’un élément</span><span class="sxs-lookup"><span data-stu-id="c8367-111">View the CSS for an element</span></span>  

1.  <span data-ttu-id="c8367-112">[Ouvrez des exemples CSS.](#open-css-examples)</span><span class="sxs-lookup"><span data-stu-id="c8367-112">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="c8367-113">Pointez sur `Inspect Me!` le texte, ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.</span><span class="sxs-lookup"><span data-stu-id="c8367-113">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="c8367-114">Dans DevTools, sur l’outil **Elements,** dans le panneau Arborescence **DOM,** l’élément `Inspect Me!` est mis en surbrillrillant.</span><span class="sxs-lookup"><span data-stu-id="c8367-114">In DevTools, on the **Elements** tool, in the **DOM Tree** panel, the `Inspect Me!` element is highlighted.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="L’élément inspecté est mis en surbrillant dans l’arborescence DOM" lightbox="../media/css-elements-inspect-me.msft.png":::
           <span data-ttu-id="c8367-116">L’élément inspecté est mis en surbrillant dans l’arborescence **DOM**</span><span class="sxs-lookup"><span data-stu-id="c8367-116">The inspected element is highlighted in the **DOM Tree**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="c8367-117">Dans `Inspect Me!` l’élément, recherchez la valeur de `data-message` l’attribut et copiez-la.</span><span class="sxs-lookup"><span data-stu-id="c8367-117">In the `Inspect Me!` element, find the value of the `data-message` attribute and copy it.</span></span>  
1.  <span data-ttu-id="c8367-118">Sur la page, dans la **boîte de texte Valeur de `data-message` :** , entrez la valeur.</span><span class="sxs-lookup"><span data-stu-id="c8367-118">On the page, in the **Value of `data-message`:** textbox, enter the value.</span></span>  
1.  <span data-ttu-id="c8367-119">Pointez sur `Inspect Me!` le texte, ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.</span><span class="sxs-lookup"><span data-stu-id="c8367-119">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="c8367-120">Dans DevTools, dans l’outil **Éléments,** sélectionnez le **panneau Styles.**</span><span class="sxs-lookup"><span data-stu-id="c8367-120">In DevTools, on the **Elements** tool, select the **Styles** panel.</span></span>  
    1.  <span data-ttu-id="c8367-121">Dans le **panneau Styles,** `Inspect Me!` l’élément est mis en surbrillant.</span><span class="sxs-lookup"><span data-stu-id="c8367-121">In the **Styles** panel, the `Inspect Me!` element is highlighted.</span></span>  
    1.  <span data-ttu-id="c8367-122">Dans `Inspect Me!` l’élément, recherchez la `aloha` règle de classe.</span><span class="sxs-lookup"><span data-stu-id="c8367-122">In the `Inspect Me!` element, find the `aloha` class rule.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="c8367-123">Cette règle s’affiche, car elle est appliquée à `Inspect Me!` l’élément.</span><span class="sxs-lookup"><span data-stu-id="c8367-123">This rule is displayed, because it is being applied to the `Inspect Me!` element.</span></span>  
        
    1.  <span data-ttu-id="c8367-124">Dans la `aloha` classe, recherchez la valeur du `padding` style et copiez-la.</span><span class="sxs-lookup"><span data-stu-id="c8367-124">In the `aloha` class, find the value for the `padding` style and copy it.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="Les classes CSS sont appliquées à l’élément inspecté sont mises en surbrill" lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           <span data-ttu-id="c8367-126">Les classes CSS sont appliquées à l’élément sélectionné, par exemple, sont affichées dans le `aloha` **panneau Styles**</span><span class="sxs-lookup"><span data-stu-id="c8367-126">CSS classes is applied to the selected element, such as `aloha`, are displayed in the **Styles** panel</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="c8367-127">Sur la page, dans la **boîte de texte Valeur de `padding` :** , entrez la valeur.</span><span class="sxs-lookup"><span data-stu-id="c8367-127">On the page, in the **Value of `padding`:** textbox, enter the value.</span></span>  

## <a name="add-a-css-declaration-to-an-element"></a><span data-ttu-id="c8367-128">Ajouter une déclaration CSS à un élément</span><span class="sxs-lookup"><span data-stu-id="c8367-128">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="c8367-129">Utilisez le **panneau Styles** lorsque vous souhaitez modifier ou ajouter des déclarations CSS à un élément.</span><span class="sxs-lookup"><span data-stu-id="c8367-129">Use the **Styles** panel when you want to change or add CSS declarations to an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="c8367-130">Complétez le didacticiel [Afficher les CSS d’un](#view-the-css-for-an-element) élément avant de le faire.</span><span class="sxs-lookup"><span data-stu-id="c8367-130">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="c8367-131">[Ouvrez des exemples CSS.](#open-css-examples)</span><span class="sxs-lookup"><span data-stu-id="c8367-131">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="c8367-132">Pointez sur `Add A Background Color To Me!` le texte, ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.</span><span class="sxs-lookup"><span data-stu-id="c8367-132">Hover on the `Add A Background Color To Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="c8367-133">Choisissez `element.style` en haut du panneau **Styles.**</span><span class="sxs-lookup"><span data-stu-id="c8367-133">Choose `element.style` near the top of the **Styles** panel.</span></span>  
1.  <span data-ttu-id="c8367-134">Tapez `background-color` et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c8367-134">Type `background-color` and select `Enter`.</span></span>  
1.  <span data-ttu-id="c8367-135">Tapez `honeydew` et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c8367-135">Type `honeydew` and select `Enter`.</span></span>  <span data-ttu-id="c8367-136">Dans **l’arborescence DOM,** une déclaration de style inline appliquée à l’élément s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c8367-136">In the **DOM Tree**, an inline style declaration applied to the element is displayed.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Ajouter une déclaration CSS à l’élément à l’aide du panneau Styles" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       <span data-ttu-id="c8367-138">La `background-color:honeydew` déclaration est appliquée à l’élément à l’aide de la section du panneau `element.style` **Styles**</span><span class="sxs-lookup"><span data-stu-id="c8367-138">The `background-color:honeydew` declaration is applied to the element using the `element.style` section of the **Styles** panel</span></span>  
    :::image-end:::  
    
## <a name="add-a-css-class-to-an-element"></a><span data-ttu-id="c8367-139">Ajouter une classe CSS à un élément</span><span class="sxs-lookup"><span data-stu-id="c8367-139">Add a CSS class to an element</span></span>  

<span data-ttu-id="c8367-140">Pour afficher l’apparence d’un élément lorsqu’une classe CSS est appliquée à un élément ou supprimée d’un élément, accédez au **panneau Styles.**</span><span class="sxs-lookup"><span data-stu-id="c8367-140">To display how an element looks when a CSS class is applied to or removed from an element, navigate to the **Styles** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="c8367-141">Complétez le didacticiel [Afficher les CSS d’un](#view-the-css-for-an-element) élément avant de le faire.</span><span class="sxs-lookup"><span data-stu-id="c8367-141">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="c8367-142">[Ouvrez des exemples CSS.](#open-css-examples)</span><span class="sxs-lookup"><span data-stu-id="c8367-142">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="c8367-143">Pointez sur `Add A Class To Me!` le texte, ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.</span><span class="sxs-lookup"><span data-stu-id="c8367-143">Hover on the `Add A Class To Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="c8367-144">Choisissez **.cls**.</span><span class="sxs-lookup"><span data-stu-id="c8367-144">Choose **.cls**.</span></span>  <span data-ttu-id="c8367-145">DevTools révèle une zone de texte dans laquelle vous pouvez ajouter des classes à l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c8367-145">DevTools reveals a text box where you may add classes to the selected element.</span></span>  
1.  <span data-ttu-id="c8367-146">Tapez dans la zone de texte Ajouter une nouvelle `color_me` classe, puis  sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c8367-146">Type `color_me` in the **Add new class** text box and then select `Enter`.</span></span>  <span data-ttu-id="c8367-147">Une case à cocher s’affiche sous la **zone** de texte Ajouter une nouvelle classe, dans laquelle vous pouvez l’élémenter ou le désébaser.</span><span class="sxs-lookup"><span data-stu-id="c8367-147">A checkbox appears below the **Add new class** text box, where you may toggle the class on and off.</span></span>  <span data-ttu-id="c8367-148">Si d’autres classes sont appliquées à l’élément, vous pouvez également les faire basculer `Add A Class To Me!` à partir d’ici.</span><span class="sxs-lookup"><span data-stu-id="c8367-148">If the `Add A Class To Me!` element has any other classes applied to it, you are also able to toggle each from here.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Appliquer la color_me classe à l’élément" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       <span data-ttu-id="c8367-150">La `color_me` classe est appliquée à l’élément à l’aide de la section **.cls** du **panneau Styles**</span><span class="sxs-lookup"><span data-stu-id="c8367-150">The `color_me` class is applied to the element using the **.cls** section of the **Styles** panel</span></span>  
    :::image-end:::  
    
## <a name="add-a-pseudostate-to-a-class"></a><span data-ttu-id="c8367-151">Ajouter un pseudo-état à une classe</span><span class="sxs-lookup"><span data-stu-id="c8367-151">Add a pseudostate to a class</span></span>  

<span data-ttu-id="c8367-152">Utilisez le **panneau Styles** pour appliquer définitivement un pseudo-état CSS à un élément.</span><span class="sxs-lookup"><span data-stu-id="c8367-152">Use the **Styles** panel to permanently apply a CSS pseudostate to an element.</span></span>  <span data-ttu-id="c8367-153">DevTools prend `:active` en charge , et `:focus` `:hover` `:visited` .</span><span class="sxs-lookup"><span data-stu-id="c8367-153">DevTools supports `:active`, `:focus`, `:hover`, and `:visited`.</span></span>  

> [!NOTE]
> <span data-ttu-id="c8367-154">Complétez le didacticiel [Afficher les CSS d’un](#view-the-css-for-an-element) élément avant de le faire.</span><span class="sxs-lookup"><span data-stu-id="c8367-154">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="c8367-155">[Ouvrez des exemples CSS.](#open-css-examples)</span><span class="sxs-lookup"><span data-stu-id="c8367-155">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="c8367-156">Pointez sur le `Hover Over Me!` texte.</span><span class="sxs-lookup"><span data-stu-id="c8367-156">Hover on the `Hover Over Me!` text.</span></span>  <span data-ttu-id="c8367-157">La couleur d’arrière-plan change.</span><span class="sxs-lookup"><span data-stu-id="c8367-157">The background color changes.</span></span>  
1.  <span data-ttu-id="c8367-158">Pointez sur `Hover Over Me!` le texte, ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.</span><span class="sxs-lookup"><span data-stu-id="c8367-158">Hover on the `Hover Over Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="c8367-159">Dans le **panneau Styles,** choisissez **:hov**.</span><span class="sxs-lookup"><span data-stu-id="c8367-159">In the **Styles** panel, choose **:hov**.</span></span>  
1.  <span data-ttu-id="c8367-160">Cochez **la case :hover.**</span><span class="sxs-lookup"><span data-stu-id="c8367-160">Check the **:hover** checkbox.</span></span>  <span data-ttu-id="c8367-161">La couleur d’arrière-plan change comme avant, même si vous ne pointez pas réellement sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="c8367-161">The background color changes like before, even though you are not actually hovering over the element.</span></span>  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Basculez le pseudo-état de pointage sur un élément" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       <span data-ttu-id="c8367-163">Basculez le `:hover` pseudo-état sur un élément</span><span class="sxs-lookup"><span data-stu-id="c8367-163">Toggle the `:hover` pseudostate on an element</span></span>  
    :::image-end:::  
    
## <a name="change-the-dimensions-of-an-element"></a><span data-ttu-id="c8367-164">Modifier les dimensions d’un élément</span><span class="sxs-lookup"><span data-stu-id="c8367-164">Change the dimensions of an element</span></span>  

<span data-ttu-id="c8367-165">Utilisez le diagramme interactif **De modèle** de zone dans le panneau **Styles** pour modifier la largeur, la hauteur, l’espacement, la marge ou la longueur de bordure d’un élément.</span><span class="sxs-lookup"><span data-stu-id="c8367-165">Use the **Box Model** interactive diagram in the **Styles** panel to change the width, height, padding, margin, or border length of an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="c8367-166">Complétez le didacticiel [Afficher les CSS d’un](#view-the-css-for-an-element) élément avant de le faire.</span><span class="sxs-lookup"><span data-stu-id="c8367-166">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="c8367-167">[Ouvrez des exemples CSS.](#open-css-examples)</span><span class="sxs-lookup"><span data-stu-id="c8367-167">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="c8367-168">Pointez sur `Change My Margin!` le texte, ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.</span><span class="sxs-lookup"><span data-stu-id="c8367-168">Hover on the `Change My Margin!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="c8367-169">Dans le diagramme **de modèle Box** dans le panneau **Styles,** pointez sur **remplissage.**</span><span class="sxs-lookup"><span data-stu-id="c8367-169">In the **Box Model** diagram in the **Styles** panel, hover on **padding**.</span></span>  <span data-ttu-id="c8367-170">Le remplissage d’un élément est mis en surbrillement dans laport d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c8367-170">The padding of an element is highlighted in the viewport.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="c8367-171">Selon la taille de votre fenêtre DevTools, vous devrez peut-être faire défiler jusqu’au bas du panneau **Styles** pour afficher le **modèle box**.</span><span class="sxs-lookup"><span data-stu-id="c8367-171">Depending on the size of your DevTools window, you may need to scroll to the bottom of the **Styles** panel to display the **Box Model**.</span></span>  

1.  <span data-ttu-id="c8367-172">Double-cliquez sur la marge de gauche dans le modèle **Box,** qui a actuellement une valeur qui signifie que l’élément `-` n’a pas de marge de gauche.</span><span class="sxs-lookup"><span data-stu-id="c8367-172">Double-click the left margin in the **Box Model**, which currently has a value of `-` meaning that the element does not have a left-margin.</span></span>  
1.  <span data-ttu-id="c8367-173">Tapez `100px` et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c8367-173">Type `100px` and select `Enter`.</span></span>  <span data-ttu-id="c8367-174">Par **défaut, le** modèle Box est en pixels, mais il accepte également d’autres valeurs, telles `25%` que , ou `10vw` .</span><span class="sxs-lookup"><span data-stu-id="c8367-174">The **Box Model** defaults to pixels, but it also accepts other values, such as `25%`, or `10vw`.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Pointer sur le remplissage de l’élément" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             <span data-ttu-id="c8367-176">Pointer sur le remplissage de l’élément</span><span class="sxs-lookup"><span data-stu-id="c8367-176">Hover on the padding of the element</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Modifier la marge gauche de l’élément" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             <span data-ttu-id="c8367-178">Modifier la marge gauche de l’élément</span><span class="sxs-lookup"><span data-stu-id="c8367-178">Change the left-margin of the element</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="debugging-media-queries"></a><span data-ttu-id="c8367-179">Débogage de requêtes multimédias</span><span class="sxs-lookup"><span data-stu-id="c8367-179">Debugging Media Queries</span></span>  

<span data-ttu-id="c8367-180">[Les requêtes multimédias][MDNUsingMediaGueries] sont un moyen de faire en sorte que votre produit web réagisse aux modifications apportées aux paramètres de configuration de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c8367-180">[Media Queries][MDNUsingMediaGueries] are a way to make your web product react to changes in the configuration settings for each user.</span></span>  <span data-ttu-id="c8367-181">Le cas d’utilisation le plus significatif consiste à fournir à votre produit une disposition CSS différente en fonction des dimensions de la vue.</span><span class="sxs-lookup"><span data-stu-id="c8367-181">The most significant use case is to provide your product a different CSS layout depending on the dimensions of the viewport.</span></span>  <span data-ttu-id="c8367-182">L’utilisation de dispositions distinctes permet une disposition d’une colonne pour les appareils mobiles et des dispositions multi-colonnes lorsqu’il y a plus d’espace d’écran disponible.</span><span class="sxs-lookup"><span data-stu-id="c8367-182">Using separate layouts allows for a one-column layout for mobile devices and multi-column layouts when there is more screen estate available.</span></span>  

<span data-ttu-id="c8367-183">Si vous souhaitez déboguer ou tester les requêtes multimédias que vous avez définies dans votre CSS, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="c8367-183">If you want to debug or test the Media Queries you defined in your CSS, use the following steps.</span></span>  

1.  <span data-ttu-id="c8367-184">Ouvrez les outils  de développement et sélectionnez l’icône de la barre d’outils de l’appareil bascule en deuxième position en haut à gauche, ou sélectionnez `Ctrl` + `Shift` + `M` \( `Cmd` + `Shift` + `M` sur macOS\).</span><span class="sxs-lookup"><span data-stu-id="c8367-184">Open the developer tools and select the **Toggle device toolbar** icon second on the top-left, or select `Ctrl`+`Shift`+`M` \(`Cmd`+`Shift`+`M` on macOS\).</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Ouvrir la barre d’outils de l’appareil" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       <span data-ttu-id="c8367-186">Ouvrir la barre d’outils de l’appareil</span><span class="sxs-lookup"><span data-stu-id="c8367-186">Open the device toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8367-187">Une fois la barre d’outils de l’appareil ouverte, sélectionnez le menu en haut à droite `...` et choisissez Afficher les requêtes **multimédias.**</span><span class="sxs-lookup"><span data-stu-id="c8367-187">With the device toolbar open, select the `...` menu on the top-right and choose **View Media Queries**.</span></span>  <span data-ttu-id="c8367-188">Les barres de couleur affichées au-dessus de la page web représentent les différentes requêtes multimédias.</span><span class="sxs-lookup"><span data-stu-id="c8367-188">The colored bars displayed above the webpage represent the different media queries.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Afficher les requêtes multimédias dans la barre d’outils de l’appareil" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       <span data-ttu-id="c8367-190">Afficher les requêtes multimédias dans la barre d’outils de l’appareil</span><span class="sxs-lookup"><span data-stu-id="c8367-190">Show Media Queries in Device Toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8367-191">Pointez sur les limites des barres pour afficher les valeurs des différentes requêtes multimédias.</span><span class="sxs-lookup"><span data-stu-id="c8367-191">Hover on the boundaries in the bars to display the values of the different media queries.</span></span>  <span data-ttu-id="c8367-192">Choisissez chacune d’elles pour resizer la page web à mettre en correspondance.</span><span class="sxs-lookup"><span data-stu-id="c8367-192">Choose each to resize the web page to match.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Choisir la requête multimédia dans la barre d’aperçu" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       <span data-ttu-id="c8367-194">Choisir la requête multimédia dans la barre d’aperçu</span><span class="sxs-lookup"><span data-stu-id="c8367-194">Choose Media Query from preview bar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8367-195">Pour déboguer les requêtes multimédias et ouvrir le fichier CSS dans l’éditeur ; pointez sur l’un des segments de barre, ouvrez le menu contextuel `Sources` \(clic droit\), puis sélectionnez `reveal in source code` .</span><span class="sxs-lookup"><span data-stu-id="c8367-195">To debug media queries and open the CSS file in the `Sources` editor; hover on any of the bar segments, open the contextual menu \(right-click\), and select `reveal in source code`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Révéler les requêtes multimédias dans l’Éditeur de sources" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       <span data-ttu-id="c8367-197">Révéler les requêtes multimédias dans l’Éditeur de sources</span><span class="sxs-lookup"><span data-stu-id="c8367-197">Reveal Media Queries in Sources Editor</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c8367-198">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="c8367-198">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Modifier l’emplacement de Microsoft Edge DevTools (Undock, Dock to Bottom, Dock To Left)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Exemples CSS - Microsoft Edge (Chromium) DevTools | Glitch"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Utilisation de requêtes multimédias | MDN"  

> [!NOTE]
> <span data-ttu-id="c8367-202">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c8367-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c8367-203">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/index) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="c8367-203">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="c8367-205">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c8367-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
