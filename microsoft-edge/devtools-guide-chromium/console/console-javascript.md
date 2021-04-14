---
description: Introduction à l'utilisation de l'outil Console dans les outils de développement Microsoft Edge en tant qu'environnement JavaScript.
title: Console en tant qu'environnement JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, JavaScript, développement web, outils f12, devtools
ms.openlocfilehash: f75ac6d728c9a69542b2f58df85248759267f76d
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483412"
---
# <a name="the-console-as-a-javascript-environment"></a><span data-ttu-id="bbd6e-104">Console en tant qu'environnement JavaScript</span><span class="sxs-lookup"><span data-stu-id="bbd6e-104">The Console as a JavaScript environment</span></span>  

<span data-ttu-id="bbd6e-105">**L'outil Console** à l'intérieur du navigateur DevTools est un [environnement REPL.][WikiReadEvalPrintLoop]</span><span class="sxs-lookup"><span data-stu-id="bbd6e-105">The **Console** tool inside the browser DevTools is a [REPL][WikiReadEvalPrintLoop] environment.</span></span>  <span data-ttu-id="bbd6e-106">Cela signifie que vous pouvez écrire n'importe quel JavaScript dans la **console** qui s'exécute immédiatement.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-106">It means that you may write any JavaScript in the **Console** that runs immediately.</span></span>

<span data-ttu-id="bbd6e-107">Pour l'essayer, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-107">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="bbd6e-108">Ouvrez la **console.**</span><span class="sxs-lookup"><span data-stu-id="bbd6e-108">Open the **Console**.</span></span>  
    *   <span data-ttu-id="bbd6e-109">Sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="bbd6e-109">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
1.  <span data-ttu-id="bbd6e-110">Tapez `2 + 2`.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-110">Type `2 + 2`.</span></span>  <span data-ttu-id="bbd6e-111">La **console** affiche déjà le résultat `4` sur la ligne suivante pendant que vous le tapez.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-111">The **Console** already displays the result `4` on the next line while you type it.</span></span>  <span data-ttu-id="bbd6e-112">La `Eager evaluation` fonctionnalité vous permet d'écrire du JavaScript valide.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-112">The `Eager evaluation` feature helps you write valid JavaScript.</span></span>  <span data-ttu-id="bbd6e-113">Il affiche le résultat lorsque vous tapez s'il est faux ou s'il existe un résultat valide.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-113">It displays the result while you type whether it's wrong or if a valid result exists.</span></span>  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="La console affiche le résultat de 2 + 2 en direct lorsque vous la tapez" lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   <span data-ttu-id="bbd6e-115">**La** console affiche le résultat de `2 + 2` la commande Live à mesure que vous la tapez.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-115">**Console** displays the result of `2 + 2` live as you type it</span></span>  
:::image-end:::  

<span data-ttu-id="bbd6e-116">Si vous sélectionnez, la console exécute la commande JavaScript, vous donne le résultat et vous permet `Enter` d'écrire la commande suivante. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="bbd6e-116">If you select `Enter`, the **Console** runs the JavaScript command, gives you the result, and allows you to write the next command.</span></span>  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Exécuter plusieurs expressions JavaScript successivement" lightbox="../media/console-javascript-several-expressions.msft.png":::
   <span data-ttu-id="bbd6e-118">Exécuter plusieurs expressions JavaScript successivement</span><span class="sxs-lookup"><span data-stu-id="bbd6e-118">Run several JavaScript expressions in succession</span></span>  
:::image-end:::  

## <a name="autocompletion-to-write-complex-expressions"></a><span data-ttu-id="bbd6e-119">Autocompletion pour écrire des expressions complexes</span><span class="sxs-lookup"><span data-stu-id="bbd6e-119">Autocompletion to write complex expressions</span></span>

<span data-ttu-id="bbd6e-120">Le dernier exemple peut sembler difficile à voir, mais la **console** vous aide à écrire du JavaScript complexe à l'aide d'une excellente fonctionnalité decompletion automatique.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-120">The last example may seem scary, but the **Console** helps you write complex JavaScript using an excellent autocompletion feature.</span></span>  <span data-ttu-id="bbd6e-121">Cette fonctionnalité est un excellent moyen d'en savoir plus sur les méthodes que vous ne connaissez pas auparavant.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-121">This feature is a great way to learn about methods you didn't know before.</span></span>  

