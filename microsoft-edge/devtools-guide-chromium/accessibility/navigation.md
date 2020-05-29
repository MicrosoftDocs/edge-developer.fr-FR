---
title: Navigation dans Microsoft Edge DevTools avec la technologie d’assistance
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 5de27e46d20957a1be79f72cf36074291566e6e5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564978"
---
<!-- Copyright Rob Dodson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="83664-103">Navigation dans Microsoft Edge DevTools avec la technologie d’assistance</span><span class="sxs-lookup"><span data-stu-id="83664-103">Navigate Microsoft Edge DevTools With Assistive Technology</span></span>   



<span data-ttu-id="83664-104">Ce guide a pour but d’aider les utilisateurs qui s’appuient essentiellement sur la technologie d’assistance comme les lecteurs d’écran à l’accès et à l’utilisation de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="83664-104">This guide aims to help users who primarily rely on assistive technology like screen readers access and use Microsoft Edge DevTools.</span></span>  <span data-ttu-id="83664-105">Microsoft Edge DevTools est une suite d’outils de développement Web intégrés au navigateur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="83664-105">Microsoft Edge DevTools is a suite of web developer tools built into the Microsoft Edge browser.</span></span>  <!--See [Accessibility Reference][DevtoolsAccessibilityReference] if you are looking for DevTools features related to improving the accessibility of a web page.  -->

<!--todo: add edge devtools index section when available  -->  
<!--todo: add reference (Accessibility Reference) section when available  -->  

<span data-ttu-id="83664-106">L’accessibilité de DevTools est une opération en cours.</span><span class="sxs-lookup"><span data-stu-id="83664-106">The accessibility of DevTools is a work-in-progress.</span></span>  <span data-ttu-id="83664-107">Certains panneaux et onglets fonctionnent mieux avec les technologies d’assistance.</span><span class="sxs-lookup"><span data-stu-id="83664-107">Some panels and tabs work better with assistive technology than others.</span></span>  <span data-ttu-id="83664-108">Ce guide vous guide à travers les écrans qui sont les plus accessibles et met en surbrillance des problèmes spécifiques que vous pouvez rencontrer.</span><span class="sxs-lookup"><span data-stu-id="83664-108">This guide walks you through the panels which are the most accessible and highlights specific issues you may encounter along the way.</span></span>  

## <span data-ttu-id="83664-109">Présentation</span><span class="sxs-lookup"><span data-stu-id="83664-109">Overview</span></span>   

<span data-ttu-id="83664-110">Avant de commencer, il est utile d’avoir un modèle mental illustrant la structure de l’interface utilisateur d’DevTools.</span><span class="sxs-lookup"><span data-stu-id="83664-110">Before starting, it helps to have a mental model of how the DevTools UI is structured.</span></span>  <span data-ttu-id="83664-111">DevTools est divisé en une série de panneaux organisés au sein d’un [tableau `tablist` Aria ][W3CWaiAriaTablist].</span><span class="sxs-lookup"><span data-stu-id="83664-111">DevTools is divided into a series of panels which are organized into an [ARIA `tablist`][W3CWaiAriaTablist].</span></span>  

<span data-ttu-id="83664-112">Exemple:</span><span class="sxs-lookup"><span data-stu-id="83664-112">For example:</span></span>  

