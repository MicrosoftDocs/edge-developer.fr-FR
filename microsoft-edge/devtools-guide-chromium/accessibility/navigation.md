---
description: Guide sur la navigation dans Microsoft Edge DevTools à l’aide d’une technologie d’assistance telle que les lecteurs d’écran.
title: Naviguer dans Microsoft Edge DevTools avec la technologie d’assistance
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 343ce99188234b40dd8554e3db8bf303876e7b2f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398433"
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

# <a name="navigate-microsoft-edge-devtools-with-assistive-technology"></a>Naviguer dans Microsoft Edge DevTools avec la technologie d’assistance  

L’article suivant vise à aider les utilisateurs qui s’appuient principalement sur des technologies d’assistance telles que les lecteurs d’écran à accéder et à utiliser [Microsoft Edge DevTools.][MicrosoftEdgeDevtoolsMain]  [Microsoft Edge DevTools est][MicrosoftEdgeDevtoolsMain] une suite d’outils de développement web intégrés au navigateur Microsoft Edge.  Si vous recherchez des fonctionnalités DevTools relatives à l’amélioration de l’accessibilité d’une page web, accédez à La Référence [d’accessibilité.][DevtoolsAccessibilityReference]  

L’accessibilité de DevTools est un travail en cours.  Certains panneaux et onglets fonctionnent mieux avec la technologie d’assistance que d’autres.  Ce guide vous guide à travers les panneaux qui sont les plus accessibles et met en évidence des problèmes spécifiques que vous pouvez rencontrer en cours de route.  

## <a name="overview"></a>Vue d'ensemble  

Avant de commencer, il est utile d’avoir un modèle de structure de l’interface utilisateur DevTools.  DevTools est divisé en une série de panneaux organisés en une [liste de tabulations ARIA.][W3CWaiAriaTablist]  

Par exemple:  

*   **L’outil Elements** vous permet [d’afficher et de modifier les nodes DOM][DevtoolsDomIndexNavigateDomTreeKeyboard] ou [CSS][DevtoolsCssIndex].  
*   Le [panneau console vous][DevtoolsConsoleIndex] permet de lire les journaux JavaScript et d’éditer des objets en direct.  

Dans la zone de contenu de chaque panneau se trouve un certain nombre d’outils différents, souvent appelés onglets ou volets dans la documentation.  
Par exemple, l’outil **Elements** contient des onglets supplémentaires pour inspecter les écouteurs d’événements, l’arborescence d’accessibilité, et bien plus encore.  La distinction entre les onglets et les volets est quelque peu arbitraire.  La seule raison pour laquelle vous pouvez passer en revue un terme ou l’autre est de maintenir la cohérence avec le reste de la documentation officielle de DevTools.  

## <a name="keyboard-shortcuts"></a>Raccourcis clavier  

[DevTools Keyboard Shortcuts reference][DevtoolsShortcuts] est une feuille de calcul utile.  N’oubliez pas de le mettre en signet et de vous y référer lorsque vous explorez les différents panneaux.  

## <a name="open-devtools"></a>Ouvrir DevTools  

Pour commencer, accédez à [Ouvrir Microsoft Edge DevTools][DevtoolsOpen].  Il existe plusieurs façons d’ouvrir DevTools, par le biais de raccourcis clavier ou d’éléments de menu.  

## <a name="navigate-between-panels"></a>Naviguer entre les panneaux  

### <a name="navigate-by-keyboard"></a>Naviguer à l’aide du clavier  

*   Avec DevTools ouvert, sélectionnez `Control` + `]` \(Windows, Linux\) ou `Command` + `]` \(macOS\) pour mettre le panneau suivant au point.  
*   Sélectionnez `Control` + `[` \(Windows, Linux\) ou `Command` + `[` \(macOS\) pour centrer le panneau précédent.  
*   Il est également possible de déplacer le focus dans la liste d’onglets ARIA d’un panneau et d’utiliser les touches de direction pour modifier les panneaux, bien qu’il soit plus rapide d’utiliser les `Shift` + `Tab` raccourcis mentionnés précédemment. [][W3CWaiAriaTablist]  

