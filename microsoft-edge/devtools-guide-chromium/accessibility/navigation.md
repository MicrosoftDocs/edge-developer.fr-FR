---
description: Guide sur la navigation dans Microsoft Edge DevTools à l’aide d’une technologie d’assistance telle que les lecteurs d’écran.
title: Naviguer Microsoft Edge DevTools avec la technologie d’assistance
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 2cb57a8ea1ea34506b4698d80ae0981d8716f3d2
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597098"
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
# <a name="navigate-microsoft-edge-devtools-with-assistive-technology"></a>Naviguer Microsoft Edge DevTools avec la technologie d’assistance  

Cet article aide les utilisateurs qui s’appuient principalement sur des technologies d’assistance telles que les lecteurs [d’écran Microsoft Edge devTools][MicrosoftEdgeDevtoolsMain].  DevTools est une suite d’outils de développement web intégrés au navigateur Microsoft Edge web.  

Pour les fonctionnalités DevTools relatives à l’amélioration de l’accessibilité d’une page web, voir fonctionnalités de test de l’accessibilité dans [DevTools][DevtoolsAccessibilityReference] et Vue d’ensemble des tests d’accessibilité à l’aide [de DevTools](accessibility-testing-in-devtools.md).

L’accessibilité de DevTools est un travail en cours.  Certains outils et onglets fonctionnent mieux avec la technologie d’assistance que d’autres.  Ce guide vous guide à travers les outils et les onglets qui sont les plus accessibles, et met en évidence des problèmes spécifiques que vous pouvez rencontrer en cours de route.  

## <a name="overview"></a>Vue d'ensemble  

DevTools est divisé en une série d’outils.  (Dans le **menu Commande,** les outils sont appelés _panneaux.)_  Les outils sont organisés en une liste d’onglets [ARIA][W3CWaiAriaTablist] dans la barre d’outils principale et dans la barre d’outils de caisse.

Voici quelques exemples d’outils :

*   **L’outil Elements** vous permet [d’afficher et de modifier les nodes DOM][DevtoolsDomIndexNavigateDomTreeKeyboard] ou [CSS][DevtoolsCssIndex].  
*   **L’outil Console** vous permet de lire les journaux JavaScript et d’éditer des objets en direct.  Pour plus d’informations, [accédez à Utiliser la console.][DevtoolsConsoleIndex]

Chaque outil présente un ou plusieurs ensembles d’onglets.  Par exemple, **l’outil Elements** contient un ensemble d’onglets, notamment **Styles,** **Écouteurs**d’événements et **Accessibilité.**

## <a name="keyboard-shortcuts"></a>Raccourcis clavier  

[DevTools Keyboard Shortcuts reference][DevtoolsShortcuts] est une feuille de astuce utile.  N’oubliez pas de le mettre en signet et de vous y référer lorsque vous explorez les différents outils.

## <a name="open-devtools"></a>Ouvrir DevTools  

Pour commencer, accédez à [Open Microsoft Edge DevTools][DevtoolsOpen].  Il existe plusieurs façons d’ouvrir DevTools, par le biais de raccourcis clavier ou d’éléments de menu.  

## <a name="navigate-between-tools"></a>Naviguer entre les outils

### <a name="navigate-by-keyboard"></a>Naviguer à l’aide du clavier  

*   Avec DevTools ouvert, sélectionnez `Control` + `]` \(Windows, Linux\) ou `Command` + \(macOS\) pour déplacer le focus vers l’outil suivant dans la `]` barre d’outils principale.
*   Sélectionnez `Control` + `[` \(Windows, Linux\) ou `Command` + \(macOS\) pour déplacer le focus vers l’outil précédent de la `[` barre d’outils principale.
*   Sélectionnez ou répétez cette sélection jusqu’à ce que le focus se déplace vers les onglets de la barre d’outils principale ou de la barre d’outils de caisse, puis utilisez les touches de direction pour vous déplacer `Tab` `Shift` + `Tab` parmi les outils.

