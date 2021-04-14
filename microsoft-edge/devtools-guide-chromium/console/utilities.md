---
description: Référence des commandes pratiques disponibles dans la console Microsoft Edge DevTools.
title: Référence de l’API des utilitaires de console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: c6a0356bd590809f9164aa62fd42156f901cef0f
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483281"
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
# <a name="console-utilities-api-reference"></a><span data-ttu-id="608bd-104">Référence de l’API des utilitaires de console</span><span class="sxs-lookup"><span data-stu-id="608bd-104">Console Utilities API reference</span></span>  

<span data-ttu-id="608bd-105">L'API Des utilitaires de console contient une collection de commandes pratiques pour effectuer les tâches courantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="608bd-105">The Console Utilities API contains a collection of convenience commands to complete the following common tasks.</span></span>  

*   <span data-ttu-id="608bd-106">Choisir et inspecter les éléments DOM</span><span class="sxs-lookup"><span data-stu-id="608bd-106">Choose and inspect DOM elements</span></span>  
*   <span data-ttu-id="608bd-107">Afficher les données dans un format lisible</span><span class="sxs-lookup"><span data-stu-id="608bd-107">Display data in readable format</span></span>  
*   <span data-ttu-id="608bd-108">Arrêter et démarrer le profileur</span><span class="sxs-lookup"><span data-stu-id="608bd-108">Stop and start the profiler</span></span>  
*   <span data-ttu-id="608bd-109">Surveiller les événements DOM</span><span class="sxs-lookup"><span data-stu-id="608bd-109">Monitor DOM events</span></span>  
    
> [!WARNING]
> <span data-ttu-id="608bd-110">Les commandes suivantes fonctionnent uniquement dans la \*\*\*\* console DevTools de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="608bd-110">The following commands only work in the Microsoft Edge DevTools **Console**.</span></span>  <span data-ttu-id="608bd-111">Les commandes ne fonctionnent pas si elles sont exécutés à partir de vos scripts.</span><span class="sxs-lookup"><span data-stu-id="608bd-111">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="608bd-112">Pour plus d'informations sur les méthodes et le reste des méthodes, accédez à Référence de `console.log()` `console.error()` `console.*` [l'API console.][DevToolsConsoleApi]</span><span class="sxs-lookup"><span data-stu-id="608bd-112">For more information about the `console.log()` and `console.error()` methods and the rest of the `console.*` methods, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  

## <a name="recently-evaluated-expression"></a><span data-ttu-id="608bd-113">Expression récemment évaluée</span><span class="sxs-lookup"><span data-stu-id="608bd-113">Recently evaluated expression</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-114">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-114">Console syntax</span></span>  

```console
$_
```  

<span data-ttu-id="608bd-115">Cette commande renvoie la valeur de la dernière expression évaluée.</span><span class="sxs-lookup"><span data-stu-id="608bd-115">This command returns the value of the most recently evaluated expression.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-116">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-116">Console example</span></span>  

<span data-ttu-id="608bd-117">Dans la figure suivante, une expression simple \( `2 + 2` \) est évaluée.</span><span class="sxs-lookup"><span data-stu-id="608bd-117">In the following figure, a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="608bd-118">La `$_` propriété est ensuite évaluée, qui contient la même valeur.</span><span class="sxs-lookup"><span data-stu-id="608bd-118">The `$_` property is then evaluated, which contains the same value.</span></span>  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ est la dernière expression évaluée" lightbox="../media/console-arithmatic.msft.png":::
   `$_` <span data-ttu-id="608bd-120">est l'expression évaluée la plus récente</span><span class="sxs-lookup"><span data-stu-id="608bd-120">is the most recently evaluated expression</span></span>  
:::image-end:::  

<span data-ttu-id="608bd-121">Dans la figure suivante, l'expression évaluée contient initialement un tableau de noms.</span><span class="sxs-lookup"><span data-stu-id="608bd-121">In the following figure, the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="608bd-122">L'évaluation de la longueur du tableau, la valeur stockée dans devient la `$_.length` `$_` dernière expression évaluée, `4` .</span><span class="sxs-lookup"><span data-stu-id="608bd-122">Evaluating `$_.length` to find the length of the array, the value stored in `$_` becomes the latest evaluated expression, `4`.</span></span>  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$_ change lorsque de nouvelles commandes sont évaluées" lightbox="../media/console-array-length.msft.png":::
   `$_` <span data-ttu-id="608bd-124">modifications lors de l'évaluation de nouvelles commandes ;</span><span class="sxs-lookup"><span data-stu-id="608bd-124">changes when new commands are evaluated</span></span>  
:::image-end:::  

---  

## <a name="recently-chosen-element-or-javascript-object"></a><span data-ttu-id="608bd-125">Élément ou objet JavaScript récemment choisi</span><span class="sxs-lookup"><span data-stu-id="608bd-125">Recently chosen element or JavaScript object</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-126">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-126">Console syntax</span></span>  

```console
$0
```  

<span data-ttu-id="608bd-127">Cette commande renvoie l'élément ou l'objet JavaScript le plus récemment choisi.</span><span class="sxs-lookup"><span data-stu-id="608bd-127">This command returns the most recently chosen element or JavaScript object.</span></span>  `$1` <span data-ttu-id="608bd-128">renvoie le deuxième dernier choix, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="608bd-128">returns the second most recently chosen one, and so on.</span></span>  <span data-ttu-id="608bd-129">Les commandes , , et les commandes fonctionnent comme une référence historique aux cinq derniers éléments `$0` `$1` `$2` `$3` `$4` DOM inspectés \*\*\*\* \*\*\*\* dans l'outil Elements ou aux cinq derniers objets de tas JavaScript choisis dans l'outil Mémoire.</span><span class="sxs-lookup"><span data-stu-id="608bd-129">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** tool or the last five JavaScript heap objects chosen in the **Memory** tool.</span></span>  

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
      &nbsp;
   :::column-end:::