**Problèmes connus**  

*   Certains panneaux, tels **** que les outils **Console** et Performances, peuvent déplacer le focus dans la zone de contenu du panneau dès que chaque panneau est activé.  Cela peut rendre difficile la navigation par les touches de direction.  
*   Le nom du panneau sélectionné est annoncé, mais uniquement après avoir lu le contenu sélectionné dans le panneau.  Cela peut être très facile à manquer.  

### <a name="navigate-by-command-menu"></a>Naviguer par menu de commande  

Pour mettre au point un panneau spécifique, utilisez [le menu Commande][DevtoolsCommandMenuIndex]:  

1.  Avec DevTools ouvert, sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le **menu Commande.**  
    Le **menu Commande est** une zone de liste déroulante de la recherche de recherche automatique.  
1.  Tapez le nom du panneau que vous souhaitez ouvrir, puis utilisez le clavier `Down Arrow` pour accéder à l’option correcte.  
1.  Sélectionnez `Enter` pour exécuter une commande.  

Effectuer les actions suivantes pour ouvrir **l’outil Éléments.**  

1.  Ouvrez **le menu Commande.**  
1.  Tapez `E` ensuite `L` .  **L’option > afficher les éléments** est sélectionnée.  
1.  Sélectionnez `Enter` pour exécuter la commande qui ouvre le panneau.  

Ouvrez un panneau de cette façon pour diriger le focus vers le contenu du panneau.  Dans le cas de l’outil **Elements,** le focus se déplace dans l’arborescence **DOM**.  

## <a name="elements-panel"></a>Panneau Éléments  

### <a name="inspect-an-element-on-the-page"></a>Inspecter un élément sur la page  

1.  Accédez à l’élément que vous souhaitez inspecter à l’aide du curseur dans le lecteur d’écran.  
1.  Simulez un clic droit à l’aide d’une souris sur l’élément pour ouvrir le menu contextif.  
1.  Choisissez **l’option Inspecter.**  Cela [ouvre le panneau Éléments et concentre l’élément dans l’arborescence DOM][DevtoolsDomIndexViewDomNodes].  

**L’arborescence DOM** est disposé en tant [qu’arborescence ARIA.][W3CWaiAriaTree]  Par exemple, accédez à [Naviguer dans l’arborescence **DOM** avec un clavier][DevtoolsDomIndexNavigateDomTreeKeyboard].  

### <a name="copy-the-code-for-an-element-in-the-dom-tree"></a>Copier le code d’un élément dans l’arborescence DOM  

1.  Avec le focus sur un nœud dans l’arborescence **DOM,** pointez sur le nœud et ouvrez le menu contextuel \(clic droit\).  
1.  Développez **l’option** Copier.  
1.  Choose **Copy outerHTML**.  

**Problèmes connus**  

*   **La copie outerHTML** ne sélectionne souvent pas le nœud actuel, mais sélectionne plutôt le nœud parent.  Toutefois, le contenu de l’élément doit toujours se faire dans le outerHTML copié.  

### <a name="modify-the-attributes-of-an-element-in-the-dom-tree"></a>Modifier les attributs d’un élément dans l’arborescence DOM  

*   Avec le focus sur un nœud dans l’arborescence **DOM,** sélectionnez `Enter` pour le rendre modifiable.  
*   Sélectionnez `Tab` pour passer d’une valeur d’attribut à une autre.  Lorsque vous entendez « espace », vous êtes à l’intérieur d’une entrée de texte vide et êtes en mesure de taper une nouvelle valeur d’attribut.  
*   Sélectionnez `Control` + `Enter` \(Windows, Linux\) ou `Command` + \(macOS\) pour accepter la modification et écouter tout le `Enter` contenu de l’élément.  

**Problèmes connus**  

*   Lorsque vous tapez dans l’entrée de texte, vous n’obtenez aucun commentaire.  Si vous faites une faute de frappe et que vous utilisez les touches de direction pour explorer votre entrée, vous n’obtenez aucun commentaire.  Le moyen le plus simple de vérifier votre travail consiste à accepter la modification, puis à écouter l’intégralité de l’élément à annoncer.  

