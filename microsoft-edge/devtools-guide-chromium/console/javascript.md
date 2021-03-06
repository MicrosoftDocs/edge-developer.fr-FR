---
description: Découvrez comment exécuter JavaScript dans la console.
title: Commencer à utiliser JavaScript dans la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: c1d6c393b6278f4622cf80576ccc8f9c70bdb6b5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398818"
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

# <a name="get-started-with-running-javascript-in-the-console"></a><span data-ttu-id="eff31-104">Commencer à utiliser JavaScript dans la console</span><span class="sxs-lookup"><span data-stu-id="eff31-104">Get started with running JavaScript in the Console</span></span>  

<span data-ttu-id="eff31-105">Ce didacticiel interactif vous montre comment exécuter JavaScript dans la **console**Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="eff31-105">This interactive tutorial shows you how to run JavaScript in the Microsoft Edge DevTools **Console**.</span></span>  <span data-ttu-id="eff31-106">Pour plus d’informations sur la journalisation des messages dans la **console,** accédez à [Démarrer avec la journalisation des messages.][DevToolsConsoleLoggingMessages]</span><span class="sxs-lookup"><span data-stu-id="eff31-106">For more information about how to log messages to the **Console**, navigate to [Get Started With Logging Messages][DevToolsConsoleLoggingMessages].</span></span>  <span data-ttu-id="eff31-107">Pour plus d’informations sur la façon de suspendre du code JavaScript et de le parcourir une ligne à la fois, accédez à Commencer avec [le débogage javaScript][DevToolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="eff31-107">For more information about how to pause JavaScript code and step through it one line at a time, navigate to [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="The Console" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   <span data-ttu-id="eff31-109">Console \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="eff31-109">The **Console**</span></span>  
:::image-end:::  

## <a name="overview"></a><span data-ttu-id="eff31-110">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="eff31-110">Overview</span></span>  

<span data-ttu-id="eff31-111">La **console** est [un rePL,][WikiReadEvalPrintLoop]qui signifie Read, Evaluate, Print et Loop.</span><span class="sxs-lookup"><span data-stu-id="eff31-111">The **Console** is a [REPL][WikiReadEvalPrintLoop], which stands for Read, Evaluate, Print, and Loop.</span></span>  <span data-ttu-id="eff31-112">Il lit le code JavaScript que vous tapez dans celui-ci, évalue votre code, imprime le résultat de votre [expression,][2alityExpressionsVersusStatements]puis revient à la première étape.</span><span class="sxs-lookup"><span data-stu-id="eff31-112">It reads the JavaScript that you type into it, evaluates your code, prints out the result of your [expression][2alityExpressionsVersusStatements], and then loops back to the first step.</span></span>  

## <a name="set-up-devtools"></a><span data-ttu-id="eff31-113">Configurer DevTools</span><span class="sxs-lookup"><span data-stu-id="eff31-113">Set up DevTools</span></span>  

<span data-ttu-id="eff31-114">Ce didacticiel est conçu pour ouvrir la démonstration et essayer tous les flux de travail vous-même.</span><span class="sxs-lookup"><span data-stu-id="eff31-114">This tutorial is designed for you to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="eff31-115">Lorsque vous suivez physiquement le processus, vous êtes plus susceptible de mémoriser les flux de travail ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="eff31-115">When you physically follow along, you are more likely to remember the workflows later.</span></span>

1.  <span data-ttu-id="eff31-116">Sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\) pour ouvrir la **console.**</span><span class="sxs-lookup"><span data-stu-id="eff31-116">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open the **Console**.</span></span>  
1.  <span data-ttu-id="eff31-117">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Javascript Example** to open in a new window.</span><span class="sxs-lookup"><span data-stu-id="eff31-117">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Javascript Example** to open in a new window.</span></span>  
    
    *   [<span data-ttu-id="eff31-118">Exemple JavaScript pour la console</span><span class="sxs-lookup"><span data-stu-id="eff31-118">Console Javascript Example</span></span>][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="Page Exemple JavaScript pour la console à gauche et DevTools à droite" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       <span data-ttu-id="eff31-120">Page Exemple JavaScript pour la console à gauche et DevTools à droite</span><span class="sxs-lookup"><span data-stu-id="eff31-120">The Console JavaScript Example page on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
## <a name="view-and-change-the-javascript-or-dom-of-the-page"></a><span data-ttu-id="eff31-121">Afficher et modifier le JavaScript ou le DOM de la page</span><span class="sxs-lookup"><span data-stu-id="eff31-121">View and change the JavaScript or DOM of the page</span></span>  

<span data-ttu-id="eff31-122">Lors de la création ou du débogage d’une page, il est souvent utile d’exécuter des instructions dans la **console** afin de modifier l’apparence ou l’apparence de la page.</span><span class="sxs-lookup"><span data-stu-id="eff31-122">When building or debugging a page, it is often useful to run statements in the **Console** in order to change how the page looks or runs.</span></span>  
    
1.  <span data-ttu-id="eff31-123">Notez le texte dans le bouton.</span><span class="sxs-lookup"><span data-stu-id="eff31-123">Notice the text in the button.</span></span>  
1.  <span data-ttu-id="eff31-124">Tapez `document.getElementById('hello').textContent = 'Hello, Console!'` dans la **console,** puis sélectionnez `Enter` pour évaluer l’expression.</span><span class="sxs-lookup"><span data-stu-id="eff31-124">Type `document.getElementById('hello').textContent = 'Hello, Console!'` in the **Console** and then select `Enter` to evaluate the expression.</span></span>  <span data-ttu-id="eff31-125">Notez que le texte à l’intérieur du bouton change.</span><span class="sxs-lookup"><span data-stu-id="eff31-125">Notice how the text inside the button changes.</span></span>  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Apparence de la console après l’évaluation de l’expression" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       <span data-ttu-id="eff31-127">Apparence de la **console** après l’évaluation de l’expression</span><span class="sxs-lookup"><span data-stu-id="eff31-127">How the **Console** looks after evaluating the expression</span></span>  
    :::image-end:::  
    
    `"Hello, Console!"`<span data-ttu-id="eff31-128">, s’affiche sous le code que vous avez évalué.</span><span class="sxs-lookup"><span data-stu-id="eff31-128">, is displayed below the code that you evaluated.</span></span>  <span data-ttu-id="eff31-129">N’oubliez pas les 4 étapes de REPL : lire, évaluer, imprimer, boucle.</span><span class="sxs-lookup"><span data-stu-id="eff31-129">Remember the 4 steps of REPL: read, evaluate, print, loop.</span></span>  <span data-ttu-id="eff31-130">Après avoir évalué votre code, un rePL imprime le résultat de l’expression.</span><span class="sxs-lookup"><span data-stu-id="eff31-130">After evaluating your code, a REPL prints the result of the expression.</span></span>  <span data-ttu-id="eff31-131">Vous `"Hello, Console!"` devez donc être le résultat de l’évaluation. `document.getElementById('hello').textContent = 'Hello, Console!'`</span><span class="sxs-lookup"><span data-stu-id="eff31-131">So `"Hello, Console!"` must be the result of evaluating `document.getElementById('hello').textContent = 'Hello, Console!'`.</span></span>  
    
## <a name="run-arbitrary-javascript-that-is-not-related-to-the-page"></a><span data-ttu-id="eff31-132">Exécuter un javaScript arbitraire qui n’est pas lié à la page</span><span class="sxs-lookup"><span data-stu-id="eff31-132">Run arbitrary JavaScript that is not related to the page</span></span>  

<span data-ttu-id="eff31-133">Parfois, vous souhaitez simplement un aire de jeu de code où vous pouvez tester du code ou tester de nouvelles fonctionnalités JavaScript que vous ne connaissez pas.</span><span class="sxs-lookup"><span data-stu-id="eff31-133">Sometimes, you just want a code playground where you are able to test some code, or try out new JavaScript features you are not familiar with.</span></span>  <span data-ttu-id="eff31-134">La **console** est un endroit idéal pour ces types d’expériences.</span><span class="sxs-lookup"><span data-stu-id="eff31-134">The **Console** is a perfect place for these kinds of experiments.</span></span>  

1.  <span data-ttu-id="eff31-135">Tapez `5 + 15` dans la console et sélectionnez pour évaluer `Enter` l’expression.</span><span class="sxs-lookup"><span data-stu-id="eff31-135">Type `5 + 15` in the Console and select `Enter` to evaluate the expression.</span></span> <span data-ttu-id="eff31-136">La console imprime le résultat de l’expression sous votre code.</span><span class="sxs-lookup"><span data-stu-id="eff31-136">The Console prints out the result of the expression below your code.</span></span>  <span data-ttu-id="eff31-137">Dans la figure suivante, votre **console** doit afficher le résultat après avoir évalué l’expression.</span><span class="sxs-lookup"><span data-stu-id="eff31-137">In the following figure, your **Console** should display the result after evaluating the expression.</span></span>  

1.  <span data-ttu-id="eff31-138">Tapez le code suivant dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="eff31-138">Type the following code into the **Console**.</span></span>  <span data-ttu-id="eff31-139">Essayez de la taper, caractère par caractère, plutôt que de la copier-coller.</span><span class="sxs-lookup"><span data-stu-id="eff31-139">Try typing it out, character-by-character, rather than copy-pasting it.</span></span>  
    
    ```javascript
    function add(a, b=20)
    ```  
    
    <span data-ttu-id="eff31-140">Si vous ne connaissez pas la `b=20` syntaxe, accédez à la définition des [valeurs par défaut des arguments de fonction.][Esma6DefaultParameterValues]</span><span class="sxs-lookup"><span data-stu-id="eff31-140">If you are unfamiliar with the `b=20` syntax, navigate to [define default values for function arguments][Esma6DefaultParameterValues].</span></span>  
    
1.  <span data-ttu-id="eff31-141">À présent, exécutez la fonction que vous venons de définir.</span><span class="sxs-lookup"><span data-stu-id="eff31-141">Now, run the function that you just defined.</span></span>  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="La console s’affiche après l’évaluation des expressions dans l’extrait de code" lightbox="../media/console-javascript-example-console-playground.msft.png":::
             <span data-ttu-id="eff31-143">La **console s’affiche** après l’évaluation des expressions dans l’extrait de code</span><span class="sxs-lookup"><span data-stu-id="eff31-143">The **Console** displays after evaluating the expressions in the code snippet</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` <span data-ttu-id="eff31-144">est évaluée `45` à, car lorsque la `add` fonction est appelée sans second argument, est par défaut `b` . `20`</span><span class="sxs-lookup"><span data-stu-id="eff31-144">evaluates to `45` because when the `add` function is called without a second argument, `b` defaults to `20`.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="eff31-145">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="eff31-145">Next steps</span></span>  

<!--To explore more features related to running JavaScript in the **Console**, navigate to [Run JavaScript][DevToolsConsoleReference].  -->  

<!--todo: add console reference (run javascript) section when available  -->  

<span data-ttu-id="eff31-146">DevTools vous permet de suspendre un script en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="eff31-146">DevTools lets you pause a script in the middle of running.</span></span>  <span data-ttu-id="eff31-147">Pendant que vous êtes suspendu, vous pouvez utiliser la **console** pour afficher et modifier le ou la page à `window` ce `DOM` moment-là.</span><span class="sxs-lookup"><span data-stu-id="eff31-147">While you are paused, you may use the **Console** to view and change the `window` or `DOM` of the page at that moment in time.</span></span>  <span data-ttu-id="eff31-148">Le flux de travail constitue un flux de travail de débogage puissant.</span><span class="sxs-lookup"><span data-stu-id="eff31-148">The workflow makes for a powerful debugging workflow.</span></span>  <span data-ttu-id="eff31-149">Pour un didacticiel interactif, [accédez à Commencer avec le débogage de JavaScript][DevToolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="eff31-149">For an interactive tutorial, navigate to [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

<span data-ttu-id="eff31-150">La **console** dispose également d’un ensemble de fonctions pratiques qui facilitent l’interaction avec une page.</span><span class="sxs-lookup"><span data-stu-id="eff31-150">The **Console** also has a set of convenience functions that make it easier to interact with a page.</span></span>  <span data-ttu-id="eff31-151">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="eff31-151">For example:</span></span>  

*   <span data-ttu-id="eff31-152">Au lieu de taper `document.querySelector()` pour sélectionner un élément, tapez `$()` .</span><span class="sxs-lookup"><span data-stu-id="eff31-152">Rather than typing `document.querySelector()` to select an element, type `$()`.</span></span>  <span data-ttu-id="eff31-153">Cette syntaxe s’inspire de jQuery, mais elle n’est pas réellement jQuery.</span><span class="sxs-lookup"><span data-stu-id="eff31-153">This syntax is inspired by jQuery, but it is not actually jQuery.</span></span>  <span data-ttu-id="eff31-154">Il s’agit simplement d’un alias pour `document.querySelector()` .</span><span class="sxs-lookup"><span data-stu-id="eff31-154">It is just an alias for `document.querySelector()`.</span></span>  
*   `debug(function)` <span data-ttu-id="eff31-155">définit effectivement un point d’arrêt sur la première ligne de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="eff31-155">effectively sets a breakpoint on the first line of that function.</span></span>  
*   `keys(object)` <span data-ttu-id="eff31-156">renvoie un tableau contenant les clés de l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="eff31-156">returns an array containing the keys of the specified object.</span></span>  

<span data-ttu-id="eff31-157">Pour plus d’informations sur les fonctions pratiques, accédez à référence de [l’API des utilitaires de console.][DevToolsConsoleUtilities]</span><span class="sxs-lookup"><span data-stu-id="eff31-157">For more information about the convenience functions, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="eff31-158">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="eff31-158">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Commencer à journalisation des messages dans la console | Documents Microsoft"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Référence de la console | Documents Microsoft"  
[DevToolsConsoleUtilities]: ./utilities.md "Référence de l’API des utilitaires de console | Documents Microsoft"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Commencer à déboguer JavaScript dans Microsoft Edge DevTools | Documents Microsoft"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Expressions et instructions en JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Valeurs des paramètres par défaut - Gestion étendue des paramètres - ECMAScript 6 — Nouvelles fonctionnalités : vue d’ensemble & comparaison"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Exemple de console Javascript | Glitch"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Read-eval-print loop - Wikipedia"  

> [!NOTE]
> <span data-ttu-id="eff31-167">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="eff31-167">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="eff31-168">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/javascript) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="eff31-168">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/javascript) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="eff31-170">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="eff31-170">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
