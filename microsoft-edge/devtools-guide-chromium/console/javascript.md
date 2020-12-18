---
description: Apprenez à exécuter JavaScript dans la console.
title: Commencer à utiliser JavaScript sur la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: ecd1a2fffb311990b6e743e99d038f1f2a519ee4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231089"
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

# <span data-ttu-id="48275-104">Commencer à utiliser JavaScript sur la console</span><span class="sxs-lookup"><span data-stu-id="48275-104">Get Started With Running JavaScript In The Console</span></span>  

<span data-ttu-id="48275-105">Ce didacticiel interactif vous montre comment exécuter JavaScript dans la **console**Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="48275-105">This interactive tutorial shows you how to run JavaScript in the Microsoft Edge DevTools **Console**.</span></span>  <span data-ttu-id="48275-106">Pour plus d’informations sur la façon de consigner les messages dans la **console**, accédez à la section [commencer à utiliser la journalisation des messages][DevToolsConsoleLoggingMessages].</span><span class="sxs-lookup"><span data-stu-id="48275-106">For more information about how to log messages to the **Console**, navigate to [Get Started With Logging Messages][DevToolsConsoleLoggingMessages].</span></span>  <span data-ttu-id="48275-107">Pour plus d’informations sur la façon de suspendre le code JavaScript et de parcourir ce code une ligne à la fois, accédez à la rubrique mise [en route du JavaScript][DevToolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="48275-107">For more information about how to pause JavaScript code and step through it one line at a time, navigate to [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="La console" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   <span data-ttu-id="48275-109">La **console**</span><span class="sxs-lookup"><span data-stu-id="48275-109">The **Console**</span></span>  
:::image-end:::  

## <span data-ttu-id="48275-110">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="48275-110">Overview</span></span>  

<span data-ttu-id="48275-111">La **console** est une valeur [REPL][WikiReadEvalPrintLoop]qui correspond à la lecture, à l’évaluation, à l’impression et au bouclage.</span><span class="sxs-lookup"><span data-stu-id="48275-111">The **Console** is a [REPL][WikiReadEvalPrintLoop], which stands for Read, Evaluate, Print, and Loop.</span></span>  <span data-ttu-id="48275-112">Elle lit le code JavaScript que vous entrez, évalue votre code, imprime le résultat de l' [expression][2alityExpressionsVersusStatements], puis revient à la première étape.</span><span class="sxs-lookup"><span data-stu-id="48275-112">It reads the JavaScript that you type into it, evaluates your code, prints out the result of your [expression][2alityExpressionsVersusStatements], and then loops back to the first step.</span></span>  

## <span data-ttu-id="48275-113">Configurer DevTools</span><span class="sxs-lookup"><span data-stu-id="48275-113">Set up DevTools</span></span>  

<span data-ttu-id="48275-114">Ce didacticiel est conçu pour vous permettre d’ouvrir la démonstration et d’essayer les flux de travail vous-même.</span><span class="sxs-lookup"><span data-stu-id="48275-114">This tutorial is designed for you to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="48275-115">Lorsque vous effectuez une suivi physique, il est plus probable de mémoriser les flux de travail.</span><span class="sxs-lookup"><span data-stu-id="48275-115">When you physically follow along, you are more likely to remember the workflows later.</span></span>

1.  <span data-ttu-id="48275-116">Sélectionnez `Control` + `Shift` + `J` \ (Windows, Linux \) ou `Command` + `Option` + `J` \ (MacOS \) pour ouvrir la **console**.</span><span class="sxs-lookup"><span data-stu-id="48275-116">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open the **Console**.</span></span>  
1.  <span data-ttu-id="48275-117">Maintenez la touche Windows enfoncée `Control` `Command` et sélectionnez l' **exemple de console JavaScript** à ouvrir dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="48275-117">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Javascript Example** to open in a new window.</span></span>  
    
    *   [<span data-ttu-id="48275-118">Exemple de console JavaScript</span><span class="sxs-lookup"><span data-stu-id="48275-118">Console Javascript Example</span></span>][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="Page d’exemple de langage JavaScript de la console à gauche et DevTools sur la droite" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       <span data-ttu-id="48275-120">Page d’exemple de langage JavaScript de la console à gauche et DevTools sur la droite</span><span class="sxs-lookup"><span data-stu-id="48275-120">The Console JavaScript Example page on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="48275-121">Afficher et modifier le code JavaScript ou DOM de la page</span><span class="sxs-lookup"><span data-stu-id="48275-121">View and change the JavaScript or DOM of the page</span></span>  

<span data-ttu-id="48275-122">Lorsque vous créez ou déboguez une page, il est souvent utile d’exécuter des instructions dans la **console** afin de modifier l’apparence ou l’exécution de la page.</span><span class="sxs-lookup"><span data-stu-id="48275-122">When building or debugging a page, it is often useful to run statements in the **Console** in order to change how the page looks or runs.</span></span>  
    
1.  <span data-ttu-id="48275-123">Notez le texte du bouton.</span><span class="sxs-lookup"><span data-stu-id="48275-123">Notice the text in the button.</span></span>  
1.  <span data-ttu-id="48275-124">Entrez `document.getElementById('hello').textContent = 'Hello, Console!'` dans la **console** , puis sélectionnez `Enter` pour évaluer l’expression.</span><span class="sxs-lookup"><span data-stu-id="48275-124">Type `document.getElementById('hello').textContent = 'Hello, Console!'` in the **Console** and then select `Enter` to evaluate the expression.</span></span>  <span data-ttu-id="48275-125">Notez la façon dont le texte à l’intérieur du bouton change.</span><span class="sxs-lookup"><span data-stu-id="48275-125">Notice how the text inside the button changes.</span></span>  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Aspect de la console après l’évaluation de l’expression" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       <span data-ttu-id="48275-127">Aspect de la **console** après l’évaluation de l’expression</span><span class="sxs-lookup"><span data-stu-id="48275-127">How the **Console** looks after evaluating the expression</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="48275-128">Le code que vous avez évalué est affiché sous `"Hello, Console!"` .</span><span class="sxs-lookup"><span data-stu-id="48275-128">Below the code that you evaluated you see `"Hello, Console!"`.</span></span>  <span data-ttu-id="48275-129">Rappelez-vous des 4 étapes de REPL: lecture, évaluation, impression, boucle.</span><span class="sxs-lookup"><span data-stu-id="48275-129">Recall the 4 steps of REPL: read, evaluate, print, loop.</span></span>  <span data-ttu-id="48275-130">Après avoir évalué votre code, une valeur REPL imprime le résultat de l’expression.</span><span class="sxs-lookup"><span data-stu-id="48275-130">After evaluating your code, a REPL prints the result of the expression.</span></span>  <span data-ttu-id="48275-131">`"Hello, Console!"`Le résultat doit donc être évalué `document.getElementById('hello').textContent = 'Hello, Console!'` .</span><span class="sxs-lookup"><span data-stu-id="48275-131">So `"Hello, Console!"` must be the result of evaluating `document.getElementById('hello').textContent = 'Hello, Console!'`.</span></span>  
    
## <span data-ttu-id="48275-132">Exécuter du JavaScript arbitraire qui n’est pas lié à la page</span><span class="sxs-lookup"><span data-stu-id="48275-132">Run arbitrary JavaScript that is not related to the page</span></span>  

<span data-ttu-id="48275-133">Il arrive parfois que vous souhaitiez créer un code de laboratoire dans lequel vous pouvez tester du code ou essayer de nouvelles fonctionnalités JavaScript que vous ne connaissez pas.</span><span class="sxs-lookup"><span data-stu-id="48275-133">Sometimes, you just want a code playground where you are able to test some code, or try out new JavaScript features you are not familiar with.</span></span>  <span data-ttu-id="48275-134">La **console** est l’endroit idéal pour ces types d’expériences.</span><span class="sxs-lookup"><span data-stu-id="48275-134">The **Console** is a perfect place for these kinds of experiments.</span></span>  

1.  <span data-ttu-id="48275-135">Entrez `5 + 15` dans la console, puis sélectionnez `Enter` pour évaluer l’expression.</span><span class="sxs-lookup"><span data-stu-id="48275-135">Type `5 + 15` in the Console and select `Enter` to evaluate the expression.</span></span> <span data-ttu-id="48275-136">La console imprime le résultat de l’expression sous votre code.</span><span class="sxs-lookup"><span data-stu-id="48275-136">The Console prints out the result of the expression below your code.</span></span>  <span data-ttu-id="48275-137">Dans l’illustration suivante, votre **console** doit afficher le résultat après l’évaluation de l’expression.</span><span class="sxs-lookup"><span data-stu-id="48275-137">In the following figure, your **Console** should display the result after evaluating the expression.</span></span>  

1.  <span data-ttu-id="48275-138">Tapez le code suivant dans la **console**.</span><span class="sxs-lookup"><span data-stu-id="48275-138">Type the following code into the **Console**.</span></span>  <span data-ttu-id="48275-139">Essayez de taper le texte, caractère par caractère, plutôt que de copier-coller.</span><span class="sxs-lookup"><span data-stu-id="48275-139">Try typing it out, character-by-character, rather than copy-pasting it.</span></span>  
    
    ```javascript
    function add(a, b=20)
    ```  
    
    <span data-ttu-id="48275-140">Si vous n’êtes pas familiarisé avec la `b=20` syntaxe, accédez à la section [définir les valeurs par défaut des arguments de fonction][Esma6DefaultParameterValues].</span><span class="sxs-lookup"><span data-stu-id="48275-140">If you are unfamiliar with the `b=20` syntax, navigate to [define default values for function arguments][Esma6DefaultParameterValues].</span></span>  
    
1.  <span data-ttu-id="48275-141">À présent, exécutez la fonction que vous venez de définir.</span><span class="sxs-lookup"><span data-stu-id="48275-141">Now, run the function that you just defined.</span></span>  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="La console s’affiche après l’évaluation des expressions dans l’extrait de code" lightbox="../media/console-javascript-example-console-playground.msft.png":::
             <span data-ttu-id="48275-143">La **console** s’affiche après l’évaluation des expressions dans l’extrait de code</span><span class="sxs-lookup"><span data-stu-id="48275-143">The **Console** displays after evaluating the expressions in the code snippet</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` <span data-ttu-id="48275-144">prend la valeur, `45` car lorsque la `add` fonction est appelée sans deuxième argument, la `b` valeur par défaut est `20` .</span><span class="sxs-lookup"><span data-stu-id="48275-144">evaluates to `45` because when the `add` function is called without a second argument, `b` defaults to `20`.</span></span>  

## <span data-ttu-id="48275-145">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="48275-145">Next steps</span></span>  

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

<span data-ttu-id="48275-146">DevTools vous permet de suspendre un script au milieu de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="48275-146">DevTools lets you pause a script in the middle of running.</span></span>  <span data-ttu-id="48275-147">Lorsque vous êtes en pause, vous pouvez utiliser la **console** pour afficher et modifier le `window` ou la `DOM` page à ce moment précis.</span><span class="sxs-lookup"><span data-stu-id="48275-147">While you are paused, you may use the **Console** to view and change the `window` or `DOM` of the page at that moment in time.</span></span>  <span data-ttu-id="48275-148">Le flux de travail effectue un flux de travail puissant de débogage.</span><span class="sxs-lookup"><span data-stu-id="48275-148">The workflow makes for a powerful debugging workflow.</span></span>  <span data-ttu-id="48275-149">Pour un didacticiel interactif, naviguez jusqu’à la section [commencer le débogage de JavaScript][DevToolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="48275-149">For an interactive tutorial, navigate to [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

<span data-ttu-id="48275-150">La **console** dispose également d’un ensemble de fonctions pratiques qui facilitent l’interaction avec une page.</span><span class="sxs-lookup"><span data-stu-id="48275-150">The **Console** also has a set of convenience functions that make it easier to interact with a page.</span></span>  <span data-ttu-id="48275-151">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="48275-151">For example:</span></span>  

*   <span data-ttu-id="48275-152">Au lieu de taper `document.querySelector()` pour sélectionner un élément, tapez `$()` .</span><span class="sxs-lookup"><span data-stu-id="48275-152">Rather than typing `document.querySelector()` to select an element, type `$()`.</span></span>  <span data-ttu-id="48275-153">Cette syntaxe est inspirée par jQuery, mais elle n’est pas réellement jQuery.</span><span class="sxs-lookup"><span data-stu-id="48275-153">This syntax is inspired by jQuery, but it is not actually jQuery.</span></span>  <span data-ttu-id="48275-154">Il s’agit simplement d’un alias pour `document.querySelector()` .</span><span class="sxs-lookup"><span data-stu-id="48275-154">It is just an alias for `document.querySelector()`.</span></span>  
*   `debug(function)` <span data-ttu-id="48275-155">définit efficacement un point d’arrêt sur la première ligne de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="48275-155">effectively sets a breakpoint on the first line of that function.</span></span>  
*   `keys(object)` <span data-ttu-id="48275-156">retourne une matrice contenant les clés de l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="48275-156">returns an array containing the keys of the specified object.</span></span>  

<span data-ttu-id="48275-157">Pour plus d’informations sur les fonctions de commodité, accédez à informations de référence sur l’API de la [console][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="48275-157">For more information about the convenience functions, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <span data-ttu-id="48275-158">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="48275-158">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Commencer à utiliser la journalisation des messages dans la console | Documents Microsoft"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Référence de la console | Documents Microsoft"  
[DevToolsConsoleUtilities]: ./utilities.md "Référence sur l’API des utilitaires de console | Documents Microsoft"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools | Documents Microsoft"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Expressions et instructions dans JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Valeurs de paramètre par défaut-gestion étendue des paramètres-ECMAScript 6: nouvelles fonctionnalités: vue d’ensemble & comparaison"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Exemple de console JavaScript | Problème"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Lecture-eval-imprimer en boucle-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="48275-167">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="48275-167">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="48275-168">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/javascript) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="48275-168">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/javascript) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="48275-170">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="48275-170">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
