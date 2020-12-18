---
description: Guide sur la navigation dans Microsoft Edge DevTools à l’aide de technologies d’assistance telles que les lecteurs d’écran.
title: Navigation dans Microsoft Edge DevTools avec la technologie d’assistance
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: d72c856e9136291e9255b3784aad7c6cd99f92fc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230809"
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

L’article suivant a pour but de permettre aux utilisateurs qui s’appuient essentiellement sur la technologie d’assistance comme les lecteurs d’écran d’accéder et d’utiliser [Microsoft Edge devtools][MicrosoftEdgeDevtoolsMain].  [Microsoft Edge devtools][MicrosoftEdgeDevtoolsMain] est une suite d’outils de développement Web intégrés au navigateur Microsoft Edge.  Si vous recherchez des fonctionnalités DevTools liées à l’amélioration de l’accessibilité d’une page Web, accédez à référence sur l' [accessibilité][DevtoolsAccessibilityReference].  

L’accessibilité de DevTools est une opération en cours.  Certains panneaux et onglets fonctionnent mieux avec les technologies d’assistance.  Ce guide vous guide à travers les écrans qui sont les plus accessibles et met en surbrillance des problèmes spécifiques que vous pouvez rencontrer.  

## Vue d'ensemble  

Avant de commencer, il est utile d’avoir un modèle mental illustrant la structure de l’interface utilisateur d’DevTools.  DevTools est divisé en une série de panneaux organisés en [TabList Aria][W3CWaiAriaTablist].  

Par exemple:  

*   Le panneau **éléments** vous permet d’accéder à [afficher et modifier les nœuds DOM] [DevtoolsDomIndexNavigateDomTreeKeyboard] ou [CSS][DevtoolsCssIndex].  
*   Le [panneau Console][DevtoolsConsoleIndex] vous permet de lire les journaux JavaScript et de modifier les objets dynamiques.  

Dans la zone de contenu de chaque panneau, il existe un certain nombre d’outils différents, souvent désignés sous le nom d’onglets ou de volets dans la documentation.  
Par exemple, le panneau **éléments** contient d’autres onglets pour inspecter les écouteurs d’événements, l’arborescence d’accessibilité, et bien plus encore.  La distinction entre les onglets et les volets est un peu arbitraire.  La seule raison pour laquelle il est possible que vous deviez examiner un terme ou l’autre consiste à assurer une cohérence avec le reste de la documentation officielle DevTools.  

## Raccourcis clavier  

Les raccourcis clavier [DevTools] [DevtoolsShortcuts] sont des Cheatsheet utiles.  Prenez soin de la marquer et de vous y référer lorsque vous explorez les différents panneaux.  

## Ouvrir DevTools  

Pour commencer, accédez à [ouvrez Microsoft Edge DevTools] [DevtoolsOpen].  Il existe plusieurs façons d’ouvrir DevTools, à l’aide des raccourcis clavier ou des éléments de menu.  

## Naviguer entre les panneaux  

### Navigation à l’aide du clavier  

*   Avec devtools ouvert, sélectionnez `Control` + `]` \ (Windows, Linux \) ou `Command` + `]` \ (MacOS \) pour cibler le panneau suivant.  
*   Sélectionnez `Control` + `[` \ (Windows, Linux \) ou `Command` + `[` \ (MacOS \) pour cibler le panneau précédent.  
*   Il est également possible d’utiliser le `Shift` + `Tab` pour déplacer le focus vers l' [TabList Aria][W3CWaiAriaTablist] d’un panneau et utiliser les touches de direction pour modifier les panneaux, même s’il peut être plus rapide d’utiliser les raccourcis mentionnés précédemment.  

**Problèmes connus**  

*   Certains panneaux, tels que les panneaux **console** et **performance** , risquent de déplacer le focus dans la zone de contenu du panneau dès que chaque panneau est activé.  Cela risque de compliquer la navigation à l’aide des touches de direction.  
*   Le nom du panneau sélectionné est annoncé, mais uniquement après avoir lu le contenu prioritaire dans le panneau.  C’est aussi facile à manquer.  

### Navigation à l’aide du menu de commandes  

Pour vous concentrer sur un panneau spécifique, utilisez le [menu de commandes][DevtoolsCommandMenuIndex]:  