:::row-end:::  

### <a name="console-example"></a><span data-ttu-id="608bd-130">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-130">Console example</span></span>  

<span data-ttu-id="608bd-131">Dans la figure suivante, un `img` élément est choisi dans l'outil **Elements.**</span><span class="sxs-lookup"><span data-stu-id="608bd-131">In the following figure, an `img` element is chosen in the **Elements** tool.</span></span>  <span data-ttu-id="608bd-132">Dans le caisse **de** la console, `$0` a été évalué et affiche le même élément.</span><span class="sxs-lookup"><span data-stu-id="608bd-132">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="La valeur $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   <span data-ttu-id="608bd-134">La liste </span><span class="sxs-lookup"><span data-stu-id="608bd-134">The</span></span> `$0`  
:::image-end:::  

<span data-ttu-id="608bd-135">Dans la figure suivante, l'image affiche un autre élément choisi dans la même page web.</span><span class="sxs-lookup"><span data-stu-id="608bd-135">In the following figure, the image displays a different element chosen in the same webpage.</span></span>  <span data-ttu-id="608bd-136">Le `$0` fait maintenant fait référence à l'élément nouvellement choisi, tandis qu'il renvoie `$1` l'élément précédemment choisi.</span><span class="sxs-lookup"><span data-stu-id="608bd-136">The `$0` now refers to the newly chosen element, while `$1` returns the previously chosen one.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="La valeur $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   <span data-ttu-id="608bd-138">La liste </span><span class="sxs-lookup"><span data-stu-id="608bd-138">The</span></span> `$1`  
:::image-end:::  

---  

## <a name="query-selector"></a><span data-ttu-id="608bd-139">Sélecteur de requête</span><span class="sxs-lookup"><span data-stu-id="608bd-139">Query selector</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-140">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-140">Console syntax</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="608bd-141">Cette commande renvoie la référence au premier élément DOM avec le sélecteur CSS spécifié.</span><span class="sxs-lookup"><span data-stu-id="608bd-141">This command returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="608bd-142">Cette méthode est un alias de la [méthode document.querySelector().][MdnDocsWebApiDocumentQueryselector]</span><span class="sxs-lookup"><span data-stu-id="608bd-142">This method is an alias for the [document.querySelector()][MdnDocsWebApiDocumentQueryselector] method.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-143">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-143">Console example</span></span>  

<span data-ttu-id="608bd-144">Dans la figure suivante, une référence au premier `<img>` élément de la page web est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="608bd-144">In the following figure, a reference to the first `<img>` element in the webpage is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$('img')" lightbox="../media/console-element-selector-image.msft.png":::
   <span data-ttu-id="608bd-146">La liste </span><span class="sxs-lookup"><span data-stu-id="608bd-146">The</span></span> `$('img')`  
:::image-end:::  

<span data-ttu-id="608bd-147">Pour rechercher le premier élément dans le DOM ou pour le rechercher et l'afficher sur la page web, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="608bd-147">To find the first element in the DOM or to find and display it on the webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="608bd-148">Pointez sur le résultat renvoyé.</span><span class="sxs-lookup"><span data-stu-id="608bd-148">Hover on the returned result.</span></span>  
1.  <span data-ttu-id="608bd-149">Ouvrez le menu contextuel \(cliquez avec le bouton droit\).</span><span class="sxs-lookup"><span data-stu-id="608bd-149">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="608bd-150">Choisissez **Révéler dans le panneau Éléments.**</span><span class="sxs-lookup"><span data-stu-id="608bd-150">Choose **Reveal in Elements Panel**.</span></span>  

<span data-ttu-id="608bd-151">Dans la figure suivante, une référence à l'élément actuellement choisi est renvoyée et la `src` propriété est affichée.</span><span class="sxs-lookup"><span data-stu-id="608bd-151">In the following figure, a reference to the currently chosen element is returned and the `src` property is displayed.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="Le $('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   <span data-ttu-id="608bd-153">La liste </span><span class="sxs-lookup"><span data-stu-id="608bd-153">The</span></span> `$('img').src`  
:::image-end:::  

<span data-ttu-id="608bd-154">Cette méthode prend également en charge un deuxième paramètre, qui spécifie un élément ou un nœud à partir duquel `startNode` rechercher des éléments.</span><span class="sxs-lookup"><span data-stu-id="608bd-154">This method also supports a second parameter, `startNode`, that specifies an element or node from which to search for elements.</span></span>  <span data-ttu-id="608bd-155">La valeur par défaut du paramètre est `document` .</span><span class="sxs-lookup"><span data-stu-id="608bd-155">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="608bd-156">Dans la figure suivante, le premier élément une fois l'élément trouvé et la `img` `title--image` propriété de `src` `img` l'élément est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="608bd-156">In the following figure, the first `img` element after the `title--image` element is found, and the `src` property of the `img` element is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="The $('img', document.querySelector('title--image')).src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   <span data-ttu-id="608bd-158">La liste </span><span class="sxs-lookup"><span data-stu-id="608bd-158">The</span></span> `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="608bd-159">Si vous utilisez une bibliothèque telle que jQuery qui utilise , la fonctionnalité est écrasée et correspond à l'implémentation de `$` `$` cette bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="608bd-159">If you are using a library such as jQuery that uses `$`, the functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

