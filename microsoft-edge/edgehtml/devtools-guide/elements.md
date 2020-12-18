---
description: Utilisez le panneau éléments pour inspecter les fichiers HTML, CSS, DOM et l’accessibilité de votre page.
title: DevTools-éléments
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, éléments, html, CSS, points d’arrêt DOM, événements, accessibilité
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 14052bc40b9f94e628f0b575ede6c1ca8ccf179a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232909"
---
# <span data-ttu-id="f454d-104">Éléments</span><span class="sxs-lookup"><span data-stu-id="f454d-104">Elements</span></span>

<span data-ttu-id="f454d-105">Le panneau **éléments** vous permet d’effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="f454d-105">The **Elements** panel helps you to:</span></span>

* <span data-ttu-id="f454d-106">[Identifier et modifier les éléments dans l’arborescence html](#html-tree-view) de la page active</span><span class="sxs-lookup"><span data-stu-id="f454d-106">[Identify and edit elements in the HTML tree](#html-tree-view) of the current page</span></span>
* <span data-ttu-id="f454d-107">[Inspecter et modifier des feuilles CSS](./elements/styles.md) sur la page, y compris des Pseudo-États et des Pseudo-éléments</span><span class="sxs-lookup"><span data-stu-id="f454d-107">[Inspect and modify CSS](./elements/styles.md) on the page, including pseudo-states and pseudo-elements</span></span>
* <span data-ttu-id="f454d-108">Présentation de [la disposition CSS et du style en cascade](./elements/computed.md) sur la page</span><span class="sxs-lookup"><span data-stu-id="f454d-108">[Understand the CSS layout and style cascade](./elements/computed.md) happening on the page</span></span>
* <span data-ttu-id="f454d-109">[Effectuer le suivi des gestionnaires d’événements malveillants](./elements/events.md) pour pouvoir les déboguer</span><span class="sxs-lookup"><span data-stu-id="f454d-109">[Track down rogue event handlers](./elements/events.md) so you can debug them</span></span>
* <span data-ttu-id="f454d-110">[Définir des points d’arrêt de débogage pour les modifications visuelles inattendues](./elements/dom-breakpoints.md) afin de sauter dans le code qui les entraîne</span><span class="sxs-lookup"><span data-stu-id="f454d-110">[Set debugging breakpoints for unexpected visual changes](./elements/dom-breakpoints.md) to jump into the code causing them</span></span>
* <span data-ttu-id="f454d-111">[Obtenez des informations détaillées sur les polices utilisées sur la page](./elements/fonts.md) et leur emplacement de chargement</span><span class="sxs-lookup"><span data-stu-id="f454d-111">[Get detailed information about the fonts used on the page](./elements/fonts.md) and where they're loading from</span></span>
* <span data-ttu-id="f454d-112">[Afficher votre page à partir du point de vue d’un lecteur d’écran](./elements/accessibility.md) pour vérifier et tester l’accessibilité</span><span class="sxs-lookup"><span data-stu-id="f454d-112">[View your page from a screen reader's point of view](./elements/accessibility.md) to verify and test accessibility</span></span> 
* <span data-ttu-id="f454d-113">[Passez en revue les modifications](./elements/changes.md) que vous apportez lors du débogage de l’interface utilisateur de votre page.</span><span class="sxs-lookup"><span data-stu-id="f454d-113">[Review a running diff of the CSS changes](./elements/changes.md) you make as you debug the UI of your page</span></span>

## <span data-ttu-id="f454d-114">Arborescence HTML</span><span class="sxs-lookup"><span data-stu-id="f454d-114">HTML tree view</span></span>

![Panneau éléments de DevTools Microsoft Edge](./media/elements.png)

1. <span data-ttu-id="f454d-116">\*\*\*\* `Ctrl+B` Pour rechercher un élément dans l' **arborescence html** , utilisez l’outil sélectionner un élément () et cliquez dessus dans la page.</span><span class="sxs-lookup"><span data-stu-id="f454d-116">Use the **Select element** (`Ctrl+B`) tool to locate an element in the **HTML tree view** by clicking on it in the page.</span></span>

2. <span data-ttu-id="f454d-117">Utilisez l’outil de **mise en surbrillance des éléments** `Ctrl+Shift+L` pour localiser un élément sur la page en pointant dessus dans l' **arborescence html**.</span><span class="sxs-lookup"><span data-stu-id="f454d-117">Use the **Element highlighting** (`Ctrl+Shift+L`) tool to locate an element on the page by hovering over it in the **HTML tree view**.</span></span>

3. <span data-ttu-id="f454d-118">Ouvrir l’outil de **sélection de couleurs** ( `Ctrl+K` ) pour afficher une liste des couleurs utilisées dans la page active.</span><span class="sxs-lookup"><span data-stu-id="f454d-118">Open the **Color picker** (`Ctrl+K`) tool to see a list of the colors in use on the current page.</span></span> <span data-ttu-id="f454d-119">Pour plus d’informations, cliquez sur une couleur de la liste, puis sur couleur de nuance, de saturation et de luminosité.</span><span class="sxs-lookup"><span data-stu-id="f454d-119">Clicking on a color on the list will provide further details (Hue, Saturation, Lightness, Alpha).</span></span> <span data-ttu-id="f454d-120">Le *Sélecteur de couleur* s’ouvre également lorsque vous cliquez sur le carré de couleur en regard d’une valeur de couleur dans le volet **styles** , ce qui vous permet de modifier la couleur d’un élément de page et d’afficher immédiatement les résultats.</span><span class="sxs-lookup"><span data-stu-id="f454d-120">The *Color picker* also opens when you click on the colored square next to a color value in the **Styles** pane, allowing you to edit the color of a page element and immediately see the results.</span></span>

4. <span data-ttu-id="f454d-121">Le bouton **arborescence d’accessibilité** ( `Ctrl+Shift+A` ) permet d’ouvrir le volet de l' [arborescence d’accessibilité](./elements/accessibility.md) présentant la structure de votre page telle qu’elle apparaîtra dans une technologie d’assistance, telle que le [narrateur Windows](https://support.microsoft.com/help/22798/windows-10-narrator-get-started) lecteur d’écran.</span><span class="sxs-lookup"><span data-stu-id="f454d-121">The **Accessibility tree** (`Ctrl+Shift+A`) button will open the [Accessibility tree](./elements/accessibility.md) pane showing the structure of your page as it would appear to an assistive technology, such as the [Windows Narrator](https://support.microsoft.com/help/22798/windows-10-narrator-get-started) screenreader.</span></span>

5. <span data-ttu-id="f454d-122">Vous pouvez également **Rechercher** ( `Ctrl+F` ) un élément dans l’arborescence html en recherchant son nom de balise, ses attributs ou son contenu de texte.</span><span class="sxs-lookup"><span data-stu-id="f454d-122">You can also **Find** (`Ctrl+F`) an element in the HTML tree view by searching for its tag name, attributes, or text content.</span></span>

### <span data-ttu-id="f454d-123">Modification des éléments</span><span class="sxs-lookup"><span data-stu-id="f454d-123">Editing elements</span></span>

<span data-ttu-id="f454d-124">Vous pouvez modifier un élément en cliquant dessus avec le bouton droit dans l’arborescence HTML et en sélectionnant **modifier en tant que html** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="f454d-124">You can edit an element by right-clicking on it within the HTML tree view and selecting **Edit as HTML** from the context menu.</span></span> <span data-ttu-id="f454d-125">Le menu contextuel fournit également des options permettant de supprimer, de couper, de copier, de coller, de *définir des Pseudo*-classes CSS (*: actif*, *: Focus*, *: hover*</span><span class="sxs-lookup"><span data-stu-id="f454d-125">The context menu also provides options to delete, cut, copy, paste, set CSS pseudo-classes (*:active*, *:focus*, *:hover*, *:visited*) and add attributes.</span></span> <span data-ttu-id="f454d-126">Une autre méthode de modification d’un attribut et/ou sa valeur est de double-cliquer sur celui-ci dans l’arborescence HTML.</span><span class="sxs-lookup"><span data-stu-id="f454d-126">Another way to edit an attribute and/or its value is to double-click it from the HTML tree view.</span></span>

![Menu contextuel de l’affichage d’arborescence HTML](./media/elements_html_tree_context.png)

> [!NOTE]
> <span data-ttu-id="f454d-128">La modification de l’arborescence HTML n’affecte pas le balisage source sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="f454d-128">Editing the HTML tree does not affect the underlying source markup.</span></span> <span data-ttu-id="f454d-129">L’actualisation de la page annule les modifications et rend uniquement la mise en page déterminée par la source de la page.</span><span class="sxs-lookup"><span data-stu-id="f454d-129">Refreshing the page will revert your changes and render only the layout determined by the page source.</span></span> <span data-ttu-id="f454d-130">Vous pouvez **copier** votre code html modifié dans le presse-papiers en cliquant avec le bouton droit sur l’élément souhaité (ou l' `html` élément global, si vous voulez la page entière) pour ouvrir le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="f454d-130">You can **Copy** your modified HTML to the clipboard by right-clicking the desired element (or the global `html` element, if you want the entire page) to open up the context menu.</span></span> <span data-ttu-id="f454d-131">(Les options**couper** et **coller** sont également disponibles).</span><span class="sxs-lookup"><span data-stu-id="f454d-131">(**Cut** and **Paste** options are also available).</span></span>

<span data-ttu-id="f454d-132">Dans le volet [styles](./elements/styles.md) , vous pouvez également ajouter/supprimer/modifier des Pseudo-États CSS et des Pseudo-éléments.</span><span class="sxs-lookup"><span data-stu-id="f454d-132">From the [Styles](./elements/styles.md) pane you can also add/delete/edit CSS pseudo-states and pseudo-elements.</span></span>

## <span data-ttu-id="f454d-133">Volets d’outils</span><span class="sxs-lookup"><span data-stu-id="f454d-133">Tool Panes</span></span>

<span data-ttu-id="f454d-134">Une fois que vous avez sélectionné un élément de page intéressant, vous pouvez utiliser les volets d’outils pour examiner de nouveau ses différentes styles et propriétés d’accessibilité, afficher ses écouteurs d’événements et définir des points d’arrêt de mutation DOM.</span><span class="sxs-lookup"><span data-stu-id="f454d-134">Once you have selected a page element of interest, you can use the tool panes to further inspect its different styles and accessibility properties, view its event listeners, and set DOM mutation breakpoints.</span></span>

![Volets outils du panneau éléments](./media/elements_toolpanes.png)

1. <span data-ttu-id="f454d-136">[**Styles**](./elements/styles.md): styles actuellement appliqués organisés par feuille de style</span><span class="sxs-lookup"><span data-stu-id="f454d-136">[**Styles**](./elements/styles.md): Currently applied styles organized by stylesheet</span></span>

2. <span data-ttu-id="f454d-137">[**Calculs**](./elements/computed.md): styles actuellement appliqués organisés par des attributs CSS</span><span class="sxs-lookup"><span data-stu-id="f454d-137">[**Computed**](./elements/computed.md): Currently applied styles organized by CSS attributes</span></span>

3. <span data-ttu-id="f454d-138">[**Événements**](./elements/events.md): écouteurs d’événements enregistrés sur l’élément actif et éléments ancêtres</span><span class="sxs-lookup"><span data-stu-id="f454d-138">[**Events**](./elements/events.md): Event listeners registered on the current element and ancestor elements</span></span>

4. <span data-ttu-id="f454d-139">[**Points d’arrêt DOM**](./elements/dom-breakpoints.md): points d’arrêt de mutation DOM</span><span class="sxs-lookup"><span data-stu-id="f454d-139">[**DOM breakpoints**](./elements/dom-breakpoints.md): DOM Mutation Breakpoints</span></span> 

5. <span data-ttu-id="f454d-140">[**Polices**](./elements/fonts.md): polices appliquées actuellement pour un élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="f454d-140">[**Fonts**](./elements/fonts.md): Currently applied fonts for a selected element</span></span>

6. <span data-ttu-id="f454d-141">[**Accessibilité**](./elements/accessibility.md): propriétés d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="f454d-141">[**Accessibility**](./elements/accessibility.md):  Accessibility properties</span></span>

7. <span data-ttu-id="f454d-142">[**Modifications**](./elements/changes.md): modifications CSS effectuées lors de la session de diagnostic</span><span class="sxs-lookup"><span data-stu-id="f454d-142">[**Changes**](./elements/changes.md): CSS changes made during diagnostic session</span></span>  

## <span data-ttu-id="f454d-143">Raccourcis</span><span class="sxs-lookup"><span data-stu-id="f454d-143">Shortcuts</span></span>

| <span data-ttu-id="f454d-144">Action</span><span class="sxs-lookup"><span data-stu-id="f454d-144">Action</span></span>               | <span data-ttu-id="f454d-145">Raccourci</span><span class="sxs-lookup"><span data-stu-id="f454d-145">Shortcut</span></span>               |
|:---------------------|:-----------------------|
| <span data-ttu-id="f454d-146">Panneau éléments</span><span class="sxs-lookup"><span data-stu-id="f454d-146">Elements panel</span></span>       | `Ctrl` + `1`           |
| <span data-ttu-id="f454d-147">Mise en surbrillance des éléments</span><span class="sxs-lookup"><span data-stu-id="f454d-147">Element highlighting</span></span> | `Ctrl` + `Shift` + `L` |
| <span data-ttu-id="f454d-148">Sélectionner un élément</span><span class="sxs-lookup"><span data-stu-id="f454d-148">Select element</span></span>       | `Ctrl` + `B`           |
| <span data-ttu-id="f454d-149">Sélecteur de couleurs</span><span class="sxs-lookup"><span data-stu-id="f454d-149">Color picker</span></span>         | `Ctrl` + `K`           |
| <span data-ttu-id="f454d-150">Arborescence d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="f454d-150">Accessibility tree</span></span>   | `Ctrl` + `Shift` + `A` |
