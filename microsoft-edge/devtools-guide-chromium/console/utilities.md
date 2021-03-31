---
description: Référence des commandes pratiques disponibles dans la console Microsoft Edge DevTools.
title: Référence de l’API des utilitaires de console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: e7253bf5402a03d1659f56ba083bb87e93b3af38
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398825"
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

# <a name="console-utilities-api-reference"></a><span data-ttu-id="6ca9b-104">Référence de l’API des utilitaires de console</span><span class="sxs-lookup"><span data-stu-id="6ca9b-104">Console Utilities API reference</span></span>  

<span data-ttu-id="6ca9b-105">L’API des utilitaires de console contient une collection de commandes pratiques pour effectuer des tâches courantes : sélection et inspection des éléments DOM, affichage de données dans un format lisible, arrêt et démarrage du profileur et surveillance des événements DOM.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-105">The Console Utilities API contains a collection of convenience commands for performing common tasks:  selecting and inspecting DOM elements, displaying data in readable format, stopping and starting the profiler, and monitoring DOM events.</span></span>  

> [!WARNING]
> <span data-ttu-id="6ca9b-106">Les commandes suivantes fonctionnent uniquement dans la console Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-106">The following commands only work in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="6ca9b-107">Les commandes ne fonctionnent pas si elles sont exécutés à partir de vos scripts.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-107">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="6ca9b-108">Pour le reste des méthodes et méthodes, accédez à Référence de `console.log()` `console.error()` `console.*` [l’API console.][DevToolsConsoleApi]</span><span class="sxs-lookup"><span data-stu-id="6ca9b-108">For the `console.log()` and `console.error()` methods the rest of the `console.*` methods, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  

## <a name="recently-evaluated-expression"></a><span data-ttu-id="6ca9b-109">Expression récemment évaluée</span><span class="sxs-lookup"><span data-stu-id="6ca9b-109">Recently Evaluated Expression</span></span>  

```console
$_
```  

<span data-ttu-id="6ca9b-110">Renvoie la valeur de l’expression la plus récemment évaluée.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-110">Returns the value of the most recently evaluated expression.</span></span>  

<span data-ttu-id="6ca9b-111">Dans la figure suivante, une expression simple \( `2 + 2` \) est évaluée.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-111">In the following figure, a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="6ca9b-112">La `$_` propriété est ensuite évaluée, qui contient la même valeur.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-112">The `$_` property is then evaluated, which contains the same value.</span></span>  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ est la dernière expression évaluée" lightbox="../media/console-arithmatic.msft.png":::
   <span data-ttu-id="6ca9b-114">Figure 1 :  `$_` est l’expression la plus récemment évaluée</span><span class="sxs-lookup"><span data-stu-id="6ca9b-114">Figure 1:  `$_` is the most recently evaluated expression</span></span>  
:::image-end:::  

<span data-ttu-id="6ca9b-115">Dans la figure suivante, l’expression évaluée contient initialement un tableau de noms.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-115">In the following figure, the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="6ca9b-116">Évaluation pour trouver la longueur du tableau, la valeur stockée dans les modifications pour devenir la dernière `$_.length` `$_` expression évaluée, `4` .</span><span class="sxs-lookup"><span data-stu-id="6ca9b-116">Evaluating `$_.length` to find the length of the array, the value stored in `$_` changes to become the latest evaluated expression, `4`.</span></span>  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$_ change lorsque de nouvelles commandes sont évaluées" lightbox="../media/console-array-length.msft.png":::
   <span data-ttu-id="6ca9b-118">Figure 2 :  `$_` modifications lors de l’évaluation de nouvelles commandes</span><span class="sxs-lookup"><span data-stu-id="6ca9b-118">Figure 2:  `$_` changes when new commands are evaluated</span></span>  
:::image-end:::  

## <a name="recently-chosen-element-or-javascript-object"></a><span data-ttu-id="6ca9b-119">Élément récemment choisi ou objet JavaScript</span><span class="sxs-lookup"><span data-stu-id="6ca9b-119">Recently Chosen Element Or JavaScript Object</span></span>  

```console
$0
```  

<span data-ttu-id="6ca9b-120">Renvoie l’élément ou l’objet JavaScript sélectionné le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-120">Returns the most recently selected element or JavaScript object.</span></span>  `$1` <span data-ttu-id="6ca9b-121">renvoie la deuxième dernière sélection, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-121">returns the second most recently selected one, and so on.</span></span>  <span data-ttu-id="6ca9b-122">Les commandes , , et les commandes fonctionnent comme une référence historique aux cinq derniers éléments DOM inspectés dans l’outil Elements ou aux cinq derniers objets de tas `$0` `$1` `$2` `$3` `$4` JavaScript sélectionnés   dans l’outil Mémoire.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-122">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** tool or the last five JavaScript heap objects selected in the **Memory** tool.</span></span>  

