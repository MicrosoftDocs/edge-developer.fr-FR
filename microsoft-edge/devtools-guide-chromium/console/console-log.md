---
description: Comment enregistrer des messages et exécuter JavaScript dans la Microsoft Edge console DevTools.
title: Journal des messages dans l’outil Console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: d48a48de7b261a628ac99f58680deb119268a980
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483418"
---
# <a name="log-messages-in-the-console-tool"></a>Journal des messages dans l’outil Console  

Depuis que les navigateurs ont commencé à proposer des outils de développement, **la console** est un favori.  La raison est simple.  

*   Dans la plupart des cours de programmation, vous apprenez à obtenir un type de commande d’impression pour obtenir des informations sur ce qui se produit.  

Avant DevTools, vous étiez limité à une instruction ou à `alert()` un débogage dans le `document.write()` navigateur.  

Si vous souhaitez enregistrer des informations dans la **console,** de nombreuses méthodes sont disponibles.  Examinez toutes les méthodes disponibles dans la référence [d’API.][DevtoolsConsoleApi]  L’extrait de code suivant répertorie les méthodes les plus importantes.  

```javascript
// prints the text to the console as  a log message
console.log('This is a log message')
// prints the text to the console as an informational message
console.info('This is some information') 
// prints the text to the console as an error message
console.error('This is an error')
// prints the text to the console as a warning
console.warn('This is a warning') 
```  

Copiez et collez l’extrait de code précédent dans la **console** ou accédez à des exemples de messages de console : [journal, informations, erreur et avertissement.][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingExamplesHtml]  Lorsque vous essayez une méthode dans la **console,** les méthodes et les méthodes semblent faire la même chose, tandis que les méthodes et les méthodes affichent une icône à côté du message et un moyen d’inspecter la trace de pile du `log()` `info()` `error()` `warn()` message. [][WikiStackTrace]  

:::image type="complex" source="../media/console-log-examples.msft.png" alt-text="La console affiche les messages provenant de différentes API de journal" lightbox="../media/console-log-examples.msft.png":::
   La **console affiche** les messages provenant de différentes API de journal  
:::image-end:::  

Toutefois, il est toujours bon d’utiliser et de réaliser différentes tâches de journal, car cela vous permet de filtrer à l’aide du `info()` `log()` type dans la [console.][DevtoolsConsoleConsoleFilters]  

## <a name="different-types-of-logs"></a>Différents types de journaux  

Au lieu de lire le texte du journal, vous pouvez envoyer des références JavaScript ou DOM valides à la **console.**  La **console** est élégante et détermine le type que vous envoyez.  Il vous offre ensuite la meilleure représentation possible.  Copiez et collez l’extrait de code suivant dans la **console** ou pour afficher les résultats, accédez à [des exemples de messages][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingTypesHtml]de console : journalisation de différents types .  

```javascript
let x = 2;
// logs the value of x
console.log(x);
// logs the name x and value of x
console.log({x})   
// logs a DOM reference  
console.log(document.querySelector('body'));
// logs an Object
console.log({"type":"life", "meaning": 42});
let w3techs = ['HTML', 'CSS', 'SVG', 'MathML'];
// logs an Array
console.log(w3techs);
```  

Chaque résultat s’affiche d’une manière différente.  Utilisez les triangles pour faire bascule les informations et analyser chacune d’elles de plus en plus en détail.  Les accolades autour de la variable sont une bonne petite astuce pour éviter un grand nombre de messages de journal où vous obtenez uniquement une valeur, mais vous ne savez pas `{}` `x` d’où elle provient.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-types.msft.png" alt-text="Journal des variables de différents types dans la console" lightbox="../media/console-log-types.msft.png":::
         Journal des variables de différents types dans la **console**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-types-expanded.msft.png" alt-text="Journal des variables de différents types dans la console avec des informations supplémentaires étendues" lightbox="../media/console-log-types-expanded.msft.png":::
         Journal des variables de différents types dans la **console** avec des informations supplémentaires étendues  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="format-and-convert-values-with-specifiers"></a>Formater et convertir des valeurs avec des spécifiés

