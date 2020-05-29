---
title: Présentation de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 6062afb929a5d763c095d4915a2960993bc5ab4c
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601784"
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





# <span data-ttu-id="df526-103">Présentation de la console</span><span class="sxs-lookup"><span data-stu-id="df526-103">Console Overview</span></span>   

  

<span data-ttu-id="df526-104">Cette page décrit la façon dont la console Microsoft Edge DevTools simplifie le développement de pages Web.</span><span class="sxs-lookup"><span data-stu-id="df526-104">This page explains how the Microsoft Edge DevTools Console makes it easier to develop web pages.</span></span>  <span data-ttu-id="df526-105">La console a 2 utilisations principales: [afficher les messages enregistrés](#viewing-logged-messages) et [exécuter JavaScript](#running-javascript).</span><span class="sxs-lookup"><span data-stu-id="df526-105">The Console has 2 main uses: [viewing logged messages](#viewing-logged-messages) and [running JavaScript](#running-javascript).</span></span>  

## <span data-ttu-id="df526-106">Affichage des messages enregistrés</span><span class="sxs-lookup"><span data-stu-id="df526-106">Viewing logged messages</span></span>   

<span data-ttu-id="df526-107">Les développeurs Web enregistrent souvent les messages sur la console pour s’assurer que leur JavaScript fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="df526-107">Web developers often log messages to the Console to make sure that their JavaScript is working as expected.</span></span>  <span data-ttu-id="df526-108">Pour enregistrer un message, vous devez insérer une expression telle que `console.log('Hello, Console!')` dans votre code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="df526-108">To log a message, you insert an expression like `console.log('Hello, Console!')` into your JavaScript.</span></span>  <span data-ttu-id="df526-109">Lorsque le navigateur exécute votre JavaScript et voit une expression semblable à celle-ci, il enregistre le message sur la console.</span><span class="sxs-lookup"><span data-stu-id="df526-109">When the browser runs your JavaScript and sees an expression like that, it logs the message to the Console.</span></span>  <span data-ttu-id="df526-110">Par exemple, supposons que vous écriviez le code HTML et JavaScript pour une page:</span><span class="sxs-lookup"><span data-stu-id="df526-110">For example, suppose that you are writing the HTML and JavaScript for a page:</span></span>  

```html
<!doctype html>
<html>
  <head>
    <title>Console Demo</title>
  </head>
  <body>
    <h1>Hello, World!</h1>
    <script>
      console.log('Loading!');
      const h1 = document.querySelector('h1');
      console.log(h1.textContent);
      console.assert(document.querySelector('h2'), 'h2 not found!');
      const artists = [
        {
          first: 'René',
          last: 'Magritte'
        },
        {
          first: 'Chaim',
          last: 'Soutine'
        },
        {
          first: 'Henri',
          last: 'Matisse'
        }
      ];
      console.table(artists);
      setTimeout(() => {
        h1.textContent = 'Hello, Console!';
        console.log(h1.textContent);
      }, 3000);
    </script>
  </body>
</html>
```  

<span data-ttu-id="df526-111">La [figure 1](#figure-1) montre à quoi ressemble la console après le chargement de la page et l’attente de 3 secondes.</span><span class="sxs-lookup"><span data-stu-id="df526-111">[Figure 1](#figure-1) shows what the Console looks like after loading the page and waiting 3 seconds.</span></span>  <span data-ttu-id="df526-112">Essayez de déterminer les lignes de code ayant entraîné l’affichage du journal dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="df526-112">Try to figure out which lines of code caused the browser to log the messages.</span></span>  

> ##### <span data-ttu-id="df526-113">Figure1</span><span class="sxs-lookup"><span data-stu-id="df526-113">Figure 1</span></span>  
> <span data-ttu-id="df526-114">Panneau de la console</span><span class="sxs-lookup"><span data-stu-id="df526-114">The Console panel</span></span>  
> ![Panneau de la console][ImageConsole]  

<span data-ttu-id="df526-116">Les développeurs Web consignent les messages pour 2 raisons générales:</span><span class="sxs-lookup"><span data-stu-id="df526-116">Web developers log messages for 2 general reasons:</span></span>  

*   <span data-ttu-id="df526-117">Vérifier que le code s’exécute dans l’ordre approprié.</span><span class="sxs-lookup"><span data-stu-id="df526-117">Making sure that code is running in the right order.</span></span>  
*   <span data-ttu-id="df526-118">Inspecter les valeurs des variables à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="df526-118">Inspecting the values of variables at a certain moment in time.</span></span>  

<span data-ttu-id="df526-119">Pour en savoir plus sur la journalisation, voir [utiliser les messages de journalisation][DevtoolsConsoleLoggingMessages] .</span><span class="sxs-lookup"><span data-stu-id="df526-119">See [Get Started With Logging Messages][DevtoolsConsoleLoggingMessages] to get hands-on experience with logging.</span></span>  <span data-ttu-id="df526-120">Pour consulter la liste complète des méthodes, voir la référence de l’API de la [console][DevToolsConsoleAPI] `console` .</span><span class="sxs-lookup"><span data-stu-id="df526-120">See the [Console API Reference][DevToolsConsoleAPI] to browse the full list of `console` methods.</span></span>  <span data-ttu-id="df526-121">La principale différence entre les méthodes est le mode d’affichage des données qui sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="df526-121">The main difference between the methods is how the data being logged is displayed.</span></span>  

## <span data-ttu-id="df526-122">Exécution de JavaScript</span><span class="sxs-lookup"><span data-stu-id="df526-122">Running JavaScript</span></span>   

<span data-ttu-id="df526-123">La console est également une [REPL][WikiREPLoop].</span><span class="sxs-lookup"><span data-stu-id="df526-123">The Console is also a [REPL][WikiREPLoop].</span></span>  <span data-ttu-id="df526-124">Vous pouvez exécuter JavaScript dans la console pour interagir avec la page inspectée.</span><span class="sxs-lookup"><span data-stu-id="df526-124">You may run JavaScript in the Console to interact with the page being inspected.</span></span>  <span data-ttu-id="df526-125">Par exemple, la [figure 2](#figure-2) montre la console en regard de la page d’accueil de devtools et la [figure 3](#figure-3) qui s’affiche après l’utilisation de la console pour modifier le titre supérieur de la page.</span><span class="sxs-lookup"><span data-stu-id="df526-125">For example, [Figure 2](#figure-2) shows the Console next to the DevTools homepage, and [Figure 3](#figure-3) shows that same page after using the Console to change the top heading of the page.</span></span>  

> ##### <span data-ttu-id="df526-126">Figure 2</span><span class="sxs-lookup"><span data-stu-id="df526-126">Figure 2</span></span>  
> <span data-ttu-id="df526-127">Panneau console en regard de la page d’accueil de DevTools</span><span class="sxs-lookup"><span data-stu-id="df526-127">The Console panel next to the DevTools homepage</span></span>  
> ![Panneau console en regard de la page d’accueil de DevTools][ImageConsoleOverview]  

> ##### <span data-ttu-id="df526-129">Figure3</span><span class="sxs-lookup"><span data-stu-id="df526-129">Figure 3</span></span>  
> <span data-ttu-id="df526-130">Utiliser la console pour modifier le titre supérieur de la page</span><span class="sxs-lookup"><span data-stu-id="df526-130">Using the Console to change the top heading of the page</span></span>  
> ![Utiliser la console pour modifier le titre supérieur de la page][ImageConsoleChangeTitle]  

<span data-ttu-id="df526-132">La modification de la page à partir de la console est possible, car la console dispose d’un accès complet à la [fenêtre][MDNWindow] de la page.</span><span class="sxs-lookup"><span data-stu-id="df526-132">Modifying the page from the Console is possible because the Console has full access to the [window][MDNWindow] of the page.</span></span>  <span data-ttu-id="df526-133">DevTools offre quelques fonctions de commodité qui vous permettent d’inspecter une page plus facilement.</span><span class="sxs-lookup"><span data-stu-id="df526-133">DevTools has a few convenience functions that make it easier to inspect a page.</span></span>  <span data-ttu-id="df526-134">Par exemple, supposons que votre JavaScript contienne une fonction appelée `hideModal` .</span><span class="sxs-lookup"><span data-stu-id="df526-134">For example, suppose that your JavaScript contains a function called `hideModal`.</span></span>  <span data-ttu-id="df526-135">L’exécution `debug(hideModal)` interrompt votre code sur la première ligne `hideModal` la prochaine fois que vous l’exécutez.</span><span class="sxs-lookup"><span data-stu-id="df526-135">Running `debug(hideModal)` pauses your code on the first line of `hideModal` the next time that you run it.</span></span>  <span data-ttu-id="df526-136">Pour en savoir plus sur la liste complète des fonctions utilitaires, voir référence sur l’API de la [console][DevtoolsConsoleUtilitiesDebug] .</span><span class="sxs-lookup"><span data-stu-id="df526-136">See [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug] to see the full list of utility functions.</span></span>  

<span data-ttu-id="df526-137">Lorsque vous exécutez JavaScript, vous n’avez pas besoin d’interagir avec la page.</span><span class="sxs-lookup"><span data-stu-id="df526-137">When you run JavaScript you do not have to interact with the page.</span></span>  <span data-ttu-id="df526-138">Vous pouvez utiliser la console pour essayer le nouveau code non lié à la page.</span><span class="sxs-lookup"><span data-stu-id="df526-138">You may use the Console to try out new code unrelated to the page.</span></span>  <span data-ttu-id="df526-139">Par exemple, supposons que vous viens d’apprendre sur la méthode intégrée de mappage de tableau JavaScript [()][MDNMap] et que vous souhaitez tester.</span><span class="sxs-lookup"><span data-stu-id="df526-139">For example, suppose you just learned about the built-in JavaScript Array [map()][MDNMap] method, and you want to experiment with it.</span></span>  
<span data-ttu-id="df526-140">La **console** est l’endroit idéal pour tester la fonction.</span><span class="sxs-lookup"><span data-stu-id="df526-140">The **Console** is a good place to try out the function.</span></span>  

<span data-ttu-id="df526-141">Voir [commencer][ImageConsoleChangeTitle] à utiliser JavaScript pour bénéficier d’une expérience pratique avec l’exécution de JavaScript dans la console.</span><span class="sxs-lookup"><span data-stu-id="df526-141">See [Get Started With Running JavaScript][ImageConsoleChangeTitle] to get hands-on experience with running JavaScript in the Console.</span></span>  

   

  

<!-- image links -->  

[ImageConsole]: /microsoft-edge/devtools-guide-chromium/media/console-console-demo.msft.png "Figure 1: panneau de la console"  
[ImageConsoleChangeTitle]: /microsoft-edge/devtools-guide-chromium/media/devtools-console-h1-changed.msft.png "Figure 3: utilisation de la console pour modifier le titre supérieur de la page"  
[ImageConsoleOverview]: /microsoft-edge/devtools-guide-chromium/media/devtools-console-empty.msft.png "Figure 2: panneau de console en regard de la page d’accueil de DevTools"  

<!-- links -->  

[DevToolsConsoleAPI]: /microsoft-edge/devtools-guide-chromium/console/api "Référence sur les API de la console"  
[DevtoolsConsoleLoggingMessages]: /microsoft-edge/devtools-guide-chromium/console/log "Commencer à utiliser la journalisation des messages dans la console"  
[DevtoolsConsoleRunningJavascript]: /microsoft-edge/devtools-guide-chromium/console/javascript "Commencer à utiliser JavaScript sur la console"  
[DevtoolsConsoleUtilitiesDebug]: /microsoft-edge/devtools-guide-chromium/console/utilities#debug "XXXXXX xxx xxxxxxx xxxxxxxxx xxxxxxxxx"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array. prototype. map () | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Fenêtre | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lecture-eval-imprimer en boucle-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="df526-152">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="df526-152">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="df526-153">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="df526-153">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="df526-155">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="df526-155">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
