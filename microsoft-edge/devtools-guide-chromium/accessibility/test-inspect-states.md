---
description: Inspectez l’accessibilité de tous les états des éléments, tels que le contraste du texte pendant l’état de pointage, dans le volet Styles à l’aide de l’état de l’élément Bascule.
title: Vérifier l’accessibilité de tous les états d’éléments
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 129a89f94925de24a4e649bd91f513de031d6b4a
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597362"
---
# <a name="verify-accessibility-of-all-states-of-elements"></a>Vérifier l’accessibilité de tous les états d’éléments

<!-- 5. STYLES: TOGGLE STATE -->

Vérifiez l’accessibilité de tous les états des éléments, tels que le contraste de couleur du texte pendant `hover` l’état.  **L’outil Inspect** signale les problèmes d’accessibilité pour un état à la fois.  Pour vérifier l’accessibilité des différents états des éléments, dans l’onglet **Styles,** sélectionnez **\:hov** (**Toggle Element State**), comme décrit dans cet article. Nous montrons d’abord pourquoi la simulation d’état est nécessaire à l’aide de l’outil **Inspect,** puis nous montrons comment utiliser la simulation d’état.


## <a name="checking-text-color-contrast-in-the-default-state"></a>Vérification du contraste de couleur du texte dans l’état par défaut

<!-- Inspect tool: information overlay: Accessibility section: Contrast row -->

Outre les tests **automatiques** de contraste de couleur dans l’outil Problèmes, vous pouvez également utiliser l’outil **Inspect** pour vérifier si les éléments de page individuels ont un contraste suffisant.  Si des informations de contraste sont disponibles, la superposition **Inspect** affiche le coefficient de contraste et un élément de case à cocher.  Une icône de coche verte indique qu’il y a suffisamment de contraste et une icône d’alerte jaune indique qu’il n’y en a pas assez.

Par exemple, les liens du menu de navigation de la barre latérale ont un contraste suffisant.  Toutefois, **** l’élément vert de la **liste** État du don ne présente pas suffisamment de contraste et est donc marqué par un avertissement dans la superposition **Inspect.**

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
        

## <a name="hovering-when-the-inspect-tool-is-active-doesnt-show-the-text-color-contrast-for-the-hover-state"></a>Le fait de pointer lorsque l’outil Inspect est actif n’affiche pas le contraste de couleur du texte pour l’état de pointage

La **superposition** des informations de l’outil Inspect ne représente qu’un seul état.  Les éléments de la page peuvent avoir différents états, qui doivent tous être testés.  Par exemple, lorsque vous placez le pointeur de la souris sur le menu de la page de démonstration de test d’accessibilité, vous obtenez une animation qui modifie les couleurs. Effectuez les étapes suivantes.

1.  Ouvrez la [page web de démonstration des tests d’accessibilité][DevToolsA11yErrorsDemopage] dans un nouvel onglet.

1.  Pointez sur les éléments de menu bleu dans le menu de navigation de la barre latérale.  Notez que chaque élément possède une animation.

    :::image type="complex" source="../media/a11y-testing-hover.msft.png" alt-text="Élément de menu affichant différentes couleurs lorsque le pointeur de la souris est sur celui-ci" lightbox="../media/a11y-testing-hover.msft.png":::
        Élément de menu affichant différentes couleurs lorsque le pointeur de la souris est sur celui-ci
    :::image-end:::
    
À présent, utilisez l’outil Inspect. Lorsque l’outil Inspect est utilisé, les animations sur les éléments de menu ne s’exécutent pas lorsque vous pointez dessus.  Lorsque vous utilisez l’outil Inspect, vous ne pouvez pas atteindre l’état des éléments de menu pour tester le coefficient de contraste, car l’état de vos `hover` `hover` styles n’est pas déclenché.  
    
Pour confirmer que vos animations ne s’exécutent pas, effectuez les étapes suivantes.
    
1.  Sélectionnez **le bouton Inspect** \( le bouton Inspect \) dans le coin supérieur gauche de ![ DevTools afin que l’icône soit en surbrillant ](../media/inspect-icon.msft.png) (bleu).

1.  Pointez sur les liens bleus dans le menu de navigation de la barre latérale.  Les animations des éléments de menu ne s’exécutent pas. Au lieu de cela, les éléments de menu sont affichés à l’aide de couleurs et de sur-points forts pour la superposition flexbox.

La recherche d’un contraste de texte suffisant de cette façon n’est pas suffisante, car les éléments de la page peuvent avoir des états différents.


## <a name="use-state-simulation-to-simulate-the-hover-state-of-an-animated-menu-item"></a>Utiliser la simulation d’état pour simuler l’état de pointer d’un élément de menu animé 

<!-- Elements tool: Styles pane: Toggle Element State -->

