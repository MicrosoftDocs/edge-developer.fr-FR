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

# <a name="get-started-with-running-javascript-in-the-console"></a>Commencer à utiliser JavaScript dans la console  

Ce didacticiel interactif vous montre comment exécuter JavaScript dans la **console**Microsoft Edge DevTools.  Pour plus d’informations sur la journalisation des messages dans la **console,** accédez à [Démarrer avec la journalisation des messages.][DevToolsConsoleLoggingMessages]  Pour plus d’informations sur la façon de suspendre du code JavaScript et de le parcourir une ligne à la fois, accédez à Commencer avec [le débogage javaScript][DevToolsJavascriptIndex].  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="The Console" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   Console ****  
:::image-end:::  

## <a name="overview"></a>Vue d'ensemble  

La **console** est [un rePL,][WikiReadEvalPrintLoop]qui signifie Read, Evaluate, Print et Loop.  Il lit le code JavaScript que vous tapez dans celui-ci, évalue votre code, imprime le résultat de votre [expression,][2alityExpressionsVersusStatements]puis revient à la première étape.  

## <a name="set-up-devtools"></a>Configurer DevTools  

Ce didacticiel est conçu pour ouvrir la démonstration et essayer tous les flux de travail vous-même.  Lorsque vous suivez physiquement le processus, vous êtes plus susceptible de mémoriser les flux de travail ultérieurement.

1.  Sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\) pour ouvrir la **console.**  
1.  Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Javascript Example** to open in a new window.  
    
    *   [Exemple JavaScript pour la console][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="Page Exemple JavaScript pour la console à gauche et DevTools à droite" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       Page Exemple JavaScript pour la console à gauche et DevTools à droite  
    :::image-end:::  
    
## <a name="view-and-change-the-javascript-or-dom-of-the-page"></a>Afficher et modifier le JavaScript ou le DOM de la page  

Lors de la création ou du débogage d’une page, il est souvent utile d’exécuter des instructions dans la **console** afin de modifier l’apparence ou l’apparence de la page.  
    
1.  Notez le texte dans le bouton.  
1.  Tapez `document.getElementById('hello').textContent = 'Hello, Console!'` dans la **console,** puis sélectionnez `Enter` pour évaluer l’expression.  Notez que le texte à l’intérieur du bouton change.  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Apparence de la console après l’évaluation de l’expression" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       Apparence de la **console** après l’évaluation de l’expression  
    :::image-end:::  
    
    `"Hello, Console!"`, s’affiche sous le code que vous avez évalué.  N’oubliez pas les 4 étapes de REPL : lire, évaluer, imprimer, boucle.  Après avoir évalué votre code, un rePL imprime le résultat de l’expression.  Vous `"Hello, Console!"` devez donc être le résultat de l’évaluation. `document.getElementById('hello').textContent = 'Hello, Console!'`  
    
## <a name="run-arbitrary-javascript-that-is-not-related-to-the-page"></a>Exécuter un javaScript arbitraire qui n’est pas lié à la page  

Parfois, vous souhaitez simplement un aire de jeu de code où vous pouvez tester du code ou tester de nouvelles fonctionnalités JavaScript que vous ne connaissez pas.  La **console** est un endroit idéal pour ces types d’expériences.  

1.  Tapez `5 + 15` dans la console et sélectionnez pour évaluer `Enter` l’expression. La console imprime le résultat de l’expression sous votre code.  Dans la figure suivante, votre **console** doit afficher le résultat après avoir évalué l’expression.  

1.  Tapez le code suivant dans la **console.**  Essayez de la taper, caractère par caractère, plutôt que de la copier-coller.  
    
    ```javascript
    function add(a, b=20)
    ```  
    
    Si vous ne connaissez pas la `b=20` syntaxe, accédez à la définition des [valeurs par défaut des arguments de fonction.][Esma6DefaultParameterValues]  
    
1.  À présent, exécutez la fonction que vous venons de définir.  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="La console s’affiche après l’évaluation des expressions dans l’extrait de code" lightbox="../media/console-javascript-example-console-playground.msft.png":::
             La **console s’affiche** après l’évaluation des expressions dans l’extrait de code  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` est évaluée `45` à, car lorsque la `add` fonction est appelée sans second argument, est par défaut `b` . `20`  

## <a name="next-steps"></a>Étapes suivantes  

<!--To explore more features related to running JavaScript in the **Console**, navigate to [Run JavaScript][DevToolsConsoleReference].  -->  

<!--todo: add console reference (run javascript) section when available  -->  

DevTools vous permet de suspendre un script en cours d’exécution.  Pendant que vous êtes suspendu, vous pouvez utiliser la **console** pour afficher et modifier le ou la page à `window` ce `DOM` moment-là.  Le flux de travail constitue un flux de travail de débogage puissant.  Pour un didacticiel interactif, [accédez à Commencer avec le débogage de JavaScript][DevToolsJavascriptIndex].  

La **console** dispose également d’un ensemble de fonctions pratiques qui facilitent l’interaction avec une page.  Par exemple:  

*   Au lieu de taper `document.querySelector()` pour sélectionner un élément, tapez `$()` .  Cette syntaxe s’inspire de jQuery, mais elle n’est pas réellement jQuery.  Il s’agit simplement d’un alias pour `document.querySelector()` .  
*   `debug(function)` définit effectivement un point d’arrêt sur la première ligne de cette fonction.  
*   `keys(object)` renvoie un tableau contenant les clés de l’objet spécifié.  

Pour plus d’informations sur les fonctions pratiques, accédez à référence de [l’API des utilitaires de console.][DevToolsConsoleUtilities]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

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
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/javascript) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
