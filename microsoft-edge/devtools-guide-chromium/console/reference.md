---
description: Référence complète sur chaque fonctionnalité et chaque comportement liés à l’interface utilisateur de la console dans Microsoft Edge DevTools.
title: Référence de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 27d521a4af528e95d06f58ac240f620a9c745044
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125257"
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

Cette page est une référence des fonctionnalités liées à la console Microsoft Edge DevTools.  Il part du principe que vous connaissez déjà l’utilisation de la console pour afficher les messages enregistrés et exécuter JavaScript.  Si ce n’est pas le cas, accédez à [la section commencer à utiliser JavaScript dans la console][DevToolsConsoleJavascript] et [commencez à utiliser les messages dans la console][DevToolsConsoleLog].  

Si vous recherchez la référence de l’API sur des fonctions telles que voir référence sur l’API de la `console.log()` [console][DevToolsConsoleApi].  Pour obtenir une référence sur les fonctions telles que `monitorEvents()` , accédez à la référence sur l' [API des utilitaires de console][DevToolsConsoleUtilities].  

## Ouvrez la console.  

Vous pouvez ouvrir la console en tant que [panneau](#open-the-console-panel) ou en tant qu' [onglet dans le tiroir](#open-the-console-tab-in-the-drawer).  

### Ouvrir l’écran de la console  

Sélectionnez `Control` + `Shift` + `J` \ (Windows, Linux \) ou `Command` + `Option` + `J` \ (MacOS \).  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Panneau de la console" lightbox="../media/console-hello-console.msft.png":::
   Panneau de la **console**  
:::image-end:::  

Pour ouvrir le panneau console à partir du [menu de commandes][DevToolsCommandMenu], commencez à taper, `Console` puis exécutez la commande Afficher la **console** contenant le badge du **panneau** .  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Panneau de la console" lightbox="../media/console-command-menu-show-console.msft.png":::
   Commande pour afficher le panneau de la **console**  
:::image-end:::  

### Ouvrir l’onglet de console dans le tiroir  

Activez ou désactivez l’option `Escape` **personnaliser et contrôler devtools** \ ( `...` \), puis sélectionnez **afficher le tiroir**de la console.  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Panneau de la console" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **Afficher le tiroir de la console**  
:::image-end:::  

Le tiroir apparaît en bas de la fenêtre de DevTools, avec l’onglet **console** ouvert.  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Panneau de la console" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   Onglet **console** du **tiroir**  
:::image-end:::  

Pour ouvrir l’onglet de la console à partir du [menu de commandes][DevToolsCommandMenu], commencez à taper, `Console` puis exécutez la commande **afficher la console** dont le badge est associé au **tiroir** .  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Panneau de la console" lightbox="../media/console-command-menu-show-console.msft.png":::
   Commande d’affichage de l’onglet de la **console** dans le **tiroir**  
:::image-end:::  

### Ouvrir les paramètres de la console  

Choisissez **paramètres** de la console \ ( ![ icône Paramètres de la console ][ImageSettingsButtonIcon] \).  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Panneau de la console" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **Paramètres de la console**  
:::image-end:::  

Les liens ci-dessous décrivent chaque paramètre:  

*   [**Masquer le réseau**](#hide-network-messages)  
*   [**Conserver le journal**](#persist-messages-across-page-loads)  
*   [**Contexte sélectionné uniquement**](#filter-out-messages-from-different-contexts)  
*   [**Groupe similaire**](#disable-message-grouping)  
*   [**Enregistrer les fichiers XmlHttpRequest**](#log-xhr-and-fetch-requests)  
*   [**Évaluation hâtif**](#disable-eager-evaluation)  
*   [**Saisie semi-automatique dans l’historique**](#disable-autocomplete-from-history)  
    
### Ouvrir la barre latérale de la console  

Sélectionnez **afficher la barre latérale** de la console \ ( ![ afficher le panneau de ][ImageShowConsoleSidebarIcon] la console) pour afficher la barre latérale, qui est utile pour le filtrage.  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Panneau de la console" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **Console** Gadget  
:::image-end:::  

## Afficher des messages  

Cette section contient des fonctionnalités qui changent le mode d’affichage des messages dans la console.  Pour obtenir une procédure pas à pas, voir [afficher les messages][DevToolsConsoleViewMessages] .  

### Désactiver le regroupement des messages  

[Ouvrez les paramètres](#open-console-settings) de la console et désactivez l’option groupe, de la **même façon** que le comportement de regroupement des messages par défaut de la console.  Pour obtenir un exemple [, voir journaux de XHR et récupérer des requêtes](#log-xhr-and-fetch-requests) .  

### Journalisation des requêtes XHR et FETCH  

[Ouvrez les paramètres](#open-console-settings) de la console et activez le **Journal** des utilisateurs pour enregistrer toutes les `XMLHttpRequest` `Fetch` demandes de la console en temps réel.  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Panneau de la console" lightbox="../media/console-xhr-fetch.msft.png":::
   Journalisation `XMLHttpRequest` et `Fetch` demandes  
:::image-end:::  
Le message supérieur de la figure précédente affiche le comportement de regroupement par défaut de la **console**.  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="Panneau de la console" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### Faire persister des messages au chargement de la page  

Par défaut, la console est effacée dès que vous chargez une nouvelle page.  Pour conserver les messages au cours du chargement de la page, [cliquez sur paramètres](#open-console-settings) de la console, puis activez la case à cocher conserver le **Journal** .  

### Masquer les messages réseau  

Par défaut, le navigateur enregistre les messages réseau sur la **console**.  Dans l’illustration suivante, le message sélectionné représente un code d’état HTTP de `429` .  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Panneau de la console" lightbox="../media/console-show-network.msft.png":::
   `429`Message sur la **console**  
:::image-end:::  
Pour masquer les messages réseau:  

1.  [Ouvrez paramètres](#open-console-settings)de la console.  
1.  Activez la case à cocher **masquer le réseau** .  
    
## Filtrer les messages  

Il existe de nombreuses façons de filtrer les messages dans la console.  

### Filtrer les messages du navigateur  

[Ouvrez la barre latérale de la console](#open-the-console-sidebar) et sélectionnez **messages utilisateur** pour afficher uniquement les messages provenant du JavaScript de la page.  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Panneau de la console" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   Afficher les messages des utilisateurs  
:::image-end:::  

### Filtrer par niveau de journal  

DevTools affecte chaque `console.*` méthode un niveau de gravité.  Il y a 4 niveaux: `Verbose` ,, `Info` `Warning` et `Error` .  Par exemple, `console.log()` se trouve dans le `Info` groupe, alors qu’il `console.error()` se trouve dans le `Error` groupe.  La [référence de l’API console][DevToolsConsoleApi] décrit le niveau de gravité de chaque méthode applicable.  Les messages que le navigateur enregistre sur la console ont également un niveau de gravité.  Vous pouvez masquer tous les niveaux de messages qui ne vous intéressent pas.  Par exemple, si vous êtes intéressé uniquement par les `Error` messages, vous pouvez masquer les 3 autres groupes.  

Cliquez sur la liste déroulante **niveaux du journal** pour activer ou désactiver ou `Verbose` `Info` `Warning` `Error` messages.  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Panneau de la console" lightbox="../media/console-log-level-default-levels.msft.png":::
   Liste déroulante **niveaux du journal**  
:::image-end:::  

Vous pouvez également filtrer par niveau de journal en [ouvrant la barre latérale de la console](#open-the-console-sidebar) , puis en cliquant sur **erreurs**, **avertissements**, **informations**ou **Commentaires**.  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Panneau de la console" lightbox="../media/console-sidebar-warnings.msft.png":::
   Utiliser la barre latérale pour afficher les avertissements  
:::image-end:::  

### Filtrer les messages par URL  

Tapez `url:` suivi d’une URL pour afficher uniquement les messages provenant de cette URL.  Après que vous avez tapé `url:` devtools affiche toutes les URL pertinentes.  Les domaines fonctionnent également.  Par exemple, si `https://example.com/a.js` `https://example.com/b.js` vous consignez des messages, `url:https://example.com` vous pouvez vous concentrer sur les messages de ces deux scripts.  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Panneau de la console" lightbox="../media/console-filter-text.msft.png":::
   Filtre d’URL  
:::image-end:::  

Entrez `-url:` pour masquer les messages de cette URL.  Ce filtre est appelé filtre d’URL négatif.  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Panneau de la console" lightbox="../media/console-negative-filter-text.msft.png":::
   Un filtre d’URL négatif masquant tous les messages correspondant à l' `https://b.wal.co` URL;
:::image-end:::  

Vous pouvez également afficher les messages d’une URL unique en [ouvrant la barre latérale](#open-the-console-sidebar)de la console, en développant la section messages de l' **utilisateur** , puis en cliquant sur l’URL du script contenant les messages sur lesquels vous souhaitez vous concentrer.  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Panneau de la console" lightbox="../media/console-filter-text-specified.msft.png":::
   Afficher les messages de `wp-ad.min.js`  
:::image-end:::  

### Filtrer les messages de différents contextes  

Imaginons que vous ayez une annonce (publicité) sur votre page.  La publicité est incorporée dans un `<iframe>` et génère un grand nombre de messages dans votre console.  Dans la mesure où la publicité s’exécute dans un autre [contexte JavaScript](#select-javascript-context), une façon de masquer les messages consiste à [ouvrir les paramètres](#open-console-settings) de la console et à activer la case à cocher **contexte sélectionnée uniquement** .  

### Filtrer les messages qui ne correspondent pas à un modèle d’expression régulière  

Tapez une expression régulière telle que `/[gm][ta][mi]/` dans la zone de texte de **filtre** pour filtrer les messages ne correspondant pas à ce modèle.  DevTools vérifie si le modèle se trouve dans le texte du message ou dans le script qui a entraîné la journalisation du message.  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Panneau de la console" lightbox="../media/console-filter-regex.msft.png":::
   Filtrer les messages ne correspondant pas à l' `/[gm][ta][mi]/` expression Regex  
:::image-end:::  

## Exécuter JavaScript  

Cette section contient des fonctionnalités relatives à l’exécution de JavaScript dans la console.  Pour obtenir une procédure pas à pas, voir [exécuter JavaScript][DevToolsConsoleOverviewJavascript] .  

### Réexécuter des expressions à partir de l’historique  

Appuyez sur la `Up Arrow` touche pour parcourir l’historique des expressions JavaScript que vous avez exécutées auparavant dans la console.  Sélectionnez `Enter` pour réexécuter cette expression.  

### Regardez la valeur d’une expression en temps réel avec des expressions dynamiques  

Si vous vous intentez de taper la même expression JavaScript dans la console à plusieurs reprises, il est possible que vous puissiez constater qu’il est plus facile de créer une **expression dynamique**.  Dans les **expressions dynamiques** , vous tapez une expression une seule fois, puis épinglez celle-ci en haut de votre console.  La valeur de l’expression est mise à jour en temps réel.  Voir [valeurs d’expression JavaScript dans Real-Time avec des expressions dynamiques][DevToolsConsoleLiveExpressions].  

### Désactiver l’évaluation hâtif  

Lorsque vous tapez des expressions JavaScript dans la console, l' **évaluation hâtif** affiche un aperçu de la valeur de retour pour cette expression.  [Ouvrez paramètres](#open-console-settings) de la console et désactivez la case à cocher **évaluation hâtif** pour désactiver les aperçus des valeurs de retour.  

### Désactiver la saisie semi-automatique dans l’historique  

Lors de la saisie d’une expression, la fenêtre contextuelle de saisie semi-automatique de la console affiche les expressions que vous avez exécutées auparavant.  Ces expressions sont précédées du `>` caractère.  [Ouvrez paramètres](#open-console-settings) de la console et désactivez l’option **saisie semi-automatique de l’historique** pour ne plus afficher les expressions de votre historique.  

> [!NOTE]
> Dans l’illustration ci-dessous, `document.querySelector('a')` `document.querySelector('img')` sont des expressions évaluées auparavant.  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="Panneau de la console" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   La fenêtre contextuelle de saisie semi-automatique affiche les expressions de l’historique.  
:::image-end:::  

### Sélectionner un contexte JavaScript  

Par défaut, la liste déroulante du **contexte JavaScript** est définie sur **Top**, qui représente le [contexte de navigation][MDNBrowsingContext] du document principal.  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Panneau de la console" lightbox="../media/console-dom-level-top.msft.png":::
   Liste déroulante **contextuelle JavaScript**  
:::image-end:::  

Imaginons que vous ayez une publicité sur votre page incorporée dans une `<iframe>` .  Vous souhaitez exécuter JavaScript afin de peaufiner le DOM de la publicité.  Vous devez tout d’abord sélectionner le contexte de navigation de la publicité dans la liste déroulante **contexte JavaScript** .  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Panneau de la console" lightbox="../media/console-dom-level-multiple.msft.png":::
   Sélectionner un autre contexte JavaScript  
:::image-end:::  

## Effacement de la console  

Vous pouvez utiliser les flux de travail suivants pour effacer la console:  

*   Sélectionnez **effacer la console** \ ( ![ effacer la console ][ImageClearConsoleIcon] \).  
*   Cliquez avec le bouton droit sur un message, puis sélectionnez **effacer la console**.  
*   Entrez `clear()` dans la console et sélectionnez `Enter` .  
*   Exécution `console.clear()` à partir du JavaScript de votre page Web.  
*   Sélectionnez `Control` + `L` lorsque la console a le focus.  
    
## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Affichage des messages enregistrés-vue d’ensemble de la console | Documents Microsoft"  
[DevToolsConsoleApi]: ./api.md "Référence sur les API de console | Documents Microsoft"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "JavaScript en cours d’exécution-vue d’ensemble de la console | Documents Microsoft"  
[DevToolsConsoleJavascript]: ./javascript.md "Commencer à utiliser JavaScript dans la console | Documents Microsoft"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Regardez des valeurs d’expression JavaScript en temps réel avec des expressions dynamiques | Documents Microsoft"  
[DevToolsConsoleLog]: ./log.md "Commencer à utiliser la journalisation des messages dans la console | Documents Microsoft"  
[DevToolsConsoleUtilities]: ./utilities.md "Référence sur l’API des utilitaires de console | Documents Microsoft"  

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