**Problèmes connus**  

*   Certains outils, tels **** que les outils **Console** et Performances, peuvent déplacer le focus dans la zone de contenu de l’outil dès que l’outil est sélectionné.  Cela peut rendre difficile la navigation par les touches de direction.  
*   Le nom de l’outil sélectionné est annoncé, mais seulement après avoir annoncé le contenu sélectionné dans l’outil.  Cette séquence d’annonces peut faciliter l’accès au nom de l’outil.

### <a name="navigate-by-command-menu"></a>Naviguer par menu de commande  

Pour sélectionner un outil spécifique, utilisez le [menu Commande.][DevtoolsCommandMenuIndex]  Dans le menu Commande, un outil est appelé _panneau_.

1.  Avec DevTools ouvert, sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) **** pour ouvrir le menu commande.  
    Le **menu Commande** est une zone de liste déroulante de recherche automatique à recherche floue.  
1.  Tapez le nom d’un panneau (outil), puis utilisez le clavier `Down Arrow` pour accéder à l’option correcte.  
1.  Sélectionnez `Enter` pour exécuter une commande.  

Pour ouvrir **l’outil Éléments** :

1.  Ouvrez **le menu Commande.**  
1.  Tapez `E` ensuite `L` .  **L’option > afficher les éléments** est sélectionnée.  
1.  Sélectionnez `Enter` .  

L’ouverture d’un outil de cette façon place le focus dans la zone de contenu de l’outil.  Dans le cas de l’outil **Elements,** le focus se déplace dans l’arborescence **DOM**.

## <a name="elements-tool"></a>Outil Éléments

### <a name="inspect-an-element-on-the-page"></a>Inspecter un élément sur la page  

1.  Accédez à l’élément que vous souhaitez inspecter à l’aide du curseur dans le lecteur d’écran.  
1.  Simulez un clic droit sur l’élément, pour ouvrir le menu contextif.  
1.  Choisissez **l’option Inspecter.**  [ouvre l’outil Elements et concentre l’élément dans l’arborescence DOM][DevtoolsDomIndexViewDomNodes].  

**L’arborescence DOM** est disposé en tant [qu’arborescence ARIA.][W3CWaiAriaTree]  Pour obtenir un exemple, accédez à [Naviguer dans l’arborescence **DOM** avec un clavier][DevtoolsDomIndexNavigateDomTreeKeyboard].  

### <a name="copy-the-code-for-an-element-in-the-dom-tree"></a>Copier le code d’un élément dans l’arborescence DOM  

1.  Avec le focus sur un nœud dans l’arborescence **DOM,** pointez sur le nœud et ouvrez le menu contextuel \(clic droit\).  
1.  Développez **l’option** Copier.  
1.  Choose **Copy outerHTML**.  

**Problèmes connus**  

*   **La copie outerHTML** ne sélectionne souvent pas le nœud actuel, mais sélectionne plutôt le nœud parent.  Toutefois, le contenu de l’élément doit toujours se faire dans le outerHTML copié.  

### <a name="modify-the-attributes-of-an-element-in-the-dom-tree"></a>Modifier les attributs d’un élément dans l’arborescence DOM  

*   Avec le focus sur un nœud dans l’arborescence **DOM,** sélectionnez `Enter` pour le rendre modifiable.  
*   Sélectionnez `Tab` pour passer d’une valeur d’attribut à une autre.  Lorsque vous entendez « espace », vous êtes à l’intérieur d’une entrée de texte vide et êtes en mesure de taper une nouvelle valeur d’attribut.  
*   Sélectionnez `Control` + `Enter` \(Windows, Linux\) ou `Command` + \(macOS\) pour accepter la modification et écouter l’intégralité du `Enter` contenu de l’élément.  

**Problèmes connus**  

