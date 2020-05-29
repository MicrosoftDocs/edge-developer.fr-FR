---
title: Navigation dans Microsoft Edge DevTools avec la technologie d’assistance
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 5de27e46d20957a1be79f72cf36074291566e6e5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564978"
---
<!-- Copyright Rob Dodson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# Navigation dans Microsoft Edge DevTools avec la technologie d’assistance   



Ce guide a pour but d’aider les utilisateurs qui s’appuient essentiellement sur la technologie d’assistance comme les lecteurs d’écran à l’accès et à l’utilisation de Microsoft Edge DevTools.  Microsoft Edge DevTools est une suite d’outils de développement Web intégrés au navigateur Microsoft Edge.  <!--See [Accessibility Reference][DevtoolsAccessibilityReference] if you are looking for DevTools features related to improving the accessibility of a web page.  -->

<!--todo: add edge devtools index section when available  -->  
<!--todo: add reference (Accessibility Reference) section when available  -->  

L’accessibilité de DevTools est une opération en cours.  Certains panneaux et onglets fonctionnent mieux avec les technologies d’assistance.  Ce guide vous guide à travers les écrans qui sont les plus accessibles et met en surbrillance des problèmes spécifiques que vous pouvez rencontrer.  

## Présentation   

Avant de commencer, il est utile d’avoir un modèle mental illustrant la structure de l’interface utilisateur d’DevTools.  DevTools est divisé en une série de panneaux organisés au sein d’un [tableau `tablist` Aria ][W3CWaiAriaTablist].  

Exemple:  

*   Le panneau **éléments** vous permet d’afficher et de modifier des nœuds DOM ou [CSS] [DevtoolsCssIndex].  
*   **[DevtoolsConsoleIndex** ] permet de lire les journaux JavaScript et les objets de modification dynamique.  

<!--todo:  add dom nodes (dom nodes) section when available  -->  

Dans la zone de contenu de chaque panneau, il existe un certain nombre d’outils différents, souvent désignés sous le nom d’onglets ou de volets dans la documentation.  
Par exemple, le panneau **éléments** contient d’autres onglets pour inspecter les écouteurs d’événements, l’arborescence d’accessibilité, et bien plus encore.  La distinction entre les onglets et les volets est un peu arbitraire.  La seule raison pour laquelle il est possible que vous voyiez un terme ou l’autre consiste à assurer une cohérence avec le reste de la documentation relative au DevTools officiel.  

## Raccourcis clavier   

Les raccourcis clavier [DevTools] [DevtoolsShortcuts] sont des Cheatsheet utiles.  Prenez soin de la marquer et de vous y référer lorsque vous explorez les différents panneaux.  

## Ouvrir DevTools   

Pour commencer, consultez la [ouvrir Microsoft Edge DevTools] [DevtoolsOpen].  Il existe plusieurs façons d’ouvrir DevTools, à l’aide des raccourcis clavier ou des éléments de menu.  

## Naviguer entre les panneaux   

### Navigation à l’aide du clavier   

*   Avec devtools ouvert, appuyez sur `Control` + `]` \ (Windows \) ou `Command` + `]` \ (MacOS \) pour cibler le panneau suivant.  
*   `Control` + `[` Pour sélectionner le panneau précédent, appuyez sur \ (Windows \) ou `Command` + `[` \ (MacOS \).  
*   Il est également possible d’utiliser les `Shift` + `Tab` touches de direction pour déplacer le focus sur l’élément [ `tablist` Aria][W3CWaiAriaTablist] d’un panneau et utiliser les touches de direction pour modifier les panneaux, même s’il est plus rapide d’utiliser les raccourcis mentionnés précédemment.  

#### Problèmes connus   

*   Certains panneaux, tels que les panneaux **console** et **performance** , peuvent déplacer le focus dans la zone de contenu dès leur activation.  Cela risque de compliquer la navigation à l’aide des touches de direction.  
*   Le nom du panneau sélectionné est annoncé, mais uniquement après avoir lu le contenu prioritaire dans le panneau.  C’est aussi facile à manquer.  

### Navigation à l’aide du menu de commandes   

Pour vous concentrer sur un panneau spécifique, utilisez le [**menu de commandes**] [DevtoolsCommandMenuIndex]:  

1.  Avec devtools ouvert, appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.  
    Le **menu de commandes** est un élément ComboBox de saisie semi-automatique de recherche floue.  
1.  Entrez le nom du panneau que vous voulez ouvrir, puis utilisez le `Down Arrow` clavier visuel pour accéder à l’option appropriée.  
1.  Appuyez `Enter` pour exécuter une commande.  

