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
# <a name="log-messages-in-the-console-tool"></a><span data-ttu-id="756a7-104">Journal des messages dans l’outil Console</span><span class="sxs-lookup"><span data-stu-id="756a7-104">Log messages in the Console tool</span></span>  

<span data-ttu-id="756a7-105">Depuis que les navigateurs ont commencé à proposer des outils de développement, **la console** est un favori.</span><span class="sxs-lookup"><span data-stu-id="756a7-105">Ever since browsers started to offer developer tools, the **Console** is a favorite.</span></span>  <span data-ttu-id="756a7-106">La raison est simple.</span><span class="sxs-lookup"><span data-stu-id="756a7-106">The reason is simple.</span></span>  

*   <span data-ttu-id="756a7-107">Dans la plupart des cours de programmation, vous apprenez à obtenir un type de commande d’impression pour obtenir des informations sur ce qui se produit.</span><span class="sxs-lookup"><span data-stu-id="756a7-107">In most programming courses, you learn to output some kind of print command to gain insights about what happens.</span></span>  

<span data-ttu-id="756a7-108">Avant DevTools, vous étiez limité à une instruction ou à `alert()` un débogage dans le `document.write()` navigateur.</span><span class="sxs-lookup"><span data-stu-id="756a7-108">Before the DevTools, you were limited to an `alert()` or `document.write()` statement to debug in the browser.</span></span>  

<span data-ttu-id="756a7-109">Si vous souhaitez enregistrer des informations dans la **console,** de nombreuses méthodes sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="756a7-109">If you want to log information in the **Console**, lots of methods are available to you.</span></span>  <span data-ttu-id="756a7-110">Examinez toutes les méthodes disponibles dans la référence [d’API.][DevtoolsConsoleApi]</span><span class="sxs-lookup"><span data-stu-id="756a7-110">Review all of available methods in the [API reference][DevtoolsConsoleApi].</span></span>  <span data-ttu-id="756a7-111">L’extrait de code suivant répertorie les méthodes les plus importantes.</span><span class="sxs-lookup"><span data-stu-id="756a7-111">The following code snippet lists the most important methods.</span></span>  

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

<span data-ttu-id="756a7-112">Copiez et collez l’extrait de code précédent dans la **console** ou accédez à des exemples de messages de console : [journal, informations, erreur et avertissement.][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingExamplesHtml]</span><span class="sxs-lookup"><span data-stu-id="756a7-112">Copy and paste the previous code snippet in the **Console** or navigate to [Console messages examples: log, info, error, and warn][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingExamplesHtml].</span></span>  <span data-ttu-id="756a7-113">Lorsque vous essayez une méthode dans la **console,** les méthodes et les méthodes semblent faire la même chose, tandis que les méthodes et les méthodes affichent une icône à côté du message et un moyen d’inspecter la trace de pile du `log()` `info()` `error()` `warn()` message. [][WikiStackTrace]</span><span class="sxs-lookup"><span data-stu-id="756a7-113">When you try any method in the **Console**, the `log()` and `info()` methods seem to do the same thing, while the `error()` and `warn()` methods display an icon next to the message and a way to inspect the [stack trace][WikiStackTrace] of the message.</span></span>  

:::image type="complex" source="../media/console-log-examples.msft.png" alt-text="La console affiche les messages provenant de différentes API de journal" lightbox="../media/console-log-examples.msft.png":::
   <span data-ttu-id="756a7-115">La **console affiche** les messages provenant de différentes API de journal</span><span class="sxs-lookup"><span data-stu-id="756a7-115">The **Console** displays the messages from different log APIs</span></span>  
:::image-end:::  

<span data-ttu-id="756a7-116">Toutefois, il est toujours bon d’utiliser et de réaliser différentes tâches de journal, car cela vous permet de filtrer à l’aide du `info()` `log()` type dans la [console.][DevtoolsConsoleConsoleFilters]</span><span class="sxs-lookup"><span data-stu-id="756a7-116">It is, however, still a good idea to use `info()` and `log()` for different log tasks as that allows you to [filter using type in the Console][DevtoolsConsoleConsoleFilters].</span></span>  