*   Lorsque vous tapez dans la saisie de texte, vous n’obtenez aucun commentaire.  Si vous faites une faute de frappe et que vous utilisez les touches de direction pour explorer votre entrée, vous n’obtenez aucun commentaire.  Le moyen le plus simple de vérifier votre travail consiste à accepter la modification, puis à écouter l’intégralité de l’élément à annoncer.  

### <a name="edit-the-html-of-an-element-in-the-dom-tree"></a>Modifier le code HTML d’un élément dans l’arborescence DOM  

*   Avec le focus sur un nœud dans l’arborescence **DOM,** sélectionnez `Enter` pour le rendre modifiable.  
*   Sélectionnez `Tab` pour passer d’une valeur d’attribut à une autre.  Lorsque vous entendez le nom de l’élément, par exemple, vous êtes à l’intérieur d’une entrée de texte et peut modifier `h2` le type de l’élément.  
*   Sélectionnez `Control` + `Enter` \(Windows, Linux\) ou `Command` + `Enter` \(macOS\) pour accepter la modification.  

Par exemple, lorsque vous tapez et sélectionnez `h3` `Control` + `Enter` \(Windows, Linux\) ou `Command` + `Enter` \(macOS\), les balises de début et de fin de `h3` l’élément changent.  

## <a name="tabs-in-the-elements-tool"></a>Onglets dans l’outil Éléments

**L’outil Elements** contient des onglets supplémentaires permettant d’inspecter des éléments tels que le CSS appliqué à un élément ou l’endroit approprié dans l’arborescence d’accessibilité.  

*   Avec le focus sur un nœud dans l’arborescence **DOM,** sélectionnez jusqu’à ce que vous entendiez que l’onglet `Tab` **Styles** est sélectionné.  
*   Utilisez `Right Arrow` l’onglet pour explorer les autres onglets disponibles.

**L’arborescence DOM** transforme les éléments avec des attributs en liens sélectionnables, de sorte que vous devrez peut-être sélectionner plusieurs fois pour accéder `href` `Tab` au volet **Styles.**  

**Problèmes connus**  

Les **** **onglets Points d’arrêt et Propriétés DOM** ne sont pas accessibles au clavier.  

### <a name="styles-pane"></a>Volet Styles  

Dans le volet **Styles,** recherchez les contrôles de filtrage des styles, les états d’élément bascule \(tels que [:active][MDNActive] et [:focus][MDNFocus]\), le basculement de classes et l’ajout de nouvelles classes.  Il existe également un outil d’inspection de style puissant pour explorer et modifier les styles actuellement appliqués à l’élément qui est en focus dans l’arborescence **DOM**.  