:::row:::
   :::column span="1":::
      ```console
      $0
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $1
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $2
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ```console
      $3
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $4
      ```  
   :::column-end:::
   :::column span="1":::
   :::column-end:::
:::row-end:::  

<span data-ttu-id="6ca9b-123">Dans la figure suivante, un `img` élément est sélectionné dans l’outil **Elements.**</span><span class="sxs-lookup"><span data-stu-id="6ca9b-123">In the following figure, an `img` element is selected in the **Elements** tool.</span></span>  <span data-ttu-id="6ca9b-124">Dans le caisse **de** la console, `$0` a été évalué et affiche le même élément.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-124">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="La valeur $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   <span data-ttu-id="6ca9b-126">Figure 3 : Le</span><span class="sxs-lookup"><span data-stu-id="6ca9b-126">Figure 3:  The</span></span> `$0`  
:::image-end:::  

<span data-ttu-id="6ca9b-127">Dans la figure suivante, l’image montre un autre élément sélectionné dans la même page.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-127">In the following figure, the image shows a different element selected in the same page.</span></span>  <span data-ttu-id="6ca9b-128">L’élément sélectionné fait désormais référence à l’élément nouvellement sélectionné, tandis qu’il renvoie `$0` `$1` l’élément précédemment sélectionné.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-128">The `$0` now refers to the newly selected element, while `$1` returns the previously selected one.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="La valeur $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   <span data-ttu-id="6ca9b-130">Figure 4 : Le</span><span class="sxs-lookup"><span data-stu-id="6ca9b-130">Figure 4:  The</span></span> `$1`  
:::image-end:::  

## <a name="query-selector"></a><span data-ttu-id="6ca9b-131">Sélecteur de requêtes</span><span class="sxs-lookup"><span data-stu-id="6ca9b-131">Query Selector</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="6ca9b-132">Renvoie la référence au premier élément DOM avec le sélecteur CSS spécifié.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-132">Returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="6ca9b-133">Cette méthode est un alias de la [méthode document.querySelector().][MDNDocumentQuerySelector]</span><span class="sxs-lookup"><span data-stu-id="6ca9b-133">This method is an alias for the [document.querySelector()][MDNDocumentQuerySelector] method.</span></span>  

<span data-ttu-id="6ca9b-134">Dans la figure suivante, une référence au premier `<img>` élément du document est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-134">In the following figure, a reference to the first `<img>` element in the document is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$('img')" lightbox="../media/console-element-selector-image.msft.png":::
   <span data-ttu-id="6ca9b-136">Figure 5 : Le</span><span class="sxs-lookup"><span data-stu-id="6ca9b-136">Figure 5:  The</span></span> `$('img')`  
:::image-end:::  

<span data-ttu-id="6ca9b-137">Pointez sur le résultat renvoyé, ouvrez le menu contextuel \(clic droit\), puis  choisissez **Révéler** dans le panneau Éléments pour le trouver dans le DOM ou faites défiler vers l’affichage pour l’afficher sur la page.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-137">Hover on the returned result, open the contextual menu \(right-click\), and choose **Reveal in Elements Panel** to find it in the DOM or **Scroll in to View** to show it on the page.</span></span>  

<span data-ttu-id="6ca9b-138">Dans la figure suivante, une référence à l’élément actuellement sélectionné est renvoyée et la propriété src est affichée.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-138">In the following figure, a reference to the currently selected element is returned and the src property is displayed.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="Le $('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   <span data-ttu-id="6ca9b-140">Figure 6 : Le</span><span class="sxs-lookup"><span data-stu-id="6ca9b-140">Figure 6:  The</span></span> `$('img').src`  
:::image-end:::  

<span data-ttu-id="6ca9b-141">Cette méthode prend également en charge un deuxième paramètre, startNode, qui spécifie un « élément » ou un nœud à partir duquel rechercher des éléments.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-141">This method also supports a second parameter, startNode, that specifies an "element" or Node from which to search for elements.</span></span>  <span data-ttu-id="6ca9b-142">La valeur par défaut du paramètre est `document` .</span><span class="sxs-lookup"><span data-stu-id="6ca9b-142">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="6ca9b-143">Dans la figure suivante, le premier élément est trouvé après l’élément et l’affichage correct `img` `title--image` est `src` renvoyé.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-143">In the following figure, the first `img` element is found after the `title--image` and displays the `src` properly is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="The $('img', document.querySelector('title--image')).src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   <span data-ttu-id="6ca9b-145">Figure 7 : Le</span><span class="sxs-lookup"><span data-stu-id="6ca9b-145">Figure 7:  The</span></span> `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="6ca9b-146">Si vous utilisez une bibliothèque telle que jQuery qui utilise , la fonctionnalité est écrasée et correspond à l’implémentation de `$` `$` cette bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-146">If you are using a library such as jQuery that uses `$`, the functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