## <a name="different-types-of-logs"></a><span data-ttu-id="756a7-117">Différents types de journaux</span><span class="sxs-lookup"><span data-stu-id="756a7-117">Different types of logs</span></span>  

<span data-ttu-id="756a7-118">Au lieu de lire le texte du journal, vous pouvez envoyer des références JavaScript ou DOM valides à la **console.**</span><span class="sxs-lookup"><span data-stu-id="756a7-118">Instead of log text you may send any valid JavaScript or DOM references to the **Console**.</span></span>  <span data-ttu-id="756a7-119">La **console** est élégante et détermine le type que vous envoyez.</span><span class="sxs-lookup"><span data-stu-id="756a7-119">The **Console** is elegant and it determines the type that you send it.</span></span>  <span data-ttu-id="756a7-120">Il vous offre ensuite la meilleure représentation possible.</span><span class="sxs-lookup"><span data-stu-id="756a7-120">It then gives you the best possible representation.</span></span>  <span data-ttu-id="756a7-121">Copiez et collez l’extrait de code suivant dans la **console** ou pour afficher les résultats, accédez à [des exemples de messages][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingTypesHtml]de console : journalisation de différents types .</span><span class="sxs-lookup"><span data-stu-id="756a7-121">Copy and paste the following code snippet in the **Console** or to display the results, navigate to [Console messages examples: logging different types][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingTypesHtml].</span></span>  

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

<span data-ttu-id="756a7-122">Chaque résultat s’affiche d’une manière différente.</span><span class="sxs-lookup"><span data-stu-id="756a7-122">Each result is displayed in a different way.</span></span>  <span data-ttu-id="756a7-123">Utilisez les triangles pour faire bascule les informations et analyser chacune d’elles de plus en plus en détail.</span><span class="sxs-lookup"><span data-stu-id="756a7-123">Use the triangles to toggle the information and analyze each one in more detail.</span></span>  <span data-ttu-id="756a7-124">Les accolades autour de la variable sont une bonne petite astuce pour éviter un grand nombre de messages de journal où vous obtenez uniquement une valeur, mais vous ne savez pas `{}` `x` d’où elle provient.</span><span class="sxs-lookup"><span data-stu-id="756a7-124">The curly brace characters `{}` around the `x` variable are a nice little trick to avoid lots of log messages where you only get a value but you don't know where it originated.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-types.msft.png" alt-text="Journal des variables de différents types dans la console" lightbox="../media/console-log-types.msft.png":::
         <span data-ttu-id="756a7-126">Journal des variables de différents types dans la **console**</span><span class="sxs-lookup"><span data-stu-id="756a7-126">Log variables of different types in the **Console**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-types-expanded.msft.png" alt-text="Journal des variables de différents types dans la console avec des informations supplémentaires étendues" lightbox="../media/console-log-types-expanded.msft.png":::
         <span data-ttu-id="756a7-128">Journal des variables de différents types dans la **console** avec des informations supplémentaires étendues</span><span class="sxs-lookup"><span data-stu-id="756a7-128">Log variables of different types in the **Console** with expanded extra information</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="format-and-convert-values-with-specifiers"></a><span data-ttu-id="756a7-129">Formater et convertir des valeurs avec des spécifiés</span><span class="sxs-lookup"><span data-stu-id="756a7-129">Format and convert values with specifiers</span></span>

<span data-ttu-id="756a7-130">Une fonctionnalité spéciale de toutes les méthodes de journal est que vous pouvez utiliser des spécifiés dans votre message journal.</span><span class="sxs-lookup"><span data-stu-id="756a7-130">A special feature of all the log methods is that you may use specifiers in your log message.</span></span>  <span data-ttu-id="756a7-131">Les spécifiés font partie d’un message de journal et commencent par un signe pourcentage \( \) et vous permettent de enregistrer certaines valeurs dans différents formats et même de les `%` convertir.</span><span class="sxs-lookup"><span data-stu-id="756a7-131">Specifiers are part of a log message and start with a percentage sign \(`%`\) character and allow you to log certain values in different formats and even convert each.</span></span>  

