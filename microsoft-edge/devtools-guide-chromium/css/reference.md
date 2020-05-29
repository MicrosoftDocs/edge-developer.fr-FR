---
title: Référence CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 005d2650a1633d49a8c6c2550c4b2c0c2e3f3be6
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601845"
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







# <span data-ttu-id="130ab-103">Référence CSS</span><span class="sxs-lookup"><span data-stu-id="130ab-103">CSS Reference</span></span>   



<span data-ttu-id="130ab-104">Découvrez de nouveaux flux de travail dans cette référence complète des fonctionnalités de Microsoft Edge DevTools liées à l’affichage et à la modification de feuilles CSS.</span><span class="sxs-lookup"><span data-stu-id="130ab-104">Discover new workflows in this comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="130ab-105">Pour en savoir plus sur les concepts de base, voir prendre en [main l’affichage et la modification de feuilles CSS][DevToolsCSSGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="130ab-105">See [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted] to learn the basics.</span></span>  

## <span data-ttu-id="130ab-106">Sélectionner un élément</span><span class="sxs-lookup"><span data-stu-id="130ab-106">Select an element</span></span>   

<span data-ttu-id="130ab-107">Le panneau **éléments** de devtools vous permet d’afficher ou de modifier la feuille de style CSS d’un élément à la fois.</span><span class="sxs-lookup"><span data-stu-id="130ab-107">The **Elements** panel of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="130ab-108">L’élément sélectionné est mis en surbrillance dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="130ab-108">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="130ab-109">Les styles de l’élément apparaissent dans le volet **styles** .</span><span class="sxs-lookup"><span data-stu-id="130ab-109">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="130ab-110">Voir [afficher la feuille de style en cascade (CSS) d’un élément][DevToolsCSSGetStartedTutorial] pour un didacticiel.</span><span class="sxs-lookup"><span data-stu-id="130ab-110">See [View the CSS for an element][DevToolsCSSGetStartedTutorial] for a tutorial.</span></span>  

> [!NOTE]
> <span data-ttu-id="130ab-111">Dans la [figure 1](#figure-1), l' `h1` élément qui est surligné dans l' **arborescence DOM** est l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="130ab-111">In [Figure 1](#figure-1), the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="130ab-112">À droite, les styles de l’élément apparaissent dans le volet **styles** .</span><span class="sxs-lookup"><span data-stu-id="130ab-112">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="130ab-113">Sur la gauche, l’élément est mis en surbrillance dans la fenêtre d’affichage, mais uniquement dans la mesure où la souris pointe actuellement sur celle-ci dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="130ab-113">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

> ##### <span data-ttu-id="130ab-114">Figure1</span><span class="sxs-lookup"><span data-stu-id="130ab-114">Figure 1</span></span>  
> <span data-ttu-id="130ab-115">Exemple d’élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="130ab-115">An example of a selected element</span></span>  
> ![Exemple d’élément sélectionné][ImageSelectedElement]  

<span data-ttu-id="130ab-117">Il existe de nombreuses façons de sélectionner un élément:</span><span class="sxs-lookup"><span data-stu-id="130ab-117">There are many ways to select an element:</span></span>  

*   <span data-ttu-id="130ab-118">Dans votre fenêtre d’affichage, cliquez avec le bouton droit sur l’élément, puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="130ab-118">In your viewport, right-click the element and select **Inspect**.</span></span>  
*   <span data-ttu-id="130ab-119">Dans devtools, cliquez sur **Sélectionner un élément** ![ Sélectionnez un élément ][ImageSelectAnElementIcon] ou appuyez sur `Control` + `Shift` + `C` \ (Windows \) ou `Command` + `Shift` + `C` \ (MacOS \), puis cliquez sur l’élément dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="130ab-119">In DevTools, click **Select an element** ![Select an element][ImageSelectAnElementIcon] or press `Control`+`Shift`+`C` \(Windows\) or `Command`+`Shift`+`C` \(macOS\), and then click the element in the viewport.</span></span>  
*   <span data-ttu-id="130ab-120">Dans DevTools, cliquez sur l’élément dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="130ab-120">In DevTools, click the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="130ab-121">Dans DevTools, exécutez une requête telle que `document.querySelector('p')` dans la **console**, cliquez avec le bouton droit sur le résultat, puis sélectionnez **afficher dans le panneau éléments**.</span><span class="sxs-lookup"><span data-stu-id="130ab-121">In DevTools, run a query like `document.querySelector('p')` in the **Console**, right-click the result, and then select **Reveal in Elements panel**.</span></span>  

## <span data-ttu-id="130ab-122">Afficher les feuilles CSS</span><span class="sxs-lookup"><span data-stu-id="130ab-122">View CSS</span></span>   

### <span data-ttu-id="130ab-123">Affichage de la feuille de style externe dans laquelle une règle est définie</span><span class="sxs-lookup"><span data-stu-id="130ab-123">View the external stylesheet where a rule is defined</span></span>   

<span data-ttu-id="130ab-124">Dans le volet **styles** , cliquez sur le lien en regard d’une règle CSS pour ouvrir la feuille de style externe qui définit la règle.</span><span class="sxs-lookup"><span data-stu-id="130ab-124">In the **Styles** pane, click the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  

<span data-ttu-id="130ab-125">Si la feuille de style est minified, voir [rendre un fichier minified lisible][DevToolsJavascriptReferenceFormat].</span><span class="sxs-lookup"><span data-stu-id="130ab-125">If the stylesheet is minified, see [Make a minified file readable][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="130ab-126">Dans la [figure 2](#figure-2), `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` un clic vous permet d’accéder à la ligne 2 de `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , où la `.content h1:first-of-type` règle CSS est définie.</span><span class="sxs-lookup"><span data-stu-id="130ab-126">In [Figure 2](#figure-2), clicking `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` takes you to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

> ##### <span data-ttu-id="130ab-127">Figure 2</span><span class="sxs-lookup"><span data-stu-id="130ab-127">Figure 2</span></span>  
> <span data-ttu-id="130ab-128">Affichage de la feuille de style dans laquelle une règle est définie</span><span class="sxs-lookup"><span data-stu-id="130ab-128">Viewing the stylesheet where a rule is defined</span></span>  
> ![Affichage de la feuille de style dans laquelle une règle est définie][ImageViewRuleStylesheet]  

### <span data-ttu-id="130ab-130">Afficher uniquement les feuilles CSS appliquées actuellement à un élément</span><span class="sxs-lookup"><span data-stu-id="130ab-130">View only the CSS that is actually applied to an element</span></span>   

<span data-ttu-id="130ab-131">L’onglet **styles** affiche toutes les règles qui s’appliquent à un élément, y compris les déclarations qui ont été remplacées.</span><span class="sxs-lookup"><span data-stu-id="130ab-131">The **Styles** tab shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="130ab-132">Lorsque vous n’êtes pas intéressé par des déclarations substituées, utilisez l’onglet **calculé** pour afficher uniquement les feuilles CSS qui sont réellement appliquées à un élément.</span><span class="sxs-lookup"><span data-stu-id="130ab-132">When you are not interested in overridden declarations, use the **Computed** tab to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="130ab-133">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="130ab-133">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="130ab-134">Accédez à l’onglet **calculé** dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="130ab-134">Go to the **Computed** tab in the **Elements** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="130ab-135">Dans le cas d’une fenêtre DevTools large, l’onglet **calculé** n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="130ab-135">On a wide DevTools window, the **Computed** tab does not exist.</span></span>  <span data-ttu-id="130ab-136">Le contenu de l’onglet **calculé** est affiché dans l’onglet **styles** .</span><span class="sxs-lookup"><span data-stu-id="130ab-136">The contents of the **Computed** tab are shown on the **Styles** tab.</span></span>  

<span data-ttu-id="130ab-137">Les propriétés héritées sont opaques.</span><span class="sxs-lookup"><span data-stu-id="130ab-137">Inherited properties are opaque.</span></span>  <span data-ttu-id="130ab-138">Cochez la case **Afficher tout** pour afficher toutes les valeurs héritées.</span><span class="sxs-lookup"><span data-stu-id="130ab-138">Check the **Show All** checkbox to see all inherited values.</span></span>  

> [!NOTE]
> <span data-ttu-id="130ab-139">Dans la [figure 3](#figure-3), l’onglet **calculé** montre les propriétés CSS qui sont appliquées à l’élément actuellement sélectionné `h1` .</span><span class="sxs-lookup"><span data-stu-id="130ab-139">In [Figure 3](#figure-3), the **Computed** tab shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

> ##### <span data-ttu-id="130ab-140">Figure3</span><span class="sxs-lookup"><span data-stu-id="130ab-140">Figure 3</span></span>  
> <span data-ttu-id="130ab-141">Onglet **calculé**</span><span class="sxs-lookup"><span data-stu-id="130ab-141">The **Computed** tab</span></span>  
> ![Onglet calculé][ImageComputedTab]  

### <span data-ttu-id="130ab-143">Afficher les propriétés CSS par ordre alphabétique</span><span class="sxs-lookup"><span data-stu-id="130ab-143">View CSS properties in alphabetical order</span></span>   

<span data-ttu-id="130ab-144">Utilisez l’onglet **calculé** .  Voir [afficher uniquement la feuille de style CSS qui est réellement appliquée à un élément](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="130ab-144">Use the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="130ab-145">Afficher les propriétés CSS héritées</span><span class="sxs-lookup"><span data-stu-id="130ab-145">View inherited CSS properties</span></span>   

<span data-ttu-id="130ab-146">Cochez la case **Afficher tout** dans l’onglet **calculé** .  Voir [afficher uniquement la feuille de style CSS qui est réellement appliquée à un élément](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="130ab-146">Check the **Show All** checkbox in the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="130ab-147">Afficher le modèle de boîte pour un élément</span><span class="sxs-lookup"><span data-stu-id="130ab-147">View the box model for an element</span></span>   

<span data-ttu-id="130ab-148">Pour afficher [le modèle de zone][MDNBoxModel] d’un élément, accédez à l’onglet **styles** .  Si votre fenêtre DevTools est étroite, le diagramme de **modèle de cadre** est en bas de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="130ab-148">To view [the box model][MDNBoxModel] of an element, go to the **Styles** tab.  If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the tab.</span></span>  

<span data-ttu-id="130ab-149">Pour modifier une valeur, double-cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="130ab-149">To change a value, double-click on it.</span></span>  

> [!NOTE]
> <span data-ttu-id="130ab-150">Dans la [figure 4](#figure-4), le diagramme de **modèle de cadre** sous l’onglet **styles** montre le modèle de zone de l’élément actuellement sélectionné `h1` .</span><span class="sxs-lookup"><span data-stu-id="130ab-150">In [Figure 4](#figure-4), the **Box Model** diagram in the **Styles** tab shows the box model for the currently selected `h1` element.</span></span>  

> ##### <span data-ttu-id="130ab-151">Figure 4</span><span class="sxs-lookup"><span data-stu-id="130ab-151">Figure 4</span></span>  
> <span data-ttu-id="130ab-152">Diagramme de **modèle de cadre**</span><span class="sxs-lookup"><span data-stu-id="130ab-152">The **Box Model** diagram</span></span>  
> ![Diagramme de modèle de cadre][ImageBoxModel]  

### <span data-ttu-id="130ab-154">Rechercher et filtrer la CSS d’un élément</span><span class="sxs-lookup"><span data-stu-id="130ab-154">Search and filter the CSS of an element</span></span>   

<span data-ttu-id="130ab-155">Utilisez la zone de texte **filtre** des **styles** et des onglets **calculés** pour rechercher des propriétés ou des valeurs CSS spécifiques.</span><span class="sxs-lookup"><span data-stu-id="130ab-155">Use the **Filter** text box on the **Styles** and **Computed** tabs to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="130ab-156">Pour effectuer une recherche dans les propriétés héritées dans l’onglet **calculé** , activez la case à cocher **Afficher tout** .</span><span class="sxs-lookup"><span data-stu-id="130ab-156">To also search inherited properties in the **Computed** tab, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="130ab-157">Dans la [figure 5](#figure-5), l’onglet **styles** est filtré pour afficher uniquement les règles qui incluent la requête de recherche `color` .</span><span class="sxs-lookup"><span data-stu-id="130ab-157">In [Figure 5](#figure-5), the **Styles** tab is filtered to only show rules that include the search query `color`.</span></span>  

> ##### <span data-ttu-id="130ab-158">Figure 5</span><span class="sxs-lookup"><span data-stu-id="130ab-158">Figure 5</span></span>  
> <span data-ttu-id="130ab-159">Filtrage de l’onglet **styles**</span><span class="sxs-lookup"><span data-stu-id="130ab-159">Filtering the **Styles** tab</span></span>  
> ![Filtrage de l’onglet styles][ImageStylesFilter]  

> [!NOTE]
> <span data-ttu-id="130ab-161">Dans la [figure 6](#figure-6), l’onglet **calculé** est filtré pour afficher uniquement les déclarations qui incluent la requête de recherche `100%` .</span><span class="sxs-lookup"><span data-stu-id="130ab-161">In [Figure 6](#figure-6), the **Computed** tab is filtered to only show declarations that include the search query `100%`.</span></span>  

> ##### <span data-ttu-id="130ab-162">Figure 6</span><span class="sxs-lookup"><span data-stu-id="130ab-162">Figure 6</span></span>  
> <span data-ttu-id="130ab-163">Filtrage de l’onglet **calculé**</span><span class="sxs-lookup"><span data-stu-id="130ab-163">Filtering the **Computed** tab</span></span>  
> ![Filtrage de l’onglet calculé][ImageComputerFilter]  

### <span data-ttu-id="130ab-165">Basculer une pseudo-classe</span><span class="sxs-lookup"><span data-stu-id="130ab-165">Toggle a pseudo-class</span></span>   

<span data-ttu-id="130ab-166">Pour basculer une pseudo-classe comme `:active` , `:focus` , `:hover` ou `:visited` :</span><span class="sxs-lookup"><span data-stu-id="130ab-166">To toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`:</span></span>  

1.  <span data-ttu-id="130ab-167">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="130ab-167">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="130ab-168">Dans le panneau **éléments** , accédez à l’onglet **styles** .</span><span class="sxs-lookup"><span data-stu-id="130ab-168">On the **Elements** panel, go to the **Styles** tab.</span></span>  
1.  <span data-ttu-id="130ab-169">Cliquez sur **: HOV**.</span><span class="sxs-lookup"><span data-stu-id="130ab-169">Click **:hov**.</span></span>  
1.  <span data-ttu-id="130ab-170">Vérifiez la pseudo-classe que vous souhaitez activer.</span><span class="sxs-lookup"><span data-stu-id="130ab-170">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="130ab-171">Dans la [figure 7](#figure-7), activez la `:hover` Pseudo-classe.</span><span class="sxs-lookup"><span data-stu-id="130ab-171">In [Figure 7](#figure-7), toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="130ab-172">Dans la fenêtre d’affichage, vérifiez que la `background-color: cornflowerblue` déclaration est appliquée à l’élément, même si celui-ci n’est pas en cours de pointage.</span><span class="sxs-lookup"><span data-stu-id="130ab-172">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

> ##### <span data-ttu-id="130ab-173">Figure 7</span><span class="sxs-lookup"><span data-stu-id="130ab-173">Figure 7</span></span>  
> <span data-ttu-id="130ab-174">Bascule de la `:hover` Pseudo-classe</span><span class="sxs-lookup"><span data-stu-id="130ab-174">Toggling the `:hover` pseudo-class</span></span>  
> ![Activation/désactivation de la pseudo-classe Hover][ImagePseudoClass]  

<span data-ttu-id="130ab-176">Pour un didacticiel interactif, voir [Ajouter un PseudoState à une classe][DevToolsCSSGetStartedAddPseudoState] .</span><span class="sxs-lookup"><span data-stu-id="130ab-176">See [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState] for an interactive tutorial.</span></span> 

### <span data-ttu-id="130ab-177">Afficher une page en mode d’impression</span><span class="sxs-lookup"><span data-stu-id="130ab-177">View a page in print mode</span></span>   

<span data-ttu-id="130ab-178">Pour afficher une page en mode impression:</span><span class="sxs-lookup"><span data-stu-id="130ab-178">To view a page in print mode:</span></span>  

1.  <span data-ttu-id="130ab-179">[Ouvrir le menu de commandes][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="130ab-179">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="130ab-180">Commencez à taper `Rendering` et sélectionnez `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="130ab-180">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="130ab-181">Dans la liste déroulante **émuler le média CSS** , sélectionnez **Imprimer**.</span><span class="sxs-lookup"><span data-stu-id="130ab-181">For the **Emulate CSS Media** dropdown, select **print**.</span></span>  

### <span data-ttu-id="130ab-182">Afficher les feuilles CSS utilisées et inutilisées avec l’onglet couverture</span><span class="sxs-lookup"><span data-stu-id="130ab-182">View used and unused CSS with the Coverage tab</span></span>   

<span data-ttu-id="130ab-183">L’onglet couverture vous indique la feuille de style en cascade qui est utilisée réellement par une page.</span><span class="sxs-lookup"><span data-stu-id="130ab-183">The Coverage tab shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="130ab-184">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) alors que devtools est sur le point d’ouvrir le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="130ab-184">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to open the Command Menu.</span></span>  
1.  <span data-ttu-id="130ab-185">Commencez à taper `coverage` et sélectionnez **afficher la couverture**.</span><span class="sxs-lookup"><span data-stu-id="130ab-185">Start typing `coverage` and select **Show Coverage**.</span></span>  <span data-ttu-id="130ab-186">L’onglet couverture apparaît.</span><span class="sxs-lookup"><span data-stu-id="130ab-186">The Coverage tab appears.</span></span>  
    
    > ##### <span data-ttu-id="130ab-187">Figure8</span><span class="sxs-lookup"><span data-stu-id="130ab-187">Figure 8</span></span>  
    > <span data-ttu-id="130ab-188">Ouverture de l’onglet couverture dans le menu de commandes</span><span class="sxs-lookup"><span data-stu-id="130ab-188">Opening the Coverage tab from the Command Menu</span></span>  
    > ![Ouverture de l’onglet couverture dans le menu de commandes][ImageCommandMenu]  
    
    > ##### <span data-ttu-id="130ab-190">Figure9</span><span class="sxs-lookup"><span data-stu-id="130ab-190">Figure 9</span></span>  
    > <span data-ttu-id="130ab-191">Onglet couverture</span><span class="sxs-lookup"><span data-stu-id="130ab-191">The Coverage tab</span></span>  
    > ![Onglet couverture][ImageCoverageEmpty]  
    
1.  <span data-ttu-id="130ab-193">Cliquez sur **Démarrer la couverture d’instrumentation et actualiser la page** de démarrage de l' ![ instrumentation et actualiser la page ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="130ab-193">Click **Start instrumenting coverage and refresh the page** ![Start instrumenting coverage and refresh the page][ImageRefreshIcon].</span></span>  <span data-ttu-id="130ab-194">La page actualise et l’onglet couverture fournit une vue d’ensemble de la quantité CSS \ (et JavaScript \) utilisée à partir de chaque fichier chargé par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="130ab-194">The page refreshes and the Coverage tab provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="130ab-195">Green représente les feuilles CSS utilisées.</span><span class="sxs-lookup"><span data-stu-id="130ab-195">Green represents used CSS.</span></span>  <span data-ttu-id="130ab-196">Rouge représente les feuilles CSS inutilisées.</span><span class="sxs-lookup"><span data-stu-id="130ab-196">Red represents unused CSS.</span></span>  
    
    > ##### <span data-ttu-id="130ab-197">Figure10</span><span class="sxs-lookup"><span data-stu-id="130ab-197">Figure 10</span></span>  
    > <span data-ttu-id="130ab-198">Vue d’ensemble de la quantité d’utilisation et de la feuille de style CSS (JavaScript)</span><span class="sxs-lookup"><span data-stu-id="130ab-198">An overview of how much CSS (and JavaScript) is used and unused</span></span>  
    > ![Vue d’ensemble de la quantité d’utilisation et de la feuille de style CSS (JavaScript)][ImageCoverageOverview]  

1.  <span data-ttu-id="130ab-200">Cliquez sur un fichier CSS pour afficher une répartition ligne par ligne de la feuille de style CSS qu’il utilise.</span><span class="sxs-lookup"><span data-stu-id="130ab-200">Click a CSS file to see a line-by-line breakdown of what CSS it uses.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="130ab-201">Dans la [figure 11](#figure-11), les lignes 145 à 147 et 149 à 151 `b66bc881.site-ltr.css` sont inutilisées, alors que les lignes 163 à 166 sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="130ab-201">In [Figure 11](#figure-11), lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    > ##### <span data-ttu-id="130ab-202">Figure11</span><span class="sxs-lookup"><span data-stu-id="130ab-202">Figure 11</span></span>  
    > <span data-ttu-id="130ab-203">Une répartition ligne par ligne de feuilles CSS utilisées et inutilisées</span><span class="sxs-lookup"><span data-stu-id="130ab-203">A line-by-line breakdown of used and unused CSS</span></span>  
    > ![Une répartition ligne par ligne de feuilles CSS utilisées et inutilisées][ImageCoverageDetail]  
    
### <span data-ttu-id="130ab-205">Forcer le mode aperçu avant impression</span><span class="sxs-lookup"><span data-stu-id="130ab-205">Force print preview mode</span></span>   

<span data-ttu-id="130ab-206">Pour plus d’DevTools, voir [mode aperçu avant impression][DevToolsCssPrintPreview].</span><span class="sxs-lookup"><span data-stu-id="130ab-206">See [Force DevTools Into Print Preview Mode][DevToolsCssPrintPreview].</span></span>  

## <span data-ttu-id="130ab-207">Modifier CSS</span><span class="sxs-lookup"><span data-stu-id="130ab-207">Change CSS</span></span>   

<!-- todo s/CSS declaration/declaration/ -->  

### <span data-ttu-id="130ab-208">Ajouter une déclaration CSS à un élément</span><span class="sxs-lookup"><span data-stu-id="130ab-208">Add a CSS declaration to an element</span></span>   

<span data-ttu-id="130ab-209">Dans la mesure où l’ordre des déclarations affecte la façon dont un élément est stylisé, vous pouvez ajouter des déclarations de différentes manières:</span><span class="sxs-lookup"><span data-stu-id="130ab-209">Since the order of declarations affects how an element is styled, you may add declarations in different ways:</span></span>  

*   <span data-ttu-id="130ab-210">[Ajoutez une déclaration inline](#add-an-inline-declaration).</span><span class="sxs-lookup"><span data-stu-id="130ab-210">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="130ab-211">Équivalent à l’ajout d’un `style` attribut au code HTML d’un élément.</span><span class="sxs-lookup"><span data-stu-id="130ab-211">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="130ab-212">[Ajoutez une déclaration à une règle de style](#add-a-declaration-to-a-style-rule).</span><span class="sxs-lookup"><span data-stu-id="130ab-212">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="130ab-213">Quel flux de travail devez-vous utiliser?</span><span class="sxs-lookup"><span data-stu-id="130ab-213">What workflow should you use?</span></span>** <span data-ttu-id="130ab-214">Pour la plupart des scénarios, vous souhaiterez probablement utiliser le flux de travail de déclaration inline.</span><span class="sxs-lookup"><span data-stu-id="130ab-214">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="130ab-215">Les déclarations Inline ont une spécificité supérieure à celle d’un élément externe, de sorte que le flux de travail intraligne vérifie que les modifications entrent en vigueur dans l’élément comme prévu.</span><span class="sxs-lookup"><span data-stu-id="130ab-215">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in the element as you would expect.</span></span>  <span data-ttu-id="130ab-216">Pour plus d’informations sur les [types de sélecteur][MDNSelectorTypes] , voir spécificité.</span><span class="sxs-lookup"><span data-stu-id="130ab-216">See [Selector Types][MDNSelectorTypes] for more on specificity.</span></span>  

<span data-ttu-id="130ab-217">Si vous déboguez des styles de l’élément et que vous devez spécifiquement tester ce qui se produit quand une déclaration est définie à des emplacements différents, utilisez l’autre flux de travail.</span><span class="sxs-lookup"><span data-stu-id="130ab-217">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <span data-ttu-id="130ab-218">Ajouter une déclaration en ligne</span><span class="sxs-lookup"><span data-stu-id="130ab-218">Add an inline declaration</span></span>   

<span data-ttu-id="130ab-219">Pour ajouter une déclaration en ligne:</span><span class="sxs-lookup"><span data-stu-id="130ab-219">To add an inline declaration:</span></span>  

1.  <span data-ttu-id="130ab-220">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="130ab-220">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="130ab-221">Dans le volet **styles** , cliquez entre les crochets de la section **élément. style** .</span><span class="sxs-lookup"><span data-stu-id="130ab-221">In the **Styles** pane, click between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="130ab-222">Le curseur s’attache pour vous permettre d’entrer du texte.</span><span class="sxs-lookup"><span data-stu-id="130ab-222">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="130ab-223">Entrez un nom de propriété et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="130ab-223">Enter a property name and press `Enter`.</span></span>  
1.  <span data-ttu-id="130ab-224">Entrez une valeur valide pour cette propriété et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="130ab-224">Enter a valid value for that property and press `Enter`.</span></span>  <span data-ttu-id="130ab-225">Dans l' **arborescence DOM**, vérifiez qu’un `style` attribut a été ajouté à l’élément.</span><span class="sxs-lookup"><span data-stu-id="130ab-225">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="130ab-226">Dans [figure 12](#figure-12), les `margin-top` `background-color` Propriétés et ont été appliquées à l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="130ab-226">In [Figure 12](#figure-12), the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="130ab-227">Dans l' **arborescence DOM** , assurez-vous que les déclarations sont reflétées dans l' `style` attribut d’un élément.</span><span class="sxs-lookup"><span data-stu-id="130ab-227">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

> ##### <span data-ttu-id="130ab-228">Figure12</span><span class="sxs-lookup"><span data-stu-id="130ab-228">Figure 12</span></span>  
> <span data-ttu-id="130ab-229">Ajout de déclarations Inline</span><span class="sxs-lookup"><span data-stu-id="130ab-229">Adding inline declarations</span></span>  
> ![Ajout de déclarations Inline][ImageInlineDeclarations]  

#### <span data-ttu-id="130ab-231">Ajouter une déclaration à une règle de style</span><span class="sxs-lookup"><span data-stu-id="130ab-231">Add a declaration to a style rule</span></span>   

<span data-ttu-id="130ab-232">Pour ajouter une déclaration à une règle de style existante:</span><span class="sxs-lookup"><span data-stu-id="130ab-232">To add a declaration to an existing style rule:</span></span>  

1.  <span data-ttu-id="130ab-233">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="130ab-233">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="130ab-234">Dans le volet **styles** , cliquez entre les crochets de la règle de style auxquelles vous souhaitez ajouter la déclaration.</span><span class="sxs-lookup"><span data-stu-id="130ab-234">In the **Styles** pane, click between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="130ab-235">Le curseur s’attache pour vous permettre d’entrer du texte.</span><span class="sxs-lookup"><span data-stu-id="130ab-235">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="130ab-236">Entrez un nom de propriété et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="130ab-236">Enter a property name and press `Enter`.</span></span>  
1.  <span data-ttu-id="130ab-237">Entrez une valeur valide pour cette propriété et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="130ab-237">Enter a valid value for that property and press `Enter`.</span></span>  

> ##### <span data-ttu-id="130ab-238">Figure13</span><span class="sxs-lookup"><span data-stu-id="130ab-238">Figure 13</span></span>  
> <span data-ttu-id="130ab-239">Ajout `border-bottom-style:groove` de la déclaration à une règle de style</span><span class="sxs-lookup"><span data-stu-id="130ab-239">Adding the `border-bottom-style:groove` declaration to a style rule</span></span>  
> ![Ajout d’une déclaration à une règle de style][ImageAddDeclarationExistingRule]  

### <span data-ttu-id="130ab-241">Modifier le nom ou la valeur d’une déclaration</span><span class="sxs-lookup"><span data-stu-id="130ab-241">Change a declaration name or value</span></span>   

<span data-ttu-id="130ab-242">Double-cliquez sur le nom ou la valeur d’une déclaration pour la modifier.</span><span class="sxs-lookup"><span data-stu-id="130ab-242">Double-click the name or value of a declaration to change it.</span></span>  <span data-ttu-id="130ab-243">Voir [modifier les valeurs de déclaration avec des raccourcis clavier](#change-declaration-values-with-keyboard-shortcuts) pour les raccourcis permettant d’incrémenter ou de décrémenter rapidement une valeur par `0.1` ,, ou par `1` `10` `100` unités.</span><span class="sxs-lookup"><span data-stu-id="130ab-243">See [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts) for shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units.</span></span>  

> ##### <span data-ttu-id="130ab-244">Figure14</span><span class="sxs-lookup"><span data-stu-id="130ab-244">Figure 14</span></span>  
> <span data-ttu-id="130ab-245">Modification de la valeur de l’argument</span><span class="sxs-lookup"><span data-stu-id="130ab-245">Changing the value of the</span></span> `border-bottom-style`  
> ![Modification de la valeur d’une déclaration][ImageAddDeclarationExistingRule2]  

### <span data-ttu-id="130ab-247">Modification des valeurs de déclaration avec les raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="130ab-247">Change declaration values with keyboard shortcuts</span></span>   

<span data-ttu-id="130ab-248">Lors de la modification de la valeur d’une déclaration, vous pouvez utiliser les raccourcis clavier suivants pour incrémenter la valeur à l’aide d’un montant fixe:</span><span class="sxs-lookup"><span data-stu-id="130ab-248">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a fixed amount:</span></span>  

*   <span data-ttu-id="130ab-249">Appuyez sur `Alt` + `Up` \ (Windows \) ou `Option` + `Up` \ (MacOS \) pour incrémenter par `0.1` .</span><span class="sxs-lookup"><span data-stu-id="130ab-249">Press `Alt`+`Up` \(Windows\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="130ab-250">Appuyez sur `Up` pour modifier la valeur par `1` , ou `0.1` si la valeur actuelle est comprise entre `-1` et `1` .</span><span class="sxs-lookup"><span data-stu-id="130ab-250">Press `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="130ab-251">Appuyez sur `Shift` + `Up` pour incrémenter par `10` .</span><span class="sxs-lookup"><span data-stu-id="130ab-251">Press `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="130ab-252">Appuyez sur `Shift` + `Page Up` \ (Windows \) ou `Shift` + `Command` + `Up` \ (MacOS \) pour incrémenter la valeur `100` .</span><span class="sxs-lookup"><span data-stu-id="130ab-252">Press `Shift`+`Page Up` \(Windows\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="130ab-253">La décrémentation fonctionne également.</span><span class="sxs-lookup"><span data-stu-id="130ab-253">Decrementing also works.</span></span>  <span data-ttu-id="130ab-254">Il vous suffit de remplacer chaque instance décrite `Up` plus haut par `Down` .</span><span class="sxs-lookup"><span data-stu-id="130ab-254">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <span data-ttu-id="130ab-255">Ajouter une classe à un élément</span><span class="sxs-lookup"><span data-stu-id="130ab-255">Add a class to an element</span></span>   

<span data-ttu-id="130ab-256">Pour ajouter une classe à un élément:</span><span class="sxs-lookup"><span data-stu-id="130ab-256">To add a class to an element:</span></span>  

1.  <span data-ttu-id="130ab-257">[Sélectionnez l’élément](#select-an-element) dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="130ab-257">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="130ab-258">Cliquez sur **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="130ab-258">Click **.cls**.</span></span>  
1.  <span data-ttu-id="130ab-259">Entrez le nom de la classe dans la zone de texte **Ajouter une nouvelle classe** .</span><span class="sxs-lookup"><span data-stu-id="130ab-259">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="130ab-260">Appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="130ab-260">Press `Enter`.</span></span>  

> ##### <span data-ttu-id="130ab-261">Figure15</span><span class="sxs-lookup"><span data-stu-id="130ab-261">Figure 15</span></span>  
> <span data-ttu-id="130ab-262">Volet **classes d’éléments**</span><span class="sxs-lookup"><span data-stu-id="130ab-262">The **Element Classes** pane</span></span>  
> ![Volet classes d’éléments][ImageElementClasses]  

### <span data-ttu-id="130ab-264">Basculer une classe</span><span class="sxs-lookup"><span data-stu-id="130ab-264">Toggle a class</span></span>   

<span data-ttu-id="130ab-265">Pour activer ou désactiver une classe sur un élément:</span><span class="sxs-lookup"><span data-stu-id="130ab-265">To enable or disable a class on an element:</span></span>  

1.  <span data-ttu-id="130ab-266">[Sélectionnez l’élément](#select-an-element) dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="130ab-266">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="130ab-267">Ouvrez le volet **classes d’éléments** .</span><span class="sxs-lookup"><span data-stu-id="130ab-267">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="130ab-268">Voir [Ajouter une classe à un élément](#add-a-class-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="130ab-268">See [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="130ab-269">Sous la zone de texte **Ajouter une nouvelle classe** figurent toutes les classes qui sont appliquées à cet élément.</span><span class="sxs-lookup"><span data-stu-id="130ab-269">Below the **Add New Class** text box are all of the classes that are being applied to this element.</span></span>  
1.  <span data-ttu-id="130ab-270">Activez/désactivez la case à cocher en regard de la classe que vous souhaitez activer ou désactiver.</span><span class="sxs-lookup"><span data-stu-id="130ab-270">Toggle the checkbox next to the class that you want to enable or disable.</span></span>  

### <span data-ttu-id="130ab-271">Ajouter une règle de style</span><span class="sxs-lookup"><span data-stu-id="130ab-271">Add a style rule</span></span>   

<span data-ttu-id="130ab-272">Pour ajouter une nouvelle règle de style:</span><span class="sxs-lookup"><span data-stu-id="130ab-272">To add a new style rule:</span></span>  

1.  <span data-ttu-id="130ab-273">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="130ab-273">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="130ab-274">Cliquez sur **nouvelle règle de style** ![ nouvelle règle de style ][ImageNewStyleRuleIcon] .</span><span class="sxs-lookup"><span data-stu-id="130ab-274">Click **New Style Rule** ![New Style Rule][ImageNewStyleRuleIcon].</span></span>  <span data-ttu-id="130ab-275">DevTools insère une nouvelle règle sous la règle **élément. style** .</span><span class="sxs-lookup"><span data-stu-id="130ab-275">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="130ab-276">Dans la [figure 16](#figure-16), devtools ajoute la `h1.devsite-page-title` règle de style après avoir cliqué sur **nouvelle règle de style**.</span><span class="sxs-lookup"><span data-stu-id="130ab-276">In [Figure 16](#figure-16), DevTools adds the `h1.devsite-page-title` style rule after clicking **New Style Rule**.</span></span>  

> ##### <span data-ttu-id="130ab-277">Figure16</span><span class="sxs-lookup"><span data-stu-id="130ab-277">Figure 16</span></span>  
> <span data-ttu-id="130ab-278">Ajout d’une nouvelle règle de style</span><span class="sxs-lookup"><span data-stu-id="130ab-278">Adding a new style rule</span></span>  
> ![Ajout d’une nouvelle règle de style][ImageStyleRule]  

#### <span data-ttu-id="130ab-280">Sélectionner la feuille de style à laquelle ajouter une règle</span><span class="sxs-lookup"><span data-stu-id="130ab-280">Choose which stylesheet to add a rule to</span></span>   

<span data-ttu-id="130ab-281">Lors de l' [Ajout d’une nouvelle règle de style](#add-a-style-rule), cliquez de **nouveau** sur la règle de style et maintenez-la enfoncée ![ ][ImageNewStyleRuleIcon] pour sélectionner la feuille de style à laquelle ajouter la règle de style.</span><span class="sxs-lookup"><span data-stu-id="130ab-281">When [adding a new style rule](#add-a-style-rule), click and hold **New Style Rule** ![New Style Rule][ImageNewStyleRuleIcon] to choose which stylesheet to add the style rule to.</span></span>  

> ##### <span data-ttu-id="130ab-282">Figure17</span><span class="sxs-lookup"><span data-stu-id="130ab-282">Figure 17</span></span>  
> <span data-ttu-id="130ab-283">Choix d’une feuille de style</span><span class="sxs-lookup"><span data-stu-id="130ab-283">Choosing a stylesheet</span></span>  
> ![Choix d’une feuille de style][ImageChooseStylesheet]  

#### <span data-ttu-id="130ab-285">Ajouter une règle de style à un emplacement spécifique</span><span class="sxs-lookup"><span data-stu-id="130ab-285">Add a style rule to a specific location</span></span>   

<span data-ttu-id="130ab-286">Pour ajouter une règle de style à un emplacement spécifique, accédez à l’onglet **styles** :</span><span class="sxs-lookup"><span data-stu-id="130ab-286">To add a style rule to a specific location in the **Styles** tab:</span></span>  

1.  <span data-ttu-id="130ab-287">Pointez sur la règle de style qui se trouve directement au-dessus de l’endroit où vous souhaitez ajouter votre nouvelle règle de style.</span><span class="sxs-lookup"><span data-stu-id="130ab-287">Hover over the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="130ab-288">[Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="130ab-288">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="130ab-289">Cliquez sur **Insérer une règle de style sous** ![ Insérer une règle de style ci-dessous ][ImageNewStyleRuleIcon] .</span><span class="sxs-lookup"><span data-stu-id="130ab-289">Click **Insert Style Rule Below** ![Insert Style Rule Below][ImageNewStyleRuleIcon].</span></span>  

> ##### <span data-ttu-id="130ab-290">Figure 18</span><span class="sxs-lookup"><span data-stu-id="130ab-290">Figure 18</span></span>  
> **<span data-ttu-id="130ab-291">Insérer une règle de style en dessous</span><span class="sxs-lookup"><span data-stu-id="130ab-291">Insert Style Rule Below</span></span>**  
> ![Insérer une règle de style en dessous][ImageInsertStyleRuleBelow]  

### <span data-ttu-id="130ab-293">Afficher la barre d’outils plus d’actions</span><span class="sxs-lookup"><span data-stu-id="130ab-293">Reveal the More Actions toolbar</span></span>   

<span data-ttu-id="130ab-294">La barre d’outils **plus d’actions** vous permet d’effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="130ab-294">The **More Actions** toolbar lets you:</span></span>  

*   <span data-ttu-id="130ab-295">Insérez une règle de style juste en dessous de celle qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="130ab-295">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="130ab-296">Ajoutez une `background-color` `color` `box-shadow` `text-shadow` déclaration à la règle de style sur laquelle vous êtes prioritaire.</span><span class="sxs-lookup"><span data-stu-id="130ab-296">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="130ab-297">Pour afficher la barre d’outils **plus d’actions** :</span><span class="sxs-lookup"><span data-stu-id="130ab-297">To reveal the **More Actions** toolbar:</span></span>  

1.  <span data-ttu-id="130ab-298">Dans l’onglet **styles** , pointez sur une règle de style.</span><span class="sxs-lookup"><span data-stu-id="130ab-298">In the **Styles** tab, hover over a style rule.</span></span>  <span data-ttu-id="130ab-299">**Plus d’actions** `...` est affiché dans le coin inférieur droit de la section règle de style.</span><span class="sxs-lookup"><span data-stu-id="130ab-299">**More Actions** `...` is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="130ab-300">Dans la [figure 19](#figure-19), placez le pointeur sur la `.header-holder.has-default-focus` règle de style et d' **autres actions** sont affichées dans le coin inférieur droit de la section règle de style.</span><span class="sxs-lookup"><span data-stu-id="130ab-300">In [Figure 19](#figure-19), hover over the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    > ##### <span data-ttu-id="130ab-301">Figure 19</span><span class="sxs-lookup"><span data-stu-id="130ab-301">Figure 19</span></span>  
    > <span data-ttu-id="130ab-302">Affichage **plus d’actions**</span><span class="sxs-lookup"><span data-stu-id="130ab-302">Revealing **More Actions**</span></span>  
    > ![Affichage plus d’actions][ImageRevealMore]  
    
1.  <span data-ttu-id="130ab-304">Placez le pointeur sur **plus d’actions** `...` pour afficher les actions mentionnées ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="130ab-304">Hover over **More Actions** `...` to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="130ab-305">L’action **Insérer une règle de style ci-dessous** apparaît après avoir pointé sur **plus d’actions**.</span><span class="sxs-lookup"><span data-stu-id="130ab-305">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    > ##### <span data-ttu-id="130ab-306">Figure 20</span><span class="sxs-lookup"><span data-stu-id="130ab-306">Figure 20</span></span>  
    > <span data-ttu-id="130ab-307">Barre d’outils **plus d’actions**</span><span class="sxs-lookup"><span data-stu-id="130ab-307">The **More Actions** toolbar</span></span>  
    > ![Barre d’outils plus d’actions][ImageInsertStyleRuleBelow2]  
    
### <span data-ttu-id="130ab-309">Basculer une déclaration</span><span class="sxs-lookup"><span data-stu-id="130ab-309">Toggle a declaration</span></span>   

<span data-ttu-id="130ab-310">Pour activer ou désactiver une déclaration unique:</span><span class="sxs-lookup"><span data-stu-id="130ab-310">To toggle a single declaration on or off:</span></span>  

1.  <span data-ttu-id="130ab-311">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="130ab-311">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="130ab-312">Dans le volet **styles** , pointez sur la règle qui définit la déclaration.</span><span class="sxs-lookup"><span data-stu-id="130ab-312">In the **Styles** pane, hover over the rule that defines the declaration.</span></span>  <span data-ttu-id="130ab-313">Les cases à cocher s’affichent en regard de chaque déclaration.</span><span class="sxs-lookup"><span data-stu-id="130ab-313">Checkboxes appear next to each declaration.</span></span>  
1.  <span data-ttu-id="130ab-314">Activez ou désactivez la case à cocher en regard de la déclaration.</span><span class="sxs-lookup"><span data-stu-id="130ab-314">Check or uncheck the checkbox next to the declaration.</span></span>  <span data-ttu-id="130ab-315">Lorsque vous décochez une déclaration, DevTools la traverse pour indiquer qu’elle n’est plus active.</span><span class="sxs-lookup"><span data-stu-id="130ab-315">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="130ab-316">Dans la [figure 21](#figure-21), la `margin-top` propriété de l’élément actuellement sélectionné a été activée.</span><span class="sxs-lookup"><span data-stu-id="130ab-316">In [Figure 21](#figure-21), the `margin-top` property for the currently selected element has been toggled off.</span></span>  

> ##### <span data-ttu-id="130ab-317">Figure 21</span><span class="sxs-lookup"><span data-stu-id="130ab-317">Figure 21</span></span>  
> <span data-ttu-id="130ab-318">Basculer une déclaration</span><span class="sxs-lookup"><span data-stu-id="130ab-318">Toggling a declaration</span></span>  
> ![Basculer une déclaration][ImageToggleDeclaration]  

### <span data-ttu-id="130ab-320">Ajouter une déclaration couleur d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="130ab-320">Add a background-color declaration</span></span>   

<span data-ttu-id="130ab-321">Pour ajouter une `background-color` déclaration à un élément:</span><span class="sxs-lookup"><span data-stu-id="130ab-321">To add a `background-color` declaration to an element:</span></span>  

1.  <span data-ttu-id="130ab-322">Pointez sur la règle de style à laquelle vous souhaitez ajouter la `background-color` déclaration.</span><span class="sxs-lookup"><span data-stu-id="130ab-322">Hover over the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="130ab-323">[Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="130ab-323">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="130ab-324">Cliquez sur **Ajouter une couleur d’arrière-** ![ plan ajouter une couleur d’arrière-plan ][ImageAddBackgroundColorIcon] .</span><span class="sxs-lookup"><span data-stu-id="130ab-324">Click **Add Background Color** ![Add Background Color][ImageAddBackgroundColorIcon].</span></span>  

> ##### <span data-ttu-id="130ab-325">Figure 22</span><span class="sxs-lookup"><span data-stu-id="130ab-325">Figure 22</span></span>  
> **<span data-ttu-id="130ab-326">Ajouter une couleur d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="130ab-326">Add Background Color</span></span>**  
> ![Ajouter une couleur d’arrière-plan][ImageAddBackgroundColor]  

### <span data-ttu-id="130ab-328">Ajouter une déclaration de couleur</span><span class="sxs-lookup"><span data-stu-id="130ab-328">Add a color declaration</span></span>   

<span data-ttu-id="130ab-329">Pour ajouter une `color` déclaration à un élément:</span><span class="sxs-lookup"><span data-stu-id="130ab-329">To add a `color` declaration to an element:</span></span>  

1.  <span data-ttu-id="130ab-330">Pointez sur la règle de style à laquelle vous souhaitez ajouter la `color` déclaration.</span><span class="sxs-lookup"><span data-stu-id="130ab-330">Hover over the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="130ab-331">[Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="130ab-331">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="130ab-332">Cliquez sur **Ajouter** une couleur ajouter une couleur ![ ][ImageAddColorIcon] .</span><span class="sxs-lookup"><span data-stu-id="130ab-332">Click **Add Color** ![Add Color][ImageAddColorIcon].</span></span>  

> ##### <span data-ttu-id="130ab-333">Figure 23</span><span class="sxs-lookup"><span data-stu-id="130ab-333">Figure 23</span></span>  
> **<span data-ttu-id="130ab-334">Ajouter de la couleur</span><span class="sxs-lookup"><span data-stu-id="130ab-334">Add Color</span></span>**  
> ![Ajouter de la couleur][ImageAddColor]  

### <span data-ttu-id="130ab-336">Ajouter une déclaration d’ombre Box</span><span class="sxs-lookup"><span data-stu-id="130ab-336">Add a box-shadow declaration</span></span>   

<span data-ttu-id="130ab-337">Pour ajouter une `box-shadow` déclaration à un élément:</span><span class="sxs-lookup"><span data-stu-id="130ab-337">To add a `box-shadow` declaration to an element:</span></span>  

1.  <span data-ttu-id="130ab-338">Pointez sur la règle de style à laquelle vous souhaitez ajouter la `box-shadow` déclaration.</span><span class="sxs-lookup"><span data-stu-id="130ab-338">Hover over the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="130ab-339">[Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="130ab-339">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="130ab-340">Cliquez sur **Ajouter** une ombre de zone Ajouter une ombre ![ ][ImageAddBoxShadowIcon] .</span><span class="sxs-lookup"><span data-stu-id="130ab-340">Click **Add Box Shadow** ![Add Box Shadow][ImageAddBoxShadowIcon].</span></span>  

> ##### <span data-ttu-id="130ab-341">Figure 24</span><span class="sxs-lookup"><span data-stu-id="130ab-341">Figure 24</span></span>  
> **<span data-ttu-id="130ab-342">Ajouter une ombre de zone</span><span class="sxs-lookup"><span data-stu-id="130ab-342">Add Box Shadow</span></span>**  
> ![Ajouter une ombre de zone][ImageAddBoxShadow]  

### <span data-ttu-id="130ab-344">Ajouter une déclaration d’ombre textuelle</span><span class="sxs-lookup"><span data-stu-id="130ab-344">Add a text-shadow declaration</span></span>   

<span data-ttu-id="130ab-345">Pour ajouter une `text-shadow` déclaration à un élément:</span><span class="sxs-lookup"><span data-stu-id="130ab-345">To add a `text-shadow` declaration to an element:</span></span>  

1.  <span data-ttu-id="130ab-346">Pointez sur la règle de style à laquelle vous souhaitez ajouter la `text-shadow` déclaration.</span><span class="sxs-lookup"><span data-stu-id="130ab-346">Hover over the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="130ab-347">[Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="130ab-347">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="130ab-348">Cliquez sur **Ajouter une ombre du texte** ![ Ajouter une ombre ][ImageAddTextShadowIcon] .</span><span class="sxs-lookup"><span data-stu-id="130ab-348">Click **Add Text Shadow** ![Add Text Shadow][ImageAddTextShadowIcon].</span></span>  

> ##### <span data-ttu-id="130ab-349">Figure 25</span><span class="sxs-lookup"><span data-stu-id="130ab-349">Figure 25</span></span>  
> **<span data-ttu-id="130ab-350">Ajouter une ombre de texte</span><span class="sxs-lookup"><span data-stu-id="130ab-350">Add Text Shadow</span></span>**  
> ![Ajouter une ombre de texte][ImageAddTextShadow]  

### <span data-ttu-id="130ab-352">Changer les couleurs à l’aide du sélecteur de couleurs</span><span class="sxs-lookup"><span data-stu-id="130ab-352">Change colors with the Color Picker</span></span>   

<span data-ttu-id="130ab-353">Le **Sélecteur de couleurs** fournit une interface utilisateur pour le changement `color` et la `background-color` déclaration.</span><span class="sxs-lookup"><span data-stu-id="130ab-353">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="130ab-354">Pour ouvrir le **Sélecteur de couleurs**:</span><span class="sxs-lookup"><span data-stu-id="130ab-354">To open the **Color Picker**:</span></span>  

1.  <span data-ttu-id="130ab-355">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="130ab-355">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="130ab-356">Dans l’onglet **styles** , recherchez la `color` `background-color` déclaration, ou similaire, que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="130ab-356">In the **Styles** tab, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="130ab-357">À gauche de la `color` valeur, `background-color` ou similaire, il existe un petit carré, qui est un aperçu de la couleur.</span><span class="sxs-lookup"><span data-stu-id="130ab-357">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="130ab-358">Dans la [figure 26](#figure-26), le petit carré à gauche de `rgba(0, 0, 0, 0.7)` est un aperçu de cette couleur.</span><span class="sxs-lookup"><span data-stu-id="130ab-358">In [Figure 26](#figure-26), the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    > ##### <span data-ttu-id="130ab-359">Figure 26</span><span class="sxs-lookup"><span data-stu-id="130ab-359">Figure 26</span></span>  
    > <span data-ttu-id="130ab-360">Aperçu de couleur</span><span class="sxs-lookup"><span data-stu-id="130ab-360">Color preview</span></span>  
    > ![Aperçu de couleur][ImageColorPreview]  
    
1.  <span data-ttu-id="130ab-362">Cliquez sur l’Aperçu pour ouvrir le **Sélecteur de couleurs**.</span><span class="sxs-lookup"><span data-stu-id="130ab-362">Click the preview to open the **Color Picker**.</span></span>  
    
    > ##### <span data-ttu-id="130ab-363">Figure 27</span><span class="sxs-lookup"><span data-stu-id="130ab-363">Figure 27</span></span>  
    > <span data-ttu-id="130ab-364">**Sélecteur de couleurs**</span><span class="sxs-lookup"><span data-stu-id="130ab-364">The **Color Picker**</span></span>  
    > ![Sélecteur de couleurs][ImageColorPicker]  
    
<span data-ttu-id="130ab-366">Voici une description de chaque élément d’interface utilisateur du sélecteur de **couleurs**:</span><span class="sxs-lookup"><span data-stu-id="130ab-366">Here is a description of each of the UI elements of the **Color Picker**:</span></span>  

> ##### <span data-ttu-id="130ab-367">Figure 28</span><span class="sxs-lookup"><span data-stu-id="130ab-367">Figure 28</span></span>  
> <span data-ttu-id="130ab-368">Sélecteur de couleurs, annoté</span><span class="sxs-lookup"><span data-stu-id="130ab-368">The Color Picker, annotated</span></span>  
> ![Sélecteur de couleurs, annoté][ImageColorPickerAnnotated]  

1.  <span data-ttu-id="130ab-370">**Nuances de gris**.</span><span class="sxs-lookup"><span data-stu-id="130ab-370">**Shades**.</span></span>  
1.  <span data-ttu-id="130ab-371">**Pipette**.</span><span class="sxs-lookup"><span data-stu-id="130ab-371">**Eyedropper**.</span></span>  <span data-ttu-id="130ab-372">Pour en savoir plus, voir [exemple de couleur de la page avec le](#sample-a-color-off-the-page-with-the-eyedropper)compte-gouttes.</span><span class="sxs-lookup"><span data-stu-id="130ab-372">See [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
1.  <span data-ttu-id="130ab-373">**Copier dans le presse-papiers**.</span><span class="sxs-lookup"><span data-stu-id="130ab-373">**Copy To Clipboard**.</span></span>  <span data-ttu-id="130ab-374">Copiez la **valeur d’affichage** dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="130ab-374">Copy the **Display Value** to your clipboard.</span></span>  
1.  <span data-ttu-id="130ab-375">**Valeur d’affichage**.</span><span class="sxs-lookup"><span data-stu-id="130ab-375">**Display Value**.</span></span>  <span data-ttu-id="130ab-376">La représentation RVBA, HSLA ou Hex de la couleur.</span><span class="sxs-lookup"><span data-stu-id="130ab-376">The RGBA, HSLA, or Hex representation of the color.</span></span>  
1.  <span data-ttu-id="130ab-377">**Palette de couleurs**.</span><span class="sxs-lookup"><span data-stu-id="130ab-377">**Color Palette**.</span></span>  <span data-ttu-id="130ab-378">Cliquez sur l’un de ces carrés pour modifier la couleur de ce carré.</span><span class="sxs-lookup"><span data-stu-id="130ab-378">Click one of these squares to change the color to that square.</span></span>  
1.  <span data-ttu-id="130ab-379">**Nuance**.</span><span class="sxs-lookup"><span data-stu-id="130ab-379">**Hue**.</span></span>  
1.  <span data-ttu-id="130ab-380">**Opacity**.</span><span class="sxs-lookup"><span data-stu-id="130ab-380">**Opacity**.</span></span>  
1.  <span data-ttu-id="130ab-381">**Sélecteur de valeurs d’affichage**.</span><span class="sxs-lookup"><span data-stu-id="130ab-381">**Display Value Switcher**.</span></span>  <span data-ttu-id="130ab-382">Basculer entre les représentations RVBA, HSLA et Hex de la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="130ab-382">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
1.  <span data-ttu-id="130ab-383">**Sélecteur de palette de couleurs**.</span><span class="sxs-lookup"><span data-stu-id="130ab-383">**Color Palette Switcher**.</span></span>  <span data-ttu-id="130ab-384">Basculer entre la [palette de création matérielle][MaterialDesignColorSystem], une palette personnalisée ou une palette de couleurs de page.</span><span class="sxs-lookup"><span data-stu-id="130ab-384">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="130ab-385">DevTools génère la palette de couleurs de page en fonction des couleurs qu’il trouve dans vos feuilles de style.</span><span class="sxs-lookup"><span data-stu-id="130ab-385">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  

#### <span data-ttu-id="130ab-386">Exemple de couleur de la page avec le compte-gouttes</span><span class="sxs-lookup"><span data-stu-id="130ab-386">Sample a color off the page with the Eyedropper</span></span>   

<span data-ttu-id="130ab-387">Lorsque vous ouvrez le **Sélecteur de couleurs**, la pipette de la **pipette** ![ ][ImageEyedropperIcon] est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="130ab-387">When you open the **Color Picker**, the **Eyedropper** ![Eyedropper][ImageEyedropperIcon] is on by default.</span></span>  <span data-ttu-id="130ab-388">Pour changer la couleur sélectionnée en fonction de la couleur de la page, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="130ab-388">To change the selected color to some other color on the page:</span></span>  

1.  <span data-ttu-id="130ab-389">Placez le pointeur de la souris sur la couleur cible dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="130ab-389">Hover over the target color in the viewport.</span></span>  
1.  <span data-ttu-id="130ab-390">Cliquez sur pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="130ab-390">Click to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="130ab-391">Dans la [figure 29](#figure-29), le **Sélecteur de couleurs** affiche une valeur de couleur actuelle de `rgba(0,0,0,0.7)` , qui est proche de noir.</span><span class="sxs-lookup"><span data-stu-id="130ab-391">In [Figure 29](#figure-29), the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="130ab-392">Lorsque vous cliquez sur le noir lorsque vous cliquez sur la fenêtre d’affichage, cette couleur doit changer.</span><span class="sxs-lookup"><span data-stu-id="130ab-392">This color should change to the black that is currently highlighted in the viewport once the black was clicked.</span></span>  
    
    > ##### <span data-ttu-id="130ab-393">Figure 29</span><span class="sxs-lookup"><span data-stu-id="130ab-393">Figure 29</span></span>  
    > <span data-ttu-id="130ab-394">Utiliser le compte-gouttes</span><span class="sxs-lookup"><span data-stu-id="130ab-394">Using the Eyedropper</span></span>  
    > ![Utiliser le compte-gouttes][ImageUsingEyedropper]  
    
 



<!-- image links -->  

[ImageAddBackgroundColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: /microsoft-edge/devtools-guide-chromium/media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-an-element-icon.msft.png  

[ImageSelectedElement]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1.msft.png "Figure 1: exemple d’un élément sélectionné"  
[ImageViewRuleStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-highlight.msft.png "Figure 2: affichage de la feuille de calcul à l’endroit où une règle est définie"  
[ImageComputedTab]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-h1.msft.png "Figure 3: onglet calculé"  
[ImageBoxModel]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-2.msft.png "Figure 4: diagramme de modèle de cadre"  
[ImageStylesFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-color.msft.png "Figure 5: filtrer l’onglet styles"  
[ImageComputerFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-filter-100.msft.png "Figure 6: filtrage de l’onglet calculé"  
[ImagePseudoClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-hov-hover.msft.png "Figure 7: activation/désactivation de la pseudo-classe Hover"  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-coverage.msft.png "Figure 8: ouverture de l’onglet couverture dans le menu de commandes"  
[ImageCoverageEmpty]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-empty.msft.png "Figure 9: onglet couverture"  
[ImageCoverageOverview]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-run.msft.png "Figure 10: vue d’ensemble de la quantité d’utilisation et de la feuille de style CSS (JavaScript)"  
[ImageCoverageDetail]: /microsoft-edge/devtools-guide-chromium/media/css-sources-css-coverage.msft.png "Figure 11: une répartition ligne par ligne de feuilles CSS utilisées et inutilisées"  
[ImageInlineDeclarations]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-margin-top-background-color.msft.png "Figure 12: ajout de déclarations Inline"  
[ImageAddDeclarationExistingRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style.msft.png "Figure 13: ajout d’une déclaration à une règle de style"  
[ImageAddDeclarationExistingRule2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style-dropdown.msft.png "Figure 14: modification de la valeur d’une déclaration"  
[ImageElementClasses]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-classes.msft.png "Figure 15: volet classes d’éléments"  
[ImageStyleRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new.msft.png "Figure 16: ajout d’une nouvelle règle de style"  
[ImageChooseStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new-select-exisiting.msft.png "Figure 17: choix d’une feuille de style"  
[ImageInsertStyleRuleBelow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-insert-style-rule-below.msft.png "Figure 18: insérer une règle de style en dessous"  
[ImageRevealMore]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-new-rule-styles.msft.png "Figure 19: révéler plus d’actions"  
[ImageInsertStyleRuleBelow2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png "Figure 20: barre d’outils plus d’actions"  
[ImageToggleDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-deactivated.msft.png "Figure 21: basculer une déclaration"  
[ImageAddBackgroundColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-background-color.msft.png "Figure 22: ajouter une couleur d’arrière-plan"  
[ImageAddColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-color.msft.png "Figure 23: ajouter une couleur"  
[ImageAddBoxShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-box-shadow.msft.png "Figure 24: ombre de la zone Ajouter"  
[ImageAddTextShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-text-shadow.msft.png "Figure 25: ajouter une ombre de texte"  
[ImageColorPreview]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-overlay-color-box.msft.png "Figure 26: aperçu des couleurs"  
[ImageColorPicker]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker.msft.png "Figure 27: sélecteur de couleurs"  
[ImageColorPickerAnnotated]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker-annotated.msft.png "Figure 28: sélecteur de couleurs, annoté"  
[ImageUsingEyedropper]: /microsoft-edge/devtools-guide-chromium/media/css-color-picker-eye-dropper.msft.png "Figure 29: utilisation du compte-gouttes"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  
[DevToolsCSSGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Découvrir comment afficher et modifier des feuilles CSS"  
[DevToolsCSSGetStartedAddPseudoState]: /microsoft-edge/devtools-guide-chromium/css/index#add-a-pseudostate-to-a-class "Ajouter un PseudoState à une classe: Familiarisez-vous avec l’affichage et la modification de feuilles CSS"  
[DevToolsCSSGetStartedTutorial]: /microsoft-edge/devtools-guide-chromium/css/index#view-the-css-for-an-element "Affichage de la feuille de style en cascade (CSS) d’un élément: commencez à afficher et modifier des feuilles CSS"  
[DevToolsCssPrintPreview]: /microsoft-edge/devtools-guide-chromium/css/print-preview "Force Microsoft Edge DevTools en mode d’aperçu avant impression (CSS Print Media Type)"  
[DevToolsJavascriptReferenceFormat]: /microsoft-edge/devtools-guide-chromium/javascript/reference#make-a-minified-file-readable "Créer une référence de débogage de fichier minified-JavaScript lisible"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "Conception système couleur-matériau"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "Le modèle de zone | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Types de sélecteur-spécificité | MDN"  

> [!NOTE]
> <span data-ttu-id="130ab-434">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="130ab-434">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="130ab-435">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="130ab-435">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="130ab-437">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="130ab-437">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