## <a name="query-selector-all"></a><span data-ttu-id="6ca9b-147">Sélecteur de requêtes tous</span><span class="sxs-lookup"><span data-stu-id="6ca9b-147">Query Selector All</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="6ca9b-148">Renvoie un tableau d’éléments qui correspondent au sélecteur CSS spécifié.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-148">Returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="6ca9b-149">Cette méthode équivaut à l’exécution de la [méthode document.querySelectorAll().][MDNDocumentQuerySelectorAll]</span><span class="sxs-lookup"><span data-stu-id="6ca9b-149">This method is equivalent to running the [document.querySelectorAll()][MDNDocumentQuerySelectorAll] method.</span></span>  

<span data-ttu-id="6ca9b-150">Dans l’exemple de code et la figure suivants, utilisez pour créer un tableau de tous les éléments du document actuel et afficher la valeur de la propriété `$$()` `<img>` pour chaque `src` élément.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-150">In the following code sample and figure, use `$$()` to create an array of all `<img>` elements in the current document and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Utilisation de $$() pour sélectionner toutes les images du document et afficher les sources" lightbox="../media/console-element-selector-image-all.msft.png":::
   <span data-ttu-id="6ca9b-152">Figure 8 : Utilisation `$$()` pour sélectionner toutes les images du document et afficher les sources</span><span class="sxs-lookup"><span data-stu-id="6ca9b-152">Figure 8:  Using `$$()` to select all images in the document and display the sources</span></span>  
:::image-end:::  

<span data-ttu-id="6ca9b-153">Cette méthode prend également en charge un deuxième paramètre, startNode, qui spécifie un élément ou un nœud à partir duquel rechercher des éléments.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-153">This method also supports a second parameter, startNode, that specifies an element or Node from which to search for elements.</span></span>  <span data-ttu-id="6ca9b-154">La valeur par défaut du paramètre est `document` .</span><span class="sxs-lookup"><span data-stu-id="6ca9b-154">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="6ca9b-155">Dans l’exemple de code et la figure suivants, une version modifiée de l’exemple de code et de la figure précédents utilise pour créer un tableau de tous les éléments qui apparaissent dans le document actuel après le nœud `$$()` `<img>` sélectionné.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-155">In the following code sample and figure, a modified version of the previous code sample and figure uses `$$()` to create an array of all `<img>` elements that appear in the current document after the selected Node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Using $$() to select all images that appear after the specified <div> element in the document and display the sources" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   <span data-ttu-id="6ca9b-157">Figure 9 : Utilisation pour sélectionner toutes les images qui apparaissent après l’élément spécifié dans le document et afficher `$$()` `<div>` les sources</span><span class="sxs-lookup"><span data-stu-id="6ca9b-157">Figure 9:  Using `$$()` to select all images that appear after the specified `<div>` element in the document and display the sources</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="6ca9b-158">Sélectionnez `Shift` + `Enter` dans la console pour démarrer une nouvelle ligne sans l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-158">Select `Shift`+`Enter` in the console to start a new line without running the script.</span></span>  

## <a name="xpath"></a><span data-ttu-id="6ca9b-159">XPath</span><span class="sxs-lookup"><span data-stu-id="6ca9b-159">XPath</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="6ca9b-160">Renvoie un tableau d’éléments DOM qui correspondent à l’expression XPath spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-160">Returns an array of DOM elements that match the specified XPath expression.</span></span>  

<span data-ttu-id="6ca9b-161">Dans l’exemple de code et la figure suivants, tous les éléments `<p>` de la page sont renvoyés.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-161">In the following code sample and figure, all of the `<p>` elements on the page are returned.</span></span>  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Utilisation d’un sélecteur XPath" lightbox="../media/console-array-xpath.msft.png":::
   <span data-ttu-id="6ca9b-163">Figure 10 : Utilisation d’un sélecteur XPath</span><span class="sxs-lookup"><span data-stu-id="6ca9b-163">Figure 10:  Using an XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="6ca9b-164">Dans l’exemple de code et la figure suivants, tous les éléments `<p>` qui contiennent des `<a>` éléments sont renvoyés.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-164">In the following code sample and figure, all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Utilisation d’un sélecteur XPath plus compliqué" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   <span data-ttu-id="6ca9b-166">Figure 11 : Utilisation d’un sélecteur XPath plus compliqué</span><span class="sxs-lookup"><span data-stu-id="6ca9b-166">Figure 11:  Using a more complicated XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="6ca9b-167">Comme pour les autres commandes de sélecteur, possède un deuxième paramètre facultatif, qui spécifie un élément ou un nœud à partir duquel rechercher `$x(path)` `startNode` des éléments.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-167">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or Node from which to search for elements.</span></span>  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Utilisation d’un sélecteur XPath avec startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   <span data-ttu-id="6ca9b-169">Figure 12 : Utilisation d’un sélecteur XPath avec</span><span class="sxs-lookup"><span data-stu-id="6ca9b-169">Figure 12:  Using an XPath selector with</span></span> `startNode`  
