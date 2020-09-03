---
description: 'Les principales utilisations de la console Microsoft Edge DevTools: journalisation des messages et exécution de JavaScript.'
title: Présentation de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 0cdce953b22d22f9a2bf8048a6eff89388aa6e2e
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993155"
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





# Présentation de la console   

  

Cette page décrit la façon dont la console Microsoft Edge DevTools simplifie le développement de pages Web.  La console a 2 utilisations principales: [afficher les messages enregistrés](#viewing-logged-messages) et [exécuter JavaScript](#running-javascript).  

## Affichage des messages enregistrés   

Les développeurs Web enregistrent souvent les messages sur la console pour s’assurer que leur JavaScript fonctionne comme prévu.  Pour enregistrer un message, vous devez insérer une expression telle que `console.log('Hello, Console!')` dans votre code JavaScript.  Lorsque le navigateur exécute votre JavaScript et voit une expression semblable à celle-ci, il enregistre le message sur la console.  

:::row:::
   :::column span="":::
      HTML et JavaScript pour la page.  
      
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
                      { first: 'Henri', last: 'Matisse' }
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
      Dans l’illustration suivante, la **console** affiche les résultats du chargement de la page et l’attente de 3 secondes.  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="Panneau de la console" lightbox="../media/console-console-demo.msft.png":::
         Panneau de la **console**  
      :::image-end:::  
      
      Essayez de déterminer les lignes de code à l’origine du journal du navigateur.  
   :::column-end:::
:::row-end:::  

Les développeurs Web consignent les messages pour les 2 raisons générales suivantes.  

*   Vérifier que le code s’exécute dans l’ordre approprié.  
*   Inspecter les valeurs des variables à un moment donné.  

Pour en savoir plus sur la journalisation, voir [utiliser les messages de journalisation][DevtoolsConsoleLoggingMessages] .  Pour consulter la liste complète des méthodes, voir la référence de l’API de la [console][DevToolsConsoleAPI] `console` .  La principale différence entre les méthodes est le mode d’affichage des données qui sont enregistrées.  

## Exécution de JavaScript   

La **console** est également une [REPL][WikiREPLoop].  Vous pouvez exécuter JavaScript dans la **console** pour interagir avec la page inspectée.   

:::row:::
   :::column span="":::
      Dans l’illustration suivante, la **console** est affichée en regard de la page d’accueil devtools.  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="Panneau console en regard de la page d’accueil de DevTools" lightbox="../media/devtools-console-empty.msft.png":::
         Panneau **console** en regard de la page d’accueil de devtools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Dans l’illustration suivante, la même page s’affiche après l’utilisation de la **console** pour modifier le titre supérieur de la page.
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Utiliser la console pour modifier le titre supérieur de la page" lightbox="../media/devtools-console-h1-changed.msft.png":::
         Utiliser la **console** pour modifier le titre supérieur de la page  
      :::image-end:::  
   :::column-end:::
:::row-end:::

La modification de la page à partir de la **console** est possible, car la **console** dispose d’un accès complet à la [fenêtre][MDNWindow] de la page.  DevTools offre quelques fonctions de commodité qui vous permettent d’inspecter une page plus facilement.  Par exemple, supposons que votre JavaScript contienne une fonction appelée `hideModal` .  L’exécution `debug(hideModal)` interrompt votre code sur la première ligne `hideModal` la prochaine fois que vous l’exécutez.  Pour plus d’informations sur la liste complète des fonctions d’utilitaire, voir informations de référence sur l' [API des utilitaires de console][DevtoolsConsoleUtilitiesDebug].  

Lorsque vous exécutez JavaScript, vous n’avez pas besoin d’interagir avec la page.  Vous pouvez utiliser la **console** pour essayer le nouveau code non lié à la page.  Par exemple, supposons que vous viens d’apprendre sur la méthode intégrée de mappage de tableau JavaScript [()][MDNMap] et que vous souhaitez tester.  
La **console** est l’endroit idéal pour tester la fonction.  

Pour plus d’informations sur la façon d’utiliser JavaScript dans la **console**, voir [commencer à utiliser JavaScript][DevtoolsConsoleRunningJavascript].  

   

  

<!-- links -->  

[DevToolsConsoleAPI]: ./api.md "Référence sur les API de console | Documents Microsoft"  
[DevtoolsConsoleLoggingMessages]: ./log.md "Commencer à utiliser la journalisation des messages dans la console | Documents Microsoft"  
[DevtoolsConsoleRunningJavascript]: ./javascript.md "Commencer à utiliser JavaScript dans la console | Documents Microsoft"  
[DevtoolsConsoleUtilitiesDebug]: ./utilities.md#debug "XXXXXX xxx xxxxxxx xxx xxxxxxx xxxxx Documents Microsoft"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array. prototype. map () | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Fenêtre | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lecture-eval-imprimer en boucle-Wikipédia"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