<span data-ttu-id="bbd6e-122">Pour l'essayer, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-122">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="bbd6e-123">Tapez `doc`.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-123">Type `doc`.</span></span>  
1.  <span data-ttu-id="bbd6e-124">Choisissez `document` dans le menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-124">Choose `document` from the dropdown menu.</span></span>  
1.  <span data-ttu-id="bbd6e-125">Sélectionnez `tab` la clé pour la sélectionner.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-125">Select the `tab` key to choose it.</span></span>  
1.  <span data-ttu-id="bbd6e-126">Tapez `.bo`.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-126">Type `.bo`.</span></span>  
1.  <span data-ttu-id="bbd6e-127">Sélectionnez `tab` pour obtenir `document.body` .</span><span class="sxs-lookup"><span data-stu-id="bbd6e-127">Select `tab` to get `document.body`.</span></span>  
1.  <span data-ttu-id="bbd6e-128">Tapez un autre pour obtenir une grande liste des propriétés et méthodes possibles disponibles dans le `.` corps de la page web actuelle.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-128">Type another `.` to get a large list of possible properties and methods available on the body of the current webpage.</span></span>  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Autocompletion de console des expressions JavaScript" lightbox="../media/console-javascript-autocomplete.msft.png":::
   <span data-ttu-id="bbd6e-130">**Autocompletion** de console des expressions JavaScript</span><span class="sxs-lookup"><span data-stu-id="bbd6e-130">**Console** autocompletion of JavaScript expressions</span></span>  
:::image-end:::  

## <a name="console-history"></a><span data-ttu-id="bbd6e-131">Historique de la console</span><span class="sxs-lookup"><span data-stu-id="bbd6e-131">Console history</span></span>

<span data-ttu-id="bbd6e-132">Comme avec de nombreuses autres expériences de ligne de commande, vous avez également un historique des commandes.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-132">As with many other command-line experiences, you also have a history of commands.</span></span>  <span data-ttu-id="bbd6e-133">Sélectionnez `Arrow Up` pour afficher les commandes que vous avez entrées auparavant.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-133">Select `Arrow Up` to display the commands you entered before.</span></span>  <span data-ttu-id="bbd6e-134">Lacompletion automatique conserve également un historique des commandes que vous avez tapés précédemment.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-134">Autocompletion also keeps a history of the commands you previously typed.</span></span>  <span data-ttu-id="bbd6e-135">Vous pouvez taper les premières lettres des commandes précédentes et vos choix précédents s'affichent dans une boîte de texte.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-135">You may type the first few letters of earlier commands and your previous choices display in a textbox.</span></span>  

<span data-ttu-id="bbd6e-136">En outre, **la console** offre également quelques méthodes [utilitaires qui][DevtoolsConsoleUtilities] vous facilitent la vie.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-136">Also, the **Console** also offers quite a few [utility methods][DevtoolsConsoleUtilities] that make your life easier.</span></span>  <span data-ttu-id="bbd6e-137">Par exemple, contient toujours le résultat de la dernière expression que vous avez écrite `$_` dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="bbd6e-137">For example, `$_` always contains the result of the last expression you ran in the **Console**.</span></span>

:::image type="complex" source="../media/console-javascript-console-history.msft.png" alt-text="L$expression $_ dans la console contient toujours le dernier résultat" lightbox="../media/console-javascript-console-history.msft.png":::
    <span data-ttu-id="bbd6e-139">`$_`L'expression dans la **console** contient toujours le dernier résultat</span><span class="sxs-lookup"><span data-stu-id="bbd6e-139">The `$_` expression in the **Console** always contains the last result</span></span>  
:::image-end:::  

## <a name="multiline-edits"></a><span data-ttu-id="bbd6e-140">Modifications multilignes</span><span class="sxs-lookup"><span data-stu-id="bbd6e-140">Multiline edits</span></span>

