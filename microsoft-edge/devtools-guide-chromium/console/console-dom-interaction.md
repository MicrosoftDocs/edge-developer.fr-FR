---
description: Vue d'ensemble de l'interaction avec la page web actuelle dans le navigateur à l'aide de l'outil Console
title: Utiliser la console pour interagir avec le DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 80b0e4368b1c8feaf28a58ac2e3bd9c1ea2f1f92
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483416"
---
# <a name="use-the-console-to-interact-with-the-dom"></a><span data-ttu-id="d7b4e-104">Utiliser la console pour interagir avec le DOM</span><span class="sxs-lookup"><span data-stu-id="d7b4e-104">Use the Console to interact with the DOM</span></span>

<span data-ttu-id="d7b4e-105">**L'outil Console** n'est pas uniquement utilisé pour la [journalisation des informations][DevtoolsConsoleConsoleLog] ou pour exécuter un [javaScript arbitraire.][DevtoolsConsoleConsoleJavascript]</span><span class="sxs-lookup"><span data-stu-id="d7b4e-105">The **Console** tool isn't only for [logging information][DevtoolsConsoleConsoleLog] or to [run arbitrary JavaScript][DevtoolsConsoleConsoleJavascript].</span></span>  <span data-ttu-id="d7b4e-106">Il s'agit également d'un excellent moyen d'interagir avec la page web dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-106">It also is a great way to interact with the webpage in the browser.</span></span>  <span data-ttu-id="d7b4e-107">Considérez-la comme une version d'environnement de script de **l'outil Inspect.**</span><span class="sxs-lookup"><span data-stu-id="d7b4e-107">Consider it a script-environment version of the **Inspect** tool.</span></span>  

## <a name="read-from-the-dom"></a><span data-ttu-id="d7b4e-108">Lecture à partir du DOM</span><span class="sxs-lookup"><span data-stu-id="d7b4e-108">Read from the DOM</span></span>

<span data-ttu-id="d7b4e-109">Pour référencer l'en-tête de la page web, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-109">To reference the header of the webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="d7b4e-110">Ouvrez la **console.**</span><span class="sxs-lookup"><span data-stu-id="d7b4e-110">Open the **Console**.</span></span>
    *   <span data-ttu-id="d7b4e-111">Sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="d7b4e-111">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
1.  <span data-ttu-id="d7b4e-112">Tapez ou copiez-collez l'extrait de code suivant dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="d7b4e-112">Type or copy and paste the following code snippet in the **Console**.</span></span>  
    
    ```javascript
    document.querySelector('header')
    ```  
    
:::image type="complex" source="../media/console-dom-get-reference.msft.png" alt-text="Pour obtenir une référence à l'en-tête dans la console, utilisez document.querySelector" lightbox="../media/console-dom-get-reference.msft.png":::
    <span data-ttu-id="d7b4e-114">Pour obtenir une référence à l'en-tête dans la console, utilisez</span><span class="sxs-lookup"><span data-stu-id="d7b4e-114">To get a reference to the header in console, use</span></span> `document.querySelector`  
:::image-end:::  

<span data-ttu-id="d7b4e-115">Si vous sélectionnez ou déplacez le curseur de la souris sur le résultat `Shift` + `Tab` HTML, DevTools met l'en-tête en surdessin pour vous.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-115">If you select `Shift`+`Tab` or move your mouse cursor over the HTML result, DevTools highlights the header for you.</span></span>  

:::image type="complex" source="../media/console-dom-highlight-element.msft.png" alt-text="DevTools met en évidence la section que vous choisissez dans la console" lightbox="../media/console-dom-highlight-element.msft.png":::
    <span data-ttu-id="d7b4e-117">DevTools met en évidence la section que vous choisissez dans la **console**</span><span class="sxs-lookup"><span data-stu-id="d7b4e-117">DevTools highlights the section you choose in the **Console**</span></span>  
:::image-end:::  

## <a name="manipulate-the-dom"></a><span data-ttu-id="d7b4e-118">Manipuler le DOM</span><span class="sxs-lookup"><span data-stu-id="d7b4e-118">Manipulate the DOM</span></span>

