---
description: Commencer à tester les problèmes d’accessibilité à l’aide de DevTools
title: Vue d’ensemble des tests d’accessibilité à l’aide de DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 50661f68c7b3269d003bdc25f6a8098ae0e3ec89
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597400"
---
# <a name="overview-of-accessibility-testing-using-devtools"></a>Vue d’ensemble des tests d’accessibilité à l’aide de DevTools

Dans cet article, nous traitons de certaines des fonctionnalités que vous pouvez utiliser dans DevTools pour tester les problèmes d’accessibilité.  Nous utilisons différentes fonctionnalités de DevTools pour détecter les problèmes d’accessibilité dans une page de démonstration, et nous abordons comment les résoudre.  Ouvrez la [page de démonstration][DevToolsA11yErrorsDemopage] dans un nouvel onglet pour l’essayer vous-même et vous pouvez le tester.

:::image type="complex" source="../media/a11y-testing-basics-demopage.msft.png" alt-text="Page de démonstration utilisée dans cet article avec quelques problèmes d’accessibilité" lightbox="../media/a11y-testing-basics-demopage.msft.png":::
    Page de démonstration utilisée dans cet article avec quelques problèmes d’accessibilité
:::image-end:::


## <a name="automated-testing-by-using-the-issues-tool"></a>Tests automatisés à l’aide de l’outil Problèmes

Lorsque vous ouvrez la page de démonstration dans le navigateur et que vous ouvrez DevTools, notez que certains problèmes sont automatiquement détectés dans le compteur **Problèmes.**  Sélectionnez **le compteur Problèmes** \( Compteur de problèmes \) pour ouvrir l’outil Problèmes pour afficher les problèmes et plus ![ ](../media/issues-counter-icon.msft.png) d’informations. [][DevToolsIssuesTool]

:::image type="complex" source="../media/a11y-testing-issues-tracker.msft.png" alt-text="Le compteur Problèmes indique le nombre de problèmes dans la page web actuelle et ouvre l’outil Problèmes" lightbox="../media/a11y-testing-issues-tracker.msft.png":::
    Le compteur Problèmes indique le nombre de problèmes dans la page web actuelle et ouvre l’outil Problèmes
:::image-end:::

Pour cet article, nous allons nous concentrer sur la section **Accessibilité** de **l’outil** Problèmes.

:::image type="complex" source="../media/a11y-testing-accessibility-issues.msft.png" alt-text="Avertissements d’accessibilité affichés dans l’outil Problèmes" lightbox="../media/a11y-testing-accessibility-issues.msft.png":::
    Avertissements d’accessibilité affichés dans l’outil Problèmes
:::image-end:::

Pour obtenir la procédure pas à pas détaillée, accédez à la [section Accessibilité de l’outil Problèmes.][DevToolsAccessibilityTestIssuesToolViewAccSection]


### <a name="automatically-checking-that-input-fields-have-labels"></a>Vérification automatique de l’étiquetage des champs d’entrée

Le premier avertissement affiché est `Form elements must have labels: Element has no title attribute. Element has no placeholder attribute` .  Lorsque vous développez cette **** section, puis sélectionnez le lien Ouvrir dans les éléments, l’outil **Éléments** s’ouvre, avec l’élément mis en surbrillon dans l’arborescence DOM.  **L’onglet** Styles affiche le CSS appliqué à l’élément.

Pour obtenir la procédure pas à pas détaillée, accédez à Vérifier que les champs [d’entrée ont des étiquettes.][DevtoolsAccessibilityTestIssuesToolCheckFieldsLabels]

:::image type="complex" source="../media/a11y-testing-inspect-problematic-element.msft.png" alt-text="Outil Éléments affichant le code HTML problématique après la sélection du lien dans l’outil Problèmes" lightbox="../media/a11y-testing-inspect-problematic-element.msft.png":::
    Outil Éléments affichant le code HTML problématique après la sélection du lien dans l’outil Problèmes
:::image-end:::

Dans ce cas, le code HTML possède un `label` élément qui ne fonctionne pas.

```html
<label>Search</label>
<input type="search">
<input type="submit" value="go">
```

L’utilisation de `label` l’élément ici est erronée, car il n’existe aucune connexion entre `label` l’élément et `input` l’élément.  Une étiquette HTML valide met le focus sur la zone de texte d’entrée de recherche lorsque vous sélectionnez **l’étiquette** De recherche. 

Vous pouvez résoudre ce problème en imbriant l’élément dans un élément ou en ajoutant un attribut qui pointe vers un attribut `input` `label` de `for` `id` `input` l’élément.  Pour afficher une connexion correcte, sélectionnez **l’étiquette Other** dans le formulaire de don.

Vous pouvez également sélectionner les liens explicatifs dans l’outil **Problèmes** pour obtenir ces informations.

:::image type="complex" source="../media/a11y-testing-more-information-links.msft.png" alt-text="Liens dans l’outil Problèmes pointant vers des informations plus détaillées sur le problème" lightbox="../media/a11y-testing-more-information-links.msft.png":::
    Liens dans **l’outil Problèmes** pointant vers des informations plus détaillées sur le problème
:::image-end:::


### <a name="automatically-checking-that-images-have-alt-text"></a>Vérification automatique de la mise en place d’un texte de alt pour les images

L’autre problème détecté automatiquement est que de nombreuses images de la page n’ont pas de texte de remplacement.  Si vous développez `Images must have alternate text: Element has no title attribute` l’avertissement, vous obtenez quatre instances d’images avec ce problème.

:::image type="complex" source="../media/a11y-testing-images-without-alt.msft.png" alt-text="L’outil Problèmes, rapport d’images avec un texte de remplacement manquant" lightbox="../media/a11y-testing-images-without-alt.msft.png":::
    **L’outil Problèmes,** rapport d’images avec un texte de remplacement manquant
:::image-end:::

Pour obtenir la procédure pas à pas détaillée, accédez à Vérifier que les [images ont un texte de alt][DevtoolsAccessibilityTestIssuesToolCheckAltText].


### <a name="automatically-checking-that-text-colors-have-enough-contrast"></a>Vérification automatique du contraste des couleurs du texte

**L’outil Problèmes** signale également lorsque deux éléments de la page ne sont pas assez contrastés.

:::image type="complex" source="../media/a11y-testing-contrast-issues.msft.png" alt-text="Problèmes de contraste signalés dans l’outil Problèmes" lightbox="../media/a11y-testing-contrast-issues.msft.png":::
    Problèmes de contraste signalés dans **l’outil Problèmes**
:::image-end:::

**L’outil Problèmes** fournit des explications détaillées de l’avertissement.  Lorsque vous descendez, vous obtenez une liste des éléments qui ont ce problème.  Dans **l’outil Problèmes,** la sélection d’un lien qui pointe vers un élément met en évidence cet élément sur la page rendue.

