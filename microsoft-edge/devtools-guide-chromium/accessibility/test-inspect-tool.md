---
description: Utilisez l’outil Inspect pour détecter les problèmes d’accessibilité en pointant sur la page web.
title: Utiliser l’outil Inspect pour détecter les problèmes d’accessibilité en pointant sur la page web
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: c95116d38e5b0bda88af43ef8bfde4204b8cb372
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597336"
---
# <a name="use-the-inspect-tool-to-detect-accessibility-issues-by-hovering-over-the-webpage"></a>Utiliser l’outil Inspect pour détecter les problèmes d’accessibilité en pointant sur la page web

**L’outil Inspect** affiche des informations sur les éléments individuels lorsque vous pointez sur la page web affichée, y compris les informations d’accessibilité.
En revanche, **l’outil Problèmes** signale automatiquement les problèmes pour la page web entière.

Le **bouton d’outil** Inspect \( Inspect \) se trouve dans le coin supérieur gauche ![ de ](../media/inspect-icon.msft.png) DevTools.  Lorsque vous sélectionnez le **bouton Inspecter** l’outil, le bouton devient bleu, ce qui indique que l’outil **Inspect** est actif.

Lorsque **l’outil Inspect** est actif, le fait de pointer sur un élément de la page web affichée affiche la superposition **Inspect.** Cette superposition affiche des informations générales et des informations d’accessibilité sur cet élément.  La section **Accessibilité de** la superposition **Inspect** affiche des informations sur le contraste de couleur du texte, le texte du lecteur d’écran et la prise en charge du clavier.

:::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="L’outil Inspect, montrant la zone de l’élément sous la mesure d’une superposition multicolore, et montrant les détails de l’élément sous la mesure d’une superposition d’informations importante" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
    **L’outil Inspect,** montrant la zone de l’élément sous la mesure d’une superposition multicolore, et montrant les détails de l’élément sous la mesure d’une superposition d’informations importante
:::image-end:::


## <a name="check-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support"></a>Vérifier le contraste du texte, le texte du lecteur d’écran et la prise en charge du clavier pour chaque élément

<!-- Inspect tool: Accessibility section of overlay -->

1.  Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.

1.  Sélectionnez **le bouton Inspect** \( Inspect \) dans le coin supérieur gauche de ![ DevTools afin que l’icône soit mise en surbrillant ](../media/inspect-icon.msft.png) (bleu).

    :::image type="complex" source="../media/a11y-testing-basics-inspector.msft.png" alt-text="Pour activer l’outil Inspect, sélectionnez le bouton Inspecter" lightbox="../media/a11y-testing-basics-inspector.msft.png":::
        Pour activer l’outil **Inspect,** sélectionnez le **bouton Inspecter**
    :::image-end:::

1.  Pointez sur n’importe quel élément de la page web de démonstration rendue.  **L’outil Inspect** affiche une superposition d’informations sous l’élément dans la page web rendue.

    :::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="Outil Inspect, montrant la disposition de l’élément sous forme de superposition multicolore et montrant les détails de l’élément sous la forme d’une superposition d’informations importante" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
        Outil **Inspect,** montrant la disposition de l’élément sous forme de superposition multicolore et montrant les détails de l’élément sous la forme d’une superposition d’informations importante
    :::image-end:::

La partie inférieure de la superposition **Inspect** comporte une section **Accessibilité** qui contient les informations suivantes :

*   **Le** contraste définit si un élément peut être compris par les personnes ayant une vision faible.  Le [coefficient de contraste][W3CContrastRatio] défini par les directives [WCAG][WCAG] indique s’il y a suffisamment de contraste (icône de coche verte) ou pas assez (icône de point d’exclamation orange).

*   **Les technologies** **d’assistance** telles que les lecteurs d’écran signalent l’élément en fonction du nom et du rôle.
    *   Le **nom est** le contenu de texte d’un `a` élément.  Pour l’élément, `<a href="/">About Us</a>` le nom **affiché** dans l’outil Inspect est « À propos de nous ».
    *   Rôle **de** l’élément.  Il s’agit généralement du nom de l’élément, tel `article` que , , ou `img` `link` `heading` .  Les `div` éléments et les éléments sont `span` appelés `generic` .

*   **La mise au point du clavier** indique si les utilisateurs peuvent accéder à l’élément quel que soit le périphérique d’entrée.
    *   Une icône de coche verte indique que l’élément est focusable au clavier.
    *   Un cercle gris avec une ligne diagonale indique que l’élément ne peut pas être mis au point au clavier.


## <a name="additional-information-in-the-inspect-overlay"></a>Informations supplémentaires dans la superposition Inspect

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

La partie supérieure de la superposition **Inspect,** qui se trouve au-dessus de la section **Accessibilité,** répertorie les détails suivants de l’élément.