### <a name="edit-the-html-of-an-element-in-the-dom-tree"></a>Modifier le code HTML d’un élément dans l’arborescence DOM  

*   Avec le focus sur un nœud dans l’arborescence **DOM,** sélectionnez `Enter` pour le rendre modifiable.  
*   Sélectionnez `Tab` pour passer d’une valeur d’attribut à une autre.  Lorsque vous entendez le nom de l’élément, par exemple, vous êtes à l’intérieur d’une entrée de texte et peut modifier `h2` le type de l’élément.  
*   Sélectionnez `Control` + `Enter` \(Windows, Linux\) ou `Command` + `Enter` \(macOS\) pour accepter la modification.  

Par exemple, lorsque vous tapez et sélectionnez `h3` `Control` + `Enter` \(Windows, Linux\) ou `Command` + `Enter` \(macOS\), les balises de début et de fin de `h3` l’élément changent.  

## <a name="elements-tool-panels"></a>Panneaux d’outils Éléments  

**L’outil Elements** contient des onglets supplémentaires pour inspecter des éléments tels que le CSS appliqué à un élément ou l’endroit approprié dans l’arborescence d’accessibilité.  

*   Avec le focus sur un nœud dans l’arborescence **DOM,** sélectionnez jusqu’à ce que vous entendiez que le volet `Tab` **Styles** est sélectionné.  
*   Utilisez `Right Arrow` l’onglet pour explorer les autres onglets disponibles.  

**L’arborescence DOM** transforme les éléments avec des attributs en liens sélectionnables, de sorte que vous devrez peut-être sélectionner plusieurs fois pour accéder `href` `Tab` au volet **Styles.**  

**Problèmes connus**  

Les **** **onglets Points d’arrêt et Propriétés DOM** ne sont pas accessibles au clavier.  

### <a name="styles-pane"></a>Volet Styles  

Dans le volet **Styles,** recherchez les contrôles de filtrage des styles, les états d’élément bascule \(tels que [:active][MDNActive] et [:focus][MDNFocus]\), le basculement de classes et l’ajout de nouvelles classes.  Il existe également un outil d’inspection de style puissant pour explorer et modifier les styles actuellement appliqués à l’élément qui est en focus dans l’arborescence **DOM**.  