<span data-ttu-id="d7b4e-119">Vous pouvez également manipuler la page web.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-119">You may manipulate the webpage, too.</span></span>  <span data-ttu-id="d7b4e-120">Par exemple, si vous copiez et collez ou tapez ce qui suit dans la **console,** une bordure verte s'affiche autour de l'en-tête.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-120">For example, if you copy and paste or type the following into the **Console**, a green border displays around the header.</span></span>

```javascript
document.querySelector('header').style.border = '2em solid green'
```  

:::image type="complex" source="../media/console-dom-add-border.msft.png" alt-text="Pour ajouter une bordure à un élément, utilisez la console" lightbox="../media/console-dom-add-border.msft.png":::
    <span data-ttu-id="d7b4e-122">Pour ajouter une bordure à un élément, utilisez la **console**</span><span class="sxs-lookup"><span data-stu-id="d7b4e-122">To add a border to an element, use the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="d7b4e-123">Selon la complexité de la page web, il peut être difficile de trouver l'élément à manipuler.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-123">Depending on the complexity of the webpage, It may be daunting to find the right element to manipulate.</span></span>  <span data-ttu-id="d7b4e-124">Toutefois, vous pouvez utiliser **l'outil Inspect** pour vous aider.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-124">But you may use the **Inspect** tool to help you.</span></span>  <span data-ttu-id="d7b4e-125">Dites que vous souhaitez manipuler la `Documentation` partie dans l'en-tête.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-125">Say you want to manipulate the `Documentation` part in the header.</span></span>

:::image type="complex" source="../media/console-dom-highlight-documentation.msft.png" alt-text="Afficher l'élément que vous inspectez à l'écran" lightbox="../media/console-dom-highlight-documentation.msft.png":::
    <span data-ttu-id="d7b4e-127">Afficher l'élément que vous inspectez à l'écran</span><span class="sxs-lookup"><span data-stu-id="d7b4e-127">Display the element that you inspect on the screen</span></span>  
:::image-end:::  

<span data-ttu-id="d7b4e-128">Pour obtenir une référence directe à l'élément à manipuler, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-128">To get a direct reference to the element to manipulate, complete the following actions.</span></span>  

1.  <span data-ttu-id="d7b4e-129">Utilisez **l'outil Inspect** pour choisir l'élément.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-129">Use the **Inspect** tool to choose the element.</span></span>  

    :::image type="complex" source="../media/console-dom-use-inspector-to-get-element.msft.png" alt-text="Pour choisir un élément, utilisez l'outil Inspecteur" lightbox="../media/console-dom-use-inspector-to-get-element.msft.png":::
        <span data-ttu-id="d7b4e-131">Pour choisir un élément, utilisez **l'outil Inspecteur**</span><span class="sxs-lookup"><span data-stu-id="d7b4e-131">To choose an element, use the **Inspector** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7b4e-132">Choisissez-le et DevTools passe à **l'outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="d7b4e-132">Choose it and DevTools jumps to the **Elements** tool.</span></span>  
1.  <span data-ttu-id="d7b4e-133">Choisissez le `...` menu en regard de l'élément dans l'affichage DOM.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-133">Choose the `...` menu next to the element in the DOM view.</span></span>  
    
    :::image type="complex" source="../media/console-dom-overflow-menu-in-elements.msft.png" alt-text="L'élément choisi s'affiche dans l'arborescence DOM de l'outil Elements, choisissez le menu de dépassement pour obtenir d'autres fonctionnalités" lightbox="../media/console-dom-overflow-menu-in-elements.msft.png":::
        <span data-ttu-id="d7b4e-135">L'élément choisi s'affiche dans l'arborescence DOM de l'outil **Elements,** choisissez le menu de dépassement pour obtenir d'autres fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="d7b4e-135">The chosen element displays in the DOM tree of the **Elements** tool, choose the overflow menu to get more features</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7b4e-136">Ouvrez le menu contextuel et choisissez `Copy`  >  `Copy JS Path` .</span><span class="sxs-lookup"><span data-stu-id="d7b4e-136">Open the contextual menu and choose `Copy` > `Copy JS Path`.</span></span>  
    
    :::image type="complex" source="../media/console-dom-copy-JS-path.msft.png" alt-text="Copier le chemin d'accès JavaScript à partir d'un élément dans l'affichage DOM de l'outil Elements" lightbox="../media/console-dom-copy-JS-path.msft.png":::
        <span data-ttu-id="d7b4e-138">Copier le chemin d'accès JavaScript à partir d'un élément dans l'affichage DOM de **l'outil Elements**</span><span class="sxs-lookup"><span data-stu-id="d7b4e-138">Copy the JavaScript path from an element in the DOM view of the **Elements** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7b4e-139">Revenir à la **console et** coller la commande.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-139">Go back to the **Console** and paste the command.</span></span>  
    