:::image type="complex" source="../media/a11y-testing-element-with-contrast-issues.msft.png" alt-text="Élément de la page mis en surbrillon après la sélection du lien vers celui-ci" lightbox="../media/a11y-testing-element-with-contrast-issues.msft.png":::
    Élément de la page mis en surbrillon après la sélection du lien vers celui-ci
:::image-end:::

Pour obtenir la procédure pas à pas détaillée, accédez à Vérifier que [les couleurs du texte ont un contraste suffisant.][DevtoolsAccessibilityTestIssuesToolCheckContrast]


### <a name="verify-that-the-webpage-layout-is-usable-when-narrow"></a>Vérifier que la mise en page web est utilisable lorsqu’elle est étroite

<!-- by design, this section doesn't have a corresponding how-to article -->

Une partie importante de l’accessibilité consiste à s’assurer que vos produits web fonctionnent bien sur une vue étroite. De nombreux utilisateurs doivent effectuer un zoom sur la page pour pouvoir l’utiliser, ce qui signifie qu’il ne reste plus beaucoup d’espace. Lorsqu’il n’y a pas suffisamment d’espace, votre disposition sur plusieurs colonnes doit se transformer en une disposition à une seule colonne, avec un contenu placé dans un ordre compréhensible. Cela signifie que vous placez le contenu le plus important en haut de la page et que vous placez du contenu supplémentaire plus bas.

En rendant la fenêtre du navigateur étroite et en utilisant les touches de direction pour faire défiler la page, vous pouvez voir que la barre de navigation supérieure de la page de démonstration présente certains problèmes d’accessibilité.  La barre de navigation supérieure chevauche le **formulaire de** recherche, comme illustré dans l’image précédente, et ce problème doit être résolu.

Vous pouvez simuler une fenêtre d’affichage étroite en re resserrez la fenêtre du navigateur, mais un meilleur moyen de tester la réactivité de votre conception consiste à utiliser l’outil **Device Emulation.**  Voici quelques fonctionnalités de l’outil **Device Emulation** qui vous aident à trouver les problèmes d’accessibilité de n’importe quel site web :

*  Sans re resserriser la fenêtre du navigateur, resizez la page et testez si vos requêtes [multimédias CSS][DevToolsMediaQueries] déclenchent une modification de la disposition.
*  Recherchez les dépendances qui utilisent une souris. Par défaut, l’émulation de l’appareil suppose un périphérique tactile. Cela signifie que toutes les fonctionnalités de votre produit qui reposent sur l’interaction avec le pointer ne fonctionneront pas. 
*  Effectuez des tests visuels en simulant différents appareils, niveaux de zoom et proportions de pixels.
*  Testez le comportement de votre produit sur des connexions non fiables ou lorsque l’utilisateur est hors connexion.  L’affichage des interactions les plus importantes avec un utilisateur sur une connexion lente est également une considération d’accessibilité.

Pour en savoir plus sur l’outil **Émulation** d’appareil, accédez à Émuler des appareils [mobiles dans Microsoft Edge DevTools][DevToolsDeviceModeIndex].


### <a name="wavy-underlines-in-the-dom-tree-indicate-automatically-detected-issues"></a>Les soulignements ondulés dans l’arborescence DOM indiquent des problèmes détectés automatiquement

L’arborescence DOM de l’outil **Elements** détecte automatiquement les problèmes directement dans le code HTML en ajoutant un soulignement ondulé.  Si vous `Shift` + `click` avez un élément avec un soulignement ondulé, **l’outil Problèmes** s’ouvre.

:::image type="complex" source="../media/a11y-testing-wavy-underlines.msft.png" alt-text="Un élément affiché avec un soulignement ondulé dans l’arborescence DOM présente des problèmes.  Shift+click the element to get directly to the issue" lightbox="../media/a11y-testing-wavy-underlines.msft.png":::
    Un élément affiché avec un soulignement ondulé dans l’arborescence DOM présente des problèmes.  `Shift`+`click` l’élément à obtenir directement au problème.
:::image-end:::

Ces problèmes qui ont été trouvés par l’outil **Problèmes** sont des problèmes d’accessibilité relativement évidents qui peuvent être évités.  **L’utilisation de l’outil** Problèmes et de ses explications guidées pour les résoudre vous permet d’atteindre un produit accessible.


## <a name="limits-of-automated-testing"></a>Limites des tests automatisés

[L’outil Problèmes,][DevToolsIssuesTool] [Accessibility Insights][AccessibilityInsights]et Le [Projet][Lighthouse] sont des outils qui génèrent automatiquement un rapport d’accessibilité pour une page web.  L’obtention d’un rapport automatisé à partir de ces outils n’est que le début de votre parcours de test de l’accessibilité.

L’accessibilité est une question d’interaction humaine : les personnes ayant des besoins différents utilisant vos produits dans différents environnements techniques.  Ce test ne peut pas être entièrement automatisé, mais doit être vérifié par un humain qui navigue sur le produit.  Dans le meilleur scénario, vous avez accès aux testeurs ayant des besoins d’accessibilité différents et aux testeurs utilisant différents environnements.  Toutefois, vous pouvez déjà faire beaucoup de choses vous-même en utilisant le clavier pour naviguer et en inspectant différentes parties de la page.

Dans la page de démonstration, il existe d’autres problèmes que les tests automatisés ne peuvent pas détecter, notamment : 

*  Problèmes qui surviennent après l’interaction avec la page. 
*  Problèmes liés aux modifications de l’affichage, telles que l’étroitesse de la fenêtre.

L’un de ces problèmes est le formulaire de don.  Lorsque vous utilisez une souris, vous pouvez cliquer sur les différentes options pour gagner de l’argent.  Mais lorsque vous essayez d’utiliser le clavier pour accéder au formulaire de don, rien ne se produit. Pour résoudre ce problème, vous devez utiliser **l’outil Inspect.**

:::image type="complex" source="../media/a11y-testing-basics-donation-form-issue.msft.png" alt-text="Le formulaire de don sur la page de démonstration est mis en évidence" lightbox="../media/a11y-testing-basics-donation-form-issue.msft.png":::
    Le formulaire de don sur la page de démonstration est mis en évidence
:::image-end:::


## <a name="using-the-inspect-tool-to-detect-accessibility-issues"></a>Utilisation de l’outil Inspect pour détecter les problèmes d’accessibilité

Utilisez **l’outil Inspect** pour détecter les problèmes d’accessibilité en pointant sur des parties de la page web.  **L’outil** Inspect \( Inspect \) se trouve dans le coin supérieur gauche ![ de ](../media/inspect-icon.msft.png) DevTools.  Pour activer l’outil Inspect, sélectionnez le bouton **Inspecter.**