*   <span data-ttu-id="83664-113">Le panneau **éléments** vous permet d’afficher et de modifier des nœuds DOM ou [CSS] [DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="83664-113">The **Elements** panel lets you view and change DOM nodes or [CSS][DevtoolsCssIndex].</span></span>  
*   <span data-ttu-id="83664-114">**[DevtoolsConsoleIndex** ] permet de lire les journaux JavaScript et les objets de modification dynamique.</span><span class="sxs-lookup"><span data-stu-id="83664-114">The [**Console** panel][DevtoolsConsoleIndex] lets you read JavaScript logs and live edit objects.</span></span>  

<!--todo:  add dom nodes (dom nodes) section when available  -->  

<span data-ttu-id="83664-115">Dans la zone de contenu de chaque panneau, il existe un certain nombre d’outils différents, souvent désignés sous le nom d’onglets ou de volets dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="83664-115">Within the content area of each panel, there are a number of different tools, often referred to as tabs or panes in the documentation.</span></span>  
<span data-ttu-id="83664-116">Par exemple, le panneau **éléments** contient d’autres onglets pour inspecter les écouteurs d’événements, l’arborescence d’accessibilité, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="83664-116">For instance, the **Elements** panel contains additional tabs to inspect event listeners, the accessibility tree, and much more.</span></span>  <span data-ttu-id="83664-117">La distinction entre les onglets et les volets est un peu arbitraire.</span><span class="sxs-lookup"><span data-stu-id="83664-117">The distinction between tabs and panes is somewhat arbitrary.</span></span>  <span data-ttu-id="83664-118">La seule raison pour laquelle il est possible que vous voyiez un terme ou l’autre consiste à assurer une cohérence avec le reste de la documentation relative au DevTools officiel.</span><span class="sxs-lookup"><span data-stu-id="83664-118">The only reason you may see one term or the other is to maintain consistency with the rest of the official DevTools documentation.</span></span>  

## <span data-ttu-id="83664-119">Raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="83664-119">Keyboard shortcuts</span></span>   

<span data-ttu-id="83664-120">Les raccourcis clavier [DevTools] [DevtoolsShortcuts] sont des Cheatsheet utiles.</span><span class="sxs-lookup"><span data-stu-id="83664-120">The [DevTools Keyboard Shortcuts reference][DevtoolsShortcuts] is a helpful cheatsheet.</span></span>  <span data-ttu-id="83664-121">Prenez soin de la marquer et de vous y référer lorsque vous explorez les différents panneaux.</span><span class="sxs-lookup"><span data-stu-id="83664-121">Be sure to bookmark it and refer back to it as you explore the different panels.</span></span>  

## <span data-ttu-id="83664-122">Ouvrir DevTools</span><span class="sxs-lookup"><span data-stu-id="83664-122">Open DevTools</span></span>   

<span data-ttu-id="83664-123">Pour commencer, consultez la [ouvrir Microsoft Edge DevTools] [DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="83664-123">To get started, read through [Open Microsoft Edge DevTools][DevtoolsOpen].</span></span>  <span data-ttu-id="83664-124">Il existe plusieurs façons d’ouvrir DevTools, à l’aide des raccourcis clavier ou des éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="83664-124">There are a number of ways to open DevTools, either through keyboard shortcuts or menu items.</span></span>  

## <span data-ttu-id="83664-125">Naviguer entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="83664-125">Navigate between panels</span></span>   

### <span data-ttu-id="83664-126">Navigation à l’aide du clavier</span><span class="sxs-lookup"><span data-stu-id="83664-126">Navigate by keyboard</span></span>   

*   <span data-ttu-id="83664-127">Avec devtools ouvert, appuyez sur `Control` + `]` \ (Windows \) ou `Command` + `]` \ (MacOS \) pour cibler le panneau suivant.</span><span class="sxs-lookup"><span data-stu-id="83664-127">With DevTools open, press `Control`+`]` \(Windows\) or `Command`+`]` \(macOS\) to focus the next panel.</span></span>  
*   <span data-ttu-id="83664-128">`Control` + `[` Pour sélectionner le panneau précédent, appuyez sur \ (Windows \) ou `Command` + `[` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="83664-128">Press `Control`+`[` \(Windows\) or `Command`+`[` \(macOS\) to focus the previous panel.</span></span>  
*   <span data-ttu-id="83664-129">Il est également possible d’utiliser les `Shift` + `Tab` touches de direction pour déplacer le focus sur l’élément [ `tablist` Aria][W3CWaiAriaTablist] d’un panneau et utiliser les touches de direction pour modifier les panneaux, même s’il est plus rapide d’utiliser les raccourcis mentionnés précédemment.</span><span class="sxs-lookup"><span data-stu-id="83664-129">It is also possible to use `Shift`+`Tab` to move focus into the [ARIA `tablist`][W3CWaiAriaTablist] of a panel and use the arrow keys to change panels, though it may be faster to use the previously mentioned shortcuts.</span></span>  

#### <span data-ttu-id="83664-130">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="83664-130">Known issues</span></span>   

*   <span data-ttu-id="83664-131">Certains panneaux, tels que les panneaux **console** et **performance** , peuvent déplacer le focus dans la zone de contenu dès leur activation.</span><span class="sxs-lookup"><span data-stu-id="83664-131">Some panels, such as the **Console** and **Performance** panels, may move focus into their content area as soon as they are activated.</span></span>  <span data-ttu-id="83664-132">Cela risque de compliquer la navigation à l’aide des touches de direction.</span><span class="sxs-lookup"><span data-stu-id="83664-132">This may make navigating by arrow keys difficult.</span></span>  
*   <span data-ttu-id="83664-133">Le nom du panneau sélectionné est annoncé, mais uniquement après avoir lu le contenu prioritaire dans le panneau.</span><span class="sxs-lookup"><span data-stu-id="83664-133">The name of the selected panel is announced, but only after it has read the focused content in the panel.</span></span>  <span data-ttu-id="83664-134">C’est aussi facile à manquer.</span><span class="sxs-lookup"><span data-stu-id="83664-134">This may make it very easy to miss.</span></span>  

### <span data-ttu-id="83664-135">Navigation à l’aide du menu de commandes</span><span class="sxs-lookup"><span data-stu-id="83664-135">Navigate by Command Menu</span></span>   

<span data-ttu-id="83664-136">Pour vous concentrer sur un panneau spécifique, utilisez le [**menu de commandes**] [DevtoolsCommandMenuIndex]:</span><span class="sxs-lookup"><span data-stu-id="83664-136">To focus a specific panel, use the [**Command Menu**][DevtoolsCommandMenuIndex]:</span></span>  

1.  <span data-ttu-id="83664-137">Avec devtools ouvert, appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="83664-137">With DevTools open, press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    <span data-ttu-id="83664-138">Le **menu de commandes** est un élément ComboBox de saisie semi-automatique de recherche floue.</span><span class="sxs-lookup"><span data-stu-id="83664-138">The **Command Menu** is a fuzzy search autocomplete combobox.</span></span>  
1.  <span data-ttu-id="83664-139">Entrez le nom du panneau que vous voulez ouvrir, puis utilisez le `Down Arrow` clavier visuel pour accéder à l’option appropriée.</span><span class="sxs-lookup"><span data-stu-id="83664-139">Type the name of the panel you want to open, then use the `Down Arrow` on the keyboard to navigate to the correct option.</span></span>  
1.  <span data-ttu-id="83664-140">Appuyez `Enter` pour exécuter une commande.</span><span class="sxs-lookup"><span data-stu-id="83664-140">Press `Enter` to run a command.</span></span>  

<span data-ttu-id="83664-141">Par exemple, pour ouvrir le panneau **éléments** :</span><span class="sxs-lookup"><span data-stu-id="83664-141">For example, to open the **Elements** panel:</span></span>  

1.  <span data-ttu-id="83664-142">Ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="83664-142">Open the **Command Menu**.</span></span>  
1.  <span data-ttu-id="83664-143">Tapez `E` ensuite `L` .</span><span class="sxs-lookup"><span data-stu-id="83664-143">Type `E` then `L`.</span></span>  <span data-ttu-id="83664-144">Option **panneau > afficher les éléments** sélectionnée</span><span class="sxs-lookup"><span data-stu-id="83664-144">The **Panel > Show Elements** option is selected.</span></span>  
1.  <span data-ttu-id="83664-145">Appuyez `Enter` pour exécuter la commande qui ouvre le panneau.</span><span class="sxs-lookup"><span data-stu-id="83664-145">Press `Enter` to run the command that opens the panel.</span></span>  

<span data-ttu-id="83664-146">L’ouverture d’un panneau permet de transférer le focus sur le contenu du panneau.</span><span class="sxs-lookup"><span data-stu-id="83664-146">Opening a panel this way directs focus to the contents of the panel.</span></span>  <span data-ttu-id="83664-147">Dans le cas du panneau d' **éléments** , le focus est déplacé vers l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="83664-147">In the case of the **Elements** panel, focus moves into the **DOM Tree**.</span></span>  

## <span data-ttu-id="83664-148">Panneau éléments</span><span class="sxs-lookup"><span data-stu-id="83664-148">Elements panel</span></span>   

### <span data-ttu-id="83664-149">Inspecter un élément sur la page</span><span class="sxs-lookup"><span data-stu-id="83664-149">Inspect an element on the page</span></span>   

1.  <span data-ttu-id="83664-150">Naviguez jusqu’à l’élément que vous voulez inspecter à l’aide du curseur dans le lecteur d’écran.</span><span class="sxs-lookup"><span data-stu-id="83664-150">Navigate to the element you want to inspect using the cursor in the screen reader.</span></span>  
1.  <span data-ttu-id="83664-151">Simulez un clic droit sur l’élément pour ouvrir le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="83664-151">Simulate a right-mouse click on the element to open the context menu.</span></span>  
1.  <span data-ttu-id="83664-152">Sélectionnez l’option **inspecter** .</span><span class="sxs-lookup"><span data-stu-id="83664-152">Choose the **Inspect** option.</span></span>  <span data-ttu-id="83664-153">Cette action ouvre le panneau d' **éléments** et le centre de l’élément dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="83664-153">This opens the **Elements** panel and focuses the element in the **DOM Tree**.</span></span>  

<!--todo:  add dom nodes (elements pane) section when available  -->  

<span data-ttu-id="83664-154">L' **arborescence DOM** est disposée en tant qu' [Aria `tree` ][W3CWaiAriaTree].</span><span class="sxs-lookup"><span data-stu-id="83664-154">The **DOM Tree** is laid out as an [ARIA `tree`][W3CWaiAriaTree].</span></span>  <!--See [Navigate the **DOM Tree** with a keyboard][DevtoolsDomIndexNavigateDomTreeKeyboard] for an example.  -->  

<!--todo: add dom index navigation tree section then available  -->

### <span data-ttu-id="83664-155">Copiez le code d’un élément dans l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="83664-155">Copy the code for an element in the DOM Tree</span></span>   

1.  <span data-ttu-id="83664-156">Avec le focus sur un nœud dans l' **arborescence DOM**, afficher le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="83664-156">With focus on a node in the **DOM Tree**, bring up the right-click context menu.</span></span>  
1.  <span data-ttu-id="83664-157">Développez l’option **copier** .</span><span class="sxs-lookup"><span data-stu-id="83664-157">Expand the **Copy** option.</span></span>  
1.  <span data-ttu-id="83664-158">Sélectionnez **Copy outerHTML**.</span><span class="sxs-lookup"><span data-stu-id="83664-158">Select **Copy outerHTML**.</span></span>  

#### <span data-ttu-id="83664-159">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="83664-159">Known issues</span></span>   

*   <span data-ttu-id="83664-160">Dans le cas d’une **copie outerHTML** , le nœud actif ne doit pas être sélectionné, mais au lieu de cela, il sélectionne le nœud parent.</span><span class="sxs-lookup"><span data-stu-id="83664-160">**Copy outerHTML** often does not select the current node but instead selects the parent node.</span></span>  <span data-ttu-id="83664-161">Toutefois, le contenu de l’élément doit toujours figurer dans le outerHTML copié.</span><span class="sxs-lookup"><span data-stu-id="83664-161">However, the contents of the element should still be in the copied outerHTML.</span></span>  

### <span data-ttu-id="83664-162">Modifier les attributs d’un élément dans l’arborescence DOM</span><span class="sxs-lookup"><span data-stu-id="83664-162">Modify the attributes of an element in the DOM Tree</span></span>   

*   <span data-ttu-id="83664-163">Avec le focus sur un nœud dans l' **arborescence DOM**, appuyez sur `Enter` pour le rendre modifiable.</span><span class="sxs-lookup"><span data-stu-id="83664-163">With focus on a node in the **DOM Tree**, press `Enter` to make it editable.</span></span>  
*   <span data-ttu-id="83664-164">Appuyez `Tab` pour vous déplacer entre les valeurs d’attribut.</span><span class="sxs-lookup"><span data-stu-id="83664-164">Press `Tab` to move between attribute values.</span></span>  <span data-ttu-id="83664-165">Lorsque vous entendez «espace» vous vous trouvez à l’intérieur d’une entrée de texte vide et êtes en mesure de taper une nouvelle valeur d’attribut.</span><span class="sxs-lookup"><span data-stu-id="83664-165">When you hear "space" you are inside of an empty text input and are able to type a new attribute value.</span></span>  
*   <span data-ttu-id="83664-166">`Control` + `Enter` `Command` + `Enter` Pour accepter la modification et entendre tout le contenu de l’élément, appuyez sur \ (Windows \) ou \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="83664-166">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to accept the change and hear the entire contents of the element.</span></span>  

#### <span data-ttu-id="83664-167">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="83664-167">Known issues</span></span>   

*   <span data-ttu-id="83664-168">Lorsque vous tapez dans la saisie de texte, vous ne recevez aucune commentaires.</span><span class="sxs-lookup"><span data-stu-id="83664-168">When you type into the text input you get no feedback.</span></span>  <span data-ttu-id="83664-169">Si vous faites une faute de frappe et que vous utilisez les touches de direction pour explorer votre entrée, vous ne recevez pas de commentaires.</span><span class="sxs-lookup"><span data-stu-id="83664-169">If you make a typo and use the arrow keys to explore your input you also get no feedback.</span></span>  <span data-ttu-id="83664-170">Le moyen le plus simple de vérifier votre tâche est d’accepter la modification, puis de surveiller l’intégralité de l’élément.</span><span class="sxs-lookup"><span data-stu-id="83664-170">The easiest way to check your work is to accept the change, then listen for the entire element to be announced.</span></span>  

### <span data-ttu-id="83664-171">Modifier le code HTML d’un élément dans l’arborescence DOM</span><span class="sxs-lookup"><span data-stu-id="83664-171">Edit the HTML of an element in the DOM Tree</span></span>   

*   <span data-ttu-id="83664-172">Avec le focus sur un nœud dans l' **arborescence DOM**, appuyez sur `Enter` pour le rendre modifiable.</span><span class="sxs-lookup"><span data-stu-id="83664-172">With focus on a node in the **DOM Tree**, press `Enter` to make it editable.</span></span>  
*   <span data-ttu-id="83664-173">Appuyez `Tab` pour vous déplacer entre les valeurs d’attribut.</span><span class="sxs-lookup"><span data-stu-id="83664-173">Press `Tab` to move between attribute values.</span></span>  <span data-ttu-id="83664-174">Lorsque vous entendez le nom de l’élément, par exemple, «H2», vous vous trouvez à l’intérieur d’une entrée de texte et vous pouvez modifier le type de l’élément.</span><span class="sxs-lookup"><span data-stu-id="83664-174">When you hear the name of the element, for instance, "h2", you are inside of a text input and may change the type of the element.</span></span>  
*   <span data-ttu-id="83664-175">Appuyez sur `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) pour accepter la modification.</span><span class="sxs-lookup"><span data-stu-id="83664-175">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to accept the change.</span></span>  

<span data-ttu-id="83664-176">Par exemple, le fait de taper `h3` et d’appuyer sur `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) change les balises de début et de fin de l’élément en `h3` .</span><span class="sxs-lookup"><span data-stu-id="83664-176">For example, typing `h3` and pressing `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) changes the start and end tags of the element to `h3`.</span></span>  

## <span data-ttu-id="83664-177">Onglets du panneau éléments</span><span class="sxs-lookup"><span data-stu-id="83664-177">Elements panel tabs</span></span>   

<span data-ttu-id="83664-178">Le panneau **éléments** contient d’autres onglets permettant d’inspecter les éléments tels que la feuille de style CSS appliquée à un élément ou l’emplacement approprié dans l’arborescence accessibilité.</span><span class="sxs-lookup"><span data-stu-id="83664-178">The **Elements** panel contains additional tabs for inspecting things like the CSS applied to an element or the relevant place in the accessibility tree.</span></span>  

*   <span data-ttu-id="83664-179">Avec le focus sur un nœud dans l' **arborescence DOM**, appuyez `Tab` jusqu’à ce que vous entendiez que le volet **styles** est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="83664-179">With focus on a node in the **DOM Tree**, press `Tab` until you hear that the **Styles** pane is selected.</span></span>  
*   <span data-ttu-id="83664-180">Utilisez la `Right Arrow` pour explorer d’autres onglets disponibles.</span><span class="sxs-lookup"><span data-stu-id="83664-180">Use the `Right Arrow` to explore other available tabs.</span></span>  

<span data-ttu-id="83664-181">L' **arborescence DOM** transforme les éléments à l’aide d' `href` attributs en liens pouvant être actifs; il est donc possible que vous deviez appuyer `Tab` plusieurs fois pour accéder au volet **styles** .</span><span class="sxs-lookup"><span data-stu-id="83664-181">The **DOM Tree** turns elements with `href` attributes into focusable links, so you may need to press `Tab` more than once to reach the **Styles** pane.</span></span>  

### <span data-ttu-id="83664-182">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="83664-182">Known issues</span></span>   

<span data-ttu-id="83664-183">Les onglets de **Propriétés** et de points de passe **DOM** ne sont pas accessibles via le clavier.</span><span class="sxs-lookup"><span data-stu-id="83664-183">The **DOM Breakpoints** and **Properties** tabs are not keyboard accessible.</span></span>  

### <span data-ttu-id="83664-184">Volet styles</span><span class="sxs-lookup"><span data-stu-id="83664-184">Styles pane</span></span>   

<span data-ttu-id="83664-185">Dans le volet **styles** , recherchez des contrôles pour le filtrage des styles, le basculement vers les États des éléments \ (par exemple [`:active`][MDNActive] et [`:focus`][MDNFocus] \), le basculement entre les classes et l’ajout de nouvelles classes.</span><span class="sxs-lookup"><span data-stu-id="83664-185">In the **Styles** pane find controls for filtering styles, toggling element states \(such as [`:active`][MDNActive] and [`:focus`][MDNFocus]\), toggling classes, and adding new classes.</span></span>  <span data-ttu-id="83664-186">Il existe également un outil d’inspection des styles puissant permettant d’explorer et de modifier les styles actuellement appliqués à l’élément qui a le focus dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="83664-186">There is also a powerful style inspection tool to explore and modify styles currently applied to the element that is in focus in the **DOM Tree**.</span></span>  

<span data-ttu-id="83664-187">Le principal concept à comprendre à propos du volet **styles** est qu’il affiche uniquement les styles du nœud actuellement sélectionné dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="83664-187">The key concept to understand about the **Styles** pane is that it only shows styles for the currently-selected node in the **DOM Tree**.</span></span>  <span data-ttu-id="83664-188">Par exemple, supposons que vous ayez vérifié les styles d’un `<header>` nœud et que vous voulez maintenant consulter les styles d’un `<footer>` nœud.</span><span class="sxs-lookup"><span data-stu-id="83664-188">For example, suppose you are done inspecting the styles of a `<header>` node, and now you want to look at the styles for a `<footer>` node.</span></span>  <span data-ttu-id="83664-189">Pour ce faire, vous devez d’abord sélectionner le `<footer>` nœud dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="83664-189">To do that, you first need to select the `<footer>` node in the **DOM Tree**.</span></span>  <span data-ttu-id="83664-190">Vous constaterez peut-être qu’il est plus rapide d’utiliser le flux de travail [Inspect](#inspect-an-element-on-the-page) pour examiner un nœud qui se trouve à proximité du `footer` nœud \ (par exemple, un lien dans le pied de page \), qui Centre l' **arborescence DOM**, puis utilisez votre clavier pour accéder au nœud exact qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="83664-190">You may find it faster to use the [Inspect](#inspect-an-element-on-the-page) workflow to inspect a node that is in the general vicinity of the `footer` node \(such as a link within the footer\), which focuses the **DOM Tree**, and then use your keyboard to navigate to the exact node in which you are interested.</span></span>  

#### <span data-ttu-id="83664-191">Naviguer dans le volet styles</span><span class="sxs-lookup"><span data-stu-id="83664-191">Navigate the Styles pane</span></span>   

<span data-ttu-id="83664-192">Dans la mesure où tous les outils de style se connectent d’une façon ou d’une autre dans le volet **styles** , il est préférable d’abord de mettre en avant ce outil.</span><span class="sxs-lookup"><span data-stu-id="83664-192">Because all of the style tools connect in one way or another back to the **Styles** pane, it makes sense to master this tool first.</span></span>  

*   <span data-ttu-id="83664-193">Le focus étant placé sur le volet **styles** , appuyez sur `Tab` pour déplacer le focus à l’intérieur et explorer le contenu.</span><span class="sxs-lookup"><span data-stu-id="83664-193">With focus on the **Styles** pane, press `Tab` to move focus inside and explore the contents.</span></span>  
*   <span data-ttu-id="83664-194">Appuyez sur `Tab` jusqu’à ce que le premier style devienne actif.</span><span class="sxs-lookup"><span data-stu-id="83664-194">Press `Tab` until the first style becomes active.</span></span>  <span data-ttu-id="83664-195">Si vous utilisez un lecteur d’écran, le premier style est annoncé comme suit: «élément. style {} ».</span><span class="sxs-lookup"><span data-stu-id="83664-195">If you are using a screen reader this first style is announced as "element.style {}".</span></span>  
*   <span data-ttu-id="83664-196">Appuyez `Down Arrow` pour parcourir la liste des styles par ordre de spécificité.</span><span class="sxs-lookup"><span data-stu-id="83664-196">Press `Down Arrow` to navigate the list of styles in order of specificity.</span></span>  <span data-ttu-id="83664-197">Un lecteur d’écran annonce chaque style en commençant par le nom du fichier CSS, le numéro de ligne sur lequel apparaît le style et le nom du style.</span><span class="sxs-lookup"><span data-stu-id="83664-197">A screen reader announces each style starting with the name of the CSS file, the line number on which the style appears, and the name of the style.</span></span>  <span data-ttu-id="83664-198">Par exemple: "main. CSS: 233. card__img {} "</span><span class="sxs-lookup"><span data-stu-id="83664-198">For example: "main.css:233 .card__img {}"</span></span>  
*   <span data-ttu-id="83664-199">`Enter`Pour plus d’informations, appuyez sur pour vérifier un style.</span><span class="sxs-lookup"><span data-stu-id="83664-199">Press `Enter` to inspect a style in more detail.</span></span>  <span data-ttu-id="83664-200">Le focus commence sur une version modifiable du nom du style.</span><span class="sxs-lookup"><span data-stu-id="83664-200">Focus begins on an editable version of the style name.</span></span>  
*   <span data-ttu-id="83664-201">Appuyez `Tab` pour passer d’une version éditable à une autre de chaque propriété CSS et leurs valeurs correspondantes.</span><span class="sxs-lookup"><span data-stu-id="83664-201">Press `Tab` to move between editable versions of each CSS property and their corresponding values.</span></span>  <span data-ttu-id="83664-202">À la fin de chaque bloc de style s’agit d’un champ de texte modifiable vierge que vous pouvez utiliser pour ajouter des propriétés CSS supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="83664-202">At the end of each style block is a blank editable text field which you may use to add additional CSS properties.</span></span>  
*   <span data-ttu-id="83664-203">Vous pouvez continuer d’appuyer sur `Tab` pour parcourir la liste des styles ou appuyer sur `Escape` pour quitter ce mode et revenir à la navigation à l’aide des touches de direction.</span><span class="sxs-lookup"><span data-stu-id="83664-203">You may continue to press `Tab` to move through the list of styles, or press `Escape` to exit this mode and go back to navigating by arrow keys.</span></span>  

<span data-ttu-id="83664-204">Assurez-vous de lire le Guide [Guide de référence clavier du volet styles] [DevtoolsShortcutsStylesPaneKeyboard] pour afficher d’autres raccourcis.</span><span class="sxs-lookup"><span data-stu-id="83664-204">Be sure to read through the [Styles pane keyboard reference][DevtoolsShortcutsStylesPaneKeyboard] for additional shortcuts.</span></span>  

##### <span data-ttu-id="83664-205">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="83664-205">Known Issues</span></span>   

*   <span data-ttu-id="83664-206">Si vous utilisez le champ de texte modifiable **filtre** , vous n’êtes plus en mesure de parcourir la liste des styles.</span><span class="sxs-lookup"><span data-stu-id="83664-206">If you use the **Filter** editable text field, you are no longer be able to navigate the list of styles.</span></span>  

#### <span data-ttu-id="83664-207">Changer l’état de l’élément</span><span class="sxs-lookup"><span data-stu-id="83664-207">Toggle element state</span></span>   

<span data-ttu-id="83664-208">Pour activer ou désactiver l’état d’un élément, par `:active` exemple `:focus` :</span><span class="sxs-lookup"><span data-stu-id="83664-208">To toggle the state of an element, such as `:active` or `:focus`:</span></span>  

1.  <span data-ttu-id="83664-209">Accédez au volet **styles** , puis appuyez sur `Tab` jusqu’à ce que le bouton **afficher l’État** de l’élément soit actif.</span><span class="sxs-lookup"><span data-stu-id="83664-209">Navigate to the **Styles** pane and press `Tab` until the **Toggle Element State** button has focus.</span></span>  
1.  <span data-ttu-id="83664-210">Appuyez `Enter` pour développer la collection d’États d’éléments.</span><span class="sxs-lookup"><span data-stu-id="83664-210">Press `Enter` to expand the collection of element states.</span></span>  <span data-ttu-id="83664-211">Les États des éléments s’affichent sous la forme d’un groupe de cases à cocher.</span><span class="sxs-lookup"><span data-stu-id="83664-211">The element states are presented as a group of checkboxes.</span></span>  
1.  <span data-ttu-id="83664-212">Appuyez sur `Tab` jusqu’à ce que le premier état `:active` ait le focus.</span><span class="sxs-lookup"><span data-stu-id="83664-212">Press `Tab` until the first state, `:active`, has focus.</span></span>  
1.  <span data-ttu-id="83664-213">Appuyez sur `Space` pour l’activer.</span><span class="sxs-lookup"><span data-stu-id="83664-213">Press `Space` to enable it.</span></span>  <span data-ttu-id="83664-214">Le style de l’élément actuellement sélectionné dans l’arborescence DOM `:active` est désormais appliqué.</span><span class="sxs-lookup"><span data-stu-id="83664-214">If the currently-selected element in the DOM Tree has an `:active` style, it is now applied.</span></span>  
1.  <span data-ttu-id="83664-215">Continuez `Tab` d’appuyer sur pour explorer tous les États disponibles.</span><span class="sxs-lookup"><span data-stu-id="83664-215">Continue pressing `Tab` to explore all of the available states.</span></span>  

#### <span data-ttu-id="83664-216">Ajouter une classe existante</span><span class="sxs-lookup"><span data-stu-id="83664-216">Add an existing class</span></span>   

<span data-ttu-id="83664-217">Adjacent au bouton **afficher l’État** de l’élément est le bouton **classes d’éléments** .</span><span class="sxs-lookup"><span data-stu-id="83664-217">Adjacent to the **Toggle Element State** button is the **Element Classes** button.</span></span>  <span data-ttu-id="83664-218">Positionnez le focus sur celui-ci en appuyant sur la touche `Tab` `Enter` .</span><span class="sxs-lookup"><span data-stu-id="83664-218">Move focus to it by pressing `Tab` then `Enter`.</span></span>  <span data-ttu-id="83664-219">Le focus se déplace dans un champ de texte d’édition intitulé **Ajouter une nouvelle classe**.</span><span class="sxs-lookup"><span data-stu-id="83664-219">Focus moves into an edit text field labeled **Add New Class**.</span></span>  

<span data-ttu-id="83664-220">Le bouton **classes d’éléments** est principalement utilisé pour ajouter des classes existantes à un élément.</span><span class="sxs-lookup"><span data-stu-id="83664-220">The **Element Classes** button is primarily used for adding existing classes to an element.</span></span>  <span data-ttu-id="83664-221">Par exemple, si votre feuille de style contenait une classe d’assistance nommée `.clearfix` , vous pouvez appuyer `.` dans le champ de texte modifier pour afficher une liste de suggestions de classes et utiliser la `Down Arrow` pour trouver la `.clearfix` suggestion.</span><span class="sxs-lookup"><span data-stu-id="83664-221">For example, if your stylesheet contained a helper class named `.clearfix` you may press `.` inside of the edit text field to see a suggestion list of classes and use the `Down Arrow` to find the `.clearfix` suggestion.</span></span>  <span data-ttu-id="83664-222">Vous pouvez également taper le nom de la classe vous-même et appuyer sur l' `Enter` application.</span><span class="sxs-lookup"><span data-stu-id="83664-222">Or type the class name out yourself and press `Enter` to apply it.</span></span>  

#### <span data-ttu-id="83664-223">Ajouter une nouvelle règle de style</span><span class="sxs-lookup"><span data-stu-id="83664-223">Add a new style rule</span></span>   

<span data-ttu-id="83664-224">Adjacent au bouton **classes d’éléments** correspond au bouton **nouvelle règle de style** .</span><span class="sxs-lookup"><span data-stu-id="83664-224">Adjacent to the **Element Classes** button is the **New Style Rule** button.</span></span>  <span data-ttu-id="83664-225">Positionnez le focus sur celui-ci en appuyant et en appuyant `Tab` sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="83664-225">Move focus to it by pressing `Tab` and press `Enter`.</span></span>  <span data-ttu-id="83664-226">Le focus se déplace dans un champ de texte modifiable dans l’inspecteur de style.</span><span class="sxs-lookup"><span data-stu-id="83664-226">Focus moves into an editable text field inside of the style inspector.</span></span>  <span data-ttu-id="83664-227">Le contenu du texte initial du champ correspond au nom de balise de l’élément sélectionné dans l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="83664-227">The initial text content of the field is the tag name of the element that is selected in the **DOM Tree**.</span></span>  
<span data-ttu-id="83664-228">Vous pouvez taper le nom de la classe souhaité dans ce champ, puis appuyer sur `Tab` pour lui affecter des propriétés CSS.</span><span class="sxs-lookup"><span data-stu-id="83664-228">You may type any class name you want into this field and then press `Tab` to assign CSS properties to it.</span></span>  

### <span data-ttu-id="83664-229">Onglet calculé</span><span class="sxs-lookup"><span data-stu-id="83664-229">Computed tab</span></span>   

<span data-ttu-id="83664-230">Le focus étant placé sur l’onglet **calculé** , appuyez `Tab` pour déplacer le focus à l’intérieur et explorer le contenu.</span><span class="sxs-lookup"><span data-stu-id="83664-230">With focus on the **Computed** tab, press `Tab` to move focus inside and explore the contents.</span></span>  <span data-ttu-id="83664-231">Dans l’onglet **calculé** , il existe des contrôles pour explorer les propriétés CSS qui sont réellement appliquées à un élément selon l’ordre de la spécificité.</span><span class="sxs-lookup"><span data-stu-id="83664-231">Within the **Computed** tab there are controls for exploring which CSS properties are actually applied to an element in order of specificity.</span></span>  

<!--todo: add computed tab section when available  -->  

#### <span data-ttu-id="83664-232">Découvrir tous les styles calculés</span><span class="sxs-lookup"><span data-stu-id="83664-232">Explore all computed styles</span></span>   

<span data-ttu-id="83664-233">Appuyez sur `Tab` jusqu’à atteindre la collection de styles calculés.</span><span class="sxs-lookup"><span data-stu-id="83664-233">Press `Tab` until you reach the collection of computed styles.</span></span>  <span data-ttu-id="83664-234">Celles-ci s’affichent sous la forme d’un [Aria `tree` ][W3CWaiAriaTree].</span><span class="sxs-lookup"><span data-stu-id="83664-234">These are presented as an [ARIA `tree`][W3CWaiAriaTree].</span></span>  <span data-ttu-id="83664-235">Le développement d’une classe ListBox révèle les sélecteurs de CSS qui appliquent le style calculé.</span><span class="sxs-lookup"><span data-stu-id="83664-235">Expanding a listbox reveals which CSS selectors are applying the computed style.</span></span>  <span data-ttu-id="83664-236">Ces sélecteurs sont organisés par spécificité.</span><span class="sxs-lookup"><span data-stu-id="83664-236">These selectors are organized by specificity.</span></span>  <span data-ttu-id="83664-237">Un lecteur d’écran annonce la valeur calculée, le sélecteur CSS actuellement correspondant, le nom de fichier de la feuille de style qui contient le sélecteur et le numéro de ligne pour le sélecteur.</span><span class="sxs-lookup"><span data-stu-id="83664-237">A screen reader announces the computed value, which CSS selector is currently matching, the filename of the stylesheet that contains the selector, and the line number for the selector.</span></span>  

#### <span data-ttu-id="83664-238">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="83664-238">Known issues</span></span>   

*   <span data-ttu-id="83664-239">Si vous utilisez le champ de texte **filtre** , il n’est plus possible d’inspecter les styles.</span><span class="sxs-lookup"><span data-stu-id="83664-239">If you use the **Filter** text field, you are no longer able to inspect styles.</span></span>  

### <span data-ttu-id="83664-240">Onglet écouteur d’événements</span><span class="sxs-lookup"><span data-stu-id="83664-240">Event listeners tab</span></span>   

<span data-ttu-id="83664-241">Dans le panneau d' **éléments** , vous pouvez examiner les écouteurs d’événements appliqués à un élément à l’aide de l’onglet **écouteurs d’événements** .  Avec le focus dans le volet **styles** , appuyez sur `Right Arrow` pour accéder à l’onglet **écouteur d’événements** .</span><span class="sxs-lookup"><span data-stu-id="83664-241">From within the **Elements** panel you may inspect the event listeners applied to an element using the **Event Listeners** tab.  With focus on the **Styles** pane, press the `Right Arrow` to navigate to the **Event Listeners** tab.</span></span>  

#### <span data-ttu-id="83664-242">Explorer les détecteurs d’événements</span><span class="sxs-lookup"><span data-stu-id="83664-242">Explore event listeners</span></span>   

<span data-ttu-id="83664-243">Les détecteurs d’événements s’affichent sous forme de [Aria `tree` ][W3CWaiAriaTree].</span><span class="sxs-lookup"><span data-stu-id="83664-243">Event listeners are presented as an [ARIA `tree`][W3CWaiAriaTree].</span></span>  <span data-ttu-id="83664-244">Vous pouvez utiliser les touches de direction pour les parcourir.</span><span class="sxs-lookup"><span data-stu-id="83664-244">You may use the arrow keys to navigate them.</span></span>  <span data-ttu-id="83664-245">Un lecteur d’écran annonce le nom de l’objet DOM auquel l’écouteur d’événements est attaché, ainsi que le nom du fichier dans lequel l’écouteur d’événements est défini et le numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="83664-245">A screen reader announces the name of the DOM object that the event listener is attached to, as well as the file name where the event listener is defined and the line number.</span></span>  

### <span data-ttu-id="83664-246">Volet accessibilité</span><span class="sxs-lookup"><span data-stu-id="83664-246">Accessibility pane</span></span>   

<span data-ttu-id="83664-247">Le focus étant placé sur le volet **accessibilité** , appuyez sur `Tab` pour déplacer le focus à l’intérieur et explorer le contenu.</span><span class="sxs-lookup"><span data-stu-id="83664-247">With focus on the **Accessibility** pane, press `Tab` to move focus inside and explore the contents.</span></span>  <span data-ttu-id="83664-248">Dans le volet **accessibilité** , il existe des contrôles pour explorer l’arborescence d’accessibilité, les attributs Aria appliqués à un élément et les propriétés d’accessibilité calculées.</span><span class="sxs-lookup"><span data-stu-id="83664-248">Within the **Accessibility** pane there are controls for exploring the accessibility tree, the ARIA attributes applied to an element, and the computed accessibility properties.</span></span>  

<!--todo: add reference (Accessibility pane) section when available  -->  

#### <span data-ttu-id="83664-249">Arborescence d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="83664-249">Accessibility Tree</span></span>   

<span data-ttu-id="83664-250">L' **arborescence d’accessibilité** s’affiche sous la forme d’une expression [Aria `tree` ][W3CWaiAriaTree] qui `treeitem` correspond chacune à un élément du DOM.</span><span class="sxs-lookup"><span data-stu-id="83664-250">The **Accessibility Tree** is presented as an [ARIA `tree`][W3CWaiAriaTree] where each `treeitem` corresponds to an element in the DOM.</span></span>  <span data-ttu-id="83664-251">L’arborescence annonce le rôle calculé pour le nœud sélectionné.</span><span class="sxs-lookup"><span data-stu-id="83664-251">The tree announces the computed role for the selected node.</span></span>  <span data-ttu-id="83664-252">Éléments génériques comme `div` et `span` annoncés sous la forme «GenericContainer» dans l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="83664-252">Generic elements like `div` and `span` are announced as "GenericContainer" in the tree.</span></span>  <span data-ttu-id="83664-253">Utilisez les touches de direction pour parcourir l’arborescence et explorer les relations parent-enfant.</span><span class="sxs-lookup"><span data-stu-id="83664-253">Use the arrow keys to traverse the tree and explore parent-child relationships.</span></span>  

#### <span data-ttu-id="83664-254">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="83664-254">Known issues</span></span>   

*   <span data-ttu-id="83664-255">Le type de [Aria `tree` ][W3CWaiAriaTree] utilisé par le volet **accessibilité** risque de ne pas être correctement exposé dans Microsoft Edge pour les lecteurs d’écran MacOS tels que VoiceOver.</span><span class="sxs-lookup"><span data-stu-id="83664-255">The type of [ARIA `tree`][W3CWaiAriaTree] used by the **Accessibility** pane may not be properly exposed in Microsoft Edge for macOS screen readers like VoiceOver.</span></span>  <span data-ttu-id="83664-256">Abonnez-vous [#868480 problème de chrome][ChromiumIssues868480] pour être informé de la progression de ce problème.</span><span class="sxs-lookup"><span data-stu-id="83664-256">Subscribe to [Chromium issue #868480][ChromiumIssues868480] to be informed about progress on this issue.</span></span>  
*   <span data-ttu-id="83664-257">Chacun des sections d' **attributs Aria** et de **propriétés calculées** sont marqués en tant [que `tree` Aria ][W3CWaiAriaTree], mais chacun n’a pas de gestion du focus et ne fonctionne pas avec le clavier.</span><span class="sxs-lookup"><span data-stu-id="83664-257">Each of the **ARIA Attributes** and **Computed Properties** sections are marked up as an [ARIA `tree`][W3CWaiAriaTree], but each does not currently have focus management and is not keyboard operable.</span></span>  

## <span data-ttu-id="83664-258">Panneau d’audit</span><span class="sxs-lookup"><span data-stu-id="83664-258">Audits panel</span></span>   

<span data-ttu-id="83664-259">Le panneau **d’audit** vous devez exécuter une série de tests sur un site pour vérifier les problèmes courants liés à la performance, l’accessibilité, le SEO et un certain nombre d’autres catégories.</span><span class="sxs-lookup"><span data-stu-id="83664-259">The **Audits** panel you should run a series of tests against a site to check for common issues related to performance, accessibility, SEO, and a number of other categories.</span></span>  

### <span data-ttu-id="83664-260">Configuration et exécution d’un audit</span><span class="sxs-lookup"><span data-stu-id="83664-260">Configure and run an audit</span></span>   

1.  <span data-ttu-id="83664-261">Lorsque le panneau **audits** est ouvert pour la première fois, le focus est placé sur le bouton **exécuter l’audit** à la fin du formulaire.</span><span class="sxs-lookup"><span data-stu-id="83664-261">When the **Audits** panel is first opened, focus is placed on the **Run Audit** button at the end of the form.</span></span>  <span data-ttu-id="83664-262">Par défaut, le formulaire est configuré pour exécuter des audits pour chaque catégorie à l’aide de l’émulation mobile sur une connexion 3G simulée.</span><span class="sxs-lookup"><span data-stu-id="83664-262">By default the form is configured to run audits for every category using mobile emulation on a simulated 3G connection.</span></span>  
1.  <span data-ttu-id="83664-263">Utilisez `Shift` + `Tab` ou revenez en mode navigation pour modifier les paramètres d’audit.</span><span class="sxs-lookup"><span data-stu-id="83664-263">Use `Shift`+`Tab` or navigate back in Browse mode to change the audit settings.</span></span>  
1.  <span data-ttu-id="83664-264">Lorsque vous êtes prêt à exécuter l’audit, revenez au bouton **exécuter l’audit** et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="83664-264">When you are ready to run the audit, navigate back to the **Run Audit** button and press `Enter`.</span></span>  
1.  <span data-ttu-id="83664-265">Le focus se déplace dans une fenêtre modale avec un bouton d' **annulation** qui vous permet de quitter l’audit.</span><span class="sxs-lookup"><span data-stu-id="83664-265">Focus moves into a modal window with a **Cancel** button which allows you to exit the audit.</span></span>  <span data-ttu-id="83664-266">Il est possible que vous entendiez une série de earcons pendant que l’audit s’exécute et actualise la page plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="83664-266">You may hear a series of earcons as the audit runs and refreshes the page multiple times.</span></span>  

#### <span data-ttu-id="83664-267">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="83664-267">Known issues</span></span>   

*   <span data-ttu-id="83664-268">Les différentes sections du formulaire de configuration ne sont pas actuellement marquées avec un `fieldset` élément.</span><span class="sxs-lookup"><span data-stu-id="83664-268">The different sections of the configuration form are not currently marked up with a `fieldset` element.</span></span>  <span data-ttu-id="83664-269">Il est parfois plus facile de naviguer à l’aide du mode navigation pour déterminer les contrôles associés à chaque section.</span><span class="sxs-lookup"><span data-stu-id="83664-269">It may be easier to navigate them in Browse mode to figure out which controls are associated with each section.</span></span>  
*   <span data-ttu-id="83664-270">Il n’y a aucune annonce de earcon ou de région en direct lorsque l’audit est terminé.</span><span class="sxs-lookup"><span data-stu-id="83664-270">There is no earcon or live region announcement when the audit is finished running.</span></span>  <span data-ttu-id="83664-271">En règle générale, vous devez être en mesure de parcourir les résultats de 30 secondes.</span><span class="sxs-lookup"><span data-stu-id="83664-271">Generally it takes about 30 seconds, after which you should be able to navigate to the results.</span></span>  <span data-ttu-id="83664-272">L’utilisation du mode navigation est le moyen le plus simple d’accéder aux résultats.</span><span class="sxs-lookup"><span data-stu-id="83664-272">Using Browse mode may be the easiest way to reach the results.</span></span>  

### <span data-ttu-id="83664-273">Parcourir le rapport d’audit</span><span class="sxs-lookup"><span data-stu-id="83664-273">Navigate the audit report</span></span>   

<span data-ttu-id="83664-274">Le rapport d’audit est organisé en sections correspondant à chacune des catégories d’audit.</span><span class="sxs-lookup"><span data-stu-id="83664-274">The audit report is organized into sections that correspond with each of the audit categories.</span></span>  <span data-ttu-id="83664-275">Le rapport s’ouvre et affiche une liste de notes pour chaque catégorie.</span><span class="sxs-lookup"><span data-stu-id="83664-275">The report opens with a list of scores for each category.</span></span>  <span data-ttu-id="83664-276">Ces résultats sont également des liens qui peuvent être utilisés pour passer aux sections pertinentes.</span><span class="sxs-lookup"><span data-stu-id="83664-276">These scores are also links which are able to be used to skip to the relevant sections.</span></span>  <span data-ttu-id="83664-277">Dans chaque section se trouvent des éléments pouvant être développés `details` , qui contiennent des informations relatives aux audits réussis ou failés.</span><span class="sxs-lookup"><span data-stu-id="83664-277">Within each section are expandable `details` elements, which contain information relating to passed or failed audits.</span></span>  <span data-ttu-id="83664-278">Par défaut, seuls les audits qui échouent apparaissent.</span><span class="sxs-lookup"><span data-stu-id="83664-278">By default, only failing audits are shown.</span></span>  <span data-ttu-id="83664-279">Chaque section se termine par un `details` élément final qui contient tous les audits transmis.</span><span class="sxs-lookup"><span data-stu-id="83664-279">Each section ends with a final `details` element which contains all of the passed audits.</span></span>  

<span data-ttu-id="83664-280">Pour effectuer un nouvel audit, utilisez `Shift` + `Tab` pour quitter le rapport et recherchez le bouton **effectuer un audit** .</span><span class="sxs-lookup"><span data-stu-id="83664-280">To run a new audit, use `Shift`+`Tab` to exit the report and look for the **Perform An Audit** button.</span></span>  

## <span data-ttu-id="83664-281">Commentaires</span><span class="sxs-lookup"><span data-stu-id="83664-281">Feedback</span></span>   

*   <span data-ttu-id="83664-282">Envoyez des rapports de bogue DevTools ou des demandes de fonctionnalité au [suivi des problèmes de chrome][MonorailChromiumIssues].</span><span class="sxs-lookup"><span data-stu-id="83664-282">Send DevTools bug reports or feature requests to [Chromium Issue Tracker][MonorailChromiumIssues].</span></span>  
*   <span data-ttu-id="83664-283">Envoyez des commentaires relatifs à ce document à [GitHub][GithubEdgeDeveloperNewIssue].</span><span class="sxs-lookup"><span data-stu-id="83664-283">Send any feedback related to this document to [GitHub][GithubEdgeDeveloperNewIssue].</span></span>  

<!-- image links -->  

<!-- links -->  

<!--[DevtoolsAccessibilityReference]: reference.md "Accessibility Reference"  -->  
<!--[DevtoolsAccessibilityReferencePane]: reference.md#the-accessibility-pane "The Accessibility pane - Accessibility Reference"  -->  

<!--[MicrosoftEdgeDevtoolsIndex]: ../index.md "Microsoft Edge DevTools"  -->  
[DevtoolsCommandMenuIndex]: .. /Command-menu/index.MD "exécuter les commandes à l’aide du menu de commandes Microsoft Edge DevTools"  
[DevtoolsConsoleIndex]: .. /Console/index.MD "présentation de la console"  
[DevtoolsCssIndex]: .. /CSS/index.MD "découvrir comment afficher et modifier des feuilles CSS"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get Started With Viewing And Changing The DOM"  -->  
<!--[DevtoolsDomIndexNavigateDomTreeKeyboard]: ../dom/index.md#navigate-the-dom-tree-with-a-keyboard "Navigate the DOM Tree with a keyboard - Get Started With Viewing And Changing The DOM"  -->
[DevtoolsOpen]: .. /open.md "Ouvrez Microsoft Edge DevTools"  
[DevtoolsShortcuts]: .. /shortcuts.md "raccourcis clavier de Microsoft Edge DevTools"  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /Shortcuts.MD # styles-volet-raccourcis clavier-raccourcis clavier pour le volet de styles-raccourcis clavier de Microsoft Edge DevTools "  

[ChromiumIssues868480]: https://bugs.chromium.org/p/chromium/issues/detail?id=868480 "Problème 868480-exposer les arborescences ARIA sous forme de tableaux dans l’accessibilité Mac"  
[GithubEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Docs%20Feedback%5D "Nouveau problème-MicrosoftDocs/Edge-développeur | GitHub"  
[MDNActive]: https://developer.mozilla.org/docs/Web/CSS/:active ": actif | MDN"  
[MDNFocus]: https://developer.mozilla.org/docs/Web/CSS/:focus ": Focus | MDN"  
[MonorailChromiumIssues]: https://crbug.com "Problèmes-chrome-monorail"  
[W3CWaiAriaTablist]: https://www.w3.org/TR/wai-aria-1.1/#tablist "TabList (rôle)-applications Internet riches accessibles (WAI-ARIA) 1,1 | W3C"  
[W3CWaiAriaTree]: https://www.w3.org/TR/wai-aria-1.1/#tree "arborescence (rôle)-applications Internet riches accessibles (WAI-ARIA) 1,1 | W3C"  

> [!NOTE]
> <span data-ttu-id="83664-297">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="83664-297">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="83664-298">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) et est créée par [Rob Dodson][RobDodson] \ (Contributor, Google Web Fundamentals).</span><span class="sxs-lookup"><span data-stu-id="83664-298">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) and is authored by [Rob Dodson][RobDodson] \(Contributor, Google WebFundamentals\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="83664-300">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="83664-300">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[RobDodson]: https://developers.google.com/web/resources/contributors/robdodson  
