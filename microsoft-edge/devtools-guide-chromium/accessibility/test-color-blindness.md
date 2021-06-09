---
description: Vérifiez que les pages web sont utilisables par les personnes daltonies à l’aide de la liste liste de listes de listes listes des émuler les faiblesses de vision dans l’outil de rendu.
title: Vérifier que la page est utilisable par les personnes daltonismes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 54cd7230f0402bfeb4b5ee28d2bcd0947794676f
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597367"
---
# <a name="verify-that-the-page-is-usable-by-people-with-color-blindness"></a>Vérifier que la page est utilisable par les personnes daltonismes

<!-- Rendering tool: Emulate vision deficiencies: Protanopia -->

Pour vérifier qu’une page web est utilisable par **** des personnes daltonies, dans l’outil de rendu, utilisez la liste liste de listes des problèmes de **vision** émuler.

Sur la page web de démonstration des tests d’accessibilité, les différents états de don utilisent la couleur comme seul moyen de différenciation.
*  Vert signifie qu’un montant élevé de dons a été reçu.
*  Le jaune signifie qu’un montant moyen de dons a été reçu.
*  Le rouge signifie qu’un faible montant de dons a été reçu.

Mais vous ne pouvez pas vous attendre à ce que tous vos utilisateurs utilisent ces couleurs comme prévu.  En utilisant la fonctionnalité Émuler **** les défauts de **vision** de l’outil de rendu, vous pouvez découvrir que cette conception n’est pas suffisamment bonne, en simulant la façon dont les personnes ayant une vision différente persoraient votre conception.


Pour vérifier si une page web est utilisable par des personnes daltonisme :

1.  Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.

1.  Sélectionnez **Échap** pour ouvrir le caisse en bas de DevTools.  Sélectionnez l’icône en haut du caisse pour voir la liste des outils, puis **+** sélectionnez **Rendu.**  

1.  Dans la liste liste de listes des **défaillances** de vision Émuler, sélectionnez **Protanopia**.  _La protanopie_ est une réduction de la sensibilité à la lumière rouge, ce qui rend difficile la différenciation du vert, du rouge et du jaune.

    :::image type="complex" source="../media/a11y-testing-simulating-protanopia.msft.png" alt-text="Affichage du document comme une personne avec une protanopie le verra" lightbox="../media/a11y-testing-simulating-protanopia.msft.png":::
        Affichage du document comme une personne avec une protanopie le verra
    :::image-end:::
    
1.  Dans **l’outil de** rendu, sous Émuler les **défaillances visuelles,** sélectionnez Aucune **émulation** pour supprimer la simulation.


## <a name="see-also"></a>Articles associés

*  [Émuler][DevToolsVisionDeficiencies] les défaillances visuelles : définit les éléments de la liste de listes de défaillances de **vision** Émuler, y compris Protanopia, Deuteranopia, Tritanopia et Achromatopsia.
*  [Vue d’ensemble des tests d’accessibilité à l’aide de DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsVisionDeficiencies]: ./emulate-vision-deficiencies.md "Émuler les défaillances visuelles | Documents Microsoft"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
