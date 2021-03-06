---
description: Découvrez comment enregistrer des messages dans la console.
title: Commencer à journalisation des messages dans la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: e2ea1a8327dd2a591e067b69198c4509b2abcb2d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399168"
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

# <a name="get-started-with-logging-messages-in-the-console"></a>Commencer à journalisation des messages dans la console  

Ce didacticiel interactif vous montre comment enregistrer et filtrer des messages dans la console [Microsoft Edge DevTools.][MicrosoftEdgeDevTools]  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Messages dans la console" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   Messages dans la **console**  
:::image-end:::  

Ce didacticiel est destiné à être terminé dans l’ordre.  Il part du principe que vous comprenez les principes de base du développement web, comme l’utilisation de JavaScript pour ajouter de l’interactivité à une page.  

## <a name="set-up-the-demo-and-devtools"></a>Configurer la démonstration et DevTools  

Ce didacticiel est conçu pour vous permettre d’ouvrir la démonstration et d’essayer tous les flux de travail vous-même.  Lorsque vous suivez physiquement le processus, vous êtes plus susceptible de mémoriser les flux de travail ultérieurement.  

1.  Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Log Examples** to open in a new tab.  
    
    [Exemples de journaux de console][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  Concentrez la démonstration, puis sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\) pour ouvrir DevTools.  Par défaut, DevTools s’ouvre à droite de la démonstration.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="DevTools s’ouvre à droite de la démonstration" lightbox="../media/console-example-devtools-right-console.msft.png":::
             DevTools s’ouvre à droite de la démonstration  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Ancrez DevTools en bas de la fenêtre.][DevToolsCustomizePlacement]  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools docked to the bottom of the demo" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             DevTools docked to the bottom of the demo  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > [Désédock DevTools dans une fenêtre distincte.][DevToolsCustomizePlacement]  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Navigateur dans une fenêtre distincte" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             Navigateur dans une fenêtre distincte  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Undock DevTools dans une fenêtre distincte.][DevToolsCustomizePlacement]  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="DevTools non barraté dans une fenêtre distincte" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             DevTools non barraté dans une fenêtre distincte  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="view-messages-logged-from-javascript"></a>Afficher les messages enregistrés à partir de JavaScript  

La plupart des messages affichés dans la **console** proviennent des développeurs web qui ont écrit le JavaScript de la page.  L’objectif de cette section est de vous présenter les différents types de messages que vous êtes susceptible de passer en revue dans la **console**et d’expliquer comment vous pouvez enregistrer chaque type de message vous-même à partir de votre propre javaScript.  

1.  Sélectionnez **le bouton Informations sur** le journal dans la démonstration.  `Hello, Console!` est consigné dans la console.
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="Console après avoir choisi Les informations du journal" lightbox="../media/console-log-info.msft.png":::
       Console **après** avoir choisi Les **informations du journal**  
    :::image-end:::  
    
1.  En face du `Hello, Console!` message dans la console, choisissez **log.js:2**.  Le panneau Sources s’ouvre et met en évidence la ligne de code à l’origine de la journalisé du message sur la console.  Le message a été enregistré lors de l’utilisation du javaScript de la `console.log('Hello, Console!')` page.
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="DevTools ouvre l’outil Sources après avoir choisi log.js:2" lightbox="../media/console-sources-logjs.msft.png":::
       DevTools ouvre l’outil **Sources** une fois que vous avez choisi `log.js:2`  
    :::image-end:::  
    
1.  Revenir à la **console à l’aide** de l’un des flux de travail suivants :  
    
    *   Choisissez **l’outil Console.**  
    *   Sélectionnez `Control` + `[` \(Windows, Linux\) ou `Command` + `[` \(macOS\) **** jusqu’à ce que l’outil console soit en focus.  
    *   [Ouvrez le menu Commande,][DevToolsCommandMenu]tapez, choisissez la commande Afficher le panneau de `Console` **console,** puis sélectionnez `Enter` .  
    
1.  Sélectionnez le **bouton Avertissement** du journal dans la démonstration.  `Abandon Hope All Ye Who Enter` est consigné dans la **console**.  Les messages formatés comme ceci sont des avertissements.  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="Console après avoir choisi Avertissement de journal" lightbox="../media/console-log-warning.msft.png":::
       Console **après avoir** choisi Avertissement de **journal**  
    :::image-end:::  
    
    > [!TIP]
    > Si vous souhaitez afficher le code à l’origine de la journalisé d’un message d’une certaine façon, choisissez un script \(tel que \) pour afficher le code à l’origine de la mise en forme du `log.js:12` message.  

1.  Choose the **Expand** \( ![ Expand ][ImageExpandIcon] \) icon in front of `Abandon Hope All Ye Who Enter` .  DevTools affiche la [trace de pile][WikiStackTrace] précédant l’appel.  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Une trace de pile" lightbox="../media/console-log-warning-expanded.msft.png":::
       Une trace de pile  
    :::image-end:::  
    
    La trace de pile vous dit qu’une fonction nommée est exécuté, qui à son tour `logWarning` exécute une fonction nommée `quoteDante` .  En d’autres termes, la demande qui s’est produite en premier se trouve en bas de la trace de pile.  Vous pouvez enregistrer les traces de pile à tout moment en exécutant `console.trace()` .  

