---
title: XXXXXX xxxxxxx xxx xxxxxxxxx
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: efa03e02813d718514f73445bc0dceb3a1a83f39
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "10708803"
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

# <span data-ttu-id="68fb6-103">XXXXXX xxxxxxx xxx xxxxxxxxx</span><span class="sxs-lookup"><span data-stu-id="68fb6-103">Console Utilities API Reference</span></span>  

<span data-ttu-id="68fb6-104">L’API des utilitaires de la console contient une collection de commandes pratiques permettant d’effectuer des tâches courantes: la sélection et l’examen des éléments DOM, l’affichage des données dans un format lisible, l’arrêt et le démarrage du profileur, et la surveillance des événements DOM.</span><span class="sxs-lookup"><span data-stu-id="68fb6-104">The Console Utilities API contains a collection of convenience commands for performing common tasks:  selecting and inspecting DOM elements, displaying data in readable format, stopping and starting the profiler, and monitoring DOM events.</span></span>  

> [!WARNING]
> <span data-ttu-id="68fb6-105">Les commandes suivantes fonctionnent uniquement dans la console Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="68fb6-105">The following commands only work in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="68fb6-106">Les commandes ne fonctionnent pas si celles-ci sont exécutées à partir de vos scripts.</span><span class="sxs-lookup"><span data-stu-id="68fb6-106">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="68fb6-107">Vous recherchez `console.log()` , `console.error()` et le reste des `console.*` méthodes?</span><span class="sxs-lookup"><span data-stu-id="68fb6-107">Looking for `console.log()`, `console.error()`, and the rest of the `console.*` methods?</span></span>  <span data-ttu-id="68fb6-108">Voir [référence][DevToolsConsoleApi]sur l’API de la console.</span><span class="sxs-lookup"><span data-stu-id="68fb6-108">See [Console API Reference][DevToolsConsoleApi].</span></span>  

## <span data-ttu-id="68fb6-109">Expression récemment évaluée</span><span class="sxs-lookup"><span data-stu-id="68fb6-109">Recently Evaluated Expression</span></span>  

```console
$_
```  

<span data-ttu-id="68fb6-110">Renvoie la valeur de l’expression évaluée le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="68fb6-110">Returns the value of the most recently evaluated expression.</span></span>  

<span data-ttu-id="68fb6-111">Dans l’illustration suivante, une expression simple \ ( `2 + 2` \) est évaluée.</span><span class="sxs-lookup"><span data-stu-id="68fb6-111">In the following figure, a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="68fb6-112">La `$_` propriété est alors évaluée, qui contient la même valeur.</span><span class="sxs-lookup"><span data-stu-id="68fb6-112">The `$_` property is then evaluated, which contains the same value.</span></span>  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$ _ est l’expression la plus récemment évaluée." lightbox="../media/console-arithmatic.msft.png":::
   <span data-ttu-id="68fb6-114">Figure 1: `$_` l’expression la plus récente est évaluée</span><span class="sxs-lookup"><span data-stu-id="68fb6-114">Figure 1:  `$_` is the most recently evaluated expression</span></span>  
:::image-end:::  

<span data-ttu-id="68fb6-115">Dans l’illustration suivante, l’expression évaluée contient initialement un tableau de noms.</span><span class="sxs-lookup"><span data-stu-id="68fb6-115">In the following figure, the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="68fb6-116">Si vous évaluez la `$_.length` longueur de l’argument matrice, la valeur stockée dans `$_` les modifications devient la dernière expression évaluée `4` .</span><span class="sxs-lookup"><span data-stu-id="68fb6-116">Evaluating `$_.length` to find the length of the array, the value stored in `$_` changes to become the latest evaluated expression, `4`.</span></span>  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$ _ change lorsque de nouvelles commandes sont évaluées" lightbox="../media/console-array-length.msft.png":::
   <span data-ttu-id="68fb6-118">Figure 2: `$_` modifications lors de l’évaluation de nouvelles commandes</span><span class="sxs-lookup"><span data-stu-id="68fb6-118">Figure 2:  `$_` changes when new commands are evaluated</span></span>  
:::image-end:::  

## <span data-ttu-id="68fb6-119">Élément récemment sélectionné ou objet JavaScript</span><span class="sxs-lookup"><span data-stu-id="68fb6-119">Recently Selected Element Or JavaScript Object</span></span>  

```console
$0
```  

<span data-ttu-id="68fb6-120">Retourne l’élément le plus récemment sélectionné ou l’objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="68fb6-120">Returns the most recently selected element or JavaScript object.</span></span>  `$1` <span data-ttu-id="68fb6-121">renvoie le second dernier sélectionné, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="68fb6-121">returns the second most recently selected one, and so on.</span></span>  <span data-ttu-id="68fb6-122">Les `$0` commandes,,, `$1` `$2` `$3` et `$4` permettent de faire une référence historique aux cinq derniers éléments DOM examinés dans le panneau **éléments** ou les cinq derniers objets du tas JavaScript sélectionnés dans le panneau **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="68fb6-122">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** panel or the last five JavaScript heap objects selected in the **Memory** panel.</span></span>  

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