<span data-ttu-id="d7b4e-140">Pour modifier le texte du lien vers `My Playground` , ajoutez `.textContent = "My Playground"` à la commande que vous avez précédemment pastée.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-140">To change the text of the link to `My Playground`, add `.textContent = "My Playground"` to the command you previously pasted.</span></span>  

:::image type="complex" source="../media/console-dom-change-content.msft.png" alt-text="Utiliser la console pour modifier le contenu d'un élément" lightbox="../media/console-dom-change-content.msft.png":::
    <span data-ttu-id="d7b4e-142">Utiliser la **console pour** modifier le contenu d'un élément</span><span class="sxs-lookup"><span data-stu-id="d7b4e-142">Use the **Console** to change the content of an element</span></span>  
:::image-end:::  

<span data-ttu-id="d7b4e-143">Utilisez toutes les manipulations DOM JavaScript que vous souhaitez faire dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="d7b4e-143">Use any JavaScript DOM manipulations you want to do in the **Console**.</span></span>  <span data-ttu-id="d7b4e-144">Pour le rendre plus pratique, **la console** est livré avec quelques méthodes d'aide.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-144">To make it more convenient, the **Console** comes with a few helper methods.</span></span>  

## <a name="helpful-console-utility-methods"></a><span data-ttu-id="d7b4e-145">Méthodes utilitaires de console utiles</span><span class="sxs-lookup"><span data-stu-id="d7b4e-145">Helpful Console utility methods</span></span>  

<span data-ttu-id="d7b4e-146">De nombreuses méthodes et raccourcis pratiques sont disponibles en tant [qu'utilitaires de console.][DevtoolsConsoleUtilities]</span><span class="sxs-lookup"><span data-stu-id="d7b4e-146">Many convenience methods and shortcuts are available to you as [Console Utilities][DevtoolsConsoleUtilities].</span></span>  <span data-ttu-id="d7b4e-147">Certaines méthodes sont extrêmement puissantes et sont des éléments que vous avez probablement écrits sous la mesure d'une série `console.log()` d'instructions dans le passé.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-147">Some of the methods are incredibly powerful and are things you probably wrote as a series of `console.log()` statements in the past.</span></span>

### <a name="the-power-to-the-"></a><span data-ttu-id="d7b4e-148">L'alimentation vers le $</span><span class="sxs-lookup"><span data-stu-id="d7b4e-148">The power to the $</span></span>

<span data-ttu-id="d7b4e-149">La console dispose de puissances spéciales et vous vous en souvenez `$` peut-être à partir de jQuery. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d7b4e-149">The `$` has special powers in **Console** and you may remember that from jQuery.</span></span>

*   `$_` <span data-ttu-id="d7b4e-150">stocke le résultat de la dernière commande.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-150">stores the result of the last command.</span></span>  <span data-ttu-id="d7b4e-151">Ainsi, si vous `2 + 2` tapez et sélectionnez, puis `Enter` `$_` tapez , la **console** vous `4` affiche.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-151">So, if you type `2 + 2` and select `Enter`, and then type `$_`, the **Console** displays you `4`.</span></span>
*   `$0` <span data-ttu-id="d7b4e-152">est une pile des derniers éléments `$4` inspectés est toujours la plus `$0` nouvelle.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-152">to `$4` is a stack of the last inspected elements `$0` is always the newest one.</span></span>  <span data-ttu-id="d7b4e-153">Dans l'exemple précédent, vous avez donc choisi l'élément dans l'outil **Inspecteur** et le type `$0.textContent = "My Playground"` pour obtenir le même effet.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-153">So in the earlier example, you just chose the element in the **Inspector** tool and type `$0.textContent = "My Playground"` to get the same effect.</span></span>
*   `$x()` <span data-ttu-id="d7b4e-154">vous permet de choisir des éléments DOM à l'aide de XPATH.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-154">allows you to choose DOM elements using XPATH.</span></span>
*   `$()` <span data-ttu-id="d7b4e-155">et `$$()` sont des versions plus courtes de for et `document.querySelector()` `document.querySelectorAll()` .</span><span class="sxs-lookup"><span data-stu-id="d7b4e-155">and `$$()` are shorter versions of for `document.querySelector()` and `document.querySelectorAll()`.</span></span>  
    
<span data-ttu-id="d7b4e-156">Par exemple, l'extrait de code suivant extrait tous les liens de la page web \(comme c'est le cas pour \) et affiche les liens sous la forme d'un tableau triable à copier et coller, par exemple, dans `$$('a')` `document.querySelectorAll('a')` Excel.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-156">For example, the following code snippet retrieves all the links in the webpage \(as `$$('a')` is short for `document.querySelectorAll('a')`\) and displays the links as a sortable table to copy and paste, for example, into Excel.</span></span>

