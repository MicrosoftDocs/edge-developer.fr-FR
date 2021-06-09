---
description: Analyse de l’absence d’indication du focus du clavier dans un menu de barre latérale, en raison de l’absence d’une règle de pseudo-classe CSS pour l’état de mise au point sur un lien, combinée avec le lien n’ayant pas de paramètre de plan.
title: Analyser l’absence d’indication du focus du clavier dans un menu de barre latérale
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 3626de9bdc2cce266efafe4b1b2e8fff501a74f7
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597380"
---
# <a name="analyze-the-lack-of-indication-of-keyboard-focus-in-a-sidebar-menu"></a>Analyser l’absence d’indication du focus du clavier dans un menu de barre latérale

<!-- Inspect tool, and CSS rules: pseudo-classes for states -->

Dans la page de démonstration des tests d’accessibilité, le menu de navigation de la barre latérale avec des liens bleus n’indique pas visuellement quel lien a le focus, lors de l’utilisation d’un clavier.  Pour savoir pourquoi le menu de la barre latérale est déroutant pour les utilisateurs du clavier, nous allons rechercher des règles de pseudo-classe CSS pour les états et les états, ainsi que la propriété CSS pour les contours des `hover` `focus` liens.  

Cette analyse trouve que l’absence d’indication du focus du clavier dans les liens du menu de navigation de la barre latérale est dû aux éléments suivants :
*  Les `a` liens ont un paramètre de propriété CSS de `outline: none` .
*  Les `a` liens ne disposent pas d’une règle de pseudo-classe CSS pour l’état. `:focus`

Pour accéder au CSS, nous allons utiliser l’outil **Inspect** pour mettre en évidence un lien bleu dans le menu de navigation de la barre latérale, puis afficher l’arborescence DOM et CSS pour l’élément qui définit ce `a` lien.

1.  Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.

1.  Sélectionnez **le bouton Inspect** \( Inspect icon \) dans le coin supérieur gauche de DevTools afin que le bouton soit mis en ![ ](../media/inspect-icon.msft.png) surbrillant (bleu).

1.  Pointez sur le lien **chats** bleus dans le menu de navigation de la barre latérale.  La superposition Inspect s’affiche, montrant que l’élément est `a` focusable au clavier.  Mais la superposition ne montre pas qu’il n’y a aucune indication visuelle lorsque le lien a le focus.

    Ensuite, nous allons examiner le style CSS de ce lien.
 
1.  Sélectionnez **le lien Chats** dans le menu de navigation de la barre latérale.  **L’outil Inspect** s’éteint et l’outil **Elements** s’ouvre, mettant en surbrillance le nœud dans `a` l’arborescence DOM.

1.  Sélectionnez **l’onglet Styles.**  La règle CSS apparaît, ainsi qu’un lien `#sidebar nav li a` vers un numéro de ligne dans `styles.css` .

    :::image type="complex" source="../media/a11y-testing-menu-link.msft.png" alt-text="Inspection du code source et des styles appliqués d’un lien dans le menu" lightbox="../media/a11y-testing-menu-link.msft.png":::
        Inspection du code source et des styles appliqués d’un lien dans le menu
    :::image-end:::
    
1.  Sélectionnez le lien vers le fichier CSS.  Le fichier CSS s’ouvre dans l’outil **Sources.**

    :::image type="complex" source="../media/a11y-testing-menu-link-styles.msft.png" alt-text="Styles appliqués au lien dans l’outil Sources" lightbox="../media/a11y-testing-menu-link-styles.msft.png":::
        Styles appliqués au lien dans l’outil Sources
    :::image-end:::
    
Les styles de la page ont une règle de pseudo-classe CSS pour l’état qui indique l’élément de menu que vous utilisez lorsque vous utilisez `hover` une souris : `#sidebar nav li a:hover` .  Toutefois, il n’existe aucune règle de pseudo-classe CSS pour que l’état indique visuellement l’élément de menu sur lequel vous vous trouvez lorsque vous utilisez un `focus` clavier, tel que `#sidebar nav li a:focus` .

Notez également que les liens ont un paramètre de propriété CSS de `outline: none` .  Il s’agit d’une pratique courante qui consiste à supprimer le plan que les navigateurs ajoutent automatiquement aux éléments lorsque vous vous concentrez sur eux à l’aide d’un clavier.  Le fait de ne pas `focus` utiliser de style crée de la confusion pour vos utilisateurs.


## <a name="see-also"></a>Articles associés 

*  [Effectuer le suivi de l’élément actif](focus.md)
*  [Vue d’ensemble des tests d’accessibilité à l’aide de DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