*   `%s` <span data-ttu-id="756a7-132">journaux en tant que chaînes</span><span class="sxs-lookup"><span data-stu-id="756a7-132">logs as Strings</span></span>
*   `%i` <span data-ttu-id="756a7-133">ou `%d` se connecte en tant qu’integers</span><span class="sxs-lookup"><span data-stu-id="756a7-133">or `%d` logs as Integers</span></span>
*   `%f` <span data-ttu-id="756a7-134">logs as a floating-point value</span><span class="sxs-lookup"><span data-stu-id="756a7-134">logs as a floating-point value</span></span>
*   `%o` <span data-ttu-id="756a7-135">journaux en tant qu’élément DOM expandable</span><span class="sxs-lookup"><span data-stu-id="756a7-135">logs as an expandable DOM element</span></span>
*   `%O` <span data-ttu-id="756a7-136">logs as an expandable JavaScript object</span><span class="sxs-lookup"><span data-stu-id="756a7-136">logs as an expandable JavaScript object</span></span>
*   `%c` <span data-ttu-id="756a7-137">vous permet de donner un style à votre message avec CSS</span><span class="sxs-lookup"><span data-stu-id="756a7-137">allows you to style you message with CSS</span></span>

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

<span data-ttu-id="756a7-138">Le premier exemple montre que l’ordre de remplacement des spécifiés est l’ordre des paramètres qui suit la chaîne.</span><span class="sxs-lookup"><span data-stu-id="756a7-138">The first example displays that the order of replacement of specifiers is the parameter order following the string.</span></span>  <span data-ttu-id="756a7-139">Pour afficher les résultats, copiez et collez l’extrait de code précédent dans la **console** ou accédez à [des exemples de messages][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithSpecifiersHtml]de console : Journalisation avec des spécifiés .</span><span class="sxs-lookup"><span data-stu-id="756a7-139">To display the results, copy and paste the previous code snippet in the **Console** or navigate to [Console messages examples: Logging with specifiers][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithSpecifiersHtml].</span></span>  <span data-ttu-id="756a7-140">Développez les informations dans le journal pour afficher la différence considérable entre `%o` et `%O` .</span><span class="sxs-lookup"><span data-stu-id="756a7-140">Expand the information in the log to display the huge difference between `%o` and `%O`.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-specifiers.msft.png" alt-text="Utiliser des spécifiés pour enregistrer et convertir des valeurs" lightbox="../media/console-log-specifiers.msft.png":::
         <span data-ttu-id="756a7-142">Utiliser des spécifiés pour enregistrer et convertir des valeurs</span><span class="sxs-lookup"><span data-stu-id="756a7-142">Use specifiers to log and convert values</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-specifiers-expanded.msft.png" alt-text="Développer les résultats affiche la différence entre le %O et %o specifier : le corps est affiché sous la forme d’un nœud DOM expandable ou sous la forme d’une liste complète de toutes les propriétés JavaScript sur le corps de la page web" lightbox="../media/console-log-specifiers-expanded.msft.png":::
        <span data-ttu-id="756a7-144">Développer les résultats affiche la différence entre le spécifié et le spécifié : le corps est affiché sous forme de nœud DOM expandable ou sous la forme d’une liste complète de toutes les propriétés JavaScript sur le corps de la `%O` `%o` page web</span><span class="sxs-lookup"><span data-stu-id="756a7-144">Expand the results displays the difference between the `%O` and `%o` specifier - the body is either displayed as an expandable DOM node or as a full list of all JavaScript properties on the webpage body</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="group-log-messages"></a><span data-ttu-id="756a7-145">Messages du journal de groupe</span><span class="sxs-lookup"><span data-stu-id="756a7-145">Group log messages</span></span>

