---
description: Vérification de l’arborescence d’accessibilité pour la prise en charge du clavier et du lecteur d’écran.
title: Vérifier l’arborescence d’accessibilité pour la prise en charge du clavier et du lecteur d’écran
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 0ab5e5609485505d1ad5fa6e2fffced9af25edcb
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597381"
---
# <a name="check-the-accessibility-tree-for-keyboard-and-screen-reader-support"></a>Vérifier l’arborescence d’accessibilité pour la prise en charge du clavier et du lecteur d’écran

<!-- Accessibility tab: Accessibility Tree -->

Plusieurs fonctionnalités DevTools vérifient la prise en charge du clavier et du lecteur d’écran.  **L’utilisation de l’outil Inspect** pour vérifier l’accessibilité de chaque élément de page individuellement peut prendre beaucoup de temps.  Une autre façon de vérifier une page web consiste à utiliser **l’arborescence d’accessibilité.**  **L’arborescence d’accessibilité** indique les informations que la page fournit aux technologies d’assistance telles que les lecteurs d’écran.

**L’arborescence** d’accessibilité est un sous-ensemble de l’arborescence DOM, qui contient des éléments de l’arborescence DOM pertinents et utiles pour l’affichage du contenu d’une page dans un lecteur d’écran.  **L’arborescence de l’accessibilité** se trouve dans **l’onglet** Accessibilité de l’outil **Éléments** (près de l’onglet **Styles).**


Pour explorer l’utilisation de l’arborescence d’accessibilité avec la page de démonstration :

1.  Ouvrez la [page web de démonstration des tests d’accessibilité][DevToolsA11yErrorsDemopage] dans un nouvel onglet.  Sélectionnez **ensuite F12** pour ouvrir DevTools.

1.  Sélectionnez **le bouton Inspect** \( l’icône Inspect \) dans le coin supérieur gauche de ![ DevTools afin que le bouton soit mis en surbrillant ](../media/inspect-icon.msft.png) (bleu).

1.  Dans la page web rendue, dans la section **Donation,** pointez sur le **bouton 100.**  La **superposition de** l’outil Inspect s’affiche.

1.  Dans la page web rendue, sélectionnez le **bouton 100.**  Dans DevTools, l’outil **Elements** s’affiche.  L’arborescence DOM affiche `div` l’élément du **bouton 100.**  Le **volet Styles** affiche les paramètres CSS de l’élément.

1.  À droite de l’onglet **Styles,** sélectionnez **l’onglet** Accessibilité.  **L’arborescence d’accessibilité** de l’élément s’affiche et est étendue.

:::image type="complex" source="../media/a11y-testing-accessibility-tree.msft.png" alt-text="Bouton Du formulaire de don dans l’outil Arborescence de l’accessibilité" lightbox="../media/a11y-testing-accessibility-tree.msft.png":::
    Bouton Du formulaire de don dans l’outil Arborescence de l’accessibilité
:::image-end:::

Tout élément dans l’arborescence qui n’a pas de nom ou qui a un rôle (tel que l’élément) est un problème, car cet élément n’est pas disponible pour les utilisateurs du clavier ou pour les utilisateurs qui utilisent la technologie `generic` `div` d’assistance.


## <a name="see-also"></a>Articles associés

*  [Afficher la position d’un élément dans l’arborescence d’accessibilité][DevtoolsAccessibilityAccessibilityTabViewTree]
*  [Vue d’ensemble des tests d’accessibilité à l’aide de DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevtoolsAccessibilityAccessibilityTabViewTree]: accessibility-tab.md#view-the-position-of-an-element-in-the-accessibility-tree "Afficher la position d’un élément dans l’arborescence d’accessibilité - Tester l’accessibilité à l’aide de l’onglet Accessibilité | Documents Microsoft"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
