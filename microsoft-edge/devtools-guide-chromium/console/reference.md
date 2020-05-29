---
title: Référence de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: bd2a610b48905c6651663d490b9c9f1a0a8c7674
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601783"
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





# Référence de la console   



Cette page est une référence des fonctionnalités liées à la console Microsoft Edge DevTools.  Il part du principe que vous connaissez déjà l’utilisation de la console pour afficher les messages enregistrés et exécuter JavaScript.  Si ce n’est pas le cas, voir [prendre en main JavaScript dans la console][DevToolsConsoleJavascript] et [commencer à utiliser les messages de journalisation dans la console][DevToolsConsoleLog].  

Si vous recherchez la référence de l’API sur des fonctions telles que voir référence sur l’API de la `console.log()` [console][DevToolsConsoleApi].  Pour obtenir une référence sur les fonctions telles que `monitorEvents()` Voir la référence des API d’utilitaires de [console][DevToolsConsoleUtilities].  

## Ouvrez la console.   

Vous pouvez ouvrir la console en tant que [panneau](#open-the-console-panel) ou en tant qu' [onglet dans le tiroir](#open-the-console-tab-in-the-drawer).  

### Ouvrir l’écran de la console   

Appuyez sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).  

> ##### Figure1  
> Panneau de la console  
> ![Panneau de la console][ImageConsolePanel]  

Pour ouvrir le panneau console à partir du [menu de commandes][DevToolsCommandMenu], commencez à taper, `Console` puis exécutez la commande Afficher la **console** contenant le badge du **panneau** .  

> ##### Figure 2  
> Commande d’affichage de l’écran de la console  
> ![Commande d’affichage de l’écran de la console][ImageCommandShowConsole]  

### Ouvrir l’onglet de console dans le tiroir   

Appuyez `Escape` ou cliquez sur **personnaliser et contrôler devtools** `...` puis sélectionnez **afficher le tiroir**de la console.  

> ##### Figure3  
> Afficher le tiroir de la console  
> ![Afficher le tiroir de la console][ImageShowConsoleDrawer]  

Le tiroir apparaît en bas de la fenêtre de DevTools, avec l’onglet **console** ouvert.  

> ##### Figure 4  
> Onglet Console du tiroir  
> ![Onglet Console du tiroir][ImageDrawerConsole]  

Pour ouvrir l’onglet de la console à partir du [menu de commandes][DevToolsCommandMenu], commencez à taper, `Console` puis exécutez la commande **afficher la console** dont le badge est associé au **tiroir** .  

> ##### Figure 5  
> Commande d’affichage de l’onglet de console dans le tiroir  
> ![Commande d’affichage de l’onglet de console dans le tiroir][ImageShowDrawerCommand]  

### Ouvrir les paramètres de la console   

Cliquez sur paramètres de la console **paramètres** de la console ![ ][ImageSettingsButtonIcon] .  

> ##### Figure 6  
> Paramètres de la console  
> ![Paramètres de la console][ImageConsoleSettings]  

Les liens ci-dessous décrivent chaque paramètre:  

