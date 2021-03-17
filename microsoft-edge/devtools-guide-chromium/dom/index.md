---
description: Découvrez comment afficher les nœuds, rechercher des nœuds, modifier des nœuds, référencer des nœuds dans la console, rompre sur les modifications de nœuds, etc.
title: Commencer à afficher et modifier le DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: e4c08fb2fd5f360f037502c04edabaabb873ba16
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439239"
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

# <a name="get-started-with-viewing-and-changing-the-dom"></a><span data-ttu-id="82569-104">Commencer à afficher et modifier le DOM</span><span class="sxs-lookup"><span data-stu-id="82569-104">Get started with viewing and changing the DOM</span></span>  

<span data-ttu-id="82569-105">Complétez ces didacticiels interactifs pour découvrir les principes de base de l’affichage et de la modification du DOM d’une page à l’aide de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="82569-105">Complete these interactive tutorials to learn the basics of viewing and changing the DOM of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="82569-106">Ce didacticiel suppose que vous connaissez la différence entre le DOM et le code HTML.</span><span class="sxs-lookup"><span data-stu-id="82569-106">This tutorial assumes that you know the difference between the DOM and HTML.</span></span>  <span data-ttu-id="82569-107">Accédez à [l’Annexe : HTML par rapport au DOM](#appendix-html-versus-the-dom) pour obtenir une explication.</span><span class="sxs-lookup"><span data-stu-id="82569-107">Navigate to [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <a name="open-dom-examples"></a><span data-ttu-id="82569-108">Exemples d’ouverture de DOM</span><span class="sxs-lookup"><span data-stu-id="82569-108">Open DOM examples</span></span>  

1.  <span data-ttu-id="82569-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **DOM Examples** to open in a new tab.</span><span class="sxs-lookup"><span data-stu-id="82569-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="82569-110">Exemples DOM</span><span class="sxs-lookup"><span data-stu-id="82569-110">DOM Examples</span></span>][GlitchDomExamples]  
    
## <a name="view-dom-nodes"></a><span data-ttu-id="82569-111">Afficher les nodes DOM</span><span class="sxs-lookup"><span data-stu-id="82569-111">View DOM nodes</span></span>  

<span data-ttu-id="82569-112">L’arborescence DOM du panneau Éléments est l’endroit où vous pouvez faire toutes les activités liées au DOM dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="82569-112">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <a name="inspect-a-node"></a><span data-ttu-id="82569-113">Inspecter un nœud</span><span class="sxs-lookup"><span data-stu-id="82569-113">Inspect a node</span></span>  