<span data-ttu-id="68fb6-123">Dans l’illustration suivante, un `img` élément est sélectionné dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="68fb6-123">In the following figure, an `img` element is selected in the **Elements** panel.</span></span>  <span data-ttu-id="68fb6-124">Le tiroir **Console** de la console `$0` a été évalué et affiche le même élément.</span><span class="sxs-lookup"><span data-stu-id="68fb6-124">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="$0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   <span data-ttu-id="68fb6-126">Figure 3: le</span><span class="sxs-lookup"><span data-stu-id="68fb6-126">Figure 3:  The</span></span> `$0`  
:::image-end:::  

<span data-ttu-id="68fb6-127">Dans l’illustration suivante, l’image montre un élément différent sélectionné dans la même page.</span><span class="sxs-lookup"><span data-stu-id="68fb6-127">In the following figure, the image shows a different element selected in the same page.</span></span>  <span data-ttu-id="68fb6-128">L' `$0` élément désormais fait référence à l’élément que vous venez de sélectionner, tandis qu’il `$1` renvoie le précédent.</span><span class="sxs-lookup"><span data-stu-id="68fb6-128">The `$0` now refers to the newly selected element, while `$1` returns the previously selected one.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="$1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   <span data-ttu-id="68fb6-130">Figure 4: le</span><span class="sxs-lookup"><span data-stu-id="68fb6-130">Figure 4:  The</span></span> `$1`  
:::image-end:::  

## <span data-ttu-id="68fb6-131">Sélecteur de requête</span><span class="sxs-lookup"><span data-stu-id="68fb6-131">Query Selector</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="68fb6-132">Renvoie la référence au premier élément DOM avec le sélecteur CSS spécifié.</span><span class="sxs-lookup"><span data-stu-id="68fb6-132">Returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="68fb6-133">Cette méthode est un alias de la méthode [document. querySelector ()][MDNDocumentQuerySelector] .</span><span class="sxs-lookup"><span data-stu-id="68fb6-133">This method is an alias for the [document.querySelector()][MDNDocumentQuerySelector] method.</span></span>  

<span data-ttu-id="68fb6-134">Dans l’illustration suivante, une référence au premier `<img>` élément du document est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="68fb6-134">In the following figure, a reference to the first `<img>` element in the document is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$ ('Img')" lightbox="../media/console-element-selector-image.msft.png":::
   <span data-ttu-id="68fb6-136">Figure 5: le</span><span class="sxs-lookup"><span data-stu-id="68fb6-136">Figure 5:  The</span></span> `$('img')`  
:::image-end:::  

<span data-ttu-id="68fb6-137">Positionnez le pointeur sur le résultat retourné, ouvrez le menu contextuel (cliquez avec le bouton droit sur \), puis sélectionnez l’option **révéler dans le panneau d’éléments** pour le Rechercher dans le DOM ou **faire défiler pour** afficher la page.</span><span class="sxs-lookup"><span data-stu-id="68fb6-137">Hover on the returned result, open the contextual menu \(right-click\), and select **Reveal in Elements Panel** to find it in the DOM or **Scroll in to View** to show it on the page.</span></span>  

<span data-ttu-id="68fb6-138">Dans l’illustration suivante, une référence à l’élément actuellement sélectionné est renvoyée et la propriété SRC est affichée.</span><span class="sxs-lookup"><span data-stu-id="68fb6-138">In the following figure, a reference to the currently selected element is returned and the src property is displayed.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="$ ('Img'). SRC" lightbox="../media/console-element-selector-image-source.msft.png":::
   <span data-ttu-id="68fb6-140">Figure 6: le</span><span class="sxs-lookup"><span data-stu-id="68fb6-140">Figure 6:  The</span></span> `$('img').src`  
:::image-end:::  