:::image-end:::  

## <a name="clear"></a><span data-ttu-id="6ca9b-170">clear</span><span class="sxs-lookup"><span data-stu-id="6ca9b-170">clear</span></span>  

```console
clear()
```  

<span data-ttu-id="6ca9b-171">Cette commande permet d’effacer la console de l’historique.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-171">Clears the console of the history.</span></span>  

```console
clear()
```  

## <a name="copy"></a><span data-ttu-id="6ca9b-172">copy</span><span class="sxs-lookup"><span data-stu-id="6ca9b-172">copy</span></span>  

```console
copy(object)
```  

<span data-ttu-id="6ca9b-173">La `copy(object)` méthode copie une représentation sous la chaîne de l’objet spécifié dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-173">The `copy(object)` method copies a string representation of the specified object to the clipboard.</span></span>  

```console
copy($0)
```  

## <a name="debug"></a><span data-ttu-id="6ca9b-174">déboguer</span><span class="sxs-lookup"><span data-stu-id="6ca9b-174">debug</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="6ca9b-175">Le [problème Chromium #1050237][MonorailIssue1050237] suivi d’un bogue avec la `debug()` fonction.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-175">The [Chromium issue #1050237][MonorailIssue1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="6ca9b-176">Si vous rencontrez le problème, essayez plutôt [d’utiliser des points d’arrêt.][DevtoolsJavascriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="6ca9b-176">If you encounter the issue, try [using breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="6ca9b-177">Lorsque vous demandez la méthode spécifiée, le déboguer est appelé et s’interrompt à l’intérieur de la méthode sur l’outil **Sources,** ce qui vous permet d’aller pas à pas dans le code et de le déboguer.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-177">When you request the specified method, the debugger is invoked and breaks inside the method on the **Sources** tool allowing you to step through the code and debug it.</span></span>  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Rupture à l’intérieur d’une méthode avec débogage()" lightbox="../media/console-debug-text.msft.png":::
   <span data-ttu-id="6ca9b-179">Figure 13 : Rupture à l’intérieur d’une méthode avec</span><span class="sxs-lookup"><span data-stu-id="6ca9b-179">Figure 13:  Breaking inside a method with</span></span> `debug()`  
:::image-end:::  

<span data-ttu-id="6ca9b-180">Permet d’arrêter la rupture de la méthode ou d’utiliser `undebug(method)` l’interface utilisateur pour désactiver tous les points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-180">Use `undebug(method)` to stop breaking on the method, or use the UI to disable all breakpoints.</span></span>  