<span data-ttu-id="756a7-146">Si vous enregistrez beaucoup d’informations, vous pouvez utiliser les méthodes et les méthodes pour afficher les messages journaux en tant que groupes ex `group` `groupCollapsed` expandables et réductibles dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="756a7-146">If you log much information, you may use the `group` and `groupCollapsed` methods to display log messages as expandable and collapsible groups in the **Console**.</span></span>  <span data-ttu-id="756a7-147">Les groupes peuvent être imbrmbrés et nommés pour faciliter la compréhension des données.</span><span class="sxs-lookup"><span data-stu-id="756a7-147">Groups may be nested and named to make the data much easier to understand.</span></span>  

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

<span data-ttu-id="756a7-148">Dans le deuxième exemple, les noms de groupe peuvent également être générés.</span><span class="sxs-lookup"><span data-stu-id="756a7-148">Also in the second example, the group names may be optionally generated.</span></span>  <span data-ttu-id="756a7-149">Pour afficher les résultats, copiez et collez l’extrait de code précédent dans la **console** ou accédez à des exemples de messages de console : regroupement [des journaux.][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithGroupsHtml]</span><span class="sxs-lookup"><span data-stu-id="756a7-149">To display the results, copy and paste the previous code snippet in the **Console** or navigate to [Console messages examples: grouping logs][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithGroupsHtml].</span></span>  <span data-ttu-id="756a7-150">Vous pouvez développer et réduire chacune des sections.</span><span class="sxs-lookup"><span data-stu-id="756a7-150">You may expand and collapse each of the sections.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-groups.msft.png" alt-text="Enregistrer un grand nombre de valeurs en tant que groupes" lightbox="../media/console-log-groups.msft.png":::
         <span data-ttu-id="756a7-152">Enregistrer un grand nombre de valeurs en tant que groupes</span><span class="sxs-lookup"><span data-stu-id="756a7-152">Log lots of values as groups</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-groups-expanded.msft.png" alt-text="Chaque groupe peut être développé et réduire" lightbox="../media/console-log-groups-expanded.msft.png":::
        <span data-ttu-id="756a7-154">Chaque groupe peut être développé et réduire</span><span class="sxs-lookup"><span data-stu-id="756a7-154">Each group may be expanded and collapsed</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="display-complex-data-as-tables"></a><span data-ttu-id="756a7-155">Afficher des données complexes en tant que tableaux</span><span class="sxs-lookup"><span data-stu-id="756a7-155">Display complex data as tables</span></span>  

<span data-ttu-id="756a7-156">La méthode enregistre les données complexes non pas en tant qu’objet réductible et ex expandable, mais en tant que tableau que vous pouvez trier à l’aide `console.table()` d’en-têtes différents.</span><span class="sxs-lookup"><span data-stu-id="756a7-156">The `console.table()` method logs complex data not as a collapsible and expandable object, but as a table that you may sort using different headers.</span></span>  <span data-ttu-id="756a7-157">Un tableau trié permet aux personnes de passer en revue les informations beaucoup plus facilement.</span><span class="sxs-lookup"><span data-stu-id="756a7-157">A sorted table makes it much easier for people to review the information.</span></span>  <span data-ttu-id="756a7-158">Pour l’afficher dans un exemple, accédez à des [exemples de messages de console : Utilisation du tableau][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithTableHtml].</span><span class="sxs-lookup"><span data-stu-id="756a7-158">To display it in an example, navigate to [Console messages examples: Using table][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithTableHtml].</span></span>

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
   <span data-ttu-id="756a7-160">Afficher des données `console.table` pour faciliter la lecture</span><span class="sxs-lookup"><span data-stu-id="756a7-160">Display data with `console.table` to make it much easier to read</span></span>
:::image-end:::  