Le concept clé à comprendre sur le volet **Styles** est qu’il affiche uniquement les styles pour le nœud actuellement sélectionné dans l’arborescence **DOM**.  Par exemple, supposons que vous avez terminé d’inspecter les styles d’un nœud et que vous souhaitez maintenant examiner les `<header>` styles `<footer>` d’un nœud.  Pour ce faire, vous devez d’abord sélectionner le `<footer>` nœud dans l’arborescence **DOM.**  Vous trouverez peut-être [](#inspect-an-element-on-the-page) plus rapide d’utiliser le flux de travail Inspect pour inspecter un nœud qui se trouve à proximité générale du nœud \(par exemple, un lien dans le pied de groupe\), qui se concentre sur l’arborescence `footer` **DOM,** puis utilisez votre clavier pour accéder au nœud exact qui vous intéresse.  

#### <a name="navigate-the-styles-pane"></a>Naviguer dans le volet Styles  

Étant donné que tous les outils de style se connectent d’une manière ou d’une autre au volet **Styles,** il est tout d’abord logique de devenir expert dans cet outil.  

*   Avec le focus sur le **volet Styles,** sélectionnez pour déplacer le focus à `Tab` l’intérieur et explorez le contenu.  
*   Sélectionnez `Tab` jusqu’à ce que le premier style devienne actif.  Si vous utilisez un lecteur d’écran, ce premier style est annoncé comme `element.style {}` .  
*   Sélectionnez `Down Arrow` pour parcourir la liste des styles par ordre de spécificité.  Un lecteur d’écran annonce chaque style en commençant par le nom du fichier CSS, le numéro de ligne sur lequel le style apparaît et le nom du style.  Exemple : `main.css:233 .card__img {}`.  
*   Sélectionnez `Enter` pour inspecter un style plus en détail.  Le focus commence sur une version modifiable du nom du style.  
*   Choisissez `Tab` de vous déplacer entre les versions modifiables de chaque propriété CSS et les valeurs correspondantes.  À la fin de chaque bloc de style se trouve un champ de texte modifiable vide que vous pouvez utiliser pour ajouter des propriétés CSS supplémentaires.  
*   Vous pouvez continuer à choisir de parcourir la liste des styles ou de quitter le mode et revenir à la navigation par `Tab` `Escape` les touches de direction.  

Pour d’autres raccourcis, accédez à [Référence du clavier du volet Styles][DevtoolsShortcutsStylesPaneKeyboard].  

**Problèmes connus**  

*   Si vous utilisez le **champ de** texte modifiable Filtrer, vous ne pouvez plus naviguer dans la liste des styles.  

#### <a name="toggle-element-state"></a>État de l’élément Bascule  

Pour faire bascule l’état d’un élément, tel que `:active` : `:focus`  

1.  Accédez au **volet Styles** et sélectionnez jusqu’à ce que le bouton d’état de l’élément bascule `Tab` ait le focus. ****  
1.  Sélectionnez `Enter` pour développer la collection d’états d’élément.  Les états d’élément sont présentés comme un groupe de case à cocher.  
1.  Sélectionnez `Tab` jusqu’au premier état, `:active` , a le focus.  
1.  Sélectionnez `Space` pour l’activer.  Si l’élément actuellement sélectionné dans l’arborescence DOM possède un `:active` style, il est désormais appliqué.  
1.  `Tab`Maintenez-la pour explorer tous les états disponibles.  

#### <a name="add-an-existing-class"></a>Ajouter une classe existante  

Adjacent au bouton **d’état de l’élément Bascule,** se trouve le **bouton Classes d’élément.**  Pour déplacer la sélection sur celui-ci, `Tab` sélectionnez et sélectionnez `Enter` .  Le focus se déplace dans un champ de texte d’édition étiqueté **Ajouter une nouvelle classe.**  

Le **bouton Classes d’élément** est principalement utilisé pour ajouter des classes existantes à un élément.  Par exemple, si votre feuille de style contenait une classe d’aide nommée, vous pouvez sélectionner à l’intérieur du champ modifier le texte pour afficher une liste de suggestions de classes et utiliser la pour rechercher `.clearfix` `.` la `Down Arrow` `.clearfix` suggestion.  Vous pouvez également taper le nom de la classe vous-même et choisir `Enter` de l’appliquer.  

#### <a name="add-a-new-style-rule"></a>Ajouter une nouvelle règle de style  

Adjacent au bouton **Classes d’éléments** se trouve le **bouton Nouvelle règle de style.**  Pour déplacer la sélection sur celui-ci, `Tab` sélectionnez et sélectionnez `Enter` .  Le focus se déplace dans un champ de texte modifiable à l’intérieur de l’inspecteur de style.  Le contenu de texte initial du champ est le nom de balise de l’élément sélectionné dans l’arborescence **DOM**.  
Vous pouvez taper le nom de classe de votre choix dans ce champ, puis lui attribuer des `Tab` propriétés CSS.  

### <a name="computed-tab"></a>Onglet calculé  

Avec le focus sur **l’onglet Calculé,** sélectionnez pour déplacer le focus à `Tab` l’intérieur et explorez le contenu.  Dans **l’onglet Calculé,** il existe des contrôles pour l’exploration des propriétés CSS qui sont réellement appliquées à un élément par ordre de spécificité.  

<!--todo: add computed tab section when available  -->  

#### <a name="explore-all-computed-styles"></a>Explorer tous les styles calculés  

Sélectionnez `Tab` jusqu’à atteindre la collection de styles calculés.  Celles-ci sont présentées sous la la nom [d’une arborescence ARIA.][W3CWaiAriaTree]  Le développement d’une boîte de liste révèle les sélecteurs CSS qui appliquent le style calculé.  Ces sélecteurs sont organisés par spécificité.  Un lecteur d’écran annonce la valeur calculée, le sélecteur CSS correspondant actuellement, le nom de fichier de la feuille de style qui contient le sélecteur et le numéro de ligne du sélecteur.  

**Problèmes connus**  

*   Si vous utilisez le **champ de** texte Filtre, vous ne pouvez plus inspecter les styles.  

### <a name="event-listeners-tab"></a>Onglet Écouteurs d’événements  

À partir de **l’outil Elements,** vous pouvez inspecter les écouteurs d’événements appliqués à un élément à l’aide de l’onglet **Écouteurs d’événements.**  Avec le focus sur le **panneau Styles,** sélectionnez le panneau Pour accéder au panneau Écouteurs `Right Arrow` **d’événements.**  

#### <a name="explore-event-listeners"></a>Explorer les écouteurs d’événements  

Les écouteurs d’événements sont présentés comme [une arborescence ARIA.][W3CWaiAriaTree]  Vous pouvez utiliser les touches de direction pour les parcourir.  Un lecteur d’écran annonce le nom de l’objet DOM à laquelle l’écoute d’événements est joint, ainsi que le nom de fichier dans lequel l’écoute d’événements est défini et le numéro de ligne.  

### <a name="accessibility-pane"></a>Volet Accessibilité  

Avec le focus sur le volet **Accessibilité,** sélectionnez pour déplacer le focus à l’intérieur `Tab` et explorez le contenu.  Dans le [volet Accessibilité,][DevtoolsAccessibilityReference] il existe des contrôles pour explorer l’arborescence d’accessibilité, les attributs ARIA appliqués à un élément et les propriétés d’accessibilité calculées.  

#### <a name="accessibility-tree"></a>Arborescence d’accessibilité  

**L’arborescence d’accessibilité** est présentée comme une [arborescence ARIA][W3CWaiAriaTree] où chacune `treeitem` correspond à un élément dans le DOM.  L’arborescence annonce le rôle calculé pour le nœud sélectionné.  Les éléments génériques, tels que « GenericContainer », sont annoncés dans `div` `span` l’arborescence.  Utilisez les touches de direction pour parcourir l’arborescence et explorer les relations parent-enfant.  

**Problèmes connus**  

*   Le type d’arborescence **** [ARIA][W3CWaiAriaTree] utilisé par le volet Accessibilité peut ne pas être correctement exposé dans Microsoft Edge pour les lecteurs d’écran macOS tels que VoiceOver.  [Abonnez-vous au problème Chromium #868480][ChromiumIssues868480] être informé de la progression de ce problème.  
*   Chacune des **** **sections Attributs ARIA** et propriétés calculées est marquée comme une arborescence [ARIA,][W3CWaiAriaTree]mais elle ne dispose pas actuellement de la gestion du focus et n’est pas particulièrement sensible au clavier.  

## <a name="audits-panel"></a>Panneau Audits  

**L’outil Audits** vous devez exécuter une série de tests sur un site pour vérifier les problèmes courants liés aux performances, à l’accessibilité, au seO et à un certain nombre d’autres catégories.  

### <a name="configure-and-run-an-audit"></a>Configurer et exécuter un audit  

1.  Lorsque **l’outil Audits** est ouvert pour la première fois, le focus est placé sur le bouton Exécuter **l’audit** à la fin du formulaire.  Par défaut, le formulaire est configuré pour exécuter des audits pour chaque catégorie à l’aide de l’émulation mobile sur une connexion 3G simulée.  
1.  Utilisez `Shift` + `Tab` ou naviguez vers l’arrière en mode Parcourir pour modifier les paramètres d’audit.  
1.  Lorsque vous êtes prêt à exécuter l’audit, revenir au bouton **Exécuter l’audit** et sélectionnez `Enter` .  
1.  Le focus se déplace dans une fenêtre modale avec un **bouton Annuler** qui vous permet de quitter l’audit.  Vous entendez peut-être une série d’écouteurs lorsque l’audit s’exécute et actualise la page plusieurs fois.  

**Problèmes connus**  

*   Les différentes sections du formulaire de configuration ne sont pas actuellement marquées avec un `fieldset` élément.  Il peut être plus facile de les parcourir en mode Parcourir pour déterminer quels contrôles sont associés à chaque section.  
*   Il n’existe aucune annonce d’écouteur ou de région en direct lorsque l’audit est terminé.  En règle générale, la navigation vers les résultats prend environ 30 secondes.  L’utilisation du mode Parcourir peut être le moyen le plus simple d’atteindre les résultats.  

### <a name="navigate-the-audit-report"></a>Parcourir le rapport d’audit  

Le rapport d’audit est organisé en sections qui correspondent à chacune des catégories d’audit.  Le rapport s’ouvre avec une liste de scores pour chaque catégorie.  Ces scores sont également des liens qui peuvent être utilisés pour passer aux sections pertinentes.  Chaque section contient des éléments ex expandables, qui contiennent des informations `details` relatives aux audits réussis ou ayant échoué.  Par défaut, seuls les audits défaillants sont affichés.  Chaque section se termine par un élément final `details` qui contient tous les audits passés.  

Pour exécuter un nouvel audit, quittez le rapport et recherchez le bouton Effectuer `Shift` + `Tab` **un audit.**  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsAccessibilityReference]: ./reference.md "Référence d’accessibilité | Documents Microsoft"  
[DevtoolsAccessibilityReferencePane]: reference.md#the-accessibility-pane "Volet Accessibilité : référence sur l’accessibilité | Documents Microsoft"  
[MicrosoftEdgeDevtoolsMain]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Exécuter des commandes avec le menu de commandes Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsConsoleIndex]: ../console/index.md "Présentation de la console | Documents Microsoft"  
[DevtoolsCssIndex]: ../css/index.md "Commencer à afficher et modifier les | Documents Microsoft"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element | Microsoft Docs"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get started with viewing and changing the DOM | Microsoft Docs"  -->  
[DevtoolsDomIndexViewDomNodes]: .. /dom/index.md#view-dom-nodes «View DOM nodes - Get started with viewing and changing the DOM | Microsoft Docs »  
[DevtoolsDomIndexNavigateDomTreeKeyboard]: .. /dom/index.md#navigate-the-dom-tree-with-a-keyboard " Navigate the DOM Tree with a keyboard - Get started with viewing and changing the DOM | Microsoft Docs »  
[DevtoolsOpen]: .. /open/index.md «Open Microsoft Edge DevTools | Microsoft Docs »  
[DevtoolsShortcuts] : .. /shortcuts/index.md «Microsoft Edge DevTools Keyboard Shortcuts | Microsoft Docs »  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /shortcuts/index.md#styles-panel-keyboard-shortcuts «Styles panel keyboard shortcuts - Microsoft Edge DevTools Keyboard Shortcuts | Microsoft Docs »  

[ChromiumIssues868480]: https://bugs.chromium.org/p/chromium/issues/detail?id=868480 "Problème 868480 : exposer des arbre ARIA en tant que tables dans l’accessibilité de Mac"  

[GithubEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Docs%20Feedback%5D "Nouveau problème : MicrosoftDocs/edge-developer | GitHub"  

[MDNActive]: https://developer.mozilla.org/docs/Web/CSS/:active ":active | MDN"  
[MDNFocus]: https://developer.mozilla.org/docs/Web/CSS/:focus ":focus | MDN"  

[MonorailChromiumIssues]: https://crbug.com "Problèmes - chromium - Monorail"  

[W3CWaiAriaTablist]: https://www.w3.org/TR/wai-aria-1.1/#tablist "tablist (role) - Accessible Rich Internet Applications (ARIA-ARIA) 1.1 | W3C"  
[W3CWaiAriaTree]: https://www.w3.org/TR/wai-aria-1.1/#tree "tree (role) - Accessible Rich Internet Applications (ARIA-ARIA) 1.1 | W3C"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est [trouvée ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) et a été rédigé par [Rob Dodson][RobDodson] \(Contributor, Google Web Pdf\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[RobDodson]: https://developers.google.com/web/resources/contributors/robdodson  
