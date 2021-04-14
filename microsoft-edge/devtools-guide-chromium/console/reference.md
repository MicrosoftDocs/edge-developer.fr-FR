---
description: Une référence complète pour chaque fonctionnalité et comportement de l'interface utilisateur de la console dans Microsoft Edge DevTools.
title: Référence de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: adc3f6c33d6e1a2f6c7db8336c5ab803e76c3307
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483266"
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

Cet article est une référence des fonctionnalités liées à la console Microsoft Edge DevTools.  Il part du principe que vous êtes déjà familiarisé avec l'utilisation de la console pour afficher les messages enregistrés et exécuter JavaScript.  Si ce n'est pas le cas, accédez à Commencer à l'exécution [de JavaScript][DevtoolsConsoleConsoleJavascript] dans la console et à la journalisation des [messages dans la console.][DevtoolsConsoleConsoleLog]  

Si vous recherchez la référence d'API sur des fonctions telles que , accédez à Référence `console.log()` [de l'API console.][DevToolsConsoleApi]  Pour obtenir la référence sur des fonctions telles que , accédez à Référence de `monitorEvents()` [l'API des utilitaires de console.][DevToolsConsoleUtilities]  

## <a name="open-the-console"></a>Ouvrir la console  

Vous pouvez ouvrir la **console en tant** qu'outil dans le [volet](#open-the-console-tool) supérieur ou en tant qu'outil dans [le caisse.](#open-the-console-tool-in-the-drawer)  

### <a name="open-the-console-tool"></a>Ouvrir l'outil Console  

Sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="L'outil Console" lightbox="../media/console-hello-console.msft.png":::
   **L'outil Console**  
:::image-end:::  

Pour ouvrir **l'outil Console** à partir du [menu][DevtoolsCommandMenuIndex]Commande, tapez, puis exécutez la commande Afficher la console qui a le `Console` badge **Panneau** à côté de celui-ci. ****  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Exécutez la commande pour afficher l'outil Console" lightbox="../media/console-command-menu-show-console.msft.png":::
   Exécutez la commande pour afficher **l'outil Console**  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a>Ouvrir l'outil Console dans le caisse  

Sélectionnez `Esc` ou choisissez Personnaliser et contrôler **DevTools** \( \), puis choisissez Afficher le caisse `...` de la **console.**  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Afficher le caisse de la console" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **Afficher le caisse de la console**  
:::image-end:::  

Le caisse s'ouvre en bas de la fenêtre DevTools, avec l'outil **Console** ouvert.  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Outil Console dans le caisse" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   Outil **Console** dans le **caisse**  
:::image-end:::  

Pour ouvrir **l'outil Console** à partir du [menu][DevtoolsCommandMenuIndex]Commande, tapez, puis exécutez la commande Afficher la console qui a le badge à l'aide de `Console` celui-ci. **** ****  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Exécutez la commande pour afficher l'outil **Console** dans le caisse" lightbox="../media/console-command-menu-show-console.msft.png":::
   Exécutez la commande pour afficher **l'outil Console** dans le **caisse**  
:::image-end:::  

### <a name="open-console-settings"></a>Ouvrir les paramètres de la console  

Choisissez le **bouton Paramètres de la console** \( Icône ![ Paramètres de la console ](../media/settings-button-icon.msft.png) \).  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Paramètres de la console" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **Paramètres de la console**  
:::image-end:::  

Les liens suivants expliquent chaque paramètre.  

*   [Masquer le réseau](#hide-network-messages)  
*   [Conserver le journal](#persist-messages-across-page-loads)  
*   [Contexte sélectionné uniquement](#filter-out-messages-from-different-contexts)  
*   [Groupe similaire](#turn-off-message-grouping)  
*   [Log XMLHttpRequests](#log-xhr-and-fetch-requests)  
*   [Évaluation enthousiaste](#turn-off-eager-evaluation)  
*   [Autocomplete from history](#turn-off-autocomplete-from-history)  
<!--*   Evaluate triggers user activation  -->  
    
### <a name="open-the-console-sidebar"></a>Ouvrir la barre latérale de la console  

Pour afficher la barre **latérale, choisissez** **Afficher la barre latérale de la console** \( Afficher la barre latérale de la console ![ ](../media/show-console-sidebar-icon.msft.png) \).  La **barre latérale vous** aide à filtrer.  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Console Sidebar" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **Console Sidebar**  
:::image-end:::  

## <a name="view-messages"></a>Afficher les messages  

Cette section contient des fonctionnalités qui modifient la présentation des messages dans la console.  Pour une walkthrough pratique, accédez à [Afficher les messages.][DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage]  

### <a name="turn-off-message-grouping"></a>Désactiver le regroupement de messages  

Pour désactiver le comportement de regroupement des messages par défaut de la **console,** ouvrez [Paramètres](#open-console-settings) de la console et cochez la case en regard de **Groupe similaire.**  Pour obtenir un exemple, accédez à [Log XHR et fetch requests](#log-xhr-and-fetch-requests).  

### <a name="log-xhr-and-fetch-requests"></a>Enregistrer les demandes XHR et Fetch  

Pour enregistrer toutes les demandes et toutes les demandes sur la console, ouvrez paramètres de la console et cochez la case en regard de `XMLHttpRequest` `Fetch` Log **XMLHttpRequests**. **** [](#open-console-settings)  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Log XMLHttpRequest and Fetch requests" lightbox="../media/console-xhr-fetch.msft.png":::
   Journal `XMLHttpRequest` et `Fetch` demandes  
:::image-end:::  

Le premier message de la figure précédente affiche le comportement de regroupement par défaut de la **console.**  <!--  In the following figure, the same log is displayed after you [turn off message grouping](#turn-off-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a>Persist messages across page loads  

Lorsque vous chargez une nouvelle page web, l'action par défaut permet d'effacer la **console.**  Pour conserver les messages entre les chargements de page, [ouvrez paramètres](#open-console-settings) de la console et cochez la case en regard de **Conserver le journal.**  

### <a name="hide-network-messages"></a>Masquer les messages réseau  

L'action par défaut de Microsoft Edge consiste à enregistrer les messages réseau dans la **console.**  Dans la figure suivante, le message choisi représente un code d'état HTTP de `429` .  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Un message 429 dans la console" lightbox="../media/console-show-network.msft.png":::
   Un `429` message dans la **console**  
:::image-end:::  

Pour masquer les messages réseau, effectuer les actions suivantes.  

1.  [Ouvrez paramètres de la console.](#open-console-settings)  
1.  Cochez la case en regard de **Masquer le réseau.**  
    
## <a name="filter-messages"></a>Filtrer les messages  

Il existe de nombreuses façons de filtrer les messages dans la **console.**  

### <a name="filter-out-browser-messages"></a>Filtrer les messages du navigateur  

[Ouvrez la barre latérale de la console](#open-the-console-sidebar) et choisissez # **messages** utilisateur pour afficher uniquement les messages provenant du JavaScript de la page web.  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Afficher les messages de l'utilisateur" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   Afficher les messages de l'utilisateur  
:::image-end:::  

### <a name="filter-by-log-level"></a>Filtrer par niveau de journal  

DevTools affecte à chaque `console.*` méthode l'un des quatre niveaux de gravité.  

*   `Error`  
*   `Info`  
*   `Verbose`  
*   `Warning`  
    
Par exemple, `console.log()` se trouve dans le `Info` groupe, mais dans le `console.error()` `Error` groupe.  La [référence de l'API][DevToolsConsoleApi] console décrit le niveau de gravité de chaque méthode applicable.  Chaque message journal de la console par le navigateur présente également un niveau de gravité.  Vous pouvez masquer n'importe quel niveau de messages qui ne vous intéresse pas.  Par exemple, si les messages vous intéressent uniquement, vous pouvez `Error` masquer les trois autres groupes.  

Pour filtrer les messages, sélectionnez la dropdown **Niveaux** du journal `Verbose` et choisissez , ou `Info` `Warning` `Error` .  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="La dropdown Log Levels" lightbox="../media/console-log-level-default-levels.msft.png":::
   La **dropdown Log Levels**  
:::image-end:::  

Pour utiliser le niveau de journal pour filtrer, ouvrez **** la barre latérale de la [console,](#open-the-console-sidebar) puis choisissez **Erreurs, Avertissements,** Informations ou **Détaillé.** ****  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Utiliser la barre latérale pour afficher les avertissements" lightbox="../media/console-sidebar-warnings.msft.png":::
   Utiliser la barre latérale pour afficher les avertissements  
:::image-end:::  

### <a name="filter-messages-by-url"></a>Filtrer les messages par URL  

Tapez `url:` suivi d'une URL pour afficher uniquement les messages provenant de cette URL.  Une fois que `url:` vous avez tapé, DevTools affiche toutes les URL pertinentes.  Les domaines fonctionnent également.  Par exemple, si et journalisation des messages, vous permet de vous concentrer sur les messages de `https://example.com/a.js` `https://example.com/b.js` ces deux `url:https://example.com` scripts.  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Filtre d'URL" lightbox="../media/console-filter-text.msft.png":::
   Filtre d'URL  
:::image-end:::  

Pour masquer les messages d'une URL, tapez `-url:` .  Il s'agit d'un filtre d'URL négatif.  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Filtre d'URL négatif qui masque tous les messages qui correspondent à https://b.wal.co l'URL" lightbox="../media/console-negative-filter-text.msft.png":::
   Filtre d'URL négatif qui masque tous les messages qui correspondent à `https://b.wal.co` l'URL
:::image-end:::  

Pour afficher des messages à partir d'une URL unique, effectuer les actions suivantes.  

1.  [Ouvrez la barre latérale de la console.](#open-the-console-sidebar)  
1.  Développez la section **#user messages.**  
1.  Choisissez l'URL du script qui contient les messages sur lesquels vous souhaitez vous concentrer.  
    
:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Afficher les messages provenant de wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   Afficher les messages d'où ils sont issus `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a>Filtrer les messages de différents contextes  

Supposons que vous avez une annonce \(ad\) sur votre page web.  La publicitaire est incorporée dans un `<iframe>` et génère de nombreux messages dans votre **console.**  Étant donné que la publicitaire s'exécute dans un contexte [JavaScript](#choose-javascript-context)différent, une façon de masquer les messages consiste à ouvrir les [paramètres](#open-console-settings) de la console et à cocher la case en regard du **contexte sélectionné uniquement.**  

### <a name="filter-out-messages-that-dont-match-a-regular-expression-pattern"></a>Filtrer les messages qui ne correspondent pas à un modèle d'expression régulière  

Tapez une expression régulière telle que dans la boîte de texte Filtrer pour filtrer les messages qui ne correspondent `/[gm][ta][mi]/` pas à ce modèle. ****  DevTools vérifie si le modèle est trouvé dans le texte du message ou dans le script à l'origine de la consigner.  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtrer les messages qui ne correspondent pas à l'expression regex" lightbox="../media/console-filter-regex.msft.png":::
   Filtrer les messages qui ne correspondent pas à `/[gm][ta][mi]/` l'expression regex  
:::image-end:::  

## <a name="run-javascript"></a>Exécuter JavaScript  

Cette section contient des fonctionnalités liées à l'exécution de JavaScript dans la **console.**  Pour une walkthrough pratique, accédez à [Exécuter JavaScript][DevtoolsConsoleConsoleJavascript].  

### <a name="rerun-expressions-from-history"></a>Réexécuter des expressions à partir de l'historique  

Sélectionnez `Up Arrow` pour passer en cycle l'historique des expressions JavaScript que vous avez précédemment dans la **console.**  Sélectionnez `Enter` pour exécuter à nouveau cette expression.  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a>Regarder la valeur d'une expression en temps réel avec des expressions live  

Si vous vous trouvez en train de taper la même expression JavaScript dans la **console** à plusieurs reprises, vous trouverez peut-être plus facile de créer une **expression live.**  Avec **les expressions live,** vous tapez une expression une fois, puis vous l'épinglez en haut de votre **console.**  La valeur de l'expression est mise à jour en temps quasi réel.  Accédez à [regarder les valeurs d'expression JavaScript Real-Time avec des expressions live.][DevToolsConsoleLiveExpressions]  

### <a name="turn-off-eager-evaluation"></a>Désactiver l'évaluation enthousiaste  

**L'évaluation** enthousiaste affiche un aperçu de la valeur de retour lorsque vous tapez des expressions JavaScript dans la **console.**  Pour désactiver les aperçus de valeur de retour, effectuer les actions suivantes.  

1.  [Ouvrez paramètres de la console.](#open-console-settings)  
1.  Supprimez la case à cocher en regard **de l'évaluation enthousiaste.**  
    
### <a name="turn-off-autocomplete-from-history"></a>Désactiver la mise encomplet automatique de l'historique  

Lorsque vous tapez une expression, la fenêtre popup de la console decomplet automatique affiche les expressions que vous avez précédemment entrées. ****  Les expressions sont pré-pendées avec le `>` caractère.  Pour arrêter d'afficher les expressions de votre historique, ouvrez [paramètres](#open-console-settings) de la console et supprimez la case à cocher en regard de la case à cocher De l'historique de la mise à jour de la mise **à** jour automatique.  

> [!NOTE]
> Dans la figure suivante, `document.querySelector('a')` sont des expressions qui ont été `document.querySelector('img')` évaluées précédemment.  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="Le menu popup de la mise à jour automatique affiche les expressions de l'historique" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   Le menu popup de la mise à jour automatique affiche les expressions de l'historique  
:::image-end:::  

### <a name="choose-javascript-context"></a>Choisir le contexte JavaScript  

L'option par défaut pour la liste **liste finale du contexte JavaScript** est supérieure, qui représente le contexte de navigation de la page web principale. **** [][MdnDocsGlossaryBrowsingContext]  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="La dropdown de contexte JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   La **dropdown de contexte JavaScript**  
:::image-end:::  

Supposons que vous avez une vidéo sur votre page web incorporée dans un `<iframe>` .  Vous souhaitez exécuter JavaScript pour ajuster le DOM de l'ad.  Tout d'abord, choisissez le contexte de navigation de la nouvelle dans la description du contexte **JavaScript.**  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Choisir un autre contexte JavaScript" lightbox="../media/console-dom-level-multiple.msft.png":::
   Choisir un autre contexte JavaScript  
:::image-end:::  

## <a name="clear-the-console"></a>Effacer la console  

Pour effacer la **console,** terminez l'un des flux de travail suivants.  

*   Choisissez le **bouton Effacer la console** \( Effacer la console ![ ](../media/clear-console-button-icon.msft.png) \).  
*   Pointez sur un message, ouvrez le menu contextuel \(clic droit\), puis choisissez **Effacer la console.**  
*   Entrez `clear()` dans la **console,** puis sélectionnez `Enter` .  
*   Exécutez `console.clear()` à partir de JavaScript pour votre page web.  
*   Sélectionnez `Control` + `L` pendant que **la console** est en focus.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Référence de l'API de console | Documents Microsoft"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Journal des messages dans l'outil console | Documents Microsoft"  
[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Console en tant qu'environnement JavaScript | Documents Microsoft"  
[DevtoolsConsoleIndex]: .index.md "Utiliser la console | Documents Microsoft"  
[DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage]: ./index.md#inspect-and-filter-information-on-the-current-webpage "Inspecter et filtrer les informations sur la page web | Documents Microsoft"  
[DevtoolsConsoleLiveExpressions]: ./live-expressions.md "Surveiller les modifications apportées dans JavaScript à l'aide d'expressions | Documents Microsoft"  
[DevtoolsConsoleUtilities]: ./utilities.md "Référence de l'API des utilitaires de console | Documents Microsoft"  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Exécuter des commandes avec le menu DevTools Command de Microsoft Edge | Documents Microsoft"  

[MdnDocsGlossaryBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexte de navigation | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