Par exemple, pour ouvrir le panneau **éléments** :  

1.  Ouvrir le **menu de commandes**.  
1.  Tapez `E` ensuite `L` .  Option **panneau > afficher les éléments** sélectionnée  
1.  Appuyez `Enter` pour exécuter la commande qui ouvre le panneau.  

L’ouverture d’un panneau permet de transférer le focus sur le contenu du panneau.  Dans le cas du panneau d' **éléments** , le focus est déplacé vers l' **arborescence DOM**.  

## Panneau éléments   

### Inspecter un élément sur la page   

1.  Naviguez jusqu’à l’élément que vous voulez inspecter à l’aide du curseur dans le lecteur d’écran.  
1.  Simulez un clic droit sur l’élément pour ouvrir le menu contextuel.  
1.  Sélectionnez l’option **inspecter** .  Cette action ouvre le panneau d' **éléments** et le centre de l’élément dans l' **arborescence DOM**.  

<!--todo:  add dom nodes (elements pane) section when available  -->  

L' **arborescence DOM** est disposée en tant qu' [Aria `tree` ][W3CWaiAriaTree].  <!--See [Navigate the **DOM Tree** with a keyboard][DevtoolsDomIndexNavigateDomTreeKeyboard] for an example.  -->  

<!--todo: add dom index navigation tree section then available  -->

### Copiez le code d’un élément dans l’arborescence DOM.   

1.  Avec le focus sur un nœud dans l' **arborescence DOM**, afficher le menu contextuel.  
1.  Développez l’option **copier** .  
1.  Sélectionnez **Copy outerHTML**.  

#### Problèmes connus   

*   Dans le cas d’une **copie outerHTML** , le nœud actif ne doit pas être sélectionné, mais au lieu de cela, il sélectionne le nœud parent.  Toutefois, le contenu de l’élément doit toujours figurer dans le outerHTML copié.  

### Modifier les attributs d’un élément dans l’arborescence DOM   

*   Avec le focus sur un nœud dans l' **arborescence DOM**, appuyez sur `Enter` pour le rendre modifiable.  
*   Appuyez `Tab` pour vous déplacer entre les valeurs d’attribut.  Lorsque vous entendez «espace» vous vous trouvez à l’intérieur d’une entrée de texte vide et êtes en mesure de taper une nouvelle valeur d’attribut.  
*   `Control` + `Enter` `Command` + `Enter` Pour accepter la modification et entendre tout le contenu de l’élément, appuyez sur \ (Windows \) ou \ (MacOS \).  

#### Problèmes connus   

*   Lorsque vous tapez dans la saisie de texte, vous ne recevez aucune commentaires.  Si vous faites une faute de frappe et que vous utilisez les touches de direction pour explorer votre entrée, vous ne recevez pas de commentaires.  Le moyen le plus simple de vérifier votre tâche est d’accepter la modification, puis de surveiller l’intégralité de l’élément.  

### Modifier le code HTML d’un élément dans l’arborescence DOM   

*   Avec le focus sur un nœud dans l' **arborescence DOM**, appuyez sur `Enter` pour le rendre modifiable.  
*   Appuyez `Tab` pour vous déplacer entre les valeurs d’attribut.  Lorsque vous entendez le nom de l’élément, par exemple, «H2», vous vous trouvez à l’intérieur d’une entrée de texte et vous pouvez modifier le type de l’élément.  
*   Appuyez sur `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) pour accepter la modification.  

Par exemple, le fait de taper `h3` et d’appuyer sur `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) change les balises de début et de fin de l’élément en `h3` .  

## Onglets du panneau éléments   

Le panneau **éléments** contient d’autres onglets permettant d’inspecter les éléments tels que la feuille de style CSS appliquée à un élément ou l’emplacement approprié dans l’arborescence accessibilité.  

*   Avec le focus sur un nœud dans l' **arborescence DOM**, appuyez `Tab` jusqu’à ce que vous entendiez que le volet **styles** est sélectionné.  
*   Utilisez la `Right Arrow` pour explorer d’autres onglets disponibles.  

L' **arborescence DOM** transforme les éléments à l’aide d' `href` attributs en liens pouvant être actifs; il est donc possible que vous deviez appuyer `Tab` plusieurs fois pour accéder au volet **styles** .  

### Problèmes connus   

Les onglets de **Propriétés** et de points de passe **DOM** ne sont pas accessibles via le clavier.  

### Volet styles   

Dans le volet **styles** , recherchez des contrôles pour le filtrage des styles, le basculement vers les États des éléments \ (par exemple [`:active`][MDNActive] et [`:focus`][MDNFocus] \), le basculement entre les classes et l’ajout de nouvelles classes.  Il existe également un outil d’inspection des styles puissant permettant d’explorer et de modifier les styles actuellement appliqués à l’élément qui a le focus dans l' **arborescence DOM**.  

