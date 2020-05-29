---
title: Commencer à utiliser JavaScript sur la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 724d0e3c7c8439551538383e68a5fc4465eade94
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601725"
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







# <span data-ttu-id="52288-103">Commencer à utiliser JavaScript sur la console</span><span class="sxs-lookup"><span data-stu-id="52288-103">Get Started With Running JavaScript In The Console</span></span>   



<span data-ttu-id="52288-104">Ce didacticiel interactif vous montre comment exécuter JavaScript dans la console Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="52288-104">This interactive tutorial shows you how to run JavaScript in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="52288-105">Pour plus d’informations sur la façon de consigner les messages dans la console, voir [utiliser la journalisation][DevToolsConsoleLoggingMessages] .</span><span class="sxs-lookup"><span data-stu-id="52288-105">See [Get Started With Logging Messages][DevToolsConsoleLoggingMessages] to learn how to log messages to the Console.</span></span>  <span data-ttu-id="52288-106">Pour plus d’informations sur la façon de suspendre le code JavaScript et de parcourir le code JavaScript à la fois, voir [prendre en main le débogage][DevToolsJavascriptIndex] .</span><span class="sxs-lookup"><span data-stu-id="52288-106">See [Get Started With Debugging JavaScript][DevToolsJavascriptIndex] to learn how to pause JavaScript code and step through it one line at a time.</span></span>  

> ##### <span data-ttu-id="52288-107">Figure1</span><span class="sxs-lookup"><span data-stu-id="52288-107">Figure 1</span></span>  
> <span data-ttu-id="52288-108">La **console**</span><span class="sxs-lookup"><span data-stu-id="52288-108">The **Console**</span></span>  
> ![La console][ImageConsole]  

## <span data-ttu-id="52288-110">Présentation</span><span class="sxs-lookup"><span data-stu-id="52288-110">Overview</span></span>   

<span data-ttu-id="52288-111">La **console** est une valeur [REPL][WikiReadEvalPrintLoop]qui correspond à la lecture, à l’évaluation, à l’impression et au bouclage.</span><span class="sxs-lookup"><span data-stu-id="52288-111">The **Console** is a [REPL][WikiReadEvalPrintLoop], which stands for Read, Evaluate, Print, and Loop.</span></span>  <span data-ttu-id="52288-112">Elle lit le code JavaScript que vous entrez, évalue votre code, imprime le résultat de l' [expression][2alityExpressionsVersusStatements], puis revient à la première étape.</span><span class="sxs-lookup"><span data-stu-id="52288-112">It reads the JavaScript that you type into it, evaluates your code, prints out the result of your [expression][2alityExpressionsVersusStatements], and then loops back to the first step.</span></span>  

## <span data-ttu-id="52288-113">Configurer DevTools</span><span class="sxs-lookup"><span data-stu-id="52288-113">Set up DevTools</span></span>   

<span data-ttu-id="52288-114">Ce didacticiel est conçu pour vous permettre d’ouvrir la démonstration et d’essayer les flux de travail vous-même.</span><span class="sxs-lookup"><span data-stu-id="52288-114">This tutorial is designed for you to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="52288-115">Lorsque vous effectuez une suivi physique, il est plus probable de mémoriser les flux de travail.</span><span class="sxs-lookup"><span data-stu-id="52288-115">When you physically follow along, you are more likely to remember the workflows later.</span></span>

