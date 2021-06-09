---
description: Vérifiez que les pages web sont utilisables avec l’animation de l’interface utilisateur désactivée (mouvement réduit) à l’aide de la fonctionnalité multimédia Émuler CSS préférant une liste de listes de déplacement avec mouvement réduit dans l’outil de rendu.
title: Vérifier que la page est utilisable avec l’animation de l’interface utilisateur désactivée
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: ec30925b706b4b1c6dfaaa6ce66a38fab8759ac2
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597333"
---
# <a name="verify-that-the-page-is-usable-with-ui-animation-turned-off"></a>Vérifier que la page est utilisable avec l’animation de l’interface utilisateur désactivée

Une page web ne doit pas afficher d’animations pour un utilisateur qui a désactivé les animations dans le système d’exploitation.  Les animations peuvent faciliter l’utilisation d’un produit, mais elles peuvent également provoquer une distraction, une confusion ou une confusion.

Pour vérifier qu’une page web est utilisable avec l’animation **** de l’interface utilisateur désactivée (mouvement réduit), dans l’outil de rendu, utilisez la fonctionnalité émuler la fonctionnalité multimédia **CSS** préférant la liste de listes de présentation à mouvement réduit.

Dans la page web de démonstration des tests d’accessibilité, lorsque vous désélectez les animations dans le système d’exploitation ou émulez ces paramètres à l’aide de DevTools, la page web n’utilise pas le défilement fluide lorsque vous sélectionnez les liens du menu de navigation de la barre latérale.  Pour ce faire, vous pouvez ingériser le paramètre de défilement **** fluide dans CSS dans une requête multimédia, puis utiliser l’outil de rendu pour émuler le paramètre du système d’exploitation pour réduire l’animation.

Pour vérifier si la page est utilisable avec des animations désactivées :

1.  Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.

1.  En haut de DevTools, sélectionnez l’outil **Sources,** puis, dans le volet de **navigation** à gauche, sélectionnez `styles.css` .  Le fichier CSS apparaît dans **le** volet Éditeur.

1.  Sélectionnez **Ctrl+F** sur Windows/Linux ou **Command+F** sur macOS, puis entrez `@media` .  La requête multimédia CSS suivante s’affiche, ce qui confirme qu’elle est utilisée sur la page web.

    ```css
    @media (prefers-reduced-motion: no-preference) {
      html {
        scroll-behavior: smooth;
      }
    }
    ```

    Ensuite, émulez le paramètre du système d’exploitation pour réduire l’animation, comme suit.

1.  Sélectionnez **Échap** pour ouvrir le caisse en bas de DevTools.  Sélectionnez **le bouton Plus d’outils** () en haut du caisse pour voir la liste des outils, puis **+** sélectionnez **Rendu.**  

1.  Dans la **fonctionnalité émuler le support CSS préférant la** liste de listes de déplacement à mouvement réduit, sélectionnez **prefers-reduced-motion: reduced**.

    :::image type="complex" source="../media/a11y-testing-simulating-reduced-motion.msft.png" alt-text="Simulation d’un mouvement réduit et du CSS qui permet de s’assurer que le défilement fluide se produit uniquement lorsque l’utilisateur le souhaite" lightbox="../media/a11y-testing-simulating-reduced-motion.msft.png":::
        Simulation d’un mouvement réduit et du CSS qui permet de s’assurer que le défilement fluide se produit uniquement lorsque l’utilisateur le souhaite
    :::image-end:::

1.  Dans la page web, sélectionnez les éléments de menu bleu, tels que **La maison ou** les **espaces.**  À présent, la page web défile instantanément jusqu’à la section sélectionnée, au lieu d’utiliser l’animation à défilement fluide.

1.  Dans **l’outil de** rendu, sous Émuler la fonctionnalité multimédia **CSS préférer le**mouvement réduit, sélectionnez Aucune **émulation** pour supprimer ce paramètre.
   
Notez que la page web de démonstration exécute toujours les animations suivantes, même avec les paramètres de requête et d’émulation multimédia ci-dessus. Lorsque vous construisez votre produit web, veillez à corriger toutes les animations similaires.  
*  Animation des éléments de menu bleu lorsque vous pointez dessus.
*  Animation des cercles sur les **liens Plus** lorsque vous pointez dessus.



## <a name="see-also"></a>Articles associés

*  [Simulation de mouvement réduit](reduced-motion-simulation.md)
*  [Vue d’ensemble des tests d’accessibilité à l’aide de DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
