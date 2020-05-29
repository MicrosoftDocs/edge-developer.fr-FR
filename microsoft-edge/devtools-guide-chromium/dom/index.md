---
title: Découvrir comment afficher et modifier le DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 4dee8b4e3ea927e72c0f98517f264b2c1d453013
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607446"
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





# <span data-ttu-id="7e2ed-103">Découvrir comment afficher et modifier le DOM</span><span class="sxs-lookup"><span data-stu-id="7e2ed-103">Get Started With Viewing And Changing The DOM</span></span>   



<span data-ttu-id="7e2ed-104">Pour découvrir les notions de base de l’affichage et de la modification du DOM d’une page, suivez les didacticiels interactifs de Microsoft DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-104">Complete these interactive tutorials to learn the basics of viewing and changing the DOM of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="7e2ed-105">Ce didacticiel part du principe que vous connaissez la différence entre le DOM et le code HTML.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-105">This tutorial assumes that you know the difference between the DOM and HTML.</span></span>  <span data-ttu-id="7e2ed-106">Pour obtenir une explication, voir [appendice: HTML et DOM](#appendix-html-versus-the-dom) .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-106">See [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <span data-ttu-id="7e2ed-107">Exemples d’ouverture de DOM</span><span class="sxs-lookup"><span data-stu-id="7e2ed-107">Open DOM Examples</span></span>  

1.  <span data-ttu-id="7e2ed-108">Maintenez `Control` la touche Windows enfoncée `Command` et cliquez sur les **exemples DOM** à ouvrir dans un nouvel onglet.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-108">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="7e2ed-109">Exemples DOM</span><span class="sxs-lookup"><span data-stu-id="7e2ed-109">DOM Examples</span></span>][GlitchDomExamples]  
    
## <span data-ttu-id="7e2ed-110">Afficher les nœuds DOM</span><span class="sxs-lookup"><span data-stu-id="7e2ed-110">View DOM nodes</span></span>   

<span data-ttu-id="7e2ed-111">L’arborescence DOM du panneau éléments vous permet d’effectuer toutes les activités liées au DOM dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-111">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <span data-ttu-id="7e2ed-112">Inspecter un nœud</span><span class="sxs-lookup"><span data-stu-id="7e2ed-112">Inspect a node</span></span>   

<span data-ttu-id="7e2ed-113">Lorsque vous êtes intéressé par un nœud DOM particulier, **Inspect** est un moyen rapide d’ouvrir devtools et d’examiner ce nœud.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-113">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="7e2ed-114">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-114">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="7e2ed-115">Sous **inspecter un nœud**, cliquez avec le bouton droit sur **Michelangelo** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-115">Under **Inspect a Node**, right-click **Michelangelo** and select **Inspect**.</span></span>  
    
    > ##### <span data-ttu-id="7e2ed-116">Figure1</span><span class="sxs-lookup"><span data-stu-id="7e2ed-116">Figure 1</span></span>  
    > <span data-ttu-id="7e2ed-117">Examen d’un nœud</span><span class="sxs-lookup"><span data-stu-id="7e2ed-117">Inspecting a node</span></span>  
    > ![Examen d’un nœud][ImageInspectingNode]  
    
    1.  <span data-ttu-id="7e2ed-119">Le panneau **éléments** de devtools s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-119">The **Elements** panel of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="7e2ed-120">est mise en évidence dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-120">is highlighted in the **DOM Tree**.</span></span>  
        
        > ##### <span data-ttu-id="7e2ed-121">Figure 2</span><span class="sxs-lookup"><span data-stu-id="7e2ed-121">Figure 2</span></span>  
        > <span data-ttu-id="7e2ed-122">Mise en surbrillance du nœud Michelangelo</span><span class="sxs-lookup"><span data-stu-id="7e2ed-122">Highlighting the Michelangelo node</span></span>  
        > ![Mise en surbrillance du nœud Michelangelo][ImageHighlightingMichelangeloNode]  
        
        1.  <span data-ttu-id="7e2ed-124">Cliquez sur l’icône **Inspect** ![ Inspect ][ImageInspectIcon] située dans le coin supérieur gauche de devtools.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-124">Click the **Inspect** ![Inspect][ImageInspectIcon] icon in the top-left corner of DevTools.</span></span>  
            
            > ##### <span data-ttu-id="7e2ed-125">Figure3</span><span class="sxs-lookup"><span data-stu-id="7e2ed-125">Figure 3</span></span>  
            > <span data-ttu-id="7e2ed-126">Icône Inspect</span><span class="sxs-lookup"><span data-stu-id="7e2ed-126">The Inspect icon</span></span>  
            > ![Icône Inspect][ImageInspect]  
            
1.  <span data-ttu-id="7e2ed-128">Sous **inspecter un nœud**, cliquez sur le texte de **Tokyo** .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-128">Under **Inspect a Node**, click the **Tokyo** text.</span></span>  <span data-ttu-id="7e2ed-129">Est désormais `<li>Tokyo</li>` mis en surbrillance dans l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-129">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="7e2ed-130">L’examen d’un nœud est également la première étape de l’affichage et de la modification des styles d’un nœud.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-130">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="7e2ed-131">Voir [commencer à afficher et modifier des feuilles CSS][DevToolsCssGetStarted].</span><span class="sxs-lookup"><span data-stu-id="7e2ed-131">See [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <span data-ttu-id="7e2ed-132">Parcourir l’arborescence DOM à l’aide d’un clavier</span><span class="sxs-lookup"><span data-stu-id="7e2ed-132">Navigate the DOM Tree with a keyboard</span></span>   

<span data-ttu-id="7e2ed-133">Une fois que vous avez sélectionné un nœud dans l’arborescence DOM, vous pouvez parcourir l’arborescence DOM à l’aide de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-133">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="7e2ed-134">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-134">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="7e2ed-135">Sous **naviguez dans l’arborescence DOM à l’aide d’un clavier**, cliquez avec le bouton droit sur **Ringo** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-135">Under **Navigate the DOM Tree with a Keyboard**, right-click **Ringo** and select **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="7e2ed-136">est sélectionnée dans l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-136">is selected in the DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="7e2ed-137">Figure 4</span><span class="sxs-lookup"><span data-stu-id="7e2ed-137">Figure 4</span></span>  
    > <span data-ttu-id="7e2ed-138">Examen du nœud Ringo</span><span class="sxs-lookup"><span data-stu-id="7e2ed-138">Inspecting the Ringo node</span></span>  
    > ![Examen du nœud Ringo][ImageInspectingRingoNode]  
    
    1.  <span data-ttu-id="7e2ed-140">Appuyez sur la `Up` touche de direction 2 fois.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-140">Press the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="7e2ed-141"> est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-141">is selected.</span></span>  
        
        > ##### <span data-ttu-id="7e2ed-142">Figure 5</span><span class="sxs-lookup"><span data-stu-id="7e2ed-142">Figure 5</span></span>  
        > <span data-ttu-id="7e2ed-143">Examen du nœud UL</span><span class="sxs-lookup"><span data-stu-id="7e2ed-143">Inspecting the ul node</span></span>  
        > ![Examen du nœud UL][ImageInspectingUlNode]  
        
    1.  <span data-ttu-id="7e2ed-145">Appuyez sur la `Left` touche de direction.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-145">Press the `Left` arrow key.</span></span>  <span data-ttu-id="7e2ed-146">La `<ul>` liste est réduite.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-146">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="7e2ed-147">Appuyez de `Left` nouveau sur la touche de direction.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-147">Press the `Left` arrow key again.</span></span>  <span data-ttu-id="7e2ed-148">Le parent du `<ul>` nœud est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-148">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="7e2ed-149">Dans le cas présent, il s’agit de l' `<div>` ID with `navigate-the-dom-tree-with-a-keyboard-1` .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-149">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="7e2ed-150">Appuyez `Down` deux fois sur la touche de direction pour que vous ayez sélectionné de nouveau la `<ul>` liste que vous venez de réduire.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-150">Press the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="7e2ed-151">Il doit se présenter comme suit:</span><span class="sxs-lookup"><span data-stu-id="7e2ed-151">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="7e2ed-152">Appuyez sur la `Right` touche de direction.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-152">Press the `Right` arrow key.</span></span>  <span data-ttu-id="7e2ed-153">La liste est développée.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-153">The list expands.</span></span>  

### <span data-ttu-id="7e2ed-154">Faire défiler l’affichage</span><span class="sxs-lookup"><span data-stu-id="7e2ed-154">Scroll into view</span></span>   

<span data-ttu-id="7e2ed-155">Lors de l’affichage de l’arborescence DOM, il se peut que vous vous trouviez intéressé par un nœud DOM qui n’est pas disponible dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-155">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="7e2ed-156">Par exemple, supposons que vous faites défiler vers le bas de la page et que vous soyez intéressé par le `<h1>` nœud en haut de la page.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-156">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="7e2ed-157">Le **défilement dans l’affichage** vous permet de repositionner rapidement la fenêtre d’affichage de manière à ce que vous puissiez voir le nœud.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-157">**Scroll into view** lets you quickly reposition the viewport so that you are able to see the node.</span></span>  

1.  <span data-ttu-id="7e2ed-158">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-158">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="7e2ed-159">Sous **défilement dans l’affichage**, cliquez avec le bouton droit sur **Magritte** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-159">Under **Scroll into View**, right-click **Magritte** and select **Inspect**.</span></span>  
1.  <span data-ttu-id="7e2ed-160">Faites défiler vers le bas de la page des exemples DOM.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-160">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="7e2ed-161">Le `<li>Magritte</li>` nœud doit toujours être sélectionné dans votre arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-161">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="7e2ed-162">Si ce n’est pas le cas, revenez à la [fenêtre de défilement pour faire défiler](#scroll-into-view) le document.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-162">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="7e2ed-163">Cliquez avec le bouton droit sur le `<li>Magritte</li>` nœud et sélectionnez **défilement dans l’affichage**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-163">Right-click the `<li>Magritte</li>` node and select **Scroll into view**.</span></span>  <span data-ttu-id="7e2ed-164">Votre fenêtre d’affichage défile vers le haut pour que le nœud **Magritte** puisse s’afficher.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-164">Your viewport scrolls back up so that you may see the **Magritte** node.</span></span>  <span data-ttu-id="7e2ed-165">Voir [appendice: options manquantes](#appendix-missing-options) si vous n’êtes pas en mesure d’afficher l’option **défilement dans l’affichage** .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-165">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.</span></span>
    
    > ##### <span data-ttu-id="7e2ed-166">Figure 6</span><span class="sxs-lookup"><span data-stu-id="7e2ed-166">Figure 6</span></span>  
    > <span data-ttu-id="7e2ed-167">Faire défiler l’affichage</span><span class="sxs-lookup"><span data-stu-id="7e2ed-167">Scroll into view</span></span>  
    > ![Faire défiler l’affichage][ImageScrollView]  

### <span data-ttu-id="7e2ed-169">Rechercher des nœuds</span><span class="sxs-lookup"><span data-stu-id="7e2ed-169">Search for nodes</span></span>   

<span data-ttu-id="7e2ed-170">Vous pouvez effectuer une recherche dans l’arborescence DOM par chaîne, sélecteur CSS ou sélecteur XPath.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-170">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="7e2ed-171">Pointez votre curseur sur le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-171">Focus your cursor on the **Elements** panel.</span></span>  
1.  <span data-ttu-id="7e2ed-172">Appuyez sur `Control` + `F` \ (Windows \) ou `Command` + `F` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-172">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="7e2ed-173">La barre de recherche s’ouvre en bas de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-173">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="7e2ed-174">Entrez `The Moon is a Harsh Mistress`.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-174">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="7e2ed-175">Dernière phrase mise en évidence dans l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-175">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="7e2ed-176">Figure 7</span><span class="sxs-lookup"><span data-stu-id="7e2ed-176">Figure 7</span></span>  
    > <span data-ttu-id="7e2ed-177">Mise en surbrillance de la requête dans la barre de recherche</span><span class="sxs-lookup"><span data-stu-id="7e2ed-177">Highlighting the query in the Search bar</span></span>  
    > ![Mise en surbrillance de la requête dans la barre de recherche][ImageHighlightingQuerySearchBar]  
    
<span data-ttu-id="7e2ed-179">Comme mentionné précédemment, la barre de recherche prend également en charge les sélecteurs de CSS et de XPath.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-179">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <span data-ttu-id="7e2ed-180">Modifier le DOM</span><span class="sxs-lookup"><span data-stu-id="7e2ed-180">Edit the DOM</span></span>   

<span data-ttu-id="7e2ed-181">Vous pouvez modifier le DOM à la volée et constater l’incidence de ces modifications sur la page.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-181">You may edit the DOM on the fly and see how those changes affect the page.</span></span>  

### <span data-ttu-id="7e2ed-182">Modifier du contenu</span><span class="sxs-lookup"><span data-stu-id="7e2ed-182">Edit content</span></span>   

<span data-ttu-id="7e2ed-183">Pour modifier le contenu d’un nœud, double-cliquez sur le contenu de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-183">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="7e2ed-184">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-184">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="7e2ed-185">Sous **modifier le contenu**, cliquez avec le bouton droit sur **Michelle** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-185">Under **Edit Content**, right-click **Michelle** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="7e2ed-186">Dans l’arborescence DOM, double-cliquez `Michelle` .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-186">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="7e2ed-187">En d’autres termes, double-cliquez sur le texte entre `<li>` et `</li>` .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-187">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="7e2ed-188">Le texte est mis en surbrillance pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-188">The text is highlighted to indicate that it is selected.</span></span>  
        
        > ##### <span data-ttu-id="7e2ed-189">Figure8</span><span class="sxs-lookup"><span data-stu-id="7e2ed-189">Figure 8</span></span>  
        > <span data-ttu-id="7e2ed-190">Modification du texte</span><span class="sxs-lookup"><span data-stu-id="7e2ed-190">Editing the text</span></span>  
        > ![Modification du texte][ImageEditingText]  
        
    1.  <span data-ttu-id="7e2ed-192">Supprimez `Michelle` , tapez `Leela` , puis appuyez sur `Enter` pour confirmer la modification.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-192">Delete `Michelle`, type `Leela`, then press `Enter` to confirm the change.</span></span>  <span data-ttu-id="7e2ed-193">Le texte du DOM passe de **Michelle** à **Leela**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-193">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <span data-ttu-id="7e2ed-194">Modifier les attributs</span><span class="sxs-lookup"><span data-stu-id="7e2ed-194">Edit attributes</span></span>   

<span data-ttu-id="7e2ed-195">Pour modifier les attributs, double-cliquez sur le nom ou la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-195">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="7e2ed-196">Suivez les instructions pour savoir comment ajouter des attributs à un nœud.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-196">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="7e2ed-197">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-197">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="7e2ed-198">Sous **modifier les attributs**, cliquez avec le bouton droit sur **Howard** et sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-198">Under **Edit Attributes**, right-click **Howard** and select **Inspect**.</span></span>  

1.  <span data-ttu-id="7e2ed-199">Double-cliquez sur `<li>` .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-199">Double-click `<li>`.</span></span>  <span data-ttu-id="7e2ed-200">Le texte est mis en surbrillance pour indiquer que le nœud est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-200">The text is highlighted to indicate that the node is selected.</span></span>  
    
    > ##### <span data-ttu-id="7e2ed-201">Figure9</span><span class="sxs-lookup"><span data-stu-id="7e2ed-201">Figure 9</span></span>  
    > <span data-ttu-id="7e2ed-202">Modification du nœud</span><span class="sxs-lookup"><span data-stu-id="7e2ed-202">Editing the node</span></span>  
    > ![Modification du nœud][ImageEditingNode]  
    
1.  <span data-ttu-id="7e2ed-204">Appuyez sur la `Right` touche de direction, ajoutez un espace, tapez le texte `style="background-color:gold"` et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-204">Press the `Right` arrow key, add a space, type `style="background-color:gold"`, and then press `Enter`.</span></span>  <span data-ttu-id="7e2ed-205">La couleur d’arrière-plan du nœud devient or.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-205">The background color of the node changes to gold.</span></span>  
    
    > ##### <span data-ttu-id="7e2ed-206">Figure10</span><span class="sxs-lookup"><span data-stu-id="7e2ed-206">Figure 10</span></span>  
    > <span data-ttu-id="7e2ed-207">Ajouter un attribut de style au nœud</span><span class="sxs-lookup"><span data-stu-id="7e2ed-207">Adding a style attribute to the node</span></span>  
    > ![Ajouter un attribut de style au nœud][ImageAddingStyleAttributeNode]  
    
### <span data-ttu-id="7e2ed-209">Modifier le type de nœud</span><span class="sxs-lookup"><span data-stu-id="7e2ed-209">Edit node type</span></span>   

<span data-ttu-id="7e2ed-210">Pour modifier le type d’un nœud, double-cliquez sur le type et tapez le nouveau type.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-210">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="7e2ed-211">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-211">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="7e2ed-212">Sous **modifier le type de nœud**, cliquez avec le bouton droit sur **Hank** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-212">Under **Edit Node Type**, right-click **Hank** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="7e2ed-213">Double-cliquez sur `<li>` .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-213">Double-click `<li>`.</span></span>  <span data-ttu-id="7e2ed-214">Le texte `li` est mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-214">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="7e2ed-215">Suppr `li` , type `button` , puis appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-215">Delete `li`, type `button`, then press `Enter`.</span></span>  <span data-ttu-id="7e2ed-216">Le `<li>` nœud devient un `<button>` nœud.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-216">The `<li>` node changes to a `<button>` node.</span></span>  
        
        > ##### <span data-ttu-id="7e2ed-217">Figure11</span><span class="sxs-lookup"><span data-stu-id="7e2ed-217">Figure 11</span></span>  
        > <span data-ttu-id="7e2ed-218">Changer le type de nœud en Button</span><span class="sxs-lookup"><span data-stu-id="7e2ed-218">Changing the node type to button</span></span>  
        > ![Changer le type de nœud en Button][ImageChangingNodeButton]  
        
### <span data-ttu-id="7e2ed-220">Réorganiser les nœuds DOM</span><span class="sxs-lookup"><span data-stu-id="7e2ed-220">Reorder DOM nodes</span></span>   

<span data-ttu-id="7e2ed-221">Faites glisser les nœuds pour les réorganiser.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-221">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="7e2ed-222">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-222">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="7e2ed-223">Sous **Réorganiser les nœuds DOM**, cliquez avec le bouton droit sur **Elvis Presley** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-223">Under **Reorder DOM Nodes**, right-click **Elvis Presley** and select **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="7e2ed-224">Il s’agit du dernier élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-224">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="7e2ed-225">Dans l’arborescence DOM, faites glisser `<li>Elvis Presley</li>` vers le haut de la liste.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-225">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        > ##### <span data-ttu-id="7e2ed-226">Figure12</span><span class="sxs-lookup"><span data-stu-id="7e2ed-226">Figure 12</span></span>  
        > <span data-ttu-id="7e2ed-227">Glissement du nœud vers le haut de la liste</span><span class="sxs-lookup"><span data-stu-id="7e2ed-227">Dragging the node to the top of the list</span></span>  
        > ![Glissement du nœud vers le haut de la liste][ImageDraggingNodeTopList]  
        
### <span data-ttu-id="7e2ed-229">État de la force</span><span class="sxs-lookup"><span data-stu-id="7e2ed-229">Force state</span></span>   

<span data-ttu-id="7e2ed-230">Vous pouvez imposer aux nœuds de rester dans des États, y compris,,, `:active` `:hover` `:focus` `:visited` et `:focus-within` .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-230">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="7e2ed-231">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-231">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="7e2ed-232">Dans **État**de l’état de force, pointez sur **le Seigneur du brusque**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-232">Under **Force state**, hover over **The Lord of the Flies**.</span></span>  <span data-ttu-id="7e2ed-233">La couleur d’arrière-plan devient orange.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-233">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="7e2ed-234">Cliquez avec le bouton droit sur **le Seigneur du brusque** et sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-234">Right-click **The Lord of the Flies** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="7e2ed-235">Cliquez avec le bouton droit `<li class="demo--hover">The Lord of the Flies</li>` de la souris et sélectionnez **forcer l’État**  >  **: hover**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-235">Right-click `<li class="demo--hover">The Lord of the Flies</li>` and select **Force State** > **:hover**.</span></span>  <span data-ttu-id="7e2ed-236">Voir [annexe: options manquantes](#appendix-missing-options) si vous ne voyez pas cette option.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-236">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  <span data-ttu-id="7e2ed-237">La couleur d’arrière-plan reste orange même si vous n’êtes pas en train de pointer sur le nœud.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-237">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <span data-ttu-id="7e2ed-238">Masquer un nœud</span><span class="sxs-lookup"><span data-stu-id="7e2ed-238">Hide a node</span></span>   

<span data-ttu-id="7e2ed-239">Appuyez `H` pour masquer un nœud.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-239">Press `H` to hide a node.</span></span>  

1.  <span data-ttu-id="7e2ed-240">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-240">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="7e2ed-241">Sous **masquer un nœud**, cliquez avec le bouton droit sur **l’étoile** et sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-241">Under **Hide a node**, right-click **The Stars My Destination** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="7e2ed-242">Appuyez sur la `H` touche.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-242">Press the `H` key.</span></span>  <span data-ttu-id="7e2ed-243">Le nœud est masqué.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-243">The node is hidden.</span></span>  
        
        > ##### <span data-ttu-id="7e2ed-244">Figure13</span><span class="sxs-lookup"><span data-stu-id="7e2ed-244">Figure 13</span></span>  
        > <span data-ttu-id="7e2ed-245">Aspect du nœud dans l’arborescence DOM après son masquage</span><span class="sxs-lookup"><span data-stu-id="7e2ed-245">What the node looks like in the DOM Tree after it is hidden</span></span>  
        > ![Aspect du nœud dans l’arborescence DOM après son masquage][ImageNodeDomTreeAfterHidden]  
        
    1.  <span data-ttu-id="7e2ed-247">Appuyez de `H` nouveau sur la touche.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-247">Press the `H` key again.</span></span>  <span data-ttu-id="7e2ed-248">Le nœud s’affiche à nouveau.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-248">The node is shown again.</span></span>  

### <span data-ttu-id="7e2ed-249">Supprimer un nœud</span><span class="sxs-lookup"><span data-stu-id="7e2ed-249">Delete a node</span></span>   

<span data-ttu-id="7e2ed-250">Appuyez `Delete` pour supprimer un nœud.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-250">Press `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="7e2ed-251">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-251">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="7e2ed-252">Sous **supprimer un nœud**, cliquez avec le bouton droit sur **base** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-252">Under **Delete a Node**, right-click **Foundation** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="7e2ed-253">Appuyez sur la `Delete` touche.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-253">Press the `Delete` key.</span></span>  <span data-ttu-id="7e2ed-254">Le nœud est supprimé.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-254">The node is deleted.</span></span>  
    1.  <span data-ttu-id="7e2ed-255">Appuyez sur `Control` + `Z` \ (Windows \) ou `Command` + `Z` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-255">Press `Control`+`Z` \(Windows\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="7e2ed-256">La dernière action est déstablie et le nœud réapparaît.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-256">The last action is undone and the node reappears.</span></span>  

## <span data-ttu-id="7e2ed-257">Accéder aux nœuds de la console</span><span class="sxs-lookup"><span data-stu-id="7e2ed-257">Access nodes in the Console</span></span>   

<span data-ttu-id="7e2ed-258">DevTools fournit plusieurs raccourcis pour accéder aux nœuds DOM à partir de la console ou pour obtenir des références JavaScript à chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-258">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <span data-ttu-id="7e2ed-259">Faire référence au nœud actuellement sélectionné avec $0</span><span class="sxs-lookup"><span data-stu-id="7e2ed-259">Reference the currently-selected node with $0</span></span>   

<span data-ttu-id="7e2ed-260">Lorsque vous examinez un nœud, le `== $0` texte en regard du nœud signifie que vous pouvez référencer ce nœud dans la console avec la variable `$0` .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-260">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="7e2ed-261">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-261">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="7e2ed-262">Sous **faire référence au nœud actuellement sélectionné avec $0**, cliquez avec le bouton droit sur **la gauche de l’obscurité** et sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-262">Under **Reference the currently-selected node with $0**, right-click **The Left Hand of Darkness** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="7e2ed-263">Appuyez sur la `Escape` touche pour ouvrir le tiroir de la console.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-263">Press the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="7e2ed-264">Tapez `$0` , puis appuyez sur la `Enter` touche.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-264">Type `$0` and press the `Enter` key.</span></span>  <span data-ttu-id="7e2ed-265">Le résultat de l’expression indique `$0` `<li>The Left Hand of Darkness</li>` .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-265">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        > ##### <span data-ttu-id="7e2ed-266">Figure14</span><span class="sxs-lookup"><span data-stu-id="7e2ed-266">Figure 14</span></span>  
        > <span data-ttu-id="7e2ed-267">Résultat de la première `$0` expression de la console.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-267">The result of the first `$0` expression in the Console</span></span>  
        > ![Résultat de la première expression $0 dans la console.][ImageFirstConsole]  
        
    1.  <span data-ttu-id="7e2ed-269">Positionnez le pointeur sur le résultat.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-269">Hover over the result.</span></span>  <span data-ttu-id="7e2ed-270">Le nœud est mis en surbrillance dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-270">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="7e2ed-271">Cliquez `<li>Dune</li>` dans l’arborescence DOM, tapez `$0` de nouveau la console, puis appuyez de `Enter` nouveau.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-271">Click `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then press `Enter` again.</span></span>  <span data-ttu-id="7e2ed-272">`$0`Évalue désormais `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-272">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        > ##### <span data-ttu-id="7e2ed-273">Figure15</span><span class="sxs-lookup"><span data-stu-id="7e2ed-273">Figure 15</span></span>  
        > <span data-ttu-id="7e2ed-274">Résultat de la deuxième `$0` expression dans la console, ![ le résultat de la deuxième expression $0 de la console.][ImageSecondConsole]</span><span class="sxs-lookup"><span data-stu-id="7e2ed-274">The result of the second `$0` expression in the Console ![The result of the second $0 expression in the Console][ImageSecondConsole]</span></span>  
        
### <span data-ttu-id="7e2ed-275">Store en tant que variable globale</span><span class="sxs-lookup"><span data-stu-id="7e2ed-275">Store as global variable</span></span>   

<span data-ttu-id="7e2ed-276">Si vous devez vous référer à un nœud à plusieurs reprises, stockez-le en tant que variable globale.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-276">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="7e2ed-277">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-277">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="7e2ed-278">Sous **stocker comme variable globale**, cliquez avec le bouton droit sur **la grande** mise en veille et sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-278">Under **Store as global variable**, right-click **The Big Sleep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="7e2ed-279">Cliquez avec le bouton droit `<li>The Big Sleep</li>` dans l’arborescence DOM et sélectionnez **Store As global variable**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-279">Right-click `<li>The Big Sleep</li>` in the DOM Tree and select **Store as global variable**.</span></span>  <span data-ttu-id="7e2ed-280">Voir [annexe: options manquantes](#appendix-missing-options) si vous ne voyez pas cette option.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-280">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  
    1.  <span data-ttu-id="7e2ed-281">Entrez `temp1` dans la console et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-281">Type `temp1` in the Console and then press `Enter`.</span></span>  <span data-ttu-id="7e2ed-282">Le résultat de l’expression indique que la variable est évaluée au nœud.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-282">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        > ##### <span data-ttu-id="7e2ed-283">Figure16</span><span class="sxs-lookup"><span data-stu-id="7e2ed-283">Figure 16</span></span>  
        > <span data-ttu-id="7e2ed-284">Résultat de l’expression temp1.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-284">The result of the temp1 expression</span></span>  
        > ![Résultat de l’expression temp1.][ImageResultTemp1]  
        
### <span data-ttu-id="7e2ed-286">Copier le chemin d’accès JS</span><span class="sxs-lookup"><span data-stu-id="7e2ed-286">Copy JS path</span></span>   

<span data-ttu-id="7e2ed-287">Copiez le chemin d’accès JavaScript vers un nœud lorsque vous devez le référencer dans un test automatisé.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-287">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="7e2ed-288">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-288">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="7e2ed-289">Sous **Copy js Path**, cliquez avec le bouton droit sur **l’Karamazov frères** et sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-289">Under **Copy JS path**, right-click **The Brothers Karamazov** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="7e2ed-290">`<li>The Brothers Karamazov</li>`Dans l’arborescence DOM, cliquez avec le bouton droit, puis sélectionnez **copier**le  >  **chemin d’accès js**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-290">Right-click `<li>The Brothers Karamazov</li>` in the DOM Tree and select **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="7e2ed-291">Une `document.querySelector()` expression qui est résolue en nœud est copiée dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-291">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="7e2ed-292">Appuyez sur `Control` + `V` \ (Windows \) ou `Command` + `V` \ (MacOS \) pour coller l’expression dans la console.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-292">Press `Control`+`V` \(Windows\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="7e2ed-293">Appuyez `Enter` pour évaluer l’expression.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-293">Press `Enter` to evaluate the expression.</span></span>
        
        > ##### <span data-ttu-id="7e2ed-294">Figure17</span><span class="sxs-lookup"><span data-stu-id="7e2ed-294">Figure 17</span></span>  
        > <span data-ttu-id="7e2ed-295">Résultat de l’expression de chemin d’accès JS de copie</span><span class="sxs-lookup"><span data-stu-id="7e2ed-295">The result of the Copy JS Path expression</span></span>  
        > ![Résultat de l’expression de chemin d’accès JS de copie][ImageResultCopyJSPath]  
        
## <span data-ttu-id="7e2ed-297">Arrêt sur les modifications DOM</span><span class="sxs-lookup"><span data-stu-id="7e2ed-297">Break on DOM changes</span></span>   

<span data-ttu-id="7e2ed-298">DevTools vous permet de suspendre le JavaScript d’une page lorsque JavaScript modifie le DOM.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-298">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <span data-ttu-id="7e2ed-299">Annuler les modifications apportées aux attributs</span><span class="sxs-lookup"><span data-stu-id="7e2ed-299">Break on attribute modifications</span></span>   

<span data-ttu-id="7e2ed-300">Utilisez des points d’arrêt de modification d’attribut lorsque vous souhaitez suspendre le JavaScript qui entraîne la modification des attributs d’un nœud.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-300">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="7e2ed-301">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-301">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="7e2ed-302">Dans la section **arrêter la modification des attributs**, cliquez avec le bouton droit sur **sauerkraut** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-302">Under **Break on attribute modifications**, right-click **Sauerkraut** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="7e2ed-303">Dans l’arborescence DOM, cliquez avec le bouton droit, `<li id="target">Sauerkraut</li>` puis sélectionnez **arrêter de**  >  **modifier les attributs**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-303">In the DOM Tree, right-click `<li id="target">Sauerkraut</li>` and select **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="7e2ed-304">Voir [annexe: options manquantes](#appendix-missing-options) si vous ne pouvez pas voir cette option.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-304">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>
        
        > ##### <span data-ttu-id="7e2ed-305">Figure 18</span><span class="sxs-lookup"><span data-stu-id="7e2ed-305">Figure 18</span></span>  
        > <span data-ttu-id="7e2ed-306">Annuler les modifications apportées aux attributs</span><span class="sxs-lookup"><span data-stu-id="7e2ed-306">Break on attribute modifications</span></span>  
        > ![Annuler les modifications apportées aux attributs][ImageBreakAttributeModification]  
        
    1.  <span data-ttu-id="7e2ed-308">Dans la prochaine étape, vous allez être invité à cliquer sur un bouton qui met en pause le code de la page.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-308">In the next step you are going to be instructed to click a button that pauses the code of the page.</span></span>  <span data-ttu-id="7e2ed-309">Après l’interruption de la page, vous ne pouvez plus faire défiler la page.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-309">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="7e2ed-310">**Resume Script** ![ ][ImageResumeScriptIcon] Pour pouvoir faire défiler la page, vous devez cliquer sur curriculum vitae du script de reprise.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-310">You must click **Resume Script** ![Resume Script][ImageResumeScriptIcon] in order to make the page scrollable again.</span></span>
        
        > ##### <span data-ttu-id="7e2ed-311">Figure 19</span><span class="sxs-lookup"><span data-stu-id="7e2ed-311">Figure 19</span></span>  
        > <span data-ttu-id="7e2ed-312">Où reprendre l’exécution du script</span><span class="sxs-lookup"><span data-stu-id="7e2ed-312">Where to resume script running</span></span>  
        > ![Où reprendre l’exécution du script][ImageResumeScript]  
        
    1.  <span data-ttu-id="7e2ed-314">Cliquez sur le bouton **définir l’arrière-plan** ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-314">Click the **Set Background** button above.</span></span>  <span data-ttu-id="7e2ed-315">L' `style` attribut du nœud est alors défini sur `background-color:thistle` .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-315">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="7e2ed-316">DevTools interrompt la page et met en surbrillance le code à l’origine du changement d’attribut.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-316">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="7e2ed-317">Cliquez sur reprendre le script de reprise de **script** ![ ][ImageResumeScriptIcon] , comme mentionné plus haut.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-317">Click **Resume Script** ![Resume Script][ImageResumeScriptIcon], as mentioned earlier.</span></span>  
    
### <span data-ttu-id="7e2ed-318">Arrêt lors de la suppression du nœud</span><span class="sxs-lookup"><span data-stu-id="7e2ed-318">Break on node removal</span></span>   

<span data-ttu-id="7e2ed-319">Si vous souhaitez suspendre la suppression d’un nœud particulier, utilisez des points d’arrêt de suppression de nœud.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-319">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="7e2ed-320">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-320">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="7e2ed-321">Sous **arrêt du nœud lors de la suppression du nœud**, cliquez avec le bouton droit sur **Neuromancer** , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-321">Under **Break on Node Removal**, right-click **Neuromancer** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="7e2ed-322">Dans l’arborescence DOM, cliquez avec le bouton droit, `<li id="target">Neuromancer</li>` puis sélectionnez **arrêter lors de**la  >  **suppression du nœud**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-322">In the DOM Tree, right-click `<li id="target">Neuromancer</li>` and select **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="7e2ed-323">Voir [annexe: options manquantes](#appendix-missing-options) si vous ne pouvez pas voir cette option.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-323">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="7e2ed-324">Cliquez sur le bouton **supprimer** .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-324">Click the **Delete** button above.</span></span>  <span data-ttu-id="7e2ed-325">DevTools interrompt la page et met en surbrillance le code ayant entraîné la suppression du nœud.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-325">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="7e2ed-326">Cliquez sur reprendre le script de reprise de **script** ![ ][ImageResumeScriptIcon] .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-326">Click **Resume Script** ![Resume Script][ImageResumeScriptIcon].</span></span>  
    
### <span data-ttu-id="7e2ed-327">Modification de la sous-arborescence</span><span class="sxs-lookup"><span data-stu-id="7e2ed-327">Break on subtree modifications</span></span>   

<span data-ttu-id="7e2ed-328">Après avoir placé un point d’arrêt de modification de sous-arborescence sur un nœud, DevTools interrompt la page lorsque l’un des descendants du nœud est ajouté ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-328">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="7e2ed-329">[Ouvrir des exemples DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-329">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="7e2ed-330">Dans **modifications de**la sous-arborescence, cliquez avec le bouton droit sur **un feu sur le** côté et sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-330">Under **Break on Subtree Modifications**, right-click **A Fire Upon The Deep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="7e2ed-331">Dans l’arborescence DOM, cliquez avec le bouton droit `<ul id="target">` , qui correspond au nœud ci-dessus `<li>A Fire Upon the Deep</li>` , puis sélectionnez l’option **arrêter**la modification de la sous-  >  **arborescence**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-331">In the DOM Tree, right-click `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, and select **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="7e2ed-332">Voir [annexe: options manquantes](#appendix-missing-options) si vous ne pouvez pas voir cette option.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-332">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="7e2ed-333">Cliquez sur **Ajouter un enfant**.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-333">Click **Add Child**.</span></span>  <span data-ttu-id="7e2ed-334">Le code s’interrompt, car un `<li>` nœud a été ajouté à la liste.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-334">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="7e2ed-335">Cliquez sur reprendre le script de reprise de **script** ![ ][ImageResumeScriptIcon] .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-335">Click **Resume Script** ![Resume Script][ImageResumeScriptIcon].</span></span>  
    
## <span data-ttu-id="7e2ed-336">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="7e2ed-336">Next steps</span></span>   

<span data-ttu-id="7e2ed-337">Ce qui couvre la plupart des fonctionnalités relatives au DOM dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-337">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="7e2ed-338">Vous pouvez découvrir les autres options disponibles en cliquant avec le bouton droit sur les nœuds de l’arborescence DOM et en expérimentant les autres options qui n’ont pas été traitées dans ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-338">You are able to discover the rest of them by right-clicking nodes in the DOM Tree and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="7e2ed-339">Voir aussi [raccourcis clavier du panneau éléments][DevToolsShortcutsElements].</span><span class="sxs-lookup"><span data-stu-id="7e2ed-339">See also [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="7e2ed-340">Consultez la [page d’accueil de Microsoft Edge devtools][MicrosoftEdgeDevTools] pour découvrir tout ce que vous pouvez faire avec devtools.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-340">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--See [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  



## <span data-ttu-id="7e2ed-341">Annexe: HTML et DOM</span><span class="sxs-lookup"><span data-stu-id="7e2ed-341">Appendix: HTML versus the DOM</span></span>   

<span data-ttu-id="7e2ed-342">Cette section décrit rapidement la différence entre le code HTML et le DOM.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-342">This section quickly explains the difference between HTML and the DOM.</span></span>  

<span data-ttu-id="7e2ed-343">Lorsque vous utilisez un navigateur Web pour demander une page, le serveur renvoie le code HTML comme suit:</span><span class="sxs-lookup"><span data-stu-id="7e2ed-343">When you use a web browser to request a page, the server returns HTML like this:</span></span>  

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

<span data-ttu-id="7e2ed-344">Le navigateur analyse le code HTML et crée une arborescence d’objets comme suit:</span><span class="sxs-lookup"><span data-stu-id="7e2ed-344">The browser parses the HTML and creates a tree of objects like this:</span></span>  

```dom
html
  head
    title
  body
    h1
    p
    script
```  

<span data-ttu-id="7e2ed-345">Ce type d’arborescence d’objets ou de nœuds, qui représente le contenu de la page, est appelé le DOM.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-345">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  <span data-ttu-id="7e2ed-346">Dans le cas présent, le code HTML ressemble à ceci, mais supposez que le script référencé en bas du code HTML exécute ce code:</span><span class="sxs-lookup"><span data-stu-id="7e2ed-346">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs this code:</span></span>  

```javascript
const h1 = document.querySelector('h1');
h1.parentElement.removeChild(h1);
const p = document.createElement('p');
p.textContent = 'Wildcard!';
document.body.appendChild(p);
```  

<span data-ttu-id="7e2ed-347">Ce code supprime le `h1` nœud et ajoute un autre `p` nœud au DOM.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-347">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="7e2ed-348">Le DOM complet se présente désormais comme suit:</span><span class="sxs-lookup"><span data-stu-id="7e2ed-348">The complete DOM now looks like this:</span></span>  

```dom
html
  head
    title
  body
    p
    script
    p
```  

<span data-ttu-id="7e2ed-349">Le code HTML de la page est désormais différent du DOM.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-349">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="7e2ed-350">En d’autres termes, HTML représente le contenu de page initial et le DOM représente le contenu de la page active.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-350">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="7e2ed-351">Lorsque JavaScript ajoute, supprime ou modifie des nœuds, le DOM devient différent du code HTML.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-351">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="7e2ed-352">Pour en savoir plus, voir [Présentation du DOM][MDNIntroductionToDOM] .</span><span class="sxs-lookup"><span data-stu-id="7e2ed-352">See [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

<!--
## Appendix: Scroll into view   

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and select **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    > ##### Figure 19  
    > Scroll into view  
    > ![Scroll into view][ImageScrollView]  
    -->  

## <span data-ttu-id="7e2ed-353">Annexe: options manquantes</span><span class="sxs-lookup"><span data-stu-id="7e2ed-353">Appendix: Missing options</span></span>   

<span data-ttu-id="7e2ed-354">La plupart des instructions de ce didacticiel vous demandent de cliquer avec le bouton droit sur un nœud dans l’arborescence DOM, puis de sélectionner une option dans le menu contextuel qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-354">Many of the instructions in this tutorial instruct you to right-click a node in the DOM Tree and then select an option from the context menu that pops up.</span></span>  <span data-ttu-id="7e2ed-355">Si vous ne voyez pas l’option spécifiée dans le menu contextuel, effectuez un clic droit en dehors du texte du nœud.</span><span class="sxs-lookup"><span data-stu-id="7e2ed-355">If you do not see the specified option in the context menu, try right-clicking away from the node text.</span></span>  

> ##### <span data-ttu-id="7e2ed-356">Figure 20</span><span class="sxs-lookup"><span data-stu-id="7e2ed-356">Figure 20</span></span>  
> <span data-ttu-id="7e2ed-357">Où cliquer pour afficher toutes les options</span><span class="sxs-lookup"><span data-stu-id="7e2ed-357">Where to click if you are not seeing all the options</span></span>  
> ![Où cliquer pour afficher toutes les options][ImageNotSeeingAllOptions]  

<!-- image links -->  

[ImageInspectIcon]: /microsoft-edge/devtools-guide-chromium/media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-icon.msft.png  

[ImageInspectingNode]: /microsoft-edge/devtools-guide-chromium/media/dom-glitch-dom-examples-michelangelo-inspect.msft.png "Figure 1: examen d’un nœud"  
[ImageHighlightingMichelangeloNode]: /microsoft-edge/devtools-guide-chromium/media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png "Figure 2: mise en surbrillance du nœud Michelangelo"  
[ImageInspect]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-select-element-page-inspect.msft.png "Figure 3: icône inspecter"  
[ImageInspectingRingoNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png "Figure 4: examen du nœud Ringo"  
[ImageInspectingUlNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png "Figure 5: examen du nœud UL"  
[ImageScrollView]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png "Figure 6: défilement dans l’affichage"  
[ImageHighlightingQuerySearchBar]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-search-nodes-highlight.msft.png "Figure 7: mise en surbrillance de la requête dans la barre de recherche"  
[ImageEditingText]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-content.msft.png "Figure 8: modification du texte"  
[ImageEditingNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-attributes-highlighted.msft.png "Figure 9: modification du nœud"  
[ImageAddingStyleAttributeNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-attributes-inline-css.msft.png "Figure 10: ajouter un attribut de style au nœud"  
[ImageChangingNodeButton]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-node-type-button.msft.png "Figure 11: changer le type de nœud en bouton"  
[ImageDraggingNodeTopList]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-reorder-dom-nodes.msft.png "Figure 12: glissement du nœud vers le haut de la liste"  
[ImageNodeDomTreeAfterHidden]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-hide-a-node.msft.png "Figure 13: apparence du nœud dans l’arborescence DOM après son masquage"  
[ImageFirstConsole]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png "Figure 14: résultat de la première expression $0 dans la console"  
[ImageSecondConsole]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png "Figure 15: résultat de la deuxième expression $0 dans la console"  
[ImageResultTemp1]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png "Figure 16: résultat de l’expression Temp1"  
[ImageResultCopyJSPath]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png "Figure 17: résultat de l’expression de chemin d’accès JS de copie"  
[ImageBreakAttributeModification]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png "Figure 18: arrêt du changement d’attribut"  
[ImageResumeScript]: /microsoft-edge/devtools-guide-chromium/media/dom-break-attribute-modifications-sources-paused-on.msft.png "Figure 19: emplacement de reprise de l’exécution du script"  
[ImageNotSeeingAllOptions]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-right-click-right-side.msft.png "Figure 20: cliquez sur l’emplacement où cliquer pour afficher toutes les options"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge \ (chrome \)"  
[DevToolsCssGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Découvrir comment afficher et modifier des feuilles CSS"  
[DevToolsShortcutsElements]: /microsoft-edge/devtools-guide-chromium/shortcuts#elements-panel-keyboard-shortcuts "Raccourcis clavier du panneau d’éléments-raccourcis clavier de Microsoft Edge DevTools"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Exemple de modèle DOM Microsoft Edge (chrome) DevTools Problème"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introduction au DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="7e2ed-384">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7e2ed-384">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7e2ed-385">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/dom/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools & phare \).</span><span class="sxs-lookup"><span data-stu-id="7e2ed-385">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="7e2ed-387">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7e2ed-387">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