<span data-ttu-id="68fb6-141">Cette méthode prend également en charge un second paramètre, startNode, qui spécifie un élément ou un nœud à partir duquel Rechercher des éléments.</span><span class="sxs-lookup"><span data-stu-id="68fb6-141">This method also supports a second parameter, startNode, that specifies an "element" or Node from which to search for elements.</span></span>  <span data-ttu-id="68fb6-142">La valeur par défaut du paramètre est `document` .</span><span class="sxs-lookup"><span data-stu-id="68fb6-142">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="68fb6-143">Dans l’illustration suivante, le premier `img` élément est trouvé après `title--image` et affiche le `src` résultat correct.</span><span class="sxs-lookup"><span data-stu-id="68fb6-143">In the following figure, the first `img` element is found after the `title--image` and displays the `src` properly is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="$ ('Img', document. querySelector ('title--image')). SRC" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   <span data-ttu-id="68fb6-145">Figure 7: le</span><span class="sxs-lookup"><span data-stu-id="68fb6-145">Figure 7:  The</span></span> `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="68fb6-146">Si vous utilisez une bibliothèque telle que jQuery qui utilise `$` , la fonctionnalité est écrasée et `$` correspond à l’implémentation de cette bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="68fb6-146">If you are using a library such as jQuery that uses `$`, the functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

## <span data-ttu-id="68fb6-147">Sélecteur de requête</span><span class="sxs-lookup"><span data-stu-id="68fb6-147">Query Selector All</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="68fb6-148">Retourne un tableau d’éléments qui correspondent au sélecteur CSS spécifié.</span><span class="sxs-lookup"><span data-stu-id="68fb6-148">Returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="68fb6-149">Cette méthode équivaut à appeler la méthode [document. querySelectorAll ()][MDNDocumentQuerySelectorAll] .</span><span class="sxs-lookup"><span data-stu-id="68fb6-149">This method is equivalent to calling the [document.querySelectorAll()][MDNDocumentQuerySelectorAll] method.</span></span>  

<span data-ttu-id="68fb6-150">Dans l’exemple de code et la figure ci-dessous, utilisez `$$()` pour créer un tableau de tous les `<img>` éléments du document actuel et afficher la valeur de la `src` propriété de chaque élément.</span><span class="sxs-lookup"><span data-stu-id="68fb6-150">In the following code sample and figure, use `$$()` to create an array of all `<img>` elements in the current document and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Utilisation de $ $ () pour sélectionner toutes les images du document et afficher les sources" lightbox="../media/console-element-selector-image-all.msft.png":::
   <span data-ttu-id="68fb6-152">Figure 8: utilisation `$$()` pour sélectionner toutes les images du document et afficher les sources</span><span class="sxs-lookup"><span data-stu-id="68fb6-152">Figure 8:  Using `$$()` to select all images in the document and display the sources</span></span>  
:::image-end:::  

<span data-ttu-id="68fb6-153">Cette méthode prend également en charge un second paramètre, startNode, qui spécifie un élément ou un nœud à partir duquel Rechercher des éléments.</span><span class="sxs-lookup"><span data-stu-id="68fb6-153">This method also supports a second parameter, startNode, that specifies an element or Node from which to search for elements.</span></span>  <span data-ttu-id="68fb6-154">La valeur par défaut du paramètre est `document` .</span><span class="sxs-lookup"><span data-stu-id="68fb6-154">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="68fb6-155">Dans l’exemple de code et la figure ci-dessous, une version modifiée de l’exemple de code précédent et de la figure utilise `$$()` pour créer un tableau de tous les `<img>` éléments qui s’affichent dans le document actif suite au nœud sélectionné.</span><span class="sxs-lookup"><span data-stu-id="68fb6-155">In the following code sample and figure, a modified version of the previous code sample and figure uses `$$()` to create an array of all `<img>` elements that appear in the current document after the selected Node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Utilisation de $ $ () pour sélectionner toutes les images qui s’affichent après l’élément <div> spécifié dans le document et afficher les sources" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   <span data-ttu-id="68fb6-157">Figure 9: utilisation `$$()` pour sélectionner toutes les images qui apparaissent après l' `<div>` élément spécifié dans le document et afficher les sources</span><span class="sxs-lookup"><span data-stu-id="68fb6-157">Figure 9:  Using `$$()` to select all images that appear after the specified `<div>` element in the document and display the sources</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="68fb6-158">Appuyez sur `Shift` + `Enter` la console pour commencer une nouvelle ligne sans exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="68fb6-158">Press `Shift`+`Enter` in the console to start a new line without running the script.</span></span>  

## <span data-ttu-id="68fb6-159">Suivante</span><span class="sxs-lookup"><span data-stu-id="68fb6-159">XPath</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="68fb6-160">Renvoie un tableau d’éléments DOM qui correspondent à l’expression XPath spécifiée.</span><span class="sxs-lookup"><span data-stu-id="68fb6-160">Returns an array of DOM elements that match the specified XPath expression.</span></span>  

<span data-ttu-id="68fb6-161">Dans l’exemple de code et la figure ci-dessous, tous les `<p>` éléments de la page sont renvoyés.</span><span class="sxs-lookup"><span data-stu-id="68fb6-161">In the following code sample and figure, all of the `<p>` elements on the page are returned.</span></span>  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Utilisation d’un sélecteur XPath" lightbox="../media/console-array-xpath.msft.png":::
   <span data-ttu-id="68fb6-163">Figure 10: utilisation d’un sélecteur XPath</span><span class="sxs-lookup"><span data-stu-id="68fb6-163">Figure 10:  Using an XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="68fb6-164">Dans l’exemple de code et la figure ci-dessous, tous les `<p>` éléments qui contiennent des `<a>` éléments sont renvoyés.</span><span class="sxs-lookup"><span data-stu-id="68fb6-164">In the following code sample and figure, all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Utilisation d’un sélecteur XPath plus complexe" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   <span data-ttu-id="68fb6-166">Figure 11: utilisation d’un sélecteur XPath plus complexe</span><span class="sxs-lookup"><span data-stu-id="68fb6-166">Figure 11:  Using a more complicated XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="68fb6-167">À l’instar des autres commandes de sélecteur, `$x(path)` possède un deuxième paramètre facultatif, `startNode` qui spécifie un élément ou un nœud à partir duquel Rechercher des éléments.</span><span class="sxs-lookup"><span data-stu-id="68fb6-167">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or Node from which to search for elements.</span></span>  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Utilisation d’un sélecteur XPath avec startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   <span data-ttu-id="68fb6-169">Figure 12: utilisation d’un sélecteur XPath avec</span><span class="sxs-lookup"><span data-stu-id="68fb6-169">Figure 12:  Using an XPath selector with</span></span> `startNode`  
:::image-end:::  

## <span data-ttu-id="68fb6-170">supprime</span><span class="sxs-lookup"><span data-stu-id="68fb6-170">clear</span></span>  

```console
clear()
```  

<span data-ttu-id="68fb6-171">Efface la console de l’historique.</span><span class="sxs-lookup"><span data-stu-id="68fb6-171">Clears the console of the history.</span></span>  

```console
clear()
```  

## <span data-ttu-id="68fb6-172">copy</span><span class="sxs-lookup"><span data-stu-id="68fb6-172">copy</span></span>  

```console
copy(object)
```  

<span data-ttu-id="68fb6-173">La `copy(object)` méthode copie une représentation de chaîne de l’objet spécifié dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="68fb6-173">The `copy(object)` method copies a string representation of the specified object to the clipboard.</span></span>  

```console
copy($0)
```  

## <span data-ttu-id="68fb6-174">déboguer</span><span class="sxs-lookup"><span data-stu-id="68fb6-174">debug</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="68fb6-175">Le [#1050237 problème de chrome][MonorailIssue1050237] effectue le suivi d’un bogue avec la `debug()` fonction.</span><span class="sxs-lookup"><span data-stu-id="68fb6-175">The [Chromium issue #1050237][MonorailIssue1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="68fb6-176">Si vous rencontrez un problème, essayez plutôt d' [utiliser des points d’arrêt][DevtoolsJavascriptBreakpoints] .</span><span class="sxs-lookup"><span data-stu-id="68fb6-176">If you encounter the issue, try [using breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="68fb6-177">Lorsque vous demandez la méthode spécifiée, le débogueur est appelé et s’interrompt à l’intérieur de la méthode sur le panneau **sources** pour vous permettre de parcourir le code et de le déboguer.</span><span class="sxs-lookup"><span data-stu-id="68fb6-177">When you request the specified method, the debugger is invoked and breaks inside the method on the **Sources** panel allowing you to step through the code and debug it.</span></span>  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Casser au sein d’une méthode à l’aide du débogage ()" lightbox="../media/console-debug-text.msft.png":::
   <span data-ttu-id="68fb6-179">Figure 13: rupture dans une méthode avec</span><span class="sxs-lookup"><span data-stu-id="68fb6-179">Figure 13:  Breaking inside a method with</span></span> `debug()`  
:::image-end:::  

<span data-ttu-id="68fb6-180">Utilisez `undebug(method)` cette commande pour arrêter l’interruption de la méthode, ou utilisez l’interface utilisateur pour désactiver tous les points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="68fb6-180">Use `undebug(method)` to stop breaking on the method, or use the UI to disable all breakpoints.</span></span>  

<span data-ttu-id="68fb6-181">Pour plus d’informations sur les points d’arrêt, voir [suspendre votre code avec des points d’arrêt][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="68fb6-181">For more information on breakpoints, see [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <span data-ttu-id="68fb6-182">dir</span><span class="sxs-lookup"><span data-stu-id="68fb6-182">dir</span></span>  

```console
dir(object)
```  

<span data-ttu-id="68fb6-183">Affiche une liste de styles d’objet de toutes les propriétés de l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="68fb6-183">Displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="68fb6-184">Cette méthode est un alias de la méthode [console. dir ()][MDNConsoleDir] .</span><span class="sxs-lookup"><span data-stu-id="68fb6-184">This method is an alias for the [console.dir()][MDNConsoleDir] method.</span></span>  

<span data-ttu-id="68fb6-185">Évaluez `document.head` la console pour afficher le code HTML entre `<head>` les `</head>` balises et.</span><span class="sxs-lookup"><span data-stu-id="68fb6-185">Evaluate `document.head` in the Console to display the HTML between the `<head>` and `</head>` tags.</span></span>  <span data-ttu-id="68fb6-186">Dans l’exemple de code et la figure ci-dessous, une liste à l’aide de l’objet s’affiche après utilisation `console.dir()` de la console.</span><span class="sxs-lookup"><span data-stu-id="68fb6-186">In the following code sample and figure, an object-style listing is displayed after using `console.dir()` in the Console.</span></span>  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Journalisation du document. Head avec la méthode dir ()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   <span data-ttu-id="68fb6-188">Figure 14: journalisation `document.head` avec la `dir()` méthode</span><span class="sxs-lookup"><span data-stu-id="68fb6-188">Figure 14:  Logging `document.head` with `dir()` method</span></span>  
:::image-end:::  

<span data-ttu-id="68fb6-189">Pour plus d’informations, consultez l' [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entrée dans l’API de la console.</span><span class="sxs-lookup"><span data-stu-id="68fb6-189">For more information, see the [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entry in the Console API.</span></span>  

## <span data-ttu-id="68fb6-190">dirxml</span><span class="sxs-lookup"><span data-stu-id="68fb6-190">dirxml</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="68fb6-191">Imprime une représentation XML de l’objet spécifié, comme indiqué dans l’onglet **éléments** .  Cette méthode est équivalente à la méthode [console. DirXML ()][MDNConsoleDirxml] .</span><span class="sxs-lookup"><span data-stu-id="68fb6-191">Prints an XML representation of the specified object, as seen in the **Elements** tab.  This method is equivalent to the [console.dirxml()][MDNConsoleDirxml] method.</span></span>  

## <span data-ttu-id="68fb6-192">recherche</span><span class="sxs-lookup"><span data-stu-id="68fb6-192">inspect</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="68fb6-193">Ouvre et sélectionne l’élément ou l’objet spécifié dans le panneau approprié: soit le panneau des **éléments** pour les éléments DOM, soit le panneau **mémoire** pour les objets du tas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="68fb6-193">Opens and selects the specified element or object in the appropriate panel:  either the **Elements** panel for DOM elements or the **Memory** panel for JavaScript heap objects.</span></span>  

<span data-ttu-id="68fb6-194">Dans l’exemple de code et la figure ci-après, l' `document.body` élément s’ouvre dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="68fb6-194">In the following code sample and figure, the `document.body` opens in the **Elements** panel.</span></span>  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Inspecter un élément avec Inspect ()" lightbox="../media/console-inspect-document-body.msft.png":::
   <span data-ttu-id="68fb6-196">Figure 15: examen d’un élément avec</span><span class="sxs-lookup"><span data-stu-id="68fb6-196">Figure 15:  Inspecting an element with</span></span> `inspect()`  
:::image-end:::  

<span data-ttu-id="68fb6-197">Lorsque vous passez une méthode à inspecter, la méthode ouvre le document dans le panneau **sources** que vous pouvez inspecter.</span><span class="sxs-lookup"><span data-stu-id="68fb6-197">When passing a method to inspect, the method opens the document in the **Sources** panel for you to inspect.</span></span>  

## <span data-ttu-id="68fb6-198">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="68fb6-198">getEventListeners</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="68fb6-199">Renvoie les écouteurs d’événements enregistrés sur l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="68fb6-199">Returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="68fb6-200">La valeur de retour est un objet qui contient un tableau pour chaque type d’événement inscrit \ (tel que `click` ou `keydown` \).</span><span class="sxs-lookup"><span data-stu-id="68fb6-200">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="68fb6-201">Les membres de chaque tableau sont des objets qui décrivent l’écouteur inscrit pour chaque type.</span><span class="sxs-lookup"><span data-stu-id="68fb6-201">The members of each array are objects that describe the listener registered for each type.</span></span>  <span data-ttu-id="68fb6-202">Dans l’exemple de code suivant, tous les détecteurs d’événements enregistrés sur l’objet document apparaissent.</span><span class="sxs-lookup"><span data-stu-id="68fb6-202">In the following code sample figure, all of the event listeners registered on the document object are listed.</span></span>  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Sortie de l’utilisation de getEventListeners (document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   <span data-ttu-id="68fb6-204">Figure 16: résultat de l’utilisation de</span><span class="sxs-lookup"><span data-stu-id="68fb6-204">Figure 16:  The result of using</span></span> `getEventListeners(document)`  
:::image-end:::  

<span data-ttu-id="68fb6-205">S’il existe plusieurs écouteurs enregistrés sur l’objet spécifié, le tableau contient un membre pour chaque écouteur.</span><span class="sxs-lookup"><span data-stu-id="68fb6-205">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="68fb6-206">Dans l’illustration suivante, deux écouteurs d’événements sont inscrits dans l’élément document pour l' `click` événement.</span><span class="sxs-lookup"><span data-stu-id="68fb6-206">In the following figure, there are two event listeners registered on the document element for the `click` event.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Écouteurs multiples" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   <span data-ttu-id="68fb6-208">Figure 17: écouteurs multiples</span><span class="sxs-lookup"><span data-stu-id="68fb6-208">Figure 17:  Multiple listeners</span></span>  
:::image-end:::  

<span data-ttu-id="68fb6-209">Vous pouvez également développer chacun des objets suivants pour découvrir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="68fb6-209">You may further expand each of the following objects to explore the properties.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Affichage développé de l’objet Listener" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   <span data-ttu-id="68fb6-211">Figure 18: vue développée de l’objet Listener</span><span class="sxs-lookup"><span data-stu-id="68fb6-211">Figure 18:  Expanded view of listener object</span></span>  
:::image-end:::  

## <span data-ttu-id="68fb6-212">clés</span><span class="sxs-lookup"><span data-stu-id="68fb6-212">keys</span></span>  

```console
keys(object)
```  

<span data-ttu-id="68fb6-213">Retourne une matrice contenant les noms des propriétés appartenant à l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="68fb6-213">Returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="68fb6-214">Pour obtenir les valeurs associées des mêmes propriétés, utilisez `values()` .</span><span class="sxs-lookup"><span data-stu-id="68fb6-214">To get the associated values of the same properties, use `values()`.</span></span>  

<span data-ttu-id="68fb6-215">Par exemple, supposons que votre application définisse l’objet suivant.</span><span class="sxs-lookup"><span data-stu-id="68fb6-215">For example, suppose your application defined the following object.</span></span>  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

<span data-ttu-id="68fb6-216">Dans les exemples de code et figures suivants, le résultat suppose qu’il `player1` a été défini dans l’espace de noms global \ (pour la simplicité \) avant de taper `keys(player1)` et `values(player1)` dans la console.</span><span class="sxs-lookup"><span data-stu-id="68fb6-216">In the following code samples and figure, the result assumes `player1` was defined in the global namespace \(for simplicity\) prior to typing `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Commandes Keys () et values ()" lightbox="../media/console-keys-values.msft.png":::
   <span data-ttu-id="68fb6-218">Figure 19: `keys()` commandes et `values()`</span><span class="sxs-lookup"><span data-stu-id="68fb6-218">Figure 19:  The `keys()` and `values()` commands</span></span>  
