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





# Présentation de la console   

  

Cette page décrit la façon dont la console Microsoft Edge DevTools simplifie le développement de pages Web.  La console a 2 utilisations principales: [afficher les messages enregistrés](#viewing-logged-messages) et [exécuter JavaScript](#running-javascript).  

## Affichage des messages enregistrés   

Les développeurs Web enregistrent souvent les messages sur la console pour s’assurer que leur JavaScript fonctionne comme prévu.  Pour enregistrer un message, vous devez insérer une expression telle que `console.log('Hello, Console!')` dans votre code JavaScript.  Lorsque le navigateur exécute votre JavaScript et voit une expression semblable à celle-ci, il enregistre le message sur la console.  Par exemple, supposons que vous écriviez le code HTML et JavaScript pour une page:  

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

La [figure 1](#figure-1) montre à quoi ressemble la console après le chargement de la page et l’attente de 3 secondes.  Essayez de déterminer les lignes de code ayant entraîné l’affichage du journal dans le navigateur.  

> ##### Figure1  
> Panneau de la console  
> ![Panneau de la console][ImageConsole]  

Les développeurs Web consignent les messages pour 2 raisons générales:  

*   Vérifier que le code s’exécute dans l’ordre approprié.  
*   Inspecter les valeurs des variables à un moment donné.  

Pour en savoir plus sur la journalisation, voir [utiliser les messages de journalisation][DevtoolsConsoleLoggingMessages] .  Pour consulter la liste complète des méthodes, voir la référence de l’API de la [console][DevToolsConsoleAPI] `console` .  La principale différence entre les méthodes est le mode d’affichage des données qui sont enregistrées.  

## Exécution de JavaScript   

La console est également une [REPL][WikiREPLoop].  Vous pouvez exécuter JavaScript dans la console pour interagir avec la page inspectée.  Par exemple, la [figure 2](#figure-2) montre la console en regard de la page d’accueil de devtools et la [figure 3](#figure-3) qui s’affiche après l’utilisation de la console pour modifier le titre supérieur de la page.  

> ##### Figure 2  
> Panneau console en regard de la page d’accueil de DevTools  
> ![Panneau console en regard de la page d’accueil de DevTools][ImageConsoleOverview]  

> ##### Figure3  
> Utiliser la console pour modifier le titre supérieur de la page  
> ![Utiliser la console pour modifier le titre supérieur de la page][ImageConsoleChangeTitle]  

La modification de la page à partir de la console est possible, car la console dispose d’un accès complet à la [fenêtre][MDNWindow] de la page.  DevTools offre quelques fonctions de commodité qui vous permettent d’inspecter une page plus facilement.  Par exemple, supposons que votre JavaScript contienne une fonction appelée `hideModal` .  L’exécution `debug(hideModal)` interrompt votre code sur la première ligne `hideModal` la prochaine fois que vous l’exécutez.  Pour en savoir plus sur la liste complète des fonctions utilitaires, voir référence sur l’API de la [console][DevtoolsConsoleUtilitiesDebug] .  

Lorsque vous exécutez JavaScript, vous n’avez pas besoin d’interagir avec la page.  Vous pouvez utiliser la console pour essayer le nouveau code non lié à la page.  Par exemple, supposons que vous viens d’apprendre sur la méthode intégrée de mappage de tableau JavaScript [()][MDNMap] et que vous souhaitez tester.  
La **console** est l’endroit idéal pour tester la fonction.  

Voir [commencer][ImageConsoleChangeTitle] à utiliser JavaScript pour bénéficier d’une expérience pratique avec l’exécution de JavaScript dans la console.  

   

  

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
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
