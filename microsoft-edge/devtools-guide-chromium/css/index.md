---
title: Découvrir comment afficher et modifier des feuilles CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 85fceaa44b0143a82ca8f66ef8c63e1a9275dcd8
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601816"
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





# <span data-ttu-id="7b086-103">Découvrir comment afficher et modifier des feuilles CSS</span><span class="sxs-lookup"><span data-stu-id="7b086-103">Get Started With Viewing And Changing CSS</span></span>   



<span data-ttu-id="7b086-104">Suivez ces didacticiels interactifs pour découvrir les notions de base de l’affichage et de la modification de la CSS d’une page à l’aide de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="7b086-104">Complete these interactive tutorials to learn the basics of viewing and changing the CSS for a page using Microsoft Edge DevTools.</span></span>  

## <span data-ttu-id="7b086-105">Exemples de CSS ouverts</span><span class="sxs-lookup"><span data-stu-id="7b086-105">Open CSS Examples</span></span>  

1.  <span data-ttu-id="7b086-106">Maintenez la touche Windows enfoncée `Control` `Command` et cliquez sur les **exemples CSS** pour ouvrir une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7b086-106">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **CSS Examples** to open in a new window.</span></span>  
    
    [<span data-ttu-id="7b086-107">Exemples CSS</span><span class="sxs-lookup"><span data-stu-id="7b086-107">CSS Examples</span></span>][GlitchDevToolsCssExamples]  