:::image type="complex" source="../media/a11y-testing-basics-inspector.msft.png" alt-text="Activer l’outil Inspect en sélectionnant le bouton Inspecter l’outil" lightbox="../media/a11y-testing-basics-inspector.msft.png":::
    Activer l’outil **Inspect** en sélectionnant le bouton **Inspecter** l’outil
:::image-end:::

Après avoir sélectionné le bouton **Inspecter** l’outil, vous pouvez déplacer votre pointeur sur n’importe quel élément de la page rendue.  L’outil Inspect affiche la disposition de l’élément sous la forme d’une superposition flexbox superposée et affiche les détails de l’élément sous la forme d’une superposition d’informations similaire à une info-bulle.

:::image type="complex" source="../media/inspect-tool-flexbox-overlay.msft.png" alt-text="Superposition de flexbox multicolore et superposition d’informations lors de l’utilisation de l’outil Inspect" lightbox="../media/inspect-tool-flexbox-overlay.msft.png":::
    Superposition de flexbox multicolore et superposition d’informations lors de l’utilisation de **l’outil Inspect**
:::image-end:::

La section Accessibilité de l’outil **Inspect** inclut une **ligne de** contraste, le cas échéant.

:::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="La section Accessibilité de l’outil Inspect inclut une ligne de contraste, le cas échéant." lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
    La section Accessibilité de l’outil **Inspect** inclut une **ligne de** contraste, le cas échéant.
:::image-end:::

Pour obtenir la procédure pas à pas détaillée, accédez à Identifier les régions imbrmbrées à l’aide de la [mise en surbrillance des couleurs.][DevtoolsAccessibilityTestInspectToolColorHighlighting]
<!-- = test-inspect-tool.md##identify-nested-regions-using-color-highlighting -->

La section supérieure **** de la superposition des informations de l’outil Inspect affiche les informations suivantes :

* Type de disposition ; si l’élément est positionné à l’aide d’une boîte de flexbox ou d’une grille, vous voyez une icône appropriée \(![Icône De disposition de la grille](../media/grid-icon.msft.png)\).
* Nom de l’élément, tel **qu’un**élément , **h1**ou **div**.
* Dimensions de l’élément, en pixels.
* Couleur, sous la forme d’un échantillon de couleur (petit carré de couleur) et d’une valeur mise en forme (par `#336699` exemple).
* Informations sur les polices (taille et familles de polices).
* Marge et remplissage, en pixels.

La **partie Accessibilité** de la superposition **Inspect** est décrite dans la section suivante.


### <a name="checking-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support"></a>Vérification du contraste du texte, du texte du lecteur d’écran et de la prise en charge du clavier pour les éléments individuels

La section **Accessibilité** de la superposition **Inspect** contient les lignes suivantes :

*   **Le** contraste définit si un élément peut être compris par les personnes malvoyantes.
    *   Le [coefficient de contraste][W3CContrastRatio] défini par les directives [WCAG][WCAG] indique s’il existe un contraste suffisant entre les couleurs de texte et d’arrière-plan.  Une icône de coche verte indique qu’il y a suffisamment de contraste et qu’une icône de point d’exclamation orange indique qu’il n’y a pas assez de contraste.

*   **Le nom** et **le rôle** indiquent les technologies d’assistance aux informations, telles que les lecteurs d’écran, qui signalent l’élément.
    *   Le **nom est** le contenu de texte d’un `a` élément.  Pour l’élément, `<a href="/">About Us</a>` le nom **affiché** dans l’outil Inspect est « À propos de nous ».
    *   Rôle **de** l’élément.  Le **rôle** est généralement le nom de l’élément, tel `article` que , , ou `img` `link` `heading` .  Les `div` éléments et les éléments sont `span` représentés en tant que `generic` .

*   **La mise au point du clavier** indique si les utilisateurs peuvent accéder à l’élément à l’aide de périphériques d’entrée autres qu’une souris.
    *   Une icône de coche verte indique que l’élément est focusable au clavier.
    *   Un cercle gris avec une ligne diagonale indique que l’élément ne peut pas être focusé au clavier.

Pour obtenir la procédure pas à pas détaillée, accédez à Vérifier les éléments individuels pour le contraste du texte, le texte du lecteur d’écran et la prise en charge [du clavier.][DevtoolsAccessibilityTestInspectToolIndivElems]
<!-- = test-inspect-tool.md#check-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support -->


### <a name="using-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css"></a>Utilisation de l’outil Inspect pour pointer sur la page web afin de mettre en évidence le DOM et le CSS

Lorsque vous utilisez **l’outil Inspect,** la sélection d’un élément sur la page rendue ouvre **l’outil Elements.**  L’arborescence DOM affiche le code HTML de l’élément, et **Styles** les propriétés CSS qui sont appliquées à l’élément.

:::image type="complex" source="../media/a11y-testing-basics-inspector-selected-element.msft.png" alt-text="Détails sur l’élément sélectionné affiché dans l’outil Éléments" lightbox="../media/a11y-testing-basics-inspector-selected-element.msft.png":::
    Détails sur l’élément sélectionné affiché dans l’outil Éléments
:::image-end:::

Lorsque vous utilisez **l’outil Inspect,** lorsque vous pointez sur différentes parties de la page rendue avec les éléments ouverts, vous remarquerez que l’arborescence DOM s’actualit automatiquement. ****

Pour obtenir la procédure pas à pas détaillée, accédez à Utiliser l’outil Inspect pour pointer sur la page web afin de mettre en évidence le DOM et [CSS.][DevtoolsAccessibilityTestInspectToolDomCss]
<!-- = test-inspect-tool.md#use-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css -->


## <a name="verify-keyboard-support-by-using-the-tab-and-enter-keys"></a>Vérifier la prise en charge du clavier à l’aide des touches Tab et Entrée

Toutes les personnes n’utilisent pas de pointeur ou d’appareils tactiles, et certaines personnes peuvent avoir une vision faible. Pour répondre à ces scénarios, assurez-vous que les UIS fonctionnent avec les claviers.

Vous pouvez tester l’utilisation d’un clavier pour naviguer dans la page, en utilisant ou en sautant `Tab` `Shift+Tab` d’un élément à l’autre.  Si vous appuyez sur la page de démonstration, la première chose qui reçoit le focus est le formulaire de `Tab` recherche dans l’en-tête de page. ****  Appuyer même sur vous permet d’envoyer le formulaire, ce qui fonctionne, malgré le problème d’étiquette que nous avons détecté précédemment lors de l’utilisation de `Enter` **l’outil** Problèmes.