---  

## <a name="query-selector-all"></a><span data-ttu-id="608bd-160">Sélecteur de requête tout</span><span class="sxs-lookup"><span data-stu-id="608bd-160">Query selector all</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-161">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-161">Console syntax</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="608bd-162">Cette commande renvoie un tableau d'éléments qui correspondent au sélecteur CSS spécifié.</span><span class="sxs-lookup"><span data-stu-id="608bd-162">This command returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="608bd-163">Cette méthode équivaut à l'exécution de la [méthode document.querySelectorAll().][MdnDocsWebApiDocumentQueryselectorall]</span><span class="sxs-lookup"><span data-stu-id="608bd-163">This method is equivalent to running the [document.querySelectorAll()][MdnDocsWebApiDocumentQueryselectorall] method.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-164">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-164">Console example</span></span>  

<span data-ttu-id="608bd-165">Dans l'exemple de code et la figure suivants, utilisez cette procédure pour créer un tableau de tous les éléments de la page web actuelle et afficher la valeur de la propriété `$$()` `<img>` pour chaque `src` élément.</span><span class="sxs-lookup"><span data-stu-id="608bd-165">In the following code sample and figure, use `$$()` to create an array of all `<img>` elements in the current webpage and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Utilisation de $$() pour choisir toutes les images de la page web et afficher les sources" lightbox="../media/console-element-selector-image-all.msft.png":::
   <span data-ttu-id="608bd-167">Utilisation `$$()` pour choisir toutes les images de la page web et afficher les sources</span><span class="sxs-lookup"><span data-stu-id="608bd-167">Using `$$()` to choose all images in the webpage and display the sources</span></span>  
:::image-end:::  

<span data-ttu-id="608bd-168">Cette méthode prend également en charge un deuxième paramètre, qui spécifie un élément ou un nœud à partir duquel `startNode` rechercher des éléments.</span><span class="sxs-lookup"><span data-stu-id="608bd-168">This method also supports a second parameter, `startNode`, that specifies an element or node from which to search for elements.</span></span>  <span data-ttu-id="608bd-169">La valeur par défaut du paramètre est `document` .</span><span class="sxs-lookup"><span data-stu-id="608bd-169">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="608bd-170">Dans l'exemple de code et la figure suivants, une version modifiée de l'exemple de code et de la figure précédents utilise pour créer un tableau de tous les éléments qui apparaissent dans la page web actuelle après le nœud `$$()` `<img>` choisi.</span><span class="sxs-lookup"><span data-stu-id="608bd-170">In the following code sample and figure, a modified version of the previous code sample and figure uses `$$()` to create an array of all `<img>` elements that appear in the current webpage after the chosen node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Using $$() to choose all images that appear after the specified <div> element in the webpage and display the sources" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   <span data-ttu-id="608bd-172">Utilisation `$$()` pour choisir toutes les images qui apparaissent après l'élément spécifié dans la page web et afficher les `<div>` sources</span><span class="sxs-lookup"><span data-stu-id="608bd-172">Using `$$()` to choose all images that appear after the specified `<div>` element in the webpage and display the sources</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="608bd-173">Sélectionnez `Shift` + `Enter` dans la **console** pour démarrer une nouvelle ligne sans l'exécution du script.</span><span class="sxs-lookup"><span data-stu-id="608bd-173">Select `Shift`+`Enter` in the **Console** to start a new line without running the script.</span></span>  

---  

## <a name="xpath"></a><span data-ttu-id="608bd-174">XPath</span><span class="sxs-lookup"><span data-stu-id="608bd-174">XPath</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-175">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-175">Console syntax</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="608bd-176">Cette commande renvoie un tableau d'éléments DOM qui correspondent à l'expression XPath spécifiée.</span><span class="sxs-lookup"><span data-stu-id="608bd-176">This command returns an array of DOM elements that match the specified XPath expression.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-177">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-177">Console example</span></span>  

<span data-ttu-id="608bd-178">Dans l'exemple de code et la figure suivants, tous les éléments `<p>` de la page web sont renvoyés.</span><span class="sxs-lookup"><span data-stu-id="608bd-178">In the following code sample and figure, all of the `<p>` elements on the webpage are returned.</span></span>  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Utilisation d'un sélecteur XPath" lightbox="../media/console-array-xpath.msft.png":::
   <span data-ttu-id="608bd-180">Utilisation d'un sélecteur XPath</span><span class="sxs-lookup"><span data-stu-id="608bd-180">Using an XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="608bd-181">Dans l'exemple de code et la figure suivants, tous les éléments `<p>` qui contiennent des `<a>` éléments sont renvoyés.</span><span class="sxs-lookup"><span data-stu-id="608bd-181">In the following code sample and figure, all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Utilisation d'un sélecteur XPath plus compliqué" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   <span data-ttu-id="608bd-183">Utilisation d'un sélecteur XPath plus compliqué</span><span class="sxs-lookup"><span data-stu-id="608bd-183">Using a more complicated XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="608bd-184">Similaire aux autres commandes de sélecteur, a un deuxième paramètre facultatif, qui spécifie un élément ou un nœud à partir duquel rechercher `$x(path)` `startNode` des éléments.</span><span class="sxs-lookup"><span data-stu-id="608bd-184">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or node from which to search for elements.</span></span>  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Utilisation d'un sélecteur XPath avec startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   <span data-ttu-id="608bd-186">Utilisation d'un sélecteur XPath avec</span><span class="sxs-lookup"><span data-stu-id="608bd-186">Using an XPath selector with</span></span> `startNode`  