1.  Choose **Log Error**.  Le message d’erreur suivant est consigné : `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Message d’erreur" lightbox="../media/console-log-error.msft.png":::
       Message d’erreur  
    :::image-end:::  
    
1.  Choose **Log Table**.  Un tableau sur ces derniers est enregistré sur la **console.**  
    
    > [!NOTE]
    > La `birthday` colonne est remplie uniquement pour une ligne.  Examinez le code pour en déterminer la raison.
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Un tableau dans la console" lightbox="../media/console-log-table.msft.png":::
       Un tableau dans la **console**  
    :::image-end:::  
    
1.  Choose **Log Group**.  Les noms de 4 personnes qui se disputent la violence sont regroupés sous `Adolescent Irradiated Espionage Tortoises` l’étiquette.  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Un groupe de messages dans la console" lightbox="../media/console-log-group.msft.png":::
       Un groupe de messages dans la **console**  
    :::image-end:::  
    
1.  Choose **Log Custom**.  Un message avec une bordure rouge et un arrière-plan bleu est enregistré dans la console.  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Message avec mise en forme personnalisée dans la console" lightbox="../media/console-log-custom.msft.png":::
       Message avec mise en forme personnalisée dans la **console**  
    :::image-end:::  
    
L’idée principale ici est que lorsque vous souhaitez enregistrer des messages dans la console à partir de votre JavaScript, vous utilisez l’une `console` des méthodes.  Chaque méthode formate les messages différemment.  

Il existe encore plus de méthodes que celles qui ont été démontrées dans cette section.  Ce didacticiel vous montre comment explorer le reste des méthodes.  

## <a name="view-messages-logged-by-the-browser"></a>Afficher les messages enregistrés par le navigateur  

Le navigateur enregistre également les messages dans la console.  Cela se produit généralement en cas de problème avec la page.  

1.  Choose **Cause 404**.  Le navigateur enregistre un code d’état HTTP d’erreur réseau, car le code JavaScript de la page a tenté d’extraire un fichier qui `404` n’existe pas.  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Une erreur 404 dans la console" lightbox="../media/console-cause-404.msft.png":::
       Une `404` erreur dans la **console**  
    :::image-end:::  
    
1.  Choose **Cause Error**.  Le navigateur enregistre un non-journal, car javaScript tente de mettre à jour un nœud DOM qui `TypeError` n’existe pas.  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="Un TypeError dans la console" lightbox="../media/console-cause-error.msft.png":::
       A `TypeError` dans la **console**  
    :::image-end:::  
    
1.  Sélectionnez **la dropdown Log Levels** (Niveaux du journal) et activez l’option **Verbose** si elle est désactivée.  Pour en savoir plus sur le filtrage, voir la section suivante.  Vous devez effectuer cette étape pour vous assurer que le message suivant que vous enregistrez est visible.  
    
    > [!NOTE]
    > Si la barre des niveaux par défaut est désactivée, vous devrez peut-être fermer la **barre** latérale de la console.  Filtrez par source de message ci-dessous pour plus d’informations sur la **barre** latérale de la console.
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Activation du niveau de journal détaillé" lightbox="../media/console-cause-error-log-levels.msft.png":::
       Activation du niveau de journal détaillé  
    :::image-end:::  
    
1.  Choose **Cause Violation**.  La page ne répond plus pendant quelques secondes, puis le navigateur enregistre le message `[Violation] 'click' handler took 3000ms` dans la console.  La durée exacte peut varier.  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Violation dans la console" lightbox="../media/console-cause-violation.msft.png":::
       Violation dans la **console**  
    :::image-end:::  
    
## <a name="filter-messages"></a>Filtrer les messages  

Sur certaines pages web, vous examinez la **console** et vous recevez des messages.  DevTools offre de nombreuses façons différentes de filtrer les messages qui ne sont pas pertinents pour la tâche en cours.  

### <a name="filter-by-log-level"></a>Filtrer par niveau de journal  

Chaque `console` méthode se voit attribuer un niveau de gravité : , , ou `Verbose` `Info` `Warning` `Error` .  Par exemple, `console.log()` il s’agit `Info` d’un message de niveau -level, tandis `console.error()` qu’il s’agit d’un `Error` message de niveau -.  

1.  Choose the **Log Levels** dropdown and disable **Errors**.  Un niveau est désactivé lorsqu’il n’y a plus de coche en regard.  Les `Error` messages de niveau -disparaissent.  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Désactiver les messages de niveau erreur dans la console" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       Désactiver les messages de niveau erreur dans la **console**  
    :::image-end:::  
    
1.  Sélectionnez de nouveau la dropdown **Log Levels** (Niveaux de journal) et ré-activez Errors **(Erreurs).**  Les `Error` messages de niveau réapparaissent.  

### <a name="filter-by-text"></a>Filtrer par texte  

Lorsque vous souhaitez afficher uniquement les messages qui incluent une chaîne exacte, tapez cette chaîne dans la **zone de** texte Filtrer.  

1.  Tapez `Dave` dans la zone **de** texte Filtrer.  Tous les messages qui n’incluent pas la `Dave` chaîne sont masqués.  Vous pouvez également passer en revue `Adolescent Irradiated Espionage Tortoises` l’étiquette.  Il s’agit d’un bogue.  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Filtrer les messages qui n’incluent pas Dave" lightbox="../media/console-all-messages-text-filter.msft.png":::
       Filtrer les messages qui n’incluent pas `Dave`  
    :::image-end:::  
    
1.  Supprimer `Dave` de la zone **de** texte Filtrer.  Tous les messages réapparaissent.  

### <a name="filter-by-regular-expression"></a>Filtrer par expression régulière  

Lorsque vous souhaitez afficher tous les messages qui incluent un modèle de texte, plutôt qu’une chaîne spécifique, utilisez une [expression régulière][MDNRegularExpressions].  

1.  Tapez `/^[AH]/` dans la zone **de** texte Filtrer.  Tapez le modèle [dans RegExr][|::ref1::|Main] pour obtenir une explication de ce qu’il fait.  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Filtrage de tous les messages qui ne correspondent pas à un modèle" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       Filtrage de tous les messages qui ne correspondent pas au modèle `/^[AH]/`  
    :::image-end:::  
    
1.  Supprimer `/^[AH]/` de la zone **de** texte Filtrer.  Tous les messages sont de nouveau visibles.  

### <a name="filter-by-message-source"></a>Filtrer par source de message  

Lorsque vous souhaitez afficher uniquement les messages provenant d’une URL spécifique, utilisez la **barre latérale**.  

1.  Choose **Show Console Sidebar** \( ![ Show Console Sidebar ][ImageShowConsoleSidebarIcon] \).  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="Barre latérale" lightbox="../media/console-sidebar-all-messages.msft.png":::
       Barre latérale  
    :::image-end:::  
    
1.  Sélectionnez **l’icône** Développer \( ![ Développer ][ImageExpandIcon] \) en de côté du nombre de messages.  Dans la figure suivante, le nombre de messages est indiqué en tant que **13 Messages**.  La **barre latérale affiche** la liste des URL à l’origine de la journalologie des messages.  Par exemple, `log.js` 11 messages ont été envoyés.  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Affichage de la source des messages dans la barre latérale" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       Affichage de la source des messages dans la barre latérale  
    :::image-end:::  
    
### <a name="filter-by-user-messages"></a>Filtrer par messages utilisateur  

Précédemment, lorsque vous choisissez **Log Info**, un script nommé pour enregistrer le message sur `console.log('Hello, Console!')` la console.  Les messages enregistrés à partir de JavaScript comme celui-ci sont nommés **messages d’utilisateur.**  En revanche, lorsque vous choisissez **Cause 404,** le navigateur enregistre un message de niveau -indiquant que la ressource demandée `Error` est in trouvée.  Les messages de ce genre sont considérés comme **des messages de navigateur.**  Utilisez la **barre latérale pour** filtrer les messages du navigateur et afficher uniquement les messages de l’utilisateur.  

1.  Choose **9 User Messages**.  Les messages du navigateur sont masqués.  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Filtrage des messages du navigateur" lightbox="../media/console-sidebar-user-messages.msft.png":::
       Filtrage des messages du navigateur  
    :::image-end:::  
    
1.  Choisissez **13 messages** pour afficher à nouveau tous les messages.  

## <a name="use-the-console-alongside-any-other-tools"></a>Utiliser la console avec tous les autres outils  

Si vous modifiez des styles, mais que vous devez rapidement vérifier le journal de la console, utilisez le caisse.  

1.  Choisissez **l’outil Éléments.**  
1.  Sélectionnez `Escape` .  **L’outil Console** dans **le caisse s’ouvre.**  Il comporte toutes les fonctionnalités du panneau Console que vous avez utilisé tout au long de ce didacticiel.  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="Outil Console dans le caisse" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         Outil **Console** dans le **caisse**  
    :::image-end:::  
    
## <a name="see-also"></a>Voir également  

*   Pour explorer d’autres fonctionnalités et flux de travail liés à l’interface utilisateur de la **console,** accédez à [Référence de console.][DevToolsConsoleApi]  
*   Pour en savoir plus sur toutes les méthodes démontrées dans Afficher les messages enregistrés à partir de JavaScript et explorer les autres méthodes non couvertes dans cet article, accédez à référence de `console` [](#view-messages-logged-from-javascript) `console` l’API console. [][DevToolsConsoleReference]  
<!--*   Navigate to [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  
     
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge \(Chromium\) | Documents Microsoft"  
[DevToolsCommandMenu]: ../command-menu/index.md "Exécuter des commandes avec le menu DevTools Command de Microsoft Edge | Documents Microsoft"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Modifier le placement de Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsConsoleApi]: ./api.md "Référence de l’API de console | Documents Microsoft"  
[DevToolsConsoleReference]: ./reference.md "Référence de la console | Documents Microsoft"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Mise en place de la journalisation des messages | Glitch"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expressions régulières | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Trace de pile : Wikipedia"  
> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/log) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