*   [**Masquer le réseau**](#hide-network-messages)  
*   [**Conserver le journal**](#persist-messages-across-page-loads)  
*   [**Contexte sélectionné uniquement**](#filter-out-messages-from-different-contexts)  
*   [**Groupe similaire**](#disable-message-grouping)  
*   [**Enregistrer les fichiers XmlHttpRequest**](#log-xhr-and-fetch-requests)  
*   [**Évaluation hâtif**](#disable-eager-evaluation)  
*   [**Saisie semi-automatique dans l’historique**](#disable-autocomplete-from-history)  

### Ouvrir la barre latérale de la console   

Cliquez sur **Afficher** ![ la barre latérale ][ImageShowConsoleSidebarIcon] de la console pour afficher la barre latérale, qui est utile pour le filtrage.  

> ##### Figure 7  
> Barre latérale de la console  
> ![Barre latérale de la console][ImageConsoleSidebar]  

## Afficher des messages   

Cette section contient des fonctionnalités qui changent le mode d’affichage des messages dans la console.  Pour obtenir une procédure pas à pas, voir [afficher les messages][DevToolsConsoleViewMessages] .  

### Désactiver le regroupement des messages   

[Ouvrez les paramètres](#open-console-settings) de la console et désactivez l’option groupe, de la **même façon** que le comportement de regroupement des messages par défaut de la console.  Pour obtenir un exemple [, voir journaux de XHR et récupérer des requêtes](#log-xhr-and-fetch-requests) .  

### Journalisation des requêtes XHR et FETCH   

[Ouvrez les paramètres](#open-console-settings) de la console et activez le **Journal** des utilisateurs pour enregistrer toutes les `XMLHttpRequest` `Fetch` demandes de la console en temps réel.  

> ##### Figure8  
> Journalisation `XMLHttpRequest` et `Fetch` demandes  
> ![Journalisation des requêtes XMLHttpRequest et FETCH][ImageXhrGrouped]  

Le message principal de la [figure 8](#figure-8) montre le comportement de regroupement par défaut de la console.  <!--  [Figure 9](#figure-9) shows how the same log looks after [disabling message grouping](#disable-message-grouping).  -->  

<!--

> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> ![How the logged XMLHttpRequest and Fetch requests look after ungrouping][ImageXhrUngrouped]  

-->

<!--todo: add example for ungrouping console items  -->  

### Faire persister des messages au chargement de la page   

Par défaut, la console est effacée dès que vous chargez une nouvelle page.  Pour conserver les messages au cours du chargement de la page, [cliquez sur paramètres](#open-console-settings) de la console, puis activez la case à cocher conserver le **Journal** .  

### Masquer les messages réseau   

Par défaut, le navigateur enregistre les messages réseau sur la **console**.  Par exemple, le message sélectionné dans [figure 9](#figure-9) représente un code d’état de `429` .  

> ##### Figure9  
> Message 429 dans la console  
> ! [Un message 429 dans la console] [Image429Message]  

Pour masquer les messages réseau:  

1.  [Ouvrez paramètres](#open-console-settings)de la console.  
1.  Activez la case à cocher **masquer le réseau** .  

## Filtrer les messages   

Il existe de nombreuses façons de filtrer les messages dans la console.  

### Filtrer les messages du navigateur   

[Ouvrez la barre latérale de la console](#open-the-console-sidebar) et cliquez sur **messages utilisateur** pour afficher uniquement les messages provenant du JavaScript de la page.  

> ##### Figure10  
> Affichage des messages des utilisateurs  
> ! [Affichage des messages des utilisateurs] [ImageUserMessages]  

### Filtrer par niveau de journal   

DevTools affecte chaque `console.*` méthode un niveau de gravité.  Il y a 4 niveaux: `Verbose` ,, `Info` `Warning` et `Error` .  Par exemple, `console.log()` se trouve dans le `Info` groupe, alors qu’il `console.error()` se trouve dans le `Error` groupe.  La [référence de l’API console][DevToolsConsoleApi] décrit le niveau de gravité de chaque méthode applicable.  Les messages que le navigateur enregistre sur la console ont également un niveau de gravité.  Vous pouvez masquer tous les niveaux de messages qui ne vous intéressent pas.  Par exemple, si vous êtes intéressé uniquement par les `Error` messages, vous pouvez masquer les 3 autres groupes.  

Cliquez sur la liste déroulante **niveaux du journal** pour activer ou désactiver ou `Verbose` `Info` `Warning` `Error` messages.  

> ##### Figure11  
> Liste déroulante **niveaux du journal**  
> ! [Liste déroulante des niveaux de journaux] [ImageLogLevels]  

Vous pouvez également filtrer par niveau de journal en [ouvrant la barre latérale de la console](#open-the-console-sidebar) , puis en cliquant sur **erreurs**, **avertissements**, **informations**ou **Commentaires**.  

> ##### Figure12  
> Utiliser la barre latérale pour afficher les avertissements  
> ! [Utilisation de la barre latérale pour afficher les avertissements] [ImageSidebarWarnings]  

### Filtrer les messages par URL   

Tapez `url:` suivi d’une URL pour afficher uniquement les messages provenant de cette URL.  Après que vous avez tapé `url:` devtools affiche toutes les URL pertinentes.  Les domaines fonctionnent également.  Par exemple, si `https://example.com/a.js` `https://example.com/b.js` vous consignez des messages, `url:https://example.com` vous pouvez vous concentrer sur les messages de ces deux scripts.  

> ##### Figure13  
> Filtre d’URL  
> ! [Filtre d’URL] [ImageUrlFilter]  

Entrez `-url:` pour masquer les messages de cette URL.  Ce filtre est appelé filtre d’URL négatif.  

> ##### Figure14  
> Un filtre d’URL négatif masquant tous les messages correspondant à l’URL; `https://b.wal.co`  
> ! [Filtre d’URL négatif masquant tous les messages correspondant à l’URL https://b.wal.co ] [ImageNegativeUrlFilter1]  

Vous pouvez également afficher les messages d’une URL unique en [ouvrant la barre latérale](#open-the-console-sidebar)de la console, en développant la section messages de l' **utilisateur** , puis en cliquant sur l’URL du script contenant les messages sur lesquels vous souhaitez vous concentrer.  

> ##### Figure15  
> Affichage des messages de `wp-ad.min.js`  
> ! [Affichage des messages issus de WP-ad. min. js] [ImageNegativeUrlFilter2]  

### Filtrer les messages de différents contextes   

Imaginons que vous ayez une annonce (publicité) sur votre page.  La publicité est incorporée dans un `<iframe>` et génère un grand nombre de messages dans votre console.  Dans la mesure où la publicité s’exécute dans un autre [contexte JavaScript](#select-javascript-context), une façon de masquer les messages consiste à [ouvrir les paramètres](#open-console-settings) de la console et à activer la case à cocher **contexte sélectionnée uniquement** .  

### Filtrer les messages qui ne correspondent pas à un modèle d’expression régulière   

Tapez une expression régulière telle que `/[gm][ta][mi]/` dans la zone de texte de **filtre** pour filtrer les messages ne correspondant pas à ce modèle.  DevTools vérifie si le modèle se trouve dans le texte du message ou dans le script qui a entraîné la journalisation du message.  

> ##### Figure16  
> Filtrage des messages ne correspondant pas `/[gm][ta][mi]/`  
> ! [En filtrant les messages ne correspondant pas à l’expression Regex] [ImageRegExFilter]  

## Exécuter JavaScript   

Cette section contient des fonctionnalités relatives à l’exécution de JavaScript dans la console.  Pour obtenir une procédure pas à pas, voir [exécuter JavaScript][DevToolsConsoleOverviewJavascript] .  

### Réexécuter des expressions à partir de l’historique   

Appuyez sur la `Up Arrow` touche pour parcourir l’historique des expressions JavaScript que vous avez exécutées auparavant dans la console.  Appuyez sur `Enter` pour réexécuter cette expression.  

### Regardez la valeur d’une expression en temps réel avec des expressions dynamiques   

Si vous vous intentez de taper la même expression JavaScript dans la console à plusieurs reprises, il est possible que vous puissiez constater qu’il est plus facile de créer une **expression dynamique**.  Dans les **expressions dynamiques** , vous tapez une expression une seule fois, puis épinglez celle-ci en haut de votre console.  La valeur de l’expression est mise à jour en temps réel.  Voir [valeurs d’expression JavaScript en temps réel avec des expressions dynamiques][DevToolsConsoleLiveExpressions].  

### Désactiver l’évaluation hâtif   

Lorsque vous tapez des expressions JavaScript dans la console, l' **évaluation hâtif** affiche un aperçu de la valeur de retour pour cette expression.  [Ouvrez paramètres](#open-console-settings) de la console et désactivez la case à cocher **évaluation hâtif** pour désactiver les aperçus des valeurs de retour.  

### Désactiver la saisie semi-automatique dans l’historique   

Lors de la saisie d’une expression, la fenêtre contextuelle de saisie semi-automatique de la console affiche les expressions que vous avez exécutées auparavant.  Ces expressions sont précédées du `>` caractère.  [Ouvrez paramètres](#open-console-settings) de la console et désactivez l’option **saisie semi-automatique de l’historique** pour ne plus afficher les expressions de votre historique.  

> [!NOTE]
> Dans la [figure 17](#figure-17), `document.querySelector('a')` et `document.querySelector('img')` sont des expressions évaluées auparavant.  

> ##### Figure17  
> Fenêtre contextuelle de saisie semi-automatique montrant des expressions de l’historique  
> ! [Fenêtre de saisie semi-automatique montrant des expressions de l’historique] [ImageHistoryAutocomplete]  

### Sélectionner un contexte JavaScript   

Par défaut, la liste déroulante du **contexte JavaScript** est définie sur **Top**, qui représente le [contexte de navigation][MDNBrowsingContext] du document principal.  

> ##### Figure 18  
> Liste déroulante **contextuelle JavaScript**  
> ! [Zone de liste déroulante de contexte JavaScript] [ImageJavascriptContext]  

Imaginons que vous ayez une publicité sur votre page incorporée dans une `<iframe>` .  Vous souhaitez exécuter JavaScript afin de peaufiner le DOM de la publicité.  Vous devez tout d’abord sélectionner le contexte de navigation de la publicité dans la liste déroulante **contexte JavaScript** .  

> ##### Figure 19  
> Sélection d’un autre contexte JavaScript  
> ! [Sélection d’un autre contexte JavaScript] [ImageSelectContext]  

## Effacement de la console   

Vous pouvez utiliser les flux de travail suivants pour effacer la console:  

*   Cliquez sur **Effacer** la console effacer la console ![ ][ImageClearConsoleIcon] .  
*   Cliquez avec le bouton droit sur un message, puis sélectionnez **effacer la console**.  
*   Entrez `clear()` dans la console et appuyez sur `Enter` .  
*   Appelez `console.clear()` depuis JavaScript pour votre page Web.  
*   Appuyez une fois sur `Control` + `L` le focus de la console.  

 



<!-- image links -->  

[ImageClearConsoleIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageConsolePanel]: /microsoft-edge/devtools-guide-chromium/media/console-hello-console.msft.png "Figure 1: panneau de la console"  
[ImageCommandShowConsole]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Figure 2: commande d’affichage du panneau de la console"  
[ImageShowConsoleDrawer]: /microsoft-edge/devtools-guide-chromium/media/console-elements-customize-control-devtools-show-console-drawer.msft.png "Figure 3: afficher le tiroir de la console"  
[ImageDrawerConsole]: /microsoft-edge/devtools-guide-chromium/media/console-elements-console-drawer-hello-world.msft.png "Figure 4: onglet de la console dans le tiroir"  
[ImageShowDrawerCommand]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Figure 5: commande d’affichage de l’onglet de console dans le tiroir"  
[ImageConsoleSettings]: /microsoft-edge/devtools-guide-chromium/media/console-settings-group-similar-empty.msft.png "Figure 6: paramètres de la console"  
[ImageConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/media/console-sidebar-drawer-empty.msft.png "Figure 7: barre latérale de la console"  
[ImageXhrGrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch.msft.png "Figure 8: enregistrement des demandes de fichiers XMLHttpRequest et FETCH"  
<!--[ImageXhrUngrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch-all.msft.png "Figure old 9: How the logged XMLHttpRequest and Fetch requests look after ungrouping"  -->  
[Image429Message]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Show-Network.msft.png "figure 9: message 429 dans la console"  
[ImageUserMessages]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Sidebar-Drawer-user-messages.msft.png "figure 10: affichage des messages des utilisateurs"  
[ImageLogLevels]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-log-Level-default-Levels.msft.png "figure 11: liste déroulante des niveaux de journaux"  
[ImageSidebarWarnings]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Sidebar-Warnings.msft.png "figure 12: utilisation de la barre latérale pour afficher les avertissements"  
[ImageUrlFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Filter-Text.msft.png "figure 13: filtre d’URL"  
[ImageNegativeUrlFilter1]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Negative-Filter-Text.msft.png "figure 14: filtre d’URL négatif masquant tous les messages correspondant à l’URL https://b.wal.co "  
[ImageNegativeUrlFilter2]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Filter-Text-specified.msft.png "figure 15: affichage des messages livrés avec WP-ad. min. js"  
[ImageRegExFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Filter-Regex.msft.png "figure 16: filtrage des messages ne correspondant pas à l’expression Regex"  
[ImageHistoryAutocomplete]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Filter-Text-AutoFilter-History.msft.png "figure 17: fenêtre contextuelle de saisie semi-automatique avec expressions de l’historique"  
[ImageJavascriptContext]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-DOM-Level-Top.msft.png "figure 18: liste déroulante de contexte JavaScript"  
[ImageSelectContext]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-DOM-Level-multiple.msft.png "figure 19: sélection d’un autre contexte JavaScript"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  
[DevToolsConsoleViewMessages]: /microsoft-edge/devtools-guide-chromium/console/index#viewing-logged-messages "Affichage des messages enregistrés-vue d’ensemble de la console"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Référence sur les API de la console"  
[DevToolsConsoleOverviewJavascript]: /microsoft-edge/devtools-guide-chromium/console/index#running-javascript "JavaScript en cours d’exécution-vue d’ensemble de la console"  
[DevToolsConsoleJavascript]: /microsoft-edge/devtools-guide-chromium/console/javascript "Commencer à utiliser JavaScript sur la console"  
[DevToolsConsoleLiveExpressions]: /microsoft-edge/devtools-guide-chromium/console/live-expressions "Regardez des valeurs d’expression JavaScript en temps réel avec des expressions dynamiques"  
[DevToolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Commencer à utiliser la journalisation des messages dans la console"  
[DevToolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "XXXXXX xxxxxxx xxx xxxxxxxxx"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexte de navigation | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