<span data-ttu-id="6ca9b-181">Pour plus d’informations sur les points d’arrêt, accédez à [Suspendre votre code avec des points d’arrêt.][DevToolsJavascriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="6ca9b-181">For more information on breakpoints, navigate to [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <a name="dir"></a><span data-ttu-id="6ca9b-182">dir</span><span class="sxs-lookup"><span data-stu-id="6ca9b-182">dir</span></span>  

```console
dir(object)
```  

<span data-ttu-id="6ca9b-183">Affiche une liste de style objet de toutes les propriétés de l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-183">Displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="6ca9b-184">Cette méthode est un alias de la [méthode console.dir().][MDNConsoleDir]</span><span class="sxs-lookup"><span data-stu-id="6ca9b-184">This method is an alias for the [console.dir()][MDNConsoleDir] method.</span></span>  

<span data-ttu-id="6ca9b-185">Évaluez `document.head` dans la console pour afficher le code HTML entre les `<head>` `</head>` balises et les balises.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-185">Evaluate `document.head` in the Console to display the HTML between the `<head>` and `</head>` tags.</span></span>  <span data-ttu-id="6ca9b-186">Dans l’exemple de code et la figure suivants, une liste de style objet s’affiche après l’utilisation `console.dir()` dans la console.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-186">In the following code sample and figure, an object-style listing is displayed after using `console.dir()` in the Console.</span></span>  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Journalisation de document.head avec la méthode dir()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   <span data-ttu-id="6ca9b-188">Figure 14 : Journalisation `document.head` avec `dir()` méthode</span><span class="sxs-lookup"><span data-stu-id="6ca9b-188">Figure 14:  Logging `document.head` with `dir()` method</span></span>  
:::image-end:::  

<span data-ttu-id="6ca9b-189">Pour plus d’informations, accédez [`console.dir()`][DevToolsConsoleApiConsoleDirObject] à l’entrée dans l’API console.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-189">For more information, navigate to [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entry in the Console API.</span></span>  

## <a name="dirxml"></a><span data-ttu-id="6ca9b-190">dirxml</span><span class="sxs-lookup"><span data-stu-id="6ca9b-190">dirxml</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="6ca9b-191">Imprime une représentation XML de l’objet spécifié, tel qu’il est affiché dans **l’outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="6ca9b-191">Prints an XML representation of the specified object, as displayed in the **Elements** tool.</span></span>  <span data-ttu-id="6ca9b-192">Cette méthode est équivalente à la [méthode console.dirxml().][MDNConsoleDirxml]</span><span class="sxs-lookup"><span data-stu-id="6ca9b-192">This method is equivalent to the [console.dirxml()][MDNConsoleDirxml] method.</span></span>  

## <a name="inspect"></a><span data-ttu-id="6ca9b-193">inspect</span><span class="sxs-lookup"><span data-stu-id="6ca9b-193">inspect</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="6ca9b-194">Ouvre et sélectionne l’élément ou l’objet spécifié dans le panneau approprié  : l’outil **Elements** pour les éléments DOM ou l’outil Mémoire pour les objets tas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-194">Opens and selects the specified element or object in the appropriate panel:  either the **Elements** tool for DOM elements or the **Memory** tool for JavaScript heap objects.</span></span>  

<span data-ttu-id="6ca9b-195">Dans l’exemple de code et la figure `document.body` suivants, l’élément s’ouvre dans **l’outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="6ca9b-195">In the following code sample and figure, the `document.body` opens in the **Elements** tool.</span></span>  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Inspection d’un élément avec inspect()" lightbox="../media/console-inspect-document-body.msft.png":::
   <span data-ttu-id="6ca9b-197">Figure 15 : Inspection d’un élément avec</span><span class="sxs-lookup"><span data-stu-id="6ca9b-197">Figure 15:  Inspecting an element with</span></span> `inspect()`  
:::image-end:::  

<span data-ttu-id="6ca9b-198">Lors de la transmission d’une méthode à inspecter, la méthode ouvre le document dans l’outil **Sources** que vous pouvez inspecter.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-198">When passing a method to inspect, the method opens the document in the **Sources** tool for you to inspect.</span></span>  

## <a name="geteventlisteners"></a><span data-ttu-id="6ca9b-199">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="6ca9b-199">getEventListeners</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="6ca9b-200">Renvoie les écouteurs d’événements enregistrés sur l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-200">Returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="6ca9b-201">La valeur de retour est un objet qui contient un tableau pour chaque type d’événement enregistré \(par exemple `click` ou `keydown` \).</span><span class="sxs-lookup"><span data-stu-id="6ca9b-201">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="6ca9b-202">Les membres de chaque tableau sont des objets qui décrivent l’écoute enregistrée pour chaque type.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-202">The members of each array are objects that describe the listener registered for each type.</span></span>  <span data-ttu-id="6ca9b-203">Dans l’exemple de code suivant, tous les écouteurs d’événements enregistrés sur l’objet document sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-203">In the following code sample figure, all of the event listeners registered on the document object are listed.</span></span>  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Sortie de l’utilisation de getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   <span data-ttu-id="6ca9b-205">Figure 16 : Résultat de l’utilisation</span><span class="sxs-lookup"><span data-stu-id="6ca9b-205">Figure 16:  The result of using</span></span> `getEventListeners(document)`  
:::image-end:::  

<span data-ttu-id="6ca9b-206">Si plusieurs listener sont inscrits sur l’objet spécifié, le tableau contient un membre pour chaque listener.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-206">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="6ca9b-207">Dans la figure suivante, deux écouteurs d’événements sont enregistrés sur l’élément de document pour `click` l’événement.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-207">In the following figure, there are two event listeners registered on the document element for the `click` event.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Plusieurs écouteurs" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   <span data-ttu-id="6ca9b-209">Figure 17 : Plusieurs écouteurs</span><span class="sxs-lookup"><span data-stu-id="6ca9b-209">Figure 17:  Multiple listeners</span></span>  
:::image-end:::  

<span data-ttu-id="6ca9b-210">Vous pouvez développer chacun des objets suivants pour explorer les propriétés.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-210">You may further expand each of the following objects to explore the properties.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Vue étendue de l’objet d’écoute" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   <span data-ttu-id="6ca9b-212">Figure 18 : Vue étendue de l’objet d’écoute</span><span class="sxs-lookup"><span data-stu-id="6ca9b-212">Figure 18:  Expanded view of listener object</span></span>  
:::image-end:::  

## <a name="keys"></a><span data-ttu-id="6ca9b-213">clés</span><span class="sxs-lookup"><span data-stu-id="6ca9b-213">keys</span></span>  

```console
keys(object)
```  

<span data-ttu-id="6ca9b-214">Renvoie un tableau contenant les noms des propriétés appartenant à l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-214">Returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="6ca9b-215">Pour obtenir les valeurs associées des mêmes propriétés, utilisez `values()` .</span><span class="sxs-lookup"><span data-stu-id="6ca9b-215">To get the associated values of the same properties, use `values()`.</span></span>  

<span data-ttu-id="6ca9b-216">Par exemple, supposons que votre application a défini l’objet suivant.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-216">For example, suppose your application defined the following object.</span></span>  

```console
var player1 =   
```  

<span data-ttu-id="6ca9b-217">Dans les exemples de code et la figure suivants, le résultat suppose qu’il a été défini dans l’espace de noms global \(par souci de simplicité\) avant la saisie et dans `player1` `keys(player1)` la `values(player1)` console.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-217">In the following code samples and figure, the result assumes `player1` was defined in the global namespace \(for simplicity\) prior to typing `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Commandes keys() et values()" lightbox="../media/console-keys-values.msft.png":::
   <span data-ttu-id="6ca9b-219">Figure 19 : Commandes `keys()` `values()` et commandes</span><span class="sxs-lookup"><span data-stu-id="6ca9b-219">Figure 19:  The `keys()` and `values()` commands</span></span>  
:::image-end:::  

## <a name="monitor"></a><span data-ttu-id="6ca9b-220">moniteur</span><span class="sxs-lookup"><span data-stu-id="6ca9b-220">monitor</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="6ca9b-221">Enregistre un message dans la console qui indique le nom de la méthode ainsi que les arguments transmis à la méthode lors de son appel.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-221">Logs a message to the console that indicates the method name along with the arguments that are passed to the method when it was called.</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="Méthode monitor()" lightbox="../media/console-function-monitor-sum.msft.png":::
   <span data-ttu-id="6ca9b-223">Figure 20 : `monitor()` Méthode</span><span class="sxs-lookup"><span data-stu-id="6ca9b-223">Figure 20:  The `monitor()` method</span></span>  
:::image-end:::  

<span data-ttu-id="6ca9b-224">À utiliser `unmonitor(method)` pour cesser la surveillance.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-224">Use `unmonitor(method)` to cease monitoring.</span></span>  

## <a name="monitorevents"></a><span data-ttu-id="6ca9b-225">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="6ca9b-225">monitorEvents</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="6ca9b-226">Lorsqu’un des événements spécifiés se produit sur l’objet spécifié, l’objet d’événement est consigné dans la console.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-226">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="6ca9b-227">Vous pouvez spécifier un seul événement à surveiller, un tableau d’événements ou l’un des types d’événements génériques qui sont mappés à une collection prédéfinie d’événements.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-227">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  <span data-ttu-id="6ca9b-228">Examinez l’exemple de code et la figure suivants.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-228">Review the following code sample and figure.</span></span>  

<span data-ttu-id="6ca9b-229">L’exemple suivant surveille tous les événements de resize sur l’objet fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-229">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Événements de resize de fenêtre d’analyse" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   <span data-ttu-id="6ca9b-231">Figure 21 : Événements de resize de fenêtre de surveillance</span><span class="sxs-lookup"><span data-stu-id="6ca9b-231">Figure 21:  Monitoring window resize events</span></span>  
:::image-end:::  

<span data-ttu-id="6ca9b-232">L’exemple suivant définit un tableau pour surveiller les événements et les `resize` `scroll` événements sur l’objet fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-232">The following defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="6ca9b-233">Vous pouvez également spécifier l’un des types d’événements disponibles, les chaînes qui m’indiquent des jeux d’événements prédéfinés.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-233">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="6ca9b-234">Le tableau suivant affiche les types d’événements disponibles et les mappages d’événements associés.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-234">The following table displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="6ca9b-235">Type d’événement</span><span class="sxs-lookup"><span data-stu-id="6ca9b-235">Event type</span></span> | <span data-ttu-id="6ca9b-236">Événements mappés correspondants</span><span class="sxs-lookup"><span data-stu-id="6ca9b-236">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="6ca9b-237">« click », « dblclick », « mousedown », « mousemove », « mouseout », « mouseover », « mouseup », « mousewheel »</span><span class="sxs-lookup"><span data-stu-id="6ca9b-237">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="6ca9b-238">«keydown», «keypress», «keyup», «textInput»</span><span class="sxs-lookup"><span data-stu-id="6ca9b-238">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="6ca9b-239">« touchcancel », « touchend », « touchmove », « touchstart »</span><span class="sxs-lookup"><span data-stu-id="6ca9b-239">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="6ca9b-240">«flou», «modifier», «focus», «réinitialiser», «resize», «scroll», «select», «submit», «zoom»</span><span class="sxs-lookup"><span data-stu-id="6ca9b-240">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="6ca9b-241">Dans l’exemple de code suivant, le type d’événement correspondant aux événements sur un champ de texte d’entrée est actuellement sélectionné `key` `key` dans **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="6ca9b-241">In the following code sample, the `key` event type corresponding to `key` events on an input text field are currently selected in the **Elements** tool.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="6ca9b-242">Dans la figure suivante, l’exemple de sortie après avoir tapé un caractère dans le champ de texte s’affiche.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-242">In the following figure the sample output after typing a character in the text field is displayed.</span></span>  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Surveillance des événements clés" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   <span data-ttu-id="6ca9b-244">Figure 22 : Surveillance des événements clés</span><span class="sxs-lookup"><span data-stu-id="6ca9b-244">Figure 22:  Monitoring key events</span></span>  
:::image-end:::  

## <a name="profile"></a><span data-ttu-id="6ca9b-245">profile</span><span class="sxs-lookup"><span data-stu-id="6ca9b-245">profile</span></span>  

```console
profile([name])
```  

<span data-ttu-id="6ca9b-246">Démarre une session de profilage du processeur JavaScript avec un nom facultatif.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-246">Starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="6ca9b-247">La [méthode profileEnd()](#profileend) termine le profil et affiche les résultats dans l’outil Mémoire. </span><span class="sxs-lookup"><span data-stu-id="6ca9b-247">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** tool.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="6ca9b-248">Exécutez la `profile()` méthode pour démarrer le profilage.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-248">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="6ca9b-249">Exécutez [la méthode profileEnd()](#profileend) pour arrêter le profilage et afficher les résultats dans l’outil Mémoire. </span><span class="sxs-lookup"><span data-stu-id="6ca9b-249">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** tool.</span></span>  

<span data-ttu-id="6ca9b-250">Les profils peuvent également être imbrmbrés.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-250">Profiles may also be nested.</span></span>  <span data-ttu-id="6ca9b-251">Dans les exemples de code suivants et la figure, le résultat est le même quelle que soit la commande.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-251">In the following code samples and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="6ca9b-252">Plusieurs profils d’UC peuvent fonctionner en même temps et vous n’êtes pas obligé de fermer chacun d’eux dans l’ordre de création.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-252">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <a name="profileend"></a><span data-ttu-id="6ca9b-253">profileEnd</span><span class="sxs-lookup"><span data-stu-id="6ca9b-253">profileEnd</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="6ca9b-254">Termine une session de profilage du processeur JavaScript et affiche les résultats dans **l’outil** Mémoire.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-254">Completes a JavaScript CPU profiling session and displays the results in the **Memory** tool.</span></span>  <span data-ttu-id="6ca9b-255">Vous devez être en cours d’exécution [de la méthode profile().](#profile)</span><span class="sxs-lookup"><span data-stu-id="6ca9b-255">You must be running the [profile()](#profile) method.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="6ca9b-256">Exécutez [la méthode profile()](#profile) pour démarrer le profilage.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-256">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="6ca9b-257">Exécutez la `profileEnd()` méthode pour arrêter le profilage et afficher les résultats dans l’outil Mémoire. </span><span class="sxs-lookup"><span data-stu-id="6ca9b-257">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** tool.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="6ca9b-258">Les profils peuvent également être imbrmbrés.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-258">Profiles may also be nested.</span></span>  <span data-ttu-id="6ca9b-259">Dans l’exemple de code suivant et la figure, le résultat est le même quelle que soit la commande.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-259">In the following code sample and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="6ca9b-260">Le résultat s’affiche sous la mesure d’une capture instantanée de tas dans **l’outil Mémoire.**</span><span class="sxs-lookup"><span data-stu-id="6ca9b-260">The result appears as a Heap Snapshot in the **Memory** tool.</span></span>  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Profils groupés" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   <span data-ttu-id="6ca9b-262">Figure 23 : Profils groupés</span><span class="sxs-lookup"><span data-stu-id="6ca9b-262">Figure 23:  Grouped profiles</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="6ca9b-263">Plusieurs profils d’UC peuvent fonctionner en même temps et vous n’êtes pas obligé de fermer chacun d’eux dans l’ordre de création.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-263">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <a name="queryobjects"></a><span data-ttu-id="6ca9b-264">queryObjects</span><span class="sxs-lookup"><span data-stu-id="6ca9b-264">queryObjects</span></span>  

```console
queryObjects(Constructor)
```  

<span data-ttu-id="6ca9b-265">Renvoyer un tableau d’objets créés avec le constructeur spécifié.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-265">Return an array of objects created with the specified constructor.</span></span>  <span data-ttu-id="6ca9b-266">L’étendue `queryObjects()` est le contexte d’runtime actuellement sélectionné dans la console.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-266">The scope of `queryObjects()` is the currently-selected runtime context in the console.</span></span>

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      <span data-ttu-id="6ca9b-267">Renvoie tout `Promises` .</span><span class="sxs-lookup"><span data-stu-id="6ca9b-267">Returns all `Promises`.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      <span data-ttu-id="6ca9b-268">Renvoie tous les éléments HTML.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-268">Returns all HTML elements.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      <span data-ttu-id="6ca9b-269">Renvoie tous les objets qui ont été ins instantiés à l’aide `new functionName()` de .</span><span class="sxs-lookup"><span data-stu-id="6ca9b-269">Returns all objects that were instantiated using `new functionName()`.</span></span>  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a><span data-ttu-id="6ca9b-270">table</span><span class="sxs-lookup"><span data-stu-id="6ca9b-270">table</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="6ca9b-271">Enregistre les données d’objet avec une mise en forme de tableau basée sur l’objet de données avec des en-tête de colonne facultatifs.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-271">Logs object data with table formatting based upon the data object in with optional column headings.</span></span>  <span data-ttu-id="6ca9b-272">Dans l’exemple de code et la figure suivants, une liste de noms utilisant un tableau dans la console s’affiche.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-272">In the following code sample and figure, a list of names using a table in the console is displayed.</span></span>  

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

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="Résultat de la méthode table()" lightbox="../media/console-table-display.msft.png":::
   <span data-ttu-id="6ca9b-274">Figure 24 : Résultat de la `table()` méthode</span><span class="sxs-lookup"><span data-stu-id="6ca9b-274">Figure 24:  The result of the `table()` method</span></span>  
:::image-end:::  

## <a name="undebug"></a><span data-ttu-id="6ca9b-275">undebug</span><span class="sxs-lookup"><span data-stu-id="6ca9b-275">undebug</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="6ca9b-276">Arrête le débogage de la méthode spécifiée de sorte que lorsque la méthode est appelée, le déboguer n’est plus appelé.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-276">Stops the debugging of the specified method so that when the method is called, the debugger is no longer invoked.</span></span>  

```console
undebug(getData);
```  

## <a name="unmonitor"></a><span data-ttu-id="6ca9b-277">unmonitor</span><span class="sxs-lookup"><span data-stu-id="6ca9b-277">unmonitor</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="6ca9b-278">Arrête la surveillance de la méthode spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-278">Stops the monitoring of the specified method.</span></span>  <span data-ttu-id="6ca9b-279">Cette méthode est utilisée de concert avec la [méthode monitor().](#monitor)</span><span class="sxs-lookup"><span data-stu-id="6ca9b-279">This method is used in concert with the [monitor()](#monitor) method.</span></span>  

```console
unmonitor(getData);
```  

## <a name="unmonitorevents"></a><span data-ttu-id="6ca9b-280">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="6ca9b-280">unmonitorEvents</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="6ca9b-281">Arrête la surveillance des événements pour l’objet et les événements spécifiés.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-281">Stops monitoring events for the specified object and events.</span></span>  <span data-ttu-id="6ca9b-282">Par exemple, l’exemple suivant arrête l’analyse des événements sur l’objet fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-282">For example, the following stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="6ca9b-283">Vous pouvez également arrêter de manière sélective la surveillance d’événements spécifiques sur un objet.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-283">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="6ca9b-284">Par exemple, le code suivant démarre la surveillance de tous les événements sur l’élément actuellement sélectionné, puis arrête la surveillance des événements \(peut-être pour réduire le bruit dans la `mouse` `mousemove` sortie de la console\).</span><span class="sxs-lookup"><span data-stu-id="6ca9b-284">For example, the following code starts monitoring all `mouse` events on the currently selected element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <a name="values"></a><span data-ttu-id="6ca9b-285">values</span><span class="sxs-lookup"><span data-stu-id="6ca9b-285">values</span></span>  

```console
values(object)
```  

<span data-ttu-id="6ca9b-286">Renvoie un tableau contenant les valeurs de toutes les propriétés appartenant à l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="6ca9b-286">Returns an array containing the values of all properties belonging to the specified object.</span></span>  

```console
values(object);
```  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6ca9b-287">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="6ca9b-287">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Référence de l’API de console"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir - Référence de l’API console"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Accélérer le runtime JavaScript"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Problème 1050237 : débogage(fonction) ne fonctionne pas | Monorail"  

> [!NOTE]
> <span data-ttu-id="6ca9b-297">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6ca9b-297">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6ca9b-298">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/utilities) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="6ca9b-298">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="6ca9b-300">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6ca9b-300">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