:::image-end:::  

---  

## <a name="clear"></a><span data-ttu-id="608bd-187">clear</span><span class="sxs-lookup"><span data-stu-id="608bd-187">clear</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-188">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-188">Console syntax</span></span>  

```console
clear()
```  

<span data-ttu-id="608bd-189">Cette commnad permet d'effacer la console de l'historique.</span><span class="sxs-lookup"><span data-stu-id="608bd-189">This commnad clears the console of the history.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-190">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-190">Console example</span></span>  

```console
clear()
```  

## <a name="copy"></a><span data-ttu-id="608bd-191">copy</span><span class="sxs-lookup"><span data-stu-id="608bd-191">copy</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-192">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-192">Console syntax</span></span>  

```console
copy(object)
```  

<span data-ttu-id="608bd-193">Cette méthode copie une représentation sous la chaîne de l'objet spécifié dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="608bd-193">This method copies a string representation of the specified object to the clipboard.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-194">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-194">Console example</span></span>  

```console
copy($0)
```  

---  

## <a name="debug"></a><span data-ttu-id="608bd-195">déboguer</span><span class="sxs-lookup"><span data-stu-id="608bd-195">debug</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-196">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-196">Console syntax</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="608bd-197">Le [problème Chromium #1050237][CR1050237] suivi d'un bogue avec la `debug()` fonction.</span><span class="sxs-lookup"><span data-stu-id="608bd-197">The [Chromium issue #1050237][CR1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="608bd-198">Si vous rencontrez le problème, essayez plutôt d'utiliser des [points d'arrêt.][DevtoolsJavascriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="608bd-198">If you encounter the issue, try using [breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="608bd-199">Lorsque vous demandez la méthode spécifiée, le déboqueur appelle et s'interrompt à l'intérieur de la méthode sur **l'outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="608bd-199">When you request the specified method, the debugger invokes and breaks inside the method on the **Sources** tool.</span></span>  <span data-ttu-id="608bd-200">Il vous permet d'aller pas à pas et de déboguer le code.</span><span class="sxs-lookup"><span data-stu-id="608bd-200">It allows you to step through and debug the code.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-201">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-201">Console example</span></span>  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Rupture à l'intérieur d'une méthode avec débogage()" lightbox="../media/console-debug-text.msft.png":::
   <span data-ttu-id="608bd-203">Rupture à l'intérieur d'une méthode avec</span><span class="sxs-lookup"><span data-stu-id="608bd-203">Breaking inside a method with</span></span> `debug()`  
:::image-end:::  

<span data-ttu-id="608bd-204">Permet `undebug(method)` d'arrêter de rompre la méthode ou d'utiliser l'interface utilisateur pour désactiver tous les points d'arrêt.</span><span class="sxs-lookup"><span data-stu-id="608bd-204">Use `undebug(method)` to stop breaking on the method, or use the UI to turn off all breakpoints.</span></span>  

<span data-ttu-id="608bd-205">Pour plus d'informations sur les points d'arrêt, accédez à Comment suspendre votre code avec des points d'arrêt dans [Microsoft Edge DevTools][DevtoolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="608bd-205">For more information on breakpoints, navigate to [How to pause your code with breakpoints in Microsoft Edge DevTools][DevtoolsJavascriptBreakpoints].</span></span>  

---  

## <a name="dir"></a><span data-ttu-id="608bd-206">dir</span><span class="sxs-lookup"><span data-stu-id="608bd-206">dir</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-207">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-207">Console syntax</span></span>  

```console
dir(object)
```  

<span data-ttu-id="608bd-208">Cette commande affiche une liste de toutes les propriétés de l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="608bd-208">This command displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="608bd-209">Cette méthode est un alias de la [méthode console.dir().][MdnDocsWebApiConsoleDir]</span><span class="sxs-lookup"><span data-stu-id="608bd-209">This method is an alias for the [console.dir()][MdnDocsWebApiConsoleDir] method.</span></span>  

<span data-ttu-id="608bd-210">Évaluez `document.head` dans la console **pour** afficher le code HTML entre les `<head>` `</head>` balises et les balises.</span><span class="sxs-lookup"><span data-stu-id="608bd-210">Evaluate `document.head` in the **Console** to display the HTML between the `<head>` and `</head>` tags.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-211">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-211">Console example</span></span>  

<span data-ttu-id="608bd-212">Dans l'exemple de code et la figure suivants, une liste de style objet s'affiche après l'utilisation `console.dir()` dans la **console**.</span><span class="sxs-lookup"><span data-stu-id="608bd-212">In the following code sample and figure, an object-style listing is displayed after using `console.dir()` in the **Console**.</span></span>  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Journalisation de document.head avec la méthode dir()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   <span data-ttu-id="608bd-214">Journalisation `document.head` avec `dir()` la méthode</span><span class="sxs-lookup"><span data-stu-id="608bd-214">Logging `document.head` with `dir()` method</span></span>  
:::image-end:::  

<span data-ttu-id="608bd-215">Pour plus d'informations, [accédez à console.dir()][DevToolsConsoleApiConsoleDirObject] dans l'API console.</span><span class="sxs-lookup"><span data-stu-id="608bd-215">For more information, navigate to [console.dir()][DevToolsConsoleApiConsoleDirObject] in the Console API.</span></span>  

---  