```javascript
console.table($$('a'),['href','text']);
```  

:::image type="complex" source="../media/console-dom-get-all-links.msft.png" alt-text="Obtenir tous les liens dans la page web et afficher le résultat sous la mesure d'un tableau" lightbox="../media/console-dom-get-all-links.msft.png":::
    <span data-ttu-id="d7b4e-158">Obtenir tous les liens dans la page web et afficher le résultat sous la mesure d'un tableau</span><span class="sxs-lookup"><span data-stu-id="d7b4e-158">Get all links in the webpage and display the result as a table</span></span>  
:::image-end:::  

<span data-ttu-id="d7b4e-159">Toutefois, si vous ne souhaitez pas afficher les informations, mais que vous souhaitez les récupérer en tant que données.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-159">However, if you don't want to display the information, but you want to grab it as data.</span></span>  <span data-ttu-id="d7b4e-160">Le `$$('a')` raccourci fournit les liens d'ancrage et toutes les propriétés de chacun d'eux.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-160">The `$$('a')` shortcut provides the anchor links and all of the properties for each one.</span></span>  <span data-ttu-id="d7b4e-161">Le problème est que vous souhaitez uniquement les liens et le texte associé.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-161">The problem is that you only want the links and the related text.</span></span>  

:::image type="complex" source="../media/console-dom-too-much-link-information.msft.png" alt-text="Le raccourci $$ renvoie beaucoup trop d'informations" lightbox="../media/console-dom-too-much-link-information.msft.png":::
    <span data-ttu-id="d7b4e-163">Le `$$` raccourci renvoie beaucoup trop d'informations</span><span class="sxs-lookup"><span data-stu-id="d7b4e-163">The `$$` shortcut returns far too much information</span></span>  
:::image-end:::  

<span data-ttu-id="d7b4e-164">Le `$$` raccourci présente une fonctionnalité supplémentaire intéressante.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-164">The `$$` shortcut has an interesting extra feature.</span></span>  <span data-ttu-id="d7b4e-165">Au lieu de renvoyer un `NodeList` pur comme , le raccourci vous donne toutes les `document.querySelectorAll()` `$$` `Array` méthodes.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-165">Instead of returning a pure `NodeList` like `document.querySelectorAll()`, the `$$` shortcut gives you all of the `Array` methods.</span></span>  <span data-ttu-id="d7b4e-166">Utilisez `map()` la méthode pour réduire les informations à ce dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-166">Use `map()` method to reduce the information to what you need.</span></span>  