:::image-end:::  

## <span data-ttu-id="68fb6-219">moniteur</span><span class="sxs-lookup"><span data-stu-id="68fb6-219">monitor</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="68fb6-220">Consigne un message dans la console indiquant le nom de la méthode, ainsi que les arguments transmis à la méthode lors de son appel.</span><span class="sxs-lookup"><span data-stu-id="68fb6-220">Logs a message to the console that indicates the method name along with the arguments that are passed to the method when it was called.</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="Méthode Monitor ()" lightbox="../media/console-function-monitor-sum.msft.png":::
   <span data-ttu-id="68fb6-222">Figure 20: `monitor()` méthode</span><span class="sxs-lookup"><span data-stu-id="68fb6-222">Figure 20:  The `monitor()` method</span></span>  
:::image-end:::  

<span data-ttu-id="68fb6-223">Utiliser `unmonitor(method)` pour cesser de surveiller.</span><span class="sxs-lookup"><span data-stu-id="68fb6-223">Use `unmonitor(method)` to cease monitoring.</span></span>  

## <span data-ttu-id="68fb6-224">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="68fb6-224">monitorEvents</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="68fb6-225">Quand l’un des événements spécifiés se produit sur l’objet spécifié, l’objet Event est enregistré dans la console.</span><span class="sxs-lookup"><span data-stu-id="68fb6-225">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="68fb6-226">Vous pouvez spécifier un événement unique à surveiller, un tableau d’événements ou l’un des types d’événements génériques mappés à une collection prédéfinie d’événements.</span><span class="sxs-lookup"><span data-stu-id="68fb6-226">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  <span data-ttu-id="68fb6-227">Consultez l’exemple de code et la figure suivants.</span><span class="sxs-lookup"><span data-stu-id="68fb6-227">See the following code sample and figure.</span></span>  