Pour obtenir la procédure pas à pas détaillée, accédez à Vérifier la prise en charge du clavier à l’aide des [touches Tab et Entrée.](test-tab-enter-keys.md)

Lorsque vous appuyez à la place, l’élément suivant qui reçoit le focus est le premier lien Plus dans la section de contenu de la page, comme indiqué par `Tab` `Enter` un plan. ****

:::image type="complex" source="../media/a11y-testing-keyboard-focus-on-element.msft.png" alt-text="Navigation dans la page à l’aide de la touche tabulation.  Le focus est affiché sur un lien Plus dans la page." lightbox="../media/a11y-testing-keyboard-focus-on-element.msft.png":::
    Navigation dans la page à l’aide de la `Tab` touche.  Le focus est affiché sur **un lien Plus** dans la page.
:::image-end:::

Une fois que vous avez passé le dernier lien **Plus,** la page défile vers le haut et il n’est pas clair quel élément a le focus.

Si vous regardez en bas à gauche de l’écran ou si **** vous utilisez un lecteur d’écran, vous pouvez savoir que le lien chats bleus dans le menu de navigation de la barre latérale a le focus, car le navigateur affiche l’URL `#cats` .

:::image type="complex" source="../media/a11y-testing-lack-of-focus-style.msft.png" alt-text="En raison d’un manque de style de mise au point, il est impossible de savoir où vous vous trouvez actuellement dans la page.  Le seul conseil est l’affichage de la cible du lien dans le coin inférieur gauche de la fenêtre." lightbox="../media/a11y-testing-lack-of-focus-style.msft.png":::
    En raison d’un manque de style de mise au point, il est impossible de savoir où vous vous trouvez actuellement dans la page.  Le seul conseil est l’affichage de la cible du lien dans le coin inférieur gauche de la fenêtre.
:::image-end:::

Une nouvelle `Tab` sélection vous place dans la boîte de texte d’entrée du formulaire de don.  Toutefois, vous ne pouvez pas atteindre **les boutons 50,** **100** ou **200** au-dessus de la boîte de texte d’entrée.  En outre, lorsque le focus est sur cette boîte de texte d’entrée, la sélection `Enter` n’envoie pas le formulaire.

:::image type="complex" source="../media/a11y-testing-form-field-with-outline.msft.png" alt-text="Le seul élément accessible au clavier dans le formulaire de don est le champ de texte d’entrée." lightbox="../media/a11y-testing-form-field-with-outline.msft.png":::
    Le seul élément accessible au clavier dans le formulaire de don est le champ de texte
:::image-end:::

La sélection de nouveau met le focus sur la barre de navigation supérieure, où vous pouvez choisir d’aller à une autre section de la page ou à une `Tab` `Enter` autre page du site.  Vous connaissez l’élément sur lequel vous vous concentrez, car il existe un plan de mise au point.  Pour sélectionner un lien dans la barre de navigation supérieure, utilisez ou mettez le focus sur un `Tab` `Shift+Tab` lien, puis sélectionnez `Enter` .

:::image type="complex" source="../media/a11y-testing-menu-with-outline.msft.png" alt-text="La barre de navigation supérieure présente une surbrillation et un plan de mise au point, et est donc accessible au clavier" lightbox="../media/a11y-testing-menu-with-outline.msft.png":::
    La barre de navigation supérieure présente une surbrillation et un plan de mise au point, et est donc accessible au clavier
:::image-end:::

Nous avons trouvé certains problèmes ici pour résoudre :

* Le menu de navigation de la barre latérale n’indique pas aux utilisateurs où se trouve le focus lorsque vous utilisez des claviers pour `Tab` se déplacer sur la page.
* Sur le formulaire de don, les boutons **50, 100, ** et **200** et la fonctionnalité d’soumission du formulaire ne fonctionnent pas lorsque vous utilisez le clavier.
* L’ordre de tabulation du clavier est incorrect. La touche permet de parcourir tous les liens Plus de la page avant `Tab` le menu de navigation de la barre latérale. ****  Cet ordre n’est pas utile, car la navigation à la barre latérale est destinée à vous permettre d’atteindre les différentes `Tab` sections de cette page. 

Nous allons analyser ces problèmes à l’aide de DevTools.


## <a name="analyze-keyboard-accessibility-issues-using-devtools"></a>Analyser les problèmes d’accessibilité du clavier à l’aide de DevTools


### <a name="analyzing-the-lack-of-indication-of-keyboard-focus-in-the-sidebar-menu"></a>Analyse de l’absence d’indication du focus du clavier dans le menu de la barre latérale

Pour savoir pourquoi la navigation de la barre latérale n’est pas optimisée comme prévu pour une utilisation avec les claviers, commencez par utiliser l’outil **Inspect** pour mettre en surbrillez un lien dans le menu de navigation de la barre latérale, puis recherchez l’élément dans l’arborescence `a` DOM. 

:::image type="complex" source="../media/a11y-testing-menu-link.msft.png" alt-text="Inspection du code source et des styles appliqués d’un lien dans le menu de navigation de la barre latérale" lightbox="../media/a11y-testing-menu-link.msft.png":::
    Inspection du code source et des styles appliqués d’un lien dans le menu de navigation de la barre latérale
:::image-end:::

Dans l’onglet **Styles,** vous pouvez voir le fichier CSS qui est appliqué au lien, et si vous sélectionnez le lien vers , le fichier s’ouvre dans l’outil `styles.css` **Sources.**

:::image type="complex" source="../media/a11y-testing-menu-link-styles.msft.png" alt-text="Styles appliqués au lien, affichés dans l’outil Sources" lightbox="../media/a11y-testing-menu-link-styles.msft.png":::
    Styles appliqués au lien, affichés dans l’outil Sources
:::image-end:::

Dans l’exemple ci-dessus, les styles de la page incluent un état sur l’élément de menu lorsque vous utilisez une souris, mais il n’y a aucun état dans le CSS pour les utilisateurs `hover` `focus` du clavier.  

En outre, dans cet exemple, les liens utilisent `outline: none` . Ce style permet de supprimer le plan qui est automatiquement ajouté par les navigateurs aux éléments lorsqu’ils ont le focus et que les claviers sont utilisés.  Pour éviter ce problème, n’utilisez pas `outline: none` .

Pour obtenir la procédure pas à pas détaillée, accédez à Analyser l’absence d’indication du focus du clavier dans [un menu de barre latérale.](test-analyze-no-focus-indicator.md)


### <a name="analyzing-the-lack-of-keyboard-support-in-the-donation-form"></a>Analyse de l’absence de prise en charge du clavier dans le formulaire de don

Les boutons du formulaire de don sont implémentés à l’aide de l’élément, qui n’est pas reconnu par les outils de test automatisés en tant que `div` contrôle sur un formulaire.