```javascript
$$('a').map(a => {
    return {url: a.href, text: a.innerText}
})
```  

<span data-ttu-id="d7b4e-167">L'extrait de code renvoie un tableau de tous les liens en tant qu'objets avec `url` et `text` propriétés.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-167">The code snippet returns an Array of all the links as objects with `url` and `text` properties.</span></span>  

:::image type="complex" source="../media/console-dom-filter-link-data.msft.png" alt-text="Utiliser la carte sur $$ pour filtrer les informations au minimum" lightbox="../media/console-dom-filter-link-data.msft.png":::
    <span data-ttu-id="d7b4e-169">Utiliser la carte pour `$$` filtrer les informations jusqu'au minimum</span><span class="sxs-lookup"><span data-stu-id="d7b4e-169">Use map on `$$` to filter information down to the bare minimum</span></span>  
:::image-end:::  

<span data-ttu-id="d7b4e-170">Vous n'avez pas encore terminé, plusieurs liens sont des liens internes vers la page web ou ont du texte vide.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-170">You aren't done yet, several links are internal links to the webpage or have empty text.</span></span>  <span data-ttu-id="d7b4e-171">Utilisez la méthode de filtre pour vous débarrasser des liens internes.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-171">Use the filter method to get rid of the internal links.</span></span>  

```javascript
$$('a').map(a => {
    return {text: a.innerText, url: a.href}
}).filter(a => {
    return a.text !== '' && !a.url.match('docs.microsoft.com')
})
```  

:::image type="complex" source="../media/console-dom-filter-out-empty-links.msft.png" alt-text="Obtenir les liens qui ne sont pas vides et qui sont externes" lightbox="../media/console-dom-filter-out-empty-links.msft.png":::
    <span data-ttu-id="d7b4e-173">Obtenir les liens qui ne sont pas vides et qui sont externes</span><span class="sxs-lookup"><span data-stu-id="d7b4e-173">Get the links that aren't empty and are external</span></span>  
:::image-end:::  

<span data-ttu-id="d7b4e-174">Comme affiché au début de la page web, vous pouvez également modifier ces éléments.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-174">As displayed at the start of the webpage, you may also change these elements.</span></span>  <span data-ttu-id="d7b4e-175">Par exemple, l'extrait de code suivant crée une bordure verte autour de tous les liens externes :</span><span class="sxs-lookup"><span data-stu-id="d7b4e-175">For example, the following code snippet creates a green border around all external links:</span></span>

```javascript
$$('a[href^="https://"]').forEach(
  a => a.style.border = '1px solid green'
)
```  

:::image type="complex" source="../media/console-dom-highlight-links.msft.png" alt-text="Pour mettre en surbrillez tous les liens externes, ajoutez une bordure verte autour de chacun d'eux" lightbox="../media/console-dom-highlight-links.msft.png":::
    <span data-ttu-id="d7b4e-177">Pour mettre en surbrillez tous les liens externes, ajoutez une bordure verte autour de chacun d'eux</span><span class="sxs-lookup"><span data-stu-id="d7b4e-177">To highlight all external links, add a green border around each</span></span>  
:::image-end:::  

<span data-ttu-id="d7b4e-178">Au lieu d'écrire du JavaScript complexe pour filtrer les résultats, utilisez la puissance des sélecteurs CSS.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-178">Instead of writing complex JavaScript to filter results, use the power of CSS selectors.</span></span>  

<span data-ttu-id="d7b4e-179">Pour créer un tableau des images et des informations de toutes les images de la page web qui ne sont pas des images en ligne, complétez `src` `alt` les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-179">To create a table of the `src` and `alt` information for all images on the webpage that aren't inline images, complete the following actions.</span></span>  

1.  <span data-ttu-id="d7b4e-180">Ouvrez la **console.**</span><span class="sxs-lookup"><span data-stu-id="d7b4e-180">Open the **Console**.</span></span>  
1.  <span data-ttu-id="d7b4e-181">Tapez ou copiez-collez l'extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-181">Type or copy and paste the following code snippet.</span></span>  

