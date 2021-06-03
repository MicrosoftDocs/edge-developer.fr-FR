---
description: Découvrez les nouveaux flux de travail pour l’affichage et la modification de CSS dans Microsoft Edge DevTools.
title: Référence CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 0680b08c9809698c1db6c186a7be76a93c31df4b
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564475"
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
# <a name="css-reference"></a><span data-ttu-id="5f0c1-104">Référence CSS</span><span class="sxs-lookup"><span data-stu-id="5f0c1-104">CSS reference</span></span>  

<span data-ttu-id="5f0c1-105">Découvrez les nouveaux flux de travail dans la référence complète Microsoft Edge fonctionnalités DevTools relatives à l’affichage et à la modification de CSS.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-105">Discover new workflows in the following comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="5f0c1-106">Pour en savoir plus sur les bases, [accédez à Prise en main avec l’affichage et la modification de CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="5f0c1-106">To learn the basics, navigate to [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted].</span></span>  

## <a name="choose-an-element"></a><span data-ttu-id="5f0c1-107">Choisir un élément</span><span class="sxs-lookup"><span data-stu-id="5f0c1-107">Choose an element</span></span>  

<span data-ttu-id="5f0c1-108">**L’outil** Elements de DevTools vous permet d’afficher ou de modifier la CSS d’un élément à la fois.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-108">The **Elements** tool of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="5f0c1-109">L’élément sélectionné est mis en surbrillant dans **l’arborescence DOM.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-109">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="5f0c1-110">Les styles de l’élément sont affichés dans le **volet Styles.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-110">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="5f0c1-111">Pour un didacticiel, [accédez à Afficher le CSS d’un élément.][DevToolsCSSGetStartedTutorial]</span><span class="sxs-lookup"><span data-stu-id="5f0c1-111">For a tutorial, navigate to [View the CSS for an element][DevToolsCSSGetStartedTutorial].</span></span>  

> [!NOTE]
> <span data-ttu-id="5f0c1-112">Dans la figure suivante, l’élément mis en surbrillant dans l’arborescence `h1` **DOM** est l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-112">In the following figure, the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="5f0c1-113">À droite, les styles de l’élément sont affichés dans le **volet Styles.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-113">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="5f0c1-114">À gauche, l’élément est mis en surbrillrillation dans la vue, mais uniquement parce que la souris passe actuellement au-dessus de celui-ci dans l’arborescence **DOM**.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-114">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Exemple d’élément sélectionné" lightbox="../media/css-elements-styles-h1.msft.png":::
   <span data-ttu-id="5f0c1-116">Exemple d’élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="5f0c1-116">An example of a selected element</span></span>  
:::image-end:::  

<span data-ttu-id="5f0c1-117">Utilisez l’une des actions suivantes pour sélectionner un élément.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-117">Use one the following actions to select an element.</span></span>  

*   <span data-ttu-id="5f0c1-118">Dans votreport d’affichage, pointez sur l’élément, ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-118">In your viewport, hover on the element, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
*   <span data-ttu-id="5f0c1-119">Dans DevTools, choisissez Sélectionner un élément **\(** Sélectionnez un élément \) ou sélectionnez ![ ](../media/select-an-element-icon.msft.png) `Control` + `Shift` + `C` \(Windows, Linux\) ou `Command` + `Shift` + `C` \(macOS\), puis choisissez l’élément dans la vue.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-119">In DevTools, choose **Select an element** \(![Select an element](../media/select-an-element-icon.msft.png)\) or select `Control`+`Shift`+`C` \(Windows, Linux\) or `Command`+`Shift`+`C` \(macOS\), and then choose the element in the viewport.</span></span>  
*   <span data-ttu-id="5f0c1-120">Dans DevTools, choisissez l’élément dans l’arborescence **DOM**.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-120">In DevTools, choose the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="5f0c1-121">Dans DevTools, exécutez une requête comme dans la console, pointez sur le résultat, ouvrez le menu contextuel `document.querySelector('p')` \(clic \*\*\*\* droit\), puis choisissez Révéler dans le panneau **Éléments.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-121">In DevTools, run a query like `document.querySelector('p')` in the **Console**, hover on the result, open the contextual menu \(right-click\), and choose **Reveal in Elements panel**.</span></span>  

## <a name="view-css"></a><span data-ttu-id="5f0c1-122">Afficher les CSS</span><span class="sxs-lookup"><span data-stu-id="5f0c1-122">View CSS</span></span>  

### <a name="view-the-external-stylesheet-where-a-rule-is-defined"></a><span data-ttu-id="5f0c1-123">Afficher la feuille de style externe dans laquelle une règle est définie</span><span class="sxs-lookup"><span data-stu-id="5f0c1-123">View the external stylesheet where a rule is defined</span></span>  

<span data-ttu-id="5f0c1-124">Dans le **volet Styles,** choisissez le lien en face d’une règle CSS pour ouvrir la feuille de style externe qui définit la règle.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-124">In the **Styles** pane, choose the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  <span data-ttu-id="5f0c1-125">La feuille de style s’ouvre dans le volet **Éditeur** de l’outil **Sources.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-125">The stylesheet opens in the **Editor** pane of the **Sources** tool.</span></span>  

<span data-ttu-id="5f0c1-126">Si la feuille de style est minifiée, choisissez le **bouton Format** \( Format \), en bas du ![ volet ](../media/format-icon.msft.png) Éditeur. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5f0c1-126">If the stylesheet is minified, choose the **Format** \(![Format](../media/format-icon.msft.png)\) button, at the bottom of the **Editor** pane.</span></span>  <span data-ttu-id="5f0c1-127">Pour plus d’informations, accédez à [Reformater un fichier JavaScript minifié avec des caractères assez imprimés.][DevToolsJavascriptReferenceFormat]</span><span class="sxs-lookup"><span data-stu-id="5f0c1-127">For more information, navigate to [Reformat a minified JavaScript file with pretty-print][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="5f0c1-128">Dans la figure suivante, une fois que vous avez choisi, vous êtes conduit à la ligne 2 de , où la règle `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` `.content h1:first-of-type` CSS est définie.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-128">In the following figure, after you choose `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` you are taken to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Affichage de la feuille de style dans laquelle une règle est définie" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  <span data-ttu-id="5f0c1-130">Affichage de la feuille de style dans laquelle une règle est définie</span><span class="sxs-lookup"><span data-stu-id="5f0c1-130">Viewing the stylesheet where a rule is defined</span></span>  
:::image-end:::  