Pour ce faire, vous pouvez utiliser l’outil **Inspect** pour pointer sur les boutons du formulaire de don.  Par conséquent, aucun d’entre eux n’est accessible au **** clavier, comme indiqué par l’anneau gris sur la ligne de superposition d’informations qui peut être axée sur le clavier.  Comme indiqué **** dans **** les lignes Nom et rôle de la superposition d’informations, les boutons du formulaire de don n’ont pas non plus de nom et ont un rôle (représentant ou éléments), ce qui signifie qu’ils ne sont pas accessibles à la technologie `generic` `div` `span` d’assistance.

:::image type="complex" source="../media/a11y-testing-donation-button-info.msft.png" alt-text="L’inspection des boutons du formulaire indique qu’ils ne sont pas accessibles au clavier" lightbox="../media/a11y-testing-donation-button-info.msft.png":::
    L’inspection des boutons du formulaire indique qu’ils ne sont pas accessibles au clavier
:::image-end:::

Pour obtenir la procédure pas à pas détaillée, accédez à Analyser l’absence de prise en charge du clavier [dans un formulaire.](test-analyze-no-keyboard-support.md)

Si vous sélectionnez le **bouton Contrôle,** l’outil **Inspect** vous permet d’utiliser l’outil **Elements** et de vous faire voir le code HTML du formulaire.

```HTML
<div class="donationrow">
    <div class="donationbutton">50</div>
    <div class="donationbutton">100</div>
    <div class="donationbutton">200</div>
</div>
<div class="donationrow">
    <label for="freedonation">Other</label>
    <input id="freedonation" class="smallinput">
</div>
<div class="donationrow">
    <div class="submitbutton">Donate</div>
</div>
```

L’utilisation des éléments et des éléments est valide, ce qui permet à l’étiquette de fonctionner comme prévu et la boîte de texte `label` `input` est accessible au `input` clavier.  Le reste du formulaire utilise des éléments, faciles à styler mais sans `div` signification sémantique.

Ensuite, nous allons analyser la fonctionnalité JavaScript du formulaire. Dans **Éléments,** sélectionnez **l’onglet Écouteurs** d’événements pour analyser le javaScript du formulaire.

:::image type="complex" source="../media/a11y-testing-event-handlers-on-button.msft.png" alt-text="Onglet Écouteurs d’événements, avec un lien vers javaScript pour le formulaire" lightbox="../media/a11y-testing-event-handlers-on-button.msft.png":::
    Onglet **Écouteurs** d’événements, avec un lien vers javaScript pour le formulaire
:::image-end:::

Sous **l’onglet Écouteurs** d’événements, sélectionnez le lien pour ouvrir `buttons.js:18` l’outil **Sources,** puis examinez le JavaScript responsable des fonctionnalités du formulaire.

:::image type="complex" source="../media/a11y-testing-form-handling-javascript.msft.png" alt-text="JavaScript responsable de la fonctionnalité du formulaire de don, présentée dans l’outil Sources" lightbox="../media/a11y-testing-form-handling-javascript.msft.png":::
    JavaScript responsable de la fonctionnalité du formulaire de don, présentée dans l’outil **Sources**
:::image-end:::

L’utilisation d’événements avec des boutons est recommandée, car les événements fonctionnent à la fois avec les pointeurs de souris `click` `click` et les claviers.  Toutefois, étant donné qu’un élément n’est pas accessible au clavier et que le bouton Button est implémenté en tant `div` qu’élément, ce JavaScript s’exécute uniquement lorsqu’une souris est **** `div` utilisée.

L’utilisation d’un bouton en tant que bouton est un exemple classique dans lequel du JavaScript supplémentaire est nécessaire pour créer des fonctionnalités fournies `div` `button` par les éléments. Par conséquent, cela conduit à une expérience inaccessible.


### <a name="checking-the-accessibility-tree-for-keyboard-and-screen-reader-support"></a>Vérification de l’arborescence d’accessibilité pour la prise en charge du clavier et du lecteur d’écran

**L’utilisation de l’outil Inspect** pour vérifier individuellement chaque élément de la page prend beaucoup de temps.  Utilisez plutôt l’onglet **Accessibilité** pour naviguer dans l’arborescence **d’accessibilité de la page.**  L’arborescence d’accessibilité indique les informations que la page fournit aux technologies d’assistance telles que les lecteurs d’écran.

:::image type="complex" source="../media/a11y-testing-accessibility-tree.msft.png" alt-text="Bouton Du formulaire de don dans l’arborescence d’accessibilité" lightbox="../media/a11y-testing-accessibility-tree.msft.png":::
    Bouton Du formulaire de don dans **l’arborescence d’accessibilité**
:::image-end:::

Tout élément dans l’arborescence qui n’a pas de nom ou qui a un rôle de , est un problème, car cet élément n’est pas disponible pour les utilisateurs du clavier ou pour les personnes utilisant la technologie `generic` d’assistance.

Pour obtenir la procédure pas à pas détaillée, accédez à Vérifier l’arborescence d’accessibilité pour la prise en charge du clavier et du [lecteur d’écran.](test-accessibility-tree.md)


### <a name="analyzing-the-order-of-keyboard-access-to-sections-of-the-page"></a>Analyse de l’ordre d’accès au clavier aux sections de la page

Un autre problème est l’ordre de tabulation peu clair sur la page.  Les utilisateurs du clavier n’atteignent le menu de navigation de la barre latérale qu’après avoir tabulationé tous les liens **Plus** dans toute la page.  Dans cet exemple, le menu de navigation de la barre latérale est destiné à être un raccourci vers différentes sections de cette page.  Cet ordre de tabulation entraîne une expérience utilisateur médiocre. 

La raison de cette confusion est `Tab` qu’elle est déterminée par l’ordre source du document.  L’ordre de tabulation peut également être modifié à l’aide de l’attribut sur un élément qui sort cet élément de `tabindex` l’ordre de la source par défaut.

Dans le code source du document, le menu de navigation de la barre latérale apparaît après le contenu principal de la page.  Le menu de navigation de la barre latérale apparaît au-dessus du contenu principal de la page uniquement car le menu de navigation de la barre latérale a été positionné à l’aide de CSS.

L’ordre source d’un document est important pour la technologie d’assistance et peut être différent de l’ordre dans lequel les éléments apparaissent sur la page rendue.  À l’aide de CSS, vous pouvez ré-orderer les éléments de page d’une manière visuelle, mais cela ne signifie pas que les technologies d’assistance telles que les lecteurs d’écran représentent les éléments de page dans le même ordre que ce CSS.