Une fonctionnalité spéciale de toutes les méthodes de journal est que vous pouvez utiliser des spécifiés dans votre message journal.  Les spécifiés font partie d’un message de journal et commencent par un signe pourcentage \( \) et vous permettent de enregistrer certaines valeurs dans différents formats et même de les `%` convertir.  

*   `%s` journaux en tant que chaînes
*   `%i` ou `%d` se connecte en tant qu’integers
*   `%f` logs as a floating-point value
*   `%o` journaux en tant qu’élément DOM expandable
*   `%O` logs as an expandable JavaScript object
*   `%c` vous permet de donner un style à votre message avec CSS

```javascript
// logs "10x console developer"
console.log('%ix %s developer', 10, 'console');
// logs PI => 3.141592653589793
console.log(Math.PI); 
// logs PI as an integer = 3
console.log('%i', Math.PI); 
// logs the webpage body as a DOM node
console.log('%o', document.body); 
// logs the body of the webpage as a JavaScript object with all properties
console.log('%O', document.body); 
// Displays the message as red and big
console.log('%cImportant message follows','color:red;font-size:40px');
```  

Le premier exemple montre que l’ordre de remplacement des spécifiés est l’ordre des paramètres qui suit la chaîne.  Pour afficher les résultats, copiez et collez l’extrait de code précédent dans la **console** ou accédez à [des exemples de messages][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithSpecifiersHtml]de console : Journalisation avec des spécifiés .  Développez les informations dans le journal pour afficher la différence considérable entre `%o` et `%O` .  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-specifiers.msft.png" alt-text="Utiliser des spécifiés pour enregistrer et convertir des valeurs" lightbox="../media/console-log-specifiers.msft.png":::
         Utiliser des spécifiés pour enregistrer et convertir des valeurs  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-specifiers-expanded.msft.png" alt-text="Développer les résultats affiche la différence entre le %O et %o specifier : le corps est affiché sous la forme d’un nœud DOM expandable ou sous la forme d’une liste complète de toutes les propriétés JavaScript sur le corps de la page web" lightbox="../media/console-log-specifiers-expanded.msft.png":::
        Développer les résultats affiche la différence entre le spécifié et le spécifié : le corps est affiché sous forme de nœud DOM expandable ou sous la forme d’une liste complète de toutes les propriétés JavaScript sur le corps de la `%O` `%o` page web  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="group-log-messages"></a>Messages du journal de groupe

Si vous enregistrez beaucoup d’informations, vous pouvez utiliser les méthodes et les méthodes pour afficher les messages journaux en tant que groupes ex `group` `groupCollapsed` expandables et réductibles dans la **console.**  Les groupes peuvent être imbrmbrés et nommés pour faciliter la compréhension des données.  

```javascript
console.group("Passengers: Heart of Gold");
console.log('Zaphod');
console.log('Trillian');
console.log('Ford');
console.log('Arthur');
console.log('Marvin');
console.groupCollapsed("Hidden");
console.log('(Frankie & Benjy)');
console.groupEnd("Hidden");
console.groupEnd("Passengers: Heart of Gold");

let technologies = {
  "Standards": ["HTML", "CSS", "SVG", "ECMAScript"],
  "Others": ["jQuery", "Markdown", "Textile", "Sass", "Pug"]
}
for (tech in technologies) {
  console.groupCollapsed(tech);
  technologies[tech].forEach(t => console.log(t));
  console.groupEnd(tech);
}
```  

Dans le deuxième exemple, les noms de groupe peuvent également être générés.  Pour afficher les résultats, copiez et collez l’extrait de code précédent dans la **console** ou accédez à des exemples de messages de console : regroupement [des journaux.][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithGroupsHtml]  Vous pouvez développer et réduire chacune des sections.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-groups.msft.png" alt-text="Enregistrer un grand nombre de valeurs en tant que groupes" lightbox="../media/console-log-groups.msft.png":::
         Enregistrer un grand nombre de valeurs en tant que groupes  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-groups-expanded.msft.png" alt-text="Chaque groupe peut être développé et réduire" lightbox="../media/console-log-groups-expanded.msft.png":::
        Chaque groupe peut être développé et réduire  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="display-complex-data-as-tables"></a>Afficher des données complexes en tant que tableaux  

