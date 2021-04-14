---
description: Présentation de l'outil Console à l'intérieur des outils de développement Microsoft Edge.
title: Utiliser la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 3f2f8c01a9bc9c4f40158f0959ba5b60e03bfb80
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483195"
---
# <a name="use-the-console"></a><span data-ttu-id="452d4-104">Utiliser la console</span><span class="sxs-lookup"><span data-stu-id="452d4-104">Use the Console</span></span>  

<span data-ttu-id="452d4-105">**L'outil Console** de DevTools vous aide à effectuer plusieurs tâches.</span><span class="sxs-lookup"><span data-stu-id="452d4-105">The **Console** tool of the DevTools helps you with several tasks.</span></span>  <span data-ttu-id="452d4-106">La liste suivante inclut certaines des tâches.</span><span class="sxs-lookup"><span data-stu-id="452d4-106">The following list includes some of the tasks.</span></span>  

*   <span data-ttu-id="452d4-107">Découvrez pourquoi quelque chose ne fonctionne pas dans le projet actuel et [recherchez les problèmes.][DevtoolsConsoleConsoleDebugJavascript]</span><span class="sxs-lookup"><span data-stu-id="452d4-107">Find out why something isn't working in the current project and [track down problems][DevtoolsConsoleConsoleDebugJavascript].</span></span>  
*   <span data-ttu-id="452d4-108">[Obtenez des informations sur le projet web dans][DevtoolsConsoleConsoleFilters] le navigateur en tant que messages de journal.</span><span class="sxs-lookup"><span data-stu-id="452d4-108">[Get information about the web project][DevtoolsConsoleConsoleFilters] in the browser as log messages.</span></span>  
*   <span data-ttu-id="452d4-109">[Journal des informations][DevtoolsConsoleConsoleLog] dans les scripts à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="452d4-109">[Log information][DevtoolsConsoleConsoleLog] in scripts for debugging purposes.</span></span>  
*   <span data-ttu-id="452d4-110">[Essayez les expressions JavaScript][DevtoolsConsoleConsoleJavascript] en direct dans [un environnement REPL.][WikiReadEvalPrintLoop]</span><span class="sxs-lookup"><span data-stu-id="452d4-110">[Try JavaScript expressions][DevtoolsConsoleConsoleJavascript] live in a [REPL][WikiReadEvalPrintLoop] environment.</span></span>  
*   <span data-ttu-id="452d4-111">[Interagir avec le projet web dans le navigateur à l'aide][DevtoolsConsoleConsoleDomInteraction] de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="452d4-111">[Interact with the web project in the browser][DevtoolsConsoleConsoleDomInteraction] using JavaScript.</span></span>  
    
<span data-ttu-id="452d4-112">La **console est** un excellent outil complémentaire à utiliser avec d'autres outils.</span><span class="sxs-lookup"><span data-stu-id="452d4-112">The **Console** is a great companion tool to use with others tools.</span></span>  <span data-ttu-id="452d4-113">La **console offre** un moyen puissant de scripter des fonctionnalités, d'inspecter et de manipuler la page web actuelle à l'aide de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="452d4-113">The **Console** provides a powerful way to script functionality, inspect, and manipulate the current webpage using JavaScript.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-main.msft.png" alt-text="Outil Console ouvert dans le panneau supérieur" lightbox="../media/console-intro-console-main.msft.png":::
         <span data-ttu-id="452d4-115">Outil **Console** ouvert dans le panneau supérieur</span><span class="sxs-lookup"><span data-stu-id="452d4-115">The **Console** tool open in the upper panel</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-panel.msft.png" alt-text="Console dans le panneau inférieur avec l'outil Éléments ouvert au-dessus" lightbox="../media/console-intro-console-panel.msft.png":::
         <span data-ttu-id="452d4-117">**Console dans** le panneau inférieur avec l'outil **Éléments** ouvert au-dessus</span><span class="sxs-lookup"><span data-stu-id="452d4-117">**Console** in the lower panel with the **Elements** tool open above it</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="452d4-118">Le moyen le plus rapide d'ouvrir directement la **console** consiste à sélectionner `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="452d4-118">The fastest way to directly open the **Console** is to select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

## <a name="error-reports-and-console"></a><span data-ttu-id="452d4-119">Rapports d'erreur et console</span><span class="sxs-lookup"><span data-stu-id="452d4-119">Error reports and Console</span></span>  

<span data-ttu-id="452d4-120">**La console** est l'endroit par défaut où les erreurs de connectivité et JavaScript sont signalées.</span><span class="sxs-lookup"><span data-stu-id="452d4-120">**Console** is the default place where JavaScript and connectivity errors are reported.</span></span>  <span data-ttu-id="452d4-121">Si des erreurs se produisent, un bouton s'affiche à côté de l'icône **Paramètres** dans DevTools qui fournit le nombre d'erreurs et d'avertissements.</span><span class="sxs-lookup"><span data-stu-id="452d4-121">If any errors occur, a button displays next to the **Settings** icon in DevTools that provides the number of errors and warnings.</span></span>  <span data-ttu-id="452d4-122">Choisissez-la pour ouvrir **la console** et afficher le problème.</span><span class="sxs-lookup"><span data-stu-id="452d4-122">Choose it to open the **Console** and display the problem.</span></span>  <span data-ttu-id="452d4-123">Pour plus d'informations, accédez [aux erreurs de débogage signalées dans la console.][DevtoolsConsoleConsoleDebugJavascript]</span><span class="sxs-lookup"><span data-stu-id="452d4-123">For more information, navigate to [Debug errors reported in Console][DevtoolsConsoleConsoleDebugJavascript].</span></span>  

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="DevTools fournit des informations détaillées sur l'erreur dans la console" lightbox="../media/console-debug-displays-error.msft.png":::
   <span data-ttu-id="452d4-125">DevTools fournit des informations détaillées sur l'erreur dans la **console**</span><span class="sxs-lookup"><span data-stu-id="452d4-125">DevTools gives detailed information about the error in the **Console**</span></span>  
:::image-end:::  

## <a name="inspect-and-filter-information-on-the-current-webpage"></a><span data-ttu-id="452d4-126">Inspecter et filtrer des informations sur la page web actuelle</span><span class="sxs-lookup"><span data-stu-id="452d4-126">Inspect and filter information on the current webpage</span></span>  

<span data-ttu-id="452d4-127">Lorsque vous ouvrez de DevTools sur une page web, vous risquez d'afficher une suragée d'informations consignées dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="452d4-127">When you open the DevTools on a webpage, you're likely to display a deluge of information logged to the **Console**.</span></span>  <span data-ttu-id="452d4-128">La quantité d'informations devient un problème lorsque vous devez identifier des informations importantes.</span><span class="sxs-lookup"><span data-stu-id="452d4-128">The amount of information becomes a problem when you need to identify important information.</span></span>  <span data-ttu-id="452d4-129">Pour afficher les informations importantes qui doivent être prises en compte, utilisez l'outil [Problèmes][DevtoolsIssuesIndex] dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="452d4-129">To view the important information that needs action, use the [Issues][DevtoolsIssuesIndex] tool in DevTools.</span></span>  <span data-ttu-id="452d4-130">Une grande partie du bruit reste, c'est pourquoi il est bon de connaître les [options][DevtoolsConsoleConsoleFilters] de journal automatisé et de filtre dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="452d4-130">Much of the noise remains, which is why it's a good idea to know about the [automated log and filter options][DevtoolsConsoleConsoleFilters] in the **Console**.</span></span>  

:::image type="complex" source="../media/console-intro-noise.msft.png" alt-text="DevTools avec une console pleine de messages" lightbox="../media/console-intro-noise.msft.png":::
   <span data-ttu-id="452d4-132">DevTools avec une **console pleine** de messages</span><span class="sxs-lookup"><span data-stu-id="452d4-132">DevTools with a **Console** full of messages</span></span>  
:::image-end:::  

## <a name="log-information-to-display-in-the-console"></a><span data-ttu-id="452d4-133">Informations de journal à afficher dans la console</span><span class="sxs-lookup"><span data-stu-id="452d4-133">Log information to display in the Console</span></span>  

<span data-ttu-id="452d4-134">Le cas d'utilisation le plus populaire de la console est la **journalisation** des informations de vos scripts à l'aide de la méthode ou d'autres `console.log()` méthodes similaires.</span><span class="sxs-lookup"><span data-stu-id="452d4-134">The most popular use case for the **Console** is logging information from your scripts using the `console.log()` method or other similar methods.</span></span>  <span data-ttu-id="452d4-135">Pour l'essayer, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="452d4-135">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="452d4-136">Pour ouvrir **console,** `Control` + `Shift` + `J` sélectionnez \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="452d4-136">To open **Console**, select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
1.  <span data-ttu-id="452d4-137">Accédez aux exemples de messages de [la console : journal, informations,][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]erreur et avertissement, ou copiez et exécutez l'extrait de code suivant dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="452d4-137">Navigate to [Console messages examples: log, info, error and warn][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml], or copy and run the following code snippet in the **Console**.</span></span>  
    
    ```javascript
    console.log('This is a log message');
    console.info('This is some information'); 
    console.error('This is an error');
    console.warn('This is a warning');
    console.log(document.body.getBoundingClientRect());
    console.table(document.body.getBoundingClientRect());
    let technologies = ["HTML", "CSS", "SVG", "ECMAScript"];
    console.groupCollapsed('Technolgies');
    technologies.forEach(tech => {console.info(tech);})
    console.groupEnd('Technolgies');
    ```  
    
1.  <span data-ttu-id="452d4-138">La **console** affiche les résultats.</span><span class="sxs-lookup"><span data-stu-id="452d4-138">The **Console** displays the results.</span></span>  
    
    :::image type="complex" source="../media/console-intro-logging.msft.png" alt-text="Console pleine de messages provoqués par du code de démonstration" lightbox="../media/console-intro-logging.msft.png":::
       <span data-ttu-id="452d4-140">**Console pleine** de messages provoqués par du code de démonstration</span><span class="sxs-lookup"><span data-stu-id="452d4-140">**Console** full of messages caused by demo code</span></span>  
    :::image-end:::  
    
<span data-ttu-id="452d4-141">De nombreuses méthodes utiles sont disponibles lorsque vous travaillez avec la **console.**</span><span class="sxs-lookup"><span data-stu-id="452d4-141">Many useful methods are available when you work with the **Console**.</span></span>  <span data-ttu-id="452d4-142">Pour plus d'informations, [accédez à Journal des messages dans l'outil Console.][DevtoolsConsoleConsoleLog]</span><span class="sxs-lookup"><span data-stu-id="452d4-142">For more information, navigate to [Log messages in the Console tool][DevtoolsConsoleConsoleLog].</span></span>  

## <a name="try-your-javascript-live-in-the-console"></a><span data-ttu-id="452d4-143">Essayez votre javaScript en direct dans la console</span><span class="sxs-lookup"><span data-stu-id="452d4-143">Try your JavaScript live in the Console</span></span>  

<span data-ttu-id="452d4-144">La **console n'est** pas seulement un endroit où enregistrer des informations.</span><span class="sxs-lookup"><span data-stu-id="452d4-144">The **Console** isn't only a place to log information.</span></span>  <span data-ttu-id="452d4-145">La **console** est un [environnement REPL.][WikiReadEvalPrintLoop]</span><span class="sxs-lookup"><span data-stu-id="452d4-145">The **Console** is a [REPL][WikiReadEvalPrintLoop] environment.</span></span>  <span data-ttu-id="452d4-146">Lorsque vous écrivez du code JavaScript dans la **console,** le code s'exécute immédiatement.</span><span class="sxs-lookup"><span data-stu-id="452d4-146">When you write any JavaScript in the **Console**, the code runs immediately.</span></span>  <span data-ttu-id="452d4-147">Il peut s'avérer utile de tester certaines nouvelles fonctionnalités JavaScript ou d'y faire des calculs rapides.</span><span class="sxs-lookup"><span data-stu-id="452d4-147">You may find it useful to test some new JavaScript features or to do some quick calculations.</span></span>  <span data-ttu-id="452d4-148">En outre, vous obtenez toutes les fonctionnalités que vous attendez d'un environnement d'édition moderne, telles que lacompletion automatique, la mise en surbrillance de la syntaxe et l'historique.</span><span class="sxs-lookup"><span data-stu-id="452d4-148">Also, you get all of the features you expect from a modern editing environment, such as autocompletion, syntax highlighting, and history.</span></span>  <span data-ttu-id="452d4-149">Pour l'essayer, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="452d4-149">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="452d4-150">Accédez à la **console.**</span><span class="sxs-lookup"><span data-stu-id="452d4-150">Navigate to the **Console**.</span></span>  
1.  <span data-ttu-id="452d4-151">Tapez `2 + 2`.</span><span class="sxs-lookup"><span data-stu-id="452d4-151">Type `2 + 2`.</span></span>  
    
<span data-ttu-id="452d4-152">La **console** affiche le résultat `4` sur la ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="452d4-152">The **Console** displays the result `4` on the following line.</span></span>  <span data-ttu-id="452d4-153">Cette **fonctionnalité d'évaluation** est utile pour déboguer et vérifier que vous n'avez pas fait d'erreurs dans votre code.</span><span class="sxs-lookup"><span data-stu-id="452d4-153">This **Eager evaluation** feature is useful to debug and verify that you aren't making mistakes in your code.</span></span>  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="La console affiche le résultat de 2 + 2 en direct lorsque vous le tapez" lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   <span data-ttu-id="452d4-155">La **console** affiche le résultat de la commande `2 + 2` live à mesure que vous la tapez.</span><span class="sxs-lookup"><span data-stu-id="452d4-155">The **Console** displays the result of `2 + 2` live as you type it</span></span>  
:::image-end:::  

<span data-ttu-id="452d4-156">Pour exécuter l'expression JavaScript dans la **console** et éventuellement afficher un résultat, sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="452d4-156">To run the JavaScript expression in the **Console** and optionally display a result, select `Enter`.</span></span>  <span data-ttu-id="452d4-157">Ensuite, vous pouvez écrire le code JavaScript suivant à exécuter dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="452d4-157">Then, you may write the next JavaScript code to run in the **Console**.</span></span>  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Exécuter plusieurs lignes de code JavaScript successivement" lightbox="../media/console-javascript-several-expressions.msft.png":::
   <span data-ttu-id="452d4-159">Exécuter plusieurs lignes de code JavaScript successivement</span><span class="sxs-lookup"><span data-stu-id="452d4-159">Run several lines of JavaScript code in succession</span></span>  
:::image-end:::  

<span data-ttu-id="452d4-160">Par défaut, vous exécutez du code JavaScript sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="452d4-160">By default, you run JavaScript code on a single line.</span></span>  <span data-ttu-id="452d4-161">Pour exécuter une ligne, tapez votre JavaScript, puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="452d4-161">To run a line, type your JavaScript and then select `Enter`.</span></span>  <span data-ttu-id="452d4-162">Pour contourner la limitation d'une seule ligne, sélectionnez `Shift` + `Enter` plutôt . `Enter`</span><span class="sxs-lookup"><span data-stu-id="452d4-162">To work around the single-line limitation, select `Shift`+`Enter` instead of `Enter`.</span></span>  <span data-ttu-id="452d4-163">Comme pour d'autres expériences de ligne de commande, pour accéder à vos commandes JavaScript précédentes, sélectionnez `Arrow-Up` .</span><span class="sxs-lookup"><span data-stu-id="452d4-163">Similar to other command-line experiences, to access your previous JavaScript commands, select `Arrow-Up`.</span></span>  <span data-ttu-id="452d4-164">La fonctionnalité decompletion automatique de la **console** est un excellent moyen d'en savoir plus sur les méthodes peu familières.</span><span class="sxs-lookup"><span data-stu-id="452d4-164">The autocompletion feature of the **Console** is a great way to learn about unfamiliar methods.</span></span>  <span data-ttu-id="452d4-165">Pour l'essayer, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="452d4-165">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="452d4-166">Ouvrez la **console.**</span><span class="sxs-lookup"><span data-stu-id="452d4-166">Open the **Console**.</span></span>  
1.  <span data-ttu-id="452d4-167">Tapez `doc`.</span><span class="sxs-lookup"><span data-stu-id="452d4-167">Type `doc`.</span></span>  
1.  <span data-ttu-id="452d4-168">Choisissez `document` dans le menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="452d4-168">Choose `document` from the dropdown menu.</span></span>  
1.  <span data-ttu-id="452d4-169">Sélectionnez `tab` la clé pour la sélectionner.</span><span class="sxs-lookup"><span data-stu-id="452d4-169">Select the `tab` key to choose it.</span></span>  
1.  <span data-ttu-id="452d4-170">Tapez `.bo`.</span><span class="sxs-lookup"><span data-stu-id="452d4-170">Type `.bo`.</span></span>  
1.  <span data-ttu-id="452d4-171">Sélectionnez `tab` pour obtenir `document.body` .</span><span class="sxs-lookup"><span data-stu-id="452d4-171">Select `tab` to get `document.body`.</span></span>  
1.  <span data-ttu-id="452d4-172">Tapez un autre pour afficher la liste complète des propriétés et méthodes `.` disponibles dans le corps de la page web actuelle.</span><span class="sxs-lookup"><span data-stu-id="452d4-172">Type another `.` to display the complete list of properties and methods available on the body of the current webpage.</span></span>  
    
<span data-ttu-id="452d4-173">Pour plus d'informations sur toutes les façons de travailler avec **console,** accédez à [Console en tant qu'environnement JavaScript.][DevtoolsConsoleConsoleJavascript]</span><span class="sxs-lookup"><span data-stu-id="452d4-173">For more information about all the ways to work with **Console**, navigate to [Console as a JavaScript environment][DevtoolsConsoleConsoleJavascript].</span></span>  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Autocompletion de console des expressions JavaScript" lightbox="../media/console-javascript-autocomplete.msft.png":::
   <span data-ttu-id="452d4-175">**Autocompletion** de console des expressions JavaScript</span><span class="sxs-lookup"><span data-stu-id="452d4-175">**Console** autocompletion of JavaScript expressions</span></span>  
:::image-end:::  

## <a name="interact-with-the-current-webpage-in-the-browser"></a><span data-ttu-id="452d4-176">Interagir avec la page web actuelle dans le navigateur</span><span class="sxs-lookup"><span data-stu-id="452d4-176">Interact with the current webpage in the browser</span></span>  

<span data-ttu-id="452d4-177">La **console** a accès à [l'objet Window][MdnDocsWebApiWindow] du navigateur.</span><span class="sxs-lookup"><span data-stu-id="452d4-177">The **Console** has access to the [Window][MdnDocsWebApiWindow] object of the browser.</span></span>  <span data-ttu-id="452d4-178">Vous pouvez écrire des scripts qui interagissent avec la page web actuelle.</span><span class="sxs-lookup"><span data-stu-id="452d4-178">You may write scripts that interact with the current webpage.</span></span>  <span data-ttu-id="452d4-179">Pour l'essayer, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="452d4-179">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="452d4-180">Ouvrez la **console.**</span><span class="sxs-lookup"><span data-stu-id="452d4-180">Open the **Console**.</span></span>  
1.  <span data-ttu-id="452d4-181">Copiez et collez l'extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="452d4-181">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    document.querySelector('h1').innerHTML
    ```  
    
:::image type="complex" source="../media/console-intro-reading-DOM.msft.png" alt-text="Copier le contenu de titre supérieur (h1) à partir du DOM et afficher dans la console" lightbox="../media/console-intro-reading-DOM.msft.png":::
   <span data-ttu-id="452d4-183">Copier le contenu de titre supérieur \( \) à partir du DOM et afficher `h1` dans la **console**</span><span class="sxs-lookup"><span data-stu-id="452d4-183">Copy the top heading \(`h1`\) content from the DOM and display in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="452d4-184">Au lieu de lire uniquement la page web, vous pouvez également la modifier.</span><span class="sxs-lookup"><span data-stu-id="452d4-184">Instead of only reading from the webpage, you may also change it.</span></span>  <span data-ttu-id="452d4-185">Pour l'essayer, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="452d4-185">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="452d4-186">Ouvrez la **console.**</span><span class="sxs-lookup"><span data-stu-id="452d4-186">Open the **Console**.</span></span>  
1.  <span data-ttu-id="452d4-187">Copiez et collez l'extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="452d4-187">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    document.querySelector('h1').innerHTML = 'Rocking the Console';
    ```  
    
:::image type="complex" source="../media/console-intro-wrtiting-DOM.msft.png" alt-text="Écrire du texte dans le DOM de la console" lightbox="../media/console-intro-wrtiting-DOM.msft.png":::
   <span data-ttu-id="452d4-189">Écrire du texte dans le DOM de la **console**</span><span class="sxs-lookup"><span data-stu-id="452d4-189">Write text to the DOM in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="452d4-190">Vous avez modifié le titre principal de la page web en **Basculement de la console.**</span><span class="sxs-lookup"><span data-stu-id="452d4-190">You changed the main heading of the webpage to **Rocking the Console**.</span></span>  <span data-ttu-id="452d4-191">Les **méthodes de l'utilitaire** console vous rendent facile d'accéder à la page web actuelle et de la manipuler.</span><span class="sxs-lookup"><span data-stu-id="452d4-191">The **Console Utility** methods make it easy to access and manipulate the current webpage.</span></span>  <span data-ttu-id="452d4-192">Pour plus d'informations, accédez à [la référence de l'API des utilitaires de console.][DevtoolsConsoleUtilities]</span><span class="sxs-lookup"><span data-stu-id="452d4-192">For more information, navigate to [Console Utilities API reference][DevtoolsConsoleUtilities].</span></span>  <span data-ttu-id="452d4-193">Par exemple, pour ajouter une bordure verte autour de tous les liens de la page web actuelle, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="452d4-193">For example, to add a green border around all the links in the current webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="452d4-194">Ouvrez la **console.**</span><span class="sxs-lookup"><span data-stu-id="452d4-194">Open the **Console**.</span></span>  
1.  <span data-ttu-id="452d4-195">Copiez et collez l'extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="452d4-195">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    $$('a').forEach(a => a.style.border='1px solid lime');
    ```  
    

:::image type="complex" source="../media/console-intro-changing-styles.msft.png" alt-text="Manipuler une sélection d'éléments à l'aide de la console" lightbox="../media/console-intro-changing-styles.msft.png":::
    <span data-ttu-id="452d4-197">Manipuler une sélection d'éléments à l'aide de la **console**</span><span class="sxs-lookup"><span data-stu-id="452d4-197">Manipulate a selection of elements using the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="452d4-198">Pour plus d'informations sur l'utilisation du DOM, accédez à [Utiliser la console pour interagir avec le DOM.][DevtoolsConsoleConsoleDomInteraction]</span><span class="sxs-lookup"><span data-stu-id="452d4-198">For more information about working with the DOM, navigate to [Use the Console to interact with the DOM][DevtoolsConsoleConsoleDomInteraction].</span></span>  

## <a name="learn-more-about-console"></a><span data-ttu-id="452d4-199">En savoir plus sur console</span><span class="sxs-lookup"><span data-stu-id="452d4-199">Learn more about Console</span></span>  

<span data-ttu-id="452d4-200">Pour plus d'informations sur la **console,** accédez à la référence de [console,][DevtoolsConsoleReference]à la référence d'API des utilitaires de [console][DevtoolsConsoleUtilities]et à la référence de [l'API de console.][DevtoolsConsoleApi]</span><span class="sxs-lookup"><span data-stu-id="452d4-200">For more information about the **Console**, navigate to [Console reference][DevtoolsConsoleReference], [Console Utilities API reference][DevtoolsConsoleUtilities], and [Console API reference][DevtoolsConsoleApi].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="452d4-201">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="452d4-201">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Référence de l'API de console | Documents Microsoft"  
[DevtoolsConsoleConsoleDebugJavascript]: ./console-debug-javascript.md "Erreurs de débogage signalées dans console | Documents Microsoft"  
[DevtoolsConsoleConsoleDomInteraction]: ./console-dom-interaction.md "Utiliser la console pour interagir avec la console DOM | Documents Microsoft" 
[DevtoolsConsoleConsoleFilters]: ./console-filters.md "Filtrer les messages de la console | Documents Microsoft"  
[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Console en tant qu'environnement JavaScript | Documents Microsoft"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Journal des messages dans l'outil console | Documents Microsoft"  
[DevtoolsConsoleReference]: ./reference.md "Référence de la console | Documents Microsoft"  
[DevtoolsConsoleUtilities]: ./utilities.md "Référence de l'API des utilitaires de console | Documents Microsoft"  

[DevtoolsIssuesIndex]: ../issues/index.md "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"  

[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-demo.html "Exemples de messages de console : journal, informations, erreurs et avertissements | GitHub"  

[MdnDocsWebApiWindow]: https://developer.mozilla.org/docs/Web/API/Window "Fenêtre | MDN"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lecture-eval-print loop | Wikipedia"  