Vous pouvez tester l’ordre des éléments de page à l’aide de l’Observateur de commandes **source** dans **l’onglet** Accessibilité.  Faites défiler jusqu’au bas et cochez la case Afficher la **commande** source.  Désormais, lorsque vous naviguez dans l’arborescence DOM dans l’outil **Éléments,** par exemple en sélectionnant l’élément, les superpositions numériques sont affichées dans les sections de la page rendue qui représentent l’ordre `header` source. 

:::image type="complex" source="../media/a11y-testing-source-order-viewer.msft.png" alt-text="L’turning on the Source Order Viewer shows the order of the elements in the source code as numeric overlays on the page" lightbox="../media/a11y-testing-source-order-viewer.msft.png":::
    L’turning on the **Source Order Viewer shows** the order of the elements in the source code as numeric overlays on the page
:::image-end:::

Pour obtenir la procédure pas à pas détaillée, accédez à la prise en charge du clavier test à l’aide de l’Observateur de [commandes source.](test-tab-key-source-order-viewer.md)


## <a name="testing-contrast-of-text-colors-in-various-states"></a>Test du contraste des couleurs de texte dans différents états

**L’outil Inspect** signale les problèmes d’accessibilité pour un état à la fois.  Tout d’abord, nous allons décrire la limitation de l’utilisation de l’outil Inspect pour afficher uniquement l’état statique d’un élément de page.  Nous allons ensuite expliquer comment inspecter les autres états d’un élément de page en sélectionnant **\:hov (Toggle Element State)** sous l’onglet **Styles.**

### <a name="checking-text-color-contrast-in-the-default-state"></a>Vérification du contraste de couleur du texte dans l’état par défaut

Outre les tests **automatiques** de contraste de couleur dans l’outil Problèmes, vous pouvez également utiliser l’outil **Inspect** pour vérifier si les éléments de page individuels ont un contraste suffisant.  Si des informations de contraste sont disponibles, la superposition **Inspect** affiche le coefficient de contraste et un élément de case à cocher.  Une icône de coche verte indique qu’il y a suffisamment de contraste et qu’une icône d’alerte jaune indique un contraste insuffisant.

Par exemple, les liens dans le menu de navigation de la barre latérale ont un contraste suffisant, mais l’élément vert de la liste **Des chiens** dans la section **État** du don ne le fait pas.  Un élément qui n’a pas assez de contraste est marqué par un avertissement dans la superposition **Inspect.**

:::row:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Le contraste des liens dans le menu de navigation de la barre latérale est suffisant, comme illustré dans la superposition Inspect" lightbox="../media/a11y-testing-enough-contrast.msft.png":::
            Le contraste des liens dans le menu de navigation de la barre latérale est suffisant, comme illustré dans la superposition **Inspect** :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Un élément qui n’a pas assez de contraste est marqué par un avertissement dans la superposition Inspect" lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
            Un élément qui n’a pas assez de contraste est marqué par un avertissement dans la superposition **Inspect** :::image-end:::
    :::column-end:::
:::row-end:::

**L’utilisation de l’outil** Inspect de cette façon ne teste pas complètement vos éléments. Les éléments de la page peuvent avoir des états différents, qui doivent tous être testés. Par exemple, si vous pointez la souris sur le menu de navigation de la barre latérale, notez l’animation qui modifie la couleur des liens.

:::image type="complex" source="../media/a11y-testing-hover.msft.png" alt-text="Élément de menu affichant différentes couleurs lorsque le pointeur de la souris est sur celui-ci" lightbox="../media/a11y-testing-hover.msft.png":::
    Élément de menu affichant différentes couleurs lorsque le pointeur de la souris est sur celui-ci
:::image-end:::

### <a name="verify-accessibility-of-all-states-of-elements-such-as-the-contrast-on-hover"></a>Vérifier l’accessibilité de tous les états des éléments, tels que le contraste lors du survol

Lorsque vous utilisez DevTools, vous devez simuler tous les états de votre élément, car l’outil **Inspect** n’affiche pas d’informations pour tous les états en même temps. Dans cet exemple, lorsque vous utilisez l’outil **Inspect,** vous ne pouvez pas atteindre l’état du lien Chats dans le menu de navigation de la barre latérale pour analyser le coefficient de contraste dans un état, car l’état dans vos `hover` styles **** `hover` `hover` n’est pas déclenché.  Au lieu de cela, vous devez simuler l’état de l’élément de menu **Chats** à l’aide de la simulation d’état dans l’onglet **Styles.**

Pour obtenir la procédure pas à pas détaillée, accédez à [Vérifier l’accessibilité de tous les états des éléments.](test-inspect-states.md)

Activer **l’outil Inspect,** puis dans la page rendue, sélectionnez le lien **chats** bleus dans le menu de navigation de la barre latérale.  **L’outil** Elements s’ouvre, avec `a` l’élément sélectionné dans l’arborescence DOM.  Si nécessaire, dans l’arborescence DOM, accédez à l’élément qui a un `hover` état dans le CSS.  Dans ce cas, `a` l’élément a un `hover` état.

:::image type="complex" source="../media/a11y-testing-inspecting-link-to-hover.msft.png" alt-text="Inspection de l’élément dont l’état de pointage est dans l’outil Éléments" lightbox="../media/a11y-testing-inspecting-link-to-hover.msft.png":::
    Inspection de l’élément dont l’état de pointage est dans l’outil Éléments
:::image-end:::

Sous **l’onglet Styles,** sélectionnez le bouton **\:hov (Toggle Element State).**  Ensuite, utilisez les case **à cocher d’état** de l’élément Force pour choisir l’état à simuler.

:::image type="complex" source="../media/a11y-testing-state-simulation.msft.png" alt-text="Fonctionnalité de simulation d’état affichant toutes les options" lightbox="../media/a11y-testing-state-simulation.msft.png":::
    Fonctionnalité de simulation d’état affichant toutes les options
:::image-end:::

Cochez **la case \:hover.**  Un point jaune apparaît maintenant à côté de l’élément DOM, indiquant que l’élément DOM a un état simulé.  En outre, le lien **Chats** dans le menu de navigation de la barre latérale est désormais mis en surbrillon dans la page, comme si le pointeur de la souris pointait sur elle.

:::image type="complex" source="../media/a11y-testing-hover-simulated.msft.png" alt-text="DevTools simulant un état de pointage" lightbox="../media/a11y-testing-hover-simulated.msft.png":::
    DevTools simulant un état de pointage
:::image-end:::

Une fois l’état simulé appliqué, vous pouvez à nouveau utiliser l’outil **Inspect** pour vérifier le contraste de l’élément lorsque l’utilisateur passe dessus.  Dans ce cas, le contraste n’est pas assez élevé.

