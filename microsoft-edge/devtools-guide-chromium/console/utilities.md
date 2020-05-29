---
title: XXXXXX xxxxxxx xxx xxxxxxxxx
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 28b40f3f79928725d3d49418e01cf02247224370
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601795"
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





# <span data-ttu-id="b7f4b-103">XXXXXX xxxxxxx xxx xxxxxxxxx</span><span class="sxs-lookup"><span data-stu-id="b7f4b-103">Console Utilities API Reference</span></span>   



<span data-ttu-id="b7f4b-104">L’API des utilitaires de la console contient une collection de commandes pratiques permettant d’effectuer des tâches courantes: la sélection et l’examen des éléments DOM, l’affichage des données dans un format lisible, l’arrêt et le démarrage du profileur, et la surveillance des événements DOM.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-104">The Console Utilities API contains a collection of convenience commands for performing common tasks:  selecting and inspecting DOM elements, displaying data in readable format, stopping and starting the profiler, and monitoring DOM events.</span></span>  

> [!WARNING]
> <span data-ttu-id="b7f4b-105">Les commandes suivantes fonctionnent uniquement dans la console Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-105">The following commands only work in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="b7f4b-106">Les commandes ne fonctionnent pas si celles-ci sont exécutées à partir de vos scripts.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-106">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="b7f4b-107">Vous recherchez `console.log()` , `console.error()` et le reste des `console.*` méthodes?</span><span class="sxs-lookup"><span data-stu-id="b7f4b-107">Looking for `console.log()`, `console.error()`, and the rest of the `console.*` methods?</span></span>  <span data-ttu-id="b7f4b-108">Voir [référence][DevToolsConsoleApi]sur l’API de la console.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-108">See [Console API Reference][DevToolsConsoleApi].</span></span>  

## <span data-ttu-id="b7f4b-109">Expression récemment évaluée</span><span class="sxs-lookup"><span data-stu-id="b7f4b-109">Recently Evaluated Expression</span></span>  

```console
$_
```  

<span data-ttu-id="b7f4b-110">Renvoie la valeur de l’expression évaluée le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-110">Returns the value of the most recently evaluated expression.</span></span>  