<span data-ttu-id="68fb6-228">Le code suivant analyse tous les événements de redimensionnement sur l’objet Window.</span><span class="sxs-lookup"><span data-stu-id="68fb6-228">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Surveiller les événements de redimensionnement d’une fenêtre" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   <span data-ttu-id="68fb6-230">Figure 21: surveiller les événements de redimensionnement d’une fenêtre</span><span class="sxs-lookup"><span data-stu-id="68fb6-230">Figure 21:  Monitoring window resize events</span></span>  
:::image-end:::  

<span data-ttu-id="68fb6-231">Le code suivant définit un tableau pour contrôler les deux `resize` et les `scroll` événements sur l’objet Window.</span><span class="sxs-lookup"><span data-stu-id="68fb6-231">The following defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="68fb6-232">Vous pouvez également spécifier l’un des types d’événements disponibles, qui mappent à des ensembles prédéfinis d’événements.</span><span class="sxs-lookup"><span data-stu-id="68fb6-232">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="68fb6-233">Le tableau ci-dessous répertorie les types d’événements disponibles et les mappages d’événements associés.</span><span class="sxs-lookup"><span data-stu-id="68fb6-233">The table below displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="68fb6-234">Type d’événement</span><span class="sxs-lookup"><span data-stu-id="68fb6-234">Event type</span></span> | <span data-ttu-id="68fb6-235">Événements mappés correspondants</span><span class="sxs-lookup"><span data-stu-id="68fb6-235">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="68fb6-236">"Click", "DblClick", "MouseDown", "MouseMove", "mouseout", "MouseOver", "MouseUp", "MouseWheel"</span><span class="sxs-lookup"><span data-stu-id="68fb6-236">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="68fb6-237">"KeyDown", "KeyPress", "KeyUp", "textInput"</span><span class="sxs-lookup"><span data-stu-id="68fb6-237">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="68fb6-238">"touchcancel", "touchend", "touchmove", "touchstart"</span><span class="sxs-lookup"><span data-stu-id="68fb6-238">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="68fb6-239">"Blur", "changement", "Focus", "Réinitialiser", "Redimensionner", "défilement", "sélectionner", "soumission", "zoom"</span><span class="sxs-lookup"><span data-stu-id="68fb6-239">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="68fb6-240">Dans l’exemple de code suivant, le `key` type d’événement correspondant aux `key` événements sur un champ de saisie de texte est actuellement sélectionné dans le panneau **éléments** .</span><span class="sxs-lookup"><span data-stu-id="68fb6-240">In the following code sample, the `key` event type corresponding to `key` events on an input text field are currently selected in the **Elements** panel.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="68fb6-241">Dans l’illustration suivante, la sortie de l’exemple après saisie d’un caractère dans le champ de texte s’affiche.</span><span class="sxs-lookup"><span data-stu-id="68fb6-241">In the following figure the sample output after typing a character in the text field is displayed.</span></span>  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Surveiller les événements de touche" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   <span data-ttu-id="68fb6-243">Figure 22: surveiller les événements de touche</span><span class="sxs-lookup"><span data-stu-id="68fb6-243">Figure 22:  Monitoring key events</span></span>  
:::image-end:::  

