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

# <a name="console-overview"></a>Présentation de la console  

  

Cette page explique comment la console Microsoft Edge DevTools facilite le développement de pages web.  La **console a** 2 utilisations principales : l’affichage des messages [enregistrés](#viewing-logged-messages) et [l’exécution de JavaScript](#running-javascript).  

## <a name="viewing-logged-messages"></a>Affichage des messages enregistrés  

Les développeurs web enregistrent souvent des messages dans la console pour s’assurer que leur JavaScript fonctionne comme prévu.  Pour enregistrer un message, vous insérez une expression comme `console.log('Hello, Console!')` dans votre JavaScript.  Lorsque le navigateur exécute votre JavaScript et traite une expression comme celle-ci, le navigateur enregistre le message dans la **console.**  

:::row:::
   :::column span="":::
      Code HTML et JavaScript pour la page.  
      
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
      Dans la figure suivante, la **console affiche** les résultats du chargement de la page et de l’attente de 3 secondes.  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="Panneau console" lightbox="../media/console-console-demo.msft.png":::
         **L’outil Console**  
      :::image-end:::  
      
      Essayez de déterminer les lignes de code à l’origine du journal des messages par le navigateur.  
   :::column-end:::
:::row-end:::  

Les développeurs web enregistrent les messages pour les 2 raisons générales suivantes.  

*   Assurez-vous que le code s’exécute dans le bon ordre.  
*   Inspection des valeurs des variables à un moment donné.  

Pour obtenir une expérience pratique de la journalisation, accédez à [Démarrer avec la journalisation des messages.][DevtoolsConsoleLoggingMessages]  Pour parcourir la liste complète des `console` méthodes, accédez à la référence de [l’API console.][DevToolsConsoleAPI]  La principale différence entre les méthodes est la façon dont les données enregistrées sont affichées.  

## <a name="running-javascript"></a>Exécution de JavaScript  

La **console** est également un [rePL][WikiREPLoop].  Vous pouvez exécuter JavaScript dans la **console pour** interagir avec la page en cours d’inspection.   

:::row:::
   :::column span="":::
      Dans la figure suivante, la **console est** affichée à côté de la page d’accueil de DevTools.  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="Outil console en de côté de la page d’accueil de DevTools" lightbox="../media/devtools-console-empty.msft.png":::
         **L’outil Console** en de côté de la page d’accueil de DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Dans la figure suivante, la même page s’affiche après avoir utilisé la **console** pour modifier le titre supérieur de la page.
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Utiliser la console pour modifier l’en-tête supérieur de la page" lightbox="../media/devtools-console-h1-changed.msft.png":::
         Utiliser la **console pour** modifier l’en-tête supérieur de la page  
      :::image-end:::  
   :::column-end:::
:::row-end:::

La modification de la page à partir de la **console** est possible, car la **console** dispose d’un accès complet à [la fenêtre][MDNWindow] de la page.  DevTools a quelques fonctions pratiques qui facilitent l’inspection d’une page.  Par exemple, supposons que votre JavaScript contient une fonction appelée `hideModal` .  `debug(hideModal)`L’exécution interrompt votre code sur la première ligne `hideModal` de la prochaine exécution.  Pour plus d’informations sur la liste complète des fonctions utilitaires, accédez à référence de [l’API des utilitaires de console.][DevtoolsConsoleUtilitiesDebug]  

Lorsque vous exécutez JavaScript, vous n’avez pas besoin d’interagir avec la page.  Vous pouvez utiliser la **console pour** tester un nouveau code non lié à la page.  Par exemple, supposons que vous venons d’apprendre la méthode intégrée de tableau JavaScript [map()][MDNMap] et que vous souhaitez l’expérimenter.  
La **console** est un bon endroit pour tester la fonction.  

Pour plus d’expérience pratique avec l’exécution de JavaScript dans la **console,** accédez à Démarrer [avec l’exécution de JavaScript][DevtoolsConsoleRunningJavascript].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

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
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/index) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