<span data-ttu-id="bbd6e-141">Par défaut, la **console ne** vous donne qu'une seule ligne pour écrire votre expression JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-141">By default, the **Console** only gives you one line to write your JavaScript expression.</span></span>  <span data-ttu-id="bbd6e-142">Vous exécutez le code lorsque vous sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="bbd6e-142">You code runs when you select `Enter`.</span></span> <span data-ttu-id="bbd6e-143">La limitation d'une ligne peut vous insérait.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-143">The one line limitation may frustrate you.</span></span>  <span data-ttu-id="bbd6e-144">Pour contourner la limitation d'une ligne, sélectionnez `Shift` + `Enter` plutôt `Enter` .</span><span class="sxs-lookup"><span data-stu-id="bbd6e-144">To work around the one line limitation, select `Shift`+`Enter` instead of `Enter`.</span></span>  <span data-ttu-id="bbd6e-145">Dans l'exemple suivant, la valeur affichée est le résultat de toutes les lignes s'exécutent dans l'ordre.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-145">In the following example, the value displayed is the result of all the lines run in order.</span></span>  

:::image type="complex" source="../media/console-javascript-multiline.msft.png" alt-text="Sélectionnez Shift+Enter pour écrire plusieurs lignes de JavaScript et la valeur résultante est exécuté dans l'ordre" lightbox="../media/console-javascript-multiline.msft.png":::
   <span data-ttu-id="bbd6e-147">Sélectionnez pour écrire plusieurs lignes de JavaScript et la valeur `Shift` + `Enter` résultante est exécuté dans l'ordre</span><span class="sxs-lookup"><span data-stu-id="bbd6e-147">Select `Shift`+`Enter` to write several lines of JavaScript and the resulting value is run in order</span></span>  
:::image-end:::  

<span data-ttu-id="bbd6e-148">Si vous démarrez une instruction multiligne dans la **console,** elle est automatiquement reconnue et en retrait.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-148">If you start a multiline statement in the **Console**, it gets automatically recognized and indented.</span></span>  <span data-ttu-id="bbd6e-149">Par exemple, si vous démarrez une instruction block avec une accolade.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-149">For example, if you start a block statement with a curly brace.</span></span>  

:::image type="complex" source="../media/console-javascript-automatic-lineindent.msft.png" alt-text="La console reconnaît déjà les expressions multilignes à l'aide d'accolades et de retraits pour vous" lightbox="../media/console-javascript-automatic-lineindent.msft.png":::
    <span data-ttu-id="bbd6e-151">**La console** reconnaît déjà les expressions multilignes à l'aide d'accolades et de retraits pour vous</span><span class="sxs-lookup"><span data-stu-id="bbd6e-151">**Console** already recognizes multiline expressions using curly braces and indents each for you</span></span>  
:::image-end:::  

## <a name="network-requests-using-top-level-await"></a><span data-ttu-id="bbd6e-152">Demandes réseau utilisant await() de niveau supérieur</span><span class="sxs-lookup"><span data-stu-id="bbd6e-152">Network requests using top-level await()</span></span>  