```javascript
console.table($$('img:not([src^=data])'), ['src','alt'])
```  

:::image type="complex" source="../media/console-dom-complex-CSS-selector.msft.png" alt-text="Pour choisir des éléments, utilisez un sélecteur CSS complexe" lightbox="../media/console-dom-complex-CSS-selector.msft.png":::
    <span data-ttu-id="d7b4e-183">Pour choisir des éléments, utilisez un sélecteur CSS complexe</span><span class="sxs-lookup"><span data-stu-id="d7b4e-183">To choose elements, use a complex CSS selector</span></span>  
:::image-end:::  

<span data-ttu-id="d7b4e-184">Prêt pour un exemple encore plus complexe ?</span><span class="sxs-lookup"><span data-stu-id="d7b4e-184">Ready for an even more complex example?</span></span>  <span data-ttu-id="d7b4e-185">Les pages web HTML générées à partir de markdown comme cet article ont des valeurs d'ID automatiques pour chaque titre afin de vous permettre d'établir un lien profond vers cette section.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-185">HTML webpages generated from markdown like this article, have automatic ID values for each heading to allow you to deep link to that section.</span></span>  <span data-ttu-id="d7b4e-186">Par exemple, une `# New features` modification apportée `<h1 id="new-features">New features</h1>` à .</span><span class="sxs-lookup"><span data-stu-id="d7b4e-186">For example, a `# New features` changes to `<h1 id="new-features">New features</h1>`.</span></span>  

<span data-ttu-id="d7b4e-187">Pour lister tous les en-tête automatiques à copier et coller, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-187">To list of all of the automatic headings to copy and paste, complete the following actions.</span></span>  

1.  <span data-ttu-id="d7b4e-188">Ouvrez la **console.**</span><span class="sxs-lookup"><span data-stu-id="d7b4e-188">Open the **Console**.</span></span>  
1.  <span data-ttu-id="d7b4e-189">Tapez ou copiez-collez l'extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-189">Type or copy and paste the following code snippet.</span></span>  

```javascript
let out = '';
$$('#main [id]').filter(
    elm => {return elm.nodeName.startsWith('H')}
).forEach(elm => {
   out += elm.innerText + "\n" + 
          document.location.href + '#' +
          elm.id + "\n";
});
console.log(out);
```  

<span data-ttu-id="d7b4e-190">Le résultat est le texte qui contient le contenu de chaque titre suivi de l'URL complète qui pointe vers celui-ci.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-190">The result is text that contains content for each heading followed by the full URL that points to it.</span></span>  

:::image type="complex" source="../media/console-dom-get-generated-headings.msft.png" alt-text="Obtenir tous les titres et les URL générées à partir de la page web" lightbox="../media/console-dom-get-generated-headings.msft.png":::
    <span data-ttu-id="d7b4e-192">Obtenir tous les titres et les URL générées à partir de la page web</span><span class="sxs-lookup"><span data-stu-id="d7b4e-192">Get all the headings and the generated URLs from the webpage</span></span>  
:::image-end:::  

### <a name="clean-up-with-clear-and-copy"></a><span data-ttu-id="d7b4e-193">Nettoyer avec effacer et copier</span><span class="sxs-lookup"><span data-stu-id="d7b4e-193">Clean up with clear and copy</span></span>

<span data-ttu-id="d7b4e-194">Lorsque vous développez **dans la console,** les choses peuvent être désordessée.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-194">When developing in the **Console**, things may get messy.</span></span>  <span data-ttu-id="d7b4e-195">Vous trouverez peut-être frustrant d'essayer de choisir des résultats pendant que vous copiez et collez.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-195">You may find it frustrating to try to choose results while you copy and paste.</span></span>  <span data-ttu-id="d7b4e-196">Les deux méthodes utilitaires suivantes vous aident.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-196">The following two utility methods help you.</span></span>  