### <a name="view-only-the-css-that-is-actually-applied-to-an-element"></a><span data-ttu-id="5f0c1-131">Afficher uniquement le CSS réellement appliqué à un élément</span><span class="sxs-lookup"><span data-stu-id="5f0c1-131">View only the CSS that is actually applied to an element</span></span>  

<span data-ttu-id="5f0c1-132">Le **panneau Styles** affiche toutes les règles qui s’appliquent à un élément, y compris les déclarations qui ont été overridées.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-132">The **Styles** panel shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="5f0c1-133">Lorsque les déclarations non appliquées ne \*\*\*\* vous intéressent pas, utilisez le panneau Calculé pour afficher uniquement le CSS réellement appliqué à un élément.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-133">When you are not interested in overridden declarations, use the **Computed** panel to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="5f0c1-134">[Sélectionnez un élément.](#choose-an-element)</span><span class="sxs-lookup"><span data-stu-id="5f0c1-134">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="5f0c1-135">Accédez au **panneau Calculé** dans **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-135">Navigate to the **Computed** panel in the **Elements** tool.</span></span>  

> [!NOTE]
> <span data-ttu-id="5f0c1-136">Dans une fenêtre DevTools \*\*\*\* large, le panneau Calculé n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-136">On a wide DevTools window, the **Computed** panel does not exist.</span></span>  <span data-ttu-id="5f0c1-137">Le contenu du panneau **Calculé** est affiché dans le **panneau Styles.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-137">The contents of the **Computed** panel are shown on the **Styles** panel.</span></span>  

<span data-ttu-id="5f0c1-138">Les propriétés héritées sont opaques.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-138">Inherited properties are opaque.</span></span>  <span data-ttu-id="5f0c1-139">Pour afficher toutes les valeurs héritées, cochez **la case Afficher** tout.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-139">To display all inherited values, select the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="5f0c1-140">Dans la figure suivante, le panneau **Calculé** montre les propriétés CSS appliquées à l’élément actuellement `h1` sélectionné.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-140">In the following figure, the **Computed** panel shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="Panneau calculé" lightbox="../media/css-elements-computed-h1.msft.png":::
   <span data-ttu-id="5f0c1-142">Panneau **calculé**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-142">The **Computed** panel</span></span>  
:::image-end:::  

### <a name="view-css-properties-in-alphabetical-order"></a><span data-ttu-id="5f0c1-143">Afficher les propriétés CSS par ordre alphabétique</span><span class="sxs-lookup"><span data-stu-id="5f0c1-143">View CSS properties in alphabetical order</span></span>  

<span data-ttu-id="5f0c1-144">Utilisez le **panneau calculé.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-144">Use the **Computed** panel.</span></span>  <span data-ttu-id="5f0c1-145">Accédez [à Afficher uniquement le CSS réellement appliqué à un élément.](#view-only-the-css-that-is-actually-applied-to-an-element)</span><span class="sxs-lookup"><span data-stu-id="5f0c1-145">Navigate to [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <a name="view-inherited-css-properties"></a><span data-ttu-id="5f0c1-146">Afficher les propriétés CSS héritées</span><span class="sxs-lookup"><span data-stu-id="5f0c1-146">View inherited CSS properties</span></span>  

<span data-ttu-id="5f0c1-147">Cochez **la case Afficher** tout dans le panneau **calculé.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-147">Check the **Show All** checkbox in the **Computed** panel.</span></span>  <span data-ttu-id="5f0c1-148">Accédez [à Afficher uniquement le CSS réellement appliqué à un élément.](#view-only-the-css-that-is-actually-applied-to-an-element)</span><span class="sxs-lookup"><span data-stu-id="5f0c1-148">Navigate to [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <a name="view-the-box-model-for-an-element"></a><span data-ttu-id="5f0c1-149">Afficher le modèle de zone d’un élément</span><span class="sxs-lookup"><span data-stu-id="5f0c1-149">View the box model for an element</span></span>  

<span data-ttu-id="5f0c1-150">Pour afficher [le modèle de zone d’un][MDNBoxModel] élément, accédez au panneau **Styles.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-150">To view [the box model][MDNBoxModel] of an element, navigate to the **Styles** panel.</span></span>  <span data-ttu-id="5f0c1-151">Si votre fenêtre DevTools \*\*\*\* est étroite, le diagramme DevTools se trouve en bas du panneau.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-151">If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the panel.</span></span>  

<span data-ttu-id="5f0c1-152">Choisissez et modifiez une valeur pour modifier une valeur.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-152">Choose and edit on a value to change a value.</span></span>  

> [!NOTE]
> <span data-ttu-id="5f0c1-153">Dans la figure suivante, le diagramme **Modèle** de zone dans le panneau **Styles** montre le modèle de case pour l’élément `h1` actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-153">In the following figure, the **Box Model** diagram in the **Styles** panel shows the box model for the currently selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="Diagramme du modèle Box" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   <span data-ttu-id="5f0c1-155">Diagramme **du modèle Box**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-155">The **Box Model** diagram</span></span>  
:::image-end:::  

### <a name="search-and-filter-the-css-of-an-element"></a><span data-ttu-id="5f0c1-156">Rechercher et filtrer le CSS d’un élément</span><span class="sxs-lookup"><span data-stu-id="5f0c1-156">Search and filter the CSS of an element</span></span>  

<span data-ttu-id="5f0c1-157">Utilisez la **zone de** texte \*\*\*\* Filtre des **panneaux Styles** et Calculé pour rechercher des propriétés ou des valeurs CSS spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-157">Use the **Filter** text box on the **Styles** and **Computed** panels to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="5f0c1-158">Pour également rechercher les propriétés héritées dans le **panneau Calculé,** cochez la case **Afficher tout.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-158">To also search inherited properties in the **Computed** panel, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="5f0c1-159">Dans la figure suivante, le panneau **Styles** est filtré pour afficher uniquement les règles qui incluent la requête de `color` recherche.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-159">In the following figure, the **Styles** panel is filtered to only show rules that include the search query `color`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Filtrer le panneau Styles" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   <span data-ttu-id="5f0c1-161">Filtrer le **panneau Styles**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-161">Filter the **Styles** panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="5f0c1-162">Dans la figure suivante, le panneau **calculé** est filtré pour afficher uniquement les déclarations qui incluent la requête de `100%` recherche.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-162">In the following figure, the **Computed** panel is filtered to only show declarations that include the search query `100%`.</span></span>  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Filtrer le panneau calculé" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   <span data-ttu-id="5f0c1-164">Filtrer **le panneau calculé**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-164">Filter the **Computed** panel</span></span>  
:::image-end:::  

### <a name="toggle-a-pseudo-class"></a><span data-ttu-id="5f0c1-165">Faire basculer une pseudo-classe</span><span class="sxs-lookup"><span data-stu-id="5f0c1-165">Toggle a pseudo-class</span></span>  

<span data-ttu-id="5f0c1-166">Effectuer les actions suivantes pour faire basculer une pseudo-classe telle `:active` `:focus` que , ou `:hover` `:visited` .</span><span class="sxs-lookup"><span data-stu-id="5f0c1-166">Complete the following actions to toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`.</span></span>  

1.  <span data-ttu-id="5f0c1-167">[Sélectionnez un élément.](#choose-an-element)</span><span class="sxs-lookup"><span data-stu-id="5f0c1-167">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="5f0c1-168">Dans **l’outil Éléments,** accédez au **panneau Styles.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-168">On the **Elements** tool, navigate to the **Styles** panel.</span></span>  
1.  <span data-ttu-id="5f0c1-169">Choose **:hov**.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-169">Choose **:hov**.</span></span>  
1.  <span data-ttu-id="5f0c1-170">Vérifiez la pseudo-classe que vous souhaitez activer.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-170">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="5f0c1-171">Dans la figure suivante, basculez la `:hover` pseudo-classe.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-171">In the following figure, toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="5f0c1-172">Dans laport d’affichage, vérifiez que la déclaration est appliquée à l’élément, même si l’élément n’est pas réellement `background-color: cornflowerblue` survolé.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-172">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Toggle the :hover pseudo-class" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   <span data-ttu-id="5f0c1-174">Faire bascule la `:hover` pseudo-classe</span><span class="sxs-lookup"><span data-stu-id="5f0c1-174">Toggle the `:hover` pseudo-class</span></span>  
:::image-end:::  

<span data-ttu-id="5f0c1-175">Pour un didacticiel interactif, [accédez à Ajouter un pseudo-état à une classe.][DevToolsCSSGetStartedAddPseudoState]</span><span class="sxs-lookup"><span data-stu-id="5f0c1-175">For an interactive tutorial, navigate to [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState].</span></span>  

### <a name="view-a-page-in-print-mode"></a><span data-ttu-id="5f0c1-176">Afficher une page en mode d’impression</span><span class="sxs-lookup"><span data-stu-id="5f0c1-176">View a page in print mode</span></span>  

<span data-ttu-id="5f0c1-177">Effectuer les actions suivantes pour afficher une page en mode d’impression.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-177">Complete the following actions to view a page in print mode.</span></span>  

1.  <span data-ttu-id="5f0c1-178">[Ouvrez le menu Commande.][DevToolsCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="5f0c1-178">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="5f0c1-179">Commencez à taper `Rendering` et sélectionnez `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="5f0c1-179">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="5f0c1-180">For the **Emulate CSS Media** dropdown, choose **print**.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-180">For the **Emulate CSS Media** dropdown, choose **print**.</span></span>  

### <a name="view-used-and-unused-css-with-the-coverage-tool"></a><span data-ttu-id="5f0c1-181">Afficher les CSS utilisés et inutilisés avec l’outil Couverture</span><span class="sxs-lookup"><span data-stu-id="5f0c1-181">View used and unused CSS with the Coverage tool</span></span>  

<span data-ttu-id="5f0c1-182">**L’outil** Couverture vous montre ce que les CSS d’une page utilisent réellement.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-182">The **Coverage** tool shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="5f0c1-183">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) alors que DevTools [][DevToolsCommandMenu]est en focus pour ouvrir le menu Commande.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-183">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to [open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="5f0c1-184">Commencez à taper `coverage` et choisissez Afficher la **couverture.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-184">Start typing `coverage` and choose **Show Coverage**.</span></span>  <span data-ttu-id="5f0c1-185">**L’outil** Couverture s’affiche.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-185">The **Coverage** tool appears.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Ouverture de l’outil Couverture à partir du menu Commande" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             <span data-ttu-id="5f0c1-187">Ouvrir **l’outil Couverture** à partir du **menu Commande**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-187">Open the **Coverage** tool from the **Command Menu**</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="L’outil Couverture" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             <span data-ttu-id="5f0c1-189">**L’outil Couverture**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-189">The **Coverage** tool</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="5f0c1-190">Choose **Start instrumenting coverage and refresh the page** \( Start ![ instrumenting coverage and refresh the page ](../media/refresh-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="5f0c1-190">Choose **Start instrumenting coverage and refresh the page** \(![Start instrumenting coverage and refresh the page](../media/refresh-icon.msft.png)\).</span></span>  <span data-ttu-id="5f0c1-191">La page est \*\*\*\* actualisée et l’outil Couverture fournit une vue d’ensemble de la quantité de CSS \(et JavaScript\) utilisée à partir de chaque fichier chargé par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-191">The page refreshes and the **Coverage** tool provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="5f0c1-192">Le vert représente le CSS utilisé.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-192">Green represents used CSS.</span></span>  <span data-ttu-id="5f0c1-193">Le rouge représente les CSS inutilisés.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-193">Red represents unused CSS.</span></span>  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Vue d’ensemble de la quantité de CSS (et JavaScript) utilisée et inutilisée" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       <span data-ttu-id="5f0c1-195">Vue d’ensemble de la quantité de fichiers CSS \(et JavaScript\) utilisées et inutilisées</span><span class="sxs-lookup"><span data-stu-id="5f0c1-195">An overview of how much CSS \(and JavaScript\) is used and unused</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="5f0c1-196">Pour afficher une répartition ligne par ligne du fichier CSS utilisé, choisissez un fichier CSS.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-196">To display a line-by-line breakdown of what CSS is used, choose a CSS file.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5f0c1-197">Dans la figure suivante, les lignes 145 à 147 et 149 à 151 sont inutilisées, tandis que les lignes `b66bc881.site-ltr.css` 163 à 166 sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-197">In the following figure, lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Répartition ligne par ligne des CSS utilisées et inutilisées" lightbox="../media/css-sources-css-coverage.msft.png":::
       <span data-ttu-id="5f0c1-199">Répartition ligne par ligne des CSS utilisées et inutilisées</span><span class="sxs-lookup"><span data-stu-id="5f0c1-199">A line-by-line breakdown of used and unused CSS</span></span>  
    :::image-end:::  
    
### <a name="force-print-preview-mode"></a><span data-ttu-id="5f0c1-200">Forcer le mode d’aperçu avant impression</span><span class="sxs-lookup"><span data-stu-id="5f0c1-200">Force print preview mode</span></span>  

<span data-ttu-id="5f0c1-201">Accédez à [Forcer DevTools en mode Aperçu avant impression.][DevToolsCssPrintPreview]</span><span class="sxs-lookup"><span data-stu-id="5f0c1-201">Navigate to [Force DevTools into Print Preview mode][DevToolsCssPrintPreview].</span></span>  

## <a name="change-css"></a><span data-ttu-id="5f0c1-202">Modifier CSS</span><span class="sxs-lookup"><span data-stu-id="5f0c1-202">Change CSS</span></span>  

<!-- todo s/CSS declaration/declaration/ -->  

### <a name="add-a-css-declaration-to-an-element"></a><span data-ttu-id="5f0c1-203">Ajouter une déclaration CSS à un élément</span><span class="sxs-lookup"><span data-stu-id="5f0c1-203">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="5f0c1-204">L’ordre des déclarations affecte le style d’un élément. Utilisez la liste suivante pour vous aider à ajouter des déclarations de différentes manières.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-204">The order of declarations affects how an element is styled, use the following list to help you add declarations in different ways.</span></span>  

*   <span data-ttu-id="5f0c1-205">[Ajoutez une déclaration inline](#add-an-inline-declaration).</span><span class="sxs-lookup"><span data-stu-id="5f0c1-205">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="5f0c1-206">Équivaut à ajouter un `style` attribut au code HTML d’un élément.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-206">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="5f0c1-207">[Ajoutez une déclaration à une règle de style.](#add-a-declaration-to-a-style-rule)</span><span class="sxs-lookup"><span data-stu-id="5f0c1-207">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="5f0c1-208">Quel flux de travail devez-vous utiliser ?</span><span class="sxs-lookup"><span data-stu-id="5f0c1-208">What workflow should you use?</span></span>** <span data-ttu-id="5f0c1-209">Pour la plupart des scénarios, vous souhaitez probablement utiliser le flux de travail de déclaration inline.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-209">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="5f0c1-210">Les déclarations inline ont une spécificité plus élevée que les déclarations externes, de sorte que le flux de travail en ligne garantit que les modifications prennent effet dans votre élément attendu.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-210">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in your expected element.</span></span>  <span data-ttu-id="5f0c1-211">Pour plus d’informations sur la spécificité, accédez à [Types de sélecteur.][MDNSelectorTypes]</span><span class="sxs-lookup"><span data-stu-id="5f0c1-211">For more information about specificity, navigate to [Selector Types][MDNSelectorTypes].</span></span>  

<span data-ttu-id="5f0c1-212">Si vous déboguer des styles de l’élément et que vous devez spécifiquement tester ce qui se produit lorsqu’une déclaration est définie à différents endroits, utilisez l’autre flux de travail.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-212">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <a name="add-an-inline-declaration"></a><span data-ttu-id="5f0c1-213">Ajouter une déclaration inline</span><span class="sxs-lookup"><span data-stu-id="5f0c1-213">Add an inline declaration</span></span>  

<span data-ttu-id="5f0c1-214">Pour ajouter une déclaration inline, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-214">Complete the following actions to add an inline declaration.</span></span>  

1.  <span data-ttu-id="5f0c1-215">[Sélectionnez un élément.](#choose-an-element)</span><span class="sxs-lookup"><span data-stu-id="5f0c1-215">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="5f0c1-216">Dans le **volet Styles,** choisissez entre les crochets de la section **element.style.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-216">In the **Styles** pane, choose between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="5f0c1-217">Le curseur se concentre, ce qui vous permet d’entrer du texte.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-217">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="5f0c1-218">Entrez un nom de propriété et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5f0c1-218">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="5f0c1-219">Entrez une valeur valide pour cette propriété et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5f0c1-219">Enter a valid value for that property and select `Enter`.</span></span>  <span data-ttu-id="5f0c1-220">Dans **l’arborescence DOM,** vérifiez qu’un attribut a `style` été ajouté à l’élément.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-220">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="5f0c1-221">Dans la figure suivante, les propriétés et les propriétés `margin-top` `background-color` ont été appliquées à l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-221">In the following figure, the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="5f0c1-222">Dans **l’arborescence DOM,** vérifiez que les déclarations sont reflétées dans `style` l’attribut d’un élément.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-222">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Ajouter des déclarations inline" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   <span data-ttu-id="5f0c1-224">Ajouter des déclarations inline</span><span class="sxs-lookup"><span data-stu-id="5f0c1-224">Add inline declarations</span></span>  
:::image-end:::  

#### <a name="add-a-declaration-to-a-style-rule"></a><span data-ttu-id="5f0c1-225">Ajouter une déclaration à une règle de style</span><span class="sxs-lookup"><span data-stu-id="5f0c1-225">Add a declaration to a style rule</span></span>  

<span data-ttu-id="5f0c1-226">Effectuer les actions suivantes pour ajouter une déclaration à une règle de style existante.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-226">Complete the following actions to add a declaration to an existing style rule.</span></span>  

1.  <span data-ttu-id="5f0c1-227">[Sélectionnez un élément.](#choose-an-element)</span><span class="sxs-lookup"><span data-stu-id="5f0c1-227">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="5f0c1-228">Dans le **volet Styles,** choisissez entre les crochets de la règle de style à laquelle vous souhaitez ajouter la déclaration.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-228">In the **Styles** pane, choose between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="5f0c1-229">Le curseur se concentre, ce qui vous permet d’entrer du texte.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-229">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="5f0c1-230">Entrez un nom de propriété et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5f0c1-230">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="5f0c1-231">Entrez une valeur valide pour cette propriété et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5f0c1-231">Enter a valid value for that property and select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Ajout d’une déclaration à une règle de style" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   <span data-ttu-id="5f0c1-233">Ajouter la `border-bottom-style:groove` déclaration à une règle de style</span><span class="sxs-lookup"><span data-stu-id="5f0c1-233">Add the `border-bottom-style:groove` declaration to a style rule</span></span>  
:::image-end:::  

### <a name="change-a-declaration-name-or-value"></a><span data-ttu-id="5f0c1-234">Modifier le nom ou la valeur d’une déclaration</span><span class="sxs-lookup"><span data-stu-id="5f0c1-234">Change a declaration name or value</span></span>  

<span data-ttu-id="5f0c1-235">Choisissez et modifiez le nom ou la valeur d’une déclaration pour la modifier.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-235">Choose and edit the name or value of a declaration to change it.</span></span>  <span data-ttu-id="5f0c1-236">Pour obtenir des raccourcis pour incrémenter ou décrémenter rapidement une valeur par , ou par unité, accédez à Modifier les valeurs de déclaration à l’aide de `0.1` `1` `10` `100` [raccourcis clavier.](#change-declaration-values-with-keyboard-shortcuts)</span><span class="sxs-lookup"><span data-stu-id="5f0c1-236">For shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units, navigate to [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts).</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Modification de la valeur d’une déclaration" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   <span data-ttu-id="5f0c1-238">Modifier la valeur de la `border-bottom-style` déclaration</span><span class="sxs-lookup"><span data-stu-id="5f0c1-238">Change the value of the `border-bottom-style` declaration</span></span>  
:::image-end:::  

### <a name="change-declaration-values-with-keyboard-shortcuts"></a><span data-ttu-id="5f0c1-239">Modifier les valeurs de déclaration à l’aide de raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="5f0c1-239">Change declaration values with keyboard shortcuts</span></span>  

<span data-ttu-id="5f0c1-240">Lors de la modification de la valeur d’une déclaration, vous pouvez utiliser les raccourcis clavier suivants pour incrémenter la valeur d’une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-240">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a specific amount.</span></span>  

*   <span data-ttu-id="5f0c1-241">Sélectionnez `Alt` + `Up` \(Windows, Linux\) ou `Option` + `Up` \(macOS\) pour incrémenter par `0.1` .</span><span class="sxs-lookup"><span data-stu-id="5f0c1-241">Select `Alt`+`Up` \(Windows, Linux\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="5f0c1-242">Sélectionnez `Up` pour modifier la valeur par ou par si la valeur actuelle est entre et `1` `0.1` `-1` `1` .</span><span class="sxs-lookup"><span data-stu-id="5f0c1-242">Select `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="5f0c1-243">Sélectionnez `Shift` + `Up` pour incrémenter par `10` .</span><span class="sxs-lookup"><span data-stu-id="5f0c1-243">Select `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="5f0c1-244">Sélectionnez `Shift` + `Page Up` \(Windows, Linux\) ou `Shift` + `Command` + `Up` \(macOS\) pour incrémenter la valeur par `100` .</span><span class="sxs-lookup"><span data-stu-id="5f0c1-244">Select `Shift`+`Page Up` \(Windows, Linux\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="5f0c1-245">La décrémentation fonctionne également.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-245">Decrementing also works.</span></span>  <span data-ttu-id="5f0c1-246">Remplacez simplement chaque instance mentionnée `Up` ci-dessus par `Down` .</span><span class="sxs-lookup"><span data-stu-id="5f0c1-246">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <a name="add-a-class-to-an-element"></a><span data-ttu-id="5f0c1-247">Ajouter une classe à un élément</span><span class="sxs-lookup"><span data-stu-id="5f0c1-247">Add a class to an element</span></span>  

<span data-ttu-id="5f0c1-248">Pour ajouter une classe à un élément, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-248">Complete the following actions to add a class to an element.</span></span>  

1.  <span data-ttu-id="5f0c1-249">[Sélectionnez l’élément](#choose-an-element) dans **l’arborescence DOM.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-249">[Select the element](#choose-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="5f0c1-250">Choisissez **.cls**.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-250">Choose **.cls**.</span></span>  
1.  <span data-ttu-id="5f0c1-251">Entrez le nom de la classe dans la zone de texte Ajouter **une nouvelle** classe.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-251">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="5f0c1-252">Sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5f0c1-252">Select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Volet Classes d’éléments" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   <span data-ttu-id="5f0c1-254">Volet **Classes d’éléments**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-254">The **Element Classes** pane</span></span>  
:::image-end:::  

### <a name="toggle-a-class"></a><span data-ttu-id="5f0c1-255">Faire basculer une classe</span><span class="sxs-lookup"><span data-stu-id="5f0c1-255">Toggle a class</span></span>  

<span data-ttu-id="5f0c1-256">Effectuer les actions suivantes pour activer ou désactiver une classe sur un élément.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-256">Complete the following actions to enable or disable a class on an element.</span></span>  

1.  <span data-ttu-id="5f0c1-257">[Sélectionnez l’élément](#choose-an-element) dans **l’arborescence DOM.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-257">[Select the element](#choose-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="5f0c1-258">Ouvrez le **volet Classes** d’éléments.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-258">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="5f0c1-259">Accédez à [Ajouter une classe à un élément.](#add-a-class-to-an-element)</span><span class="sxs-lookup"><span data-stu-id="5f0c1-259">Navigate to [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="5f0c1-260">Sous la **zone de texte Ajouter une nouvelle** classe se trouverez toutes les classes appliquées à l’élément spécifique.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-260">Below the **Add New Class** text box are all of the classes applied to the specific element.</span></span>  
1.  <span data-ttu-id="5f0c1-261">Basculez la case à cocher en regard de la classe que vous souhaitez activer ou désactiver.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-261">Toggle the checkbox next to the class that you want to turn on or off.</span></span>  

### <a name="add-a-style-rule"></a><span data-ttu-id="5f0c1-262">Ajouter une règle de style</span><span class="sxs-lookup"><span data-stu-id="5f0c1-262">Add a style rule</span></span>  

<span data-ttu-id="5f0c1-263">Pour ajouter une nouvelle règle de style, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-263">Complete the following actions to add a new style rule.</span></span>  

1.  <span data-ttu-id="5f0c1-264">[Sélectionnez un élément.](#choose-an-element)</span><span class="sxs-lookup"><span data-stu-id="5f0c1-264">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="5f0c1-265">Choose **New Style Rule** \( New Style Rule ![ ](../media/new-style-rule-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="5f0c1-265">Choose **New Style Rule** \(![New Style Rule](../media/new-style-rule-icon.msft.png)\).</span></span>  <span data-ttu-id="5f0c1-266">DevTools insère une nouvelle règle sous la **règle element.style.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-266">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="5f0c1-267">Dans la figure suivante, DevTools ajoute la règle de style après avoir `h1.devsite-page-title` choisi Nouvelle règle de **style**.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-267">In the following figure, DevTools adds the `h1.devsite-page-title` style rule after you choose **New Style Rule**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Ajouter une nouvelle règle de style" lightbox="../media/css-elements-styles-style-new.msft.png":::
   <span data-ttu-id="5f0c1-269">Ajouter une nouvelle règle de style</span><span class="sxs-lookup"><span data-stu-id="5f0c1-269">Add a new style rule</span></span>  
:::image-end:::  

#### <a name="choose-which-stylesheet-to-add-a-rule-to"></a><span data-ttu-id="5f0c1-270">Choisir la feuille de style à laquelle ajouter une règle</span><span class="sxs-lookup"><span data-stu-id="5f0c1-270">Choose which stylesheet to add a rule to</span></span>  

<span data-ttu-id="5f0c1-271">Lorsque [vous ajoutez une nouvelle](#add-a-style-rule)règle de style, choisissez et maintenez la nouvelle règle de **style** \( Nouvelle règle de style \) pour choisir la feuille de style à laquelle ajouter la règle ![ de ](../media/new-style-rule-icon.msft.png) style.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-271">When [adding a new style rule](#add-a-style-rule), choose and hold **New Style Rule** \(![New Style Rule](../media/new-style-rule-icon.msft.png)\) to choose which stylesheet to add the style rule to.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Choisir une feuille de style" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   <span data-ttu-id="5f0c1-273">Choisir une feuille de style</span><span class="sxs-lookup"><span data-stu-id="5f0c1-273">Choose a stylesheet</span></span>  
:::image-end:::  

#### <a name="add-a-style-rule-to-a-specific-location"></a><span data-ttu-id="5f0c1-274">Ajouter une règle de style à un emplacement spécifique</span><span class="sxs-lookup"><span data-stu-id="5f0c1-274">Add a style rule to a specific location</span></span>  

<span data-ttu-id="5f0c1-275">Pour ajouter une règle de style à un emplacement spécifique dans le panneau **Styles,** complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-275">Complete the following actions to add a style rule to a specific location in the **Styles** panel.</span></span>  

1.  <span data-ttu-id="5f0c1-276">Pointez sur la règle de style qui se trouve directement au-dessus de l’endroit où vous souhaitez ajouter votre nouvelle règle de style.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-276">Hover on the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="5f0c1-277">[Révéler la **barre d’outils Actions** plus](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5f0c1-277">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5f0c1-278">Choose **Insert Style Rule Below** \( Insert Style Rule Below icon ![ ](../media/new-style-rule-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="5f0c1-278">Choose **Insert Style Rule Below** \(![Insert Style Rule Below icon](../media/new-style-rule-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Insérer une règle de style en dessous" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **<span data-ttu-id="5f0c1-280">Insérer une règle de style en dessous</span><span class="sxs-lookup"><span data-stu-id="5f0c1-280">Insert Style Rule Below</span></span>**  
:::image-end:::  

### <a name="reveal-the-more-actions-toolbar"></a><span data-ttu-id="5f0c1-281">Révéler la barre d’outils Autres actions</span><span class="sxs-lookup"><span data-stu-id="5f0c1-281">Reveal the More Actions toolbar</span></span>  

<span data-ttu-id="5f0c1-282">La **barre d’outils Autres actions** vous permet d’effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-282">The **More Actions** toolbar lets you perform the following actions.</span></span>  

*   <span data-ttu-id="5f0c1-283">Insérez une règle de style directement sous celle sur qui vous vous concentrez.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-283">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="5f0c1-284">Ajoutez une déclaration , ou une déclaration à la règle de style sur qui `background-color` `color` vous vous `box-shadow` `text-shadow` concentrez.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-284">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="5f0c1-285">Effectuer les actions suivantes pour révéler la **barre d’outils Plus d’actions.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-285">Complete the following actions to reveal the **More Actions** toolbar.</span></span>  

1.  <span data-ttu-id="5f0c1-286">Dans le panneau **Styles,** pointez sur une règle de style.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-286">In the **Styles** panel, hover on a style rule.</span></span>  <span data-ttu-id="5f0c1-287">**D’autres actions** \( \) sont révélées dans le coin inférieur droit `...` de la section de règle de style.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-287">**More Actions** \(`...`\) is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5f0c1-288">Dans la figure suivante, pointez sur la règle de style et d’autres actions sont révélés dans le coin inférieur droit de la `.header-holder.has-default-focus` section de règle de style. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5f0c1-288">In the following figure, hover on the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Révéler d’autres actions" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       <span data-ttu-id="5f0c1-290">Révéler **d’autres actions** \( `...` \)</span><span class="sxs-lookup"><span data-stu-id="5f0c1-290">Reveal **More Actions** \(`...`\)</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5f0c1-291">Pointez sur **plus d’actions** \( `...` \) pour révéler les actions mentionnées ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-291">Hover on **More Actions** \(`...`\) to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5f0c1-292">**L’action Insérer une règle de style ci-dessous** s’est révélée après avoir survolé **d’autres actions.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-292">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="Barre d’outils Autres actions" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       <span data-ttu-id="5f0c1-294">Barre **d’outils Autres actions**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-294">The **More Actions** toolbar</span></span>  
    :::image-end:::  
    
### <a name="toggle-a-declaration"></a><span data-ttu-id="5f0c1-295">Faire basculer une déclaration</span><span class="sxs-lookup"><span data-stu-id="5f0c1-295">Toggle a declaration</span></span>  

<span data-ttu-id="5f0c1-296">Complétez les actions qui s’annoncent pour faire basculer une déclaration unique sur \(ou off\).</span><span class="sxs-lookup"><span data-stu-id="5f0c1-296">Complete the folllwoing actions to toggle a single declaration on \(or off\).</span></span>  

1.  <span data-ttu-id="5f0c1-297">[Sélectionnez un élément.](#choose-an-element)</span><span class="sxs-lookup"><span data-stu-id="5f0c1-297">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="5f0c1-298">Dans le **volet Styles,** pointez sur la règle qui définit la déclaration.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-298">In the **Styles** pane, hover on the rule that defines the declaration.</span></span>  <span data-ttu-id="5f0c1-299">Une case à cocher s’affiche en regard de chaque déclaration.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-299">A checkbox appears next to each declaration.</span></span>  
1.  <span data-ttu-id="5f0c1-300">Cochez \(ou décochez\) la case à cocher en regard de la déclaration.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-300">Check \(or uncheck\) the checkbox next to the declaration.</span></span>  <span data-ttu-id="5f0c1-301">Lorsque vous décochez une déclaration, DevTools la croise pour indiquer qu’elle n’est plus active.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-301">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="5f0c1-302">Dans la figure suivante, la `margin-top` propriété de l’élément actuellement sélectionné a été éteinte.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-302">In the following figure, the `margin-top` property for the currently selected element has been toggled off.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Faire basculer une déclaration" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   <span data-ttu-id="5f0c1-304">Faire basculer une déclaration</span><span class="sxs-lookup"><span data-stu-id="5f0c1-304">Toggle a declaration</span></span>  
:::image-end:::  

### <a name="add-a-background-color-declaration"></a><span data-ttu-id="5f0c1-305">Ajouter une déclaration de couleur d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="5f0c1-305">Add a background-color declaration</span></span>  

<span data-ttu-id="5f0c1-306">Effectuer les actions suivantes pour ajouter une `background-color` déclaration à un élément.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-306">Complete the following actions to add a `background-color` declaration to an element.</span></span>  

1.  <span data-ttu-id="5f0c1-307">Pointez sur la règle de style à ajouter à `background-color` la déclaration.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-307">Hover on the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="5f0c1-308">[Révéler la **barre d’outils Actions** plus](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5f0c1-308">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5f0c1-309">Choose **Add Background Color** \( Add Background Color icon ![ ](../media/add-background-color-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="5f0c1-309">Choose **Add Background Color** \(![Add Background Color icon](../media/add-background-color-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Ajouter une couleur d’arrière-plan" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **<span data-ttu-id="5f0c1-311">Ajouter une couleur d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="5f0c1-311">Add Background Color</span></span>**  
:::image-end:::  

### <a name="add-a-color-declaration"></a><span data-ttu-id="5f0c1-312">Ajouter une déclaration de couleur</span><span class="sxs-lookup"><span data-stu-id="5f0c1-312">Add a color declaration</span></span>  

<span data-ttu-id="5f0c1-313">Effectuer les actions suivantes pour ajouter une `color` déclaration à un élément.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-313">Complete the following actions to add a `color` declaration to an element.</span></span>  

1.  <span data-ttu-id="5f0c1-314">Pointez sur la règle de style à ajouter à `color` la déclaration.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-314">Hover on the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="5f0c1-315">[Révéler la **barre d’outils Actions** plus](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5f0c1-315">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5f0c1-316">Choose **Add Color** \( Add Color icon ![ ](../media/add-color-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="5f0c1-316">Choose **Add Color** \(![Add Color icon](../media/add-color-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Ajouter une couleur" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **<span data-ttu-id="5f0c1-318">Ajouter une couleur</span><span class="sxs-lookup"><span data-stu-id="5f0c1-318">Add Color</span></span>**  
:::image-end:::  

### <a name="add-a-box-shadow-declaration"></a><span data-ttu-id="5f0c1-319">Ajouter une déclaration d’ombre de zone</span><span class="sxs-lookup"><span data-stu-id="5f0c1-319">Add a box-shadow declaration</span></span>  

<span data-ttu-id="5f0c1-320">Effectuer les actions suivantes pour ajouter une `box-shadow` déclaration à un élément.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-320">Complete the follwoing actions to add a `box-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="5f0c1-321">Pointez sur la règle de style à ajouter à `box-shadow` la déclaration.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-321">Hover on the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="5f0c1-322">[Révéler la **barre d’outils Actions** plus](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5f0c1-322">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5f0c1-323">Choose **Add Box Shadow** \( Add Box Shadow icon ![ ](../media/add-box-shadow-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="5f0c1-323">Choose **Add Box Shadow** \(![Add Box Shadow icon](../media/add-box-shadow-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Ajouter une ombre de zone" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **<span data-ttu-id="5f0c1-325">Ajouter une ombre de zone</span><span class="sxs-lookup"><span data-stu-id="5f0c1-325">Add Box Shadow</span></span>**  
:::image-end:::  

### <a name="add-a-text-shadow-declaration"></a><span data-ttu-id="5f0c1-326">Ajouter une déclaration d’ombre de texte</span><span class="sxs-lookup"><span data-stu-id="5f0c1-326">Add a text-shadow declaration</span></span>  

<span data-ttu-id="5f0c1-327">Effectuer les actions suivantes pour ajouter une `text-shadow` déclaration à un élément.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-327">Complete the following actions to add a `text-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="5f0c1-328">Pointez sur la règle de style à ajouter à `text-shadow` la déclaration.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-328">Hover on the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="5f0c1-329">[Révéler la **barre d’outils Actions** plus](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5f0c1-329">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5f0c1-330">Choose **Add Text Shadow** \( Add Text Shadow icon ![ ](../media/add-text-shadow-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="5f0c1-330">Choose **Add Text Shadow** \(![Add Text Shadow icon](../media/add-text-shadow-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Ajouter une ombre de texte" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **<span data-ttu-id="5f0c1-332">Ajouter une ombre de texte</span><span class="sxs-lookup"><span data-stu-id="5f0c1-332">Add Text Shadow</span></span>**  
:::image-end:::  

### <a name="change-colors-with-the-color-picker"></a><span data-ttu-id="5f0c1-333">Modifier les couleurs avec le s sélectionneur de couleurs</span><span class="sxs-lookup"><span data-stu-id="5f0c1-333">Change colors with the Color Picker</span></span>  

<span data-ttu-id="5f0c1-334">Le **s sélectionneur de couleurs** fournit une interface graphique graphique pour la modification `color` et les `background-color` déclarations.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-334">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="5f0c1-335">Effectuer les actions suivantes pour ouvrir le **s picker de couleur**.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-335">Complete the following actions to open the **Color Picker**.</span></span>  

1.  <span data-ttu-id="5f0c1-336">[Sélectionnez un élément.](#choose-an-element)</span><span class="sxs-lookup"><span data-stu-id="5f0c1-336">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="5f0c1-337">Dans le **panneau Styles,** recherchez la déclaration , ou une déclaration similaire, que `color` vous `background-color` souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-337">In the **Styles** panel, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="5f0c1-338">À gauche de la valeur , ou une valeur similaire, il existe un petit carré qui `color` est un aperçu de la `background-color` couleur.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-338">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5f0c1-339">Dans la figure suivante, le petit carré à gauche est un `rgba(0, 0, 0, 0.7)` aperçu de cette couleur.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-339">In the following figure, the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Aperçu de couleur" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       <span data-ttu-id="5f0c1-341">Aperçu de couleur</span><span class="sxs-lookup"><span data-stu-id="5f0c1-341">Color preview</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5f0c1-342">Choisissez l’aperçu pour ouvrir le **s picker de couleurs.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-342">Choose the preview to open the **Color Picker**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="S sélectionneur de couleurs" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       <span data-ttu-id="5f0c1-344">S **sélectionneur de couleurs**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-344">The **Color Picker**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="5f0c1-345">La figure et la liste suivantes dcries de chacun des éléments d’interface utilisateur du s **picker de couleur**.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-345">The following figure and list descries of each of the UI elements of the **Color Picker**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="S sélectionneur de couleurs, annoté" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   <span data-ttu-id="5f0c1-347">Le **s sélectionneur de couleurs,** annoté</span><span class="sxs-lookup"><span data-stu-id="5f0c1-347">The **Color Picker**, annotated</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      <span data-ttu-id="5f0c1-348">1</span><span class="sxs-lookup"><span data-stu-id="5f0c1-348">1</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="5f0c1-349">Nuances</span><span class="sxs-lookup"><span data-stu-id="5f0c1-349">Shades</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="5f0c1-350">2</span><span class="sxs-lookup"><span data-stu-id="5f0c1-350">2</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="5f0c1-351">Eyedropper</span><span class="sxs-lookup"><span data-stu-id="5f0c1-351">Eyedropper</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5f0c1-352">Pour plus d’informations, accédez à l’exemple de couleur de la [page avec le eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span><span class="sxs-lookup"><span data-stu-id="5f0c1-352">For more information, navigate to [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="5f0c1-353">3</span><span class="sxs-lookup"><span data-stu-id="5f0c1-353">3</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="5f0c1-354">Copier dans le Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="5f0c1-354">Copy To Clipboard</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5f0c1-355">Copiez **la valeur d’affichage** dans votre Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-355">Copy the **Display Value** to your clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="5f0c1-356">4</span><span class="sxs-lookup"><span data-stu-id="5f0c1-356">4</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="5f0c1-357">Valeur d’affichage</span><span class="sxs-lookup"><span data-stu-id="5f0c1-357">Display Value</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5f0c1-358">Représentation RGBA, HSLA ou Hex de la couleur.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-358">The RGBA, HSLA, or Hex representation of the color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="5f0c1-359">5</span><span class="sxs-lookup"><span data-stu-id="5f0c1-359">5</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="5f0c1-360">Palette de couleurs</span><span class="sxs-lookup"><span data-stu-id="5f0c1-360">Color Palette</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5f0c1-361">Choisissez l’un des carrés pour changer la couleur de ce carré.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-361">Choose one of the squares to change the color to that square.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="5f0c1-362">6</span><span class="sxs-lookup"><span data-stu-id="5f0c1-362">6</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="5f0c1-363">Hue</span><span class="sxs-lookup"><span data-stu-id="5f0c1-363">Hue</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="5f0c1-364">7</span><span class="sxs-lookup"><span data-stu-id="5f0c1-364">7</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="5f0c1-365">Opacity</span><span class="sxs-lookup"><span data-stu-id="5f0c1-365">Opacity</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="5f0c1-366">8</span><span class="sxs-lookup"><span data-stu-id="5f0c1-366">8</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="5f0c1-367">Commutateur valeur d’affichage</span><span class="sxs-lookup"><span data-stu-id="5f0c1-367">Display Value Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5f0c1-368">Bascule entre les représentations RGBA, HSLA et Hex de la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-368">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="5f0c1-369">9</span><span class="sxs-lookup"><span data-stu-id="5f0c1-369">9</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="5f0c1-370">S switcher de palette de couleurs</span><span class="sxs-lookup"><span data-stu-id="5f0c1-370">Color Palette Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5f0c1-371">Basculez entre la [palette de][MaterialDesignColorSystem]conception de matériaux, une palette personnalisée ou une palette de couleurs de page.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-371">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="5f0c1-372">DevTools génère la palette de couleurs de page en fonction des couleurs qu’il trouve dans vos feuilles de style.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-372">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  
   :::column-end:::
:::row-end:::  

#### <a name="sample-a-color-off-the-page-with-the-eyedropper"></a><span data-ttu-id="5f0c1-373">Exemple de couleur de la page avec le eyedropper</span><span class="sxs-lookup"><span data-stu-id="5f0c1-373">Sample a color off the page with the Eyedropper</span></span>  

<span data-ttu-id="5f0c1-374">Lorsque vous ouvrez le s **picker**de couleur, le **eyedropper** \( ![ Eyedropper ](../media/eyedropper-icon.msft.png) \) est sur par défaut.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-374">When you open the **Color Picker**, the **Eyedropper** \(![Eyedropper](../media/eyedropper-icon.msft.png)\) is on by default.</span></span>  <span data-ttu-id="5f0c1-375">Effectuer les actions suivantes pour modifier la couleur sélectionnée en une autre couleur sur la page.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-375">Complete the following actions to change the selected color to some other color on the page.</span></span>  

1.  <span data-ttu-id="5f0c1-376">Pointez sur la couleur cible dans la vue.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-376">Hover on the target color in the viewport.</span></span>  
1.  <span data-ttu-id="5f0c1-377">Choisissez de confirmer.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-377">Choose to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5f0c1-378">Dans la figure suivante, le s **sélectionneur** de couleurs affiche une valeur de couleur actuelle de , qui est proche `rgba(0,0,0,0.7)` du noir.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-378">In the following figure, the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="5f0c1-379">La couleur spécifique doit changer pour la version du noir qui est actuellement mise en surbrillant dans la vue une fois que vous l’avez choisie.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-379">The specific color should change to the version of black that is currently highlighted in the viewport after you chose it.</span></span>  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Utilisation du eyedropper" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       <span data-ttu-id="5f0c1-381">Utilisation du eyedropper</span><span class="sxs-lookup"><span data-stu-id="5f0c1-381">Using the Eyedropper</span></span>  
    :::image-end:::  
    
<!--todo:  add the section on the Angle clock section for What's New 88.  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="5f0c1-382">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="5f0c1-382">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Exécuter des commandes avec le menu de Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsCSSGetStarted]: ../css/index.md "Prise en main Avec l’affichage et la modification des | Documents Microsoft"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Ajouter un pseudo-état à une classe : Prise en main avec l’affichage et la modification des CSS | Documents Microsoft"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Afficher le CSS d’un élément : Prise en main avec l’affichage et la modification de CSS | Documents Microsoft"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Forcer Microsoft Edge devTools en mode Aperçu avant impression (type de média d’impression CSS) | Documents Microsoft"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#reformat-a-minified-javascript-file-with-pretty-print "Reformater un fichier JavaScript minifié avec une impression assez grande : utilisez le débogger | Documents Microsoft"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "Système de couleurs - Conception des matériaux"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "Modèle de zone | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Types de sélecteur : | MDN"  

> [!NOTE]
> <span data-ttu-id="5f0c1-392">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5f0c1-392">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5f0c1-393">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="5f0c1-393">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="5f0c1-395">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5f0c1-395">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  