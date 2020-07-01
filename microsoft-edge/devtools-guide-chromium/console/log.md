---
title: Commencer à utiliser la journalisation des messages dans la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 4c930caf60af2b5e276e003378546e147c249548
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843963"
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





# Commencer à utiliser la journalisation des messages dans la console   



Ce didacticiel interactif vous montre comment consigner et filtrer des messages dans la console [Microsoft Edge devtools][MicrosoftEdgeDevTools] .  

> ##### Figure1  
> Messages dans la console  
> ![Messages dans la console][ImageLogExample]  

Ce didacticiel est destiné à être finalisé dans l’ordre.  Il part du principe que vous comprenez les principes de base du développement Web, notamment comment utiliser JavaScript pour ajouter de l’interactivité à une page.  

## Configurer la démo et DevTools   

Ce didacticiel est conçu pour que vous puissiez ouvrir la démonstration et essayer les flux de travail vous-même.  Lorsque vous effectuez une suivi physique, il est plus probable de mémoriser les flux de travail.  

1.  Maintenez `Control` la touche Windows enfoncée `Command` et cliquez sur les **exemples de journaux** de la console pour l’ouvrir dans un nouvel onglet.  
    
    [Exemples de journaux de la console][GlitchDevToolsConsoleLogExamples]
    
    <!-- > [!TIP]
    > Move the demo to a separate window.  
    > 
    > > ##### old Figure 2  
    > > The tutorial on the left, and the demo on the right  
    > > ![The tutorial on the left, and the demo on the right][ImageLogSetUp1]  -->
    
1.  Focalisez la démonstration, puis appuyez sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) pour ouvrir devtools.  Par défaut, DevTools s’ouvre à droite de la démonstration.  
    
    > ##### Figure 2  
    > DevTools s’ouvre à droite de la démonstration.  
    > ! [DevTools s’ouvre à droite de la démonstration] [ImageDevToolsRight]  
    
    > [!TIP]
    > [Ancrez devtools en bas de la fenêtre ou déverrouillez-la dans une fenêtre séparée][DevToolsCustomizePlacement].  
    
    > ##### Figure3  
    > DevTools ancré en bas de la démo  
    > ! [DevTools ancré en bas de la démonstration] [ImageDevToolsBottom]  
    
    > ##### Figure 4  
    > Navigateur dans une fenêtre séparée  
    > ! [Navigateur dans une fenêtre séparée] [ImageDevToolsSeparateBrowse]  
    
    > ##### Figure 5  
    > DevTools non ancré dans une fenêtre séparée  
    > ! [DevTools pas ancré dans une fenêtre séparée] [ImageDevToolsSeparateDevTools]  
    
## Afficher les messages enregistrés depuis JavaScript   

La plupart des messages que vous voyez dans la console proviennent des développeurs Web qui écrivent le JavaScript de la page.  L’objectif de cette section consiste à vous présenter les différents types de messages que vous risquez de voir dans la console et à expliquer la façon dont vous pouvez enregistrer chaque type de message vous-même dans JavaScript.  

1.  Cliquez sur le bouton **informations du journal** dans la démonstration.  `Hello, Console!` est connecté à la console.
    
    > ##### Figure 6  
    > La console après avoir cliqué sur **informations du journal**  
    > ! [La console après avoir cliqué sur informations du journal] [ImageLogInfo]  
    
1.  En regard du `Hello, Console!` message dans la console, cliquez sur **log.js:2**.  Le panneau sources s’ouvre et met en surbrillance la ligne de code qui a entraîné le message à se connecter à la console.  Le message a été enregistré lors de l’exécution du code JavaScript de la page `console.log('Hello, Console!')` .
    
    > ##### Figure 7  
    > DevTools ouvre le panneau sources après avoir cliqué sur **log.js:2**  
    > ! [DevTools ouvre le panneau sources après avoir cliqué sur log.js:2] [ImageSourceLog]  
    
1.  Revenez à la console à l’aide de l’un des flux de travail suivants:  
    
    *   Cliquez sur l’onglet de la **console** .  
    *   Appuyez sur `Control` + `[` \ (Windows \) ou `Command` + `[` \ (MacOS \) jusqu’à ce que le panneau de la console ait le focus.  
    *   [Ouvrez le menu de commandes][DevToolsCommandMenu], commencez à taper `Console` , sélectionnez l’option **afficher le panneau** de la console, puis appuyez sur `Enter` .  
    
