---
title: Référence CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 908e32140d9deb89489089442055e188cd2d9378
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931348"
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

# <span data-ttu-id="e8866-103">Référence CSS</span><span class="sxs-lookup"><span data-stu-id="e8866-103">CSS reference</span></span>  

<span data-ttu-id="e8866-104">Découvrez les nouveaux flux de travail dans les informations de référence détaillées suivantes sur les fonctionnalités de Microsoft Edge DevTools liées à l’affichage et la modification de feuilles CSS.</span><span class="sxs-lookup"><span data-stu-id="e8866-104">Discover new workflows in the following comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="e8866-105">Pour en savoir plus sur les concepts de base, voir prendre en [main l’affichage et la modification de feuilles CSS][DevToolsCSSGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="e8866-105">See [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted] to learn the basics.</span></span>  

## <span data-ttu-id="e8866-106">Sélectionner un élément</span><span class="sxs-lookup"><span data-stu-id="e8866-106">Select an element</span></span>  

<span data-ttu-id="e8866-107">Le panneau **éléments** de devtools vous permet d’afficher ou de modifier la feuille de style CSS d’un élément à la fois.</span><span class="sxs-lookup"><span data-stu-id="e8866-107">The **Elements** panel of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="e8866-108">L’élément sélectionné est mis en surbrillance dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="e8866-108">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="e8866-109">Les styles de l’élément apparaissent dans le volet **styles** .</span><span class="sxs-lookup"><span data-stu-id="e8866-109">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="e8866-110">Voir [afficher la feuille de style en cascade (CSS) d’un élément][DevToolsCSSGetStartedTutorial] pour un didacticiel.</span><span class="sxs-lookup"><span data-stu-id="e8866-110">See [View the CSS for an element][DevToolsCSSGetStartedTutorial] for a tutorial.</span></span>  

> [!NOTE]
> <span data-ttu-id="e8866-111">Dans l’illustration suivante, l' `h1` élément qui est surligné dans l' **arborescence DOM** est l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e8866-111">In the following figure, the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="e8866-112">À droite, les styles de l’élément apparaissent dans le volet **styles** .</span><span class="sxs-lookup"><span data-stu-id="e8866-112">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="e8866-113">Sur la gauche, l’élément est mis en surbrillance dans la fenêtre d’affichage, mais uniquement dans la mesure où la souris pointe actuellement sur celle-ci dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="e8866-113">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Exemple d’élément sélectionné" lightbox="../media/css-elements-styles-h1.msft.png":::
   <span data-ttu-id="e8866-115">Exemple d’élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="e8866-115">An example of a selected element</span></span>  
:::image-end:::  

<span data-ttu-id="e8866-116">Utilisez l’une des actions suivantes pour sélectionner un élément.</span><span class="sxs-lookup"><span data-stu-id="e8866-116">Use one the following actions to select an element.</span></span>  

*   <span data-ttu-id="e8866-117">Dans votre fenêtre d’affichage, pointez sur l’élément, ouvrez le menu contextuel (cliquez avec le bouton droit sur \), puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="e8866-117">In your viewport, hover on the element, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
*   <span data-ttu-id="e8866-118">Dans devtools, choisissez **Sélectionner un élément** \ ( ![ Sélectionnez un élément ][ImageSelectAnElementIcon] \) ou `Control` + `Shift` + `C` \ (Windows \) ou `Command` + `Shift` + `C` \ (MacOS \), puis sélectionnez l’élément dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e8866-118">In DevTools, choose **Select an element** \(![Select an element][ImageSelectAnElementIcon]\) or select `Control`+`Shift`+`C` \(Windows\) or `Command`+`Shift`+`C` \(macOS\), and then choose the element in the viewport.</span></span>  
*   <span data-ttu-id="e8866-119">Dans DevTools, sélectionnez l’élément dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="e8866-119">In DevTools, choose the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="e8866-120">Dans DevTools, exécutez une requête telle que `document.querySelector('p')` dans la **console**, pointez sur le résultat, ouvrez le menu contextuel, puis cliquez sur **afficher dans le panneau éléments**.</span><span class="sxs-lookup"><span data-stu-id="e8866-120">In DevTools, run a query like `document.querySelector('p')` in the **Console**, hover on the result, open the contextual menu \(right-click\), and select **Reveal in Elements panel**.</span></span>  

## <span data-ttu-id="e8866-121">Afficher les feuilles CSS</span><span class="sxs-lookup"><span data-stu-id="e8866-121">View CSS</span></span>  

### <span data-ttu-id="e8866-122">Affichage de la feuille de style externe dans laquelle une règle est définie</span><span class="sxs-lookup"><span data-stu-id="e8866-122">View the external stylesheet where a rule is defined</span></span>  

<span data-ttu-id="e8866-123">Dans le volet **styles** , cliquez sur le lien en regard d’une règle CSS pour ouvrir la feuille de style externe qui définit la règle.</span><span class="sxs-lookup"><span data-stu-id="e8866-123">In the **Styles** pane, choose the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  

<span data-ttu-id="e8866-124">Si la feuille de style est minified, voir [rendre un fichier minified lisible][DevToolsJavascriptReferenceFormat].</span><span class="sxs-lookup"><span data-stu-id="e8866-124">If the stylesheet is minified, see [Make a minified file readable][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="e8866-125">Dans l’illustration suivante, une fois que vous avez choisi, `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` vous êtes redirigé vers la ligne 2 de `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , où la `.content h1:first-of-type` règle CSS est définie.</span><span class="sxs-lookup"><span data-stu-id="e8866-125">In the following figure, after you choose `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` you are taken to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Affichage de la feuille de style dans laquelle une règle est définie" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  <span data-ttu-id="e8866-127">Affichage de la feuille de style dans laquelle une règle est définie</span><span class="sxs-lookup"><span data-stu-id="e8866-127">Viewing the stylesheet where a rule is defined</span></span>  
:::image-end:::  

### <span data-ttu-id="e8866-128">Afficher uniquement les feuilles CSS appliquées actuellement à un élément</span><span class="sxs-lookup"><span data-stu-id="e8866-128">View only the CSS that is actually applied to an element</span></span>  

<span data-ttu-id="e8866-129">L’onglet **styles** affiche toutes les règles qui s’appliquent à un élément, y compris les déclarations qui ont été remplacées.</span><span class="sxs-lookup"><span data-stu-id="e8866-129">The **Styles** tab shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="e8866-130">Lorsque vous n’êtes pas intéressé par des déclarations substituées, utilisez l’onglet **calculé** pour afficher uniquement les feuilles CSS qui sont réellement appliquées à un élément.</span><span class="sxs-lookup"><span data-stu-id="e8866-130">When you are not interested in overridden declarations, use the **Computed** tab to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="e8866-131">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="e8866-131">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="e8866-132">Accédez à l’onglet **calculé** dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="e8866-132">Go to the **Computed** tab in the **Elements** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="e8866-133">Dans le cas d’une fenêtre DevTools large, l’onglet **calculé** n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="e8866-133">On a wide DevTools window, the **Computed** tab does not exist.</span></span>  <span data-ttu-id="e8866-134">Le contenu de l’onglet **calculé** est affiché dans l’onglet **styles** .</span><span class="sxs-lookup"><span data-stu-id="e8866-134">The contents of the **Computed** tab are shown on the **Styles** tab.</span></span>  

<span data-ttu-id="e8866-135">Les propriétés héritées sont opaques.</span><span class="sxs-lookup"><span data-stu-id="e8866-135">Inherited properties are opaque.</span></span>  <span data-ttu-id="e8866-136">Cochez la case **Afficher tout** pour afficher toutes les valeurs héritées.</span><span class="sxs-lookup"><span data-stu-id="e8866-136">Check the **Show All** checkbox to see all inherited values.</span></span>  

> [!NOTE]
> <span data-ttu-id="e8866-137">Dans l’illustration suivante, l’onglet **calculé** montre les propriétés CSS qui sont appliquées à l’élément actuellement sélectionné `h1` .</span><span class="sxs-lookup"><span data-stu-id="e8866-137">In the following figure, the **Computed** tab shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="Onglet calculé" lightbox="../media/css-elements-computed-h1.msft.png":::
   <span data-ttu-id="e8866-139">Onglet **calculé**</span><span class="sxs-lookup"><span data-stu-id="e8866-139">The **Computed** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="e8866-140">Afficher les propriétés CSS par ordre alphabétique</span><span class="sxs-lookup"><span data-stu-id="e8866-140">View CSS properties in alphabetical order</span></span>  

<span data-ttu-id="e8866-141">Utilisez l’onglet **calculé** .  Voir [afficher uniquement la feuille de style CSS qui est réellement appliquée à un élément](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="e8866-141">Use the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="e8866-142">Afficher les propriétés CSS héritées</span><span class="sxs-lookup"><span data-stu-id="e8866-142">View inherited CSS properties</span></span>  

<span data-ttu-id="e8866-143">Cochez la case **Afficher tout** dans l’onglet **calculé** .  Voir [afficher uniquement la feuille de style CSS qui est réellement appliquée à un élément](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="e8866-143">Check the **Show All** checkbox in the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="e8866-144">Afficher le modèle de boîte pour un élément</span><span class="sxs-lookup"><span data-stu-id="e8866-144">View the box model for an element</span></span>  

<span data-ttu-id="e8866-145">Pour afficher [le modèle de zone][MDNBoxModel] d’un élément, accédez à l’onglet **styles** .  Si votre fenêtre DevTools est étroite, le diagramme de **modèle de cadre** est en bas de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="e8866-145">To view [the box model][MDNBoxModel] of an element, go to the **Styles** tab.  If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the tab.</span></span>  

<span data-ttu-id="e8866-146">Pour modifier une valeur, sélectionnez et modifiez sur une valeur.</span><span class="sxs-lookup"><span data-stu-id="e8866-146">Choose and edit on a value to change a value.</span></span>  

> [!NOTE]
> <span data-ttu-id="e8866-147">Dans l’illustration suivante, le diagramme de **modèle de cadre** sous l’onglet **styles** affiche le modèle de zone de l’élément actuellement sélectionné `h1` .</span><span class="sxs-lookup"><span data-stu-id="e8866-147">In the following figure, the **Box Model** diagram in the **Styles** tab shows the box model for the currently selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="Diagramme de modèle de cadre" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   <span data-ttu-id="e8866-149">Diagramme de **modèle de cadre**</span><span class="sxs-lookup"><span data-stu-id="e8866-149">The **Box Model** diagram</span></span>  
:::image-end:::  

### <span data-ttu-id="e8866-150">Rechercher et filtrer la CSS d’un élément</span><span class="sxs-lookup"><span data-stu-id="e8866-150">Search and filter the CSS of an element</span></span>  

<span data-ttu-id="e8866-151">Utilisez la zone de texte **filtre** des **styles** et des onglets **calculés** pour rechercher des propriétés ou des valeurs CSS spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e8866-151">Use the **Filter** text box on the **Styles** and **Computed** tabs to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="e8866-152">Pour effectuer une recherche dans les propriétés héritées dans l’onglet **calculé** , activez la case à cocher **Afficher tout** .</span><span class="sxs-lookup"><span data-stu-id="e8866-152">To also search inherited properties in the **Computed** tab, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="e8866-153">Dans l’illustration suivante, l’onglet **styles** est filtré pour afficher uniquement les règles qui incluent la requête de recherche `color` .</span><span class="sxs-lookup"><span data-stu-id="e8866-153">In the following figure, the **Styles** tab is filtered to only show rules that include the search query `color`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Filtrer l’onglet styles" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   <span data-ttu-id="e8866-155">Filtrer l’onglet **styles**</span><span class="sxs-lookup"><span data-stu-id="e8866-155">Filter the **Styles** tab</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="e8866-156">Dans l’illustration suivante, l’onglet **calculé** est filtré pour afficher uniquement les déclarations qui incluent la requête de recherche `100%` .</span><span class="sxs-lookup"><span data-stu-id="e8866-156">In the following figure, the **Computed** tab is filtered to only show declarations that include the search query `100%`.</span></span>  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Filtrer l’onglet calculé" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   <span data-ttu-id="e8866-158">Filtrer l’onglet **calculé**</span><span class="sxs-lookup"><span data-stu-id="e8866-158">Filter the **Computed** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="e8866-159">Basculer une pseudo-classe</span><span class="sxs-lookup"><span data-stu-id="e8866-159">Toggle a pseudo-class</span></span>  

<span data-ttu-id="e8866-160">Effectuez les opérations suivantes pour basculer une pseudo-classe comme `:active` , `:focus` , `:hover` ou `:visited` .</span><span class="sxs-lookup"><span data-stu-id="e8866-160">Complete the following actions to toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`.</span></span>  

1.  <span data-ttu-id="e8866-161">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="e8866-161">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="e8866-162">Dans le panneau **éléments** , accédez à l’onglet **styles** .</span><span class="sxs-lookup"><span data-stu-id="e8866-162">On the **Elements** panel, go to the **Styles** tab.</span></span>  
1.  <span data-ttu-id="e8866-163">Choisissez **: HOV**.</span><span class="sxs-lookup"><span data-stu-id="e8866-163">Choose **:hov**.</span></span>  
1.  <span data-ttu-id="e8866-164">Vérifiez la pseudo-classe que vous souhaitez activer.</span><span class="sxs-lookup"><span data-stu-id="e8866-164">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="e8866-165">Dans l’illustration suivante, faites basculer la `:hover` Pseudo-classe.</span><span class="sxs-lookup"><span data-stu-id="e8866-165">In the following figure, toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="e8866-166">Dans la fenêtre d’affichage, vérifiez que la `background-color: cornflowerblue` déclaration est appliquée à l’élément, même si celui-ci n’est pas en cours de pointage.</span><span class="sxs-lookup"><span data-stu-id="e8866-166">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Basculer entre la pseudo-classe Hover" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   <span data-ttu-id="e8866-168">Activer/désactiver la `:hover` Pseudo-classe</span><span class="sxs-lookup"><span data-stu-id="e8866-168">Toggle the `:hover` pseudo-class</span></span>  
:::image-end:::  

<span data-ttu-id="e8866-169">Pour un didacticiel interactif, voir [Ajouter un PseudoState à une classe][DevToolsCSSGetStartedAddPseudoState].</span><span class="sxs-lookup"><span data-stu-id="e8866-169">For an interactive tutorial, see [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState].</span></span>  

### <span data-ttu-id="e8866-170">Afficher une page en mode d’impression</span><span class="sxs-lookup"><span data-stu-id="e8866-170">View a page in print mode</span></span>  

<span data-ttu-id="e8866-171">Effectuez les opérations suivantes pour afficher une page en mode d’impression.</span><span class="sxs-lookup"><span data-stu-id="e8866-171">Complete the following actions to view a page in print mode.</span></span>  

1.  <span data-ttu-id="e8866-172">[Ouvrir le menu de commandes][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="e8866-172">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="e8866-173">Commencez à taper `Rendering` et sélectionnez `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="e8866-173">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="e8866-174">Dans la liste déroulante **émuler le média CSS** , sélectionnez **Imprimer**.</span><span class="sxs-lookup"><span data-stu-id="e8866-174">For the **Emulate CSS Media** dropdown, select **print**.</span></span>  

### <span data-ttu-id="e8866-175">Afficher les feuilles CSS utilisées et inutilisées avec l’onglet couverture</span><span class="sxs-lookup"><span data-stu-id="e8866-175">View used and unused CSS with the Coverage tab</span></span>  

<span data-ttu-id="e8866-176">L’onglet couverture vous indique la feuille de style en cascade qui est utilisée réellement par une page.</span><span class="sxs-lookup"><span data-stu-id="e8866-176">The Coverage tab shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="e8866-177">`Control` + `Shift` + `P` Dans le menu contextuel, sélectionnez \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \), tandis que devtools est sur le point d' [ouvrir le menu de commandes][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="e8866-177">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to [open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="e8866-178">Commencez à taper `coverage` et sélectionnez **afficher la couverture**.</span><span class="sxs-lookup"><span data-stu-id="e8866-178">Start typing `coverage` and select **Show Coverage**.</span></span>  <span data-ttu-id="e8866-179">L’onglet couverture apparaît.</span><span class="sxs-lookup"><span data-stu-id="e8866-179">The Coverage tab appears.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Ouverture de l’onglet couverture dans le menu de commandes" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             <span data-ttu-id="e8866-181">Ouvrir l’onglet **couverture** dans le **menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="e8866-181">Open the **Coverage** tab from the **Command Menu**</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="Onglet couverture" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             <span data-ttu-id="e8866-183">Onglet **couverture**</span><span class="sxs-lookup"><span data-stu-id="e8866-183">The **Coverage** tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="e8866-184">Sélectionnez **Démarrer l’instrumentation et actualiser la page** \ ( ![ commencer l’instrumentation et actualiser la page ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="e8866-184">Choose **Start instrumenting coverage and refresh the page** \(![Start instrumenting coverage and refresh the page][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="e8866-185">La page actualise et l’onglet couverture fournit une vue d’ensemble de la quantité CSS \ (et JavaScript \) utilisée à partir de chaque fichier chargé par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="e8866-185">The page refreshes and the Coverage tab provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="e8866-186">Green représente les feuilles CSS utilisées.</span><span class="sxs-lookup"><span data-stu-id="e8866-186">Green represents used CSS.</span></span>  <span data-ttu-id="e8866-187">Rouge représente les feuilles CSS inutilisées.</span><span class="sxs-lookup"><span data-stu-id="e8866-187">Red represents unused CSS.</span></span>  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Vue d’ensemble de la quantité d’utilisation et de la feuille de style CSS (JavaScript)" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       <span data-ttu-id="e8866-189">Vue d’ensemble de la quantité d’utilisation et de la feuille de style CSS \ (et JavaScript \)</span><span class="sxs-lookup"><span data-stu-id="e8866-189">An overview of how much CSS \(and JavaScript\) is used and unused</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="e8866-190">Choisissez un fichier CSS pour afficher une répartition ligne par ligne de la feuille de style CSS qu’il utilise.</span><span class="sxs-lookup"><span data-stu-id="e8866-190">Choose a CSS file to see a line-by-line breakdown of what CSS it uses.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e8866-191">Dans l’illustration suivante, les lignes 145 à 147 et 149 à 151 `b66bc881.site-ltr.css` sont inutilisées, tandis que les lignes 163 à 166 sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="e8866-191">In the following figure, lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Une répartition ligne par ligne de feuilles CSS utilisées et inutilisées" lightbox="../media/css-sources-css-coverage.msft.png":::
       <span data-ttu-id="e8866-193">Une répartition ligne par ligne de feuilles CSS utilisées et inutilisées</span><span class="sxs-lookup"><span data-stu-id="e8866-193">A line-by-line breakdown of used and unused CSS</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="e8866-194">Forcer le mode aperçu avant impression</span><span class="sxs-lookup"><span data-stu-id="e8866-194">Force print preview mode</span></span>  

<span data-ttu-id="e8866-195">Pour plus d’DevTools, voir [mode aperçu avant impression][DevToolsCssPrintPreview].</span><span class="sxs-lookup"><span data-stu-id="e8866-195">See [Force DevTools into Print Preview mode][DevToolsCssPrintPreview].</span></span>  

## <span data-ttu-id="e8866-196">Modifier CSS</span><span class="sxs-lookup"><span data-stu-id="e8866-196">Change CSS</span></span>  

<!-- todo s/CSS declaration/declaration/ -->  

### <span data-ttu-id="e8866-197">Ajouter une déclaration CSS à un élément</span><span class="sxs-lookup"><span data-stu-id="e8866-197">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="e8866-198">L’ordre des déclarations affecte la façon dont un élément est stylisé, utilisez la liste suivante pour vous aider à ajouter des déclarations de différentes manières.</span><span class="sxs-lookup"><span data-stu-id="e8866-198">The order of declarations affects how an element is styled, use the following list to help you add declarations in different ways.</span></span>  

*   <span data-ttu-id="e8866-199">[Ajoutez une déclaration inline](#add-an-inline-declaration).</span><span class="sxs-lookup"><span data-stu-id="e8866-199">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="e8866-200">Équivalent à l’ajout d’un `style` attribut au code HTML d’un élément.</span><span class="sxs-lookup"><span data-stu-id="e8866-200">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="e8866-201">[Ajoutez une déclaration à une règle de style](#add-a-declaration-to-a-style-rule).</span><span class="sxs-lookup"><span data-stu-id="e8866-201">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="e8866-202">Quel flux de travail devez-vous utiliser?</span><span class="sxs-lookup"><span data-stu-id="e8866-202">What workflow should you use?</span></span>** <span data-ttu-id="e8866-203">Pour la plupart des scénarios, vous souhaiterez probablement utiliser le flux de travail de déclaration inline.</span><span class="sxs-lookup"><span data-stu-id="e8866-203">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="e8866-204">Les déclarations Inline sont d’une plus grande spécificité par rapport aux déclarations externes, de sorte que le flux de travail intraligne vérifie que les modifications entrent en vigueur dans votre élément attendu.</span><span class="sxs-lookup"><span data-stu-id="e8866-204">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in your expected element.</span></span>  <span data-ttu-id="e8866-205">Pour plus d’informations sur la spécificité, voir [types de sélecteur][MDNSelectorTypes].</span><span class="sxs-lookup"><span data-stu-id="e8866-205">For more information about specificity, see [Selector Types][MDNSelectorTypes].</span></span>  

<span data-ttu-id="e8866-206">Si vous déboguez des styles de l’élément et que vous devez spécifiquement tester ce qui se produit quand une déclaration est définie à des emplacements différents, utilisez l’autre flux de travail.</span><span class="sxs-lookup"><span data-stu-id="e8866-206">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <span data-ttu-id="e8866-207">Ajouter une déclaration en ligne</span><span class="sxs-lookup"><span data-stu-id="e8866-207">Add an inline declaration</span></span>  

<span data-ttu-id="e8866-208">Complétez les actions suivantes pour ajouter une déclaration inline.</span><span class="sxs-lookup"><span data-stu-id="e8866-208">Complete the following actions to add an inline declaration.</span></span>  

1.  <span data-ttu-id="e8866-209">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="e8866-209">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="e8866-210">Dans le volet **styles** , choisissez entre les crochets de la section **élément. style** .</span><span class="sxs-lookup"><span data-stu-id="e8866-210">In the **Styles** pane, choose between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="e8866-211">Le curseur s’attache pour vous permettre d’entrer du texte.</span><span class="sxs-lookup"><span data-stu-id="e8866-211">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="e8866-212">Entrez un nom de propriété et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e8866-212">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="e8866-213">Entrez une valeur valide pour cette propriété, puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e8866-213">Enter a valid value for that property and select `Enter`.</span></span>  <span data-ttu-id="e8866-214">Dans l' **arborescence DOM**, vérifiez qu’un `style` attribut a été ajouté à l’élément.</span><span class="sxs-lookup"><span data-stu-id="e8866-214">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="e8866-215">Dans l’illustration suivante, les `margin-top` `background-color` Propriétés et ont été appliquées à l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e8866-215">In the following figure, the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="e8866-216">Dans l' **arborescence DOM** , assurez-vous que les déclarations sont reflétées dans l' `style` attribut d’un élément.</span><span class="sxs-lookup"><span data-stu-id="e8866-216">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Ajouter des déclarations en ligne" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   <span data-ttu-id="e8866-218">Ajouter des déclarations en ligne</span><span class="sxs-lookup"><span data-stu-id="e8866-218">Add inline declarations</span></span>  
:::image-end:::  

#### <span data-ttu-id="e8866-219">Ajouter une déclaration à une règle de style</span><span class="sxs-lookup"><span data-stu-id="e8866-219">Add a declaration to a style rule</span></span>  

<span data-ttu-id="e8866-220">Pour ajouter une déclaration à une règle de style existante, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="e8866-220">Complete the following actions to add a declaration to an existing style rule.</span></span>  

1.  <span data-ttu-id="e8866-221">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="e8866-221">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="e8866-222">Dans le volet **styles** , choisissez entre les crochets de la règle de style auxquelles vous souhaitez ajouter la déclaration.</span><span class="sxs-lookup"><span data-stu-id="e8866-222">In the **Styles** pane, choose between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="e8866-223">Le curseur s’attache pour vous permettre d’entrer du texte.</span><span class="sxs-lookup"><span data-stu-id="e8866-223">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="e8866-224">Entrez un nom de propriété et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e8866-224">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="e8866-225">Entrez une valeur valide pour cette propriété, puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e8866-225">Enter a valid value for that property and select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Ajout d’une déclaration à une règle de style" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   <span data-ttu-id="e8866-227">Ajouter la `border-bottom-style:groove` déclaration à une règle de style</span><span class="sxs-lookup"><span data-stu-id="e8866-227">Add the `border-bottom-style:groove` declaration to a style rule</span></span>  
:::image-end:::  

### <span data-ttu-id="e8866-228">Modifier le nom ou la valeur d’une déclaration</span><span class="sxs-lookup"><span data-stu-id="e8866-228">Change a declaration name or value</span></span>  

<span data-ttu-id="e8866-229">Choisissez et modifiez le nom ou la valeur d’une déclaration pour la modifier.</span><span class="sxs-lookup"><span data-stu-id="e8866-229">Choose and edit the name or value of a declaration to change it.</span></span>  <span data-ttu-id="e8866-230">Voir [modifier les valeurs de déclaration avec des raccourcis clavier](#change-declaration-values-with-keyboard-shortcuts) pour les raccourcis permettant d’incrémenter ou de décrémenter rapidement une valeur par `0.1` ,, ou par `1` `10` `100` unités.</span><span class="sxs-lookup"><span data-stu-id="e8866-230">See [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts) for shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Modification de la valeur d’une déclaration" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   <span data-ttu-id="e8866-232">Modifiez la valeur de la `border-bottom-style` déclaration.</span><span class="sxs-lookup"><span data-stu-id="e8866-232">Change the value of the `border-bottom-style` declaration</span></span>  
:::image-end:::  

### <span data-ttu-id="e8866-233">Modification des valeurs de déclaration avec les raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="e8866-233">Change declaration values with keyboard shortcuts</span></span>  

<span data-ttu-id="e8866-234">Lors de la modification de la valeur d’une déclaration, vous pouvez utiliser les raccourcis clavier suivants pour incrémenter la valeur à un certain montant.</span><span class="sxs-lookup"><span data-stu-id="e8866-234">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a specific amount.</span></span>  

*   <span data-ttu-id="e8866-235">Sélectionnez `Alt` + `Up` \ (Windows \) ou `Option` + `Up` \ (MacOS \) `0.1` .</span><span class="sxs-lookup"><span data-stu-id="e8866-235">Select `Alt`+`Up` \(Windows\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="e8866-236">`Up`Pour modifier la valeur par `1` ou `0.1` si la valeur actuelle est comprise entre `-1` et `1` .</span><span class="sxs-lookup"><span data-stu-id="e8866-236">Select `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="e8866-237">Sélectionner `Shift` + `Up` pour incrémenter par `10` .</span><span class="sxs-lookup"><span data-stu-id="e8866-237">Select `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="e8866-238">Sélectionnez `Shift` + `Page Up` \ (Windows \) ou `Shift` + `Command` + `Up` \ (MacOS \) pour incrémenter la valeur `100` .</span><span class="sxs-lookup"><span data-stu-id="e8866-238">Select `Shift`+`Page Up` \(Windows\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="e8866-239">La décrémentation fonctionne également.</span><span class="sxs-lookup"><span data-stu-id="e8866-239">Decrementing also works.</span></span>  <span data-ttu-id="e8866-240">Il vous suffit de remplacer chaque instance décrite `Up` plus haut par `Down` .</span><span class="sxs-lookup"><span data-stu-id="e8866-240">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <span data-ttu-id="e8866-241">Ajouter une classe à un élément</span><span class="sxs-lookup"><span data-stu-id="e8866-241">Add a class to an element</span></span>  

<span data-ttu-id="e8866-242">Pour ajouter une classe à un élément, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="e8866-242">Complete the following actions to add a class to an element.</span></span>  

1.  <span data-ttu-id="e8866-243">[Sélectionnez l’élément](#select-an-element) dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="e8866-243">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="e8866-244">Sélectionnez **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="e8866-244">Choose **.cls**.</span></span>  
1.  <span data-ttu-id="e8866-245">Entrez le nom de la classe dans la zone de texte **Ajouter une nouvelle classe** .</span><span class="sxs-lookup"><span data-stu-id="e8866-245">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="e8866-246">Sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e8866-246">Select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Volet classes d’éléments" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   <span data-ttu-id="e8866-248">Volet **classes d’éléments**</span><span class="sxs-lookup"><span data-stu-id="e8866-248">The **Element Classes** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="e8866-249">Basculer une classe</span><span class="sxs-lookup"><span data-stu-id="e8866-249">Toggle a class</span></span>  

<span data-ttu-id="e8866-250">Pour activer ou désactiver une classe sur un élément, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="e8866-250">Complete the following actions to enable or disable a class on an element.</span></span>  

1.  <span data-ttu-id="e8866-251">[Sélectionnez l’élément](#select-an-element) dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="e8866-251">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="e8866-252">Ouvrez le volet **classes d’éléments** .</span><span class="sxs-lookup"><span data-stu-id="e8866-252">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="e8866-253">Voir [Ajouter une classe à un élément](#add-a-class-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="e8866-253">See [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="e8866-254">Sous la zone de texte **Ajouter une nouvelle classe** figurent toutes les classes qui sont appliquées à l’élément spécifique.</span><span class="sxs-lookup"><span data-stu-id="e8866-254">Below the **Add New Class** text box are all of the classes that are being applied to the specific element.</span></span>  
1.  <span data-ttu-id="e8866-255">Activez/désactivez la case à cocher en regard de la classe que vous souhaitez activer ou désactiver.</span><span class="sxs-lookup"><span data-stu-id="e8866-255">Toggle the checkbox next to the class that you want to enable or disable.</span></span>  

### <span data-ttu-id="e8866-256">Ajouter une règle de style</span><span class="sxs-lookup"><span data-stu-id="e8866-256">Add a style rule</span></span>  

<span data-ttu-id="e8866-257">Complétez les actions suivantes pour ajouter une nouvelle règle de style.</span><span class="sxs-lookup"><span data-stu-id="e8866-257">Complete the following actions to add a new style rule.</span></span>  

1.  <span data-ttu-id="e8866-258">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="e8866-258">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="e8866-259">Cliquez sur **nouvelle règle de style** \ ( ![ nouvelle règle de style ][ImageNewStyleRuleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="e8866-259">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\).</span></span>  <span data-ttu-id="e8866-260">DevTools insère une nouvelle règle sous la règle **élément. style** .</span><span class="sxs-lookup"><span data-stu-id="e8866-260">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="e8866-261">Dans l’illustration suivante, DevTools ajoute la `h1.devsite-page-title` règle de style après que vous avez choisi **nouvelle règle de style**.</span><span class="sxs-lookup"><span data-stu-id="e8866-261">In the following figure, DevTools adds the `h1.devsite-page-title` style rule after you choose **New Style Rule**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Ajouter une nouvelle règle de style" lightbox="../media/css-elements-styles-style-new.msft.png":::
   <span data-ttu-id="e8866-263">Ajouter une nouvelle règle de style</span><span class="sxs-lookup"><span data-stu-id="e8866-263">Add a new style rule</span></span>  
:::image-end:::  

#### <span data-ttu-id="e8866-264">Sélectionner la feuille de style à laquelle ajouter une règle</span><span class="sxs-lookup"><span data-stu-id="e8866-264">Choose which stylesheet to add a rule to</span></span>  

<span data-ttu-id="e8866-265">Lors de l' [Ajout d’une nouvelle règle de style](#add-a-style-rule), choisissez une **nouvelle règle de style** et maintenez-la enfoncée ![ ][ImageNewStyleRuleIcon] .</span><span class="sxs-lookup"><span data-stu-id="e8866-265">When [adding a new style rule](#add-a-style-rule), choose and hold **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) to choose which stylesheet to add the style rule to.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Sélectionner une feuille de style" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   <span data-ttu-id="e8866-267">Sélectionner une feuille de style</span><span class="sxs-lookup"><span data-stu-id="e8866-267">Choose a stylesheet</span></span>  
:::image-end:::  

#### <span data-ttu-id="e8866-268">Ajouter une règle de style à un emplacement spécifique</span><span class="sxs-lookup"><span data-stu-id="e8866-268">Add a style rule to a specific location</span></span>  

<span data-ttu-id="e8866-269">Pour ajouter une règle de style à un emplacement spécifique, accédez à l’onglet **styles** , procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="e8866-269">Complete the following actions to add a style rule to a specific location in the **Styles** tab.</span></span>  

1.  <span data-ttu-id="e8866-270">Pointez sur la règle de style qui se trouve directement au-dessus de l’endroit où vous souhaitez ajouter votre nouvelle règle de style.</span><span class="sxs-lookup"><span data-stu-id="e8866-270">Hover over the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="e8866-271">[Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="e8866-271">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="e8866-272">Choisissez **Insérer une règle de style ci-dessous** \ ( ![ Insérer une règle de style ci-dessous ][ImageNewStyleRuleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="e8866-272">Choose **Insert Style Rule Below** \(![Insert Style Rule Below][ImageNewStyleRuleIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Insérer une règle de style en dessous" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **<span data-ttu-id="e8866-274">Insérer une règle de style en dessous</span><span class="sxs-lookup"><span data-stu-id="e8866-274">Insert Style Rule Below</span></span>**  
:::image-end:::  

### <span data-ttu-id="e8866-275">Afficher la barre d’outils plus d’actions</span><span class="sxs-lookup"><span data-stu-id="e8866-275">Reveal the More Actions toolbar</span></span>  

<span data-ttu-id="e8866-276">La barre d’outils **plus d’actions** vous permet d’effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e8866-276">The **More Actions** toolbar lets you perform the following actions.</span></span>  

*   <span data-ttu-id="e8866-277">Insérez une règle de style juste en dessous de celle qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="e8866-277">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="e8866-278">Ajoutez une `background-color` `color` `box-shadow` `text-shadow` déclaration à la règle de style sur laquelle vous êtes prioritaire.</span><span class="sxs-lookup"><span data-stu-id="e8866-278">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="e8866-279">Effectuez les opérations suivantes pour afficher la barre d’outils **plus d’actions** .</span><span class="sxs-lookup"><span data-stu-id="e8866-279">Complete the following actions to reveal the **More Actions** toolbar.</span></span>  

1.  <span data-ttu-id="e8866-280">Dans l’onglet **styles** , pointez sur une règle de style.</span><span class="sxs-lookup"><span data-stu-id="e8866-280">In the **Styles** tab, hover over a style rule.</span></span>  <span data-ttu-id="e8866-281">D' **autres actions** ( `...` \) sont affichées dans le coin inférieur droit de la section règle de style.</span><span class="sxs-lookup"><span data-stu-id="e8866-281">**More Actions** \(`...`\) is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e8866-282">Dans l’illustration suivante, placez le pointeur de la souris sur la `.header-holder.has-default-focus` règle de style et d' **autres actions** sont affichées dans le coin inférieur droit de la section règle de style.</span><span class="sxs-lookup"><span data-stu-id="e8866-282">In the following figure, hover over the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Afficher d’autres actions" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       <span data-ttu-id="e8866-284">Afficher d' **autres actions** `...`</span><span class="sxs-lookup"><span data-stu-id="e8866-284">Reveal **More Actions** \(`...`\)</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e8866-285">Placez le pointeur sur **plus d’actions** `...` pour afficher les actions mentionnées ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="e8866-285">Hover over **More Actions** \(`...`\) to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e8866-286">L’action **Insérer une règle de style ci-dessous** apparaît après avoir pointé sur **plus d’actions**.</span><span class="sxs-lookup"><span data-stu-id="e8866-286">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="Barre d’outils plus d’actions" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       <span data-ttu-id="e8866-288">Barre d’outils **plus d’actions**</span><span class="sxs-lookup"><span data-stu-id="e8866-288">The **More Actions** toolbar</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="e8866-289">Basculer une déclaration</span><span class="sxs-lookup"><span data-stu-id="e8866-289">Toggle a declaration</span></span>  

<span data-ttu-id="e8866-290">Complétez les actions folllwoing pour basculer une déclaration unique sur \ (ou désactivé).</span><span class="sxs-lookup"><span data-stu-id="e8866-290">Complete the folllwoing actions to toggle a single declaration on \(or off\).</span></span>  

1.  <span data-ttu-id="e8866-291">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="e8866-291">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="e8866-292">Dans le volet **styles** , pointez sur la règle qui définit la déclaration.</span><span class="sxs-lookup"><span data-stu-id="e8866-292">In the **Styles** pane, hover over the rule that defines the declaration.</span></span>  <span data-ttu-id="e8866-293">Une case à cocher est affichée en regard de chaque déclaration.</span><span class="sxs-lookup"><span data-stu-id="e8866-293">A checkbox appears next to each declaration.</span></span>  
1.  <span data-ttu-id="e8866-294">Activez/désactivez la case à cocher en regard de la déclaration.</span><span class="sxs-lookup"><span data-stu-id="e8866-294">Check \(or uncheck\) the checkbox next to the declaration.</span></span>  <span data-ttu-id="e8866-295">Lorsque vous décochez une déclaration, DevTools la traverse pour indiquer qu’elle n’est plus active.</span><span class="sxs-lookup"><span data-stu-id="e8866-295">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="e8866-296">Dans l’illustration suivante, la `margin-top` propriété de l’élément actuellement sélectionné a été activée.</span><span class="sxs-lookup"><span data-stu-id="e8866-296">In the following figure, the `margin-top` property for the currently selected element has been toggled off.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Basculer une déclaration" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   <span data-ttu-id="e8866-298">Basculer une déclaration</span><span class="sxs-lookup"><span data-stu-id="e8866-298">Toggle a declaration</span></span>  
:::image-end:::  

### <span data-ttu-id="e8866-299">Ajouter une déclaration couleur d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="e8866-299">Add a background-color declaration</span></span>  

<span data-ttu-id="e8866-300">Pour ajouter une `background-color` déclaration à un élément, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="e8866-300">Complete the following actions to add a `background-color` declaration to an element.</span></span>  

1.  <span data-ttu-id="e8866-301">Pointez sur la règle de style à laquelle vous souhaitez ajouter la `background-color` déclaration.</span><span class="sxs-lookup"><span data-stu-id="e8866-301">Hover over the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="e8866-302">[Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="e8866-302">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="e8866-303">Sélectionnez **Ajouter une couleur d’arrière-plan** \ ( ![ Ajouter une couleur d’arrière-plan ][ImageAddBackgroundColorIcon] \).</span><span class="sxs-lookup"><span data-stu-id="e8866-303">Choose **Add Background Color** \(![Add Background Color][ImageAddBackgroundColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Ajouter une couleur d’arrière-plan" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **<span data-ttu-id="e8866-305">Ajouter une couleur d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="e8866-305">Add Background Color</span></span>**  
:::image-end:::  

### <span data-ttu-id="e8866-306">Ajouter une déclaration de couleur</span><span class="sxs-lookup"><span data-stu-id="e8866-306">Add a color declaration</span></span>  

<span data-ttu-id="e8866-307">Pour ajouter une `color` déclaration à un élément, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="e8866-307">Complete the following actions to add a `color` declaration to an element.</span></span>  

1.  <span data-ttu-id="e8866-308">Pointez sur la règle de style à laquelle vous souhaitez ajouter la `color` déclaration.</span><span class="sxs-lookup"><span data-stu-id="e8866-308">Hover over the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="e8866-309">[Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="e8866-309">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="e8866-310">Sélectionnez **Ajouter une couleur** \ (ajouter une couleur ![ ][ImageAddColorIcon] ).</span><span class="sxs-lookup"><span data-stu-id="e8866-310">Choose **Add Color** \(![Add Color][ImageAddColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Ajouter de la couleur" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **<span data-ttu-id="e8866-312">Ajouter de la couleur</span><span class="sxs-lookup"><span data-stu-id="e8866-312">Add Color</span></span>**  
:::image-end:::  

### <span data-ttu-id="e8866-313">Ajouter une déclaration d’ombre Box</span><span class="sxs-lookup"><span data-stu-id="e8866-313">Add a box-shadow declaration</span></span>  

<span data-ttu-id="e8866-314">Pour ajouter une `box-shadow` déclaration à un élément, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="e8866-314">Complete the follwoing actions to add a `box-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="e8866-315">Pointez sur la règle de style à laquelle vous souhaitez ajouter la `box-shadow` déclaration.</span><span class="sxs-lookup"><span data-stu-id="e8866-315">Hover over the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="e8866-316">[Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="e8866-316">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="e8866-317">Choisissez **ombrer une zone** , puis sélectionnez ombre dans ![ la zone ][ImageAddBoxShadowIcon] .</span><span class="sxs-lookup"><span data-stu-id="e8866-317">Choose **Add Box Shadow** \(![Add Box Shadow][ImageAddBoxShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Ajouter une ombre de zone" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **<span data-ttu-id="e8866-319">Ajouter une ombre de zone</span><span class="sxs-lookup"><span data-stu-id="e8866-319">Add Box Shadow</span></span>**  
:::image-end:::  

### <span data-ttu-id="e8866-320">Ajouter une déclaration d’ombre textuelle</span><span class="sxs-lookup"><span data-stu-id="e8866-320">Add a text-shadow declaration</span></span>  

<span data-ttu-id="e8866-321">Pour ajouter une `text-shadow` déclaration à un élément, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="e8866-321">Complete the following actions to add a `text-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="e8866-322">Pointez sur la règle de style à laquelle vous souhaitez ajouter la `text-shadow` déclaration.</span><span class="sxs-lookup"><span data-stu-id="e8866-322">Hover over the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="e8866-323">[Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="e8866-323">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="e8866-324">Cliquez sur **Ajouter une ombre de texte** \ (ajouter une ombre de ![ texte ][ImageAddTextShadowIcon] ).</span><span class="sxs-lookup"><span data-stu-id="e8866-324">Choose **Add Text Shadow** \(![Add Text Shadow][ImageAddTextShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Ajouter une ombre de texte" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **<span data-ttu-id="e8866-326">Ajouter une ombre de texte</span><span class="sxs-lookup"><span data-stu-id="e8866-326">Add Text Shadow</span></span>**  
:::image-end:::  

### <span data-ttu-id="e8866-327">Changer les couleurs à l’aide du sélecteur de couleurs</span><span class="sxs-lookup"><span data-stu-id="e8866-327">Change colors with the Color Picker</span></span>  

<span data-ttu-id="e8866-328">Le **Sélecteur de couleurs** fournit une interface utilisateur pour le changement `color` et la `background-color` déclaration.</span><span class="sxs-lookup"><span data-stu-id="e8866-328">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="e8866-329">Procédez comme suit pour ouvrir le **Sélecteur de couleurs**.</span><span class="sxs-lookup"><span data-stu-id="e8866-329">Complete the following actions to open the **Color Picker**.</span></span>  

1.  <span data-ttu-id="e8866-330">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="e8866-330">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="e8866-331">Dans l’onglet **styles** , recherchez la `color` `background-color` déclaration, ou similaire, que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="e8866-331">In the **Styles** tab, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="e8866-332">À gauche de la `color` valeur, `background-color` ou similaire, il existe un petit carré, qui est un aperçu de la couleur.</span><span class="sxs-lookup"><span data-stu-id="e8866-332">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e8866-333">Dans l’illustration ci-dessous, le petit carré à gauche de `rgba(0, 0, 0, 0.7)` est un aperçu de cette couleur.</span><span class="sxs-lookup"><span data-stu-id="e8866-333">In the following figure, the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Aperçu de couleur" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       <span data-ttu-id="e8866-335">Aperçu de couleur</span><span class="sxs-lookup"><span data-stu-id="e8866-335">Color preview</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e8866-336">Sélectionnez l’Aperçu pour ouvrir le **Sélecteur de couleurs**.</span><span class="sxs-lookup"><span data-stu-id="e8866-336">Choose the preview to open the **Color Picker**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="Sélecteur de couleurs" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       <span data-ttu-id="e8866-338">**Sélecteur de couleurs**</span><span class="sxs-lookup"><span data-stu-id="e8866-338">The **Color Picker**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="e8866-339">La figure et la liste suivantes décrit de chaque élément d’interface utilisateur du **Sélecteur de couleurs**.</span><span class="sxs-lookup"><span data-stu-id="e8866-339">The following figure and list descries of each of the UI elements of the **Color Picker**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="Sélecteur de couleurs, annoté" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   <span data-ttu-id="e8866-341">**Sélecteur de couleurs**, annoté</span><span class="sxs-lookup"><span data-stu-id="e8866-341">The **Color Picker**, annotated</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      <span data-ttu-id="e8866-342">1</span><span class="sxs-lookup"><span data-stu-id="e8866-342">1</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="e8866-343">Niveaux</span><span class="sxs-lookup"><span data-stu-id="e8866-343">Shades</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="e8866-344">deuxième</span><span class="sxs-lookup"><span data-stu-id="e8866-344">2</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="e8866-345">Compte</span><span class="sxs-lookup"><span data-stu-id="e8866-345">Eyedropper</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8866-346">Pour plus d’informations, reportez-vous à la section [exemple de couleur de la page avec le pipette](#sample-a-color-off-the-page-with-the-eyedropper).</span><span class="sxs-lookup"><span data-stu-id="e8866-346">For more information, see [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="e8866-347">3D</span><span class="sxs-lookup"><span data-stu-id="e8866-347">3</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="e8866-348">Copier dans le Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="e8866-348">Copy To Clipboard</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8866-349">Copiez la **valeur d’affichage** dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="e8866-349">Copy the **Display Value** to your clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="e8866-350">n°4</span><span class="sxs-lookup"><span data-stu-id="e8866-350">4</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="e8866-351">Valeur d’affichage</span><span class="sxs-lookup"><span data-stu-id="e8866-351">Display Value</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8866-352">La représentation RVBA, HSLA ou Hex de la couleur.</span><span class="sxs-lookup"><span data-stu-id="e8866-352">The RGBA, HSLA, or Hex representation of the color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="e8866-353">n°5</span><span class="sxs-lookup"><span data-stu-id="e8866-353">5</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="e8866-354">Palette de couleurs</span><span class="sxs-lookup"><span data-stu-id="e8866-354">Color Palette</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8866-355">Choisissez l’un des carrés pour changer la couleur en carré.</span><span class="sxs-lookup"><span data-stu-id="e8866-355">Choose one of the squares to change the color to that square.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="e8866-356">6</span><span class="sxs-lookup"><span data-stu-id="e8866-356">6</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="e8866-357">Teinte</span><span class="sxs-lookup"><span data-stu-id="e8866-357">Hue</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="e8866-358">6</span><span class="sxs-lookup"><span data-stu-id="e8866-358">7</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="e8866-359">Opacity</span><span class="sxs-lookup"><span data-stu-id="e8866-359">Opacity</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="e8866-360">version8</span><span class="sxs-lookup"><span data-stu-id="e8866-360">8</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="e8866-361">Sélecteur de valeurs d’affichage</span><span class="sxs-lookup"><span data-stu-id="e8866-361">Display Value Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8866-362">Basculer entre les représentations RVBA, HSLA et Hex de la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="e8866-362">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="e8866-363">09</span><span class="sxs-lookup"><span data-stu-id="e8866-363">9</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="e8866-364">Sélecteur de palettes de couleurs</span><span class="sxs-lookup"><span data-stu-id="e8866-364">Color Palette Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8866-365">Basculer entre la [palette de création matérielle][MaterialDesignColorSystem], une palette personnalisée ou une palette de couleurs de page.</span><span class="sxs-lookup"><span data-stu-id="e8866-365">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="e8866-366">DevTools génère la palette de couleurs de page en fonction des couleurs qu’il trouve dans vos feuilles de style.</span><span class="sxs-lookup"><span data-stu-id="e8866-366">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="e8866-367">Exemple de couleur de la page avec le compte-gouttes</span><span class="sxs-lookup"><span data-stu-id="e8866-367">Sample a color off the page with the Eyedropper</span></span>  

<span data-ttu-id="e8866-368">Lorsque vous ouvrez le **Sélecteur de couleurs**, la **pipette** \ ( ![ pipette ][ImageEyedropperIcon] \) est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="e8866-368">When you open the **Color Picker**, the **Eyedropper** \(![Eyedropper][ImageEyedropperIcon]\) is on by default.</span></span>  <span data-ttu-id="e8866-369">Procédez comme suit pour modifier la couleur sélectionnée sur une autre couleur de la page.</span><span class="sxs-lookup"><span data-stu-id="e8866-369">Complete the following actions to change the selected color to some other color on the page.</span></span>  

1.  <span data-ttu-id="e8866-370">Placez le pointeur de la souris sur la couleur cible dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e8866-370">Hover over the target color in the viewport.</span></span>  
1.  <span data-ttu-id="e8866-371">Confirmez votre choix.</span><span class="sxs-lookup"><span data-stu-id="e8866-371">Choose to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e8866-372">Dans l’illustration ci-dessous, le **Sélecteur de couleurs** affiche une valeur de couleur actuelle de `rgba(0,0,0,0.7)` , qui est proche de noir.</span><span class="sxs-lookup"><span data-stu-id="e8866-372">In the following figure, the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="e8866-373">La couleur spécifique doit être modifiée en une version de noir actuellement mise en surbrillance dans la fenêtre d’affichage, une fois que vous avez choisi celle-ci.</span><span class="sxs-lookup"><span data-stu-id="e8866-373">The specific color should change to the version of black that is currently highlighted in the viewport after you chose it.</span></span>  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Utiliser le compte-gouttes" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       <span data-ttu-id="e8866-375">Utiliser le compte-gouttes</span><span class="sxs-lookup"><span data-stu-id="e8866-375">Using the Eyedropper</span></span>  
    :::image-end:::  
    
<!-- image links -->  

[ImageAddBackgroundColorIcon]: ../media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: ../media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: ../media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: ../media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: ../media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: ../media/select-an-element-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsCSSGetStarted]: ../css/index.md "Découvrir comment afficher et modifier des feuilles CSS | Documents Microsoft"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Ajouter un PseudoState à une classe: Familiarisez-vous avec l’affichage et la modification d’une feuille de style CSS | Documents Microsoft"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Affichage de la feuille de style en cascade (CSS) d’un élément: commencez à afficher et modifier des feuilles CSS | Documents Microsoft"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Forcez Microsoft Edge DevTools en mode d’aperçu avant impression (CSS Print Media Type) | Documents Microsoft"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#make-a-minified-file-readable "Faire une référence de débogage de fichier minified-JavaScript Documents Microsoft"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "Conception système couleur-matériau"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "Le modèle de zone | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Types de sélecteur-spécificité | MDN"  

> [!NOTE]
> <span data-ttu-id="e8866-385">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e8866-385">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e8866-386">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="e8866-386">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="e8866-388">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e8866-388">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