:::image type="complex" source="../media/a11y-testing-hover-contrast-testing.msft.png" alt-text="Test du contraste d’un élément dans un état de pointer simulé" lightbox="../media/a11y-testing-hover-contrast-testing.msft.png":::
    Test du contraste d’un élément dans un état de pointer simulé
:::image-end:::

La simulation d’état est également un bon moyen de vérifier si vous avez pris en compte différents besoins de l’utilisateur.  Pour le menu de navigation de la barre latérale, vous pouvez détecter que `:focus` l’état présente un problème de contraste.


## <a name="use-the-rendering-tool-to-test-accessibility-for-visual-impairment"></a>Utiliser l’outil de rendu pour tester l’accessibilité des troubles visuels

### <a name="check-contrast-issues-with-dark-theme-and-light-themes"></a>Vérifier les problèmes de contraste avec le thème foncé et les thèmes clair

En ce qui concerne l’accessibilité des couleurs, vous devez également tenir compte du fait qu’il peut y avoir différents thèmes que vous devez tester pour les problèmes de contraste.  La plupart des systèmes d’exploitation ont un mode sombre et un mode clair.  Votre page web peut réagir à ces différents paramètres à l’aide de requêtes multimédias CSS.

Cette page de démonstration a un thème clair et foncé.  Vous pouvez tester les deux thèmes sans modifier votre système d’exploitation, à l’aide de la [simulation][DevToolsColorSchemeSimulation] de jeu de couleurs foncées ou claires dans **l’outil de** rendu.  Jusqu’à présent, cet article a examiné la page de démonstration avec un système d’exploitation utilisant un paramètre de thème foncé.  Si nous simulons à la place un **** schéma de lumière, puis actualisons la page, l’outil Problèmes affiche six problèmes de contraste de couleur au lieu de deux.

Pour obtenir la procédure pas à pas détaillée, accédez à Vérifier les problèmes de contraste avec le thème foncé [et le thème clair.](test-dark-mode.md)


Lorsque vous basculez vers un thème clair dans **l’outil de** rendu, notez les éléments suivants.

*  De nouveaux problèmes de contraste sont détectés en raison de la modification du thème clair.
*  Toute la section **État du** don de la page est illisible en mode clair.

:::row:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png" alt-text="Nouveaux problèmes de contraste détectés en raison de la modification du thème clair" lightbox="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png":::
            Nouveaux problèmes de contraste détectés en raison de la modification du thème clair :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-donation-state-light-contrast.msft.png" alt-text="Les éléments d’état du don marqués comme problèmes de contraste en mode clair" lightbox="../media/a11y-testing-donation-state-light-contrast.msft.png":::
            Les éléments d’état du don marqués comme problèmes de contraste en mode clair :::image-end:::
    :::column-end:::
:::row-end:::


### <a name="verify-that-the-webpage-is-usable-by-people-with-color-blindness"></a>Vérifier que la page web est utilisable par les personnes daltonismes

Les différents états de don utilisent la couleur (rouge, vert, jaune) comme seul moyen de différencier les états de financement.  Cependant, vous ne pouvez pas vous attendre à ce que tous vos utilisateurs utilisent ces couleurs comme prévu.  Si vous [][DevToolsVisionDeficiencies] utilisez la fonctionnalité d’émulation des défaillances visuelles de DevTools, vous pouvez découvrir que ce n’est pas assez bon, en simulant la façon dont les personnes ayant une vision différente persoraient votre conception.
Pour obtenir la procédure pas à pas détaillée, accédez à Vérifier que la page est utilisable par les personnes [daltonistes.](test-color-blindness.md)
:::image type="complex" source="../media/a11y-testing-simulating-protanopia.msft.png" alt-text="Affichage de la page en tant que personne présentant une protanopie (daltonisme rouge)" lightbox="../media/a11y-testing-simulating-protanopia.msft.png":::
    Affichage de la page comme si une personne présentant une protanopie (daltonisme rouge) la voit
:::image-end:::



### <a name="verify-that-the-webpage-is-usable-with-blurred-vision"></a>Vérifier que la page web est utilisable avec une vision floue

Une autre fonctionnalité intéressante de l’outil **de** rendu est que vous pouvez simuler une vision floue.  Si nous **** choisissons l’option Vision floue dans la liste déroulante Émuler les défauts de **vision,** nous pouvons voir que l’ombre portée sur le texte dans le menu supérieur complique la lecture des éléments de menu.
Pour obtenir la procédure pas à pas détaillée, accédez à Vérifier que la page est [utilisable avec une vision floue.](test-blurred-vision.md)

:::image type="complex" source="../media/a11y-testing-simulating-blur.msft.png" alt-text="La simulation d’une page floue peut révéler des problèmes d’accessibilité" lightbox="../media/a11y-testing-simulating-blur.msft.png":::
    La simulation d’une page floue peut révéler des problèmes d’accessibilité
:::image-end:::


### <a name="verify-that-the-page-is-usable-with-ui-animation-turned-off-reduced-motion"></a>Vérifier que la page est utilisable avec l’animation de l’interface utilisateur désactivée (mouvement réduit)

Un autre paramètre que les systèmes d’exploitation viennent avec ces jours-ci est un moyen de désactiver les animations.  Les animations peuvent faciliter l’utilisation d’un produit, mais elles peuvent également provoquer de nombreux problèmes, allant de la confusion à la confusion. C’est pourquoi vos produits ne doivent pas afficher d’animations aux utilisateurs qui les ont désactivées dans le système d’exploitation.  À l’aide d’une requête multimédia CSS, vous pouvez vérifier si l’utilisateur souhaite voir les animations et les désactiver en conséquence.  Et, comme avec le mode sombre et clair, il existe un moyen de simuler un mouvement réduit à l’aide [de DevTools][DevToolsReducedMotion].

Dans la page de démonstration, la arrêt des animations arrête le défilement fluide de la page lorsque vous sélectionnez différentes parties du menu de navigation de la barre latérale.  Pour ce faire, insérez le paramètre de défilement fluide dans CSS dans une requête multimédia :

:::image type="complex" source="../media/a11y-testing-simulating-reduced-motion.msft.png" alt-text="Simulation d’un mouvement réduit et du CSS qui permet de s’assurer que le défilement fluide se produit uniquement lorsque l’utilisateur le souhaite" lightbox="../media/a11y-testing-simulating-reduced-motion.msft.png":::
    Simulation d’un mouvement réduit et du CSS qui permet de s’assurer que le défilement fluide se produit uniquement lorsque l’utilisateur le souhaite
:::image-end:::

```css
@media (prefers-reduced-motion: no-preference) {
  html {
    scroll-behavior: smooth;
  }
}
```