Le principal concept à comprendre à propos du volet **styles** est qu’il affiche uniquement les styles du nœud actuellement sélectionné dans l' **arborescence DOM**.  Par exemple, supposons que vous ayez vérifié les styles d’un `<header>` nœud et que vous voulez maintenant consulter les styles d’un `<footer>` nœud.  Pour ce faire, vous devez d’abord sélectionner le `<footer>` nœud dans l' **arborescence DOM**.  Vous constaterez peut-être qu’il est plus rapide d’utiliser le flux de travail [Inspect](#inspect-an-element-on-the-page) pour examiner un nœud qui se trouve à proximité du `footer` nœud \ (par exemple, un lien dans le pied de page \), qui Centre l' **arborescence DOM**, puis utilisez votre clavier pour accéder au nœud exact qui vous intéresse.  

#### Naviguer dans le volet styles   

Dans la mesure où tous les outils de style se connectent d’une façon ou d’une autre dans le volet **styles** , il est préférable d’abord de mettre en avant ce outil.  

*   Le focus étant placé sur le volet **styles** , appuyez sur `Tab` pour déplacer le focus à l’intérieur et explorer le contenu.  
*   Appuyez sur `Tab` jusqu’à ce que le premier style devienne actif.  Si vous utilisez un lecteur d’écran, le premier style est annoncé comme suit: «élément. style {} ».  
*   Appuyez `Down Arrow` pour parcourir la liste des styles par ordre de spécificité.  Un lecteur d’écran annonce chaque style en commençant par le nom du fichier CSS, le numéro de ligne sur lequel apparaît le style et le nom du style.  Par exemple: "main. CSS: 233. card__img {} "  
*   `Enter`Pour plus d’informations, appuyez sur pour vérifier un style.  Le focus commence sur une version modifiable du nom du style.  
*   Appuyez `Tab` pour passer d’une version éditable à une autre de chaque propriété CSS et leurs valeurs correspondantes.  À la fin de chaque bloc de style s’agit d’un champ de texte modifiable vierge que vous pouvez utiliser pour ajouter des propriétés CSS supplémentaires.  
*   Vous pouvez continuer d’appuyer sur `Tab` pour parcourir la liste des styles ou appuyer sur `Escape` pour quitter ce mode et revenir à la navigation à l’aide des touches de direction.  

Assurez-vous de lire le Guide [Guide de référence clavier du volet styles] [DevtoolsShortcutsStylesPaneKeyboard] pour afficher d’autres raccourcis.  

##### Problèmes connus   

*   Si vous utilisez le champ de texte modifiable **filtre** , vous n’êtes plus en mesure de parcourir la liste des styles.  

#### Changer l’état de l’élément   

Pour activer ou désactiver l’état d’un élément, par `:active` exemple `:focus` :  

1.  Accédez au volet **styles** , puis appuyez sur `Tab` jusqu’à ce que le bouton **afficher l’État** de l’élément soit actif.  
1.  Appuyez `Enter` pour développer la collection d’États d’éléments.  Les États des éléments s’affichent sous la forme d’un groupe de cases à cocher.  
1.  Appuyez sur `Tab` jusqu’à ce que le premier état `:active` ait le focus.  
1.  Appuyez sur `Space` pour l’activer.  Le style de l’élément actuellement sélectionné dans l’arborescence DOM `:active` est désormais appliqué.  
1.  Continuez `Tab` d’appuyer sur pour explorer tous les États disponibles.  

#### Ajouter une classe existante   

Adjacent au bouton **afficher l’État** de l’élément est le bouton **classes d’éléments** .  Positionnez le focus sur celui-ci en appuyant sur la touche `Tab` `Enter` .  Le focus se déplace dans un champ de texte d’édition intitulé **Ajouter une nouvelle classe**.  

Le bouton **classes d’éléments** est principalement utilisé pour ajouter des classes existantes à un élément.  Par exemple, si votre feuille de style contenait une classe d’assistance nommée `.clearfix` , vous pouvez appuyer `.` dans le champ de texte modifier pour afficher une liste de suggestions de classes et utiliser la `Down Arrow` pour trouver la `.clearfix` suggestion.  Vous pouvez également taper le nom de la classe vous-même et appuyer sur l' `Enter` application.  

#### Ajouter une nouvelle règle de style   

Adjacent au bouton **classes d’éléments** correspond au bouton **nouvelle règle de style** .  Positionnez le focus sur celui-ci en appuyant et en appuyant `Tab` sur `Enter` .  Le focus se déplace dans un champ de texte modifiable dans l’inspecteur de style.  Le contenu du texte initial du champ correspond au nom de balise de l’élément sélectionné dans l' **arborescence DOM**.  
Vous pouvez taper le nom de la classe souhaité dans ce champ, puis appuyer sur `Tab` pour lui affecter des propriétés CSS.  

### Onglet calculé   

Le focus étant placé sur l’onglet **calculé** , appuyez `Tab` pour déplacer le focus à l’intérieur et explorer le contenu.  Dans l’onglet **calculé** , il existe des contrôles pour explorer les propriétés CSS qui sont réellement appliquées à un élément selon l’ordre de la spécificité.  

<!--todo: add computed tab section when available  -->  

#### Découvrir tous les styles calculés   

Appuyez sur `Tab` jusqu’à atteindre la collection de styles calculés.  Celles-ci s’affichent sous la forme d’un [Aria `tree` ][W3CWaiAriaTree].  Le développement d’une classe ListBox révèle les sélecteurs de CSS qui appliquent le style calculé.  Ces sélecteurs sont organisés par spécificité.  Un lecteur d’écran annonce la valeur calculée, le sélecteur CSS actuellement correspondant, le nom de fichier de la feuille de style qui contient le sélecteur et le numéro de ligne pour le sélecteur.  

#### Problèmes connus   

*   Si vous utilisez le champ de texte **filtre** , il n’est plus possible d’inspecter les styles.  

### Onglet écouteur d’événements   

Dans le panneau d' **éléments** , vous pouvez examiner les écouteurs d’événements appliqués à un élément à l’aide de l’onglet **écouteurs d’événements** .  Avec le focus dans le volet **styles** , appuyez sur `Right Arrow` pour accéder à l’onglet **écouteur d’événements** .  

#### Explorer les détecteurs d’événements   

Les détecteurs d’événements s’affichent sous forme de [Aria `tree` ][W3CWaiAriaTree].  Vous pouvez utiliser les touches de direction pour les parcourir.  Un lecteur d’écran annonce le nom de l’objet DOM auquel l’écouteur d’événements est attaché, ainsi que le nom du fichier dans lequel l’écouteur d’événements est défini et le numéro de ligne.  

### Volet accessibilité   

Le focus étant placé sur le volet **accessibilité** , appuyez sur `Tab` pour déplacer le focus à l’intérieur et explorer le contenu.  Dans le volet **accessibilité** , il existe des contrôles pour explorer l’arborescence d’accessibilité, les attributs Aria appliqués à un élément et les propriétés d’accessibilité calculées.  

<!--todo: add reference (Accessibility pane) section when available  -->  

#### Arborescence d’accessibilité   

L' **arborescence d’accessibilité** s’affiche sous la forme d’une expression [Aria `tree` ][W3CWaiAriaTree] qui `treeitem` correspond chacune à un élément du DOM.  L’arborescence annonce le rôle calculé pour le nœud sélectionné.  Éléments génériques comme `div` et `span` annoncés sous la forme «GenericContainer» dans l’arborescence.  Utilisez les touches de direction pour parcourir l’arborescence et explorer les relations parent-enfant.  

#### Problèmes connus   

*   Le type de [Aria `tree` ][W3CWaiAriaTree] utilisé par le volet **accessibilité** risque de ne pas être correctement exposé dans Microsoft Edge pour les lecteurs d’écran MacOS tels que VoiceOver.  Abonnez-vous [#868480 problème de chrome][ChromiumIssues868480] pour être informé de la progression de ce problème.  
*   Chacun des sections d' **attributs Aria** et de **propriétés calculées** sont marqués en tant [que `tree` Aria ][W3CWaiAriaTree], mais chacun n’a pas de gestion du focus et ne fonctionne pas avec le clavier.  

## Panneau d’audit   

Le panneau **d’audit** vous devez exécuter une série de tests sur un site pour vérifier les problèmes courants liés à la performance, l’accessibilité, le SEO et un certain nombre d’autres catégories.  

### Configuration et exécution d’un audit   

1.  Lorsque le panneau **audits** est ouvert pour la première fois, le focus est placé sur le bouton **exécuter l’audit** à la fin du formulaire.  Par défaut, le formulaire est configuré pour exécuter des audits pour chaque catégorie à l’aide de l’émulation mobile sur une connexion 3G simulée.  
1.  Utilisez `Shift` + `Tab` ou revenez en mode navigation pour modifier les paramètres d’audit.  
1.  Lorsque vous êtes prêt à exécuter l’audit, revenez au bouton **exécuter l’audit** et appuyez sur `Enter` .  
1.  Le focus se déplace dans une fenêtre modale avec un bouton d' **annulation** qui vous permet de quitter l’audit.  Il est possible que vous entendiez une série de earcons pendant que l’audit s’exécute et actualise la page plusieurs fois.  

#### Problèmes connus   

*   Les différentes sections du formulaire de configuration ne sont pas actuellement marquées avec un `fieldset` élément.  Il est parfois plus facile de naviguer à l’aide du mode navigation pour déterminer les contrôles associés à chaque section.  
*   Il n’y a aucune annonce de earcon ou de région en direct lorsque l’audit est terminé.  En règle générale, vous devez être en mesure de parcourir les résultats de 30 secondes.  L’utilisation du mode navigation est le moyen le plus simple d’accéder aux résultats.  

### Parcourir le rapport d’audit   

Le rapport d’audit est organisé en sections correspondant à chacune des catégories d’audit.  Le rapport s’ouvre et affiche une liste de notes pour chaque catégorie.  Ces résultats sont également des liens qui peuvent être utilisés pour passer aux sections pertinentes.  Dans chaque section se trouvent des éléments pouvant être développés `details` , qui contiennent des informations relatives aux audits réussis ou failés.  Par défaut, seuls les audits qui échouent apparaissent.  Chaque section se termine par un `details` élément final qui contient tous les audits transmis.  

Pour effectuer un nouvel audit, utilisez `Shift` + `Tab` pour quitter le rapport et recherchez le bouton **effectuer un audit** .  

## Commentaires   

*   Envoyez des rapports de bogue DevTools ou des demandes de fonctionnalité au [suivi des problèmes de chrome][MonorailChromiumIssues].  
*   Envoyez des commentaires relatifs à ce document à [GitHub][GithubEdgeDeveloperNewIssue].  

<!-- image links -->  

<!-- links -->  

<!--[DevtoolsAccessibilityReference]: reference.md "Accessibility Reference"  -->  
<!--[DevtoolsAccessibilityReferencePane]: reference.md#the-accessibility-pane "The Accessibility pane - Accessibility Reference"  -->  

<!--[MicrosoftEdgeDevtoolsIndex]: ../index.md "Microsoft Edge DevTools"  -->  
[DevtoolsCommandMenuIndex]: .. /Command-menu/index.MD "exécuter les commandes à l’aide du menu de commandes Microsoft Edge DevTools"  
[DevtoolsConsoleIndex]: .. /Console/index.MD "présentation de la console"  
[DevtoolsCssIndex]: .. /CSS/index.MD "découvrir comment afficher et modifier des feuilles CSS"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get Started With Viewing And Changing The DOM"  -->  
<!--[DevtoolsDomIndexNavigateDomTreeKeyboard]: ../dom/index.md#navigate-the-dom-tree-with-a-keyboard "Navigate the DOM Tree with a keyboard - Get Started With Viewing And Changing The DOM"  -->
[DevtoolsOpen]: .. /open.md "Ouvrez Microsoft Edge DevTools"  
[DevtoolsShortcuts]: .. /shortcuts.md "raccourcis clavier de Microsoft Edge DevTools"  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /Shortcuts.MD # styles-volet-raccourcis clavier-raccourcis clavier pour le volet de styles-raccourcis clavier de Microsoft Edge DevTools "  

[ChromiumIssues868480]: https://bugs.chromium.org/p/chromium/issues/detail?id=868480 "Problème 868480-exposer les arborescences ARIA sous forme de tableaux dans l’accessibilité Mac"  
[GithubEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Docs%20Feedback%5D "Nouveau problème-MicrosoftDocs/Edge-développeur | GitHub"  
[MDNActive]: https://developer.mozilla.org/docs/Web/CSS/:active ": actif | MDN"  
[MDNFocus]: https://developer.mozilla.org/docs/Web/CSS/:focus ": Focus | MDN"  
[MonorailChromiumIssues]: https://crbug.com "Problèmes-chrome-monorail"  
[W3CWaiAriaTablist]: https://www.w3.org/TR/wai-aria-1.1/#tablist "TabList (rôle)-applications Internet riches accessibles (WAI-ARIA) 1,1 | W3C"  
[W3CWaiAriaTree]: https://www.w3.org/TR/wai-aria-1.1/#tree "arborescence (rôle)-applications Internet riches accessibles (WAI-ARIA) 1,1 | W3C"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) et est créée par [Rob Dodson][RobDodson] \ (Contributor, Google Web Fundamentals).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[RobDodson]: https://developers.google.com/web/resources/contributors/robdodson  