*   Type de disposition. Si l’élément est positionné à l’aide d’une flexbox ou d’une grille, une icône \(![Icône De disposition de la grille](../media/grid-icon.msft.png)\) s’affiche.
*   Nom de l’élément, tel `h1` que `h2` , ou `div` .
*   Dimensions de l’élément en pixels.
*   Couleur sous la forme d’un échantillon de couleur (ou d’un petit carré de couleur) et sous forme de chaîne (par `#336699` exemple).
*   Informations sur les polices, telles que la taille et les familles de polices.
*   Marge et remplissage en pixels.


## <a name="identify-nested-regions-using-color-highlighting"></a>Identifier les régions imbrmbrées à l’aide de la mise en surbrillance des couleurs 

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

En plus de la superposition d’informations, l’outil **Inspect** fournit également une couleur de région similaire au pointage dans l’arborescence DOM de l’outil **Elements.**

1.  Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.

1.  Sélectionnez **le bouton Inspecter** \( Inspecter l’icône de l’outil \) dans le coin supérieur gauche de ![ DevTools, afin que le bouton soit mis en surbrillant ](../media/inspect-icon.msft.png) (bleu).

1.  Pointez sur différentes parties de la page web de démonstration rendue.  Chaque élément de la page web s’affiche désormais avec une superposition multicolore. Cette superposition multicolore peut afficher des régions imbrmbrées à l’intérieur d’un élément. Par exemple, pointez sur la marge gauche des **chats**.  **L’outil Inspect** met en évidence plusieurs parties rectangulaires de la section **Chats** avec des couleurs différentes, montrant la disposition qui résulte des définitions de flexbox CSS sur votre page web.

:::image type="complex" source="../media/inspect-tool-flexbox-overlay.msft.png" alt-text="Superposition de flexbox multicolore et superposition d’informations lors de l’utilisation de l’outil Inspect" lightbox="../media/inspect-tool-flexbox-overlay.msft.png":::
    Superposition de flexbox multicolore et superposition d’informations lors de l’utilisation de **l’outil Inspect**
:::image-end:::

Pour configurer la superposition de la grille ou la superposition flexbox, dans l’outil **Éléments,** sélectionnez **l’onglet** Disposition.  Pour plus d’informations, [accédez à Inspect CSS Grid](..\css\grid.md).


## <a name="use-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css"></a>Utiliser l’outil Inspect pour pointer sur la page web afin de mettre en évidence le DOM et le CSS

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

1.  Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.

1.  Sélectionnez **le bouton** Inspecter \( l’outil Inspect \) dans le coin supérieur gauche de ![ DevTools, afin que le bouton soit mis en surbrillant ](../media/inspect-icon.msft.png) (bleu).

1.  Sélectionnez **l’outil Éléments.**

1.  Avec **l’outil Inspect** actif, pointez sur différentes parties de la page web rendue.  Dans **l’outil Elements,** l’arborescence DOM HTML se développe automatiquement pour afficher des informations sur l’élément sur quoi vous pointez.  Le survol n’entraîne pas la mise à jour du volet **Styles.**

1.  Sélectionnez maintenant n’importe quel élément dans la page web rendue.  **L’outil** Elements s’ouvre et affiche automatiquement le code HTML de l’élément dans l’arborescence DOM. L’outil affiche également le CSS appliqué sur l’élément dans le **volet Styles.**  La sélection d’un élément sur la page web rendue permet de mettre hors service **l’outil Inspect.**

:::image type="complex" source="../media/a11y-testing-basics-inspector-selected-element.msft.png" alt-text="Les détails sur l’élément sélectionné sont affichés dans l’outil Éléments" lightbox="../media/a11y-testing-basics-inspector-selected-element.msft.png":::
    Les détails sur l’élément sélectionné sont affichés dans **l’outil Éléments**
:::image-end:::

Après avoir sélectionné un élément dans la page **** rendue, vous pouvez utiliser l’onglet **** Accessibilité (près de l’onglet **Styles)** pour afficher l’arborescence d’accessibilité et utiliser l’Afficheur des commandes **source.**


## <a name="see-also"></a>Articles associés

*  [Inspecter un nœud](../dom/index.md#inspect-a-node)
*  [Vérifier le contraste de couleur du texte à l’état par défaut à l’aide de l’outil Inspect](test-inspect-text-contrast.md)
*  [Vue d’ensemble des tests d’accessibilité à l’aide de DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
[W3CContrastRatio]: https://www.w3.org/TR/WCAG21/#dfn-contrast-ratio "taux de contraste | W3C"
[WCAG]: https://www.w3.org/TR/WCAG21/ "Recommandations en matière d’accessibilité du contenu web | W3C"