Cette requête multimédia CSS exécute l’animation de « défilement fluide ».  Toutefois, l’animation de la barre de **** navigation supérieure, du menu de navigation de la barre latérale et des liens Plus s’exécute toujours, même lorsque l’utilisateur ne souhaite pas voir d’animations. Ces autres animations doivent être exécutés de manière conditionnable, par exemple en ajoutant des requêtes multimédias supplémentaires.

Pour obtenir la procédure pas à pas détaillée, accédez à Vérifier que la page est utilisable avec l’animation de [l’interface utilisateur désactivée.](test-reduced-ui-motion.md)


## <a name="what-to-do-next"></a>Que faire ensuite ?

Nous avons abordé un certain nombre d’outils que vous pouvez utiliser pour vous assurer que vous prenez en compte les problèmes d’accessibilité dans vos produits.  Ces outils vont des vérifications automatisées et manuelles aux vérifications des détails jusqu’à la simulation de différents états et environnements.  Ces outils sont résumés dans les fonctionnalités [de test d’accessibilité dans DevTools](reference.md).  Les outils automatisés ne peuvent pas trouver tous les problèmes dans un produit, car de nombreux obstacles à l’accessibilité s’affiche uniquement lors d’une utilisation interactive.

Aucun de ces outils ne peut remplacer une série appropriée de tests de vos produits par des personnes qui utilisent des technologies d’assistance et qui suivent un plan pour vérifier tous les tests requis. Vous pouvez également utiliser la fonctionnalité [Évaluations][AccessibilityInsightsAssessment] de [Insights sur l’accessibilité.][AccessibilityInsights]  Vous devrez peut-être effectuer des vérifications supplémentaires telles que :

* Test lors d’un zoom avant.
* Test avec les lecteurs d’écran.
* Test avec reconnaissance vocale.
* Test en mode de contraste élevé.

Une autre façon de savoir comment améliorer votre produit web consiste à utiliser [l’extension dehint web pour Visual Studio Code][WebhintForCode].  Cette extension indicateurs les problèmes d’accessibilité facilement détectables dans votre code source et donne des informations sur la façon de les résoudre.

:::image type="complex" source="../media/a11y-testing-webhint-in-vs-code.msft.png" alt-text="Webhint dans Visual Studio Code, montrant un problème d’accessibilité en soulignementant l’élément HTML et en affichant une explication du problème" lightbox="../media/a11y-testing-webhint-in-vs-code.msft.png":::
    Webhint dans Visual Studio Code, montrant un problème d’accessibilité en soulignementant l’élément HTML et en affichant une explication du problème
:::image-end:::

Nous travaillons en permanence sur les nouvelles fonctionnalités d’accessibilité pour DevTools.  S’il vous manque quelque chose, envoyez-nous un message et dites-nous ce que nous pouvons faire.


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]


<!-- links -->
[DevToolsMediaQueries]: ../device-mode/index.md#show-media-queries "Afficher les requêtes multimédias : émuler des appareils mobiles dans Microsoft Edge devTools | Documents Microsoft"
[DevToolsDeviceModeIndex]: ../device-mode/index.md "Émuler des appareils mobiles dans Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsAccessibilityReference]: reference.md "Fonctionnalités de test de l’accessibilité dans DevTools | Documents Microsoft"
[DevToolsColorSchemeSimulation]: ./preferred-color-scheme-simulation.md "Modèle de simulation de jeu de couleurs sombres ou claires | Documents Microsoft"
[DevToolsIssuesTool]: ../issues/index.md "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"
[DevToolsReducedMotion]: ./reduced-motion-simulation.md "Simulation de mouvement réduit | Documents Microsoft"
[DevToolsVisionDeficiencies]: ./emulate-vision-deficiencies.md "Émuler les défaillances visuelles | Documents Microsoft"
<!-- links into test-issues-tool.md -->
[DevToolsAccessibilityTestIssuesToolViewAccSection]: test-issues-tool.md#view-the-accessibility-section-of-the-issues-tool "Afficher la section Accessibilité de l’outil Problèmes - Tester automatiquement une page web pour les problèmes d’accessibilité | Documents Microsoft"
[DevtoolsAccessibilityTestIssuesToolCheckFieldsLabels]: test-issues-tool.md#verify-that-input-fields-have-labels "Vérifiez que les champs d’entrée ont des étiquettes : testez automatiquement une page web pour les problèmes d’accessibilité | Documents Microsoft" 
[DevtoolsAccessibilityTestIssuesToolCheckAltText]: test-issues-tool.md#verify-that-images-have-alt-text "Vérifiez que les images ont un texte de alt - Testez automatiquement une page web pour les problèmes d’accessibilité | Documents Microsoft "
[DevtoolsAccessibilityTestIssuesToolCheckContrast]: test-issues-tool.md#verify-that-text-colors-have-enough-contrast "Vérifiez que le contraste des couleurs du texte est suffisant : testez automatiquement une page web pour les problèmes d’accessibilité | Documents Microsoft"
<!-- links into test-inspect-tool.md -->
[DevtoolsAccessibilityTestInspectToolColorHighlighting]: test-inspect-tool.md#identify-nested-regions-using-color-highlighting "Identifier les régions imbrmbrées à l’aide de la mise en surbrillance des couleurs : utilisez l’outil Inspect pour détecter les problèmes d’accessibilité en pointant sur la page web | Documents Microsoft"
[DevtoolsAccessibilityTestInspectToolIndivElems]: test-inspect-tool.md#check-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support "Vérifier le contraste du texte, le texte du lecteur d’écran et la prise en charge du clavier des éléments individuels : utilisez l’outil Inspect pour détecter les problèmes d’accessibilité en pointant sur la page web | Documents Microsoft"
[DevtoolsAccessibilityTestInspectToolDomCss]: test-inspect-tool.md#use-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css "Utilisez l’outil Inspect pour pointer sur la page web afin de mettre en évidence le DOM et le CSS : utilisez l’outil Inspect pour détecter les problèmes d’accessibilité en pointant sur la page web | Documents Microsoft"
<!-- external links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
[W3CContrastRatio]: https://www.w3.org/TR/WCAG21/#dfn-contrast-ratio "taux de contraste | W3C"
[WCAG]: https://www.w3.org/TR/WCAG21/ "Recommandations en matière d’accessibilité du contenu web | W3C"
[AccessibilityInsightsAssessment]: https://accessibilityinsights.io/docs/en/web/getstarted/assessment/ "Évaluation dans Accessibility Insights for Web | Informations sur l’accessibilité"
[AccessibilityInsights]: https://accessibilityinsights.io "Informations sur l’accessibilité"
[Lighthouse]: https://developers.google.com/web/tools/lighthouse/ "Les | Google"
[WebhintForCode]:https://aka.ms/webhint4code "webhint | Visual Studio Marketplace"