*   `copy()` <span data-ttu-id="d7b4e-197">copie ce que vous lui donnez dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-197">copies whatever you give it to the clipboard.</span></span>  <span data-ttu-id="d7b4e-198">La `copy()` méthode est particulièrement utile lorsque vous la mélangez `$_` avec celle qui copie le dernier résultat.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-198">The `copy()` method is especially useful when you mix it with `$_` that copies the last result.</span></span>
*   `clear()` <span data-ttu-id="d7b4e-199">clears the **Console**.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-199">clears the **Console**.</span></span>

### <a name="read-and-monitor-events"></a><span data-ttu-id="d7b4e-200">Lire et surveiller les événements</span><span class="sxs-lookup"><span data-stu-id="d7b4e-200">Read and monitor events</span></span>

<span data-ttu-id="d7b4e-201">Deux autres méthodes utilitaires intéressantes de **console** traitent de la gestion des événements.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-201">Two other interesting utility methods of **Console** deal with event handling.</span></span>

*   `getEventListeners(node)` <span data-ttu-id="d7b4e-202">répertorie tous les écouteurs d'événements d'un nœud.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-202">lists all the event listeners of a node.</span></span>
*   `monitorEvents(node, events)` <span data-ttu-id="d7b4e-203">surveille et enregistre les événements qui se produisent sur un nœud.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-203">monitors and logs the events that happen on a node.</span></span>

<span data-ttu-id="d7b4e-204">Pour lister tous les auditeurs d'événements affectés au premier formulaire dans la page web, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-204">To list all of the event listener assigned to the first form in the webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="d7b4e-205">Ouvrez la **console.**</span><span class="sxs-lookup"><span data-stu-id="d7b4e-205">Open the **Console**.</span></span>  
1.  <span data-ttu-id="d7b4e-206">Tapez ou copiez-collez l'extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-206">Type or copy and paste the following code snippet.</span></span>  
    
    ```javascript
    getEventListeners($('form')); 
    ```  

:::image type="complex" source="../media/console-dom-get-form-events.msft.png" alt-text="Obtenir tous les écouteurs d'événements pour le premier formulaire dans la page web" lightbox="../media/console-dom-get-form-events.msft.png":::
    <span data-ttu-id="d7b4e-208">Obtenir tous les écouteurs d'événements pour le premier formulaire dans la page web</span><span class="sxs-lookup"><span data-stu-id="d7b4e-208">Get all events listeners for the first form in the webpage</span></span>  
:::image-end:::  

<span data-ttu-id="d7b4e-209">Lorsque vous surveillez, vous recevez une notification dans la **console** chaque fois que des modifications sont apportées aux éléments spécifiés.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-209">When you monitor, you to get a notification in the **Console** every time something changes to the specified elements.</span></span>  <span data-ttu-id="d7b4e-210">Vous définissez les événements que vous souhaitez écouter en tant que deuxième paramètre.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-210">You define the events you want to listen to as a second parameter.</span></span>  <span data-ttu-id="d7b4e-211">Il est important que vous définissiez les événements que vous souhaitez surveiller, sinon tout événement qui se produit sur l'élément est signalé.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-211">It is important for you to define the events that you want to monitor, otherwise any event happening to the element is reported.</span></span>

<span data-ttu-id="d7b4e-212">Pour obtenir une notification dans la **console** chaque fois que vous faites défiler, resizez la fenêtre ou lorsque l'utilisateur tape dans le formulaire de recherche, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-212">To get a notification in the **Console** every time you scroll, resize the window, or when the user types in the search form, complete the following actions.</span></span>  

1.  <span data-ttu-id="d7b4e-213">Ouvrez la **console.**</span><span class="sxs-lookup"><span data-stu-id="d7b4e-213">Open the **Console**.</span></span>  
1.  <span data-ttu-id="d7b4e-214">Tapez ou copiez-collez l'extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-214">Type or copy and paste the following code snippet.</span></span>  
    
    ```javascript
    monitorEvents(window, ['resize', 'scroll']);
    monitorEvents($0, 'keyup');
    ```  
    