## <a name="dirxml"></a><span data-ttu-id="608bd-216">dirxml</span><span class="sxs-lookup"><span data-stu-id="608bd-216">dirxml</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-217">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-217">Console syntax</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="608bd-218">Cette commande imprime une représentation XML de l'objet spécifié, tel qu'il est affiché dans **l'outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="608bd-218">This command prints an XML representation of the specified object, as displayed in the **Elements** tool.</span></span>  <span data-ttu-id="608bd-219">Cette méthode est équivalente à la [méthode console.dirxml().][MdnDocsWebApiConsoleDirxml]</span><span class="sxs-lookup"><span data-stu-id="608bd-219">This method is equivalent to the [console.dirxml()][MdnDocsWebApiConsoleDirxml] method.</span></span>  

---  

## <a name="inspect"></a><span data-ttu-id="608bd-220">inspect</span><span class="sxs-lookup"><span data-stu-id="608bd-220">inspect</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-221">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-221">Console syntax</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="608bd-222">Cette commande s'ouvre et choisit l'élément ou l'objet spécifié dans le \*\*\*\* panneau approprié : l'outil **Elements** pour les éléments DOM ou l'outil Mémoire pour les objets de tas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="608bd-222">This command opens and chooses the specified element or object in the appropriate panel:  either the **Elements** tool for DOM elements or the **Memory** tool for JavaScript heap objects.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-223">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-223">Console example</span></span>  

<span data-ttu-id="608bd-224">Dans l'exemple de code et la figure `document.body` suivants, l'élément s'ouvre dans **l'outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="608bd-224">In the following code sample and figure, the `document.body` opens in the **Elements** tool.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-225">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-225">Console example</span></span>  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Inspection d'un élément avec inspect()" lightbox="../media/console-inspect-document-body.msft.png":::
   <span data-ttu-id="608bd-227">Inspection d'un élément avec</span><span class="sxs-lookup"><span data-stu-id="608bd-227">Inspecting an element with</span></span> `inspect()`  
:::image-end:::  

<span data-ttu-id="608bd-228">Lors de la transmission d'une méthode à inspecter, la méthode ouvre la page web dans l'outil **Sources** que vous pouvez inspecter.</span><span class="sxs-lookup"><span data-stu-id="608bd-228">When passing a method to inspect, the method opens the webpage in the **Sources** tool for you to inspect.</span></span>  

---  

## <a name="geteventlisteners"></a><span data-ttu-id="608bd-229">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="608bd-229">getEventListeners</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-230">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-230">Console syntax</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="608bd-231">Cette commande renvoie les écouteurs d'événements enregistrés sur l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="608bd-231">This command returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="608bd-232">La valeur de retour est un objet qui contient un tableau pour chaque type d'événement enregistré \(par exemple `click` ou `keydown` \).</span><span class="sxs-lookup"><span data-stu-id="608bd-232">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="608bd-233">Les membres de chaque tableau sont des objets qui décrivent l'écoute enregistrée pour chaque type.</span><span class="sxs-lookup"><span data-stu-id="608bd-233">The members of each array are objects that describe the listener registered for each type.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-234">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-234">Console example</span></span>  

<span data-ttu-id="608bd-235">Dans l'extrait de code et la figure suivantes, tous les écouteurs d'événements enregistrés sur `document` l'objet sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="608bd-235">In the following code snippet and figure, all of the event listeners registered on the `document` object are listed.</span></span>  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Sortie de l'utilisation de getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   <span data-ttu-id="608bd-237">Résultat de l'utilisation</span><span class="sxs-lookup"><span data-stu-id="608bd-237">The result of using</span></span> `getEventListeners(document)`  
:::image-end:::  

<span data-ttu-id="608bd-238">Si plusieurs listener sont inscrits sur l'objet spécifié, le tableau contient un membre pour chaque listener.</span><span class="sxs-lookup"><span data-stu-id="608bd-238">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="608bd-239">Dans la figure suivante, deux écouteurs d'événements sont enregistrés sur `document` l'élément pour `click` l'événement.</span><span class="sxs-lookup"><span data-stu-id="608bd-239">In the following figure, two event listeners are registered on the `document` element for the `click` event.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Plusieurs écouteurs" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   <span data-ttu-id="608bd-241">Plusieurs écouteurs</span><span class="sxs-lookup"><span data-stu-id="608bd-241">Multiple listeners</span></span>  
:::image-end:::  

<span data-ttu-id="608bd-242">Vous pouvez développer chacun des objets suivants pour explorer les propriétés.</span><span class="sxs-lookup"><span data-stu-id="608bd-242">You may further expand each of the following objects to explore the properties.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Vue étendue de l'objet d'écoute" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   <span data-ttu-id="608bd-244">Vue étendue de l'objet d'écoute</span><span class="sxs-lookup"><span data-stu-id="608bd-244">Expanded view of listener object</span></span>  
:::image-end:::  

---  

## <a name="keys"></a><span data-ttu-id="608bd-245">clés</span><span class="sxs-lookup"><span data-stu-id="608bd-245">keys</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-246">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-246">Console syntax</span></span>  

```console
keys(object)
```  

<span data-ttu-id="608bd-247">Cette commande renvoie un tableau contenant les noms des propriétés appartenant à l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="608bd-247">This command returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="608bd-248">Pour obtenir les valeurs associées des mêmes propriétés, utilisez `values()` .</span><span class="sxs-lookup"><span data-stu-id="608bd-248">To get the associated values of the same properties, use `values()`.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-249">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-249">Console example</span></span>  

<span data-ttu-id="608bd-250">Par exemple, supposons que votre application a défini l'objet suivant.</span><span class="sxs-lookup"><span data-stu-id="608bd-250">For example, suppose your application defined the following object.</span></span>  

```console
var player1 = {"name": "Ted", "level": 42}
```  

