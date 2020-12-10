---
description: Découvrez de nouveaux flux de travail pour l’affichage et la modification de feuilles CSS dans Microsoft Edge DevTools.
title: Référence CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 83edc15549b4f8e668af99a4d95966736aaa0992
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/09/2020
ms.locfileid: "11204011"
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

# <span data-ttu-id="d137f-104">Référence CSS</span><span class="sxs-lookup"><span data-stu-id="d137f-104">CSS reference</span></span>  

<span data-ttu-id="d137f-105">Découvrez les nouveaux flux de travail dans les informations de référence détaillées suivantes sur les fonctionnalités de Microsoft Edge DevTools liées à l’affichage et la modification de feuilles CSS.</span><span class="sxs-lookup"><span data-stu-id="d137f-105">Discover new workflows in the following comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="d137f-106">Pour en savoir plus sur les concepts de base, voir prendre en [main l’affichage et la modification de feuilles CSS][DevToolsCSSGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="d137f-106">See [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted] to learn the basics.</span></span>  

## <span data-ttu-id="d137f-107">Sélectionner un élément</span><span class="sxs-lookup"><span data-stu-id="d137f-107">Select an element</span></span>  

<span data-ttu-id="d137f-108">Le panneau **éléments** de devtools vous permet d’afficher ou de modifier la feuille de style CSS d’un élément à la fois.</span><span class="sxs-lookup"><span data-stu-id="d137f-108">The **Elements** panel of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="d137f-109">L’élément sélectionné est mis en surbrillance dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="d137f-109">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="d137f-110">Les styles de l’élément apparaissent dans le volet **styles** .</span><span class="sxs-lookup"><span data-stu-id="d137f-110">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="d137f-111">Voir [afficher la feuille de style en cascade (CSS) d’un élément][DevToolsCSSGetStartedTutorial] pour un didacticiel.</span><span class="sxs-lookup"><span data-stu-id="d137f-111">See [View the CSS for an element][DevToolsCSSGetStartedTutorial] for a tutorial.</span></span>  

> [!NOTE]
> <span data-ttu-id="d137f-112">Dans l’illustration suivante, l' `h1` élément qui est surligné dans l' **arborescence DOM** est l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d137f-112">In the following figure, the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="d137f-113">À droite, les styles de l’élément apparaissent dans le volet **styles** .</span><span class="sxs-lookup"><span data-stu-id="d137f-113">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="d137f-114">Sur la gauche, l’élément est mis en surbrillance dans la fenêtre d’affichage, mais uniquement dans la mesure où la souris pointe actuellement sur celle-ci dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="d137f-114">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Exemple d’élément sélectionné" lightbox="../media/css-elements-styles-h1.msft.png":::
   <span data-ttu-id="d137f-116">Exemple d’élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="d137f-116">An example of a selected element</span></span>  
:::image-end:::  

<span data-ttu-id="d137f-117">Utilisez l’une des actions suivantes pour sélectionner un élément.</span><span class="sxs-lookup"><span data-stu-id="d137f-117">Use one the following actions to select an element.</span></span>  

*   <span data-ttu-id="d137f-118">Dans votre fenêtre d’affichage, pointez sur l’élément, ouvrez le menu contextuel (cliquez avec le bouton droit sur \), puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="d137f-118">In your viewport, hover on the element, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
*   <span data-ttu-id="d137f-119">Dans devtools, choisissez **Sélectionner un élément** \ ( ![ Sélectionnez un élément ][ImageSelectAnElementIcon] \) ou `Control` + `Shift` + `C` \ (Windows, Linux \) ou `Command` + `Shift` + `C` \ (MacOS \), puis sélectionnez l’élément dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d137f-119">In DevTools, choose **Select an element** \(![Select an element][ImageSelectAnElementIcon]\) or select `Control`+`Shift`+`C` \(Windows, Linux\) or `Command`+`Shift`+`C` \(macOS\), and then choose the element in the viewport.</span></span>  
*   <span data-ttu-id="d137f-120">Dans DevTools, sélectionnez l’élément dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="d137f-120">In DevTools, choose the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="d137f-121">Dans DevTools, exécutez une requête telle que `document.querySelector('p')` dans la **console**, pointez sur le résultat, ouvrez le menu contextuel, puis cliquez sur **afficher dans le panneau éléments**.</span><span class="sxs-lookup"><span data-stu-id="d137f-121">In DevTools, run a query like `document.querySelector('p')` in the **Console**, hover on the result, open the contextual menu \(right-click\), and choose **Reveal in Elements panel**.</span></span>  

## <span data-ttu-id="d137f-122">Afficher les feuilles CSS</span><span class="sxs-lookup"><span data-stu-id="d137f-122">View CSS</span></span>  

### <span data-ttu-id="d137f-123">Affichage de la feuille de style externe dans laquelle une règle est définie</span><span class="sxs-lookup"><span data-stu-id="d137f-123">View the external stylesheet where a rule is defined</span></span>  

<span data-ttu-id="d137f-124">Dans le volet **styles** , cliquez sur le lien en regard d’une règle CSS pour ouvrir la feuille de style externe qui définit la règle.</span><span class="sxs-lookup"><span data-stu-id="d137f-124">In the **Styles** pane, choose the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  

<span data-ttu-id="d137f-125">S’il s’agit de minified, accédez à la section [rendre un fichier minified lisible][DevToolsJavascriptReferenceFormat].</span><span class="sxs-lookup"><span data-stu-id="d137f-125">If the stylesheet is minified, navigate to [Make a minified file readable][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="d137f-126">Dans l’illustration suivante, une fois que vous avez choisi, `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` vous êtes redirigé vers la ligne 2 de `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , où la `.content h1:first-of-type` règle CSS est définie.</span><span class="sxs-lookup"><span data-stu-id="d137f-126">In the following figure, after you choose `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` you are taken to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Affichage de la feuille de style dans laquelle une règle est définie" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  <span data-ttu-id="d137f-128">Affichage de la feuille de style dans laquelle une règle est définie</span><span class="sxs-lookup"><span data-stu-id="d137f-128">Viewing the stylesheet where a rule is defined</span></span>  
:::image-end:::  

### <span data-ttu-id="d137f-129">Afficher uniquement les feuilles CSS appliquées actuellement à un élément</span><span class="sxs-lookup"><span data-stu-id="d137f-129">View only the CSS that is actually applied to an element</span></span>  

<span data-ttu-id="d137f-130">L’onglet **styles** affiche toutes les règles qui s’appliquent à un élément, y compris les déclarations qui ont été remplacées.</span><span class="sxs-lookup"><span data-stu-id="d137f-130">The **Styles** tab shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="d137f-131">Lorsque vous n’êtes pas intéressé par des déclarations substituées, utilisez l’onglet **calculé** pour afficher uniquement les feuilles CSS qui sont réellement appliquées à un élément.</span><span class="sxs-lookup"><span data-stu-id="d137f-131">When you are not interested in overridden declarations, use the **Computed** tab to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="d137f-132">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="d137f-132">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="d137f-133">Accédez à l’onglet **calculé** dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="d137f-133">Go to the **Computed** tab in the **Elements** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="d137f-134">Dans le cas d’une fenêtre DevTools large, l’onglet **calculé** n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="d137f-134">On a wide DevTools window, the **Computed** tab does not exist.</span></span>  <span data-ttu-id="d137f-135">Le contenu de l’onglet **calculé** est affiché dans l’onglet **styles** .</span><span class="sxs-lookup"><span data-stu-id="d137f-135">The contents of the **Computed** tab are shown on the **Styles** tab.</span></span>  

<span data-ttu-id="d137f-136">Les propriétés héritées sont opaques.</span><span class="sxs-lookup"><span data-stu-id="d137f-136">Inherited properties are opaque.</span></span>  <span data-ttu-id="d137f-137">Cochez la case **Afficher tout** pour afficher toutes les valeurs héritées.</span><span class="sxs-lookup"><span data-stu-id="d137f-137">Check the **Show All** checkbox to see all inherited values.</span></span>  

> [!NOTE]
> <span data-ttu-id="d137f-138">Dans l’illustration suivante, l’onglet **calculé** montre les propriétés CSS qui sont appliquées à l’élément actuellement sélectionné `h1` .</span><span class="sxs-lookup"><span data-stu-id="d137f-138">In the following figure, the **Computed** tab shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="Onglet calculé" lightbox="../media/css-elements-computed-h1.msft.png":::
   <span data-ttu-id="d137f-140">Onglet **calculé**</span><span class="sxs-lookup"><span data-stu-id="d137f-140">The **Computed** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="d137f-141">Afficher les propriétés CSS par ordre alphabétique</span><span class="sxs-lookup"><span data-stu-id="d137f-141">View CSS properties in alphabetical order</span></span>  

<span data-ttu-id="d137f-142">Utilisez l’onglet **calculé** .  Voir [afficher uniquement la feuille de style CSS qui est réellement appliquée à un élément](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="d137f-142">Use the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="d137f-143">Afficher les propriétés CSS héritées</span><span class="sxs-lookup"><span data-stu-id="d137f-143">View inherited CSS properties</span></span>  

<span data-ttu-id="d137f-144">Cochez la case **Afficher tout** dans l’onglet **calculé** .  Voir [afficher uniquement la feuille de style CSS qui est réellement appliquée à un élément](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="d137f-144">Check the **Show All** checkbox in the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="d137f-145">Afficher le modèle de boîte pour un élément</span><span class="sxs-lookup"><span data-stu-id="d137f-145">View the box model for an element</span></span>  

<span data-ttu-id="d137f-146">Pour afficher [le modèle de zone][MDNBoxModel] d’un élément, accédez à l’onglet **styles** .  Si votre fenêtre DevTools est étroite, le diagramme de **modèle de cadre** est en bas de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="d137f-146">To view [the box model][MDNBoxModel] of an element, go to the **Styles** tab.  If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the tab.</span></span>  

<span data-ttu-id="d137f-147">Pour modifier une valeur, sélectionnez et modifiez sur une valeur.</span><span class="sxs-lookup"><span data-stu-id="d137f-147">Choose and edit on a value to change a value.</span></span>  

> [!NOTE]
> <span data-ttu-id="d137f-148">Dans l’illustration suivante, le diagramme de **modèle de cadre** sous l’onglet **styles** affiche le modèle de zone de l’élément actuellement sélectionné `h1` .</span><span class="sxs-lookup"><span data-stu-id="d137f-148">In the following figure, the **Box Model** diagram in the **Styles** tab shows the box model for the currently selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="Diagramme de modèle de cadre" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   <span data-ttu-id="d137f-150">Diagramme de **modèle de cadre**</span><span class="sxs-lookup"><span data-stu-id="d137f-150">The **Box Model** diagram</span></span>  
:::image-end:::  

### <span data-ttu-id="d137f-151">Rechercher et filtrer la CSS d’un élément</span><span class="sxs-lookup"><span data-stu-id="d137f-151">Search and filter the CSS of an element</span></span>  

<span data-ttu-id="d137f-152">Utilisez la zone de texte **filtre** des **styles** et des onglets **calculés** pour rechercher des propriétés ou des valeurs CSS spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d137f-152">Use the **Filter** text box on the **Styles** and **Computed** tabs to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="d137f-153">Pour effectuer une recherche dans les propriétés héritées dans l’onglet **calculé** , activez la case à cocher **Afficher tout** .</span><span class="sxs-lookup"><span data-stu-id="d137f-153">To also search inherited properties in the **Computed** tab, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="d137f-154">Dans l’illustration suivante, l’onglet **styles** est filtré pour afficher uniquement les règles qui incluent la requête de recherche `color` .</span><span class="sxs-lookup"><span data-stu-id="d137f-154">In the following figure, the **Styles** tab is filtered to only show rules that include the search query `color`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Filtrer l’onglet styles" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   <span data-ttu-id="d137f-156">Filtrer l’onglet **styles**</span><span class="sxs-lookup"><span data-stu-id="d137f-156">Filter the **Styles** tab</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="d137f-157">Dans l’illustration suivante, l’onglet **calculé** est filtré pour afficher uniquement les déclarations qui incluent la requête de recherche `100%` .</span><span class="sxs-lookup"><span data-stu-id="d137f-157">In the following figure, the **Computed** tab is filtered to only show declarations that include the search query `100%`.</span></span>  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Filtrer l’onglet calculé" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   <span data-ttu-id="d137f-159">Filtrer l’onglet **calculé**</span><span class="sxs-lookup"><span data-stu-id="d137f-159">Filter the **Computed** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="d137f-160">Basculer une pseudo-classe</span><span class="sxs-lookup"><span data-stu-id="d137f-160">Toggle a pseudo-class</span></span>  

<span data-ttu-id="d137f-161">Effectuez les opérations suivantes pour basculer une pseudo-classe comme `:active` , `:focus` , `:hover` ou `:visited` .</span><span class="sxs-lookup"><span data-stu-id="d137f-161">Complete the following actions to toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`.</span></span>  

1.  <span data-ttu-id="d137f-162">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="d137f-162">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="d137f-163">Dans le panneau **éléments** , accédez à l’onglet **styles** .</span><span class="sxs-lookup"><span data-stu-id="d137f-163">On the **Elements** panel, go to the **Styles** tab.</span></span>  
1.  <span data-ttu-id="d137f-164">Choisissez **: HOV**.</span><span class="sxs-lookup"><span data-stu-id="d137f-164">Choose **:hov**.</span></span>  
1.  <span data-ttu-id="d137f-165">Vérifiez la pseudo-classe que vous souhaitez activer.</span><span class="sxs-lookup"><span data-stu-id="d137f-165">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="d137f-166">Dans l’illustration suivante, faites basculer la `:hover` Pseudo-classe.</span><span class="sxs-lookup"><span data-stu-id="d137f-166">In the following figure, toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="d137f-167">Dans la fenêtre d’affichage, vérifiez que la `background-color: cornflowerblue` déclaration est appliquée à l’élément, même si celui-ci n’est pas en cours de pointage.</span><span class="sxs-lookup"><span data-stu-id="d137f-167">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Basculer entre la pseudo-classe Hover" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   <span data-ttu-id="d137f-169">Activer/désactiver la `:hover` Pseudo-classe</span><span class="sxs-lookup"><span data-stu-id="d137f-169">Toggle the `:hover` pseudo-class</span></span>  
:::image-end:::  

<span data-ttu-id="d137f-170">Pour un didacticiel interactif, accédez à [Ajouter un PseudoState à une classe][DevToolsCSSGetStartedAddPseudoState].</span><span class="sxs-lookup"><span data-stu-id="d137f-170">For an interactive tutorial, navigate to [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState].</span></span>  

### <span data-ttu-id="d137f-171">Afficher une page en mode d’impression</span><span class="sxs-lookup"><span data-stu-id="d137f-171">View a page in print mode</span></span>  

<span data-ttu-id="d137f-172">Effectuez les opérations suivantes pour afficher une page en mode d’impression.</span><span class="sxs-lookup"><span data-stu-id="d137f-172">Complete the following actions to view a page in print mode.</span></span>  

1.  <span data-ttu-id="d137f-173">[Ouvrir le menu de commandes][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="d137f-173">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="d137f-174">Commencez à taper `Rendering` et sélectionnez `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="d137f-174">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="d137f-175">Dans la liste déroulante **émuler les contenus multimédias CSS** , sélectionnez **Imprimer**.</span><span class="sxs-lookup"><span data-stu-id="d137f-175">For the **Emulate CSS Media** dropdown, choose **print**.</span></span>  

### <span data-ttu-id="d137f-176">Afficher les feuilles CSS utilisées et inutilisées avec l’onglet couverture</span><span class="sxs-lookup"><span data-stu-id="d137f-176">View used and unused CSS with the Coverage tab</span></span>  

<span data-ttu-id="d137f-177">L’onglet couverture vous indique la feuille de style en cascade qui est utilisée réellement par une page.</span><span class="sxs-lookup"><span data-stu-id="d137f-177">The Coverage tab shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="d137f-178">`Control` + `Shift` + `P` Dans le menu contextuel, sélectionnez \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \), tandis que devtools est sur le point d' [ouvrir le menu de commandes][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="d137f-178">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to [open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="d137f-179">Commencez à taper `coverage` et sélectionnez **afficher la couverture**.</span><span class="sxs-lookup"><span data-stu-id="d137f-179">Start typing `coverage` and choose **Show Coverage**.</span></span>  <span data-ttu-id="d137f-180">L’onglet couverture apparaît.</span><span class="sxs-lookup"><span data-stu-id="d137f-180">The Coverage tab appears.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Ouverture de l’onglet couverture dans le menu de commandes" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             <span data-ttu-id="d137f-182">Ouvrir l’onglet **couverture** dans le **menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="d137f-182">Open the **Coverage** tab from the **Command Menu**</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="Onglet couverture" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             <span data-ttu-id="d137f-184">Onglet **couverture**</span><span class="sxs-lookup"><span data-stu-id="d137f-184">The **Coverage** tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="d137f-185">Sélectionnez **Démarrer l’instrumentation et actualiser la page** \ ( ![ commencer l’instrumentation et actualiser la page ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d137f-185">Choose **Start instrumenting coverage and refresh the page** \(![Start instrumenting coverage and refresh the page][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="d137f-186">La page actualise et l’onglet couverture fournit une vue d’ensemble de la quantité CSS \ (et JavaScript \) utilisée à partir de chaque fichier chargé par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="d137f-186">The page refreshes and the Coverage tab provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="d137f-187">Green représente les feuilles CSS utilisées.</span><span class="sxs-lookup"><span data-stu-id="d137f-187">Green represents used CSS.</span></span>  <span data-ttu-id="d137f-188">Rouge représente les feuilles CSS inutilisées.</span><span class="sxs-lookup"><span data-stu-id="d137f-188">Red represents unused CSS.</span></span>  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Vue d’ensemble de la quantité d’utilisation et de la feuille de style CSS (JavaScript)" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       <span data-ttu-id="d137f-190">Vue d’ensemble de la quantité d’utilisation et de la feuille de style CSS \ (et JavaScript \)</span><span class="sxs-lookup"><span data-stu-id="d137f-190">An overview of how much CSS \(and JavaScript\) is used and unused</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="d137f-191">Choisissez un fichier CSS pour afficher une répartition ligne par ligne de la feuille de style CSS qu’il utilise.</span><span class="sxs-lookup"><span data-stu-id="d137f-191">Choose a CSS file to see a line-by-line breakdown of what CSS it uses.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d137f-192">Dans l’illustration suivante, les lignes 145 à 147 et 149 à 151 `b66bc881.site-ltr.css` sont inutilisées, tandis que les lignes 163 à 166 sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="d137f-192">In the following figure, lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Une répartition ligne par ligne de feuilles CSS utilisées et inutilisées" lightbox="../media/css-sources-css-coverage.msft.png":::
       <span data-ttu-id="d137f-194">Une répartition ligne par ligne de feuilles CSS utilisées et inutilisées</span><span class="sxs-lookup"><span data-stu-id="d137f-194">A line-by-line breakdown of used and unused CSS</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="d137f-195">Forcer le mode aperçu avant impression</span><span class="sxs-lookup"><span data-stu-id="d137f-195">Force print preview mode</span></span>  

<span data-ttu-id="d137f-196">Pour plus d’DevTools, voir [mode aperçu avant impression][DevToolsCssPrintPreview].</span><span class="sxs-lookup"><span data-stu-id="d137f-196">See [Force DevTools into Print Preview mode][DevToolsCssPrintPreview].</span></span>  

## <span data-ttu-id="d137f-197">Modifier CSS</span><span class="sxs-lookup"><span data-stu-id="d137f-197">Change CSS</span></span>  

<!-- todo s/CSS declaration/declaration/ -->  

### <span data-ttu-id="d137f-198">Ajouter une déclaration CSS à un élément</span><span class="sxs-lookup"><span data-stu-id="d137f-198">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="d137f-199">L’ordre des déclarations affecte la façon dont un élément est stylisé, utilisez la liste suivante pour vous aider à ajouter des déclarations de différentes manières.</span><span class="sxs-lookup"><span data-stu-id="d137f-199">The order of declarations affects how an element is styled, use the following list to help you add declarations in different ways.</span></span>  

*   <span data-ttu-id="d137f-200">[Ajoutez une déclaration inline](#add-an-inline-declaration).</span><span class="sxs-lookup"><span data-stu-id="d137f-200">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="d137f-201">Équivalent à l’ajout d’un `style` attribut au code HTML d’un élément.</span><span class="sxs-lookup"><span data-stu-id="d137f-201">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="d137f-202">[Ajoutez une déclaration à une règle de style](#add-a-declaration-to-a-style-rule).</span><span class="sxs-lookup"><span data-stu-id="d137f-202">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="d137f-203">Quel flux de travail devez-vous utiliser?</span><span class="sxs-lookup"><span data-stu-id="d137f-203">What workflow should you use?</span></span>** <span data-ttu-id="d137f-204">Pour la plupart des scénarios, vous souhaiterez probablement utiliser le flux de travail de déclaration inline.</span><span class="sxs-lookup"><span data-stu-id="d137f-204">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="d137f-205">Les déclarations Inline sont d’une plus grande spécificité par rapport aux déclarations externes, de sorte que le flux de travail intraligne vérifie que les modifications entrent en vigueur dans votre élément attendu.</span><span class="sxs-lookup"><span data-stu-id="d137f-205">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in your expected element.</span></span>  <span data-ttu-id="d137f-206">Pour plus d’informations sur la spécificité, accédez à [types de sélecteur][MDNSelectorTypes].</span><span class="sxs-lookup"><span data-stu-id="d137f-206">For more information about specificity, navigate to [Selector Types][MDNSelectorTypes].</span></span>  

<span data-ttu-id="d137f-207">Si vous déboguez des styles de l’élément et que vous devez spécifiquement tester ce qui se produit quand une déclaration est définie à des emplacements différents, utilisez l’autre flux de travail.</span><span class="sxs-lookup"><span data-stu-id="d137f-207">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <span data-ttu-id="d137f-208">Ajouter une déclaration en ligne</span><span class="sxs-lookup"><span data-stu-id="d137f-208">Add an inline declaration</span></span>  

<span data-ttu-id="d137f-209">Complétez les actions suivantes pour ajouter une déclaration inline.</span><span class="sxs-lookup"><span data-stu-id="d137f-209">Complete the following actions to add an inline declaration.</span></span>  

1.  <span data-ttu-id="d137f-210">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="d137f-210">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="d137f-211">Dans le volet **styles** , choisissez entre les crochets de la section **élément. style** .</span><span class="sxs-lookup"><span data-stu-id="d137f-211">In the **Styles** pane, choose between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="d137f-212">Le curseur s’attache pour vous permettre d’entrer du texte.</span><span class="sxs-lookup"><span data-stu-id="d137f-212">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="d137f-213">Entrez un nom de propriété et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="d137f-213">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="d137f-214">Entrez une valeur valide pour cette propriété, puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="d137f-214">Enter a valid value for that property and select `Enter`.</span></span>  <span data-ttu-id="d137f-215">Dans l' **arborescence DOM**, vérifiez qu’un `style` attribut a été ajouté à l’élément.</span><span class="sxs-lookup"><span data-stu-id="d137f-215">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="d137f-216">Dans l’illustration suivante, les `margin-top` `background-color` Propriétés et ont été appliquées à l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d137f-216">In the following figure, the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="d137f-217">Dans l' **arborescence DOM** , assurez-vous que les déclarations sont reflétées dans l' `style` attribut d’un élément.</span><span class="sxs-lookup"><span data-stu-id="d137f-217">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Ajouter des déclarations en ligne" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   <span data-ttu-id="d137f-219">Ajouter des déclarations en ligne</span><span class="sxs-lookup"><span data-stu-id="d137f-219">Add inline declarations</span></span>  
:::image-end:::  

#### <span data-ttu-id="d137f-220">Ajouter une déclaration à une règle de style</span><span class="sxs-lookup"><span data-stu-id="d137f-220">Add a declaration to a style rule</span></span>  

<span data-ttu-id="d137f-221">Pour ajouter une déclaration à une règle de style existante, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d137f-221">Complete the following actions to add a declaration to an existing style rule.</span></span>  

1.  <span data-ttu-id="d137f-222">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="d137f-222">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="d137f-223">Dans le volet **styles** , choisissez entre les crochets de la règle de style auxquelles vous souhaitez ajouter la déclaration.</span><span class="sxs-lookup"><span data-stu-id="d137f-223">In the **Styles** pane, choose between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="d137f-224">Le curseur s’attache pour vous permettre d’entrer du texte.</span><span class="sxs-lookup"><span data-stu-id="d137f-224">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="d137f-225">Entrez un nom de propriété et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="d137f-225">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="d137f-226">Entrez une valeur valide pour cette propriété, puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="d137f-226">Enter a valid value for that property and select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Ajout d’une déclaration à une règle de style" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   <span data-ttu-id="d137f-228">Ajouter la `border-bottom-style:groove` déclaration à une règle de style</span><span class="sxs-lookup"><span data-stu-id="d137f-228">Add the `border-bottom-style:groove` declaration to a style rule</span></span>  
:::image-end:::  

### <span data-ttu-id="d137f-229">Modifier le nom ou la valeur d’une déclaration</span><span class="sxs-lookup"><span data-stu-id="d137f-229">Change a declaration name or value</span></span>  

<span data-ttu-id="d137f-230">Choisissez et modifiez le nom ou la valeur d’une déclaration pour la modifier.</span><span class="sxs-lookup"><span data-stu-id="d137f-230">Choose and edit the name or value of a declaration to change it.</span></span>  <span data-ttu-id="d137f-231">Voir [modifier les valeurs de déclaration avec des raccourcis clavier](#change-declaration-values-with-keyboard-shortcuts) pour les raccourcis permettant d’incrémenter ou de décrémenter rapidement une valeur par `0.1` ,, ou par `1` `10` `100` unités.</span><span class="sxs-lookup"><span data-stu-id="d137f-231">See [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts) for shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Modification de la valeur d’une déclaration" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   <span data-ttu-id="d137f-233">Modifiez la valeur de la `border-bottom-style` déclaration.</span><span class="sxs-lookup"><span data-stu-id="d137f-233">Change the value of the `border-bottom-style` declaration</span></span>  
:::image-end:::  

### <span data-ttu-id="d137f-234">Modification des valeurs de déclaration avec les raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="d137f-234">Change declaration values with keyboard shortcuts</span></span>  

<span data-ttu-id="d137f-235">Lors de la modification de la valeur d’une déclaration, vous pouvez utiliser les raccourcis clavier suivants pour incrémenter la valeur à un certain montant.</span><span class="sxs-lookup"><span data-stu-id="d137f-235">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a specific amount.</span></span>  

*   <span data-ttu-id="d137f-236">Sélectionnez `Alt` + `Up` \ (Windows, Linux \) ou `Option` + `Up` \ (MacOS \) `0.1` .</span><span class="sxs-lookup"><span data-stu-id="d137f-236">Select `Alt`+`Up` \(Windows, Linux\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="d137f-237">`Up`Pour modifier la valeur par `1` ou `0.1` si la valeur actuelle est comprise entre `-1` et `1` .</span><span class="sxs-lookup"><span data-stu-id="d137f-237">Select `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="d137f-238">Sélectionner `Shift` + `Up` pour incrémenter par `10` .</span><span class="sxs-lookup"><span data-stu-id="d137f-238">Select `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="d137f-239">Sélectionnez `Shift` + `Page Up` \ (Windows, Linux \) ou `Shift` + `Command` + `Up` \ (MacOS \) pour incrémenter la valeur `100` .</span><span class="sxs-lookup"><span data-stu-id="d137f-239">Select `Shift`+`Page Up` \(Windows, Linux\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="d137f-240">La décrémentation fonctionne également.</span><span class="sxs-lookup"><span data-stu-id="d137f-240">Decrementing also works.</span></span>  <span data-ttu-id="d137f-241">Il vous suffit de remplacer chaque instance décrite `Up` plus haut par `Down` .</span><span class="sxs-lookup"><span data-stu-id="d137f-241">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <span data-ttu-id="d137f-242">Ajouter une classe à un élément</span><span class="sxs-lookup"><span data-stu-id="d137f-242">Add a class to an element</span></span>  

<span data-ttu-id="d137f-243">Pour ajouter une classe à un élément, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d137f-243">Complete the following actions to add a class to an element.</span></span>  

1.  <span data-ttu-id="d137f-244">[Sélectionnez l’élément](#select-an-element) dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="d137f-244">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="d137f-245">Sélectionnez **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="d137f-245">Choose **.cls**.</span></span>  
1.  <span data-ttu-id="d137f-246">Entrez le nom de la classe dans la zone de texte **Ajouter une nouvelle classe** .</span><span class="sxs-lookup"><span data-stu-id="d137f-246">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="d137f-247">Sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="d137f-247">Select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Volet classes d’éléments" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   <span data-ttu-id="d137f-249">Volet **classes d’éléments**</span><span class="sxs-lookup"><span data-stu-id="d137f-249">The **Element Classes** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="d137f-250">Basculer une classe</span><span class="sxs-lookup"><span data-stu-id="d137f-250">Toggle a class</span></span>  

<span data-ttu-id="d137f-251">Pour activer ou désactiver une classe sur un élément, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d137f-251">Complete the following actions to enable or disable a class on an element.</span></span>  

1.  <span data-ttu-id="d137f-252">[Sélectionnez l’élément](#select-an-element) dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="d137f-252">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="d137f-253">Ouvrez le volet **classes d’éléments** .</span><span class="sxs-lookup"><span data-stu-id="d137f-253">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="d137f-254">Voir [Ajouter une classe à un élément](#add-a-class-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="d137f-254">See [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="d137f-255">Sous la zone de texte **Ajouter une nouvelle classe** figurent toutes les classes qui sont appliquées à l’élément spécifique.</span><span class="sxs-lookup"><span data-stu-id="d137f-255">Below the **Add New Class** text box are all of the classes that are being applied to the specific element.</span></span>  
1.  <span data-ttu-id="d137f-256">Activez/désactivez la case à cocher en regard de la classe que vous souhaitez activer ou désactiver.</span><span class="sxs-lookup"><span data-stu-id="d137f-256">Toggle the checkbox next to the class that you want to enable or disable.</span></span>  

### <span data-ttu-id="d137f-257">Ajouter une règle de style</span><span class="sxs-lookup"><span data-stu-id="d137f-257">Add a style rule</span></span>  

<span data-ttu-id="d137f-258">Complétez les actions suivantes pour ajouter une nouvelle règle de style.</span><span class="sxs-lookup"><span data-stu-id="d137f-258">Complete the following actions to add a new style rule.</span></span>  

1.  <span data-ttu-id="d137f-259">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="d137f-259">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="d137f-260">Cliquez sur **nouvelle règle de style** \ ( ![ nouvelle règle de style ][ImageNewStyleRuleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d137f-260">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\).</span></span>  <span data-ttu-id="d137f-261">DevTools insère une nouvelle règle sous la règle **élément. style** .</span><span class="sxs-lookup"><span data-stu-id="d137f-261">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="d137f-262">Dans l’illustration suivante, DevTools ajoute la `h1.devsite-page-title` règle de style après que vous avez choisi **nouvelle règle de style**.</span><span class="sxs-lookup"><span data-stu-id="d137f-262">In the following figure, DevTools adds the `h1.devsite-page-title` style rule after you choose **New Style Rule**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Ajouter une nouvelle règle de style" lightbox="../media/css-elements-styles-style-new.msft.png":::
   <span data-ttu-id="d137f-264">Ajouter une nouvelle règle de style</span><span class="sxs-lookup"><span data-stu-id="d137f-264">Add a new style rule</span></span>  
:::image-end:::  

#### <span data-ttu-id="d137f-265">Sélectionner la feuille de style à laquelle ajouter une règle</span><span class="sxs-lookup"><span data-stu-id="d137f-265">Choose which stylesheet to add a rule to</span></span>  

<span data-ttu-id="d137f-266">Lors de l' [Ajout d’une nouvelle règle de style](#add-a-style-rule), choisissez une **nouvelle règle de style** et maintenez-la enfoncée ![ ][ImageNewStyleRuleIcon] .</span><span class="sxs-lookup"><span data-stu-id="d137f-266">When [adding a new style rule](#add-a-style-rule), choose and hold **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) to choose which stylesheet to add the style rule to.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Sélectionner une feuille de style" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   <span data-ttu-id="d137f-268">Sélectionner une feuille de style</span><span class="sxs-lookup"><span data-stu-id="d137f-268">Choose a stylesheet</span></span>  
:::image-end:::  

#### <span data-ttu-id="d137f-269">Ajouter une règle de style à un emplacement spécifique</span><span class="sxs-lookup"><span data-stu-id="d137f-269">Add a style rule to a specific location</span></span>  

<span data-ttu-id="d137f-270">Pour ajouter une règle de style à un emplacement spécifique, accédez à l’onglet **styles** , procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d137f-270">Complete the following actions to add a style rule to a specific location in the **Styles** tab.</span></span>  

1.  <span data-ttu-id="d137f-271">Pointez sur la règle de style qui se trouve directement au-dessus de l’endroit où vous souhaitez ajouter votre nouvelle règle de style.</span><span class="sxs-lookup"><span data-stu-id="d137f-271">Hover over the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="d137f-272">[Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="d137f-272">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="d137f-273">Choisissez **Insérer une règle de style sous** \ ( ![ Insérer une règle de style ci-dessous ][ImageNewStyleRuleIcon] ).</span><span class="sxs-lookup"><span data-stu-id="d137f-273">Choose **Insert Style Rule Below** \(![Insert Style Rule Below icon][ImageNewStyleRuleIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Insérer une règle de style en dessous" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **<span data-ttu-id="d137f-275">Insérer une règle de style en dessous</span><span class="sxs-lookup"><span data-stu-id="d137f-275">Insert Style Rule Below</span></span>**  
:::image-end:::  

### <span data-ttu-id="d137f-276">Afficher la barre d’outils plus d’actions</span><span class="sxs-lookup"><span data-stu-id="d137f-276">Reveal the More Actions toolbar</span></span>  

<span data-ttu-id="d137f-277">La barre d’outils **plus d’actions** vous permet d’effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="d137f-277">The **More Actions** toolbar lets you perform the following actions.</span></span>  

*   <span data-ttu-id="d137f-278">Insérez une règle de style juste en dessous de celle qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="d137f-278">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="d137f-279">Ajoutez une `background-color` `color` `box-shadow` `text-shadow` déclaration à la règle de style sur laquelle vous êtes prioritaire.</span><span class="sxs-lookup"><span data-stu-id="d137f-279">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="d137f-280">Effectuez les opérations suivantes pour afficher la barre d’outils **plus d’actions** .</span><span class="sxs-lookup"><span data-stu-id="d137f-280">Complete the following actions to reveal the **More Actions** toolbar.</span></span>  

1.  <span data-ttu-id="d137f-281">Dans l’onglet **styles** , pointez sur une règle de style.</span><span class="sxs-lookup"><span data-stu-id="d137f-281">In the **Styles** tab, hover over a style rule.</span></span>  <span data-ttu-id="d137f-282">D' **autres actions** ( `...` \) sont affichées dans le coin inférieur droit de la section règle de style.</span><span class="sxs-lookup"><span data-stu-id="d137f-282">**More Actions** \(`...`\) is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d137f-283">Dans l’illustration suivante, placez le pointeur de la souris sur la `.header-holder.has-default-focus` règle de style et d' **autres actions** sont affichées dans le coin inférieur droit de la section règle de style.</span><span class="sxs-lookup"><span data-stu-id="d137f-283">In the following figure, hover over the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Afficher d’autres actions" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       <span data-ttu-id="d137f-285">Afficher d' **autres actions** `...`</span><span class="sxs-lookup"><span data-stu-id="d137f-285">Reveal **More Actions** \(`...`\)</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d137f-286">Placez le pointeur sur **plus d’actions** `...` pour afficher les actions mentionnées ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="d137f-286">Hover over **More Actions** \(`...`\) to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d137f-287">L’action **Insérer une règle de style ci-dessous** apparaît après avoir pointé sur **plus d’actions**.</span><span class="sxs-lookup"><span data-stu-id="d137f-287">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="Barre d’outils plus d’actions" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       <span data-ttu-id="d137f-289">Barre d’outils **plus d’actions**</span><span class="sxs-lookup"><span data-stu-id="d137f-289">The **More Actions** toolbar</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="d137f-290">Basculer une déclaration</span><span class="sxs-lookup"><span data-stu-id="d137f-290">Toggle a declaration</span></span>  

<span data-ttu-id="d137f-291">Complétez les actions folllwoing pour basculer une déclaration unique sur \ (ou désactivé).</span><span class="sxs-lookup"><span data-stu-id="d137f-291">Complete the folllwoing actions to toggle a single declaration on \(or off\).</span></span>  

1.  <span data-ttu-id="d137f-292">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="d137f-292">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="d137f-293">Dans le volet **styles** , pointez sur la règle qui définit la déclaration.</span><span class="sxs-lookup"><span data-stu-id="d137f-293">In the **Styles** pane, hover over the rule that defines the declaration.</span></span>  <span data-ttu-id="d137f-294">Une case à cocher est affichée en regard de chaque déclaration.</span><span class="sxs-lookup"><span data-stu-id="d137f-294">A checkbox appears next to each declaration.</span></span>  
1.  <span data-ttu-id="d137f-295">Activez/désactivez la case à cocher en regard de la déclaration.</span><span class="sxs-lookup"><span data-stu-id="d137f-295">Check \(or uncheck\) the checkbox next to the declaration.</span></span>  <span data-ttu-id="d137f-296">Lorsque vous décochez une déclaration, DevTools la traverse pour indiquer qu’elle n’est plus active.</span><span class="sxs-lookup"><span data-stu-id="d137f-296">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="d137f-297">Dans l’illustration suivante, la `margin-top` propriété de l’élément actuellement sélectionné a été activée.</span><span class="sxs-lookup"><span data-stu-id="d137f-297">In the following figure, the `margin-top` property for the currently selected element has been toggled off.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Basculer une déclaration" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   <span data-ttu-id="d137f-299">Basculer une déclaration</span><span class="sxs-lookup"><span data-stu-id="d137f-299">Toggle a declaration</span></span>  
:::image-end:::  

### <span data-ttu-id="d137f-300">Ajouter une déclaration couleur d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="d137f-300">Add a background-color declaration</span></span>  

<span data-ttu-id="d137f-301">Pour ajouter une `background-color` déclaration à un élément, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d137f-301">Complete the following actions to add a `background-color` declaration to an element.</span></span>  

1.  <span data-ttu-id="d137f-302">Pointez sur la règle de style à laquelle vous souhaitez ajouter la `background-color` déclaration.</span><span class="sxs-lookup"><span data-stu-id="d137f-302">Hover over the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="d137f-303">[Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="d137f-303">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="d137f-304">Sélectionnez **Ajouter une couleur d’arrière-plan** \ ( ![ icône couleur d’arrière-plan ][ImageAddBackgroundColorIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d137f-304">Choose **Add Background Color** \(![Add Background Color icon][ImageAddBackgroundColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Ajouter une couleur d’arrière-plan" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **<span data-ttu-id="d137f-306">Ajouter une couleur d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="d137f-306">Add Background Color</span></span>**  
:::image-end:::  

### <span data-ttu-id="d137f-307">Ajouter une déclaration de couleur</span><span class="sxs-lookup"><span data-stu-id="d137f-307">Add a color declaration</span></span>  

<span data-ttu-id="d137f-308">Pour ajouter une `color` déclaration à un élément, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d137f-308">Complete the following actions to add a `color` declaration to an element.</span></span>  

1.  <span data-ttu-id="d137f-309">Pointez sur la règle de style à laquelle vous souhaitez ajouter la `color` déclaration.</span><span class="sxs-lookup"><span data-stu-id="d137f-309">Hover over the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="d137f-310">[Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="d137f-310">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="d137f-311">Sélectionnez **Ajouter une couleur** \ ( ![ icône Ajouter une couleur ][ImageAddColorIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d137f-311">Choose **Add Color** \(![Add Color icon][ImageAddColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Ajouter de la couleur" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **<span data-ttu-id="d137f-313">Ajouter de la couleur</span><span class="sxs-lookup"><span data-stu-id="d137f-313">Add Color</span></span>**  
:::image-end:::  

### <span data-ttu-id="d137f-314">Ajouter une déclaration d’ombre Box</span><span class="sxs-lookup"><span data-stu-id="d137f-314">Add a box-shadow declaration</span></span>  

<span data-ttu-id="d137f-315">Pour ajouter une `box-shadow` déclaration à un élément, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d137f-315">Complete the follwoing actions to add a `box-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="d137f-316">Pointez sur la règle de style à laquelle vous souhaitez ajouter la `box-shadow` déclaration.</span><span class="sxs-lookup"><span data-stu-id="d137f-316">Hover over the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="d137f-317">[Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="d137f-317">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="d137f-318">Sélectionnez **Ajouter une ombre de zone** \ ( ![ icône d’ombre dans la zone Ajouter ][ImageAddBoxShadowIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d137f-318">Choose **Add Box Shadow** \(![Add Box Shadow icon][ImageAddBoxShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Ajouter une ombre de zone" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **<span data-ttu-id="d137f-320">Ajouter une ombre de zone</span><span class="sxs-lookup"><span data-stu-id="d137f-320">Add Box Shadow</span></span>**  
:::image-end:::  

### <span data-ttu-id="d137f-321">Ajouter une déclaration d’ombre textuelle</span><span class="sxs-lookup"><span data-stu-id="d137f-321">Add a text-shadow declaration</span></span>  

<span data-ttu-id="d137f-322">Pour ajouter une `text-shadow` déclaration à un élément, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d137f-322">Complete the following actions to add a `text-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="d137f-323">Pointez sur la règle de style à laquelle vous souhaitez ajouter la `text-shadow` déclaration.</span><span class="sxs-lookup"><span data-stu-id="d137f-323">Hover over the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="d137f-324">[Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="d137f-324">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="d137f-325">Cliquez sur **Ajouter une ombre de texte** \ ( ![ icône Ajouter une ombre de texte ][ImageAddTextShadowIcon] ).</span><span class="sxs-lookup"><span data-stu-id="d137f-325">Choose **Add Text Shadow** \(![Add Text Shadow icon][ImageAddTextShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Ajouter une ombre de texte" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **<span data-ttu-id="d137f-327">Ajouter une ombre de texte</span><span class="sxs-lookup"><span data-stu-id="d137f-327">Add Text Shadow</span></span>**  
:::image-end:::  

### <span data-ttu-id="d137f-328">Changer les couleurs à l’aide du sélecteur de couleurs</span><span class="sxs-lookup"><span data-stu-id="d137f-328">Change colors with the Color Picker</span></span>  

<span data-ttu-id="d137f-329">Le **Sélecteur de couleurs** fournit une interface utilisateur pour le changement `color` et la `background-color` déclaration.</span><span class="sxs-lookup"><span data-stu-id="d137f-329">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="d137f-330">Procédez comme suit pour ouvrir le **Sélecteur de couleurs**.</span><span class="sxs-lookup"><span data-stu-id="d137f-330">Complete the following actions to open the **Color Picker**.</span></span>  

1.  <span data-ttu-id="d137f-331">[Sélectionnez un élément](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="d137f-331">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="d137f-332">Dans l’onglet **styles** , recherchez la `color` `background-color` déclaration, ou similaire, que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="d137f-332">In the **Styles** tab, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="d137f-333">À gauche de la `color` valeur, `background-color` ou similaire, il existe un petit carré, qui est un aperçu de la couleur.</span><span class="sxs-lookup"><span data-stu-id="d137f-333">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d137f-334">Dans l’illustration ci-dessous, le petit carré à gauche de `rgba(0, 0, 0, 0.7)` est un aperçu de cette couleur.</span><span class="sxs-lookup"><span data-stu-id="d137f-334">In the following figure, the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Aperçu de couleur" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       <span data-ttu-id="d137f-336">Aperçu de couleur</span><span class="sxs-lookup"><span data-stu-id="d137f-336">Color preview</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d137f-337">Sélectionnez l’Aperçu pour ouvrir le **Sélecteur de couleurs**.</span><span class="sxs-lookup"><span data-stu-id="d137f-337">Choose the preview to open the **Color Picker**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="Sélecteur de couleurs" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       <span data-ttu-id="d137f-339">**Sélecteur de couleurs**</span><span class="sxs-lookup"><span data-stu-id="d137f-339">The **Color Picker**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d137f-340">La figure et la liste suivantes décrit de chaque élément d’interface utilisateur du **Sélecteur de couleurs**.</span><span class="sxs-lookup"><span data-stu-id="d137f-340">The following figure and list descries of each of the UI elements of the **Color Picker**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="Sélecteur de couleurs, annoté" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   <span data-ttu-id="d137f-342">**Sélecteur de couleurs**, annoté</span><span class="sxs-lookup"><span data-stu-id="d137f-342">The **Color Picker**, annotated</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      <span data-ttu-id="d137f-343">1</span><span class="sxs-lookup"><span data-stu-id="d137f-343">1</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d137f-344">Niveaux</span><span class="sxs-lookup"><span data-stu-id="d137f-344">Shades</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="d137f-345">deuxième</span><span class="sxs-lookup"><span data-stu-id="d137f-345">2</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d137f-346">Compte</span><span class="sxs-lookup"><span data-stu-id="d137f-346">Eyedropper</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d137f-347">Pour plus d’informations, accédez à l' [exemple de couleur de la page à l’aide du](#sample-a-color-off-the-page-with-the-eyedropper)compte-gouttes.</span><span class="sxs-lookup"><span data-stu-id="d137f-347">For more information, navigate to [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="d137f-348">3D</span><span class="sxs-lookup"><span data-stu-id="d137f-348">3</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d137f-349">Copier dans le Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="d137f-349">Copy To Clipboard</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d137f-350">Copiez la **valeur d’affichage** dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="d137f-350">Copy the **Display Value** to your clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="d137f-351">n°4</span><span class="sxs-lookup"><span data-stu-id="d137f-351">4</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d137f-352">Valeur d’affichage</span><span class="sxs-lookup"><span data-stu-id="d137f-352">Display Value</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d137f-353">La représentation RVBA, HSLA ou Hex de la couleur.</span><span class="sxs-lookup"><span data-stu-id="d137f-353">The RGBA, HSLA, or Hex representation of the color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="d137f-354">n°5</span><span class="sxs-lookup"><span data-stu-id="d137f-354">5</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d137f-355">Palette de couleurs</span><span class="sxs-lookup"><span data-stu-id="d137f-355">Color Palette</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d137f-356">Choisissez l’un des carrés pour changer la couleur en carré.</span><span class="sxs-lookup"><span data-stu-id="d137f-356">Choose one of the squares to change the color to that square.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="d137f-357">6</span><span class="sxs-lookup"><span data-stu-id="d137f-357">6</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d137f-358">Teinte</span><span class="sxs-lookup"><span data-stu-id="d137f-358">Hue</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="d137f-359">6</span><span class="sxs-lookup"><span data-stu-id="d137f-359">7</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d137f-360">Opacity</span><span class="sxs-lookup"><span data-stu-id="d137f-360">Opacity</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="d137f-361">version8</span><span class="sxs-lookup"><span data-stu-id="d137f-361">8</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d137f-362">Sélecteur de valeurs d’affichage</span><span class="sxs-lookup"><span data-stu-id="d137f-362">Display Value Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d137f-363">Basculer entre les représentations RVBA, HSLA et Hex de la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="d137f-363">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="d137f-364">09</span><span class="sxs-lookup"><span data-stu-id="d137f-364">9</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d137f-365">Sélecteur de palettes de couleurs</span><span class="sxs-lookup"><span data-stu-id="d137f-365">Color Palette Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d137f-366">Basculer entre la [palette de création matérielle][MaterialDesignColorSystem], une palette personnalisée ou une palette de couleurs de page.</span><span class="sxs-lookup"><span data-stu-id="d137f-366">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="d137f-367">DevTools génère la palette de couleurs de page en fonction des couleurs qu’il trouve dans vos feuilles de style.</span><span class="sxs-lookup"><span data-stu-id="d137f-367">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="d137f-368">Exemple de couleur de la page avec le compte-gouttes</span><span class="sxs-lookup"><span data-stu-id="d137f-368">Sample a color off the page with the Eyedropper</span></span>  

<span data-ttu-id="d137f-369">Lorsque vous ouvrez le **Sélecteur de couleurs**, la **pipette** \ ( ![ pipette ][ImageEyedropperIcon] \) est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="d137f-369">When you open the **Color Picker**, the **Eyedropper** \(![Eyedropper][ImageEyedropperIcon]\) is on by default.</span></span>  <span data-ttu-id="d137f-370">Procédez comme suit pour modifier la couleur sélectionnée sur une autre couleur de la page.</span><span class="sxs-lookup"><span data-stu-id="d137f-370">Complete the following actions to change the selected color to some other color on the page.</span></span>  

1.  <span data-ttu-id="d137f-371">Placez le pointeur de la souris sur la couleur cible dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d137f-371">Hover over the target color in the viewport.</span></span>  
1.  <span data-ttu-id="d137f-372">Confirmez votre choix.</span><span class="sxs-lookup"><span data-stu-id="d137f-372">Choose to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d137f-373">Dans l’illustration ci-dessous, le **Sélecteur de couleurs** affiche une valeur de couleur actuelle de `rgba(0,0,0,0.7)` , qui est proche de noir.</span><span class="sxs-lookup"><span data-stu-id="d137f-373">In the following figure, the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="d137f-374">La couleur spécifique doit être modifiée en une version de noir actuellement mise en surbrillance dans la fenêtre d’affichage, une fois que vous avez choisi celle-ci.</span><span class="sxs-lookup"><span data-stu-id="d137f-374">The specific color should change to the version of black that is currently highlighted in the viewport after you chose it.</span></span>  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Utiliser le compte-gouttes" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       <span data-ttu-id="d137f-376">Utiliser le compte-gouttes</span><span class="sxs-lookup"><span data-stu-id="d137f-376">Using the Eyedropper</span></span>  
    :::image-end:::  
    
<!--todo:  add the section on the Angle clock section for What's New 88.  -->  

## <span data-ttu-id="d137f-377">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="d137f-377">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

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
> <span data-ttu-id="d137f-387">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d137f-387">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d137f-388">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="d137f-388">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="d137f-390">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d137f-390">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  