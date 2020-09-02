---
title: Découvrir comment afficher et modifier le DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 6d41b072a8bd19ae728cc02b43eb2f843d91b332
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991202"
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





# <span data-ttu-id="20cfd-103">Découvrir comment afficher et modifier le DOM</span><span class="sxs-lookup"><span data-stu-id="20cfd-103">Get started with viewing and changing the DOM</span></span>   



<span data-ttu-id="20cfd-104">Pour découvrir les notions de base de l’affichage et de la modification du DOM d’une page, suivez les didacticiels interactifs de Microsoft DevTools.</span><span class="sxs-lookup"><span data-stu-id="20cfd-104">Complete these interactive tutorials to learn the basics of viewing and changing the DOM of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="20cfd-105">Ce didacticiel part du principe que vous connaissez la différence entre le DOM et le code HTML.</span><span class="sxs-lookup"><span data-stu-id="20cfd-105">This tutorial assumes that you know the difference between the DOM and HTML.</span></span>  <span data-ttu-id="20cfd-106">Pour obtenir une explication, voir [appendice: HTML et DOM](#appendix-html-versus-the-dom) .</span><span class="sxs-lookup"><span data-stu-id="20cfd-106">See [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <span data-ttu-id="20cfd-107">Exemples d’ouverture de DOM</span><span class="sxs-lookup"><span data-stu-id="20cfd-107">Open DOM examples</span></span>  

1.  <span data-ttu-id="20cfd-108">Maintenez `Control` la touche Windows enfoncée `Command` et cliquez sur les **exemples DOM** à ouvrir dans un nouvel onglet.</span><span class="sxs-lookup"><span data-stu-id="20cfd-108">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="20cfd-109">Exemples DOM</span><span class="sxs-lookup"><span data-stu-id="20cfd-109">DOM Examples</span></span>][GlitchDomExamples]  
    
## <span data-ttu-id="20cfd-110">Afficher les nœuds DOM</span><span class="sxs-lookup"><span data-stu-id="20cfd-110">View DOM nodes</span></span>   

<span data-ttu-id="20cfd-111">L’arborescence DOM du panneau éléments vous permet d’effectuer toutes les activités liées au DOM dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="20cfd-111">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <span data-ttu-id="20cfd-112">Inspecter un nœud</span><span class="sxs-lookup"><span data-stu-id="20cfd-112">Inspect a node</span></span>   

<span data-ttu-id="20cfd-113">Lorsque vous êtes intéressé par un nœud DOM particulier, **Inspect** est un moyen rapide d’ouvrir devtools et d’examiner ce nœud.</span><span class="sxs-lookup"><span data-stu-id="20cfd-113">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="20cfd-114">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="20cfd-114">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="20cfd-115">Sous **inspecter un nœud**, cliquez avec le bouton droit sur **Michelangelo** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-115">Under **Inspect a Node**, right-click **Michelangelo** and select **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Inspecter un nœud" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       <span data-ttu-id="20cfd-117">Inspecter un nœud</span><span class="sxs-lookup"><span data-stu-id="20cfd-117">Inspect a node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="20cfd-118">Le panneau **éléments** de devtools s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="20cfd-118">The **Elements** panel of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="20cfd-119">est mise en évidence dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-119">is highlighted in the **DOM Tree**.</span></span>  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Mise en surbrillance du nœud Michelangelo" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           <span data-ttu-id="20cfd-121">Mettre en surbrillance le `Michelangelo` nœud</span><span class="sxs-lookup"><span data-stu-id="20cfd-121">Highlight the `Michelangelo` node</span></span>  
        :::image-end:::  
        
        1.  <span data-ttu-id="20cfd-122">**Inspect** ![ ][ImageInspectIcon] Dans le coin supérieur gauche de devtools, cliquez sur l’icône d’examen.</span><span class="sxs-lookup"><span data-stu-id="20cfd-122">Click the **Inspect** \(![Inspect][ImageInspectIcon]\) icon in the top-left corner of DevTools.</span></span>  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Icône Inspect" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               <span data-ttu-id="20cfd-124">Icône **Inspect**</span><span class="sxs-lookup"><span data-stu-id="20cfd-124">The **Inspect** icon</span></span>  
            :::image-end:::  
            
