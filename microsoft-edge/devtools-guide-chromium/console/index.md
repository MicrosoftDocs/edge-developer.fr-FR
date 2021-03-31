---
description: Les principales utilisations de la console Microsoft Edge DevTools sont la journalisation des messages et l’exécution de JavaScript.
title: Présentation de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 496caa4d304d9511d4b1c341846f377899ba4597
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399119"
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

# <a name="console-overview"></a><span data-ttu-id="db490-104">Présentation de la console</span><span class="sxs-lookup"><span data-stu-id="db490-104">Console overview</span></span>  

  

<span data-ttu-id="db490-105">Cette page explique comment la console Microsoft Edge DevTools facilite le développement de pages web.</span><span class="sxs-lookup"><span data-stu-id="db490-105">This page explains how the Microsoft Edge DevTools Console makes it easier to develop web pages.</span></span>  <span data-ttu-id="db490-106">La **console a** 2 utilisations principales : l’affichage des messages [enregistrés](#viewing-logged-messages) et [l’exécution de JavaScript](#running-javascript).</span><span class="sxs-lookup"><span data-stu-id="db490-106">The **Console** has 2 main uses: [viewing logged messages](#viewing-logged-messages) and [running JavaScript](#running-javascript).</span></span>  

## <a name="viewing-logged-messages"></a><span data-ttu-id="db490-107">Affichage des messages enregistrés</span><span class="sxs-lookup"><span data-stu-id="db490-107">Viewing logged messages</span></span>  

<span data-ttu-id="db490-108">Les développeurs web enregistrent souvent des messages dans la console pour s’assurer que leur JavaScript fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="db490-108">Web developers often log messages to the Console to make sure that their JavaScript is working as expected.</span></span>  <span data-ttu-id="db490-109">Pour enregistrer un message, vous insérez une expression comme `console.log('Hello, Console!')` dans votre JavaScript.</span><span class="sxs-lookup"><span data-stu-id="db490-109">To log a message, you insert an expression like `console.log('Hello, Console!')` into your JavaScript.</span></span>  <span data-ttu-id="db490-110">Lorsque le navigateur exécute votre JavaScript et traite une expression comme celle-ci, le navigateur enregistre le message dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="db490-110">When the browser runs your JavaScript and processes an expression like it, the browser logs the message to the **Console**.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="db490-111">Code HTML et JavaScript pour la page.</span><span class="sxs-lookup"><span data-stu-id="db490-111">The HTML and JavaScript for the page.</span></span>  
      
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
                      { first: 'René', last: 'Magritte' },
                      { first: 'Chaim', last: 'Soutine' },
                        
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
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="db490-112">Dans la figure suivante, la **console affiche** les résultats du chargement de la page et de l’attente de 3 secondes.</span><span class="sxs-lookup"><span data-stu-id="db490-112">In the following figure, the **Console** displays the results of loading the page and waiting 3 seconds.</span></span>  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="Panneau console" lightbox="../media/console-console-demo.msft.png":::
         <span data-ttu-id="db490-114">**L’outil Console**</span><span class="sxs-lookup"><span data-stu-id="db490-114">The **Console** tool</span></span>  
      :::image-end:::  
      
      <span data-ttu-id="db490-115">Essayez de déterminer les lignes de code à l’origine du journal des messages par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="db490-115">Try to determine which lines of code caused the browser to log the messages.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="db490-116">Les développeurs web enregistrent les messages pour les 2 raisons générales suivantes.</span><span class="sxs-lookup"><span data-stu-id="db490-116">Web developers log messages for the following 2 general reasons.</span></span>  

*   <span data-ttu-id="db490-117">Assurez-vous que le code s’exécute dans le bon ordre.</span><span class="sxs-lookup"><span data-stu-id="db490-117">Making sure that code is running in the right order.</span></span>  
*   <span data-ttu-id="db490-118">Inspection des valeurs des variables à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="db490-118">Inspecting the values of variables at a certain moment in time.</span></span>  

<span data-ttu-id="db490-119">Pour obtenir une expérience pratique de la journalisation, accédez à [Démarrer avec la journalisation des messages.][DevtoolsConsoleLoggingMessages]</span><span class="sxs-lookup"><span data-stu-id="db490-119">To get hands-on experience with logging, navigate to [Get Started With Logging Messages][DevtoolsConsoleLoggingMessages].</span></span>  <span data-ttu-id="db490-120">Pour parcourir la liste complète des `console` méthodes, accédez à la référence de [l’API console.][DevToolsConsoleAPI]</span><span class="sxs-lookup"><span data-stu-id="db490-120">To browse the full list of `console` methods, navigate to the [Console API Reference][DevToolsConsoleAPI].</span></span>  <span data-ttu-id="db490-121">La principale différence entre les méthodes est la façon dont les données enregistrées sont affichées.</span><span class="sxs-lookup"><span data-stu-id="db490-121">The main difference between the methods is how the data being logged is displayed.</span></span>  

## <a name="running-javascript"></a><span data-ttu-id="db490-122">Exécution de JavaScript</span><span class="sxs-lookup"><span data-stu-id="db490-122">Running JavaScript</span></span>  

<span data-ttu-id="db490-123">La **console** est également un [rePL][WikiREPLoop].</span><span class="sxs-lookup"><span data-stu-id="db490-123">The **Console** is also a [REPL][WikiREPLoop].</span></span>  <span data-ttu-id="db490-124">Vous pouvez exécuter JavaScript dans la **console pour** interagir avec la page en cours d’inspection.</span><span class="sxs-lookup"><span data-stu-id="db490-124">You may run JavaScript in the **Console** to interact with the page being inspected.</span></span>   

:::row:::
   :::column span="":::
      <span data-ttu-id="db490-125">Dans la figure suivante, la **console est** affichée à côté de la page d’accueil de DevTools.</span><span class="sxs-lookup"><span data-stu-id="db490-125">In the following figure, the **Console** is shown next to the DevTools homepage.</span></span>  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="Outil console en de côté de la page d’accueil de DevTools" lightbox="../media/devtools-console-empty.msft.png":::
         <span data-ttu-id="db490-127">**L’outil Console** en de côté de la page d’accueil de DevTools</span><span class="sxs-lookup"><span data-stu-id="db490-127">The **Console** tool next to the DevTools homepage</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="db490-128">Dans la figure suivante, la même page s’affiche après avoir utilisé la **console** pour modifier le titre supérieur de la page.</span><span class="sxs-lookup"><span data-stu-id="db490-128">In the following figure, the same page is shown after using the **Console** to change the top heading of the page.</span></span>
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Utiliser la console pour modifier l’en-tête supérieur de la page" lightbox="../media/devtools-console-h1-changed.msft.png":::
         <span data-ttu-id="db490-130">Utiliser la **console pour** modifier l’en-tête supérieur de la page</span><span class="sxs-lookup"><span data-stu-id="db490-130">Use the **Console** to change the top heading of the page</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="db490-131">La modification de la page à partir de la **console** est possible, car la **console** dispose d’un accès complet à [la fenêtre][MDNWindow] de la page.</span><span class="sxs-lookup"><span data-stu-id="db490-131">Modifying the page from the **Console** is possible because the **Console** has full access to the [window][MDNWindow] of the page.</span></span>  <span data-ttu-id="db490-132">DevTools a quelques fonctions pratiques qui facilitent l’inspection d’une page.</span><span class="sxs-lookup"><span data-stu-id="db490-132">DevTools has a few convenience functions that make it easier to inspect a page.</span></span>  <span data-ttu-id="db490-133">Par exemple, supposons que votre JavaScript contient une fonction appelée `hideModal` .</span><span class="sxs-lookup"><span data-stu-id="db490-133">For example, suppose that your JavaScript contains a function called `hideModal`.</span></span>  <span data-ttu-id="db490-134">`debug(hideModal)`L’exécution interrompt votre code sur la première ligne `hideModal` de la prochaine exécution.</span><span class="sxs-lookup"><span data-stu-id="db490-134">Running `debug(hideModal)` pauses your code on the first line of `hideModal` the next time that you run it.</span></span>  <span data-ttu-id="db490-135">Pour plus d’informations sur la liste complète des fonctions utilitaires, accédez à référence de [l’API des utilitaires de console.][DevtoolsConsoleUtilitiesDebug]</span><span class="sxs-lookup"><span data-stu-id="db490-135">For more information about the full list of utility functions, navigate to [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug].</span></span>  

<span data-ttu-id="db490-136">Lorsque vous exécutez JavaScript, vous n’avez pas besoin d’interagir avec la page.</span><span class="sxs-lookup"><span data-stu-id="db490-136">When you run JavaScript you do not have to interact with the page.</span></span>  <span data-ttu-id="db490-137">Vous pouvez utiliser la **console pour** tester un nouveau code non lié à la page.</span><span class="sxs-lookup"><span data-stu-id="db490-137">You may use the **Console** to try out new code unrelated to the page.</span></span>  <span data-ttu-id="db490-138">Par exemple, supposons que vous venons d’apprendre la méthode intégrée de tableau JavaScript [map()][MDNMap] et que vous souhaitez l’expérimenter.</span><span class="sxs-lookup"><span data-stu-id="db490-138">For example, suppose you just learned about the built-in JavaScript Array [map()][MDNMap] method, and you want to experiment with it.</span></span>  
<span data-ttu-id="db490-139">La **console** est un bon endroit pour tester la fonction.</span><span class="sxs-lookup"><span data-stu-id="db490-139">The **Console** is a good place to try out the function.</span></span>  

<span data-ttu-id="db490-140">Pour plus d’expérience pratique avec l’exécution de JavaScript dans la **console,** accédez à Démarrer [avec l’exécution de JavaScript][DevtoolsConsoleRunningJavascript].</span><span class="sxs-lookup"><span data-stu-id="db490-140">For more hands-on experience with running JavaScript in the **Console**, navigate to [Get Started With Running JavaScript][DevtoolsConsoleRunningJavascript].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="db490-141">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="db490-141">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleAPI]: ./api.md "Console API Reference | Documents Microsoft"  
[DevtoolsConsoleLoggingMessages]: ./log.md "Commencer à journalisation des messages dans la console | Documents Microsoft"  
[DevtoolsConsoleRunningJavascript]: ./javascript.md "Commencer à utiliser JavaScript dans la console | Documents Microsoft"  
[DevtoolsConsoleUtilitiesDebug]: ./utilities.md#debug "debug - Console Utilities API Reference | Documents Microsoft"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array.prototype.map() | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Fenêtre | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Read-eval-print loop - Wikipedia"  

> [!NOTE]
> <span data-ttu-id="db490-149">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="db490-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="db490-150">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/index) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="db490-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="db490-152">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="db490-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