1.  <span data-ttu-id="52288-116">Appuyez sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) pour ouvrir la **console**.</span><span class="sxs-lookup"><span data-stu-id="52288-116">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console**.</span></span>  
1.  <span data-ttu-id="52288-117">Maintenez `Control` la touche \ (Windows \) ou `Command` \ (MacOS \), puis cliquez sur l' **exemple de console JavaScript** pour l’ouvrir dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="52288-117">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **Console Javascript Example** to open in a new window.</span></span>  
    
    [<span data-ttu-id="52288-118">Exemple de console JavaScript</span><span class="sxs-lookup"><span data-stu-id="52288-118">Console Javascript Example</span></span>][GlitchConsoleJavascriptExample]  
    
    > ##### <span data-ttu-id="52288-119">Figure 2</span><span class="sxs-lookup"><span data-stu-id="52288-119">Figure 2</span></span>  
    > <span data-ttu-id="52288-120">Page d’exemple de langage JavaScript de la console à gauche et DevTools sur la droite</span><span class="sxs-lookup"><span data-stu-id="52288-120">The Console JavaScript Example page on the left, and DevTools on the right</span></span>  
    > ![Page d’exemple de langage JavaScript de la console à gauche et DevTools sur la droite][ImageTutorialDevToolsJs]  

## <span data-ttu-id="52288-122">Afficher et modifier le code JavaScript ou DOM de la page</span><span class="sxs-lookup"><span data-stu-id="52288-122">View and change the JavaScript or DOM of the page</span></span>   

<span data-ttu-id="52288-123">Lorsque vous créez ou déboguez une page, il est souvent utile d’exécuter des instructions dans la **console** afin de modifier l’apparence ou l’exécution de la page.</span><span class="sxs-lookup"><span data-stu-id="52288-123">When building or debugging a page, it is often useful to run statements in the **Console** in order to change how the page looks or runs.</span></span>  
    
1.  <span data-ttu-id="52288-124">Notez le texte du bouton.</span><span class="sxs-lookup"><span data-stu-id="52288-124">Notice the text in the button.</span></span>  
1.  <span data-ttu-id="52288-125">Entrez `document.getElementById('hello').textContent = 'Hello, Console!'` dans la **console** , puis appuyez `Enter` sur pour évaluer l’expression.</span><span class="sxs-lookup"><span data-stu-id="52288-125">Type `document.getElementById('hello').textContent = 'Hello, Console!'` in the **Console** and then press `Enter` to evaluate the expression.</span></span>  <span data-ttu-id="52288-126">Notez la façon dont le texte à l’intérieur du bouton change.</span><span class="sxs-lookup"><span data-stu-id="52288-126">Notice how the text inside the button changes.</span></span>  
    
    > ##### <span data-ttu-id="52288-127">Figure3</span><span class="sxs-lookup"><span data-stu-id="52288-127">Figure 3</span></span>  
    > <span data-ttu-id="52288-128">Aspect de la console après l’évaluation de l’expression</span><span class="sxs-lookup"><span data-stu-id="52288-128">How the Console looks after evaluating the expression</span></span>  
    > ![Aspect de la console après l’évaluation de l’expression][ImageConsoleAfterEvaluating]  
    
    <span data-ttu-id="52288-130">Le code que vous avez évalué est affiché sous `"Hello, Console!"` .</span><span class="sxs-lookup"><span data-stu-id="52288-130">Below the code that you evaluated you see `"Hello, Console!"`.</span></span>  <span data-ttu-id="52288-131">Rappelez-vous des 4 étapes de REPL: lecture, évaluation, impression, boucle.</span><span class="sxs-lookup"><span data-stu-id="52288-131">Recall the 4 steps of REPL: read, evaluate, print, loop.</span></span>  <span data-ttu-id="52288-132">Après avoir évalué votre code, une valeur REPL imprime le résultat de l’expression.</span><span class="sxs-lookup"><span data-stu-id="52288-132">After evaluating your code, a REPL prints the result of the expression.</span></span>  <span data-ttu-id="52288-133">`"Hello, Console!"`Le résultat doit donc être évalué `document.getElementById('hello').textContent = 'Hello, Console!'` .</span><span class="sxs-lookup"><span data-stu-id="52288-133">So `"Hello, Console!"` must be the result of evaluating `document.getElementById('hello').textContent = 'Hello, Console!'`.</span></span>  
    
## <span data-ttu-id="52288-134">Exécuter du JavaScript arbitraire qui n’est pas lié à la page</span><span class="sxs-lookup"><span data-stu-id="52288-134">Run arbitrary JavaScript that is not related to the page</span></span>   

