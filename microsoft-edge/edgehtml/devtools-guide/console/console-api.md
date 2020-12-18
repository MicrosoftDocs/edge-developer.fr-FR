---
description: Utiliser l’API de console pour déboguer et profiler votre code par programmation
title: DevTools-console-API de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, API console
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 46a74b80b504358ff7dbea40970528c8e2b228cf
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232928"
---
# <span data-ttu-id="ecb8f-104">API de la console</span><span class="sxs-lookup"><span data-stu-id="ecb8f-104">Console API</span></span>

<span data-ttu-id="ecb8f-105">L' *API console* fournit un accès par programmation et en ligne de commande à la console devtools par le biais de l' `console` objet global, ce qui vous permet d’effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-105">The *Console API* provides command-line and programmatic access to the  DevTools Console through the global `console` object, allowing you to:</span></span>

 - <span data-ttu-id="ecb8f-106">[Enregistrer les messages personnalisés](#logging-custom-messages) de votre code</span><span class="sxs-lookup"><span data-stu-id="ecb8f-106">[Log custom messages](#logging-custom-messages) from you code</span></span>
 - <span data-ttu-id="ecb8f-107">[Inspecter des objets et des éléments](#inspecting-objects-and-elements) et enregistrer leurs informations</span><span class="sxs-lookup"><span data-stu-id="ecb8f-107">[Inspect objects and elements](#inspecting-objects-and-elements) and log their information</span></span>
 - <span data-ttu-id="ecb8f-108">[Tester et mesurer votre code](#testing-and-measuring) en définissant des affirmations, minuteurs et compteurs</span><span class="sxs-lookup"><span data-stu-id="ecb8f-108">[Test and measure your code](#testing-and-measuring) by setting assertions, timers and counters</span></span>
 - <span data-ttu-id="ecb8f-109">[Utiliser des instantanés du tas](#taking-heap-snapshots) pour évaluer la consommation de mémoire de votre code en cours d’exécution et identifier les fuites de mémoire</span><span class="sxs-lookup"><span data-stu-id="ecb8f-109">[Take snapshots of the heap](#taking-heap-snapshots) to assess the memory consumption of your running code and identify memory leaks</span></span>
 - <span data-ttu-id="ecb8f-110">[Tracer votre callstacks](#tracing-callstacks) pour comprendre l’emplacement à partir duquel votre code est appelé</span><span class="sxs-lookup"><span data-stu-id="ecb8f-110">[Trace your callstacks](#tracing-callstacks) to understand where your code is being called from</span></span> 
 - <span data-ttu-id="ecb8f-111">[Organiser votre sortie journal](#organizing-log-output) pour rationaliser votre débogage</span><span class="sxs-lookup"><span data-stu-id="ecb8f-111">[Organize your log output](#organizing-log-output) to streamline your debugging</span></span>

<span data-ttu-id="ecb8f-112">Voici les commandes et les paramètres de mise en forme actuellement pris en charge par Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-112">The following are the commands and formatting parameters currently supported by Microsoft Edge.</span></span> <span data-ttu-id="ecb8f-113">Ils fonctionnent de la même manière sur les navigateurs les plus importants.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-113">They work similarly on major browsers.</span></span>

## <span data-ttu-id="ecb8f-114">Journalisation des messages personnalisés</span><span class="sxs-lookup"><span data-stu-id="ecb8f-114">Logging custom messages</span></span>

<span data-ttu-id="ecb8f-115">Votre code peut envoyer différents types de messages personnalisés à la console, à savoir:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-115">Your code can send several types of custom messages to the console, including:</span></span>

<span data-ttu-id="ecb8f-116">Type de message</span><span class="sxs-lookup"><span data-stu-id="ecb8f-116">Message type</span></span>  | &nbsp;   |
:------------------- | :------ |
<span data-ttu-id="ecb8f-117">[**erreur ()**](https://developer.mozilla.org/docs/Web/API/Console/error) et [ **exception ()**](https://developer.mozilla.org/docs/Web/API/Console/error)</span><span class="sxs-lookup"><span data-stu-id="ecb8f-117">[**error()**](https://developer.mozilla.org/docs/Web/API/Console/error) and [**exception()**](https://developer.mozilla.org/docs/Web/API/Console/error)</span></span>| <span data-ttu-id="ecb8f-118">Erreurs critiques et échecs</span><span class="sxs-lookup"><span data-stu-id="ecb8f-118">Critical errors and failures</span></span>
[**<span data-ttu-id="ecb8f-119">Warn ()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-119">warn()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/warn) | <span data-ttu-id="ecb8f-120">Erreurs possibles ou comportement inattendu</span><span class="sxs-lookup"><span data-stu-id="ecb8f-120">Possible errors or unexpected behavior</span></span> 
[**<span data-ttu-id="ecb8f-121">info ()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-121">info()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/info) | <span data-ttu-id="ecb8f-122">Informations utiles, mais non critiques</span><span class="sxs-lookup"><span data-stu-id="ecb8f-122">Useful, but non-critical information</span></span>
<span data-ttu-id="ecb8f-123">[**log ()**](https://developer.mozilla.org/docs/Web/API/Console/log) et [ **debug ()**](https://developer.mozilla.org/docs/Web/API/Console/log)</span><span class="sxs-lookup"><span data-stu-id="ecb8f-123">[**log()**](https://developer.mozilla.org/docs/Web/API/Console/log) and [**debug()**](https://developer.mozilla.org/docs/Web/API/Console/log)</span></span> | <span data-ttu-id="ecb8f-124">Débogage général (sans générer d’icône d’alerte système dans la console)</span><span class="sxs-lookup"><span data-stu-id="ecb8f-124">General debugging (without generating a system alert icon in the console)</span></span>

   
<span data-ttu-id="ecb8f-125">Vous pouvez les regrouper et les filtrer en même temps que les autres messages générés par Microsoft Edge à partir de la console.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-125">You can group and filter these along with the other messages generated from Microsoft Edge from the  Console panel.</span></span> <span data-ttu-id="ecb8f-126">Toutes les méthodes de message personnalisées nécessitent un paramètre de chaîne (message) et des paramètres de substitution de format facultatif.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-126">All custom message methods require a string (message) parameter and optional format substitution parameters.</span></span> <span data-ttu-id="ecb8f-127">Microsoft Edge prend en charge les options de mise en forme suivantes:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-127">Microsoft Edge supports the following formatting options:</span></span>

<span data-ttu-id="ecb8f-128">Paramètre format</span><span class="sxs-lookup"><span data-stu-id="ecb8f-128">Format parameter</span></span> | &nbsp;
:------------------- | :--- |
**<span data-ttu-id="ecb8f-129">% b</span><span class="sxs-lookup"><span data-stu-id="ecb8f-129">%b</span></span>** | <span data-ttu-id="ecb8f-130">Binaire</span><span class="sxs-lookup"><span data-stu-id="ecb8f-130">Binary</span></span>
**<span data-ttu-id="ecb8f-131">% c</span><span class="sxs-lookup"><span data-stu-id="ecb8f-131">%c</span></span>** | <span data-ttu-id="ecb8f-132">Style CSS intraligne (Voir l’exemple ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="ecb8f-132">Inline CSS style (see example below)</span></span>
<span data-ttu-id="ecb8f-133">**% d**, **% i**</span><span class="sxs-lookup"><span data-stu-id="ecb8f-133">**%d**, **%i**</span></span> | <span data-ttu-id="ecb8f-134">entier.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-134">Integer</span></span> 
**<span data-ttu-id="ecb8f-135">% f</span><span class="sxs-lookup"><span data-stu-id="ecb8f-135">%f</span></span>** | <span data-ttu-id="ecb8f-136">Flottant</span><span class="sxs-lookup"><span data-stu-id="ecb8f-136">Float</span></span>  
**<span data-ttu-id="ecb8f-137">% s</span><span class="sxs-lookup"><span data-stu-id="ecb8f-137">%s</span></span>** | <span data-ttu-id="ecb8f-138">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ecb8f-138">String</span></span> 
**<span data-ttu-id="ecb8f-139">% x</span><span class="sxs-lookup"><span data-stu-id="ecb8f-139">%x</span></span>** | <span data-ttu-id="ecb8f-140">Hexadécimal</span><span class="sxs-lookup"><span data-stu-id="ecb8f-140">Hexadecimal</span></span> 
**<span data-ttu-id="ecb8f-141">% e</span><span class="sxs-lookup"><span data-stu-id="ecb8f-141">%e</span></span>** | <span data-ttu-id="ecb8f-142">Négatifs</span><span class="sxs-lookup"><span data-stu-id="ecb8f-142">Exponent</span></span> 

<span data-ttu-id="ecb8f-143">Par exemple, voici comment inclure les variables chaîne et entier dans votre message électronique:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-143">For example, here's how you would include string and integer variables in your log message:</span></span>

```javascript
var myText = 'pieces';
var myVal = 5;
console.log("The number of %s is %d.", myText, myVal);
```

>`The number of pieces is 5.`

<span data-ttu-id="ecb8f-144">Vous pouvez également ajouter un effet de surbrillance vert à un message électronique avec une feuille de style CSS inline ( `%c` ):</span><span class="sxs-lookup"><span data-stu-id="ecb8f-144">And here's how you might add a green highlight effect to a log message with inline CSS (`%c`):</span></span>

```javascript
console.log("%cHighlight this log message in green", "background-color: #10ff00; text-transform: uppercase;");
```

![Journal de console avec styles intralignes](../media/console_api_css.png)

## <span data-ttu-id="ecb8f-146">Inspecter des objets et des éléments</span><span class="sxs-lookup"><span data-stu-id="ecb8f-146">Inspecting objects and elements</span></span>

<span data-ttu-id="ecb8f-147">Les objets inspectables apparaissent dans la console dans une arborescence réduite avec des nœuds extensibles.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-147">Inspectable objects appear in the console in a collapsed tree view with expandable nodes.</span></span> <span data-ttu-id="ecb8f-148">La console détecte si vous envoyez un nœud DOM (par exemple, une balise div) ou un objet JavaScript (par exemple, un événement) et que vous les affichez automatiquement en tant que type détecté.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-148">The console detects whether you are sending a DOM node (like a div) or a JavaScript object (like an event) and displays them as the detected type automatically.</span></span>

<span data-ttu-id="ecb8f-149">Vous pouvez également forcer une sortie spécifique:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-149">You can also force a specific output:</span></span>

<span data-ttu-id="ecb8f-150">Commande</span><span class="sxs-lookup"><span data-stu-id="ecb8f-150">Command</span></span> | &nbsp;
:------------------- | :--- |
[**<span data-ttu-id="ecb8f-151">dir ()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-151">dir()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/dir) | <span data-ttu-id="ecb8f-152">Affiche en tant qu’objet JavaScript inspectable</span><span class="sxs-lookup"><span data-stu-id="ecb8f-152">Displays as inspectable JavaScript object</span></span>
[**<span data-ttu-id="ecb8f-153">dirxml()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-153">dirxml()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/dirxml) | <span data-ttu-id="ecb8f-154">Affiche en tant que nœud DOM inspectable</span><span class="sxs-lookup"><span data-stu-id="ecb8f-154">Displays as inspectable DOM node</span></span>

<span data-ttu-id="ecb8f-155">Par exemple, essayez d’ouvrir la console et de comparer les sorties suivantes pour l' `<div id='main'>` élément sur cette page:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-155">For example, try opening the console and compare the following outputs for the `<div id='main'>` element on this page:</span></span>

```javascript
console.dir(document.querySelector('#main'));
console.dirxml(document.querySelector('#main'));
```

![Comparaison de la sortie «dir» par rapport à «DirXML»](../media/console_api_dir.png)

### <span data-ttu-id="ecb8f-157">Sélection d’un élément dans le panneau **éléments**</span><span class="sxs-lookup"><span data-stu-id="ecb8f-157">Selecting an element in the **Elements** panel</span></span>

<span data-ttu-id="ecb8f-158">Vous pouvez sélectionner un élément à l’intérieur du contexte d’arborescence HTML de la page directement dans la console pour le débogage immédiat de la disposition et du style.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-158">You can select an element within the HTML tree context of the page directly from the console for immediate layout and style debugging.</span></span>

<span data-ttu-id="ecb8f-159">Commande</span><span class="sxs-lookup"><span data-stu-id="ecb8f-159">Command</span></span> | &nbsp;
:------------------- | :--- |
**<span data-ttu-id="ecb8f-160">Select ()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-160">select()</span></span>** | <span data-ttu-id="ecb8f-161">Bascule vers le panneau **éléments** et positionne le focus sur l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-161">Switches to the **Elements** panel and sets focus to the specified element.</span></span>

<span data-ttu-id="ecb8f-162">Par exemple, si vous ouvrez la console sur cette page et tapez:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-162">For example, if you open the console on this page and type:</span></span>

```javascript
console.select(document.querySelector("body"));
```

<span data-ttu-id="ecb8f-163">Le DevTools bascule vers le panneau **éléments** (s’il n’est pas déjà actif) et définit le focus dans l' [*arborescence html*](../elements.md#html-tree-view) pour l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-163">The DevTools will switch to the **Elements** panel (if its not already the current) and set focus in the [*HTML tree view*](../elements.md#html-tree-view) to the specified element.</span></span>

![Exemple de la méthode «Select»](../media/console_api_select.png)

## <span data-ttu-id="ecb8f-165">Tests et mesures</span><span class="sxs-lookup"><span data-stu-id="ecb8f-165">Testing and measuring</span></span>

### <span data-ttu-id="ecb8f-166">Test de votre code</span><span class="sxs-lookup"><span data-stu-id="ecb8f-166">Testing your code</span></span>

<span data-ttu-id="ecb8f-167">Ajoutez des affirmations de test de l’API console à votre code pour le test unitaire et le débogage de votre code au fur et à mesure qu’il s’exécute dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-167">Add Console API test assertions to your code for unit testing and debugging your code as it runs in the browser.</span></span>

<span data-ttu-id="ecb8f-168">Commande</span><span class="sxs-lookup"><span data-stu-id="ecb8f-168">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="ecb8f-169">assertion ()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-169">assert()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/assert) | <span data-ttu-id="ecb8f-170">Consigne un message d’erreur de console si l’expression fournie a pour résultat la *valeur faux*.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-170">Logs a console error message if the provided expression evaluates to *false*.</span></span>

<span data-ttu-id="ecb8f-171">Outre l’expression logique fournie en tant qu’assertion testable, vous pouvez ajouter un message facultatif et des paramètres de mise en forme comme vous le feriez avec d’autres [messages de console personnalisés](#logging-custom-messages).</span><span class="sxs-lookup"><span data-stu-id="ecb8f-171">In addition to the logical expression you supply as the testable assertion, you can add an optional message and formatting parameters as you would use with other [custom console messages](#logging-custom-messages).</span></span> <span data-ttu-id="ecb8f-172">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-172">For example:</span></span>

```javascript
var x = 26.8;
console.assert(x < 25, 'The value of x is %f (it is NOT less than %i)', x, 25);
```

![Exemple de la méthode «assertion»](../media/console_api_assert.png)

### <span data-ttu-id="ecb8f-174">Comptage des exécutions dans votre code</span><span class="sxs-lookup"><span data-stu-id="ecb8f-174">Counting executions in your code</span></span>

<span data-ttu-id="ecb8f-175">Vous pouvez définir des compteurs dans votre code pour suivre le nombre de fois que le code environnant est exécuté.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-175">You can set counters in your code to keep track of how many times the surrounding code gets executed.</span></span> <span data-ttu-id="ecb8f-176">La définition de compteurs permet de garantir que votre code s’exécute comme prévu et vous aide à diagnostiquer les goulets d’étranglement de performances.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-176">Setting counters can help ensure your code is running as expected and assist you in diagnosing performance bottlenecks.</span></span>

<span data-ttu-id="ecb8f-177">Commande</span><span class="sxs-lookup"><span data-stu-id="ecb8f-177">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="ecb8f-178">Count ()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-178">count()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/count) | <span data-ttu-id="ecb8f-179">Augmente et enregistre le nombre de fois que le nombre de fois *()* pour l’étiquette donnée a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-179">Increments and logs the number of times *count()* for the given label has been executed.</span></span>
[**<span data-ttu-id="ecb8f-180">countReset()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-180">countReset()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/countReset) | <span data-ttu-id="ecb8f-181">Rétablit le nombre à zéro pour l’étiquette de compteur fournie.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-181">Resets the count to zero for the given counter label.</span></span>

<span data-ttu-id="ecb8f-182">Par exemple, en exécutant les lignes suivantes dans la console:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-182">For example, executing the following lines in console:</span></span>

```javascript
console.count('My Counter');
console.count('My Counter');
console.countReset('My Counter');
console.count('My Counter');
```

 <span data-ttu-id="ecb8f-183">.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-183">.</span></span> <span data-ttu-id="ecb8f-184">.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-184">.</span></span> <span data-ttu-id="ecb8f-185">.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-185">.</span></span> <span data-ttu-id="ecb8f-186">entraînera:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-186">will result in:</span></span>
> <span data-ttu-id="ecb8f-187">Mon compteur: 1</span><span class="sxs-lookup"><span data-stu-id="ecb8f-187">My Counter: 1</span></span>

### <span data-ttu-id="ecb8f-188">Chronométrage de votre code</span><span class="sxs-lookup"><span data-stu-id="ecb8f-188">Timing your code</span></span>

<span data-ttu-id="ecb8f-189">Instrumentez votre code avec des minuteurs étiquetés pour mesurer le temps nécessaire à l’exécution d’une opération donnée.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-189">Instrument your code with labeled timers to measure how long it takes to complete a given operation.</span></span>

<span data-ttu-id="ecb8f-190">Commande</span><span class="sxs-lookup"><span data-stu-id="ecb8f-190">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="ecb8f-191">Time ()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-191">time()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/time) | <span data-ttu-id="ecb8f-192">Démarre un minuteur avec l’étiquette fournie.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-192">Starts a timer with the given label.</span></span>
[**<span data-ttu-id="ecb8f-193">timeEnd()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-193">timeEnd()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/timeEnd) | <span data-ttu-id="ecb8f-194">Termine le minuteur avec l’étiquette spécifiée et indique le temps écoulé (en millisecondes).</span><span class="sxs-lookup"><span data-stu-id="ecb8f-194">Ends the timer with the given label and reports the time elapsed (in milliseconds).</span></span>
[**<span data-ttu-id="ecb8f-195">timeStamp ()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-195">timeStamp()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/timeStamp) | <span data-ttu-id="ecb8f-196">Indique l’heure actuelle du système (en millisecondes).</span><span class="sxs-lookup"><span data-stu-id="ecb8f-196">Reports the current system time (in milliseconds).</span></span>

<span data-ttu-id="ecb8f-197">Par exemple, essayez d’exécuter les lignes suivantes dans la console:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-197">For example, try executing the following lines in console:</span></span>

```javascript
console.time('My Timer');
console.timeEnd('My Timer');
```

### <span data-ttu-id="ecb8f-198">Captures d’instantanés de tas</span><span class="sxs-lookup"><span data-stu-id="ecb8f-198">Taking heap snapshots</span></span>

<span data-ttu-id="ecb8f-199">Prenez des instantanés du tas pour évaluer la consommation de mémoire de votre code en cours d’exécution et identifier les fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-199">Take snapshots of the heap to assess the memory consumption of your running code and identify memory leaks.</span></span>

<span data-ttu-id="ecb8f-200">Commande</span><span class="sxs-lookup"><span data-stu-id="ecb8f-200">Command</span></span> | &nbsp;
:------------ | :-------------
**<span data-ttu-id="ecb8f-201">takeHeapSnapshot()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-201">takeHeapSnapshot()</span></span>** | <span data-ttu-id="ecb8f-202">Capture les détails du tas JavaScript actuel et de ses objets attribués.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-202">Captures details about the current JavaScript heap and its allocated objects.</span></span>

<span data-ttu-id="ecb8f-203">Le [testeur de mémoire](../memory.md#toolbar) devtools doit être en cours d’exécution pour pouvoir utiliser des instantanés de tas.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-203">The  DevTools [memory profiler](../memory.md#toolbar) must be running in order to take heap snapshots.</span></span> <span data-ttu-id="ecb8f-204">Chaque photo apparaît sous la forme d’une vignette dans la [*synthèse de capture instantanée*](../memory.md#snapshot-summary) du panneau [**mémoire**](../memory.md) pour une inspection plus poussée.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-204">Each snapshot will appear as a tile in the [*Snapshot summary*](../memory.md#snapshot-summary) of the [**Memory**](../memory.md) panel for further inspection.</span></span>

## <span data-ttu-id="ecb8f-205">Suivi de callstacks</span><span class="sxs-lookup"><span data-stu-id="ecb8f-205">Tracing callstacks</span></span>

<span data-ttu-id="ecb8f-206">Le fait de comprendre l’objet de l’appel de votre code, le code en cours d’exécution et la durée nécessaire à l’exécution pour l’analyse de la lenteur ou du comportement inattendu.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-206">Understanding where your code is being called from, what code is running, and how long that execution takes can be useful in analyzing slowness or unexpected behavior.</span></span> <span data-ttu-id="ecb8f-207">Une trace de pile indique le chemin d’exécution que votre code a pris pour y accéder, à partir de la demande de suivi via le chemin.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-207">A stack trace shows you the execution path your code took to reach it, from the trace request upward through the path.</span></span> 

<span data-ttu-id="ecb8f-208">Commande</span><span class="sxs-lookup"><span data-stu-id="ecb8f-208">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="ecb8f-209">trace ()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-209">trace()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/trace) | <span data-ttu-id="ecb8f-210">Génère une trace de la pile des appels d’exécution du script actuelle.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-210">Outputs a trace of the current script execution callstack.</span></span>

<span data-ttu-id="ecb8f-211">Par exemple, en exécutant le code suivant dans la console:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-211">For example, running the following code in the console:</span></span>

```javascript
function a(){
  c();
}
function b(){
  c();
}
function c(){
  console.trace()
}
function d(){
  b();
}

a();
d();
```

<span data-ttu-id="ecb8f-212">.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-212">.</span></span> <span data-ttu-id="ecb8f-213">.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-213">.</span></span> <span data-ttu-id="ecb8f-214">.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-214">.</span></span> <span data-ttu-id="ecb8f-215">va générer les traces de pile suivantes:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-215">will output the following stack traces:</span></span>
> <span data-ttu-id="ecb8f-216">Console. trace () sur c (code eval: 8:3) à a (code eval: 2:3) sur le code d’évaluation (code d’évaluation: 14:1)</span><span class="sxs-lookup"><span data-stu-id="ecb8f-216">console.trace() at c (eval code:8:3) at a (eval code:2:3) at eval code (eval code:14:1)</span></span>
> 
> <span data-ttu-id="ecb8f-217">Console. trace () sur c (code d’erreur: 8:3) à l’adresse b (code d’évaluation: 5:3) sur le code d’erreur (code d’erreur 11:3).</span><span class="sxs-lookup"><span data-stu-id="ecb8f-217">console.trace() at c (eval code:8:3) at b (eval code:5:3) at d (eval code:11:3) at eval code (eval code:15:1)</span></span>

## <span data-ttu-id="ecb8f-218">Organisation de la sortie Journal</span><span class="sxs-lookup"><span data-stu-id="ecb8f-218">Organizing log output</span></span>

<span data-ttu-id="ecb8f-219">Pour effacer toute la sortie de la console précédente, utilisez *console. Clear ()* (ou `CTRL + L` ).</span><span class="sxs-lookup"><span data-stu-id="ecb8f-219">To simply clear all previous console output, use *console.clear()* (or `CTRL + L`).</span></span> <span data-ttu-id="ecb8f-220">Cela n’efface pas la pile de l’historique de commandes de votre console (vous pouvez toujours l’utiliser avec les touches de direction vers le haut et vers le bas).</span><span class="sxs-lookup"><span data-stu-id="ecb8f-220">This does not clear the backstack of your console command history (you can still traverse it with the up and down arrow keys).</span></span>

<span data-ttu-id="ecb8f-221">Commande</span><span class="sxs-lookup"><span data-stu-id="ecb8f-221">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="ecb8f-222">Clear ()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-222">clear()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/clear) | <span data-ttu-id="ecb8f-223">Efface toutes les sorties précédentes de la console.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-223">Clears all previous console output.</span></span>

<span data-ttu-id="ecb8f-224">Si votre code génère un grand nombre de messages de console, vous pouvez les organiser visuellement en blocs imbriqués à l’aide des commandes suivantes:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-224">If your code outputs a lot of console messages, you can visually organize them into nested blocks with the following commands:</span></span>

 <span data-ttu-id="ecb8f-225">Commande</span><span class="sxs-lookup"><span data-stu-id="ecb8f-225">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="ecb8f-226">groupe ()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-226">group()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/group) | <span data-ttu-id="ecb8f-227">Commence un nouveau niveau d’imbrication pour la sortie de console avec l’étiquette spécifiée (optional).</span><span class="sxs-lookup"><span data-stu-id="ecb8f-227">Starts a new level of nesting for console output with the specified (optional) label.</span></span>
[**<span data-ttu-id="ecb8f-228">groupCollapsed()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-228">groupCollapsed()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/groupCollapsed) | <span data-ttu-id="ecb8f-229">Commence un nouveau niveau d’imbrication pour la sortie de console avec l’étiquette spécifiée (optional), mais le contrôle de regroupement est réduit par défaut et doit être développé (en cliquant sur le contrôle Arrow) pour afficher la sortie enfant.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-229">Starts a new level of nesting for console output with the specified (optional) label, however the grouping control is collapsed by default and must be expanded (by clicking on the arrow control) to display the child output.</span></span>
[**<span data-ttu-id="ecb8f-230">groupEnd()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-230">groupEnd()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/groupEnd) | <span data-ttu-id="ecb8f-231">Termine le groupe imbriqué pour l’étiquette spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-231">Ends the nesting group for the specified label.</span></span>

<span data-ttu-id="ecb8f-232">Par exemple, essayez d’entrer les commandes suivantes dans la console:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-232">For example, try entering the following commands in the console:</span></span>

```javascript
console.groupCollapsed('Group 1');
console.log('In Group 1');
console.groupCollapsed('Group 1.1');
console.log('In Group 1.1');
console.groupEnd('Group 1.1');
console.groupEnd('Group 1');
console.log('No longer in a group');
```

<span data-ttu-id="ecb8f-233">.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-233">.</span></span> <span data-ttu-id="ecb8f-234">.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-234">.</span></span> <span data-ttu-id="ecb8f-235">.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-235">.</span></span> <span data-ttu-id="ecb8f-236">Développez ensuite les contrôles de groupe *1* et *1,1* pour voir comment les commentaires du journal sont imbriqués:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-236">and then expand the *Group 1* and *Group 1.1* controls to see how the log comments are nested:</span></span>

![Regroupement de messages dans la console](../media/console_api_group.png)

<span data-ttu-id="ecb8f-238">Il est parfois plus facile de visualiser un objet ou un tableau JavaScript sous forme tabulaire qu’une liste plate.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-238">Sometimes its easier to visualize a JavaScript object or array in tabular form, rather than a flat list.</span></span> <span data-ttu-id="ecb8f-239">Pour cela, vous pouvez utiliser la commande *console. table ()* :</span><span class="sxs-lookup"><span data-stu-id="ecb8f-239">For that, you can use the *console.table()* command:</span></span>

<span data-ttu-id="ecb8f-240">Commande</span><span class="sxs-lookup"><span data-stu-id="ecb8f-240">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="ecb8f-241">table ()</span><span class="sxs-lookup"><span data-stu-id="ecb8f-241">table()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/table) | <span data-ttu-id="ecb8f-242">Génère le tableau ou l’objet fourni dans la console sous forme tabulaire.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-242">Outputs the supplied array or object to the console in tabular form.</span></span>

<span data-ttu-id="ecb8f-243">Par exemple, le tableau d’objets suivant:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-243">For example, the following object array:</span></span>

```javascript
var orders = [{'Size':'XL', 'Quantity':1},{'Size':'M', 'Quantity':3}, {'Size':'L', 'Quantity':2}];
console.table(orders);
```

<span data-ttu-id="ecb8f-244">.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-244">.</span></span> <span data-ttu-id="ecb8f-245">.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-245">.</span></span> <span data-ttu-id="ecb8f-246">.</span><span class="sxs-lookup"><span data-stu-id="ecb8f-246">.</span></span> <span data-ttu-id="ecb8f-247">sera restitué en tant que table dans la console:</span><span class="sxs-lookup"><span data-stu-id="ecb8f-247">will render as this table in the console:</span></span>

![Afficher un tableau d’objets en tant que table dans la console](../media/console_api_table.png)