:::image type="complex" source="../media/console-dom-monitor-events.msft.png" alt-text="La console affiche tous les événements de défilement qui se produisent sur la fenêtre" lightbox="../media/console-dom-monitor-events.msft.png":::
    <span data-ttu-id="d7b4e-216">**La console** affiche tous les événements de défilement qui se produisent sur la fenêtre</span><span class="sxs-lookup"><span data-stu-id="d7b4e-216">**Console** displays every scroll event that happens on the Window</span></span>  
:::image-end:::  

<span data-ttu-id="d7b4e-217">Pour enregistrer n'importe quelle action de touche sur l'élément actuellement choisi, concentrez-vous sur le formulaire de recherche dans l'en-tête et sélectionnez certaines touches.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-217">To log any key action on the currently chosen element, focus on the search form in the header and select some keys.</span></span>  

:::image type="complex" source="../media/console-dom-monitor-key-events.msft.png" alt-text="La console affiche les événements de keyup qui se produisent sur le formulaire" lightbox="../media/console-dom-monitor-key-events.msft.png":::
    <span data-ttu-id="d7b4e-219">**La console** affiche les `keyup` événements qui se produisent sur le formulaire</span><span class="sxs-lookup"><span data-stu-id="d7b4e-219">**Console** displays `keyup` events that happen on the form</span></span>  
:::image-end:::  

<span data-ttu-id="d7b4e-220">Pour l'arrêter, supprimez la surveillance que vous définissez à l'aide de l'extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-220">To stop it, remove the monitoring you set using the following code snippet.</span></span>  

```javascript
unmonitorEvents(window, ['resize', 'scroll']);
unmonitorEvents($0, 'key');
```  

## <a name="reuse-dom-manipulation-scripts"></a><span data-ttu-id="d7b4e-221">Réutilisation des scripts de manipulation DOM</span><span class="sxs-lookup"><span data-stu-id="d7b4e-221">Reuse DOM manipulation scripts</span></span>

<span data-ttu-id="d7b4e-222">Il peut s'avérer utile de manipuler le DOM à partir de la **console.**</span><span class="sxs-lookup"><span data-stu-id="d7b4e-222">You may find it useful to manipulate the DOM from the **Console**.</span></span>  <span data-ttu-id="d7b4e-223">Vous pouvez bientôt vous lancer dans les limitations de la **console** en tant que plateforme de développement.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-223">You may soon run into the limitations of the **Console** as a development platform.</span></span>  <span data-ttu-id="d7b4e-224">La bonne nouvelle est que l'outil [Sources][DevtoolsSourcesIndex] dans DevTools offre un environnement de développement complet.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-224">The good news is that the [Sources][DevtoolsSourcesIndex] tool in DevTools offers a fully featured development environment.</span></span>  <span data-ttu-id="d7b4e-225">Dans **l'outil Sources,** vous pouvez effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-225">In the **Sources** tool, you may complete the following actions.</span></span>  

*   <span data-ttu-id="d7b4e-226">Stockez vos scripts pour la **console en** tant [qu'extraits de code.][DevToolsJavascriptSnippets]</span><span class="sxs-lookup"><span data-stu-id="d7b4e-226">Store your scripts for the **Console** as [Snippets][DevToolsJavascriptSnippets].</span></span>  
*   <span data-ttu-id="d7b4e-227">Exécutez les scripts dans une page web à l'aide d'un raccourci clavier ou de l'éditeur.</span><span class="sxs-lookup"><span data-stu-id="d7b4e-227">Run the scripts in a webpage using a keyboard shortcut or the editor.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="d7b4e-228">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="d7b4e-228">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Console en tant qu'environnement JavaScript | Documents Microsoft"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Logs in the Console tool | Documents Microsoft"  
[DevtoolsConsoleUtilities]: ./utilities.md "Référence de l'API des utilitaires de console | Documents Microsoft"  

[DevToolsJavascriptSnippets]: ../javascript/snippets.md "Exécuter des extraits de code JavaScript sur n'importe quelle page avec Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsSourcesIndex]: ../sources/index.md "Vue d'ensemble de l'outil Sources | Documents Microsoft"  