<span data-ttu-id="bbd6e-153">Autre que dans vos propres scripts, **console** prend en charge [l'attente][GithubTc39ProposalTopLevelAwait] de niveau supérieur pour exécuter arbitraire javaScript asynchrone dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-153">Other than in your own scripts, **Console** supports [top level await][GithubTc39ProposalTopLevelAwait] to run arbitrary asynchronous JavaScript in it.</span></span>  <span data-ttu-id="bbd6e-154">Par exemple, utilisez `fetch` l'API sans habillage de `await` l'instruction avec une fonction async.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-154">For example, use the `fetch` API without wrapping the `await` statement with an async function.</span></span>  

<span data-ttu-id="bbd6e-155">Pour obtenir les 50 derniers problèmes classés dans les outils de développement [Microsoft Edge pour Visual Studio référentiel][GithubMicrosoftVscodeEdgeDevtools] GitHub code, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-155">To get the last 50 issues filed on the [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] GitHub repo, complete the following actions.</span></span>  

1.  <span data-ttu-id="bbd6e-156">Ouvrez la **console.**</span><span class="sxs-lookup"><span data-stu-id="bbd6e-156">Open the **Console**.</span></span>  
1.  <span data-ttu-id="bbd6e-157">Copiez et collez l'extrait de code suivant pour obtenir un objet qui contient 10 entrées.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-157">Copy and paste the following code snippet to get an object that contains 10 entries.</span></span>  
    
    ```javascript
    await ( await fetch(
    'https://api.github.com/repos/microsoft/vscode-edge-devtools/issues?state=all&per_page=50&page=1'
    )).json();
    ```  
    
:::image type="complex" source="../media/console-javascript-top-level-await.msft.png" alt-text="La console affiche le résultat d'une demande d'extraction async de niveau supérieur" lightbox="../media/console-javascript-top-level-await.msft.png":::
    <span data-ttu-id="bbd6e-159">**La** console affiche le résultat d'une demande async de niveau `fetch` supérieur</span><span class="sxs-lookup"><span data-stu-id="bbd6e-159">**Console** displays the result of a top-level async `fetch` request</span></span>  
:::image-end:::  

<span data-ttu-id="bbd6e-160">Les 10 entrées sont difficiles à reconnaître, car de nombreuses informations sont affichées.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-160">The 10 entries are hard to recognize, since a lot of information is displayed.</span></span>  <span data-ttu-id="bbd6e-161">Heureusement, vous pouvez utiliser la méthode log pour recevoir uniquement les informations qui `console.table()` vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-161">Luckily enough, you may use the `console.table()` log method to only receive the information in which you're interested.</span></span>  

:::image type="complex" source="../media/console-javascript-filtered-with-table.msft.png" alt-text="Afficher le dernier résultat dans un format lisible par l'homme à l'aide de console.table" lightbox="../media/console-javascript-filtered-with-table.msft.png":::
    <span data-ttu-id="bbd6e-163">Affichage du dernier résultat dans un format lisible par l'homme à l'aide</span><span class="sxs-lookup"><span data-stu-id="bbd6e-163">Display the last result in a human readable format using</span></span> `console.table`  
:::image-end:::  

<span data-ttu-id="bbd6e-164">Pour réutiliser les données renvoyées par une expression, vous pouvez utiliser la méthode `copy()` utilitaire de la **console**.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-164">To reuse the data returned from an expression, you may use the `copy()` utility method of the **Console**.</span></span>  <span data-ttu-id="bbd6e-165">L'extrait de code suivant envoie la demande et copie les données de la réponse dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-165">The following code snippet sends the request and copies the data from the response to the clipboard.</span></span>  

```javascript
copy(await (await fetch(
'https://api.github.com/repos/microsoft/vscode-edge-devtools/issues?state=all&per_page=50&page=1'
)).json())
```  

<span data-ttu-id="bbd6e-166">Utilisez la **console** comme un excellent moyen de pratique des fonctionnalités JavaScript et d'y faire des calculs rapides.</span><span class="sxs-lookup"><span data-stu-id="bbd6e-166">Use the **Console** as a great way to practice JavaScript functionality and to do some quick calculations.</span></span>  <span data-ttu-id="bbd6e-167">La puissance réelle est le fait que vous avez accès à [l'objet fenêtre.][MdnDocsWebApiWindow]</span><span class="sxs-lookup"><span data-stu-id="bbd6e-167">The real power is the fact that you have access to the [window][MdnDocsWebApiWindow] object.</span></span>  <span data-ttu-id="bbd6e-168">Vous pouvez [interagir avec le DOM dans la console.][DevtoolsConsoleConsoleDomInteraction]</span><span class="sxs-lookup"><span data-stu-id="bbd6e-168">You may [interact with the DOM in Console][DevtoolsConsoleConsoleDomInteraction].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="bbd6e-169">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="bbd6e-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleDomInteraction]: ./console-dom-interaction.md "Utiliser la console pour interagir avec la console DOM | Documents Microsoft"  
[DevtoolsConsoleUtilities]: ./utilities.md "Référence de l'API des utilitaires de console | Documents Microsoft"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubTc39ProposalTopLevelAwait]: https://github.com/tc39/proposal-top-level-await "Proposition ECMAScript : Top-level await - tc39/proposal-top-level-await | GitHub"

[MdnDocsWebApiWindow]: https://developer.mozilla.org/docs/Web/API/Window "Fenêtre | MDN"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lecture-eval-print loop | Wikipedia"  