> [!NOTE]
> <span data-ttu-id="7b086-108">Si vous voulez [ancrer votre fenêtre devtools][DevToolsCustomizePlacement] à droite de votre fenêtre d’affichage \ (illustrée dans la [figure 1](#figure-1)\), cliquez sur **personnaliser et contrôler devtools** `...` .</span><span class="sxs-lookup"><span data-stu-id="7b086-108">If you want to [dock your DevTools window][DevToolsCustomizePlacement] to the right of your viewport \(displayed in [Figure 1](#figure-1)\), click **Customize and control DevTools** `...`.</span></span>  <span data-ttu-id="7b086-109">Dans le menu déroulant **personnaliser et contrôler devtools** , dans la section **ancrer** , sélectionnez **ancrer à droite**.</span><span class="sxs-lookup"><span data-stu-id="7b086-109">On the **Customize and control DevTools** drop-down menu, in the **Dock side** section, select **Dock to right**.</span></span>  
    
## <span data-ttu-id="7b086-110">Affichage de la feuille de style en cascade pour un élément</span><span class="sxs-lookup"><span data-stu-id="7b086-110">View the CSS for an element</span></span>   

1.  <span data-ttu-id="7b086-111">[Exemples de CSS ouverts](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="7b086-111">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="7b086-112">Cliquez avec le bouton droit sur le `Inspect Me!` texte, puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7b086-112">Right-click the `Inspect Me!` text and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="7b086-113">Dans DevTools, dans le panneau **éléments** , dans l’onglet **arborescence DOM** , l' `Inspect Me!` élément est mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="7b086-113">In DevTools, on the **Elements** panel, in the **DOM Tree** tab, the `Inspect Me!` element is highlighted.</span></span>  
        
        > ##### <span data-ttu-id="7b086-114">Figure1</span><span class="sxs-lookup"><span data-stu-id="7b086-114">Figure 1</span></span>  
        > <span data-ttu-id="7b086-115">L’élément inspecté est surligné dans l' **arborescence DOM**</span><span class="sxs-lookup"><span data-stu-id="7b086-115">The inspected element is highlighted in the **DOM Tree**</span></span>  
        > ![L’élément inspecté est surligné dans l’arborescence DOM][ImageInspect]  
        
    1.  <span data-ttu-id="7b086-117">Dans l' `Inspect Me!` élément, recherchez la valeur de l' `data-message` attribut et copiez-la.</span><span class="sxs-lookup"><span data-stu-id="7b086-117">In the `Inspect Me!` element, find the value of the `data-message` attribute and copy it.</span></span>  
1.  <span data-ttu-id="7b086-118">Dans la page, dans la zone **valeur de `data-message` :** , entrez la valeur.</span><span class="sxs-lookup"><span data-stu-id="7b086-118">On the page, in the **Value of `data-message`:** textbox, enter the value.</span></span>  
1.  <span data-ttu-id="7b086-119">Cliquez avec le bouton droit sur le `Inspect Me!` texte, puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7b086-119">Right-click the `Inspect Me!` text and select **Inspect**.</span></span>  
    
    1.  <span data-ttu-id="7b086-120">Dans DevTools, dans le panneau **éléments** , sélectionnez l’onglet **styles** .</span><span class="sxs-lookup"><span data-stu-id="7b086-120">In DevTools, on the **Elements** panel, select the **Styles** tab.</span></span>  
    1.  <span data-ttu-id="7b086-121">Dans l’onglet **styles** , l' `Inspect Me!` élément est mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="7b086-121">In the **Styles** tab, the `Inspect Me!` element is highlighted.</span></span>  
    1.  <span data-ttu-id="7b086-122">Dans l' `Inspect Me!` élément, recherchez la `aloha` règle de classe.</span><span class="sxs-lookup"><span data-stu-id="7b086-122">In the `Inspect Me!` element, find the `aloha` class rule.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="7b086-123">Cette règle s’affiche, car elle est appliquée à l' `Inspect Me!` élément.</span><span class="sxs-lookup"><span data-stu-id="7b086-123">You see this rule because it is being applied to the `Inspect Me!` element.</span></span>  
        
    1.  <span data-ttu-id="7b086-124">Dans la `aloha` classe, recherchez la valeur du `padding` style et copiez-la.</span><span class="sxs-lookup"><span data-stu-id="7b086-124">In the `aloha` class, find the value for the `padding` style and copy it.</span></span>  
        
        > ##### <span data-ttu-id="7b086-125">Figure 2</span><span class="sxs-lookup"><span data-stu-id="7b086-125">Figure 2</span></span>  
        > <span data-ttu-id="7b086-126">Les classes CSS qui sont appliquées à l’élément sélectionné, par exemple `aloha` , sont affichées dans l’onglet **styles** .</span><span class="sxs-lookup"><span data-stu-id="7b086-126">CSS classes being applied to the selected element, such as `aloha`, are displayed in the **Styles** tab</span></span>  
        > ![Les classes CSS appliquées à l’élément inspecté sont mises en surbrillance dans l’onglet styles][ImageAloha]  
        
1.  <span data-ttu-id="7b086-128">Dans la page, dans la zone **valeur de `padding` :** , entrez la valeur.</span><span class="sxs-lookup"><span data-stu-id="7b086-128">On the page, in the **Value of `padding`:** textbox, enter the value.</span></span>  

## <span data-ttu-id="7b086-129">Ajouter une déclaration CSS à un élément</span><span class="sxs-lookup"><span data-stu-id="7b086-129">Add a CSS declaration to an element</span></span>   

<span data-ttu-id="7b086-130">Utilisez l’onglet **styles** lorsque vous voulez modifier ou ajouter des déclarations CSS à un élément.</span><span class="sxs-lookup"><span data-stu-id="7b086-130">Use the **Styles** tab when you want to change or add CSS declarations to an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="7b086-131">Complétez la [fenêtre d’affichage de la feuille de style en cascade pour un élément](#view-the-css-for-an-element) , avant d’effectuer celle-ci.</span><span class="sxs-lookup"><span data-stu-id="7b086-131">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="7b086-132">[Exemples de CSS ouverts](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="7b086-132">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="7b086-133">Cliquez avec le bouton droit sur le `Add A Background Color To Me!` texte, puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7b086-133">Right-click the `Add A Background Color To Me!` text and select **Inspect**.</span></span>  
1.  <span data-ttu-id="7b086-134">Cliquez `element.style` près du haut de l’onglet **styles** .</span><span class="sxs-lookup"><span data-stu-id="7b086-134">Click `element.style` near the top of the **Styles** tab.</span></span>  
1.  <span data-ttu-id="7b086-135">Tapez `background-color` et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7b086-135">Type `background-color` and press `Enter`.</span></span>  
1.  <span data-ttu-id="7b086-136">Tapez `honeydew` et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7b086-136">Type `honeydew` and press `Enter`.</span></span>  <span data-ttu-id="7b086-137">Dans l' **arborescence DOM** , vous devez voir qu’une déclaration de style intraligne a été appliquée à l’élément.</span><span class="sxs-lookup"><span data-stu-id="7b086-137">In the **DOM Tree** you should see that an inline style declaration was applied to the element.</span></span>  

> ##### <span data-ttu-id="7b086-138">Figure3</span><span class="sxs-lookup"><span data-stu-id="7b086-138">Figure 3</span></span>  
> <span data-ttu-id="7b086-139">La `background-color:honeydew` déclaration a été appliquée à l’élément à l’aide `element.style` de la section de l’onglet **styles** .</span><span class="sxs-lookup"><span data-stu-id="7b086-139">The `background-color:honeydew` declaration has been applied to the element using the `element.style` section of the **Styles** tab</span></span>  
> ![Ajout d’une déclaration CSS à l’élément à l’aide de l’onglet styles][ImageDeclaration]  

## <span data-ttu-id="7b086-141">Ajouter une classe CSS à un élément</span><span class="sxs-lookup"><span data-stu-id="7b086-141">Add a CSS class to an element</span></span>   

<span data-ttu-id="7b086-142">Utilisez l’onglet **styles** pour voir l’apparence d’un élément lorsqu’une classe CSS est appliquée à un élément ou a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="7b086-142">Use the **Styles** tab to see how an element looks when a CSS class is applied to or removed from an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="7b086-143">Complétez la [fenêtre d’affichage de la feuille de style en cascade pour un élément](#view-the-css-for-an-element) , avant d’effectuer celle-ci.</span><span class="sxs-lookup"><span data-stu-id="7b086-143">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="7b086-144">[Exemples de CSS ouverts](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="7b086-144">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="7b086-145">Cliquez avec le bouton droit sur l' `Add A Class To Me!` élément, puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7b086-145">Right-click the `Add A Class To Me!` element and select **Inspect**.</span></span>  
1.  <span data-ttu-id="7b086-146">Cliquez sur **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="7b086-146">Click **.cls**.</span></span>  <span data-ttu-id="7b086-147">DevTools révèle une zone de texte dans laquelle vous pouvez ajouter des classes à l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7b086-147">DevTools reveals a text box where you may add classes to the selected element.</span></span>  
1.  <span data-ttu-id="7b086-148">Entrez `color_me` dans la zone de texte **Ajouter une nouvelle classe** , puis appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7b086-148">Type `color_me` in the **Add new class** text box and then press `Enter`.</span></span>  <span data-ttu-id="7b086-149">Une case à cocher s’affiche sous la zone de texte **Ajouter une nouvelle classe** , dans laquelle vous pouvez activer ou désactiver la classe.</span><span class="sxs-lookup"><span data-stu-id="7b086-149">A checkbox appears below the **Add new class** text box, where you may toggle the class on and off.</span></span>  <span data-ttu-id="7b086-150">Si d' `Add A Class To Me!` autres classes sont appliquées à l’élément, vous pouvez également basculer chacun d’eux ici.</span><span class="sxs-lookup"><span data-stu-id="7b086-150">If the `Add A Class To Me!` element has any other classes applied to it, you are also able to toggle each from here.</span></span>  

> ##### <span data-ttu-id="7b086-151">Figure 4</span><span class="sxs-lookup"><span data-stu-id="7b086-151">Figure 4</span></span>  
> <span data-ttu-id="7b086-152">La `color_me` classe a été appliquée à l’élément à l’aide de la section **. CLS** de l’onglet **styles** .</span><span class="sxs-lookup"><span data-stu-id="7b086-152">The `color_me` class has been applied to the element using the **.cls** section of the **Styles** tab</span></span>  
> ![Application de la classe color_me à l’élément][ImageApplyClass]  

## <span data-ttu-id="7b086-154">Ajouter un PseudoState à une classe</span><span class="sxs-lookup"><span data-stu-id="7b086-154">Add a pseudostate to a class</span></span>   

<span data-ttu-id="7b086-155">Utilisez l’onglet **styles** pour appliquer de manière définitive une PseudoState CSS à un élément.</span><span class="sxs-lookup"><span data-stu-id="7b086-155">Use the **Styles** tab to permanently apply a CSS pseudostate to an element.</span></span>  <span data-ttu-id="7b086-156">DevTools prend en charge `:active` , `:focus` , `:hover` et `:visited` .</span><span class="sxs-lookup"><span data-stu-id="7b086-156">DevTools supports `:active`, `:focus`, `:hover`, and `:visited`.</span></span>  

> [!NOTE]
> <span data-ttu-id="7b086-157">Complétez la [fenêtre d’affichage de la feuille de style en cascade pour un élément](#view-the-css-for-an-element) , avant d’effectuer celle-ci.</span><span class="sxs-lookup"><span data-stu-id="7b086-157">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="7b086-158">[Exemples de CSS ouverts](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="7b086-158">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="7b086-159">Placez le pointeur sur le `Hover Over Me!` texte.</span><span class="sxs-lookup"><span data-stu-id="7b086-159">Hover over the `Hover Over Me!` text.</span></span>  <span data-ttu-id="7b086-160">La couleur d’arrière-plan change.</span><span class="sxs-lookup"><span data-stu-id="7b086-160">The background color changes.</span></span>  
1.  <span data-ttu-id="7b086-161">Cliquez avec le bouton droit sur le `Hover Over Me!` texte, puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7b086-161">Right-click the `Hover Over Me!` text and select **Inspect**.</span></span>  
1.  <span data-ttu-id="7b086-162">Dans l’onglet **styles** , cliquez sur **: HOV**.</span><span class="sxs-lookup"><span data-stu-id="7b086-162">In the **Styles** tab, click **:hov**.</span></span>  
1.  <span data-ttu-id="7b086-163">Cochez la case **sensitif** .</span><span class="sxs-lookup"><span data-stu-id="7b086-163">Check the **:hover** checkbox.</span></span>  <span data-ttu-id="7b086-164">La couleur d’arrière-plan change comme auparavant, même si vous n’avez pas réellement pointé sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="7b086-164">The background color changes like before, even though you are not actually hovering over the element.</span></span>  

> ##### <span data-ttu-id="7b086-165">Figure 5</span><span class="sxs-lookup"><span data-stu-id="7b086-165">Figure 5</span></span>  
> <span data-ttu-id="7b086-166">Activer/désactiver le `:hover` PseudoState sur un élément</span><span class="sxs-lookup"><span data-stu-id="7b086-166">Toggling the `:hover` pseudostate on an element</span></span>  
> ![Activation de la fonction Hover PseudoState sur un élément][ImageSetHover]  

## <span data-ttu-id="7b086-168">Modifier les dimensions d’un élément</span><span class="sxs-lookup"><span data-stu-id="7b086-168">Change the dimensions of an element</span></span>   

<span data-ttu-id="7b086-169">Pour modifier la largeur, la hauteur, le remplissage, la marge ou la taille de la bordure d’un élément, utilisez le diagramme interactif du **modèle de zone** dans l’onglet **styles** .</span><span class="sxs-lookup"><span data-stu-id="7b086-169">Use the **Box Model** interactive diagram in the **Styles** tab to change the width, height, padding, margin, or border length of an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="7b086-170">Complétez la [fenêtre d’affichage de la feuille de style en cascade pour un élément](#view-the-css-for-an-element) , avant d’effectuer celle-ci.</span><span class="sxs-lookup"><span data-stu-id="7b086-170">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="7b086-171">[Exemples de CSS ouverts](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="7b086-171">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="7b086-172">Cliquez avec le bouton droit sur l' `Change My Margin!` élément, puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7b086-172">Right-click the `Change My Margin!` element and select **Inspect**.</span></span>  
1.  <span data-ttu-id="7b086-173">Dans le diagramme de **modèle de zone** de l’onglet **styles** , pointez sur **remplissage**.</span><span class="sxs-lookup"><span data-stu-id="7b086-173">In the **Box Model** diagram in the **Styles** tab, hover over **padding**.</span></span>  <span data-ttu-id="7b086-174">Le remplissage d’un élément est mis en surbrillance dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="7b086-174">The padding of an element is highlighted in the viewport.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="7b086-175">En fonction de la taille de votre fenêtre DevTools, il est possible que vous deviez faire défiler vers le bas de l’onglet **styles** pour afficher le **modèle de zone**.</span><span class="sxs-lookup"><span data-stu-id="7b086-175">Depending on the size of your DevTools window, you may need to scroll to the bottom of the **Styles** tab to see the **Box Model**.</span></span>  

1.  <span data-ttu-id="7b086-176">Double-cliquez sur la marge gauche dans le **modèle de zone**, ce qui a pour effet de savoir `-` que l’élément n’a pas de marge gauche.</span><span class="sxs-lookup"><span data-stu-id="7b086-176">Double-click the left margin in the **Box Model**, which currently has a value of `-` meaning that the element does not have a left-margin.</span></span>  
1.  <span data-ttu-id="7b086-177">Tapez `100px` et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7b086-177">Type `100px` and press `Enter`.</span></span>  <span data-ttu-id="7b086-178">Le **modèle Box** utilise par défaut la valeur pixels, mais accepte également d’autres valeurs, comme `25%` , ou `10vw` .</span><span class="sxs-lookup"><span data-stu-id="7b086-178">The **Box Model** defaults to pixels, but it also accepts other values, such as `25%`, or `10vw`.</span></span>  

> ##### <span data-ttu-id="7b086-179">Figure 6</span><span class="sxs-lookup"><span data-stu-id="7b086-179">Figure 6</span></span>  
> <span data-ttu-id="7b086-180">Survol du remplissage de l’élément</span><span class="sxs-lookup"><span data-stu-id="7b086-180">Hovering over the padding of the element</span></span>  
> ![Survol du remplissage de l’élément][ImageShowPadding]  

> ##### <span data-ttu-id="7b086-182">Figure 7</span><span class="sxs-lookup"><span data-stu-id="7b086-182">Figure 7</span></span>  
> <span data-ttu-id="7b086-183">Modification de la marge gauche de l’élément</span><span class="sxs-lookup"><span data-stu-id="7b086-183">Changing the left-margin of the element</span></span>  
> ![Modification de la marge gauche de l’élément][ImageChangeMargin]  

 



<!-- image links -->  

[ImageInspect]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me.msft.png "Figure 1: l’élément inspecté est surligné dans l’arborescence DOM"  
[ImageAloha]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me-styles.msft.png "Figure 2: les classes CSS appliquées à l’élément inspecté sont mises en surbrillance dans l’onglet styles"  
[ImageDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-background-color-to-me-styles-p.msft.png "Figure 3: ajouter une déclaration CSS à l’élément à l’aide de l’onglet styles"  
[ImageApplyClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-a-class-to-me-styles-cls.msft.png "Figure 4: application de la classe color_me à l’élément"  
[ImageSetHover]: /microsoft-edge/devtools-guide-chromium/media/css-elements-hover-over-me-styles-hov-hover.msft.png "Figure 5: activer/désactiver le survol PseudoState sur un élément"  
[ImageShowPadding]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-padding.msft.png "Figure 6: survol du remplissage de l’élément"  
[ImageChangeMargin]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-margin-edit.msft.png "Figure 7: modification de la marge gauche de l’élément"  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Exemples CSS-Microsoft Edge (chrome) DevTools | Problème"  

> [!NOTE]
> <span data-ttu-id="7b086-194">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7b086-194">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7b086-195">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="7b086-195">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="7b086-197">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7b086-197">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