<span data-ttu-id="b7f4b-111">Dans la [figure 1](#figure-1), une expression simple \ ( `2 + 2` \) est évaluée.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-111">In [Figure 1](#figure-1), a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="b7f4b-112">La `$_` propriété est alors évaluée, qui contient la même valeur.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-112">The `$_` property is then evaluated, which contains the same value.</span></span>  

> ##### <span data-ttu-id="b7f4b-113">Figure1</span><span class="sxs-lookup"><span data-stu-id="b7f4b-113">Figure 1</span></span>  
> `$_` <span data-ttu-id="b7f4b-114">est la dernière expression évaluée</span><span class="sxs-lookup"><span data-stu-id="b7f4b-114">is the most recently evaluated expression</span></span>  
> ![$ _ est l’expression la plus récemment évaluée.][ImageRecentExpression]  

<span data-ttu-id="b7f4b-116">Dans la [figure 2](#figure-2), l’expression évaluée contient initialement un tableau de noms.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-116">In [Figure 2](#figure-2), the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="b7f4b-117">Si vous évaluez la `$_.length` longueur de l’argument matrice, la valeur stockée dans `$_` les modifications devient la dernière expression évaluée `4` .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-117">Evaluating `$_.length` to find the length of the array, the value stored in `$_` changes to become the latest evaluated expression, `4`.</span></span>  

> ##### <span data-ttu-id="b7f4b-118">Figure 2</span><span class="sxs-lookup"><span data-stu-id="b7f4b-118">Figure 2</span></span>  
> `$_` <span data-ttu-id="b7f4b-119">change lorsque de nouvelles commandes sont évaluées</span><span class="sxs-lookup"><span data-stu-id="b7f4b-119">changes when new commands are evaluated</span></span>  
> ![$ _ change lorsque de nouvelles commandes sont évaluées][ImageChangedRecentExpression]  

## <span data-ttu-id="b7f4b-121">Élément récemment sélectionné ou objet JavaScript</span><span class="sxs-lookup"><span data-stu-id="b7f4b-121">Recently Selected Element Or JavaScript Object</span></span>  

```console
$0
```  

<span data-ttu-id="b7f4b-122">Retourne l’élément le plus récemment sélectionné ou l’objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-122">Returns the most recently selected element or JavaScript object.</span></span>  `$1` <span data-ttu-id="b7f4b-123">renvoie le second dernier sélectionné, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-123">returns the second most recently selected one, and so on.</span></span>  <span data-ttu-id="b7f4b-124">Les `$0` commandes,,, `$1` `$2` `$3` et `$4` permettent de faire une référence historique aux cinq derniers éléments DOM examinés dans le panneau **éléments** ou les cinq derniers objets du tas JavaScript sélectionnés dans le panneau **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-124">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** panel or the last five JavaScript heap objects selected in the **Memory** panel.</span></span>  

```console
$1
```  

```console
$2
```  

```console
$3
```  

```console
$4
```  

<span data-ttu-id="b7f4b-125">Dans [figure 3](#figure-3), un `img` élément est sélectionné dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-125">In [Figure 3](#figure-3), an `img` element is selected in the **Elements** panel.</span></span>  <span data-ttu-id="b7f4b-126">Le tiroir **Console** de la console `$0` a été évalué et affiche le même élément.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-126">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

> ##### <span data-ttu-id="b7f4b-127">Figure3</span><span class="sxs-lookup"><span data-stu-id="b7f4b-127">Figure 3</span></span>  
> <span data-ttu-id="b7f4b-128">La liste </span><span class="sxs-lookup"><span data-stu-id="b7f4b-128">The</span></span> `$0`  
> ![$0][ImageElement0]  

<span data-ttu-id="b7f4b-130">Dans la [figure 4](#figure-4), l’image montre un élément différent sélectionné dans la même page.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-130">In [Figure 4](#figure-4), the image shows a different element selected in the same page.</span></span>  <span data-ttu-id="b7f4b-131">L' `$0` élément désormais fait référence à l’élément que vous venez de sélectionner, tandis qu’il `$1` renvoie le précédent.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-131">The `$0` now refers to the newly selected element, while `$1` returns the previously selected one.</span></span>  

> ##### <span data-ttu-id="b7f4b-132">Figure 4</span><span class="sxs-lookup"><span data-stu-id="b7f4b-132">Figure 4</span></span>  
> <span data-ttu-id="b7f4b-133">La liste </span><span class="sxs-lookup"><span data-stu-id="b7f4b-133">The</span></span> `$1`  
> ![$1][ImageElement1]  

## <span data-ttu-id="b7f4b-135">Sélecteur de requête</span><span class="sxs-lookup"><span data-stu-id="b7f4b-135">Query Selector</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="b7f4b-136">Renvoie la référence au premier élément DOM avec le sélecteur CSS spécifié.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-136">Returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="b7f4b-137">Cette méthode est un alias de la méthode [document. querySelector ()][MDNDocumentQuerySelector] .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-137">This method is an alias for the [document.querySelector()][MDNDocumentQuerySelector] method.</span></span>  

<span data-ttu-id="b7f4b-138">Dans la [figure 5](#figure-5), une référence au premier `<img>` élément du document est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-138">In [Figure 5](#figure-5), a reference to the first `<img>` element in the document is returned.</span></span>  

> ##### <span data-ttu-id="b7f4b-139">Figure 5</span><span class="sxs-lookup"><span data-stu-id="b7f4b-139">Figure 5</span></span>  
> <span data-ttu-id="b7f4b-140">La liste </span><span class="sxs-lookup"><span data-stu-id="b7f4b-140">The</span></span> `$('img')`  
> ![$ ('Img')][ImageElementImg]  

<span data-ttu-id="b7f4b-142">Cliquez avec le bouton droit sur le résultat retourné et sélectionnez **Reveal dans le panneau d’éléments** pour le Rechercher dans le DOM ou **faites défiler l’écran** pour l’afficher sur la page.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-142">Right-click on the returned result and select **Reveal in Elements Panel** to find it in the DOM, or **Scroll in to View** to show it on the page.</span></span>  

<span data-ttu-id="b7f4b-143">Dans la [figure 6](#figure-6), une référence à l’élément actuellement sélectionné est renvoyée et la propriété SRC est affichée.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-143">In [Figure 6](#figure-6), a reference to the currently selected element is returned and the src property is displayed.</span></span>  

> ##### <span data-ttu-id="b7f4b-144">Figure 6</span><span class="sxs-lookup"><span data-stu-id="b7f4b-144">Figure 6</span></span>  
> <span data-ttu-id="b7f4b-145">La liste </span><span class="sxs-lookup"><span data-stu-id="b7f4b-145">The</span></span> `$('img').src`  
> ![$ ('Img'). SRC][ImageElementImgSource]  

<span data-ttu-id="b7f4b-147">Cette méthode prend également en charge un second paramètre, startNode, qui spécifie un élément ou un nœud à partir duquel Rechercher des éléments.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-147">This method also supports a second parameter, startNode, that specifies an "element" or Node from which to search for elements.</span></span>  <span data-ttu-id="b7f4b-148">La valeur par défaut de ce paramètre est `document` .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-148">The default value of this parameter is `document`.</span></span>  

<span data-ttu-id="b7f4b-149">Dans la [figure 7](#figure-7), le premier `img` élément est trouvé après `title--image` et affiche le `src` résultat correct.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-149">In [Figure 7](#figure-7), the first `img` element is found after the `title--image` and displays the `src` properly is returned.</span></span>  

> ##### <span data-ttu-id="b7f4b-150">Figure 7</span><span class="sxs-lookup"><span data-stu-id="b7f4b-150">Figure 7</span></span>  
> <span data-ttu-id="b7f4b-151">$ ('Img', document. querySelector ('title--image')). SRC</span><span class="sxs-lookup"><span data-stu-id="b7f4b-151">The $('img', document.querySelector('title--image')).src</span></span>  
> ![$ ('Img', document. querySelector ('title--image')). SRC][ImageElementImgNodeSource]  

> [!NOTE]
> <span data-ttu-id="b7f4b-153">Si vous utilisez une bibliothèque telle que jQuery qui utilise `$` , cette fonctionnalité est écrasée et `$` correspond à l’implémentation de cette bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-153">If you are using a library such as jQuery that uses `$`, this functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

## <span data-ttu-id="b7f4b-154">Sélecteur de requête</span><span class="sxs-lookup"><span data-stu-id="b7f4b-154">Query Selector All</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="b7f4b-155">Retourne un tableau d’éléments qui correspondent au sélecteur CSS spécifié.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-155">Returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="b7f4b-156">Cette méthode équivaut à appeler la méthode [document. querySelectorAll ()][MDNDocumentQuerySelectorAll] .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-156">This method is equivalent to calling the [document.querySelectorAll()][MDNDocumentQuerySelectorAll] method.</span></span>  

<span data-ttu-id="b7f4b-157">Dans la [figure 8](#figure-8), utilisez `$$()` pour créer un tableau de tous les `<img>` éléments du document actuel et afficher la valeur de la `src` propriété de chaque élément.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-157">In [Figure 8](#figure-8), use `$$()` to create an array of all `<img>` elements in the current document and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

> ##### <span data-ttu-id="b7f4b-158">Figure8</span><span class="sxs-lookup"><span data-stu-id="b7f4b-158">Figure 8</span></span>  
> <span data-ttu-id="b7f4b-159">Utiliser `$$()` pour sélectionner toutes les images du document et afficher les sources</span><span class="sxs-lookup"><span data-stu-id="b7f4b-159">Using `$$()` to select all images in the document and display the sources</span></span>  
> ![Utilisation de $ $ () pour sélectionner toutes les images du document et afficher les sources][ImageArrayElementImgSource]  

<span data-ttu-id="b7f4b-161">Cette méthode prend également en charge un second paramètre, startNode, qui spécifie un élément ou un nœud à partir duquel Rechercher des éléments.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-161">This method also supports a second parameter, startNode, that specifies an element or Node from which to search for elements.</span></span>  <span data-ttu-id="b7f4b-162">La valeur par défaut de ce paramètre est `document` .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-162">The default value of this parameter is `document`.</span></span>  

<span data-ttu-id="b7f4b-163">Dans la [figure 9](#figure-9), une version modifiée de la [figure 8](#figure-8) utilise `$$()` pour créer un tableau de tous les `<img>` éléments qui s’affichent dans le document actuel après le nœud sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-163">In [Figure 9](#figure-9), a modified version of [Figure 8](#figure-8) uses `$$()` to create an array of all `<img>` elements that appear in the current document after the selected Node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

> ##### <span data-ttu-id="b7f4b-164">Figure9</span><span class="sxs-lookup"><span data-stu-id="b7f4b-164">Figure 9</span></span>  
> <span data-ttu-id="b7f4b-165">Utiliser `$$()` pour sélectionner toutes les images qui apparaissent après l' `<div>` élément spécifié dans le document et afficher les sources</span><span class="sxs-lookup"><span data-stu-id="b7f4b-165">Using `$$()` to select all images that appear after the specified `<div>` element in the document and display the sources</span></span>  
> ![Utilisation de $ $ () pour sélectionner toutes les images qui s’affichent après l’élément <div> spécifié dans le document et afficher les sources][ImageArrayElementImgNodeSource]  

> [!NOTE]
> <span data-ttu-id="b7f4b-167">Appuyez sur `Shift` + `Enter` la console pour commencer une nouvelle ligne sans exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-167">Press `Shift`+`Enter` in the console to start a new line without running the script.</span></span>  

## <span data-ttu-id="b7f4b-168">Suivante</span><span class="sxs-lookup"><span data-stu-id="b7f4b-168">XPath</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="b7f4b-169">Renvoie un tableau d’éléments DOM qui correspondent à l’expression XPath spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-169">Returns an array of DOM elements that match the specified XPath expression.</span></span>  

<span data-ttu-id="b7f4b-170">Dans la [figure 10](#figure-10), tous les `<p>` éléments de la page sont renvoyés.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-170">In [Figure 10](#figure-10), all of the `<p>` elements on the page are returned.</span></span>  

```console
$x("//p")
```  

> ##### <span data-ttu-id="b7f4b-171">Figure10</span><span class="sxs-lookup"><span data-stu-id="b7f4b-171">Figure 10</span></span>  
> <span data-ttu-id="b7f4b-172">Utilisation d’un sélecteur XPath</span><span class="sxs-lookup"><span data-stu-id="b7f4b-172">Using an XPath selector</span></span>  
> ![Utilisation d’un sélecteur XPath][ImageArrayXpath]  

<span data-ttu-id="b7f4b-174">Dans la [figure 11](#figure-11), tous les `<p>` éléments contenant des `<a>` éléments sont renvoyés.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-174">In [Figure 11](#figure-11), all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

> ##### <span data-ttu-id="b7f4b-175">Figure11</span><span class="sxs-lookup"><span data-stu-id="b7f4b-175">Figure 11</span></span>  
> <span data-ttu-id="b7f4b-176">Utilisation d’un sélecteur XPath plus complexe</span><span class="sxs-lookup"><span data-stu-id="b7f4b-176">Using a more complicated XPath selector</span></span>  
> ![Utilisation d’un sélecteur XPath plus complexe][ImageArrayXpathChild]  

<span data-ttu-id="b7f4b-178">À l’instar des autres commandes de sélecteur, `$x(path)` possède un deuxième paramètre facultatif, `startNode` qui spécifie un élément ou un nœud à partir duquel Rechercher des éléments.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-178">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or Node from which to search for elements.</span></span>  

> ##### <span data-ttu-id="b7f4b-179">Figure12</span><span class="sxs-lookup"><span data-stu-id="b7f4b-179">Figure 12</span></span>  
> <span data-ttu-id="b7f4b-180">Utilisation d’un sélecteur XPath avec</span><span class="sxs-lookup"><span data-stu-id="b7f4b-180">Using an XPath selector with</span></span> `startNode`  
> ![Utilisation d’un sélecteur XPath avec startNode][ImageArrayXpathNode]  

## <span data-ttu-id="b7f4b-182">supprime</span><span class="sxs-lookup"><span data-stu-id="b7f4b-182">clear</span></span>  

```console
clear()
```  

<span data-ttu-id="b7f4b-183">Efface la console de l’historique.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-183">Clears the console of the history.</span></span>  

```console
clear()
```  

## <span data-ttu-id="b7f4b-184">copy</span><span class="sxs-lookup"><span data-stu-id="b7f4b-184">copy</span></span>  

```console
copy(object)
```  

<span data-ttu-id="b7f4b-185">La `copy(object)` méthode copie une représentation de chaîne de l’objet spécifié dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-185">The `copy(object)` method copies a string representation of the specified object to the clipboard.</span></span>  

```console
copy($0)
```  

## <span data-ttu-id="b7f4b-186">déboguer</span><span class="sxs-lookup"><span data-stu-id="b7f4b-186">debug</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="b7f4b-187">Le [#1050237 problème de chrome][MonorailIssue1050237] effectue le suivi d’un bogue avec la `debug()` fonction.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-187">The [Chromium issue #1050237][MonorailIssue1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="b7f4b-188">Si vous rencontrez ce problème, essayez plutôt d' [utiliser des points d’arrêt][DevtoolsJavascriptBreakpoints] .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-188">If you encounter this issue, try [using breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="b7f4b-189">Lorsque vous demandez la méthode spécifiée, le débogueur est appelé et s’interrompt à l’intérieur de la méthode sur le panneau **sources** pour vous permettre de parcourir le code et de le déboguer.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-189">When you request the specified method, the debugger is invoked and breaks inside the method on the **Sources** panel allowing you to step through the code and debug it.</span></span>  

```console
debug("debug");
```  

> ##### <span data-ttu-id="b7f4b-190">Figure13</span><span class="sxs-lookup"><span data-stu-id="b7f4b-190">Figure 13</span></span>  
> <span data-ttu-id="b7f4b-191">Casser dans une méthode avec</span><span class="sxs-lookup"><span data-stu-id="b7f4b-191">Breaking inside a method with</span></span> `debug()`  
> ![Casser au sein d’une méthode à l’aide du débogage ()][ImageDebugMethod]  

<span data-ttu-id="b7f4b-193">Utilisez `undebug(method)` cette commande pour arrêter l’interruption de la méthode, ou utilisez l’interface utilisateur pour désactiver tous les points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-193">Use `undebug(method)` to stop breaking on the method, or use the UI to disable all breakpoints.</span></span>  

<span data-ttu-id="b7f4b-194">Pour plus d’informations sur les points d’arrêt, voir [suspendre votre code avec des points d’arrêt][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="b7f4b-194">For more information on breakpoints, see [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <span data-ttu-id="b7f4b-195">dir</span><span class="sxs-lookup"><span data-stu-id="b7f4b-195">dir</span></span>  

```console
dir(object)
```  

<span data-ttu-id="b7f4b-196">Affiche une liste de styles d’objet de toutes les propriétés de l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-196">Displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="b7f4b-197">Cette méthode est un alias de la méthode [console. dir ()][MDNConsoleDir] .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-197">This method is an alias for the [console.dir()][MDNConsoleDir] method.</span></span>  

<span data-ttu-id="b7f4b-198">Évaluez `document.head` la console pour afficher le code HTML entre `<head>` les `</head>` balises et.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-198">Evaluate `document.head` in the Console to display the HTML between the `<head>` and `</head>` tags.</span></span>  <span data-ttu-id="b7f4b-199">Dans la [figure 14](#figure-14), une liste de styles d’objet s’affiche après utilisation `console.dir()` dans la console.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-199">In [Figure 14](#figure-14), an object-style listing is displayed after using `console.dir()` in the Console.</span></span>  

```console
document.head;
dir(document.head);
```  

> ##### <span data-ttu-id="b7f4b-200">Figure14</span><span class="sxs-lookup"><span data-stu-id="b7f4b-200">Figure 14</span></span>  
> <span data-ttu-id="b7f4b-201">Journalisation `document.head` avec la `dir()` méthode</span><span class="sxs-lookup"><span data-stu-id="b7f4b-201">Logging `document.head` with `dir()` method</span></span>  
> ![Journalisation du document. Head avec la méthode dir ()][ImageLogObject]  

<span data-ttu-id="b7f4b-203">Pour plus d’informations, consultez l' [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entrée dans l’API de la console.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-203">For more information, see the [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entry in the Console API.</span></span>  

## <span data-ttu-id="b7f4b-204">dirxml</span><span class="sxs-lookup"><span data-stu-id="b7f4b-204">dirxml</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="b7f4b-205">Imprime une représentation XML de l’objet spécifié, comme indiqué dans l’onglet **éléments** .  Cette méthode est équivalente à la méthode [console. DirXML ()][MDNConsoleDirxml] .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-205">Prints an XML representation of the specified object, as seen in the **Elements** tab.  This method is equivalent to the [console.dirxml()][MDNConsoleDirxml] method.</span></span>  

## <span data-ttu-id="b7f4b-206">recherche</span><span class="sxs-lookup"><span data-stu-id="b7f4b-206">inspect</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="b7f4b-207">Ouvre et sélectionne l’élément ou l’objet spécifié dans le panneau approprié: soit le panneau des **éléments** pour les éléments DOM, soit le panneau **mémoire** pour les objets du tas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-207">Opens and selects the specified element or object in the appropriate panel:  either the **Elements** panel for DOM elements or the **Memory** panel for JavaScript heap objects.</span></span>  

<span data-ttu-id="b7f4b-208">Dans la [figure 15](#figure-15), l' `document.body` écran s’ouvre dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-208">In [Figure 15](#figure-15), the `document.body` opens in the **Elements** panel.</span></span>  

```console
inspect(document.body);
```  

> ##### <span data-ttu-id="b7f4b-209">Figure15</span><span class="sxs-lookup"><span data-stu-id="b7f4b-209">Figure 15</span></span>  
> <span data-ttu-id="b7f4b-210">Examen d’un élément avec</span><span class="sxs-lookup"><span data-stu-id="b7f4b-210">Inspecting an element with</span></span> `inspect()`  
> ![Inspecter un élément avec Inspect ()][ImageInspectElement]  

<span data-ttu-id="b7f4b-212">Lorsque vous passez une méthode à inspecter, la méthode ouvre le document dans le panneau **sources** et vous pouvez le consulter.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-212">When passing a method to inspect, the method opens the document up in the **Sources** panel for you to inspect.</span></span>  

## <span data-ttu-id="b7f4b-213">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="b7f4b-213">getEventListeners</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="b7f4b-214">Renvoie les écouteurs d’événements enregistrés sur l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-214">Returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="b7f4b-215">La valeur de retour est un objet qui contient un tableau pour chaque type d’événement inscrit \ (tel que `click` ou `keydown` \).</span><span class="sxs-lookup"><span data-stu-id="b7f4b-215">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="b7f4b-216">Les membres de chaque tableau sont des objets qui décrivent l’écouteur inscrit pour chaque type.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-216">The members of each array are objects that describe the listener registered for each type.</span></span>  <span data-ttu-id="b7f4b-217">Dans la [figure 16](#figure-16), tous les détecteurs d’événements enregistrés sur l’objet document apparaissent.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-217">In [Figure 16](#figure-16), all of the event listeners registered on the document object are listed.</span></span>  

```console
getEventListeners(document);
```  

> ##### <span data-ttu-id="b7f4b-218">Figure16</span><span class="sxs-lookup"><span data-stu-id="b7f4b-218">Figure 16</span></span>  
> <span data-ttu-id="b7f4b-219">Résultat de l’utilisation de</span><span class="sxs-lookup"><span data-stu-id="b7f4b-219">Output of using</span></span> `getEventListeners(document)`  
> ![Sortie de l’utilisation de getEventListeners (document)][ImageGetListeners]  

<span data-ttu-id="b7f4b-221">S’il existe plusieurs écouteurs enregistrés sur l’objet spécifié, le tableau contient un membre pour chaque écouteur.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-221">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="b7f4b-222">Dans la [figure 16](#figure-16), deux écouteurs d’événements sont inscrits dans l’élément document pour l' `click` événement.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-222">In [Figure 16](#figure-16), there are two event listeners registered on the document element for the `click` event.</span></span>  

> ##### <span data-ttu-id="b7f4b-223">Figure17</span><span class="sxs-lookup"><span data-stu-id="b7f4b-223">Figure 17</span></span>  
> <span data-ttu-id="b7f4b-224">Écouteurs multiples</span><span class="sxs-lookup"><span data-stu-id="b7f4b-224">Multiple listeners</span></span>  
> ![Écouteurs multiples][ImageMultipleListeners]  

<span data-ttu-id="b7f4b-226">Vous pouvez également développer chacun des objets suivants pour découvrir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-226">You may further expand each of the following objects to explore the properties.</span></span>  

> ##### <span data-ttu-id="b7f4b-227">Figure 18</span><span class="sxs-lookup"><span data-stu-id="b7f4b-227">Figure 18</span></span>  
> <span data-ttu-id="b7f4b-228">Affichage développé de l’objet Listener</span><span class="sxs-lookup"><span data-stu-id="b7f4b-228">Expanded view of listener object</span></span>  
> ![Affichage développé de l’objet Listener][ImageListenersExpanded]  

## <span data-ttu-id="b7f4b-230">clés</span><span class="sxs-lookup"><span data-stu-id="b7f4b-230">keys</span></span>  

```console
keys(object)
```  

<span data-ttu-id="b7f4b-231">Retourne une matrice contenant les noms des propriétés appartenant à l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-231">Returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="b7f4b-232">Pour obtenir les valeurs associées des mêmes propriétés, utilisez `values()` .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-232">To get the associated values of the same properties, use `values()`.</span></span>  

<span data-ttu-id="b7f4b-233">Par exemple, supposons que votre application définisse l’objet suivant.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-233">For example, suppose your application defined the following object.</span></span>  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

<span data-ttu-id="b7f4b-234">Dans la [figure 19](#figure-19), le résultat suppose qu’il `player1` a été défini dans l’espace de noms global \ (pour la simplicité \) avant de taper `keys(player1)` et `values(player1)` dans la console.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-234">In [Figure 19](#figure-19), the result assumes `player1` was defined in the global namespace \(for simplicity\) prior to typing `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)
```  

```console
values(player1)
```  

> ##### <span data-ttu-id="b7f4b-235">Figure 19</span><span class="sxs-lookup"><span data-stu-id="b7f4b-235">Figure 19</span></span>  
> <span data-ttu-id="b7f4b-236">`keys()`Commandes et `values()`</span><span class="sxs-lookup"><span data-stu-id="b7f4b-236">The `keys()` and `values()` commands</span></span>  
> ![Commandes Keys () et values ()][ImageConsoleKeysValues]  

## <span data-ttu-id="b7f4b-238">moniteur</span><span class="sxs-lookup"><span data-stu-id="b7f4b-238">monitor</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="b7f4b-239">Consigne un message dans la console indiquant le nom de la méthode, ainsi que les arguments transmis à la méthode lors de son appel.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-239">Logs a message to the console that indicates the method name along with the arguments that are passed to the method when it was called.</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

> ##### <span data-ttu-id="b7f4b-240">Figure 20</span><span class="sxs-lookup"><span data-stu-id="b7f4b-240">Figure 20</span></span>  
> <span data-ttu-id="b7f4b-241">La `monitor()` méthode</span><span class="sxs-lookup"><span data-stu-id="b7f4b-241">The `monitor()` method</span></span>  
> ![Méthode Monitor ()][ImageConsoleMonitorSum]  

<span data-ttu-id="b7f4b-243">Utiliser `unmonitor(method)` pour cesser de surveiller.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-243">Use `unmonitor(method)` to cease monitoring.</span></span>  

## <span data-ttu-id="b7f4b-244">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="b7f4b-244">monitorEvents</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="b7f4b-245">Quand l’un des événements spécifiés se produit sur l’objet spécifié, l’objet Event est enregistré dans la console.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-245">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="b7f4b-246">Vous pouvez spécifier un événement unique à surveiller, un tableau d’événements ou l’un des types d’événements génériques mappés à une collection prédéfinie d’événements.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-246">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  <span data-ttu-id="b7f4b-247">Voir [figure 21](#figure-21).</span><span class="sxs-lookup"><span data-stu-id="b7f4b-247">See [Figure 21](#figure-21).</span></span>  

<span data-ttu-id="b7f4b-248">Le code suivant analyse tous les événements de redimensionnement sur l’objet Window.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-248">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

> ##### <span data-ttu-id="b7f4b-249">Figure 21</span><span class="sxs-lookup"><span data-stu-id="b7f4b-249">Figure 21</span></span>  
> <span data-ttu-id="b7f4b-250">Surveiller les événements de redimensionnement d’une fenêtre</span><span class="sxs-lookup"><span data-stu-id="b7f4b-250">Monitoring window resize events</span></span>  
> ![Surveiller les événements de redimensionnement d’une fenêtre][ImageMonitorResize]  

<span data-ttu-id="b7f4b-252">Le code suivant définit un tableau pour contrôler les deux `resize` et les `scroll` événements sur l’objet Window.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-252">The following defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="b7f4b-253">Vous pouvez également spécifier l’un des types d’événements disponibles, qui mappent à des ensembles prédéfinis d’événements.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-253">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="b7f4b-254">Le tableau ci-dessous répertorie les types d’événements disponibles et les mappages d’événements associés.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-254">The table below displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="b7f4b-255">Type d’événement</span><span class="sxs-lookup"><span data-stu-id="b7f4b-255">Event type</span></span> | <span data-ttu-id="b7f4b-256">Événements mappés correspondants</span><span class="sxs-lookup"><span data-stu-id="b7f4b-256">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="b7f4b-257">"Click", "DblClick", "MouseDown", "MouseMove", "mouseout", "MouseOver", "MouseUp", "MouseWheel"</span><span class="sxs-lookup"><span data-stu-id="b7f4b-257">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="b7f4b-258">"KeyDown", "KeyPress", "KeyUp", "textInput"</span><span class="sxs-lookup"><span data-stu-id="b7f4b-258">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="b7f4b-259">"touchcancel", "touchend", "touchmove", "touchstart"</span><span class="sxs-lookup"><span data-stu-id="b7f4b-259">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="b7f4b-260">"Blur", "changement", "Focus", "Réinitialiser", "Redimensionner", "défilement", "sélectionner", "soumission", "zoom"</span><span class="sxs-lookup"><span data-stu-id="b7f4b-260">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="b7f4b-261">Dans la [figure 22](#figure-22), le `key` type d’événement correspondant aux `key` événements dans un champ de texte de saisie est actuellement sélectionné dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-261">In [Figure 22](#figure-22), the `key` event type corresponding to `key` events on an input text field are currently selected in the **Elements** panel.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="b7f4b-262">Dans la [figure 22](#figure-22) , l’exemple de sortie après avoir tapé un caractère dans le champ de texte est affiché.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-262">In [Figure 22](#figure-22) the sample output after typing a character in the text field is displayed.</span></span>  

> ##### <span data-ttu-id="b7f4b-263">Figure 22</span><span class="sxs-lookup"><span data-stu-id="b7f4b-263">Figure 22</span></span>  
> <span data-ttu-id="b7f4b-264">Surveiller les événements de touche</span><span class="sxs-lookup"><span data-stu-id="b7f4b-264">Monitoring key events</span></span>  
> ![Surveiller les événements de touche][ImageMonitorKey]  

## <span data-ttu-id="b7f4b-266">profile</span><span class="sxs-lookup"><span data-stu-id="b7f4b-266">profile</span></span>  

```console
profile([name])
```  

<span data-ttu-id="b7f4b-267">Démarre une session de profil de l’UC JavaScript avec un nom facultatif.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-267">Starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="b7f4b-268">La méthode [profileEnd ()](#profileend) termine le profil et affiche les résultats dans le panneau **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-268">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** panel.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="b7f4b-269">Exécutez la `profile()` méthode pour démarrer le profilage.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-269">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="b7f4b-270">Exécutez la méthode [profileEnd ()](#profileend) pour arrêter le profilage et afficher les résultats dans le panneau **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-270">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** panel.</span></span>  

<span data-ttu-id="b7f4b-271">Les profils risquent également d’être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-271">Profiles may also be nested.</span></span>  <span data-ttu-id="b7f4b-272">Dans la [figure 23](#figure-23) , le résultat est le même quel que soit l’ordre.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-272">In [Figure 23](#figure-23) the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="b7f4b-273">Les profils d’UC multiples peuvent fonctionner en même temps et vous n’avez pas besoin de les clôturer dans l’ordre de création.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-273">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="b7f4b-274">profileEnd</span><span class="sxs-lookup"><span data-stu-id="b7f4b-274">profileEnd</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="b7f4b-275">Effectue une session de profilage de l’UC JavaScript et affiche les résultats dans le panneau **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-275">Completes a JavaScript CPU profiling session and displays the results in the **Memory** panel.</span></span>  <span data-ttu-id="b7f4b-276">Vous devez exécuter la méthode [Profile ()](#profile) .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-276">You must be running the [profile()](#profile) method.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="b7f4b-277">Exécutez la méthode [Profile ()](#profile) pour démarrer le profilage.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-277">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="b7f4b-278">Exécutez la `profileEnd()` méthode pour arrêter le profilage et afficher les résultats dans le panneau **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-278">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** panel.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="b7f4b-279">Les profils risquent également d’être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-279">Profiles may also be nested.</span></span>  <span data-ttu-id="b7f4b-280">Dans la [figure 23](#figure-23) , le résultat est le même quel que soit l’ordre.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-280">In [Figure 23](#figure-23) the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="b7f4b-281">Le résultat s’affiche sous la forme d’un instantané de tas dans le panneau **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-281">The result appears as a Heap Snapshot in the **Memory** panel.</span></span>  

> ##### <span data-ttu-id="b7f4b-282">Figure 23</span><span class="sxs-lookup"><span data-stu-id="b7f4b-282">Figure 23</span></span>  
> <span data-ttu-id="b7f4b-283">Profils groupés</span><span class="sxs-lookup"><span data-stu-id="b7f4b-283">Grouped profiles</span></span>  
> ![Profils groupés][ImageGroupedProfiles]  

> [!NOTE]
> <span data-ttu-id="b7f4b-285">Les profils d’UC multiples peuvent fonctionner en même temps et vous n’avez pas besoin de les clôturer dans l’ordre de création.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-285">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="b7f4b-286">tabulaire</span><span class="sxs-lookup"><span data-stu-id="b7f4b-286">table</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="b7f4b-287">Enregistre les données d’objet avec une mise en forme de tableau en fonction de l’objet de données avec des en-têtes de colonnes facultatifs.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-287">Logs object data with table formatting based upon the data object in with optional column headings.</span></span>  <span data-ttu-id="b7f4b-288">Dans la [figure 24](#figure-24), une liste de noms utilisant une table dans la console s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-288">In [Figure 24](#figure-24), a list of names using a table in the console is displayed.</span></span>  

```console
var names = {
    0:  {
        firstName:  "John",
        lastName:  "Smith"
    },
    1:  {
        firstName:  "Jane",
        lastName:  "Doe"
    }
};
table(names);
```  

> ##### <span data-ttu-id="b7f4b-289">Figure 24</span><span class="sxs-lookup"><span data-stu-id="b7f4b-289">Figure 24</span></span>  
> <span data-ttu-id="b7f4b-290">La `table()` méthode</span><span class="sxs-lookup"><span data-stu-id="b7f4b-290">The `table()` method</span></span>  
> ![Méthode table ()][ImageConsoleTable]  

## <span data-ttu-id="b7f4b-292">déboguer</span><span class="sxs-lookup"><span data-stu-id="b7f4b-292">undebug</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="b7f4b-293">Arrête le débogage de la méthode spécifiée de telle sorte que lorsque la méthode est appelée, le débogueur n’est plus appelé.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-293">Stops the debugging of the specified method so that when the method is called, the debugger is no longer invoked.</span></span>  

```console
undebug(getData);
```  

## <span data-ttu-id="b7f4b-294">ne plus surveiller</span><span class="sxs-lookup"><span data-stu-id="b7f4b-294">unmonitor</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="b7f4b-295">Arrête l’analyse de la méthode spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-295">Stops the monitoring of the specified method.</span></span>  <span data-ttu-id="b7f4b-296">Ce mode est utilisé en concert avec la méthode [Monitor ()](#monitor) .</span><span class="sxs-lookup"><span data-stu-id="b7f4b-296">This is used in concert with the [monitor()](#monitor) method.</span></span>  

```console
unmonitor(getData);
```  

## <span data-ttu-id="b7f4b-297">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="b7f4b-297">unmonitorEvents</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="b7f4b-298">Arrête de surveiller les événements relatifs aux objets et aux événements spécifiés.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-298">Stops monitoring events for the specified object and events.</span></span>  <span data-ttu-id="b7f4b-299">Par exemple, la commande suivante arrête tout le suivi des événements sur l’objet Window.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-299">For example, the following stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="b7f4b-300">Vous pouvez également cesser de surveiller de manière sélective des événements spécifiques sur un objet.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-300">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="b7f4b-301">Par exemple, le code suivant commence à surveiller tous les `mouse` événements de l’élément actuellement sélectionné, puis cesse de surveiller les `mousemove` événements (il peut s’avérer utile de réduire le bruit dans la sortie de la console).</span><span class="sxs-lookup"><span data-stu-id="b7f4b-301">For example, the following code starts monitoring all `mouse` events on the currently selected element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <span data-ttu-id="b7f4b-302">doubl</span><span class="sxs-lookup"><span data-stu-id="b7f4b-302">values</span></span>  

```console
values(object)
```  

<span data-ttu-id="b7f4b-303">Renvoie une matrice contenant les valeurs de toutes les propriétés de l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="b7f4b-303">Returns an array containing the values of all properties belonging to the specified object.</span></span>  

```console
values(object);
```  

<!--   -->  



<!-- image links -->  

[ImageRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-arithmatic.msft.png "Figure 1: $ _ est l’expression la plus récemment évaluée"  
[ImageChangedRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-array-length.msft.png "Figure 2: $ _ change lorsque de nouvelles commandes sont évaluées"  
[ImageElement0]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$0.msft.png "Figure 3: $0"  
[ImageElement1]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$1.msft.png "Figure 4: $1"  
[ImageElementImg]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image.msft.png "Figure 5: $ ('img')"  
[ImageElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-source.msft.png "Figure 6: $ ('img'). SRC"  
[ImageElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-source.msft.png "Figure 7: $ ('img', document. querySelector ('title--image')). SRC"  
[ImageArrayElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-all.msft.png "Figure 8: utilisation de $ $ () pour sélectionner toutes les images du document et afficher les sources"  
[ImageArrayElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-all.msft.png "Figure 9: utilisation de $ $ () pour sélectionner toutes les images qui s’affichent après l’élément <div> spécifié dans le document et afficher les sources"  
[ImageArrayXpath]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath.msft.png "Figure 10: utilisation d’un sélecteur XPath"  
[ImageArrayXpathChild]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-sub-element.msft.png "Figure 11: utilisation d’un sélecteur XPath plus complexe"  
[ImageArrayXpathNode]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-startnode.msft.png "Figure 12: utilisation d’un sélecteur XPath avec startNode"  
[ImageDebugMethod]: /microsoft-edge/devtools-guide-chromium/media/console-debug-text.msft.png "Figure 13: rupture au sein d’une méthode à l’aide du débogage ()"  
[ImageLogObject]: /microsoft-edge/devtools-guide-chromium/media/console-dir-document-head-expanded.msft.png "Figure 14: enregistrement du document. Body avec la méthode dir ()"  
[ImageInspectElement]: /microsoft-edge/devtools-guide-chromium/media/console-inspect-document-body.msft.png "Figure 15: examen d’un élément avec Inspect ()"  
[ImageGetListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document.msft.png "Figure 16: sortie de l’utilisation de getEventListeners (document)"  
[ImageMultipleListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png "Figure 17: écouteurs multiples"  
[ImageListenersExpanded]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png "Figure 18: vue développée de l’objet Listener"  
[ImageConsoleKeysValues]: /microsoft-edge/devtools-guide-chromium/media/console-keys-values.msft.png "Figure 19: commandes Keys () et values ()"  
[ImageConsoleMonitorSum]: /microsoft-edge/devtools-guide-chromium/media/console-function-monitor-sum.msft.png "Figure 20: méthode Monitor ()"  
[ImageMonitorResize]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-resize-window.msft.png "Figure 21: surveiller les événements de redimensionnement d’une fenêtre"  
[ImageMonitorKey]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-type-t-y.msft.png "Figure 22: surveiller les événements de touche"  
[ImageGroupedProfiles]: /microsoft-edge/devtools-guide-chromium/media/console-memory-multiple-cpu-profiles.msft.png "Figure 23: profils groupés"  
[ImageConsoleTable]: /microsoft-edge/devtools-guide-chromium/media/console-table-display.msft.png "Figure 24: méthode table ()"  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Référence sur les API de la console"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "Rép."  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Accélérer le runtime JavaScript"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console. dir () | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console. DirXML () | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document. querySelector () | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document. querySelectorAll () | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Problème 1050237: le débogage (fonction) ne fonctionne pas | Monorail"  

> [!NOTE]
> <span data-ttu-id="b7f4b-337">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b7f4b-337">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b7f4b-338">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/utilities) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="b7f4b-338">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="b7f4b-340">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b7f4b-340">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