Le concept clé à comprendre sur le volet **Styles** est qu’il affiche uniquement les styles pour le nœud actuellement sélectionné dans l’arborescence **DOM**.  Par exemple, supposons que vous avez terminé d’inspecter les styles d’un nœud et que vous souhaitez maintenant examiner les `<header>` styles `<footer>` d’un nœud.  Pour ce faire, vous devez d’abord sélectionner le `<footer>` nœud dans l’arborescence **DOM**.  Vous trouverez peut-être [](#inspect-an-element-on-the-page) plus rapide d’utiliser le flux de travail Inspect pour inspecter un nœud qui se trouve à proximité générale du nœud \(par exemple, un lien dans le pied de groupe\), qui se concentre sur l’arborescence `footer` **DOM,** puis utilisez votre clavier pour accéder au nœud exact qui vous intéresse.  

#### <a name="navigate-the-styles-pane"></a>Naviguer dans le volet Styles  

Étant donné que tous les outils de style se connectent d’une manière ou d’une autre au volet **Styles,** il est tout d’abord logique de devenir expert dans cet outil.  

*   Avec le focus sur le **volet Styles,** sélectionnez pour déplacer le focus à `Tab` l’intérieur et explorez le contenu.  
*   Sélectionnez `Tab` jusqu’à ce que le premier style devienne actif.  Si vous utilisez un lecteur d’écran, ce premier style est annoncé comme `element.style {}` .  
*   Sélectionnez `Down Arrow` pour parcourir la liste des styles par ordre de spécificité.  Un lecteur d’écran annonce chaque style en commençant par le nom du fichier CSS, le numéro de ligne sur lequel le style apparaît et le nom du style.  Par exemple : `main.css:233 .card__img {}`.  
*   Sélectionnez `Enter` pour inspecter un style plus en détail.  Le focus commence sur une version modifiable du nom du style.  
*   Choisissez `Tab` de passer des versions modifiables de chaque propriété CSS aux valeurs correspondantes.  À la fin de chaque bloc de style se trouve un champ de texte modifiable vide que vous pouvez utiliser pour ajouter des propriétés CSS supplémentaires.  
*   Vous pouvez continuer à choisir de parcourir la liste des styles ou de quitter le mode et revenir à la navigation par `Tab` `Escape` les touches de direction.  

Pour d’autres raccourcis, accédez à [Référence du clavier du volet Styles][DevtoolsShortcutsStylesPaneKeyboard].  

**Problèmes connus**  

*   Si vous utilisez le **champ de** texte modifiable Filtre, vous ne pouvez plus naviguer dans la liste des styles.  

#### <a name="toggle-element-state"></a>État de l’élément Bascule  

Pour faire bascule l’état d’un élément, tel que `:active` : `:focus`  

1.  Accédez au **volet Styles** et sélectionnez jusqu’à ce que le bouton d’état de l’élément bascule `Tab` ait le focus. ****  
1.  Sélectionnez `Enter` pour développer la collection d’états d’élément.  Les états d’élément sont présentés comme un groupe de case à cocher.  
1.  Sélectionnez `Tab` jusqu’au premier état, `:active` , a le focus.  
1.  Sélectionnez `Space` pour l’activer.  Si l’élément actuellement sélectionné dans l’arborescence DOM possède un `:active` style, il est désormais appliqué.  
1.  `Tab`Maintenez-la pour explorer tous les états disponibles.  

#### <a name="add-an-existing-class"></a>Ajouter une classe existante  

Le bouton **Classes** d’élément est adjacent au **bouton d’état de** l’élément bascule.  Pour y déplacer la sélection, `Tab` sélectionnez, puis sélectionnez `Enter` .  Le focus se déplace dans un champ de texte d’édition étiqueté **Ajouter une nouvelle classe.**  

Le **bouton Classes d’élément** est principalement utilisé pour ajouter des classes existantes à un élément.  Par exemple, si votre feuille de style contenait une classe d’aide nommée , vous pouvez sélectionner à l’intérieur du champ modifier le texte pour afficher une liste de suggestions de classes et utiliser la pour rechercher la `.clearfix` `.` `Down Arrow` `.clearfix` suggestion.  Ou tapez vous-même le nom de la classe et `Enter` sélectionnez-le pour l’appliquer.  

#### <a name="add-a-new-style-rule"></a>Ajouter une nouvelle règle de style  

Adjacent au bouton **Classes d’éléments** se trouve le **bouton Nouvelle règle de style.**  Pour y déplacer la sélection, `Tab` sélectionnez, puis sélectionnez `Enter` .  Le focus se déplace dans un champ de texte modifiable à l’intérieur de l’inspecteur de style.  Le contenu de texte initial du champ est le nom de balise de l’élément sélectionné dans l’arborescence **DOM**.  
Vous pouvez taper n’importe quel nom de classe de votre choix dans ce champ, puis lui attribuer des `Tab` propriétés CSS.  

### <a name="computed-tab"></a>Onglet calculé  

Avec le focus sur **l’onglet Calculé,** sélectionnez pour déplacer le focus à `Tab` l’intérieur et explorez le contenu.  Dans **l’onglet Calculé,** il existe des contrôles pour l’exploration des propriétés CSS qui sont réellement appliquées à un élément par ordre de spécificité.  

<!--todo: add Computed tab section when available  -->  

#### <a name="explore-all-computed-styles"></a>Explorer tous les styles calculés  

Sélectionnez `Tab` jusqu’à atteindre la collection de styles calculés.  Celles-ci sont présentées sous la la nom [d’une arborescence ARIA.][W3CWaiAriaTree]  Le développement d’une boîte de liste révèle les sélecteurs CSS qui appliquent le style calculé.  Ces sélecteurs sont organisés par spécificité.  Un lecteur d’écran annonce la valeur calculée, le sélecteur CSS correspondant actuellement, le nom de fichier de la feuille de style qui contient le sélecteur et le numéro de ligne du sélecteur.  

**Problèmes connus**  

*   Si vous utilisez le **champ de** texte Filtre, vous ne pouvez plus inspecter les styles.  

### <a name="event-listeners-tab"></a>Onglet Écouteurs d’événements  

Pour inspecter les écouteurs d’événements appliqués à un **** élément, sélectionnez l’outil **Éléments,** puis sélectionnez l’onglet Écouteurs d’événements (regroupés avec l’onglet **Styles).**

#### <a name="explore-event-listeners"></a>Explorer les écouteurs d’événements  

Les écouteurs d’événements sont présentés comme [une arborescence ARIA.][W3CWaiAriaTree]  Vous pouvez utiliser les touches de direction pour les parcourir.  Un lecteur d’écran annonce le nom de l’objet DOM à laquelle l’écoute d’événements est joint, ainsi que le nom de fichier où l’écoute d’événements est défini et le numéro de ligne.  

### <a name="accessibility-tab"></a>Onglet Accessibilité

Sélectionnez `Tab` la clé à **** déplacer dans l’onglet Accessibilité de **l’outil Éléments.**

**L’onglet Accessibilité** se trouve près de **l’onglet Styles.** Sous l’onglet Accessibilité, il existe des contrôles pour explorer l’arborescence d’accessibilité, les attributs ARIA appliqués à un élément et les propriétés d’accessibilité calculées.  Pour plus d’informations, accédez à [Tester l’accessibilité à l’aide de l’onglet Accessibilité.][DevtoolsAccessibilityTab]

#### <a name="accessibility-tree"></a>Arborescence d’accessibilité  

**L’arborescence d’accessibilité** est présentée comme une [arborescence ARIA][W3CWaiAriaTree] où chacune `treeitem` correspond à un élément dans le DOM.  L’arborescence annonce le rôle calculé pour le nœud sélectionné.  Les éléments génériques, tels que « GenericContainer », sont annoncés dans `div` `span` l’arborescence.  Utilisez les touches de direction pour parcourir l’arborescence et explorer les relations parent-enfant.  

**Problèmes connus**  

*   Le type d’arborescence **** [ARIA][W3CWaiAriaTree] utilisé par l’onglet Accessibilité peut ne pas être correctement exposé dans Microsoft Edge pour les lecteurs d’écran macOS tels que VoiceOver.  [S’abonner Chromium problème #868480][ChromiumIssues868480] être informé de la progression de ce problème.  
*   Chacune des **** **sections Attributs ARIA** et propriétés calculées est marquée comme une arborescence [ARIA,][W3CWaiAriaTree]mais elle ne dispose pas actuellement de la gestion du focus et n’est pas particulièrement sensible au clavier.  

## <a name="lighthouse-tool"></a>Outil De lumière

**Ce dernier** exécute une série de tests sur un site pour vérifier les problèmes courants liés aux performances, à l’accessibilité, au seO et à un certain nombre d’autres catégories.  

### <a name="configure-and-generate-a-report"></a>Configurer et générer un rapport

1.  Lorsque **l’outil Îles** est ouvert pour la première fois dans DevTools, le focus est placé sur le **bouton Générer un** rapport.  Par défaut, le formulaire est configuré pour exécuter des rapports pour chaque catégorie à l’aide de l’émulation mobile sur une connexion 3G simulée.  
1.  Pour modifier les paramètres du rapport, utilisez cette fonction pour mettre le focus sur les paramètres de l’état ou revenir `Shift` + `Tab` en mode Parcourir. ****  
1.  Lorsque vous êtes prêt à exécuter le rapport, revenir au bouton **Générer** le rapport et sélectionnez `Enter` .  
1.  Le focus se déplace dans une fenêtre modale avec un **bouton Annuler** qui vous permet de quitter l’audit.  Vous entendez peut-être une série d’écouteurs lorsque l’audit s’exécute et actualise la page plusieurs fois.  

**Problèmes connus**  

*   Les différentes sections du formulaire de configuration ne sont actuellement pas marquées avec un `fieldset` élément.  Il peut être plus facile de les parcourir en mode Parcourir pour déterminer quels contrôles sont associés à chaque section.  
*   Il n’existe aucune annonce d’écouteur ou de région en direct lorsque l’audit est terminé.  En règle générale, l’audit prend environ 30 secondes, après quoi vous devriez être en mesure d’accéder aux résultats.  L’utilisation du mode Parcourir peut être le moyen le plus simple d’atteindre les résultats.  

### <a name="navigate-the-lighthouse-report"></a>Naviguer dans le rapport Dente  

Le rapport de Laser est organisé en sections qui correspondent à chacune des catégories d’audit.  Le rapport s’ouvre avec une liste de scores pour chaque catégorie.  Ces scores sont également des liens que vous pouvez utiliser pour passer aux sections pertinentes.  Chaque section contient des éléments ex expandables, qui contiennent des informations `details` relatives aux audits réussis ou ayant échoué.  Par défaut, seuls les audits défaillants sont affichés.  Chaque section se termine par un élément final `details` qui contient tous les audits passés.  

Pour exécuter un nouvel audit, quittez le rapport `Shift` + `Tab` et sélectionnez le bouton Générer **le** rapport.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  
[DevtoolsAccessibilityReference]: reference.md "Fonctionnalités de test de l’accessibilité dans DevTools | Documents Microsoft"  
[DevtoolsAccessibilityTab]: accessibility-tab.md "Tester l’accessibilité à l’aide de l’onglet Accessibilité | Documents Microsoft"  
[MicrosoftEdgeDevtoolsMain]: ../../devtools-guide-chromium/index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  
[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Exécuter des commandes avec le menu de Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsConsoleIndex]: ../console/index.md "Présentation de la console | Documents Microsoft"  
[DevtoolsCssIndex]: ../css/index.md "Prise en main Avec l’affichage et la modification des | Documents Microsoft"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element | Microsoft Docs"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get started with viewing and changing the DOM | Microsoft Docs"  -->  
[DevtoolsDomIndexViewDomNodes]: .. /dom/index.md#view-dom-nodes «View DOM nodes - Get started with viewing and changing the DOM | Microsoft Docs »  
[DevtoolsDomIndexNavigateDomTreeKeyboard]: .. /dom/index.md#navigate-the-dom-tree-with-a-keyboard " Navigate the DOM Tree with a keyboard - Get started with viewing and changing the DOM | Microsoft Docs »  
[DevtoolsOpen]: .. /open/index.md «Open Microsoft Edge DevTools | Microsoft Docs »  
[DevtoolsShortcuts] : .. /shortcuts/index.md «Microsoft Edge raccourcis clavier DevTools | Microsoft Docs »  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /shortcuts/index.md#styles-panel-keyboard-shortcuts «Styles panel keyboard shortcuts - Microsoft Edge DevTools Keyboard Shortcuts | Microsoft Docs »  

[ChromiumIssues868480]: https://bugs.chromium.org/p/chromium/issues/detail?id=868480 "Problème 868480 : exposer des arbre ARIA en tant que tableaux dans l’accessibilité de Mac"  

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
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[RobDodson]: https://developers.google.com/web/resources/contributors#rob-dodson  