1.  Avec devtools ouvert, sélectionnez `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.  
    Le **menu de commandes** est un élément ComboBox de saisie semi-automatique de recherche floue.  
1.  Entrez le nom du panneau que vous voulez ouvrir, puis utilisez le `Down Arrow` clavier visuel pour accéder à l’option appropriée.  
1.  Sélectionnez `Enter` pour exécuter une commande.  

Procédez comme suit pour ouvrir le panneau **éléments** .  

1.  Ouvrir le **menu de commandes**.  
1.  Tapez `E` ensuite `L` .  Option **panneau > afficher les éléments** sélectionnée  
1.  Sélectionnez cette option `Enter` pour exécuter la commande qui ouvre le panneau.  

L’ouverture d’un panneau permet de transférer le focus sur le contenu du panneau.  Dans le cas du panneau d' **éléments** , le focus est déplacé vers l' **arborescence DOM**.  

## Panneau éléments  

### Inspecter un élément sur la page  

1.  Naviguez jusqu’à l’élément que vous voulez inspecter à l’aide du curseur dans le lecteur d’écran.  
1.  Simulez un clic avec le bouton droit sur l’élément pour ouvrir le menu contextuel.  
1.  Sélectionnez l’option **inspecter** .  Cet élément [ouvre le panneau éléments et il a pour but de concentrer l’élément dans l’arborescence DOM] [DevtoolsDomIndexViewDomNodes].  

L' **arborescence DOM** est disposée en tant qu' [arborescence Aria][W3CWaiAriaTree].  Pour obtenir un exemple, naviguez jusqu’à [naviguez dans l' **arborescence DOM** à l’aide d’un clavier] [DevtoolsDomIndexNavigateDomTreeKeyboard].  

### Copiez le code d’un élément dans l’arborescence DOM.  

1.  Avec le focus positionné sur un nœud dans l' **arborescence DOM**, pointez sur le nœud et ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \).  
1.  Développez l’option **copier** .  
1.  Sélectionnez **Copy outerHTML**.  

**Problèmes connus**  

*   Dans le cas d’une **copie outerHTML** , le nœud actif ne doit pas être sélectionné, mais au lieu de cela, il sélectionne le nœud parent.  Toutefois, le contenu de l’élément doit toujours figurer dans le outerHTML copié.  

### Modifier les attributs d’un élément dans l’arborescence DOM  

*   Avec le focus sur un nœud dans l' **arborescence DOM**, sélectionnez `Enter` pour le rendre modifiable.  
*   `Tab`Pour vous déplacer entre les valeurs d’attribut.  Lorsque vous entendez «espace» vous vous trouvez à l’intérieur d’une entrée de texte vide et êtes en mesure de taper une nouvelle valeur d’attribut.  
*   `Control` + `Enter` `Command` + `Enter` Pour accepter la modification et entendre tout le contenu de l’élément, sélectionnez \ (Windows, Linux \) ou \ (MacOS \).  

**Problèmes connus**  

*   Lorsque vous tapez dans la saisie de texte, vous ne recevez aucune commentaires.  Si vous faites une faute de frappe et que vous utilisez les touches de direction pour explorer votre entrée, vous ne recevez pas de commentaires.  Le moyen le plus simple de vérifier votre tâche est d’accepter la modification, puis de surveiller l’intégralité de l’élément.  

### Modifier le code HTML d’un élément dans l’arborescence DOM  

*   Avec le focus sur un nœud dans l' **arborescence DOM**, sélectionnez `Enter` pour le rendre modifiable.  
*   `Tab`Pour vous déplacer entre les valeurs d’attribut.  Lorsque vous entendez le nom de l’élément, par exemple, `h2` vous vous trouvez à l’intérieur d’une entrée de texte et risquez de changer le type de l’élément.  
*   Sélectionnez `Control` + `Enter` \ (Windows, Linux \) ou `Command` + `Enter` \ (MacOS \) pour accepter la modification.  

Par exemple, lorsque vous tapez `h3` et sélectionnez `Control` + `Enter` \ (Windows, Linux \) ou `Command` + `Enter` \ (MacOS \), les balises de début et de fin de l' `h3` élément changent.  

## Onglets du panneau éléments  

Le panneau **éléments** contient d’autres onglets permettant d’inspecter les éléments tels que la feuille de style CSS appliquée à un élément ou l’emplacement approprié dans l’arborescence accessibilité.  

*   Avec le focus sur un nœud dans l' **arborescence DOM**, sélectionnez `Tab` jusqu’à ce que vous entendiez que le volet **styles** est sélectionné.  
*   Utilisez la `Right Arrow` pour explorer d’autres onglets disponibles.  

L' **arborescence DOM** transforme les éléments à l’aide d' `href` attributs en liens pouvant être actifs; vous devrez donc sélectionner `Tab` plusieurs fois pour atteindre le volet **styles** .  

**Problèmes connus**  

Les onglets de **Propriétés** et de points de passe **DOM** ne sont pas accessibles via le clavier.  

### Volet styles  

Dans le volet **styles** , recherchez des contrôles pour le filtrage des styles, en basculant vers les États des éléments \ (par exemple, [actif][MDNActive] et [: Focus][MDNFocus]\), le basculement entre les classes et l’ajout de nouvelles classes.  Il existe également un outil d’inspection des styles puissant permettant d’explorer et de modifier les styles actuellement appliqués à l’élément qui a le focus dans l' **arborescence DOM**.  

Le principal concept à comprendre à propos du volet **styles** est qu’il affiche uniquement les styles du nœud actuellement sélectionné dans l' **arborescence DOM**.  Par exemple, supposons que vous ayez vérifié les styles d’un `<header>` nœud et que vous voulez maintenant consulter les styles d’un `<footer>` nœud.  Pour ce faire, vous devez d’abord sélectionner le `<footer>` nœud dans l' **arborescence DOM**.  Vous constaterez peut-être qu’il est plus rapide d’utiliser le flux de travail [Inspect](#inspect-an-element-on-the-page) pour examiner un nœud qui se trouve à proximité du `footer` nœud \ (par exemple, un lien dans le pied de page \), qui Centre l' **arborescence DOM**, puis utilisez votre clavier pour accéder au nœud exact qui vous intéresse.  

#### Naviguer dans le volet styles  

Dans la mesure où tous les outils de style se connectent d’une façon ou d’une autre dans le volet **styles** , il est préférable de commencer par être un expert de cet outil.  

*   Le focus étant placé sur le volet **styles** , sélectionnez `Tab` pour déplacer le focus à l’intérieur et explorer le contenu.  
*   Sélectionnez `Tab` jusqu’à ce que le premier style devienne actif.  Si vous utilisez un lecteur d’écran, le premier style est annoncé comme suit `element.style {}` :  
*   `Down Arrow`Pour parcourir la liste des styles par ordre de spécificité.  Un lecteur d’écran annonce chaque style en commençant par le nom du fichier CSS, le numéro de ligne sur lequel apparaît le style et le nom du style.  Exemple : `main.css:233 .card__img {}`.  
*   `Enter`Pour plus d’informations, sélectionnez un style.  Le focus commence sur une version modifiable du nom du style.  
*   `Tab`Pour vous déplacer entre les versions modifiables de chaque propriété CSS et les valeurs correspondantes.  À la fin de chaque bloc de style s’agit d’un champ de texte modifiable vierge que vous pouvez utiliser pour ajouter des propriétés CSS supplémentaires.  
*   Il est possible que vous deviez sélectionner `Tab` pour parcourir la liste des styles ou sélectionner `Escape` pour quitter le mode et revenir à la navigation à l’aide des touches de direction.  

Pour accéder à d’autres raccourcis, accédez à [Référence du clavier du volet styles] [DevtoolsShortcutsStylesPaneKeyboard].  

**Problèmes connus**  

*   Si vous utilisez le champ de texte modifiable **filtre** , vous n’êtes plus en mesure de parcourir la liste des styles.  

#### Changer l’état de l’élément  

Pour activer ou désactiver l’état d’un élément, par `:active` exemple `:focus` :  

1.  Accédez au volet **styles** et sélectionnez `Tab` jusqu’à ce que le bouton afficher l’état de l' **élément bascule** soit actif.  
1.  Sélectionnez `Enter` pour développer la collection d’États des éléments.  Les États des éléments s’affichent sous la forme d’un groupe de cases à cocher.  
1.  Sélectionnez `Tab` jusqu’à ce que le premier état `:active` ait le focus.  
1.  Sélectionnez `Space` pour l’activer.  Le style de l’élément actuellement sélectionné dans l’arborescence DOM `:active` est désormais appliqué.  
1.  Prenez connaissance `Tab` de tous les États disponibles.  

#### Ajouter une classe existante  

Adjacent au bouton **afficher l’État** de l’élément est le bouton **classes d’éléments** .  Pour y placer le focus, sélectionnez `Tab` et sélectionnez `Enter` .  Le focus se déplace dans un champ de texte d’édition intitulé **Ajouter une nouvelle classe**.  

Le bouton **classes d’éléments** est principalement utilisé pour ajouter des classes existantes à un élément.  Par exemple, si votre feuille de style contenait une classe d’assistance nommée `.clearfix` , vous pouvez sélectionner `.` dans le champ de texte modifier pour afficher une liste de suggestions de classes et utiliser la `Down Arrow` pour trouver la `.clearfix` suggestion.  Vous pouvez également entrer le nom de la classe vous-même, puis sélectionner l' `Enter` appliquer.  

#### Ajouter une nouvelle règle de style  

Adjacent au bouton **classes d’éléments** correspond au bouton **nouvelle règle de style** .  Pour y placer le focus, sélectionnez `Tab` et sélectionnez `Enter` .  Le focus se déplace dans un champ de texte modifiable dans l’inspecteur de style.  Le contenu du texte initial du champ correspond au nom de balise de l’élément sélectionné dans l' **arborescence DOM**.  
Vous pouvez taper le nom de la classe souhaité dans ce champ, puis sélectionner `Tab` lui affecter des propriétés CSS.  

### Onglet calculé  

Le focus étant placé sur l’onglet **calculé** , sélectionnez `Tab` pour déplacer le focus à l’intérieur et explorer le contenu.  Dans l’onglet **calculé** , il existe des contrôles pour explorer les propriétés CSS qui sont réellement appliquées à un élément selon l’ordre de la spécificité.  

<!--todo: add computed tab section when available  -->  

#### Découvrir tous les styles calculés  

Sélectionnez `Tab` jusqu’à atteindre la collection de styles calculés.  Celles-ci s’affichent sous la forme d’une [arborescence Aria][W3CWaiAriaTree].  Le développement d’une classe ListBox révèle les sélecteurs de CSS qui appliquent le style calculé.  Ces sélecteurs sont organisés par spécificité.  Un lecteur d’écran annonce la valeur calculée, le sélecteur CSS actuellement correspondant, le nom de fichier de la feuille de style qui contient le sélecteur et le numéro de ligne pour le sélecteur.  

**Problèmes connus**  

*   Si vous utilisez le champ de texte **filtre** , il n’est plus possible d’inspecter les styles.  

### Onglet écouteur d’événements  

Dans le panneau d' **éléments** , vous pouvez examiner les écouteurs d’événements appliqués à un élément à l’aide de l’onglet **écouteurs d’événements** .  Avec le focus dans le volet **styles** , sélectionnez les `Right Arrow` pour accéder à l’onglet **écouteurs d’événements** .  

#### Explorer les détecteurs d’événements  

Les détecteurs d’événements s’affichent sous forme d' [arborescence Aria][W3CWaiAriaTree].  Vous pouvez utiliser les touches de direction pour les parcourir.  Un lecteur d’écran annonce le nom de l’objet DOM auquel l’écouteur d’événements est attaché, ainsi que le nom du fichier dans lequel l’écouteur d’événements est défini et le numéro de ligne.  

### Volet accessibilité  

Le focus étant placé sur le volet **accessibilité** , sélectionnez `Tab` pour déplacer le focus à l’intérieur et explorer le contenu.  Dans le [volet accessibilité][DevtoolsAccessibilityReference] , il existe des contrôles pour explorer l’arborescence d’accessibilité, les attributs Aria appliqués à un élément et les propriétés d’accessibilité calculées.  

#### Arborescence d’accessibilité  

L' **arborescence d’accessibilité** s’affiche sous la forme d’une [arborescence Aria][W3CWaiAriaTree] qui `treeitem` correspond à un élément du DOM.  L’arborescence annonce le rôle calculé pour le nœud sélectionné.  Éléments génériques comme `div` et `span` annoncés sous la forme «GenericContainer» dans l’arborescence.  Utilisez les touches de direction pour parcourir l’arborescence et explorer les relations parent-enfant.  

**Problèmes connus**  

*   Le type d' [arborescence Aria][W3CWaiAriaTree] utilisé par le volet **accessibilité** risque de ne pas être correctement exposé dans Microsoft Edge pour les lecteurs d’écran MacOS tels que VoiceOver.  Abonnez-vous [#868480 problème de chrome][ChromiumIssues868480] pour être informé de la progression de ce problème.  
*   Chacun des sections d' **attributs Aria** et de **propriétés calculées** sont marqués en tant qu' [arborescence Aria][W3CWaiAriaTree], mais chacun n’a pas de gestion du focus et ne fonctionne pas avec le clavier.  

## Panneau d’audit  

Le panneau **d’audit** vous devez exécuter une série de tests sur un site pour vérifier les problèmes courants liés à la performance, l’accessibilité, le SEO et un certain nombre d’autres catégories.  

### Configuration et exécution d’un audit  

1.  Lorsque le panneau **audits** est ouvert pour la première fois, le focus est placé sur le bouton **exécuter l’audit** à la fin du formulaire.  Par défaut, le formulaire est configuré pour exécuter des audits pour chaque catégorie à l’aide de l’émulation mobile sur une connexion 3G simulée.  
1.  Utilisez `Shift` + `Tab` ou revenez en mode navigation pour modifier les paramètres d’audit.  
1.  Lorsque vous êtes prêt à exécuter l’audit, revenez au bouton **exécuter l’audit** et sélectionnez `Enter` .  
1.  Le focus se déplace dans une fenêtre modale avec un bouton d' **annulation** qui vous permet de quitter l’audit.  Il est possible que vous entendiez une série de earcons pendant que l’audit s’exécute et actualise la page plusieurs fois.  

**Problèmes connus**  

*   Les différentes sections du formulaire de configuration ne sont pas actuellement marquées avec un `fieldset` élément.  Il est parfois plus facile de naviguer à l’aide du mode navigation pour déterminer les contrôles associés à chaque section.  
*   Il n’y a aucune annonce de earcon ou de région en direct lorsque l’audit est terminé.  En règle générale, vous devez être en mesure de parcourir les résultats de 30 secondes.  L’utilisation du mode navigation est le moyen le plus simple d’accéder aux résultats.  

### Parcourir le rapport d’audit  

Le rapport d’audit est organisé en sections correspondant à chacune des catégories d’audit.  Le rapport s’ouvre et affiche une liste de notes pour chaque catégorie.  Ces résultats sont également des liens qui peuvent être utilisés pour passer aux sections pertinentes.  Dans chaque section se trouvent des éléments pouvant être développés `details` , qui contiennent des informations relatives aux audits réussis ou failés.  Par défaut, seuls les audits qui échouent apparaissent.  Chaque section se termine par un `details` élément final qui contient tous les audits transmis.  

Pour effectuer un nouvel audit, utilisez `Shift` + `Tab` pour quitter le rapport et recherchez le bouton **effectuer un audit** .  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsAccessibilityReference]: ./reference.md "Référence d’accessibilité | Documents Microsoft"  
[DevtoolsAccessibilityReferencePane]: reference.md#the-accessibility-pane "Volet accessibilité-référence de l’accessibilité | Documents Microsoft"  
[MicrosoftEdgeDevtoolsMain]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsConsoleIndex]: ../console/index.md "Présentation de la console | Documents Microsoft"  
[DevtoolsCssIndex]: ../css/index.md "Découvrir comment afficher et modifier des feuilles CSS | Documents Microsoft"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element | Microsoft Docs"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get started with viewing and changing the DOM | Microsoft Docs"  -->  
[DevtoolsDomIndexViewDomNodes]: .. /Dom/index.MD # View-DOM-Nodes "afficher les nœuds DOM-découvrir comment afficher et modifier le DOM | Documents Microsoft  
[DevtoolsDomIndexNavigateDomTreeKeyboard]: .. /Dom/index.MD # navigation------------------------------------------------- Documents Microsoft  
[DevtoolsOpen]: .. /Open/index.MD "Ouvrez Microsoft Edge DevTools | Documents Microsoft  
[DevtoolsShortcuts]: .. /shortcuts/index.MD "raccourcis clavier Microsoft Edge DevTools | Documents Microsoft  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /shortcuts/index.MD # styles-volet-raccourcis clavier-raccourcis clavier du volet de styles-raccourcis clavier de Microsoft Edge DevTools | Documents Microsoft  

[ChromiumIssues868480]: https://bugs.chromium.org/p/chromium/issues/detail?id=868480 "Problème 868480-exposer les arborescences ARIA sous forme de tableaux dans l’accessibilité Mac"  

[GithubEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Docs%20Feedback%5D "Nouveau problème-MicrosoftDocs/Edge-développeur | GitHub"  

[MDNActive]: https://developer.mozilla.org/docs/Web/CSS/:active ": actif | MDN"  
[MDNFocus]: https://developer.mozilla.org/docs/Web/CSS/:focus ": Focus | MDN"  

[MonorailChromiumIssues]: https://crbug.com "Problèmes-chrome-monorail"  

[W3CWaiAriaTablist]: https://www.w3.org/TR/wai-aria-1.1/#tablist "TabList (rôle)-applications Internet riches accessibles (WAI-ARIA) 1,1 | W3C"  
[W3CWaiAriaTree]: https://www.w3.org/TR/wai-aria-1.1/#tree "arborescence (rôle)-applications Internet riches accessibles (WAI-ARIA) 1,1 | W3C"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) et est créée par [Rob Dodson][RobDodson] \ (Contributor, Google Web Fundamentals).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[RobDodson]: https://developers.google.com/web/resources/contributors/robdodson  