<span data-ttu-id="82569-114">Lorsque vous êtes intéressé par un nœud DOM particulier, **Inspect** est un moyen rapide d’ouvrir DevTools et d’examiner ce nœud.</span><span class="sxs-lookup"><span data-stu-id="82569-114">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="82569-115">[Ouvrez des exemples DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="82569-115">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="82569-116">Under **Inspect a Node**, right-choose **Contrôleo** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="82569-116">Under **Inspect a Node**, right-choose **Michelangelo** and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Inspecter un nœud" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       <span data-ttu-id="82569-118">Inspecter un nœud</span><span class="sxs-lookup"><span data-stu-id="82569-118">Inspect a node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="82569-119">**L’outil Elements** de DevTools s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="82569-119">The **Elements** tool of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="82569-120">est mis en surbrillant dans **l’arborescence DOM.**</span><span class="sxs-lookup"><span data-stu-id="82569-120">is highlighted in the **DOM Tree**.</span></span>  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Mettre en surbrillon le nœud" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           <span data-ttu-id="82569-122">Mettre en `Michelangelo` surbrillade le nœud</span><span class="sxs-lookup"><span data-stu-id="82569-122">Highlight the `Michelangelo` node</span></span>  
        :::image-end:::  
        
        1.  <span data-ttu-id="82569-123">Choisissez **l’icône Inspect** \( Inspect \) dans le ![ coin supérieur gauche de ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="82569-123">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Icône Inspecter" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               <span data-ttu-id="82569-125">Icône **Inspecter**</span><span class="sxs-lookup"><span data-stu-id="82569-125">The **Inspect** icon</span></span>  
            :::image-end:::  
            
1.  <span data-ttu-id="82569-126">Sous **Inspecter un nœud,** choisissez le **texte Tokyo.**</span><span class="sxs-lookup"><span data-stu-id="82569-126">Under **Inspect a Node**, choose the **Tokyo** text.</span></span>  <span data-ttu-id="82569-127">À présent, `<li>Tokyo</li>` est mis en surbrillant dans l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="82569-127">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="82569-128">L’inspection d’un nœud constitue également la première étape de l’affichage et de la modification des styles d’un nœud.</span><span class="sxs-lookup"><span data-stu-id="82569-128">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="82569-129">Accédez [à la mise en place de l’affichage et de la modification de CSS][DevToolsCssGetStarted].</span><span class="sxs-lookup"><span data-stu-id="82569-129">Navigate to [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <a name="navigate-the-dom-tree-with-a-keyboard"></a><span data-ttu-id="82569-130">Naviguer dans l’arborescence DOM avec un clavier</span><span class="sxs-lookup"><span data-stu-id="82569-130">Navigate the DOM Tree with a keyboard</span></span>  

<span data-ttu-id="82569-131">Une fois que vous avez sélectionné un nœud dans l’arborescence DOM, vous pouvez naviguer dans l’arborescence DOM avec votre clavier.</span><span class="sxs-lookup"><span data-stu-id="82569-131">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="82569-132">[Ouvrez des exemples DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="82569-132">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="82569-133">Under **Navigate the DOM Tree with a Keyboard**, right-choose **Ringo** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="82569-133">Under **Navigate the DOM Tree with a Keyboard**, right-choose **Ringo** and choose **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="82569-134">est sélectionné dans l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="82569-134">is selected in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Inspecter le nœud Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       <span data-ttu-id="82569-136">Inspecter le `Ringo` nœud</span><span class="sxs-lookup"><span data-stu-id="82569-136">Inspect the `Ringo` node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="82569-137">Sélectionnez la `Up` touche de direction 2 fois.</span><span class="sxs-lookup"><span data-stu-id="82569-137">Select the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="82569-138"> est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="82569-138">is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Inspecter le nœud ul" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           <span data-ttu-id="82569-140">Inspecter le `ul` nœud</span><span class="sxs-lookup"><span data-stu-id="82569-140">Inspect the `ul` node</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="82569-141">Sélectionnez la `Left` touche de direction.</span><span class="sxs-lookup"><span data-stu-id="82569-141">Select the `Left` arrow key.</span></span>  <span data-ttu-id="82569-142">La `<ul>` liste est réduire.</span><span class="sxs-lookup"><span data-stu-id="82569-142">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="82569-143">Sélectionnez de `Left` nouveau la touche de direction.</span><span class="sxs-lookup"><span data-stu-id="82569-143">Select the `Left` arrow key again.</span></span>  <span data-ttu-id="82569-144">Le parent du `<ul>` nœud est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="82569-144">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="82569-145">Dans ce cas, il s’agit `<div>` de l’ID `navigate-the-dom-tree-with-a-keyboard-1` .</span><span class="sxs-lookup"><span data-stu-id="82569-145">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="82569-146">Sélectionnez la touche de direction 2 fois de sorte que vous avez re-sélectionné la liste `Down` `<ul>` que vous venons de réduire.</span><span class="sxs-lookup"><span data-stu-id="82569-146">Select the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="82569-147">Il doit se présenter comme suit:</span><span class="sxs-lookup"><span data-stu-id="82569-147">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="82569-148">Sélectionnez la `Right` touche de direction.</span><span class="sxs-lookup"><span data-stu-id="82569-148">Select the `Right` arrow key.</span></span>  <span data-ttu-id="82569-149">La liste se développe.</span><span class="sxs-lookup"><span data-stu-id="82569-149">The list expands.</span></span>  

### <a name="scroll-into-view"></a><span data-ttu-id="82569-150">Faire défiler vers l’avant</span><span class="sxs-lookup"><span data-stu-id="82569-150">Scroll into view</span></span>  

<span data-ttu-id="82569-151">Lorsque vous affichez l’arborescence DOM, vous pouvez être intéressé par un nœud DOM qui ne se trouve pas actuellement dans laport d’affichage.</span><span class="sxs-lookup"><span data-stu-id="82569-151">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="82569-152">Par exemple, supposons que vous avez fait défiler vers le bas de la page et que le nœud en haut de la page vous `<h1>` intéresse.</span><span class="sxs-lookup"><span data-stu-id="82569-152">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="82569-153">**Le défilement vers l’affichage** vous permet de repositionner rapidement la vue afin de pouvoir passer en revue le nœud.</span><span class="sxs-lookup"><span data-stu-id="82569-153">**Scroll into view** lets you quickly reposition the viewport so that you are able to review the node.</span></span>  

1.  <span data-ttu-id="82569-154">[Ouvrez des exemples DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="82569-154">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="82569-155">Under **Scroll into View**, right-choose **Magritte** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="82569-155">Under **Scroll into View**, right-choose **Magritte** and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="82569-156">Faites défiler vers le bas de la page Exemples DOM.</span><span class="sxs-lookup"><span data-stu-id="82569-156">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="82569-157">Le `<li>Magritte</li>` nœud doit toujours être sélectionné dans votre arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="82569-157">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="82569-158">Si ce n’est pas le cas, revenir [à Scroll into view](#scroll-into-view) et recommencer.</span><span class="sxs-lookup"><span data-stu-id="82569-158">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="82569-159">Pointez sur `<li>Magritte</li>` le nœud, ouvrez le menu contextuel \(clic droit\), puis choisissez Faire **défiler l’affichage.**</span><span class="sxs-lookup"><span data-stu-id="82569-159">Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.</span></span>  <span data-ttu-id="82569-160">Votre port d’affichage défile vers le haut afin de passer en revue le nœud **Magritte.**</span><span class="sxs-lookup"><span data-stu-id="82569-160">Your viewport scrolls back up so that you may review the **Magritte** node.</span></span>  <span data-ttu-id="82569-161">Accédez à [l’Annexe : options manquantes](#appendix-missing-options) si vous n’êtes pas en mesure de passer en revue l’option **Défilement vers l’affichage.**</span><span class="sxs-lookup"><span data-stu-id="82569-161">Navigate to [Appendix: Missing options](#appendix-missing-options) if you are not able to review the **Scroll into view** option.</span></span>
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Faire défiler vers l’avant" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **<span data-ttu-id="82569-163">Faire défiler vers l’avant</span><span class="sxs-lookup"><span data-stu-id="82569-163">Scroll into view</span></span>**  
    :::image-end:::  

### <a name="search-for-nodes"></a><span data-ttu-id="82569-164">Rechercher des nodes</span><span class="sxs-lookup"><span data-stu-id="82569-164">Search for nodes</span></span>  

<span data-ttu-id="82569-165">Vous pouvez effectuer une recherche dans l’arborescence DOM par chaîne, sélecteur CSS ou sélecteur XPath.</span><span class="sxs-lookup"><span data-stu-id="82569-165">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="82569-166">Concentrez votre curseur sur **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="82569-166">Focus your cursor on the **Elements** tool.</span></span>  
1.  <span data-ttu-id="82569-167">Sélectionnez `Control` + `F` \(Windows, Linux\) ou `Command` + `F` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="82569-167">Select `Control`+`F` \(Windows, Linux\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="82569-168">La barre de recherche s’ouvre en bas de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="82569-168">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="82569-169">Entrez `The Moon is a Harsh Mistress`.</span><span class="sxs-lookup"><span data-stu-id="82569-169">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="82569-170">La dernière phrase est mise en évidence dans l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="82569-170">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Mettre la requête en surbrill valeur dans la barre de recherche" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       <span data-ttu-id="82569-172">Mettre la requête en surbrill valeur dans la barre de recherche</span><span class="sxs-lookup"><span data-stu-id="82569-172">Highlight the query in the Search bar</span></span>  
    :::image-end:::  
    
<span data-ttu-id="82569-173">Comme mentionné ci-dessus, la barre de recherche prend également en charge les sélecteurs CSS et XPath.</span><span class="sxs-lookup"><span data-stu-id="82569-173">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <a name="edit-the-dom"></a><span data-ttu-id="82569-174">Modifier le DOM</span><span class="sxs-lookup"><span data-stu-id="82569-174">Edit the DOM</span></span>  

<span data-ttu-id="82569-175">Vous pouvez modifier le DOM à la volée et examiner l’impact des modifications sur la page.</span><span class="sxs-lookup"><span data-stu-id="82569-175">You may edit the DOM on the fly and review how the changes affect the page.</span></span>  

### <a name="edit-content"></a><span data-ttu-id="82569-176">Modifier le contenu</span><span class="sxs-lookup"><span data-stu-id="82569-176">Edit content</span></span>  

<span data-ttu-id="82569-177">Pour modifier le contenu d’un nœud, double-cliquez sur le contenu dans l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="82569-177">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="82569-178">[Ouvrez des exemples DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="82569-178">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="82569-179">Under **Edit Content**, right-choose **Michelle** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="82569-179">Under **Edit Content**, right-choose **Michelle** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="82569-180">Dans l’arborescence DOM, double-cliquez `Michelle` sur .</span><span class="sxs-lookup"><span data-stu-id="82569-180">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="82569-181">En d’autres termes, double-cliquez sur le texte entre `<li>` et `</li>` .</span><span class="sxs-lookup"><span data-stu-id="82569-181">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="82569-182">Le texte est mis en surbrillant pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="82569-182">The text is highlighted to indicate that it is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Modifier le texte" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           <span data-ttu-id="82569-184">Modifier le texte</span><span class="sxs-lookup"><span data-stu-id="82569-184">Edit the text</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="82569-185">Supprimer `Michelle` , `Leela` tapez , puis `Enter` sélectionnez pour confirmer la modification.</span><span class="sxs-lookup"><span data-stu-id="82569-185">Delete `Michelle`, type `Leela`, then select `Enter` to confirm the change.</span></span>  <span data-ttu-id="82569-186">Le texte du DOM change de **Michelle** en **Leela**.</span><span class="sxs-lookup"><span data-stu-id="82569-186">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <a name="edit-attributes"></a><span data-ttu-id="82569-187">Modifier les attributs</span><span class="sxs-lookup"><span data-stu-id="82569-187">Edit attributes</span></span>  

<span data-ttu-id="82569-188">Pour modifier les attributs, double-cliquez sur le nom ou la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="82569-188">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="82569-189">Suivez les instructions pour apprendre à ajouter des attributs à un nœud.</span><span class="sxs-lookup"><span data-stu-id="82569-189">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="82569-190">[Ouvrez des exemples DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="82569-190">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="82569-191">Under **Edit Attributes**, right-choose **Contrôle** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="82569-191">Under **Edit Attributes**, right-choose **Howard** and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="82569-192">Double-cliquez `<li>` sur .</span><span class="sxs-lookup"><span data-stu-id="82569-192">Double-click `<li>`.</span></span>  <span data-ttu-id="82569-193">Le texte est mis en surbrillade pour indiquer que le nœud est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="82569-193">The text is highlighted to indicate that the node is selected.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Modifier le nœud" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       <span data-ttu-id="82569-195">Modifier le nœud</span><span class="sxs-lookup"><span data-stu-id="82569-195">Edit the node</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="82569-196">Sélectionnez `Right` la touche de direction, ajoutez un espace, `style="background-color:gold"` tapez, puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="82569-196">Select the `Right` arrow key, add a space, type `style="background-color:gold"`, and then select `Enter`.</span></span>  <span data-ttu-id="82569-197">La couleur d’arrière-plan du nœud est or.</span><span class="sxs-lookup"><span data-stu-id="82569-197">The background color of the node changes to gold.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Ajouter un attribut de style au nœud" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       <span data-ttu-id="82569-199">Ajouter un `style` attribut au nœud</span><span class="sxs-lookup"><span data-stu-id="82569-199">Add a `style` attribute to the node</span></span>  
    :::image-end:::  
    
### <a name="edit-node-type"></a><span data-ttu-id="82569-200">Modifier le type de nœud</span><span class="sxs-lookup"><span data-stu-id="82569-200">Edit node type</span></span>  

<span data-ttu-id="82569-201">Pour modifier le type d’un nœud, double-cliquez sur le type, puis tapez le nouveau type.</span><span class="sxs-lookup"><span data-stu-id="82569-201">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="82569-202">[Ouvrez des exemples DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="82569-202">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="82569-203">Under **Edit Node Type**, right-chooseEve and choose **Inspect**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="82569-203">Under **Edit Node Type**, right-choose **Hank** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="82569-204">Double-cliquez `<li>` sur .</span><span class="sxs-lookup"><span data-stu-id="82569-204">Double-click `<li>`.</span></span>  <span data-ttu-id="82569-205">Le texte `li` est mis en surbrillant.</span><span class="sxs-lookup"><span data-stu-id="82569-205">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="82569-206">`li`Supprimer, `button` tapez, puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="82569-206">Delete `li`, type `button`, then select `Enter`.</span></span>  <span data-ttu-id="82569-207">Le `<li>` nœud est changé en `<button>` nœud.</span><span class="sxs-lookup"><span data-stu-id="82569-207">The `<li>` node changes to a `<button>` node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Changer le type de nœud en bouton" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           <span data-ttu-id="82569-209">Modifier le type de nœud par</span><span class="sxs-lookup"><span data-stu-id="82569-209">Change the node type to</span></span> `button`  
        :::image-end:::  
        
### <a name="reorder-dom-nodes"></a><span data-ttu-id="82569-210">Réordez les nodes DOM</span><span class="sxs-lookup"><span data-stu-id="82569-210">Reorder DOM nodes</span></span>  

<span data-ttu-id="82569-211">Faites glisser les nodes pour les réorder.</span><span class="sxs-lookup"><span data-stu-id="82569-211">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="82569-212">[Ouvrez des exemples DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="82569-212">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="82569-213">Under **Reorder DOM Nodes**, right-choose **Contrôle and** choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="82569-213">Under **Reorder DOM Nodes**, right-choose **Elvis Presley** and choose **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="82569-214">Il s’agit du dernier élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="82569-214">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="82569-215">Dans l’arborescence DOM, faites `<li>Elvis Presley</li>` glisser vers le haut de la liste.</span><span class="sxs-lookup"><span data-stu-id="82569-215">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Faire glisser le nœud vers le haut de la liste" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           <span data-ttu-id="82569-217">Faire glisser le nœud vers le haut de la liste</span><span class="sxs-lookup"><span data-stu-id="82569-217">Drag the node to the top of the list</span></span>  
        :::image-end:::  
        
### <a name="force-state"></a><span data-ttu-id="82569-218">État de force</span><span class="sxs-lookup"><span data-stu-id="82569-218">Force state</span></span>  

<span data-ttu-id="82569-219">Vous pouvez forcer les nodes à rester dans les états, y compris `:active` , , `:hover` et `:focus` `:visited` `:focus-within` .</span><span class="sxs-lookup"><span data-stu-id="82569-219">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="82569-220">[Ouvrez des exemples DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="82569-220">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="82569-221">Dans **l’état Force,** **pointez sur le cadre de l’en-dessous.**</span><span class="sxs-lookup"><span data-stu-id="82569-221">Under **Force state**, hover on **The Lord of the Flies**.</span></span>  <span data-ttu-id="82569-222">La couleur d’arrière-plan devient orange.</span><span class="sxs-lookup"><span data-stu-id="82569-222">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="82569-223">Pointez **sur le Bouton de l’enfant,** ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.</span><span class="sxs-lookup"><span data-stu-id="82569-223">Hover on **The Lord of the Flies**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="82569-224">Pointez `<li class="demo--hover">The Lord of the Flies</li>` dessus, ouvrez le menu contextuel \(clic droit\), puis choisissez **Force State**  >  **:hover**.</span><span class="sxs-lookup"><span data-stu-id="82569-224">Hover on `<li class="demo--hover">The Lord of the Flies</li>`, open the contextual menu \(right-click\), and choose **Force State** > **:hover**.</span></span>  <span data-ttu-id="82569-225">Accédez à [l’Annexe : Options manquantes](#appendix-missing-options) si l’option n’est pas affichée.</span><span class="sxs-lookup"><span data-stu-id="82569-225">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  <span data-ttu-id="82569-226">La couleur d’arrière-plan reste orange même si vous ne pointez pas réellement sur le nœud.</span><span class="sxs-lookup"><span data-stu-id="82569-226">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <a name="hide-a-node"></a><span data-ttu-id="82569-227">Masquer un nœud</span><span class="sxs-lookup"><span data-stu-id="82569-227">Hide a node</span></span>  

<span data-ttu-id="82569-228">Sélectionnez `H` pour masquer un nœud.</span><span class="sxs-lookup"><span data-stu-id="82569-228">Select `H` to hide a node.</span></span>  

1.  <span data-ttu-id="82569-229">[Ouvrez des exemples DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="82569-229">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="82569-230">Sous **Masquer un nœud,** choisissez avec le droit de la main **Les étoiles ma destination** et sélectionnez **Inspecter.**</span><span class="sxs-lookup"><span data-stu-id="82569-230">Under **Hide a node**, right-choose **The Stars My Destination** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="82569-231">Sélectionnez la `H` clé.</span><span class="sxs-lookup"><span data-stu-id="82569-231">Select the `H` key.</span></span>  <span data-ttu-id="82569-232">Le nœud est masqué.</span><span class="sxs-lookup"><span data-stu-id="82569-232">The node is hidden.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Apparence du nœud dans l’arborescence DOM une fois masqué" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           <span data-ttu-id="82569-234">Apparence du nœud dans l’arborescence DOM une fois masqué</span><span class="sxs-lookup"><span data-stu-id="82569-234">What the node looks like in the DOM Tree after it is hidden</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="82569-235">Sélectionnez `H` de nouveau la clé.</span><span class="sxs-lookup"><span data-stu-id="82569-235">Select the `H` key again.</span></span>  <span data-ttu-id="82569-236">Le nœud est de nouveau affiché.</span><span class="sxs-lookup"><span data-stu-id="82569-236">The node is shown again.</span></span>  

### <a name="delete-a-node"></a><span data-ttu-id="82569-237">Supprimer un nœud</span><span class="sxs-lookup"><span data-stu-id="82569-237">Delete a node</span></span>  

<span data-ttu-id="82569-238">Sélectionnez `Delete` pour supprimer un nœud.</span><span class="sxs-lookup"><span data-stu-id="82569-238">Select `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="82569-239">[Ouvrez des exemples DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="82569-239">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="82569-240">Under **Delete a Node**, right-choose **Foundation** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="82569-240">Under **Delete a Node**, right-choose **Foundation** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="82569-241">Sélectionnez la `Delete` clé.</span><span class="sxs-lookup"><span data-stu-id="82569-241">Select the `Delete` key.</span></span>  <span data-ttu-id="82569-242">Le nœud est supprimé.</span><span class="sxs-lookup"><span data-stu-id="82569-242">The node is deleted.</span></span>  
    1.  <span data-ttu-id="82569-243">Sélectionnez `Control` + `Z` \(Windows, Linux\) ou `Command` + `Z` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="82569-243">Select `Control`+`Z` \(Windows, Linux\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="82569-244">La dernière action est annulée et le nœud réapparaît.</span><span class="sxs-lookup"><span data-stu-id="82569-244">The last action is undone and the node reappears.</span></span>  

## <a name="access-nodes-in-the-console"></a><span data-ttu-id="82569-245">Accès aux nodes dans la console</span><span class="sxs-lookup"><span data-stu-id="82569-245">Access nodes in the Console</span></span>  

<span data-ttu-id="82569-246">DevTools fournit quelques raccourcis pour accéder aux nodes DOM à partir de la console ou obtenir des références JavaScript à chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="82569-246">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <a name="reference-the-currently-selected-node-with-0"></a><span data-ttu-id="82569-247">Référencer le nœud actuellement sélectionné avec 0 $</span><span class="sxs-lookup"><span data-stu-id="82569-247">Reference the currently-selected node with $0</span></span>  

<span data-ttu-id="82569-248">Lorsque vous examinez un nœud, le texte en face du nœud signifie que vous pouvez faire référence à ce nœud dans la `== $0` console avec la variable `$0` .</span><span class="sxs-lookup"><span data-stu-id="82569-248">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="82569-249">[Ouvrez des exemples DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="82569-249">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="82569-250">Sous Référencer le nœud actuellement sélectionné avec **0 $,** choisissez la **main gauche** de la noirceur et choisissez **Inspecter**.</span><span class="sxs-lookup"><span data-stu-id="82569-250">Under **Reference the currently-selected node with $0**, right-choose **The Left Hand of Darkness** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="82569-251">Sélectionnez `Escape` la clé pour ouvrir le caisse de la console.</span><span class="sxs-lookup"><span data-stu-id="82569-251">Select the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="82569-252">Tapez `$0` et sélectionnez la `Enter` clé.</span><span class="sxs-lookup"><span data-stu-id="82569-252">Type `$0` and select the `Enter` key.</span></span>  <span data-ttu-id="82569-253">Le résultat de l’expression indique `$0` que le résultat est `<li>The Left Hand of Darkness</li>` .</span><span class="sxs-lookup"><span data-stu-id="82569-253">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Résultat de la première expression $0 dans la console" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            <span data-ttu-id="82569-255">Résultat de la première `$0` expression dans la **console**</span><span class="sxs-lookup"><span data-stu-id="82569-255">The result of the first `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="82569-256">Pointez sur le résultat.</span><span class="sxs-lookup"><span data-stu-id="82569-256">Hover on the result.</span></span>  <span data-ttu-id="82569-257">Le nœud est mis en surbrillade dans laport d’affichage.</span><span class="sxs-lookup"><span data-stu-id="82569-257">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="82569-258">Choisissez `<li>Dune</li>` dans l’arborescence DOM, tapez `$0` de nouveau dans la console, puis sélectionnez à `Enter` nouveau.</span><span class="sxs-lookup"><span data-stu-id="82569-258">Choose `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then select `Enter` again.</span></span>  <span data-ttu-id="82569-259">À présent, `$0` évalue à `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="82569-259">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Résultat de la deuxième expression $0 dans la console" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           <span data-ttu-id="82569-261">Résultat de la deuxième `$0` expression dans la **console**</span><span class="sxs-lookup"><span data-stu-id="82569-261">The result of the second `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
### <a name="store-as-global-variable"></a><span data-ttu-id="82569-262">Store en tant que variable globale</span><span class="sxs-lookup"><span data-stu-id="82569-262">Store as global variable</span></span>  

<span data-ttu-id="82569-263">Si vous devez faire référence à un nœud plusieurs fois, stockez-le en tant que variable globale.</span><span class="sxs-lookup"><span data-stu-id="82569-263">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="82569-264">[Ouvrez des exemples DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="82569-264">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="82569-265">Sous **Store en tant que variable globale,** pointez sur la grande **veille,** ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.</span><span class="sxs-lookup"><span data-stu-id="82569-265">Under **Store as global variable**, hover on **The Big Sleep**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="82569-266">Pointez `<li>The Big Sleep</li>` dessus dans l’arborescence DOM, ouvrez le menu contextuel \(clic droit\), puis choisissez Store en tant que variable **globale.**</span><span class="sxs-lookup"><span data-stu-id="82569-266">Hover on `<li>The Big Sleep</li>` in the DOM Tree, open the contextual menu \(right-click\), and choose **Store as global variable**.</span></span>  <span data-ttu-id="82569-267">Accédez à [l’Annexe : Options manquantes](#appendix-missing-options) si l’option n’est pas affichée.</span><span class="sxs-lookup"><span data-stu-id="82569-267">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="82569-268">Tapez `temp1` dans la console, puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="82569-268">Type `temp1` in the Console and then select `Enter`.</span></span>  <span data-ttu-id="82569-269">Le résultat de l’expression indique que la variable est évaluée au nœud.</span><span class="sxs-lookup"><span data-stu-id="82569-269">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Résultat de l’expression temp1" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           <span data-ttu-id="82569-271">Résultat de `temp1` l’expression</span><span class="sxs-lookup"><span data-stu-id="82569-271">The result of the `temp1` expression</span></span>  
        :::image-end:::  
        
### <a name="copy-js-path"></a><span data-ttu-id="82569-272">Copier le chemin d’accès JS</span><span class="sxs-lookup"><span data-stu-id="82569-272">Copy JS path</span></span>  

<span data-ttu-id="82569-273">Copiez le chemin d’accès JavaScript sur un nœud lorsque vous devez le référencer dans un test automatisé.</span><span class="sxs-lookup"><span data-stu-id="82569-273">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="82569-274">[Ouvrez des exemples DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="82569-274">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="82569-275">Sous **Copier le chemin d’accès JS,** pointez sur le contrôle **ContrôleZov,** ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.</span><span class="sxs-lookup"><span data-stu-id="82569-275">Under **Copy JS path**, hover on **The Brothers Karamazov**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="82569-276">Pointez `<li>The Brothers Karamazov</li>` dessus dans l’arborescence DOM, ouvrez le menu contextuel \(clic droit\), puis choisissez **Copier**le  >  **chemin d’accès JS**.</span><span class="sxs-lookup"><span data-stu-id="82569-276">Hover on `<li>The Brothers Karamazov</li>` in the DOM Tree, open the contextual menu \(right-click\), and choose **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="82569-277">Une expression résolue en nœud a `document.querySelector()` été copiée dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="82569-277">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="82569-278">Sélectionnez `Control` + `V` \(Windows, Linux\) ou `Command` + `V` \(macOS\) pour coller l’expression dans la console.</span><span class="sxs-lookup"><span data-stu-id="82569-278">Select `Control`+`V` \(Windows, Linux\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="82569-279">Sélectionnez `Enter` pour évaluer l’expression.</span><span class="sxs-lookup"><span data-stu-id="82569-279">Select `Enter` to evaluate the expression.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Résultat de l’expression Copier le chemin d’accès JS" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           <span data-ttu-id="82569-281">Résultat de l’expression **Copier le chemin d’accès JS**</span><span class="sxs-lookup"><span data-stu-id="82569-281">The result of the **Copy JS Path** expression</span></span>  
        :::image-end:::  
        
## <a name="break-on-dom-changes"></a><span data-ttu-id="82569-282">Pause sur les modifications DOM</span><span class="sxs-lookup"><span data-stu-id="82569-282">Break on DOM changes</span></span>  

<span data-ttu-id="82569-283">DevTools vous permet de suspendre le code JavaScript d’une page lorsque javaScript modifie le DOM.</span><span class="sxs-lookup"><span data-stu-id="82569-283">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <a name="break-on-attribute-modifications"></a><span data-ttu-id="82569-284">Pause sur les modifications d’attribut</span><span class="sxs-lookup"><span data-stu-id="82569-284">Break on attribute modifications</span></span>  

<span data-ttu-id="82569-285">Utilisez des points d’arrêt de modification d’attribut lorsque vous souhaitez suspendre le JavaScript qui entraîne la modification de n’importe quel attribut d’un nœud.</span><span class="sxs-lookup"><span data-stu-id="82569-285">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="82569-286">[Ouvrez des exemples DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="82569-286">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="82569-287">Under **Break on attribute modifications**, right-choose **Saueruterut** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="82569-287">Under **Break on attribute modifications**, right-choose **Sauerkraut** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="82569-288">Dans l’arborescence DOM, pointez sur , ouvrez le menu contextuel `<li id="target">Sauerkraut</li>` \(clic droit\), puis choisissez **Break On**  >  **Attribute Modifications**.</span><span class="sxs-lookup"><span data-stu-id="82569-288">In the DOM Tree, hover on `<li id="target">Sauerkraut</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="82569-289">Accédez à [l’Annexe : Options manquantes](#appendix-missing-options) si l’option n’est pas affichée.</span><span class="sxs-lookup"><span data-stu-id="82569-289">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Pause sur les modifications d’attribut" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **<span data-ttu-id="82569-291">Pause sur les modifications d’attribut</span><span class="sxs-lookup"><span data-stu-id="82569-291">Break on attribute modifications</span></span>**  
        :::image-end:::  
        
    1.  <span data-ttu-id="82569-292">À l’étape suivante, il vous sera demandé de choisir un bouton qui interrompt le code de la page.</span><span class="sxs-lookup"><span data-stu-id="82569-292">In the next step you are going to be instructed to choose a button that pauses the code of the page.</span></span>  <span data-ttu-id="82569-293">Une fois la page suspendue, vous ne pouvez plus la faire défiler.</span><span class="sxs-lookup"><span data-stu-id="82569-293">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="82569-294">Vous devez choisir **Resume Script** \( Resume Script \) pour que la page défile ![ à ](../media/resume-script-icon.msft.png) nouveau.</span><span class="sxs-lookup"><span data-stu-id="82569-294">You must choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\) in order to make the page scrollable again.</span></span>
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Où reprendre l’exécution du script" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           <span data-ttu-id="82569-296">Où reprendre l’exécution du script</span><span class="sxs-lookup"><span data-stu-id="82569-296">Where to resume script running</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="82569-297">Sélectionnez le **bouton Définir l’arrière-plan** ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="82569-297">Choose the **Set Background** button above.</span></span>  <span data-ttu-id="82569-298">Cela définit `style` l’attribut du nœud sur `background-color:thistle` .</span><span class="sxs-lookup"><span data-stu-id="82569-298">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="82569-299">DevTools suspend la page et met en évidence le code à l’origine de la modification de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="82569-299">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="82569-300">Choose **Resume Script** \( Resume Script ![ ](../media/resume-script-icon.msft.png) \), as mentioned earlier.</span><span class="sxs-lookup"><span data-stu-id="82569-300">Choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\), as mentioned earlier.</span></span>  
    
### <a name="break-on-node-removal"></a><span data-ttu-id="82569-301">Rupture lors de la suppression du nœud</span><span class="sxs-lookup"><span data-stu-id="82569-301">Break on node removal</span></span>  

<span data-ttu-id="82569-302">Si vous souhaitez suspendre lorsqu’un nœud particulier est supprimé, utilisez des points d’arrêt de suppression de nœud.</span><span class="sxs-lookup"><span data-stu-id="82569-302">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="82569-303">[Ouvrez des exemples DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="82569-303">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="82569-304">Under **Break on Node Removal**, right-choose **Contrôlemancer** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="82569-304">Under **Break on Node Removal**, right-choose **Neuromancer** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="82569-305">Dans l’arborescence DOM, pointez sur , ouvrez le menu contextuel `<li id="target">Neuromancer</li>` \(clic droit\), puis choisissez **Pause sur**la suppression  >  **du nœud.**</span><span class="sxs-lookup"><span data-stu-id="82569-305">In the DOM Tree, hover on `<li id="target">Neuromancer</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="82569-306">Accédez à [l’Annexe : Options manquantes](#appendix-missing-options) si l’option n’est pas affichée.</span><span class="sxs-lookup"><span data-stu-id="82569-306">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="82569-307">Sélectionnez le **bouton Supprimer** ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="82569-307">Choose the **Delete** button above.</span></span>  <span data-ttu-id="82569-308">DevTools suspend la page et met en évidence le code à l’origine de la suppression du nœud.</span><span class="sxs-lookup"><span data-stu-id="82569-308">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="82569-309">Choose **Resume Script** \( Resume Script ![ ](../media/resume-script-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="82569-309">Choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\).</span></span>  
    
### <a name="break-on-subtree-modifications"></a><span data-ttu-id="82569-310">Pause sur les modifications de sous-arbre</span><span class="sxs-lookup"><span data-stu-id="82569-310">Break on subtree modifications</span></span>  

<span data-ttu-id="82569-311">Après avoir placé un point d’arrêt de modification de sous-arbre sur un nœud, DevTools interrompt la page lorsque l’un des descendants du nœud est ajouté ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="82569-311">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="82569-312">[Ouvrez des exemples DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="82569-312">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="82569-313">Under **Break on Subtree Modifications**, right-choose A Fire Upon The **Deep** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="82569-313">Under **Break on Subtree Modifications**, right-choose **A Fire Upon The Deep** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="82569-314">Dans l’arborescence DOM, pointez sur , qui est le nœud ci-dessus, ouvrez le menu contextuel `<ul id="target">` `<li>A Fire Upon the Deep</li>` \(clic droit\), puis choisissez **Break On**  >  **Subtree Modifications**.</span><span class="sxs-lookup"><span data-stu-id="82569-314">In the DOM Tree, hover on `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="82569-315">Si l’option n’est pas affichée, accédez à Annexe [: Options manquantes.](#appendix-missing-options)</span><span class="sxs-lookup"><span data-stu-id="82569-315">If the option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).</span></span>  
    1.  <span data-ttu-id="82569-316">Choose **Add Child**.</span><span class="sxs-lookup"><span data-stu-id="82569-316">Choose **Add Child**.</span></span>  <span data-ttu-id="82569-317">Le code s’interrompt car un nœud a `<li>` été ajouté à la liste.</span><span class="sxs-lookup"><span data-stu-id="82569-317">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="82569-318">Choose **Resume Script** \( Resume Script ![ ](../media/resume-script-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="82569-318">Choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\).</span></span>  
    
## <a name="next-steps"></a><span data-ttu-id="82569-319">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="82569-319">Next steps</span></span>  

<span data-ttu-id="82569-320">Cela couvre la plupart des fonctionnalités DOM dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="82569-320">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="82569-321">Vous pouvez découvrir le reste des fonctionnalités en pointant sur les nodes dans l’arborescence DOM, en ouvrant le menu contextuel \(clic droit\) et en testant les autres options qui n’ont pas été couvertes dans ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="82569-321">You are able to discover the rest of the features by hovering on nodes in the DOM Tree, opening the contextual menu \(right-click\), and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="82569-322">Accédez aux [raccourcis clavier du panneau][DevToolsShortcutsElements]Éléments.</span><span class="sxs-lookup"><span data-stu-id="82569-322">Navigate to [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="82569-323">Consultez la [page d’accueil de Microsoft Edge DevTools][MicrosoftEdgeDevTools] pour découvrir tout ce que vous pouvez faire avec DevTools.</span><span class="sxs-lookup"><span data-stu-id="82569-323">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--Navigate to [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## <a name="appendix-html-versus-the-dom"></a><span data-ttu-id="82569-324">Annexe : HTML par rapport au DOM</span><span class="sxs-lookup"><span data-stu-id="82569-324">Appendix: HTML versus the DOM</span></span>  

<span data-ttu-id="82569-325">La section suivante explique rapidement la différence entre le code HTML et le DOM.</span><span class="sxs-lookup"><span data-stu-id="82569-325">The following section quickly explains the difference between HTML and the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="82569-326">Lorsque vous utilisez un navigateur web pour demander une page, le serveur renvoie du code HTML comme l’extrait de code suivant</span><span class="sxs-lookup"><span data-stu-id="82569-326">When you use a web browser to request a page, the server returns HTML like the following code snippet</span></span>  

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
      <span data-ttu-id="82569-327">Le navigateur pare le code HTML et crée une arborescence d’objets comme la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="82569-327">The browser parses the HTML and creates a tree of objects like the following list.</span></span>  
      
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

<span data-ttu-id="82569-328">Cette arborescence d’objets, ou de nodes, représentant le contenu de la page est appelée DOM.</span><span class="sxs-lookup"><span data-stu-id="82569-328">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="82569-329">Pour l’instant, il ressemble au code HTML, mais supposons que le script référencé en bas du code HTML exécute l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="82569-329">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs the following code snippet.</span></span>  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="82569-330">Ce code supprime le `h1` nœud et ajoute un autre nœud au `p` DOM.</span><span class="sxs-lookup"><span data-stu-id="82569-330">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="82569-331">Le DOM complet affiche maintenant la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="82569-331">The complete DOM now displays the following list.</span></span>  
      
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

<span data-ttu-id="82569-332">Le code HTML de la page est désormais différent du DOM.</span><span class="sxs-lookup"><span data-stu-id="82569-332">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="82569-333">En d’autres termes, html représente le contenu de la page initiale et le DOM représente le contenu de la page actuelle.</span><span class="sxs-lookup"><span data-stu-id="82569-333">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="82569-334">Lorsque JavaScript ajoute, supprime ou modifie des nodes, le DOM devient différent du code HTML.</span><span class="sxs-lookup"><span data-stu-id="82569-334">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="82569-335">Accédez [à Introduction au DOM][MDNIntroductionToDOM] pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="82569-335">Navigate to [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.  Your viewport scrolls back up so that the **Magritte** node is displayed.  If you the **Scroll into view** option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## <a name="appendix-missing-options"></a><span data-ttu-id="82569-336">Annexe : Options manquantes</span><span class="sxs-lookup"><span data-stu-id="82569-336">Appendix: Missing options</span></span>  

<span data-ttu-id="82569-337">De nombreuses instructions de ce didacticiel vous indiquent de pointer sur un nœud dans l’arborescence DOM, d’ouvrir le menu contextuel \(clic droit\), puis de choisir une option dans le menu contextuel qui s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="82569-337">Many of the instructions in this tutorial instruct you to hover on a node in the DOM Tree, open the contextual menu \(right-click\), and then choose an option from the context menu that pops up.</span></span>  <span data-ttu-id="82569-338">Si l’option spécifiée dans le menu contextuel n’est pas affichée, essayez de pointer à l’extérieur du texte du nœud et d’ouvrir le menu contextuel \(clic droit\).</span><span class="sxs-lookup"><span data-stu-id="82569-338">If the specified option in the context menu is not displayed, try hovering away from the node text and opening the contextual menu \(right-click\).</span></span>  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Où choisir si toutes les options ne sont pas affichées" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   <span data-ttu-id="82569-340">Où choisir si toutes les options ne sont pas affichées</span><span class="sxs-lookup"><span data-stu-id="82569-340">Where to choose if all of the options are not displayed</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="82569-341">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="82569-341">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge \(Chromium\) | Documents Microsoft"  
[DevToolsCssGetStarted]: ../css/index.md "Commencer à afficher et modifier les | Documents Microsoft"  
[DevToolsShortcutsElements]: ../shortcuts/index.md#elements-tool-keyboard-shortcuts "Raccourcis clavier de l’outil Éléments : raccourcis clavier Microsoft Edge DevTools | Documents Microsoft"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Exemple de dom Microsoft Edge (Chromium) DevTools | Glitch"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Présentation de la | DOM MDN"  

> [!NOTE]
> <span data-ttu-id="82569-347">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="82569-347">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="82569-348">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/dom/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="82569-348">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="82569-350">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="82569-350">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