<span data-ttu-id="756a7-161">La sortie de la console a un format de tableau non seulement `console.table` lorsqu’elle s’affiche dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="756a7-161">The output of `console.table` has a table format not only when it displays in the **Console**.</span></span>    <span data-ttu-id="756a7-162">Par exemple, si vous copiez et collez un tableau dans Excel, Word ou tout autre produit qui prend en charge les données tabulaires, la structure reste intacte.</span><span class="sxs-lookup"><span data-stu-id="756a7-162">For example, if you copy and paste a table into Excel, Word, or any other product that supports tabular data, the structure remains intact.</span></span>  

<!--  The output of `console.table` has a table format not only when it displays in the **Console**.  For example, copy and paste a table in Excel, Word, or any other products that support tabular data.  -->  

<span data-ttu-id="756a7-163">Si les données ont des paramètres nommés, la méthode vous permet également de spécifier un nombre de colonnes pour chaque propriété à afficher `console.table()` en tant que deuxième `Array` paramètre.</span><span class="sxs-lookup"><span data-stu-id="756a7-163">If the data has named parameters, the `console.table()` method also allows you to specify an `Array` of columns for each property to display as a second parameter.</span></span>  <span data-ttu-id="756a7-164">L’exemple suivant montre comment spécifier un tableau de colonnes plus lisible.</span><span class="sxs-lookup"><span data-stu-id="756a7-164">The following example displays how to specify an array of columns that is more readable.</span></span>  

```javascript
// get all the h1, p and script elements 
let contentElements = document.querySelectorAll(':is(h1,p,script)');
// display the elements as an unfiltered table 
console.table(contentElements)
// display only relevant columns 
console.table(contentElements,['nodeName', 'innerText', 'offsetHeight'])
```  

:::image type="complex" source="../media/console-log-table-filtered.msft.png" alt-text="Filtrer les informations affichées par console.table et fournir un tableau de propriétés à afficher en tant que deuxième paramètre" lightbox="../media/console-log-table-filtered.msft.png":::
   <span data-ttu-id="756a7-166">Filtrer les informations `console.table` qui affichent et fournissent un tableau de propriétés à afficher en tant que deuxième paramètre</span><span class="sxs-lookup"><span data-stu-id="756a7-166">Filter information that `console.table` displays and provide an array of properties to display as a second parameter</span></span>  
:::image-end:::  

<span data-ttu-id="756a7-167">Vous pouvez être tenté d’utiliser les méthodes de journal comme principal moyen de déboguer les pages web, car les méthodes de journal sont simples à utiliser.</span><span class="sxs-lookup"><span data-stu-id="756a7-167">You may be tempted to use the log methods as your main means to debug webpages, because log methods are simple to use.</span></span>  <span data-ttu-id="756a7-168">Prenez en compte le résultat d’une `console.log()` demande.</span><span class="sxs-lookup"><span data-stu-id="756a7-168">Consider the result of any `console.log()` request.</span></span>  <span data-ttu-id="756a7-169">Les produits Live ne doivent pas utiliser de journal utilisé pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="756a7-169">Live products shouldn't use any log that was used to debug.</span></span>  <span data-ttu-id="756a7-170">Il peut révéler à l’intérieur des informations aux personnes.</span><span class="sxs-lookup"><span data-stu-id="756a7-170">It may reveal inside information to people.</span></span>  <span data-ttu-id="756a7-171">Et le bruit créé dans la **console** est écrasant.</span><span class="sxs-lookup"><span data-stu-id="756a7-171">And the noise created in the **Console** is overwhelming.</span></span>  <span data-ttu-id="756a7-172">Lorsque vous utilisez [le débogage][DevtoolsJavascriptBreakpoints] de points d’arrêt ou des [expressions][DevtoolsConsoleLiveExpressions]live, il se peut que vous trouviez que vos flux de travail sont plus efficaces et que vous obtenez de meilleurs résultats.</span><span class="sxs-lookup"><span data-stu-id="756a7-172">When you use [Breakpoint Debugging][DevtoolsJavascriptBreakpoints] or [Live Expressions][DevtoolsConsoleLiveExpressions], you may find that your workflows are more effective and you get better results.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="756a7-173">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="756a7-173">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
