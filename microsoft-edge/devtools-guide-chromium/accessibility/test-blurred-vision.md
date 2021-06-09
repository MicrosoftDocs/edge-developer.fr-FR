---
description: Pour vérifier qu’une page web est utilisable avec une vision floue, dans l’outil de rendu, utilisez la liste de listes de listes des défaillances de vision Émuler.
title: Vérifier que la page est utilisable avec une vision floue
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 2fc1a1cf7746591573fce07946c7fb11abf42705
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597369"
---
# <a name="verify-that-the-page-is-usable-with-blurred-vision"></a>Vérifier que la page est utilisable avec une vision floue

<!-- Rendering tool: Emulate vision deficiencies: Blurred vision -->

Pour simuler une vision floue, dans l’outil **de** rendu, utilisez le menu Émuler les **faiblesses de la** vision.  Lorsque vous utilisez cette fonctionnalité avec la page web de démonstration, vous pouvez voir que l’ombre portée du texte dans le menu supérieur complique la lecture des éléments de menu.

Pour vérifier si une page web est utilisable avec une vision floue :

1.  Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.

1.  Sélectionnez **Échap** pour ouvrir le caisse en bas de DevTools.  Sélectionnez l’icône en haut du caisse pour afficher la liste des outils, puis **+** sélectionnez **Rendu.**  

1.  Dans la liste liste de listes des **défaillances** de vision Émuler, **sélectionnez Vision floue.**

    :::image type="complex" source="../media/a11y-testing-simulating-blur.msft.png" alt-text="Simulation d’une page floue" lightbox="../media/a11y-testing-simulating-blur.msft.png":::
        Simulation d’une page floue
    :::image-end:::

    Notez que la propriété CSS complique la lecture du texte des éléments `text-shadow` de menu dans le menu supérieur. Par exemple, examinez **la page d’accueil**, **Adopter un**enfant de compagnie et d’autres éléments de menu.
    
1.  Dans **l’outil de** rendu, dans Émuler les **défaillances visuelles,** sélectionnez Aucune **émulation** pour supprimer la simulation de vision floue.


## <a name="see-also"></a>Articles associés

*  [Émuler les faiblesses de la vision](emulate-vision-deficiencies.md)
*  [Vue d’ensemble des tests d’accessibilité à l’aide de DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