1.  Cliquez sur le bouton **Avertissement du journal** dans la démonstration.  `Abandon Hope All Ye Who Enter` est connecté à la console.  Les messages mis en forme comme celui-ci sont des avertissements.  
    
    > ##### Figure8  
    > La console après avoir cliqué sur **Avertissement du journal**  
    > ! [La console après avoir cliqué sur avertissement du journal] [ImageConsoleLogWarning]  
    
    > [!TIP]
    > Si vous souhaitez voir le code ayant entraîné l’enregistrement d’un message d’une certaine façon, cliquez sur un script (par exemple, `log.js:12` \) pour afficher le code ayant entraîné la mise en forme du message.  

1.  Cliquez sur **l'** ![ icône développer ][ImageExpandIcon] `Abandon Hope All Ye Who Enter` .  DevTools affiche la [trace de pile][WikiStackTrace] qui se trouve au début de l’appel.  
    
    > ##### Figure9  
    > Une trace de pile  
    > ! [Une trace de pile] [ImageStackTrace]  
    
    La trace de pile vous indique qu’une fonction nommée `logWarning` a été appelée, qui à son tour appelait une fonction nommée `quoteDante` .  En d’autres termes, l’appel qui s’est produit en premier est en bas de la trace de pile.  Vous pouvez enregistrer des traces de pile à tout moment en les appelant `console.trace()` .  