<span data-ttu-id="52288-135">Il arrive parfois que vous souhaitiez créer un code de laboratoire dans lequel vous pouvez tester du code ou essayer de nouvelles fonctionnalités JavaScript que vous ne connaissez pas.</span><span class="sxs-lookup"><span data-stu-id="52288-135">Sometimes, you just want a code playground where you are able to test some code, or try out new JavaScript features you are not familiar with.</span></span>  <span data-ttu-id="52288-136">La console est l’endroit idéal pour ces types d’expériences.</span><span class="sxs-lookup"><span data-stu-id="52288-136">The Console is a perfect place for these kinds of experiments.</span></span>  

1.  <span data-ttu-id="52288-137">Entrez `5 + 15` dans la console et appuyez sur `Enter` pour évaluer l’expression.</span><span class="sxs-lookup"><span data-stu-id="52288-137">Type `5 + 15` in the Console and press `Enter` to evaluate the expression.</span></span> <span data-ttu-id="52288-138">La console imprime le résultat de l’expression sous votre code.</span><span class="sxs-lookup"><span data-stu-id="52288-138">The Console prints out the result of the expression below your code.</span></span>  <span data-ttu-id="52288-139">La **figure 4** ci-dessous montre à quoi votre console doit ressortir après avoir évalué cette expression.</span><span class="sxs-lookup"><span data-stu-id="52288-139">**Figure 4** below shows how your Console should look after evaluating this expression.</span></span>  

1.  <span data-ttu-id="52288-140">Tapez le code suivant dans la **console**.</span><span class="sxs-lookup"><span data-stu-id="52288-140">Type the following code into the **Console**.</span></span>  <span data-ttu-id="52288-141">Essayez de taper le texte, caractère par caractère, plutôt que de copier-coller.</span><span class="sxs-lookup"><span data-stu-id="52288-141">Try typing it out, character-by-character, rather than copy-pasting it.</span></span>  
    
    ```javascript
    function add(a, b=20) {
        return a + b;
    }
    ```  
    
    <span data-ttu-id="52288-142">Pour plus d’inconnaissances de la syntaxe, voir [définir les valeurs par défaut des arguments de fonction][Esma6DefaultParameterValues] `b=20` .</span><span class="sxs-lookup"><span data-stu-id="52288-142">See [define default values for function arguments][Esma6DefaultParameterValues] if you are unfamiliar with the `b=20` syntax.</span></span>  
    
1.  <span data-ttu-id="52288-143">À présent, appelez la fonction que vous venez de définir.</span><span class="sxs-lookup"><span data-stu-id="52288-143">Now, call the function that you just defined.</span></span>  
    
    ```javascript
    add(25);
    ```  
    
    > ##### <span data-ttu-id="52288-144">Figure 4</span><span class="sxs-lookup"><span data-stu-id="52288-144">Figure 4</span></span>  
    > <span data-ttu-id="52288-145">Aspect de la console après avoir évalué les expressions ci-dessus</span><span class="sxs-lookup"><span data-stu-id="52288-145">How the Console looks after evaluating the expressions above</span></span>  
    > ![Aspect de la console après avoir évalué les expressions ci-dessus][ImagePlayground]  
    
    `add(25)` <span data-ttu-id="52288-147">prend la valeur, `45` car lorsque la `add` fonction est appelée sans deuxième argument, la `b` valeur par défaut est `20` .</span><span class="sxs-lookup"><span data-stu-id="52288-147">evaluates to `45` because when the `add` function is called without a second argument, `b` defaults to `20`.</span></span>  

## <span data-ttu-id="52288-148">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="52288-148">Next steps</span></span>   

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