Lorsque **l’outil Inspect** est actif, au lieu de pointer sur un élément animé, vous devez simuler l’état de l’élément de menu.  Pour simuler l’état d’un élément de menu, utilisez la simulation d’état dans le **volet Styles.**  Le **volet Styles** possède un bouton **\:hov** (**Toggle Element State**), qui affiche un groupe de case à cocher avec l’état de l’élément **Force**.

Pour activer l’état de pointer lors de l’utilisation de l’outil Inspect :

1.  S’il n’est pas déjà ouvert, ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration de test d’accessibilité dans un nouvel onglet.  Sélectionnez **ensuite F12** pour ouvrir DevTools.

1.  Sélectionnez **le bouton Inspect** \( Inspect tool button \) dans le coin supérieur gauche de ![ DevTools afin que l’icône soit mise en surbrillant ](../media/inspect-icon.msft.png) (bleu).

1.  Dans la page web rendue, sélectionnez le lien **chats** bleus dans le menu de navigation de la barre latérale.  **L’outil Elements** s’ouvre, avec l’élément `<a href="#cats">Cats</a>` sélectionné.

    :::image type="complex" source="../media/a11y-testing-inspecting-link-to-hover.msft.png" alt-text="Inspection de l’élément dont l’état de pointage est dans l’outil Elements" lightbox="../media/a11y-testing-inspecting-link-to-hover.msft.png":::
        Inspection de l’élément dont l’état de pointage est dans l’outil Elements
    :::image-end:::

1.  Sélectionnez **l’onglet Styles.**  L’élément sélectionné possède un état dans le CSS qui lui est appliqué, mais qui n’est pas visible dans le `a` `hover` volet **Styles.** 

1.  Dans le **volet Styles,** à droite de la règle de `#sidebar nav li a` style, sélectionnez le `styles.css` lien.  **L’outil Sources** s’ouvre.  Recherchez ensuite la règle de pseudo-classe CSS `#sidebar nav li a:hover` .  Cette règle ne s’exécute pas lorsque **l’outil Inspect** est actif.  Nous allons simuler l’exécution de cette règle d’état dans les étapes suivantes.

1.  Sélectionnez **l’outil Éléments.**  Ensuite, dans **le volet Styles,** sélectionnez le bouton **:hov** (**Toggle Element State**).  Le **groupe d’états d’élément Force** des case à cocher s’affiche.

    :::image type="complex" source="../media/a11y-testing-state-simulation.msft.png" alt-text="Outil de simulation d’état affichant toutes les options" lightbox="../media/a11y-testing-state-simulation.msft.png":::
        Outil de simulation d’état affichant toutes les options
    :::image-end:::

1.  **Cochez la case :hover.**  Dans le DOM, à gauche de l’élément, un point jaune s’affiche, indiquant que l’élément `<a href="#cats">Cats</a>` a un état simulé.  **L’élément** de menu Chats apparaît maintenant dans la page web comme si le pointeur pointait sur celui-ci.  L’animation sur l’élément de menu peut s’exécuter.

    :::image type="complex" source="../media/a11y-testing-hover-simulated.msft.png" alt-text="DevTools simulant un état de pointage" lightbox="../media/a11y-testing-hover-simulated.msft.png":::
        DevTools simulant un état de pointage
    :::image-end:::

    Une fois l’état simulé appliqué, vous pouvez à nouveau utiliser l’outil **Inspect** pour vérifier le contraste de l’élément lorsque l’utilisateur passe dessus, comme suit.

1.  Sélectionnez **le bouton Inspect** \( Inspector icon \) dans le coin supérieur gauche de ![ DevTools afin que l’icône soit en surbrillant ](../media/inspect-icon.msft.png) (bleu).

1.  Pointez sur le lien **chats** bleus dans le menu de navigation de la barre latérale.  Le lien est désormais bleu clair, en raison de l’animation de pointation simulée.  La **superposition** des informations de l’outil Inspect s’affiche, affichant un point d’exclamation orange dans la ligne **Contraste,** indiquant que le contraste n’est pas assez élevé.

    :::image type="complex" source="../media/a11y-testing-hover-contrast-testing.msft.png" alt-text="Test du contraste d’un élément dans un état de pointer simulé" lightbox="../media/a11y-testing-hover-contrast-testing.msft.png":::
        Test du contraste d’un élément dans un état de pointer simulé
    :::image-end:::

La simulation d’état est également un bon moyen de vérifier si vous avez pris en compte différents besoins des utilisateurs, tels que les besoins des utilisateurs du clavier.  En utilisant les case à cocher d’état de l’élément **Force,** vous pouvez simuler l’état pour découvrir que l’interface utilisateur reste inchangée `:focus` lorsqu’elle a le focus. Cette absence d’indicateur lorsqu’un élément a le focus est un problème.


## <a name="see-also"></a>Articles associés

*  [Vue d’ensemble des tests d’accessibilité à l’aide de DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