1.  Cliquez sur **erreur de connexion**.  Le message d’erreur suivant s’affiche: `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    > ##### Figure10  
    > Un message d’erreur  
    > ! [Message d’erreur] [ImageLogError]  
    
1.  Cliquez sur **table du journal**.  Un tableau sur les artistes célèbres est connecté à la console.  
    
    > [!NOTE]
    > La `birthday` colonne est uniquement remplie pour une seule ligne.  Vérifiez le code pour savoir pourquoi c’est.
    
    > ##### Figure11  
    > Tableau sur la console  
    > ! [Une table dans la console] [ImageConsoleTable]  
    
1.  Cliquez sur **groupe de journaux**.  Les noms des 4 plus célèbres et des tortues sont regroupés sous l' `Adolescent Irradiated Espionage Tortoises` étiquette.  
    
    > ##### Figure12  
    > Groupe de messages dans la console  
    > ! [Groupe de messages dans la console] [ImageConsoleLogGroup]  
    
1.  Cliquez sur **journal personnalisé**.  Un message avec une bordure rouge et un arrière-plan bleu est connecté à la console.  
    
    > ##### Figure13  
    > Message avec une mise en forme personnalisée dans la console  
    > ! [Un message avec une mise en forme personnalisée dans la console] [ImageConsoleLogCustomFormatting]  
    
Le principe principal est le suivant: lorsque vous souhaitez consigner des messages dans la console à partir de votre JavaScript, vous utilisez l’une des `console` méthodes.  Chaque méthode met en forme les messages différemment.  

Il existe encore plus de méthodes que celles présentées dans cette section.  Ce didacticiel vous explique comment découvrir le reste des méthodes.  

## Afficher les messages enregistrés par le navigateur   

Le navigateur enregistre également les messages sur la console.  Cela se produit généralement lorsque la page rencontre un problème.  

1.  Cliquez sur **Cause 404**.  Le navigateur enregistre une `404` erreur réseau, car le code JavaScript de la page essayait de récupérer un fichier qui n’existe pas.  
    
    > ##### Figure14  
    > Erreur 404 dans la console  
    > ! [Erreur 404 dans la console] [ImageConsoleLogError]  
    
1.  Cliquez sur **provoquer une erreur**.  Le navigateur enregistre une incapture `TypeError` car JavaScript tente de mettre à jour un nœud DOM qui n’existe pas.  
    
    > ##### Figure15  
    > A TypeError dans la console  
    > ! [A TypeError dans la console] [ImageConsoleLogTypeError]  
    
1.  Cliquez sur la liste déroulante **niveaux du journal** et activez l’option **détaillé** s’il est désactivé.  Pour plus d’informations sur le filtrage, voir la section suivante.  Vous devez effectuer cette opération pour vérifier que le message suivant que vous enregistrez est visible.  
    **Remarque:** Si la liste déroulante niveaux par défaut est désactivée, vous devrez peut-être fermer la barre latérale. Filtrer par source de message ci-dessous pour plus d’informations sur la barre latérale de la console.
    
    > ##### Figure16  
    > Activer le niveau de journalisation **détaillé**  
    > ! [Activation du niveau de journalisation détaillé] [ImageVerboseLogLevel]  
    
1.  Cliquez sur **provoquer une violation**.  La page cesse de répondre pendant quelques secondes, puis le navigateur enregistre le message `[Violation] 'click' handler took 3000ms` sur la console.  La durée exacte est variable.  
    
    > ##### Figure17  
    > Violation dans la console  
    > ! [Violation dans la console] [ImageConsoleLogViolation]  
    
## Filtrer les messages   

Dans certaines pages, la console est inondée de messages.  DevTools offre différentes façons de filtrer les messages qui ne sont pas pertinents pour la tâche en cours.  

### Filtrer par niveau de journal   

`console`Un niveau de gravité est attribué à chaque méthode: `Verbose` , `Info` , `Warning` ou `Error` .  Par exemple, `console.log()` il s’agit d’un `Info` message de `console.error()` niveau supérieur `Error` .  

1.  Cliquez sur la liste déroulante **niveaux du journal** et désactivez **Erreurs**.  Un niveau est désactivé quand il n’y a plus de coche en regard de celui-ci.  Les `Error` messages de niveau disparaissent.  
    
    > ##### Figure 18  
    > Désactivation des `Error` messages de niveau de la console  
    > ! [Désactivation des messages de niveau erreur dans la console] [ImageConsoleDisablingLogError]  
    
1.  Cliquez de nouveau sur la liste déroulante **niveaux du journal** et activez de nouveau les **Erreurs**.  Les `Error` messages de niveau supérieur apparaissent.  

### Filtrer par texte   

Lorsque vous souhaitez uniquement afficher les messages qui incluent une chaîne exacte, tapez cette chaîne dans la zone de texte du **filtre** .  

1.  Entrez `Dave` dans la zone de texte du **filtre** .  Tous les messages n’incluant pas la chaîne `Dave` sont masqués.  Vous pouvez également voir l' `Adolescent Irradiated Espionage Tortoises` étiquette.  Il s’agit d’un bogue.  
    
    > ##### Figure 19  
    > Filtrage des messages n’incluant pas `Dave`  
    > ! [Filtrage des messages n’incluant pas Dave] [ImageLogTextFiltering]  
    
1.  Supprimer `Dave` de la zone de texte du **filtre** .  Tous les messages réapparaissent.  

### Filtrer par expression régulière   

Pour afficher tous les messages qui incluent un modèle de texte plutôt qu’une chaîne spécifique, utilisez une [expression régulière][MDNRegularExpressions].  

1.  Entrez `/^[AH]/` dans la zone de texte du **filtre** .  Tapez ce modèle dans [Regex][|::ref1::|Main] pour obtenir une explication de ce qu’il fait.  
    
    > ##### Figure 20  
    > Filtrage de tout message ne correspondant pas au modèle `/^[AH]/`  
    > ! [En filtrant les messages ne correspondant à aucun modèle] [ImageLogRegExFiltering]  
    
1.  Supprimer `/^[AH]/` de la zone de texte du **filtre** .  Tous les messages sont de nouveau visibles.  

### Filtrer par source de message   

Pour afficher uniquement les messages provenant d’une URL spécifique, utilisez la **barre latérale**.  

1.  Cliquez sur Afficher la barre latérale de la **console** ![ ][ImageShowConsoleSidebarIcon] .  
    
    > ##### Figure 21  
    > Barre latérale  
    > ! [Barre latérale] [ImageConsoleSidebar]  
    
1.  Cliquez sur **l'** ![ ][ImageExpandIcon] icône de développement située en regard du nombre de messages.  Dans la [figure 21](#figure-21), le nombre de messages est indiqué par **13 messages**.  La **barre latérale** affiche une liste des URL ayant entraîné la journalisation des messages.  Par exemple, il `log.js` a généré 11 messages.  
    
    > ##### Figure 22  
    > Affichage de la source de messages dans la barre latérale  
    > ! [Affichage de la source de messages dans la barre latérale] [ImageConsoleSidebarLogSource]  
    
### Filtrer par message utilisateur   

Auparavant, lorsque vous cliquiez sur informations sur le **Journal**, un script appelé pour `console.log('Hello, Console!')` consigner le message sur la console.  Les messages enregistrés depuis JavaScript comme celui-ci s’appelle **messages utilisateur**.  En revanche, lorsque vous avez cliqué sur **Cause 404**, le navigateur a enregistré un `Error` message de niveau indiquant que la ressource demandée est introuvable.  Les messages comme les **messages du navigateur**.  Utilisez la **barre latérale** pour filtrer les messages de navigateur et afficher uniquement les messages utilisateurs.  

1.  Cliquez sur **9 messages utilisateur**.  Les messages de navigateur sont masqués.  
    
    > ##### Figure 23  
    > Filtrage des messages de navigateur  
    > ! [Filtrage des messages de navigateur] [ImageConsoleLogBrowserFiltering]  
    
1.  Cliquez sur **13 messages** pour afficher de nouveau tous les messages.  

## Utiliser la console en même temps que d’autres panneaux   

Que se passe-t-il si vous modifiez les styles, mais vous avez besoin de consulter rapidement le journal de la console pour obtenir un élément? Utiliser le tiroir.  

1.  Cliquez sur l’onglet **éléments** .  
1.  Appuyez sur `Escape` .  L’onglet Console du **tiroir** s’ouvre.  Toutes les fonctionnalités du panneau de la console que vous avez utilisées tout au long de ce didacticiel.  
    
    > ##### Figure 24  
    > Onglet Console du tiroir  
    > ! [L’onglet Console du tiroir] [ImageDrawerConsole]  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

 



<!-- image links -->  

[ImageExpandIcon]: /microsoft-edge/devtools-guide-chromium/media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageLogExample]: /microsoft-edge/devtools-guide-chromium/media/console-ars-technica-console-onload.msft.png "Figure 1: messages de la console"  
<!--[ImageLogSetUp1]: /microsoft-edge/devtools-guide-chromium/media/log-set-up-1.msft.png "old Figure 2: The tutorial on the left, and the demo on the right"  -->  
[ImageDevToolsRight]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-example-devtools-right-console.msft.png "figure 2: DevTools s’ouvre à droite de la démonstration"  
[ImageDevToolsBottom]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-example-devtools-bottom-console.msft.png "figure 3: DevTools ancré en bas de la démonstration"  
[ImageDevToolsSeparateBrowse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-example-devtools-separate-console-browse.msft.png "figure 4: navigateur dans une fenêtre séparée"  
[ImageDevToolsSeparateDevTools]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-example-devtools-separate-console-devtools.msft.png "figure 5: DevTools non ancré dans une fenêtre séparée"  
[ImageLogInfo]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-info.msft.png "figure 6: la console après avoir cliqué sur informations du journal"  
[ImageSourceLog]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-sources-logjs.msft.png "figure 7: DevTools ouvre le panneau sources après que vous avez cliqué sur log.js:2"  
[ImageConsoleLogWarning]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-warning.msft.png "figure 8: la console après avoir cliqué sur avertissement du journal"  
[ImageStackTrace]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-warning-expanded.msft.png "figure 9: trace de pile"  
[ImageLogError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-error.msft.png "figure 10: message d’erreur"  
[ImageConsoleTable]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-table.msft.png "figure 11: une table dans la console"  
[ImageConsoleLogGroup]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-group.msft.png "figure 12: un groupe de messages dans la console"  
[ImageConsoleLogCustomFormatting]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-custom.msft.png "figure 13: message avec une mise en forme personnalisée dans la console"  
[ImageConsoleLogError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-cause-404.msft.png "figure 14: erreur 404 dans la console"  
[ImageConsoleLogTypeError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-cause-error.msft.png "figure 15: un TypeError dans la console"  
[ImageVerboseLogLevel]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-cause-error-log-levels.msft.png "figure 16: activer le niveau de journalisation détaillé"  
[ImageConsoleLogViolation]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-cause-violation.msft.png "figure 17: violation dans la console"  
[ImageConsoleDisablingLogError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-cause-violation-log-levels.msft.png "figure 18: désactivation des messages de niveau erreur dans la console"  
[ImageLogTextFiltering]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-all-messages-text-filter.msft.png "figure 19: filtrage des messages n’incluant pas Dave"  
[ImageLogRegExFiltering]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-all-messages-regex-filter.msft.png "figure 20: filtrage de tout message ne correspondant à aucun modèle"  
[ImageConsoleSidebar]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-sidebar-all-messages.msft.png "figure 21: barre latérale"  
[ImageConsoleSidebarLogSource]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-sidebar-expanded-all-messages.msft.png "figure 22: affichage de la source de messages dans la barre latérale"  
[ImageConsoleLogBrowserFiltering]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-sidebar-user-messages.msft.png "figure 23: filtrage des messages de navigateur"  
[ImageDrawerConsole]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-elements-drawer-console-sidebar-all-messages.msft.png "figure 24: onglet de console dans le tiroir"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge \ (chrome \)"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  
[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Référence sur les API de la console"  
[DevToolsConsoleReference]: /microsoft-edge/devtools-guide-chromium/console/reference "Référence de la console"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Commencer à utiliser la journalisation des messages | Problème"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expressions régulières | MDN"  

[RegExrMain]: https://regexr.com "RegEx"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Trace de pile-Wikipédia"  


> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/log) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