La méthode enregistre les données complexes non pas en tant qu’objet réductible et ex expandable, mais en tant que tableau que vous pouvez trier à l’aide `console.table()` d’en-têtes différents.  Un tableau trié permet aux personnes de passer en revue les informations beaucoup plus facilement.  Pour l’afficher dans un exemple, accédez à des [exemples de messages de console : Utilisation du tableau][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithTableHtml].

```javascript
let technologies = {
  "Standards": ["HTML", "CSS", "SVG", "ECMAScript"],
  "Others": ["jQuery", "Markdown", "Textile", "Sass", "Pug"]
}
// log technologies as an object
console.log(technologies);
// display technologies as a table
console.table(technologies);

// get the dimensions of the webpage body
let bodyDimensions = document.body.getBoundingClientRect();
// display dimensions as an object
console.log(bodyDimensions);
// display dimensions as a table
console.table(bodyDimensions);
```  

:::image type="complex" source="../media/console-log-table.msft.png" alt-text="Afficher des données avec console.table pour faciliter la lecture" lightbox="../media/console-log-table.msft.png":::
   Afficher des données `console.table` pour faciliter la lecture
:::image-end:::  

La sortie de la console a un format de tableau non seulement `console.table` lorsqu’elle s’affiche dans la **console.**    Par exemple, si vous copiez et collez un tableau dans Excel, Word ou tout autre produit qui prend en charge les données tabulaires, la structure reste intacte.  

<!--  The output of `console.table` has a table format not only when it displays in the **Console**.  For example, copy and paste a table in Excel, Word, or any other products that support tabular data.  -->  

Si les données ont des paramètres nommés, la méthode vous permet également de spécifier un nombre de colonnes pour chaque propriété à afficher `console.table()` en tant que deuxième `Array` paramètre.  L’exemple suivant montre comment spécifier un tableau de colonnes plus lisible.  

```javascript
// get all the h1, p and script elements 
let contentElements = document.querySelectorAll(':is(h1,p,script)');
// display the elements as an unfiltered table 
console.table(contentElements)
// display only relevant columns 
console.table(contentElements,['nodeName', 'innerText', 'offsetHeight'])
```  

:::image type="complex" source="../media/console-log-table-filtered.msft.png" alt-text="Filtrer les informations affichées par console.table et fournir un tableau de propriétés à afficher en tant que deuxième paramètre" lightbox="../media/console-log-table-filtered.msft.png":::
   Filtrer les informations `console.table` qui affichent et fournissent un tableau de propriétés à afficher en tant que deuxième paramètre  
:::image-end:::  

Vous pouvez être tenté d’utiliser les méthodes de journal comme principal moyen de déboguer les pages web, car les méthodes de journal sont simples à utiliser.  Prenez en compte le résultat d’une `console.log()` demande.  Les produits Live ne doivent pas utiliser de journal utilisé pour le débogage.  Il peut révéler à l’intérieur des informations aux personnes.  Et le bruit créé dans la **console** est écrasant.  Lorsque vous utilisez [le débogage][DevtoolsJavascriptBreakpoints] de points d’arrêt ou des [expressions][DevtoolsConsoleLiveExpressions]live, il se peut que vous trouviez que vos flux de travail sont plus efficaces et que vous obtenez de meilleurs résultats.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Référence de l’API de console | Documents Microsoft"  
[DevtoolsConsoleConsoleFilters]: ./console-filters.md "Filtrer les messages de la console | Documents Microsoft"  
[DevtoolsConsoleLiveExpressions]: ./live-expressions.md "Surveiller les modifications apportées dans JavaScript à l’aide d’expressions | Documents Microsoft"  

[DevtoolsJavascriptBreakpoints]: ../javascript/breakpoints.md "Comment suspendre votre code avec des points d’arrêt Microsoft Edge devTools | Documents Microsoft"  

[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingExamplesHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-examples.html "Exemples de messages de console : journal, informations, erreurs et avertissements | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingTypesHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-types.html "Exemples de messages de console : journalisation de différents types | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithGroupsHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-with-groups.html "Exemples de messages de console : regroupement des journaux | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithSpecifiersHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-with-specifiers.html "Exemples de messages de console : journalisation avec des | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithTableHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-with-table.html "Exemples de messages de console : utilisation du tableau | GitHub"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Stack trace | Wikipedia"  
