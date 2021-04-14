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
# <a name="the-console-as-a-javascript-environment"></a>Console en tant qu'environnement JavaScript  

**L'outil Console** à l'intérieur du navigateur DevTools est un [environnement REPL.][WikiReadEvalPrintLoop]  Cela signifie que vous pouvez écrire n'importe quel JavaScript dans la **console** qui s'exécute immédiatement.

Pour l'essayer, complétez les actions suivantes.  

1.  Ouvrez la **console.**  
    *   Sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).  
1.  Tapez `2 + 2`.  La **console** affiche déjà le résultat `4` sur la ligne suivante pendant que vous le tapez.  La `Eager evaluation` fonctionnalité vous permet d'écrire du JavaScript valide.  Il affiche le résultat lorsque vous tapez s'il est faux ou s'il existe un résultat valide.  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="La console affiche le résultat de 2 + 2 en direct lorsque vous la tapez" lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   **La** console affiche le résultat de `2 + 2` la commande Live à mesure que vous la tapez.  
:::image-end:::  

Si vous sélectionnez, la console exécute la commande JavaScript, vous donne le résultat et vous permet `Enter` d'écrire la commande suivante. ****  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Exécuter plusieurs expressions JavaScript successivement" lightbox="../media/console-javascript-several-expressions.msft.png":::
   Exécuter plusieurs expressions JavaScript successivement  
:::image-end:::  

## <a name="autocompletion-to-write-complex-expressions"></a>Autocompletion pour écrire des expressions complexes

Le dernier exemple peut sembler difficile à voir, mais la **console** vous aide à écrire du JavaScript complexe à l'aide d'une excellente fonctionnalité decompletion automatique.  Cette fonctionnalité est un excellent moyen d'en savoir plus sur les méthodes que vous ne connaissez pas auparavant.  

Pour l'essayer, complétez les actions suivantes.  

1.  Tapez `doc`.  
1.  Choisissez `document` dans le menu déroulant.  
1.  Sélectionnez `tab` la clé pour la sélectionner.  
1.  Tapez `.bo`.  
1.  Sélectionnez `tab` pour obtenir `document.body` .  
1.  Tapez un autre pour obtenir une grande liste des propriétés et méthodes possibles disponibles dans le `.` corps de la page web actuelle.  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Autocompletion de console des expressions JavaScript" lightbox="../media/console-javascript-autocomplete.msft.png":::
   **Autocompletion** de console des expressions JavaScript  
:::image-end:::  

## <a name="console-history"></a>Historique de la console

Comme avec de nombreuses autres expériences de ligne de commande, vous avez également un historique des commandes.  Sélectionnez `Arrow Up` pour afficher les commandes que vous avez entrées auparavant.  Lacompletion automatique conserve également un historique des commandes que vous avez tapés précédemment.  Vous pouvez taper les premières lettres des commandes précédentes et vos choix précédents s'affichent dans une boîte de texte.  

En outre, **la console** offre également quelques méthodes [utilitaires qui][DevtoolsConsoleUtilities] vous facilitent la vie.  Par exemple, contient toujours le résultat de la dernière expression que vous avez écrite `$_` dans la **console.**

:::image type="complex" source="../media/console-javascript-console-history.msft.png" alt-text="L$expression $_ dans la console contient toujours le dernier résultat" lightbox="../media/console-javascript-console-history.msft.png":::
    `$_`L'expression dans la **console** contient toujours le dernier résultat  
:::image-end:::  

## <a name="multiline-edits"></a>Modifications multilignes

Par défaut, la **console ne** vous donne qu'une seule ligne pour écrire votre expression JavaScript.  Vous exécutez le code lorsque vous sélectionnez `Enter` . La limitation d'une ligne peut vous insérait.  Pour contourner la limitation d'une ligne, sélectionnez `Shift` + `Enter` plutôt `Enter` .  Dans l'exemple suivant, la valeur affichée est le résultat de toutes les lignes s'exécutent dans l'ordre.  

