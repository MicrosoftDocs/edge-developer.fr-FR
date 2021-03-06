---
description: Une référence complète sur chaque fonctionnalité et comportement liés à l’interface utilisateur de la console dans Microsoft Edge DevTools.
title: Référence de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 1aed46486240dea19420e8b7cb52b6758f1f528b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399161"
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

# <a name="console-reference"></a>Référence de la console  

Cette page est une référence de fonctionnalités liées à la console Microsoft Edge DevTools.  Il part du principe que vous êtes déjà familiarisé avec l’utilisation de la console pour afficher les messages enregistrés et exécuter JavaScript.  Si ce n’est pas le cas, accédez à l’exécution de [JavaScript][DevToolsConsoleJavascript] dans la console et à la journalisation des [messages dans la console.][DevToolsConsoleLog]  

Si vous recherchez la référence d’API sur des fonctions telles que , accédez à Référence `console.log()` de [l’API console.][DevToolsConsoleApi]  Pour obtenir la référence sur des fonctions telles que , accédez à Référence de `monitorEvents()` [l’API des utilitaires de console.][DevToolsConsoleUtilities]  

## <a name="open-the-console"></a>Ouvrir la console  

Vous pouvez ouvrir la **console en tant** qu’outil dans le [volet](#open-the-console-tool) supérieur ou en tant qu’outil dans [le caisse.](#open-the-console-tool-in-the-drawer)  

### <a name="open-the-console-tool"></a>Ouvrir l’outil Console  

Sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="L’outil Console" lightbox="../media/console-hello-console.msft.png":::
   **L’outil Console**  
:::image-end:::  

Pour ouvrir **l’outil Console** à partir du [menu][DevToolsCommandMenu]Commande, commencez à taper, puis exécutez la commande Afficher la console qui a le `Console` badge **Panneau** à côté. ****  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Commande pour afficher le panneau console" lightbox="../media/console-command-menu-show-console.msft.png":::
   Commande pour afficher **l’outil Console**  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a>Ouvrir l’outil Console dans le caisse  

Sélectionnez `Escape` ou choisissez Personnaliser et contrôler **DevTools** \( \), puis choisissez Afficher le caisse `...` de la **console.**  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Afficher le caisse de la console" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **Afficher le caisse de la console**  
:::image-end:::  

Le caisse s’ouvre en bas de la fenêtre DevTools, avec l’outil **Console** ouvert.  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Outil Console dans le caisse" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   Outil **Console** dans le **caisse**  
:::image-end:::  

Pour ouvrir **l’outil Console** à partir du [menu][DevToolsCommandMenu]Commande, commencez à taper, puis exécutez la commande Afficher la console qui a le badge à l’aide `Console` de celui-ci. **** ****  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Commande permettant d’afficher l’outil **Console** dans le caisse" lightbox="../media/console-command-menu-show-console.msft.png":::
   Commande permettant d’afficher **l’outil Console** dans le **caisse**  
:::image-end:::  

### <a name="open-console-settings"></a>Ouvrir les paramètres de la console  

Choose **Console Settings** \( ![ Console Settings icon ][ImageSettingsButtonIcon] \).  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Paramètres de la console" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **Paramètres de la console**  
:::image-end:::  

Les liens ci-dessous expliquent chaque paramètre :  

*   [**Masquer le réseau**](#hide-network-messages)  
*   [**Conserver le journal**](#persist-messages-across-page-loads)  
*   [**Contexte sélectionné uniquement**](#filter-out-messages-from-different-contexts)  
*   [**Groupe similaire**](#disable-message-grouping)  
*   [**Log XmlHttpRequests**](#log-xhr-and-fetch-requests)  
*   [**Évaluation enthousiaste**](#disable-eager-evaluation)  
*   [**Autocomplete From History**](#disable-autocomplete-from-history)  
    
### <a name="open-the-console-sidebar"></a>Ouvrir la barre latérale de la console  

Choisissez **Afficher la barre latérale de la console** \( Afficher la barre latérale de la console \) pour afficher la barre latérale, ce qui est utile pour le ![ ][ImageShowConsoleSidebarIcon] filtrage.  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Console Sidebar" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **Console** Barre latérale  
:::image-end:::  

## <a name="view-messages"></a>Afficher les messages  

Cette section contient des fonctionnalités qui modifient la présentation des messages dans la console.  Pour une walkthrough pratique, accédez à [Afficher les messages.][DevToolsConsoleViewMessages]  

### <a name="disable-message-grouping"></a>Désactiver le regroupement de messages  

[Ouvrez paramètres de](#open-console-settings) la console et désactivez **le groupe** de façon à désactiver le comportement de regroupement des messages par défaut de la console.  Pour obtenir un exemple, accédez à [Log XHR et fetch requests](#log-xhr-and-fetch-requests).  

### <a name="log-xhr-and-fetch-requests"></a>Enregistrer les demandes XHR et Fetch  

[Ouvrez les paramètres de](#open-console-settings) la console et activez **log XMLHttpRequests** pour enregistrer toutes les demandes et les demandes sur la `XMLHttpRequest` console au cours de leur `Fetch` temps.  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Log XMLHttpRequest and Fetch requests" lightbox="../media/console-xhr-fetch.msft.png":::
   Journal `XMLHttpRequest` et `Fetch` demandes  
:::image-end:::  
Le premier message de la figure précédente affiche le comportement de regroupement par défaut de la **console.**  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a>Persist messages across page loads  

Par défaut, la console s’effacera chaque fois que vous chargez une nouvelle page.  Pour conserver les messages entre les chargements de page, [ouvrez paramètres](#open-console-settings) de la console, puis activez la case à cocher Conserver **le** journal.  

### <a name="hide-network-messages"></a>Masquer les messages réseau  

Par défaut, le navigateur enregistre les messages réseau dans la **console.**  Dans la figure suivante, le message sélectionné représente un code d’état HTTP de `429` .  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Un message 429 dans la console" lightbox="../media/console-show-network.msft.png":::
   Un `429` message dans la **console**  
:::image-end:::  
Pour masquer les messages réseau :  

1.  [Ouvrez paramètres de la console.](#open-console-settings)  
1.  Activez la **case à cocher** Masquer le réseau.  
    
## <a name="filter-messages"></a>Filtrer les messages  

Il existe de nombreuses façons de filtrer les messages dans la console.  

### <a name="filter-out-browser-messages"></a>Filtrer les messages du navigateur  

[Ouvrez la barre latérale de la console](#open-the-console-sidebar) et choisissez **Messages** de l’utilisateur pour afficher uniquement les messages provenant du JavaScript de la page.  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Afficher les messages de l’utilisateur" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   Afficher les messages de l’utilisateur  
:::image-end:::  

### <a name="filter-by-log-level"></a>Filtrer par niveau de journal  

DevTools affecte à chaque `console.*` méthode un niveau de gravité.  Il existe 4 niveaux `Verbose` : , `Info` et `Warning` `Error` .  Par exemple, `console.log()` se trouve dans le `Info` groupe, tandis `console.error()` qu’il se trouve dans le `Error` groupe.  La [référence de l’API][DevToolsConsoleApi] console décrit le niveau de gravité de chaque méthode applicable.  Chaque message journal de la console par le navigateur présente également un niveau de gravité.  Vous pouvez masquer n’importe quel niveau de messages qui ne vous intéresse pas.  Par exemple, si seuls les messages vous intéressent, vous pouvez `Error` masquer les 3 autres groupes.  

Choose the **Log Levels** dropdown to enable or disable , , `Verbose` or `Info` `Warning` `Error` messages.  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="La dropdown Log Levels" lightbox="../media/console-log-level-default-levels.msft.png":::
   La **dropdown Log Levels**  
:::image-end:::  

Vous pouvez également filtrer par niveau de journal en **** ouvrant la barre latérale de la [console,](#open-the-console-sidebar) puis en cinglant les **erreurs, les avertissements,** les informations **ou** **les commentaires.**  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Utiliser la barre latérale pour afficher les avertissements" lightbox="../media/console-sidebar-warnings.msft.png":::
   Utiliser la barre latérale pour afficher les avertissements  
:::image-end:::  

### <a name="filter-messages-by-url"></a>Filtrer les messages par URL  

Tapez `url:` suivi d’une URL pour afficher uniquement les messages provenant de cette URL.  Une fois que `url:` vous avez tapé, DevTools affiche toutes les URL pertinentes.  Les domaines fonctionnent également.  Par exemple, si et journalisation des messages, vous permet de vous concentrer sur les messages de `https://example.com/a.js` `https://example.com/b.js` ces `url:https://example.com` 2 scripts.  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Filtre d’URL" lightbox="../media/console-filter-text.msft.png":::
   Filtre d’URL  
:::image-end:::  

Tapez `-url:` pour masquer les messages de cette URL.  Il s’agit d’un filtre d’URL négatif.  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Filtre d’URL négatif qui masque tous les messages qui correspondent à https://b.wal.co l’URL" lightbox="../media/console-negative-filter-text.msft.png":::
   Filtre d’URL négatif qui masque tous les messages qui correspondent à `https://b.wal.co` l’URL
:::image-end:::  

Vous pouvez également afficher les messages à partir d’une URL unique en ouvrant la barre latérale de la [console,](#open-the-console-sidebar)en développez la section **Messages** utilisateur, puis enchoosant l’URL du script contenant les messages sur lesquels vous souhaitez vous concentrer.  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Afficher les messages provenant de wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   Afficher les messages d’où ils sont issus `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a>Filtrer les messages à partir de différents contextes  

Supposons que vous avez une annonce \(ad\) sur votre page.  La publicitaire est incorporée dans une console et génère un `<iframe>` grand nombre de messages.  Étant donné que la publicitaire s’exécute dans un contexte [JavaScript](#select-javascript-context)différent, une façon de masquer les messages consiste à ouvrir les [paramètres](#open-console-settings) de la console et à activer la case à cocher Contexte **uniquement** sélectionné.  

### <a name="filter-out-messages-that-do-not-match-a-regular-expression-pattern"></a>Filtrer les messages qui ne correspondent pas à un modèle d’expression régulière  

Tapez une expression régulière telle que dans la zone de texte Filtrer pour filtrer les messages qui ne `/[gm][ta][mi]/` correspondent pas à ce modèle. ****  DevTools vérifie si le modèle est trouvé dans le texte du message ou dans le script à l’origine de la consigner.  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtrer tous les messages qui ne correspondent pas à l’expression regex" lightbox="../media/console-filter-regex.msft.png":::
   Filtrer les messages qui ne correspondent pas à `/[gm][ta][mi]/` l’expression regex  
:::image-end:::  

## <a name="run-javascript"></a>Exécuter JavaScript  

Cette section contient des fonctionnalités liées à l’exécution de JavaScript dans la console.  Pour une walkthrough pratique, accédez à [Exécuter JavaScript][DevToolsConsoleOverviewJavascript].  

### <a name="re-run-expressions-from-history"></a>Ré-exécuter des expressions à partir de l’historique  

Sélectionnez la clé à utiliser pour passer en cycle de l’historique des expressions JavaScript que vous avez précédemment dans `Up Arrow` la console.  Sélectionnez `Enter` pour exécuter à nouveau cette expression.  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a>Regarder la valeur d’une expression en temps réel avec des expressions en direct  

Si vous vous trouvez en train de taper la même expression JavaScript dans la console à plusieurs reprises, vous trouverez peut-être plus facile de créer une **expression live.**  Avec **les expressions live,** vous tapez une expression une seule fois, puis vous l’épinglez en haut de votre console.  La valeur de l’expression est mise à jour en temps quasi réel.  Accédez à [regarder les valeurs d’expression JavaScript Real-Time avec des expressions live.][DevToolsConsoleLiveExpressions]  

### <a name="disable-eager-evaluation"></a>Désactiver l’évaluation enthousiaste  

Lorsque vous tapez des expressions JavaScript dans la console, **l’évaluation de l’enthousiaste** affiche un aperçu de la valeur de retour de cette expression.  [Ouvrez les paramètres de](#open-console-settings) la console et désactivez la case à cocher Évaluation de l’adage **pour** désactiver les aperçus de valeur de retour.  

### <a name="disable-autocomplete-from-history"></a>Désactiver la mise encomplet automatique de l’historique  

Lorsque vous tapez une expression, la fenêtre popup de la console de lacomplet automatique affiche les expressions que vous avez déjà écrites.  Ces expressions sont précédées du `>` caractère.  [Ouvrez paramètres de](#open-console-settings) **** la console et désactivez la case à cocher De l’historique pour arrêter d’afficher les expressions de votre historique.  

> [!NOTE]
> Dans la figure suivante, `document.querySelector('a')` sont des expressions qui ont été `document.querySelector('img')` évaluées précédemment.  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="La fenêtre de recomplet automatique affiche les expressions de l’historique" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   La fenêtre de recomplet automatique affiche les expressions de l’historique  
:::image-end:::  

### <a name="select-javascript-context"></a>Sélectionner un contexte JavaScript  

Par défaut, la liste liste de listes des [][MDNBrowsingContext] contextes **JavaScript** est définie sur **haut,** ce qui représente le contexte de navigation du document principal.  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="La dropdown de contexte JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   La **dropdown de contexte JavaScript**  
:::image-end:::  

Supposons que vous avez une vidéo sur votre page incorporée dans un `<iframe>` .  Vous souhaitez exécuter JavaScript afin d’ajuster le DOM de la commande.  Vous devez tout d’abord sélectionner le contexte de navigation de la nouvelle dans la dropdown Contexte **JavaScript.**  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Choisir un autre contexte JavaScript" lightbox="../media/console-dom-level-multiple.msft.png":::
   Choisir un autre contexte JavaScript  
:::image-end:::  

## <a name="clear-the-console"></a>Effacer la console  

Vous pouvez utiliser l’un des flux de travail suivants pour effacer la console :  

*   Choose **Clear Console** \( Clear Console ![ ][ImageClearConsoleIcon] \).  
*   Pointez sur un message, ouvrez le menu contextuel \(righ-click\), puis choisissez **Effacer la console.**  
*   Entrez `clear()` dans la **console,** puis sélectionnez `Enter` .  
*   Exécutez `console.clear()` à partir de JavaScript pour votre page web.  
*   Sélectionnez `Control` + `L` pendant que **la console** est en focus.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Exécuter des commandes avec le menu DevTools Command de Microsoft Edge | Documents Microsoft"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Affichage des messages enregistrés : vue d’ensemble de la console | Documents Microsoft"  
[DevToolsConsoleApi]: ./api.md "Référence de l’API de console | Documents Microsoft"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Exécution de JavaScript : vue d’ensemble de la console | Documents Microsoft"  
[DevToolsConsoleJavascript]: ./javascript.md "Commencer à utiliser JavaScript dans la console | Documents Microsoft"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Regardez les valeurs des expressions JavaScript en temps réel avec les expressions | Documents Microsoft"  
[DevToolsConsoleLog]: ./log.md "Commencer à journalisation des messages dans la console | Documents Microsoft"  
[DevToolsConsoleUtilities]: ./utilities.md "Référence de l’API des utilitaires de console | Documents Microsoft"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexte de navigation | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