1.  <span data-ttu-id="20cfd-125">Sous **inspecter un nœud**, cliquez sur le texte de **Tokyo** .</span><span class="sxs-lookup"><span data-stu-id="20cfd-125">Under **Inspect a Node**, click the **Tokyo** text.</span></span>  <span data-ttu-id="20cfd-126">Est désormais `<li>Tokyo</li>` mis en surbrillance dans l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="20cfd-126">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="20cfd-127">L’examen d’un nœud est également la première étape de l’affichage et de la modification des styles d’un nœud.</span><span class="sxs-lookup"><span data-stu-id="20cfd-127">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="20cfd-128">Voir [commencer à afficher et modifier des feuilles CSS][DevToolsCssGetStarted].</span><span class="sxs-lookup"><span data-stu-id="20cfd-128">See [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <span data-ttu-id="20cfd-129">Parcourir l’arborescence DOM à l’aide d’un clavier</span><span class="sxs-lookup"><span data-stu-id="20cfd-129">Navigate the DOM Tree with a keyboard</span></span>   

<span data-ttu-id="20cfd-130">Une fois que vous avez sélectionné un nœud dans l’arborescence DOM, vous pouvez parcourir l’arborescence DOM à l’aide de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="20cfd-130">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="20cfd-131">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="20cfd-131">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="20cfd-132">Sous **naviguez dans l’arborescence DOM à l’aide d’un clavier**, cliquez avec le bouton droit sur **Ringo** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-132">Under **Navigate the DOM Tree with a Keyboard**, right-click **Ringo** and select **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="20cfd-133">est sélectionnée dans l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="20cfd-133">is selected in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Inspectez le nœud Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       <span data-ttu-id="20cfd-135">Inspecter le `Ringo` nœud</span><span class="sxs-lookup"><span data-stu-id="20cfd-135">Inspect the `Ringo` node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="20cfd-136">Appuyez sur la `Up` touche de direction 2 fois.</span><span class="sxs-lookup"><span data-stu-id="20cfd-136">Press the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="20cfd-137"> est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="20cfd-137">is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Examen du nœud UL" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           <span data-ttu-id="20cfd-139">Inspecter le `ul` nœud</span><span class="sxs-lookup"><span data-stu-id="20cfd-139">Inspect the `ul` node</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="20cfd-140">Appuyez sur la `Left` touche de direction.</span><span class="sxs-lookup"><span data-stu-id="20cfd-140">Press the `Left` arrow key.</span></span>  <span data-ttu-id="20cfd-141">La `<ul>` liste est réduite.</span><span class="sxs-lookup"><span data-stu-id="20cfd-141">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="20cfd-142">Appuyez de `Left` nouveau sur la touche de direction.</span><span class="sxs-lookup"><span data-stu-id="20cfd-142">Press the `Left` arrow key again.</span></span>  <span data-ttu-id="20cfd-143">Le parent du `<ul>` nœud est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="20cfd-143">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="20cfd-144">Dans le cas présent, il s’agit de l' `<div>` ID with `navigate-the-dom-tree-with-a-keyboard-1` .</span><span class="sxs-lookup"><span data-stu-id="20cfd-144">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="20cfd-145">Appuyez `Down` deux fois sur la touche de direction pour que vous ayez sélectionné de nouveau la `<ul>` liste que vous venez de réduire.</span><span class="sxs-lookup"><span data-stu-id="20cfd-145">Press the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="20cfd-146">Il doit se présenter comme suit:</span><span class="sxs-lookup"><span data-stu-id="20cfd-146">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="20cfd-147">Appuyez sur la `Right` touche de direction.</span><span class="sxs-lookup"><span data-stu-id="20cfd-147">Press the `Right` arrow key.</span></span>  <span data-ttu-id="20cfd-148">La liste est développée.</span><span class="sxs-lookup"><span data-stu-id="20cfd-148">The list expands.</span></span>  

### <span data-ttu-id="20cfd-149">Faire défiler l’affichage</span><span class="sxs-lookup"><span data-stu-id="20cfd-149">Scroll into view</span></span>   

<span data-ttu-id="20cfd-150">Lors de l’affichage de l’arborescence DOM, il se peut que vous vous trouviez intéressé par un nœud DOM qui n’est pas disponible dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="20cfd-150">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="20cfd-151">Par exemple, supposons que vous faites défiler vers le bas de la page et que vous soyez intéressé par le `<h1>` nœud en haut de la page.</span><span class="sxs-lookup"><span data-stu-id="20cfd-151">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="20cfd-152">Le **défilement dans l’affichage** vous permet de repositionner rapidement la fenêtre d’affichage de manière à ce que vous puissiez voir le nœud.</span><span class="sxs-lookup"><span data-stu-id="20cfd-152">**Scroll into view** lets you quickly reposition the viewport so that you are able to see the node.</span></span>  

1.  <span data-ttu-id="20cfd-153">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="20cfd-153">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="20cfd-154">Sous **défilement dans l’affichage**, cliquez avec le bouton droit sur **Magritte** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-154">Under **Scroll into View**, right-click **Magritte** and select **Inspect**.</span></span>  
1.  <span data-ttu-id="20cfd-155">Faites défiler vers le bas de la page des exemples DOM.</span><span class="sxs-lookup"><span data-stu-id="20cfd-155">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="20cfd-156">Le `<li>Magritte</li>` nœud doit toujours être sélectionné dans votre arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="20cfd-156">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="20cfd-157">Si ce n’est pas le cas, revenez à la [fenêtre de défilement pour faire défiler](#scroll-into-view) le document.</span><span class="sxs-lookup"><span data-stu-id="20cfd-157">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="20cfd-158">Cliquez avec le bouton droit sur le `<li>Magritte</li>` nœud et sélectionnez **défilement dans l’affichage**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-158">Right-click the `<li>Magritte</li>` node and select **Scroll into view**.</span></span>  <span data-ttu-id="20cfd-159">Votre fenêtre d’affichage défile vers le haut pour que le nœud **Magritte** puisse s’afficher.</span><span class="sxs-lookup"><span data-stu-id="20cfd-159">Your viewport scrolls back up so that you may see the **Magritte** node.</span></span>  <span data-ttu-id="20cfd-160">Voir [appendice: options manquantes](#appendix-missing-options) si vous n’êtes pas en mesure d’afficher l’option **défilement dans l’affichage** .</span><span class="sxs-lookup"><span data-stu-id="20cfd-160">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.</span></span>
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Faire défiler l’affichage" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **<span data-ttu-id="20cfd-162">Faire défiler l’affichage</span><span class="sxs-lookup"><span data-stu-id="20cfd-162">Scroll into view</span></span>**  
    :::image-end:::  

### <span data-ttu-id="20cfd-163">Rechercher des nœuds</span><span class="sxs-lookup"><span data-stu-id="20cfd-163">Search for nodes</span></span>   

<span data-ttu-id="20cfd-164">Vous pouvez effectuer une recherche dans l’arborescence DOM par chaîne, sélecteur CSS ou sélecteur XPath.</span><span class="sxs-lookup"><span data-stu-id="20cfd-164">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="20cfd-165">Pointez votre curseur sur le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="20cfd-165">Focus your cursor on the **Elements** panel.</span></span>  
1.  <span data-ttu-id="20cfd-166">Appuyez sur `Control` + `F` \ (Windows \) ou `Command` + `F` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="20cfd-166">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="20cfd-167">La barre de recherche s’ouvre en bas de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="20cfd-167">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="20cfd-168">Entrez `The Moon is a Harsh Mistress`.</span><span class="sxs-lookup"><span data-stu-id="20cfd-168">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="20cfd-169">Dernière phrase mise en évidence dans l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="20cfd-169">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Mettre en surbrillance la requête dans la barre de recherche" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       <span data-ttu-id="20cfd-171">Mettre en surbrillance la requête dans la barre de recherche</span><span class="sxs-lookup"><span data-stu-id="20cfd-171">Highlight the query in the Search bar</span></span>  
    :::image-end:::  
    
<span data-ttu-id="20cfd-172">Comme mentionné précédemment, la barre de recherche prend également en charge les sélecteurs de CSS et de XPath.</span><span class="sxs-lookup"><span data-stu-id="20cfd-172">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <span data-ttu-id="20cfd-173">Modifier le DOM</span><span class="sxs-lookup"><span data-stu-id="20cfd-173">Edit the DOM</span></span>   

<span data-ttu-id="20cfd-174">Vous pouvez modifier le DOM à la volée et constater l’incidence de ces modifications sur la page.</span><span class="sxs-lookup"><span data-stu-id="20cfd-174">You may edit the DOM on the fly and see how those changes affect the page.</span></span>  

### <span data-ttu-id="20cfd-175">Modifier du contenu</span><span class="sxs-lookup"><span data-stu-id="20cfd-175">Edit content</span></span>   

<span data-ttu-id="20cfd-176">Pour modifier le contenu d’un nœud, double-cliquez sur le contenu de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="20cfd-176">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="20cfd-177">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="20cfd-177">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="20cfd-178">Sous **modifier le contenu**, cliquez avec le bouton droit sur **Michelle** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-178">Under **Edit Content**, right-click **Michelle** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="20cfd-179">Dans l’arborescence DOM, double-cliquez `Michelle` .</span><span class="sxs-lookup"><span data-stu-id="20cfd-179">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="20cfd-180">En d’autres termes, double-cliquez sur le texte entre `<li>` et `</li>` .</span><span class="sxs-lookup"><span data-stu-id="20cfd-180">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="20cfd-181">Le texte est mis en surbrillance pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="20cfd-181">The text is highlighted to indicate that it is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Modifier le texte" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           <span data-ttu-id="20cfd-183">Modifier le texte</span><span class="sxs-lookup"><span data-stu-id="20cfd-183">Edit the text</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="20cfd-184">Supprimez `Michelle` , tapez `Leela` , puis appuyez sur `Enter` pour confirmer la modification.</span><span class="sxs-lookup"><span data-stu-id="20cfd-184">Delete `Michelle`, type `Leela`, then press `Enter` to confirm the change.</span></span>  <span data-ttu-id="20cfd-185">Le texte du DOM passe de **Michelle** à **Leela**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-185">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <span data-ttu-id="20cfd-186">Modifier les attributs</span><span class="sxs-lookup"><span data-stu-id="20cfd-186">Edit attributes</span></span>   

<span data-ttu-id="20cfd-187">Pour modifier les attributs, double-cliquez sur le nom ou la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="20cfd-187">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="20cfd-188">Suivez les instructions pour savoir comment ajouter des attributs à un nœud.</span><span class="sxs-lookup"><span data-stu-id="20cfd-188">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="20cfd-189">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="20cfd-189">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="20cfd-190">Sous **modifier les attributs**, cliquez avec le bouton droit sur **Howard** et sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-190">Under **Edit Attributes**, right-click **Howard** and select **Inspect**.</span></span>  
1.  <span data-ttu-id="20cfd-191">Double-cliquez sur `<li>` .</span><span class="sxs-lookup"><span data-stu-id="20cfd-191">Double-click `<li>`.</span></span>  <span data-ttu-id="20cfd-192">Le texte est mis en surbrillance pour indiquer que le nœud est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="20cfd-192">The text is highlighted to indicate that the node is selected.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Modifier le nœud" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       <span data-ttu-id="20cfd-194">Modifier le nœud</span><span class="sxs-lookup"><span data-stu-id="20cfd-194">Edit the node</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="20cfd-195">Appuyez sur la `Right` touche de direction, ajoutez un espace, tapez le texte `style="background-color:gold"` et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="20cfd-195">Press the `Right` arrow key, add a space, type `style="background-color:gold"`, and then press `Enter`.</span></span>  <span data-ttu-id="20cfd-196">La couleur d’arrière-plan du nœud devient or.</span><span class="sxs-lookup"><span data-stu-id="20cfd-196">The background color of the node changes to gold.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Ajouter un attribut de style au nœud" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       <span data-ttu-id="20cfd-198">Ajouter un `style` attribut au nœud</span><span class="sxs-lookup"><span data-stu-id="20cfd-198">Add a `style` attribute to the node</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="20cfd-199">Modifier le type de nœud</span><span class="sxs-lookup"><span data-stu-id="20cfd-199">Edit node type</span></span>   

<span data-ttu-id="20cfd-200">Pour modifier le type d’un nœud, double-cliquez sur le type et tapez le nouveau type.</span><span class="sxs-lookup"><span data-stu-id="20cfd-200">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="20cfd-201">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="20cfd-201">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="20cfd-202">Sous **modifier le type de nœud**, cliquez avec le bouton droit sur **Hank** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-202">Under **Edit Node Type**, right-click **Hank** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="20cfd-203">Double-cliquez sur `<li>` .</span><span class="sxs-lookup"><span data-stu-id="20cfd-203">Double-click `<li>`.</span></span>  <span data-ttu-id="20cfd-204">Le texte `li` est mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="20cfd-204">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="20cfd-205">Suppr `li` , type `button` , puis appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="20cfd-205">Delete `li`, type `button`, then press `Enter`.</span></span>  <span data-ttu-id="20cfd-206">Le `<li>` nœud devient un `<button>` nœud.</span><span class="sxs-lookup"><span data-stu-id="20cfd-206">The `<li>` node changes to a `<button>` node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Changer le type de nœud en bouton" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           <span data-ttu-id="20cfd-208">Changer le type de nœud en</span><span class="sxs-lookup"><span data-stu-id="20cfd-208">Change the node type to</span></span> `button`  
        :::image-end:::  
        
### <span data-ttu-id="20cfd-209">Réorganiser les nœuds DOM</span><span class="sxs-lookup"><span data-stu-id="20cfd-209">Reorder DOM nodes</span></span>   

<span data-ttu-id="20cfd-210">Faites glisser les nœuds pour les réorganiser.</span><span class="sxs-lookup"><span data-stu-id="20cfd-210">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="20cfd-211">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="20cfd-211">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="20cfd-212">Sous **Réorganiser les nœuds DOM**, cliquez avec le bouton droit sur **Elvis Presley** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-212">Under **Reorder DOM Nodes**, right-click **Elvis Presley** and select **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="20cfd-213">Il s’agit du dernier élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="20cfd-213">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="20cfd-214">Dans l’arborescence DOM, faites glisser `<li>Elvis Presley</li>` vers le haut de la liste.</span><span class="sxs-lookup"><span data-stu-id="20cfd-214">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Faites glisser le nœud vers le haut de la liste." lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           <span data-ttu-id="20cfd-216">Faites glisser le nœud vers le haut de la liste.</span><span class="sxs-lookup"><span data-stu-id="20cfd-216">Drag the node to the top of the list</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="20cfd-217">État de la force</span><span class="sxs-lookup"><span data-stu-id="20cfd-217">Force state</span></span>   

<span data-ttu-id="20cfd-218">Vous pouvez imposer aux nœuds de rester dans des États, y compris,,, `:active` `:hover` `:focus` `:visited` et `:focus-within` .</span><span class="sxs-lookup"><span data-stu-id="20cfd-218">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="20cfd-219">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="20cfd-219">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="20cfd-220">Dans **État**de l’état de force, pointez sur **le Seigneur du brusque**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-220">Under **Force state**, hover over **The Lord of the Flies**.</span></span>  <span data-ttu-id="20cfd-221">La couleur d’arrière-plan devient orange.</span><span class="sxs-lookup"><span data-stu-id="20cfd-221">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="20cfd-222">Cliquez avec le bouton droit sur **le Seigneur du brusque** et sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-222">Right-click **The Lord of the Flies** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="20cfd-223">Cliquez avec le bouton droit `<li class="demo--hover">The Lord of the Flies</li>` de la souris et sélectionnez **forcer l’État**  >  **: hover**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-223">Right-click `<li class="demo--hover">The Lord of the Flies</li>` and select **Force State** > **:hover**.</span></span>  <span data-ttu-id="20cfd-224">Voir [annexe: options manquantes](#appendix-missing-options) si vous ne voyez pas cette option.</span><span class="sxs-lookup"><span data-stu-id="20cfd-224">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  <span data-ttu-id="20cfd-225">La couleur d’arrière-plan reste orange même si vous n’êtes pas en train de pointer sur le nœud.</span><span class="sxs-lookup"><span data-stu-id="20cfd-225">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <span data-ttu-id="20cfd-226">Masquer un nœud</span><span class="sxs-lookup"><span data-stu-id="20cfd-226">Hide a node</span></span>   

<span data-ttu-id="20cfd-227">Appuyez `H` pour masquer un nœud.</span><span class="sxs-lookup"><span data-stu-id="20cfd-227">Press `H` to hide a node.</span></span>  

1.  <span data-ttu-id="20cfd-228">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="20cfd-228">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="20cfd-229">Sous **masquer un nœud**, cliquez avec le bouton droit sur **l’étoile** et sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-229">Under **Hide a node**, right-click **The Stars My Destination** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="20cfd-230">Appuyez sur la `H` touche.</span><span class="sxs-lookup"><span data-stu-id="20cfd-230">Press the `H` key.</span></span>  <span data-ttu-id="20cfd-231">Le nœud est masqué.</span><span class="sxs-lookup"><span data-stu-id="20cfd-231">The node is hidden.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Aspect du nœud dans l’arborescence DOM après son masquage" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           <span data-ttu-id="20cfd-233">Aspect du nœud dans l’arborescence DOM après son masquage</span><span class="sxs-lookup"><span data-stu-id="20cfd-233">What the node looks like in the DOM Tree after it is hidden</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="20cfd-234">Appuyez de `H` nouveau sur la touche.</span><span class="sxs-lookup"><span data-stu-id="20cfd-234">Press the `H` key again.</span></span>  <span data-ttu-id="20cfd-235">Le nœud s’affiche à nouveau.</span><span class="sxs-lookup"><span data-stu-id="20cfd-235">The node is shown again.</span></span>  

### <span data-ttu-id="20cfd-236">Supprimer un nœud</span><span class="sxs-lookup"><span data-stu-id="20cfd-236">Delete a node</span></span>   

<span data-ttu-id="20cfd-237">Appuyez `Delete` pour supprimer un nœud.</span><span class="sxs-lookup"><span data-stu-id="20cfd-237">Press `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="20cfd-238">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="20cfd-238">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="20cfd-239">Sous **supprimer un nœud**, cliquez avec le bouton droit sur **base** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-239">Under **Delete a Node**, right-click **Foundation** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="20cfd-240">Appuyez sur la `Delete` touche.</span><span class="sxs-lookup"><span data-stu-id="20cfd-240">Press the `Delete` key.</span></span>  <span data-ttu-id="20cfd-241">Le nœud est supprimé.</span><span class="sxs-lookup"><span data-stu-id="20cfd-241">The node is deleted.</span></span>  
    1.  <span data-ttu-id="20cfd-242">Appuyez sur `Control` + `Z` \ (Windows \) ou `Command` + `Z` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="20cfd-242">Press `Control`+`Z` \(Windows\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="20cfd-243">La dernière action est déstablie et le nœud réapparaît.</span><span class="sxs-lookup"><span data-stu-id="20cfd-243">The last action is undone and the node reappears.</span></span>  

## <span data-ttu-id="20cfd-244">Accéder aux nœuds de la console</span><span class="sxs-lookup"><span data-stu-id="20cfd-244">Access nodes in the Console</span></span>   

<span data-ttu-id="20cfd-245">DevTools fournit plusieurs raccourcis pour accéder aux nœuds DOM à partir de la console ou pour obtenir des références JavaScript à chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="20cfd-245">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <span data-ttu-id="20cfd-246">Faire référence au nœud actuellement sélectionné avec $0</span><span class="sxs-lookup"><span data-stu-id="20cfd-246">Reference the currently-selected node with $0</span></span>   

<span data-ttu-id="20cfd-247">Lorsque vous examinez un nœud, le `== $0` texte en regard du nœud signifie que vous pouvez référencer ce nœud dans la console avec la variable `$0` .</span><span class="sxs-lookup"><span data-stu-id="20cfd-247">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="20cfd-248">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="20cfd-248">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="20cfd-249">Sous **faire référence au nœud actuellement sélectionné avec $0**, cliquez avec le bouton droit sur **la gauche de l’obscurité** et sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-249">Under **Reference the currently-selected node with $0**, right-click **The Left Hand of Darkness** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="20cfd-250">Appuyez sur la `Escape` touche pour ouvrir le tiroir de la console.</span><span class="sxs-lookup"><span data-stu-id="20cfd-250">Press the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="20cfd-251">Tapez `$0` , puis appuyez sur la `Enter` touche.</span><span class="sxs-lookup"><span data-stu-id="20cfd-251">Type `$0` and press the `Enter` key.</span></span>  <span data-ttu-id="20cfd-252">Le résultat de l’expression indique `$0` `<li>The Left Hand of Darkness</li>` .</span><span class="sxs-lookup"><span data-stu-id="20cfd-252">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Résultat de la première expression $0 dans la console." lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            <span data-ttu-id="20cfd-254">Résultat de la première `$0` expression de la **console** .</span><span class="sxs-lookup"><span data-stu-id="20cfd-254">The result of the first `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="20cfd-255">Positionnez le pointeur sur le résultat.</span><span class="sxs-lookup"><span data-stu-id="20cfd-255">Hover over the result.</span></span>  <span data-ttu-id="20cfd-256">Le nœud est mis en surbrillance dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="20cfd-256">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="20cfd-257">Cliquez `<li>Dune</li>` dans l’arborescence DOM, tapez `$0` de nouveau la console, puis appuyez de `Enter` nouveau.</span><span class="sxs-lookup"><span data-stu-id="20cfd-257">Click `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then press `Enter` again.</span></span>  <span data-ttu-id="20cfd-258">`$0`Évalue désormais `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="20cfd-258">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Résultat de la deuxième expression $0 dans la console." lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           <span data-ttu-id="20cfd-260">Résultat de la deuxième `$0` expression de la **console** .</span><span class="sxs-lookup"><span data-stu-id="20cfd-260">The result of the second `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="20cfd-261">Store en tant que variable globale</span><span class="sxs-lookup"><span data-stu-id="20cfd-261">Store as global variable</span></span>   

<span data-ttu-id="20cfd-262">Si vous devez vous référer à un nœud à plusieurs reprises, stockez-le en tant que variable globale.</span><span class="sxs-lookup"><span data-stu-id="20cfd-262">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="20cfd-263">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="20cfd-263">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="20cfd-264">Sous **stocker comme variable globale**, cliquez avec le bouton droit sur **la grande** mise en veille et sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-264">Under **Store as global variable**, right-click **The Big Sleep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="20cfd-265">Cliquez avec le bouton droit `<li>The Big Sleep</li>` dans l’arborescence DOM et sélectionnez **Store As global variable**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-265">Right-click `<li>The Big Sleep</li>` in the DOM Tree and select **Store as global variable**.</span></span>  <span data-ttu-id="20cfd-266">Voir [annexe: options manquantes](#appendix-missing-options) si vous ne voyez pas cette option.</span><span class="sxs-lookup"><span data-stu-id="20cfd-266">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  
    1.  <span data-ttu-id="20cfd-267">Entrez `temp1` dans la console et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="20cfd-267">Type `temp1` in the Console and then press `Enter`.</span></span>  <span data-ttu-id="20cfd-268">Le résultat de l’expression indique que la variable est évaluée au nœud.</span><span class="sxs-lookup"><span data-stu-id="20cfd-268">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Résultat de l’expression temp1." lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           <span data-ttu-id="20cfd-270">Le résultat de l' `temp1` expression.</span><span class="sxs-lookup"><span data-stu-id="20cfd-270">The result of the `temp1` expression</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="20cfd-271">Copier le chemin d’accès JS</span><span class="sxs-lookup"><span data-stu-id="20cfd-271">Copy JS path</span></span>   

<span data-ttu-id="20cfd-272">Copiez le chemin d’accès JavaScript vers un nœud lorsque vous devez le référencer dans un test automatisé.</span><span class="sxs-lookup"><span data-stu-id="20cfd-272">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="20cfd-273">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="20cfd-273">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="20cfd-274">Sous **Copy js Path**, cliquez avec le bouton droit sur **l’Karamazov frères** et sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-274">Under **Copy JS path**, right-click **The Brothers Karamazov** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="20cfd-275">`<li>The Brothers Karamazov</li>`Dans l’arborescence DOM, cliquez avec le bouton droit, puis sélectionnez **copier**le  >  **chemin d’accès js**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-275">Right-click `<li>The Brothers Karamazov</li>` in the DOM Tree and select **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="20cfd-276">Une `document.querySelector()` expression qui est résolue en nœud est copiée dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="20cfd-276">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="20cfd-277">Appuyez sur `Control` + `V` \ (Windows \) ou `Command` + `V` \ (MacOS \) pour coller l’expression dans la console.</span><span class="sxs-lookup"><span data-stu-id="20cfd-277">Press `Control`+`V` \(Windows\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="20cfd-278">Appuyez `Enter` pour évaluer l’expression.</span><span class="sxs-lookup"><span data-stu-id="20cfd-278">Press `Enter` to evaluate the expression.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Résultat de l’expression de chemin d’accès JS de copie" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           <span data-ttu-id="20cfd-280">Résultat de l’expression de **chemin d’accès js de copie**</span><span class="sxs-lookup"><span data-stu-id="20cfd-280">The result of the **Copy JS Path** expression</span></span>  
        :::image-end:::  
        
## <span data-ttu-id="20cfd-281">Arrêt sur les modifications DOM</span><span class="sxs-lookup"><span data-stu-id="20cfd-281">Break on DOM changes</span></span>   

<span data-ttu-id="20cfd-282">DevTools vous permet de suspendre le JavaScript d’une page lorsque JavaScript modifie le DOM.</span><span class="sxs-lookup"><span data-stu-id="20cfd-282">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <span data-ttu-id="20cfd-283">Annuler les modifications apportées aux attributs</span><span class="sxs-lookup"><span data-stu-id="20cfd-283">Break on attribute modifications</span></span>   

<span data-ttu-id="20cfd-284">Utilisez des points d’arrêt de modification d’attribut lorsque vous souhaitez suspendre le JavaScript qui entraîne la modification des attributs d’un nœud.</span><span class="sxs-lookup"><span data-stu-id="20cfd-284">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="20cfd-285">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="20cfd-285">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="20cfd-286">Dans la section **arrêter la modification des attributs**, cliquez avec le bouton droit sur **sauerkraut** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-286">Under **Break on attribute modifications**, right-click **Sauerkraut** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="20cfd-287">Dans l’arborescence DOM, cliquez avec le bouton droit, `<li id="target">Sauerkraut</li>` puis sélectionnez **arrêter de**  >  **modifier les attributs**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-287">In the DOM Tree, right-click `<li id="target">Sauerkraut</li>` and select **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="20cfd-288">Voir [annexe: options manquantes](#appendix-missing-options) si vous ne pouvez pas voir cette option.</span><span class="sxs-lookup"><span data-stu-id="20cfd-288">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Annuler les modifications apportées aux attributs" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **<span data-ttu-id="20cfd-290">Annuler les modifications apportées aux attributs</span><span class="sxs-lookup"><span data-stu-id="20cfd-290">Break on attribute modifications</span></span>**  
        :::image-end:::  
        
    1.  <span data-ttu-id="20cfd-291">Dans la prochaine étape, vous allez être invité à cliquer sur un bouton qui met en pause le code de la page.</span><span class="sxs-lookup"><span data-stu-id="20cfd-291">In the next step you are going to be instructed to click a button that pauses the code of the page.</span></span>  <span data-ttu-id="20cfd-292">Après l’interruption de la page, vous ne pouvez plus faire défiler la page.</span><span class="sxs-lookup"><span data-stu-id="20cfd-292">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="20cfd-293">Pour faire en **Resume Script** sorte que ![ ][ImageResumeScriptIcon] la page puisse être défiler à nouveau, vous devez cliquer sur le script de reprise</span><span class="sxs-lookup"><span data-stu-id="20cfd-293">You must click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\) in order to make the page scrollable again.</span></span>
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Où reprendre l’exécution du script" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           <span data-ttu-id="20cfd-295">Où reprendre l’exécution du script</span><span class="sxs-lookup"><span data-stu-id="20cfd-295">Where to resume script running</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="20cfd-296">Cliquez sur le bouton **définir l’arrière-plan** ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="20cfd-296">Click the **Set Background** button above.</span></span>  <span data-ttu-id="20cfd-297">L' `style` attribut du nœud est alors défini sur `background-color:thistle` .</span><span class="sxs-lookup"><span data-stu-id="20cfd-297">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="20cfd-298">DevTools interrompt la page et met en surbrillance le code à l’origine du changement d’attribut.</span><span class="sxs-lookup"><span data-stu-id="20cfd-298">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="20cfd-299">Cliquez sur **script de reprise** \ ( ![ curriculum vitae ][ImageResumeScriptIcon] \), comme mentionné précédemment.</span><span class="sxs-lookup"><span data-stu-id="20cfd-299">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\), as mentioned earlier.</span></span>  
    
### <span data-ttu-id="20cfd-300">Arrêt lors de la suppression du nœud</span><span class="sxs-lookup"><span data-stu-id="20cfd-300">Break on node removal</span></span>   

<span data-ttu-id="20cfd-301">Si vous souhaitez suspendre la suppression d’un nœud particulier, utilisez des points d’arrêt de suppression de nœud.</span><span class="sxs-lookup"><span data-stu-id="20cfd-301">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="20cfd-302">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="20cfd-302">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="20cfd-303">Sous **arrêt du nœud lors de la suppression du nœud**, cliquez avec le bouton droit sur **Neuromancer** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-303">Under **Break on Node Removal**, right-click **Neuromancer** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="20cfd-304">Dans l’arborescence DOM, cliquez avec le bouton droit, `<li id="target">Neuromancer</li>` puis sélectionnez **arrêter lors de**la  >  **suppression du nœud**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-304">In the DOM Tree, right-click `<li id="target">Neuromancer</li>` and select **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="20cfd-305">Voir [annexe: options manquantes](#appendix-missing-options) si vous ne pouvez pas voir cette option.</span><span class="sxs-lookup"><span data-stu-id="20cfd-305">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="20cfd-306">Cliquez sur le bouton **supprimer** .</span><span class="sxs-lookup"><span data-stu-id="20cfd-306">Click the **Delete** button above.</span></span>  <span data-ttu-id="20cfd-307">DevTools interrompt la page et met en surbrillance le code ayant entraîné la suppression du nœud.</span><span class="sxs-lookup"><span data-stu-id="20cfd-307">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="20cfd-308">Cliquez sur le **script de c.v.** ![ ][ImageResumeScriptIcon]</span><span class="sxs-lookup"><span data-stu-id="20cfd-308">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
### <span data-ttu-id="20cfd-309">Modification de la sous-arborescence</span><span class="sxs-lookup"><span data-stu-id="20cfd-309">Break on subtree modifications</span></span>   

<span data-ttu-id="20cfd-310">Après avoir placé un point d’arrêt de modification de sous-arborescence sur un nœud, DevTools interrompt la page lorsque l’un des descendants du nœud est ajouté ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="20cfd-310">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="20cfd-311">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="20cfd-311">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="20cfd-312">Dans **modifications de**la sous-arborescence, cliquez avec le bouton droit sur **un feu sur le** côté et sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-312">Under **Break on Subtree Modifications**, right-click **A Fire Upon The Deep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="20cfd-313">Dans l’arborescence DOM, cliquez avec le bouton droit `<ul id="target">` , qui correspond au nœud ci-dessus `<li>A Fire Upon the Deep</li>` , puis sélectionnez l’option **arrêter**la modification de la sous-  >  **arborescence**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-313">In the DOM Tree, right-click `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, and select **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="20cfd-314">Voir [annexe: options manquantes](#appendix-missing-options) si vous ne pouvez pas voir cette option.</span><span class="sxs-lookup"><span data-stu-id="20cfd-314">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="20cfd-315">Cliquez sur **Ajouter un enfant**.</span><span class="sxs-lookup"><span data-stu-id="20cfd-315">Click **Add Child**.</span></span>  <span data-ttu-id="20cfd-316">Le code s’interrompt, car un `<li>` nœud a été ajouté à la liste.</span><span class="sxs-lookup"><span data-stu-id="20cfd-316">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="20cfd-317">Cliquez sur le **script de c.v.** ![ ][ImageResumeScriptIcon]</span><span class="sxs-lookup"><span data-stu-id="20cfd-317">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
## <span data-ttu-id="20cfd-318">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="20cfd-318">Next steps</span></span>   

<span data-ttu-id="20cfd-319">Ce qui couvre la plupart des fonctionnalités relatives au DOM dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="20cfd-319">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="20cfd-320">Vous pouvez découvrir les autres options disponibles en cliquant avec le bouton droit sur les nœuds de l’arborescence DOM et en expérimentant les autres options qui n’ont pas été traitées dans ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="20cfd-320">You are able to discover the rest of them by right-clicking nodes in the DOM Tree and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="20cfd-321">Voir aussi [raccourcis clavier du panneau éléments][DevToolsShortcutsElements].</span><span class="sxs-lookup"><span data-stu-id="20cfd-321">See also [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="20cfd-322">Consultez la [page d’accueil de Microsoft Edge devtools][MicrosoftEdgeDevTools] pour découvrir tout ce que vous pouvez faire avec devtools.</span><span class="sxs-lookup"><span data-stu-id="20cfd-322">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--See [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  



## <span data-ttu-id="20cfd-323">Annexe: HTML et DOM</span><span class="sxs-lookup"><span data-stu-id="20cfd-323">Appendix: HTML versus the DOM</span></span>   

<span data-ttu-id="20cfd-324">La section suivante décrit rapidement la différence entre le code HTML et le DOM.</span><span class="sxs-lookup"><span data-stu-id="20cfd-324">The following section quickly explains the difference between HTML and the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="20cfd-325">Lorsque vous utilisez un navigateur Web pour demander une page, le serveur retourne du code HTML, comme dans l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="20cfd-325">When you use a web browser to request a page, the server returns HTML like the following code snippet</span></span>  

      ```html
      <!doctype html>
      <html>
          <head>
              <title>Hello, world!</title>
          </head>
          <body>
              <h1>Hello, world!</h1>
              <p>This is a hypertext document on the World Wide Web.</p>
              <script src="/script.js" async></script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="20cfd-326">Le navigateur analyse le code HTML et crée une arborescence d’objets, comme la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="20cfd-326">The browser parses the HTML and creates a tree of objects like the following list.</span></span>  
      
      ```dom
      html
          head
              title
          body
              h1
              p
              script
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="20cfd-327">Ce type d’arborescence d’objets ou de nœuds, qui représente le contenu de la page, est appelé le DOM.</span><span class="sxs-lookup"><span data-stu-id="20cfd-327">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="20cfd-328">Dans le cas présent, le code HTML ressemble à ceci, mais supposez que le script référencé en bas du code HTML exécute l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="20cfd-328">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs the following code snippet.</span></span>  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="20cfd-329">Ce code supprime le `h1` nœud et ajoute un autre `p` nœud au DOM.</span><span class="sxs-lookup"><span data-stu-id="20cfd-329">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="20cfd-330">Le DOM complet affiche désormais la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="20cfd-330">The complete DOM now displays the following list.</span></span>  
      
      ```dom
      html
          head
              title
          body
              p
              script
              p
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="20cfd-331">Le code HTML de la page est désormais différent du DOM.</span><span class="sxs-lookup"><span data-stu-id="20cfd-331">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="20cfd-332">En d’autres termes, HTML représente le contenu de page initial et le DOM représente le contenu de la page active.</span><span class="sxs-lookup"><span data-stu-id="20cfd-332">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="20cfd-333">Lorsque JavaScript ajoute, supprime ou modifie des nœuds, le DOM devient différent du code HTML.</span><span class="sxs-lookup"><span data-stu-id="20cfd-333">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="20cfd-334">Pour en savoir plus, voir [Présentation du DOM][MDNIntroductionToDOM] .</span><span class="sxs-lookup"><span data-stu-id="20cfd-334">See [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

<!--
## Appendix: Scroll into view   

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and select **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    > ##### Figure 19  
    > Scroll into view  
    > :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
   Scroll into view  
:::image-end:::  
    -->  

## <span data-ttu-id="20cfd-335">Annexe: options manquantes</span><span class="sxs-lookup"><span data-stu-id="20cfd-335">Appendix: Missing options</span></span>   

<span data-ttu-id="20cfd-336">La plupart des instructions de ce didacticiel vous demandent de cliquer avec le bouton droit sur un nœud dans l’arborescence DOM, puis de sélectionner une option dans le menu contextuel qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="20cfd-336">Many of the instructions in this tutorial instruct you to right-click a node in the DOM Tree and then select an option from the context menu that pops up.</span></span>  <span data-ttu-id="20cfd-337">Si vous ne voyez pas l’option spécifiée dans le menu contextuel, effectuez un clic droit en dehors du texte du nœud.</span><span class="sxs-lookup"><span data-stu-id="20cfd-337">If you do not see the specified option in the context menu, try right-clicking away from the node text.</span></span>  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Où cliquer pour afficher toutes les options" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   <span data-ttu-id="20cfd-339">Où cliquer pour afficher toutes les options</span><span class="sxs-lookup"><span data-stu-id="20cfd-339">Where to click if you are not seeing all the options</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: ../media/resume-script-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge \ (chrome \) | Documents Microsoft"  
[DevToolsCssGetStarted]: ../css/index.md "Découvrir comment afficher et modifier des feuilles CSS | Documents Microsoft"  
[DevToolsShortcutsElements]: ../shortcuts.md#elements-panel-keyboard-shortcuts "Raccourcis clavier du panneau d’éléments-raccourcis clavier de Microsoft Edge DevTools | Documents Microsoft"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Exemple de modèle DOM Microsoft Edge (chrome) DevTools Problème"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introduction au DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="20cfd-345">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="20cfd-345">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="20cfd-346">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/dom/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="20cfd-346">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="20cfd-348">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="20cfd-348">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