:::image type="complex" source="../media/console-javascript-multiline.msft.png" alt-text="Sélectionnez Shift+Enter pour écrire plusieurs lignes de JavaScript et la valeur résultante est exécuté dans l'ordre" lightbox="../media/console-javascript-multiline.msft.png":::
   Sélectionnez pour écrire plusieurs lignes de JavaScript et la valeur `Shift` + `Enter` résultante est exécuté dans l'ordre  
:::image-end:::  

Si vous démarrez une instruction multiligne dans la **console,** elle est automatiquement reconnue et en retrait.  Par exemple, si vous démarrez une instruction block avec une accolade.  

:::image type="complex" source="../media/console-javascript-automatic-lineindent.msft.png" alt-text="La console reconnaît déjà les expressions multilignes à l'aide d'accolades et de retraits pour vous" lightbox="../media/console-javascript-automatic-lineindent.msft.png":::
    **La console** reconnaît déjà les expressions multilignes à l'aide d'accolades et de retraits pour vous  
:::image-end:::  

## <a name="network-requests-using-top-level-await"></a>Demandes réseau utilisant await() de niveau supérieur  

Autre que dans vos propres scripts, **console** prend en charge [l'attente][GithubTc39ProposalTopLevelAwait] de niveau supérieur pour exécuter arbitraire javaScript asynchrone dans celui-ci.  Par exemple, utilisez `fetch` l'API sans habillage de `await` l'instruction avec une fonction async.  

Pour obtenir les 50 derniers problèmes classés dans les outils de développement [Microsoft Edge pour Visual Studio référentiel][GithubMicrosoftVscodeEdgeDevtools] GitHub code, effectuer les actions suivantes.  

1.  Ouvrez la **console.**  
1.  Copiez et collez l'extrait de code suivant pour obtenir un objet qui contient 10 entrées.  
    
    ```javascript
    await ( await fetch(
    'https://api.github.com/repos/microsoft/vscode-edge-devtools/issues?state=all&per_page=50&page=1'
    )).json();
    ```  
    
:::image type="complex" source="../media/console-javascript-top-level-await.msft.png" alt-text="La console affiche le résultat d'une demande d'extraction async de niveau supérieur" lightbox="../media/console-javascript-top-level-await.msft.png":::
    **La** console affiche le résultat d'une demande async de niveau `fetch` supérieur  
:::image-end:::  

Les 10 entrées sont difficiles à reconnaître, car de nombreuses informations sont affichées.  Heureusement, vous pouvez utiliser la méthode log pour recevoir uniquement les informations qui `console.table()` vous intéressent.  

:::image type="complex" source="../media/console-javascript-filtered-with-table.msft.png" alt-text="Afficher le dernier résultat dans un format lisible par l'homme à l'aide de console.table" lightbox="../media/console-javascript-filtered-with-table.msft.png":::
    Affichage du dernier résultat dans un format lisible par l'homme à l'aide `console.table`  
:::image-end:::  

Pour réutiliser les données renvoyées par une expression, vous pouvez utiliser la méthode `copy()` utilitaire de la **console**.  L'extrait de code suivant envoie la demande et copie les données de la réponse dans le Presse-papiers.  

```javascript
copy(await (await fetch(
'https://api.github.com/repos/microsoft/vscode-edge-devtools/issues?state=all&per_page=50&page=1'
)).json())
```  

Utilisez la **console** comme un excellent moyen de pratique des fonctionnalités JavaScript et d'y faire des calculs rapides.  La puissance réelle est le fait que vous avez accès à [l'objet fenêtre.][MdnDocsWebApiWindow]  Vous pouvez [interagir avec le DOM dans la console.][DevtoolsConsoleConsoleDomInteraction]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleDomInteraction]: ./console-dom-interaction.md "Utiliser la console pour interagir avec la console DOM | Documents Microsoft"  
[DevtoolsConsoleUtilities]: ./utilities.md "Référence de l'API des utilitaires de console | Documents Microsoft"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubTc39ProposalTopLevelAwait]: https://github.com/tc39/proposal-top-level-await "Proposition ECMAScript : Top-level await - tc39/proposal-top-level-await | GitHub"

[MdnDocsWebApiWindow]: https://developer.mozilla.org/docs/Web/API/Window "Fenêtre | MDN"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lecture-eval-print loop | Wikipedia"  