<span data-ttu-id="52288-149">DevTools vous permet de suspendre un script au milieu de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="52288-149">DevTools lets you pause a script in the middle of running.</span></span>  <span data-ttu-id="52288-150">Lorsque vous êtes en pause, vous pouvez utiliser la **console** pour afficher et modifier le `window` ou la `DOM` page à ce moment précis.</span><span class="sxs-lookup"><span data-stu-id="52288-150">While you are paused, you may use the **Console** to view and change the `window` or `DOM` of the page at that moment in time.</span></span>  <span data-ttu-id="52288-151">Cela permet de disposer d’un flux de travail puissant de débogage.</span><span class="sxs-lookup"><span data-stu-id="52288-151">This makes for a powerful debugging workflow.</span></span>  <span data-ttu-id="52288-152">Voir [commencer à déboguer JavaScript][DevToolsJavascriptIndex] pour un didacticiel interactif.</span><span class="sxs-lookup"><span data-stu-id="52288-152">See [Get Started With Debugging JavaScript][DevToolsJavascriptIndex] for an interactive tutorial.</span></span>  

<span data-ttu-id="52288-153">La **console** dispose également d’un ensemble de fonctions pratiques qui facilitent l’interaction avec une page.</span><span class="sxs-lookup"><span data-stu-id="52288-153">The **Console** also has a set of convenience functions that make it easier to interact with a page.</span></span>  <span data-ttu-id="52288-154">Exemple:</span><span class="sxs-lookup"><span data-stu-id="52288-154">For example:</span></span>  

*   <span data-ttu-id="52288-155">Au lieu de taper `document.querySelector()` pour sélectionner un élément, tapez `$()` .</span><span class="sxs-lookup"><span data-stu-id="52288-155">Rather than typing `document.querySelector()` to select an element, type `$()`.</span></span>  <span data-ttu-id="52288-156">Cette syntaxe est inspirée par jQuery, mais elle n’est pas réellement jQuery.</span><span class="sxs-lookup"><span data-stu-id="52288-156">This syntax is inspired by jQuery, but it is not actually jQuery.</span></span>  <span data-ttu-id="52288-157">Il s’agit simplement d’un alias pour `document.querySelector()` .</span><span class="sxs-lookup"><span data-stu-id="52288-157">It is just an alias for `document.querySelector()`.</span></span>  
*   `debug(function)` <span data-ttu-id="52288-158">définit efficacement un point d’arrêt sur la première ligne de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="52288-158">effectively sets a breakpoint on the first line of that function.</span></span>  
*   `keys(object)` <span data-ttu-id="52288-159">retourne une matrice contenant les clés de l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="52288-159">returns an array containing the keys of the specified object.</span></span>  

<!--See [Console Utilities API Reference][DevToolsConsoleUtilities] to explore all the convenience functions.  -->  

<!--todo: add console utilities api reference section when available  -->  

 



<!-- image links -->  

[ImageConsole]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-playground.msft.png "Figure 1: console"  
[ImageTutorialDevToolsJs]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-empty.msft.png "Figure 2: page d’exemple de code JavaScript de la console à gauche et DevTools sur la droite"  
[ImageConsoleAfterEvaluating]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-change-button-text.msft.png "Figure 3: apparence de la console après l’évaluation de l’expression"  
[ImagePlayground]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-playground.msft.png "Figure 4: apparence de la console après avoir évalué les expressions ci-dessus"  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: /microsoft-edge/devtools-guide-chromium/console/log "Commencer à utiliser la journalisation des messages dans la console"  
[DevToolsConsoleReference]: /microsoft-edge/devtools-guide-chromium/console/reference#run-javascript "Référence de la console"  
[DevToolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium//console/utilities "XXXXXX xxxxxxx xxx xxxxxxxxx"  

[DevToolsJavascriptIndex]: /microsoft-edge/devtools-guide-chromium/javascript/index "Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Expressions et instructions dans JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Valeurs de paramètre par défaut-gestion étendue des paramètres-ECMAScript 6: nouvelles fonctionnalités: vue d’ensemble & comparaison"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Exemple de console JavaScript | Problème"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Lecture-eval-imprimer en boucle-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="52288-172">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="52288-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="52288-173">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/javascript) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="52288-173">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/javascript) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="52288-175">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="52288-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
