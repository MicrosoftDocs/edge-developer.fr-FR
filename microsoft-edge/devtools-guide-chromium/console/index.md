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
# <a name="use-the-console"></a>Utiliser la console  

**L'outil Console** de DevTools vous aide à effectuer plusieurs tâches.  La liste suivante inclut certaines des tâches.  

*   Découvrez pourquoi quelque chose ne fonctionne pas dans le projet actuel et [recherchez les problèmes.][DevtoolsConsoleConsoleDebugJavascript]  
*   [Obtenez des informations sur le projet web dans][DevtoolsConsoleConsoleFilters] le navigateur en tant que messages de journal.  
*   [Journal des informations][DevtoolsConsoleConsoleLog] dans les scripts à des fins de débogage.  
*   [Essayez les expressions JavaScript][DevtoolsConsoleConsoleJavascript] en direct dans [un environnement REPL.][WikiReadEvalPrintLoop]  
*   [Interagir avec le projet web dans le navigateur à l'aide][DevtoolsConsoleConsoleDomInteraction] de JavaScript.  
    
La **console est** un excellent outil complémentaire à utiliser avec d'autres outils.  La **console offre** un moyen puissant de scripter des fonctionnalités, d'inspecter et de manipuler la page web actuelle à l'aide de JavaScript.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-main.msft.png" alt-text="Outil Console ouvert dans le panneau supérieur" lightbox="../media/console-intro-console-main.msft.png":::
         Outil **Console** ouvert dans le panneau supérieur  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-panel.msft.png" alt-text="Console dans le panneau inférieur avec l'outil Éléments ouvert au-dessus" lightbox="../media/console-intro-console-panel.msft.png":::
         **Console dans** le panneau inférieur avec l'outil **Éléments** ouvert au-dessus  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Le moyen le plus rapide d'ouvrir directement la **console** consiste à sélectionner `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).  

## <a name="error-reports-and-console"></a>Rapports d'erreur et console  

**La console** est l'endroit par défaut où les erreurs de connectivité et JavaScript sont signalées.  Si des erreurs se produisent, un bouton s'affiche à côté de l'icône **Paramètres** dans DevTools qui fournit le nombre d'erreurs et d'avertissements.  Choisissez-la pour ouvrir **la console** et afficher le problème.  Pour plus d'informations, accédez [aux erreurs de débogage signalées dans la console.][DevtoolsConsoleConsoleDebugJavascript]  

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="DevTools fournit des informations détaillées sur l'erreur dans la console" lightbox="../media/console-debug-displays-error.msft.png":::
   DevTools fournit des informations détaillées sur l'erreur dans la **console**  
:::image-end:::  

## <a name="inspect-and-filter-information-on-the-current-webpage"></a>Inspecter et filtrer des informations sur la page web actuelle  

Lorsque vous ouvrez de DevTools sur une page web, vous risquez d'afficher une suragée d'informations consignées dans la **console.**  La quantité d'informations devient un problème lorsque vous devez identifier des informations importantes.  Pour afficher les informations importantes qui doivent être prises en compte, utilisez l'outil [Problèmes][DevtoolsIssuesIndex] dans DevTools.  Une grande partie du bruit reste, c'est pourquoi il est bon de connaître les [options][DevtoolsConsoleConsoleFilters] de journal automatisé et de filtre dans la **console.**  

:::image type="complex" source="../media/console-intro-noise.msft.png" alt-text="DevTools avec une console pleine de messages" lightbox="../media/console-intro-noise.msft.png":::
   DevTools avec une **console pleine** de messages  
:::image-end:::  

## <a name="log-information-to-display-in-the-console"></a>Informations de journal à afficher dans la console  

Le cas d'utilisation le plus populaire de la console est la **journalisation** des informations de vos scripts à l'aide de la méthode ou d'autres `console.log()` méthodes similaires.  Pour l'essayer, complétez les actions suivantes.  

1.  Pour ouvrir **console,** `Control` + `Shift` + `J` sélectionnez \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).  
1.  Accédez aux exemples de messages de [la console : journal, informations,][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]erreur et avertissement, ou copiez et exécutez l'extrait de code suivant dans la **console.**  
    
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
    
1.  La **console** affiche les résultats.  
    
    :::image type="complex" source="../media/console-intro-logging.msft.png" alt-text="Console pleine de messages provoqués par du code de démonstration" lightbox="../media/console-intro-logging.msft.png":::
       **Console pleine** de messages provoqués par du code de démonstration  
    :::image-end:::  
    
De nombreuses méthodes utiles sont disponibles lorsque vous travaillez avec la **console.**  Pour plus d'informations, [accédez à Journal des messages dans l'outil Console.][DevtoolsConsoleConsoleLog]  

## <a name="try-your-javascript-live-in-the-console"></a>Essayez votre javaScript en direct dans la console  

La **console n'est** pas seulement un endroit où enregistrer des informations.  La **console** est un [environnement REPL.][WikiReadEvalPrintLoop]  Lorsque vous écrivez du code JavaScript dans la **console,** le code s'exécute immédiatement.  Il peut s'avérer utile de tester certaines nouvelles fonctionnalités JavaScript ou d'y faire des calculs rapides.  En outre, vous obtenez toutes les fonctionnalités que vous attendez d'un environnement d'édition moderne, telles que lacompletion automatique, la mise en surbrillance de la syntaxe et l'historique.  Pour l'essayer, complétez les actions suivantes.  

1.  Accédez à la **console.**  
1.  Tapez `2 + 2`.  
    
La **console** affiche le résultat `4` sur la ligne suivante.  Cette **fonctionnalité d'évaluation** est utile pour déboguer et vérifier que vous n'avez pas fait d'erreurs dans votre code.  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="La console affiche le résultat de 2 + 2 en direct lorsque vous le tapez" lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   La **console** affiche le résultat de la commande `2 + 2` live à mesure que vous la tapez.  
:::image-end:::  

Pour exécuter l'expression JavaScript dans la **console** et éventuellement afficher un résultat, sélectionnez `Enter` .  Ensuite, vous pouvez écrire le code JavaScript suivant à exécuter dans la **console.**  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Exécuter plusieurs lignes de code JavaScript successivement" lightbox="../media/console-javascript-several-expressions.msft.png":::
   Exécuter plusieurs lignes de code JavaScript successivement  
:::image-end:::  

Par défaut, vous exécutez du code JavaScript sur une seule ligne.  Pour exécuter une ligne, tapez votre JavaScript, puis sélectionnez `Enter` .  Pour contourner la limitation d'une seule ligne, sélectionnez `Shift` + `Enter` plutôt . `Enter`  Comme pour d'autres expériences de ligne de commande, pour accéder à vos commandes JavaScript précédentes, sélectionnez `Arrow-Up` .  La fonctionnalité decompletion automatique de la **console** est un excellent moyen d'en savoir plus sur les méthodes peu familières.  Pour l'essayer, complétez les actions suivantes.  

1.  Ouvrez la **console.**  
1.  Tapez `doc`.  
1.  Choisissez `document` dans le menu déroulant.  
1.  Sélectionnez `tab` la clé pour la sélectionner.  
1.  Tapez `.bo`.  
1.  Sélectionnez `tab` pour obtenir `document.body` .  
1.  Tapez un autre pour afficher la liste complète des propriétés et méthodes `.` disponibles dans le corps de la page web actuelle.  
    
Pour plus d'informations sur toutes les façons de travailler avec **console,** accédez à [Console en tant qu'environnement JavaScript.][DevtoolsConsoleConsoleJavascript]  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Autocompletion de console des expressions JavaScript" lightbox="../media/console-javascript-autocomplete.msft.png":::
   **Autocompletion** de console des expressions JavaScript  
:::image-end:::  

## <a name="interact-with-the-current-webpage-in-the-browser"></a>Interagir avec la page web actuelle dans le navigateur  

La **console** a accès à [l'objet Window][MdnDocsWebApiWindow] du navigateur.  Vous pouvez écrire des scripts qui interagissent avec la page web actuelle.  Pour l'essayer, complétez les actions suivantes.  

1.  Ouvrez la **console.**  
1.  Copiez et collez l'extrait de code suivant.  
    
    ```javascript
    document.querySelector('h1').innerHTML
    ```  
    
:::image type="complex" source="../media/console-intro-reading-DOM.msft.png" alt-text="Copier le contenu de titre supérieur (h1) à partir du DOM et afficher dans la console" lightbox="../media/console-intro-reading-DOM.msft.png":::
   Copier le contenu de titre supérieur \( \) à partir du DOM et afficher `h1` dans la **console**  
:::image-end:::  

Au lieu de lire uniquement la page web, vous pouvez également la modifier.  Pour l'essayer, complétez les actions suivantes.  

1.  Ouvrez la **console.**  
1.  Copiez et collez l'extrait de code suivant.  
    
    ```javascript
    document.querySelector('h1').innerHTML = 'Rocking the Console';
    ```  
    
:::image type="complex" source="../media/console-intro-wrtiting-DOM.msft.png" alt-text="Écrire du texte dans le DOM de la console" lightbox="../media/console-intro-wrtiting-DOM.msft.png":::
   Écrire du texte dans le DOM de la **console**  
:::image-end:::  

Vous avez modifié le titre principal de la page web en **Basculement de la console.**  Les **méthodes de l'utilitaire** console vous rendent facile d'accéder à la page web actuelle et de la manipuler.  Pour plus d'informations, accédez à [la référence de l'API des utilitaires de console.][DevtoolsConsoleUtilities]  Par exemple, pour ajouter une bordure verte autour de tous les liens de la page web actuelle, complétez les actions suivantes.  

1.  Ouvrez la **console.**  
1.  Copiez et collez l'extrait de code suivant.  
    
    ```javascript
    $$('a').forEach(a => a.style.border='1px solid lime');
    ```  
    

:::image type="complex" source="../media/console-intro-changing-styles.msft.png" alt-text="Manipuler une sélection d'éléments à l'aide de la console" lightbox="../media/console-intro-changing-styles.msft.png":::
    Manipuler une sélection d'éléments à l'aide de la **console**  
:::image-end:::  

Pour plus d'informations sur l'utilisation du DOM, accédez à [Utiliser la console pour interagir avec le DOM.][DevtoolsConsoleConsoleDomInteraction]  

## <a name="learn-more-about-console"></a>En savoir plus sur console  

Pour plus d'informations sur la **console,** accédez à la référence de [console,][DevtoolsConsoleReference]à la référence d'API des utilitaires de [console][DevtoolsConsoleUtilities]et à la référence de [l'API de console.][DevtoolsConsoleApi]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

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