<span data-ttu-id="608bd-251">Dans les exemples de code et la figure suivants, le résultat suppose qu'il a été défini dans l'espace de noms global \(par souci de simplicité\) avant que vous tapiez et dans `player1` `keys(player1)` la `values(player1)` console.</span><span class="sxs-lookup"><span data-stu-id="608bd-251">In the following code samples and figure, the result assumes `player1` was defined in the global namespace \(for simplicity\) before you type `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Commandes keys() et values()" lightbox="../media/console-keys-values.msft.png":::
   <span data-ttu-id="608bd-253">Commandes `keys()` Et `values()`</span><span class="sxs-lookup"><span data-stu-id="608bd-253">The `keys()` and `values()` commands</span></span>  
:::image-end:::  

---  

## <a name="monitor"></a><span data-ttu-id="608bd-254">moniteur</span><span class="sxs-lookup"><span data-stu-id="608bd-254">monitor</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-255">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-255">Console syntax</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="608bd-256">Cette commande enregistre un message dans la console qui indique le nom de la méthode ainsi que les arguments transmis à la méthode dans le cadre d'une demande.</span><span class="sxs-lookup"><span data-stu-id="608bd-256">This command logs a message to the console that indicates the method name along with the arguments passed to the method as part of a request.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-257">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-257">Console example</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="Méthode monitor()" lightbox="../media/console-function-monitor-sum.msft.png":::
   <span data-ttu-id="608bd-259">Méthode `monitor()`</span><span class="sxs-lookup"><span data-stu-id="608bd-259">The `monitor()` method</span></span>  
:::image-end:::  

<span data-ttu-id="608bd-260">À utiliser `unmonitor(method)` pour terminer l'analyse.</span><span class="sxs-lookup"><span data-stu-id="608bd-260">Use `unmonitor(method)` to end monitoring.</span></span>  

---  

## <a name="monitorevents"></a><span data-ttu-id="608bd-261">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="608bd-261">monitorEvents</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-262">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-262">Console syntax</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="608bd-263">Lorsqu'un des événements spécifiés se produit sur l'objet spécifié, l'objet d'événement est consigné dans la console.</span><span class="sxs-lookup"><span data-stu-id="608bd-263">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="608bd-264">Vous pouvez spécifier un seul événement à surveiller, un tableau d'événements ou l'un des types d'événements génériques qui sont mappés à une collection prédéfinie d'événements.</span><span class="sxs-lookup"><span data-stu-id="608bd-264">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-265">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-265">Console example</span></span>  

<span data-ttu-id="608bd-266">Examinez l'exemple de code et la figure suivants.</span><span class="sxs-lookup"><span data-stu-id="608bd-266">Review the following code sample and figure.</span></span>  

<span data-ttu-id="608bd-267">L'exemple suivant surveille tous les événements de resize sur l'objet fenêtre.</span><span class="sxs-lookup"><span data-stu-id="608bd-267">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Événements de resize de fenêtre de surveillance" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   <span data-ttu-id="608bd-269">Événements de resize de fenêtre de surveillance</span><span class="sxs-lookup"><span data-stu-id="608bd-269">Monitoring window resize events</span></span>  
:::image-end:::  

<span data-ttu-id="608bd-270">L'extrait de code suivant définit un tableau pour surveiller à la fois et les événements `resize` `scroll` sur l'objet fenêtre.</span><span class="sxs-lookup"><span data-stu-id="608bd-270">The following code snippet defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="608bd-271">Vous pouvez également spécifier l'un des types d'événements disponibles, les chaînes qui m'indiquent des jeux d'événements prédéfinés.</span><span class="sxs-lookup"><span data-stu-id="608bd-271">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="608bd-272">Le tableau suivant affiche les types d'événements disponibles et les mappages d'événements associés.</span><span class="sxs-lookup"><span data-stu-id="608bd-272">The following table displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="608bd-273">Type d’événement</span><span class="sxs-lookup"><span data-stu-id="608bd-273">Event type</span></span> | <span data-ttu-id="608bd-274">Événements mappés correspondants</span><span class="sxs-lookup"><span data-stu-id="608bd-274">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="608bd-275">« click », « dblclick », « mousedown », « mousemove », « mouseout », « mouseover », « mouseup », « mousewheel »</span><span class="sxs-lookup"><span data-stu-id="608bd-275">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="608bd-276">«keydown», «keypress», «keyup», «textInput»</span><span class="sxs-lookup"><span data-stu-id="608bd-276">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="608bd-277">« touchcancel », « touchend », « touchmove », « touchstart »</span><span class="sxs-lookup"><span data-stu-id="608bd-277">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="608bd-278">«flou», «modifier», «focus», «réinitialiser», «resize», «scroll», «select», «submit», «zoom»</span><span class="sxs-lookup"><span data-stu-id="608bd-278">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="608bd-279">Dans l'exemple de code suivant, le type d'événement correspondant aux événements sur un champ de texte d'entrée est actuellement `key` `key` choisi dans **l'outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="608bd-279">In the following code sample, the `key` event type corresponding to `key` events on an input text field are currently chosen in the **Elements** tool.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="608bd-280">Dans la figure suivante, l'exemple de sortie après la saisie d'un caractère dans le champ de texte s'affiche.</span><span class="sxs-lookup"><span data-stu-id="608bd-280">In the following figure, the sample output after typing a character in the text field is displayed.</span></span>  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Surveillance des événements clés" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   <span data-ttu-id="608bd-282">Surveillance des événements clés</span><span class="sxs-lookup"><span data-stu-id="608bd-282">Monitoring key events</span></span>  
:::image-end:::  

---  

## <a name="profile"></a><span data-ttu-id="608bd-283">profile</span><span class="sxs-lookup"><span data-stu-id="608bd-283">profile</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-284">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-284">Console syntax</span></span>  

```console
profile([name])
```  

<span data-ttu-id="608bd-285">Cette commande démarre une session de profilage de l'UC JavaScript avec un nom facultatif.</span><span class="sxs-lookup"><span data-stu-id="608bd-285">This command starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="608bd-286">La [méthode profileEnd()](#profileend) termine le profil et affiche les résultats dans l'outil Mémoire. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="608bd-286">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** tool.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJsRuntime].  -->  

### <a name="console-example"></a><span data-ttu-id="608bd-287">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-287">Console example</span></span>  

1.  <span data-ttu-id="608bd-288">Exécutez la `profile()` méthode pour démarrer le profilage.</span><span class="sxs-lookup"><span data-stu-id="608bd-288">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="608bd-289">Exécutez [la méthode profileEnd()](#profileend) pour arrêter le profilage et afficher les résultats dans l'outil Mémoire. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="608bd-289">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** tool.</span></span>  

<span data-ttu-id="608bd-290">Les profils peuvent également être imbrmbrés.</span><span class="sxs-lookup"><span data-stu-id="608bd-290">Profiles may also be nested.</span></span>  <span data-ttu-id="608bd-291">Dans la figure et les exemples de code suivants, le résultat est le même quel que soit l'ordre.</span><span class="sxs-lookup"><span data-stu-id="608bd-291">In the following code samples and figure, the result is the same whatever the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="608bd-292">Plusieurs profils d'UC peuvent fonctionner en même temps et vous n'êtes pas obligé de fermer chacun d'eux dans l'ordre de création.</span><span class="sxs-lookup"><span data-stu-id="608bd-292">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

---  

## <a name="profileend"></a><span data-ttu-id="608bd-293">profileEnd</span><span class="sxs-lookup"><span data-stu-id="608bd-293">profileEnd</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-294">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-294">Console syntax</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="608bd-295">Cette commande termine une session de profilage de l'UC JavaScript et affiche les résultats dans **l'outil** Mémoire.</span><span class="sxs-lookup"><span data-stu-id="608bd-295">This command completes a JavaScript CPU profiling session and displays the results in the **Memory** tool.</span></span>  <span data-ttu-id="608bd-296">Vous devez être en cours d'exécution [de la méthode profile().](#profile)</span><span class="sxs-lookup"><span data-stu-id="608bd-296">You must be running the [profile()](#profile) method.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJsRuntime].  -->  

### <a name="console-example"></a><span data-ttu-id="608bd-297">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-297">Console example</span></span>  

1.  <span data-ttu-id="608bd-298">Exécutez [la méthode profile()](#profile) pour démarrer le profilage.</span><span class="sxs-lookup"><span data-stu-id="608bd-298">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="608bd-299">Exécutez la `profileEnd()` méthode pour arrêter le profilage et afficher les résultats dans l'outil Mémoire. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="608bd-299">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** tool.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="608bd-300">Les profils peuvent également être imbrmbrés.</span><span class="sxs-lookup"><span data-stu-id="608bd-300">Profiles may also be nested.</span></span>  <span data-ttu-id="608bd-301">Dans l'exemple de code et la figure suivants, le résultat est le même quelle que soit la commande.</span><span class="sxs-lookup"><span data-stu-id="608bd-301">In the following code sample and figure, the result is the same whatever the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="608bd-302">Le résultat s'affiche sous la mesure d'une capture instantanée de tas dans **l'outil Mémoire.**</span><span class="sxs-lookup"><span data-stu-id="608bd-302">The result appears as a Heap Snapshot in the **Memory** tool.</span></span>  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Profils groupés" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   <span data-ttu-id="608bd-304">Profils groupés</span><span class="sxs-lookup"><span data-stu-id="608bd-304">Grouped profiles</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="608bd-305">Plusieurs profils d'UC peuvent fonctionner en même temps et vous n'êtes pas obligé de fermer chacun d'eux dans l'ordre de création.</span><span class="sxs-lookup"><span data-stu-id="608bd-305">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

---  

## <a name="queryobjects"></a><span data-ttu-id="608bd-306">queryObjects</span><span class="sxs-lookup"><span data-stu-id="608bd-306">queryObjects</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-307">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-307">Console syntax</span></span>  

```console
queryObjects(Constructor)
```  

<span data-ttu-id="608bd-308">Cette commande renvoie un tableau d'objets créés avec le constructeur spécifié.</span><span class="sxs-lookup"><span data-stu-id="608bd-308">This command returns an array of objects created with the specified constructor.</span></span>  <span data-ttu-id="608bd-309">L'étendue `queryObjects()` est le contexte d'runtime actuellement choisi dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="608bd-309">The scope of `queryObjects()` is the currently chosen runtime context in the **Console**.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-310">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-310">Console example</span></span>  

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      <span data-ttu-id="608bd-311">Renvoie tout `Promises` .</span><span class="sxs-lookup"><span data-stu-id="608bd-311">Returns all `Promises`.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      <span data-ttu-id="608bd-312">Renvoie tous les éléments HTML.</span><span class="sxs-lookup"><span data-stu-id="608bd-312">Returns all HTML elements.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      <span data-ttu-id="608bd-313">Renvoie tous les objets qui ont été ins instantiés à l'aide `new functionName()` de .</span><span class="sxs-lookup"><span data-stu-id="608bd-313">Returns all objects that were instantiated using `new functionName()`.</span></span>  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a><span data-ttu-id="608bd-314">table</span><span class="sxs-lookup"><span data-stu-id="608bd-314">table</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-315">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-315">Console syntax</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="608bd-316">Cette commande enregistre les données d'objet avec une mise en forme de tableau basée sur l'objet de données avec des en-tête de colonne facultatifs.</span><span class="sxs-lookup"><span data-stu-id="608bd-316">This command logs object data with table formatting based upon the data object in with optional column headings.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-317">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-317">Console example</span></span>  

<span data-ttu-id="608bd-318">Dans l'exemple de code et la figure suivants, une liste de noms utilisant un tableau dans la console s'affiche.</span><span class="sxs-lookup"><span data-stu-id="608bd-318">In the following code sample and figure, a list of names using a table in the console is displayed.</span></span>  

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
   <span data-ttu-id="608bd-320">Résultat de la `table()` méthode</span><span class="sxs-lookup"><span data-stu-id="608bd-320">The result of the `table()` method</span></span>  
:::image-end:::  

---  

## <a name="undebug"></a><span data-ttu-id="608bd-321">undebug</span><span class="sxs-lookup"><span data-stu-id="608bd-321">undebug</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-322">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-322">Console syntax</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="608bd-323">Cette commande arrête le débogage de la méthode spécifiée.</span><span class="sxs-lookup"><span data-stu-id="608bd-323">This command stops the debug of the specified method.</span></span> <span data-ttu-id="608bd-324">Ainsi, lorsque la méthode est demandée, le débogger n'est plus appelé.</span><span class="sxs-lookup"><span data-stu-id="608bd-324">So when the method is requested, the debugger is no longer invoked.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-325">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-325">Console example</span></span>  

```console
undebug(getData);
```  

---  

## <a name="unmonitor"></a><span data-ttu-id="608bd-326">unmonitor</span><span class="sxs-lookup"><span data-stu-id="608bd-326">unmonitor</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-327">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-327">Console syntax</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="608bd-328">Cette commande arrête la surveillance de la méthode spécifiée.</span><span class="sxs-lookup"><span data-stu-id="608bd-328">This command stops the monitoring of the specified method.</span></span>  <span data-ttu-id="608bd-329">Cette méthode est utilisée de concert avec la [méthode monitor().](#monitor)</span><span class="sxs-lookup"><span data-stu-id="608bd-329">This method is used in concert with the [monitor()](#monitor) method.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-330">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-330">Console example</span></span>  

```console
unmonitor(getData);
```  

---  

## <a name="unmonitorevents"></a><span data-ttu-id="608bd-331">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="608bd-331">unmonitorEvents</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-332">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-332">Console syntax</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="608bd-333">Cette commande arrête la surveillance des événements pour l'objet et les événements spécifiés.</span><span class="sxs-lookup"><span data-stu-id="608bd-333">This command stops monitoring events for the specified object and events.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-334">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-334">Console example</span></span>  

<span data-ttu-id="608bd-335">Par exemple, l'extrait de code suivant arrête toute surveillance des événements sur l'objet fenêtre.</span><span class="sxs-lookup"><span data-stu-id="608bd-335">For example, the following code snippet stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="608bd-336">Vous pouvez également arrêter de manière sélective la surveillance d'événements spécifiques sur un objet.</span><span class="sxs-lookup"><span data-stu-id="608bd-336">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="608bd-337">Par exemple, le code suivant démarre la surveillance de tous les événements sur l'élément actuellement choisi, puis arrête la surveillance des événements \(peut-être pour réduire le bruit dans la `mouse` `mousemove` sortie de la console\).</span><span class="sxs-lookup"><span data-stu-id="608bd-337">For example, the following code starts monitoring all `mouse` events on the currently chosen element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

---  

## <a name="values"></a><span data-ttu-id="608bd-338">values</span><span class="sxs-lookup"><span data-stu-id="608bd-338">values</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="608bd-339">Syntaxe de la console</span><span class="sxs-lookup"><span data-stu-id="608bd-339">Console syntax</span></span>  

```console
values(object)
```  

<span data-ttu-id="608bd-340">Cette commande renvoie un tableau contenant les valeurs de toutes les propriétés appartenant à l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="608bd-340">This command returns an array containing the values of all properties belonging to the specified object.</span></span>  

### <a name="console-example"></a><span data-ttu-id="608bd-341">Exemple de console</span><span class="sxs-lookup"><span data-stu-id="608bd-341">Console example</span></span>  

```console
values(object);
```  

---  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="608bd-342">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="608bd-342">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Référence de l'API de console | Documents Microsoft"  
[DevToolsConsoleApiConsoleDirObject]: ./api.md#dir "dir - Console API reference | Documents Microsoft"  

[DevtoolsJavascriptBreakpoints]: ../javascript/breakpoints.md "Comment suspendre votre code avec des points d'arrêt dans Microsoft Edge DevTools | Documents Microsoft"  

[DevtoolsRenderingToolsJsRuntime]: ../rendering-tools/js-runtime.md "Accélérer le runtime JavaScript | Documents Microsoft"  

[CR1050237]: https://crbug.com/1050237 "Problème 1050237 : débogage(fonction) ne fonctionne pas | Bogues Chromium"  

[MdnDocsWebApiConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MdnDocsWebApiConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MdnDocsWebApiDocumentQueryselector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MdnDocsWebApiDocumentQueryselectorall]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

> [!NOTE]
> <span data-ttu-id="608bd-352">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="608bd-352">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="608bd-353">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/utilities) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="608bd-353">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="608bd-355">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="608bd-355">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
