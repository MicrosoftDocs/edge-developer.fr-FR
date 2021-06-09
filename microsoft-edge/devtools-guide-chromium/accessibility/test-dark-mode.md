---
description: Recherchez les problèmes de contraste avec le thème foncé et le thème clair (pour le mode sombre et le mode clair) à l’aide de la liste de listes de listes listes dans l’outil de rendu « Émuler la fonctionnalité multimédia CSS prefers-color-scheme\ ».
title: Vérifier les problèmes de contraste avec le thème foncé et le thème clair
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 052c75b610ec872329f387e46819867f299a8ca9
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597366"
---
# <a name="check-for-contrast-issues-with-dark-theme-and-light-theme"></a>Vérifier les problèmes de contraste avec le thème foncé et le thème clair

<!-- Rendering tool: Emulate CSS media feature prefers-color-scheme -->

Lorsque vous testez l’accessibilité des couleurs, il peut y avoir différents thèmes de couleur d’affichage que vous devez tester pour les problèmes de contraste.

La plupart des systèmes d’exploitation sont en mode sombre et clair.  Votre page web peut réagir à ce paramètre de système d’exploitation à l’aide d’une requête multimédia CSS.  Vous pouvez tester ces thèmes et tester votre requête multimédia CSS sans avoir à modifier le paramètre de votre système d’exploitation, à l’aide des options CSS de l’outil `prefers-color-scheme` **de** rendu.

Par exemple, la page de démonstration des tests d’accessibilité inclut un thème clair et un thème foncé.  La page de démonstration hérite du paramètre de thème foncé ou clair du système d’exploitation.  Si nous utilisons DevTools pour simuler la mise en place d’un **** schéma lumineux pour le système d’exploitation, puis actualiser la page web de démonstration, l’outil Problèmes montre six problèmes de contraste de couleur au lieu de deux.  (Vous pouvez voir des nombres différents.)


Pour émuler la sélection d’un thème de couleur préféré par un utilisateur :

1.  Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.

1.  Sélectionnez **Échap** pour ouvrir le caisse en bas de DevTools.  Sélectionnez l’icône en haut du caisse pour voir la liste des outils, puis **+** sélectionnez **Rendu.**  L’outil de rendu s’affiche.

1.  Dans la **fonctionnalité émuler CSS media prefers-color-scheme** dropdown list, select **prefers-color-scheme: light**.      La page web est restituer à l’aide `light-theme.css` de .


    :::image type="complex" source="../media/a11y-testing-simulating-light-mode.msft.png" alt-text="Utilisation de l’outil de rendu pour simuler un mode clair et déclencher l’autre thème du document" lightbox="../media/a11y-testing-simulating-light-mode.msft.png":::
        Utilisation de l’outil de rendu pour simuler un mode clair et déclencher l’autre thème du document
    :::image-end:::


1.  Sélectionnez **l’outil Problèmes,** puis développez la section **Accessibilité.**  En fonction de différents facteurs, vous pouvez obtenir `Insufficient color contrast` des avertissements. Notez que **dans RESSOURCES AFFECTÉEs,** il existe 6 éléments avec un contraste de couleur insuffisant.
    
    :::image type="complex" source="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png" alt-text="Nouveaux problèmes de contraste détectés en raison de la modification du thème clair" lightbox="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png":::
        Nouveaux problèmes de contraste détectés en raison de la modification du thème clair
    :::image-end:::
    
    Dans notre page de démonstration, la section **Sur** l’état du don de la page est illisible en mode clair et doit changer. 
    
    :::image type="complex" source="../media/a11y-testing-donation-state-light-contrast.msft.png" alt-text="La section État du don présente des problèmes de contraste en mode clair" lightbox="../media/a11y-testing-donation-state-light-contrast.msft.png":::
        La section **État du** don présente des problèmes de contraste en mode clair
    :::image-end:::
    
1.  Dans DevTools, sélectionnez l’outil **Elements,** puis **Ctrl+F** sur Windows/Linux ou **Command+F** sur macOS.  La **zone de** texte Rechercher s’affiche pour effectuer une recherche dans l’arborescence DOM HTML.
 
1.  Entrez `scheme` .  Les requêtes multimédias CSS suivantes sont trouvées et les fichiers CSS correspondants peuvent maintenant être mis à jour.

    ```html
    <link rel="stylesheet" href="css/light-theme.css" media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)">
    <link rel="stylesheet" href="css/dark-theme.css" media="(prefers-color-scheme: dark)">
    ```


## <a name="see-also"></a>Articles associés

*  [Simulation de jeu de couleurs sombres ou claires][DevToolsColorSchemeSimulation]
*  [Vue d’ensemble des tests d’accessibilité à l’aide de DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsColorSchemeSimulation]: ./preferred-color-scheme-simulation.md "Modèle de simulation de jeu de couleurs sombres ou claires | Documents Microsoft"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