## <span data-ttu-id="68fb6-244">profile</span><span class="sxs-lookup"><span data-stu-id="68fb6-244">profile</span></span>  

```console
profile([name])
```  

<span data-ttu-id="68fb6-245">Démarre une session de profil de l’UC JavaScript avec un nom facultatif.</span><span class="sxs-lookup"><span data-stu-id="68fb6-245">Starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="68fb6-246">La méthode [profileEnd ()](#profileend) termine le profil et affiche les résultats dans le panneau **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="68fb6-246">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** panel.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="68fb6-247">Exécutez la `profile()` méthode pour démarrer le profilage.</span><span class="sxs-lookup"><span data-stu-id="68fb6-247">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="68fb6-248">Exécutez la méthode [profileEnd ()](#profileend) pour arrêter le profilage et afficher les résultats dans le panneau **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="68fb6-248">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** panel.</span></span>  

<span data-ttu-id="68fb6-249">Les profils risquent également d’être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="68fb6-249">Profiles may also be nested.</span></span>  <span data-ttu-id="68fb6-250">Dans les exemples de code suivants et figure le résultat est le même quel que soit l’ordre.</span><span class="sxs-lookup"><span data-stu-id="68fb6-250">In the following code samples and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="68fb6-251">Les profils d’UC multiples peuvent fonctionner en même temps et vous n’avez pas besoin de les clôturer dans l’ordre de création.</span><span class="sxs-lookup"><span data-stu-id="68fb6-251">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="68fb6-252">profileEnd</span><span class="sxs-lookup"><span data-stu-id="68fb6-252">profileEnd</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="68fb6-253">Effectue une session de profilage de l’UC JavaScript et affiche les résultats dans le panneau **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="68fb6-253">Completes a JavaScript CPU profiling session and displays the results in the **Memory** panel.</span></span>  <span data-ttu-id="68fb6-254">Vous devez exécuter la méthode [Profile ()](#profile) .</span><span class="sxs-lookup"><span data-stu-id="68fb6-254">You must be running the [profile()](#profile) method.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="68fb6-255">Exécutez la méthode [Profile ()](#profile) pour démarrer le profilage.</span><span class="sxs-lookup"><span data-stu-id="68fb6-255">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="68fb6-256">Exécutez la `profileEnd()` méthode pour arrêter le profilage et afficher les résultats dans le panneau **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="68fb6-256">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** panel.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="68fb6-257">Les profils risquent également d’être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="68fb6-257">Profiles may also be nested.</span></span>  <span data-ttu-id="68fb6-258">Dans l’exemple de code suivant et la figure, le résultat est le même quel que soit l’ordre.</span><span class="sxs-lookup"><span data-stu-id="68fb6-258">In the following code sample and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="68fb6-259">Le résultat s’affiche sous la forme d’un instantané de tas dans le panneau **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="68fb6-259">The result appears as a Heap Snapshot in the **Memory** panel.</span></span>  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Profils groupés" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   <span data-ttu-id="68fb6-261">Figure 23: profils groupés</span><span class="sxs-lookup"><span data-stu-id="68fb6-261">Figure 23:  Grouped profiles</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="68fb6-262">Les profils d’UC multiples peuvent fonctionner en même temps et vous n’avez pas besoin de les clôturer dans l’ordre de création.</span><span class="sxs-lookup"><span data-stu-id="68fb6-262">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="68fb6-263">queryObjects</span><span class="sxs-lookup"><span data-stu-id="68fb6-263">queryObjects</span></span>  

```console
queryObjects(Constructor)
```  

<span data-ttu-id="68fb6-264">Retourne un tableau d’objets créé avec le constructeur spécifié.</span><span class="sxs-lookup"><span data-stu-id="68fb6-264">Return an array of objects created with the specified constructor.</span></span>  <span data-ttu-id="68fb6-265">L’étendue de `queryObjects()` correspond au contexte d’exécution actuellement sélectionné dans la console.</span><span class="sxs-lookup"><span data-stu-id="68fb6-265">The scope of `queryObjects()` is the currently-selected runtime context in the console.</span></span>

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      <span data-ttu-id="68fb6-266">Renvoie tous `Promises` .</span><span class="sxs-lookup"><span data-stu-id="68fb6-266">Returns all `Promises`.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      <span data-ttu-id="68fb6-267">Renvoie tous les éléments HTML.</span><span class="sxs-lookup"><span data-stu-id="68fb6-267">Returns all HTML elements.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      <span data-ttu-id="68fb6-268">Renvoie tous les objets qui ont été instanciés à l’aide de `new functionName()` .</span><span class="sxs-lookup"><span data-stu-id="68fb6-268">Returns all objects that were instantiated using `new functionName()`.</span></span>  
   :::column-end:::
:::row-end:::  

---  

## <span data-ttu-id="68fb6-269">tabulaire</span><span class="sxs-lookup"><span data-stu-id="68fb6-269">table</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="68fb6-270">Enregistre les données d’objet avec une mise en forme de tableau en fonction de l’objet de données avec des en-têtes de colonnes facultatifs.</span><span class="sxs-lookup"><span data-stu-id="68fb6-270">Logs object data with table formatting based upon the data object in with optional column headings.</span></span>  <span data-ttu-id="68fb6-271">Dans l’exemple de code et la figure ci-dessous, une liste de noms utilisant une table dans la console s’affiche.</span><span class="sxs-lookup"><span data-stu-id="68fb6-271">In the following code sample and figure, a list of names using a table in the console is displayed.</span></span>  

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

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="Résultat de la méthode table ()." lightbox="../media/console-table-display.msft.png":::
   <span data-ttu-id="68fb6-273">Figure 24: résultat de la `table()` méthode</span><span class="sxs-lookup"><span data-stu-id="68fb6-273">Figure 24:  The result of the `table()` method</span></span>  
:::image-end:::  

## <span data-ttu-id="68fb6-274">déboguer</span><span class="sxs-lookup"><span data-stu-id="68fb6-274">undebug</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="68fb6-275">Arrête le débogage de la méthode spécifiée de telle sorte que lorsque la méthode est appelée, le débogueur n’est plus appelé.</span><span class="sxs-lookup"><span data-stu-id="68fb6-275">Stops the debugging of the specified method so that when the method is called, the debugger is no longer invoked.</span></span>  

```console
undebug(getData);
```  

## <span data-ttu-id="68fb6-276">ne plus surveiller</span><span class="sxs-lookup"><span data-stu-id="68fb6-276">unmonitor</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="68fb6-277">Arrête l’analyse de la méthode spécifiée.</span><span class="sxs-lookup"><span data-stu-id="68fb6-277">Stops the monitoring of the specified method.</span></span>  <span data-ttu-id="68fb6-278">Cette méthode est utilisée en concert avec la méthode [Monitor ()](#monitor) .</span><span class="sxs-lookup"><span data-stu-id="68fb6-278">This method is used in concert with the [monitor()](#monitor) method.</span></span>  

```console
unmonitor(getData);
```  

## <span data-ttu-id="68fb6-279">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="68fb6-279">unmonitorEvents</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="68fb6-280">Arrête de surveiller les événements relatifs aux objets et aux événements spécifiés.</span><span class="sxs-lookup"><span data-stu-id="68fb6-280">Stops monitoring events for the specified object and events.</span></span>  <span data-ttu-id="68fb6-281">Par exemple, la commande suivante arrête tout le suivi des événements sur l’objet Window.</span><span class="sxs-lookup"><span data-stu-id="68fb6-281">For example, the following stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="68fb6-282">Vous pouvez également cesser de surveiller de manière sélective des événements spécifiques sur un objet.</span><span class="sxs-lookup"><span data-stu-id="68fb6-282">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="68fb6-283">Par exemple, le code suivant commence à surveiller tous les `mouse` événements de l’élément actuellement sélectionné, puis cesse de surveiller les `mousemove` événements (il peut s’avérer utile de réduire le bruit dans la sortie de la console).</span><span class="sxs-lookup"><span data-stu-id="68fb6-283">For example, the following code starts monitoring all `mouse` events on the currently selected element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <span data-ttu-id="68fb6-284">doubl</span><span class="sxs-lookup"><span data-stu-id="68fb6-284">values</span></span>  

```console
values(object)
```  

<span data-ttu-id="68fb6-285">Renvoie une matrice contenant les valeurs de toutes les propriétés de l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="68fb6-285">Returns an array containing the values of all properties belonging to the specified object.</span></span>  

```console
values(object);
```  

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
> <span data-ttu-id="68fb6-295">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="68fb6-295">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="68fb6-296">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/utilities) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="68fb6-296">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="68fb6-298">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="68fb6-298">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
