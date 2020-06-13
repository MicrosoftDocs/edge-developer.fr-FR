---
title: Prise en main de l’affichage et de la modification de réplication Commerce Server
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 346145a7deb9e8ac951ed0578a5060da72817463
ms.sourcegitcommit: a34858dd3260967ba9699842fa839c7a94775fe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2020
ms.locfileid: "10710384"
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

# <span data-ttu-id="f04fe-103">Prise en main de l’affichage et de la modification de réplication Commerce Server</span><span class="sxs-lookup"><span data-stu-id="f04fe-103">Get Started With Viewing And Changing CSS</span></span>  

<span data-ttu-id="f04fe-104">Suivez ces didacticiels interactifs pour découvrir les notions de base de l’affichage et de la modification de la CSS d’une page à l’aide de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="f04fe-104">Complete these interactive tutorials to learn the basics of viewing and changing the CSS for a page using Microsoft Edge DevTools.</span></span>  

## <span data-ttu-id="f04fe-105">Exemples de CSS ouverts</span><span class="sxs-lookup"><span data-stu-id="f04fe-105">Open CSS Examples</span></span>  

1.  <span data-ttu-id="f04fe-106">Appuyez `Control` sur \ (Windows \) ou `Command` \ (MacOS \) et sélectionnez **exemples CSS** à ouvrir dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f04fe-106">Hold `Control` \(Windows\) or `Command` \(macOS\) and select **CSS Examples** to open in a new window.</span></span>  
    
    [<span data-ttu-id="f04fe-107">Exemples CSS</span><span class="sxs-lookup"><span data-stu-id="f04fe-107">CSS Examples</span></span>][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > <span data-ttu-id="f04fe-108">Si vous voulez [ancrer votre fenêtre devtools][DevToolsCustomizePlacement] à droite de votre fenêtre d’affichage \ (affichée dans la figure ci-dessous), sélectionnez **personnaliser et contrôler devtools** `...` .</span><span class="sxs-lookup"><span data-stu-id="f04fe-108">If you want to [dock your DevTools window][DevToolsCustomizePlacement] to the right of your viewport \(displayed in the following figure\), select **Customize and control DevTools** `...`.</span></span>  <span data-ttu-id="f04fe-109">Dans le menu déroulant **personnaliser et contrôler devtools** , dans la section **ancrer** , sélectionnez **ancrer à droite**.</span><span class="sxs-lookup"><span data-stu-id="f04fe-109">On the **Customize and control DevTools** drop-down menu, in the **Dock side** section, select **Dock to right**.</span></span>  
    
## <span data-ttu-id="f04fe-110">Affichage de la feuille de style en cascade pour un élément</span><span class="sxs-lookup"><span data-stu-id="f04fe-110">View the CSS for an element</span></span>  

1.  <span data-ttu-id="f04fe-111">[Exemples de CSS ouverts](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="f04fe-111">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="f04fe-112">Positionnez le pointeur sur le `Inspect Me!` texte, ouvrez le menu contextuel, puis cliquez sur **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="f04fe-112">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="f04fe-113">Dans DevTools, dans le panneau **éléments** , dans l’onglet **arborescence DOM** , l' `Inspect Me!` élément est mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="f04fe-113">In DevTools, on the **Elements** panel, in the **DOM Tree** tab, the `Inspect Me!` element is highlighted.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="L’élément inspecté est surligné dans l’arborescence DOM" lightbox="../media/css-elements-inspect-me.msft.png":::
           <span data-ttu-id="f04fe-115">Figure 1: l’élément inspecté est surligné dans l' **arborescence DOM**</span><span class="sxs-lookup"><span data-stu-id="f04fe-115">Figure 1:  The inspected element is highlighted in the **DOM Tree**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="f04fe-116">Dans l' `Inspect Me!` élément, recherchez la valeur de l' `data-message` attribut et copiez-la.</span><span class="sxs-lookup"><span data-stu-id="f04fe-116">In the `Inspect Me!` element, find the value of the `data-message` attribute and copy it.</span></span>  
1.  <span data-ttu-id="f04fe-117">Dans la page, dans la zone **valeur de `data-message` :** , entrez la valeur.</span><span class="sxs-lookup"><span data-stu-id="f04fe-117">On the page, in the **Value of `data-message`:** textbox, enter the value.</span></span>  
1.  <span data-ttu-id="f04fe-118">Positionnez le pointeur sur le `Inspect Me!` texte, ouvrez le menu contextuel, puis cliquez sur **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="f04fe-118">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="f04fe-119">Dans DevTools, dans le panneau **éléments** , sélectionnez l’onglet **styles** .</span><span class="sxs-lookup"><span data-stu-id="f04fe-119">In DevTools, on the **Elements** panel, select the **Styles** tab.</span></span>  
    1.  <span data-ttu-id="f04fe-120">Dans l’onglet **styles** , l' `Inspect Me!` élément est mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="f04fe-120">In the **Styles** tab, the `Inspect Me!` element is highlighted.</span></span>  
    1.  <span data-ttu-id="f04fe-121">Dans l' `Inspect Me!` élément, recherchez la `aloha` règle de classe.</span><span class="sxs-lookup"><span data-stu-id="f04fe-121">In the `Inspect Me!` element, find the `aloha` class rule.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="f04fe-122">Cette règle s’affiche, car elle est appliquée à l' `Inspect Me!` élément.</span><span class="sxs-lookup"><span data-stu-id="f04fe-122">You see this rule because it is being applied to the `Inspect Me!` element.</span></span>  
        
    1.  <span data-ttu-id="f04fe-123">Dans la `aloha` classe, recherchez la valeur du `padding` style et copiez-la.</span><span class="sxs-lookup"><span data-stu-id="f04fe-123">In the `aloha` class, find the value for the `padding` style and copy it.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="Les classes CSS appliquées à l’élément inspecté sont mises en surbrillance dans l’onglet styles" lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           <span data-ttu-id="f04fe-125">Figure 2: les classes CSS qui sont appliquées à l’élément sélectionné, par exemple `aloha` , sont affichées dans l’onglet **styles**</span><span class="sxs-lookup"><span data-stu-id="f04fe-125">Figure 2:  CSS classes being applied to the selected element, such as `aloha`, are displayed in the **Styles** tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="f04fe-126">Dans la page, dans la zone **valeur de `padding` :** , entrez la valeur.</span><span class="sxs-lookup"><span data-stu-id="f04fe-126">On the page, in the **Value of `padding`:** textbox, enter the value.</span></span>  

## <span data-ttu-id="f04fe-127">Ajouter une déclaration CSS à un élément</span><span class="sxs-lookup"><span data-stu-id="f04fe-127">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="f04fe-128">Utilisez l’onglet **styles** lorsque vous voulez modifier ou ajouter des déclarations CSS à un élément.</span><span class="sxs-lookup"><span data-stu-id="f04fe-128">Use the **Styles** tab when you want to change or add CSS declarations to an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="f04fe-129">Complétez la [fenêtre d’affichage de la feuille de style en cascade pour un élément](#view-the-css-for-an-element) , avant d’effectuer celle-ci.</span><span class="sxs-lookup"><span data-stu-id="f04fe-129">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="f04fe-130">[Exemples de CSS ouverts](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="f04fe-130">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="f04fe-131">Positionnez le pointeur sur le `Add A Background Color To Me!` texte, ouvrez le menu contextuel, puis cliquez sur **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="f04fe-131">Hover on the `Add A Background Color To Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="f04fe-132">Sélectionnez `element.style` près du haut de l’onglet **styles** .</span><span class="sxs-lookup"><span data-stu-id="f04fe-132">Select `element.style` near the top of the **Styles** tab.</span></span>  
1.  <span data-ttu-id="f04fe-133">Tapez `background-color` et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="f04fe-133">Type `background-color` and press `Enter`.</span></span>  
1.  <span data-ttu-id="f04fe-134">Tapez `honeydew` et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="f04fe-134">Type `honeydew` and press `Enter`.</span></span>  <span data-ttu-id="f04fe-135">Dans l' **arborescence DOM** , vous devez voir qu’une déclaration de style intraligne a été appliquée à l’élément.</span><span class="sxs-lookup"><span data-stu-id="f04fe-135">In the **DOM Tree** you should see that an inline style declaration was applied to the element.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Ajout d’une déclaration CSS à l’élément à l’aide de l’onglet styles" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       <span data-ttu-id="f04fe-137">Figure 3: la `background-color:honeydew` déclaration a été appliquée à l’élément à l’aide `element.style` de la section de l’onglet **styles** .</span><span class="sxs-lookup"><span data-stu-id="f04fe-137">Figure 3:  The `background-color:honeydew` declaration has been applied to the element using the `element.style` section of the **Styles** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f04fe-138">Ajouter une classe CSS à un élément</span><span class="sxs-lookup"><span data-stu-id="f04fe-138">Add a CSS class to an element</span></span>  

<span data-ttu-id="f04fe-139">Utilisez l’onglet **styles** pour voir l’apparence d’un élément lorsqu’une classe CSS est appliquée à un élément ou a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="f04fe-139">Use the **Styles** tab to see how an element looks when a CSS class is applied to or removed from an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="f04fe-140">Complétez la [fenêtre d’affichage de la feuille de style en cascade pour un élément](#view-the-css-for-an-element) , avant d’effectuer celle-ci.</span><span class="sxs-lookup"><span data-stu-id="f04fe-140">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="f04fe-141">[Exemples de CSS ouverts](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="f04fe-141">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="f04fe-142">Positionnez le pointeur sur le `Add A Class To Me!` texte, ouvrez le menu contextuel, puis cliquez sur **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="f04fe-142">Hover on the `Add A Class To Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="f04fe-143">Sélectionnez **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="f04fe-143">Select **.cls**.</span></span>  <span data-ttu-id="f04fe-144">DevTools révèle une zone de texte dans laquelle vous pouvez ajouter des classes à l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="f04fe-144">DevTools reveals a text box where you may add classes to the selected element.</span></span>  
1.  <span data-ttu-id="f04fe-145">Entrez `color_me` dans la zone de texte **Ajouter une nouvelle classe** , puis appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="f04fe-145">Type `color_me` in the **Add new class** text box and then press `Enter`.</span></span>  <span data-ttu-id="f04fe-146">Une case à cocher s’affiche sous la zone de texte **Ajouter une nouvelle classe** , dans laquelle vous pouvez activer ou désactiver la classe.</span><span class="sxs-lookup"><span data-stu-id="f04fe-146">A checkbox appears below the **Add new class** text box, where you may toggle the class on and off.</span></span>  <span data-ttu-id="f04fe-147">Si d' `Add A Class To Me!` autres classes sont appliquées à l’élément, vous pouvez également basculer chacun d’eux ici.</span><span class="sxs-lookup"><span data-stu-id="f04fe-147">If the `Add A Class To Me!` element has any other classes applied to it, you are also able to toggle each from here.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Application de la classe color_me à l’élément" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       <span data-ttu-id="f04fe-149">Figure 4: la `color_me` classe a été appliquée à l’élément à l’aide de la section **. CLS** de l’onglet **styles**</span><span class="sxs-lookup"><span data-stu-id="f04fe-149">Figure 4:  The `color_me` class has been applied to the element using the **.cls** section of the **Styles** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f04fe-150">Ajouter un PseudoState à une classe</span><span class="sxs-lookup"><span data-stu-id="f04fe-150">Add a pseudostate to a class</span></span>  

<span data-ttu-id="f04fe-151">Utilisez l’onglet **styles** pour appliquer de manière définitive une PseudoState CSS à un élément.</span><span class="sxs-lookup"><span data-stu-id="f04fe-151">Use the **Styles** tab to permanently apply a CSS pseudostate to an element.</span></span>  <span data-ttu-id="f04fe-152">DevTools prend en charge `:active` , `:focus` , `:hover` et `:visited` .</span><span class="sxs-lookup"><span data-stu-id="f04fe-152">DevTools supports `:active`, `:focus`, `:hover`, and `:visited`.</span></span>  

> [!NOTE]
> <span data-ttu-id="f04fe-153">Complétez la [fenêtre d’affichage de la feuille de style en cascade pour un élément](#view-the-css-for-an-element) , avant d’effectuer celle-ci.</span><span class="sxs-lookup"><span data-stu-id="f04fe-153">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="f04fe-154">[Exemples de CSS ouverts](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="f04fe-154">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="f04fe-155">Placez le pointeur sur le `Hover Over Me!` texte.</span><span class="sxs-lookup"><span data-stu-id="f04fe-155">Hover over the `Hover Over Me!` text.</span></span>  <span data-ttu-id="f04fe-156">La couleur d’arrière-plan change.</span><span class="sxs-lookup"><span data-stu-id="f04fe-156">The background color changes.</span></span>  
1.  <span data-ttu-id="f04fe-157">Positionnez le pointeur sur le `Hover Over Me!` texte, ouvrez le menu contextuel, puis cliquez sur **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="f04fe-157">Hover on the `Hover Over Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="f04fe-158">Dans l’onglet **styles** , sélectionnez **: HOV**.</span><span class="sxs-lookup"><span data-stu-id="f04fe-158">In the **Styles** tab, select **:hov**.</span></span>  
1.  <span data-ttu-id="f04fe-159">Cochez la case **sensitif** .</span><span class="sxs-lookup"><span data-stu-id="f04fe-159">Check the **:hover** checkbox.</span></span>  <span data-ttu-id="f04fe-160">La couleur d’arrière-plan change comme auparavant, même si vous n’avez pas réellement pointé sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="f04fe-160">The background color changes like before, even though you are not actually hovering over the element.</span></span>  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Activation de la fonction Hover PseudoState sur un élément" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       <span data-ttu-id="f04fe-162">Figure 5: activer/désactiver le `:hover` PseudoState sur un élément</span><span class="sxs-lookup"><span data-stu-id="f04fe-162">Figure 5:  Toggling the `:hover` pseudostate on an element</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f04fe-163">Modifier les dimensions d’un élément</span><span class="sxs-lookup"><span data-stu-id="f04fe-163">Change the dimensions of an element</span></span>  

<span data-ttu-id="f04fe-164">Pour modifier la largeur, la hauteur, le remplissage, la marge ou la taille de la bordure d’un élément, utilisez le diagramme interactif du **modèle de zone** dans l’onglet **styles** .</span><span class="sxs-lookup"><span data-stu-id="f04fe-164">Use the **Box Model** interactive diagram in the **Styles** tab to change the width, height, padding, margin, or border length of an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="f04fe-165">Complétez la [fenêtre d’affichage de la feuille de style en cascade pour un élément](#view-the-css-for-an-element) , avant d’effectuer celle-ci.</span><span class="sxs-lookup"><span data-stu-id="f04fe-165">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="f04fe-166">[Exemples de CSS ouverts](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="f04fe-166">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="f04fe-167">Positionnez le pointeur sur le `Change My Margin!` texte, ouvrez le menu contextuel, puis cliquez sur **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="f04fe-167">Hover on the `Change My Margin!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="f04fe-168">Dans le diagramme de **modèle de zone** de l’onglet **styles** , pointez sur **remplissage**.</span><span class="sxs-lookup"><span data-stu-id="f04fe-168">In the **Box Model** diagram in the **Styles** tab, hover over **padding**.</span></span>  <span data-ttu-id="f04fe-169">Le remplissage d’un élément est mis en surbrillance dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f04fe-169">The padding of an element is highlighted in the viewport.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="f04fe-170">En fonction de la taille de votre fenêtre DevTools, il est possible que vous deviez faire défiler vers le bas de l’onglet **styles** pour afficher le **modèle de zone**.</span><span class="sxs-lookup"><span data-stu-id="f04fe-170">Depending on the size of your DevTools window, you may need to scroll to the bottom of the **Styles** tab to see the **Box Model**.</span></span>  

1.  <span data-ttu-id="f04fe-171">Double-cliquez sur la marge gauche dans le **modèle de zone**, ce qui a pour effet de savoir `-` que l’élément n’a pas de marge gauche.</span><span class="sxs-lookup"><span data-stu-id="f04fe-171">Double-click the left margin in the **Box Model**, which currently has a value of `-` meaning that the element does not have a left-margin.</span></span>  
1.  <span data-ttu-id="f04fe-172">Tapez `100px` et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="f04fe-172">Type `100px` and press `Enter`.</span></span>  <span data-ttu-id="f04fe-173">Le **modèle Box** utilise par défaut la valeur pixels, mais accepte également d’autres valeurs, comme `25%` , ou `10vw` .</span><span class="sxs-lookup"><span data-stu-id="f04fe-173">The **Box Model** defaults to pixels, but it also accepts other values, such as `25%`, or `10vw`.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Survol du remplissage de l’élément" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             <span data-ttu-id="f04fe-175">Figure 6: survol du remplissage de l’élément</span><span class="sxs-lookup"><span data-stu-id="f04fe-175">Figure 6:  Hovering over the padding of the element</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Modification de la marge gauche de l’élément" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             <span data-ttu-id="f04fe-177">Figure 7: modification de la marge gauche de l’élément</span><span class="sxs-lookup"><span data-stu-id="f04fe-177">Figure 7:  Changing the left-margin of the element</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="f04fe-178">Débogage de requêtes multimédias</span><span class="sxs-lookup"><span data-stu-id="f04fe-178">Debugging Media Queries</span></span>  

<span data-ttu-id="f04fe-179">Les [requêtes multimédias][MDNUsingMediaGueries] permettent de répartir le produit Web aux modifications apportées aux paramètres de configuration de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f04fe-179">[Media Queries][MDNUsingMediaGueries] are a way to make your web product react to changes in the configuration settings for each user.</span></span>  <span data-ttu-id="f04fe-180">Le cas d’utilisation le plus notable consiste à fournir à votre produit une disposition CSS différente selon les dimensions de la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f04fe-180">The most significant use case is to provide your product a different CSS layout depending on the dimensions of the viewport.</span></span>  <span data-ttu-id="f04fe-181">L’utilisation de dispositions séparées autorise la mise en page à une colonne pour les appareils mobiles et les mises en page de plusieurs colonnes lorsque davantage de surface d’écran est disponible.</span><span class="sxs-lookup"><span data-stu-id="f04fe-181">Using separate layouts allows for a one-column layout for mobile devices and multi-column layouts when there is more screen estate available.</span></span>  

<span data-ttu-id="f04fe-182">Si vous souhaitez déboguer ou tester les requêtes multimédias que vous avez définies dans votre CSS, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="f04fe-182">If you want to debug or test the Media Queries you defined in your CSS, use the following steps.</span></span>  

1.  <span data-ttu-id="f04fe-183">Ouvrez les outils de développement et sélectionnez l’icône **basculer la barre d’outils** de l’appareil dans le coin supérieur gauche, ou appuyez sur `Ctrl` + `Shift` + `M` \ ( `Cmd` + `Shift` + `M` sur MacOS \).</span><span class="sxs-lookup"><span data-stu-id="f04fe-183">Open the developer tools and select the **Toggle device toolbar** icon second on the top-left, or press `Ctrl`+`Shift`+`M` \(`Cmd`+`Shift`+`M` on macOS\).</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Ouverture de la barre d’outils de l’appareil" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       <span data-ttu-id="f04fe-185">Figure 8: ouverture de la barre d’outils de l’appareil</span><span class="sxs-lookup"><span data-stu-id="f04fe-185">Figure 8:  Opening the device toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f04fe-186">Ouvrez la barre d’outils de l’appareil, sélectionnez le `...` menu dans le coin supérieur droit, puis sélectionnez **afficher les requêtes multimédias**.</span><span class="sxs-lookup"><span data-stu-id="f04fe-186">With the device toolbar open, select the `...` menu on the top-right and select **View Media Queries**.</span></span>  <span data-ttu-id="f04fe-187">Vous devez voir les barres de couleur qui s’affichent au-dessus de l’affichage de la page qui représentent les différentes requêtes multimédia.</span><span class="sxs-lookup"><span data-stu-id="f04fe-187">You should see colored bars above the display of the page that represent the different media queries.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Affichage de requêtes multimédias dans la barre d’outils de l’appareil" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       <span data-ttu-id="f04fe-189">Figure 9: affichage de requêtes multimédias dans la barre d’outils de l’appareil</span><span class="sxs-lookup"><span data-stu-id="f04fe-189">Figure 9:  Showing Media Queries in Device Toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f04fe-190">Placez le pointeur de la souris sur les limites dans les barres pour afficher les valeurs des différentes requêtes multimédias.</span><span class="sxs-lookup"><span data-stu-id="f04fe-190">Hover over the boundaries in the bars to see the values of the different media queries.</span></span> <span data-ttu-id="f04fe-191">Sélectionnez chaque pour redimensionner la page Web pour qu’elle corresponde.</span><span class="sxs-lookup"><span data-stu-id="f04fe-191">Select each to resize the web page to match.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Sélection d’une requête multimédia dans la barre d’aperçu" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       <span data-ttu-id="f04fe-193">Figure 10: sélectionner une requête multimédia dans la barre d’aperçu</span><span class="sxs-lookup"><span data-stu-id="f04fe-193">Figure 10:  Selecting Media Query from preview bar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f04fe-194">Pour déboguer des requêtes multimédias et ouvrir le fichier CSS dans l' `Sources` éditeur, pointez sur l’un des segments de la barre, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez `reveal in source code` .</span><span class="sxs-lookup"><span data-stu-id="f04fe-194">To debug media queries and open the CSS file in the `Sources` editor; hover on any of the bar segments, open the contextual menu \(right-click\), and select `reveal in source code`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Affichage de requêtes multimédias dans l’éditeur de sources" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       <span data-ttu-id="f04fe-196">Figure 11: affichage de requêtes multimédias dans l’éditeur de sources</span><span class="sxs-lookup"><span data-stu-id="f04fe-196">Figure 11:  Revealing Media Queries in Sources Editor</span></span>  
    :::image-end:::  
    
<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Exemples CSS-Microsoft Edge (chrome) DevTools | Problème"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Utilisation de requêtes multimédias | MDN"  

> [!NOTE]
> <span data-ttu-id="f04fe-200">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f04fe-200">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f04fe-201">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="f04fe-201">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="f04fe-203">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f04fe-203">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
